---
title: "Tallennettujen asetusten käyttäminen raporteissa ja niiden muokkaaminen | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan ennalta määritetyistä asetuksista ja suodattimista, joilla raportti mukautetaan ja luodaan oikeita tietoja."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d0ef9148b082b05a46283f89c3cb98bb1cd0c6d0
ms.openlocfilehash: 2a7ab137a9bf8ec3580e718053f8e67320e3af5a
ms.contentlocale: fi-fi
ms.lasthandoff: 08/06/2018

---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="e899d-103">Raporttien tallennettujen asetusten hallinta</span><span class="sxs-lookup"><span data-stu-id="e899d-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="e899d-104">Raportteja ajettaessa käyttäjä saa tyypillisesti näkyviin sivun, jolla voi määrittää tietyt luodun raportin tietojen muuttamisessa tarvittavat asetukset ja suodattimet.</span><span class="sxs-lookup"><span data-stu-id="e899d-104">When running a reports, users are typically presented with a page that lets them set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="e899d-105">Sivua kutsutaan raporttipyyntösivuksi.</span><span class="sxs-lookup"><span data-stu-id="e899d-105">This page is called the report request page.</span></span> <span data-ttu-id="e899d-106">Raportti voi sisältää vähintään yhdet *tallennetut asetukset*, joita voidaan käyttää pyyntösivun raportissa.</span><span class="sxs-lookup"><span data-stu-id="e899d-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="e899d-107">*Tallennetut asetukset* ovat periaatteessa ennalta määritettyjä asetuksia ja suodattimia.</span><span class="sxs-lookup"><span data-stu-id="e899d-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="e899d-108">Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten.</span><span class="sxs-lookup"><span data-stu-id="e899d-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="e899d-109">Lisätietoja siitä, miten tallennettuja asetuksia käytetään kohdassa [Tallennettujen asetusten käyttäminen](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="e899d-109">For more information about how saved settings are used, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="e899d-110">Jos sinulla on tarvittavat oikeudet, voit tarkastella, luoda ja muokata yrityksen kaikkien käyttäjien raporttien tallennettuja asetuksia.</span><span class="sxs-lookup"><span data-stu-id="e899d-110">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="e899d-111">Voit määrittää raportin tallennetut asetukset yksittäisille käyttäjille tai yrityksen kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="e899d-111">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="e899d-112">Kaikkien käyttäjien tallennettujen asetusten luominen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e899d-112">Create and modify saved settings for all users</span></span>
<span data-ttu-id="e899d-113">Voit hallita tallennettuja asetuksia sivun **1560 Raporttien asetukset** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="e899d-113">You manage saved settings from page **1560 Reports Settings**.</span></span> <span data-ttu-id="e899d-114">Sivun voi avata kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="e899d-114">There are two ways to open this page:</span></span>
-   <span data-ttu-id="e899d-115">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Raportin asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e899d-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="e899d-116">Avaa raportti, valitse haku **Käytetyt oletusarvot:** -ruudun vierestä, valitse **Valitse koko luettelosta**.</span><span class="sxs-lookup"><span data-stu-id="e899d-116">Open a report, choose the lookup next to the **Used default values from:** box, choose **Select from full list**.</span></span>

<span data-ttu-id="e899d-117">Sivulla näkyvät kaikki olemassa olevat kaikkien käyttäjien tallennusasetukset.</span><span class="sxs-lookup"><span data-stu-id="e899d-117">The page displays all the existing save settings entries for all users.</span></span> <span data-ttu-id="e899d-118">Jos sarakkeessa **Määritetty** on käyttäjänimi, vain kyseinen käyttäjä voi käyttää liittyvään raporttiin tallennettuja asetuksia.</span><span class="sxs-lookup"><span data-stu-id="e899d-118">If there is a user name in the **Assigned to** column, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="e899d-119">Jos valintamerkki on **Jaa kaikkien käyttäjien kanssa** -sarakkeessa, kaikki käyttäjät voivat käyttää tallennettuja asetuksia raporttia varten.</span><span class="sxs-lookup"><span data-stu-id="e899d-119">If there is a check mark in the **Share with all users** column, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="e899d-120">**Raporttiasetukset** -sivulla voit:</span><span class="sxs-lookup"><span data-stu-id="e899d-120">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="e899d-121">Valita **Uusi** luodaksesi alusta uuden tallennetun tapahtuma-asetuksen.</span><span class="sxs-lookup"><span data-stu-id="e899d-121">Choose **New** to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="e899d-122">Valita tallennettujen asetusten tapahtuman luettelosta ja valita **Kopioi** luodaksesi kopion.</span><span class="sxs-lookup"><span data-stu-id="e899d-122">Select a saved settings entry from the list, and choose **Copy** to create a copy.</span></span>
-   <span data-ttu-id="e899d-123">Valita tallennettujen asetusten tapahtuman luettelosta **Muokkaa** muokataksesi tallennettujen asetusten merkintää.</span><span class="sxs-lookup"><span data-stu-id="e899d-123">Select a saved settings entry from the list, and choose **Edit** to modify a saved settings entry.</span></span>


> [!Important]
> <span data-ttu-id="e899d-124">Harkita minkä nimen annat tallennettujen asetusten merkinnälle.</span><span class="sxs-lookup"><span data-stu-id="e899d-124">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="e899d-125">Jos luot tallennettujen asetusten merkinnän kaikille käyttäjille, ja annat sille saman nimen kuin tietyn käyttäjän aiemmin tallennetuilla merkinnöillä, jotka on määritelty vain tietylle käyttäjälle, kyseinen käyttäjä ei voi käyttää kaikille tarkoitettua asetusmerkintäjoukkoa.</span><span class="sxs-lookup"><span data-stu-id="e899d-125">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="e899d-126">Käyttäjä näkee **Tallennetut asetukset** -kentässä kaksi tallennettujen asetusten merkintää, joilla on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="e899d-126">Under **Saved Settings** on the report request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="e899d-127">Valitusta vaihtoehdosta riippumatta järjestelmä käyttää käyttäjän omia asetusmerkintöjä.</span><span class="sxs-lookup"><span data-stu-id="e899d-127">However, no matter which option he chooses, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="e899d-128">Raporttien tallennettujen asetusten ominaisuus on käytettävissä vain [SaveValues-ominaisuudessa](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property), joissa arvoksi on määritetty `Yes`.</span><span class="sxs-lookup"><span data-stu-id="e899d-128">The saved settings feature is available only on reports where the [SaveValues property](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) of the report's request page is set to `Yes`.</span></span> <span data-ttu-id="e899d-129">**SaveValues** -ominaisuus määritetään kehitysympäristössä.</span><span class="sxs-lookup"><span data-stu-id="e899d-129">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e899d-130">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e899d-130">See Also</span></span>
[<span data-ttu-id="e899d-131">Raporttien käsittely</span><span class="sxs-lookup"><span data-stu-id="e899d-131">Working with Reports</span></span>](ui-work-report.md)  

