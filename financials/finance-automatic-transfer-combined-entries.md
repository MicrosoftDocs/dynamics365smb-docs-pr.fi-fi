---
title: Automaattinen siirto ja yhdistetyt tapahtumat | Microsoft Docs
description: "Kustannuslaskennassa voi siirtää pääkirjanpitotapahtumat kustannustyyppiin yhdistetyn kirjauksen avulla. Voit määrittää, vastaanottaako kustannustyyppi yhdistettyjä tapahtumia kustannustyypin määrityksen **Yhdistä tapahtumat** -kentässä. Seuraavassa taulukossa kuvaillaan eri asetukset."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bd80d0a7a701256dfdae3346e899b84eeb990a40
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="8d28a-105">Automaattinen siirto ja yhdistetyt tapahtumat</span><span class="sxs-lookup"><span data-stu-id="8d28a-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="8d28a-106">Voit siirtää kustannuslaskennassa pääkirjanpitotapahtumat kustannustyyppiin yhdistetyn kirjauksen avulla.</span><span class="sxs-lookup"><span data-stu-id="8d28a-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="8d28a-107">Voit määrittää, jos kustannustyyppi vastaanottaa yhdistettyjä tapahtumia **Yhdistä tapahtumat** -kentässä kustannustyypin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="8d28a-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="8d28a-108">Seuraavassa taulukossa kuvaillaan eri asetukset.</span><span class="sxs-lookup"><span data-stu-id="8d28a-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="8d28a-109">Yhdistä tapahtumat</span><span class="sxs-lookup"><span data-stu-id="8d28a-109">Combine entries</span></span>|<span data-ttu-id="8d28a-110">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="8d28a-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="8d28a-111">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="8d28a-111">None</span></span>|<span data-ttu-id="8d28a-112">Kukin pääkirjanpidon tapahtuma siirretään yksitellen vastaavaan kustannustyyppiin.</span><span class="sxs-lookup"><span data-stu-id="8d28a-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="8d28a-113">Päivä</span><span class="sxs-lookup"><span data-stu-id="8d28a-113">Day</span></span>|<span data-ttu-id="8d28a-114">Kirjanpitotapahtumat, joilla on sama kirjauspäivämäärä, siirretään vastaavaan kustannustyyppiin yhtenä tapahtumana.</span><span class="sxs-lookup"><span data-stu-id="8d28a-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="8d28a-115">Kuukausi</span><span class="sxs-lookup"><span data-stu-id="8d28a-115">Month</span></span>|<span data-ttu-id="8d28a-116">Saman kalenterikuukauden aikana kaikki pääkirjanpidon tapahtumat siirretään yhtenä tapahtumana vastaavaan kustannustyyppiin.</span><span class="sxs-lookup"><span data-stu-id="8d28a-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="8d28a-117">Jos olet valinnut **Automaattinen siirto kirjanpidosta** -valintaruudun **Kustannuslaskennan asetukset** -ikkunassa, [!INCLUDE[d365fin](includes/d365fin_md.md)] päivittää kustannuslaskennan jokaisen kirjanpidon kirjauksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="8d28a-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="8d28a-118">Yhdistetyt tapahtumat eivät ole mahdollisia.</span><span class="sxs-lookup"><span data-stu-id="8d28a-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8d28a-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="8d28a-119">See Also</span></span>  
 <span data-ttu-id="8d28a-120">[Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="8d28a-120">[How to: Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="8d28a-121">[Kriteerit pääkirjanpidon tapahtumien siirtämiseksi kustannustapahtumiin](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="8d28a-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="8d28a-122">[Siirron tulokset](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="8d28a-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="8d28a-123">Kustannustapahtumien siirtäminen ja kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="8d28a-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="8d28a-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8d28a-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

