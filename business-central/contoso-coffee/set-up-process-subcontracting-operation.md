---
title: Alihankintatoiminnon määrittäminen ja käsitteleminen
description: 'Opastus, jossa kerrotaan, miten alihankintaoperaatio määritetään ja käsitellään Business Centralissa.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Alihankintatoiminnon määrittäminen ja käsitteleminen

Tässä artikkelissa on tietoja Contoso Coffee -esittelyn tietojen käytöstä alihankinnassa.

## Esimerkkitilanne

Olet Contoso Coffeen tuotantosuunnittelija. Kapasiteettirajoitusten vuoksi aiot käyttää alihankkijaa tuottaaksesi nimikkeen **SP-SCM1009, Airpot**.

Tässä voit luoda uuden vapautetun tuotantotilauksen nimikkeen SP-SCM1009, Airpot 12 yksikölle käyttämällä reititystä - SP-SCM1009-SUB-2. Käytä alihankintatyökirjaa tuotannon ostotilauksen luomiseen ja viimeistele operaatio sitten vastaanottamalla ja laskuttamalla ostotilaus.

## Vaiheet

1. Luo uusi vapautettu tuotantotilaus SP-SCM1009, Airpot -nimikkeen 12 yksikölle.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vapautettu tuotantotilaus** ja valitse sitten vastaava linkki.  

    2. Valitse **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä  |Arvo  |
        |---------|---------|
        |**Lähdetyyppi** |Nimike|
        |**Lähteen nro** |SP-SCM1009|
        |**määrä** |100|
    3. Valitse **Päivitä tuotantotilaus** -toiminto.  

2. Korvaa reititys SP-SCM1009-SUB-2:een tuotantotilausrivillä ja sitten päivitä tuotantotilaus, mutta vain reititystä varten.  

    1. Lisää Tuotannon reititysnro -kenttä vapautetun tuotantotilauksen riveille.<!--in code, this is marked as visible=false-->

    2. Muuta **Reititysnro**-kenttä arvosta *SP-SCM1009-SERIAL* arvoon *SP-SCM1009-SUB-2*.  

    3. Valitse **Päivitä tuotantotilaus** -toiminto.  

    4. Poista **Päivitä tuotantotilaus** -pyyntösivulla **Rivit**- ja **Komponenttitarve**-kentät niin, että tehtävä suoritetaan vain reititystä varten, ja valitse **OK**-painike.

3. Luo alihankintatyökirjan avulla ostotilaus alihankintaoperaatiolle vaiheessa 2 luodusta tuotantotilauksesta.  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **alihankintatyökirjat** ja valitse sitten vastaava linkki.  

    2. Valitse **Laske alihankinnat** -toiminto.

    3. Valitse **Hyväksy toimenpideviesti** -kenttä uudelle riville.

    4. Valitse **Toteuta toimenpideviesti** -toiminto.  

    5. Hyväksi **Toteuta toim.pideviesti - hank** -pyyntösivulla kaikki oletusarvot ja valitse sitten **OK**-painike.

    6. Kun eräajo päättyy, sulje alihankintatyökirja valitsemalla **OK**.  

4. Vastaanota ja laskuta ostotilaus.  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ostotilaukset** ja valitse sitten vastaava linkki.  

    2. Etsi **Ostotilaukset**-luettelosta ostotilaus toimittajan 82000 alihankkijalta.

    3. Syötä **Toimittajan laskunro** -kenttään *542349*.

    4. Valitse **Rivit**-pikavälilehdessä rivi ja määritä **Välitön kustannus** -kentän arvoksi *18*.

    5. Valitse **Kirjaa**-toiminto.  

    6. Valitse pyyntöviestissä **Vastaanota ja laskuta** -vaihtoehto.  

Nimikkeen SP-SCM1009 Airpot tuotos on nyt rekisteröity.

## Katso myös

[Johdatus Contoson kahvidemotietoihin](contoso-coffee-intro.md)  
