---
title: Nimikkeiden siirtäminen ohjattua hyllytystä ja poimintaa käyttävissä fyysisissä varastoissa
description: Tässä artikkelissa käsitellään nimikkeiden siirtämistä ohjattua hyllytystä ja poimintaa käyttävissä sijainneissa.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7351,'
---

# <a name="move-items-in-advanced-warehouse-configurations-that-use-directed-put-away-and-pick" />Nimikkeiden siirtäminen ohjattua hyllytystä ja poimintaa käyttävissä fyysisen varastoinnin laajennetuissa määrityksissä

Nimikkeitä voidaan varastopaikkojen välillä ilman lähdeasiakirjasta peräisin olevaa kysyntää. Näin voidaan toimia esimerkiksi seuraavien toimintojen osana:

* Fyysisen varaston järjestäminen uudelleen.
* Nimikkeiden tuominen tarkastusalueelle.
* Nimikkeiden poistaminen väliaikaisesti fyysisen varastoinnin poimintavarastopaikoista esimerkiksi myyntiesittelyyn esittelykappaleiksi.
* Ylimääräisten nimikkeiden siirtäminen tuotantoalueelle, jos kyse on jollakin materiaaliottomenetelmällä määritetyistä komponenteista.
* Tuotettujen tai koottujen nimikkeiden siirtäminen tuotanto- tai kokoonpanoalueelta fyysiseen varastoon.
* Nimikkeiden siirtäminen irtotavaran varastointialueelta poimintaa käytettyihin varastopaikkoihin.

Nimikkeiden siirtäminen määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Niissä fyysisen varaston määrityksissä, joissa **Ohjattu poiminta ja hyllytys** on otettu sijainneissa käyttöön vaihtopainikkeilla, suunnittelemattomat varastosiirrot voidaan rekisteröidä seuraavilla sivuilla:  

* Siirtotyökirja
* Fyysisen varaston sisäinen poiminta
* Fyysisen varaston sisäinen hyllytys
* F.var. uudelleenluokit. pvk:t

**Siirtotyökirja**-, **Fyysisen varaston sisäinen poiminta**- ja **Fyysisen varaston sisäinen hyllytys** -sivut toimivat samalla tavoin. Varastotoimintoja voi valmistella näillä sivuilla varastotyöntekijöille. Erot muodostuvat kuhunkin sivuun liitettyjen lisätoimintojen sekä eri työntekijöiden todennäköisesti suorittamien erilaisten varastotoimintojen vuoksi:

* Siirtotyökirjan avulla voidaan täyttää korkealle luokiteltuja poiminnan varastopaikkoja muiden varastopaikkojen nimikkeillä
* Hyllytykset käyttävät hyllytysmalleja
* Poiminta käyttää varastopaikkojen luokittelua ja saatavuutta

## <a name="warehouse-movement-worksheet" />Fyysisen varaston siirtotyökirja

### <a name="to-move-items-with-the-warehouse-movement-worksheet" />Siirrä nimikkeitä fyysisen varastoinnin siirtotyökirjan kanssa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston siirron työkirja** ja valitse sitten liittyvä linkki.  
2. Työkirjan rivien kentät täytetään manuaalisesti. Rivit voidaan vaihtoehtoisesti täyttää automaattisesti jollakin seuraavista toiminnoista:

    * **Hae var.paikan sisältö** täyttää työkirjan riveille määritettyjen varastopaikkojen sisällön.
    * **Laske var.paikan täydennys** ehdottaa täydennystä korkean luokittelun varastopaikoista matalamman luokittelun varastopaikkoihin.

    > [!NOTE]  
    > Jos nimike täyttää seuraavan luettelon ehdot, **Lähtöalue**- ja **Var.paikasta**-kentät ovat tyhjät. [!INCLUDE [prod_short](includes/prod_short.md)] laskee, mistä nimikkeet siirretään vain **Luo varaston siirto** -toimintoa käytettäessä.  
    >  
    > * Nimikkeellä on vanhenemispäivämäärä.  
    > * **FEFO-poiminta** on otettu valintapainikkeella käyttöön sijainnissa.  
    > * Käytössä on **Laske var.paikan täydennys**-toiminto.  

3. Varaston siirto luodaan valitsemalla **Luo varaston siirto** -toiminto. Kun siirto on valmis, se voidaan rekisteröidä.  

