---
title: Tuottojen ja kulujen siirtäminen
description: 'Jos haluat tulouttaa tuoton tai kulun jaksoon, jonka aikana tapahtumaa ei kirjattu, voit siirtää tai lykätä ne automaattisesti tietyn aikataulun mukaan.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: postpone
ms.search.form: '1700, 1701, 1702, 1703, 1704, 1705, 1706, 1707'
ms.date: 12/06/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Tuottojen ja kulujen siirtäminen

Jos haluat tulouttaa tuoton tai kulun jaksoon, joka on eri kuin se, jonka aikana tapahtuma on kirjattu, käytä toimintoja, jotka siirtävät tuotot ja kulut automaattisesti tietyn aikataulun mukaan.

Voit jakaa tuotot tai kulut liittyville kirjanpitojaksoille määrittämällä sille resurssille, nimikkeelle tai KP-tilille siirtomallin, jolle tuotto tai kulu kirjataan. Kun kirjaat liittyvän myynti- tai ostoasiakirjan, tuotto tai kulu siirretään liittyville kirjanpitojaksoille sen siirron aikataulun mukaan, jota siirtomallin ja kirjauspäivämäärän asetukset koskevat.

## KP-tilin määrittäminen siirtoa varten

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Luo siirretyille tuotoille KP-tili täyttämällä tarvittavat kentät. Lisätietoja on kohdassa [Pääkirjanpito ja tilikartta](finance-general-ledger.md).
4. Luo siirretyille kuluille uusi KP-tili toistamalla vaiheet 2 ja 3.

Valitse kummallekin siirtotyypille **Tase** **Tyyppi**-kenttään. Anna tileille soveltuvat nimet, kuten esimerkiksi siirretyille tuotoille Ansaitsematon tulo ja siirretyille kuluille Maksamattomat kulut.

## Siirtomallin määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirtomallit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät.
4. Määritä **Laskentamenetelmä**-kenttään, miten **Siirron aikataulu** -sivun kunkin jakson **Summa**-kentän arvo lasketaan. Voit valita seuraavista vaihtoehdoista:

   * **Tasapoisto**: Jaksoittaiset siirtosummat lasketaan jaksojen lukumäärän mukaan. Ne jaetaan jakson pituuden mukaan.
   * **Tasan jaksoittain**: Jaksoittaiset siirtosummat lasketaan jaksojen lukumäärän mukaan. Ne jaetaan tasan kaikille jaksoille.
   * **Päivät jaksoittain**: Jaksoittaiset siirtosummat lasketaan jakson päivien lukumäärän mukaan.
   * **Käyttäjän määrittämä**: Jaksottaisia siirtosummia ei lasketa. Siirron aikataulu -sivun kunkin jakson **Summa**-kenttä on täytettävä manuaalisesti. Lisätietoja on Siirron aikataulun muuttaminen myyntilaskusta -osassa.
5. Määritä **Jakson kuvaus** -kenttään kuvaus, joka näytetään siirron kirjauksen tapahtumissa. Voit syöttää tyypillisille arvoille seuraavat paikanvaraajien koodit. Ne lisätään automaattisesti, kun jakson kuvaus näytetään.

   * %1 = jakson kirjauspäivämäärän päivän numero
   * %2 = jakson kirjauspäivämäärän viikon numero
   * %3 = jakson kirjauspäivämäärän kuukauden numero
   * %4 = jakson kirjauspäivämäärän kuukauden nimi
   * %5 = jakson kirjauspäivämäärän kirjanpitojakson nimi
   * %6 = jakson kirjauspäivämäärän tilikausi

Esimerkki: Kirjauspäivämäärä on 6.2.2016. Jos annat Kulut siirretty: %4 %6, näytettävä kuvaus on Kulut siirretty: helmikuu 2016.

## Siirtomallin määrittäminen nimikkeelle

