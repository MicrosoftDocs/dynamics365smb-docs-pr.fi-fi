---
title: "Tietueen käytön rajoittaminen ja salliminen | Microsoft Docs"
description: "Jos haluat rajoittaa tietueen käyttöä tietyissä aktiviteeteissa, esimerkiksi ennen kuin tietue on hyväksytty, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e95d6106fd4908bf13004da11656b9b6d1446ad3
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="0ea76-103">Tietueen käytön rajoittaminen ja salliminen</span><span class="sxs-lookup"><span data-stu-id="0ea76-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="0ea76-104">Jos haluat rajoittaa tietueen käyttöä tietyissä aktiviteeteissa, esimerkiksi ennen kuin tietue on hyväksytty, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä.</span><span class="sxs-lookup"><span data-stu-id="0ea76-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="0ea76-105">Yksi työnkulku vastaus rajoittaa tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="0ea76-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="0ea76-106">Toinen työnkulku vastaus sallii tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="0ea76-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="0ea76-107">Yleisessä [!INCLUDE[d365fin](includes/d365fin_md.md)] -versiossa on kaksi vastausta tähän tarkoitukseen: **Rajoita tietueen käyttöä**</span><span class="sxs-lookup"><span data-stu-id="0ea76-107">Two responses exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="0ea76-108">ja **Salli tietueen käyttö**.</span><span class="sxs-lookup"><span data-stu-id="0ea76-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="0ea76-109">Yleinen [!INCLUDE[d365fin](includes/d365fin_md.md)] -versio tarjoaa tuen tietueen rajoittamiselle kirjaamisen, viennin maksuna ja tulostamisen sekkinä osalta.</span><span class="sxs-lookup"><span data-stu-id="0ea76-109">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="0ea76-110">Muita rajoituksia saadaan, jos Microsoft-kumppani mukauttaa sovelluksen koodin.</span><span class="sxs-lookup"><span data-stu-id="0ea76-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0ea76-111">Työnkulun toiminnallisuus rajoittaa ja sallia tietueita käytettäväksi työnkulun toimintoihin ei liity toiminnallisuuteen estää nimike, asiakas ja toimittajatietueiden kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="0ea76-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="0ea76-112">Seuraavassa kuvataan, miten rajoittaa ostotilausten kirjaamisen ennen kuin ne on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="0ea76-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="0ea76-113">Uusi työnkulku perustuu Ostolaskun hyväksymistyönkulku -työnkulkumalliin.</span><span class="sxs-lookup"><span data-stu-id="0ea76-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="0ea76-114">Voit seuraavasti luoda työnkulun vaiheen, joka rajoittaa hyväksymättömiä ostotilausten kirjaus</span><span class="sxs-lookup"><span data-stu-id="0ea76-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="0ea76-115">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Työnkulut** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="0ea76-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0ea76-116">Luo **Työnkulut** -ikkunassa uusi työnkulku nimeltä Ostotilauksen hyväksymistyönkulku.</span><span class="sxs-lookup"><span data-stu-id="0ea76-116">In the **Workflows** window, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="0ea76-117">Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="0ea76-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="0ea76-118">Valitse **Kopioi työnkulun mallista** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="0ea76-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="0ea76-119">Valita **Lähdetyönkulun koodi** -kenttä ja sitten **Työnkulkumallit**-ikkunassa valitse Ostolaskun hyväksymistyönkulku -työnkulkumalli.</span><span class="sxs-lookup"><span data-stu-id="0ea76-119">Choose the **Source Workflow Code** field, and then, in the **Workflow Templates** window, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="0ea76-120">Huomaa, että kaksi ensimmäistä työnkulun vaiheet ovat rajoittaminen ja sitten salliminen ostolaskujen käyttö.</span><span class="sxs-lookup"><span data-stu-id="0ea76-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="0ea76-121">Siirry muuttamaan uuden työnkulun ensimmäisen vaiheen tapahtumaehtoa niin, että se koskee ostotilauksia.</span><span class="sxs-lookup"><span data-stu-id="0ea76-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="0ea76-122">Valitse **Työnkulun vaiheet** -pikavälilehdessä **Tapahtuman ehdot** -kenttä ja valitse sitten **Asiakirjan tyyppi** -suodattimeksi **Tilaus**.</span><span class="sxs-lookup"><span data-stu-id="0ea76-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="0ea76-123">Siirry muokkaamaan, poistamaan tai lisäämään muita työnkulun vaiheita sovittaaksesi liiketoiminnan prosessi, joka alkaa rajoittamalla hyväksymättömien ostotilausten kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="0ea76-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0ea76-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="0ea76-124">See Also</span></span>  
<span data-ttu-id="0ea76-125">[Työnkulkujen luominen](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0ea76-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="0ea76-126">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="0ea76-126">Workflow</span></span>](across-workflow.md)   

