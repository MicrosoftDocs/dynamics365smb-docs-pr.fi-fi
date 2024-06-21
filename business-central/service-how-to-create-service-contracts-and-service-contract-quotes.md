---
title: Huoltosopimusten ja huoltosopimustarjousten käsitteleminen | Microsoft Docs
description: Huoltosopimus voidaan luoda joko manuaalisesti tai huoltosopimustarjouksesta. Voit luoda huoltosopimuksen huoltosopimustarjouksen perusteella.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="work-with-service-contracts-and-service-contract-quotes"></a>Huoltosopimusten ja huoltosopimustarjousten käyttäminen
Huoltosopimus voidaan luoda joko manuaalisesti tai huoltosopimustarjouksesta. Huoltosopimustarjousta voidaan käyttää huoltosopimuksen esiasteena, jossa yrityksesi tekee asiakkaalle tarjouksen ja joka tarvitsee asiakkaan hyväksynnän, ennen kuin se voidaan muuntaa huoltosopimukseksi. Tämän vuoksi huoltosopimus ja huoltotarjous luodaan pitkälti samalla tavoin.  

## <a name="to-create-a-service-contract-or-service-contract-quote"></a>Huoltosopimuksen tai -sopimustarjouksen luominen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimukset** tai **Huoltosopimustarjoukset** ja valitse sitten vastaava linkki.  
2. Luo uusi huoltosopimus tai huoltosopimustarjous.  
3. Syötä **Nro** -kentässä. Näyttöön avautuu valintaikkuna, jossa kysytään, haluatko täyttää yleiset tiedot sopimusmallista. Jos haluat luoda tällaisen huoltosopimuksen tai huoltosopimustarjouksen, valitse **Kyllä**-painike. Näyttöön tulee **Huoltosopimusmallin luettelo** -sivu.  
4. Valitse soveltuva malli ja luo sen avulla huoltosopimus tai huoltosopimustarjous valitsemalla **OK**.  
5. Syötä **Asiakasnro** -kentässä asiakkaan valinta.  
6. Jos et halua, että vuosittaisen summan ero jaetaan automaattisesti, valitse **Salli epätäsmäävät summat** -valintaruutu. Kenttien **Vuosittainen summa** ja **Laskettu vuosittainen summa** arvoja ei tasata automaattisesti. Jos haluat, että sovellus jakaa huoltosopimuksen muuttamisesta johtuvan mahdollisen vuosittaisen summan eron automaattisesti, jätä **Salli epätäsmäävät summat** -valintaruutu tyhjäksi.  
7. Lisää sopimusrivejä huoltosopimukseen tai -sopimustarjoukseen.  
8. Täytä muut kentät tarpeen mukaan.  

## <a name="to-convert-a-service-contract-quote-to-service-contract"></a>Huoltosopimustarjousten muuntaminen huoltosopimuksiksi
Kun asiakas on hyväksynyt huoltosopimustarjouksen, se muunnetaan huoltosopimukseksi. Ohjelman voi antaa samaan aikaan luoda huoltolaskun sopimuksen aloitusjaksolta, jos sopimuksen aloituspäivämäärä on ennen seuraavan laskutusjakson alkua.

Kun olet tehnyt seuraavat toimet, luotavan huoltosopimuksen tila on **Allekirjoitettu**. Jos ohjelma luo huoltolaskun sopimuksen aloitusjaksolta, ohjelma laskee laskutetun summan seuraavassa kuvatulla tavalla sen mukaan, onko sopimus yksityiskohtainen.  

Yksityiskohtaisten sopimusten laskutettu summa lasketaan seuraavasti:  

* Laskutettu summa = laskutetun summan yhteenlaskettu summa kunkin sopimusrivin osalta.  
* Laskutettu summa kunkin sopimusrivin osalta = ((tarjousarvo / 12) * aloitusjakson kuukausien lukumäärä) + ((tarjousarvo / vuoden päivien lukumäärä) * laskutusjaksossa jäljellä olevien päivien lukumäärä).  
* Jos sopimusrivi menee vanhaksi ennen kuin aloitusjakso päättyy, vanhentumispäivämäärästä tulee aloitusjakson lopetuspäivämäärä riville.  

