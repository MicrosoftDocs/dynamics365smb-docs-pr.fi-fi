---
title: Varaston laskeminen ja muuttaminen
description: Kuvaa, miten fyysistä varastoa lasketaan ja miten varastoasiakirjoja käytetään käytettävissä olevan varaston säätämiseen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, status, negative, positive, increase, decrease, inventory
ms.search.forms: 5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5b2e1e7a9ea7c6f2ed49c146e7e52ffdfa28c28c
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532671"
---
# <a name="count-and-adjust-inventory-using-documents"></a>Varastojen laskenta ja muutos asiakirjoja käyttämällä

Voit inventoida nimikkeet käyttämällä inventointitilauksen ja inventointitallennuksen asiakirjoja. **Inventointitilaus**-sivulla järjestetään täydellinen inventointiprojekti, kuten yksi kussakin toimipisteessä. **Inventointitallennus**-sivun avulla ilmoitetaan ja tallennetaan nimikkeiden varsinainen inventointi. Voit luoda yhdelle tilaukselle useita  tallenteita, jolloin voit esimerkiksi jakaa nimekeryhmiä eri työntekijöille.

Jokaisesta tallenteesta voidaan tulostaa **Inventointitallennus**-raportti. Tämän raportin määräkentät ovat tyhjiä, ja laskettu varasto voidaan sitten lisätä näihin kenttiin. Kun käyttäjä lopettaa inventoinnin ja määrät on lisätty **Inventointitallennus**-sivulla, valitse **Valmis**-toiminto. Määrät siirretään nyt liittyville riveille **Inventointitilaus**-sivulla. Toiminto varmistaa, ettei mitään nimikettä tallennetta kahdesti.  

> [!NOTE]
> Asiakirjoja hyödynnetään inventoinnissa, mikä parantaa hallintaa ja tukee inventoinnin jakamista useille työntekijöille. Tehtävän voi suorittaa myös käyttämällä päiväkirjojen, kuten **Varastopäiväkirjat**- ja **F. var. inventointipäiväkirjat**, sivuja. Lisätietoja on kohdassa [Varaston laskeminen, muuttaminen ja uudelleenluokitus päiväkirjojen avulla](inventory-how-count-adjust-reclassify.md). Tässä artikkelissa käsitellään inventointia asiakirjoja käyttämällä.
>
> Jos vyöhykkeet ovat käytössä, inventointitilauksia ei voi käyttää. Käytä sen sijaan **Fyysisen varaston inventointipäiväkirja** -sivua fyysisten varastointitapahtumien laskemiseen, ennen kuin ne synkronoidaan nimiketapahtumien kanssa.

Asiakirjoja hyödyntävä varaston laskenta sisältää yleisesti seuraavat vaiheet:

1. Luo inventointitilaus siten, että nimikkeiden odotetut määrät on täytetty valmiiksi.
2. Luo tilauksesta vähintään yksi inventointitallennus.
3. Lisää inventoitujen nimikkeiden määrät tallenteisiin esimerkiksi tulosteisiin kerättyjen tietojen mukaisesti ja määritä sen arvoksi **Valmis**.
4. Täytä ja kirjaa inventointitilaus.

## <a name="to-create-a-physical-inventory-order"></a>Inventointitilauksen luominen

Inventointitilaus on valmis asiakirja, joka koostuu inventointitilauksen otsikosta ja inventointitilausriveistä. Inventointitilauksen otsikossa selitetään, miten inventointi tehdään. Inventointitilauksen riveillä on tietoja nimikkeistä ja niiden sijainneista.

