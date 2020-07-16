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
ms.date: 06/22/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: c42f16f588b360b0e382ab2a3a91bd6974cc8a7e
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529186"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="a6003-103">Dynamics GP:n tietojen siirron laajennus</span><span class="sxs-lookup"><span data-stu-id="a6003-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="a6003-104">Laajennus poistetaan käytöstä 15.3-päivityksellä.</span><span class="sxs-lookup"><span data-stu-id="a6003-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="a6003-105">Microsoft suosittelee, että käyttäjät, jotka haluavat siirtyä Dynamics GP:hen, alkavat sen sijaan käyttää ohjattua **Pilvitoimintojen siirtämistä**.</span><span class="sxs-lookup"><span data-stu-id="a6003-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="a6003-106">**Pilvitoimintojen siirtäminen** -laajennuksessa on entistä vankempi toiminnallisuus, ja se tuo lisää tietoja Business Centralin Dynamics GP -toiminnosta.</span><span class="sxs-lookup"><span data-stu-id="a6003-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="a6003-107">Lisätietoja on kohdassa [Siirtyminen Business Central Onlineen Dynamics GP:stä](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) [!INCLUDE[prodshort](includes/prodshort.md)]in -hallintasisällössä.</span><span class="sxs-lookup"><span data-stu-id="a6003-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="a6003-108">Katso myös</span><span class="sxs-lookup"><span data-stu-id="a6003-108">See Also</span></span>

[<span data-ttu-id="a6003-109">Pilvisiirron älykkäät pilvilaajennukset</span><span class="sxs-lookup"><span data-stu-id="a6003-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="a6003-110">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="a6003-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="a6003-111">[[!INCLUDE[prodshort](includes/prodshort.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="a6003-111">[Customizing [!INCLUDE[prodshort](includes/prodshort.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="a6003-112">Siirtyminen Business Centralin Onlineen Dynamics GP:stä</span><span class="sxs-lookup"><span data-stu-id="a6003-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  
