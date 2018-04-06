---
title: "Kokoonpanon käyttäminen uusissa yrityksissä | Microsoft Docs"
description: "Kun olet luonut määrityspaketin, seuraava vaihe on ottaa paketti käyttöön asiakkaalle täytäntöönpanoa varten. Käytä kokoonpanoa, jossa on uusi tyhjä yritys."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0e06ca0b3c9c5532c40938dd44112f8cd889a27c
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="apply-configurations-to-new-companies"></a><span data-ttu-id="26f3f-104">Kokoonpanojen käyttäminen uusissa yrityksissä</span><span class="sxs-lookup"><span data-stu-id="26f3f-104">Apply Configurations to New Companies</span></span>
<span data-ttu-id="26f3f-105">Kun olet luonut määrityspaketin, seuraava vaihe on ottaa paketti käyttöön asiakkaalle täytäntöönpanoa varten.</span><span class="sxs-lookup"><span data-stu-id="26f3f-105">After you have created a configuration package, the next step is to deploy the package to your customer for implementation.</span></span> <span data-ttu-id="26f3f-106">Käytössä on määrityspaketti uudessa tyhjässä yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="26f3f-106">You work with the configuration package within a new empty company.</span></span>  

 <span data-ttu-id="26f3f-107">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="26f3f-107">The following table describes a sequence of tasks with links to topics that describe them.</span></span>

|<span data-ttu-id="26f3f-108">**Tehtävä**</span><span class="sxs-lookup"><span data-stu-id="26f3f-108">**To**</span></span>|<span data-ttu-id="26f3f-109">**Katso**</span><span class="sxs-lookup"><span data-stu-id="26f3f-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="26f3f-110">Luo uusi yritys, jossa asiakkaan käyttöönotto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="26f3f-110">Create a new company in which to perform a customer implementation.</span></span>|[<span data-ttu-id="26f3f-111">Uuden yrityksen luominen</span><span class="sxs-lookup"><span data-stu-id="26f3f-111">Create a New Company</span></span>](admin-how-to-create-a-new-company.md)|  
|<span data-ttu-id="26f3f-112">Tuo uuden yrityksen määrityspaketti ja ota se käyttöön.</span><span class="sxs-lookup"><span data-stu-id="26f3f-112">Import and apply a configuration package to a new company.</span></span>|[<span data-ttu-id="26f3f-113">Uusien yritysten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="26f3f-113">Configure New Companies</span></span>](admin-how-to-configure-new-companies.md)|  
|<span data-ttu-id="26f3f-114">Voit suorittaa yrityksen määrityksen helposti asetusten ohjatun määrityksen ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="26f3f-114">Use an assisted setup guide to easily complete a company configuration.</span></span>|[<span data-ttu-id="26f3f-115">Yrityksen ja ohjatun RapidStart-toiminnon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="26f3f-115">Configure a Company with the RapidStart Wizard</span></span>](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md)|
|<span data-ttu-id="26f3f-116">Lataa ja tuo määrityspaketti PowerShell-ratkaisun avulla.</span><span class="sxs-lookup"><span data-stu-id="26f3f-116">Load and import a configuration package with PowerShell.</span></span>|[<span data-ttu-id="26f3f-117">Uusien yritysten määrittäminen cmdlet-komennolla</span><span class="sxs-lookup"><span data-stu-id="26f3f-117">Configure New Companies using a Cmdlet</span></span>](admin-how-to-configure-new-companies-using-a-cmdlet.md)|
|<span data-ttu-id="26f3f-118">Kopioi yleisesti käytetyt arvot aiemmin määritetystä yrityksestä saman tietokannan uuteen yritykseen.</span><span class="sxs-lookup"><span data-stu-id="26f3f-118">Copy commonly used values from an existing company to a new one, within the same database.</span></span>|[<span data-ttu-id="26f3f-119">Tietojen kopioiminen uusiin yrityksiin</span><span class="sxs-lookup"><span data-stu-id="26f3f-119">Copy Data to New Companies</span></span>](admin-how-to-copy-data-to-new-companies.md)|  
|<span data-ttu-id="26f3f-120">Siirrä vanhat tilisaldot juuri määritettyyn yritykseen eräajon avulla. Kohdista sitten tuloksena saatavat päiväkirjatapahtumat.</span><span class="sxs-lookup"><span data-stu-id="26f3f-120">Use a batch job to transfer legacy account balances to a newly configured company and then apply the resulting journal entries.</span></span>|[<span data-ttu-id="26f3f-121">Kirjauskansion alkusaldojen luominen</span><span class="sxs-lookup"><span data-stu-id="26f3f-121">Create Journal Opening Balances</span></span>](admin-how-to-create-journal-opening-balances.md)|  

## <a name="see-also"></a><span data-ttu-id="26f3f-122">Katso myös</span><span class="sxs-lookup"><span data-stu-id="26f3f-122">See Also</span></span>  
[<span data-ttu-id="26f3f-123">Yrityksen määrittäminen RapidStart Services -palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="26f3f-123">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="26f3f-124">Hallinta</span><span class="sxs-lookup"><span data-stu-id="26f3f-124">Administration</span></span>](admin-setup-and-administration.md)

