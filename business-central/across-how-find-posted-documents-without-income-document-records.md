---
title: Liitteettömien asiakirjojen etsiminen| Microsoft Docs
Description: Voit etsiä kirjanpitotapahtumia kirjatuille myynti- ja ostoasiakirjoille, joilla ei ole saapuvia sähköisiä asiakirjoja, kuten tuotuja laskuja.
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
ms.openlocfilehash: 79504010d6bb4f2afb0f09f866991dd76f6e35b5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "923692"
---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="46879-103">Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita</span><span class="sxs-lookup"><span data-stu-id="46879-103">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="46879-104">**Tilikartta**- ja **Pääkirjanpidon tapahtumat** -sivujen hakutoiminnon avulla voit etsiä pääkirjanpidon tapahtumia kirjatuille osto- ja myyntiasiakirjoille, joilla ei ole saapuvia asiakirjatietueita. Tämän jälkeen voit keskitetysti muodostaa yhteyden olemassa oleviin tietueisiin tai luoda uusia tietueita ja niihin liittyviä asiakirjatiedostoja.</span><span class="sxs-lookup"><span data-stu-id="46879-104">From the **Chart of Accounts** and **General Ledger Entries** pages, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="46879-105">Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita</span><span class="sxs-lookup"><span data-stu-id="46879-105">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="46879-106">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="46879-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="46879-107">Valitse pääkirjanpidon tapahtumien KP-tilin rivi, kun haluat tarkastella kyseisen rivin kirjattuja osto- ja myyntiasiakirjoja, joilla ei ole saapuvia asiakirjatietueita. Valitse sitten **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="46879-107">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="46879-108">Vaihtoehtoisesti voit valita **Tapahtumakirjaukset**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="46879-108">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="46879-109">Valitse **Pääkirjanpidon tapahtumat** -sivulla **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="46879-109">On the **General Ledger Entries** page, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="46879-110">Avautuvalla **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -sivulla näkyvät kirjatut osto- ja myyntiasiakirjat, joilla ei ole saapuvia asiakirjatietueita. Sivun tiedot koskevat määrittämäsi KP-tilin pääkirjanpidon tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="46879-110">The **Posted Documents without Incoming Document** page opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the page for.</span></span> <span data-ttu-id="46879-111">Sivulla näkyy enintään 1 000 riviä.</span><span class="sxs-lookup"><span data-stu-id="46879-111">The page can show a maximum of 1000 lines.</span></span> <span data-ttu-id="46879-112">Oletusarvon mukaan **Pvm-suodatus**-kentässä on suodatin, joka rajoittaa rivit tapahtumiin, joiden kirjauspäivämäärät ulottuvat tilikauden alusta käsittelypäivämäärään.</span><span class="sxs-lookup"><span data-stu-id="46879-112">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="46879-113">Löydettyjen asiakirjojen yhdistäminen olemassa oleviin saapuviin asiakirjatietueisiin</span><span class="sxs-lookup"><span data-stu-id="46879-113">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="46879-114">Valitse **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -sivulla rivi kirjatulle asiakirjalle, jonka haluat yhdistää olemassa olevaan saapuvaan asiakirjatietueeseen. Valitse sitten **Valitse saapuva asiakirja** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="46879-114">On the **Posted Documents without Incoming Document** page, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="46879-115">Valitse **Saapuvat asiakirjat** -sivulla saapuva asiakirjatietue, jonka haluat yhdistää löydettyyn kirjattuun asiakirjaan ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="46879-115">On the **Incoming Documents** page, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="46879-116">Valittu saapuva asiakirjatietue on nyt yhdistetty **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -sivulla kirjattuun asiakirjaan, kuten **Saapuvat asiakirjatiedostot** -tietoruudusta voidaan nähdä.</span><span class="sxs-lookup"><span data-stu-id="46879-116">On the **Posted Documents without Incoming Document** page, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="46879-117">Jos **Saapuvat asiakirjat** -sivulla ei ole asiaankuuluvaa saapuvaa asiakirjatietuetta, voit luoda sen.</span><span class="sxs-lookup"><span data-stu-id="46879-117">If a relevant incoming document record does not exist on the **Incoming Documents** page, then you can create it.</span></span> <span data-ttu-id="46879-118">Lisätietoja on kohdassa [Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="46879-118">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="46879-119">Katso myös</span><span class="sxs-lookup"><span data-stu-id="46879-119">See Also</span></span>
[<span data-ttu-id="46879-120">Saapuvien asiakirjojen käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="46879-120">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="46879-121">Saapuvat asiakirjat</span><span class="sxs-lookup"><span data-stu-id="46879-121">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="46879-122">Osto</span><span class="sxs-lookup"><span data-stu-id="46879-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="46879-123">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="46879-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
