---
title: Projektin tarvikkeiden hallinta
description: Käsitellään erilaisia tapoja hallita tarvikkeita sekä ostaa materiaaleja ja palveluja projekteihin.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'project management, material, purchase'
ms.search.form: '98, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Projektin tarvikkeiden hallinta

Projektin tarvikkeiden nimikkeiden, palveluiden ja kulujen hallinta on olennainen ja tärkeä kaikkien projektien osa. Voit käyttää varastomääriä tai tehdä projektikohtaisia ostoja ostotilausten tai ostolaskujen avulla. Oletetaan esimerkiksi, että tietokoneen huoltoprojektia varten tarvitaan uusi levy. Uuden levyn ostamista varten luodaan uusi ostolasku ja projekti, jossa sitä käytetään, kirjataan.

Jos ostoprosessi ei edellytä, että fyysinen tapahtuma kirjataan erikseen, osto voidaan käsitellä **Projektin KP-päiväkirja** -sivulla. Lisätietoja on kohdassa [Projektiin liittyvän kulun kirjaaminen](projects-how-manage-project-supplies.md#to-post-a-project-related-expense).

## Nimikkeiden tai palveluiden ostaminen projektille

Seuraavassa kerrotaan, miten projektille ostetaan tuotteita ostolaskun avulla. Samat vaiheet toimivat myös silloin, kun käytetään ostotilausta.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).
3. Valitse **Projektin nro** **Projektitehtävän nro** -kentissä sen projektin tiedot, jolle haluat ostaa nimikkeitä tai huoltoja. Käytä mukautustyökaluja, jos kenttä ei ole näkyvissä. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

    **Projektin rivityyppi** -kentässä valitsemasi arvo määrittää, luodaanko suunnittelurivi nimikkeen käytön kirjaamisen yhteydessä. Jos kentän arvo on **Laskutettava**, ne projektin suunnittelurivit, jotka ovat valmiita asiakkaalta laskutettaviksi, luodaan. Lisätietoja on kohdassa [Projektien laskutus](projects-how-invoice-jobs.md).
4. Valitse **Kirjaa**-toiminto.

## Projektin ostojen arvon tarkasteleminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.
2. Avaa sopiva projektikortti.

    **Tehtävät**-pikavälilehden **Avoimet tilaukset** -kentässä näkyy projektin tehtävärivin ostoasiakirjojen varastonimikkeiden ja palveluiden avoin summa paikallisena valuuttana.  

    **Ei laskut. vast.ottojen summa** -kentässä näkyy ostoasiakirjoja vastaan toimitettujen, mutta vielä laskuttamattomien, nimikkeiden arvo.  
3. Valitse jompikumpi kentistä ja avaa **Ostorivit**-sivu, jossa voit tarkastella liittyvien ostoasiakirjarivien tietoja sekä tietoa siitä, mitkä nimikkeet tai palvelut on vastaanotettu.

## Projektiin liittyvän kulun kirjaaminen

Jos sisällytät satunnaisen tai kertaluontoisen projektin kuluja, voit käyttää **Projektin KP-päiväkirja** -sivua ja kirjata ne suoraan soveltuvalle projektitilille.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektin KP-päiväkirjat** ja valitse sitten vastaava linkki.  
2. Luo uusi rivi ja syötä kulua koskevat tiedot, mukaan lukien tiedot **Projektinro**- ja **Projektitehtävän nro** -kentissä.  
3. Kun päiväkirja on valmis, valitse **Kirjaa**-toiminto.

## Katso myös

[Projektien hallinta](projects-manage-projects.md)  
[Taloushallinto](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Business Centralin käyttäminen](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
