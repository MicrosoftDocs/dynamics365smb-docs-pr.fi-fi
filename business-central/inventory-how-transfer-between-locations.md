---
title: Nimikkeiden siirtäminen varastosijaintien välillä
description: Tietoja varastonimikkeiden siirtämisestä varastosta toiseen joko uudelleenluokituspäiväkirjan tai siirtotilausten avulla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# Varastonimikkeiden siirtäminen sijaintien välillä

Varastonimikkeitä siirretään sijaintien välillä luomalla siirtotilauksia. Vaihtoehtoisesti voit käyttää uudelleenluokituspäiväkirjaa.

> [!NOTE]
> Nimikkeiden siirtäminen edellyttää sijaintien siirtoreittien määrittämistä. Lisätietoja sijaintien määrittämisestä on kohdassa [Sijaintien määrittäminen](inventory-how-setup-locations.md). Siirtotilauksia ei voi käyttää *tyhjissä* sijainneissa.

## Siirtotilaukset

Lähtevä siirto voidaan lähettää yhdestä sijainnista ja vastaanottaa kohteessa saapuvana siirtona. Voit:

* Kuljetuksessa olevan määrän seuraaminen
* Päivämäärän laskentaa ja suunnittelua varten määritetään kalenterit, reitit sekä saapuvien ja lähtevien käsittelyajat. Lisätietoja suunnittelusta on kohdassa [Tietoja suunnittelutoiminnosta](production-about-planning-functionality.md).
* Saapuvissa ja lähtevissä sijainneissa käytetään erilaisia varastointiominaisuuksia:
* Joitakin rajoituksia lukuun ottamatta siirtotilauksia voidaan käyttää suorissa siirroissa.

## Nimikkeen uudelleenluokituspäiväkirjat

* Yksinkertainen nimikkeiden suora siirto sijaintien välillä
* Nimikkeiden siirtäminen varastopaikkojen välillä. Lisätietoja nimikkeiden siirtämisestä varastopaikkojen välillä on kohdassa [Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Erä- tai sarjanumeron vaihtaminen uuteen erä- tai sarjanumeroon. Lisätietoja sarja- ja eränumeroiden uudelleenluokittelusta on kohdassa [Sarja- ja eränumeroiden uudelleenluokittelu](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Vanhentumispäivän vaihtaminen uudeksi päivämääräksi.
* Nimikkeiden uudelleenluokitteleminen *tyhjästä* sijainnista varsinaiseen sijaintiin.
* Fyysisen varaston aktiviteetteja ei hallita. Fyysisen varastoinnin tapahtumat luodaan.

## Nimikkeiden siirtäminen siirtotilauksella

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirtotilaukset** ja valitse sitten vastaava linkki.
2. Täytä **Siirtotilaus**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Jos **Siirtoreitin määritykset** -sivun **Kuljetuksessa-koodi**-, **Kuljetusliikkeen koodi**- ja **Kuljetusliikkeen palvelu** -kentät on täytetty siirtoreitin määrityksen yhteydessä, vastaavat kentät täytetään automaattisesti siirtotilauksessa.

    Kun **Kuljetusliikkeen palvelu** -kenttä täytetään, kohteeseen-sijainnin vastaanottopäivämäärä lasketaan lisäämällä kuljetusliikkeen palvelun toimitusajan Kohteesta-pikavälilehden lähetyksen päivämäärään.

3. Täytä rivit joka antamalla ne manuaalisesti tai valitsemalla jonkin seuraavista vaihtoehdoista **Funktiot**-toiminnossa:

    * Valitse **Hae var.paikan sisältö** -toiminnolla aiemmin luotuja nimikkeita tietystä sijainnin varastopaikasta.
    * Valitse **Hae vastaanottorivit** -toiminnolla nimikkeet, jotka ovat juuri saapuneet kohteesta-sijainnista.

    Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden toimittamiseen.
4. Valita ensin **Kirjaa**-toiminto, sitten **Toimitus**-asetus ja lopuksi **OK**-painike.

    Nimikkeet ovat nyt matkalla valittujen sijaintien välillä valitun siirtoreitin mukaisesti.

    Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden vastaanottamiseen. Siirtotilausrivit ovat samat kuin toimituksen aikana eikä niitä voi muokata.
5. Valita ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-asetus ja lopuksi **OK**-painike.

## Siirrä nimikkeet nimikkeiden uudelleenluokituspäiväkirjan avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen uudell.luokit. pvk:t** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät **Nimik. uud.luok.pvk** -sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Anna **Sijaintikoodi**-kentässä sijainti, jossa nimikkeet ovat varastoituna.

    > [!NOTE]  
    > Jos siirrettävillä nimikkeillä ei ole sijainkoodia, jätä **Sijaintikoodi**-kenttä tyhjäksi.
4. Anna **Uusi sijaintikoodi** -kenttään sijainti, johon haluat siirtää nimikkeet.
5. Valitse **Kirjaa**-toiminto.

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/transfer-items/)

## Katso myös

[Varaston hallinta](inventory-manage-inventory.md)  
[Sijaintien määrittäminen](inventory-how-setup-locations.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
