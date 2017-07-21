---
title: Varaston hallinta| Microsoft Docs
description: "Tässä ohjeaiheessa käsitellään fyysisten tuotteiden, joilla käydään kauppaa, hallintaa, kuten varaston käsittelyä fyysisessä varastossa."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 920df314dc8b671d4e2d99d8449ee02a74cb9078
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017

---

# <a name="inventory"></a>Vaihto-omaisuus
Jokaiselle fyysiselle tuotteelle, jolla käydään kauppaa, on luotava **Varasto**-tyyppinen nimikekortti. Asiakkaille tarjottavat nimikkeet, joita ei säilytetä varastossa, voidaan rekisteröidä ei-varastoitaviksi nimikkeiksi. Ne voidaan muuntaa varastonimikkeiksi tarvittaessa. Voit suurentaa tai pienentää varastossa olevien nimikkeiden määrää kirjaamalla arvon suoraan nimiketapahtumiin esimerkiksi fyysisen määrän jälkeen tai jättämällä ostoja kirjaamatta.

Varaston arvon nousut ja laskut kirjataan luonnollisesti myös silloin, kun osto- ja myyntiasiakirjat kirjataan. Lisätietoja on kohdassa [Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md), [Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md) ja [Toimintaohje: Myynnin laskuttaminen](sales-how-invoice-sales.md). Sijaintien väliset siirrot muuttavat varastomääriä yrityksen fyysisten varastojen kesken.   

Voit suurentaa nimikkeiden yhteenvetoa ja auttaa niiden etsimisessä luokittelemalla nimikkeet ja antamalla niille määritteitä, joiden perusteella voidaan tehdä hakuja ja lajitteluja.

Varmista, että nimikkeiden kustannukset välitetään liittyvään lähtevään myyntitapahtuman. Tämä on tärkeää etenkin tilanteissa, joissa myyt tavaroita ennen kyseisten nimikkeiden oston laskutusta. Tätä kutsutaan kustannusten muuttamiseksi, ja sen voi tehdä manuaalisesti tai automaattisesti nimiketapahtuman kirjauksen yhteydessä.

## <a name="inventory-reconciliation"></a>Varaston täsmäytys
Kun kirjaat varastotapahtumia, kuten myyntitoimituksia, ostolaskuja tai varaston muutoksia, ohjelma kirjaa muuttuneet nimikekustannukset niiden arvotapahtumiin. Jotta varastoarvon muutos päivittyisi talouskirjoihin, varastokustannukset kirjataan automaattisesti pääkirjanpidon liittyviin varastotileihin. Ohjelma kirjaa jokaista itse kirjaamaasi varastotapahtumaa kohti sopivan arvon varastotilille, muutostilille ja myytyjen tuotteiden kustannusten tilille pääkirjanpidossa.

Vaikka kustannukset kirjattaisiin automaattisesti pääkirjanpitoon, on tarpeen varmistaa, että tavaroiden kustannukset välitetään oikealle lähtevälle transaktioille. Tämä on erityisen tärkeää, kun myyt tavaroita ennen näiden tavaroiden oston laskutusta. Tätä kutsutaan kustannusmuutokseksi. Nimikekustannukset muutetaan automaattisesti, kun kirjaat nimiketapahtumia, mutta voit muuttaa niitä myös manuaalisesti. Lisätietoja on kohdassa Toimintaohje: Nimikekustannuksien muuttaminen.

|Vastaanottaja |Katso |
|---|----|
|Luo niille varastonimikkeille nimikekortit, joilla käyt kauppaa.|[Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)|
|Jäsennä päänimikkeet, joita myydään päänimikkeen osista koostuvina paketteina tai jotka kootaan tilausta tai varastointia varten.|[Toimintaohje: Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)|
|Ylläpidä nimikkeiden yhteenvetoa ja helpottaa nimikkeiden etsimistä ja lajittelua järjestämällä nimikkeet luokkiin.|[Toimintaohje: Nimikkeiden luokitteleminen](inventory-how-categorize-items.md)|
|Nimikkeiden lajitteleminen ja löytäminen on helpompaa, kun määrität nimikkeisiin eri arvotyyppien määritteet.|[Toimintaohje: Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md)|
|Luo niille nimikkeille erityisnimikekortit, joita tarjoat asiakkaille, mutta joita ei säilytetä varastossa.|[Toimintaohje: Ei-varastoitavien nimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md)|
|Suorita nimiketapahtumien inventointi, tee niissä negatiivisia tai positiivisia oikaisuja ja muuta niiden tietoja, kuten sijaintia tai erä numeroa.|[Toimintaohje: Varaston laskeminen, muuttaminen ja uudelleenluokitus](inventory-how-count-adjust-reclassify.md)|
|Näytä nimikkeiden saatavuus sijainnin, jakson tai myynti- tai ostotapahtuman mukaan tai sen mukaan, miten niitä käytetään kokoonpanon tuoterakenteessa.|[Toimintaohje: Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)|
|Voit siirtää varastonimikkeitä sijaintien välillä siirtotilausten, varastotapahtumien hallinnan tai nimikkeen uudelleenluokituspäiväkirjan avulla.|[Toimintaohje: Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)|
|Nosta tai laske vähintään yhden varaston nimikkeen arvoa kirjaamalla nimikkeen nykyinen laskettu arvo.|[Toimintaohje: Varaston uudelleenarvostus](inventory-how-revalue-inventory.md)|
|Muuta nimikekustannuksia automaattisesti tai manuaalisesti, kun haluat siirtää saapuvien tapahtumien kustannusmuutokset liittyviin lähteviin tapahtumiin.|[Toimintaohje: Nimikekustannusten muokkaaminen](inventory-how-adjust-item-costs.md)|

## <a name="see-also"></a>Katso myös  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)    
[Toimitusketju](madeira-supply-chain.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
