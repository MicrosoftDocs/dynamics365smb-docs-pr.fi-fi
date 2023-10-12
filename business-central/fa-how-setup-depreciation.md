---
title: Poistomenetelmien määrittäminen
description: Saatavilla olevia poistomenetelmiä on monia. Business Centralissa määritetään käyttöomaisuuden poistomenetelmä **Käyttöomaisuuskortti**-sivulla.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: write down
ms.date: 06/28/2021
ms.author: bholtorf
---

# Käyttöomaisuuden poiston määrittäminen

Rahoituslaskelmien ja tuloveropalautusten valmistelussa voi käyttää useita poistomenetelmiä. Monet suuret yritykset käyttävät tasapoistoja rahoituslaskelmissaan, koska sen avulla voidaan yleensä raportoida suurempia tuloja. Tuloverotarkoituksia varten monet yritykset käyttävät kuitenkin nopeutettua poistomenetelmää, kuten vähenevän saldon poistoa. Käyttöomaisuuden poistomenetelmä määritetään **Poistomenetelmä**-kentässä **Käyttöomaisuuden kortti** -sivulla. Lisätietoja eri menetelmistä on kohdassa [Poistomenetelmät](fa-depreciation-methods.md).

Poistokirjoissa määritetään eri käyttöomaisuustyyppien poistojen laskentatavat. Kussakin poistokirjassa määritetään yksittäisiä poistoehtoja. Voidaan määrittää esimerkiksi, että käyttöomaisuudelle tulisi tehdä poisto kolmen vuoden jaksolla yhteen kirjaan ja viiden vuoden jaksolla toiseen kirjaan.

Kun olet luonut asianmukaiset poistokirjat, kuhunkin käyttöomaisuuserään tulee liittää yksi tai usea poistokirja. Käyttöomaisuuteen liitettyä poistokirjaa kutsutaan käyttöomaisuuden poistokirjaksi. Poistokirjoja käyttöomaisuudelle voi määrittää kuinka monta tahansa.  

## Poistokirjan luominen

Käyttöomaisuuden poistokirjaan voidaan määrittää, miten käyttöomaisuus poistetaan. Useiden erilaisten poistomenetelmien hallitsemiseksi voidaan määrittää useita poistokirjoja.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poistokirjat** ja valitse sitten vastaava linkki.
2. Valitse **Poistokirjaluettelo**-sivulla **Uusi**-toiminto.
3. Täytä **Poistokirjakortti**-sivun kentät tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Voit tallentaa käyttöomaisuustapahtumat **Käyttöomaisuuden KP-päiväkirja**- tai **Käyttöomaisuuspäiväkirja**-sivulle sen mukaan, koskevatko tapahtumat talousraportointia vai sisäistä hallintaa. Määritä seuraavan vaiheen mukaisesti eri käyttöomaisuustoiminnoissa oletusarvoisesti käytettävien päiväkirjojen tyypit.
4. Valitse **Integrointi**-pikavälilehdessä niiden käyttöomaisuustoimintojen valintaruudut, jotka haluat kirjata **Käyttöomaisuuden KP-päiväkirja** -sivun avulla.
5. Toista vaiheet 2–4 jokaisen sellaisen poisto- tai kirjaustavan kohdalla, jonka haluat liittää käyttöomaisuuserään poistokirjana.

> [!IMPORTANT]
> Valitse **Pyöristä jaksottain poist.** -kenttää, jos haluat pyöristää lasketut kausittaiset poistosummat kokonaisluvuiksi. Esimerkiksi jos yrityksesi käyttää myös laskun pyöristystä kokonaislukuihin **Pääkirjanpidon asetukset** -sivulla, myös poistosummien pyöristäminen kokonaislukuihin voi auttaa läpinäkyvyyttä.

Jos esimerkiksi hävität käyttöomaisuuserän, jolle poistokirjassa ei määritetä pyöristystä, mutta yrityksesi pääkirjanpidon asetukset edellyttävät pyöristystä, ja käyttöomaisuudesta luovutaan, näyttöön tulee virhesanoma siitä, että summa on pyöristettävä tapahtumassa.  

## Poistokirjan liittäminen käyttöomaisuuteen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jolle haluat määrittää käyttöomaisuuden poistokirjan.
3. Täytä **Poistokirja**-pikavälilehden kentät tarvittaessa.
4. Jos käyttöomaisuuteen on liitettävä useita poistokirjoja, valitse **Lisää poistokirjoja** -toiminto.
5. Vaihtoehtoisesti voit valita **Poistokirjat**-toiminnon ja määrittää vähintään yhden käyttöomaisuuden poistokirjan.

    > [!NOTE]  
    >   Kun käytössä on manuaalinen poistomenetelmä, poistot on vietävä manuaalisesti käyttöomaisuuden KP-päiväkirjaan. **Laske poisto** -toiminto jättää huomiotta käyttöomaisuuserät, joille käytetään manuaalista poistomenetelmää. Tätä tapaa voidaan käyttää omaisuuserille, joille ei tehdä poistoja, kuten maa-alueille.

    > [!NOTE]  
    > Kun käytät käyttäjän määrittämää poistomenetelmää, poistokirja on määritettävä eri tavalla. Lisätietoja on kohdassa [Käyttäjän määrittämän poistomenetelmän määrittäminen](fa-how-setup-user-defined-depreciation-method.md).

