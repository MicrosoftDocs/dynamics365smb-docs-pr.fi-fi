---
title: Siirrä pankkivarat
description: Voit siirtää summia pankkitililtä toisille myös muissa valuutoissa kirjaamalla tapahtuman yleiseen päiväkirjaan.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bank account transfer, multiple currencies'
ms.search.form: 39
ms.date: 04/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Siirrä pankkivarat

Joskus on siirrettävä varoja yhdeltä pankkitililtä kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] toiselle. Se tehdään kirjaamalla tapahtuma **Yleinen päiväkirja** -sivulle. Tehtävä vaihtelee sen mukaan, käytetäänkö pankkitileillä samaa vai eri valuuttaa.

## Siirtojen kirjaaminen pankkitileillä, jotka käyttävät samaa valuuttakoodia

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleinen päiväkirja** ja valitse sitten vastaava linkki.
2. Täytä päiväkirjan rivillä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.
3. Valitse **Tilityyppi**-kentässä **Pankkitili**.
4. Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.
5. Syötä siirrettävä summa **Summa**-kenttään.

    Seuraavaksi sinun täytyy määrittää vastatili. Jos liittyvät kentät eivät ole näkyvissä, valitse **Näytä lisää sarakkeita** -toiminto, jolloin kaikki käytettävissä olevat kentät tulevat näkyviin.
6. Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.
7. Valitse **Vastatilin nro**-kentässä pankkitili, johon haluat siirtää varat.
8. Kirjaa päiväkirja.

## Siirtojen kirjaaminen pankkitileillä, joilla on eri valuuttakoodit

Voit siirtää varoja eri valuuttoja käyttävien pankkitilien välillä kirjaamalla kaksi yleisen päiväkirjan riviä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleinen päiväkirja** ja valitse sitten vastaava linkki.
2. Luo kaksi päiväkirjan riviä ja täytä **Kirjauspvm**- ja **Asiakirjan nro.** -kentät.
3. Valitse **Tyyppi**-kentän ensimmäisellä rivillä **Pankkitili**.
4. Valitse **Tilinro**-kentässä pankkitili, josta haluat siirtää varat.
5. Syötä **Summa**-kenttään summa pankkitilin valuuttana vähennysmerkin kanssa tai ilman sitä.

    > [!TIP]
    > Jos summan edessä ei ole merkkiä, se on debet-summa. Muussa tapauksessa kyseessä on kredit-summa.

    > [!NOTE]
    > Jotkin yritykset siirtävät tilit mieluiten erillisillä päiväkirjariveillä. Joissakin yrityksissä kirjataan kaikki yhdelle päiväkirjariville vastatilin avulla. Varmista käytäntö tarvittaessa paikalliselta asiantuntijalta.
    >
    > Jos yrityksessä halutaan käyttää vastatiliä, määritä **Vastatilin tyyppi** -kentän arvoksi **Pankkitili** ja määritä sitten **Vastatilin nro** -kentän arvoksi se pankkitili, jolle varat halutaan siirtää. Siirry sitten vaiheeseen 9 tai 10.
    >
    > Jos yrityksessä halutaan käyttää erillistä päiväkirjariviä, siirry seuraavaan vaiheeseen.
6. Valitse **Tyyppi**-kentän toisella rivillä **Pankkitili**.
7. Valitse **Tilinro**-kentässä pankkitili, johon haluat siirtää varat.
8. Syötä **Summa**-kenttään summa pankkitilin valuuttana vähennysmerkin kanssa tai ilman sitä.

    > [!TIP]
    > Jos summan edessä ei ole merkkiä, se on debet-summa. Muussa tapauksessa kyseessä on kredit-summa.
9. Jos päiväkirjassa käytetyt vaihtokurssit eroavat **Valuutan vaihtokurssit** -sivun kursseista, syötä uusi päiväkirjarivi vaihtokurssivoittoa tai -tappiota varten.  

    1. Valitse **KP-tili**-kentässä**Pankkitili**.  

    2. Syötä **Tilinro**-kenttään valuuttakurssivoittojen ja -tappioiden KP-tilin numero.  

    3. Syötä valuuttakurssin voitto tai tappio **Summa**-kenttään miinusmerkillä kanssa tai ilman sitä.

    > [!TIP]
    > Jos summan edessä ei ole merkkiä, se on debet-summa. Muussa tapauksessa kyseessä on kredit-summa.
10. Kirjaa päiväkirja.

## Katso myös

[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]