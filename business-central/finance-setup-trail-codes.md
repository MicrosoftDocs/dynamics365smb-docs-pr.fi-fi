---
title: Kirjausketjujen määrittäminen
description: Lue lisää kirjausketjujen seurantaan käytettävien lähdekoodien ja syykoodien määrittämisestä.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '257, 259, 279'
ms.date: 04/01/2021
ms.author: edupont
---
# Kirjausketjujen lähdekoodien ja syykoodien määrittäminen

Kaikille kirjatuille tapahtumille määritetään automaattisesti lähdekoodi niin, että tapahtumien alkuperä voidaan jäljittää. Jos haluat antaa tapahtumille lisälähdekoodin, voit käyttää syykoodeja. Syykoodien avulla ilmaistaan, miksi tapahtuma on luotu. Syykoodit voidaan määrittää luomisen yhteydessä koko päiväkirjan malliin ja erään sekä yksittäisiin päiväkirjan riveihin ja asiakirjoihin.  

Käytä koodeja, jotka on helppo muistaa ja jotka ovat kuvaavia, käyttämällä sekä lähdekoodeja että syykoodeja. Koodin tulee olla yksilöivä, ja voit määrittää niin monta koodia kuin haluat.

## Lähdekoodien määrittely

Joskus haluat saada selville, miten tietty tapahtuma on syntynyt: esimerkiksi onko tapahtuma syntynyt yleisen päiväkirjan kirjauksen vai ostolaskun kirjauksen tuloksena. Lähdekoodi ilmaisee, missä tapahtuma on syntynyt. Tapahtumia syntyy, kun päiväkirja tai lasku kirjataan ja kun tietyt eräajot suoritetaan. Jokaisella kirjaustyypillä on oma lähdekoodinsa, joka liitetään, kun yksittäinen tapahtuma luodaan.  

Päiväkirjojen, tilausten, laskujen ja hyvityslaskujen kirjaaminen, sekä eräajojen suorittaminen luovat tapahtumia taloudellisiin raportteihin. **Lähdekoodiasetukset**-sivulla on useita pikavälilehtiä, yksi kutakin sovellusaluetta varten. Jokaisessa pikavälilehdessä on asianomaisen sovellusalueen lähdekoodit.

Kun kirjaat tai suoritat eräajon, ohjelma liittää tapahtumaan automaattisesti oikean lähdekoodin. Kun esimerkiksi kirjaat yleisestä päiväkirjasta, ohjelma antaa tapahtumalle koodin *YLEINENPVK*. Tämän jälkeen voit suodattaa **Pääkirjanpidon tapahtumat** -sivun näyttämään, mitkä tapahtumat on kirjattu yleisestä päivä kirjasta tai myynti asiakirjoista, esimerkiksi

### Lähdekoodien määrittely

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Lähdekoodin määritys** ja valitse sitten vastaava linkki.  

2. Määritä **lähdekoodin määrittely** -ikkunassa kunkin kirjaustyypin ja eräajon osalta asianmukainen lähdekoodi.  

Kentän sisältöä voi muuttaa myöhemmin, ja muutos vaikuttaa tuleviin kirjauksiin.

## Lähdekoodien muuttaminen

Haluat ehkä muuttaa lähdekoodia. Saatat haluta muuttaa lähdekoodin *YLEINENPVK* koodiksi *YLEINEN*.

### Lähdekoodien muuttaminen

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Lähdekoodit** ja valitse sitten vastaava linkki.

2. Valitse sillä rivillä, jolla muutettava koodi on, koodi **Koodi**-kentästä.

3. Syötä uusi koodi ja napsauta sitten **Kyllä**. Voit myös muuttaa **Kuvaus**-kentän sisältöä.

Kaikilla uusilla kirjauksilla, jotka jatkossa kirjataan yleisestä päiväkirjasta, tulee olemaan tämä uusi lähdekoodi.

## Syykoodien määrittäminen

Syykoodit täydentävät lähdekoodeja, ja niiden avulla ilmaistaan, miksi tapahtuma luotiin. Voit määritellä syykoodeja yksittäisissä merkinnöissä ja voit liittää pysyvät koodit tiettyihin päiväkirjan malleihin ja päiväkirjan eriin. Kun syykoodi on linkitetty päiväkirjan riviin tai myyntien tai ostojen otsikkoon, ohjelma merkitsee kaikkiin tapahtumiin syykoodin kirjatessaan tapahtumat.  

### Syykoodien määrittäminen

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake")  -kuvake, syötä **Syykodit** ja valitse sitten vastaava linkki.

2. Anna **Syykoodit**-ikkunan **Koodi**-kenttään ensimmäinen koodi. Syötä **Kuvaus**-kenttään selittävä teksti.

Toista nämä vaiheet kaikkien niiden koodien osalta, joita haluat käyttää. Voit määrittää niin monta koodia kuin haluat.

Seuraavassa kuvataan, miten syykoodi lisätään päiväkirjan malliin, mutta vastaavat vaiheet koskevat syykoodin lisäämistä päiväkirjan riville tai päiväkirjan erään.  

### Syykoodien määrittäminen päiväkirjan malleissa

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake")  -kuvake, syötä **Yleisen päiväkirjan mallit** ja valitse sitten liittyvä linkki.

2. Määritä haluamasi koodi valitsemasi päiväkirjan mallin sisältävän rivin **Syykoodi**-kenttään.

3. Sulje päiväkirjan malli.

Valittu syykoodi kopioituu niihin uusiin päiväkirjan eriin, jotka on luotu tämän päiväkirjan mallin avulla. Syykoodeja liitetään päiväkirjan malleihin samalla tavalla muilla sovellusalueilla.

### Syykoodien käyttäminen myynti- ja ostoasiakirjoissa

1. Avaa asianomainen myynti- tai ostoasiakirja.

2. Kirjoita koodi myynti- tai osto-otsikon **Syykoodi**-kenttään.

Kun lasku on kirjattu, syykoodi kopioituu kaikkiin KP-, asiakas- ja toimittajatapahtumiin. Et voi liittää erilaisia syykoodeja yksittäisille osto- ja myyntiriveille, koska kaikki rivit kirjataan yhtenä tapahtumana.

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/set-up-financial-management-dynamics-365-business-central/)

## Katso myös

[Rahoitus](finance.md)  
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
