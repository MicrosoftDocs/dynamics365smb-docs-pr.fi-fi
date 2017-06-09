---
title: "Kanadan arvonlisävero | Microsoft Docs"
description: "Lisätietoja arvonlisäverosta (GST) ja harmonisoidusta arvonlisäverosta (HST)."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 03/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e1866f5047a826f3d527267d901eb30279d5b4e4
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-goods-and-services-tax-in-canada"></a>Kanadan arvonlisävero
Jos Kanadassa toimittajalla ei ole liiketilaa provinssissa, jossa ostoja tehdään, toimittaja veloittaa vain arvonlisäveroa (GST) tai harmonisoitua arvonlisäveroa (HST). Jos provinssissa on käytössä provinssin arvonlisävero (PST), ostajan on laskettava myös PST ja maksettava se suoraan provinssiin. Kun provinssin veroaluekoodi on valittuna, [!INCLUDE[d365fin](includes/d365fin_md.md)] käyttää sitä PST:n laskemisessa ja kirjaa sen. Tällöin verovelkaa on sekä pääkirjanpidossa että arvonlisäverotietueissa. Tämän vuoksi valitun veroaluekoodin tulee olla se, jossa on valittuna PST, ei GST.  

Lisätietoja on kohdassa [Kanadan arvonlisävero ja veroryhmät](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>GST-/HST-tiedoston lähettäminen
Ostoasiakirjojen verotietoja käytetään veroviranomaisille annettavan GST-/HST-verkkotiedoston siirron luomisessa. Tämä tiedosto sisältää arvonlisäveron (GST) ja harmonisoidun arvonlisäveron (HST). Tiedosto on luotu .tax-muodossa, joka voidaan siirtää verkossa.  

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yhdysvaltojen ja Kanadan arvonlisävero ja veroryhmät](us-finance-sales-tax.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

