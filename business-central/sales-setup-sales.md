---
title: Myyntiprosessien määritystehtävien yleiskatsaus | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan tehtävistä, joilla määritetään myyntikäytäntöjen ja -prosessien määrityksessä käytettävät säännöt ja arvot.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 06/17/2019
ms.author: sgroespe
ms.openlocfilehash: 3ece1edb7ba18cb96099cba34065c96164390e82
ms.sourcegitcommit: 6dc83b27ac47f3b39a7b84cfb7446e7f48b8ce63
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2019
ms.locfileid: "1632704"
---
# <a name="setting-up-sales"></a><span data-ttu-id="00623-103">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="00623-103">Setting Up Sales</span></span>
<span data-ttu-id="00623-104">Ennen myyntiprosessien hallinnan aloittamista on määritettävä yrityksen myyntikäytäntöjen säännöt ja arvot.</span><span class="sxs-lookup"><span data-stu-id="00623-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="00623-105">Ensin määritetään yleiset asetukset, kuten tarvittavat myyntiasiakirjat ja niiden arvojen kirjaustavat.</span><span class="sxs-lookup"><span data-stu-id="00623-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="00623-106">Nämä yleiset asetukset tehdään tavallisesti kerran alustavan käyttöönoton yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="00623-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="00623-107">Uusien asiakkaiden rekisteröintiin liittyy erillinen sarja tehtäviä, joilla kirjataan kunkin asiakkaan mahdolliset erikoishinta- tai alennussopimukset.</span><span class="sxs-lookup"><span data-stu-id="00623-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="00623-108">Maksumenetelmiä ja valuuttoja sekä muita rahoitukseen liittyviä myyntiasetuksia käsitellään Rahoituksen asetukset -osassa.</span><span class="sxs-lookup"><span data-stu-id="00623-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="00623-109">Lisätietoja on kohdassa [Rahoituksen määrittäminen](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="00623-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="00623-110">Toiminta</span><span class="sxs-lookup"><span data-stu-id="00623-110">To</span></span> | <span data-ttu-id="00623-111">Katso</span><span class="sxs-lookup"><span data-stu-id="00623-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="00623-112">Luo asiakkaan kortti jokaiselle asiakkaalle, jolle myyt.</span><span class="sxs-lookup"><span data-stu-id="00623-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="00623-113">Uusien asiakkaiden rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="00623-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="00623-114">Ota asiakkaille käyttöön mahdollisuus maksaa PayPalin kautta valitsemalla myyntiasiakirjoissa PayPalin logo.</span><span class="sxs-lookup"><span data-stu-id="00623-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="00623-115">Asiakkaan maksujen ottaminen käyttöön PayPalin kautta</span><span class="sxs-lookup"><span data-stu-id="00623-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="00623-116">Määritä asiakkaille myönnettävät alennukset ja erikoishinnat. Ne voivat perustua nimikkeeseen, määrään ja/tai päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="00623-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="00623-117">Myyntihinnan, alennuksen ja maksusopimusten tallentaminen</span><span class="sxs-lookup"><span data-stu-id="00623-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="00623-118">Määritä myyjät niin, että voit määrittää heidät asiakaskontakteille tai mitata myyjien suorituskykyä, kun myyntiprovisiota tai bonusta lasketaan.</span><span class="sxs-lookup"><span data-stu-id="00623-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="00623-119">Myyjien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="00623-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="00623-120">Määritä yksittäisille asiakkaille tai kaikille asiakkaille myyntiasiakirjojen oletusarvoinen lähetystapa valitsemalla **Kirjaa ja lähetä** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="00623-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="00623-121">Asiakirjan lähetysprofiilien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="00623-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="00623-122">Määritä sähköposti niin, että se sisältää lähetettävän myyntiasiakirjan yhteenvedon.</span><span class="sxs-lookup"><span data-stu-id="00623-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="00623-123">[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)</span><span class="sxs-lookup"><span data-stu-id="00623-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="00623-124">Tarkista ALV-rekisteröintinumero EU:n verkkopalvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="00623-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="00623-125">ALV-rekisterinumeroiden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="00623-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="00623-126">Määritä erilaiset incoterms-toimituslausekkeet, joita tarjoat asiakkaille tai joita toimittajat tarjoavat sinulle.</span><span class="sxs-lookup"><span data-stu-id="00623-126">Define the different incoterms that you offer to customers or that your vendors offer you.</span></span>|[<span data-ttu-id="00623-127">Toimitusehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="00623-127">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)|
|<span data-ttu-id="00623-128">Syötä käytettävien kuljetusliikkeiden tietoja, mukaan lukien linkki kuljetusliikkeiden kollinseurantapalveluun.</span><span class="sxs-lookup"><span data-stu-id="00623-128">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="00623-129">Kuljetusliikkeiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="00623-129">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="00623-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="00623-130">See Also</span></span>
[<span data-ttu-id="00623-131">Myynti</span><span class="sxs-lookup"><span data-stu-id="00623-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="00623-132">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="00623-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
