---
title: Nimikkeiden hyllyttäminen
description: Nimikkeiden hyllytystapahtumat sen jälkeen, kun nimikkeet on vastaanotettu tai tuotettu, suoritetaan eri tavoin sen mukaan, miten varastoinninhallintajärjestelmän ominaisuudet on määritetty.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5770, 5783, 5784, 5786, 5795, 7334, 7352, 7354, 7356, 7375, 7379, 7390, 7394, 7396, 9312, 9315, 9343
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 90e1c5508dfa578a6231634e9a65257fae6777e1
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972120"
---
# <a name="putting-items-away"></a>Nimikkeiden hyllyttäminen

Varaston hyllytystoiminto nimikkeiden vastaanoton tai tuotoksen jälkeen suoritetaan eri tavoin sen mukaan, miten varastoinninhallintajärjestelmän ominaisuudet on määritetty. Määritysten monimutkaisuus voi vaihdella: ominaisuusluettelossa ei ole varastotoimintoja lainkaan, tilauskohtaisessa fyysisen varastoinnin perusmäärityksissä käsittelytoimintoja on vain muutama toiminto, kun laajennetuissa varastomäärityksissä kaikki varastotoiminnot tehdään ohjatun työnkulun mukaisesti. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

Jos haluat järjestää ja kirjata hyllytystiedot fyysisen varastoinnin asiakirjojen avulla, lisää valintamerkki sijaintikortin **Vaadi hyllytys** -kenttään. Tämä tarkoittaa, että kun saapuvan lähdeasiakirjan kautta on tulossa nimikkeitä fyysisen varastoinnin sijaintiin, järjestelmä hallitsee näiden nimikkeiden hyllytystä. Saapuva lähdeasiakirja voi olla ostotilaus, myyntipalautustilaus, saapuva siirtotilaus tai tuotantotilaus, jonka tuotos odottaa hyllytystä.  

Jos sijainti on asetettu käyttämään hyllytyskäsittelyä mutta ei vastaanoton käsittelyä, voit käyttää **Varaston hyllytys** -sivua hyllytyksen tietojen järjestämiseen, tulostaa sen, antaa varsinaisen hyllytyksen tuloksen ja kirjata hyllytystiedot, mikä puolestaan kirjaa myös lähdeasiakirjan vastaanottotiedot. Tuotantotilauksen yhteydessä kirjausprosessi kirjaa tilauksen tuotoksen ja päättää tuotantotilauksen.

Jos sijainnissa on määritetty pakolliseksi sekä vastaanoton että hyllytyksen käsittely eli olet lisännyt valintamerkit sijaintikortin **Vaadi vastaanotto**- ja **Vaadi hyllytys** -kenttiin, nimikkeiden hyllytykseen käytetään eri prosessia. Tällöin hyllytyksen käsittelyyn käytetään **F. varastoinnin hyllytys** -sivua. Fyysisen varastoinnin hyllytys toimii muuten samoin kuin varastohyllytys, mutta hyllytystietojen kirjauksen asemesta hyllytys rekisteröidään. Huomaa, että fyysisen varastoinnin hyllytyksen rekisteröinti ei kirjaa nimikkeiden vastaanottoa. Se vain päivittää varastopaikan sisällön. Varastopäällikkönä voit järjestää hyllytystiedot hyllytystyökirjojen avulla ennen yksittäisten fyysisen varastoinnin hyllytysohjeiden luontia.

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Kirjaa nimikkeiden vastaanotto suoraan saapuvasta tilausasiakirjasta. Tämä myös kirjaa hyllytyksen, sillä fyysisen varastoinnin määritystä ei ole.|[Nimikkeiden vastaanottaminen](warehouse-how-receive-items.md)|  
|Hyllytä nimikkeitä tilauskohtaisesti ja kirjaa vastaanotto samassa perusvarastointimäärityksen toiminnossa.  |[Nimikkeiden hyllyttäminen varastohyllytyksen avulla](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Hyllytä nimikkeitä tilauksista laajennetussa varastointimäärityksessä.|[Nimikkeiden hyllyttäminen ja fyysisen varaston hyllytykset](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  
|Hyllytä tuotettuja ja kokoonpantuja nimikkeitä fyysisen varastoinnin perusmäärityksissä tai laajennetussa varastointimäärityksessä.|[Tuotannon tai kokoonpanon tuotoksen hyllyttäminen](warehouse-how-to-put-away-production-output.md)|
|Suunnittele optimoituja hyllytysohjeita useille kirjatuille fyysisen varastoinnin vastaanotoille, jolloin varastotyöntekijöiden ei tarvitse käsitellä suoraan vastaanottoja.|[Hyllytysten suunnitteleminen työkirjoissa](warehouse-how-to-plan-put-aways-in-worksheets.md)|  
|Hyllytä uudelleen nimikkeitä, jotka on poimittu teknisesti sisäisen poiminnan avulla, esimerkiksi sellaisessa tuotantotilauksessa, joka ei ole kuluttanut odotettua määrää.|[Poimiminen ja hyllyttäminen ilman lähdeasiakirjaa](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Jaa hyllytysrivi, jotta osa hyllytysmäärästä voidaan sijoittaa varastopaikkoihin, koska määritetty varastopaikka on täysi.|[ Varastotoimintorivien jakaminen](warehouse-how-to-split-warehouse-activity-lines.md)|
|Hae suoraan varastotyöntekijälle määritetyt hyllytykset.|[Fyysisen varaston varausten etsiminen](warehouse-how-to-find-your-warehouse-assignments.md)|

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Warehouse Managementin määrittäminen](warehouse-setup-warehouse.md) 
[Kokoonpanon hallinta](assembly-assemble-items.md)
[Rakennetiedot: Warehouse Management](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]