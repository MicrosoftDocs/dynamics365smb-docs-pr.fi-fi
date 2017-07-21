---
title: "Valuutan vaihtokurssien päivittäminen| Microsoft Docs"
description: "Voit käyttää yrityksessä useita valuuttoja määrittämällä kullekin valuutalle koodin ja käyttämällä ulkoista vaihtokurssipalvelua, kuten Yahoota."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Toimintaohje: Valuutan vaihtokurssien päivittäminen
Kaikille valuutoille täytyy määrittää koodi, jos yritys ostaa tai myy käyttäen jotain muuta valuuttaa kuin paikallista valuuttaa, jos yrityksellä on myyntisaamisia tai ostovelkoja muissa valuutoissa; tai jos yritys tallentaa KP-kauppatapahtumia eri valuuttoina.  

> [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).

Voit pitää valuutan vaihtokurssit ajan tasalla ulkoisen palvelun avulla. Yahoon valuutanvaihtokurssit -palvelu on asennettu valmiiksi ja odottaa käyttöönottoa.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Valuutanvaihdon kurssipalvelun määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Valuutanvaihtokurssipalvelut** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät **Valuutanvaihtokurssipalvelut**-ikkunassa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ota palvelu käyttöön valitsemalla **Käytössä**.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Valuutan vaihtokurssien päivittäminen palvelun avulla
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, anna **Valuutat** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Päivitä valuutan vaihtokurssit** -toiminto.

**Valuutat**-ikkunan **Vaihtokurssi**-kentän arvo päivittyy uusimman valuutan vaihtokurssin mukaan.

## <a name="see-also"></a>Katso myös
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

