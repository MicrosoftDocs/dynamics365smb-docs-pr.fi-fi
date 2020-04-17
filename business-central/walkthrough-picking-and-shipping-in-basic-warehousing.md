---
title: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä | Microsoft Docs
description: Business Central -sovelluksessa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ff621150cca478f56edd113832e2253d73f7698c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195697"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Vaihekuvaus: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä

**Huomautus**: Tämä vaihekuvaus on suoritettava esittely-yrityksessä siten, että asetuksena on **Täydellinen arviointi - Kaikki mallitiedot**, joka on käytettävissä Sandbox-ympäristössä. Lisätietoja on kohdassa [Sandbox-ympäristön luominen](across-how-create-sandbox-environment.md).

[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa noudon ja toimituksen lähtevät prosessit voidaan suorittaa neljällä tavalla käyttämällä eri toimintoja varastotason monimutkaisuudesta riippuen.  

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

-   HOPEA-sijainnin määrittäminen varastopaikan käsittelyyn.  
-   Luo myyntitilaus asiakkaalle 10000 30 kaiuttimesta.  
-   Myyntitilauksen vapauttaminen varaston käsittelyyn.  
-   Varastopoiminnan julkaistusta lähdeasiakirjasta luominen  
-   Rekisteröidään fyysisen varastoinnin siirtoa varastosta ja kirjataan samanaikaisesti lähdemyyntitilauksen myyntitoimitusta.  

## <a name="roles"></a>Roolit  
Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

-   Varastopäällikkö  
-   Tilausten käsittelijä  
-   Varastotyöntekijä  

## <a name="prerequisites"></a>Vaatimukset  
Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:  

-   CRONUS Finland Oy on asennettu.  
-   Tee itsestäsi fyysisen varaston työntekijä HOPEISESSA sijainnissa tekemällä seuraavat toimet:  

    1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastotyöntekijät** ja valitse sitten liittyvä linkki.  
    2.  Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **Käyttäjät**-sivulla.  
    3.  Kirjoita **Sijaintikoodi**-kenttään HOPEA.  
    4.  Valitse **Oletus**-kenttä.  

-   Valmistusnimike LS-81 saatavilla HOPEA-sijaintiin seuraavasti:  

    1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikepäiväkirjat** ja valitse sitten liittyvä linkki.  
    2.  Avaa oletuspäiväkirja ja luo kaksi nimikepäiväkirjan riviä seuraavilla käsittelypäivämäärän tiedoilla (23. tammikuuta).  

        |Tapahtuman tyyppi|Nimikenumero|Sijaintikoodi|Varastopaikan koodi|Määrä|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Posit. muutos|LS_81|HOPEINEN|S-01-0001 **Huomautus:** Nimikkeen oletusvarastopaikka CRONUSissa|20|  
        |Posit. muutos|LS_81|HOPEINEN|S-01-0002|20|  

    3.  Valitse ensin **Kirjaa** -toiminto ja sitten **Kyllä**.  

## <a name="story"></a>Taustatietoja  
Ellen, CRONUS:n varastopäällikkö, määrittää HOPEISEN varaston Basic-poiminnan käsittelyä varten,jossa varastotyöntekijät käsittelevät lähtevät tilaukset erikseen. Susanna, tilausten käsittelijä luo myyntitilauksen LS-81-nimikkeen 30 yksikön toimituksesta asiakkaalle 10000 HOPEISESTA varastosta. Johnin, varastotyöntekijän, täytyy varmistaa, että lähetys on valmisteltu ja toimitettu asiakkaalle. John hallitsee kaikkia **Varaston poiminta** -sivulla olevia tehtäviä, jotka viittaavat automaattisesti varastopaikkoihin, joissa LS-81 on tallennettu.  

## <a name="setting-up-the-location"></a>Sijainnin määrittäminen  
**Sijaintikortti**-sivun asetuksissa määritellään yrityksen varaston työnkulut.  

### <a name="to-set-up-the-location"></a>Sijainnin määrittäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sijainnit** ja valitse sitten liittyvä linkki.  
2.  Avaa asianmukaisen HOPEA sijainnin kortti.  
3.  Valitse **Vaadi poiminta** -valintaruutu.  

## <a name="creating-the-sales-order"></a>Myyntitilauksen luominen  
Myyntitilaukset ovat yleisin lähtevien lähdeasiakirjojen tyyppi.  

### <a name="to-create-the-sales-order"></a>Myyntitilauksen luominen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Luo myyntitilaus asiakkaalle 10000 (23.1.) käsittelypäivämääränä seuraavien myyntitilausrivin kanssa.  

    |Nimike|Sijaintikoodi |määrä.|  
    |----------|-------------------|--------------|  
    |LS_81|HOPEINEN|30|  

     Siirry ja ilmoita varastolle, että myyntitilaus on valmis varaston käsittelyyn, kun toimitus saapuu.  

4.  Valitse **Vapauta**-toiminto.  

    John etenee nimikkeiden poimintaan ja toimitukseen.  

## <a name="picking-and-shipping-items"></a>Nimikkeiden poiminta ja toimitus  
**Varaston poiminta** -sivulla voit hallita kaikkia tietyn lähdeasiakirjan lähteviä varastointiaktiviteetteja, kuten myyntitilaus.  

### <a name="to-pick-and-ship-items"></a>Nimikkeiden poiminta ja lähettäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varaston poiminnat** ja valitse sitten liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Valitse **Lähdeasiakirja**-kenttä ja sitten **Myyntitilaus**.  
4.  Valitse **Lähdenro**-kentässä asiakkaalle 10000 tehdyn myynnin rivi ja valitse sitten **OK**.  

    Vaihtoehtoisesti voit valita ensin **Hae lähdeasiakirja** -toiminnon ja sitten myyntitilauksen.  
5.  Valitse **Täytä autom. käsitelt. määrä** -toiminto.  

    Syötä vaihtoehtoisesti **Käsiteltävä määrä** -kentässä vastaavasti 10 ja 30 kahdelle varastonpoimintariville.  
6.  Valita ensin **Kirjaa**-toiminto, sitten **Toimitus** ja lopuksi **OK**.  

    30 kaiutinta on nyt rekisteröity poimituiksi varastopaikoista S-01-0001- ja S-01-0002, ja luodaan negatiivinen nimiketapahtuma, joka heijastaa kirjattua myyntitoimitusta.  

## <a name="see-also"></a>Katso myös  
 [Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md)   
 [Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Poiminta tuotantoon tai kokoonpanoon](warehouse-how-to-pick-for-production.md)   
 [Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Rakennetiedot: lähtevän fyysisen varastoinnin virta](design-details-outbound-warehouse-flow.md)   
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
