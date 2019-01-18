---
title: Olemassa olevien tietokantatietojen tarkistaminen ja mukauttaminen | Microsoft Docs
description: "Kun luot kokoonpanonpaketin ratkaisua varten, voit tarkastella ja mukauttaa käytettävissä olevia tietokannan tietoja vastaamaan asiakkaan tarpeita. Tietokannan taulukolla on oltava siihen liittyvä sivu."
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
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f49d437e03ecf45a234574530f1e65d93584dea
ms.contentlocale: fi-fi
ms.lasthandoff: 12/11/2018

---
# <a name="review-and-customize-existing-database-data"></a><span data-ttu-id="b964e-104">Olemassa olevien tietokantatietojen tarkistaminen ja mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="b964e-104">Review and Customize Existing Database Data</span></span>
<span data-ttu-id="b964e-105">Kun luot kokoonpanonpaketin ratkaisua varten, voit tarkastella ja mukauttaa käytettävissä olevia tietokannan tietoja vastaamaan asiakkaan tarpeita.</span><span class="sxs-lookup"><span data-stu-id="b964e-105">As you create a configuration package for a solution, you can view and customize the available database data to suit your customer needs.</span></span> <span data-ttu-id="b964e-106">Tietokannan taulukolla on oltava siihen liittyvä sivu.</span><span class="sxs-lookup"><span data-stu-id="b964e-106">The database table has to have an associated page.</span></span>  

### <a name="to-customize-data-in-the-database"></a><span data-ttu-id="b964e-107">Mukauta tiedot tietokantaan</span><span class="sxs-lookup"><span data-stu-id="b964e-107">To customize data in the database</span></span>  

1.  <span data-ttu-id="b964e-108">Etsi määritystyökirjasta taulukot, joiden tietoja haluat tarkastella tai muokata.</span><span class="sxs-lookup"><span data-stu-id="b964e-108">In the configuration worksheet, identify the tables whose data that you want to view or customize.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="b964e-109">Varmista, että jokaiseen taulukkoon on määritetty sivun tunnus.</span><span class="sxs-lookup"><span data-stu-id="b964e-109">Make sure that each table has a page ID assigned to it.</span></span> <span data-ttu-id="b964e-110">Tämä arvo on täytetty automaattisesti vakiomuotoisissa [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukoissa.</span><span class="sxs-lookup"><span data-stu-id="b964e-110">For standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables, this value is automatically filled in.</span></span> <span data-ttu-id="b964e-111">Mukautetuille taulukoille tunnus on kuitenkin annettava.</span><span class="sxs-lookup"><span data-stu-id="b964e-111">For custom tables, you have to provide the ID.</span></span>  

2.  <span data-ttu-id="b964e-112">Valitse **Toiminnot**-välilehden **Näytä**-ryhmässä **Tietokannan tiedot**.</span><span class="sxs-lookup"><span data-stu-id="b964e-112">On the **Actions** tab, in the **Show** group, choose **Database Data**.</span></span>  

     <span data-ttu-id="b964e-113">Sivun [!INCLUDE[d365fin](includes/d365fin_md.md)] -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="b964e-113">The [!INCLUDE[d365fin](includes/d365fin_md.md)] page for the page opens.</span></span>  

3.  <span data-ttu-id="b964e-114">Tarkastele käytettävissä olevia tietoja</span><span class="sxs-lookup"><span data-stu-id="b964e-114">Review the available information.</span></span> <span data-ttu-id="b964e-115">Muokkaa sitä tarpeen mukaan poistamalla epäolennaiset tietueet tai lisäämällä uusia.</span><span class="sxs-lookup"><span data-stu-id="b964e-115">Modify it as necessary by deleting records that are not relevant or by adding new ones.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b964e-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="b964e-116">See Also</span></span>  
 [<span data-ttu-id="b964e-117">Yrityksen määrittämisen hallinta työkirjassa</span><span class="sxs-lookup"><span data-stu-id="b964e-117">Manage Company Configuration in a Worksheet</span></span>](admin-how-to-manage-company-configuration-in-a-worksheet.md)

