---
title: Varaston laskeminen ja muuttaminen
description: 'Kuvaa, miten fyysistä varastoa lasketaan ja miten varastoasiakirjoja käytetään käytettävissä olevan varaston säätämiseen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 04/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="count-and-adjust-inventory-using-documents"></a>Varastojen laskenta ja muutos asiakirjoja käyttämällä

Voit inventoida nimikkeet käyttämällä inventointitilauksen ja inventointitallennuksen asiakirjoja. **Inventointitilaus**-sivulla järjestetään täydellinen inventointiprojekti, kuten yksi kussakin toimipisteessä. **Inventointitallennus**-sivulla voi siepata ja ilmoittaa nimikkeiden todellisen määrän. Yhdelle tilaukselle voidaan luoda useita tallenteita esimerkiksi nimekeryhmiä jakamiseen eri työntekijöille.

Jokaisesta tallenteesta voidaan tulostaa **Inventointitallennus**-raportti, ja raportin tyhjiin määräkenttiin voi syöttää lasketun varaston. Kun inventointi on valmis ja määrät on lisätty **Inventointitallennus**-sivulla, valitse **Valmis**-toiminto. Toiminto siirtää määrät liittyville riveille **Inventointitilaus**-sivulla. [!INCLUDE [prod_short](includes/prod_short.md)] varmistaa, että nimikemäärää ei voi kirjata kahdesti.  

> [!NOTE]
> Asiakirjoja hyödynnetään inventoinnissa, mikä parantaa hallintaa ja tukee inventoinnin jakamista useille työntekijöille. Tehtävän voi suorittaa myös käyttämällä päiväkirjoja, kuten **Varastopäiväkirjat**- ja **F. var. inventointipäiväkirjat** -sivuja. Lisätietoja on kohdassa [Varaston laskeminen, muuttaminen ja uudelleenluokitus käyttämällä päiväkirjoja](inventory-how-count-adjust-reclassify.md). Tässä artikkelissa käsitellään asiakirjojen käyttämistä inventoinnissa.
>
> Jos varastossa käytetään vyöhykkeitä, inventointitilauksia ei voi käyttää. Fyysisten varastotapahtumien laskemiseen käytetään sen sijaan **Fyysisen varaston inventointipäiväkirja** -sivua, ennen kuin ne synkronoidaan nimiketapahtumien kanssa.

Asiakirjoja hyödyntävä varaston laskenta sisältää seuraava yleiset vaiheet:

1. Luo inventointitilaus siten, että nimikkeiden odotetut määrät on täytetty valmiiksi.
2. Luo tilauksesta vähintään yksi inventointitallennus.
3. Lisää inventoitujen nimikkeiden määrät tallenteisiin esimerkiksi tulosteisiin kerättyjen tietojen mukaisesti ja määritä sen arvoksi **Valmis**.
4. Täytä ja kirjaa inventointitilaus.

## <a name="to-create-a-physical-inventory-order"></a>Inventointitilauksen luominen

Inventointitilaus on valmis asiakirja, joka koostuu inventointitilauksen otsikosta ja tilausriveistä. Inventointitilauksen otsikossa selitetään, miten inventointi tehdään. Tilausriveillä on tietoja nimikkeistä ja niiden sijainneista.

