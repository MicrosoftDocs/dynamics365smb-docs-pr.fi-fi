---
title: Nimikkeiden järjestäminen luokkiin (sisältää videon) | Microsoft Docs
description: Nimikkeiden hakemista ja löytämistä helpottaa, kun nimikkeille määritetään määritteitä ja nimikkeet järjestetään luokkiin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.search.form: 5730, 5733, 5401
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3b3c3add698255293d4dbf6f5f7d9eb927b1c0c0
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059828"
---
# <a name="categorize-items"></a>Nimikkeiden luokitteleminen

Nimikkeet kannattaa järjestää nimikeluokkiin. Niiden avulla voi järjestellä nimikkeitä ja helpottaa nimikkeiden lajittelemista ja etsimistä.

Voit etsiä nimikkeitä ominaisuuksien mukaan, kun määrität nimikkeille ja nimikeluokille nimikkeen määritteet. Lisätietoja on kohdassa [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>Nimikeluokan luominen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikeluokat** ja valitse sitten vastaava linkki.
2. Valitse **Nimikekategoriat**-sivulla **Uusi**-toiminto.
3. Täytä tarvittaessa **Nimikeluokan kortti** -sivun **Yleinen**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Määritä **Määritteet**-pikavälilehdessä kaikki nimikeluokan nimikkeen määritteet. Lisätietoja on kohdassa [Nimikkeen määritteiden määrittäminen nimikkeen luokkiin](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Jos nimikeluokalla on Pääluokka-kentässä ilmaistu **Päänimike**-luokka, kaikki tähän päänimikeluokkaan määritetyt nimikkeen määritteet täytetään **Määritteet**-pikavälilehteen.

> [!NOTE]  
> Nimikeluokkaan määritettyjä nimikkeen määritteitä käytetään automaattisesti nimikkeessä, johon nimikeluokka on määritetty.

Jos muutat mieltäsi nimikeluokasta, voit poistaa sen. Jos se kuitenkin on jo määritetty jollekin nimikkeelle, kyseinen tehtävä on poistettava, ennen kuin nimikeluokka voidaan poistaa.

## <a name="to-assign-an-item-category-to-an-item"></a>Nimikeluokan määrittäminen nimikkeeseen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Avaa sen nimikkeen kortti, jonka haluat määrittää nimikeluokkaan.
3. Valitse **Nimikeluokan koodi** -kentän valintapainike ja valitse sitten aiemmin määritetty nimikeluokka. Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikeluokan kohdassa [Nimikeluokan luominen](inventory-how-categorize-items.md#to-create-an-item-category) esitetyllä tavalla.

## <a name="categories-attributes-and-variants"></a>Luokat, määritteet ja variantit

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Katso myös

[Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md)  
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]