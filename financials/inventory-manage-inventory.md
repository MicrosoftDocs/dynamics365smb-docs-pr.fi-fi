---
title: Varasto| Microsoft-Docs
description: "Artikkelissa kerrotaan, miten fyysisiä nimikkeitä hallitaan."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b53cae82cfa532fb0620cc9e1f305216c2321785
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017

---

# <a name="inventory"></a>Vaihto-omaisuus
Jokaiselle fyysiselle tuotteelle, jolla käydään kauppaa, on luotava **Varasto**-tyyppinen nimikekortti. Asiakkaille tarjottavat nimikkeet, joita ei säilytetä varastossa, voidaan rekisteröidä ei-varastoitaviksi nimikkeiksi. Ne voidaan muuntaa varastonimikkeiksi tarvittaessa. Voit suurentaa tai pienentää varastossa olevien nimikkeiden määrää kirjaamalla arvon suoraan nimiketapahtumiin esimerkiksi fyysisen määrän jälkeen tai jättämällä ostoja kirjaamatta.

Varaston arvon nousut ja laskut kirjataan luonnollisesti myös silloin, kun osto- ja myyntiasiakirjat kirjataan. Lisätietoja on kohdassa [Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md), [Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md) ja [Toimintaohje: Myynnin laskuttaminen](sales-how-invoice-sales.md). Sijaintien väliset siirrot muuttavat varastomääriä yrityksen fyysisten varastojen kesken.   

Voit suurentaa nimikkeiden yhteenvetoa ja auttaa niiden etsimisessä luokittelemalla nimikkeet ja antamalla niille määritteitä, joiden perusteella voidaan tehdä hakuja ja lajitteluja.

Varmista, että nimikkeiden kustannukset välitetään liittyvään lähtevään myyntitapahtuman. Tämä on tärkeää etenkin tilanteissa, joissa myyt tavaroita ennen kyseisten nimikkeiden oston laskutusta. Tätä kutsutaan kustannusten muuttamiseksi, ja sen voi tehdä manuaalisesti tai automaattisesti nimiketapahtuman kirjauksen yhteydessä.

Kaupasta johtuvat varastoarvon muutokset täsmäytetään automaattisesti talouskirjojen kanssa nimiketapahtumia kirjattaessa.

|Toiminta |Katso |
|---|----|
|Luo niille varastonimikkeille nimikekortit, joilla käyt kauppaa.|[Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)|
|Jäsennä päänimikkeet, joita myydään päänimikkeen osista koostuvina paketteina tai jotka kootaan tilausta tai varastointia varten.|[Toimintaohje: Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)|
|Ylläpidä nimikkeiden yhteenvetoa ja helpottaa nimikkeiden etsimistä ja lajittelua järjestämällä nimikkeet luokkiin.|[Toimintaohje: Nimikkeiden luokitteleminen](inventory-how-categorize-items.md)|
|Nimikkeiden lajitteleminen ja löytäminen on helpompaa, kun määrität nimikkeisiin eri arvotyyppien määritteet.|[Toimintaohje: Nimikkeen määritteiden käsitteleminen](inventory-how-work-item-attributes.md)|
|Luo niille nimikkeille erityisnimikekortit, joita tarjoat asiakkaille, mutta joita ei säilytetä varastossa.|[Toimintaohje: Ei-varastoitavien nimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md)|
|Kasvattaa tai vähentää nimikkeen varastomäärää esimerkiksi fyysisen laskennan jälkeen tai yksinkertainen tapa tallentaa tavaran vastaanottoja.|[Toimintaohje: varaston muuttaminen](inventory-how-adjust-inventory.md)|
|Näytä nimikkeiden saatavuus sijainnin, jakson tai myynti- tai ostotapahtuman mukaan tai sen mukaan, miten niitä käytetään kokoonpanon tuoterakenteessa.|[Toimintaohje: Saatavuuden yleiskuva](inventory-how-availability-overview.md)|
|Voit siirtää varastonimikkeitä sijaintien välillä siirtotilausten, varastotapahtumien hallinnan tai nimikkeen uudelleenluokituspäiväkirjan avulla.|[Toimintaohje: Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)|
|Nosta tai laske vähintään yhden varaston nimikkeen arvoa kirjaamalla nimikkeen nykyinen laskettu arvo.|[Toimintaohje: Varaston uudelleenarvostus](inventory-how-revalue-inventory.md)|
|Muuta nimikekustannuksia automaattisesti tai manuaalisesti, kun haluat siirtää saapuvien tapahtumien kustannusmuutokset liittyviin lähteviin tapahtumiin.|[Toimintaohje: Nimikekustannusten muokkaaminen](inventory-how-adjust-item-costs.md)|
|Lisätietoja tavoista, joilla kaupasta johtuvat varastoarvon muutokset täsmäytetään automaattisesti talouskirjojen kanssa.|[Lisäasetukset: Varaston täsmäytys](advanced-inventory-reconciliation.md)|

## <a name="see-also"></a>Katso myös  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)    
[Toimitusketju](madeira-supply-chain.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
