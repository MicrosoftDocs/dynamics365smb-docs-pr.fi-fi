---
title: "Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen | Microsoft Docs"
description: "Lisätietoja kustannustyypin ja kirjanpitotilin välisen suhteen määrittämisestä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f30b8b56ae4afcff230a7934a6bcac4d205db
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a><span data-ttu-id="4f5af-103">Pääkirjanpitotilien ja kustannustyyppien välisen suhteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4f5af-103">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>
<span data-ttu-id="4f5af-104">Kustannustyypin ja KP-tilin välinen suhde luodaan kustannustyypissä ja KP-tilillä.</span><span class="sxs-lookup"><span data-stu-id="4f5af-104">The relationship between the cost type and the general ledger account is created in the cost type and in the general ledger account.</span></span>  

* <span data-ttu-id="4f5af-105">**Kustannustyyppi**-taulukon **KP-tilien väli** -kenttä osoittaa, mitkä KP-tilit kuuluvat millekin kustannustyypille.</span><span class="sxs-lookup"><span data-stu-id="4f5af-105">The **G/L Account Range** field in the **Cost Type** table establishes which general ledger accounts belong to a cost type.</span></span>  
* <span data-ttu-id="4f5af-106">**Saldokustannustyypin numero** -kenttä</span><span class="sxs-lookup"><span data-stu-id="4f5af-106">The **Cost Type No.**</span></span> <span data-ttu-id="4f5af-107">tilikartassa osoittaa, mitkä KP-tilit kuuluvat millekin kustannustyypille.</span><span class="sxs-lookup"><span data-stu-id="4f5af-107">field in the chart of accounts establishes which cost type a general ledger account belongs to.</span></span>  

<span data-ttu-id="4f5af-108">Nämä kaksi kenttää täytetään automaattisesti, kun käytät **Hae kustannustyypit tilikartasta** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="4f5af-108">These two fields are filled automatically when you use the **Get Cost Types from Chart of Accounts** function.</span></span>  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a><span data-ttu-id="4f5af-109">Pääkirjanpitotilien ja kustannustyyppien välinen suhde.</span><span class="sxs-lookup"><span data-stu-id="4f5af-109">Relationship Between General Ledger Accounts and Cost Types</span></span>  
<span data-ttu-id="4f5af-110">Pääkirjanpitotilien ja kustannustyyppien välissä on olemassa n:1-suhde.</span><span class="sxs-lookup"><span data-stu-id="4f5af-110">There is an n:1 relationship between general ledger accounts and cost types.</span></span> <span data-ttu-id="4f5af-111">Useita pääkirjanpitotilejä voi kuulua yhdelle kustannustyypille, mutta jokainen pääkirjanpitotili kuuluu vain yhdelle kustannustyypille.</span><span class="sxs-lookup"><span data-stu-id="4f5af-111">Several general ledger accounts can belong to one cost type, but each general ledger account belongs to only one cost type.</span></span> <span data-ttu-id="4f5af-112">Seuraava taulukko kuvaa suhteen yksityiskohtia.</span><span class="sxs-lookup"><span data-stu-id="4f5af-112">The following table describes the details in the relationship.</span></span>  

