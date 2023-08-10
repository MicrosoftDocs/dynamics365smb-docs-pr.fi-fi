---
title: Nimikkeiden vastaanottaminen
description: Tässä artikkelissa käsitellään yleisesti erilaisia tapoja vastaanottaa nimikkeitä fyysisessä varastossa fyysisen varaston vastaanottona.
author: brentholtorf
ms.author: bholtorf
ms.topic: how-to
ms.date: 09/02/2022
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
---
# <a name="receive-items-with-warehouse-receipts"></a>Nimikkeiden vastaanottaminen fyysisen varasto vastaanottona

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeiden vastaanottoon ja hyllytykseen on neljä tapaa, jotka käsitellään seuraavassa taulukossa.

|Tapa|Saapuva prosessi|Vaadi vastaanotot|Vaadi hyllytykset|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta||Otettu käyttöön|Perus: tilauksittain.|  
|S|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta|Otettu käyttöön||Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lisätietoja saapuvien nimikkeiden käsittelemisestä on kohdassa [Fyysisen varaston saapuvien työnkulku](design-details-inbound-warehouse-flow.md).

Seuraavassa artikkelissa viitataan aiemman taulukon menetelmiin C ja D.

## <a name="receive-items-with-a-warehouse-receipt"></a>Nimikkeiden vastaanottaminen fyysisen varasto vastaanottona

Kun nimikkeet saapuvat fyysiseen varasto, joka on määritetty käsittelemään fyysisen varaston vastanotot, vastaanoton käynnistäneet vapautetun lähdeasiakirjan rivit on haettava. Varastopaikkoja käytettäessä voidaan joko hyväksyä oletusvarastopaikka tai määrittää varastopaikka, johon nimikkeet asetetaan. Jälkimmäistä vaihtoehtoa voidaan edellyttää, kun nimike vastaanotetaan ensimmäisen kerran. Sen jälkeen syötetään vastaanotettujen nimikkeiden määrä ja kirjataan vastaanotto.  

Fyysisen varaston vastaanotto voidaan luoda jommallakummalla tavalla:

