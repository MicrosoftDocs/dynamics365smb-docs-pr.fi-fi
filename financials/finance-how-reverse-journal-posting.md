---
title: "Päiväkirjakirjauksen peruuttaminen kirjaamalla palautustapahtuma| Microsoft Docs"
description: "Jos olet tehnyt virheellisen kirjauksen yleiseen päiväkirjaan, Peruuta tapahtuma -toiminnolla kumottu kirjaus luo oikean kirjausketjun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-reverse-journal-posting"></a>Päiväkirjakirjauksen peruuttaminen
Voit kumota virheellisen kirjauksen päiväkirjaan valitsemalla tapahtuman luomalla peruutustapahtuman (alkuperäistä tapahtumaa vastaava tapahtuma, jossa summakentässä on vastakkainen etumerkki), jossa on sama asiakirjanumero ja kirjauspäivämäärä kuin alkuperäisessä tapahtumassa. Kun olet peruuttanut tapahtuman, lisää tapahtuma korjattuna.

Vain yleisen päiväkirjan riviltä kirjatut tapahtumat voi peruuttaa. Tapahtuman voi peruuttaa vain kerran.

Lisätietoja yleisestä päiväkirjasta tehtävistä kirjauksista on ohjeaiheessa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).

Tapahtumia voi peruuttaa kaikista **Tapahtumakirjaukset**-ikkunoista. Seuraava menettely perustuu **Pääkirjanpidon tapahtumat** -ikkunaan.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Pääkirjanpidon tapahtuman päiväkirjakirjauksen peruuttaminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Pääkirjanpidon tapahtumat** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse ensin peruutettava tapahtuma ja sitten **Peruuta tapahtuma** -toiminto. Huomaa, että sen on oltava peräisin päiväkirjan kirjauksesta.
3. Valitse **Peruuta tapahtumat** -ikkunassa käsiteltävä tapahtuma ja valitse sitten **Peruuta**-toiminto.
4. Valitse vahvistusviestissä **Kyllä**.

## <a name="see-also"></a>Katso myös
[Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

