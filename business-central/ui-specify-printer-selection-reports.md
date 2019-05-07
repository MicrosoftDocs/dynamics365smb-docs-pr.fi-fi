---
title: Raporttien määrittäminen tulostumaan tiettyihin tulostimiin | Microsoft Docs
description: Tutustu, miten tulostin määritetään raportille ja miten Tulostimen valinnat -sivua käytetään.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: ea713fe831ce0d4befc81825531d3210f755a4cd
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "917911"
---
# <a name="specify-printer-selection-for-reports"></a><span data-ttu-id="c13c2-103">Tulostimen valinnan määrittäminen raporteille</span><span class="sxs-lookup"><span data-stu-id="c13c2-103">Specify Printer Selection for Reports</span></span>
<span data-ttu-id="c13c2-104">Tämä sivu on tyhjä, koska et voi määrittää tiettyjä tulostimia tietyille raporteille.</span><span class="sxs-lookup"><span data-stu-id="c13c2-104">This page is empty because you cannot yet set up specific printers for specific reports.</span></span> <span data-ttu-id="c13c2-105">Etsimme ongelmaan ratkaisua.</span><span class="sxs-lookup"><span data-stu-id="c13c2-105">We are working on solving this.</span></span>

<span data-ttu-id="c13c2-106">Toistaiseksi tulostettava raportti on ladattava ensin PDF-tiedostona valitsemalla **Lähetä kohteeseen** -painike.</span><span class="sxs-lookup"><span data-stu-id="c13c2-106">In the meantime, when you want to print a report, you have to download the report as a PDF document first by choosing the **Send to** button.</span></span> <span data-ttu-id="c13c2-107">Valitse tämän jälkeen tiedostotyyppi, jona haluat ladata tiedoston. Valitse nyt **PDF-asiakirja**.</span><span class="sxs-lookup"><span data-stu-id="c13c2-107">Then you select the type of file to download the report as, and here you should pick **PDF Document**.</span></span> <span data-ttu-id="c13c2-108">Voit nyt joka avata PDF-tiedoston ja tulostaa sen tai tallentaa sen myöhemmin tulostettavaksi.</span><span class="sxs-lookup"><span data-stu-id="c13c2-108">Now, you can either open the PDF document right-away and print it, or save it and print it later.</span></span>

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** page to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a><span data-ttu-id="c13c2-109">Katso myös</span><span class="sxs-lookup"><span data-stu-id="c13c2-109">See Also</span></span>
<span data-ttu-id="c13c2-110">[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c13c2-110">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c13c2-111">Eräajojen ajaminen</span><span class="sxs-lookup"><span data-stu-id="c13c2-111">Run Batch Jobs</span></span>](ui-how-run-batch-jobs.md)  
[<span data-ttu-id="c13c2-112">Asiakirjojen lähettäminen sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="c13c2-112">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