Inventointitilauksen rivit luodaan yleensä käyttämällä **Laske rivit** -toimintoa siten, että ne vastaavat nykyistä varastoa tilauksen riveinä. Vaihtoehtoisesti voit täyttää toisen avoimen tai kirjatun inventointitilauksen rivit **Kopioi asiakirjasta** -toiminnolla. Seuraavassa toimintaohjeessa käsitellään vain **Laske rivit** -toiminnon käyttö.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston tilaukset** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Yleinen**-pikavälilehden pakolliset kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Laske rivit** -toiminto.
5. Valitse tarvittavat vaihtoehdot.
6. Määritä suodattimen, jotka esimerkiksi sisällyttävät vain ensimmäisessä tallenteessa inventoitavien nimikkeiden alijoukon.

    > [!TIP]
    > Jos tarkoituksena on, että varaston laskentaan osallistuu useita työntekijöitä, on suositeltavaa määrittää eri suodattimet aina **Laske rivit** -toimintoa käytettäessä. Tällä tavoin tilaukseen täytetään vain yhden käyttäjän tallentamien varastonimikkeiden alijoukko. Tällä tavoin riski nimekkeiden inventoinnista kahdeksi on vähäinen, kun useille työntekijöille luodaan useita inventointitallenteita. Lisätietoja on kohdassa [Inventointitallennuksen luominen](#to-create-a-physical-inventory-recording).

7. Valitse **OK**-painike.

Tilaukseen lisätään rivi kullekin nimikkeelle, joka on valitussa sijainnissa ja joka on valittujen suodattimien ja vaihtoehtojen mukainen. Nimikkeillä, joille on määritetty nimikeseuranta, on valittuna **Käytä nimikeseurantaa** -valintaruutu. Tietoja odotetuista sarja- ja eränumeroista saa valitsemalla ensin **Rivit**-toiminnon ja sitten **Nimikkeen seurantarivit**. Lisätietoja on kohdassa [Nimikeseurannan käsittely varastoa laskettaessa](#handling-item-tracking-when-counting-inventory).

Voit nyt siirtyä luomaan vähintään yhden tallenteen. Tallenteet inventointia suorittaville työntekijöille suunnattuja ohjeita.  

## <a name="to-create-a-physical-inventory-recording"></a>Inventointitallennuksen luominen

Voit luoda kullekin inventointitilaukselle vähintään yhden inventointitallennusasiakirjan, johon työntekijät lisäävät lasketut määrät joko manuaalisesti tai integroidulla skannauslaitteella.

Tallenne luodaan oletusarvoisesti kaikille liittyvässä inventointitilauksessa oleville riveille. Jos kyse on jaetusta laskennasta, saman nimikkeen laskeminen useita kertoja eri työntekijöiden toimesta voidaan estää, kun inventointitilaus täytetään suositusten mukaan vähitellen määrittämällä suodattimet **Laske rivit** -erätyössä. (Lisätietoja on kohdassa Inventointitilauksen luominen.) Tämän jälkeen luodaan inventointitallennus valittaessa **Vain rivit, jotka eivät ole tallenteissa** -valintaruutua. Tämä asetus varmistaa, että kukin luotava uusi tallenne sisältää vain muista tallenteista poikkeavia nimikkeitä.

Jos kyse on manuaalisesta laskennasta, voit tulostaa luettelon, **Inventointitallennus**-raportin, jonka tyhjään sarakkeeseen lasketut määrät lisätään. Kun inventointi on valmis, tallennetut määrät lisätään **Inventointitallennus**-sivun liittyville riveille. Tallennetut määrät siirretään lopuksi liittyvään inventointitilaukseen määrittämällä tilaksi **Valmis**.

1. Valitse sillä **Inventointitilaus**-sivulla, joka sisältää yhdessä tallennuksessa laskettavien nimikkeiden rivit, **Luo uusi tallennus** -toiminto.
2. Valitse asetukset ja määritä suodattimet tarpeen mukaan.
3. Valitse **OK**-painike.

    Inventointitallennusasiakirja luodaan.

4. Lataa jokainen inventoitava nimikejoukko liittyvään inventointitilaukseen ja toista vaiheet 1–3 siten, että **Vain rivit, jotka eivät ole tallenteissa** -valintaruutu on valittuna.

5. Avaa **Inventointitallennusluettelo**-sivu valitsemalla **Tallennukset**-toiminto.
6. Avaa liittyvä tallenne.
7. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät.
8. Luo nimikeseurantaa käyttäville nimikkeille kullekin erä- tai sarjanumerokoodille lisärivi valitsemalla ensin **Toiminnot**- ja sitten **Kopioi rivi** -toiminto. Lisätietoja on kohdassa [Nimikeseurannan käsittely varastoa laskettaessa](#handling-item-tracking-when-counting-inventory).  
9. Valmistele fyysinen asiakirja, johon työntekijät kirjoittavat lasketut määrät, valitsemalla **Tulosta**-toiminto.

## <a name="to-finish-a-physical-inventory-recording"></a>Inventointitallennuksen valmistuminen

Kun työntekijät ovat laskeneet varastomäärät, niiden kirjaaminen järjestelmään on valmisteltava.

1. Valitse **Inventointitallennusluettelo**-sivulla viimeisteltävä inventointitallenne ja valitse sitten **Muokkaa**-toiminto.
2. Täytä laskettu määrä **Rivit**-pikavälilehdessä kunkin rivin **Määrä**-kenttään.
3. Jos nimikkeellä on sarja- tai eränumero (**Käytä nimikeseurantaa** -valintaruutu on valittu), lisää lasketut määrät nimikkeen sarja- ja eränumeroriveille. Lisätietoja on kohdassa [Nimikeseurannan käsittely varastoa laskettaessa](#handling-item-tracking-when-counting-inventory).
4. Valitse **Tallennettu**-valintaruutu kullakin rivillä.
5. Kun olet antanut kaikki inventointitallenteen tiedot, valitse **Valmis**-toiminto. Huomaa, että **Tallennettu**-valintaruudun on oltava valittuna kaikilla riveillä.

> [!NOTE]
> Kun inventointitallenne on valmis, kukin rivi siirretään sitä täsmälleen vastaavalle liittyvän inventointitilauksen riville. Vastaavuus edellyttää, että **Nimikenro**-, **Varianttikoodi**-, **Sijaintikoodi**- ja **Varastopaikan koodi** -kenttien arvot ovat samat tallenteessa ja tilausriveillä.<br /><br />
> Jos vastaavaa inventointitilausriviä ei ole ja jos **Salli tallennus ilman tilausta** -valintaruutu on valittu, uusi rivi lisätään automaattisesti ja **Tallennettu ilman tilausta** -valintaruutu valitaan liittyvän inventointitilauksen rivillä. Muussa tapauksessa avautuu virhesanoma ja prosessi peruutetaan.<br /><br />
> Jos useat inventointitallennuksen rivit vastaavat inventointitilauksen riviä, avautuu sanoma ja prosessi peruutetaan. Jos kaksi täysin samanlaista inventointiriviä päätyy jostain syystä inventointitilaukseen, voit ratkaista asian toiminnolla. Lisätietoja on kohdassa [Inventointitallennuksen rivien kaksoiskappaleiden löytäminen](#to-find-duplicate-physical-inventory-order-lines).

## <a name="to-complete-a-physical-inventory-order"></a>Inventointitilauksen viimeisteleminen

Kun inventointitallennus on valmis, liittyvän inventointitilauksen **Tallennettujen määrä (perus)** -kenttä päivitetään lasketuilla (tallennetuilla) arvoilla ja **Tallennuksessa**-valintarivi valitaan. Jos laskettu arvo poikkeaa odotetusta arvosta, arvojen välinen ero näkyy **Posit. määrä (perus)**- tai **Negat. määrä (perus)**-kentässä.

Jos haluat nähdä odotetut määrät ja mahdolliset nimikeseurantaa käyttävien nimikkeiden tallennetut erot, valitse **Rivit**-toiminto. Valitse sitten **Nimikkeen seurantarivit** -toiminnolla erilaisia inventoinnissa mukana olevien sarja- ja eränumeroiden näkymiä.

Voit valita myös **Inventointitilauksen erotus** -toiminnon ja tarkastella odotetun määrän ja lasketun määrän välisiä eroja.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>Inventointitilausrivien kaksoiskappaleiden löytäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston tilaukset** ja valitse sitten vastaava linkki.
2. Avaa inventointitilaus, jossa haluat tarkastella rivien kaksoiskappaleita.
3. Valitse **Näytä rivien kaksoiskappaleet** -toiminto.

Inventointitilausrivien mahdolliset kaksoiskappaleet ovat näkyvissä, joten voit poistaa ne ja säilyttää yhden rivin, jolla on yksilöllinen **Nimikenro**-, **Varianttikoodi**-, **Sijaintikoodi**- ja **Varastopaikan koodi** -kenttien arvojoukko.

### <a name="to-post-a-physical-inventory-order"></a>Inventointitilauksen kirjaaminen

Kun inventointitilaus on valmistunut ja sen tilaksi on muuttunut **Valmis**, voit kirjata sen. Inventointitilauksen tilaksi voi määrittää **Valmis** vain siinä tapauksessa, että seuraavat ehdot täyttyvät:

- Kaikkien liittyvien inventointitallenteiden tila on **Valmis**.
- Jokainen inventointitilausrivi on laskettu vähintään yhdellä varastotallennusrivillä.
- **Tallennusriveillä**- ja **Oletettu määrä laskettu** -valintaruudut on valittu kaikille inventointitilausriveille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston tilaukset** ja valitse sitten vastaava linkki.
2. Valitse ensin viimeisteltävä inventointitilaus ja sitten **Muokkaa**-toiminto.

    Voit tarkastella **Inventointitilaus**-sivulla **Tallennettujen määrä (perus)** -kenttään tallennettuja arvoja.
3. Valitse **Valmis**-toiminto.

    **Tila**-kentän arvoksi tulee **Valmis**, ja tilausta voi muuttaa nyt vain valitsemalla ensimmäiseksi **Avaa uudelleen** -toiminto.
4. Kirjaa tilaus valitsemalla **Kirjaa**-toiminto ja valitsemalla sitten **OK**-painike.

Liittyvät nimiketapahtumat päivitetään nyt mahdollisten liittyvien nimikeseurantatapahtumien ohella.

### <a name="to-view-posted-physical-inventory-orders"></a>Kirjattujen inventointitilausten tarkasteleminen

Inventointitilaus poistetaan kirjaamisen jälkeen, jonka jälkeen voit tarkastella ja arvioida asiakirjaa kirjattuna inventointitilauksena, joka sisältää myös inventointitallennukset ja mahdolliset kommentit.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut fyysisen varaston tilaukset** ja valitse sitten vastaava linkki.
2. Valitse **Kirjatut inventointitilaukset** -sivulla kirjattu inventointitilaus, jota haluat tarkastella, ja valitse sitten **Näytä**-toiminto.
3. Voit tarkastella liittyvien inventointitallennusten luetteloa valitsemalla **Tallennukset**-toiminnon.

## <a name="handling-item-tracking-when-counting-inventory"></a>Nimikeseurannan käsittely varastoa laskettaessa

Nimikeseuranta koskee nimikkeille määritettyjä sarja- tai eränumeroita. Jos laskettava nimike on tallennettu varastoon esimerkiksi 10 erilaisena eränumerona, työntekijän on voitava tallentaa mitkä eränumerot ovat varastossa ja kuinka monta yksikköä kutakin erää on varastossa. Lisätietoja nimikeseurantatoiminnosta on kohdassa [Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md).

**Käytä nimiseurantaa** -valintaruutu valitaan inventointitilausriveillä automaattisesti, jos nimikkeelle on määritetty nimikeseurantakoodi. Voit kuitenkin valita sen tai poistaa sen valinnan myös manuaalisesti.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Esimerkki – nimekeseuratun nimikkeen inventointitallennuksen valmistelu

Oletetaan, että nimikkeen A fyysinen varasto on tallennettu varastoon 10 eri sarjanumerolla.
1. Valitse nimikkeen tallennusrivillä **Käytä nimiseurantaa** -valintaruutu.
2.  Valitse **Sarjanumero**-kentässä ensimmäinen sarjanumero, joka nimikkeellä on varastossa, ja valitse sitten **OK**-painike.

    Kopioi seuraavaksi ensimmäisen nimikeseuratun nimikkeen rivi. Voit lisätä tällä tavoin varastoon tallennettujen sarjanumeroiden numeroa vastaavia lisärivejä.

3. Valitse ensin **Toiminnot**- ja sitten **Kopioi rivi** -toiminto.
4. Anna 9 **Kopioi inventointitallennusrivi** -sivun **Kopioiden lukumäärä** -kenttään ja valitse sitten **OK**-painike.
5. Valitse ensimmäisellä kopiorivillä **Sarjanumero**-kenttä ja valitse sitten nimikkeen seuraava sarjanumero.
6. Toista vaihe 5 seuraavan kahdeksan sarjanumeron osalta. Varmista, ettet valitse samaa numeroa kahdesti.
7. Valmistele tuloste, johon työntekijät kirjoittavat lasketut nimikkeet ja sarja- tai eränumero, valitsemalla **Tulosta**-toiminto.

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

**Inventointitilaus**-sivun **Negat. määrä (perus)** -kentän arvo on *8*. Kyseisen tilausrivin **Inventoinnin nimikeseurantaluettelo** -sivulla on yksittäisten eränumeroiden positiiviset tai negatiiviset määrät.

## <a name="inventory-documents"></a>Varastoasiakirjat

Seuraavat asiakirjatyypit ovat käteviä fyysisen varaston hallinnassa:

- **Varaston vastaanotoilla** voi rekisteröidä nimikkeiden positiiviset muutokset määrän, laadun ja kustannuksen perusteella.
- **Varaston lähetysten** avulla voi kirjata pois puuttuvia tai vaurioituneita tuotteita.

Nämä asiakirjat voidaan tulostaa koska tahansa. Ne voidaan vapauttaa ja avata uudelleen, minkä lisäksi niiden otsikkoon voidaan määrittää yleisiä arvoja, mukaan lukien dimensioita. Jos haluat tulostaa asiakirjat uudelleen sen jälkeen, kun ne on kirjattu, se voidaan tehdä **Kirjatut varastovastaanotot**- ja **Kirjatut varastolähetykset** -sivuilla.

> [!NOTE]
> Ennen kuin näitä asiakirjoja voidaan käyttää, niille on luotava tunnisteet määrittämällä numerosarja. Lisätietoja on seuraavassa osassa.

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

- Seuraavan käsittelyvaiheen tila määritetään **Vapauta**- tai **Avaa uudelleen** -toiminnolla  
- Kirjaa varaston vastaanotto valitsemalla **Kirjaa**-toiminto tai kirjaa vastaanotto ja tulosta testiraportti valitsemalla **Kirjaa ja tulosta**  

## <a name="printing-inventory-documents"></a>Varastoasiakirjojen tulostaminen

Eri vaiheissa tulostettavat raportit voidaan määrittää valitsemalla jokin seuraavista vaihtoehdoista **Raportin valinta – varasto** -sivun **Käyttö**-kentässä:

- Varaston vastaanotto
- Varastotoimitus
- Kirjattu varaston vastaanotto
- Kirjattu varastotoimitus

> [!NOTE]
> Käytettävissä olevat raportit voivat vaihdella maan lokalisoinnin mukaan. Perussovellus ei sisällä asetteluja.

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/adjust-inventory/)

## <a name="see-also"></a>Katso myös

[Varaston laskeminen, muuttaminen ja uudelleenluokitus käyttämällä päiväkirjoja](inventory-how-count-adjust-reclassify.md)  
[Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
