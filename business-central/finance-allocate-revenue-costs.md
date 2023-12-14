---
title: Tuoton ja kustannusten kohdistaminen useille kirjanpitotileille
description: Kustannusten kohdistaminen pääkirjanpidon tileille.
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
---

# Tuoton ja kustannusten kohdistaminen useille kirjanpitotileille

Tässä artikkelissa kuvataan, miten kohdistustilejä käytetään summien jakamiseen myynti- ja ostoasiakirjoissa sekä yleisen päiväkirjan riveillä eri KP-tileille. Summia voi kohdistaa kiinteän tai muuttuvan jaon avulla.  

Kohdistus jakaa yleisen päiväkirjan rivin **Kohdistustili**-sivulla määritettyihin riveihin. Jos esimerkiksi jaat vuokrakulun kolmeen eri tapaan dimensioita käyttämällä, sinulla on kolme riviä kirjattavana kohdistukselle. Tämän vuoksi KP-rivejä on kuusi (tai mahdollisesti enemmän, jos käytät ALV:tä tai myyntiveroa). Vaikka tämä kirjaa enemmän KP-tapahtumia kuin tarvitset, voit peruuttaa yksittäisiä rivejä sen sijaan, että peruuttaisit koko kohdistuksen.

Myös kohdistustilit toimivat siirtojen kanssa. Jos haluat lisätietoja siirroista, katso kohta [Tuottojen ja kulujen siirtäminen](finance-how-defer-revenue-expenses.md).

Seuraavassa taulukossa esitellään käytettävissä olevat kohdistusmenetelmät.

|Kohdistustapa  |Kuvaus  |
|---------|---------|
|Korjattu     | Kun haluat jakaa kulut tavalla, joka toistetaan pidemmällä aikavälillä, voit käyttää kiinteää kohdistusta. Kiinteä kohdistus mahdollistaa kohdistuksen jakamisen. Tämä jako muuttuu vain, kun asetuksia muutetaan **Kohdistustili**-sivulla.        |
|Muuttuva     | Kun haluat jakaa tuoton tai kulut ajan mittaan muuttuviin arvoihin, käytä muuttuvaa kohdistusmenetelmää. Muuttuvien kohdistusten avulla voit määrittää käytettävät lähteet kohdistusprosenttien laskennassa. Tämä menetelmä on hyödyllinen esimerkiksi sellaisten työntekijöiden kustannusten jakamisessa, jotka ovat osastojen eri henkilöstömäärän mukaan. Toinen esimerkki on vuokrakustannusten jakaminen tuotannon lattiamateriaalin perusteella, joka saattaa vaihdella tuotantorivin mukaan ajan mittaan. Muuttujakohdistukset määrittävät dimensioiden ja tilastotilien yhdistelmän avulla, miten summat jakautuvat tietylle jaksolle. Saat lisätietoja tilastotileistä, kun valitset [Analysoi tietoja tilastotilien avulla](bi-use-statistical-accounts.md). Saat lisätietoja dimensioista siirtymällä kohtaan [Dimensioiden käyttäminen](finance-dimensions.md).        |

## Summien kohdistamiseen käytetään kiinteää osaketta tai prosenttiosuutta

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kohdistustili** ja valitse sitten liittyvä linkki.  
1. Valitse **Kohdistustilit**-sivulta **Uusi**.
1. Anna **Nro** ja **Nimi**-kentät.
1. Valitse **Tilityyppi**-kentässä **Kiinteä**.
1. Valitse **Kohdetilin tyyppi** -kentässä **KP-tili** tai **Pankkitili**.
1. Valitse **Kohdetilin numero** -kentässä tili, jolle arvo kirjataan.
1. Valinnainen: Valitse **Dimensiot**-toiminto ja määritä sitten riville kirjattavat dimensiot.
1. Määritä **Jaa**- ja **Prosentti**-kenttiin, miten summat jaetaan kohdetilille.
  
   > [!TIP]
   > Jos todellinen kohdistettava summa syötetään kiinteälle kohdistukselle **Jaa**-kenttään, **Prosentti**-kentässä näkyy prosenttiosuus kokonaissummasta.
1. Toista tämä prosessi jokaisen kohdistukseen sisällytettävän tilin osalta.

