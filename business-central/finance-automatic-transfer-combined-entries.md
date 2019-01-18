---
title: Automaattinen siirto ja yhdistetyt tapahtumat | Microsoft Docs
description: "Kustannuslaskennassa voi siirtää pääkirjanpitotapahtumat kustannustyyppiin yhdistetyn kirjauksen avulla. Voit määrittää, jos kustannustyyppi vastaanottaa yhdistettyjä tapahtumia **Yhdistä tapahtumat** -kentässä kustannustyypin määrityksessä. Seuraavassa taulukossa kuvaillaan eri asetukset."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6f58e569bea6a42a9ee695095ce308e7a69e2a8d
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="03ae0-105">Automaattinen siirto ja yhdistetyt tapahtumat</span><span class="sxs-lookup"><span data-stu-id="03ae0-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="03ae0-106">Voit siirtää kustannuslaskennassa pääkirjanpitotapahtumat kustannustyyppiin yhdistetyn kirjauksen avulla.</span><span class="sxs-lookup"><span data-stu-id="03ae0-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="03ae0-107">Voit määrittää, jos kustannustyyppi vastaanottaa yhdistettyjä tapahtumia **Yhdistä tapahtumat** -kentässä kustannustyypin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="03ae0-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="03ae0-108">Seuraavassa taulukossa kuvaillaan eri asetukset.</span><span class="sxs-lookup"><span data-stu-id="03ae0-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="03ae0-109">Yhdistä tapahtumat</span><span class="sxs-lookup"><span data-stu-id="03ae0-109">Combine entries</span></span>|<span data-ttu-id="03ae0-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="03ae0-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="03ae0-111">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="03ae0-111">None</span></span>|<span data-ttu-id="03ae0-112">Kukin pääkirjanpidon tapahtuma siirretään yksitellen vastaavaan kustannustyyppiin.</span><span class="sxs-lookup"><span data-stu-id="03ae0-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="03ae0-113">Päivä</span><span class="sxs-lookup"><span data-stu-id="03ae0-113">Day</span></span>|<span data-ttu-id="03ae0-114">Kirjanpitotapahtumat, joilla on sama kirjauspäivämäärä, siirretään vastaavaan kustannustyyppiin yhtenä tapahtumana.</span><span class="sxs-lookup"><span data-stu-id="03ae0-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="03ae0-115">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="03ae0-115">Month</span></span>|<span data-ttu-id="03ae0-116">Saman kalenterikuukauden aikana kaikki pääkirjanpidon tapahtumat siirretään yhtenä tapahtumana vastaavaan kustannustyyppiin.</span><span class="sxs-lookup"><span data-stu-id="03ae0-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="03ae0-117">Jos olet valinnut **Automaattinen siirto kirjanpidosta** -valintaruudun **Kustannuslaskennan asetukset** -sivulla, [!INCLUDE[d365fin](includes/d365fin_md.md)] päivittää kustannuslaskennan jokaisen kirjanpidon kirjauksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="03ae0-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="03ae0-118">Yhdistetyt tapahtumat eivät ole mahdollisia.</span><span class="sxs-lookup"><span data-stu-id="03ae0-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="03ae0-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="03ae0-119">See Also</span></span>  
 <span data-ttu-id="03ae0-120">[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="03ae0-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="03ae0-121">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="03ae0-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

