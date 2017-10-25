---
title: "Raporttien määrittäminen tulostumaan tiettyihin tulostimiin | Microsoft Docs"
description: "Tutustu, miten tulostin määritetään raportille ja miten Tulostimen valinnat -ikkunaa käytetään."
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
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 42fb4adbcc01c443722fe90bb59edafceb34ff06
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="specify-printer-selection-for-reports"></a>Tulostimen valinnan määrittäminen raporteille
Tämä sivu on tyhjä, koska et voi määrittää tiettyjä tulostimia tietyille raporteille. Etsimme ongelmaan ratkaisua.

Toistaiseksi tulostettava raportti on ladattava ensin PDF-tiedostona valitsemalla **Lähetä kohteeseen** -painike. Valitse tämän jälkeen tiedostotyyppi, jona haluat ladata tiedoston. Valitse nyt **PDF-asiakirja**. Voit nyt joka avata PDF-tiedoston ja tulostaa sen tai tallentaa sen myöhemmin tulostettavaksi.

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
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Toimintaohje: Eräajojen ajaminen](ui-how-run-batch-jobs.md)  
[Toimintaohje: Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  

