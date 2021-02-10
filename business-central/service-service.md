---
title: Huoltohallinta | Microsoft Docs
description: Lisätietoja toiminnoista, jotka on suunniteltu tukemaan korjaamossa ja kentällä tapahtuvia huoltotoimintoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cb82642f5526db849ad5344d1f7347513d80c57a
ms.sourcegitcommit: edac6cbb8b19ac426f8dcbc83f0f9e308fb0d45d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/29/2020
ms.locfileid: "4817002"
---
# <a name="service-management"></a><span data-ttu-id="8b405-103">Huoltohallinto</span><span class="sxs-lookup"><span data-stu-id="8b405-103">Service Management</span></span>
> [!NOTE]
> <span data-ttu-id="8b405-104">Tässä ohjeaiheessa ja aliohjeaiheissa esitellyt toiminnot näkyvät käyttöliittymässä vain, jos käytössä on **Premium**-käyttökokemus.</span><span class="sxs-lookup"><span data-stu-id="8b405-104">Functionality described in this topic and sub topics is only visible in the user interface if you have the **Premium** experience.</span></span> <span data-ttu-id="8b405-105">Lisätietoja on kohdassa [Näytettävien ominaisuuksien muuttaminen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="8b405-105">For more information, see [Change Which Features are Displayed](ui-experiences.md).</span></span>

<span data-ttu-id="8b405-106">Jatkuvan huollon tarjoaminen asiakkaille on tärkeä osa liiketoimintaa. Toimiva huolto lisää asiakkaiden tyytyväisyyttä ja uskollisuutta sekä kasvattaa tuottoa</span><span class="sxs-lookup"><span data-stu-id="8b405-106">Providing ongoing service to customers is an important part of any business and one that can be a source of customer satisfaction and loyalty, in addition to revenue.</span></span> <span data-ttu-id="8b405-107">Huollon hallinta ja seuranta ei kuitenkaan aina ole helppoa. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää työkaluja, jotka helpottavat näitä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="8b405-107">However, managing and tracking service is not always easy, and [!INCLUDE[prod_short](includes/prod_short.md)] provides a set of tools to help.</span></span> <span data-ttu-id="8b405-108">Nämä työkalut on suunniteltu tukemaan korjaamojen sekä kentällä tapahtuvan huollon toimintoja, ja niitä voi käyttää myös liiketoimintaskenaarioissa, kuten asiakaspalvelun monitasoisissa jakelujärjestelmissä, tuoterakenteita käyttävissä teollisuushuoltoympäristöissä, usean huoltoteknikon lähettämisessä sekä varaosien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="8b405-108">These tools are designed to support repair shop and field service operations, and can be used in business scenarios such as complex customer service distribution systems, industrial service environments with bills of materials, and high volume dispatching of service technicians with requirements for spare parts management.</span></span>  

 <span data-ttu-id="8b405-109">Näillä työkaluilla voit tehdä seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="8b405-109">With these tools you can accomplish the following:</span></span>  

* <span data-ttu-id="8b405-110">ajoittaa huoltokäyntejä ja määrittää huoltotilauksia</span><span class="sxs-lookup"><span data-stu-id="8b405-110">Schedule service calls and set up service orders.</span></span>  
* <span data-ttu-id="8b405-111">seurata korjausosia ja tarvikkeita</span><span class="sxs-lookup"><span data-stu-id="8b405-111">Track repair parts and supplies.</span></span>  
* <span data-ttu-id="8b405-112">määrittää huoltohenkilöstöä taitojen ja saatavuuden perusteella</span><span class="sxs-lookup"><span data-stu-id="8b405-112">Assign service personnel based on skill and availability.</span></span>  
* <span data-ttu-id="8b405-113">luoda huoltoarvioita ja -laskuja.</span><span class="sxs-lookup"><span data-stu-id="8b405-113">Provide service estimates and service invoices.</span></span>  

<span data-ttu-id="8b405-114">Lisäksi työkaluja voi käyttää koodien standardisointiin, sopimusten määrittämiseen, laskutuskäytäntöjen käyttöönottoon ja huoltohenkilöstön reittikarttojen luomiseen.</span><span class="sxs-lookup"><span data-stu-id="8b405-114">In addition, you can standardize coding, set up contracts, implement a discounting policy, and create route maps for service employees.</span></span>  

<span data-ttu-id="8b405-115">Huoltohallinto koostuu tavallisesti kahdesta osasta: järjestelmän määrittämisestä ja käyttämisestä. Järjestelmä taas sisältää hinnoittelun, sopimukset, tilaukset, huoltohenkilöstön lähettämisen sekä työn aikataulutuksen.</span><span class="sxs-lookup"><span data-stu-id="8b405-115">In general, there are two aspects to service management: configuring and setting up your system, and using it for pricing, contracts, orders, service personnel dispatch, and job scheduler.</span></span>  

<span data-ttu-id="8b405-116">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="8b405-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="8b405-117">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="8b405-117">**To**</span></span>|<span data-ttu-id="8b405-118">**Katso**</span><span class="sxs-lookup"><span data-stu-id="8b405-118">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="8b405-119">Määritä huoltohallinto, kuten vikakoodit, käytännöt sekä oletusasiakirjat ja -mallit.</span><span class="sxs-lookup"><span data-stu-id="8b405-119">Set up Service Management, including fault codes, policies, default documents and templates.</span></span>|[<span data-ttu-id="8b405-120">Huoltohallinnon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8b405-120">Setting Up Service Management</span></span>](service-setup-service.md)|  
|<span data-ttu-id="8b405-121">Hallitse huoltohinnoittelua, luo huoltonimikkeitä ja hahmota etenemisen seuranta.</span><span class="sxs-lookup"><span data-stu-id="8b405-121">Manage service pricing, create service items, and understand how to monitor progress.</span></span>|[<span data-ttu-id="8b405-122">Huollon suunnittelu</span><span class="sxs-lookup"><span data-stu-id="8b405-122">Planning Service</span></span>](service-plan-service.md)|  
|<span data-ttu-id="8b405-123">Luo ja hallitse asiakkaiden kanssa tehtyjä sopimuksia.</span><span class="sxs-lookup"><span data-stu-id="8b405-123">Create and manage contractual agreements between you and your customers.</span></span>|[<span data-ttu-id="8b405-124">Huoltosopimusten toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="8b405-124">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)|  
|<span data-ttu-id="8b405-125">Tarjoa asiakkaille huoltoja ja laskuta huoltotilauksia.</span><span class="sxs-lookup"><span data-stu-id="8b405-125">Provide service to customers, and invoice service orders.</span></span>|[<span data-ttu-id="8b405-126">Huollon toimittaminen</span><span class="sxs-lookup"><span data-stu-id="8b405-126">Delivering Service</span></span>](service-deliver-service.md)|  

## <a name="see-also"></a><span data-ttu-id="8b405-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8b405-127">See Also</span></span>  
<span data-ttu-id="8b405-128">[Myyntisaamisten hallinta](receivables-manage-receivables.md) </span><span class="sxs-lookup"><span data-stu-id="8b405-128">[Managing Receivables](receivables-manage-receivables.md) </span></span>  
<span data-ttu-id="8b405-129">[Projektit](projects-how-create-jobs.md) </span><span class="sxs-lookup"><span data-stu-id="8b405-129">[Jobs](projects-how-create-jobs.md) </span></span>  
<span data-ttu-id="8b405-130">[Tervetuloa [!INCLUDE[prod_long](includes/prod_long.md)]iin!](index.md)</span><span class="sxs-lookup"><span data-stu-id="8b405-130">[Welcome to [!INCLUDE[prod_long](includes/prod_long.md)] ](index.md)</span></span>

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
