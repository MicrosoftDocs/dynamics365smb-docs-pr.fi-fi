---
title: "Yrityksen mukautettujen määrityspakettien luominen | Microsoft Docs"
description: "Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa. Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia."
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
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 868972e4d53d858834ba5985a3de3ffa1d4dcc6b
ms.contentlocale: fi-fi
ms.lasthandoff: 11/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="778e6-104">Yrityksen mukautettujen määrityspakettien luominen</span><span class="sxs-lookup"><span data-stu-id="778e6-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="778e6-105">Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="778e6-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="778e6-106">Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia.</span><span class="sxs-lookup"><span data-stu-id="778e6-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="778e6-107">Yleensä määrityspaketti luodaan toiminta-aluetta kohti. Voit esimerkiksi luoda paketin tuotantotoiminnolle.</span><span class="sxs-lookup"><span data-stu-id="778e6-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="778e6-108">Niiden avulla voit ottaa käyttöön ja määrittää yrityksen uusia alueita silloin, kun niitä tarvitaan</span><span class="sxs-lookup"><span data-stu-id="778e6-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="778e6-109">Toinen vaihtoehto olisi luoda paketti, joka sisältää taulukot, jotka määrittävät asetukset, esim. seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="778e6-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="778e6-110">Käyttöomaisuuden asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="778e6-111">Pääkirjanpidon asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="778e6-112">Varastonhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-112">Inventory Setup</span></span>  
-   <span data-ttu-id="778e6-113">Tuotannon asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="778e6-114">Ostojen ja ostovelkojen asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="778e6-115">Kontaktienhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-115">Marketing Setup</span></span>  
-   <span data-ttu-id="778e6-116">Huollon asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-116">Service Setup</span></span>  
-   <span data-ttu-id="778e6-117">Myyntien ja saamisten asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="778e6-118">Fyys. varastoinnin asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="778e6-119">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-119">General Posting Setup</span></span>  
-   <span data-ttu-id="778e6-120">ALV-kirjausten asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="778e6-121">Varastokirjauksien asetukset</span><span class="sxs-lookup"><span data-stu-id="778e6-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="778e6-122">Jos haluat nähdä asetustaulukoiden täydellisen luettelon, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="778e6-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="778e6-123">Yrityksen mukautetun määrityspaketin luominen</span><span class="sxs-lookup"><span data-stu-id="778e6-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="778e6-124">Luo uusi [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="778e6-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="778e6-125">***EI MAHDOLLISTA - linkki Uuden vuokraajan luominen -ohjeeseen***.</span><span class="sxs-lookup"><span data-stu-id="778e6-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="778e6-126">Luo uusi yritys toimialan tai ratkaisun mallin.</span><span class="sxs-lookup"><span data-stu-id="778e6-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="778e6-127">Lisätietoja on ohjeaiheessa [Uuden yrityksen luominen](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="778e6-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="778e6-128">Määritä uuden yrityksen asetukset tarvitsemallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="778e6-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="778e6-129">Täydennä kaikki pakolliset asetustaulukot.</span><span class="sxs-lookup"><span data-stu-id="778e6-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="778e6-130">Avaa uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="778e6-130">Open the new company.</span></span>
5. <span data-ttu-id="778e6-131">Avaa **Määritystyökirja**-sivu.</span><span class="sxs-lookup"><span data-stu-id="778e6-131">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="778e6-132">Lisää työkirjaan taulukot, jotka haluat siirtää toiselle yhtiölle.</span><span class="sxs-lookup"><span data-stu-id="778e6-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="778e6-133">Määritä työkirjan rivit pakettiin.</span><span class="sxs-lookup"><span data-stu-id="778e6-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="778e6-134">Luo uusi kysely usein käytettyjen asetusten taulukoille.</span><span class="sxs-lookup"><span data-stu-id="778e6-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="778e6-135">Luominen määritysmallit, jotta on helpompi luoda perustiedot, kuten asiakkaat ja nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="778e6-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="778e6-136">Vie paketti .rapidstart-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="778e6-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="778e6-137">Katso myös</span><span class="sxs-lookup"><span data-stu-id="778e6-137">See Also</span></span>  
[<span data-ttu-id="778e6-138">Yrityksen määrittäminen RapidStart Services -palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="778e6-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="778e6-139">Hallinta</span><span class="sxs-lookup"><span data-stu-id="778e6-139">Administration</span></span>](admin-setup-and-administration.md)

