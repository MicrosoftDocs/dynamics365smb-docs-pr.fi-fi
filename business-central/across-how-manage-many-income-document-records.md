---
title: "Määritä, mitkä saapuvat asiakirjat näytetään| Microsoft Docs"
description: "Voit muuttaa saapuvien asiakirjojen, kuten sähköisten laskujen oletusnäkymää parantaaksesi käsiteltyjen ja käsittelemättömien tietojen yleisnäkymää."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 445f215b4ac5ef977a29418771beddbf41000de6
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="98acb-103">Useiden saapuvien asiakirjatietueiden hallinta</span><span class="sxs-lookup"><span data-stu-id="98acb-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="98acb-104">Kun luot tai käsittelet saapuvia asiakirjatietueita, **Saapuvat asiakirjat** -ikkunan sisältämien rivien määrä voi kasvaa niin paljon, että yleiskuvauksen tarkasteleminen ei enää ole mahdollista.</span><span class="sxs-lookup"><span data-stu-id="98acb-104">As you create or process incoming document records, the number of lines in the **Incoming Documents** window may grow to an extent where you lose overview.</span></span> <span data-ttu-id="98acb-105">Tämän vuoksi voit määrittää saapuvien asiakirjatietueiden tilaksi Käsitelty, kun haluat poistaa ne oletusnäkymästä.</span><span class="sxs-lookup"><span data-stu-id="98acb-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="98acb-106">Kun valitset **Näytä kaikki** -toiminnon, näkyvillä ovat sekä käsitellyt että käsittelemättömät tietueet.</span><span class="sxs-lookup"><span data-stu-id="98acb-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="98acb-107">Et voi muokata tietoja, liittää tiedostoja tai suorittaa prosesseja niille saapuville asiakirjatietueille, joiden tilaksi on määritetty Käsitelty.</span><span class="sxs-lookup"><span data-stu-id="98acb-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="98acb-108">Niiden tilaksi on ensin määritettävä Käsittelemätön.</span><span class="sxs-lookup"><span data-stu-id="98acb-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="98acb-109">**Käsitelty**-valintaruutu valitaan automaattisesti niille saapuville asiakirjatietueille, jotka on käsitelty. Valintaruudun voi valita tai valinnan voi poistaa myös manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="98acb-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="98acb-110">Liiketoimintaprosessista riippuen saapuva asiakirjatietue voidaan käsitellä silloin, kun sille luodaan liittyvä asiakirja, tai tiedoston liittämisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="98acb-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="98acb-111">Kun avaat **Saapuvat asiakirjat** -ikkunan, jonka Roolikeskuksessa on **Omat saapuvat asiakirjat** -toiminto, oletusarvoisesti näytetään vain käsittelemättömät saapuvat asiakirjatietueet.</span><span class="sxs-lookup"><span data-stu-id="98acb-111">When you open the **Incoming Documents** window with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="98acb-112">Sitä kutsutaan tässä ohjeaiheessa "oletusnäkymäksi".</span><span class="sxs-lookup"><span data-stu-id="98acb-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="98acb-113">Saapuvien asiakirjatietueiden poistaminen oletusnäkymästä</span><span class="sxs-lookup"><span data-stu-id="98acb-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="98acb-114">Valitse **Saapuvat asiakirjat** -ikkunassa saapuvista asiakirjatietueista vähintään yksi oletusnäkymästä poistettava rivi.</span><span class="sxs-lookup"><span data-stu-id="98acb-114">In the **Incoming Documents** window, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="98acb-115">Valitse **Määritä tilaksi Käsitelty** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="98acb-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="98acb-116">Saapuvat asiakirjatietueet poistetaan oletusnäkymästä ja rivien **Käsitelty**-valintaruutu valitaan.</span><span class="sxs-lookup"><span data-stu-id="98acb-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="98acb-117">Voit tehdä tämän toiminnon yksittäiselle tietueelle **Saapuvan asiakirjan kortti** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="98acb-117">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="98acb-118">Saapuvien asiakirjatietueiden tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="98acb-118">To view all incoming document records</span></span>
1. <span data-ttu-id="98acb-119">Valitse **Saapuvat asiakirjat** -ikkunassa **Näytä kaikki** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="98acb-119">In the **Incoming Documents** window, choose the **Show All** action.</span></span>

<span data-ttu-id="98acb-120">Näkyvissä ovat kaikki saapuvat asiakirjatietueet, eli myös ne, joiden **Käsitelty**-valintaruutua ei ole valittu.</span><span class="sxs-lookup"><span data-stu-id="98acb-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="98acb-121">Saapuvien asiakirjatietueiden lisääminen oletusnäkymään</span><span class="sxs-lookup"><span data-stu-id="98acb-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="98acb-122">Valitse **Saapuvat asiakirjat** -ikkunassa **Näytä kaikki** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="98acb-122">In the **Incoming Documents** window, choose the **Show All** action.</span></span>
2. <span data-ttu-id="98acb-123">Valitse saapuvista asiakirjatietueista vähintään yksi rivi, jonka haluat näkyvän oletusnäkymässä.</span><span class="sxs-lookup"><span data-stu-id="98acb-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="98acb-124">Valitse **Määritä tilaksi Käsittelemätön** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="98acb-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="98acb-125">Voit tehdä tämän toiminnon yksittäiselle tietueelle **Saapuvan asiakirjan kortti** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="98acb-125">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="see-also"></a><span data-ttu-id="98acb-126">Katso myös</span><span class="sxs-lookup"><span data-stu-id="98acb-126">See Also</span></span>
[<span data-ttu-id="98acb-127">Saapuvien asiakirjojen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="98acb-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="98acb-128">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="98acb-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="98acb-129">Osto</span><span class="sxs-lookup"><span data-stu-id="98acb-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="98acb-130">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="98acb-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

