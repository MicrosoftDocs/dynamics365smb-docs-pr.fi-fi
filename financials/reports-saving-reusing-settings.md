---
title: "Tallennettujen asetusten käyttäminen raporteissa ja niiden muokkaaminen | Microsoft Docs"
description: "Ohjeaiheessa kerrotaan ennalta määritetyistä asetuksista ja suodattimista, joilla raportti mukautetaan ja luodaan oikeita tietoja."
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2783c3a80beed5de6b7f7a63ff6811648ef48df3
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="125fa-103">Raporttien tallennettujen asetusten hallinta</span><span class="sxs-lookup"><span data-stu-id="125fa-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="125fa-104">Ajetusta raportista riippuen näkyviin voi tulla sivu, jolla voi määrittää tietyt luodun raportin tietojen muuttamisessa tarvittavat asetukset ja suodattimet.</span><span class="sxs-lookup"><span data-stu-id="125fa-104">Depending on the report that is run, you might be presented with a page that lets you to set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="125fa-105">Sivua kutsutaan raporttipyyntösivuksi.</span><span class="sxs-lookup"><span data-stu-id="125fa-105">This page is known as the report request page.</span></span> <span data-ttu-id="125fa-106">Raportti voi sisältää vähintään yhdet *tallennetut asetukset*, joita voidaan käyttää pyyntösivun raportissa.</span><span class="sxs-lookup"><span data-stu-id="125fa-106">A report can include one or more *saved settings* that you can apply to the report from the request page.</span></span> <span data-ttu-id="125fa-107">*Tallennetut asetukset* ovat periaatteessa ennalta määritettyjä asetuksia ja suodattimia.</span><span class="sxs-lookup"><span data-stu-id="125fa-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="125fa-108">Tallennettujen asetusten käyttäminen on nopea ja helppo tapa oikeiden tietojen sisältämien raporttien luomista varten.</span><span class="sxs-lookup"><span data-stu-id="125fa-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span>

<span data-ttu-id="125fa-109">Voit tarkastella raportin käytettävissä olevia tallennettuja asetuksia raporttipyyntösivun **Tallennetut asetukset** -osassa.</span><span class="sxs-lookup"><span data-stu-id="125fa-109">You can see the saved settings that are available to you for a report in **Saved Settings** section of the report request page.</span></span>  

## <a name="to-apply-saved-settings-to-a-report"></a><span data-ttu-id="125fa-110">Tallennettujen asetusten käyttäminen raportissa</span><span class="sxs-lookup"><span data-stu-id="125fa-110">To apply saved settings to a report</span></span>
1. <span data-ttu-id="125fa-111">Avaa raportti.</span><span class="sxs-lookup"><span data-stu-id="125fa-111">Open the report.</span></span>

   <span data-ttu-id="125fa-112">Näkyviin tulee raporttipyyntösivu.</span><span class="sxs-lookup"><span data-stu-id="125fa-112">The report request page appears.</span></span>    
2. <span data-ttu-id="125fa-113">Määritä sivun **Tallennetut asetukset** -osan **Nimi**-kenttään ne tallennetut asetukset, joita haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="125fa-113">In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.</span></span>

   <span data-ttu-id="125fa-114">**Tallennetut asetukset** -osa näkyy vain, jos raportti on suoritettu aiemmin tai jos asetukset on tallennettu aiemmin.</span><span class="sxs-lookup"><span data-stu-id="125fa-114">The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries.</span></span> <span data-ttu-id="125fa-115">**Viimeksi käytetyt asetukset ja suodattimet** -kirjaus on aina saatavilla.</span><span class="sxs-lookup"><span data-stu-id="125fa-115">The saved settings entry called **Last used options and filters** is always available.</span></span> <span data-ttu-id="125fa-116">Nämä asetukset ovat valinnan ja suodattimen arvot, joita käytettiin viimeksi raportin ajon yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="125fa-116">These settings are the option and filter values that were used the last time you ran the report.</span></span>

