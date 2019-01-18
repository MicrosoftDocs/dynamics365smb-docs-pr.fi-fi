---
title: "Automaattinen irtotavaran erottelu ohjatulla hyllytyksellä ja poiminnalla | Microsoft Docs"
description: "Jos sijainneissa käytetään ohjattua hyllytystä ja poimintaa, voit erotella ison mittayksikön pienempiin mittayksiköihin, kun luodaan fyysisen varastoinnin ohjeita, jotka täyttävät lähdeasiakirjojen, tuotantotilausten tai sisäisten poimintojen ja hyllytysten tarpeet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: c328df334d1bb1be33ced814677c3ef3ea634799
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Irtotavaran ohjatulla hyllytyksellä ja poiminnalla tapahtuvan automaattisen erottelun ottaminen käyttöön
Jos sijainneissa käytetään ohjattua hyllytystä ja poimintaa, [!INCLUDE[d365fin](includes/d365fin_md.md)] voi useissa eri tilanteissa tehdä automaattisen erottelun eli jakaa ison mittayksikön pienempiin mittayksiköihin luodessaan fyysisen varastoinnin ohjeita, jotka täyttävät lähdeasiakirjojen, tuotantotilausten tai sisäisten poimintojen ja hyllytysten tarpeet. Erotteleminen tarkoittaa joskus myös sitä, että pienempiä mittayksiköitä kootaan tarpeen mukaan yhteen, jotta vastattaisiin lähteviin pyyntöihin: tämä siis tarkoittaa itse asiassa ison mittayksikön jakamista lähdeasiakirjassa tai tuotantotilauksessa pienempiin mittayksiköihin, jotka ovat saatavilla fyysisessä varastossa.   

## <a name="breakbulking-in-picks"></a>Erotteleminen poiminnoissa  
Jos haluat varastoida nimikkeitä useissa eri mittayksiköissä ja antaa ohjelman yhdistellä automaattisesti niitä tarpeiden mukaisesti poimintaprosessissa, lisää rasti sijaintikortin  **Salli erottelu** -kenttään.  

Ohjelma etsii tehtävän suorittamiseksi automaattisesti nimikettä, joka olisi samassa mittayksikössä. Jos ohjelma ei löydä tätä nimikkeen muotoa, ja jos olet lisännyt rastin kyseiseen kenttään, ohjelma ehdottaa ison mittayksikön jakamista tarvittavaksi mittayksiköksi.  

Jos järjestelmä löytää vain pieniä mittayksiköitä, se ehdottaa, että nimikkeitä kerätään yhteen toimituksen tai tuotantotilauksen määrän täyttämiseksi. Itse asiassa se jakaa lähdeasiakirjan ison mittayksikön pienempiin poimintaa varten.  

## <a name="breakbulking-in-put-aways"></a>Erottelu hyllytyksissä  
Ohjelma ehdottaa fyysisen varastoinnin hyllytyksessä automaattisesti Sijoita toimintorivit hyllytyksen mittayksikössä (esimerkiksi kappaleissa), vaikka nimikkeet saapuvat eri mittayksikössä.  

## <a name="breakbulking-in-movements"></a>Erottelu varastosiirroissa  
Ohjelma tekee automaattisen erottelun myös täydennyssiirroissa, jos **Laske var.paikan täydennys** -sivun **Vaihtoehdot**-pikavälilehden **Salli erottelu** -kenttä on valittu.  

Muunnosprosessin mittayksiköstä toiseen tuloksia voi katsella välissä olevina erotteluriveinä hyllytys-, poiminta- ja varastosiirto-ohjeissa.  

> [!NOTE]  
>  Jos lisäät valintamerkin **Määritä erottelusuodatus** -kenttään fyysisen varaston ohjeiden otsikossa, ohjelma piilottaa erottelurivit aina, kun iso mittayksikkö aiotaan käyttää kokonaan. Esimerkiksi jos kuormalava on 12 kappaletta ja aiot käyttää kaikki 12 kappaletta, poiminta ohjaa suoraan ottamaan kuormalavan ja sijoittavan 12 kappaletta. Jos sinun täytyy kuitenkin poimia vain 9 kappaletta, erottelurivejä ei piiloteta, vaikka olet lisännyt rastin **Erottelusuodatus**-kenttään, koska jäljellä olevat 3 kappaletta täytyy sijoittaa jonnekin varastossa.  

> [!NOTE]  
>  Jos haluat mittayksiköiden käytön olevan optimaalista varastossa, myös erotteluominaisuuden yhteydessä, sinun tulisi yrittää aina, kun on mahdollista:  
>   
> - Määrittää nimikkeen perusmittayksiköksi pienin mittayksikkö, jota oletat käsitteleväsi fyysisen varastoinnin prosesseissa.  
> - Määrittää nimikkeen vaihtoehtoisiksi mittayksiköiksi perusmittayksikön kerrannaisia.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

