---
title: Objektien näyttäminen verkkopalveluina | Microsoft Docs
description: Julkaise objektit verkkopalveluina, jolloin niitä voi käyttää heti Business Central -ratkaisussa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 05/19/2020
ms.author: edupont
ms.openlocfilehash: c9f12f2b15c379ad1f4765f1a20e773150f33b84
ms.sourcegitcommit: d4a77522859c5561c1f3dc43178d45657ffa31b5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/26/2020
ms.locfileid: "3402451"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="e78dc-103">Verkkopalvelun julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="e78dc-103">Publish a Web Service</span></span>

<span data-ttu-id="e78dc-104">Verkkopalvelut ovat kevyt tapa tuoda sovelluksen toiminnallisuus useiden ulkoisten järjestelmien ja käyttäjien saataville.</span><span class="sxs-lookup"><span data-stu-id="e78dc-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e78dc-105">sisältää useita objekteja, jotka näytetään oletusarvoisesti verkkopalveluina, koska ne on integroitu muiden Microsoftin palvelujen kanssa, mutta voit lisätä myös muita verkkopalveluja.</span><span class="sxs-lookup"><span data-stu-id="e78dc-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="e78dc-106">Verkkopalvelu määritetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="e78dc-106">You set up a web service in the [!INCLUDE[d365fin](includes/d365fin_md.md)] client.</span></span> <span data-ttu-id="e78dc-107">Sinun tulee sitten julkaista verkkopalvelu, jotta se on saatavilla huoltopyyntöjen käytettäväksi verkon välityksellä.</span><span class="sxs-lookup"><span data-stu-id="e78dc-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="e78dc-108">Käyttäjät löytävät verkkopalvelut osoittamalla selainta palvelinsijainnissa ja pyytämällä luettelon käytettävissä olevista palveluista.</span><span class="sxs-lookup"><span data-stu-id="e78dc-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="e78dc-109">Kun julkaiset verkkopalvelun, se tulee välittömästi käyttöön todennetuille käyttäjille verkon kautta.</span><span class="sxs-lookup"><span data-stu-id="e78dc-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="e78dc-110">Kaikki valtuutetut käyttäjät voivat käyttää verkkopalveluiden metatietoja, mutta vain käyttäjät, joilla on riittävät oikeudet, voivat käyttää varsinaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="e78dc-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="e78dc-111">Verkkopalvelun luominen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="e78dc-111">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="e78dc-112">Seuraavassa kerrotaan, kuinka voit luoda ja julkaista verkkopalvelun.</span><span class="sxs-lookup"><span data-stu-id="e78dc-112">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="e78dc-113">Verkkopalvelun luominen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="e78dc-113">To create and publish a web service</span></span>  

1. <span data-ttu-id="e78dc-114">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Verkkopalvelut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="e78dc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e78dc-115">Valitse **Verkkopalvelut**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e78dc-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="e78dc-116">**Koodiyksikkö** ja **Sivu** ovat kelvollisia SOAP-verkkopalveluja.</span><span class="sxs-lookup"><span data-stu-id="e78dc-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="e78dc-117">**Sivu** ja **Kysely** ovat kelvollisia OData-verkkopalvelutyyppejä.</span><span class="sxs-lookup"><span data-stu-id="e78dc-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    > <span data-ttu-id="e78dc-118">Jos tietokanta lisäksi sisältää useita yrityksiä, voit valita yhdelle yritykselle kuuluvan objektitunnuksen.</span><span class="sxs-lookup"><span data-stu-id="e78dc-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="e78dc-119">Palvelunimi näkyy verkkopalvelun käyttäjille, ja sen perusteella tunnistetaan ja erotellaan verkkopalvelut, joten nimen on oltava merkityksellinen.</span><span class="sxs-lookup"><span data-stu-id="e78dc-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="e78dc-120">Valitse valintaruutu **Julkaistu**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="e78dc-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="e78dc-121">Kun julkaiset verkkopalvelun, **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä näkyvät verkkopalvelua varten luodut URL-osoitteet.</span><span class="sxs-lookup"><span data-stu-id="e78dc-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="e78dc-122">Voit testata verkkopalvelua heti valitsemalla linkit **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä.</span><span class="sxs-lookup"><span data-stu-id="e78dc-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="e78dc-123">Vaihtoehtoisesti voit kopioida kentän arvon ja tallentaa sen myöhempää käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="e78dc-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

