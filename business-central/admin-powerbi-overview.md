---
title: Business Centralin Power BI -integrointiosa ja arkkitehtuurin yleiskatsaus | Microsoft Docs
description: Analyysitietojen, liiketoimintatietojen ja tunnuslukujen hakeminen Business Centralin tiedoista on helppoa Power BI:n Business Central -sovelluksia.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 23a0c72775dbddc89a81105de3b2ed79d1f09432
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753768"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a><span data-ttu-id="91574-103">[!INCLUDE[prod_short](includes/prod_short.md)]in Power BI -integrointiosa ja arkkitehtuurin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="91574-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="91574-104">Tässä artikkelissa käsitellään Power BI:n ja [!INCLUDE[prod_short](includes/prod_short.md)]in integrointia eri tavoin, mikä auttaa ymmärtämään sen toteutusta ja käyttöä.</span><span class="sxs-lookup"><span data-stu-id="91574-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prod_short](includes/prod_short.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="91574-105">Komponentit</span><span class="sxs-lookup"><span data-stu-id="91574-105">Components</span></span>

<span data-ttu-id="91574-106">Seuraavassa taulukossa käsitellään Power BI -integraation keskeisiä komponentteja.</span><span class="sxs-lookup"><span data-stu-id="91574-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="91574-107">Komponentti</span><span class="sxs-lookup"><span data-stu-id="91574-107">Component</span></span>|<span data-ttu-id="91574-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="91574-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="91574-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="91574-109">Power BI</span></span>|<span data-ttu-id="91574-110">Pilvipohjaisen raportoinnin isännöinti- ja hallintapalvelu.</span><span class="sxs-lookup"><span data-stu-id="91574-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="91574-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="91574-111">Power BI Desktop</span></span>|<span data-ttu-id="91574-112">Raporttien ja koontinäyttöjen luontityökalu, jolla voi suorittaa raportteja.</span><span class="sxs-lookup"><span data-stu-id="91574-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="91574-113">Sen voi ladata maksutta Microsoft Storesta ja se asennetaan paikallisesti.</span><span class="sxs-lookup"><span data-stu-id="91574-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prod_short](includes/prod_short.md)]|<span data-ttu-id="91574-114">Online- tai paikallinen ratkaisu yhdistimineen on näkyvissä Power BI:ssa ja mahdollistaa Power BI -osan upotuksen.</span><span class="sxs-lookup"><span data-stu-id="91574-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="91574-115">Käytettävissä heti</span><span class="sxs-lookup"><span data-stu-id="91574-115">What's available from the start</span></span>

<span data-ttu-id="91574-116">Seuraavassa taulukossa käsitellään käytettävissä olevat ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="91574-116">The following table describes available features.</span></span>

