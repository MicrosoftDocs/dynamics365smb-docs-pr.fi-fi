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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 137d44db160d0f1e832cc344a779e6bf01a64bbd
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2911129"
---
# <a name="select-a-check-layout"></a><span data-ttu-id="58113-103">Sekin asettelun valitseminen</span><span class="sxs-lookup"><span data-stu-id="58113-103">Select a Check Layout</span></span>
<span data-ttu-id="58113-104">Voit suunnitella omat sekit, joiden avulla pystyt noudattamaan paikallisten viranomaisten määrittämiä standardeja.</span><span class="sxs-lookup"><span data-stu-id="58113-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="58113-105">Sekkikuvat voidaan tulostaa englannin-, ranskan ja espanjankielisinä.</span><span class="sxs-lookup"><span data-stu-id="58113-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="58113-106">Sekit suunnitellaan tulostettavaksi sekä Yhdysvaltojen että Kanadan sekkikuvamuodoissa joko muodossa sekki-talonki-sekki tai talonki-talonki-sekki.</span><span class="sxs-lookup"><span data-stu-id="58113-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-select-a-check-layout"></a><span data-ttu-id="58113-107">Sekin asettelun valitseminen</span><span class="sxs-lookup"><span data-stu-id="58113-107">To select a check layout</span></span>
1. <span data-ttu-id="58113-108">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Raporttivalintojen pankkitili** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="58113-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="58113-109">Valitse **Raporttivalinta - Pankkitili** -sivun **Käyttö**-kentässä **Sekki**.</span><span class="sxs-lookup"><span data-stu-id="58113-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="58113-110">Valitse jompikumpi seuraavista raportin tunnuksista:</span><span class="sxs-lookup"><span data-stu-id="58113-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="58113-111">Raportin tunnus</span><span class="sxs-lookup"><span data-stu-id="58113-111">Report ID</span></span> | <span data-ttu-id="58113-112">Raportin nimi</span><span class="sxs-lookup"><span data-stu-id="58113-112">Report Name</span></span> | <span data-ttu-id="58113-113">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="58113-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="58113-114">1401</span><span class="sxs-lookup"><span data-stu-id="58113-114">1401</span></span> |<span data-ttu-id="58113-115">Sekki</span><span class="sxs-lookup"><span data-stu-id="58113-115">Check</span></span> |<span data-ttu-id="58113-116">Tämä on oletusraportti.</span><span class="sxs-lookup"><span data-stu-id="58113-116">This is the default report.</span></span> |
| <span data-ttu-id="58113-117">10411</span><span class="sxs-lookup"><span data-stu-id="58113-117">10411</span></span> |<span data-ttu-id="58113-118">Sekki (talonki/talonki/sekki)</span><span class="sxs-lookup"><span data-stu-id="58113-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="58113-119">Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/talonki/sekki.</span><span class="sxs-lookup"><span data-stu-id="58113-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="58113-120">10412</span><span class="sxs-lookup"><span data-stu-id="58113-120">10412</span></span> |<span data-ttu-id="58113-121">Sekki (talonki/sekki/talonki)</span><span class="sxs-lookup"><span data-stu-id="58113-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="58113-122">Tämä raportti on suunniteltu tulostamaan sekit muodossa talonki/sekki/talonki.</span><span class="sxs-lookup"><span data-stu-id="58113-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
| <span data-ttu-id="58113-123">10413</span><span class="sxs-lookup"><span data-stu-id="58113-123">10413</span></span> |<span data-ttu-id="58113-124">Kolme sekkiä sivulla</span><span class="sxs-lookup"><span data-stu-id="58113-124">Three Checks per Page</span></span> |<span data-ttu-id="58113-125">Tämä raportti on suunniteltu tulostamaan kolme sekkiä kullakin sivulla.</span><span class="sxs-lookup"><span data-stu-id="58113-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="58113-126">Kun olet määrittänyt sekkien asettelut, voit tulostaa sekit **Maksupäiväkirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="58113-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="58113-127">Lisätietoja on kohdassa [Sekkien käyttäminen](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="58113-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

<span data-ttu-id="58113-128">Voit muuttaa jotakin näistä sekkien oletusasetteluista käyttämällä joko Word- tai RDLC-integrointia.</span><span class="sxs-lookup"><span data-stu-id="58113-128">To change one of these default check layouts, use either the Word or the RDLC integration to do so.</span></span> <span data-ttu-id="58113-129">Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="58113-129">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="58113-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="58113-130">See Also</span></span>
[<span data-ttu-id="58113-131">Raporttien mukautettujen asettelujen luominen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="58113-131">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="58113-132">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="58113-132">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="58113-133">[Pankkitilien täsmäytys](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="58113-133">[Reconciling Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="58113-134">Kauden lopun prosessien viimeisteleminen</span><span class="sxs-lookup"><span data-stu-id="58113-134">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="58113-135">[[!INCLUDE[prodshort](includes/prodshort.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="58113-135">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="58113-136">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="58113-136">General Business Functionality</span></span>](ui-across-business-areas.md)
