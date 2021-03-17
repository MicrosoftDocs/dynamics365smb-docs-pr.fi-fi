---
title: Rakennetiedot – Varaston arvostus | Microsoft Docs
description: Varaston arvostus on varastonimikkeen kustannusten määrittäminen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 497c2fb891af31af20a6b7a150edd9a9907748e2
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389847"
---
# <a name="design-details-inventory-valuation"></a><span data-ttu-id="3590d-103">Rakennetiedot: varaston arvostus</span><span class="sxs-lookup"><span data-stu-id="3590d-103">Design Details: Inventory Valuation</span></span>
<span data-ttu-id="3590d-104">Varaston arvostus on varastonimikkeeseen kohdistettu kustannuksen määritys seuraavan yhtälön mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="3590d-104">Inventory valuation is the determination of the cost that is assigned to an inventory item, as expressed by the following equation.</span></span>  

<span data-ttu-id="3590d-105">Varasto lopussa = varasto alussa + netto-ostot – myytyjen tuotteiden kustannus</span><span class="sxs-lookup"><span data-stu-id="3590d-105">Ending inventory = beginning inventory + net purchases – cost of goods sold</span></span>  

<span data-ttu-id="3590d-106">Varastoarvon laskelma käyttää nimikkeiden kirjausten **Kustannussumma (tämänhetkinen)** -kenttää nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="3590d-106">The calculation of inventory valuation uses the **Cost Amount (Actual)** field of the value entries for the item.</span></span> <span data-ttu-id="3590d-107">Kirjaukset luokitellaan kirjaustyypin mukaan, joka vastaa kustannusosia, välittömiä kustannuksia, välillisiä kustannuksia, varianssia, uudelleenarvostusta ja pyöristystä.</span><span class="sxs-lookup"><span data-stu-id="3590d-107">The entries are classified according to the entry type that corresponds to the cost components, direct cost, indirect cost, variance, revaluation, and rounding.</span></span> <span data-ttu-id="3590d-108">Katso lisätietoja kohdasta [Rakennetiedot: kustannuskomponentit](design-details-cost-components.md).</span><span class="sxs-lookup"><span data-stu-id="3590d-108">For more information, see [Design Details: Cost Components](design-details-cost-components.md).</span></span>  

<span data-ttu-id="3590d-109">Tapahtumia käytetään toisiaan vastaan, joko kiinteällä kohdistuksella tai yleisen arvostusmenetelmän määrittämän kustannusvirtaoletuksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="3590d-109">Entries are applied against each other, either by the fixed application or according to the general cost-flow assumption defined by the costing method.</span></span> <span data-ttu-id="3590d-110">Yksi varaston arvon vähennystapahtuma voidaan kohdistaa useampaan kuin yhteen nousutapahtumaan erilaisilla kirjauspäivämäärillä ja mahdollisesti erilaisilla hankintakustannuksilla.</span><span class="sxs-lookup"><span data-stu-id="3590d-110">One entry of inventory decrease can be applied to more than one increase entry with different posting dates and possibly different acquisition costs.</span></span> <span data-ttu-id="3590d-111">Katso lisätiedot kohdasta [Rakennetiedot: nimikkeen kohdistus](design-details-item-application.md).</span><span class="sxs-lookup"><span data-stu-id="3590d-111">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span> <span data-ttu-id="3590d-112">Tämän vuoksi varastoarvon laskenta tiettynä päivänä perustuu positiivisten ja negatiivisten arvotapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="3590d-112">Therefore, calculation of the inventory value for a given date is based on summing up positive and negative value entries.</span></span>  

## <a name="inventory-valuation-report"></a><span data-ttu-id="3590d-113">Varaston arvostusraportti</span><span class="sxs-lookup"><span data-stu-id="3590d-113">Inventory Valuation report</span></span>  
<span data-ttu-id="3590d-114">Kun **Varaston arvostus** -raportin varaston arvoa lasketaan, raportti laskee ensin nimikkeen varaston arvon annettuna alkupäivämääränä.</span><span class="sxs-lookup"><span data-stu-id="3590d-114">To calculate the inventory value in the **Inventory Valuation** report, the report begins by calculating the value of the item’s inventory at a given starting date.</span></span> <span data-ttu-id="3590d-115">Se lisää tämän jälkeen varaston arvon kasvatukset ja vähentää varaston arvon vähennykset annettuun lopetuspäivämäärään asti.</span><span class="sxs-lookup"><span data-stu-id="3590d-115">It then adds the value of inventory increases and subtracts the value of inventory decreases up to a given ending date.</span></span> <span data-ttu-id="3590d-116">Lopputulos on varaston arvo päättymispäivänä.</span><span class="sxs-lookup"><span data-stu-id="3590d-116">The end result is the inventory value on the ending date.</span></span> <span data-ttu-id="3590d-117">Raportti laskee nämä arvot laskemalla yhteen arvot **Kustannussumma (nykyinen)** -kentän arvokirjauksissa käyttäen tiliöintipäiviä suodattimina.</span><span class="sxs-lookup"><span data-stu-id="3590d-117">The report calculates these values by summing the values in the **Cost Amount (Actual)** field in the value entries, using the posting dates as filters.</span></span>  

