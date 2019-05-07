---
title: Useiden nimikekuvien tuominen ZIP-tiedostosta| Microsoft Docs
description: Voit tuoda kerralla useita nimikekuvia. Sinun tarvitsee vain antaa kuvatiedostoille nimikenumeroita vastaavat nimet, pakata ne zip-tiedostoon ja hallita sitten nimikekuivien tuontia Tuo nimikekuvat -sivulla.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fa859d3e350cedb845df47521ee58ba8d2e4aade
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "940103"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="51610-104">Useiden nimikekuvien tuominen</span><span class="sxs-lookup"><span data-stu-id="51610-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="51610-105">Voit tuoda kerralla useita nimikekuvia.</span><span class="sxs-lookup"><span data-stu-id="51610-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="51610-106">Sinun tarvitsee vain antaa kuvatiedostoille nimikenumeroita vastaavat nimet, pakata ne ZIP-tiedostoon ja hallita sitten nimikekuvien tuontia **Tuo nimikekuvat** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="51610-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="51610-107">Kaikkia yleisiä tiedostomuotoja tuetaan.</span><span class="sxs-lookup"><span data-stu-id="51610-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="51610-108">Kuvatiedostojen nimeäminen nimikenimillä ja ZIP-tiedoston valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="51610-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="51610-109">Anna kullekin tiedostolle nimikekuvien tallennussijainnissa nimi, joka vastaa liittyvän nimikkeen numeroa.</span><span class="sxs-lookup"><span data-stu-id="51610-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="51610-110">Esimerkiksi:</span><span class="sxs-lookup"><span data-stu-id="51610-110">For example:</span></span>

    |<span data-ttu-id="51610-111">Nimikkeen nro</span><span class="sxs-lookup"><span data-stu-id="51610-111">Item No.</span></span>|<span data-ttu-id="51610-112">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="51610-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="51610-113">1000</span><span class="sxs-lookup"><span data-stu-id="51610-113">1000</span></span>|<span data-ttu-id="51610-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="51610-114">1000.bmp</span></span>|
    |<span data-ttu-id="51610-115">1001</span><span class="sxs-lookup"><span data-stu-id="51610-115">1001</span></span>|<span data-ttu-id="51610-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="51610-116">1001.bmp</span></span>|
    |<span data-ttu-id="51610-117">1002</span><span class="sxs-lookup"><span data-stu-id="51610-117">1002</span></span>|<span data-ttu-id="51610-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="51610-118">1002.bmp</span></span>|

2. <span data-ttu-id="51610-119">Kerää kaikki tiedostot ZIP-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="51610-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="51610-120">Valitse esimerkiksi Resurssienhallinnassa ensin tiedostot ja sitten **Lähetä kohteeseen** ja **Pakattu kansio (zip-tiedosto)**.</span><span class="sxs-lookup"><span data-stu-id="51610-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="51610-121">Nimikekuvien tuominen</span><span class="sxs-lookup"><span data-stu-id="51610-121">To import item pictures</span></span>
1. <span data-ttu-id="51610-122">Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten liittyvä linkki.</span><span class="sxs-lookup"><span data-stu-id="51610-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="51610-123">Valitse **Tuo nimikekuva** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="51610-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="51610-124">Valitse **Valitse ZIP-tiedosto** -kentässä oikea ZIP-kansio ja valitse sitten **Avaa**-painike.</span><span class="sxs-lookup"><span data-stu-id="51610-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="51610-125">**Tuo nimikekuvat** -sivulla luodaan jokaiselle nimikkeelle ja kuvalle luodaan rivi.</span><span class="sxs-lookup"><span data-stu-id="51610-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="51610-126">Jos nimikekortissa on jo kuva, **Kuva on jo olemassa** -valintaruutu on jo valittu.</span><span class="sxs-lookup"><span data-stu-id="51610-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="51610-127">Jos et haluat korvata mitään olemassa olevaa kuvaa, poista **Korvaa kuvat** -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="51610-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="51610-128">Jos et halua korvata yksittäisiä olemassa olevia kuvia, poista kyseiset rivit.</span><span class="sxs-lookup"><span data-stu-id="51610-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="51610-129">Valitse **Tuo kuvat** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="51610-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="51610-130">**Tuonnin tila** -kenttä päivitetään näyttämään, onko kuvan tuonti ohitettu tai onko se valmis.</span><span class="sxs-lookup"><span data-stu-id="51610-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="51610-131">Katso myös</span><span class="sxs-lookup"><span data-stu-id="51610-131">See Also</span></span>
[<span data-ttu-id="51610-132">Uusien nimikkeiden rekisteröiminen</span><span class="sxs-lookup"><span data-stu-id="51610-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="51610-133">Numerosarjojen luominen</span><span class="sxs-lookup"><span data-stu-id="51610-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="51610-134">Varasto</span><span class="sxs-lookup"><span data-stu-id="51610-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="51610-135">Osto</span><span class="sxs-lookup"><span data-stu-id="51610-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="51610-136">Myynti</span><span class="sxs-lookup"><span data-stu-id="51610-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="51610-137">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="51610-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>