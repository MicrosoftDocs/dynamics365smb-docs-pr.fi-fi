---
title: Uuden yrityksen luominen | Microsoft Docs
description: RapidStart Servicesin käyttämisessä tarvittavat taulukot ja sivut luodaan, mutta niissä ei ole tietoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7583837e515a4fd5fb415fe1b482512e7edf6b5a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753994"
---
# <a name="create-a-new-company"></a><span data-ttu-id="345a2-103">Uuden yrityksen luominen</span><span class="sxs-lookup"><span data-stu-id="345a2-103">Create a New Company</span></span>
<span data-ttu-id="345a2-104">Kun haluat käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in RapidStart Servicesia, luo ensin uusi yritys, jossa asiakkaan käyttöönotto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="345a2-104">To use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="345a2-105">Kun luot uuden yhtiön, standardi [!INCLUDE[prod_short](includes/prod_short.md)] -taulukot ja sivut luodaan, mutta niissä ei ole tietoja.</span><span class="sxs-lookup"><span data-stu-id="345a2-105">When you create a new company, the standard [!INCLUDE[prod_short](includes/prod_short.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="345a2-106">Voit lisäksi ottaa yrityksessä käyttöön tietyt asetustiedot alustamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="345a2-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="345a2-107">Tiedot esitetään kokoonpanopaketissa, .rapidstart-tiedostossa, joka tarjoaa sisältöä pakatussa muodossa.</span><span class="sxs-lookup"><span data-stu-id="345a2-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="345a2-108">Määrityspakettien esimerkit, mukaan lukien maa-/aluekohtaiset tiedostot, sisältyvät CRONUS-esittely-yritykseen.</span><span class="sxs-lookup"><span data-stu-id="345a2-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="345a2-109">Käytä seuraavia toimenpiteitä käyttääksesi esimerkki määrityspakettia uuden yrityksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="345a2-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="345a2-110">BASICCONFIG-esimerkkimäärityspaketin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="345a2-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="345a2-111">Avaa CRONUS Finland Oy -yritys.</span><span class="sxs-lookup"><span data-stu-id="345a2-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="345a2-112">Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="345a2-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="345a2-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="345a2-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="345a2-114">Valitse BASICCONFIG-paketti luettelosta ja valitse sitten **Vie paketti** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="345a2-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="345a2-115">Luo seuraavan menettelyn avulla uusi yritys ja käytä BASICCONFIG-pakettia prosessin osana.</span><span class="sxs-lookup"><span data-stu-id="345a2-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="345a2-116">Luo uusi yritys</span><span class="sxs-lookup"><span data-stu-id="345a2-116">To create a new company</span></span>  
1. <span data-ttu-id="345a2-117">Luo uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="345a2-117">Create a new company.</span></span> <span data-ttu-id="345a2-118">Lisätietoa on kohdassa [Uusien yritysten luominen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="345a2-118">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="345a2-119">RapidStart Servicesin käyttöönottajan roolikeskuksesta voi nyt tuoda määrityspaketin, joka vietiin CRONUS Finland Oy -yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="345a2-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="345a2-120">Kun luot uuden yhtiön, joitakin taulukoita täytetään automaattisesti, vaikka yhtiömallia ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="345a2-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="345a2-121">Voit esimerkiksi tarkastella kirjauksen ja erätapahtumien vakiokoodeja **Lähdekoodi**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="345a2-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="345a2-122">Jos määrität [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman paikallisen version, tarkista tämä taulukko ja ota huomioon mahdolliset ongelmat paikallisen kielen kanssa.</span><span class="sxs-lookup"><span data-stu-id="345a2-122">If you provide a local version of [!INCLUDE[prod_short](includes/prod_short.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="345a2-123">Tietoja tietotaulukoista</span><span class="sxs-lookup"><span data-stu-id="345a2-123">About Data Tables</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="345a2-124">-arvotaulukoita on kaksi perustyyppiä: pää- ja asetustaulukot.</span><span class="sxs-lookup"><span data-stu-id="345a2-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="345a2-125">Kun määrität yrityksen kokoonpanoa, voit käyttää näitä tyyppejä keskittyäksesi kokoonpanostrategiaasi.</span><span class="sxs-lookup"><span data-stu-id="345a2-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="345a2-126">Päätietotaulukot</span><span class="sxs-lookup"><span data-stu-id="345a2-126">Master Data Tables</span></span>  
<span data-ttu-id="345a2-127">Seuraavassa taulukossa on joitakin esimerkkejä päätietotaulukoista.</span><span class="sxs-lookup"><span data-stu-id="345a2-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="345a2-128">Kun alustat uuden yrityksen, nämä taulut ovat tyhjät.</span><span class="sxs-lookup"><span data-stu-id="345a2-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="345a2-129">Taulukon nro</span><span class="sxs-lookup"><span data-stu-id="345a2-129">Table No.</span></span>|<span data-ttu-id="345a2-130">Taulukon nimi</span><span class="sxs-lookup"><span data-stu-id="345a2-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="345a2-131">15</span><span class="sxs-lookup"><span data-stu-id="345a2-131">15</span></span>|<span data-ttu-id="345a2-132">KP-tili</span><span class="sxs-lookup"><span data-stu-id="345a2-132">G/L Account</span></span>|  
|<span data-ttu-id="345a2-133">18</span><span class="sxs-lookup"><span data-stu-id="345a2-133">18</span></span>|<span data-ttu-id="345a2-134">Asiakas</span><span class="sxs-lookup"><span data-stu-id="345a2-134">Customer</span></span>|  
|<span data-ttu-id="345a2-135">23</span><span class="sxs-lookup"><span data-stu-id="345a2-135">23</span></span>|<span data-ttu-id="345a2-136">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="345a2-136">Vendor</span></span>|  
|<span data-ttu-id="345a2-137">27</span><span class="sxs-lookup"><span data-stu-id="345a2-137">27</span></span>|<span data-ttu-id="345a2-138">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="345a2-138">Item</span></span>|  
|<span data-ttu-id="345a2-139">5050</span><span class="sxs-lookup"><span data-stu-id="345a2-139">5050</span></span>|<span data-ttu-id="345a2-140">Kontakti</span><span class="sxs-lookup"><span data-stu-id="345a2-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="345a2-141">Tietotaulukoiden asetukset</span><span class="sxs-lookup"><span data-stu-id="345a2-141">Setup Data Tables</span></span>  
<span data-ttu-id="345a2-142">Seuraavassa taulukossa on joitakin asennustaulukoita, joihin siepataan asetustietoja määrityskyselylomakkeesta.</span><span class="sxs-lookup"><span data-stu-id="345a2-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="345a2-143">Nämä taulukot sisältävät perustietoja ajalta, jolloin yritys luotiin.</span><span class="sxs-lookup"><span data-stu-id="345a2-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="345a2-144">Taulukon nro</span><span class="sxs-lookup"><span data-stu-id="345a2-144">Table No.</span></span>|<span data-ttu-id="345a2-145">Taulukon nimi</span><span class="sxs-lookup"><span data-stu-id="345a2-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="345a2-146">98</span><span class="sxs-lookup"><span data-stu-id="345a2-146">98</span></span>|<span data-ttu-id="345a2-147">Pääkirjanpidon asetukset</span><span class="sxs-lookup"><span data-stu-id="345a2-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="345a2-148">311</span><span class="sxs-lookup"><span data-stu-id="345a2-148">311</span></span>|<span data-ttu-id="345a2-149">Myyntien ja myyntisaamisten asetukset</span><span class="sxs-lookup"><span data-stu-id="345a2-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="345a2-150">312</span><span class="sxs-lookup"><span data-stu-id="345a2-150">312</span></span>|<span data-ttu-id="345a2-151">Ostojen ja ostovelkojen asetukset</span><span class="sxs-lookup"><span data-stu-id="345a2-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="345a2-152">313</span><span class="sxs-lookup"><span data-stu-id="345a2-152">313</span></span>|<span data-ttu-id="345a2-153">Varastonhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="345a2-153">Inventory Setup</span></span>|  

<span data-ttu-id="345a2-154">[!INCLUDE[prod_short](includes/prod_short.md)] sisältää asetustietotaulukoiden lisäksi myös asetustyyppisiä tietotaulukoita, jotka määrittävät yrityksen ja sen liiketoimintaprosessien perustiedot.</span><span class="sxs-lookup"><span data-stu-id="345a2-154">In addition to setup data tables, [!INCLUDE[prod_short](includes/prod_short.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="345a2-155">Seuraavassa taulukossa esitellään osa niistä.</span><span class="sxs-lookup"><span data-stu-id="345a2-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="345a2-156">Taulukon nro</span><span class="sxs-lookup"><span data-stu-id="345a2-156">Table No.</span></span>|<span data-ttu-id="345a2-157">Taulukon nimi</span><span class="sxs-lookup"><span data-stu-id="345a2-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="345a2-158">3</span><span class="sxs-lookup"><span data-stu-id="345a2-158">3</span></span>|<span data-ttu-id="345a2-159">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="345a2-159">Payment Terms</span></span>|  
|<span data-ttu-id="345a2-160">4</span><span class="sxs-lookup"><span data-stu-id="345a2-160">4</span></span>|<span data-ttu-id="345a2-161">Valuutta</span><span class="sxs-lookup"><span data-stu-id="345a2-161">Currency</span></span>|  
|<span data-ttu-id="345a2-162">6</span><span class="sxs-lookup"><span data-stu-id="345a2-162">6</span></span>|<span data-ttu-id="345a2-163">Asiakashintaryhmät</span><span class="sxs-lookup"><span data-stu-id="345a2-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="345a2-164">5700</span><span class="sxs-lookup"><span data-stu-id="345a2-164">5700</span></span>|<span data-ttu-id="345a2-165">Varastointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="345a2-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="345a2-166">Katso myös</span><span class="sxs-lookup"><span data-stu-id="345a2-166">See Also</span></span>  
[<span data-ttu-id="345a2-167">Kokoonpanojen käyttäminen uusissa yrityksissä</span><span class="sxs-lookup"><span data-stu-id="345a2-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="345a2-168">Yrityksen määrittäminen RapidStart Servicesin avulla</span><span class="sxs-lookup"><span data-stu-id="345a2-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="345a2-169">Hallinta</span><span class="sxs-lookup"><span data-stu-id="345a2-169">Administration</span></span>](admin-setup-and-administration.md)