|<span data-ttu-id="4f5af-113">Suhde</span><span class="sxs-lookup"><span data-stu-id="4f5af-113">Relationship</span></span>|<span data-ttu-id="4f5af-114">**KP-tilien väli**</span><span class="sxs-lookup"><span data-stu-id="4f5af-114">**G/L Account Range**</span></span>|<span data-ttu-id="4f5af-115">**Kustannustyypin numero**</span><span class="sxs-lookup"><span data-stu-id="4f5af-115">**Cost Type No.**</span></span>|  
|------------------|------------------------------------------------|-------------------------------------------|  
|<span data-ttu-id="4f5af-116">Yksi pääkirjanpidon tilin kullekin kustannustyypille</span><span class="sxs-lookup"><span data-stu-id="4f5af-116">One general ledger account for each cost type</span></span>|<span data-ttu-id="4f5af-117">kirjanpitotili.</span><span class="sxs-lookup"><span data-stu-id="4f5af-117">One general ledger account</span></span>|<span data-ttu-id="4f5af-118">Yksi kustannuslaji</span><span class="sxs-lookup"><span data-stu-id="4f5af-118">One cost type</span></span>|  
|<span data-ttu-id="4f5af-119">Useita kirjanpitotilejä yhdelle kustannustyypille</span><span class="sxs-lookup"><span data-stu-id="4f5af-119">Several general ledger accounts for one cost type</span></span>|<span data-ttu-id="4f5af-120">Kirjanpitotiliväli, kuten 7110–7193 jokaisen kirjanpitotilin kohdalla</span><span class="sxs-lookup"><span data-stu-id="4f5af-120">General ledger account range, for example, 7110..7193 for each general ledger account</span></span>|<span data-ttu-id="4f5af-121">Alueen kaikille pääkirjanpidon tileillä on vain yksi kustannustyyppi</span><span class="sxs-lookup"><span data-stu-id="4f5af-121">For each general ledger account in the range, there is only one cost type</span></span>|  
|<span data-ttu-id="4f5af-122">Kustannustyypit ilman vastaavia pääkirjanpitotilejä</span><span class="sxs-lookup"><span data-stu-id="4f5af-122">Cost types without corresponding general ledger accounts</span></span>|<Empty>||  
|<span data-ttu-id="4f5af-123">Kirjanpitotilit, joiden tapahtumia ei siirretä</span><span class="sxs-lookup"><span data-stu-id="4f5af-123">General ledger accounts whose entries will not be transferred</span></span>||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a><span data-ttu-id="4f5af-124">Kustannustyypit ilman suhdetta pääkirjanpitoon</span><span class="sxs-lookup"><span data-stu-id="4f5af-124">Cost Types Without a Relationship to the General Ledger</span></span>  
<span data-ttu-id="4f5af-125">Kustannuksen tyypillä ei ehkä ole yhteyttä pääkirjanpidon tileille, jos jokin seuraavista ehdoista toteutuu:</span><span class="sxs-lookup"><span data-stu-id="4f5af-125">A cost type may not have a relationship to general ledger accounts if one of the following conditions is true:</span></span>  

* <span data-ttu-id="4f5af-126">Operatiivisen kirjanpidon tilit, kuten kortin laskenta ja poistot, ottavat kustannukset vain operatiivisesta kirjanpidosta.</span><span class="sxs-lookup"><span data-stu-id="4f5af-126">Accounts for operational accounting, such as Calc. Interest and Depreciation, only take costs from the operational accounting.</span></span>  
* <span data-ttu-id="4f5af-127">Auttavia kustannustyyppejä, kuten [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa olevia tyyppejä 9901, 9902 ja 9903, käytetään kredit- ja debet-tileinä kohdistuksissa.</span><span class="sxs-lookup"><span data-stu-id="4f5af-127">Helping cost types, such as cost types 9901, 9902, and 9903 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, are used as credit and debit accounts for allocations.</span></span>  
* <span data-ttu-id="4f5af-128">Auttava tili, 9920 [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietokannassa, sisältää todellisia kertymiä, jotka näyttävät kustannusten ja KP-kulujen eron.</span><span class="sxs-lookup"><span data-stu-id="4f5af-128">The helping account, 9920 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, contains actual accruals that show the difference between costs and the expense from the general ledger.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4f5af-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="4f5af-129">See Also</span></span>  
[<span data-ttu-id="4f5af-130">Kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="4f5af-130">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="4f5af-131">[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="4f5af-131">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
[<span data-ttu-id="4f5af-132">Tietoja kustannuslaskennasta</span><span class="sxs-lookup"><span data-stu-id="4f5af-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="4f5af-133">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4f5af-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

