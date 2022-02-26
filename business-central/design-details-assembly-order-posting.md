---
title: Rakennetiedot – kokoonpanotilauksen kirjaus
description: Kokoonpanotilauksen kirjaus perustuu samoihin periaatteisiin kuin myyntitilausten ja tuotannon kulutuksen / tuotoksen kirjauksen vastaavat toiminnot.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 155fbf64c5ca0dcffce22f16f7ffbfc6375250f1
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442558"
---
# <a name="design-details-assembly-order-posting"></a>Rakennetiedot: kokoonpanotilauksen kirjaus
Kokoonpanotilauksen kirjaus perustuu samoihin periaatteisiin kuin myyntitilausten ja tuotannon kulutuksen / tuotoksen kirjauksen vastaavat toiminnot. Periaatteet on kuitenkin yhdistetty niin, että kokoonpanotilauksilla on omat kirjauksen käyttöliittymänsä, kuten myyntitilauksille on omansa ja todellinen tapahtuman kirjaus tapahtuu taustalla suorana nimikkeen ja resurssipäiväkirjan kirjauksena, kuten tuotannon kulutukselle, tuotokselle ja kapasiteetille.  

Samoin kuin tuotantotilauksen tiliöinti, käytetyt osat ja käytetyt resurssit muunnetaan ja tuotetaan kokoonpanonimikkeenä, kun kokoonpanotuotantotilaus on lähetetty. Katso lisätietoja kohdasta [Rakennetiedot: tuotantotilauksen kirjaus](design-details-production-order-posting.md). Kokoonpanotilausten kustannusvirta on kuitenkin yksinkertaisempi, erityisesti siksi, koska kokoonpanokustannuksen kirjaus tapahtuu vain kerran, ja tämän vuoksi se ei luo keskeneräisten töiden varastoa.  

Seuraavat lokitiliöinnit tapahtuvat kokoonpanotilauksen tiliöinnin aikana:  

-   Nimikkeen loki tiliöi positiiviset nimikkeen pääkirjan kirjaukset esittäen kokoonpano-osien tuotannon kokoonpanotilauksen otsikosta.  
-   Nimikkeen loki tiliöi negatiiviset nimikkeen pääkirjan kirjaukset esittäen kokoonpano-osien kulutuksen kokoonpanotilauksen riveiltä.  
-   Resurssiloki tiliöi kokoonpanoresurssien (aikayksiköt) käytön kokoonpanotilausriveiltä.  
-   Kapasiteettiloki tiliöi arvokirjaukset, jotka liittyvät resurssien käyttöön, kokoonpanotilauksen riveiltä.  

Seuraavassa kaaviossa esitetään nimikkeen ja lähteenä olevan pääkirjan kirjausten rakenne, jotka ovat seurausta kokoonpanotilauksen tiliöinnistä.  

![Kokoonpanotilauksen kirjaamisesta johtuvat nimike-, resurssi-ja kapasiteettitapahtumat.](media/design_details_assembly_posting_1.png "Kokoonpanotilauksen kirjaamisesta johtuvat nimike-, resurssi-ja kapasiteettitapahtumat")  

> [!NOTE]  
>  Kuormitusryhmät ja tuotantosolut on sisällytetty sen kuvaamiseksi, että kapasiteettitapahtumat luodaan sekä tuotannosta että kokoonpanosta.  

Seuraavassa kaaviossa esitetään, kuinka kokoonpanotiedot kulkevat pääkirjaan tiliöinnin aikana:  

![Kokoonpanoon liittyvien tapahtumien työnkulku kirjauksen aikana.](media/design_details_assembly_posting_2.png "Kokoonpanoon liittyvien tapahtumien työnkulku kirjauksen aikana")  

## <a name="posting-sequence"></a>Järjestyksen kirjaaminen  
Kokoonpanotilauksen tiliöinti tapahtuu seuraavassa järjestyksessä:  

1.  Kokoonpanotilauksen rivit on kirjattu.  
2.  Kokoonpanotilauksen otsikko on kirjattu.  

Seuraava taulukko luonnostelee toimintasarjat.  

