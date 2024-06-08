---
title: Sivun tai raportin kirjanmerkkilinkki roolikeskuksessa
description: 'Voit lisätä kirjanmerkin kuvakkeella toimintolinkin, joka avaa sivun tai raportin roolikeskuksen siirtymisvalikosta.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Sivun tai raportin kirjanmerkin luominen roolikeskuksessa
Voit lisätä kirjanmerkin kuvakkeella toimintolinkin, joka avaa sivun tai raportin roolikeskuksen siirtymisvalikosta. Kirjanmerkkien ansiosta voit nopeasti tavoittaa haluamasi sisällön tai liiketoimintatehtävän. Kirjanmerkki lisätään kohdesivulta tai raportista eli ruudusta, jonka haluat roolikeskuksen linkin avaavan.

Kirjanmerkkikuvake näkyy sivun oikeassa yläkulmassa sekä **Kerro, mitä haluat tehdä** -ikkunassa, jossa voit lisätä kirjanmerkin useille sivuille tai raportteihin. Jos sivulla on jo kirjanmerkki, kuvake on tumma ja työkaluvihjeessä lukee Lisätty kirjanmerkkeihin.

## Voit merkitä kohdesivun kirjanmerkiksi
1. Avaa sivu, johon haluat roolikeskuksen linkin kohdistuvan.
2. Valitse ![Kirjanmerkki.](media/ui_bookmark_icon.png "Kirjanmerkki") -kuvake.

Sivun mukaan nimetty toiminto lisätään nyt roolikeskuksen siirtymisvalikkoon.

## Voit merkitä kohderaportin kirjanmerkiksi
1. Avaa raporttipyyntö, johon haluat roolikeskuksen linkin kohdistuvan.
2. Valitse ![Kirjanmerkki.](media/ui_bookmark_icon.png "Kirjanmerkki") -kuvake.

Raportin mukaan nimetty toiminto lisätään nyt roolikeskuksen siirtymisvalikkoon.

## Sivun tai raportin kirjanmerkin lisääminen Ilmoita-ikkunasta
1. Avaa **Kerro, mitä haluat tehdä** -ikkuna ja kirjoita esimerkiksi **Myyntitilaukset**.
2. Siirrä osoitin **Myyntitilaukset**-sivun tai raportin hakutulosten päälle ja valitse sitten ![Kirjanmerkki.](media/ui_bookmark_icon.png "Kirjanmerkki") -kuvake.

Sivun tai raportin mukaan nimetty toiminto lisätään nyt roolikeskuksen siirtymisvalikkoon.


## Usein kysytyt kysymykset  

- **Voinko järjestellä kirjanmerkkini uudelleen?**  
Kyllä. Voit mukauttaa roolikeskuksesi ja siirtää toiminnot optimaaliseen järjestykseen tai siirtää ne olemassa oleviin ryhmiin tai alaryhmiin.  
Lue lisää [Työtilan mukauttamisesta](ui-personalization-user.md).

- **Miten poistan kirjanmerkin?**  
Valitse kohdesivun tai -raportin kirjanmerkkikuvake uudelleen, jos haluat poistaa liittyvän toiminnon roolikeskuksistasi. Voit myös mukauttaa roolikeskuksesi ja piilottaa toiminnot väliaikaisesti poistamatta niitä kokonaan.

- **Mistä löydän kirjanmerkkini?**  
Kun lisäät kirjanmerkin sivuun tai raporttiin, uusi toiminto lisätään aloitusnäytön yläsiirtymisvalikkoon (roolikeskus). Jos sinulla sattuu olemaan useita toimintoja, **Lisää**-painike on ehkä aktivoitava, jotta voit näyttää ne kaikki, koska uusi toiminto liitetään aina näiden toimintojen loppuun.
<!-- Should we add a screenshot here? -->

- **Minulla ei ole kirjanmerkkikuvaketta. Onko jotain vialla?**  
Sivun tai raportin kirjanmerkkien käyttäminen on yksi useista Business Centralin käyttäjän mukautetuista toiminnoista. Jos kirjanmerkkikuvake ei ole näkyvissä, järjestelmänvalvoja on todennäköisesti poistanut mukauttamisen käytöstä.

