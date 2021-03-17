---
title: Uuden yrityksen luominen | Microsoft Docs
description: RapidStart Servicesin käyttämisessä tarvittavat taulukot ja sivut luodaan, mutta niissä ei ole tietoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 703b70a608bd6b25b9a3218eb59e8666fcd6a0ab
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378321"
---
# <a name="create-a-new-company"></a><span data-ttu-id="f98c6-103">Uuden yrityksen luominen</span><span class="sxs-lookup"><span data-stu-id="f98c6-103">Create a New Company</span></span>
<span data-ttu-id="f98c6-104">Kun haluat käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in RapidStart Servicesia, luo ensin uusi yritys, jossa asiakkaan käyttöönotto suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="f98c6-104">To use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="f98c6-105">Kun luot uuden yhtiön, standardi [!INCLUDE[prod_short](includes/prod_short.md)] -taulukot ja sivut luodaan, mutta niissä ei ole tietoja.</span><span class="sxs-lookup"><span data-stu-id="f98c6-105">When you create a new company, the standard [!INCLUDE[prod_short](includes/prod_short.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="f98c6-106">Voit lisäksi ottaa yrityksessä käyttöön tietyt asetustiedot alustamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f98c6-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="f98c6-107">Tiedot esitetään kokoonpanopaketissa, .rapidstart-tiedostossa, joka tarjoaa sisältöä pakatussa muodossa.</span><span class="sxs-lookup"><span data-stu-id="f98c6-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="f98c6-108">Määrityspakettien esimerkit, mukaan lukien maa-/aluekohtaiset tiedostot, sisältyvät CRONUS-esittely-yritykseen.</span><span class="sxs-lookup"><span data-stu-id="f98c6-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="f98c6-109">Käytä seuraavia toimenpiteitä käyttääksesi esimerkki määrityspakettia uuden yrityksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="f98c6-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="f98c6-110">BASICCONFIG-esimerkkimäärityspaketin käyttäminen</span><span class="sxs-lookup"><span data-stu-id="f98c6-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="f98c6-111">Avaa CRONUS Finland Oy -yritys.</span><span class="sxs-lookup"><span data-stu-id="f98c6-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="f98c6-112">Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f98c6-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="f98c6-113">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Määrityspaketit** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f98c6-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="f98c6-114">Valitse BASICCONFIG-paketti luettelosta ja valitse sitten **Vie paketti** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f98c6-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="f98c6-115">Luo seuraavan menettelyn avulla uusi yritys ja käytä BASICCONFIG-pakettia prosessin osana.</span><span class="sxs-lookup"><span data-stu-id="f98c6-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="f98c6-116">Luo uusi yritys</span><span class="sxs-lookup"><span data-stu-id="f98c6-116">To create a new company</span></span>  
1. <span data-ttu-id="f98c6-117">Luo uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="f98c6-117">Create a new company.</span></span> <span data-ttu-id="f98c6-118">Lisätietoa on kohdassa [Uusien yritysten luominen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="f98c6-118">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="f98c6-119">RapidStart Servicesin käyttöönottajan roolikeskuksesta voi nyt tuoda määrityspaketin, joka vietiin CRONUS Finland Oy -yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="f98c6-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="f98c6-120">Kun luot uuden yhtiön, joitakin taulukoita täytetään automaattisesti, vaikka yhtiömallia ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="f98c6-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="f98c6-121">Voit esimerkiksi tarkastella kirjauksen ja erätapahtumien vakiokoodeja **Lähdekoodi**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f98c6-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="f98c6-122">Jos määrität [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman paikallisen version, tarkista tämä taulukko ja ota huomioon mahdolliset ongelmat paikallisen kielen kanssa.</span><span class="sxs-lookup"><span data-stu-id="f98c6-122">If you provide a local version of [!INCLUDE[prod_short](includes/prod_short.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="f98c6-123">Tietoja tietotaulukoista</span><span class="sxs-lookup"><span data-stu-id="f98c6-123">About Data Tables</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="f98c6-124">-arvotaulukoita on kaksi perustyyppiä: pää- ja asetustaulukot.</span><span class="sxs-lookup"><span data-stu-id="f98c6-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="f98c6-125">Kun määrität yrityksen kokoonpanoa, voit käyttää näitä tyyppejä keskittyäksesi kokoonpanostrategiaasi.</span><span class="sxs-lookup"><span data-stu-id="f98c6-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="f98c6-126">Päätietotaulukot</span><span class="sxs-lookup"><span data-stu-id="f98c6-126">Master Data Tables</span></span>  
<span data-ttu-id="f98c6-127">Seuraavassa taulukossa on joitakin esimerkkejä päätietotaulukoista.</span><span class="sxs-lookup"><span data-stu-id="f98c6-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="f98c6-128">Kun alustat uuden yrityksen, nämä taulut ovat tyhjät.</span><span class="sxs-lookup"><span data-stu-id="f98c6-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="f98c6-129">Taulukon nro</span><span class="sxs-lookup"><span data-stu-id="f98c6-129">Table No.</span></span>|<span data-ttu-id="f98c6-130">Taulukon nimi</span><span class="sxs-lookup"><span data-stu-id="f98c6-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="f98c6-131">15</span><span class="sxs-lookup"><span data-stu-id="f98c6-131">15</span></span>|<span data-ttu-id="f98c6-132">KP-tili</span><span class="sxs-lookup"><span data-stu-id="f98c6-132">G/L Account</span></span>|  
|<span data-ttu-id="f98c6-133">18</span><span class="sxs-lookup"><span data-stu-id="f98c6-133">18</span></span>|<span data-ttu-id="f98c6-134">Asiakas</span><span class="sxs-lookup"><span data-stu-id="f98c6-134">Customer</span></span>|  
|<span data-ttu-id="f98c6-135">23</span><span class="sxs-lookup"><span data-stu-id="f98c6-135">23</span></span>|<span data-ttu-id="f98c6-136">Toimittaja</span><span class="sxs-lookup"><span data-stu-id="f98c6-136">Vendor</span></span>|  
|<span data-ttu-id="f98c6-137">27</span><span class="sxs-lookup"><span data-stu-id="f98c6-137">27</span></span>|<span data-ttu-id="f98c6-138">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="f98c6-138">Item</span></span>|  
|<span data-ttu-id="f98c6-139">5050</span><span class="sxs-lookup"><span data-stu-id="f98c6-139">5050</span></span>|<span data-ttu-id="f98c6-140">Kontakti</span><span class="sxs-lookup"><span data-stu-id="f98c6-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="f98c6-141">Tietotaulukoiden asetukset</span><span class="sxs-lookup"><span data-stu-id="f98c6-141">Setup Data Tables</span></span>  
<span data-ttu-id="f98c6-142">Seuraavassa taulukossa on joitakin asennustaulukoita, joihin siepataan asetustietoja määrityskyselylomakkeesta.</span><span class="sxs-lookup"><span data-stu-id="f98c6-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="f98c6-143">Nämä taulukot sisältävät perustietoja ajalta, jolloin yritys luotiin.</span><span class="sxs-lookup"><span data-stu-id="f98c6-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="f98c6-144">Taulukon nro</span><span class="sxs-lookup"><span data-stu-id="f98c6-144">Table No.</span></span>|<span data-ttu-id="f98c6-145">Taulukon nimi</span><span class="sxs-lookup"><span data-stu-id="f98c6-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="f98c6-146">98</span><span class="sxs-lookup"><span data-stu-id="f98c6-146">98</span></span>|<span data-ttu-id="f98c6-147">Pääkirjanpidon asetukset</span><span class="sxs-lookup"><span data-stu-id="f98c6-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="f98c6-148">311</span><span class="sxs-lookup"><span data-stu-id="f98c6-148">311</span></span>|<span data-ttu-id="f98c6-149">Myyntien ja myyntisaamisten asetukset</span><span class="sxs-lookup"><span data-stu-id="f98c6-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="f98c6-150">312</span><span class="sxs-lookup"><span data-stu-id="f98c6-150">312</span></span>|<span data-ttu-id="f98c6-151">Ostojen ja ostovelkojen asetukset</span><span class="sxs-lookup"><span data-stu-id="f98c6-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="f98c6-152">313</span><span class="sxs-lookup"><span data-stu-id="f98c6-152">313</span></span>|<span data-ttu-id="f98c6-153">Varastonhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="f98c6-153">Inventory Setup</span></span>|  

<span data-ttu-id="f98c6-154">[!INCLUDE[prod_short](includes/prod_short.md)] sisältää asetustietotaulukoiden lisäksi myös asetustyyppisiä tietotaulukoita, jotka määrittävät yrityksen ja sen liiketoimintaprosessien perustiedot.</span><span class="sxs-lookup"><span data-stu-id="f98c6-154">In addition to setup data tables, [!INCLUDE[prod_short](includes/prod_short.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="f98c6-155">Seuraavassa taulukossa esitellään osa niistä.</span><span class="sxs-lookup"><span data-stu-id="f98c6-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="f98c6-156">Taulukon nro</span><span class="sxs-lookup"><span data-stu-id="f98c6-156">Table No.</span></span>|<span data-ttu-id="f98c6-157">Taulukon nimi</span><span class="sxs-lookup"><span data-stu-id="f98c6-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="f98c6-158">3</span><span class="sxs-lookup"><span data-stu-id="f98c6-158">3</span></span>|<span data-ttu-id="f98c6-159">Maksuehdot</span><span class="sxs-lookup"><span data-stu-id="f98c6-159">Payment Terms</span></span>|  
|<span data-ttu-id="f98c6-160">4</span><span class="sxs-lookup"><span data-stu-id="f98c6-160">4</span></span>|<span data-ttu-id="f98c6-161">Valuutta</span><span class="sxs-lookup"><span data-stu-id="f98c6-161">Currency</span></span>|  
|<span data-ttu-id="f98c6-162">6</span><span class="sxs-lookup"><span data-stu-id="f98c6-162">6</span></span>|<span data-ttu-id="f98c6-163">Asiakashintaryhmät</span><span class="sxs-lookup"><span data-stu-id="f98c6-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="f98c6-164">5700</span><span class="sxs-lookup"><span data-stu-id="f98c6-164">5700</span></span>|<span data-ttu-id="f98c6-165">Varastointiyksikkö</span><span class="sxs-lookup"><span data-stu-id="f98c6-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="f98c6-166">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f98c6-166">See Also</span></span>  
[<span data-ttu-id="f98c6-167">Kokoonpanojen käyttäminen uusissa yrityksissä</span><span class="sxs-lookup"><span data-stu-id="f98c6-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="f98c6-168">Yrityksen määrittäminen RapidStart Servicesin avulla</span><span class="sxs-lookup"><span data-stu-id="f98c6-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="f98c6-169">Hallinta</span><span class="sxs-lookup"><span data-stu-id="f98c6-169">Administration</span></span>](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]