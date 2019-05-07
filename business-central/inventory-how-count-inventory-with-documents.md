---
title: Varaston laskenta asiakirjapohjaisilla toiminnoilla| Microsoft Docs
description: Tietoja inventoinnista käyttämällä Inventointitilaus- ja Inventointitallennus-sivuja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, status, negative, positive, increase, decrease
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 24b89662ed772280da8f5f8f08677f644f75922e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "940113"
---
# <a name="count-inventory-using-documents"></a>Varastojen laskenta asiakirjoja käyttämällä
Voit inventoida nimikkeet käyttämällä inventointitilauksen ja inventointitallennuksen asiakirjoja. **Inventointitilaus**-sivulla järjestetään täydellinen inventointiprojekti, kuten yksi kussakin toimipisteessä. **Inventointitallennus**-sivun avulla ilmoitetaan ja tallennetaan nimikkeiden varsinainen inventointi. Voit luoda yhdelle tilaukselle useita  tallenteita, jolloin voit esimerkiksi jakaa nimekeryhmiä eri työntekijöille.

Jokaisesta tallenteesta voidaan tulostaa **Inventointitallennus**-raportti. Tämän raportin määräkentät ovat tyhjiä, ja laskettu varasto voidaan sitten lisätä näihin kenttiin. Kun käyttäjä lopettaa inventoinnin ja määrät on lisätty **Inventointitallennus**-sivulla, valitse **Valmis**-toiminto. Määrät siirretään nyt liittyville riveille **Inventointitilaus**-sivulla. Toiminto varmistaa, ettei mitään nimikettä tallennetta kahdesti.      

> [!NOTE]
> Tässä toiminto-ohjeessa käsitellään asiakirjoja hyödyntävää inventointia, joka parantaa hallintaa ja tukee inventoinnin jakamista useille työntekijöille. Tehtävän voi suorittaa myös käyttämällä päiväkirjojen **Varastopäiväkirjat**- ja **F. var. inventointipäiväkirjat** -sivuja. Lisätietoja on kohdassa [Varaston laskeminen, muuttaminen ja uudelleenluokitus päiväkirjojen avulla](inventory-how-count-adjust-reclassify.md).<br /><br />
> Huomaa, että jos käytät Varastopaikat- tai Alueet-toimintoja, et voi käyttää inventointitilauksia. Käytä sen sijaan **F. var. inventointipäiväkirja** -sivua fyysisen varastoinnin tapahtumien laskemiseen, ennen kuin ne synkronoidaan nimiketapahtumien kanssa.

Asiakirjoja hyödyntävä varaston laskenta sisältää yleisesti seuraavat vaiheet:

1. Luo inventointitilaus siten, että nimikkeiden odotetut määrät on täytetty valmiiksi.
2. Luo tilauksesta vähintään yksi inventointitallennus.
3. Lisää inventoitujen nimikkeiden määrät tallenteisiin esimerkiksi tulosteisiin kerättyjen tietojen mukaisesti ja määritä sen arvoksi **Valmis**.
4. Täytä ja kirjaa inventointitilaus.

## <a name="to-create-a-physical-inventory-order"></a>Inventointitilauksen luominen
Inventointitilaus on valmis asiakirja, joka koostuu inventointitilauksen otsikosta ja inventointitilausriveistä. Inventointitilauksen otsikossa selitetään, miten inventointi tehdään. Inventointitilauksen riveillä on tietoja nimikkeistä ja niiden sijainneista.

