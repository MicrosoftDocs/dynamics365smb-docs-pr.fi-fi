---
title: Käyttöomaisuuden hankkiminen
description: 'Voit määrittää käyttöomaisuuserän, liittää poistokirjan ja kirjata käyttöomaisuuserän hankintakustannuksen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="acquire-fixed-assets"></a>Käyttöomaisuuden hankkiminen

 **Käytä Käyttöomaisuuden kortti -** sivua syöttääksesi tietoja käyttöomaisuuserästä. Voit määrittää rakennuksia tai tuotantolaitoksia pääkäyttöomaisuuseräksi. Voit myös ryhmitellä niitä eri tavoin, kuten esimerkiksi luokan, osaston ja sijainnin mukaan. Poistokirja tulee määrittää ja määritellä kullekin käyttöomaisuuserälle ennen kuin sen voi hankkia.

Sen jälkeen kun käyttöomaisuuserä on määritetty ja poistokirja määriteltävä, käyttöomaisuus tulee hankkia. Voit hankkia käyttöomaisuuserän tallentamalla sen hankintamenon asianmukaiselle KO-tilille, pankkitilille tai toimittajan tietoihin kirjaamalla **Käyttöomaisuuden KP-päiväkirja** -sivun hankintatapahtuman. Voit luoda ja kirjata vaaditun yleisen päiväkirjan rivit automaattisesti **Käyttöomaisuuden avustettu hankinta** -sivun avulla.

Indeksimuutosten käyttäminen yleisten hintatason muutosten mukaan. Käytä Luetteloi KO: **teen -** eräajoa hankintamenojen ja vaihtokustannusten laskemiseen.

## <a name="add-a-fixed-asset-to-your-list-of-fixed-assets"></a>Lisää käyttöomaisuus käyttöomaisuusluetteloon

Ennen kuin käyttöomaisuuserän voi hankkia, se tulee lisätä omaisuuserien luetteloon. Luetteloon voi lisätä käyttöomaisuuserät usealla eri tavalla:

* Syötä käyttöomaisuuserien **tiedot Käyttöomaisuuden kortti -** sivulle.
*  **Lataa käyttöomaisuusluettelo työkirjaan Muokkaa Excelissä** -toiminnon avulla, lisää luetteloon uusia omaisuuseriä ja julkaise päivitystoiminto [!INCLUDE [prod_short](includes/prod_short.md)].
* Lisää käyttöomaisuuserät ostotilauksen avulla.
*  **Käytä Kopioi käyttöomaisuus -** toimintoa.

