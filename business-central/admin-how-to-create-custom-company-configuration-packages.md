---
title: Yrityksen mukautettujen määrityspakettien luominen | Microsoft Docs
description: Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa. Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 511281b5f4d8c7437324ed123a5a5a62bd4cc51d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783650"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="83add-104">Yrityksen mukautettujen määrityspakettien luominen</span><span class="sxs-lookup"><span data-stu-id="83add-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="83add-105">Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa.</span><span class="sxs-lookup"><span data-stu-id="83add-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="83add-106">Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia.</span><span class="sxs-lookup"><span data-stu-id="83add-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="83add-107">Yleensä määrityspaketti luodaan toiminta-aluetta kohti. Voit esimerkiksi luoda paketin tuotantotoiminnolle.</span><span class="sxs-lookup"><span data-stu-id="83add-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="83add-108">Niiden avulla voit ottaa käyttöön ja määrittää yrityksen uusia alueita silloin, kun niitä tarvitaan</span><span class="sxs-lookup"><span data-stu-id="83add-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="83add-109">Toinen vaihtoehto olisi luoda paketti, joka sisältää taulukot, jotka määrittävät asetukset, esim. seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="83add-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="83add-110">Käyttöomaisuuden asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="83add-111">Pääkirjanpidon asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="83add-112">Varastonhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-112">Inventory Setup</span></span>  
-   <span data-ttu-id="83add-113">Tuotannon asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="83add-114">Ostojen ja ostovelkojen asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="83add-115">Kontaktienhallinnan asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-115">Marketing Setup</span></span>  
-   <span data-ttu-id="83add-116">Huollon asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-116">Service Setup</span></span>  
-   <span data-ttu-id="83add-117">Myyntien ja saamisten asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="83add-118">Fyys. varastoinnin asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="83add-119">Yleiset kirjausasetukset</span><span class="sxs-lookup"><span data-stu-id="83add-119">General Posting Setup</span></span>  
-   <span data-ttu-id="83add-120">ALV-kirjausten asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="83add-121">Varastokirjauksien asetukset</span><span class="sxs-lookup"><span data-stu-id="83add-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="83add-122">Jos haluat nähdä asetustaulukoiden täydellisen luettelon, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, kirjoita **Manuaalinen määritys** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="83add-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="83add-123">Käytä harkintaa, jos valitset taulukkoja tai kenttiä, joilla on sama ajallinen nimi mutta jotka eroavat erikoismerkkien osalta, kuten %, &, <, >, (ja).</span><span class="sxs-lookup"><span data-stu-id="83add-123">Use caution if you choose tables or fields that have the same temporal name but are differentiated by special characters, such as %, &, <, >, (, and ).</span></span> <span data-ttu-id="83add-124">Esimerkiksi taulukossa "XYZ" voi olla "kenttä 1" ja "kenttä 1 %" -kentät.</span><span class="sxs-lookup"><span data-stu-id="83add-124">For example, table "XYZ" might contain the "Field 1" and "Field 1%" fields.</span></span>
>
> <span data-ttu-id="83add-125">XML-suoritin hyväksyy vain tietyt erikoismerkit ja poistaa ne, joita se ei hyväksy.</span><span class="sxs-lookup"><span data-stu-id="83add-125">The XML processor accepts only some special characters, and will remove those it does not.</span></span> <span data-ttu-id="83add-126">Jos poistat erikoismerkin, esimerkiksi %-merkin "Kenttä 1 %" -esimerkissä, tuloksena on kaksi tai useampia samannimistä taulukkoja tai kenttiä. Virhe ilmenee, kun viet tai tuot kokoonpanopaketin.</span><span class="sxs-lookup"><span data-stu-id="83add-126">If removing a special character, such as the % sign in "Field 1%," results in two or more tables or fields with the same name an error will occur when you export or import a configuration package.</span></span>

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="83add-127">Yrityksen mukautetun määrityspaketin luominen</span><span class="sxs-lookup"><span data-stu-id="83add-127">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="83add-128">Luo uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="83add-128">Create a new company.</span></span> <span data-ttu-id="83add-129">Lisätietoja on kohdassa [Uusien yritysten luominen Business Centralissa](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="83add-129">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="83add-130">Määritä uuden yrityksen asetukset tarvitsemallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="83add-130">Set up the new company in the way you need.</span></span> <span data-ttu-id="83add-131">Täydennä kaikki pakolliset asetustaulukot.</span><span class="sxs-lookup"><span data-stu-id="83add-131">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="83add-132">Avaa uusi yritys.</span><span class="sxs-lookup"><span data-stu-id="83add-132">Open the new company.</span></span>
5. <span data-ttu-id="83add-133">Avaa **Määritystyökirja**-sivu.</span><span class="sxs-lookup"><span data-stu-id="83add-133">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="83add-134">Lisää työkirjaan taulukot, jotka haluat siirtää toiselle yhtiölle.</span><span class="sxs-lookup"><span data-stu-id="83add-134">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="83add-135">Määritä työkirjan rivit pakettiin.</span><span class="sxs-lookup"><span data-stu-id="83add-135">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="83add-136">Luo uusi kysely usein käytettyjen asetusten taulukoille.</span><span class="sxs-lookup"><span data-stu-id="83add-136">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="83add-137">Luominen määritysmallit, jotta on helpompi luoda perustiedot, kuten asiakkaat ja nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="83add-137">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="83add-138">Vie paketti .rapidstart-tiedostona.</span><span class="sxs-lookup"><span data-stu-id="83add-138">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="83add-139">Katso myös</span><span class="sxs-lookup"><span data-stu-id="83add-139">See Also</span></span>  
[<span data-ttu-id="83add-140">Yrityksen määrittäminen RapidStart Servicesin avulla</span><span class="sxs-lookup"><span data-stu-id="83add-140">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="83add-141">Hallinta</span><span class="sxs-lookup"><span data-stu-id="83add-141">Administration</span></span>](admin-setup-and-administration.md)
