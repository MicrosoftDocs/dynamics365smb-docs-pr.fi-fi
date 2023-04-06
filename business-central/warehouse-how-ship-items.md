---
title: Nimikkeiden toimittamimen
description: Tässä artikkelissa käsitellään nimikkeiden toimittamista fyysisestä varastosta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---

# Nimikkeiden toimittaminen fyysisen varaston toimituksena

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeet poimintaan ja toimitukseen on käytettävissä neljä tapaa, jotka käsitellään seuraavassa taulukossa.

|Tapa|Lähtevien käsittely|Vaadi poiminta|Vaadi toimitus|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Poiminnan ja toimituksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Poiminnan ja toimituksen kirjaaminen varaston poiminta-asiakirjasta|Otettu käyttöön||Perus: tilauksittain.|  
|S|Poiminnan ja toimituksen kirjaaminen fyysisen varastoinnin toimitusasiakirjasta||Otettu käyttöön|Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Poiminnan kirjaaminen fyysisen varastoinnin poiminta-asiakirjasta ja toimituksen kirjaaminen fyysisen varastoinnin toimitusasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lisätietoja nimikkeiden toimittamisesta on kohdassa [Lähtevä fyysisen varastoinnin virta](design-details-outbound-warehouse-flow.md).

Tässä artikkelissa viitataan taulukon menetelmiin C ja D. Kummassakin menetelmässä aloitetaan luomatta toimitusasiakirja lähdeasiakirjasta. Poimi sitten toimitukseen määritetyt nimikkeet.

Jos sijainti edellyttää fyysisen varaston toimituksia, nimikkeitä voidaan toimittaa fyysiseen varastoon vapautettujen lähdeasiakirjojen perusteella. Lähdeasiakirjojen vapauttaminen mahdollistaa niissä olevien nimikkeiden käsittelyn fyysisessä varastossa. Esimerkkejä lähdeasiakirjoista:

* Myyntitilaukset
* Ostopalautustilaukset
* Siirtotilaukset
* Huoltotilaukset

Fyysisen varaston toimitus voidaan luoda jommallakummalla tavalla:

* Push-menetelmässä työ tehdään tilauskohtaisesti. Luo asiakirjan fyysisen varaston toimitus valitsemalla lähdeasiakirjassa **Luo fyysisen varaston toimitus** -toiminto.
* Pull-menetelmässä lähdeasiakirjan **Vapauta**-toiminto vapauttaa asiakirjan fyysiseen varastoon. Varastotyöntekijä luo ainakin yhdelle vapautetulle lähdeasiakirjalle **fyysisen varaston toimituksen**. Fyysisen varaston toimitus luodaan pull-menetelmässä seuraavasti.

## Nimikkeiden toimittaminen käyttämällä fyysisen varaston asiakirjaa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston toimitukset**, valitse sitten vastaava linkki.  
2. Valitse **Uusi**.  
3. Valitse **Nro**-kenttään numerosarja, jolla toimituksen tunnus luodaan.  
4. Valitse **Sijaintikoodi**-kentässä toimituksen lähdesijainti. 

    Lähdeasiakirjan rivejä noudettaessa joitakin sijainnin tietoja kopioidaan kullekin riville.  
