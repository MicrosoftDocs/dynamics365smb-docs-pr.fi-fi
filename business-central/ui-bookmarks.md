---
title: Roolikeskuksen sivun tai raportin kirjanmerkkilinkki
description: 'Kirjanmerkin kuvaketta käyttämällä voit lisätä toiminnon, joka avaa sivun tai raportin roolikeskuksen siirtymisvalikosta.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 07/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Sivun tai raportin merkitseminen kirjanmerkille omassa roolikeskuksessasi

Kirjanmerkin kuvaketta käyttämällä voit lisätä toiminnon, joka avaa sivun tai raportin roolikeskuksen siirtymisvalikosta. Kirjanmerkkien ansiosta voit nopeasti tavoittaa haluamasi sisällön tai liiketoimintatehtävän. Voit lisätä kirjanmerkin kohdesivulta tai -raportista siten, että näyttöön tulee roolikeskuksen linkki.

Kirjanmerkkikuvake näkyy sivun oikeassa yläkulmassa sekä **Kerro, mitä haluat tehdä** -ikkunassa, jossa voit lisätä kirjanmerkin useille sivuille tai raportteihin. Jos sivulla on jo kirjanmerkki, kuvake on tumma ja työkaluvihjeessä lukee Lisätty kirjanmerkkeihin.

## Kohteen kirjanmerkintä

1. Avaa haluamasi sivu roolikeskuksessa.
2. Valitse ![Kirjanmerkki.](media/ui_bookmark_icon.png "Kirjanmerkki") -kuvake.

Sivun mukaan nimetty toiminto lisätään nyt roolikeskuksen siirtymisvalikkoon.

## Merkitse kohderaportti kirjanmerkillä

1. Avaa mikä tahansa raporttipyyntösivu, johon haluat linkin roolikeskuksessasi.
2. Valitse ![Kirjanmerkki.](media/ui_bookmark_icon.png "Kirjanmerkki") -kuvake.

Raportin mukaan nimetty toiminto lisätään nyt roolikeskuksen siirtymisvalikkoon.

## Sivun tai raportin merkitseminen kirjanmerkillä Tell Me -ikkunasta

1. Avaa **Kerro, mitä haluat tehdä** -ikkuna ja kirjoita esimerkiksi **Myyntitilaukset**.
2. Siirrä osoitin **Myyntitilaukset**-sivun tai raportin hakutulosten päälle ja valitse sitten ![Kirjanmerkki.](media/ui_bookmark_icon.png "Kirjanmerkki") -kuvake.

Sivun tai raportin mukaan nimetty toiminto lisätään nyt roolikeskuksen siirtymisvalikkoon.

## Usein kysytyt kysymykset  

### Voinko järjestää kirjanmerkkini uudelleen?

Kyllä. Voit mukauttaa roolikeskustasi ja siirtää toiminnot optimaaliseen järjestykseen tai siirtää ne olemassa oleviin ryhmiin tai alaryhmiin.  
Lue lisää [Työtilan mukauttamisesta](ui-personalization-user.md).

### Miten poistan kirjanmerkin?

Poista toiminto roolikeskuksesta valitsemalla kohdesivulla tai -raportissa uudelleen kirjanmerkin kuvake. Voit myös mukauttaa roolikeskustasi ja piilottaa toiminnot väliaikaisesti poistamatta niitä kokonaan.

### Mistä löydän kirjanmerkkini?

Kun lisäät sivulle tai raporttiin kirjanmerkin, uusi toiminto lisätään nykyisen aloitusnäytön (Roolikeskuksen) siirtymisvalikon yläosaan. Jos sinulla sattuu olemaan useita toimintoja, **Lisää**-painike on ehkä aktivoitava, jotta voit näyttää ne kaikki, koska uusi toiminto liitetään aina näiden toimintojen loppuun.
<!-- Should we add a screenshot here? -->

### Minulla ei ole kirjanmerkkikuvaketta. Onko jokin vialla?

