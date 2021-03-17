---
title: API-mallien määrittäminen | Microsoft Docs
description: Kuvaa vaiheet, jotka sinun täytyy käydä läpi, jotta voit määrittää Dynamics 365 Business Centralin ohjelmointirajapintamalleja.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 3eeea8976f224911b95e0aad8e084c6a1a13a9c7
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378621"
---
# <a name="configuring-api-templates"></a><span data-ttu-id="8c1b6-103">API-mallien määritys</span><span class="sxs-lookup"><span data-stu-id="8c1b6-103">Configuring API Templates</span></span>
<span data-ttu-id="8c1b6-104">[!INCLUDE[prod_short_md](includes/prod_short.md)]:n API-kirjasto on taustalla olevien objektien yksinkertaistettu esitys.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-104">The API library for [!INCLUDE[prod_short_md](includes/prod_short.md)] provides a simplified representation of the underlying entities.</span></span> <span data-ttu-id="8c1b6-105">Sovelluksen kaiki ominaisuudet eivät näy liittyvän API:n kautta.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-105">All the properties in the application are not exposed through the associated API.</span></span> <span data-ttu-id="8c1b6-106">**API-asetukset** -sivulla voidaan määrittää malleja, joita käytetään täyttämään objektin tyhjät ominaisuudet, kun luot POST-toiminnon API:n kautta</span><span class="sxs-lookup"><span data-stu-id="8c1b6-106">The **API Setup** page allows you to define templates that are used to populate empty properties on an entity when you create a POST action through the API.</span></span> 

<span data-ttu-id="8c1b6-107">Esimerkiksi, jos määritysmalli on määritetty nimikeobjektille luotaessa uutta nimiketietuetta nimikkeiden API:n kautta, kaikki uuden nimikkeen ominaisuudet, joita ei ole määritetty API-kutsussa, täytetään valitusta mallista.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-107">For example, if a configuration template is defined for the item entity, when a new item record is created through the items API, any properties for the new item that are not defined in the API call will be populated from the selected template.</span></span> <span data-ttu-id="8c1b6-108">Jos esimerkiksi **Yleinen tuotteen kirjausryhmä** -kentälle ei ole määritetty arvoa API:n kautta, mutta arvo määritetään valitussa mallissa, tällöin mallissa määritettyä kirjausryhmän arvoa käytetään uuteen nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-108">If, for example, no value is defined for the **Gen. Prod. Posting Group** field through the API, but a value is defined in the selected template, then the posting group value defined in the template will be applied to the new item.</span></span> 

## <a name="setting-up-the-entity-template"></a><span data-ttu-id="8c1b6-109">Objektimallin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8c1b6-109">Setting up the Entity Template</span></span>
<span data-ttu-id="8c1b6-110">Jotta voit käyttää malleja API-kirjaston kanssa, sinun tulee ensin määrittää mallien ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-110">To use templates with the API library, you must first set up and define properties for the templates.</span></span> <span data-ttu-id="8c1b6-111">Voit määrittää nämä mallit **Määritysmallit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-111">You can set up these templates on the **Configuration Templates** page.</span></span> <span data-ttu-id="8c1b6-112">Lisätietoja on ohjeaiheessa [Asiakastietojen siirtämisen valmisteleminen](admin-use-templates-to-prepare-customer-data-for-migration.md).</span><span class="sxs-lookup"><span data-stu-id="8c1b6-112">For more information, see [Prepare to Migrate Customer Data](admin-use-templates-to-prepare-customer-data-for-migration.md).</span></span> 

## <a name="assign-the-template-to-an-api"></a><span data-ttu-id="8c1b6-113">Mallin liittäminen APIin</span><span class="sxs-lookup"><span data-stu-id="8c1b6-113">Assign the template to an API</span></span>

<span data-ttu-id="8c1b6-114">Voit liittää mallin APIin suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-114">To assign a template to an API, you must go through the following steps.</span></span>

