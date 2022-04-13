---
title: Nimikkeiden poiminta
description: Nimikkeiden poimiminen ennen nimikkeiden toimitusta tai kulutusta voidaan suorittaa eri tavoilla sen mukaan, miten varastoinninhallinnan ominaisuudet on määritetty.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5779, 5798, 7343, 7345, 7357, 7359, 7377, 7392, 7395, 7397, 9313, 9316, 9344
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 028fb8d63045964fdb4e48cbbe3a6372677512d1
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520549"
---
# <a name="pick-items"></a>Nimikkeiden poiminta

Jos varastotoimintona on nimikkeiden poimiminen ennen nimikkeiden toimitusta tai kulutusta, se voidaan suorittaa eri tavoilla sen mukaan, miten varastoinninhallinnan ominaisuudet on määritetty. Määritysten monimutkaisuus voi vaihdella: ominaisuusluettelossa ei ole varastotoimintoja lainkaan, fyysisen varastoinnin perusmääritysten tilausten käsittelyssä on vain yksi tai useita toimintoja ja laajennetuissa varastomäärityksissä kaikki varastotoiminnot on suoritettava ohjatun työnkulun mukaisesti. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Jos haluat järjestää ja kirjata poimintatoiminnot varastoasiakirjoihin, lisää valintamerkki sijaintikortin **Vaadi poiminta** -kenttään. Tämä tarkoittaa, että kun lähtevälle lähdeasiakirjalle on poimittava nimikkeitä, järjestelmän on ohjattava näiden nimikkeiden poimintaa. Lähtevä lähdeasiakirja voi olla myyntitilaus, ostopalautustilaus, lähtevä siirtotilaus, huoltotilaus tai tuotantotilaus, jonka komponentit on poimittava.

> [!NOTE]
> Vaikka asetuksen nimenä on **Vaadi poiminta**, voit silti kirjata toimituksia suoraan lähdeasiakirjasta sijainnista, jossa olet valinnut tämän valintaruudun.

Jos sijainti on määritetty edellyttämään poimintakäsittelyä mutta ei toimituskäsittelyä, voit järjestää **Varaston poiminta** -sivulla poimintatiedot ja tulostaa ne, antaa poiminnan tuloksen sekä kirjata poimintatiedot, mikä puolestaan kirjaa nimikkeiden toimituksen. Jos poimitaan komponentteja tuotantotilausta varten, poiminnan kirjaus kirjaa myös kulutuksen.

Jos sijainti on määritetty edellyttämään sekä poiminta- että toimituskäsittelyä ja olet lisännyt valintamerkit sijaintikortin **Vaadi poiminta**- ja **Vaadi toimitus** -kenttiin, voit käsitellä poiminnan **F. varastoinnin poiminta** -sivulla. Fyysisen varastoinnin poiminta toimii muuten samoin kuin varaston poiminta, mutta poimintatietojen kirjauksen asemesta poiminta rekisteröidään. Tämä rekisteröintiprosessi ei kirjaa toimitusta, sillä se vain valmistelee nimikkeet toimitusta varten. Varastopäällikkönä voit järjestää poimintatiedot poimintatyökirjojen avulla ennen yksittäisten fyysisen varastoinnin poimintaohjeiden luontia.

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.   

|**Tehtävä**|**Katso**|
|------------|-------------|  
|Kirjaa nimikkeiden toimitus suoraan lähtevään tilausasiakirjaan, koska varastointitoimintoja ei ole. (Samalla toimitaan tavoin myyntitilausten, lähtevien siirtotilausten ja palautustoimitusten kohdalla.)|[Nimikkeiden lähettäminen](warehouse-how-ship-items.md)|  
|Poimi nimikkeitä tilauskohtaisesti ja kirjaa toimitus samassa perusvarastointimäärityksen toiminnossa.  |[Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md)|
|Poimi nimikkeitä tilauksia varten laajennetussa varastointimäärityksessä.|[Nimikkeiden poiminta fyysisen varaston poiminnassa](warehouse-how-to-pick-items-for-warehouse-shipment.md)|  
|Poimi komponentteja tuotantoa tai kokoonpanoa varten perusvarastointimäärityksessä.|[Tuotanto- tai kokoonpanopoiminta perusvarastointimäärityksissä](warehouse-how-to-pick-for-production.md)|
|Poimi komponentteja tuotantoa tai kokoonpanoa laajennetussa varastointimäärityksessä.|[Tuotanto- tai kokoonpanopoiminta laajennetuissa varastointimäärityksissä](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)|  
|Suunnittele optimoituja poimintaohjeita toimituksille niin, että varastotyöntekijöiden ei tarvitse käsitellä suoraan kirjattuja toimituksia.|[Poimintojen suunnitteleminen työkirjoissa](warehouse-how-to-plan-picks-in-worksheets.md)|  
|Poimi nimikkeitä teknisesti erityistarkoituksia varten esimerkiksi silloin, kun tuotantoyksikkö tarvitsee lisää komponentteja. Tällöin nimikkeet eivät teknisesti poistu varastosta.|[Poimiminen ja hyllyttäminen ilman lähdeasiakirjaa](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Lisätietoja siitä, miten nimikkeitä poimitaan automaattisesti vanhentumispäivän perusteella esimerkiksi silloin, kun kyse on helposti pilaantuvista tuotteista.|[FEFO-poiminta](warehouse-picking-by-fefo.md)|
|Jaa poimintarivi useisiin riveihin esimerkiksi silloin, kun nimikkeitä ei ole tarpeeksi määritetyssä varastopaikassa.|[ Varastotoimintorivien jakaminen](warehouse-how-to-split-warehouse-activity-lines.md)|
|Hae suoraan varastotyöntekijälle määritetyt poiminnat.|[Fyysisen varaston varausten etsiminen](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Warehouse Managementin määrittäminen](warehouse-setup-warehouse.md) 
[Kokoonpanon hallinta](assembly-assemble-items.md)
[Rakennetiedot: Warehouse Management](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]