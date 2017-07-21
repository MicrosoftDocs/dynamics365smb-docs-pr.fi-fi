---
title: "Prioriteettitason määrittäminen toimittajalle | Microsoft Docs"
description: "Voit määrittää toimittajille numeron, joka priorisoi ne ja helpottaa maksuehdotuksia Financialsissa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2c91b28daf27ddd2b698ffe4338bbf92fd1f9adf
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-prioritize-vendors"></a>Toimittajien priorisointi
[!INCLUDE[d365fin](includes/d365fin_md.md)] voi ehdottaa eri maksuja toimittajille, esimerkiksi maksuja, jotka erääntyvät pian, ja maksuja, joista voi saada alennuksen. Lisätietoja on kohdassa [Toimintaohje: Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md).

Ensin priorisoidaan toimittajat liittämällä heille numerot.

## <a name="to-prioritize-vendors"></a>Toimittajien priorisointi
1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Toimittajat** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse asianmukainen toimittaja ja valitse sitten **Muokkaa**.
3. Syötä **Prioriteetti**-kenttään numero.

[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukaan pienin numero (paitsi 0) tarkoittaa korkeinta prioriteettia. Siten jos käytät esimerkiksi numeroita 1, 2 ja 3, numerolla 1 on korkein prioriteetti.

Jos et halua priorisoida toimittajaa, jätä **Prioriteetti**-kenttä tyhjäksi. Tämän jälkeen kun käytät maksuehdotusominaisuutta, tämä toimittaja tulee luetteloon kaikkien niiden toimittajien jälkeen, joilla on prioriteettinumero. Prioriteettitasoja voi syöttää kuinka monta tahansa.

## <a name="see-also"></a>Katso myös
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