* Push-menetelmässä työ tehdään tilauskohtaisesti. Lähdeasiakirjassa, kuten ostotilauksessa, myyntipalautustilauksessa tai siirtotilauksessa, valitaan **Luo f. varastoinnin vastaanotto** -toiminto, joka luo fyysisen varastoinnin vastaanoton yhdelle lähdeasiakirjalle.
* Pull-menetelmässä lähdeasiakirjassa, kuten ostotilauksessa, myyntipalautustilauksessa tai siirtotilauksessa, **Vapauta**-toimintoa käytetään vapauttamaan asiakirja fyysiseen varastoon. Varastotyöntekijä luo ainakin yhdelle vapautetulle lähdeasiakirjalle **fyysisen varastoinnin vastaanoton**. Fyysisen varaston vastaanotto luodaan pull-menetelmässä seuraavaksi kuvattavalla tavalla. Fyysisen varaston vastaanotto luodaan pull-menetelmässä seuraavaksi kuvattavalla tavalla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston vastaanotot**, valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  

    Täytä **Sijaintikoodi**-kenttä **Yleinen**-pikavälilehdessä. Kun haet lähdeasiakirjan rivit, ohjelma kopioi otsikon tiedot kullekin riville.

    Jos sijainti edellyttää varastopaikkojen käyttöä, täytä **Varastopaikan koodi** -kenttä. Määritysten mukaan [!INCLUDE[prod_short](includes/prod_short.md)] voi lisätä varastopaikan koodin valmiiksi. Lisätietoja on kohdassa [Alueen ja varastopaikan koodit](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. Lähdeasiakirja voidaan hakea kahdella tavalla:

    1. Valitse **Hae lähdeasiakirjat** -toiminto. **Lähdeasiakirjat – saapuva** -sivu avautuu. Tällä sivulla voidaan valita vastaanottoa edellyttävät fyysiseen varastoon vapautetut lähdeasiakirjat.
    2. Valitse **Käytä suodat. kun haet lähd.d** -toiminto. **Suod. lähdeasiakirj. saamisek. – saapuva** -sivu avautuu. Sivulla voi valita lähdeasiakirjan suodattimen ja käyttää sitä. Kaikki vapautetut lähdeasiakirjan rivit, jotka täyttävät suodatusehdot, lisätään **F.varastoinnin vastaanotto** -sivulle. Lisätietoja on kohdassa [Lähdeasiakirjojen hakeminen suodattimia käyttämällä](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents).

4. Määritä vastaanotettava määrä.

    **Vastaanotettava määrä** -kenttään sisältää kunkin rivin avoimen määrän, mutta määrää voi muuttaa tarpeen mukaan. 

    **Vastaanotettava määrä** -kentän arvoksi määritetään kaikilla riveillä valitsemalla **Poista vastaanotettava määrä** -toiminto. Määrän määrittäminen nollaksi on kätevää esimerkiksi silloin, jos vastaanotettu päivitetään viivakoodin lukijalla. Avoimet määrät voidaan lisätä lähdeasiakirjasta uudelleen valitsemalla **Täytä autom. vast.ot. määrä** -toiminnon.  

    Jos fyysisen varaston vastaanottoasiakirjan vastaanotettu määrä on suurempi kuin tilattu määrä, toteutunut vastaanotettu määrä syötetään **Vastaanotettu määrä** -kenttään. Jos lisäys on määritetyn vastaanoton ylittävän määrän koodin toleranssin rajoissa, **Vastaanoton ylittävä määrä** -kenttä päivittyy näyttämään arvon, jolla **Määrä**-kenttä on ylitetty. Jos lisäys ylittää toleranssin, vastaanoton ylittävää määrää ei sallita.

5. Kirjaa fyysisen varastoinnin vastaanotto. Lähdeasiakirjojen määräkentät päivitetään ja nimikkeet lisätään varastoon.  

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

    > [!TIP]
    > Jos käytössä on fyysisen varastoinnin hyllytys, jolla viitataan menetelmään D artikkelin alussa olevassa taulukossa, nimikkeet on vastaanotettu, mutta niitä ei voi poimia, ennen kuin ne on hyllytetty. Lisätietoja nimikkeiden hyllyttämisestä on kohdassa [Nimikkeiden hyllyttäminen fyysisen varastoinnin hyllytyksenä](warehouse-how-to-put-items-away-with-warehouse-put-aways.md).
    >
    > Muussa tapauksessa kannattaa harkita **Kirjaa ja tulosta** -toiminnon käyttämistä. Tämä toiminto kirjaa vastaanoton ja tulostaa sen hyllytysohjeeksi, jossa näyttää, mihin nimike hyllytetään.

    > [!NOTE]  
    > Jos fyysisessä varastoinnissa käytetään laiturointia, voit tarkastaa, voidaanko nimikkeet laituroida ilman hyllytystä. Lisätietoja laituroinnista on kohdassa [Nimikkeiden laiturointi](warehouse-how-to-cross-dock-items.md).

## <a name="how-to-use-filters-to-get-source-documents"></a>Lähdeasiakirjojen hakeminen suodattimien avulla

Fyysisen varastoinnin vastaanoton **Suod. lähdeasiakirj. saamisek.** -sivua voidaan käyttää niiden vapautetun lähdeasiakirjan rivien hakemiseen, jotka määrittävät vastaanotettavat nimikkeet.

1. Valitse fyysisen varaston vastaanotossa **Käytä suodat. kun haet lähd.d** -toiminto.
2. Määritä uusi suodatin antamalla kuvaileva koodi **Koodi**-kenttään, valitse **Muokkaa**-toiminto.

    **Lähdeasiakirjan suodatinkortti – lähtevä** -sivu avautuu.

3. Määritä suodattimien avulla noudettavien lähdeasiakirjarivien tyyppi. Valittavissa on esimerkiksi lähdeasiakirjatyyppejä, kuten osto- tai siirtotilauksia.
4. Valitse **Suorita**.  

Kaikki suodatusehdot täyttävät vapautetut lähdeasiakirjan rivit lisätään sillä **F. varastoinnin vastaanotto** -sivulla, jossa suodattimet aktivointiin.

Voit tehdä niin monta suodatinyhdistelmää kuin haluat. Suodattimet tallennetaan **Suod. lähdeasiakirj. saamisek.** -sivulle, jossa ne ovat käytettävissä tulevaa käyttöä varten. Voit muuttaa ehtoja milloin tahansa valitsemalla **Muokkaa**-toiminnon.

## <a name="zone-and-bin-codes"></a>Alueen ja varastopaikan koodit

Vastaanotettaessa nimikkeitä, joiden fyysisen varastoinnin luokkakoodi ei ole sama kuin asiakirjan otsikon **Varastopaikkakoodi**-kentässä olevan varastopaikan luokkakoodi, otsikon **Varastopaikkakoodi**-kenttä on tyhjennettävä ennen lähdeasiakirjan rivien hakemista nimikkeitä varten.  
<!-- TBD, table with comparison of various options-->

Jos varastopaikat ovat sijainnissa pakollisia, alueen ja varastopaikan koodit lisätään fyysisen varaston vastaanottoasiakirjoihin seuraavasti:

* [!INCLUDE [prod_short](includes/prod_short.md)] käyttää ohjattua hyllytystä ja poimintaa käyttävissä laajennetuissa määrityksissä sijainnin **Sijaintikortti**-sivun vastaanoton varastopaikkakoodia. Jos vastaanoton varastopaikan koodia ei ole määritetty, mitään varastopaikkaa ei määritä. Jos nimikkeen ja vastaanoton varastopaikat eivät ole samat, vastaanoton varastopaikan koodi on tyhjä.
* Jos toimituksen varastopaikan koodia ei ole määritetty muissa määrityksissä, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää lähdeasiakirjan varastopaikan koodia.

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