Inventointitilauksen rivit luodaan yleensä käyttämällä **Laske rivit** -toimintoa siten, että ne vastaavat nykyistä varastoa tilauksen riveinä. Vaihtoehtoisesti voit täyttää toisen avoimen tai kirjatun inventointitilauksen rivit **Kopioi asiakirja** -toiminnolla. Seuraavassa toimintaohjeessa käsitellään vain **Laske rivit** -toiminnon käyttö.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Inventointitilaukset** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Yleinen**-pikavälilehden pakolliset kentät. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Laske rivit** -toiminto.
5. Valitse tarvittavat vaihtoehdot.
6. Määritä suodattimen, jotka esimerkiksi sisällyttävät vain ensimmäisessä tallenteessa inventoitavien nimikkeiden alijoukon.

    > [!TIP]
    > Jos tarkoituksena on, että varaston laskentaan osallistuu useita työntekijöitä, on suositeltavaa määrittää eri suodattimet aina **Laske rivit** -toimintoa käytettäessä. Tällä tavoin tilaukseen täytetään vain yhden käyttäjän tallentamien varastonimikkeiden alijoukko. Tällä tavoin riski nimekkeiden inventoinnista kahdeksi on vähäinen, kun useille työntekijöille luodaan useita inventointitallenteita. Lisätietoja on kohdassa Inventointitallennuksen luominen.

7.  Valitse **OK**-painike.

Tilaukseen lisätään rivi kullekin nimikkeelle, joka on valitussa sijainnissa ja joka on valittujen suodattimien ja vaihtoehtojen mukainen. Nimikkeillä, joille on määritetty nimikeseuranta, on valittuna **Käytä nimikeseurantaa** -valintaruutu. Tietoja odotetuista sarja- ja eränumeroista saa valitsemalla ensin **Rivit**-toiminnon ja sitten **Nimikkeen seurantarivit**. Lisätietoja on kohdassa Nimikeseurannan käsittely varastoa laskettaessa.

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
8. Luo nimikeseurantaa käyttäville nimikkeille kullekin erä- tai sarjanumerokoodille lisärivi valitsemalla ensin **Toiminnot**- ja sitten **Kopioi rivi** -toiminto. Lisätietoja on kohdassa Nimikeseurannan käsittely varastoa laskettaessa.    
9. Valmistele fyysinen asiakirja, johon työntekijät kirjoittavat lasketut määrät, valitsemalla **Tulosta**-toiminto.

## <a name="to-finish-a-physical-inventory-recording"></a>Inventointitallennuksen valmistuminen
Kun työntekijät ovat laskeneet varastomäärät, niiden kirjaaminen järjestelmään on valmisteltava.

1. Valitse **Inventointitallennusluettelo**-sivulla viimeisteltävä inventointitallenne ja valitse sitten **Muokkaa**-toiminto.
2. Täytä laskettu määrä **Rivit**-pikavälilehdessä kunkin rivin **Määrä**-kenttään.
3. Jos nimikkeellä on sarja- tai eränumero (**Käytä nimikeseurantaa** -valintaruutu on valittu), lisää lasketut määrät nimikkeen sarja- ja eränumeroriveille. Lisätietoja on kohdassa Nimikeseurannan käsittely varastoa laskettaessa.
4. Valitse **Tallennettu**-valintaruutu kullakin rivillä.
5. Kun olet antanut kaikki inventointitallenteen tiedot, valitse **Valmis**-toiminto. Huomaa, että **Tallennettu**-valintaruudun on oltava valittuna kaikilla riveillä.

> [!NOTE]
> Kun inventointitallenne on valmis, kukin rivi siirretään sitä täsmälleen vastaavalle liittyvän inventointitilauksen riville. Vastaavuus edellyttää, että **Nimikenro**-, **Varianttikoodi**-, **Sijaintikoodi**- ja **Varastopaikan koodi** -kenttien arvot ovat samat tallenteessa ja tilausriveillä.<br /><br />
> Jos vastaavaa inventointitilausriviä ei ole ja jos **Salli tallennus ilman tilausta** -valintaruutu on valittu, uusi rivi lisätään automaattisesti ja **Tallennettu ilman tilausta** -valintaruutu valitaan liittyvän inventointitilauksen rivillä. Muussa tapauksessa avautuu virhesanoma ja prosessi peruutetaan.<br /><br />
> Jos useat inventointitallennuksen rivit vastaavat inventointitilauksen riviä, avautuu sanoma ja prosessi peruutetaan. Jos kaksi täysin samanlaista inventointiriviä päätyy jostain syystä inventointitilaukseen, voit ratkaista asian toiminnolla. Lisätietoja on kohdassa Inventointitallennuksen rivien kaksoiskappaleiden löytäminen.