### <a name="to-register-the-warehouse-movement" />F. varasoinnin siirron rekisteröinti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Var.siirrot** ja valitse sitten vastaava linkki.  
2. Avaa rekisteröitävä varaston siirtoasiakirja.  
3. Määritä **Aseta**-riveillä missä, mikä ja mihin mennessä nimike siirretään, valitsemalla **Alueen koodi**-, **Varastopaikan koodi**-, **Käsiteltävä määrä**- tai **Eräpäivä**-kenttien arvot.  
4. Määritä **Ota**-rivien **Käsiteltävä määrä** -kentässä varastopaikan sisällön siirrettävä määrä. Tätä kenttää voi muokata vain **Ota**-riveillä. 

    > [!NOTE]
    > Jos yhden rivin nimikkeet on poimittava useasta varastopaikasta tai asetettava useaan varastopaikkaan esimerkiksi siksi, että määritetty varastopaikka on täynnä, käytä **Rivit**-pikavälilehden **Jaa rivi** -toimintoa. Toiminto luo rivin jäljellä olevalle käsiteltävälle määrälle.
 
5. Kaikki **Määrä**-kentässä määritetyt ehdotetut määrät rekisteröidään valitsemalla **Täytä autom. käsiteltävä määrä** -toiminto.  
6. Valitse **Rekisteröi**-toiminto.  

> [!NOTE]  
> Ohjattua hyllytystä ja poimintaa käyttävissä sijainneissa ei voi siirtää manuaalisesti **VASTAANOTTO**-tyyppisten varastopaikkojen nimikkeitä, sillä niitä ei vielä pidetä saatavana olevana varastona. Näiden varastopaikkojen nimikkeet on hyllytettävä, jonka jälkeen niitä voi käyttää varaston siirroissa.

## <a name="internal-pick" />Sisäinen poiminta

