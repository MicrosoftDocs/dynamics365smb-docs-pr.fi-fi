---
title: "Toimintaohje: Valuutan vaihtokurssien päivittäminen | Microsoft Docs"
description: "Useiden valuuttojen käsitteleminen"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b261da0f233ce78a9f14c2979c876be401ffedef
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Toimintaohje: Valuutan vaihtokurssien päivittäminen
Kaikille valuutoille täytyy määrittää koodi, jos yritys ostaa tai myy käyttäen jotain muuta valuuttaa kuin paikallista valuuttaa, jos yrityksellä on myyntisaamisia tai ostovelkoja muissa valuutoissa; tai jos yritys tallentaa KP-kauppatapahtumia eri valuuttoina.  

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md).

Voit pitää valuutan vaihtokurssit ajan tasalla ulkoisen palvelun avulla. Yahoon valuutanvaihtokurssit -palvelu on asennettu valmiiksi ja odottaa käyttöönottoa.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Valuutanvaihdon kurssipalvelun määrittäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Valuutanvaihtokurssipalvelut** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät **Valuutanvaihtokurssipalvelut**-ikkunassa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ota palvelu käyttöön valitsemalla **Käytössä**.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Valuutan vaihtokurssien päivittäminen palvelun avulla
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Valuutat** ja valitse sitten liittyvä linkki.
2. Valitse **Päivitä valuutan vaihtokurssit** -toiminto.

**Valuutat**-ikkunan **Vaihtokurssi**-kentän arvo päivittyy uusimman valuutan vaihtokurssin mukaan.

## <a name="see-also"></a>Katso myös
[Vuosien ja kausien sulkeminen](year-close-years-periods.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

