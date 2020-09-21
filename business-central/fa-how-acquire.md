---
title: Käyttöomaisuuden hankinta| Microsoft Docs
description: Voit määrittää käyttöomaisuuserän, liittää poistokirjan ja kirjata käyttöomaisuuserän hankintakustannuksen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 79416d72d8ded71025270b4408e8425e0be2c827
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781158"
---
# <a name="acquire-fixed-assets"></a>Hankittu käyttöomaisuus
Kunkin käyttöomaisuuserän osalta tulee määrittää kortti, joka sisältää tietoja kyseisestä käyttöomaisuuserästä. Voit määrittää rakennuksia tai tuotantolaitoksia pääkäyttöomaisuuseräksi. Voit myös ryhmitellä niitä eri tavoin, kuten esimerkiksi luokan, osaston ja sijainnin mukaan. Kullekin käyttöomaisuuserälle on määritettävä ja liitettävä poistokirja ennen hankintaa.

Kun käyttöomaisuuserä on määritetty ja poistokirja liitetty, käyttöomaisuuserä on hankittava. Voit hankkia käyttöomaisuuserän tallentamalla sen hankintamenon asianmukaiselle KO-tilille, pankkitilille tai toimittajan tietoihin kirjaamalla **Käyttöomaisuuden KP-päiväkirja** -sivun hankintatapahtuman. Voit luoda ja kirjata vaaditun yleisen päiväkirjan rivit automaattisesti **Käyttöomaisuuden avustettu hankinta** -sivun avulla.

Jäännösarvo on käyttöomaisuuden jäljellä oleva arvo silloin, kun käyttöomaisuutta ei voida enää käyttää. Voit kirjata jäännösarvon samaan aikaan, kun hankintameno kirjataan. Lisätietoja on kohdassa [Käyttöomaisuuden poisto tai kuoletus](fa-how-depreciate-amortize.md).

