---
title: Fyysisen varaston prosessien määrittäminen
description: Yrityksen jakelustrategia vaikuttaa varastointiprosessien määrittämiseen, esimerkiksi fyysisen varaston sijainteihin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5775, 7300, 7301, 7302, 7303, 7304, 7305, 7306, 7307, 7308, 7325, 7344, 7346, 7347, 7353, 7366
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 7864b7dcb09d0528f6f0674ae7af3740ab7e5951
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973230"
---
# <a name="setting-up-warehouse-management"></a>Varastoinninhallinnan määrittäminen

Yrityksen jakelustrategia vaikuttaa varastointiprosessien määrittämiseen. Siihen sisältyy esimerkiksi erilaisten nimikkeiden käsittelyn määrittäminen fyysisen varaston eri sijainneissa, kuten varastopaikkojen valvonta-aste sekä varastotoimintojen välisen työnkulun laajuus.  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Saat yleiskuvan varastoinnin perustoimintojen ja laajennettujen toimintojen eroista.|[Rakennetiedot: Fyysisen varaston yleiskuvaus](design-details-warehouse-overview.md)|  
|Määritä kahdeksan erilaista varastopaikkatyyppiä (kuten poimintavarastopaikka) ja niihin liittyvät toiminnot.|[Varastopaikkojen määrittäminen](warehouse-how-to-set-up-bin-types.md)|  
|Luo varastopaikkoja manuaalisesti tai automaattisesti. Luodut varastopaikat sisältävät varastopaikkamallin mukaiset tiedot, kuten nimen, numerosarjan ja luokan.|[Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md)|  
|Määritä tiettyyn varastopaikkaan varastoitavat nimikkeet sekä säännöt, jotka määrittävät, milloin varastopaikka täytetään tietyllä nimikkeellä.|[Varastopaikan sisältöjen luominen](warehouse-how-to-set-up-bin-contents.md)|  
|Määritä, että nimike sijoitetaan aina tiettyyn varastopaikkaan.|[Oletusvarastopaikkojen määrittäminen nimikkeille](warehouse-how-to-assign-default-bins-to-items.md)|
|Luo malleja, jotka määrittävät, mihin ja miten nimikkeet hyllytetään ohjatun hyllytyksen aikana.|[Hyllytysmallien määrittäminen](warehouse-how-to-set-up-put-away-templates.md)|
|Määritä käyttäjät varastotyöntekijöiksi tiettyihin sijainteihin.|[Varastotyöntekijöiden määrittäminen](warehouse-how-to-set-up-warehouse-employees.md)|
|Ohjaa nimikkeiden sijoittelua tyypin, luokittelun tai käsittelytason mukaan määrittämällä fyysisen varaston erityyppiset varastopaikat.|[Sijaintien määrittäminen varastopaikkojen käyttämistä varten](warehouse-how-to-set-up-locations-to-use-bins.md)|
|Valmistele sijainti varastotoimintoja varten määrittämällä lisäasetukset.|[Aiemmin luotujen sijaintien muuntaminen fyysisen varaston sijainneiksi](warehouse-how-to-convert-existing-locations-to-warehouse-locations.md)|
|Ota käyttöön kokoonpano- tai tuotantotilausten poimiminen, siirtäminen ja hyllyttäminen fyysisen varastoinnin perusmäärityksissä.|[Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|  
|Määritä laajimman varastoinninhallinnan nimikkeet ja sijainnit, joissa kaikkien toimintojen on noudatettava tarkkaa työnkulkua.|[Nimikkeiden ja sijaintien määrittäminen ohjattua hyllytystä ja poimintaa varten](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)|  
|Määritä, milloin ja miten fyysisen varaston sijaintien nimikkeet lasketaan kunnossapitoa tai taloudellista raportointia varten.|[Varaston laskeminen, muuttaminen tai uudelleenluokitus](inventory-how-count-adjust-reclassify.md)|
|Ota käyttöön varastotyöntekijät erottelemaan suuria mittayksiköitä pieniksi mittayksiköiksi lähdeasiakirjojen tarpeen täyttämistä varten.|[Irtotavaran ohjatulla hyllytyksellä ja poiminnalla tapahtuvan automaattisen erottelun ottaminen käyttöön](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)|  
|Määritä, että fyysinen varastointi ehdottaa automaattisesti sellaisten nimikkeiden poimintaa, jotka vanhentuvat ensimmäisinä.|[FEFO-poiminnan ottaminen käyttöön](warehouse-picking-by-fefo.md)|
|Tutustu vihjeisiin, joiden avulla voi järjestellä uudelleen sijainteja, varastopaikkoja tai alueita ja tehostaa näin varastotoimintoja.|[Fyysisten varastojen uudelleenjärjestely](warehouse-how-to-restructure-warehouses.md)|
|Integroi viivakoodinlukijat varastoinninhallinnan ratkaisuihin. Vain paikallinen käyttöönotto.|[ADCS (Automated Data Capture System) -järjestelmä](warehouse-use-automated-data-capture-systems-adcs.md)|
|Määritä oletusraportteja, joita käytetään eri asiakirjatyypeille.|[Raporttien valinta Business Centralissa](across-report-selections.md)|

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)
[Rakennetiedot: Warehouse Management](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]