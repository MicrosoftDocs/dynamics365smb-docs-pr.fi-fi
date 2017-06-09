---
title: "Lisäasetukset: Varaston täsmäytys| Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten varastoarvo täsmäytetään pääkirjanpidon kanssa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: post inventory cost to G/L, reconcile inventory
ms.date: 02/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7eb07530fe80f871ef113c95e48bf89da6c29db0
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
## <a name="advanced-inventory-reconciliation"></a>Lisäasetukset: Varaston täsmäytys
Kun kirjaat varastotapahtumia, kuten myyntitoimituksia, ostolaskuja tai varaston muutoksia, ohjelma kirjaa muuttuneet nimikekustannukset niiden arvotapahtumiin. Jotta varastoarvon muutos päivittyisi talouskirjoihin, varastokustannukset kirjataan automaattisesti pääkirjanpidon liittyviin varastotileihin. Ohjelma kirjaa jokaista itse kirjaamaasi varastotapahtumaa kohti sopivan arvon varastotilille, muutostilille ja myytyjen tuotteiden kustannusten tilille pääkirjanpidossa.

Vaikka kustannukset kirjattaisiin automaattisesti pääkirjanpitoon, on tarpeen varmistaa, että tavaroiden kustannukset välitetään oikealle lähtevälle transaktioille. Tämä on erityisen tärkeää, kun myyt tavaroita ennen näiden tavaroiden oston laskutusta. Tätä kutsutaan kustannusmuutokseksi. Nimikekustannukset muutetaan automaattisesti, kun kirjaat nimiketapahtumia, mutta voit muuttaa niitä myös manuaalisesti. Lisätietoja on kohdassa [Toimintaohje: Nimikekustannuksien muuttaminen](inventory-how-adjust-item-costs.md).

## <a name="see-also"></a>Katso myös
[Varasto](inventory-manage-inventory.md)  
[Lisäasetukset: Parhaan hinnan laskenta](advanced-best-price-calculation.md)

