---
title: Ostojen määritystehtävien yleiskatsaus | Microsoft Docs
description: Ohjeaiheessa kerrotaan tehtävistä, joilla määritetään yrityksen hallintakäytäntöjä, ja määritetään ostoprosessit.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9d0058c707862144592278d08a494175adf67a2a
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115434"
---
# <a name="setting-up-purchasing"></a><span data-ttu-id="01a53-103">Ostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="01a53-103">Setting Up Purchasing</span></span>
<span data-ttu-id="01a53-104">Ennen ostoprosessien hallinnan aloittamista on määritettävä yrityksen ostokäytäntöjen säännöt ja arvot.</span><span class="sxs-lookup"><span data-stu-id="01a53-104">Before you can manage purchase processes, you must configure the rules and values that define the company's purchase policies.</span></span>

<span data-ttu-id="01a53-105">Yleiset asetukset on määritettävä. Yleisiä asetuksia ovat esimerkiksi se, mitä ostoasiakirjoja tarvitaan ja miten niiden arvot kirjataan.</span><span class="sxs-lookup"><span data-stu-id="01a53-105">You must define the general setup, such as which purchase documents are required and how their values are posted.</span></span> <span data-ttu-id="01a53-106">Nämä yleiset asetukset tehdään tavallisesti kerran alustavan käyttöönoton yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="01a53-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="01a53-107">Uusien toimittajien rekisteröintiin liittyy erillinen sarja tehtäviä, joilla kirjataan kunkin toimittajan mahdolliset erikoishinta- tai alennussopimukset.</span><span class="sxs-lookup"><span data-stu-id="01a53-107">A separate series of tasks related to registering new vendors is to record any special price or discount agreements that you have with each vendor.</span></span>

<span data-ttu-id="01a53-108">Maksumenetelmiä ja valuuttoja sekä muita rahoitukseen liittyviä ostoasetuksia käsitellään Rahoituksen asetukset -osassa.</span><span class="sxs-lookup"><span data-stu-id="01a53-108">Finance-related purchase setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="01a53-109">Lisätietoja on kohdassa [Rahoituksen määrittäminen](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="01a53-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="01a53-110">Toiminta</span><span class="sxs-lookup"><span data-stu-id="01a53-110">To</span></span> | <span data-ttu-id="01a53-111">Katso</span><span class="sxs-lookup"><span data-stu-id="01a53-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="01a53-112">Toimittajan kortin luominen kullekin toimittajalle, jolta ostetaan</span><span class="sxs-lookup"><span data-stu-id="01a53-112">Create a vendor card for each vendor that you purchase from</span></span>|[<span data-ttu-id="01a53-113">Uusien toimittajien rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="01a53-113">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md) |
| <span data-ttu-id="01a53-114">Toimittajien nimikkeiden, määrien ja/tai päivämäärien perusteella myöntäminen eri alennusten ja erikoishintojen antaminen</span><span class="sxs-lookup"><span data-stu-id="01a53-114">Enter the different discounts and special prices that vendors grant you depending on item, quantities, and/or date</span></span> |[<span data-ttu-id="01a53-115">Ostohinnan, alennuksen ja maksusopimusten tallentaminen</span><span class="sxs-lookup"><span data-stu-id="01a53-115">Record Purchase Price, Discount, and Payment Agreements</span></span>](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| <span data-ttu-id="01a53-116">Toimittajien priorisointi</span><span class="sxs-lookup"><span data-stu-id="01a53-116">Prioritize vendors</span></span> |[<span data-ttu-id="01a53-117">Toimittajien priorisointi</span><span class="sxs-lookup"><span data-stu-id="01a53-117">Prioritize Vendors</span></span>](purchasing-how-prioritize-vendors.md) |
| <span data-ttu-id="01a53-118">Ostajien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="01a53-118">Set up purchasers</span></span> |[<span data-ttu-id="01a53-119">Ostajien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="01a53-119">Set Up Purchasers</span></span>](purchasing-how-setup-purchasers.md) |
|<span data-ttu-id="01a53-120">Määritä oletusraportteja, joita käytetään eri asiakirjatyypeille.</span><span class="sxs-lookup"><span data-stu-id="01a53-120">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="01a53-121">Raporttien valinta Business Centralissa</span><span class="sxs-lookup"><span data-stu-id="01a53-121">Report Selection in Business Central</span></span>](across-report-selections.md)|

> [!TIP]
> <span data-ttu-id="01a53-122">Maantieteellinen sijaintisi mukaan jotkin sivut voivat sisältää kenttiä, joita ei ole kuvattu tässä luettelossa, koska ne koskevat paikallisia toimintoja tai mukautuksia.</span><span class="sxs-lookup"><span data-stu-id="01a53-122">Depending on your geographical location, some pages can contain fields that are not described in the articles that are listed here because they apply to local functionality or customizations.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="external-document-number"></a><span data-ttu-id="01a53-123">Ulkoisen tiedoston numero</span><span class="sxs-lookup"><span data-stu-id="01a53-123">External document number</span></span>

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="01a53-124">Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="01a53-124">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="01a53-125">Katso myös</span><span class="sxs-lookup"><span data-stu-id="01a53-125">See Also</span></span>

[<span data-ttu-id="01a53-126">Osto</span><span class="sxs-lookup"><span data-stu-id="01a53-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="01a53-127">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="01a53-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]