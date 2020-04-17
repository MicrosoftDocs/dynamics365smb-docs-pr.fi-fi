---
title: Tallennettujen asetusten käyttäminen raporteissa ja niiden muokkaaminen | Microsoft Docs
description: Ohjeaiheessa kerrotaan ennalta määritetyistä asetuksista ja suodattimista, joilla raportti mukautetaan ja luodaan oikeita tietoja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4c43429e4436400dc9e3b991b9ccca59a439372a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191881"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><span data-ttu-id="747aa-103">Raporttien ja erätöiden tallennettujen asetusten hallinta</span><span class="sxs-lookup"><span data-stu-id="747aa-103">Manage Saved Settings for Reports and Batch jobs</span></span>
<span data-ttu-id="747aa-104">Raportteja ajettaessa käyttäjät näkyvät yleensä sivun, jossa voi valita asetuksia ja määrittää suodattimia, joita tarvitaan luotuun raporttiin sisältyvien tietojen muuttamiseen.</span><span class="sxs-lookup"><span data-stu-id="747aa-104">When running reports, users are typically presented with a page that lets them select options and set filters to change the data that is included in the generated report.</span></span> <span data-ttu-id="747aa-105">Sivua kutsutaan pyyntösivuksi.</span><span class="sxs-lookup"><span data-stu-id="747aa-105">This page is called the request page.</span></span> <span data-ttu-id="747aa-106">Raportti voi sisältää vähintään yhdet *tallennetut asetukset*, joita voidaan käyttää pyyntösivun raportissa.</span><span class="sxs-lookup"><span data-stu-id="747aa-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="747aa-107">*Tallennetut asetukset* ovat periaatteessa ennalta määritettyjä asetuksia ja suodattimia.</span><span class="sxs-lookup"><span data-stu-id="747aa-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="747aa-108">Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten.</span><span class="sxs-lookup"><span data-stu-id="747aa-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="747aa-109">Lisätietoja on kohdassa [Tallennettujen asetusten käyttäminen](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="747aa-109">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

> [!NOTE]
> <span data-ttu-id="747aa-110">Tässä ohjeaiheessa viitataan pääsiassa raportteihin, mutta vastaavat tiedot koskevat myös erätöitä.</span><span class="sxs-lookup"><span data-stu-id="747aa-110">This topic refers mainly to "report", but similar information applies to batch jobs.</span></span>

<span data-ttu-id="747aa-111">Jos sinulla on tarvittavat oikeudet, voit tarkastella, luoda ja muokata yrityksen kaikkien käyttäjien kaikkien raporttien tallennettuja asetuksia.</span><span class="sxs-lookup"><span data-stu-id="747aa-111">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in a company.</span></span> <span data-ttu-id="747aa-112">Voit määrittää raportin tallennetut asetukset yksittäisille käyttäjille tai yrityksen kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="747aa-112">You can assign saved settings for a report to individual users or to all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="747aa-113">Kaikkien käyttäjien tallennettujen asetusten luominen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="747aa-113">To create and modify saved settings for all users</span></span>
<span data-ttu-id="747aa-114">Voit hallita tallennettuja asetuksia **Raporttien asetukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="747aa-114">You manage saved settings on the **Reports Settings** page.</span></span> <span data-ttu-id="747aa-115">Sivun voi avata kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="747aa-115">There are two ways to open this page:</span></span>
-   <span data-ttu-id="747aa-116">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Raporttiasetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="747aa-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="747aa-117">Avaa raportti, valitse **Käytä oletusarvoja kohteesta:** -kentän haku ja valitse sitten **Valitse koko luettelosta** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="747aa-117">Open a report, choose the lookup in the **Use default values from** field, and then choose the **Select from full list** action.</span></span>

<span data-ttu-id="747aa-118">Sivulla näkyvät kaikkien käyttäjien kaikki aiemmin tallennetut asetukset.</span><span class="sxs-lookup"><span data-stu-id="747aa-118">The page displays all the existing saved settings entries for all users.</span></span> <span data-ttu-id="747aa-119">Jos **Määritetty kohteelle** -kentässä on käyttäjänimi, vain kyseinen käyttäjä voi käyttää liittyvään raporttiin tallennettuja asetuksia.</span><span class="sxs-lookup"><span data-stu-id="747aa-119">If there is a user name in the **Assigned to** field, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="747aa-120">Jos **Jaettu kaikille käyttäjille** -kentässä on valintamerkki, kaikki käyttäjät voivat käyttää raportin tallennettuja asetuksia.</span><span class="sxs-lookup"><span data-stu-id="747aa-120">If there is a check mark in the **Share with all users** field, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="747aa-121">**Raporttiasetukset** -sivulla voit:</span><span class="sxs-lookup"><span data-stu-id="747aa-121">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="747aa-122">luoda täysin uuden asetuksen tallennustapahtuman valitsemalla **Uusi**-toiminnon</span><span class="sxs-lookup"><span data-stu-id="747aa-122">Choose the **New** action to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="747aa-123">valitse tallennettujen asetusten tapahtuman luettelosta ja luoda kopion valitsemalla **Kopioi**-toiminnon</span><span class="sxs-lookup"><span data-stu-id="747aa-123">Select a saved settings entry from the list, and choose the **Copy** action to create a copy.</span></span>
-   <span data-ttu-id="747aa-124">valita asetusten tallennustapahtuman luettelosta ja muokata asetusten tallennustapahtumaa valitsemalla **Muokkaa**-toiminnon</span><span class="sxs-lookup"><span data-stu-id="747aa-124">Select a saved settings entry from the list, and choose the **Edit** action to modify a saved settings entry.</span></span>

> [!Important]
> <span data-ttu-id="747aa-125">Harkita minkä nimen annat tallennettujen asetusten merkinnälle.</span><span class="sxs-lookup"><span data-stu-id="747aa-125">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="747aa-126">Jos luot tallennettujen asetusten merkinnän kaikille käyttäjille, ja annat sille saman nimen kuin tietyn käyttäjän aiemmin tallennetuilla merkinnöillä, jotka on määritelty vain tietylle käyttäjälle, kyseinen käyttäjä ei voi käyttää kaikille tarkoitettua asetusmerkintäjoukkoa.</span><span class="sxs-lookup"><span data-stu-id="747aa-126">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="747aa-127">Käyttäjä näkee **Tallennetut asetukset** -osassa kaksi asetusten tallennustapahtumaa, jolla on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="747aa-127">In the **Saved Settings** section on the request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="747aa-128">Valitusta vaihtoehdosta riippumatta järjestelmä käyttää käyttäjän omaa asetusten tallennustapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="747aa-128">However, no matter which option they choose, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="747aa-129">Tallennetut asetukset -ominaisuus on käytössä vain raporteissa, joissa raportin pyyntösivun [SaveValues-ominaisuudeksi](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="747aa-129">The Saved Settings feature is available only on reports where the [SaveValues property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) of the report's request page is set to **Yes**.</span></span> <span data-ttu-id="747aa-130">**SaveValues** -ominaisuus määritetään kehitysympäristössä.</span><span class="sxs-lookup"><span data-stu-id="747aa-130">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="747aa-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="747aa-131">See Also</span></span>
[<span data-ttu-id="747aa-132">Raporttien, eräajojen ja XMLportien käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="747aa-132">Working with Reports, Batch Jobs, and XMLports</span></span>](ui-work-report.md)  