> [!NOTE]  
> Tämän proseduurin vaiheet ovat samat kuin silloin, kun siirtomalli liitetään KP-tiliin tai -resurssiin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimike** ja valitse sitten vastaava linkki.
2. Avaa sen nimikkeen kortti, jonka tuotot tai kulut on siirrettävä kirjanpitojaksoille nimikkeen myynnin tai oston yhteydessä.
3. Valitse **Oletussiirtomalli**-kenttään sopiva siirtomalli.

## Siirtomallin muuttaminen myyntilaskusta

> [!NOTE]  
> Tämän menettelytavan vaiheet ovat samat kuin vaiheet silloin, kun kulun siirtomalli muutetaan ostolaskusta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.
2. Luo myyntilasku nimikkeestä, jolle on määritetty siirtomalli. Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).

    Huomaa, että heti, kun laskuriville on syötetty nimike (tai resurssi tai KP-tili), ohjelma syöttää **Siirron koodi** -kenttään määritetyn siirtomallin koodin.
3. Valitse **Siirron aikataulu** -toiminto.
4. Muuta **Siirron aikataulu** -sivun otsikon tai rivin arvojen asetuksia. Voit esimerkiksi siirtää summan lisäkirjanpitojaksoon.
5. Valitse **Laske aikataulu** -toiminto.
6. Valitse **OK**-painike. Myyntilaskun siirron aikataulu päivitetään. Liittyvää siirtomallia ei muuteta.

## Siirrettyjen tuottojen tai kulujen kirjanpitoon kirjaamisen tarkasteleminen

> [!NOTE]  
> Tämän menettelytavan vaiheet ovat samat kuin kulujen siirtojen kirjausten esikatselun vaiheet.

1. Valitse **Myyntilasku**-sivulla **Esikatsele kirjaus** -toiminto.
2. Valitse **Esikatsele kirjaus** -sivulla **KP-tapahtuma**-toiminto ja valitse sitten **Näytä aiheeseen liittyvät tapahtumat** -toiminto.

Tietylle siirtotilille, kuten Ansaitsematon tulo -tilille, kirjattavat KP-tapahtumat merkitään kuvauksella, joka syötettiin siirtomallin **Jakson kuvaus** -kenttään. Esimerkki: Siirretyt kulut: helmikuu 2016.

## Kirjattujen siirtojen tarkasteleminen Myynnin siirron yhteenveto -raportissa

> [!NOTE]  
> Tämän menettelytavan vaiheet ovat samat kuin Ostojen siirron yhteenveto -raportin tarkastelun vaiheet.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myynnin siirron yhteenveto** ja valitse sitten vastaava linkki.
2. Syötä **Myynnin siirron yhteenveto** -sivun **Saldon tilanne** -kenttään päivämäärä, johon asti siirretyt tuotot näytetään.
3. Valitse **Esikatsele**-painike.

## Kauden määrittäminen lykkäyksen kirjauksen sallimiseksi

Voit määrittää ajanjakson, jolloin ihmiset voivat kirjata transaktioita syöttämällä päivämäärät **Salli kirjaus kohteesta**- ja **Salli kirjaaminen kohteeseen** -kenttiin seuraavasti:

* Kaikille käyttäjille **Pääkirjanpidon asetukset** -sivulla
* Tietyille käyttäjille **Käyttäjäasetukset** -sivulla

Jos olet tehnyt sen, sinun täytyy tehdä poikkeuslykkäyksiä, jotta ne voitaisiin kirjata jakson ulkopuolelle. Voit määrittää kauden seuraavien vaiheiden avulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** tai **Käyttäjän määritys** ja valitse sitten vastaava linkki.
2. Syötä **Salli lykkäyskirjaus kohteesta**- ja **Salli lykkäyskirjaus kohteeseen** -kenttiin jakson alkamis- ja päättymispäivämäärä.

### Video-opastus

Seuraava video näyttää, kuinka voit määrittää ajanjakson, jonka aikana sallit ihmisten kirjata lykättyjä tuloja ja kuluja, ja kuinka määrittää poikkeuksia.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fG6C]

## Katso myös

[Taloushallinto](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käsitteleminen](ui-work-general-journals.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