## Poistokirjan liittäminen useisiin käyttöomaisuuseriin eräajon avulla

Jos haluat määrittää poistokirjan moneen käyttöomaisuuteen, voit luoda **Luo KO:n poistokirjat** -eräajolla käyttöomaisuuden poistokirjat.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten vastaava linkki.
2. Valitse käyttöomaisuus, jolle haluat määrittää ja liittää poistokirjan. Valitse sitten **Muokkaa**-toiminto.
3. Valitse **Poistokirjakortti**-sivulla **Luo KO:n poistokirjat** -toiminto.
4. Täytä **Luo KO:n poistokirjat** -sivun **Poistokirja**-kenttä.
5. Valitse ensin **Kopioi KO:sta nro** -kenttä ja valitse sen käyttöomaisuuserän numero, jota haluat käyttää pohjana uusien käyttöomaisuuspoistokirjojen luomisessa.

    Jos tämä kenttä täytetään, uusien KO-poistokirjojen poistokentissä on samat tiedot kuin kopioitavan KO-poistokirjan vastaavissa kentissä. Jätä kenttä tyhjäksi, jos haluat luoda uusia KO:n poistokirjoja, joissa on tyhjiä poistokenttiä.  
6. **Käyttöomaisuus**-pikavälilehteen voidaan asettaa suodatus valitsemaan se omaisuus, jolle halutaan luoda käyttöomaisuuden poistokirjat.
7. Valitse **OK**-painike.

## Poiston kirjaustyyppien määrittäminen

Kunkin poistokirjan osalta on määritettävä, miten [!INCLUDE[prod_short](includes/prod_short.md)] käsittelee eri kirjaustyyppejä. Voit esimerkiksi määrittää, että tuleeko kirjauksen olla debet vai kredit, ja tuleeko kirjaustyyppi sisällyttää poistopohjaan.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poistokirjat** ja valitse sitten vastaava linkki.  
2. Valitse poistokirja, jonka. Valitse sitten **KO:n kirjaustyypin asetukset** -toiminto.
3. Täytä **KO:n kirjaustyypin asetukset** -sivulla tarvittavat kentät.

    > [!NOTE]  
    >   **KO:n kirjaustyypin asetukset** -sivulla ei voi lisätä rivejä eikä poistaa niitä. Ainoastaan olemassa olevia rivejä voi muuttaa.

On hyvin suositeltavaa, ettei niiden poistokirjojen asetuksia muuteta, joiden osalta on jo kirjattu tapahtumia. Muutokset eivät vaikuta jo kirjattuihin tapahtumiin, mikä tekee poistokirjatilastoista harhaanjohtavia.

## Käyttöomaisuuden poiston oletusmallien ja -erien määrittäminen

Kunkin poistokirjan osalta määritellään mallien ja erien oletusasetukset. Voit monistaa näillä oletusarvoilla yhden päiväkirjan rivit toiseen päiväkirjaan, luomaan päiväkirjarivejä **Laske poisto**- tai **Tee indeksimuutos KO:teen** -eräajoilla ja monistamaan vakuutuspäiväkirjan hankintamenoja.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poistokirjat** ja valitse sitten vastaava linkki.  
2. Valitse poistokirja, jolle haluat määrittää oletuspäiväkirjat. Valitse sitten **KO-päiväkirjan asetukset** -toiminto.  
3. Jos haluat, että jokaisella käyttäjällä on oletusasetukset, valitse **Käyttäjätunnus**-kenttä, jotta voit tehdä valinnan **Käyttäjät**-sivulla.  
4. Valitse muille kentille oletusarvoisesti käytettävä päiväkirjamalli tai -erä.  

## Tilikausi 365 päivää -kentän poisto

Kun Laske poisto -eräajo laskee poistot, eräajo käyttää tavallisesti standardisoitua 360 päivän vuotta, jossa kussakin 12 kuukaudessa on 30 päivää.

Jos valitset tämän kentän, Laske poisto -eräajo käyttää sen sijaan 365 päivän kalenterivuotta, jossa kullekin kuukaudelle lasketaan sama päivien määrä kuin kalenterissa. Ainoa poikkeus on karkausvuosien helmikuu, jolloin helmikuussa ei katsota olevan 29 vaan 28 päivää. Tämän vuoksi kaikki vuodet, myös karkausvuodet, katsotaan 365 päivän pituisiksi.

## Katso myös

[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Taloushallinto](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
