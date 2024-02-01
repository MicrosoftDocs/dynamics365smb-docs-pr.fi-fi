---
title: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä
description: Tässä artikkelissa käsitellään poiminto- ja toimitusprosessien eri monimutkaisuustasoja.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
ms.service: dynamics-365-business-central
---
# Vaihekuvaus: Poiminta ja toimitus fyysisen varastoinnin perusmäärityksissä

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeet poimintaan ja toimitukseen on käytettävissä neljä tapaa, jotka käsitellään seuraavassa taulukossa.

|Tapa|Lähtevien käsittely|Vaadi poiminta|Vaadi toimitus|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Poiminnan ja toimituksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta|Otettu käyttöön||Perus: tilauksittain.|  
|S|Poiminnan ja toimituksen kirjaaminen fyysisen varastoinnin toimitusasiakirjasta||Otettu käyttöön|Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimitusasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lisätietoja on kohdassa [Lähtevien varaston työnkulku](design-details-outbound-warehouse-flow.md).

Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää B.  

## Tietoja tästä vaihekuvauksesta

Jos sijainnit on määritetty fyysisen varastoinnin perusmäärityksissä edellyttämään poimintakäsittelyä mutta ei toimituskäsittelyä, **Varaston poiminta** -sivua on käytettävä lähtevien lähdeasiakirjojen poiminta- ja toimitustietojen tallennuksessa ja kirjaamisessa. Lähtevä lähdeasiakirja voi olla myyntitilaus, ostopalautustilaus, lähtevä siirtotilaus tai tuotantotilaus komponenttitarpeella.  

Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

- ETELÄ-sijainnin määrittäminen varastopaikan käsittelyyn.  
- Myyntitilauksen luominen asiakkaalle 10000 30 Amsterdam-lampusta.  
- Myyntitilauksen vapauttaminen varaston käsittelyyn.  
- Varastopoiminnan julkaistusta lähdeasiakirjasta luominen  
- Rekisteröidään fyysisen varastoinnin siirtoa varastosta ja kirjataan samanaikaisesti lähdemyyntitilauksen myyntitoimitusta.  

## Roolit

Tässä vaihekuvauksessa havainnollistetaan seuraavien käyttäjäroolien tehtäviä:  

- Varastopäällikkö  
- Tilausten käsittelijä  
- Varastotyöntekijä  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## Taustatietoja

Ellen, CRONUSin varastopäällikkö, määrittää ETELÄ-varaston Basic-poiminnan käsittelyä varten. Sen mukaisesti varastotyöntekijät käsittelevät lähtevät tilaukset erikseen. Susanna, tilausten käsittelijä, luo myyntitilauksen 1928-S-nimikkeen 30 yksikön toimituksesta asiakkaalle 10000 ETELÄ-varastosta. Johnin, varastotyöntekijän, täytyy varmistaa, että lähetys on valmisteltu ja toimitettu asiakkaalle. John hallitsee kaikkia **Varaston poiminta** -sivulla olevia tehtäviä, jotka viittaavat automaattisesti varastopaikkoihin, joissa nimikettä 1928-S varastoidaan.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### Varastopaikkakoodien määrittäminen

Kun olet määrittänyt sijainnin, sinun täytyy lisätä kaksi varastopaikkaa.

#### Varastopaikkakoodien määrittäminen

1. Valitse **Varastopaikat**-toiminto.
2. Luo kaksi varastopaikkaa koodeilla *S-01-0001* ja *S-01-0002*.

### Varastotyöntekijän tekeminen sijainnissa ETELÄ

Jotta voisit käyttää tätä toimintoa, sinun on lisättävä itsesi varastotyöntekijäksi tähän sijaintiin. 

