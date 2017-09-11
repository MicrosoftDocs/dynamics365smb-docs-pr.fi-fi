---
title: Financialsin tukemat toimitusketjun toiminnot| Microsoft Docs
description: "Tässä ohjeaiheessa on tuotteen yleiskuvaus sekä lisätietoja ERP-ratkaisuun sisältyvistä tärkeistä toimitusketjun käsitteistä ja prosesseista."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product overview, ERP
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 3bae84075dc505aa9318590b1fac06e4844ffafe
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2017

---
# <a name="overview-of-supply-chain-functionality"></a><span data-ttu-id="7f237-103">Toimitusketjun toimintojen yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="7f237-103">Overview of Supply Chain Functionality</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="7f237-104"> tukee yleisiä toimitusketjun prosesseja, mutta se on rajoitettu tukku- ja jakeluyritysten tarpeisiin ilman hallittua varastonkäsittelyä.</span><span class="sxs-lookup"><span data-stu-id="7f237-104"> supports common supply chain processes, although limited to the needs of wholesale and distribution companies without managed warehouse handling.</span></span>

<span data-ttu-id="7f237-105">Myyntilaskuasiakirjojen lisäksi voit hallita tilausten toteutumista myyntitilausten kanssa, joka mahdollistaa osittaisten tilausmäärien toimittamisen, esimerkiksi silloin, kun täysi määrä ei ole heti saatavilla.</span><span class="sxs-lookup"><span data-stu-id="7f237-105">In addition to sales invoice documents, you can manage your order fulfillment with sales orders allowing you to ship parts of an order quantity, for example, because the full quantity is not available at once.</span></span> <span data-ttu-id="7f237-106">Voit valita nimikkeille suoratoimituksen toimittajalta asiakkaalle yhdistämällä myyntitilauksen liittyvään ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="7f237-106">You can have items drop shipped directly from a vendor to a customer by linking the sales order to the related purchase order.</span></span>

<span data-ttu-id="7f237-107">Varastosaldot päivitetään dynaamisesti nimikkeitä myytäessä ja ostettaessa, ja saatavuustiedot tai -varoitukset näytetään myyjille monin tavoin.</span><span class="sxs-lookup"><span data-stu-id="7f237-107">Your inventory quantities are dynamically updated as you sell and buy items, and availability information or warnings are shown to sales people in several ways.</span></span> <span data-ttu-id="7f237-108">Voit oikaista varastosaldot manuaalisesti tekemällä suoran kirjauksen nimiketapahtumiin, esimerkiksi inventoinnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="7f237-108">You can adjust inventory quantities manually by posting directly to the item ledger entries, for example, after a physical count.</span></span> <span data-ttu-id="7f237-109">Voit tarjota ja myydä nimikkeitä asiakkaillesi pitämättä niitä varastossa.</span><span class="sxs-lookup"><span data-stu-id="7f237-109">You can offer and sell items to your customers without maintaining inventory for them.</span></span> <span data-ttu-id="7f237-110">Jos haluat sisällyttää tällaiset ei-varastoitavat nimikkeet toimitusketjuusi, voit yksinkertaisesti muuntaa ne tavallisiksi nimikkeiksi.</span><span class="sxs-lookup"><span data-stu-id="7f237-110">If you want to include such nonstock items to your supply chain process, you simply convert them to normal items.</span></span>

<span data-ttu-id="7f237-111">Ostolaskuasiakirjojen lisäksi voit hallita toimituspuolta ostotilauksilla, jotka mahdollistavat osittaisten tuotemäärien vastaanottojen kirjaamisen.</span><span class="sxs-lookup"><span data-stu-id="7f237-111">In addition to purchase invoice documents, you can manage your supply side with purchase orders allowing you to record partial receipts of an order quantity.</span></span> <span data-ttu-id="7f237-112">Yksinkertaisella toimitusten suunnittelutoiminnolla voit aloittaa oston suoraan myyntilaskulta, jolle nimikkeet tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="7f237-112">A simple supply planning function allows you to initiate a purchase directly from the sales invoice that requires the items.</span></span>

<span data-ttu-id="7f237-113">Sekä myynti- että ostoasiakirjat voidaan kirjata joko toimitettuna tai vastaanotettuna, laskutettuna tai laskuttamattomana, jonka ansiosta voit jakaa tilauskäsittelijöiden ja kirjanpidon vastuita.</span><span class="sxs-lookup"><span data-stu-id="7f237-113">Both sales and purchase documents can be posted as shipped or received only or as shipped or received and invoiced, allowing you to split the responsibilities of order processors and accounting roles.</span></span>

<span data-ttu-id="7f237-114">Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.</span><span class="sxs-lookup"><span data-stu-id="7f237-114">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="7f237-115">Toiminta</span><span class="sxs-lookup"><span data-stu-id="7f237-115">To</span></span> | <span data-ttu-id="7f237-116">Katso</span><span class="sxs-lookup"><span data-stu-id="7f237-116">See</span></span> |
| --- | --- |
| <span data-ttu-id="7f237-117">Rekisteröi uusia asiakkaita, tee myyntitarjouksia, myy tuotteita tilauksilla tai laskuilla, kuten esimerkiksi suoratoimituksia, ja hallitse asiakaspalautuksia.</span><span class="sxs-lookup"><span data-stu-id="7f237-117">Register new customers, make sales offers, sell products on orders or invoices, for example as drop shipments, and manage sales returns.</span></span> |[<span data-ttu-id="7f237-118">Myynti</span><span class="sxs-lookup"><span data-stu-id="7f237-118">Sales</span></span>](sales-manage-sales.md) |
| <span data-ttu-id="7f237-119">Rekisteröi uusia toimittajia, osta nimikkeitä tilauksella tai laskulla, joka on esimerkiksi muodostettu myyntilaskusta, ja hallitse ostopalautuksia.</span><span class="sxs-lookup"><span data-stu-id="7f237-119">Register new vendors, purchase items on orders or invoices, for example initiated from a sales invoice, and manage purchase returns.</span></span> |[<span data-ttu-id="7f237-120">Osto</span><span class="sxs-lookup"><span data-stu-id="7f237-120">Purchasing</span></span>](purchasing-manage-purchasing.md) |
| <span data-ttu-id="7f237-121">Rekisteröi uusia fyysisiä tai palvelutuotteita, oikaise varastosaldoja ja hallitse varastoarvoa kirjaamalla oikaistut kustannukset pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="7f237-121">Register new physical or service products, adjust inventory quantities, and manage the inventory value by posting adjusted costs to the general ledger.</span></span> |[<span data-ttu-id="7f237-122">Varasto</span><span class="sxs-lookup"><span data-stu-id="7f237-122">Inventory</span></span>](inventory-manage-inventory.md) |

## <a name="see-also"></a><span data-ttu-id="7f237-123">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7f237-123">See Also</span></span>
[<span data-ttu-id="7f237-124">Myynnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7f237-124">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="7f237-125">[Myyntisaamisten hallinta](receivables-manage-receivables.md)   </span><span class="sxs-lookup"><span data-stu-id="7f237-125">[Managing Receivables](receivables-manage-receivables.md)   </span></span>  
[<span data-ttu-id="7f237-126">Ostojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7f237-126">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
<span data-ttu-id="7f237-127">[Ostovelkojen hallinta](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="7f237-127">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="7f237-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7f237-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="7f237-129">Yleiset liiketoimintatoiminnot</span><span class="sxs-lookup"><span data-stu-id="7f237-129">General Business Functionality</span></span>](ui-across-business-areas.md)

