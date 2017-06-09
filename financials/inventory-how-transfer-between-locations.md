---
title: "Toimintaohje: Varastonimikkeiden siirtäminen sijaintien välillä| Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten varastonimikkeitä siirretään varastosta toiseen joko uudelleenluokituspäiväkirjan tai siirtotilausten avulla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 03/28/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 43a60a6eb646de13ca9bf1458061f0bbefbeab12
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-transfer-inventory-between-locations"></a>Toimintaohje: Varastonimikkeiden siirtäminen sijaintien välillä
Varastonimikkeitä siirretään sijaintien välillä luomalla siirtotilauksia. Vaihtoehtoisesti voit käyttää uudelleenluokituspäiväkirjaa.

Siirtotilauksissa lähtevä siirto toimitetaan yhdestä sijainnista vastaanotettavaksi toisessa sijainnissa. Tämä mahdollistaa liittyvien varastointiaktiviteettien hallinnan ja tarjoaa suuremman varmuuden siitä, että varastosaldot päivitetään oikein.

Uudelleenluokituspäiväkirjaan voit yksinkertaisesti täyttää **Sijaintikoodi**- ja **Uusi sijaintikoodi** -kentät. Kun teet kirjauksen päiväkirjaan, nimiketapahtumat oikaistaan kyseisissä sijainneissa. Varastotoimintoja ei hallita tällä menetelmällä.

**Huomautus**: Jos varastoon on kirjattu nimikkeitä ilman sijaintikoodia esimerkiksi silloin, kun käytössä oli vain yksi varasto, et voi siirtää kyseisiä nimikkeitä siirtotilauksilla. Sen sijaan sinun on käytettävä uudelleenluokittelupäiväkirjaa ja luokiteltava nimikkeet uudelleen tyhjästä sijaintikoodista todelliseen sijaintikoodiin.  Lisätietoja on Nimikkeiden siirtäminen uudelleenluokituspäiväkirjan avulla -kohdan vaiheessa 3.

Sijainnit ja siirtoreitit on määritettävä, jotta nimikkeitä voi siirtää. Lisätietoja on kohdassa [Toimintaohje: Sijaintien määrittäminen](inventory-how-setup-locations.md).

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Nimikkeiden siirtäminen siirtotilauksella
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Siirtotilaukset** ja valitse sitten liittyvä linkki.
2. Täytä **Siirtotilaus**-ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    **Huomautus:** Jos täytit **Siirtoreitin määritykset** -ikkunassa **Kuljetuksessa-koodi**-, **Kuljetusliikkeen koodi**- ja **Kuljetusliikkeen palvelu** -kentät, kun olet määritit siirtoreitin, vastaavat kentät täytetään automaattisesti siirtotilaukseen.

    Kun **Kuljetusliikkeen palvelu** -kenttä täytetään, kohteeseen-sijainnin vastaanottopäivämäärä lasketaan lisäämällä kuljetusliikkeen palvelun toimitusajan Kohteesta-pikavälilehden lähetyksen päivämäärään.

    Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden toimittamiseen.
3. Valita ensin **Kirjaa**-toiminto, sitten **Toimitus**-asetus ja lopuksi **OK**-painike.

    Nimikkeet ovat nyt matkalla valittujen sijaintien välillä valitun siirtoreitin mukaisesti.

    Kohteesta-sijainnin varastotyöntekijänä voit siirtyä nimikkeiden vastaanottamiseen.
4. Valita ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-asetus ja lopuksi **OK**-painike.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Siirrä nimikkeet nimikkeiden uudelleenluokituspäiväkirjan avulla
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeen uudell.luokit. pvk:t** ja valitse sitten liittyvä linkki.
2. Täytä **Nimik. uud.luok.pvk** -ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Anna **Sijaintikoodi**-kentässä sijainti, jossa nimikkeet ovat varastoituna.

    **Huomautus**: Jos siirrettävillä nimikkeillä ei ole sijainkoodia, jätä **Sijaintikoodi**-kenttä tyhjäksi.
4. Anna **Uusi sijaintikoodi** -kenttään sijainti, johon haluat siirtää nimikkeet.
5. Valitse **Kirjaa**-toiminto.

## <a name="see-also"></a>Katso myös
[Varaston hallinta](inventory-manage-inventory.md)  
[Toimintaohje: Sijaintien määrittäminen](inventory-how-setup-locations.md)  
[Toimitusketju](madeira-supply-chain.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
[Oman [!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
