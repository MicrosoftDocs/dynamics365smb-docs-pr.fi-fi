---
title: Olemassa olevien tietokantatietojen tarkistaminen ja mukauttaminen | Microsoft Docs
description: Kun luot kokoonpanonpaketin ratkaisua varten, voit tarkastella ja mukauttaa käytettävissä olevia tietokannan tietoja vastaamaan asiakkaan tarpeita. Tietokannan taulukolla on oltava siihen liittyvä sivu.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.openlocfilehash: 95b16dc77bcdb0051447a4f153dd720661c52cf9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244559"
---
# <a name="review-and-customize-existing-database-data"></a><span data-ttu-id="1d1c1-104">Olemassa olevien tietokantatietojen tarkistaminen ja mukauttaminen</span><span class="sxs-lookup"><span data-stu-id="1d1c1-104">Review and Customize Existing Database Data</span></span>
<span data-ttu-id="1d1c1-105">Kun luot kokoonpanonpaketin ratkaisua varten, voit tarkastella ja mukauttaa käytettävissä olevia tietokannan tietoja vastaamaan asiakkaan tarpeita.</span><span class="sxs-lookup"><span data-stu-id="1d1c1-105">As you create a configuration package for a solution, you can view and customize the available database data to suit your customer needs.</span></span> <span data-ttu-id="1d1c1-106">Tietokannan taulukolla on oltava siihen liittyvä sivu.</span><span class="sxs-lookup"><span data-stu-id="1d1c1-106">The database table has to have an associated page.</span></span>  

### <a name="to-customize-data-in-the-database"></a><span data-ttu-id="1d1c1-107">Mukauta tiedot tietokantaan</span><span class="sxs-lookup"><span data-stu-id="1d1c1-107">To customize data in the database</span></span>  

1.  <span data-ttu-id="1d1c1-108">Etsi määritystyökirjasta taulukot, joiden tietoja haluat tarkastella tai muokata.</span><span class="sxs-lookup"><span data-stu-id="1d1c1-108">In the configuration worksheet, identify the tables whose data that you want to view or customize.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="1d1c1-109">Varmista, että jokaiseen taulukkoon on määritetty sivun tunnus.</span><span class="sxs-lookup"><span data-stu-id="1d1c1-109">Make sure that each table has a page ID assigned to it.</span></span> <span data-ttu-id="1d1c1-110">Tämä arvo on täytetty automaattisesti vakiomuotoisissa [!INCLUDE[d365fin](includes/d365fin_md.md)] -taulukoissa.</span><span class="sxs-lookup"><span data-stu-id="1d1c1-110">For standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables, this value is automatically filled in.</span></span> <span data-ttu-id="1d1c1-111">Mukautetuille taulukoille tunnus on kuitenkin annettava.</span><span class="sxs-lookup"><span data-stu-id="1d1c1-111">For custom tables, you have to provide the ID.</span></span>  

2.  <span data-ttu-id="1d1c1-112">Valitse **Toiminnot**-välilehden **Näytä**-ryhmässä **Tietokannan tiedot**.</span><span class="sxs-lookup"><span data-stu-id="1d1c1-112">On the **Actions** tab, in the **Show** group, choose **Database Data**.</span></span>  

     <span data-ttu-id="1d1c1-113">Sivun [!INCLUDE[d365fin](includes/d365fin_md.md)] -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="1d1c1-113">The [!INCLUDE[d365fin](includes/d365fin_md.md)] page for the page opens.</span></span>  

3.  <span data-ttu-id="1d1c1-114">Tarkastele käytettävissä olevia tietoja</span><span class="sxs-lookup"><span data-stu-id="1d1c1-114">Review the available information.</span></span> <span data-ttu-id="1d1c1-115">Muokkaa sitä tarpeen mukaan poistamalla epäolennaiset tietueet tai lisäämällä uusia.</span><span class="sxs-lookup"><span data-stu-id="1d1c1-115">Modify it as necessary by deleting records that are not relevant or by adding new ones.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1d1c1-116">Katso myös</span><span class="sxs-lookup"><span data-stu-id="1d1c1-116">See Also</span></span>  
 [<span data-ttu-id="1d1c1-117">Yrityksen määrittämisen hallinta työkirjassa</span><span class="sxs-lookup"><span data-stu-id="1d1c1-117">Manage Company Configuration in a Worksheet</span></span>](admin-how-to-manage-company-configuration-in-a-worksheet.md)