|Toiminto|Description|  
|------------|-----------------|  
|Alusta kirjaus|1.  Suorita alustavat tarkastukset.<br />2.  Lisää kirjausnumero ja muokkaa kokoonpanotilauksen otsikkoa.<br />3.  Vapauta kokoonpanotilaus.|  
|Kirjaus|<ol><li>Luo kirjatun kokoonpanotilauksen otsikko.</li><li>Kopioi kommenttirivit.</li><li>Kirjaa kokoonpanotilauksen rivit (kulutus):<br /><br /> <ol><li>Luo tilasivu kokoonpanon kulutuksen laskemiseksi.</li><li>Nouda jäljellä oleva määrä, jota käytetään nimikepäiväkirjarivin perustana.</li><li>Tyhjennä käytetyt määrät ja jäljellä olevat määrät.</li><li>Nimike-tyypin kokoonpanotilaus-rivit:<br /><br /> <ol><li>Täytä kunkin päiväkirjarivin kentät.</li><li>Siirrä varaukset nimikepäivän kirjariville.</li><li>Kirjaa nimikepäiväkirjarivi luodaksesi nimiketapahtumat.</li><li>Luo fyysisen varastoinnin päiväkirjarivit ja kirjaa ne.</li></ol></li><li>Resurssi-tyypin kokoonpanotilaus-rivit:<br /><br /> <ol><li>Täytä kunkin päiväkirjarivin kentät.</li><li>Kirjaa nimikepäiväkirjarivi. Tämä luo kapasiteettitapahtumat.</li><li>Luo ja kirjaa resurssipäiväkirjan rivi.</li></ol></li><li>Siirrä kentän arvot kokoonpanotilausriviltä juuri luodulle ja kirjatulle kokoonpanoriville.</li></ol></li><li>Kirjaa kokoonpanotilauksen otsikko (tuotos):<br /><br /> <ol><li>Täytä kunkin päiväkirjarivin kentät.</li><li>Siirrä varaukset nimikepäivän kirjariville.</li><li>Kirjaa nimikepäiväkirjarivi luodaksesi nimiketapahtumat.</li><li>Luo fyysisen varastoinnin päiväkirjarivit ja kirjaa ne.</li><li>Tyhjennä kokoonpanomäärät ja jäljellä olevat määrät.</li></ol></li></ol>|  

> [!IMPORTANT]  
>  Kokoonpanon tuotos kirjataan todellisena kustannuksena, toisin kuin tuotannon tuotos, joka kirjataan oletettuna kustannuksena.  

## <a name="cost-adjustment"></a>Kustannusten muuttaminen  
 Kun kokoonpanotilaus kirjataan, joka tarkoittaa sitä, että komponentit (materiaali) ja resurssit kootaan uudeksi nimikkeeksi, tämän kokoonpanon nimikkeen todellisen kustannuksen ja mukana olevien komponenttien todellisen varastokustannuksen määrittämisen tulisi olla mahdollista. Tämä saavutetaan siirtämällä kustannukset lähteen (komponentit ja resurssit) kirjatuista tapahtumista kohteen (kokoonpanonimike) kirjattuihin tapahtumiin. Kustannusten vienti eteenpäin tehdään laskemassa ja luomalla uudet kirjaukset nimeltä oikaisukirjaukset, jotka tulevat liittymään kohdekirjauksiin.  

 Edelleen lähetettävät kokoonpanokustannukset havaitaan tilaustason havaintomekanismin avulla. Lisätietoja muista muutoksen tunnistusmekanismeista on kohdassa [Rakennetiedot: kustannuksen muutos](design-details-cost-adjustment.md).  

### <a name="detecting-the-adjustment"></a>Muutoksen havaitseminen  
Tilaustason havainnointitoimintoa käytetään muunto-, tuotanto- ja kokoonpanoskenaarioissa. Toiminto toimii seuraavasti:  

-   Kustannusten muuttaminen havaitaan merkitsemällä tilaus aina, kun materiaali/resurssi kirjataan kulutetuksi/käytetyksi.  
-   Kustannus siirretään eteenpäin soveltamalla kustannukset materiaalista/resurssista tuotostapahtumiin, jotka on liitetty samaan tilaukseen.  

Seuraavassa kaaviossa esitetään sopeuttamiskirjauksen rakenne ja kuinka kokoonpanokustannukset määritellään.  

![Kokoonpanoon liittyvien tapahtumien työnkulku kustannusoikaisun aikana.](media/design_details_assembly_posting_3.png "Kokoonpanoon liittyvien tapahtumien työnkulku kirjauksen aikana")  

### <a name="performing-the-adjustment"></a>Muutoksen suorittaminen  
Havaittujen materiaali- ja resurssikustannusten määritysten laajennus kokoonpanon tuotantokirjauksiin suoritetaan **Määritä kustannukset – nimikekirjaukset** eräajossa. Se sisältää Suorita monitasoinen muutos -toiminnon, joka muodostuu seuraavista kahdesta elementistä:  