|<span data-ttu-id="91574-117">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="91574-117">Feature</span></span>|[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="91574-118">online- tai paikallisen version tuki</span><span class="sxs-lookup"><span data-stu-id="91574-118">online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="91574-119">Power BI -yhdistimet</span><span class="sxs-lookup"><span data-stu-id="91574-119">Power BI connectors</span></span>|<span data-ttu-id="91574-120">Molemmat.</span><span class="sxs-lookup"><span data-stu-id="91574-120">Both.</span></span> <span data-ttu-id="91574-121">Online- ja paikallisessa versioilla eri liittimet.</span><span class="sxs-lookup"><span data-stu-id="91574-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="91574-122">Samaa yhdistintä käytetään Power BI Desktopissa ja Power BI -palvelussa</span><span class="sxs-lookup"><span data-stu-id="91574-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="91574-123">Tietyn raportin upotettu tarkastelukokemus [!INCLUDE[prod_short](includes/prod_short.md)]in tietoruudussa</span><span class="sxs-lookup"><span data-stu-id="91574-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="91574-124">Molemmat.</span><span class="sxs-lookup"><span data-stu-id="91574-124">Both.</span></span> <span data-ttu-id="91574-125">Edellyttää paikallisen version raporttien näyttämisen määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="91574-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="91574-126">Power BI -raportin hallinta [!INCLUDE[prod_short](includes/prod_short.md)]issa</span><span class="sxs-lookup"><span data-stu-id="91574-126">Power BI report management from [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="91574-127">Online</span><span class="sxs-lookup"><span data-stu-id="91574-127">Online</span></span>|
|<span data-ttu-id="91574-128">Power BI:ssa näkyvät roolikeskusten Power BI -oletusraportit</span><span class="sxs-lookup"><span data-stu-id="91574-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="91574-129">Online</span><span class="sxs-lookup"><span data-stu-id="91574-129">Online</span></span>|
|<span data-ttu-id="91574-130">Power BI -sovellukset Microsoft AppSourcessa</span><span class="sxs-lookup"><span data-stu-id="91574-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="91574-131">Online.</span><span class="sxs-lookup"><span data-stu-id="91574-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="91574-132">Arkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="91574-132">Architecture</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="91574-133">integroidaan Power BI:n kanssa ODataa käyttävällä yhdistimellä.</span><span class="sxs-lookup"><span data-stu-id="91574-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="91574-134">Power BI -raporttien tietolähde näkyy OData-verkkopalveluina.</span><span class="sxs-lookup"><span data-stu-id="91574-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Power BI:n ja Business Centralin integrointiarkkitehtuuri](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="91574-136">Yleinen työnkulku</span><span class="sxs-lookup"><span data-stu-id="91574-136">General Flow</span></span>

<span data-ttu-id="91574-137">Seuraava kaavio näyttää käyttäjien perustyönkulun yhdistettäessä [!INCLUDE[prod_short](includes/prod_short.md)] Power BI:hin.</span><span class="sxs-lookup"><span data-stu-id="91574-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prod_short](includes/prod_short.md)] to Power BI.</span></span>

![Power BI:n ja Business Centralin integroinnin työnkulku](./media/power-bi-flow.png)

1. <span data-ttu-id="91574-139">Käyttää rekisteröityy Power BI -tilille.</span><span class="sxs-lookup"><span data-stu-id="91574-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="91574-140">Käyttää muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]sta Power BI:hin.</span><span class="sxs-lookup"><span data-stu-id="91574-140">User connects to Power BI from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
3. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="91574-141">tarkistaa käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="91574-141">verifies the license.</span></span>
4. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="91574-142">ottaa oletusraportit käyttöön Power BI -palvelussa.</span><span class="sxs-lookup"><span data-stu-id="91574-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="91574-143">Tämä vaihe tehdään vain [!INCLUDE[prod_short](includes/prod_short.md)] online -versiossa.</span><span class="sxs-lookup"><span data-stu-id="91574-143">This step only happens for [!INCLUDE[prod_short](includes/prod_short.md)] online.</span></span>
5. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="91574-144">tuo Power BI -raportit valittaviksi [!INCLUDE[prod_short](includes/prod_short.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="91574-144">makes reports in Power BI available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="91574-145">Oletusraportit näytetään automaattisesti Power BI -osissa.</span><span class="sxs-lookup"><span data-stu-id="91574-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="91574-146">Käyttäjä luo raportin Power BI Desktopissa.</span><span class="sxs-lookup"><span data-stu-id="91574-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="91574-147">Käyttäjä julkaisee raportin Power BI -palveluun.</span><span class="sxs-lookup"><span data-stu-id="91574-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="91574-148">Raportit ovat sitten valittavissa [!INCLUDE[prod_short](includes/prod_short.md)]issa.</span><span class="sxs-lookup"><span data-stu-id="91574-148">The reports are then available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="91574-149">Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="91574-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="91574-150">Katso myös</span><span class="sxs-lookup"><span data-stu-id="91574-150">See Also</span></span>

[<span data-ttu-id="91574-151">Business Central ja Power BI</span><span class="sxs-lookup"><span data-stu-id="91574-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="91574-152">Power BI kuluttajille</span><span class="sxs-lookup"><span data-stu-id="91574-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="91574-153">Power BI -palvelun uusi ulkoasu</span><span class="sxs-lookup"><span data-stu-id="91574-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="91574-154">Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin</span><span class="sxs-lookup"><span data-stu-id="91574-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="91574-155">Power BI -dokumentaatio</span><span class="sxs-lookup"><span data-stu-id="91574-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="91574-156">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="91574-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="91574-157">Käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="91574-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="91574-158">Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä</span><span class="sxs-lookup"><span data-stu-id="91574-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="91574-159">[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)</span><span class="sxs-lookup"><span data-stu-id="91574-159">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
<span data-ttu-id="91574-160">[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="91574-160">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="91574-161">[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Apps:n tietolähteenä](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="91574-161">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="91574-162">[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Automate'ssa](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="91574-162">[Using [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
