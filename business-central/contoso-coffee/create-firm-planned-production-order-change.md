---
title: Luo sitovasti suunniteltu tuotantotilaus muuta sitä
description: 'Vaihekuvaus Contoso Coffeen tuotantosuunnittelijalle, joka haluaa luoda sitovasti suunnitellun tuotantotilauksen ja muokata sitä.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Vaihekuvaus: Luo sitovasti suunniteltu tuotantotilaus muuta sitä

Tässä artikkelissa on tietoja Contoso Coffee -esittelyn tietojen käytöstä tuotantotilausten suhteen.  

## Esimerkkitilanne

Contoso Coffeen tuotantosuunnittelijan Eduardon on luotava uusi tuotantotilaus 10 yksikölle nimikkeelle **SP-SCM1009, Airpot**, jonka täytyy olla valmis 28. huhtikuuta. Hän taaksepäin aikatauluttaa tämän ja vahvistaa, että hän voi aloittaa tilauksen 27. huhtikuuta.  

Pian tämän tehtävän päätyttyä häntä pyydetään kasvattamaan tilausta 50 yksikköön. Kun tämä suoritetaan, taaksepäin aikataulutustoiminto siirtää tilauksen aloituspäivämäärän liian aikaiseen. Joten hän eteenpäin aikatauluttaa tilauksen 23. huhtikuuta eteenpäin määrittääkseen realistisemman päättymispäivämäärän.  

## Vaiheet

1. Luo alkuperäinen tuotantotilaus **SP-SCM1009, Airpot** -nimikkeen 10 yksikölle.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sitovasti suunn. tuotantotil.** ja valitse sitten vastaava linkki.  

    2. Valitse **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä  |Arvo  |
        |---------|---------|
        |**Lähdetyyppi** |Nimike|
        |**Lähteen nro** |SP-SCM1009|
        |**määrä** |10|
        |**Määräpäivä**|Huhtikuu 28  |

    3. Valitse **Päivitä tuotantotilaus** -toiminto.  

    4. Hyväksy **Päivitä tuotantotilaus** -sivulla kaikki oletukset ja aloita prosessi valitsemalla **OK**.  

        Nykyisissä asetuksissa tämä prosessi käyttää taaksepäin aikataulutusta. Tuotantotilauksen uudella rivillä aloitus päivämäärä on 26. huhtikuuta.  

2. Muuta tuotantotilauksen määräksi 50 yksikköä ja ajoita tilaus.  

    1. Valitse **tuotannon tuoterakenteen** **Rivit**-pikavälilehdessä viimeksi lisätty rivi ja syötä **Määrä**-kenttään *50*.  

3. Valitse **Päivitä tuotantotilaus** -toiminto.  

    Aloituspäivämäärä on nyt siirretty 20. huhtikuuta asti. Tämä ei ole hyväksyttävä päivämäärä Eduardolle.

4. Käynnistä tuotantotilauksen eteenpäin aikataulutus.

    1. Määritä **Aikataulu**-pikavälilehdessä **Aloituspvm**-kentän arvoksi *23.4.*

    Tilauksen aloitus on nyt 25. huhtikuuta, ja lopetuspäivämäärä on 2. toukokuuta. Tilauksen eräpäiväksi asetetaan päivää myöhemmin, 3. toukokuuta. Eduardo tietää nyt, että kasvatetun tilauksen toimittaminen kestää 3. toukokuuta asti.

> [!NOTE]
> Tilauksen aikatauluttaminen muuttamalla sen alkamis- tai päättymispäivämäärää ei vaadi **Päivitä tuotanto tilaus** -eräajoa, koska kaikki päivämäärät lasketaan uudelleen automaattisesti.

Uusi tuotantotilaus on nyt määritetty, ja Eduardon vaatimukset täyttyvät.  

## Katso myös

[Johdatus Contoson kahvidemotietoihin](contoso-coffee-intro.md)  
