---
title: "Prioriteettitason määrittäminen toimittajalle | Microsoft Docs"
description: "Voit määrittää toimittajille numeron, joka priorisoi ne ja helpottaa maksuehdotuksia Business Central -sovelluksessa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: cb3556c9bd8fb893448d61c4e8f18131b96a9841
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="prioritize-vendors"></a>Toimittajien priorisointi
[!INCLUDE[d365fin](includes/d365fin_md.md)] voi ehdottaa eri maksuja toimittajille, esimerkiksi maksuja, jotka erääntyvät pian, ja maksuja, joista voi saada alennuksen. Lisätietoja on kohdassa [Toimittajamaksujen ehdottaminen](payables-how-suggest-vendor-payments.md).

Ensin priorisoidaan toimittajat liittämällä heille numerot.

## <a name="to-prioritize-vendors"></a>Toimittajien priorisointi
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten liittyvä linkki.
2. Valitse asianmukainen toimittaja ja valitse sitten **Muokkaa**.
3. Syötä **Prioriteetti**-kenttään numero.

[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukaan pienin numero (paitsi 0) tarkoittaa korkeinta prioriteettia. Siten jos käytät esimerkiksi numeroita 1, 2 ja 3, numerolla 1 on korkein prioriteetti.

Jos et halua priorisoida toimittajaa, jätä **Prioriteetti**-kenttä tyhjäksi. Tämän jälkeen kun käytät maksuehdotusominaisuutta, tämä toimittaja tulee luetteloon kaikkien niiden toimittajien jälkeen, joilla on prioriteettinumero. Prioriteettitasoja voi syöttää kuinka monta tahansa.

## <a name="see-also"></a>Katso myös
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

