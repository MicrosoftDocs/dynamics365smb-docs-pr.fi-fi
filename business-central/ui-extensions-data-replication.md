---
title: Pilvipalveluihin siirtymisen laajennukset
description: Pilvipohjaisen siirron laajennusten avulla voit siirtää paikallisen datan Business Central -verkkopalveluun. Nämä laajennukset siirtävät sisäiset tiedot pilveen, jotta voit käyttää Business Centralin tietoja verkossa aiemmin luotujen tietojesi kanssa.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f02face497affd1fd1467c118e10e69f2be39b85
ms.sourcegitcommit: 951d3c9d541f0b1d26712d37e253c2958dae3321
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889122"
---
# <a name="cloud-migration-extensions-for-migrating-to-business-central-online"></a><span data-ttu-id="c4230-104">Business Central Onlineen siirtymisen pilvipalvelujen siirtymislaajennukset</span><span class="sxs-lookup"><span data-stu-id="c4230-104">Cloud Migration Extensions for Migrating to Business Central Online</span></span>

<span data-ttu-id="c4230-105">Paikallisen ratkaisun mukaan sinun on käytettävä eri laajennuksia, jotta voisit yhdistää tiedot [!INCLUDE[prod_short](includes/prod_short.md)] -verkkoon, jotta voisit siirtää ratkaisun pilveen.</span><span class="sxs-lookup"><span data-stu-id="c4230-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prod_short](includes/prod_short.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="c4230-106">Jos käytät jotakin tuettua paikallista tuotetta, voit määrittää pilviympäristön tuotekohtaisen laajennuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="c4230-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span> <span data-ttu-id="c4230-107">Kun pilviympäristö on määritetty, voit siirtää paikallisen ratkaisun tiedot [!INCLUDE[prod_short](includes/prod_short.md)]iin.</span><span class="sxs-lookup"><span data-stu-id="c4230-107">Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="c4230-108">Tämän jälkeen voit käyttää pilveä ja hyödyntää sitä liiketoiminnassa. Saat entistä enemmän tietoja liiketoiminnasta sekä voit käyttää tekoälyä ja useita laitteita milloin tahansa ja missä tahansa.</span><span class="sxs-lookup"><span data-stu-id="c4230-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="c4230-109">Lisätietoja on kohdassa [Paikallisten tietojen siirtäminen Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) -ohjelmaan [!INCLUDE[prod_short](includes/prod_short.md)]-hallintasisällössä.</span><span class="sxs-lookup"><span data-stu-id="c4230-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="c4230-110">Paikallinen Business Central</span><span class="sxs-lookup"><span data-stu-id="c4230-110">Business Central on-premises</span></span>

<span data-ttu-id="c4230-111">Jos käytät [!INCLUDE[prod_short](includes/prod_short.md)]in paikallista versiota, hanki **Älykäs Pilvipohja**, sekä **Business Central Älykäs Pilvi** -laajennukset, ja suorita sitten **Pilveen siirron määritys** -avustettu aloitusopas.</span><span class="sxs-lookup"><span data-stu-id="c4230-111">If you are using an on-premises deployment of [!INCLUDE[prod_short](includes/prod_short.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="c4230-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="c4230-112">Dynamics GP</span></span>

<span data-ttu-id="c4230-113">Jos käytät Dynamics GP:tä, hanki **Älykäs pilvipohjainen laajennus** -laajennus ja **Dynamics GP Älykäs pilvi** -laajennus, ja suorita sitten **Pilveen siirron määritys** -avustettu aloitusopas.</span><span class="sxs-lookup"><span data-stu-id="c4230-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="c4230-114">Siirtymistä Dynamics GP:stä asetusten ohjatulla **pilvitoimintojen määrityksellä** tuetaan tällä hetkellä vain seuraavilla markkina-alueilla: Yhdysvallat, Kanada ja Yhdistynyt kuningaskunta.</span><span class="sxs-lookup"><span data-stu-id="c4230-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="c4230-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="c4230-115">Dynamics SL</span></span>

<span data-ttu-id="c4230-116">Jos käytät Dynamics SL_ää, hanki **Älykäs pilvipohjainen** -laajennus, **Microsoft Dynamics SL Älykäs pilvi** -laajennus ja **Microsoft Dynamics SL Historiatietojen älykkäät listat** -laajennus ja suorita sitten **Pilveen siirron määritys** -avustettu aloitusopas.</span><span class="sxs-lookup"><span data-stu-id="c4230-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c4230-117">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c4230-117">See Also</span></span>

[<span data-ttu-id="c4230-118">Pilvipalveluihin siirtymisen peruslaajennus</span><span class="sxs-lookup"><span data-stu-id="c4230-118">Cloud Migration Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
[<span data-ttu-id="c4230-119">Paikallisten tietojen siirtäminen Business Central Onlineen</span><span class="sxs-lookup"><span data-stu-id="c4230-119">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  

[!INCLUDE[footer-include](includes/footer-banner.md)]