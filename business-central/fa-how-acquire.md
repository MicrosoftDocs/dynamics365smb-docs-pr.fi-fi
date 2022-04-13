---
title: Hankittu käyttöomaisuus
description: Voit määrittää käyttöomaisuuserän, liittää poistokirjan ja kirjata käyttöomaisuuserän hankintakustannuksen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.search.form: 5605, 5551, 5600, 5628, 5629, 5633
ms.date: 12/03/2021
ms.author: edupont
ms.openlocfilehash: 46d8b491727f566c9a96640e3dfb40cc0d417f40
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519249"
---
# <a name="acquire-fixed-assets"></a>Hankittu käyttöomaisuus
Kunkin käyttöomaisuuserän osalta tulee määrittää kortti, joka sisältää tietoja kyseisestä käyttöomaisuuserästä. Voit määrittää rakennuksia tai tuotantolaitoksia pääkäyttöomaisuuseräksi. Voit myös ryhmitellä niitä eri tavoin, kuten esimerkiksi luokan, osaston ja sijainnin mukaan. Kullekin käyttöomaisuuserälle on määritettävä ja liitettävä poistokirja ennen hankintaa.

Kun käyttöomaisuuserä on määritetty ja poistokirja liitetty, käyttöomaisuuserä on hankittava. Voit hankkia käyttöomaisuuserän tallentamalla sen hankintamenon asianmukaiselle KO-tilille, pankkitilille tai toimittajan tietoihin kirjaamalla **Käyttöomaisuuden KP-päiväkirja** -sivun hankintatapahtuman. Voit luoda ja kirjata vaaditun yleisen päiväkirjan rivit automaattisesti **Käyttöomaisuuden avustettu hankinta** -sivun avulla.

Jäännösarvo on käyttöomaisuuden jäljellä oleva arvo silloin, kun käyttöomaisuutta ei voida enää käyttää. Voit kirjata jäännösarvon samaan aikaan, kun hankintameno kirjataan. Lisätietoja on kohdassa [Käyttöomaisuuden poisto tai kuoletus](fa-how-depreciate-amortize.md).

