---
title: Automaattinen siirto ja yhdistetyt tapahtumat | Microsoft Docs
description: Kustannuslaskennassa voi siirtää pääkirjanpitotapahtumat kustannustyyppiin yhdistetyn kirjauksen avulla. Voit määrittää, jos kustannustyyppi vastaanottaa yhdistettyjä tapahtumia **Yhdistä tapahtumat** -kentässä kustannustyypin määrityksessä. Seuraavassa taulukossa kuvaillaan eri asetukset.
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
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 8f6b5328b3a7b8cdcb4582deda363bdd0361ed9a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "941152"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="f7b89-105">Automaattinen siirto ja yhdistetyt tapahtumat</span><span class="sxs-lookup"><span data-stu-id="f7b89-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="f7b89-106">Voit siirtää kustannuslaskennassa pääkirjanpitotapahtumat kustannustyyppiin yhdistetyn kirjauksen avulla.</span><span class="sxs-lookup"><span data-stu-id="f7b89-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="f7b89-107">Voit määrittää, jos kustannustyyppi vastaanottaa yhdistettyjä tapahtumia **Yhdistä tapahtumat** -kentässä kustannustyypin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="f7b89-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="f7b89-108">Seuraavassa taulukossa kuvaillaan eri asetukset.</span><span class="sxs-lookup"><span data-stu-id="f7b89-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="f7b89-109">Yhdistä tapahtumat</span><span class="sxs-lookup"><span data-stu-id="f7b89-109">Combine entries</span></span>|<span data-ttu-id="f7b89-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f7b89-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="f7b89-111">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="f7b89-111">None</span></span>|<span data-ttu-id="f7b89-112">Kukin pääkirjanpidon tapahtuma siirretään yksitellen vastaavaan kustannustyyppiin.</span><span class="sxs-lookup"><span data-stu-id="f7b89-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="f7b89-113">Päivä</span><span class="sxs-lookup"><span data-stu-id="f7b89-113">Day</span></span>|<span data-ttu-id="f7b89-114">Kirjanpitotapahtumat, joilla on sama kirjauspäivämäärä, siirretään vastaavaan kustannustyyppiin yhtenä tapahtumana.</span><span class="sxs-lookup"><span data-stu-id="f7b89-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="f7b89-115">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="f7b89-115">Month</span></span>|<span data-ttu-id="f7b89-116">Saman kalenterikuukauden aikana kaikki pääkirjanpidon tapahtumat siirretään yhtenä tapahtumana vastaavaan kustannustyyppiin.</span><span class="sxs-lookup"><span data-stu-id="f7b89-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="f7b89-117">Jos olet valinnut **Automaattinen siirto kirjanpidosta** -valintaruudun **Kustannuslaskennan asetukset** -sivulla, [!INCLUDE[d365fin](includes/d365fin_md.md)] päivittää kustannuslaskennan jokaisen kirjanpidon kirjauksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f7b89-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="f7b89-118">Yhdistetyt tapahtumat eivät ole mahdollisia.</span><span class="sxs-lookup"><span data-stu-id="f7b89-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f7b89-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="f7b89-119">See Also</span></span>  
 <span data-ttu-id="f7b89-120">[Kustannustapahtumien siirtäminen ja kirjaaminen](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="f7b89-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="f7b89-121">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7b89-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
