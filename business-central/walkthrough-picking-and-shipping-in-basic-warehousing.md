---
title: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä
description: Business Central -sovelluksessa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214651"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Vaihekuvaus: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.  

|Tapa|Saapuva prosessi|Varastopaikat|Poiminnat|Toimitukset|Monimutkaisuustaso (katso [Rakennetiedot: Fyysisen varaston asetukset](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|L|Poiminnan ja toimituksen kirjaaminen tilausriviltä|X|||2|  
|B|Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta||X||3|  
|N|Kirjaa poiminta ja lähetyksen fyysisen varastoinnin toimituksen asiakirjasta|||X|4/5/6|  
|P|Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimituksen asiakirjasta||X|X|4/5/6|  

Katso lisätietoja kohdasta [Rakennetiedot: lähtevän fyysisen varastoinnin virta](design-details-outbound-warehouse-flow.md).  

Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää B.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta

Jos sijainnit on määritetty fyysisen varastoinnin perusmäärityksissä edellyttämään poimintakäsittelyä mutta ei toimituskäsittelyä, **Varaston poiminta** -sivua on käytettävä lähtevien lähdeasiakirjojen poiminta- ja toimitustietojen tallennuksessa ja kirjaamisessa. Lähtevä lähdeasiakirja voi olla myyntitilaus, ostopalautustilaus, lähtevä siirtotilaus tai tuotantotilaus komponenttitarpeella.  

Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

- ETELÄ-sijainnin määrittäminen varastopaikan käsittelyyn.  
- Myyntitilauksen luominen asiakkaalle 10000 30 Amsterdam-lampusta.  
- Myyntitilauksen vapauttaminen varaston käsittelyyn.  
- Varastopoiminnan julkaistusta lähdeasiakirjasta luominen  
- Rekisteröidään fyysisen varastoinnin siirtoa varastosta ja kirjataan samanaikaisesti lähdemyyntitilauksen myyntitoimitusta.  

## <a name="roles"></a>Roolit

Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

- Varastopäällikkö  
- Tilausten käsittelijä  
- Varastotyöntekijä  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a>Taustatietoja

Ellen, CRONUSin varastopäällikkö, määrittää ETELÄ-varaston Basic-poiminnan käsittelyä varten. Sen mukaisesti varastotyöntekijät käsittelevät lähtevät tilaukset erikseen. Susanna, tilausten käsittelijä, luo myyntitilauksen 1928-S-nimikkeen 30 yksikön toimituksesta asiakkaalle 10000 ETELÄ-varastosta. Johnin, varastotyöntekijän, täytyy varmistaa, että lähetys on valmisteltu ja toimitettu asiakkaalle. John hallitsee kaikkia **Varaston poiminta** -sivulla olevia tehtäviä, jotka viittaavat automaattisesti varastopaikkoihin, joissa nimikettä 1928-S varastoidaan.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a>Varastopaikkakoodien määrittäminen
Kun olet määrittänyt sijainnin, sinun täytyy lisätä kaksi varastopaikkaa.

#### <a name="to-setup-the-bin-codes"></a>Varastopaikkakoodien määrittäminen

1. Valitse **Varastopaikat**-toiminto.
2. Luo kaksi varastopaikkaa koodeilla *S-01-0001* ja *S-01-0002*.

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a>Varastotyöntekijän tekeminen sijainnissa ETELÄ

Jotta voisit käyttää tätä toimintoa, sinun on lisättävä itsesi varastotyöntekijäksi tähän sijaintiin. 

#### <a name="to-make-yourself-a-warehouse-employee"></a>Tee itsestäsi varastotyöntekijä

  1. Valitse ensimmäinen ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastotyöntekijät** ja valitse sitten liittyvä linkki.  
  2. Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **F.var. työntekijät** -sivulla.
  3. Valitse **Sijaintikoodi**-kentässä ETELÄ.  
  4. Valitse **Oletus**-kenttä ja sitten **Kyllä**-painike..  

### <a name="making-item-1928-s-available"></a>Nimikkeen 1928-S tekeminen saatavaksi

Tehdäksesi nimikkeen 1928-S saatavaksi ETELÄ-sijainnissa noudata seuraavia vaiheita:  

  1. Valitse toinen ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikepäiväkirjat** ja valitse sitten liittyvä linkki.  
  2. Avaa oletuspäiväkirja ja luo kaksi nimikepäiväkirjan riviä seuraavilla käsittelypäivämäärän tiedoilla (23. tammikuuta).  

        |Tapahtuman tyyppi|Nimikenumero|Sijaintikoodi |Varastopaikan koodi|määrä|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Posit. muutos|1928-S|ETELÄ|S-01-0001|20|  
        |Posit. muutos|1928-S|ETELÄ|S-01-0002|20|  

        Oletusarvoisesti myyntirivien **Varastopaikan koodi** -kentät on piilotettu, joten ne on tuotava näkyviin. Sen tehdäksesi sinun on muokattava sivua. Lisätietoja on kohdassa, jossa [Sivun mukauttaminen mukautusvalintanauhan avulla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

  3. Valitse **Toiminnot**, sitten **Kirjaus** ja valitse sitten **Kirjaa**.  
  4. Valitse **Kyllä**-painike.  

## <a name="creating-the-sales-order"></a>Myyntitilauksen luominen

Myyntitilaukset ovat yleisin lähtevien lähdeasiakirjojen tyyppi.  

### <a name="to-create-the-sales-order"></a>Myyntitilauksen luominen

1. Valitse kolmas ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Luo myyntitilaus asiakkaalle 10000 (23.1.) käsittelypäivämääränä seuraavien myyntitilausrivin kanssa.  

    |Nimike|Sijaintikoodi |määrä|  
    |----|-------------|--------|  
    |1928-S|ETELÄ|30|  

     Siirry ja ilmoita varastolle, että myyntitilaus on valmis varaston käsittelyyn, kun toimitus saapuu.  

4. Valitse **Vapauta**-toiminto.  

    John etenee nimikkeiden poimintaan ja toimitukseen.  

## <a name="picking-and-shipping-items"></a>Nimikkeiden poiminta ja toimitus

**Varaston poiminta** -sivulla voit hallita kaikkia tietyn lähdeasiakirjan lähteviä varastointiaktiviteetteja, kuten myyntitilaus. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>Nimikkeiden poiminta ja lähettäminen

1. Valitse neljäs ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varaston poiminnat** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  

    Varmista, että **Nro**-kenttä täytetään **Yleinen**-pikavälilehdessä.
3. Valitse **Lähdeasiakirja**-kenttä ja sitten **Myyntitilaus**.  
4. Valitse **Lähdenro**-kentässä asiakkaalle 10000 tehdyn myynnin rivi ja valitse sitten **OK**.  

    Vaihtoehtoisesti voit valita ensin **Hae lähdeasiakirja** -toiminnon ja sitten myyntitilauksen.  
5. Valitse **Täytä autom. käsitelt. määrä** -toiminto.  

    Syötä vaihtoehtoisesti **Käsiteltävä määrä** -kentässä vastaavasti 10 ja 20 kahdelle varastonpoimintariville.  
6. Valita ensin **Kirjaa**-toiminto, sitten **Toimitus** ja lopuksi **OK**.  

    30 Amsterdam-lamppua on nyt rekisteröity poimituiksi varastopaikoista S-01-0001- ja S-01-0002, ja luodaan negatiivinen nimiketapahtuma, joka heijastaa kirjattua myyntitoimitusta.  

## <a name="see-also"></a>Katso myös

[Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[Poiminta tuotantoon tai kokoonpanoon](warehouse-how-to-pick-for-production.md)  
[Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Rakennetiedot: lähtevän fyysisen varastoinnin virta](design-details-outbound-warehouse-flow.md)  
[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
