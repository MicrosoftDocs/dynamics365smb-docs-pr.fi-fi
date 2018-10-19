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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c62d26dc9dc444359c0d8b5a9354b29132857de1
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="categorize-items"></a>Nimikkeiden luokitteleminen
Nimikkeet kannattaa järjestää nimikeluokkiin. Niiden avulla voi järjestellä nimikkeitä ja helpottaa nimikkeiden lajittelemista ja etsimistä.

Voit etsiä nimikkeitä ominaisuuksien mukaan, kun määrität nimikkeille ja nimikeluokille nimikkeen määritteet. Lisätietoja on kohdassa [Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Nimikeluokan luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikeluokat** ja valitse sitten liittyvä linkki.
2. Valitse **Nimikeluokat**-ikkunassa **Uusi**-toiminto.
3. Täytä tarvittaessa **Nimikeluokkakortti**-ikkunan **Yleinen**-pikavälilehden kentät: [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
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