## Summien kohdistamiseen käytetään muuttuvaa menetelmää

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Kohdistustili** ja valitse sitten liittyvä linkki.  
1. Valitse **Kohdistustilit**-sivulta **Uusi**.
1. Anna **Nro** ja **Nimi**-kentät.
1. Valitse **Tilityyppi**-kentässä **Muuttuva**.
1. Valitse **Kohdetilin tyyppi** -kentässä **KP-tili**.
1. Valitse **Kohdetilin numero** -kentässä tili, jolle arvo kirjataan.
1. Valitse **Erittelytilin tyyppi** -kentässä **Tilastotili**.
1. Valitse **Laskentajakso**-kentässä jakso, jolta summat jaetaan.
1. Valinnainen: Voit suodattaa tiettyjen globaalien dimensioiden arvojen mukaan valitsemalla **Erittelytilin saldosuodattimet** -toiminnon ja määrittämällä sitten suodattimen arvot.
1. Valinnainen: Valitse **Dimensiot**-toiminto ja määritä sitten riville kirjattavat dimensiot.

## Summien kohdistaminen lennossa

Luot kohdistustilejä tulon ja kustannusten jakamiseen KP-tileille ja pankkitileille. Kohdistuksen automatisointi voi säästää paljon aikaa. Jos kuitenkin haluat käyttää kohdistustilejä, mutta et halua luoda niitä jokaiselle KP-tilille, voit säästää vielä enemmän aikaa.

Peri pääelementistä -vaihtoehdon avulla voit käyttää kohdistustiliä jakaaksesi summia minkä tahansa KP-tilin osalta asiakirjan tai päiväkirjan rivillä. Asiakirjan tai päiväkirjan rivin **Tilityyppi**-kentässä valitaan KP-tili ja valitaan kohdistustili **Kohdistustilin numero** -kentästä. Rivillä oleva summa jaetaan KP-tilin osalta kohdistustilisi asetusten mukaisesti. Se on vähemmän läpinäkyvä tapa kohdistaa, mutta sinun ei tarvitse luoda kohdistustiliä erityisesti KP-tilille.

Tapauskohtaiset kohdistukset on helppo määrittää. Sen sijaan, että määrität pankin tai KP-tilin **Kohdistustili**-sivun **Kohdetilin tyyppi** -kenttään, valitse **Peri pääelementistä**. Jätä **Kohdetilin numero** -kenttä tyhjäksi. Kun valitset KP-tilin asiakirjalle tai päiväkirjan riville, kyseistä tiliä käytetään summien kohdistamiseen.

## Tarkista, että summat jakautuvat oikein, ennen kuin kirjaat ne.

Voit tarkistaa seuraavilla tavoilla, miten summat jakautuvat oikein:

* Valitse **Kohdistustili**-sivulta **Testikohdistus**-toiminto. Käytä **Kohdistettava summa** -kenttää, kun haluat testata eri summia.
* Valitse **Pääkirjanpidon päiväkirjat** -sivulla päiväkirja ja käytä **Kirjauksen esikatselu** -toimintoa.

## Muuta jakoa

Jos löydät kohdistuksesta jotain, jota haluat muuttaa, voit muuttaa kohdistusta ennen sen kirjaamista.  

1. Avaa asiakirja tai päiväkirja, jossa on kohdistus, jota haluat muuttaa.
1. Valitse rivi ja sitten **Jaa tilin kohdistukset uudelleen** -toiminto.
1. Tee muutokset **Muuta kohdistuksia** -sivulla.

## Kohdistustransaktion kirjaaminen

Seuraavassa kuvataan, miten kohdistustransaktio kirjataan yleisestä päiväkirjasta. Vaiheet ovat samat myynti- ja ostoasiakirjoille.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.  
1. Luo uusi rivi. Täytä kentät samalla tavalla kuin minkä tahansa muuntyyppisen yleisen päiväkirjan osalta.
1. Jos käytät kiinteää tai muuttuvaa kohdistusta, täytä seuraavat kentät:
    1. Valitse **Tilityyppi** -kentässä **Kohdistustili**.
    1. Valitse **Tilinro**-kentässä kohdistustili.
1. Jos käytät kohdistusta, joka käyttää Peri pääelementistä -vaihtoehtoa, tee seuraavat toimet:
    1. Valitse **Tilityyppi**-kentässä **KP-tili**.
    1. Valitse **Tilinumero**-kentässä KP-tili.
    1. **Kohdistustilin nro** -kentässä, valitse kohdistustili, joka on määritetty käyttämään Peri pääelementistä -vaihtoehtoa. 
1. Valitse **Kirjaa**.

## Katso myös

[Yleisten päiväkirjojen käsitteleminen](ui-work-general-journals.md)  