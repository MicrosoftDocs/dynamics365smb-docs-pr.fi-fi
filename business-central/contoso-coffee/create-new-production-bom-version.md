---
title: Uuden tuotannon tuoterakenteen ja tuoterakenneversion luominen
description: 'Vaihekuvaus, jossa kerrotaan, miten toinen kahvinkeitin lisätään Contoso Coffee -tuotelinjaan Business Centralissa.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Vaihekuvaus: Uuden tuotannon tuoterakenteen ja tuoterakenneversion luominen

Tässä artikkelissa on tietoja Contoso Coffee -esittelytietojen käytöstä tuoterakenteen käytössä tuotantoprosesseissa.  

## Esimerkkitilanne

Contoso Coffee on päättänyt lisätä toisen kahvinkeittimien tuotelinjaan: **SP-SCM1008 Airpot Lite**. Tämä kahvinkeitin on identtinen nykyisen nimikkeen **SP-SCM1009 Airpot** kanssa, paitsi että se ei sisällä lämmityslevyä **SP-BOM1104**. Erillisessä vaiheessa on/off-merkki valo, **SP-BOM1106** poistetaan Airpot Liten tuoterakenteen versiosta.

Contoso Coffeen prosessi-insinööri Oscarin on määritettävä uusi tuotannon tuoterakenne, joka määrittää Airpot Liten alkuperäiset komponenttivaatimukset. Tämän jälkeen hänen täytyy määrittää uusi tuoterakenneversio, jonka alkamis päivämäärä on 1. heinäkuuta, ja se on yhdenmukaistettava lisäsuunnitelmien kanssa toisen painoksen julkaisemiseksi.

## Vaiheet

1. Luo uusi tuotannon tuoterakenne Airpot Litelle.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotannon tuoterakenne** ja valitse sitten vastaava linkki.  

    2. Valitse **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä  |Arvo  |
        |---------|---------|
        |**Ei.** |SP-SCM1008|
        |**Kuvaus** |Airpot Lite|
        |**Mittayksikön koodi**|KPL  |

2. Kopioi tuoterakenteen komponentit tuotannon tuoterakenteesta **SP-SCM1009**.

    1. Valitse **Kopioi tuoterakenne** -toiminto.

    2. Valitse **Tuotantotuoterakent.** -sivulla kohteen **SP-SCM1009, Airpot** rivi ja valitse sitten **OK**-painike.

3. Muuta uuden tuotannon tuoterakenteen komponentteja skenaariossa kuvatulla tavalla.

    1. Valitse **Rivit**-pikaväliruudussa **SP-BOM1104**-nimikkeen rivi, ja valitse sitten **Poista rivi** -toiminto.  

4. Hyväksy uusi tuotannon tuoterakenne.  

    1. Valitse **Tila**-kentässä *Varmennettu*.  

5. Luo tuotannon tuoterakenneversio Airpot Litelle.

    1. Valitse **Versiot**-toiminto.

    2. Valitse **Tuot. tuoterak. versioluet.** -sivulla **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä  |Arvo  |
        |---------|---------|
        |**Versiokoodi** |02|
        |**Kuvaus** |Airpot Lite, v2|
        |**Mittayksikön koodi**|KPL  |  
        |**Aloituspvm**|Heinäkuu 01  |  

6. Kopioi komponenttirivit tuotannon tuoterakenteesta uuteen tuoterakenneversioon.

    1. Valitse **Kopioi tuoterakenne** -toiminto ja kopioi sitten komponentit alkuperäisestä tuotannon tuoterakenteesta valitsemalla **Kyllä**-painike.

7. Poista nimike **SP-BOM1106, on/off-valo** versiokomponenteista.

8. Hyväksy uusi tuoterakenneversio.

    1. Valitse **Tila**-kentässä *Varmennettu*.  

    2. Sulje tuoterakenteen versio

Uusi kahvinkeitin on nyt määritetty tuotannon tuoterakenteena, jolla on yksi versio.  

## Katso myös

[Johdatus Contoson kahvidemotietoihin](contoso-coffee-intro.md)  
