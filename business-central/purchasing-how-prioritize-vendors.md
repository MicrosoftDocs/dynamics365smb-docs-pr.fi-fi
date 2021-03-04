---
title: Prioriteettitason määrittäminen toimittajalle | Microsoft Docs
description: Voit määrittää toimittajille numeron, joka priorisoi ne ja helpottaa maksuehdotuksia Business Central -sovelluksessa.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87d2f7c7fe2d395d16b41b288500f22e16bd0ba0
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758540"
---
# <a name="prioritize-vendors"></a>Toimittajien priorisointi
[!INCLUDE[prod_short](includes/prod_short.md)] voi ehdottaa eri maksuja toimittajille, esimerkiksi maksuja, jotka erääntyvät pian, ja maksuja, joista voi saada alennuksen. Lisätietoja on kohdassa [Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md).

Ensin priorisoidaan toimittajat liittämällä heille numerot.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Toimittajien priorisointi
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten liittyvä linkki.
2. Valitse asianmukainen toimittaja ja valitse sitten **Muokkaa**.
3. Syötä **Prioriteetti**-kenttään numero.

[!INCLUDE[prod_short](includes/prod_short.md)]in mukaan pienin numero (paitsi 0) tarkoittaa korkeinta prioriteettia. Siten jos käytät esimerkiksi numeroita 1, 2 ja 3, numerolla 1 on korkein prioriteetti.

Jos et halua priorisoida toimittajaa, jätä **Prioriteetti**-kenttä tyhjäksi. Tämän jälkeen kun käytät maksuehdotusominaisuutta, tämä toimittaja tulee luetteloon kaikkien niiden toimittajien jälkeen, joilla on prioriteettinumero. Prioriteettitasoja voi syöttää kuinka monta tahansa.

## <a name="see-also"></a>Katso myös
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]