Inventointitilauksen rivit luodaan yleensä lisäämällä nykyinen varasto tilauksen riveinä **Laske rivit** -toimintoa käyttämällä. Toisen avoimen tai kirjatun inventointitilauksen rivit voidaan täyttää myös **Kopioi asiakirja** -toiminnolla. Seuraavassa toimintaohjeessa käsitellään vain **Laske rivit** -toiminnon käyttöä.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston tilaukset** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Yleinen**-pikavälilehden pakolliset kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Laske rivit** -toiminto.
5. Valitse tarvittavat vaihtoehdot.
6. Määritä suodattimet sisällyttämään esimerkiksi vain ensimmäisessä tallenteessa inventoitavien nimikkeiden alijoukon.

    > [!TIP]
    > Jos tarkoituksena on, että varaston laskentaan osallistuu useita työntekijöitä, eri suodattimet määritetään aina **Laske rivit** -toimintoa käytettäessä. Tällä tavoin tilaukseen täytetään vain käyttäjän kirjaamien varastonimikkeiden alijoukko. Tällä tavoin riski nimekkeiden inventoinnista kahdesti on vähäinen, kun useille työntekijöille luodaan useita inventointitallenteita. Lisätietoja on kohdassa [Inventointitallennuksen luominen](#to-create-a-physical-inventory-recording).

7. Valitse **OK**-painike.

Tilaukseen lisätään rivi kullekin nimikkeelle, joka on valitussa sijainnissa ja joka on valittujen suodattimien ja vaihtoehtojen mukainen. Nimikkeille, joille on määritetty nimikeseuranta, valitaan **Käytä nimikeseurantaa** -valintaruutu. Tietoja odotetuista sarja- ja eränumeroista saadaan valitsemalla ensin **Rivit** ja sitten **Nimikkeen seurantarivit**. Lisätietoja on kohdassa [Nimikeseurannan käsittely varastoa laskettaessa](#handle-item-tracking-when-counting-inventory).

Nyt voidaan luoda vähintään yksi tallenne. Nämä tallenteet ovat inventointia suorittaville työntekijöille tarkoitettuja ohjeita.  

> [!NOTE]
> Jos käytössä on pakettikohtainen seuranta, myös kollinumerot sisältävä varastoa voidaan laskea ja muuttaa asiakirjojen avulla. Tämän ominaisuuden käyttö aloitetaan ottamalla **Ominaisuuspäivitys: Ota paketin seuranta käyttöön fyysisen varaston tilauksissa** käyttöön **Ominaisuuksien hallinta** -sivulla. Vaikka aiemmin luodut inventointitilaukset päivitetään, [!INCLUDE [prod_short](includes/prod_short.md)] ei voi täyttää **Paketin nro** -kenttää. Nämä rivit on luotava uudelleen **Inventointitilaus**-sivun **Laske rivit** -toiminnolla.
>
> Pakettinumerot voidaan syöttää nimikkeille pakettiseurantaa varten **Inventointitallennusrivit**-sivulla. Tallenne viimeistellään valitsemalla **Valmis**.
>
> Kun **Valmis** on valittu **Inventointitilaus**-sivulla, [!INCLUDE [prod_short](includes/prod_short.md)] laskee paketin ja muiden nimikeseurannan tietojen väliset erot sekä tekee positiivisia tai negatiivisia muutoksia.

## <a name="to-create-a-physical-inventory-recording"></a>Inventointitallennuksen luominen

Kullekin inventointitallennuksella voidaan luoda vähintään yksi inventointitallennusasiakirja, joihin työntekijät voivat syöttää lasketut määrät. Työntekijät voivat syöttää määrät manuaalisesti tai lukulaitteella.

Tallenne luodaan oletusarvoisesti kaikille liittyvässä inventointitilauksessa oleville riveille. Jos kyse on jaetusta laskennasta, työntekijöitä voidaan estää laskemasta sama nimike useita kertoja täyttämällä inventointitilaus vähitellen määrittämällä suodattimet **Laske rivit** -erätyössä. Inventointitallennus luodaan sitten **Vain rivit, jotka eivät ole tallenteissa** -valintaruutu valittuna. Tämä asetus varmistaa, että kukin uusi tallenne sisältää vain muista tallenteista poikkeavia nimikkeitä.

Manuaalisesta laskennassa voidaan tulostaa **Inventointitallennus**-raportti, jonka tyhjään sarakkeeseen varastotyöntekijät voivat lisätä lasketut määrät. Kun inventointi on valmis, tallennetut määrät lisätään liittyville **Inventointitallennus**-sivun riveille. Tallennetut määrät siirretään lopuksi liittyvään inventointitilaukseen määrittämällä tilaksi **Valmis**.

1. Valitse sillä **Inventointitilaus**-sivulla, joka sisältää yhdessä tallennuksessa laskettavien nimikkeiden rivit, **Luo uusi tallennus** -toiminto.
2. Valitse asetukset ja määritä suodattimet tarpeen mukaan.
3. Valitse **OK**-painike.
4. Lataa jokainen inventoitava nimikejoukko liittyvään inventointitilaukseen ja toista vaiheet 1–3 siten, että **Vain rivit, jotka eivät ole tallenteissa** -valintaruutu on valittuna.
5. Avaa **Inventointitallennusluettelo**-sivu valitsemalla **Tallennukset**-toiminto.
6. Avaa liittyvä tallenne.
7. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.
8. Luo nimikeseurantaa käyttäville nimikkeille kullekin erä- tai sarjanumerokoodille lisärivi valitsemalla ensin **Toiminnot**- ja sitten **Kopioi rivi** -toiminto. Lisätietoja on kohdassa [Nimikeseurannan käsittely varastoa laskettaessa](#handle-item-tracking-when-counting-inventory).  
9. Valmistele fyysinen asiakirja, johon työntekijät voivat kirjata muistiin lasketut määrät, valitsemalla **Tulosta**-toiminto.

## <a name="to-finish-a-physical-inventory-recording"></a>Inventointitallennuksen valmistuminen

Työntekijöiden laskemat määrät tallennetaan [!INCLUDE [prod_short](includes/prod_short.md)]iin.

1. Valitse **Inventointitallennusluettelo**-sivulla viimeisteltävä inventointitallenne ja valitse sitten **Muokkaa**-toiminto.
2. Täytä laskettu määrä **Rivit**-pikavälilehdessä kunkin rivin **Määrä**-kenttään.
3. Jos nimikkeellä on sarja- tai eränumero (**Käytä nimikeseurantaa** -valintaruutu on valittu), lisää lasketut määrät nimikkeen sarja- ja eränumeroriveille. Lisätietoja on kohdassa [Nimikeseurannan käsittely varastoa laskettaessa](#handle-item-tracking-when-counting-inventory).
4. Valitse **Tallennettu**-valintaruutu kullakin rivillä.
5. Kun olet antanut kaikki inventointitallenteen tiedot, valitse **Valmis**-toiminto. Huomaa, että **Tallennettu**-valintaruudun on oltava valittuna kaikilla riveillä.

    > [!NOTE]
    > Kun inventointitallenne on valmis, kukin rivi siirretään sitä täsmälleen vastaavalle liittyvän inventointitilauksen riville. Vastaavuus edellyttää, että **Nimikenro**-, **Varianttikoodi**-, **Sijaintikoodi**- ja **Varastopaikan koodi** -kenttien arvot ovat samat tallenteessa ja tilausriveillä.>
    > 
    > Jos vastaavaa inventointitilausriviä ei ole ja jos **Salli tallennus ilman tilausta** -valintaruutu on valittu, uusi rivi lisätään ja **Tallennettu ilman tilausta** -valintaruutu valitaan liittyvän inventointitilauksen rivillä. Muussa tapauksessa avautuu virhesanoma ja prosessi peruutetaan.> Jos useat inventointitallennuksen rivit vastaavat inventointitilauksen riviä, sanoma avautuu ja prosessi peruutetaan. Jos kaksi täysin samanlaista inventointiriviä päätyy jostain syystä inventointitilaukseen, voit ratkaista asian toiminnolla. Lisätietoja on kohdassa [Inventointitilausrivien kaksoiskappaleiden löytäminen](#to-find-duplicate-physical-inventory-order-lines).

## <a name="to-complete-a-physical-inventory-order"></a>Inventointitilauksen viimeisteleminen

Kun inventointitallennus on valmis, liittyvän inventointitilauksen **Tallennettujen määrä (perus)** -kenttä päivitetään lasketuilla (tallennetuilla) arvoilla ja **Tallennuksessa**-valintarivi valitaan. Jos laskettu määrä poikkeaa odotetusta määrästä, ero näkyy **Posit. määrä (perus)**- tai **Negat. määrä (perus)**-kentässä.

Odotetut määrät ja mahdolliset nimikeseurantaa käyttävien nimikkeiden tallennetut erot ovat käytettävissä valitsemalla **Rivit**-toiminto. Valitse sitten **Nimikkeen seurantarivit** -toiminnolla erilaisia inventointiin sisältyviä sarja- ja eränumeroiden näkymiä.

Voit valita myös **Inventointitilauksen erotus** -toiminnon ja tarkastella odotetun määrän ja lasketun määrän välisiä eroja.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>Inventointitilausrivien kaksoiskappaleiden löytäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston tilaukset** ja valitse sitten vastaava linkki.
2. Avaa inventointitilaus, jonka rivien kaksoiskappaleita halutaan tarkastella.
3. Valitse **Näytä rivien kaksoiskappaleet** -toiminto.

Inventointitilausrivien mahdolliset kaksoiskappaleet ovat näkyvissä, joten voit poistaa ne ja säilyttää yhden rivin, jolla on yksilöllinen **Nimikenro**-, **Varianttikoodi**-, **Sijaintikoodi**- ja **Varastopaikan koodi** -kenttien arvojoukko.

### <a name="to-post-a-physical-inventory-order"></a>Inventointitilauksen kirjaaminen

Kun inventointitilaus on valmis ja sen tilaksi on muuttunut **Valmis**, se voidaan kirjata. Inventointitilauksen tilaksi voi määrittää **Valmis** vain siinä tapauksessa, että seuraavat ehdot täyttyvät:

- Kaikkien liittyvien inventointitallenteiden tila on **Valmis**.
- Jokainen inventointitilausrivi on laskettu vähintään yhdellä varastotallennusrivillä.
- **Tallennusriveillä**- ja **Oletettu määrä laskettu** -valintaruudut on valittu kaikille inventointitilausriveille.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston tilaukset** ja valitse sitten vastaava linkki.
2. Valitse ensin viimeisteltävä inventointitilaus ja sitten **Muokkaa**-toiminto.

    Tallennettu määrä näkyy **Inventointitilaus**-sivun **Tallennettujen määrä (perus)** -kentässä.
3. Valitse **Valmis**-toiminto.

    **Tila**-kentän arvo on **Valmis**. Tilausta voidaan nyt muuttaa vain valitsemalla **Avaa uudelleen** -toiminto.
4. Kirjaa tilaus valitsemalla **Kirjaa**-toiminto ja valitsemalla sitten **OK**-painike.

    Nimiketapahtumat päivitetään nyt mahdollisten liittyvien nimikeseurantatapahtumien ohella.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

### <a name="to-view-posted-physical-inventory-orders"></a>Kirjattujen inventointitilausten tarkasteleminen

Inventointitilaus poistetaan kirjaamisen jälkeen, ja asiakirjaa voidaan tarkastella ja arvioida kirjattuna inventointitilauksena. Kirjattu tilaus sisältää myös inventointitallennukset ja mahdolliset kommentit.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut fyysisen varaston tilaukset** ja valitse sitten vastaava linkki.
2. Valitse **Kirjatut inventointitilaukset** -sivulla tarkasteltava kirjattu inventointitilaus ja valitse sitten **Näytä**-toiminto.
3. Voit tarkastella liittyvien inventointitallennusten luetteloa valitsemalla **Tallennukset**-toiminnon.

## <a name="handle-item-tracking-when-counting-inventory"></a>Nimikeseurannan käsittely varastoa laskettaessa

Nimikeseuranta liittyy nimikkeille määritettyihin sarja- tai eränumeroihin. Jos laskettava nimike on tallennettu varastoon esimerkiksi 10 erilaisena eränumerona, työntekijän on voitava tallentaa, mitkä eränumerot ovat varastossa ja kuinka monta yksikköä kutakin erää on varastossa. Lisätietoja on kohdassa [Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md).

**Käytä nimiseurantaa** -valintaruutu valitaan inventointitilausriveillä automaattisesti, jos nimikkeelle on määritetty nimikeseurantakoodi. Valintaruutu voidaan kuitenkin valita tai tyhjentää manuaalisesti.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Esimerkki – nimekeseuratun nimikkeen inventointitallennuksen valmistelu

Oletetaan, että nimikkeen A fyysinen varasto on tallennettu varastoon 10 eri sarjanumerolla.

1. Valitse nimikkeen tallennusrivillä **Käytä nimiseurantaa** -valintaruutu.
2. Valitse **Sarjanumero**-kentässä ensimmäinen sarjanumero, joka nimikkeellä on varastossa, ja valitse sitten **OK**-painike.

    Kopioi seuraavaksi ensimmäisen nimikeseuratun nimikkeen rivi. Voit lisätä tällä tavoin varastoon tallennettujen sarjanumeroiden numeroa vastaavia lisärivejä.

3. Valitse ensin **Toiminnot** ja sitten **Kopioi rivi**.
4. Syötä **9** **Kopioi inventointitallennusrivi** -sivun **Kopioiden lukumäärä** -kenttään ja valitse sitten **OK**-painike.
5. Valitse ensimmäisen rivin **Sarjanumero**-kentässä nimikkeen seuraava sarjanumero.
6. Toista vaihe 5 seuraavan kahdeksan sarjanumeron osalta. Varmista, ettet valitse samaa numeroa kahdesti.
7. Valmistele tuloste, johon työntekijät kirjoittavat lasketut nimikkeet ja sarja- tai eränumeron, valitsemalla **Tulosta**.

Huomaa, että **Inventointitallennus**-raportissa nimikkeellä A on 10 riviä – yksi kullekin sarjanumerolle.

### <a name="example---record-and-post-counted-lot-number-differences"></a>Esimerkki – laskettujen eränumeroerojen tallentaminen ja kirjaaminen

Eräseurattu nimike tallennetaan varastoon LOT-numerosarjaan.

**Oletettu varasto**:

|Eränro|määrä|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Yhteensä|120|

**Tallennetut määrät**:

|Eränro|määrä|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|20|
|LOT1006|10|
|Yhteensä|112|

**Kirjattavat määrät**:

|Eränro|Oletettu määrä|Tallennettu määrä|Kirjattava määrä|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|20|-10|
|LOT1006|10|0|-10|
|Yhteensä|120|112|-8|

**Inventointitilaus**-sivun **Negat. määrä (perus)** -kentän arvo on **8**. Tilausrivin **Inventoinnin nimikeseurantaluettelo** -sivulla näkyy kunkin eränumeron positiivinen tai negatiivinen määrä.

## <a name="inventory-documents"></a>Varastoasiakirjat

Seuraavat asiakirjatyypit ovat käteviä fyysisen varaston hallinnassa:

* **Varaston vastaanottojen** avulla voi rekisteröidä nimikkeiden positiiviset muutokset määrän, laadun ja kustannuksen perusteella.
* **Varastotoimitusten** avulla voi kirjata pois puuttuvia tai vaurioituneita tuotteita.

Nämä asiakirjat voidaan tulostaa koska tahansa. Ne voidaan vapauttaa ja avata uudelleen, minkä lisäksi niiden otsikkoon voidaan määrittää yleisiä arvoja, kuten dimensioita. Asiakirjat voidaan tulostaa uudelleen kirjaamisen jälkeen **Kirjatut varastovastaanotot**- ja **Kirjatut varastolähetykset** -sivuilla.

> [!NOTE]
> Ennen kuin näitä asiakirjoja voidaan käyttää, niille on luotava tunnisteet määrittämällä numerosarja. Lisätietoja on kohdassa [Varastoasiakirjojen numeroinnin määrittäminen](#to-set-up-numbering-for-inventory-documents).

### <a name="to-set-up-numbering-for-inventory-documents"></a>Varastoasiakirjojen numeroinnin määrittäminen

Seuraavaksi käsitellään varastoasiakirjojen numeroinnin määrittämistä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten vastaava linkki.
2. Määritä seuraavissa **Numerointi**-pikavälilehden kentissä asiakirjojen numerosarjat:

   - **Varaston vastaanoton nrot**  
   - **Kirjattujen varastovastaanottojen nrot**  
   - **Varastotoimitusten nrot**  
   - **Kirjattujen varastotoimitusten nrot**  

### <a name="to-create-and-post-an-inventory-document"></a>Varastoasiakirjan luominen ja kirjaaminen

Seuraavaksi käsitellään varastovastaanoton luomista, tulostamista ja kirjaamista. Varastotoimitusten vaiheet ovat vastaavanlaiset.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston vastaanotot** ja valitse sitten vastaava linkki.  
2. Valitse **Varaston vastaanotto** -sivulla **Sijaintikoodi**-kentän sijainti ja täytä sitten jäljellä olevat kentät tarpeen mukaan.
3. Valitse **Rivit**-pikavälilehden **Nimike**-kentässä varastonimike. Anna lisättävien nimikkeiden lukumäärä **Määrä**-kentässä.
4. **Varaston vastaanotto** -raportin voi tulostaa **Varaston vastaanotto** -sivulla valitsemalla **Tulosta**-toiminnon.

**Varaston vastaanotto** -sivulla on käytössä seuraavat toiminnot:

- Seuraavan käsittelyvaiheen tila määritetään **Vapauta**- tai **Avaa uudelleen** -toiminnolla.  
- Kirjaa varaston vastaanotto valitsemalla **Kirjaa**-toiminto tai kirjaa vastaanotto ja tulosta testiraportti valitsemalla **Kirjaa ja tulosta**.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="printing-inventory-documents"></a>Varastoasiakirjojen tulostaminen

Eri vaiheissa tulostettavat raportit voidaan määrittää valitsemalla jokin seuraavista vaihtoehdoista **Raportin valinta – varasto** -sivun **Käyttö**-kentässä:

* Varaston vastaanotto
* Varastotoimitus
* Kirjattu varaston vastaanotto
* Kirjattu varastotoimitus

> [!NOTE]
> Käytettävissä olevat raportit voivat vaihdella maan tai alueen lokalisoinnin mukaan. Perussovellus ei sisällä asetteluja.

## <a name="see-also"></a>Katso myös

[Varaston laskeminen, muuttaminen ja uudelleenluokitus käyttämällä päiväkirjoja](inventory-how-count-adjust-reclassify.md)  
[Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
