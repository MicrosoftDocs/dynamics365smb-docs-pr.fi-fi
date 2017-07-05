---
title: 'Toimintaohje: Maksujen vieminen pankkitiedostoon| Microsoft Docs'
description: "Kuinka maksut viedään pankkitiedostoon"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 04/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a7f388db2d00b9916160d19edead92714f6eacc1
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-export-payments-to-a-bank-file"></a>Kuinka maksut viedään pankkitiedostoon
Kun olet valmis suorittamaan maksut toimittajille **Maksupäiväkirja**-ikkunassa, voit viedä tiedoston maksutietojen kanssa päiväkirjan riveille. Voit sitten ladata tiedoston verkkopankkiin käsitelläksesi siihen liittyvät rahansiirrot.

[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in yleisessä versiossa asetetaan ja yhdistetään yleiset palvelut pankkitietojen muuntamiseen mihin tahansa pankkisi vaatimaan muotoon. Pohjoisamerikkalaisessa versioissa maksutiedostot voidaan lähettää samalla palvelulla sähköisenä rahansiirtona, joskin prosessi on hieman erilainen. Lisätietoja on Maksujen vienti pankkitiedostoon -osan vaiheessa 6.    

**Huomautus**: Määritä liittyvän pankkitilin sähköinen muoto ennen maksutiedostojen vientiä maksupäiväkirjasta ja ota pankkitietojen muuntopalvelu käyttöön. Lisätietoja on kohdassa [Toimintaohje: Pankkitilien määrittäminen](bank-how-setup-bank-accounts.md) ja [Toimintaohje: Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-data-conversion-service.md). Valitse myös **Salli maksun vienti** -valintaruutu **Yleisen päiväkirjan erät** -ikkunassa. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  

Voit tarkastella maksupäiväkirjasta vietyjä maksutiedostoja **Hyvityksen siirron rekisterit** -ikkunassa. Ikkunassa voit myös viedä maksutiedostot uudelleen, jos tekniset virheet tai tiedostomuutokset vaativat sitä. Huomaa kuitenkin, että viedyt sähköiset rahansiirtotiedostot eivät näy tässä ikkunassa eikä niitä voi viedä uudelleen.  

## <a name="to-export-payments-to-a-bank-file"></a>Maksujen vienti pankkitiedostoon
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Maksupäiväkirjat** ja valitse sitten liittyvä linkki.
2. Voit esimerkiksi täyttää päiväkirjan rivit **Ehdota toimittajamaksuja** -toiminnolla. Lisätietoja on kohdassa [Toimintaohje: Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md).
3. Täytä maksupäiväkirjan rivien kentät tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    **Huomautus**: Jos käytät sähköistä rahansiirtoa, sinun on valittava joko **Sähköinen maksu** tai **Sähköinen maksu – IAT** **Pankkimaksun tyyppi** -kentässä.

    Eri tiedostojen vientipalvelut ja niiden tiedostomuodot edellyttävät erilaisia asetuksia **Pankkitilin kortti**- ja **Toimittajan pankkitilin kortti** -ikkunassa. Saat ilmoituksen virheellisistä tai puuttuvista asetusarvoista, kun yrität viedä tiedoston.
        
4. Kun kaikki maksupäiväkirjan rivit ovat valmiit, valitse **Vie**-toiminto.
5. Täytä **Vie sähköiset maksut** -ikkunan kentät tarpeen mukaan.

    Virheilmoituksia näkyy **maksutiedoston virheet** -tietoruudussa, jossa voit myös nähdä yksityiskohtaiset tiedot virheviestistä. Kaikki virheet on ratkaistava ennen maksutiedoston vientiä.

    **Vihje**: Pankkitietojen muuntopalvelua käytettäessä yleinen virheilmoitus kertoo, että pankkitilin numeron pituus ei ole pankin edellyttämä. Välttääksesi tai ratkaistaksesi tämän ongelman, sinun on poistettava arvo **IBAN**-kentästä **Pankkitilin kortti** -ikkunassa ja syötettävä sitten **Pankkitilin nro** -kenttään pankkitilin numero pankin vaatimassa muodossa.

6. Määritä **Tallenna nimellä** -ikkunassa paikka, johon tiedosto viedään ja valitse sitten **Tallenna**.

    **Huomautus**: Jos käytät sähköistä rahansiirtoa, tallenna saatava toimittajan maksusuorituslomake Word-asiakirjana tai valitse sen lähettäminen suoraan toimittajalle. Maksut on nyt lisätty **Luo sähköinen rahansiirtotiedosto** -ikkunaan, jossa voit luoda samanaikaisesti useita maksutilauksia, mikä säästää lähetyskustannuksia. Lisätietoja on seuraavissa vaiheissa:
7. Valitse **Maksupäiväkirja**-ikkunassa **Luo sähköinen rahansiirtotiedosto** -toiminto.

    **Luo sähköinen rahansiirtotiedosto** -ikkunassa kaikki sähköistä rahansiirtoa varten määritetyt maksut, jotka on viety maksupäiväkirjasta määritetylle pankkitilille mutta joita ei ole vielä muodostettu, on mainittu **Rivit**-pikavälilehdessä.
8. Vie kaikki sähköiset rahansiirtomaksut sisältävä tiedosto valitsemalla **Luo sähköinen rahansiirtotiedosto** -toiminto.
9. Määritä **Tallenna nimellä** -ikkunassa paikka, johon tiedosto viedään ja valitse sitten **Tallenna**.

Pankin maksutiedosto viedään määrittämääsi sijaintiin ja voit jatkaa sen lataamista verkkopankkitilille ja suorittaa todelliset maksut. Voit sitten kirjata viedyn maksupäiväkirjan rivit.

## <a name="to-export-payments-that-represent-customer-refunds"></a>Asiakashyvityksiä vastaavien maksujen vieminen
Seuraavaksi kerrotaan kiertotie sähköisten hyvitysmaksujen viennille.

**Varoitus**: Tuloksena olevan maksupäiväkirjan rivejä ei voi kirjata, poistaa eikä mitätöidä.
1. Määritä asiakas toimittajaksi. Anna sen nimeksi vaikkapa Asiakas X hyvityksiä varten. Lisätietoja on kohdassa [Toimintaohje: Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md).
2. Määritä asiakkaan maksupäiväkirjan rivin **Tilityyppi**-kentän arvoksi **Asiakas** ja **Asiakirjatyyppi**-kentän arvoksi **Hyvitys **.
3. Suorita maksun vienti tavalliseen tapaan Maksujen vienti pankkitiedostoon -osassa kuvatulla tavalla.

## <a name="to-plan-when-to-post-exported-payments"></a>Vietyjen maksujen kirjaamisajankohdan suunnitteleminen
Jos et halua kirjata viedyn maksun maksupäiväkirjan riviä, koska esimerkiksi odotat pankin vahvistusta tapahtuman käsittelystä, voit poistaa päiväkirjan rivin. Kun luot myöhemmin maksupäiväkirjan rivin, jolla maksetaan jäljellä oleva laskun summa, **Viety summa yhteensä** -kenttä näyttää, kuinka paljon maksun summasta on jo viety. Lisäksi saat lisätietoja viedystä kokonaissummasta valitsemalla **Hyvityksen siirron rekisterimerkinnät** -painikkeen, joka avaa vietyjen maksutiedostojen tiedot.

Jos noudatat prosessia, jossa maksut kirjataan vasta sen jälkeen, kun pankin suorittamasta maksujen käsittelystä on saatu vahvistus, voit hallita tätä kahdella eri tavalla.

* Maksupäiväkirjan ehdotettujen maksurivien kohdalla voit lajitella joko **Viety maksutiedostoon** -sarakkeen tai **Viety summa yhteensä**-kentän mukaan ja sitten poistaa maksuehdotukset avoimilta laskuilta, jotka on jo maksettu ja joita et halua maksaa.
* **Ehdota toimittajamaksuja** -ikkunassa, jossa määrität maksupäiväkirjaan lisättävät maksut, voit valita **Ohita viedyt maksut** -valintaruudun, jos et halua lisätä päiväkirjarivejä jo viedyille maksuille.

Saat lisätietoja viedyistä maksuista valitsemalla **Maksujen vientihistoria** -toiminnon.

## <a name="to-re-export-payments-to-a-bank-file"></a>Maksujen vieminen uudelleen pankkitiedostoon
Voit viedä maksutiedostot uudelleen **Hyvityksen siirron rekisterit** -ikkunasta. Ennen kuin poistat tai kirjaat maksupäiväkirjan rivejä, voit myös viedä maksutiedoston uudelleen **Maksupäiväkirja**-ikkunasta yksinkertaisesti viemällä uudelleen. Jos olet poistanut tai kirjannut maksupäiväkirjan rivit viennin jälkeen, voit viedä saman maksutiedoston uudelleen **Hyvityksen siirron rekisterit** -ikkunasta. Valitse rivi tilisiirtojen erälle, jonka haluat viedä uudelleen, ja käyttämällä sitten **Vie maksut uudelleen tiedostoon** -toimintoa.

**Huomautus**: Viedyt sähköiset rahansiirtotiedostot eivät näy **Hyvityksen siirron rekisterit** -ikkunassa eikä niitä voi viedä uudelleen.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Hyvityksen siirron rekisterit** ja valitse sitten liittyvä linkki.
2. Valitse ensin uudelleenvietävä maksun vienti ja sitten **Vie maksut uudelleen tiedostoon** -toiminto.

## <a name="see-also"></a>Katso myös
[Ostovelat](payables-manage-payables.md)  
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]