## <a name="to-complete-a-physical-inventory-order"></a>Inventointitilauksen viimeisteleminen
Kun inventointitallennus on valmis, liittyvän inventointitilauksen **Tallennettujen määrä (perus)** -kenttä päivitetään lasketuilla (tallennetuilla) arvoilla ja **Tallennuksessa**-valintarivi valitaan. Jos laskettu arvo poikkeaa odotetusta arvosta, arvojen välinen ero näkyy **Posit. määrä (perus)**- tai **Negat. määrä (perus)**-kentässä.

Jos haluat nähdä odotetut määrät ja mahdolliset nimikeseurantaa käyttävien nimikkeiden tallennetut erot, valitse **Rivit**-toiminto. Valitse sitten **Nimikkeen seurantarivit** -toiminnolla erilaisia inventoinnissa mukana olevien sarja- ja eränumeroiden näkymiä.

Voit valita myös **Inventointitilauksen erotus** -toiminnon, jos haluat tarkastella odotetun määrän ja lasketun määrän välisiä eroja.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>Inventointitilausrivien kaksoiskappaleiden löytäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Inventointitilaukset** ja valitse sitten liittyvä linkki.
2. Avaa inventointitilaus, jossa haluat tarkastella rivien kaksoiskappaleita.
3. Valitse **Näytä rivien kaksoiskappaleet** -toiminto.

Inventointitilausrivien mahdolliset kaksoiskappaleet ovat näkyvissä, joten voit poistaa ne ja säilyttää yhden rivin, jolla on yksilöllinen **Nimikenro**-, **Varianttikoodi**-, **Sijaintikoodi**- ja **Varastopaikan koodi** -kenttien arvojoukko.

### <a name="to-post-a-physical-inventory-order"></a>Inventointitilauksen kirjaaminen
Kun inventointitilaus on valmistunut ja sen tilaksi on muuttunut **Valmis**, voit kirjata sen. Inventointitilauksen tilaksi voi määrittää **Valmis** vain siinä tapauksessa, että seuraavat ehdot täyttyvät:

- Kaikkien liittyvien inventointitallenteiden tila on **Valmis**.
- Jokainen inventointitilausrivi on laskettu vähintään yhdellä varastotallennusrivillä.
- **Tallennusriveillä**- ja **Oletettu määrä laskettu** -valintaruudut on valittu kaikille inventointitilausriveille.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Inventointitilaukset** ja valitse sitten liittyvä linkki.
2. Valitse ensin viimeisteltävä inventointitilaus ja sitten **Muokkaa**-toiminto.

    Voit tarkastella **Inventointitilaus**-sivulla **Tallennettujen määrä (perus)** -kenttään tallennettuja arvoja.
3. Valitse **Valmis**-toiminto.

    **Tila**-kentän arvoksi tulee **Valmis**, ja tilausta voi muuttaa nyt vain valitsemalla ensimmäiseksi **Avaa uudelleen** -toiminto.
4. Kirjaa tilaus valitsemalla **Kirjaa**-toiminto ja valitsemalla sitten **OK**-painike.

Liittyvät nimiketapahtumat päivitetään nyt mahdollisten liittyvien nimikeseurantatapahtumien ohella.

### <a name="to-view-posted-physical-inventory-orders"></a>Kirjattujen inventointitilausten tarkasteleminen
Inventointitilaus poistetaan kirjaamisen jälkeen, jonka jälkeen voit tarkastella ja arvioida asiakirjaa kirjattuna inventointitilauksena, joka sisältää myös inventointitallennukset ja mahdolliset kommentit.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kirjatut inventointitilaukset** ja valitse sitten liittyvä linkki.
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

## <a name="see-also"></a>Katso myös
[Varaston laskeminen, muuttaminen ja uudelleenluokitus käyttämällä päiväkirjoja](inventory-how-count-adjust-reclassify.md)  
[Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)    
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
