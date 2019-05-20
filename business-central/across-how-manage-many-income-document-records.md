---
title: Määritä, mitkä saapuvat asiakirjat näytetään| Microsoft Docs
description: Voit muuttaa saapuvien asiakirjojen, kuten sähköisten laskujen oletusnäkymää parantaaksesi käsiteltyjen ja käsittelemättömien tietojen yleisnäkymää.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 429e276b094a8296daab8e229d60a6dd16246b53
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239956"
---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="668e7-103">Useiden saapuvien asiakirjatietueiden hallinta</span><span class="sxs-lookup"><span data-stu-id="668e7-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="668e7-104">Kun luot tai käsittelet saapuvia asiakirjatietueita, **Saapuvat asiakirjat** -sivun sisältämien rivien määrä voi kasvaa niin paljon, että yleiskuvauksen tarkasteleminen ei enää ole mahdollista.</span><span class="sxs-lookup"><span data-stu-id="668e7-104">As you create or process incoming document records, the number of lines on the **Incoming Documents** page may grow to an extent where you lose overview.</span></span> <span data-ttu-id="668e7-105">Tämän vuoksi voit määrittää saapuvien asiakirjatietueiden tilaksi Käsitelty, kun haluat poistaa ne oletusnäkymästä.</span><span class="sxs-lookup"><span data-stu-id="668e7-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="668e7-106">Kun valitset **Näytä kaikki** -toiminnon, näkyvillä ovat sekä käsitellyt että käsittelemättömät tietueet.</span><span class="sxs-lookup"><span data-stu-id="668e7-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="668e7-107">Et voi muokata tietoja, liittää tiedostoja tai suorittaa prosesseja niille saapuville asiakirjatietueille, joiden tilaksi on määritetty Käsitelty.</span><span class="sxs-lookup"><span data-stu-id="668e7-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="668e7-108">Niiden tilaksi on ensin määritettävä Käsittelemätön.</span><span class="sxs-lookup"><span data-stu-id="668e7-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="668e7-109">**Käsitelty**-valintaruutu valitaan automaattisesti niille saapuville asiakirjatietueille, jotka on käsitelty. Valintaruudun voi valita tai valinnan voi poistaa myös manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="668e7-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="668e7-110">Liiketoimintaprosessista riippuen saapuva asiakirjatietue voidaan käsitellä silloin, kun sille luodaan liittyvä asiakirja, tai tiedoston liittämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="668e7-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="668e7-111">Kun avaat **Saapuvat asiakirjat** -sivun, jonka Roolikeskuksessa on **Omat saapuvat asiakirjat** -toiminto, oletusarvoisesti näytetään vain käsittelemättömät saapuvat asiakirjatietueet.</span><span class="sxs-lookup"><span data-stu-id="668e7-111">When you open the **Incoming Documents** page with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="668e7-112">Sitä kutsutaan tässä ohjeaiheessa "oletusnäkymäksi".</span><span class="sxs-lookup"><span data-stu-id="668e7-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="668e7-113">Saapuvien asiakirjatietueiden poistaminen oletusnäkymästä</span><span class="sxs-lookup"><span data-stu-id="668e7-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="668e7-114">Valitse **Saapuvat asiakirjat** -sivulla saapuvista asiakirjatietueista vähintään yksi oletusnäkymästä poistettava rivi.</span><span class="sxs-lookup"><span data-stu-id="668e7-114">On the **Incoming Documents** page, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="668e7-115">Valitse **Määritä tilaksi Käsitelty** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="668e7-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="668e7-116">Saapuvat asiakirjatietueet poistetaan oletusnäkymästä ja rivien **Käsitelty**-valintaruutu valitaan.</span><span class="sxs-lookup"><span data-stu-id="668e7-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="668e7-117">Voit tehdä tämän toiminnon yksittäiselle tietueelle **Saapuvan asiakirjan kortti** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="668e7-117">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="668e7-118">Saapuvien asiakirjatietueiden tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="668e7-118">To view all incoming document records</span></span>
1. <span data-ttu-id="668e7-119">Valitse **Saapuvat asiakirjat** -sivulla **Näytä kaikki** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="668e7-119">On the **Incoming Documents** page, choose the **Show All** action.</span></span>

<span data-ttu-id="668e7-120">Näkyvissä ovat kaikki saapuvat asiakirjatietueet, eli myös ne, joiden **Käsitelty**-valintaruutua ei ole valittu.</span><span class="sxs-lookup"><span data-stu-id="668e7-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="668e7-121">Saapuvien asiakirjatietueiden lisääminen oletusnäkymään</span><span class="sxs-lookup"><span data-stu-id="668e7-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="668e7-122">Valitse **Saapuvat asiakirjat** -sivulla **Näytä kaikki** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="668e7-122">On the **Incoming Documents** page, choose the **Show All** action.</span></span>
2. <span data-ttu-id="668e7-123">Valitse saapuvista asiakirjatietueista vähintään yksi rivi, jonka haluat näkyvän oletusnäkymässä.</span><span class="sxs-lookup"><span data-stu-id="668e7-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="668e7-124">Valitse **Määritä tilaksi Käsittelemätön** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="668e7-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="668e7-125">Voit tehdä tämän toiminnon yksittäiselle tietueelle **Saapuvan asiakirjan kortti** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="668e7-125">You can also perform this action for the individual record on the **Incoming Document Card** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="668e7-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="668e7-126">See Also</span></span>
[<span data-ttu-id="668e7-127">Saapuvien asiakirjojen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="668e7-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="668e7-128">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="668e7-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="668e7-129">Osto</span><span class="sxs-lookup"><span data-stu-id="668e7-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="668e7-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="668e7-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
