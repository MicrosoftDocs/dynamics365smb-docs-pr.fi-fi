---
title: "Nimikkeiden järjestäminen luokkiin| Microsoft Docs"
description: "Nimikkeiden hakemista ja löytämistä helpottaa, kun nimikkeille määritetään määritteitä ja nimikkeet järjestetään luokkiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5b684df40599a730054e333f1bdf2e526c840e0b
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="categorize-items"></a>Nimikkeiden luokitteleminen
Nimikkeet kannattaa järjestää nimikeluokkiin. Niiden avulla voi järjestellä nimikkeitä ja helpottaa nimikkeiden lajittelemista ja etsimistä.

Voit etsiä nimikkeitä ominaisuuksien mukaan, kun määrität nimikkeille ja nimikeluokille nimikkeen määritteet. Lisätietoja on kohdassa [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Nimikeluokan luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikeluokat** ja valitse sitten liittyvä linkki.
2. Valitse **Nimikekategoriat**-sivulla **Uusi**-toiminto.
3. Täytä tarvittaessa **Nimikeluokan kortti** -sivun **Yleinen**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Määritä **Määritteet**-pikavälilehdessä kaikki nimikeluokan nimikkeen määritteet. Lisätietoja on kohdan [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md) osassa Nimikkeen määritteiden määrittäminen nimikeluokkaan.

> [!NOTE]  
>   Jos nimikeluokalla on Pääluokka-kentässä ilmaistu **Päänimike**-luokka, kaikki tähän päänimikeluokkaan määritetyt nimikkeen määritteet täytetään **Määritteet**-pikavälilehteen.

> [!NOTE]  
>   Nimikeluokkaan määritettyjä nimikkeen määritteitä käytetään automaattisesti nimikkeessä, johon nimikeluokka on määritetty.

## <a name="to-assign-an-item-category-to-an-item"></a>Nimikeluokan määrittäminen nimikkeeseen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jonka haluat määrittää nimikeluokkaan.
3. Valitse **Nimikeluokan koodi** -kentän valintapainike ja valitse sitten aiemmin määritetty nimikeluokka. Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikeluokan "Nimikeluokan luominen" -osassa esitetyllä tavalla.

## <a name="see-also"></a>Katso myös
[Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md)  
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

