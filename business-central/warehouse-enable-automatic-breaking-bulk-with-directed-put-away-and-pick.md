---
title: Irtotavaran erottelu ohjatulla hyllytyksellä ja poiminnalla
description: Lue, miten voit ottaa käyttöön automaattisen irtotavaran erottelun ohjatulla hyllytyksellä ja poiminnalla sekä irtotavaran erottelun esimerkiksi poiminnassa, hyllytyksessä ja siirroissa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 5703, 7352
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: f16fb21773a519edc77fca615d679e106b397af8
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2022
ms.locfileid: "8382765"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Irtotavaran ohjatulla hyllytyksellä ja poiminnalla tapahtuvan automaattisen erottelun ottaminen käyttöön
Jos sijainneissa käytetään ohjattua hyllytystä ja poimintaa, [!INCLUDE[prod_short](includes/prod_short.md)] voi useissa eri tilanteissa tehdä automaattisen erottelun eli jakaa ison mittayksikön pienempiin mittayksiköihin luodessaan fyysisen varastoinnin ohjeita, jotka täyttävät lähdeasiakirjojen, tuotantotilausten tai sisäisten poimintojen ja hyllytysten tarpeet. Erotteleminen tarkoittaa joskus myös sitä, että pienempiä mittayksiköitä kootaan tarpeen mukaan yhteen, jotta vastattaisiin lähteviin pyyntöihin: tämä siis tarkoittaa itse asiassa ison mittayksikön jakamista lähdeasiakirjassa tai tuotantotilauksessa pienempiin mittayksiköihin, jotka ovat saatavilla fyysisessä varastossa.   

## <a name="breakbulking-in-picks"></a>Erotteleminen poiminnoissa  
Jos haluat varastoida nimikkeitä useissa eri mittayksiköissä ja antaa ohjelman yhdistellä automaattisesti niitä tarpeiden mukaisesti poimintaprosessissa, lisää rasti sijaintikortin  **Salli erottelu** -kenttään.  

Sovellus etsii tehtävän toteuttamista varten automaattisesti nimikettä, joka olisi samassa mittayksikössä. Jos sovellus ei löydä tätä nimikkeen muotoa, ja jos olet valinnut kyseisen kentän, sovellus ehdottaa ison mittayksikön jakamista tarvittavaksi mittayksiköksi.  

Jos järjestelmä löytää vain pieniä mittayksiköitä, se ehdottaa, että nimikkeitä kerätään yhteen toimituksen tai tuotantotilauksen määrän täyttämiseksi. Itse asiassa se jakaa lähdeasiakirjan ison mittayksikön pienempiin poimintaa varten.  

## <a name="breakbulking-in-put-aways"></a>Erottelu hyllytyksissä  
Sovellus ehdottaa fyysisen varastoinnin hyllytyksessä automaattisesti Sijoita toimintorivit hyllytyksen mittayksikössä (esimerkiksi kappaleissa), vaikka nimikkeet saapuvat eri mittayksikössä.  

## <a name="breakbulking-in-movements"></a>Erottelu varastosiirroissa  
Sovellus tekee automaattisen erottelun myös täydennyssiirroissa, jos **Laske var.paikan täydennys** -sivun **Vaihtoehdot**-pikavälilehden **Salli erottelu** -kenttä on valittu.  

Muunnosprosessin mittayksiköstä toiseen tuloksia voi katsella välissä olevina erotteluriveinä hyllytys-, poiminta- ja varastosiirto-ohjeissa.  

> [!NOTE]  
>  Jos lisäät valintamerkin **Määritä erottelusuodatus** -kenttään fyysisen varaston ohjeiden otsikossa, sovellus piilottaa erottelurivit aina, kun iso mittayksikkö aiotaan käyttää kokonaan. Esimerkiksi jos kuormalava on 12 kappaletta ja aiot käyttää kaikki 12 kappaletta, poiminta ohjaa suoraan ottamaan kuormalavan ja sijoittavan 12 kappaletta. Jos sinun täytyy kuitenkin poimia vain 9 kappaletta, erottelurivejä ei piiloteta, vaikka olet lisännyt rastin **Erottelusuodatus**-kenttään, koska jäljellä olevat 3 kappaletta täytyy sijoittaa jonnekin varastossa.  

> [!NOTE]  
>  Jos haluat mittayksiköiden käytön olevan optimaalista varastossa, myös erotteluominaisuuden yhteydessä, sinun tulisi yrittää aina, kun on mahdollista:  
>   
> - Määrittää nimikkeen perusmittayksiköksi pienin mittayksikkö, jota oletat käsitteleväsi fyysisen varastoinnin prosesseissa.  
> - Määrittää nimikkeen vaihtoehtoisiksi mittayksiköiksi perusmittayksikön kerrannaisia.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Warehouse Managementin määrittäminen](warehouse-setup-warehouse.md) 
[Kokoonpanon hallinta](assembly-assemble-items.md)
[Rakennetiedot: Warehouse Management](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]