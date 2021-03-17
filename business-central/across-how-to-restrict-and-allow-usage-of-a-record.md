---
title: Tietueen käytön rajoittaminen ja salliminen | Microsoft Docs
description: Jos haluat rajoittaa tietueen käyttöä tietyissä aktiviteeteissa, esimerkiksi ennen kuin tietue on hyväksytty, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1c748bd115b17acf925a99f89f538cc9eca41bc3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384397"
---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="f41de-103">Tietueen käytön rajoittaminen ja salliminen</span><span class="sxs-lookup"><span data-stu-id="f41de-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="f41de-104">Jos haluat rajoittaa tietueen käyttöä tietyissä aktiviteeteissa, esimerkiksi ennen kuin tietue on hyväksytty, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä.</span><span class="sxs-lookup"><span data-stu-id="f41de-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="f41de-105">Yksi työnkulku vastaus rajoittaa tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f41de-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="f41de-106">Toinen työnkulku vastaus sallii tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f41de-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="f41de-107">Yleisessä [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa on kaksi vastausta tähän tarkoitukseen: **Rajoita tietueen käyttöä**</span><span class="sxs-lookup"><span data-stu-id="f41de-107">Two responses exist in the generic version of [!INCLUDE[prod_short](includes/prod_short.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="f41de-108">ja **Salli tietueen käyttö**.</span><span class="sxs-lookup"><span data-stu-id="f41de-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="f41de-109">Yleinen [!INCLUDE[prod_short](includes/prod_short.md)] -versio tarjoaa tuen tietueen rajoittamiselle kirjaamisen, viennin maksuna ja tulostamisen sekkinä osalta.</span><span class="sxs-lookup"><span data-stu-id="f41de-109">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="f41de-110">Muita rajoituksia saadaan, jos Microsoft-kumppani mukauttaa sovelluksen koodin.</span><span class="sxs-lookup"><span data-stu-id="f41de-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f41de-111">Työnkulun toiminnallisuus rajoittaa ja sallia tietueita käytettäväksi työnkulun toimintoihin ei liity toiminnallisuuteen estää nimike, asiakas ja toimittajatietueiden kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="f41de-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="f41de-112">Seuraavassa kuvataan, miten rajoittaa ostotilausten kirjaamisen ennen kuin ne on hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="f41de-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="f41de-113">Uusi työnkulku perustuu Ostolaskun hyväksymistyönkulku -työnkulkumalliin.</span><span class="sxs-lookup"><span data-stu-id="f41de-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="f41de-114">Voit seuraavasti luoda työnkulun vaiheen, joka rajoittaa hyväksymättömiä ostotilausten kirjaus</span><span class="sxs-lookup"><span data-stu-id="f41de-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="f41de-115">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="f41de-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f41de-116">Luo **Työnkulut**-sivulla uusi työnkulku nimeltä Ostotilauksen hyväksymistyönkulku.</span><span class="sxs-lookup"><span data-stu-id="f41de-116">On the **Workflows** page, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="f41de-117">Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f41de-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="f41de-118">Valitse **Kopioi työnkulun mallista** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="f41de-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="f41de-119">Valita **Lähdetyönkulun koodi** -kenttä ja sitten **Työnkulkumallit**-sivulla valitse Ostolaskun hyväksymistyönkulku -työnkulkumalli.</span><span class="sxs-lookup"><span data-stu-id="f41de-119">Choose the **Source Workflow Code** field, and then, on the **Workflow Templates** page, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="f41de-120">Huomaa, että kaksi ensimmäistä työnkulun vaiheet ovat rajoittaminen ja sitten salliminen ostolaskujen käyttö.</span><span class="sxs-lookup"><span data-stu-id="f41de-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="f41de-121">Siirry muuttamaan uuden työnkulun ensimmäisen vaiheen tapahtumaehtoa niin, että se koskee ostotilauksia.</span><span class="sxs-lookup"><span data-stu-id="f41de-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="f41de-122">Valitse **Työnkulun vaiheet** -pikavälilehdessä **Tapahtuman ehdot** -kenttä ja valitse sitten **Asiakirjan tyyppi** -suodattimeksi **Tilaus**.</span><span class="sxs-lookup"><span data-stu-id="f41de-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="f41de-123">Siirry muokkaamaan, poistamaan tai lisäämään muita työnkulun vaiheita sovittaaksesi liiketoiminnan prosessi, joka alkaa rajoittamalla hyväksymättömien ostotilausten kirjaaminen.</span><span class="sxs-lookup"><span data-stu-id="f41de-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f41de-124">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f41de-124">See Also</span></span>  
<span data-ttu-id="f41de-125">[Työnkulkujen luominen](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f41de-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="f41de-126">Työnkulku</span><span class="sxs-lookup"><span data-stu-id="f41de-126">Workflow</span></span>](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]