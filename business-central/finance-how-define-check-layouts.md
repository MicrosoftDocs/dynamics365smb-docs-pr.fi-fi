---
title: Sekin asettelun määrittäminen| Microsoft Docs
description: Voit suunnitella ja tulostaa sekkisi eri muodoissa standardinmukaisia vaatimuksia noudattaen.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: eace865bc70f56206d478f8e8d38fd217133925e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "935256"
---
# <a name="define-check-layouts"></a><span data-ttu-id="ec196-103">Sekkien asetteluiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ec196-103">Define Check Layouts</span></span>
<span data-ttu-id="ec196-104">Voit suunnitella omat sekit, joiden avulla pystyt noudattamaan paikallisten viranomaisten määrittämiä standardeja.</span><span class="sxs-lookup"><span data-stu-id="ec196-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="ec196-105">Sekkikuvat voidaan tulostaa englannin-, ranskan ja espanjankielisinä.</span><span class="sxs-lookup"><span data-stu-id="ec196-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="ec196-106">Sekit suunnitellaan tulostettavaksi sekä Yhdysvaltojen että Kanadan sekkikuvamuodoissa joko muodossa sekki-talonki-sekki tai talonki-talonki-sekki.</span><span class="sxs-lookup"><span data-stu-id="ec196-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="ec196-107">Sekkien asetteluiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ec196-107">To define check layouts</span></span>
1. <span data-ttu-id="ec196-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttivalintojen pankkitili** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="ec196-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="ec196-109">Valitse **Raporttivalinta - Pankkitili** -sivun **Käyttö**-kentässä **Sekki**.</span><span class="sxs-lookup"><span data-stu-id="ec196-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="ec196-110">Valitse jompikumpi seuraavista raportin tunnuksista:</span><span class="sxs-lookup"><span data-stu-id="ec196-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="ec196-111">Raportin tunnus</span><span class="sxs-lookup"><span data-stu-id="ec196-111">Report ID</span></span> | <span data-ttu-id="ec196-112">Raportin nimi</span><span class="sxs-lookup"><span data-stu-id="ec196-112">Report Name</span></span> | <span data-ttu-id="ec196-113">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="ec196-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ec196-114">1401</span><span class="sxs-lookup"><span data-stu-id="ec196-114">1401</span></span> |<span data-ttu-id="ec196-115">Sekki</span><span class="sxs-lookup"><span data-stu-id="ec196-115">Check</span></span> |<span data-ttu-id="ec196-116">Tämä on oletusraportti.</span><span class="sxs-lookup"><span data-stu-id="ec196-116">This is the default report.</span></span> |
| <span data-ttu-id="ec196-117">10401</span><span class="sxs-lookup"><span data-stu-id="ec196-117">10401</span></span> |<span data-ttu-id="ec196-118">Sekki (talonki/talonki/sekki)</span><span class="sxs-lookup"><span data-stu-id="ec196-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="ec196-119">Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/talonki/sekki.</span><span class="sxs-lookup"><span data-stu-id="ec196-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="ec196-120">10411</span><span class="sxs-lookup"><span data-stu-id="ec196-120">10411</span></span> |<span data-ttu-id="ec196-121">Sekki (talonki/sekki/talonki)</span><span class="sxs-lookup"><span data-stu-id="ec196-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="ec196-122">Tämä raportti on suunniteltu tulostamaan sekit muodossa sekki/talonki/sekki.</span><span class="sxs-lookup"><span data-stu-id="ec196-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="ec196-123">Kun olet määrittänyt sekkien asettelut, voit tulostaa sekit **Maksupäiväkirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ec196-123">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="ec196-124">Lisätietoja on kohdassa [Sekkien käyttäminen](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="ec196-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ec196-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="ec196-125">See Also</span></span>
[<span data-ttu-id="ec196-126">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="ec196-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="ec196-127">[Pankkitilien hallinta](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="ec196-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="ec196-128">Kauden lopun prosessien viimeisteleminen</span><span class="sxs-lookup"><span data-stu-id="ec196-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="ec196-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ec196-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ec196-130">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="ec196-130">General Business Functionality</span></span>](ui-across-business-areas.md)
