---
title: Kirjauskansion alkusaldojen luominen | Microsoft Docs
description: "Business Central sisältää useita eräajoja, jotka helpottavat uuden määritetyn yrityksen vanhojen tilien saldojen siirtämistä. Voit helposti siirtää nämä tiedot ja kirjauskansion kirjaukset."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 612eb9cfa5c6cd45bf154f4813efa3b349f44841
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="021c1-104">Kirjauskansion alkusaldojen luominen</span><span class="sxs-lookup"><span data-stu-id="021c1-104">Create Journal Opening Balances</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="021c1-105">sisältää useita eräajoja, jotka helpottavat uuden määritetyn yrityksen vanhojen tilien saldojen siirtämistä.</span><span class="sxs-lookup"><span data-stu-id="021c1-105"> includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="021c1-106">Voit helposti siirtää nämä tiedot asiakkaan kirjauskansioon, toimittajan kirjauskansioon, nimikepäiväkirjaan tai KP-päiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="021c1-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="021c1-107">Ensimmäiseksi luodaan kokoonpanopaketti, johon sisältyvät kyseisten päiväkirjojen asetustaulukot.</span><span class="sxs-lookup"><span data-stu-id="021c1-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="021c1-108">Seuraavassa toimenpiteessä oletetaan, että tämä vaihe on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="021c1-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="021c1-109">Lisätietoja on kohdassa [Yrityksen konfiguraation määrittäminen](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="021c1-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="021c1-110">Näissä ohjeissa kuvataan seuraavat vaiheet, joihin kuuluu yhteistyökumppanin toimittaman paketin käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="021c1-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="021c1-111">Varmista ennen aloittamista, että olet RapidStart Services -palvelun käyttöönottajan roolikeskuksen sivulla. Tämä sivu tarjoaa määritystyölle juuri oikean kontekstin.</span><span class="sxs-lookup"><span data-stu-id="021c1-111">Before you start, make sure that you are on the RapidStart Services Implementer Role Center page as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="021c1-112">Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="021c1-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="021c1-113">Käytä päiväkirjan tapahtumia uuteen yritykseen</span><span class="sxs-lookup"><span data-stu-id="021c1-113">To apply the entries in a journal to a new company</span></span>  
1. <span data-ttu-id="021c1-114">Määritä uusi yritys ja ota sille käyttöön määrityspaketti.</span><span class="sxs-lookup"><span data-stu-id="021c1-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="021c1-115">Lisätietoja on kohdassa [Yrityksen määrittämien ohjatun RapidStart-toiminnon avulla](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="021c1-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="021c1-116">Uudessa yrityksessä ei ole tietoja kirjauskansion alkusaldoista.</span><span class="sxs-lookup"><span data-stu-id="021c1-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="021c1-117">Avaa määritystyökirja ja tuo olemassa olevat tiedot asiakkaista, nimikkeistä, toimittajista ja pääkirjanpidosta.</span><span class="sxs-lookup"><span data-stu-id="021c1-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="021c1-118">Lisätietoja on ohjeaiheessa [Asiakastietojen siirtäminen](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="021c1-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  
3. <span data-ttu-id="021c1-119">Valitse esimerkiksi **Luo kirjanpitopäiväkirjan rivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="021c1-119">Choose, for example, the **Create G/L Journal Lines** action.</span></span>  
4. <span data-ttu-id="021c1-120">Täytä **Vaihtoehdot**-pikavälilehden tarvittavat kohdat ja määritä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="021c1-120">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="021c1-121">Syötä **Päiväkirjan malli** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="021c1-121">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="021c1-122">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="021c1-122">Choose the **OK** button.</span></span> <span data-ttu-id="021c1-123">Tietueet ovat nyt kirjauskansiossa, mutta summat ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="021c1-123">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="021c1-124">Vie päiväkirjataulukko Exceliin ja syötä kirjaus- ja vastatilin tiedot manuaalisesti vanhoista tiedoista.</span><span class="sxs-lookup"><span data-stu-id="021c1-124">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="021c1-125">Tuo uuden yrityksen taulukon tiedot ja ota ne käyttöön.</span><span class="sxs-lookup"><span data-stu-id="021c1-125">Import and apply the table information into the new company.</span></span> <span data-ttu-id="021c1-126">Kirjauskansion rivit ovat valmiita kirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="021c1-126">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="021c1-127">Valitse määritystyökirjassa kirjauskansion rivin taulukko ja valitse sitten **Tietokannan tiedot** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="021c1-127">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="021c1-128">Tarkista tiedot ja valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="021c1-128">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="021c1-129">Toista vaiheet tuodaksesi ja kirjataksesi muut mahdolliset avaussaldot.</span><span class="sxs-lookup"><span data-stu-id="021c1-129">Repeat the steps to import and post any other opening balances.</span></span>  

## <a name="see-also"></a><span data-ttu-id="021c1-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="021c1-130">See Also</span></span>  
[<span data-ttu-id="021c1-131">Kokoonpanojen käyttäminen uusissa yrityksissä</span><span class="sxs-lookup"><span data-stu-id="021c1-131">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="021c1-132">Yrityksen määrittäminen RapidStart Services -palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="021c1-132">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="021c1-133">Hallinta</span><span class="sxs-lookup"><span data-stu-id="021c1-133">Administration</span></span>](admin-setup-and-administration.md)