Muiden kuin yksityiskohtaisten sopimusten laskutettu summa lasketaan seuraavasti:  

* laskutettu summa = (vuosittainen summa / vuoden päivien lukumäärä) * aloitusjakson päivien lukumäärä.  
* Jos sopimus menee vanhaksi ennen kuin aloitusjakso päättyy, vanhentumispäivämäärästä tulee aloitusjakson lopetuspäivämäärä.    

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimustarjoukset** ja valitse sitten vastaava linkki.  
2. Avaa huoltosopimukseksi muunnettava huoltosopimustarjous.  
3. Valitse **Tee sopimus** -toiminto.  
4. Ohjelman voi antaa samaan aikaan luoda huoltolaskun sopimuksen aloitusjaksolta, jos sopimuksen aloituspäivämäärä on ennen seuraavan laskutusjakson alkua. Valitse **Kyllä**.  

 Ohjelma kirjaa huoltolaskun sopimuksen huoltotilille, vaikka sopimus on maksettu ennakkoon.

## <a name="to-create-contract-service-credit-memos"></a>Huoltosopimuksen hyvityslaskujen luominen
Sopimusten huoltohyvityslaskuja voi käyttää silloin, kun asiakas peruuttaa ennakkoon maksetun huoltosopimuksen tai poistaa ennakkoon maksetusta sopimuksesta huoltonimikkeen (sopimusrivin). Niitä voi käyttää myös korjaamaan virheellisen huoltolaskun.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huollon hyvityslaskut** ja valitse sitten vastaava linkki.  
2. Luo uusi huollon hyvityslasku.  
3. Syötä **Nro** -kentässä.  
4. Syötä **Asiakasnro** -kentässä huoltosopimuksessa olevan asiakkaan numero.  

     **Asiakas**-kortista kopioidut tiedot näkyvät **Laskutus**-pikavälilehdessä. Jos haluat kirjata hyvityslaskun muulle kuin **Yleinen**-pikavälilehdessä määritetylle asiakkaalle, anna kyseisen asiakkaan numero **Laskutusasiakkaan nro** -kentässä. -kentässä.  

    > [!NOTE]  
    >  Hyvityslaskua voi verrata alkuperäiseen kirjattuun asiakirjaan esimerkiksi **Kirjatut huoltolaskut** -sivulla. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut huoltolaskut** ja valitse sitten vastaava linkki.  

5. Täytä **Kirjauspvm**- ja **Asiakirjan pvm** -kentät.  
6. Syötä hyvityslaskun riveille tietoja lähetettävästä myyntialennuksesta tai nimikkeistä, jotka on palautettu tai poistettu. Voit käyttää myös **Hae enn. maksetut sop.tapaht.** -eräajoa.  

 Jos **Huoltosopimus**-sivun **Laskun yksityiskohdat** -pikavälilehden **Automaattiset hyvityslaskut** -kentässä on valintamerkki, ohjelma luo hyvityslaskun automaattisesti, kun sopimusrivit poistetaan.  

 Luo hyvityslasku, kun sopimusrivit on poistettu huoltosopimuksesta **Huoltosopimus**-sivulla valitsemalla **Hyvityslasku**.  

## <a name="updating-and-evaluating-contracts"></a>Sopimusten päivittäminen ja arvioiminen
Joskus on tarpeen muuttaa sopimuksen ehtoja sen jälkeen, kun sopimus on luotu. Useimmiten tämä onnistuu avaamalla sopimus **Huoltosopimus**-sivulla ja muuttamalla tietoja tarpeen mukaan.  

Voit muuttaa sopimuksen **Lukittu**-tilaa, lisätä ja poistaa sopimusrivejä sekä peruuttaa sopimuksen. Voit myös tarkastella liiketoiminnan voittoja ja tappioita luomalla liiketoiminta-analyysin Sopimuksen Trendscape-näkymä -toiminnolla.