### <a name="to-create-an-internal-pick" />Sisäisen poiminnan luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **F.var. sis. poim.** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.
3. Anna **Nro** Kirjoita **Yleiset**-pikavälilehden **Sijaintikoodi**- ja **Varastopaikkakoodiin**-kentän arvot. **Varastopaikkakoodiin**-kentässä määritetään varastopaikka, johon haluat sijoittaa keräillyt nimikkeet. Tuotannon yhteydessä tämä varastopaikka olisi saapuvan tuotannon varastopaikka tai avoin tuotannon varastopaikka. Muita tarkoituksia varten tulee valita sellainen varastopaikkakoodi, jonka varastopaikan tyyppiä ei käytetä ohjelmassa poimimiseen – todennäköisesti se on välivarastoinnin, toimituksen tai erityistarkoituksen varastopaikka.  
4. Valitse nimike **Nimikkeen nro** -kentästä ja täytä määrät, jotka haluat poimia.  
5. Valitse **Luo poiminta** -toiminto. Fyysisen varastoinnin poimintaohje on nyt valmis varaston työntekijälle suoritettavaksi. Vaihtoehtoisesti voidaan valita **Vapautus**-toiminto ja luoda fyysisen varastoinnin poiminnat käyttämällä **Poimintatyökirja**-sivua. Lisätietoja poimintatyökirjoista on kohdassa [Poiminta-asiakirjojen joukkoluonti poimintatyökirjan avulla](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. Kun poiminta on valmis, se voidaan rekisteröidä.  

### <a name="to-register-the-warehouse-pick" />Fyysisen varasoinnin poiminnan rekisteröinti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poiminnat** ja valitse sitten vastaava linkki.  

    Jos tiettyä poimintaa on käsiteltävä, se valitaan luettelosta. Vaihtoehtoisesti luetteloa suodattamalla voidaan etsiä itselle määritetyt poiminnat.  
2. Jos **Määritetty käyttäjätunnus** -kenttä on tyhjä, syötä tunnus tarvittaessa itse.  
3. Poimi nimikkeet.  

    Koska fyysinen varasto on määritetty käyttämään ohjattua hyllytystä ja poimintaa, varastopaikan luokittelu määrittää varastopaikan, josta poiminta suoritetaan. Varastopaikkoja ehdotetaan poimintarivillä. Ohjeissa on ainakin kaksi erillistä otto- ja asetustoimintojen riviä.  

4. Kun nimikkeet on poimittu ja asetettu toimitusalueelle tai toimituksen varastopaikkaan, valitse **Rekisteröi poiminta** -toiminto.  

## <a name="internal-put-away" />Sisäinen hyllytys

### <a name="to-create-an-internal-put-away" />Sisäisen hyllytyksen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **F.var. sis. hyllytys** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.
3. Anna **Nro** ja **Sijaintikoodi**.
4. Täytä kunkin fyysiseen varastoon siirrettävän nimikkeen rivi. **Nimikenro**- ja **Määrä**-kentät ovat pakollisia.

    > [!NOTE]  
    > Jos nimike valitaan **Nimikenro**-kentässä, **Varastopaikan sisältö**- eikä **Nimikkeet**-sivu avautuu. Tämä sivu avautuu sen vuoksi, että hyllytettävä nimike on määritetty tiettyyn varastopaikkaan (*varastopaikan sisältö*), joten kyse ei ole mistä tahansa nimikkeestä. Lisäksi varastopaikka, josta nimike on otettava, on jo tiedossa. Jos **Var.paikasta**-kenttä on täytetty, kyseinen arvo suodattaa varastopaikan sisällön.

5. Rivit voidaan täyttää koko varastopaikan sisällöllä tai sijainnin varastopaikkojen suodatetulla sisällöllä valitsemalla **Hae var.paikan sisältö** -toiminto.  
6. Valitse **Luo hyllytys** -toiminto. Varastotyöntekijän fyysisen varastoinnin hyllytysohje on nyt valmis. Vaihtoehtoisesti **Vapautus**-toiminnon valinta luo fyysisen varastoinnin hyllytykset käyttämällä **Hyllytystyökirja**-sivulla. Lisätietoja hyllytystyökirjoista on kohdassa [Hyllytysasiakirjojen joukkoluonti hyllytystyökirjan avulla](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. Kun hyllytys on valmis, se voidaan rekisteröidä.  

### <a name="to-register-the-warehouse-put-away" />Fyysisen varastoinnin hyllytyksen rekisteröinti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyllytykset** ja valitse sitten vastaava linkki.
2. Avaa fyysisen varaston hyllytys, joka on valmis käsiteltäväksi.  
3. Lisää käyttäjätunnus tarvittaessa hyllytyksen käsittelyn alussa.  

    Hyllytysprosessi voidaan optimoida lajittelemalla hyllytysrivit erilaisten ehtojen perusteella. Lajitteluperusteena voi käyttää esimerkiksi nimikettä, hyllynumeroa tai eräpäivää.

    * Jos kunkin vastaanottorivin Ota- ja Aseta-rivit eivät ole peräkkäiset ja niiden halutaan olevan peräkkäisiä, järjestä rivit valitsemalla **Nimike** **Järjestämistapa**-kentässä.  
    * Jos varastopaikan luokittelut vastaa fyysisen varaston fyysistä asettelua, järjestä työt varastopaikkojen sijainnin perusteella käyttämällä **Varastopaikan luokittelu** -järjestämistapaa.  

4. Tee hyllytys.

    Kustakin sisäisestä hyllytysrivistä on tullut vähintään kaksi riviä fyysisen varastoinnin hyllytyksessä.  

    * Ensimmäisellä rivillä, jolla **Toiminnon tyyppi** -kentässä on **Ota**, ilmaistaan, missä vastaanottoalueella nimikkeet sijaitsevat. Tällä rivillä olevaa aluetta ja varastopaikkaa ei voi muuttaa.  
    * Seuraava rivi, jonka **Toiminnon tyyppi** -kentässä on **Aseta**, osoittaa, mihin nimikkeet asetetaan fyysisessä varastossa. Jos yhdellä vastaanottorivillä vastaanotetaan suuri määrä nimikkeitä, nimikkeet on ehkä hyllytettävä useisiin varastopaikkoihin, jolloin kullakin varastopaikalla on Aseta-rivi.  

5. Kun olet asettanut kaikki nimikkeet varastopaikkoihin ohjeiden mukaisesti, valitse **Rekisteröi hyllytys** -toiminto.  

## <a name="to-register-a-movement-that-has-already-happened" />Aiemmin tehdyn varaston siirron rekisteröinti

Jos toisiin varastopaikkoihin ilman hyllytystä, poimintaa tai varaston siirtoa jo siirretyt nimikkeet on rekisteröitävä, varaston siirto voidaan rekisteröidä **F.var. uud.luokpäiväkirja** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **F.var. uud.luokpäiväkirja** ja valitse sitten vastaava linkki.  
2. Täytä **Nimikkeen nro**-, **Aluekoodista**-, **Var.paikasta**-, **Aluekoodiin**- ja **Varastopaikkakoodiin**-kentät.  
3. Valitse **Rekisteröi**-toiminto.  

## <a name="see-related-microsoft-training" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/manage-internal-warehouse-processes/)

## <a name="see-also" />Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
