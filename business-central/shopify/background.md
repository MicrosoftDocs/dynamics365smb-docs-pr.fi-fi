---
title: Tehtävien suorittaminen taustalla
description: Määritä tietojen synkronointi Business Centralin ja Shopifyn välillä taustalla.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: f353edb4c505fd7b3eb498392abca3ce481b6009
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768118"
---
# <a name="run-tasks-in-the-background"></a>Tehtävien suorittaminen taustalla

On tehokasta suorittaa joitakin tehtäviä samanaikaisesti ja automatisoidusti. Voit suorittaa tällaisia tehtäviä taustalla ja määrittää aikataulun myös silloin, kun haluat, että kyseiset tehtävät suoritetaan automaattisesti. Voit suorittaa tehtäviä taustalla kahdessa tilassa:

- Manuaalisesti käynnistyvät tehtävät ajoitetaan heti **Työjonon tapahtumien** avulla
- Toistuvat tehtävät ajoitetaan **Työjonotapahtumiin**

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Tehtävien suorittaminen taustalla tietyn myymälän osalta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, kirjoita **Shopify-myymälän** nimi ja valitse myymälän nimi luettelosta.
2. Valitse kauppa, jolle haluat synkronoida nimikkeet avataksesi **Shopify-ostoskortti**-sivun.
3. Ota käyttöön **Salli taustasynkronointi** -vaihtonäppäin.

Nyt kun synkronointitoiminto käynnistetään, se pyytää sinua odottamaan edustalla suoritettavan tehtävän sijaan. Kun se on valmis, voit siirtyä seuraavaan toimintoon. Tehtävä luodaan **Työjonotapahtumana**, ja se alkaa heti estämättömällä tavalla.

## <a name="to-schedule-recurring-tasks"></a>Toistuvien tehtävien ajoittaminen

Voit ajoittaa seuraavat toistuvat aktiviteetit suoritettavaksi automaattisesti. Lisätietoja tehtävien aikatauluttamisesta on kohdassa [Työjono](../admin-job-queues-schedule-tasks.md).

|Tehtävä|Objekti|
|------|------------|
|**Synkronoi tilaukset Shopifysta**|Raportti 30104 Shopifysta synkronoidut tilaukset|
|**Käsitellään Shopify-tilauksia**|Raportti 30103 Shopifylla luodut myyntitilaukset|
|**Synkronoi toimitukset Shopifyhin**|Raportti 30109 Shopifyhin synkronoidut toimitukset|
|**Synkronoi tuotteet ja/tai hinnat**|Raportti 30108 Shopifyn synkronoidut tuotteet|
|**Synkronoi varasto**|Raportti 30102 Shopifyhin synkronoidut varastot|
|**Synkronoi kuvat**|Raportti 30107 Shopifyn synkronoidut kuvat|
|**Synkronoi asiakkaat**|Raportti 30100 Shopifyn synkronoidut asiakkaat|
|**Synkronoi maksut**|Raportti 30105 Shopifyn synkronoidut maksut|

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