## <a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote"></a>Sopimusrivien lisääminen huoltosopimukseen tai sopimustarjoukseen:
Kun asiakas ostaa uuden nimikkeen ja haluaa sisällyttää sen olemassa olevaan huoltosopimukseen tai sopimustarjoukseen, nimike voidaan rekisteröidä huoltonimikkeeksi ja lisätä uutena sopimusrivinä sopimukseen tai sopimustarjoukseen.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimukset** ja valitse sitten vastaava linkki.  
2. Avaa huoltosopimus tai huoltosopimustarjous, johon haluat lisätä uuden sopimusrivin.  
3. Avaa muokattava huoltosopimus tai huoltosopimustarjous valitsemalla **Avaa sopimus** -toiminto.  
4. Siirry **Laskun yksityiskohdat** -pikavälilehteen ja valitse **Salli epätäsmäävät summat** -kentän valintaruutu, jos haluat muuttaa vuosittaista summaa ja jakaa vuosittaisen summan eron manuaalisesti sopimusriveille. Muussa tapauksessa poista valinta **Salli epätäsmäävät summat** -kentän valintaruudusta. Tällöin ohjelma jakaa vuosittaisen summan eron automaattisesti sopimusriveille, kun vuosittaista summaa on muutettu.  
5. Lisää kullekin sopimusriville **Rivit**-pikavälilehdessä oikea huoltonimike, nimike tai tekstikuvaus. Vaihtoehtoisesti voit lisätä sopimustarjousrivejä. Huomaa, että voit luoda huoltonimikkeelle useita sopimuksia, jolloin nimike sisältyy samanaikaisesti eri huoltosopimuksiin tai sopimustarjouksiin.  
6. Tarkasta ja korjaa tarvittaessa **Rivialennus-%**-, **Rivin alennussumma**-, **Vastausaika**-, **Huoltojakso**- ja muiden kenttien luvut.

## <a name="to-remove-contract-lines"></a>Sopimusrivien poistaminen
Huoltosopimuksesta voidaan joutua poistamaan sopimusrivejä, kun huoltonimike poistetaan huoltosopimuksesta. Sopimusrivi poistetaan tavallisesti, kun se vanhenee, tai kun huoltonimike, jota se koskee, on särkynyt.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimukset** ja valitse sitten vastaava linkki.  
2. Avaa huoltosopimus, josta haluat poistaa sopimusrivejä.  
3. Avaa muokattava huoltosopimus valitsemalla **Avaa sopimus** -toiminto.  
4. Valitse poistettava sopimusrivi. Kirjoita **Sopimuksen umpeutumispvm** -kenttään päivämäärä, jolloin haluat poistaa rivin. Voit määrittää esimerkiksi päivämäärän, jolloin huoltonimike särkyi.  
5. Valitse **Poista sopimusrivit** -toiminto. **Poista rivit sopimuksesta** -sivu aukeaa.  
6. Täytä oletussuodattimet: **Sopimusnro**, **Huoltonimikkeen nro** ja **Sopimustyyppi**. Voit myös ottaa käyttöön muita suodattimia tai muuttaa nykyisiä suodattimia.  
7. Täytä **Asetukset**-pikavälilehden kentät ja valitse sitten **Poista rivit** -toiminto.  

> [!NOTE]  
>  Jos sopimus ei ole yksityiskohtainen, **Huoltosopimus**-sivun **Laskun yksityiskohdat** -pikavälilehden **Vuosittainen summa** -kentän arvo on päivitettävä sopimuksesta poistetun huoltonimikkeen mukaisesti.  
>   
>  Jos sopimus on yksityiskohtainen sekä ennakkoon maksettu ja sille on kirjattu laskuja, voit luoda sopimukselle hyvityslaskun. Valitse **Luo hyvityslasku** -toiminto. Tämä on tarpeeton, jos **Automaattiset hyvityslaskut** -kentän valintaruutu **Laskutustiedot**-pikavälilehdellä on valittu. Tällöin hyvityslasku luodaan automaattisesti, kun sopimusrivi poistetaan.

