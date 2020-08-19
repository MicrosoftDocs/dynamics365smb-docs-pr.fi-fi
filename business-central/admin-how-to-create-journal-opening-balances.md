---
title: Kirjauskansion alkusaldojen luominen | Microsoft Docs
description: Business Central sisältää useita eräajoja, jotka helpottavat uuden määritetyn yrityksen vanhojen tilien saldojen siirtämistä. Voit helposti siirtää nämä tiedot ja kirjauskansion kirjaukset.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/14/2020
ms.author: sgroespe
ms.openlocfilehash: 5360b3a8a72387cda8d0e640562a118ca1f20ff4
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577124"
---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="31b81-104">Kirjauskansion alkusaldojen luominen</span><span class="sxs-lookup"><span data-stu-id="31b81-104">Create Journal Opening Balances</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="31b81-105">sisältää useita eräajoja, jotka helpottavat uuden määritetyn yrityksen vanhojen tilien saldojen siirtämistä.</span><span class="sxs-lookup"><span data-stu-id="31b81-105">includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="31b81-106">Voit helposti siirtää nämä tiedot asiakkaan kirjauskansioon, toimittajan kirjauskansioon, nimikepäiväkirjaan tai KP-päiväkirjaan.</span><span class="sxs-lookup"><span data-stu-id="31b81-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="31b81-107">Ensimmäiseksi luodaan kokoonpanopaketti, johon sisältyvät kyseisten päiväkirjojen asetustaulukot.</span><span class="sxs-lookup"><span data-stu-id="31b81-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="31b81-108">Seuraavassa toimenpiteessä oletetaan, että tämä vaihe on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="31b81-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="31b81-109">Lisätietoja on kohdassa [Yrityksen konfiguraation määrittäminen](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="31b81-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="31b81-110">Näissä ohjeissa kuvataan seuraavat vaiheet, joihin kuuluu yhteistyökumppanin toimittaman paketin käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="31b81-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="31b81-111">Varmista ennen aloittamista, että käytät järjestelmänvalvojan roolikeskuksen sivua, koska se tarjoaa oikean kontekstin määrittelytyöllesi.</span><span class="sxs-lookup"><span data-stu-id="31b81-111">Before you start, make sure that you are using the Administration Role Center page because it provides the correct context for your configuration work.</span></span> <span data-ttu-id="31b81-112">Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="31b81-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="31b81-113">Käytä päiväkirjan tapahtumia uuteen yritykseen</span><span class="sxs-lookup"><span data-stu-id="31b81-113">To apply the entries in a journal to a new company</span></span>

1. <span data-ttu-id="31b81-114">Määritä uusi yritys ja ota sille käyttöön määrityspaketti.</span><span class="sxs-lookup"><span data-stu-id="31b81-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="31b81-115">Lisätietoja on kohdassa [Yrityksen määrittämien ohjatun RapidStart-toiminnon avulla](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="31b81-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="31b81-116">Uudessa yrityksessä ei ole tietoja kirjauskansion alkusaldoista.</span><span class="sxs-lookup"><span data-stu-id="31b81-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="31b81-117">Avaa määritystyökirja ja tuo olemassa olevat tiedot asiakkaista, nimikkeistä, toimittajista ja pääkirjanpidosta.</span><span class="sxs-lookup"><span data-stu-id="31b81-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="31b81-118">Lisätietoja on ohjeaiheessa [Asiakastietojen siirtäminen](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="31b81-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  

    <span data-ttu-id="31b81-119">Nyt sinulla on perustiedot käytössä.</span><span class="sxs-lookup"><span data-stu-id="31b81-119">Now you have master data in place.</span></span> <span data-ttu-id="31b81-120">Seuraavaksi lisätään alkusaldot.</span><span class="sxs-lookup"><span data-stu-id="31b81-120">Next, you add the opening balances.</span></span> <span data-ttu-id="31b81-121">Seuraavissa vaiheissa kuvataan, miten KP-tileille luodaan päiväkirjarivejä, mutta sama pätee asiakkaiden, toimittajien ja nimikkeiden päiväkirjarivien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="31b81-121">The following steps describe how to create journal lines for G/L accounts, but the same apply to creating journal lines for customers, vendors, and items.</span></span>  
3. <span data-ttu-id="31b81-122">Valitse **Luo pääkirjanpidon tilien kirjauskansioiden rivit** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="31b81-122">Choose the **Create G/L Acct. Journal Lines** action.</span></span>  
4. <span data-ttu-id="31b81-123">Täytä **Vaihtoehdot**-pikavälilehden tarvittavat kohdat ja määritä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="31b81-123">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="31b81-124">Syötä **Päiväkirjan malli** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="31b81-124">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="31b81-125">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="31b81-125">Choose the **OK** button.</span></span> <span data-ttu-id="31b81-126">Tietueet ovat nyt kirjauskansiossa, mutta summat ovat tyhjiä.</span><span class="sxs-lookup"><span data-stu-id="31b81-126">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="31b81-127">Vie päiväkirjataulukko Exceliin ja syötä kirjaus- ja vastatilin tiedot manuaalisesti vanhoista tiedoista.</span><span class="sxs-lookup"><span data-stu-id="31b81-127">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="31b81-128">Tuo uuden yrityksen taulukon tiedot ja ota ne käyttöön.</span><span class="sxs-lookup"><span data-stu-id="31b81-128">Import and apply the table information into the new company.</span></span> <span data-ttu-id="31b81-129">Kirjauskansion rivit ovat valmiita kirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="31b81-129">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="31b81-130">Valitse määritystyökirjassa kirjauskansion rivin taulukko ja valitse sitten **Tietokannan tiedot** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="31b81-130">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="31b81-131">Tarkista tiedot ja valitse **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="31b81-131">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="31b81-132">Toista vaiheet tuodaksesi ja kirjataksesi muut mahdolliset avaussaldot.</span><span class="sxs-lookup"><span data-stu-id="31b81-132">Repeat the steps to import and post any other opening balances.</span></span>  

> [!TIP]
> <span data-ttu-id="31b81-133">Voit käyttää samoja eräajoja avaussaldojen lisäämiseen aina kun rekisteröit uuden asiakkaan tai toimittajan, jonka kanssa sinulla on ollut liiketoimintaa aiemmin, mutta et ole rekisteröitynyt kohteeseen [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="31b81-133">You can use the same batch jobs to add opening balances whenever you register a new customer or vendor that you have done business with before but not registered in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="31b81-134">Etsi vain haluamasi tehtävä ja valitse sitten asianmukainen linkki.</span><span class="sxs-lookup"><span data-stu-id="31b81-134">Just search for the relevant task, and then choose the relevant link.</span></span>

## <a name="see-also"></a><span data-ttu-id="31b81-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="31b81-135">See Also</span></span>

[<span data-ttu-id="31b81-136">Kokoonpanojen käyttäminen uusissa yrityksissä</span><span class="sxs-lookup"><span data-stu-id="31b81-136">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="31b81-137">Yrityksen määrittäminen RapidStart Servicesin avulla</span><span class="sxs-lookup"><span data-stu-id="31b81-137">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="31b81-138">Hallinta</span><span class="sxs-lookup"><span data-stu-id="31b81-138">Administration</span></span>](admin-setup-and-administration.md)  
