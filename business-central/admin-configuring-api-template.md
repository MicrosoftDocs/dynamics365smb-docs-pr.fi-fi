---
title: "API-mallien määrittäminen | Microsoft Docs"
description: "Kuvaa vaiheet, jotka sinun täytyy käydä läpi,l jotta voit määrittää Dynamics 365 Business Centralin API-malleja."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 05/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 1695a6950dabc1b2f0a2f85ad9e0c565012c92e1
ms.contentlocale: fi-fi
ms.lasthandoff: 05/17/2018

---

# <a name="configuring-api-templates"></a><span data-ttu-id="cd6c2-103">API-mallien määritys</span><span class="sxs-lookup"><span data-stu-id="cd6c2-103">Configuring API Templates</span></span>
<span data-ttu-id="cd6c2-104">[!INCLUDE[d365fin_md](includes/d365fin_md.md)]:n API-kirjasto on taustalla olevien objektien yksinkertaistettu esitys.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-104">The API library for [!INCLUDE[d365fin_md](includes/d365fin_md.md)] provides a simplified representation of the underlying entities.</span></span> <span data-ttu-id="cd6c2-105">Sovelluksen kaiki ominaisuudet eivät näy liittyvän API:n kautta.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-105">All the properties in the application are not exposed through the associated API.</span></span> <span data-ttu-id="cd6c2-106">**API-asetukset** -ikkunassa voidaan määrittää malleja, joita käytetään täyttämään objektin tyhjät ominaisuudet, kun luot POST-toiminnon API:n kautta</span><span class="sxs-lookup"><span data-stu-id="cd6c2-106">The **API Setup** window allows you to define templates that are used to populate empty properties on an entity when you create a POST action through the API.</span></span> 

<span data-ttu-id="cd6c2-107">Esimerkiksi, jos määritysmalli on määritetty nimikeobjektille luotaessa uutta nimiketietuetta nimikkeiden API:n kautta, kaikki uuden nimikkeen ominaisuudet, joita ei ole määritetty API-kutsussa, täytetään valitusta mallista.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-107">For example, if a configuration template is defined for the item entity, when a new item record is created through the items API, any properties for the new item that are not defined in the API call will be populated from the selected template.</span></span> <span data-ttu-id="cd6c2-108">Jos esimerkiksi **Yleinen tuotteen kirjausryhmä** -kentälle ei ole määritetty arvoa API:n kautta, mutta arvo määritetään valitussa mallissa, tällöin mallissa määritettyä kirjausryhmän arvoa käytetään uuteen nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-108">If, for example, no value is defined for the **Gen. Prod. Posting Group** field through the API, but a value is defined in the selected template, then the posting group value defined in the template will be applied to the new item.</span></span> 

## <a name="setting-up-the-entity-template"></a><span data-ttu-id="cd6c2-109">Objektimallin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cd6c2-109">Setting up the Entity Template</span></span>
<span data-ttu-id="cd6c2-110">Jotta voit käyttää malleja API-kirjaston kanssa, sinun tulee ensin määrittää mallien ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-110">To use templates with the API library, you must first set up and define properties for the templates.</span></span> <span data-ttu-id="cd6c2-111">Voit määrittää nämä mallit **Määritysmallit**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-111">You can set up these templates in the **Configuration Templates** window.</span></span> <span data-ttu-id="cd6c2-112">Lisätietoja on ohjeaiheessa [Asiakastietojen siirtämisen valmisteleminen](admin-use-templates-to-prepare-customer-data-for-migration.md).</span><span class="sxs-lookup"><span data-stu-id="cd6c2-112">For more information, see [Prepare to Migrate Customer Data](admin-use-templates-to-prepare-customer-data-for-migration.md).</span></span> 

## <a name="assign-the-template-to-an-api"></a><span data-ttu-id="cd6c2-113">Mallin liittäminen APIin</span><span class="sxs-lookup"><span data-stu-id="cd6c2-113">Assign the template to an API</span></span>

<span data-ttu-id="cd6c2-114">Voit liittää mallin APIin suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-114">To assign a template to an API, you must go through the following steps.</span></span>