<span data-ttu-id="3590d-118">Tulostetussa raportissa näkyvät aina todelliset summat eli niiden tapahtumien kustannukset, jotka on kirjattu laskutetuiksi.</span><span class="sxs-lookup"><span data-stu-id="3590d-118">The printed report always shows actual amounts, that is, the cost of entries that have been posted as invoiced.</span></span> <span data-ttu-id="3590d-119">Raporttiin tulostuvat myös niiden tapahtumien oletetut kustannukset, jotka on kirjattu vastaanotetuiksi tai toimitetuiksi, jos lisäät valintamerkin Vaihtoehdot-pikavälilehden Sisällytä oletetut kustann. -kenttään.</span><span class="sxs-lookup"><span data-stu-id="3590d-119">The report will also print the expected cost of entries that have posted as received or shipped, if you select the Include Expected Cost field on the Options FastTab.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="3590d-120">**Varaston arvostus** -raportin arvot on täsmäytetty pääkirjanpidon varastotiliin. Tämä tarkoittaa sitä, että kyseiset arvotapahtumat on kirjattu pääkirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="3590d-120">Values in the **Inventory Valuation** report is reconciled with the Inventory account in the general ledger, meaning the value entries in question have been posted to the general ledger.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="3590d-121">Määrät raportin **Arvo**-sarakkeessa perustuvat nimikkeen tapahtumien kirjauspäivämäärään.</span><span class="sxs-lookup"><span data-stu-id="3590d-121">Amounts in the **Value** columns of the report are based on the posting date of transactions for an item.</span></span>  

## <a name="inventory-valuation---wip-report"></a><span data-ttu-id="3590d-122">Varaston arvostus - KET-raportti</span><span class="sxs-lookup"><span data-stu-id="3590d-122">Inventory Valuation - WIP report</span></span>  
<span data-ttu-id="3590d-123">Tuotantoyrityksen on märitettävä kolmenlaisen varaston arvo:</span><span class="sxs-lookup"><span data-stu-id="3590d-123">A manufacturing company needs to determine the value of three types of inventory:</span></span>  

* <span data-ttu-id="3590d-124">Raaka-ainevarasto</span><span class="sxs-lookup"><span data-stu-id="3590d-124">Raw Materials inventory</span></span>  
* <span data-ttu-id="3590d-125">KET-varasto</span><span class="sxs-lookup"><span data-stu-id="3590d-125">WIP inventory</span></span>  
* <span data-ttu-id="3590d-126">Valmiiden tuotteiden varasto</span><span class="sxs-lookup"><span data-stu-id="3590d-126">Finished Goods inventory</span></span>  

<span data-ttu-id="3590d-127">KET-varaston arvo määritetään seuraavan laskutoimituksen avulla:</span><span class="sxs-lookup"><span data-stu-id="3590d-127">The value of WIP inventory is determined by the following equation:</span></span>  

* <span data-ttu-id="3590d-128">KET-varasto lopussa = KET-varasto alussa + valmistuskustannukset – valmistettujen tuotteiden kustannus</span><span class="sxs-lookup"><span data-stu-id="3590d-128">Ending WIP inventory = Beginning WIP inventory + manufacturing costs – cost of goods manufactured</span></span>  

<span data-ttu-id="3590d-129">Ostetun varaston osalta arvotapahtumat tarjoavat varaston arvostuksen perustan.</span><span class="sxs-lookup"><span data-stu-id="3590d-129">As for purchased inventory, the value entries provide the basis of the inventory valuation.</span></span> <span data-ttu-id="3590d-130">Laskelma tehdään käyttämällä arvoja nimikkeen **Kustannussumma (tämänhetkinen)** -kentässä sekä kapasiteettiarvon kirjauksia, jotka liittyvät tuotantotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="3590d-130">The calculation is made using the values in the **Cost Amount (Actual)** field of the item and capacity value entries associated with a production order.</span></span>  

<span data-ttu-id="3590d-131">WIP-varaston arvostuksen tarkoituksena on määritellä niiden nimikkeiden arvo, joiden valmistus ei ole päättynyt annetulla päivämäärällä.</span><span class="sxs-lookup"><span data-stu-id="3590d-131">The purpose of WIP inventory valuation is to determine the value of the items whose manufacturing has not yet been completed on a given date.</span></span> <span data-ttu-id="3590d-132">Tämän vuoksi KET-varaston arvo perustuu kulutukseen ja kapasiteettitapahtumiin liittyviin arvotapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="3590d-132">Therefore the WIP inventory value is based on the value entries related to the consumption and capacity ledger entries.</span></span> <span data-ttu-id="3590d-133">Kulutustapahtumat on laskutettava kokonaan arvostuspäivänä.</span><span class="sxs-lookup"><span data-stu-id="3590d-133">Consumption ledger entries must be completely invoiced at the date of the valuation.</span></span> <span data-ttu-id="3590d-134">Tämän vuoksi **Varaston arvostus - KET** -raportissa näkyvät KET-varaston arvon osoittavat kustannukset kahdessa luokassa, jotka ovat kulutus ja kapasiteetti.</span><span class="sxs-lookup"><span data-stu-id="3590d-134">Therefore, the **Inventory Valuation – WIP** report shows the costs representing the WIP inventory value in two categories: consumption and capacity.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3590d-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3590d-135">See Also</span></span>  
<span data-ttu-id="3590d-136">[Rakennetiedot: Täsmäytys pääkirjanpidon kanssa](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="3590d-136">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
<span data-ttu-id="3590d-137">[Rakennetiedot: uudelleenarvostus](design-details-revaluation.md) </span><span class="sxs-lookup"><span data-stu-id="3590d-137">[Design Details: Revaluation](design-details-revaluation.md) </span></span>  
<span data-ttu-id="3590d-138">[Rakennetiedot: Tuotantotilauksen kirjaus](design-details-production-order-posting.md)
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="3590d-138">[Design Details: Production Order Posting](design-details-production-order-posting.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
[<span data-ttu-id="3590d-139">Rahoitus</span><span class="sxs-lookup"><span data-stu-id="3590d-139">Finance</span></span>](finance.md)  
<span data-ttu-id="3590d-140">[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3590d-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]