Indeksointia käytetään muuttamaan arvoja yleisten hintatason muutosten mukaan. Tee **Indeksimuutos KO:teen** -eräajoa voidaan käyttää laskemaan hankintamenot vaihtokustannuksilla.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>Käyttöomaisuuden luominen ja hankinta automaattisesti
Seuraavassa kuvataan, miten käyttöomaisuuserä luodaan ja miten se hankitaan **Käyttöomaisuuden avustettu hankinta** -sivun avulla vaaditun käyttöomaisuuserän KP-päiväkirjarivien luomista ja kirjaamista varten. Voit myös luoda ja kirjata päiväkirjarivit manuaalisesti. Lisätietoja on kohdassa [Käyttöomaisuuden hankinnan kirjaaminen manuaalisesti käyttöomaisuuden KP-päiväkirjan avulla](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittaessa **Yleinen**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Täytä **Poistokirja**-pikavälilehden kentät tarvittaessa. Tässä vaiheessa poistokirja liitetään käyttöomaisuuteen.  
4. Jos käyttöomaisuuteen on liitettävä useita poistokirjoja, valitse **Lisää poistokirjoja** -toiminto. Lisätietoja on kohdassa [Käyttöomaisuuden poistokirjan määrittäminen](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Kun kaikki käyttöomaisuuden hankinnassa vaadittavat kentät on täytetty, sivun yläosaan tulee näkyviin **Nyt voit hankkia käyttöomaisuuden. Hanki** -ilmoitus.
5. Valitse ilmoituksen **Hanki**-toiminto.
6. Seuraa **Käyttöomaisuuden avustettu hankinta** -sivun vaiheita ja tee käyttöomaisuuden automaattinen hankinta valmiiksi.

> [!NOTE]  
>   Voit kirjata hankintamenon myös hyvityksinä. Muista tällöin, että **Hankintameno (sis. ALV)** -kentän arvon edessä on oltava hyvityksen osoittava miinusmerkki.

Kun valitset **Valmis**-arvon **Kirjanpitoarvo**-kenttä **Käyttöomaisuuden kortti** -sivulla täytetään. Se osoittaa, että käyttöomaisuus on hankittu tietyn hankintamenon avulla.  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Komponenttiluetteloiden määrittäminen pääkäyttöomaisuuserälle
Käyttöomaisuuden voi ryhmitellä pääkäyttöomaisuuseriksi ja niiden komponenteiksi. Tähän tapaan voi ryhmitellä esimerkiksi tuotantokoneen, joka koostuu useista osista.  

Sekä pääkäyttöomaisuuserä että kaikki sen komponentit tulee määrittää omiksi käyttöomaisuuden korteiksi. Sen jälkeen kun komponenttiluettelo on määritetty, [!INCLUDE[prod_short](includes/prod_short.md)] täyttää automaattisesti käyttöomaisuuskorttien **Pääkäyttöomais.erä/komponentti**- ja **Pääkäyttöomaisuuserän kompon.** -kentät.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuuserä, joka on pääkäyttöomaisuuserä, ja valitse **Pääkäyttöom.erän komponentit** -toiminto.
3. Valitse **Pääkäyttöom.erän komponentit** -sivulla **KO-nro**-kenttä. Valitse sitten käyttöomaisuuserä, jonka haluat lisätä pääkäyttöomaisuuserän komponenttina.
4. Sulje sivu.
5. Toista työvaiheet 3 ja 4 jokaisen lisättävän komponenttiomaisuuserän osalta.
6. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuden asetukset** ja valitse sitten vastaava linkki.
7. Valitse **Salli kirj. Pääkäyttöom.eriin** -valintaruutu.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>Käyttöomaisuuden hankinnan kirjaaminen manuaalisesti käyttöomaisuuden KP-päiväkirjan kanssa
Seuraavassa kerrotaan, miten käyttöomaisuus hankitaan manuaalisesti luomalla ja kirjaamalla rivit **Käyttöom. KP-päiväkirja** -sivulla. Voit hankkia käyttöomaisuuden myös automaattisesti **Käyttöomaisuuden avustettu hankinta** -sivun avulla. Lisätietoja on kohdan [Käyttöomaisuuden luominen ja hankinta automaattisesti](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically) vaiheessa 5.

> [!NOTE]  
>   Voit kirjata hankintamenon myös hyvityksinä. Muista tällöin, että **Summa**-kentän arvon edessä on oltava hyvityksen osoittava miinusmerkki.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO - KP-päiväkirjat** ja valitse sitten vastaava linkki.
2. Valitse **Käyttöom. KP-päiväkirja** -sivun **KO:n kirjaustyyppi** -kentässä **Hankintameno**.
3. Täytä tarvittavat jäljellä olevat kentät.
4. Valitse **Kirjaa**-toiminto.  

> [!TIP]  
>   Jos käyttöomaisuuden KP-päiväkirjan **Vakuutusnro**-kenttä täytetään silloin, kun hankintameno kirjataan, [!INCLUDE[prod_short](includes/prod_short.md)] kirjaa käyttöomaisuuden hankintamenon myös vakuutuksen kattavuuskirjauksiin. Lisätietoja on kohdassa [Käyttöomaisuuden vakuuttaminen](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Yhden käyttöomaisuuserän hankintamenon kirjauksen peruuttaminen
Jos teet virheen hankintamenon kirjaamisessa, voit poistaa tapahtuman **Peruuta KO-tapahtumia** -eräajon avulla ja kirjata sitten oikean hankintatapahtuman. Virheelliset merkinnät siirretään **KO-virhetapahtumat** -sivulle.

Jos esimerkiksi kirjaat hankinnan väärälle päivämäärälle, se on korjattava mahdollisimman pian, koska käyttöomaisuuserän kirjauspäivämäärää käytetään monissa laskelmissa.

> [!IMPORTANT]  
> **Peruuta tapahtumat** -toimintoa ei voi käyttää käyttöomaisuustapahtumissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **KO-tapahtumat** ja valitse sitten vastaava linkki.  
2. Valitse **KO-tapahtumat**-sivulta tapahtuma tai tapahtumat, jotka haluat peruuttaa.  
3. Valitse **Toiminnot**-valikko ja valitse sitten **Peruuta tapahtumat** -toiminto.
4. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Suorita eräajo valisemalla **OK**.
6. Kun virheellinen tapahtuma tai tapahtumat on peruutettu, voit kirjata oikean hankintamenon.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Jäännösarvon kirjaaminen yhdessä hankintamenon kanssa
Jäännösarvon voi kirjata käyttöomaisuuden KP-päiväkirjasta yhdessä hankintamenon kanssa.

> [!NOTE]
> Tämä prosessi voi edellyttää, että Käyttöomaisuuspäiväkirjat-sivua mukautetaan lisäämällä Jäännösarvo-kenttä. Kenttää ei oletusarvoisesti näytetä sivulla. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuuspäiväkirjat** ja valitse sitten liittyvä linkki.
2. Luo hankintarivi **Käyttöomaisuuspäiväkirjat**-sivulla. Lisätietoja on kohdassa [Käyttöomaisuuden hankinnan kirjaaminen manuaalisesti käyttöomaisuuden KP-päiväkirjan avulla](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).
3. Syötä kirjankansionrivien **Jäännösarvo**-kenttään jäännösarvosumma hyvityksenä (lisää summan eteen miinusmerkki, kuten **-** 100).
4. Valitse **Kirjaa**-toiminto.

> [!NOTE]
> Jos käyttöomaisuudelle on olemassa jäännösarvo, kyseistä arvoa käytetään poistokirjauksessa **KO-poistokirjat** -sivun **Loppukirjanpitoarvo**-kentän arvon sijaan. Lisätietoja on kohdassa [Loppukirjanpitoarvon hallinta](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-also"></a>Katso myös
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Rahoitus](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]