1. <span data-ttu-id="cd6c2-115">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **API-asetukset** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **API Setup**, and choose the related link.</span></span>
2. <span data-ttu-id="cd6c2-116">Valitse **Uusi** ja sitten **Järjestys** tietueen arvoksi.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-116">Choose **New**, and then choose the **Order** value for the record.</span></span>  
<span data-ttu-id="cd6c2-117">Jos API-liittymälle (Sivun tunnus) on valittu useita malleja, mallit otetaan käyttöön järjestyksessä, joka on määritetty **Järjestys**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-117">If there is more than one template selected for an API (Page ID), the templates are applied in the order defined in the **Order** column.</span></span>   
<span data-ttu-id="cd6c2-118">Kun jokaista mallia käytetään, mallissa määritettyjä kenttäarvoja käytetään vain kenttiin, joilla ei ole jo määritettyä arvoa joko eksplisiittisesti tai API-liittymässä tai järjestyksessä aiemmassa mallissa.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-118">When each template is applied, field values defined in the template are only applied to fields that have not already had a value defined, either explicitly in the API, or in a previously applied template in the order.</span></span> 
3. <span data-ttu-id="cd6c2-119">Valitse **Sivun tunnus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-119">Select a **Page ID** value.</span></span>  
<span data-ttu-id="cd6c2-120">Tämä on API:n sivu, johon malli kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-120">This is the page for the API to which the template will be applied.</span></span> <span data-ttu-id="cd6c2-121">**Sivun tunnus** -haku palauttaa kaikkien kirjastossa saatavilla olevien API-liittymien luettelon.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-121">The **Page ID** lookup provides a list of all APIs available in the library.</span></span>
4. <span data-ttu-id="cd6c2-122">Valitse arvo **Mallin koodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-122">Select a value in the **Template Code** field.</span></span>  
<span data-ttu-id="cd6c2-123">Mallikoodi on sen mallin koodi, joka määritettiin **Määritysmallit**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-123">The template code is the code for the template that was defined in the **Configuration Templates** window.</span></span> <span data-ttu-id="cd6c2-124">Määritettyjä mallin arvoja käytetään API-liittymään.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-124">The template values defined are applied to the API.</span></span> 
5. <span data-ttu-id="cd6c2-125">Määritä **Ehdot**-kentässä, mitä mallia pitäisi käyttää.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-125">In the **Conditions** field, specify which template should be applied.</span></span>  
<span data-ttu-id="cd6c2-126">Määritettyä mallia käytetään API:n kautta luotuun uuteen tietueeseen vain jos objektin uudelle esiintymälle jo määritetyt arvot täyttävät **Ehdot**-kentässä määritetyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="cd6c2-126">The defined template is applied to a new record created through the API if, and only if, the conditions defined in the **Conditions** field are met by the values already defined for the new instance of the entity.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd6c2-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="cd6c2-127">See Also</span></span>
[<span data-ttu-id="cd6c2-128">API-dokumentaatio</span><span class="sxs-lookup"><span data-stu-id="cd6c2-128">API Documentation</span></span>](/dynamics-nav/fin-graph)  
<span data-ttu-id="cd6c2-129">[Connect-sovellusten luominen ratkaisulle [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span><span class="sxs-lookup"><span data-stu-id="cd6c2-129">[Developing Connect Apps for [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span></span>  
[<span data-ttu-id="cd6c2-130">API-liittymien ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="cd6c2-130">Enabling the APIs</span></span>](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[<span data-ttu-id="cd6c2-131">API-liittymien päätepisteet</span><span class="sxs-lookup"><span data-stu-id="cd6c2-131">Endpoints for the APIs</span></span>](/dynamics-nav/endpoints-apis-for-dynamics)  
[<span data-ttu-id="cd6c2-132">Yrityksen määrittäminen RapidStart Services -palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="cd6c2-132">Setting Up a Company with RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="cd6c2-133">Hallinta</span><span class="sxs-lookup"><span data-stu-id="cd6c2-133">Administration</span></span>](admin-setup-and-administration.md)
