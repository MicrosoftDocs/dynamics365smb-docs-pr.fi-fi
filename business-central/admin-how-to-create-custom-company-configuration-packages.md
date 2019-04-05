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
ms.date: 12/07/2018
ms.author: sgroespe
ms.openlocfilehash: a51628085e640cc2e5f022272eccb89d5cec38b7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795875"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="cf94d-104">Yrityksen mukautettujen määrityspakettien luominen</span><span class="sxs-lookup"><span data-stu-id="cf94d-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="cf94d-105">Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="cf94d-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="cf94d-106">Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia.</span><span class="sxs-lookup"><span data-stu-id="cf94d-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="cf94d-107">Yleensä määrityspaketti luodaan toiminta-aluetta kohti. Voit esimerkiksi luoda paketin tuotantotoiminnolle.</span><span class="sxs-lookup"><span data-stu-id="cf94d-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="cf94d-108">Niiden avulla voit ottaa käyttöön ja määrittää yrityksen uusia alueita silloin, kun niitä tarvitaan</span><span class="sxs-lookup"><span data-stu-id="cf94d-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="cf94d-109">Toinen vaihtoehto olisi luoda paketti, joka sisältää taulukot, jotka määrittävät asetukset, esim. seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="cf94d-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="cf94d-110">Käyttöomaisuuden asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="cf94d-111">Pääkirjanpidon asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="cf94d-112">Varastonhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-112">Inventory Setup</span></span>  
-   <span data-ttu-id="cf94d-113">Tuotannon asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="cf94d-114">Ostojen ja ostovelkojen asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="cf94d-115">Kontaktienhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-115">Marketing Setup</span></span>  
-   <span data-ttu-id="cf94d-116">Huollon asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-116">Service Setup</span></span>  
-   <span data-ttu-id="cf94d-117">Myyntien ja saamisten asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="cf94d-118">Fyys. varastoinnin asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="cf94d-119">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-119">General Posting Setup</span></span>  
-   <span data-ttu-id="cf94d-120">ALV-kirjausten asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="cf94d-121">Varastokirjauksien asetukset</span><span class="sxs-lookup"><span data-stu-id="cf94d-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="cf94d-122">Jos haluat nähdä asetustaulukoiden täydellisen luettelon, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Manuaalinen määritys** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="cf94d-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="cf94d-123">Yrityksen mukautetun määrityspaketin luominen</span><span class="sxs-lookup"><span data-stu-id="cf94d-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="cf94d-124">Luo uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="cf94d-124">Create a new company.</span></span> <span data-ttu-id="cf94d-125">Lisätietoja on kohdassa [Uusien yritysten luominen Business Centralissa](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="cf94d-125">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="cf94d-126">Määritä uuden yrityksen asetukset tarvitsemallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="cf94d-126">Set up the new company in the way you need.</span></span> <span data-ttu-id="cf94d-127">Täydennä kaikki pakolliset asetustaulukot.</span><span class="sxs-lookup"><span data-stu-id="cf94d-127">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="cf94d-128">Avaa uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="cf94d-128">Open the new company.</span></span>
5. <span data-ttu-id="cf94d-129">Avaa **Määritystyökirja**-sivu.</span><span class="sxs-lookup"><span data-stu-id="cf94d-129">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="cf94d-130">Lisää työkirjaan taulukot, jotka haluat siirtää toiselle yhtiölle.</span><span class="sxs-lookup"><span data-stu-id="cf94d-130">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="cf94d-131">Määritä työkirjan rivit pakettiin.</span><span class="sxs-lookup"><span data-stu-id="cf94d-131">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="cf94d-132">Luo uusi kysely usein käytettyjen asetusten taulukoille.</span><span class="sxs-lookup"><span data-stu-id="cf94d-132">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="cf94d-133">Luominen määritysmallit, jotta on helpompi luoda perustiedot, kuten asiakkaat ja nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="cf94d-133">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="cf94d-134">Vie paketti .rapidstart-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="cf94d-134">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf94d-135">Katso myös</span><span class="sxs-lookup"><span data-stu-id="cf94d-135">See Also</span></span>  
[<span data-ttu-id="cf94d-136">Yrityksen määrittäminen RapidStart Services -palvelun avulla</span><span class="sxs-lookup"><span data-stu-id="cf94d-136">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="cf94d-137">Hallinta</span><span class="sxs-lookup"><span data-stu-id="cf94d-137">Administration</span></span>](admin-setup-and-administration.md)
