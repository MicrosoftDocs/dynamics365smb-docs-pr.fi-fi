---
title: RapidStart Servicesin käyttöönottajan roolikeskuksen käyttäminen | Microsoft Docs
description: Kun käytössä on RapidStart Services, suosittelemme työn seuraamista ja RapidStart Servicesin käyttöönottajan roolikeskuksen käyttämistä, koska se tarjoaa määritystyölle juuri oikean kontekstin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: /dynamics365/business-central/admin-set-up-company-configuration
ROBOTS: NOINDEX
ms.openlocfilehash: 908e460ae5a3fc8ecb804f27363a1cfad71d997c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307922"
---
# <a name="use-the-rapidstart-services-implementer-role-center"></a><span data-ttu-id="57f68-103">RapidStart Servicesin käyttöönottajan roolikeskuksen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="57f68-103">Use the RapidStart Services Implementer Role Center</span></span>
<span data-ttu-id="57f68-104">Kun käytössä on RapidStart Services, suosittelemme RapidStart Servicesin käyttöönottajan roolikeskuksen käyttämistä, koska se tarjoaa määritystyölle juuri oikean kontekstin.</span><span class="sxs-lookup"><span data-stu-id="57f68-104">When you use RapidStart Services, we recommend that you use the RapidStart Services Implementer Role Center as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="57f68-105">Lisätietoja on kohdassa [Roolin vaihtaminen](ui-change-basic-settings.md#to-change-the-role).</span><span class="sxs-lookup"><span data-stu-id="57f68-105">For more information, see [To change the role](ui-change-basic-settings.md#to-change-the-role).</span></span>

<span data-ttu-id="57f68-106">Kun jatkat työskentelyä, voit määrittää kunkin taulukon tilan ilmaisemaan etenemisesi prosessissa.</span><span class="sxs-lookup"><span data-stu-id="57f68-106">As you continue with your work, you can assign each table the status that reflects where you are in the process.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="57f68-107">pitää seuraa taulukon tilaa roolikeskuksen **Toimenpiteet**-osassa.</span><span class="sxs-lookup"><span data-stu-id="57f68-107">then keeps track of the table status in the **Activities** part on the Role Center.</span></span>  

<span data-ttu-id="57f68-108">Kun lisäät taulukon määritysten työkirjaan, sen tila on oletusarvoisesti tyhjä.</span><span class="sxs-lookup"><span data-stu-id="57f68-108">By default, when you add a table to the configuration worksheet, its status is set to blank.</span></span> <span data-ttu-id="57f68-109">Tämä tarkoittaa sitä, että taulukon määritys ei ole alkanut.</span><span class="sxs-lookup"><span data-stu-id="57f68-109">This means that configuration of the table has not begun.</span></span> <span data-ttu-id="57f68-110">Tämä näkyy **Ei aloitettu** -lukumäärässä **Toimenpiteet**-ruudussa.</span><span class="sxs-lookup"><span data-stu-id="57f68-110">This is reflected in the **Not Started** count in the **Activities** tile.</span></span>  

## <a name="to-update-the-status-of-a-configuration-table"></a><span data-ttu-id="57f68-111">Päivitä konfiguraatiotaulukon tila</span><span class="sxs-lookup"><span data-stu-id="57f68-111">To update the status of a configuration table</span></span>  
1.  <span data-ttu-id="57f68-112">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Määritystyökirja** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="57f68-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="57f68-113">Valitse **Muokkaa luetteloa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="57f68-113">Choose the **Edit List** action.</span></span>  
3.  <span data-ttu-id="57f68-114">Valitse taulukko ja **Korjauksen tila**-kentässä asianmukainen tila.</span><span class="sxs-lookup"><span data-stu-id="57f68-114">Select a table, and in the **Status** field, choose the appropriate status.</span></span>  
4.  <span data-ttu-id="57f68-115">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="57f68-115">Choose the **OK** button.</span></span>  

<span data-ttu-id="57f68-116">Kun palaat roolikeskukseen, **Toimenpiteet**-osan ruudut päivitetään tehtyjen muutosten mukaan.</span><span class="sxs-lookup"><span data-stu-id="57f68-116">When you return to the Role Center, the tiles in the **Activities** part are updated to reflect your changes.</span></span>  

## <a name="to-track-the-status-of-a-configuration-project"></a><span data-ttu-id="57f68-117">Seuraa kokoonpano-projektin tilaa</span><span class="sxs-lookup"><span data-stu-id="57f68-117">To track the status of a configuration project</span></span>  
- <span data-ttu-id="57f68-118">Avaa RapidStart Servicesin roolikeskus.</span><span class="sxs-lookup"><span data-stu-id="57f68-118">Open the RapidStart Services Role Center.</span></span>  

<span data-ttu-id="57f68-119">**Määritysalueet**-osassa näytetään määrittämiesi alueiden ja ryhmien valmistumistilasto.</span><span class="sxs-lookup"><span data-stu-id="57f68-119">In the **Configuration Areas** part, completion statistics are shown for the areas and groups that you have set up.</span></span> <span data-ttu-id="57f68-120">Jos et ole määrittänyt ryhmiä tai alueita, tässä osassa ei ole tietoja.</span><span class="sxs-lookup"><span data-stu-id="57f68-120">If you have not set up any groups or areas, this part has no data.</span></span>  

## <a name="to-see-a-filtered-view-of-table-status"></a><span data-ttu-id="57f68-121">Katso suodatetun näkymän taulukon tila</span><span class="sxs-lookup"><span data-stu-id="57f68-121">To see a filtered view of table status</span></span>  
1. <span data-ttu-id="57f68-122">Valitse **Taulukot**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="57f68-122">Choose the **Tables** action.</span></span>  
2. <span data-ttu-id="57f68-123">Valitse asianmukainen suodatettu näkymä.</span><span class="sxs-lookup"><span data-stu-id="57f68-123">Select the appropriate filtered view.</span></span>  

## <a name="see-also"></a><span data-ttu-id="57f68-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="57f68-124">See Also</span></span>  
[<span data-ttu-id="57f68-125">Yrityksen määrittäminen RapidStart Servicesin avulla</span><span class="sxs-lookup"><span data-stu-id="57f68-125">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="57f68-126">Hallinta</span><span class="sxs-lookup"><span data-stu-id="57f68-126">Administration</span></span>](admin-setup-and-administration.md)
