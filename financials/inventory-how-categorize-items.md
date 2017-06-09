---
title: 'Toimintaohje: Nimikkeiden luokitteleminen| Microsoft Docs'
description: "Artikkelissa käsitellään, miten nimikkeet järjestetään luokkiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 06f50a356ddc3a501c28fe34891213b55a12e3fd
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-categorize-items"></a>Toimintaohje: Nimikkeiden luokitteleminen
Nimikkeet kannattaa järjestää nimikeluokkiin. Niiden avulla voi järjestellä nimikkeitä ja helpottaa nimikkeiden lajittelemista ja etsimistä.

Voit etsiä nimikkeitä ominaisuuksien mukaan, kun määrität nimikkeille ja nimikeluokille nimikkeen määritteet. Lisätietoja on kohdassa [Toimintaohje: Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Nimikeluokan luominen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikekategoriat** ja valitse sitten liittyvä linkki.
2. Valitse **Nimikeluokat**-ikkunassa **Uusi**-toiminto.
3. Täytä tarvittaessa **Nimikeluokkakortti**-ikkunan **Yleinen**-pikavälilehden kentät: [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Määritä **Määritteet**-pikavälilehdessä kaikki nimikeluokan nimikkeen määritteet. Lisätietoja on "Nimikkeen määritteiden määrittäminen nimikeluokkaan" -osassa kohdassa [Toimintaohje: Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md).

**Huomautus**: Jos nimikeluokalla on päänimikeluokka **Pääluokka**-kentässä määritetty, kaikki tähän päänimikeluokkaan määritetyt nimikkeen määritteet täytetään **Määritteet**-pikavälilehteen.

**Huomautus**: Nimikeluokkaan määritetyt nimikkeen määritteet kohdistetaan automaattisesti nimikkeeseen, johon nimikeluokka on määritetty.

## <a name="to-assign-an-item-category-to-an-item"></a>Nimikeluokan määrittäminen nimikkeeseen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jonka haluat määrittää nimikeluokkaan.
3. Valitse **Nimikeluokan koodi** -kentän valintapainike ja valitse sitten aiemmin määritetty nimikeluokka. Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikeluokan "Nimikeluokan luominen" -osassa esitetyllä tavalla.

## <a name="see-also"></a>Katso myös
[Toimintaohje: Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md)  
[Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

