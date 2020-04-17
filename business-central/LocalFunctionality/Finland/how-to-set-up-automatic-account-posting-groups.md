---
title: Automaattisten tilin kirjausryhmien määrittäminen
description: Voit käyttää automaattisia tilikoodeja automaattisen tilin kirjausryhmän luonnin jälkeen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1d312a9c93b1cb93a7ff2582d49600f09597359a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180808"
---
# <a name="set-up-automatic-account-posting-groups"></a><span data-ttu-id="23a94-103">Automaattisten tilin kirjausryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="23a94-103">Set Up Automatic Account Posting Groups</span></span>
<span data-ttu-id="23a94-104">Voit käyttää automaattisia tilikoodeja automaattisen tilin kirjausryhmän luonnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="23a94-104">To use automatic account codes, you must create an automatic account posting group.</span></span>  

## <a name="to-set-up-automatic-account-posting-groups"></a><span data-ttu-id="23a94-105">Automaattisten tilin kirjausryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="23a94-105">To set up automatic account posting groups</span></span>  

1.  <span data-ttu-id="23a94-106">Valitse ![Etsi sivu tai raportti](../../media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Automaattijakauma** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="23a94-106">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Auto. Acc. Groups**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="23a94-107">Valitse **Uusi**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="23a94-107">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="23a94-108">Täytä **Yleinen**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="23a94-108">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="23a94-109">Kenttä</span><span class="sxs-lookup"><span data-stu-id="23a94-109">Field</span></span>|<span data-ttu-id="23a94-110">Description</span><span class="sxs-lookup"><span data-stu-id="23a94-110">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="23a94-111">**Nro**</span><span class="sxs-lookup"><span data-stu-id="23a94-111">**No.**</span></span>|<span data-ttu-id="23a94-112">Anna automaattiselle tilin kirjausryhmälle yksilöivä aakkosnumeerinen numero.</span><span class="sxs-lookup"><span data-stu-id="23a94-112">Enter a unique alphanumeric number for the automatic account posting group.</span></span>|  
    |<span data-ttu-id="23a94-113">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="23a94-113">**Description**</span></span>|<span data-ttu-id="23a94-114">Anna automaattisen tilin kirjausryhmän kuvaus.</span><span class="sxs-lookup"><span data-stu-id="23a94-114">Enter a description for the automatic account posting group.</span></span>|  

4.  <span data-ttu-id="23a94-115">Täytä **Automaattinen tilirivi** -pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="23a94-115">On the **Automatic Acc. Line** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="23a94-116">Kenttä</span><span class="sxs-lookup"><span data-stu-id="23a94-116">Field</span></span>|<span data-ttu-id="23a94-117">Description</span><span class="sxs-lookup"><span data-stu-id="23a94-117">Description</span></span>|  
    |-----------|-----------------|  
    |<span data-ttu-id="23a94-118">**Kohdistusprosentti**</span><span class="sxs-lookup"><span data-stu-id="23a94-118">**Allocation Percentage**</span></span>|<span data-ttu-id="23a94-119">Anna lähderivin summan kohdistettava prosentti.</span><span class="sxs-lookup"><span data-stu-id="23a94-119">Enter the percentage of the source line amount that is to be allocated.</span></span>|  
    |<span data-ttu-id="23a94-120">**KP-tilinro**</span><span class="sxs-lookup"><span data-stu-id="23a94-120">**G/L Account No.**</span></span>|<span data-ttu-id="23a94-121">Anna kirjanpitotilin numero, jolle kohdistus kirjataan.</span><span class="sxs-lookup"><span data-stu-id="23a94-121">Enter the general ledger account number to which the allocation should be posted.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="23a94-122">**Kokonaissaldo**-kentässä lasketaan yhteen kirjausryhmän automaattisten tilirivien **Kohdistusprosentti**-kentän arvot.</span><span class="sxs-lookup"><span data-stu-id="23a94-122">The **Total Balance** field totals the **Allocation Percentage** field for automatic account lines in a posting group.</span></span> <span data-ttu-id="23a94-123">Jos kirjausryhmän kokonaiskohdistusprosentti ei ole nolla, nimikkeen kirjauksen yhteydessä näytetään virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="23a94-123">If the total allocation percent for a posting group does not balance to zero, an error message will be displayed when the item is posted.</span></span>  

5.  <span data-ttu-id="23a94-124">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="23a94-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="23a94-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="23a94-125">See Also</span></span>  
 <span data-ttu-id="23a94-126">[Automaattiset tilikoodit](automatic-account-codes.md) </span><span class="sxs-lookup"><span data-stu-id="23a94-126">[Automatic Account Codes](automatic-account-codes.md) </span></span>  
 [<span data-ttu-id="23a94-127">Kirjausryhmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="23a94-127">Setting Up Posting Groups</span></span>](../../finance-posting-groups.md)  
 [<span data-ttu-id="23a94-128">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="23a94-128">Finance</span></span>](../../finance.md)