Sivun tai raportin kirjanmerkkien käyttäminen on yksi useista Business Centralin käyttäjän mukautetuista toiminnoista. Jos kirjanmerkkikuvake ei ole näkyvissä, järjestelmänvalvoja on todennäköisesti poistanut mukauttamisen käytöstä.

### Miksi en voi merkitä tiettyjä sivuja tai raportteja kirjanmerkkeihin?

Kaikkia sivuja ja raportteja ei voi merkitä kirjanmerkkeihin. Kun sivu tai raportti suoritetaan yrityssovelluksen hallitsemassa erikoiskontekstissa, kirjanmerkkikuvaketta ei näytetä. Esimerkiksi sivut, joita ei löydy **Ilmoita**-ikkunasta, mutta jotka on käynnistetty muualta, eivät näytä kirjanmerkkikuvaketta. Vastaavasti raportin pyyntösivut, joita käytetään vain suodatinten keräämiseen ilman raportin suorittamista, eivät näytä kirjanmerkkikuvaketta.

  Katso lisätietoja teknisistä [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method)- ja [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type)-tiedoista.

### Poistetaanko myös kirjanmerkkini, kun tyhjennät mukautukseni?

Kyllä. Kirjanmerkit sijaitsevat navigointivalikossa. Jos poistat siirtymisvalikon muutokset mistä tahansa sivusta tai tyhjennät kaikki roolikeskuksen mukautukset, kaikki uudet toiminnot poistetaan pysyvästi.

### Miksi kirjanmerkkikuvake ilmaisee edelleen, ettei sitä ole vieläkään merkitty kirjanmerkillä?

Kun lisäät kirjanmerkin, uusi toiminto lisätään Roolikeskuksen siirtymisvalikkoon, ja seuraavilla sivun tai raportin käynneillä näkyy tumma kirjanmerkkikuvake. Jos mukautat roolikeskustasi ja järjestät toiminnot uudelleen siirtämällä ne ryhmiin, kirjanmerkin kuvake ei ole enää tumma, ja voit lisätä myös uuden kirjanmerkin samalle sivulle tai raporttiin. Näin voit lisätä useita toimintoja samalle sivulle tai raporttiin ja luokitella ne eri ryhmiin.

### Miksi linkissäni raporttiin näkyy eri raportti?

Jotkin raportit voidaan korvata muilla raporteilla sen jälkeen, kun laajennusta on sovellettu Business Centraliin. Kun korvaaminen tapahtuu, uuden toiminnon tekstiä ei päivitetä, ja se näyttää edelleen alkuperäisen raportin nimen, mutta siirtyy uudempaan raporttiin. Voit korjata uuden toiminnon tekstin poistamalla uuden toiminnon ja lisäämällä sen uudelleen.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

### Onko XMLportsille saatavilla kirjanmerkkejä?

Ei. Tällä hetkellä XMLports-toimintojen lisääminen ei ole mahdollista käyttöliittymästä.

### Käännetäänkö kirjanmerkkini, kun muutan kieleni Business Centralissa?

Kun lisäät uuden toiminnon, kaikkia käännettyjä tekstejä, jotka olivat saatavilla kyseisellä hetkellä, käytetään myös kirjanmerkkejä lisättäessä. Jos uusi käännetty teksti lisätään myöhemmin, uusi toiminto ei sisällä uudempia käännöksiä.

### Miksi en voi lisätä tekstiä sivulle heti sen jälkeen, kun avaan sen kirjanmerkillä?

Kun sivu on merkitty kirjanmerkkeihin, sivu avautuu aina näkymätilassa kirjanmerkistä&mdash;vaikka se olisi ollut muokkaustilassa silloin, kun se asetettiin kirjanmerkiksi. Kuvakkeen **Tee muutoksia sivulla** valitseminen ![Näyttää kynäkuvakkeen sivun muokkaamista varten.](media/edit-pencil.png) sallii sinun lisätä tekstiä muokattaviin kenttiin.

## Katso myös

[Työtilan mukauttaminen](ui-personalization-user.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]