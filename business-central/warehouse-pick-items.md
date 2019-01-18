---
title: Nimikkeiden poiminta | Microsoft Docs
description: "Jos varastotoimintona on nimikkeiden poimiminen ennen nimikkeiden toimitusta tai kulutusta, se voidaan suorittaa eri tavoilla sen mukaan, miten varastoinninhallinnan ominaisuudet on määritetty. [Määritysten](../configure-warehouse-processes.md) monimutkaisuus voi vaihdella: ominaisuusluettelossa ei ole varastotoimintoja lainkaan, tilauskohtaisessa fyysisen varastoinnin perusmäärityksissä käsittelytoimintoja on vain muutama toiminto, kun laajennetuissa varastomäärityksissä kaikki varastotoiminnot tehdään ohjatun työnkulun mukaisesti."
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
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 6a51a509ae1281d7c6bfe19e5276b516982a5fa5
ms.contentlocale: fi-fi
ms.lasthandoff: 11/22/2018

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
|Poimi komponentteja tuotantoa tai kokoonpanoa varten fyysisen varastoinnin perusmäärityksessä tai laajennetussa varastointimäärityksessä.|[Poiminta tuotantoon tai kokoonpanoon](warehouse-how-to-pick-for-production.md)|  
|Suunnittele optimoituja poimintaohjeita toimituksille niin, että varastotyöntekijöiden ei tarvitse käsitellä suoraan kirjattuja toimituksia.|[Poimintojen suunnitteleminen työkirjoissa](warehouse-how-to-plan-picks-in-worksheets.md)|  
|Poimi nimikkeitä teknisesti erityistarkoituksia varten esimerkiksi silloin, kun tuotantoyksikkö tarvitsee lisää komponentteja. Tällöin nimikkeet eivät teknisesti poistu varastosta.|[Poimiminen ja hyllyttäminen ilman lähdeasiakirjaa](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Lisätietoja siitä, miten nimikkeitä poimitaan automaattisesti vanhentumispäivän perusteella esimerkiksi silloin, kun kyse on helposti pilaantuvista tuotteista.|[FEFO-poiminta](warehouse-picking-by-fefo.md)|
|Jaa poimintarivi useisiin riveihin esimerkiksi silloin, kun nimikkeitä ei ole tarpeeksi määritetyssä varastopaikassa.|[ Varastotoimintorivien jakaminen](warehouse-how-to-split-warehouse-activity-lines.md)|
|Hae suoraan varastotyöntekijälle määritetyt poiminnat.|[Fyysisen varaston varausten etsiminen](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