## <a name="service-line-cost-and-value"></a>Huoltorivin kustannus ja arvo
Huoltosopimusrivien **Rivikustannus**- ja **Rivin arvo** -summat lasketaan seuraavissa taulukoissa kuvatulla tavalla.

| Rivikustannusasetukset | Description|
|----------------------------------|---------------------------------------|  
|**Huoltonimike** | Ohjelma hakee automaattisesti kustannuksen **Huoltonimike**-taulukon **Oletussopimuskustannus** -kentästä ja kopioi sen **Rivikustannus**-kenttään. Rivikustannus lasketaan seuraavaa kaavaa käyttäen:<br /><br /> Myynnin yksikkökustannus * Sopimusarvo-% / 100.|  
|**Nimike** | Ohjelma hakee automaattisesti kustannuksen **Nimike**-taulukon **Yksikkökustannus**-kentästä sekä **Sopimusarvo-%**-kentän arvon **Huoltohallinnon asetukset** -taulukosta. Rivikustannus lasketaan seuraavaa kaavaa käyttäen:<br /><br /> Yksikkökustannus * Sopimusarvo-% / 100.|  
|**Tekstikuvaus:** | Ohjelma asettaa **Rivikustannus**-kentän arvoksi nolla.|  

| Rivin arvoasetukset | Description|
|----------------------------------|---------------------------------------|  
|**Huoltonimike** | Ohjelma hakee automaattisesti hinnan **Huoltonimike**-taulukon **Oletussopimusarvo** -kentästä ja kopioi sen **Riviarvo**-kenttään.|  
|**Nimike** | Riippuen kentän **Sopimusarvon laskentatapa** arvosta  **Huoltohallinnon asetukset** -taulukossa, summa haetaan joko **Yksikköhinta**- tai **Yksikkökustannus**-kentästä  **Nimike**-taulukossa. Sen jälkeen arvo kerrotaan **Sopimusarvo %** -kentän sisällöllä **Huoltohallinnon asetukset** -taulukossa ja jaetaan 100:lla. Tämä summa kopioidaan **Rivin arvo** -kenttään.<br /><br /> **HUOMAUTUS:** Jos **Sopimusarvon laskentatapa** -kentän arvoksi on määritetty **Ei mitään**, ohjelma ei laske **Rivin arvo** -kentälle arvoa.|  
|**Tekstikuvaus:** | Ohjelma asettaa **Rivin arvo**-kentän arvoksi nolla.|  

## <a name="to-add-a-contract-discount-to-service-contract-quotes"></a>Sopimusalennusten lisääminen huoltosopimustarjouksiin
Huolloille voi lisätä sopimusalennuksia sopimustarjousten ja huoltosopimusten osalta. Alennuksia voi antaa varaosille tietyissä huoltonimikeryhmissä, resurssitunneille tietyissä resurssiryhmissä olevien resurssien osalta sekä tietylle resurssikustannuksille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimustarjoukset** ja valitse vastaava linkki.  
2. Valitse tarjous, johon alennukset lisätään.  
3. Valitse **Huoltoalennukset**-toiminto. **Sopimus-/huoltoalennukset**-sivu aukeaa.  
4. Luo uusi sopimusalennus valitsemalla **Uusi**-toiminto.  
5. Täytä tarvittaessa rivin muut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  

> [!Tip]  
>  Voit lisätä sopimusalennuksia suoraan huoltosopimukseen toistamalla vastaavat **Huoltosopimus**-sivun vaiheet.  

## <a name="to-change-the-owner-of-a-service-contract"></a>Huoltosopimusten haltijan vaihtaminen
SInun täytyy ehdkä vaihtaa huoltosopimuksen haltijaa. Jos huoltosopimuksen huoltonimike on rekisteröity useaan sopimukseen, jotka samalla asiakkaalla on voimassa, ohjelma vaihtaa uuden haltijan automaattisesti kaikkiin huoltosopimuksiin, joihin tämä huoltonimike sisältyy, sekä kaikkiin muihin näihin sopimuksiin sisältyviin huoltonimikkeisiin.  