1. <span data-ttu-id="8c1b6-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **API-asetukset** ja valitse liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **API Setup**, and choose the related link.</span></span>
2. <span data-ttu-id="8c1b6-116">Valitse **Uusi** ja sitten **Järjestys** tietueen arvoksi.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-116">Choose **New**, and then choose the **Order** value for the record.</span></span>  
<span data-ttu-id="8c1b6-117">Jos API-liittymälle (Sivun tunnus) on valittu useita malleja, mallit otetaan käyttöön järjestyksessä, joka on määritetty **Järjestys**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-117">If there is more than one template selected for an API (Page ID), the templates are applied in the order defined in the **Order** column.</span></span>   
<span data-ttu-id="8c1b6-118">Kun jokaista mallia käytetään, mallissa määritettyjä kenttäarvoja käytetään vain kenttiin, joilla ei ole jo määritettyä arvoa joko eksplisiittisesti tai API-liittymässä tai järjestyksessä aiemmassa mallissa.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-118">When each template is applied, field values defined in the template are only applied to fields that have not already had a value defined, either explicitly in the API, or in a previously applied template in the order.</span></span> 
3. <span data-ttu-id="8c1b6-119">Valitse **Sivun tunnus** -arvo.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-119">Select a **Page ID** value.</span></span>  
<span data-ttu-id="8c1b6-120">Tämä on API:n sivu, johon malli kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-120">This is the page for the API to which the template will be applied.</span></span> <span data-ttu-id="8c1b6-121">**Sivun tunnus** -haku palauttaa kaikkien kirjastossa saatavilla olevien API-liittymien luettelon.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-121">The **Page ID** lookup provides a list of all APIs available in the library.</span></span>
4. <span data-ttu-id="8c1b6-122">Valitse arvo **Mallin koodi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-122">Select a value in the **Template Code** field.</span></span>  
<span data-ttu-id="8c1b6-123">Mallikoodi on sen mallin koodi, joka määritettiin **Määritysmallit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-123">The template code is the code for the template that was defined on the **Configuration Templates** page.</span></span> <span data-ttu-id="8c1b6-124">Määritettyjä mallin arvoja käytetään API-liittymään.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-124">The template values defined are applied to the API.</span></span> 
5. <span data-ttu-id="8c1b6-125">Määritä **Ehdot**-kentässä, mitä mallia pitäisi käyttää.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-125">In the **Conditions** field, specify which template should be applied.</span></span>  
<span data-ttu-id="8c1b6-126">Määritettyä mallia käytetään API:n kautta luotuun uuteen tietueeseen vain jos objektin uudelle esiintymälle jo määritetyt arvot täyttävät **Ehdot**-kentässä määritetyt ehdot.</span><span class="sxs-lookup"><span data-stu-id="8c1b6-126">The defined template is applied to a new record created through the API if, and only if, the conditions defined in the **Conditions** field are met by the values already defined for the new instance of the entity.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c1b6-127">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8c1b6-127">See Also</span></span>
[<span data-ttu-id="8c1b6-128">API-dokumentaatio</span><span class="sxs-lookup"><span data-stu-id="8c1b6-128">API Documentation</span></span>](/dynamics-nav/fin-graph)  
<span data-ttu-id="8c1b6-129">[Connect-sovellusten luominen ratkaisulle [!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span><span class="sxs-lookup"><span data-stu-id="8c1b6-129">[Developing Connect Apps for [!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span></span>  
[<span data-ttu-id="8c1b6-130">API-liittymien ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="8c1b6-130">Enabling the APIs</span></span>](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[<span data-ttu-id="8c1b6-131">API-liittymien päätepisteet</span><span class="sxs-lookup"><span data-stu-id="8c1b6-131">Endpoints for the APIs</span></span>](/dynamics-nav/endpoints-apis-for-dynamics)  
[<span data-ttu-id="8c1b6-132">Yrityksen määrittäminen RapidStart Servicesin avulla</span><span class="sxs-lookup"><span data-stu-id="8c1b6-132">Setting Up a Company with RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="8c1b6-133">Hallinta</span><span class="sxs-lookup"><span data-stu-id="8c1b6-133">Administration</span></span>](admin-setup-and-administration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]