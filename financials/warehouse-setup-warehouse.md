---
title: "Varastointiprosessien määrittäminen | Microsoft Docs"
description: "Yrityksen jakelustrategia vaikuttaa varastointiprosessien määrittämiseen. Siihen sisältyy esimerkiksi erilaisten nimikkeiden käsittelyn määrittäminen fyysisen varaston eri sijainneissa, kuten varastopaikkojen valvonta-aste sekä varastotoimintojen välisen työnkulun laajuus."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 130d266d5e9ff5a4d862dd9a03a781b57afd52be
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-warehouse-management"></a>Varastoinninhallinnan määrittäminen
Yrityksen jakelustrategia vaikuttaa varastointiprosessien määrittämiseen. Siihen sisältyy esimerkiksi erilaisten nimikkeiden käsittelyn määrittäminen fyysisen varaston eri sijainneissa, kuten varastopaikkojen valvonta-aste sekä varastotoimintojen välisen työnkulun laajuus.  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.   

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Saat yleiskuvan varastoinnin perustoimintojen ja laajennettujen toimintojen eroista.|[Rakennetiedot: Fyysisen varaston yleiskuvaus](design-details-warehouse-overview.md)|  
|Määritä kahdeksan erilaista varastopaikkatyyppiä (kuten poimintavarastopaikka) ja niihin liittyvät toiminnot.|[Toimintaohje: Varastopaikkojen määrittäminen](warehouse-how-to-set-up-bin-types.md)|  
|Luo varastopaikkoja manuaalisesti tai automaattisesti. Luodut varastopaikat sisältävät varastopaikkamallin mukaiset tiedot, kuten nimen, numerosarjan ja luokan.|[Toimintaohje: Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md)|  
|Määritä tiettyyn varastopaikkaan varastoitavat nimikkeet sekä säännöt, jotka määrittävät, milloin varastopaikka täytetään tietyllä nimikkeellä.|[Toimintaohje: Varastopaikan sisällön luominen](warehouse-how-to-set-up-bin-contents.md)|  
|Määritä, että nimike sijoitetaan aina tiettyyn varastopaikkaan.|[Oletusvarastopaikkojen määrittäminen nimikkeille](warehouse-how-to-assign-default-bins-to-items.md)|
|Luo malleja, jotka määrittävät, mihin ja miten nimikkeet hyllytetään ohjatun hyllytyksen aikana.|[Toimintaohje: Hyllytysmallien määrittäminen](warehouse-how-to-set-up-put-away-templates.md)|
|Määritä käyttäjät varastotyöntekijöiksi tiettyihin sijainteihin.|[Toimintaohje: Varastotyöntekijöiden määrittäminen](warehouse-how-to-set-up-warehouse-employees.md)|
|Ohjaa nimikkeiden sijoittelua tyypin, luokittelun tai käsittelytason mukaan määrittämällä fyysisen varaston erityyppiset varastopaikat.|[Toimintaohje: Sijaintien määrittäminen varastopaikkojen käyttämistä varten](warehouse-how-to-set-up-locations-to-use-bins.md)|
|Valmistele sijainti varastotoimintoja varten määrittämällä lisäasetukset.|[Toimintaohje: Olemassa olevien sijaintien muuntaminen fyysisen varaston sijainneiksi](warehouse-how-to-convert-existing-locations-to-warehouse-locations.md)|
|Ota käyttöön kokoonpano- tai tuotantotilausten poimiminen, siirtäminen ja hyllyttäminen fyysisen varastoinnin perusmäärityksissä.|[Toimintaohje: Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|  
|Määritä laajimman varastoinninhallinnan nimikkeet ja sijainnit, joissa kaikkien toimintojen on noudatettava tarkkaa työnkulkua.|[Toimintaohje: Nimikkeiden ja sijaintien määrittäminen ohjattua hyllytystä ja poimintaa varten](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)|  
|Määritä, milloin ja miten fyysisen varaston sijaintien nimikkeet lasketaan kunnossapitoa tai taloudellista raportointia varten.|[Toimintaohje: Varaston laskeminen, muuttaminen tai uudelleenluokitus](inventory-how-count-adjust-reclassify.md)|
|Ota käyttöön varastotyöntekijät erottelemaan suuria mittayksiköitä pieniksi mittayksiköiksi lähdeasiakirjojen tarpeen täyttämistä varten.|[Toimintaohje: Irtotavaran ohjatulla hyllytyksellä ja poiminnalla tapahtuvan automaattisen erottelun ottaminen käyttöön](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)|  
|Määritä, että fyysinen varastointi ehdottaa automaattisesti sellaisten nimikkeiden poimintaa, jotka vanhentuvat ensimmäisinä.|[Toimintaohje: FEFO-poiminnan ottaminen käyttöön](warehouse-picking-by-fefo.md)|
|Integroi viivakoodinlukijat varastoinninhallinnan ratkaisuihin.|[ADCS (Automated Data Capture System) -järjestelmä](warehouse-use-automated-data-capture-systems-adcs.md)|  
|Tutustu vihjeisiin, joiden avulla voi järjestellä uudelleen sijainteja, varastopaikkoja tai alueita ja tehostaa näin varastotoimintoja.|[Toimintaohje: Fyysisten varastojen järjesteleminen uudelleen](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