Indeksointia käytetään muuttamaan arvoja yleisten hintatason muutosten mukaan. Tee **Indeksimuutos KO:teen** -eräajoa voidaan käyttää laskemaan hankintamenot vaihtokustannuksilla.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>Käyttöomaisuuden luominen ja hankinta automaattisesti
Seuraavassa kuvataan, miten käyttöomaisuuserä luodaan ja miten se hankitaan **Käyttöomaisuuden avustettu hankinta** -sivun avulla vaaditun käyttöomaisuuserän KP-päiväkirjarivien luomista ja kirjaamista varten. Voit myös luoda ja kirjata päiväkirjarivit manuaalisesti. Lisätietoja on kohdassa [Käyttöomaisuuden hankinnan kirjaaminen manuaalisesti käyttöomaisuuden KP-päiväkirjan avulla](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuus** ja valitse sitten liittyvä linkki.  
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

Sekä pääkäyttöomaisuuserä että kaikki sen komponentit tulee määrittää omiksi käyttöomaisuuden korteiksi. Sen jälkeen kun komponenttiluettelo on määritetty, [!INCLUDE[d365fin](includes/d365fin_md.md)] täyttää automaattisesti käyttöomaisuuskorttien **Pääkäyttöomais.erä/komponentti**- ja **Pääkäyttöomaisuuserän kompon.** -kentät.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse käyttöomaisuuserä, joka on pääkäyttöomaisuuserä, ja valitse **Pääkäyttöom.erän komponentit** -toiminto.
3. Valitse **Pääkäyttöom.erän komponentit** -sivulla **KO-nro**-kenttä. Valitse sitten käyttöomaisuuserä, jonka haluat lisätä pääkäyttöomaisuuserän komponenttina.
4. Sulje sivu.
5. Toista työvaiheet 3 ja 4 jokaisen lisättävän komponenttiomaisuuserän osalta.
6. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuuden asetukset** ja valitse sitten liittyvä linkki.
7. Valitse **Salli kirj. Pääkäyttöom.eriin** -valintaruutu.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>Käyttöomaisuuden hankinnan kirjaaminen manuaalisesti käyttöomaisuuden KP-päiväkirjan kanssa
Seuraavassa kerrotaan, miten käyttöomaisuus hankitaan manuaalisesti luomalla ja kirjaamalla rivit **Käyttöom. KP-päiväkirja** -sivulla. Voit hankkia käyttöomaisuuden myös automaattisesti **Käyttöomaisuuden avustettu hankinta** -sivun avulla. Lisätietoja on kohdan [Käyttöomaisuuden luominen ja hankinta automaattisesti](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically) vaiheessa 5.

> [!NOTE]  
>   Voit kirjata hankintamenon myös hyvityksinä. Muista tällöin, että **Summa**-kentän arvon edessä on oltava hyvityksen osoittava miinusmerkki.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuuden KP-päiväkirjat** ja valitse sitten liittyvä linkki.
2. Valitse **Käyttöom. KP-päiväkirja** -sivun **KO:n kirjaustyyppi** -kentässä **Hankintameno**.
3. Täytä tarvittavat jäljellä olevat kentät.
4. Valitse **Kirjaa**-toiminto.  

> [!TIP]  
>   Jos käyttöomaisuuden KP-päiväkirjan **Vakuutusnro**-kenttä täytetään silloin, kun hankintameno kirjataan, [!INCLUDE[d365fin](includes/d365fin_md.md)] kirjaa käyttöomaisuuden hankintamenon myös vakuutuksen kattavuuskirjauksiin. Lisätietoja on kohdassa [Käyttöomaisuuden vakuuttaminen](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Yhden käyttöomaisuuserän hankintamenon kirjauksen peruuttaminen
Jos teet virheen hankintamenon kirjaamisessa, voit poistaa tapahtuman **Peruuta KO-tapahtumia** -eräajon avulla ja kirjata sitten oikean hankintatapahtuman. Virheelliset merkinnät siirretään **KO-virhetapahtumat** -sivulle.

Jos esimerkiksi kirjaat hankinnan virheelliselle päivämäärälle, se on korjattava mahdollisimman pian, koska käyttöomaisuuserän kirjauspäivämäärää käytetään useissa tärkeissä laskelmissa.

> [!IMPORTANT]  
>   **Peruuta tapahtumat** -toimintoa ei voi käyttää käyttöomaisuustapahtumissa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Peruuta KO-tapahtumia** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Suorita eräajo valitsemalla **OK**.
4. Kun virheellinen tapahtuma tai tapahtumat on peruutettu, voit kirjata oikean hankintamenon.

Voit peruuttaa useiden käyttöomaisuuserien tapahtumakirjaukset kerralla **Peruuta KO-tapahtumat** -eräajon avulla.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Jäännösarvon kirjaaminen yhdessä hankintamenon kanssa
Jäännösarvon voi kirjata käyttöomaisuuden KP-päiväkirjasta yhdessä hankintamenon kanssa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **KO-päiväkirjat** ja valitse sitten liittyvä linkki.
2. Luo hankintarivi **Käyttöomaisuuspäiväkirjat**-sivulla. Lisätietoja on kohdassa [Käyttöomaisuuden hankinnan kirjaaminen manuaalisesti käyttöomaisuuden KP-päiväkirjan avulla](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).
3. Syötä jäännösarvosumma hyvityksenä (miinusmerkillä varustettuna) **Jäännösarvo**-kenttään.
4. Valitse **Kirjaa**-toiminto.

> [!NOTE]
> Jos käyttöomaisuudelle on olemassa jäännösarvo, kyseistä arvoa käytetään poistokirjauksessa**KO-poistokirjat** -sivun **Loppukirjanpitoarvo**-kentän arvon sijaan. Lisätietoja on kohdassa [Loppukirjanpitoarvon hallinta](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-also"></a>Katso myös
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Rahoitus](finance.md)  
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
