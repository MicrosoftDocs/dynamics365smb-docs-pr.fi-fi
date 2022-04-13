---
title: Nimikkeiden siirtäminen varastosijaintien välillä
description: Tässä ohjeaiheessa kerrotaan, miten varastonimikkeitä siirretään varastosta toiseen joko uudelleenluokituspäiväkirjan tai siirtotilausten avulla.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.search.forms: 5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 347550073fc4efad89c41f180c3a48747b91d7a7
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511621"
---
# <a name="transfer-inventory-between-locations"></a>Varastonimikkeiden siirtäminen sijaintien välillä
Varastonimikkeitä siirretään sijaintien välillä luomalla siirtotilauksia. Vaihtoehtoisesti voit käyttää uudelleenluokituspäiväkirjaa.

Siirtotilauksissa lähtevä siirto toimitetaan yhdestä sijainnista vastaanotettavaksi toisessa sijainnissa. Tämä mahdollistaa liittyvien varastointiaktiviteettien hallinnan ja tarjoaa suuremman varmuuden siitä, että varastosaldot päivitetään oikein.

Uudelleenluokituspäiväkirjaan voit yksinkertaisesti täyttää **Sijaintikoodi**- ja **Uusi sijaintikoodi** -kentät. Kun teet kirjauksen päiväkirjaan, nimiketapahtumat oikaistaan kyseisissä sijainneissa. Varastotoimintoja ei hallita tällä menetelmällä.

> [!NOTE]  
>   Jos varastoon on kirjattu nimikkeitä ilman sijaintikoodia esimerkiksi silloin, kun käytössä oli vain yksi varasto, et voi siirtää kyseisiä nimikkeitä siirtotilauksilla. Sen sijaan sinun on käytettävä uudelleenluokittelupäiväkirjaa ja luokiteltava nimikkeet uudelleen tyhjästä sijaintikoodista todelliseen sijaintikoodiin.  Lisätietoja on kohdan [Nimikkeiden siirtäminen uudelleenluokituspäiväkirjan avulla](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal) vaiheessa 3.

Sijainnit ja siirtoreitit on määritettävä, jotta nimikkeitä voi siirtää. Lisätietoja on kohdassa [Sijaintien määrittäminen](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Nimikkeiden siirtäminen siirtotilauksella
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirtotilaukset** ja valitse sitten vastaava linkki.
2. Täytä **Siirtotilaus**-sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Jos olet täyttänyt **Siirtoreitin määritykset** -sivun **Kuljetuksessa-koodi**-, **Kuljetusliikkeen koodi**- ja **Kuljetusliikkeen palvelu** -kentät siirtoreitin määrityksen yhteydessä, ohjelma täyttää siirtotilauksen vastaavat kentät automaattisesti.

    Kun **Kuljetusliikkeen palvelu** -kenttä täytetään, kohteeseen-sijainnin vastaanottopäivämäärä lasketaan lisäämällä kuljetusliikkeen palvelun toimitusajan Kohteesta-pikavälilehden lähetyksen päivämäärään.

3. Täytä rivit joka antamalla ne manuaalisesti tai valitsemalla jonkin seuraavista vaihtoehdoista **Funktiot**-toiminnossa:
    - Valitse **Hae var.paikan sisältö** -toiminnolla aiemmin luotuja nimikkeita tietystä sijainnin varastopaikasta.
    - Valitse **Hae vastaanottorivit** -toiminnolla nimikkeet, jotka ovat juuri saapuneet kohteesta-sijainnista.   

    Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden toimittamiseen.
4. Valita ensin **Kirjaa**-toiminto, sitten **Toimitus**-asetus ja lopuksi **OK**-painike.

    Nimikkeet ovat nyt matkalla valittujen sijaintien välillä valitun siirtoreitin mukaisesti.

    Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden vastaanottamiseen. Siirtotilausrivit ovat samat kuin toimituksen aikana eikä niitä voi muokata.
5. Valita ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-asetus ja lopuksi **OK**-painike.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Siirrä nimikkeet nimikkeiden uudelleenluokituspäiväkirjan avulla
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen uudell.luokit. pvk:t** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät **Nimik. uud.luok.pvk** -sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Anna **Sijaintikoodi**-kentässä sijainti, jossa nimikkeet ovat varastoituna.

    > [!NOTE]  
    >   Jos siirrettävillä nimikkeillä ei ole sijainkoodia, jätä **Sijaintikoodi**-kenttä tyhjäksi.
4. Anna **Uusi sijaintikoodi** -kenttään sijainti, johon haluat siirtää nimikkeet.
5. Valitse **Kirjaa**-toiminto.

## <a name="see-also"></a>Katso myös
[Varaston hallinta](inventory-manage-inventory.md)  
[Sijaintien määrittäminen](inventory-how-setup-locations.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]