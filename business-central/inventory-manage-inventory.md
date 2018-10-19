---
title: Varaston hallinta| Microsoft Docs
description: "Tässä ohjeaiheessa käsitellään fyysisten tuotteiden, joilla käydään kauppaa, hallintaa, kuten varaston käsittelyä fyysisessä varastossa."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1f79c20cb68ff1802bb97914a7ac1e458ca28f3a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---

# <a name="inventory"></a>Vaihto-omaisuus
Jokaiselle fyysiselle tuotteelle, jolla käydään kauppaa, on luotava **Varasto**-tyyppinen nimikekortti. Asiakkaille tarjottavat nimikkeet, joita ei säilytetä varastossa, voidaan rekisteröidä luettelonimikkeiksi. Ne voidaan muuntaa varastonimikkeiksi tarvittaessa. Voit suurentaa tai pienentää varastossa olevien nimikkeiden määrää kirjaamalla arvon suoraan nimiketapahtumiin esimerkiksi fyysisen määrän jälkeen tai jättämällä ostoja kirjaamatta.

Varaston arvon nousut ja laskut kirjataan luonnollisesti myös silloin, kun osto- ja myyntiasiakirjat kirjataan. Lisätietoja on kohdissa [Ostojen kirjaaminen](purchasing-how-record-purchases.md), [Tuotteiden myyminen](sales-how-sell-products.md) ja [Myynnin laskuttaminen](sales-how-invoice-sales.md). Sijaintien väliset siirrot muuttavat varastomääriä yrityksen fyysisten varastojen kesken.   

Voit suurentaa nimikkeiden yhteenvetoa ja auttaa niiden etsimisessä luokittelemalla nimikkeet ja antamalla niille määritteitä, joiden perusteella voidaan tehdä hakuja ja lajitteluja.

> [!NOTE]
> Nimikkeiden fyysistä käsittelyä kutsutaan varastotoiminnoiksi. Lisätietoja on kohdassa [Fyysisen varaston hallinta](warehouse-manage-warehouse.md).

## <a name="inventory-reconciliation"></a>Varaston täsmäytys
Kun kirjaat varastotapahtumia, kuten myyntitoimituksia, ostolaskuja tai varaston muutoksia, muuttuneet nimikekustannukset kirjataan niiden arvotapahtumiin. Jotta varastoarvon muutos päivittyisi talouskirjoihin, varastokustannukset kirjataan automaattisesti pääkirjanpidon liittyviin varastotileihin. Jokaista itse kirjattua varastotapahtumaa kohti kirjataan sopiva arvo varastotilille, muutostilille ja myytyjen tuotteiden kustannusten tilille pääkirjanpidossa. Lisätietoja on kohdassa [Varaston kustannusten täsmäyttäminen pääkirjanpitoon](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Vaikka kustannukset kirjattaisiin automaattisesti pääkirjanpitoon, on tarpeen varmistaa, että tavaroiden kustannukset välitetään liitetään lähtevälle tapahtumalle. Tämä on erityisen tärkeää, kun myyt tavaroita ennen näiden tavaroiden oston laskutusta. Tätä kutsutaan kustannusmuutokseksi. Nimikekustannukset muutetaan automaattisesti nimiketapahtumia kirjattaessa, mutta voit muuttaa niitä myös manuaalisesti. Lisätietoja on kohdassa [Nimikekustannuksien muuttaminen](inventory-how-adjust-item-costs.md).

|Vastaanottaja |Katso |
|---|----|
|Luo niille varastonimikkeille nimikekortit, joilla käyt kauppaa.|[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)|
|Jäsennä päänimikkeet, joita myydään päänimikkeen osista koostuvina paketteina tai jotka kootaan tilausta tai varastointia varten.|[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)|
|Ylläpidä nimikkeiden yhteenvetoa ja helpottaa nimikkeiden etsimistä ja lajittelua järjestämällä nimikkeet luokkiin.|[Nimikkeiden luokitteleminen](inventory-how-categorize-items.md)|
|Nimikkeiden lajitteleminen ja löytäminen on helpompaa, kun määrität nimikkeisiin eri arvotyyppien määritteet.|[Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md)|
|Luo niille nimikkeille erityisnimikekortit, joita tarjoat asiakkaille, mutta joita ei säilytetä varastossa.|[Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md)|
|Suorita nimiketapahtumien inventointi, tee niissä negatiivisia tai positiivisia oikaisuja ja muuta niiden tietoja, kuten sijaintia tai erä numeroa.|[Varaston laskeminen, muuttaminen ja uudelleenluokitus](inventory-how-count-adjust-reclassify.md)|
|Näytä nimikkeiden saatavuus sijainnin, jakson tai myynti- tai ostotapahtuman mukaan tai sen mukaan, miten niitä käytetään tuotannon tuoterakenteessa.|[Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)|
|Voit siirtää varastonimikkeitä sijaintien välillä siirtotilausten, varastotapahtumien hallinnan tai nimikkeen uudelleenluokituspäiväkirjan avulla.|[Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)|
|Varaa varaston nimikkeitä tai saapuvia nimikkeitä myyntitilauksiin, ostotilauksiin, huoltotilauksiin, kokoonpanotilauksiin tai tuotantotilauksiin.|[Nimikkeiden varaaminen](inventory-how-to-reserve-items.md)|
|Määritä sarja- tai eränumerot lähtevän tai saapuvan asiakirjan tai päiväkirjan riville esimerkiksi silloin, kun nimikkeitä on seurattava tuotepalautusten vuoksi.|[Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md)|
|Etsi esimerkiksi palautustilanteissa, missä sarja- tai eränumeroita käytettiin toimitusketjussa.|[Nimikeseurannan nimikkeiden jäljittäminen](inventory-how-to-trace-item-tracked-items.md)|
|Estä nimikkeiden vienti myynti- tai ostoriveille tai sen kirjaaminen mihinkään tapahtumaan.|[Nimikkeiden estäminen](inventory-how-block-items.md)|
|Hallitse myyntitoimistojen, osto-osastojen tai tehtaan suunnittelutoimistojen liiketoimintatoiminnoissa eri sijainneissa.|[Vastuupaikkojen käyttäminen](inventory-responsibility-centers.md)|

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