> [!NOTE]  
>  Huomioon otetaan vain sopimukset, joita ei ole peruutettu. Sopimustarjousten tilaa ei oteta huomioon.  

> [!IMPORTANT]  
>  Huoltonimikkeet ja -sopimukset voivat liittyä toisiinsa. Huoltosopimuksen omistajan muuttaminen voi vaikuttaa näihin suhteisiin.  
>   
>  Esimerkki: Huoltonimike nro 8 kuuluu sopimuksiin SC00003 ja SC00015. Sopimus SC00015 puolestaan sisältää huoltonimikkeen nro 15, joka kuuluu myös sopimukseen SC00080. Tässä tapauksessa kaikkien näiden kolmen sopimuksen ja huoltonimikkeen haltija vaihdetaan.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimukset** ja valitse sitten vastaava linkki. Avaa asianmukaienn huoltosopimus, jonka omistajaa haluat muuttaa.  
2. Avaa muokattava sopimus valitsemalla **Avaa sopimus** -toiminto.  
3. Valitse **Vaihda asiakas** -toiminto. **Muuta asiakasta sopimuksessa** -sivu aukeaa.  
4. **Sopimusnro**- ja **Huoltonimikkeen nro** -kentissä voi tarkistaa valitun asiakkaan omistaman sopimuksen ja huoltonimikkeen numerot. Jos asiakkaalla on useita sopimuksia ja sopimuksissa on useita huoltonimikkeitä, kenttien arvo on **Useampi**. Valitse nämä kenttäarvot nähdäksesi sopimusten tai huoltonimikkeiden luettelon.  
5. Valitse **Uusi asiakasnro** -kentässä uusi asiakas.  
6. Valitse osoite **Uusi toimitusasiakkaan koodi** -kentässä.  
7. Muuta palvelusopimusten asiakas tai toimitusasiakkaan koodi valitsemalla **OK**.  
8. Lukitse sopimus valitsemalla **Lukitse sopimus** -toiminto. Voit varmistaa tällä tavoin, että muutokset sisältyvät sopimuksiin.  

## <a name="to-update-a-service-contract-price"></a>Päivitä huoltosopimuksen hinnat
Huoltosopimusten hintoja voi päivittää määrittelemällä hinnanmuutosprosentin.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Päivitä huoltosopimuksen hinnat** ja valitse sitten vastaava linkki.
2. Valitse huoltosopimus.  
3. Anna päivämäärä **Päivitä pvm:ään asti** -kentässä. Eräajo päivittää hinnat sopimuksissa, joiden seuraava hinnan päivityspäivämäärä on kyseisenä päivämääränä tai sitä ennen.  
4. Anna **Hinnanpäivitys-%**-kenttään prosentti, jolla haluat päivittää hintoja.  
5. Valitse **Toiminto**-kentästä **Päivitä sopimushinnat**.  

## <a name="to-post-prepaid-contract-entries"></a>Ennakkoon maksettujen sopimustapahtumien kirjaaminen
Jos työskentelet ennakkoon maksettujen huoltosopimusten parissa, ennakkoon maksetut sopimustapahtumat tulee kirjata säännöllisesti ja siten siirtää ennakkomaksusummat ennakkoon maksettujen sopimusten tileiltä tavallisten sopimusten tileille.  

Ennen kuin ennakkoon maksettuja sopimustapahtumia voi kirjata, **Huoltohallinnon asetukset** -sivun **Enn. maks. kirj.asiakirj. nrot** -kenttään tulee määrittää numerosarja.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjaa enn.maksetut sop.tap.** ja valitse sitten vastaava linkki.  
2. Anna päivämäärä **Kirjaa pvm:ään asti** -kentässä. Eräajo kirjaa ennakkoon maksetut huoltotapahtumat, joiden kirjauspäivämäärä on ennen tähän kenttään määritettyä päivämäärää.  
4. Anna **Kirjauspvm**-kenttään päivämäärä, jota haluat käyttää kirjauspäivämääränä yleisen päiväkirjan rivillä.  
5. Valitse **Toiminto**-kentässä **Kirjaa ennak.maksetut sop.tap**.  
6. Kirjaa tapahtumat valitsemalla **OK**.