#### Tee itsestäsi varastotyöntekijä

  1. Valitse ![Lamppu, joka avaa ensin Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston työntekijät** ja valitse sitten vastaava linkki.  
  2. Valitse ensin **Käyttäjätunnus**-kenttä ja valitse oma käyttäjätilisi **F.var. työntekijät** -sivulla.
  3. Valitse **Sijaintikoodi**-kentässä ETELÄ.  
  4. Valitse **Oletus**-kenttä ja sitten **Kyllä**-painike..  

### Nimikkeen 1928-S tekeminen saatavaksi

Tehdäksesi nimikkeen 1928-S saatavaksi ETELÄ-sijainnissa noudata seuraavia vaiheita:  

  1. Valitse ![Lamppu, joka avaa toisena Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikepäiväkirjat** ja valitse sitten vastaava linkki.  
  2. Avaa oletuspäiväkirja ja luo kaksi nimikepäiväkirjan riviä seuraavilla käsittelypäivämäärän tiedoilla (23. tammikuuta).  

        |Tapahtuman tyyppi|Nimikenumero|Sijaintikoodi |Varastopaikan koodi|määrä|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Posit. muutos|1928-S|ETELÄ|S-01-0001|20|  
        |Posit. muutos|1928-S|ETELÄ|S-01-0002|20|  

        Oletusarvoisesti myyntirivien **Varastopaikan koodi** -kentät on piilotettu, joten ne on tuotava näkyviin. Sen tehdäksesi sinun on muokattava sivua. Lisätietoja on kohdassa, jossa [Sivun mukauttaminen mukautusvalintanauhan avulla](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

  3. Valitse **Toiminnot**, sitten **Kirjaus** ja valitse sitten **Kirjaa**.  
  4. Valitse **Kyllä**-painike.  

## Myyntitilauksen luominen

Myyntitilaukset ovat yleisin lähtevien lähdeasiakirjojen tyyppi.  

### Myyntitilauksen luominen

1. Valitse ![Lamppu, joka avaa kolmantena Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Luo myyntitilaus asiakkaalle 10000 (23.1.) käsittelypäivämääränä seuraavien myyntitilausrivin kanssa.  

    |Nimike|Sijaintikoodi |määrä|  
    |----|-------------|--------|  
    |1928-S|ETELÄ|30|  

     Siirry ja ilmoita varastolle, että myyntitilaus on valmis varaston käsittelyyn, kun toimitus saapuu.  

4. Valitse **Vapauta**-toiminto.  

    John etenee nimikkeiden poimintaan ja toimitukseen.  

## Nimikkeiden poiminta ja toimitus

**Varaston poiminta** -sivulla voit hallita kaikkia tietyn lähdeasiakirjan lähteviä varastointiaktiviteetteja, kuten myyntitilaus. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### Nimikkeiden poiminta ja lähettäminen

1. Valitse ![Lamppu, joka avaa neljäntenä Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston poiminnat** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  

    Varmista, että **Nro**-kenttä täytetään **Yleinen**-pikavälilehdessä.
3. Valitse **Lähdeasiakirja**-kenttä ja sitten **Myyntitilaus**.  
4. Valitse **Lähdenro**-kentässä asiakkaalle 10000 tehdyn myynnin rivi ja valitse sitten **OK**.  

    Vaihtoehtoisesti voit valita ensin **Hae lähdeasiakirja** -toiminnon ja sitten myyntitilauksen.  
5. Valitse **Täytä autom. käsitelt. määrä** -toiminto.  

    Syötä vaihtoehtoisesti **Käsiteltävä määrä** -kentässä vastaavasti 10 ja 20 kahdelle varastonpoimintariville.  
6. Valita ensin **Kirjaa**-toiminto, sitten **Toimitus** ja lopuksi **OK**.  

    30 Amsterdam-lamppua on nyt rekisteröity poimituiksi varastopaikoista S-01-0001- ja S-01-0002, ja luodaan negatiivinen nimiketapahtuma, joka heijastaa kirjattua myyntitoimitusta.  

## Katso myös

[Nimikkeiden poiminta varaston poimintojen avulla](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Nimikkeiden poiminta fyysisen varaston toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Poiminta tuotantoon tai kokoonpanoon](warehouse-how-to-pick-for-production.md)  
[Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Rakennetiedot: lähtevän fyysisen varastoinnin virta](design-details-outbound-warehouse-flow.md)  
[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
