---
title: Useiden asiakirjojen kirjaaminen samanaikaisesti | Microsoft Docs
description: Sen sijaan että yksittäisiä asiakirjoja yksi kerrallaan, voit valita luettelosta useita kirjaamattomia asiakirjoja eräkirjausta varten. Tämä kirjaus voidaan tehdä heti tai se voidaan aikatauluttaa tapahtumaan esimerkiksi päivän päätteeksi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fd25f8b07a359414f62ef4757162f8a73889c27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912719"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="5332f-103">Useiden asiakirjojen kirjaaminen samanaikaisesti</span><span class="sxs-lookup"><span data-stu-id="5332f-103">Post Multiple Documents at the Same Time</span></span>

<span data-ttu-id="5332f-104">Sen sijaan että yksittäisiä asiakirjoja yksi kerrallaan, voit valita luettelosta useita kirjaamattomia asiakirjoja eräkirjausta varten. Tämä kirjaus voidaan tehdä heti tai se voidaan aikatauluttaa tapahtumaan vaikkapa päivän päätteeksi.</span><span class="sxs-lookup"><span data-stu-id="5332f-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="5332f-105">Tämä voi olla kätevää, jos vain esimies voi kirjata muiden käyttäjien tekemiä asiakirjoja tai jos halutaan estää järjestelmän suorituskyvyn heikentyminen työaikana tehtävien kirjausten vuoksi.</span><span class="sxs-lookup"><span data-stu-id="5332f-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="5332f-106">Useiden ostotilausten kirjaaminen heti</span><span class="sxs-lookup"><span data-stu-id="5332f-106">To post multiple purchase orders immediately</span></span>

<span data-ttu-id="5332f-107">Useita ostotilauksia voi kirjata heti toimimalla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5332f-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="5332f-108">Vaiheet ovat samanlaiset kaikissa osto- ja myyntiasiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="5332f-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="5332f-109">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5332f-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5332f-110">Siirry valitsemaan kaikki kirjattavat tilaukset **Ostotilaukset**-sivulla:</span><span class="sxs-lookup"><span data-stu-id="5332f-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="5332f-111">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="5332f-111">In the **No.**</span></span> <span data-ttu-id="5332f-112">kolme allekkain olevaa pistettä. Pikavalikko avautuu, ja voit valita **Valitse lisää** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="5332f-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="5332f-113">Valitse kaikkien samaan aikaan kirjattavien tilausrivien valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="5332f-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="5332f-114">Valitse ensin **Kirjaus**-toiminto ja sitten **Kirjaa**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="5332f-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="5332f-115">Valitse vahvistusviestissä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="5332f-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="5332f-116">Useiden ostotilausten eräkirjaaminen</span><span class="sxs-lookup"><span data-stu-id="5332f-116">To batch post multiple purchase orders</span></span>

<span data-ttu-id="5332f-117">Ostotilauksia voi eräkirjata toimimalla seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5332f-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="5332f-118">Vaiheet ovat samat kaikissa osto- ja myyntiasiakirjoissa, joissa **Eräkirjaus**-toiminto on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="5332f-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="5332f-119">Asiakirjojen eräkirjaus tehdään taustalla.</span><span class="sxs-lookup"><span data-stu-id="5332f-119">Batch posting of documents happens in the background.</span></span> <span data-ttu-id="5332f-120">[!INCLUDE [prodshort](includes/prodshort.md)] online sisältää tausta- ja eräkirjauksen oletustyöt.</span><span class="sxs-lookup"><span data-stu-id="5332f-120">[!INCLUDE [prodshort](includes/prodshort.md)] online includes default jobs for background posting and batch posting.</span></span> <span data-ttu-id="5332f-121">Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="5332f-121">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="5332f-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="5332f-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5332f-123">Siirry valitsemaan kaikki kirjattavat tilaukset **Ostotilaukset**-sivulla:</span><span class="sxs-lookup"><span data-stu-id="5332f-123">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="5332f-124">Valitse **Nro**-kenttään</span><span class="sxs-lookup"><span data-stu-id="5332f-124">In the **No.**</span></span> <span data-ttu-id="5332f-125">kolme allekkain olevaa pistettä. Pikavalikko avautuu, ja voit valita **Valitse lisää** -toiminnon.</span><span class="sxs-lookup"><span data-stu-id="5332f-125">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="5332f-126">Valitse kaikkien samaan aikaan kirjattavien tilausrivien valintaruudut.</span><span class="sxs-lookup"><span data-stu-id="5332f-126">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="5332f-127">Valitse ensin **Kirjaus**-toiminto ja sitten **Eräkirjaus**-toiminto.</span><span class="sxs-lookup"><span data-stu-id="5332f-127">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="5332f-128">Täytä tarvittavat kentät **Eräkirjaa ostotilaukset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5332f-128">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="5332f-129">Valitse **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="5332f-129">Choose the **OK** button.</span></span>
8. <span data-ttu-id="5332f-130">Voit tarkastella asiakirjojen eräkirjauksen aikana mahdollisesti esiintyneitä ongelmia avaamalla **Virhesanomarekisteri**-sivun.</span><span class="sxs-lookup"><span data-stu-id="5332f-130">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="5332f-131">Ostotilaukset lisätään nyt määritettyyn työjonotapahtumaan, joka määrittää, milloin asiakirjat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="5332f-131">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="5332f-132">Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="5332f-132">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="5332f-133">Jos valitset **Raportin tuotostyyppi** -kentässä **PDF**, ostotilaukset, joiden kirjaus onnistui, ovat käytettävissä roolikeskuksen **Saapuneet raportit** -osassa.</span><span class="sxs-lookup"><span data-stu-id="5332f-133">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="5332f-134">Katso myös</span><span class="sxs-lookup"><span data-stu-id="5332f-134">See Also</span></span>

[<span data-ttu-id="5332f-135">Asiakirjojen ja päiväkirjojen kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="5332f-135">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="5332f-136">Työjonojen käyttäminen ajoitustehtäviin</span><span class="sxs-lookup"><span data-stu-id="5332f-136">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="5332f-137">Kirjattujen asiakirjojen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="5332f-137">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="5332f-138">Maksamattomien ostolaskujen korjaaminen tai peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="5332f-138">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="5332f-139">Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla</span><span class="sxs-lookup"><span data-stu-id="5332f-139">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="5332f-140">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5332f-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
