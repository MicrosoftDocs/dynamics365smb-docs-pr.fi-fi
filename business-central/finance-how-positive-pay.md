---
title: Vie Posit. osto -tiedostot
description: 'Voit varmistaa toimittaja- ja maksutiedot sisältävän Positive Pay -tiedoston viennin avulla, että pankki vahvistaa vain tarkistetut sekit ja summat.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'check, clearing'
ms.search.form: '1231, 1232, 1233, 1234'
ms.date: 07/18/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Positive Pay -tiedoston vienti
Kun viet toimittajan tiedot, sekin numeron ja maksun summan sisältävän Positive Pay -tiedoston, jonka sitten lähetät viitetiedoiksi pankkiin maksuja käsitellessäsi, voit varmistaa, että pankki vahvistaa vain tarkistetut sekit ja summat.

[!INCLUDE[prod_short](includes/prod_short.md)] on määritetty tukemaan Bank of American ja City Bankin Positive Pay -tiedostoja.

## Positive Pay -pankkitilin määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Avaa sen pankin kortti, jossa haluat käyttää Positive Pay -toimintoa.
3. Kirjoita **Positive Pay -vientikoodi** -kenttään POSPAYBANK.
4. Sulje sivu.

## Positive Pay -tiedoston vienti
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Valitse pankkitili, johon haluat viedä Positive Pay -tiedoston.
3. Valitse **Positive Pay, vienti** -toiminto.

    **Positive Pay, vienti** -sivu avautuu ja näkyvissä on maksut, jotka on tehty pankkitilille edellisen latauspäivän jälkeen (**Edellinen latauspvm**- ja **Edellinen latausaika** -kentät).
4. Määritä Katkaisun **lähetyspvm -** kenttään päivämäärä, jota ennen maksut eivät sisälly vietyun tiedostoon.
5. Valitse **Vie**-toiminto.
6. Valitse **Vie tiedosto** -sivulla **Tallenna**-painike ja tallenna tiedosto sopivaan paikkaan.
7. Lataa tiedosto sähköisen pankin sivustoon.
8. Kirjoita muistiin tai kopioi vahvistusnumero, joka näkyy, kun tiedoston lataus on onnistunut.

## Vietyjen Positive Pay -tietueiden näyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Valitse pankkitili, jonka Positive Pay -vientitietueet haluat näyttää.
3. Valitse **Positive Pay -tapahtumat** -toiminto.

    Kaikki pankkitilin Positive Pay -vientitietueet näkyvät **Positive Pay -tapahtumat** -sivulla.
4. Anna kunkin vientitietueen **Vahvistusnumero**-kenttään numero, jonka sait, kun tiedoston lataus pankkiin onnistui.
5. Voit tarkastella liittyviä maksurivejä valitsemalla **Positive Pay -tapahtuman tiedot** -toiminnon.

## Positive Pay -tiedostojen uudelleenvienti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.
2. Valitse pankkitili, johon haluat viedä Positive Pay -tiedostot uudelleen.
3. Valitse **Positive Pay -tapahtumat** -toiminto.
4. Valitse uudelleenvietävä Positive Pay -vientitiedoston rivi.
5. Valitse **Positive Pay -tapahtumat** -sivulla **Vie Positive Pay -maksu uudelleen tiedostoon** -toiminto.

## Katso myös
[Taloushallinto](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käsitteleminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]