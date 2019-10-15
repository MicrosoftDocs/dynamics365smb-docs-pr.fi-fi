---
title: Yrityksen mukautettujen määrityspakettien luominen | Microsoft Docs
description: Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa. Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6fd35133d16056b947db6680cc9a76cfccaa6a3c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308070"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="6a360-104">Yrityksen mukautettujen määrityspakettien luominen</span><span class="sxs-lookup"><span data-stu-id="6a360-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="6a360-105">Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="6a360-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="6a360-106">Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia.</span><span class="sxs-lookup"><span data-stu-id="6a360-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="6a360-107">Yleensä määrityspaketti luodaan toiminta-aluetta kohti. Voit esimerkiksi luoda paketin tuotantotoiminnolle.</span><span class="sxs-lookup"><span data-stu-id="6a360-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="6a360-108">Niiden avulla voit ottaa käyttöön ja määrittää yrityksen uusia alueita silloin, kun niitä tarvitaan</span><span class="sxs-lookup"><span data-stu-id="6a360-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="6a360-109">Toinen vaihtoehto olisi luoda paketti, joka sisältää taulukot, jotka määrittävät asetukset, esim. seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6a360-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="6a360-110">Käyttöomaisuuden asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="6a360-111">Pääkirjanpidon asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="6a360-112">Varastonhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-112">Inventory Setup</span></span>  
-   <span data-ttu-id="6a360-113">Tuotannon asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="6a360-114">Ostojen ja ostovelkojen asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="6a360-115">Kontaktienhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-115">Marketing Setup</span></span>  
-   <span data-ttu-id="6a360-116">Huollon asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-116">Service Setup</span></span>  
-   <span data-ttu-id="6a360-117">Myyntien ja saamisten asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="6a360-118">Fyys. varastoinnin asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="6a360-119">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-119">General Posting Setup</span></span>  
-   <span data-ttu-id="6a360-120">ALV-kirjausten asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="6a360-121">Varastokirjauksien asetukset</span><span class="sxs-lookup"><span data-stu-id="6a360-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="6a360-122">Jos haluat nähdä asetustaulukoiden täydellisen luettelon, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Manuaalinen määritys** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="6a360-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="6a360-123">Yrityksen mukautetun määrityspaketin luominen</span><span class="sxs-lookup"><span data-stu-id="6a360-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="6a360-124">Luo uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="6a360-124">Create a new company.</span></span> <span data-ttu-id="6a360-125">Lisätietoja on kohdassa [Uusien yritysten luominen Business Centralissa](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="6a360-125">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="6a360-126">Määritä uuden yrityksen asetukset tarvitsemallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="6a360-126">Set up the new company in the way you need.</span></span> <span data-ttu-id="6a360-127">Täydennä kaikki pakolliset asetustaulukot.</span><span class="sxs-lookup"><span data-stu-id="6a360-127">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="6a360-128">Avaa uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="6a360-128">Open the new company.</span></span>
5. <span data-ttu-id="6a360-129">Avaa **Määritystyökirja**-sivu.</span><span class="sxs-lookup"><span data-stu-id="6a360-129">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="6a360-130">Lisää työkirjaan taulukot, jotka haluat siirtää toiselle yhtiölle.</span><span class="sxs-lookup"><span data-stu-id="6a360-130">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="6a360-131">Määritä työkirjan rivit pakettiin.</span><span class="sxs-lookup"><span data-stu-id="6a360-131">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="6a360-132">Luo uusi kysely usein käytettyjen asetusten taulukoille.</span><span class="sxs-lookup"><span data-stu-id="6a360-132">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="6a360-133">Luominen määritysmallit, jotta on helpompi luoda perustiedot, kuten asiakkaat ja nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="6a360-133">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="6a360-134">Vie paketti .rapidstart-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="6a360-134">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6a360-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="6a360-135">See Also</span></span>  
[<span data-ttu-id="6a360-136">Yrityksen määrittäminen RapidStart Servicesin avulla</span><span class="sxs-lookup"><span data-stu-id="6a360-136">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="6a360-137">Hallinta</span><span class="sxs-lookup"><span data-stu-id="6a360-137">Administration</span></span>](admin-setup-and-administration.md)
