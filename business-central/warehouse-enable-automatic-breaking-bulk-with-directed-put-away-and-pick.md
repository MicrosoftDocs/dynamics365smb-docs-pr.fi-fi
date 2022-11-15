---
title: Irtotavaran erottelu ohjatulla hyllytyksellä ja poiminnalla
description: Lue, miten voit ottaa käyttöön automaattisen irtotavaran erottelun ohjatulla hyllytyksellä ja poiminnalla sekä irtotavaran erottelun esimerkiksi poiminnassa, hyllytyksessä ja siirroissa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 5703, 7352
ms.date: 11/04/2022
ms.author: bholtorf
ms.openlocfilehash: d5e8ab6f0e60ab8874669c7e5127411acc58957b
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744675"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Irtotavaran ohjatulla hyllytyksellä ja poiminnalla tapahtuvan automaattisen erottelun ottaminen käyttöön

Jos sijainneissa käytetään ohjattua hyllytystä ja poimintaa, [!INCLUDE[prod_short](includes/prod_short.md)] voi erotella ison mittayksikön pienempiin mittayksiköihin, kun luodaan fyysisen varastoinnin ohjeita, jotka täyttävät lähdeasiakirjojen, tuotantotilausten tai sisäisten poimintojen ja hyllytysten tarpeet. Erottelu voi tarkoittaa myös sitä, että nimikkeitä kerätään pienemmissä mittayksiköissä lähdeasiakirjan tai tuotantotilauksen suuremman mittayksikön määrän verran.

## <a name="breakbulk-in-picks"></a>Erotteleminen poiminnoissa  

Jos haluat varastoida nimikkeitä useissa eri mittayksiköissä sijainnissa ja antaa ohjelman yhdistellä automaattisesti niitä poimintaprosessissa, ota käyttöön sijaintikortin **Salli erottelu** -valinta. Myöhemmin [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus etsii tehtävän toteuttamista varten automaattisesti nimikettä, joka olisi samassa mittayksikössä. Jos sellaista ei löydy, [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelma ehdottaa, että katkaiset suuremman mittayksikön tarpeen mukaan pienemmäksi.  

Jos vain pieniä mittayksiköitä on tarjolla, [!INCLUDE [prod_short](includes/prod_short.md)] ehdottaa, että nimikkeitä kerätään yhteen toimituksen tai tuotantotilauksen määrän täyttämiseksi. Itse asiassa se jakaa lähdeasiakirjan ison mittayksikön pienempiin poimintaa varten.  

## <a name="breakbulk-in-put-aways"></a>Erottelu hyllytyksissä  

[!INCLUDE [prod_short](includes/prod_short.md)] ehdottaa, että fyysisen varastoinnin hyllytykset asettavat toimenpiderivit hyllytyksen mittayksikköön. Se voi esimerkiksi ehdottaa kappaletta, vaikka nimikkeet saapuvat eri mittayksikössä.  

## <a name="breakbulk-in-movements"></a>Erottelu varastosiirroissa  

[!INCLUDE [prod_short](includes/prod_short.md)] voi myös tehdä erottelun täydennyksen siirroissa, jos **Laske varasto paikkojen täydennys** -sivulla oleva **Salli erottelu** -valinta on otettu käyttöön.  

Muunnosprosessin mittayksiköstä toiseen tuloksia voi katsella välissä olevina erotteluriveinä hyllytys-, poiminta- ja varastosiirto-ohjeissa.  

> [!NOTE]  
> Jos lisäät valintamerkin **Määritä erottelusuodatus** -kenttään fyysisen varaston ohjeiden otsikossa, sovellus piilottaa erottelurivit aina, kun iso mittayksikkö aiotaan käyttää kokonaan. Esimerkiksi jos kuormalava on 12 kappaletta ja aiot käyttää kaikki 12 kappaletta, poiminta ohjaa suoraan ottamaan 1 kuormalavan ja sijoittavan 12 kappaletta. Jos kuitenkin poimit vain 9 kappaletta, erottelurivejä ei piiloteta, vaikka olisit valinnut **erottelusuodatus**-kentän. Rivejä ei piiloteta, koska jäljellä olevat kolme kappaletta täytyy laittaa jonnekin fyysiseen varastoon.  

> [!NOTE]  
> Jos haluat mittayksiköiden käytön olevan optimaalista varastossa, myös erottelun yhteydessä, sinun tulisi yrittää:  
>
> - Määrittää nimikkeen perusmittayksiköksi pienin mittayksikkö, jota oletat käsitteleväsi fyysisen varastoinnin prosesseissa.  
> - Määrittää nimikkeen vaihtoehtoisiksi mittayksiköiksi perusmittayksikön kerrannaisia.  

## <a name="see-also"></a>Katso myös  

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Warehouse Managementin määrittäminen](warehouse-setup-warehouse.md) 
[Kokoonpanon hallinta](assembly-assemble-items.md)
[Rakennetiedot: Warehouse Management](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]