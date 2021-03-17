---
title: Business Central Älykäs pilvi -laajennukset pilvipohjaiseen siirtoon | Microsoft-dokumentit
description: Pilvipohjaisen siirron laajennusten avulla voit siirtää paikallisen datan Business Central -verkkopalveluun. Nämä laajennukset siirtävät sisäiset tiedot pilveen, jotta voit käyttää Business Centralin tietoja verkossa aiemmin luotujen tietojesi kanssa.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5d6110744f14cb959494e2fd5c9b970bd339a77f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377346"
---
# <a name="intelligent-cloud-extensions-for-cloud-migration"></a><span data-ttu-id="1123b-104">Pilvisiirron älykkäät pilvilaajennukset</span><span class="sxs-lookup"><span data-stu-id="1123b-104">Intelligent Cloud Extensions for Cloud Migration</span></span>

<span data-ttu-id="1123b-105">Paikallisen ratkaisun mukaan sinun on käytettävä eri laajennuksia, jotta voisit yhdistää tiedot [!INCLUDE[prod_short](includes/prod_short.md)] -verkkoon, jotta voisit siirtää ratkaisun pilveen.</span><span class="sxs-lookup"><span data-stu-id="1123b-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prod_short](includes/prod_short.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="1123b-106">Jos käytät jotakin tuettua paikallista tuotetta, voit määrittää pilviympäristön tuotekohtaisen laajennuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="1123b-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span> <span data-ttu-id="1123b-107">Kun pilviympäristö on määritetty, voit siirtää paikallisen ratkaisun tiedot [!INCLUDE[prod_short](includes/prod_short.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="1123b-107">Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="1123b-108">Tämän jälkeen voit käyttää pilveä ja hyödyntää sitä liiketoiminnassa. Saat entistä enemmän tietoja liiketoiminnasta sekä voit käyttää tekoälyä ja useita laitteita milloin tahansa ja missä tahansa.</span><span class="sxs-lookup"><span data-stu-id="1123b-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="1123b-109">Lisätietoja on kohdassa [Paikallisten tietojen siirtäminen Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) -ohjelmaan [!INCLUDE[prod_short](includes/prod_short.md)]-hallintasisällössä.</span><span class="sxs-lookup"><span data-stu-id="1123b-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="1123b-110">Paikallinen Business Central</span><span class="sxs-lookup"><span data-stu-id="1123b-110">Business Central on-premises</span></span>

<span data-ttu-id="1123b-111">Jos käytät [!INCLUDE[prod_short](includes/prod_short.md)]in paikallista versiota, hanki **Älykäs Pilvipohja**, sekä **Business Central Älykäs Pilvi** -laajennukset, ja suorita sitten **Pilveen siirron määritys** -avustettu aloitusopas.</span><span class="sxs-lookup"><span data-stu-id="1123b-111">If you are using an on-premises deployment of [!INCLUDE[prod_short](includes/prod_short.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="1123b-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="1123b-112">Dynamics GP</span></span>

<span data-ttu-id="1123b-113">Jos käytät Dynamics GP:tä, hanki **Älykäs pilvipohjainen laajennus** -laajennus ja **Dynamics GP Älykäs pilvi** -laajennus, ja suorita sitten **Pilveen siirron määritys** -avustettu aloitusopas.</span><span class="sxs-lookup"><span data-stu-id="1123b-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="1123b-114">Siirtymistä Dynamics GP:stä asetusten ohjatulla **pilvitoimintojen määrityksellä** tuetaan tällä hetkellä vain seuraavilla markkina-alueilla: Yhdysvallat, Kanada ja Yhdistynyt kuningaskunta.</span><span class="sxs-lookup"><span data-stu-id="1123b-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="1123b-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="1123b-115">Dynamics SL</span></span>

<span data-ttu-id="1123b-116">Jos käytät Dynamics SL_ää, hanki **Älykäs pilvipohjainen** -laajennus, **Microsoft Dynamics SL Älykäs pilvi** -laajennus ja **Microsoft Dynamics SL Historiatietojen älykkäät listat** -laajennus ja suorita sitten **Pilveen siirron määritys** -avustettu aloitusopas.</span><span class="sxs-lookup"><span data-stu-id="1123b-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1123b-117">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1123b-117">See Also</span></span>

[<span data-ttu-id="1123b-118">Älykkäät Tiedot </span><span class="sxs-lookup"><span data-stu-id="1123b-118">Intelligent Insights</span></span>](about-intelligent-cloud.md)  
[<span data-ttu-id="1123b-119">Älykäs pilvipohjainen laajennus</span><span class="sxs-lookup"><span data-stu-id="1123b-119">Intelligent Cloud Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]