- **Miksi tiettyjä sivuja tai raportteja ei voi merkitä kirjanmerkkeihin?**  
Kaikkia sivuja ja raportteja ei voi merkitä kirjanmerkkeihin. Kun sivu tai raportti suoritetaan yrityssovelluksen hallitsemassa erikoiskontekstissa, kirjanmerkkikuvaketta ei näytetä. Esimerkiksi sivut, joita ei löydy **Ilmoita**-ikkunasta, mutta jotka on käynnistetty muualta, eivät näytä kirjanmerkkikuvaketta. Vastaavasti raportin pyyntösivut, joita käytetään vain suodatinten keräämiseen ilman raportin suorittamista, eivät näytä kirjanmerkkikuvaketta.

  Katso lisätietoja teknisistä [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method)- ja [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type)-tiedoista.

- **Onko omat kirjanmerkkini poistettu yksilöinnin poistamisen yhteydessä?**  
Kyllä. Kirjanmerkit sijaitsevat navigointivalikossa. Jos tyhjennät navigointivalikkoon miltä tahansa sivulta tekemäsi muutokset tai poistat kaikki roolikeskuksen mukautukset, kaikki uudet toiminnot poistetaan pysyvästi.

- **Miksi kirjanmerkkikuvake osoittaa edelleen, ettei sitä ole vielä merkitty kirjanmerkkeihin?**  
Kun lisäät kirjanmerkin, uusi toiminto lisätään roolikeskuksen navigointivalikkoon ja sen jälkeen sivulle tai raporttiin tehdyt käynnit näyttävät tumman kirjanmerkkikuvakkeen. Jos mukautat roolikeskuksen ja järjestät toiminnot uudelleen siirtämällä ne ryhmiin, kirjanmerkkikuvake ei ole enää tumma ja voit lisätä saman sivun tai raportin toiseen kirjanmerkkiin. Näin voit lisätä useita toimintoja samalle sivulle tai raporttiin ja luokitella ne eri ryhmiin.

- **Miksi linkki raporttiin näyttää eri raportin?**  
Jotkin raportit voidaan korvata muilla raporteilla sen jälkeen, kun laajennusta on sovellettu Business Centraliin. Kun korvaaminen tapahtuu, uuden toiminnon tekstiä ei päivitetä, ja se näyttää edelleen alkuperäisen raportin nimen, mutta siirtyy uudempaan raporttiin. Voit korjata uuden toiminnon tekstin poistamalla uuden toiminnon ja lisäämällä sen uudelleen.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **Onko kirjanmerkkeihin saatavilla XMLports-määritteitä?**  
Ei. Tällä hetkellä XMLports-toimintojen lisääminen ei ole mahdollista käyttöliittymästä.

- **Käännetäänkö kirjanmerkkini, kun vaihdan kieltä Business Centralissa?**  
Kun lisäät uuden toiminnon, kaikkia käännettyjä tekstejä, jotka olivat saatavilla kyseisellä hetkellä, käytetään myös kirjanmerkkejä lisättäessä. Jos uusi käännetty teksti lisätään myöhemmin, uusi toiminto ei sisällä uudempia käännöksiä.

- **Miksi sivulle ei voi lisätä tekstiä heti sen jälkeen, kun se on avattu kirjanmerkillä?**<br> Kun sivu on merkitty kirjanmerkkeihin, sivu avautuu aina näkymätilassa kirjanmerkistä&mdash;vaikka se olisi ollut muokkaustilassa silloin, kun se asetettiin kirjanmerkiksi. Kuvakkeen **Tee muutoksia sivulla** valitseminen ![Näyttää kynäkuvakkeen sivun muokkaamista varten.](media/edit-pencil.png) sallii sinun lisätä tekstiä muokattaviin kenttiin.


## Katso myös
[Työtilan mukauttaminen](ui-personalization-user.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]