---
title: Tietojen siirto Dynamics GP:stä ennen päivitystä 15.3 | Microsoft Docs
description: Ennen päivitystä 15.3 asiakkaita, toimittajia, varastonimikkeitä, pääkirjanpidon tilejä sekä avoimia ostoreskontran ja myyntireskontran tapahtumia voitiin siirtää Dynamics GP:stä Business Centraliin Dynamics GP:n tietojen siirron laajennuksella.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: a8f6c35d031cdbe6376ed57ea9ba2e9ce79188b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757265"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="985d3-103">Dynamics GP:n tietojen siirron laajennus</span><span class="sxs-lookup"><span data-stu-id="985d3-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="985d3-104">Laajennus poistetaan käytöstä 15.3-päivityksellä.</span><span class="sxs-lookup"><span data-stu-id="985d3-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="985d3-105">Microsoft suosittelee, että käyttäjät, jotka haluavat siirtyä Dynamics GP:hen, alkavat sen sijaan käyttää ohjattua **Pilvitoimintojen siirtämistä**.</span><span class="sxs-lookup"><span data-stu-id="985d3-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="985d3-106">**Pilvitoimintojen siirtäminen** -laajennuksessa on entistä vankempi toiminnallisuus, ja se tuo lisää tietoja Business Centralin Dynamics GP -toiminnosta.</span><span class="sxs-lookup"><span data-stu-id="985d3-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="985d3-107">Lisätietoja on kohdassa [Siirtyminen Business Central Onlineen Dynamics GP:stä](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) [!INCLUDE[prod_short](includes/prod_short.md)]in -hallintasisällössä.</span><span class="sxs-lookup"><span data-stu-id="985d3-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="985d3-108">Katso myös</span><span class="sxs-lookup"><span data-stu-id="985d3-108">See Also</span></span>

[<span data-ttu-id="985d3-109">Pilvisiirron älykkäät pilvilaajennukset</span><span class="sxs-lookup"><span data-stu-id="985d3-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="985d3-110">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="985d3-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="985d3-111">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="985d3-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="985d3-112">Siirtyminen Business Centralin Onlineen Dynamics GP:stä</span><span class="sxs-lookup"><span data-stu-id="985d3-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  