-   Suorita kokoonpanotilauksen muutos – joka välittää kustannuksen materiaalin ja resurssien käytöstä kokoonpanon tuotos-tapahtumaan. Alla olevan algoritmin rivit 5 ja 6 vastaavat tästä.  
-   Suorita yhden tason muutokset – joka välittää yksittäisten nimikkeiden kustannukset niiden arvostusmenetelmällä. Alla olevan algoritmin rivit 9 ja 10 vastaavat tästä.  

![Kokoonpanon kirjauksen kustannusten muuttamisen algoritmin yhteenveto.](media/design_details_assembly_posting_4.jpg "Kokoonpanon kirjauksen kustannusten muuttamisen algoritmin yhteenveto")  

> [!NOTE]  
>  Tee WIP-sopeutukset -elementti riveillä 7 ja 8 on vastuussa tuotantomateriaalin ja kapasiteetin käytön eteenpäin toimittamisesta keskeneräisten tuotantotilausten tuotantoon. Tätä ei käytetä, kun kokoonpanotilauksen kustannuksia muutetaan, sillä KET ei koske kokoonpanoa.  

Saat lisätietoja siitä, kuinka tuotannon ja kokoonpanon kustannukset kirjataan pääkirjanpitoon kohdasta [Rakennetiedot: varaston kirjaus](design-details-inventory-posting.md).  

## <a name="assembly-costs-are-always-actual"></a>Kokoonpanokustannukset ovat aina todellisia  
 Työprosessin (WIP) konseptia ei voi käyttää kokoonpanotilauksen tiliöintiin. Kokoonpanokustannukset kirjataan vain todellisina kustannuksina, eikä koskaan oletettuina kustannuksina. Katso lisätietoja kohdasta [Rakennetiedot: oletetun kustannuksen kirjaus](design-details-expected-cost-posting.md).  

Seuraava tietorakenne käyttää tätä.  

-   Nimikepäiväkirjan **Tyyppi**-kentässä **Kapasiteettitapahtuma**- ja **Arvotapahtuma**-taulukoissa käytetään *Resurssi*-ominaisuutta kokoonpanon resurssitapahtumien tunnistamiseen.  
-   Nimiketapahtumarivien **Nimiketapahtuman tyyppi**-kentässä **Kapasiteettitapahtuma**- ja **Arvotapahtuma**-taulukossa käytetään *Kokoonpanon tuotos*- ja *Kokoonpanon kulutus* -ominaisuuksia tunnistamaan tuotoksen kokoonpanon nimikkeen tapahtumat ja vastaavasti kulutetut kokoonpanokomponentin tapahtumat.  

Lisäksi kirjausryhmä-kentät kokoonpanotilaus-otsikossa ja kokoonpanotilausriveillä täytetään oletusarvoisesti seuraavasti.  

|Kokonaisuus|Tyyppi|ALV-oletuskirjausryhmä|Yl. Tuotteen kirjausryhmä|  
|------------|----------|-------------------|------------------------------|  
|Kokoonpanotilauksen otsikko|Nimike|Varaston kirjausryhmä|Yl. Tuotteen kirjausryhmä|  
|Kokoonpanotilauksen rivi|Nimike|Varaston kirjausryhmä|Yl. Tuotteen kirjausryhmä|  
|Kokoonpanotilauksen rivi|Resurssi||Yl. Tuotteen kirjausryhmä|  

Näin ollen vain todelliset kustannukset kirjataan pääkirjanpitoon ja väliaikaisia tilejä ei täytetä kokoonpanotilauksen kirjauksesta. Lisätietoja on kohdassa [Rakennetiedot: pääkirjanpidon tilit](design-details-accounts-in-the-general-ledger.md).  

## <a name="assemble-to-order"></a>Kokoonpano tilausta varten  
Nimiketapahtuma, joka on tuloksena kokoonpanotilauksen myynnistä on liitetty kiinteästi kokoonpanon tuotokseen liittyvään nimiketapahtumaan. Näin ollen kohdan kokoonpano tilausta varten kustannus on johdettu kokoonpanotilauksesta, johon se on linkitetty.  

Kokoonpano tilausta varten -määrien kirjauksesta syntyvät myyntityypin nimiketapahtumien merkintänä on **Kyllä** **Kokoonpano tilausta varten** -kentässä.  

Niiden myyntitilausrivien kirjaaminen, joilla osa on varastomäärä ja osa kokoonpano tilausta varten -määrä, aiheuttaa erilliset nimiketapahtumat: toisen varastomäärää ja toisen kokoonpano tilausta varten -määrää varten.  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
 [Rakennetiedot: tuotantotilauksen kirjaus](design-details-production-order-posting.md)   
 [Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md)  
 [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
 [Rahoitus](finance.md)  
 [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]