## <a name="administer-saved-report-settings-for-users"></a><span data-ttu-id="125fa-117">Käyttäjille tallennettujen raporttiasetusten hallinta</span><span class="sxs-lookup"><span data-stu-id="125fa-117">Administer saved report settings for users</span></span>
<span data-ttu-id="125fa-118">Jos sinulla on tarvittavat oikeudet, voit tarkastella, luoda ja muokata yrityksen kaikkien käyttäjien raporttien tallennettuja asetuksia.</span><span class="sxs-lookup"><span data-stu-id="125fa-118">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="125fa-119">Voit määrittää raportin tallennetut asetukset yksittäisille käyttäjille tai yrityksen kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="125fa-119">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<span data-ttu-id="125fa-120">Voit hallita tallennettuja asetuksia sivun 1506 **Raporttien asetukset** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="125fa-120">You manage saved settings from page 1506 **Reports Settings**.</span></span> <span data-ttu-id="125fa-121">Avaa tämä sivu valitsemalla ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoittamalla **Raportin asetukset** ja valitsemalla sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="125fa-121">To open this page, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Settings**, and then choose the related link.</span></span>

<span data-ttu-id="125fa-122">**Raporttiasetukset**-sivulla voit luoda uudet asetukset alusta alkaen tai kopioida aiemmin määritetyt asetukset ja muokata niitä.</span><span class="sxs-lookup"><span data-stu-id="125fa-122">From the **Report Settings** page, you can create a new settings from scratch or you can make a copy and modify existing settings.</span></span> <span data-ttu-id="125fa-123">Voit muokata asetusten valintoja ja suodattimia valitsemalla **Muokkaa**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="125fa-123">To modify the options and filters for a settings, choose the **Edit** action.</span></span>

> [!NOTE]
> <span data-ttu-id="125fa-124">Raporttien tallennettujen asetusten ominaisuus on käytettävissä vain, kun pyyntösivun SaveValues-ominaisuuden arvoksi on määritetty Kyllä.</span><span class="sxs-lookup"><span data-stu-id="125fa-124">The saved settings feature on reports is only relevant when the SaveValues property of the request page is set to Yes.</span></span> <span data-ttu-id="125fa-125">SaveValues-ominaisuuden ominaisuus määritetään kehitysympäristössä.</span><span class="sxs-lookup"><span data-stu-id="125fa-125">The SaveValues property property is set in the development environment.</span></span>  

> [!Important]
> <span data-ttu-id="125fa-126">Jos luot tallennetut asetukset kaikille käyttäjille, ja niillä on sama nimi kuin tietyn käyttäjän aiemmin tallennetuilla asetuksilla, käyttäjä ei voi käyttää kaikille tarkoitettua asetusjoukkoa.</span><span class="sxs-lookup"><span data-stu-id="125fa-126">If you create a saved settings item for all users, and it has the same name as an existing saved settings for a specific user, then that user will not be able to use the saved settings that is assigned to everyone.</span></span>  <span data-ttu-id="125fa-127">Käyttäjä näkee raportin pyyntösivun Tallennetut asetukset -kentässä kaksi tallennettujen asetusten vaihtoehtoa, joilla on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="125fa-127">In the Saved Settings field on the report request page, the user will see two saved settings options with the same name.</span></span> <span data-ttu-id="125fa-128">Valitusta vaihtoehdosta riippumatta järjestelmä käyttää käyttäjän omia asetuksia.</span><span class="sxs-lookup"><span data-stu-id="125fa-128">However, no matter which option he chooses, the user-specific saved settings will be used.</span></span>

## <a name="see-also"></a><span data-ttu-id="125fa-129">Katso myös</span><span class="sxs-lookup"><span data-stu-id="125fa-129">See Also</span></span>
[<span data-ttu-id="125fa-130">Raporttien käsittely</span><span class="sxs-lookup"><span data-stu-id="125fa-130">Working with Reports</span></span>](ui-work-report.md)  

