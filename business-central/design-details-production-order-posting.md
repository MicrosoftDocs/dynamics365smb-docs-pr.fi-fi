---
title: Rakennetiedot – Tuotantotilauksen kirjaus | Microsoft Docs
description: Samoin kuin kokoonpanotilauksen tiliöinti, käytetyt osat ja käytetty koneaika muunnetaan ja tuotetaan tuotettuna nimikkeenä, kun tuotantotilaus on valmis.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 21dfc90e25c33c26bc739ff32274d0a5088a6e2f
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8146564"
---
# <a name="design-details-production-order-posting"></a>Rakennetiedot: tuotantotilauksen kirjaus
Kokoonpanotilauksen kirjauksen tavoin kulutetut komponentit ja käytetty koneaika muunnetaan ja tuotetaan tuotettuna nimikkeenä, kun tuotantotilaus on valmis. Lisätietoja on kohdassa [Rakennetiedot: Kokoonpanotilauksen kirjaus](design-details-assembly-order-posting.md). Kokoonpanotilausten kustannusvirta on kuitenkin yksinkertaisempi erityisesti sen vuoksi, että kokoonpanokustannuksen kirjaus tapahtuu vain kerran, joten se ei luo keskeneräisten töiden varastoa.


Valmistusprosessin aikaiset tapahtumat voidaan jäljittää seuraavien vaiheiden avulla:  

1.  Materiaalien ja muiden tuotannon syötteiden osto.  
2.  Muunto keskeneräiseksi työksi.  
3.  Muunto valmiiden tuotteiden varastoksi.  
4.  Valmiiden tavaroiden myynti.  

Tämän vuoksi tuotantoyrityksen on muodostettava tavallisten varastotilien lisäksi kolme erillistä varastotiliä, jotka tallentavat tapahtumat tuotannon eri vaiheissa.  

|Varastotili|Description|  
|-----------------------|---------------------------------------|  
|**Raaka-aine-tili**|Sisältää raaka-aineiden kustannukset, jotka on ostettu mutta joita ei ole vielä siirretty tuotantoon. Raakamateriaalien tilin balanssi ilmaisee käytettävissä olevia raakamateriaalien kustannuksia.<br /><br /> Kun raaka-aineita siirretään tuotanto-osastoon, materiaalikustannukset siirretään raaka-aineiden tililtä KET-tilille.|  
|**Keskeneräinen työ -tili**|Kerää kustannukset, jotka aiheutuvat tuotannon aikana tilikaudella. KET-tililtä veloitetaan niiden raaka-aineiden kustannukset, jotka siirretään raaka-aineiden fyysisestä varastosta, suoritetun välittömän työn kustannuksista ja valmistuksen aiheutuneista yleiskustannuksista.<br /><br /> KET-tilille hyvitetään niiden yksiköiden valmistuskustannukset, jotka valmistetaan tehtaassa ja siirretään valmiiden tuotteiden fyysiseen varastoon.|  
|**Valmis tavaratili**|Tämä tili sisältää niiden yksiköiden kaikki valmistuskustannukset, jotka on tehty valmiiksi, mutta joita ei ole vielä myyty. Myyntihetkellä myytyjen yksiköiden kustannukset siirretään Valmiit tuotteet -tililtä Myytyjen tuotteiden kustannukset -tilille.|  

Varaston arvo lasketaan seuraamalla kaikkia kustannusten nousuja ja laskuja seuraavassa yhtälössä ilmaistulla tavalla:  

* varaston arvo = varaston alkusaldo + kaikkien nousujen arvo - kaikkien vähennysten arvo  

Varaston tyypistä riippuen lisäykset ja vähennykset esitetään eri tapahtumilla.  

||Lisäykset|Vähennykset|  
|-|---------------|---------------|  
|**Raaka-ainevarasto**|-   Materiaalin netto-ostot<br />-   Osakokoonpanojen tuotos<br />-   Negatiivinen kulutus|Materiaalin kulutus|  
|**KET-varasto**|-   Materiaalin kulutus<br />-   Kapasiteetin kulutus<br />-   Tuotannon yleiskustannus|Loppunimikkeiden tuotos (valmistettujen tuotteiden kustannukset)|  
|**Valmiiden tuotteiden varasto**|Loppunimikkeiden tuotos (valmistettujen tuotteiden kustannukset)|-   Myynti (myytyjen tuotteiden kustannukset)<br />-   Negatiivinen tuotos|  
|**Raaka-ainevarasto**|-   Materiaalin netto-ostot<br />-   Osakokoonpanojen tuotos<br />-   Negatiivinen kulutus|Materiaalin kulutus|  

Erityyppisten valmistettujen varastojen arvonnousujen ja -laskujen arvot tallennetaan samalla tavalla kuin ostetun varaston arvot. Jokaisen varaston lisäyksen tai vähennyksen yhteydessä summalle luodaan nimiketapahtuma ja vastaava pääkirjanpidon tapahtuma. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Varaston kirjaus](design-details-inventory-posting.md).  

Vaikka niiden tapahtumien arvot, jotka liittyvät arvot ostettuihin tavaroihin kirjataan vain nimiketapahtumiksi vastaavilla arvotapahtumilla, tuotettuihin nimikkeisiin liittyvät tapahtumat kirjataan kapasiteettitapahtumiksi vastaavilla arvotapahtumilla nimiketapahtumien lisäksi.  

## <a name="posting-structure"></a>Kirjausrakenne  
tuotantotilausten kirjaaminen KET-varastoon sisältää tuotoksen, kulutuksen ja kapasiteetin.  