Kun olet lisännyt käyttöomaisuuserät luetteloon, seuraava vaihe on käyttöomaisuuden hankkiminen, jotta niitä voi käyttää transaktioissa. Lisätietoja on käyttöomaisuuden [hankinnassa](#acquire-fixed-assets).

### <a name="add-a-fixed-asset-on-the-fixed-asset-card-page"></a>Käyttöomaisuuden lisääminen Käyttöomaisuuden kortti -sivulle

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittaessa **Yleinen**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Täytä **Poistokirja**-pikavälilehden kentät tarvittaessa. Tässä vaiheessa poistokirja liitetään käyttöomaisuuteen.  
4. Jos käyttöomaisuuteen on liitettävä useita poistokirjoja, valitse **Lisää poistokirjoja** -toiminto. Lisätietoja on siirryttäessä [poistokirjan määrittelemiseen käyttöomaisuudelle](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Kun tarvittavat kentät on täytetty, **käyttöomaisuuden voi hankkia.** -ilmoitus tulee näkyviin sivun yläosaan. Jos olet nyt valmis hankkimaan omaisuuserän, valitse Hankinta-toiminto **·** . Suorita hankinta loppuun noudattamalla **avustetun käyttöomaisuuden hankinta** -sivun työvaiheita. Jos et ole valmis, voit hankkia omaisuuserän aina myöhemmin.

### <a name="use-edit-in-excel-to-add-assets"></a>Lisää käyttöomaisuuseriä Muokkaa Excelissä -kentässä.

Jos haluat lisätä useita käyttöomaisuuseriä, Muokkaa Excelissä on hyvä työkalu käytettäväksi. Työkalu lataa nykyisen luettelon työkirjan omaisuuseristä, joka sisältää suurimman osan Käyttöomaisuuden kortti -sivulla saatavilla olevista kentistä. Voit täyttää kunkin omaisuuserän rivin kentät tai kaikki kentät sekä lisätä ne luetteloon [!INCLUDE [prod_short](includes/prod_short.md)] julkaisemalla muutokset. Jos et voi täyttää kaikkia tarvittavia kenttää, se on ok. Voit päivittää tiedot, [!INCLUDE [prod_short](includes/prod_short.md)] kun olet valmis.

> [!NOTE]
> Jos haluat käyttää Muokkaa Excelissä -toimintoa, sinun on Microsoft Dynamics asennettava Office-lisäosa. Lisäosa luo yhteyden Excelin ja [!INCLUDE [prod_short](includes/prod_short.md)] Excelin välille. Lisätietoja on [Hae Business Central -lisäosa Excelissä](admin-deploy-excel-addin.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse Jaa :::image type="content" source="media/share-icon.png" alt-text="tämä sivu muiden käyttäjien tai sovellusten kanssa -kuvake."::: -kuvaketta ja valitse **muokkaa Excelissä**.
3. Avaa ladattu tiedosto ja syötä tietoja uudesta käyttöomaisuudesta.

   > [!TIP]
   > Sinun ei tarvitse syöttää tunnistetta Nro-kenttään **.** . Kun päivität tiedot, [!INCLUDE [prod_short](includes/prod_short.md)]  määrittelee tunnuksen käyttöomaisuudelle käyttämäsi numerosarjan perusteella.

4. Voit päivittää [!INCLUDE [prod_short](includes/prod_short.md)] valitsemalla **Microsoft Dynamics** ruudussa **Julkaise**.

### <a name="add-a-fixed-asset-from-a-purchase-order-or-invoice"></a>Käyttöomaisuuden lisääminen ostotilauksesta tai -laskusta

Seuraavassa kuvataan, miten käyttöomaisuus lisätään ostotilauksesta. Vaiheet ovat samanlaiset ostolaskun kohdalla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.
2. Luo uusi ostotilaus valitsemalla **Uusi** .
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
4. Valitse Rivit-pikavälilehden **·**  **Tyyppi-kentässä**  **Käyttöomaisuus**.
5. Valitse **Nro**-kenttään -kentästä, joko valitse olemassa oleva käyttöomaisuus kustannukseen tai lisää uusi käyttöomaisuuserä valitsemalla **Uusi** .
6. Kun olet syöttänyt uuden omaisuuserän ja ostotilauksen tiedot, valitse **Kirjaa**.

## <a name="acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal"></a>Käyttöomaisuuden hankkiminen käyttöomaisuuden KP-päiväkirjaa käyttämällä

Seuraavassa kuvataan, miten hankinta luodaan ja kirjataan tarvittavien käyttöomaisuuden KP-päiväkirjarivien avulla. Voit myös luoda ja kirjata päiväkirjarivit manuaalisesti. Jos haluat lisätietoja, siirry käyttöomaisuuden hankintaan [käyttämällä käyttöomaisuuden KP-päiväkirjaa](#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
1. Valitse käyttöomaisuuserä, jonka haluat hankkia, ja valitse **sitten Hanki-toiminto** .
1. Suorita hankinta loppuun noudattamalla **avustetun käyttöomaisuuden hankinta** -sivun työvaiheita.

> [!NOTE]  
> Voit kirjata hankintamenon myös hyvityksinä. Muista tällöin, että **Hankintameno (sis. ALV)** -kentän arvon edessä on oltava hyvityksen osoittava miinusmerkki.

Kun valitaan **Valmis**, Käyttöomaisuuden kortti **-sivulla oleva** Kirjanpitoarvo-kenttä **täytetään**, mikä tarkoittaa, että käyttöomaisuus on hankittu määritellyllä hankintamenolla.  

## <a name="to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal"></a>Käyttöomaisuuden hankinnan kirjaaminen manuaalisesti käyttöomaisuuden KP-päiväkirjalla

Seuraavassa kerrotaan, miten käyttöomaisuus hankitaan manuaalisesti luomalla ja kirjaamalla rivit **Käyttöom. KP-päiväkirja** -sivulla. Käyttöomaisuuden voi hankkia automaattisesti **myös Käyttöomaisuuden kortti -** sivulla valitsemalla **Hanki käyttöomaisuus -** toiminnon. Lisätietoja on siirry kohdasta [Käyttöomaisuuden](#acquire-fixed-assets) hankkiminen.

> [!NOTE]  
> Voit kirjata hankintamenon myös hyvityksinä. Muista tällöin, että **Summa**-kentän arvon edessä on oltava hyvityksen osoittava miinusmerkki.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöom. KP-päiväkirjat** ja valitse sitten liittyvä linkki.
2. Valitse **Käyttöom. KP-päiväkirja** -sivun **KO:n kirjaustyyppi** -kentässä **Hankintameno**.
3. Täytä tarvittavat jäljellä olevat kentät.
4. Valitse **Kirjaa**-toiminto.  

> [!TIP]  
> Jos Vakuutusnro-kenttä **·**  täytetäänkirjaa [!INCLUDE[prod_short](includes/prod_short.md)]  myös käyttöomaisuuden hankintamenon vakuutuksen kattavuuskirjauksiin. Lisätietoja on kohdassa [Käyttöomaisuuden vakuuttaminen](fa-how-insure.md).

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Komponenttiluetteloiden määrittäminen pääkäyttöomaisuuserälle

Käyttöomaisuuden voi ryhmitellä pääkäyttöomaisuuseriksi ja niiden komponenteiksi. Tuotantokone voi koostyä esimerkiksi useista osista, jotka haluat ryhmitllä tällä tavalla.  

Pääomaisuuserä ja kaikki sen komponentit tulee määrittää yksittäiseksi käyttöomaisuuseräksi. Sen jälkeen kun komponenttiluettelo on määritetty, [!INCLUDE[prod_short](includes/prod_short.md)]  se täyttää automaattisesti käyttöomaisuuserän Pää käyttöomaisuuserät/komponentit **·** - ja **Pääomaisuuserän** komponentit -kentät.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuuserä, joka on pääkäyttöomaisuuserä, ja valitse **Pääkäyttöom.erän komponentit** -toiminto.
3. Valitse **Pääkäyttöom.erän komponentit** -sivulla **KO-nro**-kenttä. Valitse sitten käyttöomaisuuserä, jonka haluat lisätä pääkäyttöomaisuuserän komponenttina.
4. Sulje sivu.
5. Toista työvaiheet 3 ja 4 jokaisen lisättävän komponenttiomaisuuserän osalta.
6. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuden asetukset** ja valitse sitten vastaava linkki.
7.  **Ota Käyttöön Salli kirjaus pääomaisuuseriin** -vaihto.

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Yhden käyttöomaisuuserän hankintamenon kirjauksen peruuttaminen

Jos teet virheen hankintamenon kirjaamisessa, voit poistaa tapahtuman **Peruuta KO-tapahtumia** -eräajon avulla ja kirjata sitten oikean hankintatapahtuman. Virheelliset merkinnät siirretään **KO-virhetapahtumat** -sivulle.

Jos esimerkiksi kirjaat hankinnan väärälle päivämäärälle, se on korjattava mahdollisimman pian, koska käyttöomaisuuserän kirjauspäivämäärää käytetään monissa laskelmissa.

> [!IMPORTANT]  
> Peruuta **transaktiot -toimintoa** ei voi käyttää käyttöomaisuustapahtumille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **KO-tapahtumat** ja valitse sitten vastaava linkki.  
2. Valitse **KO-tapahtumat**-sivulta tapahtuma tai tapahtumat, jotka haluat peruuttaa.  
3. Valitse **Toiminnot**-valikko ja valitse sitten **Peruuta tapahtumat** -toiminto.
4. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Suorita eräajo valisemalla **OK**.
6. Kun virheellinen tapahtuma tai tapahtumat on peruutettu, voit kirjata oikean hankintamenon.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Jäännösarvon kirjaaminen yhdessä hankintamenon kanssa

Jäännösarvo on käyttöomaisuuden jäljellä oleva arvo silloin, kun käyttöomaisuutta ei voida enää käyttää. Voit kirjata jäännösarvon samaan aikaan, kun hankintameno kirjataan. Lisätietoja on käyttöomaisuuden [poistossa](fa-how-depreciate-amortize.md) tai poistossa.

Jäännösarvon voi kirjata käyttöomaisuuden KP-päiväkirjasta yhdessä hankintamenon kanssa.

> [!NOTE]
> Tämä prosessi voi edellyttää, että Käyttöomaisuuspäiväkirjat-sivua mukautetaan lisäämällä Jäännösarvo-kenttä. Kenttää ei oletusarvoisesti näytetä sivulla. Jos haluat lisätietoja, siirry [asiakkaaksi Jako-toiminnolla Henkilö](ui-personalization-user.md), joka on henkilökohtainen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuspäiväkirjat** ja valitse sitten liittyvä linkki.
2. Luo hankintarivi **Käyttöomaisuuspäiväkirjat**-sivulla. Jos haluat lisätietoja, siirry kirjaamaan [käyttöomaisuuden hankinta manuaalisesti käyttöomaisuuden KP-päiväkirjan avulla](#to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal).
3. Syötä kirjankansionrivien **Jäännösarvo**-kenttään jäännösarvosumma hyvityksenä (lisää summan eteen miinusmerkki, kuten **-** 100).
4. Valitse **Kirjaa**-toiminto.

> [!NOTE]
> Jos käyttöomaisuudelle on olemassa jäännösarvo, tätä arvoa käytetään poistokirjauksessa KO:n poistokirjat **-sivun Loppukirjanpitoarvo-kentän**  **arvon** sijaan. Lisätietoja on [loppukirjanpitoarvon](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value) hallinnassa.

## <a name="see-also"></a>Katso myös

[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Suunnittele yksityiskohtaisia tietoja ei-määritettävissä olevasta ALV-vaikutuksesta Käyttöomaisuuteen](design-details-nondeductible-vat.md)  
[Taloushallinto](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