5. Jos sijainti edellyttää varastopaikkojen käyttöä, täytä **Varastopaikan koodi** -kenttä. Määritysten mukaan [!INCLUDE[prod_short](includes/prod_short.md)] voi lisätä varastopaikan koodin valmiiksi. Lisätietoja on kohdassa [Alueen ja varastopaikan koodit](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. Lähdeasiakirja voidaan hakea kahdella tavalla:

    * Valitse **Hae lähdeasiakirjat** -toiminto. **Lähdeasiakirjat - lähtevä** -sivu avautuu. Tällä sivulla voidaan valita toimitusta edellyttävät fyysiseen varastoon vapautetut lähdeasiakirjat.
    * Valitse **Käytä suodat. kun haet lähd.d** -toiminto. **Suod. lähdeasiakirj. saamisek.** -sivu avautuu. Lähdeasiakirjan suodatin voidaan valita ja sitä voidaan käyttää. Kaikki vapautetut lähdeasiakirjan rivit, jotka täyttävät suodatusehdot, lisätään **F.var. toimitus** -sivulle. Lisätietoja on kohdassa [Lähdeasiakirjojen hakeminen suodattimia käyttämällä](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents).

    > [!NOTE]
    > Jos sijainnissa käytetään kullakin rivillä laiturointia ja varastopaikkoja, laiturointivarastopaikkoihin asetettujen nimikkeiden määrää voidaan tarkastella. [!INCLUDE [prod_short](includes/prod_short.md)] laskee määrät aina, kun toimituksen kenttiä päivitetään. Jos nimikkeet ovat valmisteltavassa toimituksessa, kaikille nimikkeillä voidaan luoda poiminta ja viimeistellä sitten toimituksen. Lisätietoja on kohdassa [Nimikkeiden laiturointi](warehouse-how-to-cross-dock-items.md).

7. Luo fyysisen varaston poiminta. Jos sijainti edellyttää poimintaa, fyysisen varaston toimitusten poimintatoiminnot voidaan luoda jommallakummalla tavalla:

    * Push-menetelmässä käytetään **Luo poiminta** -toimintoa. Valitse poimittavat rivit ja määritä poimintoja koskevat tiedot. Kyse voi olla esimerkiksi siitä, mistä varastopaikoista poimitaan ja mihin asetetaan sekä kuinka monta yksikköä käsitellään. Varastopaikat voidaan määrittää ennalta fyysisen varaston sijainnissa tai resurssissa.
    * Pull-menetelmässä käytetään **Vapauta**-toimintoa. Hae määritetyt poiminnat käyttämällä **Poimintatyökirja**-sivun **Hae f. varastoinnin asiakirjat** -toimintoa. Kun fyysisen varastoinnin poiminnat on rekisteröity kokonaan, **Poimintatyökirja**-kohteen rivit poistetaan. Lisätietoja on kohdassa [Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md).

    > [!TIP]
    > Jos sijainnissa ei edellytetä poimintaa, fyysisen varaston toimitus voidaan tulostaa poimintaluetteloksi.

8. Määritä toimitettava määrä.  

    Jos sijainti edellyttää poimintaa, **Toimitettava määrä** -kenttä päivitetään automaattisesti, kun poiminta rekisteröidään. Muussa tapauksessa **Toimitettava määrä** -kenttään täytetään kunkin rivin avoin määrä, kun fyysisen varaston toimitusrivi on luotu.

    Vaikka määrää voidaan muuttaa, toimitettavien nimikkeiden määrä ei voi ylittää arvoa, joka on lähdeasiakirjan rivin **Avoin määrä** -kentässä tai **Poimittu määrä** -kentässä, jos poiminta on pakollinen.

    Kaikkien rivien **Toimitettava määrä** -kentän arvoksi voidaan määrittää nolla valitsemalla **Poista toimitettava määrä** -toiminto. Määrän määrittäminen nollaksi on kätevää esimerkiksi silloin, jossa toimitusmäärä päivitetään viivakoodin lukijalla. Toimitettavissa oleva määrä lisätään valitsemalla **Täytä autom. toimitet. määrä** -toiminto.

9. Kirjaa toimitus.

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

## Lähdeasiakirjojen hakeminen suodattimien avulla

Fyysisen varastoinnin toimituksen **Suod. lähdeasiakirj. saamisek.** -sivun avulla voidaan noutaa toimitettavat nimikkeet määrittävän vapautetun lähdeasiakirjan rivit.

1. Valitse fyysisen varaston toimituksessa **Käytä suodat. kun haet lähd.d** -toiminto. 
2. Määritä uusi suodatin antamalla kuvaileva koodi **Koodi**-kenttään, valitse **Muokkaa**-toiminto.

    **Lähdeasiakirjan suodatinkortti – lähtevä** -sivu avautuu.

3. Määritä suodattimien avulla noudettavien lähdeasiakirjarivien tyyppi. Valittavissa on esimerkiksi lähdeasiakirjatyyppejä, kuten myynti- tai siirtotilauksia.
4. Valitse **Suorita**.  

Kaikki suodatusehdot täyttävät vapautetut lähdeasiakirjan rivit lisätään sillä **F. varastoinnin toimitus** -sivulla, jossa suodattimet määritettiin.

Voit tehdä niin monta suodatinyhdistelmää kuin haluat. Suodattimet tallennetaan **Suod. lähdeasiakirj. saamisek.** -sivulle, jossa ne ovat käytettävissä tulevaa käyttöä varten. Voit muuttaa ehtoja milloin tahansa valitsemalla **Muokkaa**-toiminnon.

## Alueen ja varastopaikan koodit

Jos varastopaikat ovat pakollisia sijainnissa, [!INCLUDE [prod_short](includes/prod_short.md)] ehdottaa alueen ja varastopaikan koodia fyysisen varaston toimitusasiakirjassa.

* Jos kyse on laajennetuista määrityksistä, joissa sijainti käyttää ohjattua hyllytystä ja poimintaa, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää **sijaintikortin** **Toimituksen var.paikkakoodi** -kentässä määritettyä varastopaikkaa. Jos **toimituksen varastopaikan koodia** ei ole määritetty, kenttä on tyhjä. Jos nimikkeen ja toimituksen varastopaikka eivät ole samat, [!INCLUDE [prod_short](includes/prod_short.md)] jättää toimituksen varastopaikan tyhjäksi.
* Muissa tapauksissa [!INCLUDE [prod_short](includes/prod_short.md)] käyttää aina ensin **sijaintikortin** **Toimituksen var.paikkakoodi** -kentässä määritettyä varastopaikkaa. Jos toimituksen varastopaikan koodia ei ole määritetty, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää lähdeasiakirjan varastopaikan koodia.

## Kokoonpano tilausta varten -nimikkeiden käsitteleminen fyysisen varastoinnin toimituksissa

Jos kyseessä on kokoonpano tilausta varten, fyysisen varaston toimitusrivin **Toimitettava määrä** -kentän avulla voidaan kirjat koottujen yksiköiden lukumäärä. Määrä kirjataan kokoonpanon tuotoksena, kun fyysisen varastoinnin toimitus kirjataan. Muiden fyysisen varastoinnin toimitusrivien **Toimitettava määrä** -kentän arvo nolla.

Kun työntekijät saavat koko Kokoonpano tilausta varten -määrän tai sen osan, määrä kirjataan fyysisen varaston toimitusrivin **Toimitettava määrä** -kenttään. Sen jälkeen valitaan **Kirjaa toimitus** -toiminto. Kirjattavan kokoonpanon tuotos sisältää myös komponentin kulutuksen. Määrän myyntitoimitus on kirjattu myyntitilaukseen.

Valitse kokoonpanotilauksen **Kokoonpano tilausta varten: f. var. toimitusrivi**, kun haluat käyttää fyysisen varastoinnin toimitusriviä.

Kun fyysisen varaston toimitus on kirjattu, myyntitilauksen rivin kentät päivitetään näyttämään eteneminen fyysisessä varastossa. Seuraavat kentät päivitetään lisäksi näyttämään kuinka monta kokoonpanoa tilausta varten on vielä koottava ja toimitettava:

* **ATO-varaston avoin määrä**
* **ATO-varaston avoin määrä (perus)**

> [!NOTE]
> Yhdistelmätilanteissa, joissa osa määrästä on koottava ja toinen osa on toimitettava varastosta, luodaan kaksi fyysisen varaston toimitusriviä. Toinen on kokoonpano tilausta varten -määrälle ja toinen varastomäärälle.
>
> Kokoonpano tilausta varten -määrä käsitellään tässä artikkelissa kuvatulla tavalla. Varastomäärä käsitellään tavallisena fyysisen varaston toimitusrivinä. Lisätietoja yhdistelmäskenaarioista on kohdassa [Tietoja Kokoonpano tilausta varten- tai Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md).

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/ship-invoice-items-dynamics-365-business-central/).

## Katso myös

[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Varastonhallinnan yleiskatsaus](design-details-warehouse-management.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