Seuraavassa kaaviossa esitetään asiaankuuluvat tiliöintirutiinit koodiyksikössä 22.  

![Tuotantotilausten kirjausrutiinit.](media/design_details_inventory_costing_14_production_posting_1.png "Tuotantotilausten kirjausrutiinit")  

Seuraavassa kaaviossa esitetään seurauksena olevien kirjausten ja kustannusobjektien assosiaatiot.  

![Tuotannon tapahtumavuo.](media/design_details_inventory_costing_14_production_posting_2.png "Tuotannon tapahtumavuo")  

Kapasiteettilokin kirjaus kuvaa kapasiteetin kulutuksen aikayksikköinä, kun taas liittyvä arvokirjaus kuvaa erityisen kapasiteetin kulutuksen arvon.  

Nimikkeen pääkirjan kirjaus kuvaa materiaalin kulutuksen tai tuotannon määrän yksikköinä, kun taas liittyvä arvokirjaus kuvaa tämän erityisen materiaalin kulutuksen tai tuotannon arvon.  

KET-varastoarvoa kuvaava arvotapahtuma voidaan liittää yhteen seuraavista kustannuskohteiden yhdistelmistä:  

-   Tuotantotilausrivi, tuotantosolu tai kuormitusryhmä ja kapasiteettitapahtuma.  
-   Tuotantotilauksen rivi, nimike ja nimiketapahtuma.  
-   Vain tuotantotilauksen rivi  

Lisätietoja tuotannon ja kokoonpanon kustannusten kirjaamisesta pääkirjanpitoon on kohdassa [Rakennetiedot: Varastokirjaus](design-details-inventory-posting.md).  

## <a name="capacity-posting"></a>Kapasiteetin kirjaus  
Viimeisen tuotantotilauksen reititysrivin tuotoksen kirjaaminen aiheuttaa kapasiteettitapahtuman loppunimikkeelle, sen varastoarvon kasvun lisäksi.  

 Kapasiteettilokin kirjaus on sen ajan tallenne, joka on kulutettu nimikkeen tuottamiseen. Liittyvä arvokirjaus kuvaa WIP-varastoarvon kasvun, joka on siirtymiskustannusten arvo. Lisätietoja on ohjeaiheen [Rakennetiedot: Pääkirjanpidon tilit](design-details-accounts-in-the-general-ledger.md) kohdassa Kapasiteettitapahtumista.  

## <a name="production-order-costing"></a>Tuotantotilauksen arvostus  
 Tuotantoyrityksen on mitattava tuotantotilausten kustannukset varasto- ja tuotantokustannusten valvontaa varten, koska jokaisen tuotetun nimikkeen ennalta määritetyt vakiokustannukset aktivoidaan taseessa. Lisätietoja syistä, joiden vuoksi tuotetut nimikkeet käyttävät vakioarvostusmenetelmää on kohdassa [Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md).  

> [!NOTE]  
>  Ympäristöissä, joissa ei käytetä vakioarvostusmenetelmää, taseeseen siirretään tuotettujen nimikkeiden todellinen kustannus vakiokustannuksen sijasta.  

Todelliset tuotantotilauksen kustannukset koostuvat seuraavista osista:  

-   Todelliset materiaalikustannukset  
-   Todellinen kapasiteettikustannus tai alihankkijan kustannus  
-   Tuotannon yleiskustannus  

Nämä todelliset kustannukset kirjataan tuotantotilaukseen. Niitä verrataan vakiokustannuksiin erojen laskemista varten. Varianssi lasketaan jokaiselle nimikekustannusten komponenteille: raaka-aineille, kapasiteetille, alihankkijalle, kapasiteetin yleiskustannuksille ja valmistajan yleiskustannuksille. Erojen analysoinnin avulla voidaan määrittää ongelmia, kuten prosessin aikana syntyvät liialliset jätemäärät.  

Vakiokustannusympäristöissä tuotantotilauksen arvostus perustuu seuraavaan mekanismiin:  

1.  Kun edellinen reititystoiminto on kirjattu, tuotantotilauksen kustannukset kirjataan nimiketapahtumaan ja määritetään oletetuiksi kustannuksiksi.  

    Tämä kustannus on sama kuin tuotospäiväkirjaan kirjattu tuotosmäärä kerrottuna nimikekortista kopioidulla vakiokustannuksella. Kustannusta käsitellään oletettuna kustannuksena, kunnes tuotantotilaus on valmis. Katso lisätietoja kohdasta [Rakennetiedot: oletetun kustannuksen kirjaus](design-details-expected-cost-posting.md).  

    > [!NOTE]  
    >  Tämä on erilainen kuin kokoonpanotilauksen kirjaus, jossa kirjataan aina toteutuneet kustannukset. Lisätietoja on kohdassa [Rakennetiedot: Kokoonpanotilauksen kirjaus](design-details-assembly-order-posting.md).  
2.  Kun tuotantotilauksen tilaksi on määritetty **Valmis**, tilaus laskutetaan suorittamalla **Muuta kustannuksia - Nimiketapahtumat** -eräajo. Tämän seurauksena tilauksen kokonaiskustannus lasketaan kulutettujen materiaalien ja kapasiteetin vakiokustannusten perusteella. Laskettujen vakiokustannusten ja toteutuneiden tuotantokustannusten väliset erot lasketaan ja kirjataan.  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
 [Rakennetiedot: Kokoonpanotilauksen kirjaus](design-details-assembly-order-posting.md)  
 [Varaston kustannusten hallinta](finance-manage-inventory-costs.md) [Rahoitus](finance.md)  
 [Business Centralin käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]