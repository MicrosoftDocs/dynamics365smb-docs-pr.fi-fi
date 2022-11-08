---
title: Tehtävien suorittaminen taustalla ja toistuvasti
description: Määritä tietojen synkronointi Business Centralin ja Shopifyn välillä taustalla.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 4a67f6fc58fb8b158563ce58baab55e7fda2ccb1
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728597"
---
# <a name="run-tasks-in-the-background"></a>Tehtävien suorittaminen taustalla

On tehokasta suorittaa joitakin tehtäviä samanaikaisesti ja automatisoidusti. Voit suorittaa tällaisia tehtäviä taustalla ja määrittää aikataulun myös silloin, kun haluat, että kyseiset tehtävät suoritetaan automaattisesti. Voit suorittaa tehtäviä taustalla kahdessa tilassa:

- Manuaalisesti käynnistyvät tehtävät ajoitetaan heti **Työjonon tapahtumien** avulla.
- Toistuvat tehtävät ajoitetaan **Työjonotapahtumiin**.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Tehtävien suorittaminen taustalla tietyn myymälän osalta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, kirjoita **Shopify-myymälän** nimi ja valitse myymälän nimi luettelosta.
2. Valitse kauppa, jolle haluat synkronoida nimikkeet avataksesi **Shopify-ostoskortti**-sivun.
3. Ota käyttöön **Salli taustasynkronointi** -vaihtonäppäin.

Nyt kun synkronointitoiminto käynnistetään, se pyytää sinua odottamaan edustalla suoritettavan tehtävän sijaan. Kun se on valmis, voit siirtyä seuraavaan toimintoon. Tehtävä luodaan **Työjonotapahtumana**, ja se alkaa heti estämättömällä tavalla.

## <a name="to-schedule-recurring-tasks"></a>Toistuvien tehtävien ajoittaminen

Voit ajoittaa seuraavat toistuvat aktiviteetit suoritettavaksi automaattisesti. Lue lisätietoja tehtävien ajoittamisesta kohdasta [Työjonot](../admin-job-queues-schedule-tasks.md).

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

> [!NOTE]
> Useat tehtävät voivat päivittää joitakin elementtejä, esimerkiksi silloin, kun tuot tilauksia **Shopify-ostoskortin** asetuksen mukaan, järjestelmä voi myös tuoda ja päivittää asiakkaan ja/tai tuotteen tietoja. Muista käyttää samaa työjonon luokkaa ristiriitojen välttämiseksi.

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