> [!NOTE]
> <span data-ttu-id="e78dc-124">Jos verkkopalveluina näyttämäsi objektit eivät ole käytettävissä [!INCLUDE [prodshort](includes/prodshort.md)]-palvelusta online-muodossa, sinun täytyy merkitä koodissa näkyvät menetelmät muodossa `[Scope('OnPrem')]`.</span><span class="sxs-lookup"><span data-stu-id="e78dc-124">If the objects that you expose as web services must not be accessible from [!INCLUDE [prodshort](includes/prodshort.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="e78dc-125">Lisätietoja on kohdassa [Alueen määrite](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span><span class="sxs-lookup"><span data-stu-id="e78dc-125">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="e78dc-126">Verkkopalveluna julkaistu palvelu on ulkoisten osapuolien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e78dc-126">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="e78dc-127">Voit tarkistaa kyseisen verkkopalvelun saatavuuden selaimen avulla tai valitsemalla linkin **ODatan URL-osoite** - ja **SOAP:n URL-osoite** -kentissä **Verkkopalvelut**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="e78dc-127">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="e78dc-128">Seuraavassa on kuvattu, miten voit tarkistaa verkkopalvelun käytettävyyden myöhempää käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="e78dc-128">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="e78dc-129">Verkkopalvelun saatavuuden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="e78dc-129">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="e78dc-130">Kirjoita selaimeen asianmukainen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="e78dc-130">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="e78dc-131">Seuraavassa taulukossa on kuvattu URL-osoitteiden tyypit, jotka voi antaa erilaisille verkkopalvelutyypeille.</span><span class="sxs-lookup"><span data-stu-id="e78dc-131">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="e78dc-132">Tyyppi</span><span class="sxs-lookup"><span data-stu-id="e78dc-132">Type</span></span>|<span data-ttu-id="e78dc-133">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="e78dc-133">Syntax</span></span>|<span data-ttu-id="e78dc-134">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="e78dc-134">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="e78dc-135">SOAP</span><span class="sxs-lookup"><span data-stu-id="e78dc-135">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="e78dc-136">OData V4</span><span class="sxs-lookup"><span data-stu-id="e78dc-136">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="e78dc-137">Yrityksen nimi -kentässä huomioidaan kirjainkoko.</span><span class="sxs-lookup"><span data-stu-id="e78dc-137">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="e78dc-138">Tarkista tiedot, jotka näkyvät selaimessa.</span><span class="sxs-lookup"><span data-stu-id="e78dc-138">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="e78dc-139">Varmista, että näet luomasi verkkopalvelun nimen.</span><span class="sxs-lookup"><span data-stu-id="e78dc-139">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="e78dc-140">Kun siirryt verkkopalveluun ja haluat kirjoittaa tiedot takaisin kohteeseen [!INCLUDE[d365fin](includes/d365fin_md.md)], yrityksen nimi on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="e78dc-140">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="e78dc-141">Voit määrittää yrityksen esimerkkien tavoin osana URI:a tai osana kyselyparametrejä.</span><span class="sxs-lookup"><span data-stu-id="e78dc-141">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="e78dc-142">Esimerkiksi seuraavat URI:t osoittavat samaan OData-verkkopalveluun ja molemmat ovat kelvollisia URI-osoitteita.</span><span class="sxs-lookup"><span data-stu-id="e78dc-142">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="e78dc-143">Katso myös</span><span class="sxs-lookup"><span data-stu-id="e78dc-143">See Also</span></span>

[<span data-ttu-id="e78dc-144">Hallinta</span><span class="sxs-lookup"><span data-stu-id="e78dc-144">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="e78dc-145">Kehittäjien Business Central -verkkopalvelut</span><span class="sxs-lookup"><span data-stu-id="e78dc-145">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="e78dc-146">OData -pyyntörajat</span><span class="sxs-lookup"><span data-stu-id="e78dc-146">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
