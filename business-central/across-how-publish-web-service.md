---
title: Objektien näyttäminen verkkopalveluina
description: Julkaise objektit verkkopalveluina, jolloin niitä voi käyttää heti Business Central -ratkaisussa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/08/2020
ms.author: edupont
ms.openlocfilehash: 2220b5227cfe0e99a53071829096a67b6aeb0521
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754915"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="7faab-103">Verkkopalvelun julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="7faab-103">Publish a Web Service</span></span>

<span data-ttu-id="7faab-104">Verkkopalvelut ovat kevyt tapa tuoda sovelluksen toiminnallisuus erilaisten ulkoisten järjestelmien ja käyttäjien saataville.</span><span class="sxs-lookup"><span data-stu-id="7faab-104">Web services are a lightweight way to make application functionality available to different kinds of external systems and users.</span></span> <span data-ttu-id="7faab-105">Oletusarvoisesti [!INCLUDE[prod_short](includes/prod_short.md)] näyttää useita objekteja verkkopalveluina, että ne voidaan paremmin integroida muihin Microsoft-palveluihin.</span><span class="sxs-lookup"><span data-stu-id="7faab-105">By default, [!INCLUDE[prod_short](includes/prod_short.md)] exposes a number of objects as web services for better integration with other Microsoft services.</span></span> <span data-ttu-id="7faab-106">Voit lisätä muita verkkopalveluita yrityksesi tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="7faab-106">You can add other web services as your business requires.</span></span>  

<span data-ttu-id="7faab-107">Määritä verkkopalvelu [!INCLUDE[prod_short](includes/prod_short.md)] -sivustossa ja julkaise verkkopalvelu siten, että se on todennettujen käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7faab-107">Set up a web service in [!INCLUDE[prod_short](includes/prod_short.md)], and then publish the web service so that it is available to authenticated users.</span></span> <span data-ttu-id="7faab-108">Kaikki valtuutetut käyttäjät voivat käyttää verkkopalveluiden metatietoja, mutta vain käyttäjät, joilla on riittävät oikeudet, voivat käyttää varsinaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="7faab-108">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>  

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="7faab-109">Verkkopalvelun luominen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="7faab-109">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="7faab-110">Seuraavassa kerrotaan, kuinka voit luoda ja julkaista verkkopalvelun.</span><span class="sxs-lookup"><span data-stu-id="7faab-110">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="7faab-111">Verkkopalvelun luominen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="7faab-111">To create and publish a web service</span></span>  

1. <span data-ttu-id="7faab-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Verkkopalvelut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="7faab-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7faab-113">Valitse **Verkkopalvelut**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7faab-113">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="7faab-114">**Codeunit** ja **Sivu** ovat kelvollisia SOAP-verkkopalveluja.</span><span class="sxs-lookup"><span data-stu-id="7faab-114">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="7faab-115">**Sivu** ja **Kysely** ovat kelvollisia OData-verkkopalvelutyyppejä.</span><span class="sxs-lookup"><span data-stu-id="7faab-115">**Page** and **Query** are valid types for OData web services.</span></span> <span data-ttu-id="7faab-116">Versiosta 16.3 lähtien **Codeunit** on myös kelvollinen tyyppi OData v4 -verkkopalveluille, mutta käyttöliittymässä ei näy URL-osoitetta.</span><span class="sxs-lookup"><span data-stu-id="7faab-116">Starting with version 16.3, **Codeunit** is also a valid type for OData v4 web services, but then no URL is shown in the user interface.</span></span> <span data-ttu-id="7faab-117">Jos tietokanta lisäksi sisältää useita yrityksiä, voit valita yhdelle yritykselle kuuluvan objektitunnuksen.</span><span class="sxs-lookup"><span data-stu-id="7faab-117">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="7faab-118">Palvelunimi näkyy verkkopalvelun käyttäjille, ja sen perusteella tunnistetaan ja erotellaan verkkopalvelut, joten nimen on oltava merkityksellinen.</span><span class="sxs-lookup"><span data-stu-id="7faab-118">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="7faab-119">Valitse valintaruutu **Julkaistu**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="7faab-119">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="7faab-120">Kun julkaiset verkkopalvelun, uudet URL-osoitteet näkyvät **OData URL**- ja **SOAP URL** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="7faab-120">When you publish the web service, the **OData URL** and **SOAP URL** fields show the new URLs.</span></span> <span data-ttu-id="7faab-121">Koodayksiköille, jotka ovat alttiina sitoutumattomina OData v4 -toimintoina, URL-kenttiä ei kuitenkaan näytetä.</span><span class="sxs-lookup"><span data-stu-id="7faab-121">However, for codeunits that are exposed as OData v4 unbound actions, the URL fields are not shown.</span></span>  

