---
title: "Tulostimen valinnan määrittäminen raporteille | Microsoft Docs"
description: "Tulostimen valinnan määrittäminen raporteille."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e0b13ff745cddf6173b7a6dacda05e915eff41ff
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="specify-printer-selection-for-reports"></a>Tulostimen valinnan määrittäminen raporteille
Tämä sivu on tyhjä, koska et voi määrittää tiettyjä tulostimia tietyille raporteille. Etsimme ongelmaan ratkaisua.

Toistaiseksi tulostettava raportti on ladattava PDF-tiedostona valitsemalla ensin **Lähetä kohteeseen** -painike. Valitse tämän jälkeen tiedostotyyppi, jona haluat ladata tiedoston. Valitse nyt **PDF-asiakirja**. Voit nyt joka avata PDF-tiedoston ja tulostaa sen tai tallentaa sen myöhemmin tulostettavaksi.

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** window to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  
[Toimintaohje: Eräajojen ajaminen](ui-how-run-batch-jobs.md)  
[Toimintaohje: Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  

