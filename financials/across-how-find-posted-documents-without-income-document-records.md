---
title: "Liitteettömien asiakirjojen etsiminen| Microsoft Docs"
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c355657821f5f4d18c707d296d9607cf5ec60442
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="3508c-102">Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita</span><span class="sxs-lookup"><span data-stu-id="3508c-102">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="3508c-103">**Tilikartta**- ja **Pääkirjanpidon tapahtumat** -ikkunan hakutoiminnon avulla voit etsiä pääkirjanpidon tapahtumia kirjatuille osto- ja myyntiasiakirjoille, joilla ei ole saapuvia asiakirjatietueita. Tämän jälkeen voit keskitetysti muodostaa yhteyden olemassa oleviin tietueisiin tai luoda uusia tietueita ja niihin liittyviä asiakirjatiedostoja.</span><span class="sxs-lookup"><span data-stu-id="3508c-103">From the **Chart of Accounts** and **General Ledger Entries** windows, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="3508c-104">Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita</span><span class="sxs-lookup"><span data-stu-id="3508c-104">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="3508c-105">Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="3508c-105">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="3508c-106">Valitse pääkirjanpidon tapahtumien KP-tilin rivi, kun haluat tarkastella kyseisen rivin kirjattuja osto- ja myyntiasiakirjoja, joilla ei ole saapuvia asiakirjatietueita. Valitse sitten **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="3508c-106">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="3508c-107">Vaihtoehtoisesti voit valita **Tapahtumakirjaukset**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="3508c-107">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="3508c-108">Valitse **Pääkirjanpidon tapahtumat** -ikkunassa **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="3508c-108">In the **General Ledger Entries** window, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="3508c-109">Avautuvassa **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -ikkunassa näkyvät kirjatut osto- ja myyntiasiakirjat, joilla ei ole saapuvia asiakirjatietueita. Ikkunan tiedot koskevat määrittämäsi KP-tilin pääkirjanpidon tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="3508c-109">The **Posted Documents without Incoming Document** window opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the window for.</span></span> <span data-ttu-id="3508c-110">Ikkunassa näkyy enintään 1 000 riviä.</span><span class="sxs-lookup"><span data-stu-id="3508c-110">The window can show a maximum of 1000 lines.</span></span> <span data-ttu-id="3508c-111">Oletusarvon mukaan **Pvm-suodatus**-kentässä on suodatin, joka rajoittaa rivit tapahtumiin, joiden kirjauspäivämäärät ulottuvat tilikauden alusta käsittelypäivämäärään.</span><span class="sxs-lookup"><span data-stu-id="3508c-111">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="3508c-112">Löydettyjen asiakirjojen yhdistäminen olemassa oleviin saapuviin asiakirjatietueisiin</span><span class="sxs-lookup"><span data-stu-id="3508c-112">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="3508c-113">Valitse **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -ikkunassa rivi kirjatulle asiakirjalle, jonka haluat yhdistää olemassa olevaan saapuvaan asiakirjatietueeseen. Valitse sitten **Valitse saapuva asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="3508c-113">In the **Posted Documents without Incoming Document** window, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="3508c-114">Valitse **Saapuvat asiakirjat** -ikkunassa saapuva asiakirjatietue, jonka haluat yhdistää löydettyyn kirjattuun asiakirjaan ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="3508c-114">In the **Incoming Documents** window, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="3508c-115">Valittu saapuva asiakirjatietue on nyt yhdistetty **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -ikkunassa kirjattuun asiakirjaan, kuten **Saapuvat asiakirjatiedostot** -tietoruudusta voidaan nähdä.</span><span class="sxs-lookup"><span data-stu-id="3508c-115">In the **Posted Documents without Incoming Document** window, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="3508c-116">Jos **Saapuvat asiakirjat** -ikkunassa ei ole asiaankuuluvaa saapuvaa asiakirjatietuetta, voit luoda sen.</span><span class="sxs-lookup"><span data-stu-id="3508c-116">If a relevant incoming document record does not exist in the **Incoming Documents** window, then you can create it.</span></span> <span data-ttu-id="3508c-117">Lisätietoja on kohdassa [Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="3508c-117">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3508c-118">Katso myös</span><span class="sxs-lookup"><span data-stu-id="3508c-118">See Also</span></span>
[<span data-ttu-id="3508c-119">Saapuvien asiakirjojen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="3508c-119">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="3508c-120">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="3508c-120">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="3508c-121">Osto</span><span class="sxs-lookup"><span data-stu-id="3508c-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="3508c-122">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3508c-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

