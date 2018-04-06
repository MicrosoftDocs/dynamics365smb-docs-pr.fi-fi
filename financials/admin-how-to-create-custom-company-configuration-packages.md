---
title: "Yrityksen mukautettujen määrityspakettien luominen | Microsoft Docs"
description: "Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa. Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 37fe7a482b88626adff1ef16496a785399d19a8d
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="87850-104">Yrityksen mukautettujen määrityspakettien luominen</span><span class="sxs-lookup"><span data-stu-id="87850-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="87850-105">Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="87850-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="87850-106">Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia.</span><span class="sxs-lookup"><span data-stu-id="87850-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="87850-107">Yleensä määrityspaketti luodaan toiminta-aluetta kohti. Voit esimerkiksi luoda paketin tuotantotoiminnolle.</span><span class="sxs-lookup"><span data-stu-id="87850-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="87850-108">Niiden avulla voit ottaa käyttöön ja määrittää yrityksen uusia alueita silloin, kun niitä tarvitaan</span><span class="sxs-lookup"><span data-stu-id="87850-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="87850-109">Toinen vaihtoehto olisi luoda paketti, joka sisältää taulukot, jotka määrittävät asetukset, esim. seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="87850-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="87850-110">Käyttöomaisuuden asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="87850-111">Pääkirjanpidon asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="87850-112">Varastonhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-112">Inventory Setup</span></span>  
-   <span data-ttu-id="87850-113">Tuotannon asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="87850-114">Ostojen ja ostovelkojen asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="87850-115">Kontaktienhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-115">Marketing Setup</span></span>  
-   <span data-ttu-id="87850-116">Huollon asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-116">Service Setup</span></span>  
-   <span data-ttu-id="87850-117">Myyntien ja saamisten asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="87850-118">Fyys. varastoinnin asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="87850-119">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="87850-119">General Posting Setup</span></span>  
-   <span data-ttu-id="87850-120">ALV-kirjausten asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="87850-121">Varastokirjauksien asetukset</span><span class="sxs-lookup"><span data-stu-id="87850-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="87850-122">Näet asetustaulukoiden täydellisen luettelon valitsemalla ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvakkeen, syöttämällä **Asetukset** ja valitsemalla sitten aiheeseen liittyvän linkin.</span><span class="sxs-lookup"><span data-stu-id="87850-122">To see a complete list of setup tables, Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="87850-123">Yrityksen mukautetun määrityspaketin luominen</span><span class="sxs-lookup"><span data-stu-id="87850-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="87850-124">Luo uusi [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="87850-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="87850-125">***EI MAHDOLLISTA - linkki Uuden vuokraajan luominen -ohjeeseen***.</span><span class="sxs-lookup"><span data-stu-id="87850-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="87850-126">Luo uusi yritys toimialan tai ratkaisun mallin.</span><span class="sxs-lookup"><span data-stu-id="87850-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="87850-127">Lisätietoja on ohjeaiheessa [Uuden yrityksen luominen](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="87850-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="87850-128">Määritä uuden yrityksen asetukset tarvitsemallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="87850-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="87850-129">Täydennä kaikki pakolliset asetustaulukot.</span><span class="sxs-lookup"><span data-stu-id="87850-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="87850-130">Avaa uusi yritys</span><span class="sxs-lookup"><span data-stu-id="87850-130">Open the new company.</span></span>
5. <span data-ttu-id="87850-131">Avaa **Määritystyökirjat**-ikkuna.</span><span class="sxs-lookup"><span data-stu-id="87850-131">Open the **Configuration Worksheet** window.</span></span>  
6.  <span data-ttu-id="87850-132">Lisää työkirjaan taulukot, jotka haluat siirtää toiselle yhtiölle.</span><span class="sxs-lookup"><span data-stu-id="87850-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="87850-133">Määritä työkirjan rivit pakettiin.</span><span class="sxs-lookup"><span data-stu-id="87850-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="87850-134">Luo uusi kysely usein käytettyjen asetusten taulukoille.</span><span class="sxs-lookup"><span data-stu-id="87850-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="87850-135">Luominen määritysmallit, jotta on helpompi luoda perustiedot, kuten asiakkaat ja nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="87850-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="87850-136">Vie paketti .rapidstart-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="87850-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="87850-137">Katso myös</span><span class="sxs-lookup"><span data-stu-id="87850-137">See Also</span></span>  
[<span data-ttu-id="87850-138">Yrityksen määrittäminen RapidStart Services -palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="87850-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="87850-139">Hallinta</span><span class="sxs-lookup"><span data-stu-id="87850-139">Administration</span></span>](admin-setup-and-administration.md)