## <a name="changing-the-service-contract-status"></a>Huoltosopimuksen tilan muuttaminen
Kun huoltosopimus on allekirjoitettu, **Muuta tilaa** -kentän arvoksi asetetaan automaattisesti **Lukittu**. Jos huoltosopimuksen tai huoltosopimustarjouksen tietoja halutaan muokata, on sopimuksen tai sopimustarjouksen **Lukittu**-tila muutettava ensin **Avoin**-tilaksi. Huomaa, että huoltosopimukselle, jonka Muuta tilaa -tila on **Avoin**, ei voida luoda huoltolaskuja. Kun sopimuksen tai sopimustarjouksen muutokset on tehty, tilaksi on vaihdettava uudelleen **Lukittu**, jotta huoltosopimukselle voidaan luoda huoltolaskuja ja tapahtumia tehdyt muutokset mukaan lukien.  

> [!NOTE]  
>  **Muuta tilaa** -kenttä ei liity huoltotilauksen **Vapautustila** -otsikkokenttään, jolla hallitaan huoltonimikkeiden käsittelyä varastossa.  

## <a name="to-cancel-a-service-contract"></a>Sopimuksen peruuttaminen
Sopimus voi olla tarpeen peruuttaa ohjelmassa, kun sopimus on vanhentunut tai kun asiakas ja/tai sinä itse olet peruuttanut sopimuksen.  

> [!NOTE]  
>  Peruutettua sopimusta ei voi avata uudelleen.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimukset** ja valitse sitten vastaava linkki.  
2. Avaa peruutettava huoltosopimus.  
3. Avaa muokattava huoltosopimus valitsemalla **Avaa sopimus** -toiminto.  
4. Valitse sopiva syykoodi **Peruuta syykoodi** -kentässä. Voit lisätä syykoodeja valitsemalla **Lisäasetukset**-toiminnon.  

     Jos **Huoltohallinnon asetukset** -sivun **Käytä sopimuksen perussyytä** -kenttä on valittu, peruutuksen syykoodi on määritettävä sopimuksia peruutettaessa.  

5. Valitse **Tila**-kentässä **Peruutettu**.  
6. Jos sopimuksella on kirjaamattomia laskuja, hyvityslaskuja tai avattuja ennakkoon maksettuja tapahtumia , vahvistussanoma avautuu. Valitse sanomaruudussa **Ei**, jos haluat palata sopimukseen ja kirjata asiakirjat, tai **Kyllä**, jos haluat jatkaa peruuttamista.  

## <a name="filing-a-service-contract-or-contract-quote"></a>Huoltosopimuksen ja sopimustarjouksen arkistoiminen
Huoltosopimuksia ja sopimustarjouksia voi arkistoida milloin vain, jotta sopimuksesta tai huoltosopimuksesta voitaisiin tallentaa kopio. [!INCLUDE[prod_short](includes/prod_short.md)] arkistoi huoltosopimuksia automaattisesti silloin, kun sopimustarjouksia muunnetaan huoltosopimuksiksi, tai kun huoltosopimuksia peruutetaan. Voit arkistoida sopimuksen tai tarjouksen itse valitsemalla **Arkistoi sopimus** -toiminnon **Huoltosopimukset**- tai **Huoltosopimustarjoukset**-sivulla. Jos haluat tarkastella arkistoituja tarjoussopimuksia, voit hakea niitä hakusanalla **Arkistoidut sopimukset**.

## <a name="see-also"></a>Katso myös
[Huoltosopimusten määrittäminen](service-how-setup-service-contracts.md)  
[Huoltohallinto](service-service.md)  
[ALV-summia sisältävien huoltosopimusten muuntaminen](service-how-to-convert-service-contracts.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
