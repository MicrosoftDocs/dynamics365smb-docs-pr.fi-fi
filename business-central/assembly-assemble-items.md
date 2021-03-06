---
title: Kokoonpanon hallinta | Microsoft Docs
description: Tue yrityksiä, jotka toimittavat asiakkailleen tuotteita yhdistämällä osia yksinkertaisilla prosesseilla ilman tuotantotoimintojen tarvetta mutta jonka ominaisuuksilla voi koota aiemmin luotuja ominaisuuksia, kuten myynti, suunnittelu, varaukset ja varastointi, integroivia nimikkeitä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 111f78578f298c662cc5a923a0b05c487f68b4c7
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215601"
---
# <a name="assembly-management"></a>Kokoonpanon hallinta
Tukeakseen yrityksiä, jotka toimittavat asiakkailleen tuotteita yhdistämällä osia yksinkertaisissa prosesseissa ilman tuotantotoimintojen tarvetta, [!INCLUDE[prod_short](includes/prod_short.md)] sisältää ominaisuuksia, jotka kokoavat nimikkeitä, joissa on olemassa olevia ominaisuuksia, kuten myynti, suunnittelu, varaukset, ja varastointi.  

 Kokoonpanon nimike määritetään myytävänä kohteena, joka sisältää kokoonpanon tuoterakenteen. Lisätietoja on kohdassa [Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md).

 Kokoonpanotilaukset ovat sisäisiä tilauksia, aivan kuten tuotantotilaukset, joita käytetään kokoonpanoprosessin hallinnassa sekä myyntivaatimusten liittämiseksi asianmukaisiin varastotoimintoihin. Kokoonpanotilaukset eroavat muista tilaustyypeistä, sillä ne kattavat sekä tuotoksen että kulutuksen, kun ne kirjataan. Kokoonpanotilauksen otsikko toimii samaan tapaan kuin tuotospäiväkirja ja kokoonpanotilauksen rivit toimivat samalla tavalla kuin kulutuspäiväkirjan rivit.  

 Just-In-Time -varastostrategian ja kyvyn mukauttaa tuotteet asiakkaan vaatimusten mukaisiksi tukemiseksi kokoonpanotilauksia voidaan automaattisesti luoda ja linkittää heti kun myyntitilausrivi on luotu. Linkki myyntikysynnän ja kokoonpanotarjonnan kokoonpanon välillä mahdollistaa myyntitilauksen käsittelijöille kokoonpano-osan mukauttamisen lennossa, toimituspäivien lupaamisen osan saatavuuden mukaan, ja tuotoksen ja toimituksen kirjaamisen valmiille nimikkeelle suoraan myyntitilausliittymästä. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  

 Yhdellä myyntitilauksen rivillä voit myydä määrän, joka on saatavissa ja joka on poimittava varastosta, yhdessä sen määrän kanssa, joka on kokoonpantava tilausta varten. Tietyt säännöt hallinnoivat sellaisten määrien jakelua, jotta varmistetaan, että kokoonpano tilausta varten -määrät ohittavat tärkeysjärjestyksessä varastomäärät osatoimituksissa. Lisätietoja on ohjeaiheen [Tietoja Kokoonpano tilausta varten- tai Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md) kohdassa Skenaarioiden yhdistelmä.  

 Erityinen toiminto koskee tilausta varten kokoonpantujen määrien toimitusta. Kun kokoonpano tilausta varten -määrä on toimitusvalmis, varastotyöntekijä kirjaa varastopoiminnan myyntitilauksen kyseiselle riville tai riveille. Tämä puolestaan luo varastosiirron osille, kirjaa kokoonpanon tuotoksen ja myyntitilauksen toimituksen. Lisätietoja on ohjeaiheen [Nimikkeiden poiminta varaston poiminnoissa](warehouse-how-to-pick-items-with-inventory-picks.md) kohdassa Kokoonpano tilausta varten -nimikkeiden käsitteleminen varaston poiminnoissa.

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.   

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Tutustu siihen, mikä ero on nimikkeiden kokoonpanolla juuri ennen myyntitilausten toimittamista ja nimikkeiden kokoonpanolla varastoitaviksi.|[Tietoja Kokoonpano tilausta varten- ja Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Täytä sijainnin korttien kentät ja määritä varaston asetuksissa, miten nimikkeet liikkuvat kokoonpano-osastossa.|[Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Muokkaa kokoonpanon nimike asiakkaan pyynnöstä myyntiprosessin aikana ja muunna se myynniksi hyväksynnän yhteydessä.|[Kokoonpano tilausta varten -myynnin tarjous](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Yhdistä osat ja luo nimike yksinkertaisessa prosessissa tilaukseen tai varastoon.|[Kokoa nimikkeet](assembly-how-to-assemble-items.md)|  
|Myy kokoonpanon nimikkeet, jotka eivät ole tällä hetkellä saatavilla, luomalla linkitetty kokoonpanotilaus toimittamaan myyntilauksen koko määrä tai sen osa.|[Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md)|
|Kun Kokoonpano tilausta varten -nimikkeet ovat jo varastossa, vähennä määrä kokoonpanotilauksesta ja varaa se varastosta.|[Varastonimikkeiden myyminen kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Kun myyt kokoonpanon nimikkeitä varastosta ja kaikki kohteet eivät ole saatavilla, toimita myyntitilauksen määrä osittain tai kokonaan käynnistämällä kokoonpanotilaus.|[Kokoonpano tilausta varten -nimikkeiden ja varastonimikkeiden myyminen yhdessä](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Tee puitemyyntitilauksia mukautetun kokoonpanon osille, ennen kuin teet säännöllisesti todelliset myyntitilaukset puitetilauksen sopimuksen mukaisesti.|[Puitekokoonpanotilausten luominen](assembly-how-to-create-blanket-assembly-orders.md)|
|Kumoa kirjattu kokoonpanotilaus esimerkiksi siksi, että kirjatussa tilauksessa on virheitä, jotka on korjattava.|[Kokoonpanon kirjauksen kumoaminen](assembly-how-to-undo-assembly-posting.md)|
|Tutustu siihen, mikä ero on kokoonpanon tuoterakenteella ja tuotannon tuoterakenteella, sekä niihin liittyviin käsittelyeroihin.|[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)|
|Tutustu siihen, miten kokoonpanon kulutusta ja tuotosta käsitellään, kun kokoonpanotilauksia kirjataan, ja miten tästä koituvat nimike- ja resurssikustannukset käsitellään ja jaetaan pääkirjanpitoon.|[Rakennetiedot: Kokoonpanotilauksen kirjaus](design-details-assembly-order-posting.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]