<span data-ttu-id="7faab-122">Voit testata verkkopalvelua heti valitsemalla linkit **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="7faab-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="7faab-123">Vaihtoehtoisesti kopioi kentän arvo ja tallenna se myöhempää käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="7faab-123">Optionally, copy the value of the field and save it for later use.</span></span> <span data-ttu-id="7faab-124">Voit testata sitoutumattomia OData v4 -toimintoja sisältäviä codeuniteja noudattamalla kehittäjän sisällön [verkkopalvelun käytettävyyden varmistaminen](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) -osan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="7faab-124">To test codeunits that are exposed as OData v4 unbound actions, follow the instructions in the [Verifying web service availability](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) section in the developer content.</span></span>

> [!NOTE]
> <span data-ttu-id="7faab-125">Jos verkkopalveluina näyttämäsi objektit eivät ole käytettävissä [!INCLUDE[prod_short](includes/prod_short.md)]-palvelusta online-muodossa, sinun täytyy merkitä koodissa näkyvät menetelmät muodossa `[Scope('OnPrem')]`.</span><span class="sxs-lookup"><span data-stu-id="7faab-125">If the objects that you expose as web services must not be accessible from [!INCLUDE[prod_short](includes/prod_short.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="7faab-126">Lisätietoja on kohdassa [Alueen määrite](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span><span class="sxs-lookup"><span data-stu-id="7faab-126">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="7faab-127">Verkkopalveluna julkaistu palvelu on ulkoisten osapuolien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7faab-127">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="7faab-128">Voit tarkistaa kyseisen verkkopalvelun saatavuuden selaimen avulla tai valitsemalla linkin **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä **Verkkopalvelut**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="7faab-128">You can verify the availability of that web service by using a browser, or choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="7faab-129">Seuraavassa on kuvattu, miten voit tarkistaa verkkopalvelun käytettävyyden myöhempää käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="7faab-129">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="7faab-130">Verkkopalvelun saatavuuden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="7faab-130">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="7faab-131">Kirjoita selaimeen asianmukainen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="7faab-131">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="7faab-132">Seuraavassa taulukossa on kuvattu URL-osoitteiden tyypit, jotka voi antaa erilaisille verkkopalvelutyypeille.</span><span class="sxs-lookup"><span data-stu-id="7faab-132">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="7faab-133">Tyyppi</span><span class="sxs-lookup"><span data-stu-id="7faab-133">Type</span></span>|<span data-ttu-id="7faab-134">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="7faab-134">Syntax</span></span>|<span data-ttu-id="7faab-135">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="7faab-135">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="7faab-136">SOAP</span><span class="sxs-lookup"><span data-stu-id="7faab-136">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="7faab-137">OData V4</span><span class="sxs-lookup"><span data-stu-id="7faab-137">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="7faab-138">Yrityksen nimi -kentässä huomioidaan kirjainkoko.</span><span class="sxs-lookup"><span data-stu-id="7faab-138">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="7faab-139">Tarkista tiedot, jotka näkyvät selaimessa.</span><span class="sxs-lookup"><span data-stu-id="7faab-139">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="7faab-140">Varmista, että näet luomasi verkkopalvelun nimen.</span><span class="sxs-lookup"><span data-stu-id="7faab-140">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="7faab-141">Kun siirryt verkkopalveluun ja haluat kirjoittaa tiedot takaisin kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)], yrityksen nimi on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="7faab-141">When you access a web service, and you want to write data back to [!INCLUDE[prod_short](includes/prod_short.md)], you must specify the company name.</span></span> <span data-ttu-id="7faab-142">Voit määrittää yrityksen esimerkkien tavoin osana URI:a tai vaihtoehtoisesti osana kyselyparametrejä.</span><span class="sxs-lookup"><span data-stu-id="7faab-142">You can specify the company as part of the URI as shown in the examples; alternatively, specify the company as part of the query parameters.</span></span> <span data-ttu-id="7faab-143">Esimerkiksi seuraavat URI:t osoittavat samaan OData-verkkopalveluun ja molemmat ovat kelvollisia URI-osoitteita.</span><span class="sxs-lookup"><span data-stu-id="7faab-143">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="7faab-144">Katso myös</span><span class="sxs-lookup"><span data-stu-id="7faab-144">See Also</span></span>

[<span data-ttu-id="7faab-145">Hallinta</span><span class="sxs-lookup"><span data-stu-id="7faab-145">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="7faab-146">Kehittäjien Business Central -verkkopalvelut</span><span class="sxs-lookup"><span data-stu-id="7faab-146">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="7faab-147">OData -pyyntörajat</span><span class="sxs-lookup"><span data-stu-id="7faab-147">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
