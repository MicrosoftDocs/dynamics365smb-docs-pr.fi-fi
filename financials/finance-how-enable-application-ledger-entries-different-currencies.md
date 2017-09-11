---
title: Eri valuutoissa olevien tapahtumien kohdistaminen| Microsoft Docs
description: "Jos asiakkaan maksu vastaanotetaan eri valuuttana kuin myytäessä käytetty valuutta, voidaan kirjanpitotapahtumat kohdistaa useana valuuttana."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 035f4c0e98e3b7ba308319c2017568de832e26c5
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="62702-103">Toimintaohje: Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa</span><span class="sxs-lookup"><span data-stu-id="62702-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="62702-104">Jos ostat toimittajalta yhdessä valuutassa ja maksat maksun toisessa valuutassa, maksu voidaan kohdistaa ostoon.</span><span class="sxs-lookup"><span data-stu-id="62702-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="62702-105">Ja jos asiakkaalle myydään yhdessä valuutassa ja maksu vastaanotetaan toisessa valuutassa, maksu voidaan kohdistaa myyntilaskuun.</span><span class="sxs-lookup"><span data-stu-id="62702-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="62702-106">Seuraavassa kuvataan, miten tämä määritetään toimittajatapahtumille **Ostojen ja ostovelkojen asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="62702-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="62702-107">Asetukset tehdään samoin kuin asiakastapahtumille **Myyntien ja myyntisaamisten asetukset** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="62702-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="62702-108">Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**.</span><span class="sxs-lookup"><span data-stu-id="62702-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="62702-109">Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="62702-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="62702-110">Toimittajatapahtumien kohdistamisen ottaminen käyttöön eri valuutoissa</span><span class="sxs-lookup"><span data-stu-id="62702-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="62702-111">Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Ostojen ostovelkojen asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="62702-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="62702-112">Valitse **Valuuttojen välinen kohdistus** -kentässä jokin seuraavista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="62702-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="62702-113">Asetus</span><span class="sxs-lookup"><span data-stu-id="62702-113">Option</span></span> | <span data-ttu-id="62702-114">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="62702-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="62702-115">Ei yhtään</span><span class="sxs-lookup"><span data-stu-id="62702-115">None</span></span> |<span data-ttu-id="62702-116">Valuuttojen välistä kohdistusta ei sallita.</span><span class="sxs-lookup"><span data-stu-id="62702-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="62702-117">EMU</span><span class="sxs-lookup"><span data-stu-id="62702-117">EMU</span></span> |<span data-ttu-id="62702-118">EMU-valuuttojen välinen kohdistus sallitaan.</span><span class="sxs-lookup"><span data-stu-id="62702-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="62702-119">Kaikki</span><span class="sxs-lookup"><span data-stu-id="62702-119">All</span></span> |<span data-ttu-id="62702-120">Kaikkien valuuttojen välinen kohdistus sallitaan.</span><span class="sxs-lookup"><span data-stu-id="62702-120">Application between all currencies is allowed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="62702-121">Katso myös</span><span class="sxs-lookup"><span data-stu-id="62702-121">See Also</span></span>
[<span data-ttu-id="62702-122">Ostovelkojen hallinta</span><span class="sxs-lookup"><span data-stu-id="62702-122">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="62702-123">Myyntisaamisten hallinta</span><span class="sxs-lookup"><span data-stu-id="62702-123">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="62702-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="62702-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

