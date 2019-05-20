---
title: Sekin asettelun määrittäminen| Microsoft Docs
description: Voit suunnitella ja tulostaa sekkisi eri muodoissa standardinmukaisia vaatimuksia noudattaen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont
ms.openlocfilehash: f2b7fa01cff36e3aab335f7d5921954343c69b74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243593"
---
# <a name="define-check-layouts"></a><span data-ttu-id="cf06c-103">Sekkien asetteluiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cf06c-103">Define Check Layouts</span></span>
<span data-ttu-id="cf06c-104">Voit suunnitella omat sekit, joiden avulla pystyt noudattamaan paikallisten viranomaisten määrittämiä standardeja.</span><span class="sxs-lookup"><span data-stu-id="cf06c-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="cf06c-105">Sekkikuvat voidaan tulostaa englannin-, ranskan ja espanjankielisinä.</span><span class="sxs-lookup"><span data-stu-id="cf06c-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="cf06c-106">Sekit suunnitellaan tulostettavaksi sekä Yhdysvaltojen että Kanadan sekkikuvamuodoissa joko muodossa sekki-talonki-sekki tai talonki-talonki-sekki.</span><span class="sxs-lookup"><span data-stu-id="cf06c-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="cf06c-107">Sekkien asetteluiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cf06c-107">To define check layouts</span></span>
1. <span data-ttu-id="cf06c-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttivalintojen pankkitili** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="cf06c-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="cf06c-109">Valitse **Raporttivalinta - Pankkitili** -sivun **Käyttö**-kentässä **Sekki**.</span><span class="sxs-lookup"><span data-stu-id="cf06c-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="cf06c-110">Valitse jompikumpi seuraavista raportin tunnuksista:</span><span class="sxs-lookup"><span data-stu-id="cf06c-110">Select one of the following report IDs.</span></span>

  | <span data-ttu-id="cf06c-111">Raportin tunnus</span><span class="sxs-lookup"><span data-stu-id="cf06c-111">Report ID</span></span> | <span data-ttu-id="cf06c-112">Raportin nimi</span><span class="sxs-lookup"><span data-stu-id="cf06c-112">Report Name</span></span> | <span data-ttu-id="cf06c-113">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="cf06c-113">Description</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="cf06c-114">1401</span><span class="sxs-lookup"><span data-stu-id="cf06c-114">1401</span></span> |<span data-ttu-id="cf06c-115">Sekki</span><span class="sxs-lookup"><span data-stu-id="cf06c-115">Check</span></span> |<span data-ttu-id="cf06c-116">Tämä on oletusraportti.</span><span class="sxs-lookup"><span data-stu-id="cf06c-116">This is the default report.</span></span> |
  | <span data-ttu-id="cf06c-117">10411</span><span class="sxs-lookup"><span data-stu-id="cf06c-117">10411</span></span> |<span data-ttu-id="cf06c-118">Sekki (talonki/talonki/sekki)</span><span class="sxs-lookup"><span data-stu-id="cf06c-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="cf06c-119">Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/talonki/sekki.</span><span class="sxs-lookup"><span data-stu-id="cf06c-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
  | <span data-ttu-id="cf06c-120">10412</span><span class="sxs-lookup"><span data-stu-id="cf06c-120">10412</span></span> |<span data-ttu-id="cf06c-121">Sekki (talonki/sekki/talonki)</span><span class="sxs-lookup"><span data-stu-id="cf06c-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="cf06c-122">Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/sekki/talonki.</span><span class="sxs-lookup"><span data-stu-id="cf06c-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
  | <span data-ttu-id="cf06c-123">10413</span><span class="sxs-lookup"><span data-stu-id="cf06c-123">10413</span></span> |<span data-ttu-id="cf06c-124">Kolme sekkiä sivulla</span><span class="sxs-lookup"><span data-stu-id="cf06c-124">Three Checks per Page</span></span> |<span data-ttu-id="cf06c-125">Tämä raportti on suunniteltu tulostamaan kolme sekkiä kullakin sivulla.</span><span class="sxs-lookup"><span data-stu-id="cf06c-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="cf06c-126">Kun olet määrittänyt sekkien asettelut, voit tulostaa sekit **Maksupäiväkirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="cf06c-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="cf06c-127">Lisätietoja on kohdassa [Sekkien käyttäminen](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="cf06c-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="cf06c-128">Katso myös</span><span class="sxs-lookup"><span data-stu-id="cf06c-128">See Also</span></span>
[<span data-ttu-id="cf06c-129">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="cf06c-129">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="cf06c-130">[Pankkitilien hallinta](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="cf06c-130">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="cf06c-131">Kauden lopun prosessien viimeisteleminen</span><span class="sxs-lookup"><span data-stu-id="cf06c-131">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="cf06c-132">[[!INCLUDE[prodshort](includes/prodshort.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cf06c-132">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="cf06c-133">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="cf06c-133">General Business Functionality</span></span>](ui-across-business-areas.md)
