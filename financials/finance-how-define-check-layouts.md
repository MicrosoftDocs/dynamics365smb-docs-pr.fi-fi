---
title: "Sekin asettelun määrittäminen| Microsoft Docs"
description: Voit suunnitella ja tulostaa sekkisi eri muodoissa standardinmukaisia vaatimuksia noudattaen.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-define-check-layouts"></a><span data-ttu-id="f549b-103">Toimintaohje: Sekkien asetteluiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f549b-103">How to: Define Check Layouts</span></span>
<span data-ttu-id="f549b-104">Voit suunnitella omat sekit, joiden avulla pystyt noudattamaan paikallisten viranomaisten määrittämiä standardeja.</span><span class="sxs-lookup"><span data-stu-id="f549b-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="f549b-105">Sekkikuvat voidaan tulostaa englannin-, ranskan ja espanjankielisinä.</span><span class="sxs-lookup"><span data-stu-id="f549b-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="f549b-106">Sekit suunnitellaan tulostettavaksi sekä Yhdysvaltojen että Kanadan sekkikuvamuodoissa joko muodossa sekki-talonki-sekki tai talonki-talonki-sekki.</span><span class="sxs-lookup"><span data-stu-id="f549b-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="f549b-107">Sekkien asetteluiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f549b-107">To define check layouts</span></span>
1. <span data-ttu-id="f549b-108">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Raporttivalintojen pankkitili** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f549b-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="f549b-109">Valitse **Raporttivalinta - Pankkitili** -ikkunan</span><span class="sxs-lookup"><span data-stu-id="f549b-109">In the **Report Selection - Bank Acc.**</span></span> <span data-ttu-id="f549b-110">**Käyttö**-kentässä **Sekki**.</span><span class="sxs-lookup"><span data-stu-id="f549b-110">window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="f549b-111">Valitse jompikumpi seuraavista raportin tunnuksista:</span><span class="sxs-lookup"><span data-stu-id="f549b-111">Select one of the following report IDs.</span></span>

| <span data-ttu-id="f549b-112">Raportin tunnus</span><span class="sxs-lookup"><span data-stu-id="f549b-112">Report ID</span></span> | <span data-ttu-id="f549b-113">Raportin nimi</span><span class="sxs-lookup"><span data-stu-id="f549b-113">Report Name</span></span> | <span data-ttu-id="f549b-114">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f549b-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f549b-115">1401</span><span class="sxs-lookup"><span data-stu-id="f549b-115">1401</span></span> |<span data-ttu-id="f549b-116">Sekki</span><span class="sxs-lookup"><span data-stu-id="f549b-116">Check</span></span> |<span data-ttu-id="f549b-117">Tämä on oletusraportti.</span><span class="sxs-lookup"><span data-stu-id="f549b-117">This is the default report.</span></span> |
| <span data-ttu-id="f549b-118">10401</span><span class="sxs-lookup"><span data-stu-id="f549b-118">10401</span></span> |<span data-ttu-id="f549b-119">Sekki (talonki/talonki/sekki)</span><span class="sxs-lookup"><span data-stu-id="f549b-119">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="f549b-120">Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/talonki/sekki.</span><span class="sxs-lookup"><span data-stu-id="f549b-120">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="f549b-121">10411</span><span class="sxs-lookup"><span data-stu-id="f549b-121">10411</span></span> |<span data-ttu-id="f549b-122">Sekki (talonki/sekki/talonki)</span><span class="sxs-lookup"><span data-stu-id="f549b-122">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="f549b-123">Tämä raportti on suunniteltu tulostamaan sekit muodossa sekki/talonki/sekki.</span><span class="sxs-lookup"><span data-stu-id="f549b-123">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="f549b-124">Kun olet määrittänyt sekkien asettelut, voit tulostaa sekit **Maksupäiväkirja**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="f549b-124">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="f549b-125">Lisätietoja on kohdassa [Sekkien käyttäminen](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="f549b-125">For more information, see [How to: Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f549b-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f549b-126">See Also</span></span>
[<span data-ttu-id="f549b-127">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="f549b-127">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="f549b-128">[Pankkitilien hallinta](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="f549b-128">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="f549b-129">Kauden lopun prosessien viimeisteleminen</span><span class="sxs-lookup"><span data-stu-id="f549b-129">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="f549b-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f549b-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="f549b-131">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="f549b-131">General Business Functionality</span></span>](ui-across-business-areas.md)

