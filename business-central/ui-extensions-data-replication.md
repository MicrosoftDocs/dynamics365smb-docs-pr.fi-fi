---
title: Business Central Älykäs pilvi -laajennukset pilvipohjaiseen siirtoon | Microsoft-dokumentit
description: Pilvipohjaisen siirron laajennusten avulla voit siirtää paikallisen datan Business Central -verkkopalveluun. Nämä laajennukset siirtävät sisäiset tiedot pilveen, jotta voit käyttää Business Centralin tietoja verkossa aiemmin luotujen tietojesi kanssa.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 07/13/2020
ms.author: jenolson
ms.openlocfilehash: 712950571d5b45680aae46bccfd8401b999993cd
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577259"
---
# <a name="intelligent-cloud-extensions-for-cloud-migration"></a><span data-ttu-id="04189-104">Pilvisiirron älykkäät pilvilaajennukset</span><span class="sxs-lookup"><span data-stu-id="04189-104">Intelligent Cloud Extensions for Cloud Migration</span></span>

<span data-ttu-id="04189-105">Paikallisen ratkaisun mukaan sinun on käytettävä eri laajennuksia, jotta voisit yhdistää tiedot [!INCLUDE[prodshort](includes/prodshort.md)] -verkkoon, jotta voisit siirtää ratkaisun pilveen.</span><span class="sxs-lookup"><span data-stu-id="04189-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prodshort](includes/prodshort.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="04189-106">Jos käytät jotakin tuettua paikallista tuotetta, voit määrittää pilviympäristön tuotekohtaisen laajennuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="04189-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span><span data-ttu-id="04189-107"> Kun pilviympäristö on määritetty, voit siirtää paikallisen ratkaisun tiedot [!INCLUDE[prodshort](includes/prodshort.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="04189-107"> Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="04189-108">Tämän jälkeen voit käyttää pilveä ja hyödyntää sitä liiketoiminnassa. Saat entistä enemmän tietoja liiketoiminnasta sekä voit käyttää tekoälyä ja useita laitteita milloin tahansa ja missä tahansa.</span><span class="sxs-lookup"><span data-stu-id="04189-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="04189-109">Lisätietoja on kohdassa [Paikallisten tietojen siirtäminen Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) -ohjelmaan [!INCLUDE[prodshort](includes/prodshort.md)]-hallintasisällössä .</span><span class="sxs-lookup"><span data-stu-id="04189-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="04189-110">Paikallinen Business Central</span><span class="sxs-lookup"><span data-stu-id="04189-110">Business Central on-premises</span></span>

<span data-ttu-id="04189-111">Jos käytät [!INCLUDE[prodshort](includes/prodshort.md)]in paikallista versiota, hanki **Älykäs Pilvipohja**, sekä **Business Central Älykäs Pilvi** -laajennukset, ja suorita sitten **Pilveen siirron määritys** -avustettu aloitusopas.</span><span class="sxs-lookup"><span data-stu-id="04189-111">If you are using an on-premises deployment of [!INCLUDE[prodshort](includes/prodshort.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="04189-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="04189-112">Dynamics GP</span></span>

<span data-ttu-id="04189-113">Jos käytät Dynamics GP:tä, hanki **Älykäs pilvipohjainen laajennus** -laajennus ja **Dynamics GP Älykäs pilvi** -laajennus, ja suorita sitten **Pilveen siirron määritys** -avustettu aloitusopas.</span><span class="sxs-lookup"><span data-stu-id="04189-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="04189-114">Siirtymistä Dynamics GP:stä asetusten ohjatulla **pilvitoimintojen määrityksellä** tuetaan tällä hetkellä vain seuraavilla markkina-alueilla: Yhdysvallat, Kanada ja Yhdistynyt kuningaskunta.</span><span class="sxs-lookup"><span data-stu-id="04189-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="04189-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="04189-115">Dynamics SL</span></span>

<span data-ttu-id="04189-116">Jos käytät Dynamics SL_ää, hanki **Älykäs pilvipohjainen** -laajennus, **Microsoft Dynamics SL Älykäs pilvi** -laajennus ja **Microsoft Dynamics SL Historiatietojen älykkäät listat** -laajennus ja suorita sitten **Pilveen siirron määritys** -avustettu aloitusopas.</span><span class="sxs-lookup"><span data-stu-id="04189-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="04189-117">Katso myös</span><span class="sxs-lookup"><span data-stu-id="04189-117">See Also</span></span>

[<span data-ttu-id="04189-118">Älykkäät Tiedot </span><span class="sxs-lookup"><span data-stu-id="04189-118">Intelligent Insights</span></span>](about-intelligent-cloud.md)  
[<span data-ttu-id="04189-119">Älykäs pilvipohjainen laajennus</span><span class="sxs-lookup"><span data-stu-id="04189-119">Intelligent Cloud Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
