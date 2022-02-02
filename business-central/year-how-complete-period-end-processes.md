---
title: Jaksojen sulkemisen valinnaiset toiminnot
description: Tässä ohjeaiheessa kerrotaan Business Central -sovelluksen kirjanpitojaksojen sulkemisen valinnaisista prosesseista ja toiminnoista.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 9442b0617691098b32e5012a5a708e14fe5a0187
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011997"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Kirjanpitojaksojen sulkemistehtävien yleiskatsaus

[!INCLUDE[prod_short](includes/prod_short.md)] ei pakota päättämään kausia, joskin on monia kauden lopussa (kuukauden lopussa) aktiviteetteja, jotka voit tehdä. Tässä ohjeaiheessa on yleiskatsaus kausien päättämiseen liittyvistä valinnaisista prosesseista ja aktiviteeteista.  

## <a name="general-ledger"></a>Pääkirjanpito

* Määritä järjestelmänlaajuiset ja käyttäjäkohtaiset kirjausjaksot.  

    Tässä määritetään kirjausten sallittu päivämääräväli. Liiketoiminnan tarpeiden mukaan voit sallia kirjauksen jakson alussa tai jakson loppupuolella. Lisätietoja on kohdassa [Kirjausjaksojen määrittäminen](finance-how-specify-posting-periods.md).  
* Tee kaikki tarpeelliset KP-muutokset.  
* Päivitä ja kirjaa toistuvat päiväkirjat.  
  <!--* Process Consolidations-->
* Suorita KP-raporttimallit seuraavasti:  
  * Avaa **KP-raporttimalli**-sivu ja valitse sitten **Tulosta**-toiminto.  

## <a name="sales-and-receivables"></a>Myynnit ja myyntisaamiset

* Kirjaa kaikki myyntitilaukset, laskut, hyvityslaskut ja palautustilaukset.  
* Kirjaa kaikki kassapäiväkirjat.  
* Päivitä ja kirjaa myyntiin ja myyntisaamisiin liittyvät toistuvat päiväkirjat.  
* Täsmäytä myyntisaatavat pääkirjanpitoon.  
* Suorita **Poista laskutetut myyntitilaukset** -eräajo.  

## <a name="purchases-and-payables"></a>Ostot ja ostovelat

* Kirjaa kaikki ostotilaukset, laskut, hyvityslaskut ja palautustilaukset.  
* Kirjaa kaikki maksupäiväkirjat.  
* Päivitä ja kirjaa ostoihin ja ostovelkoihin liittyvät toistuvat päiväkirjat.  
* Suorita **Ostovelkojen tilanne** -raportti ja täsmäytä ostovelat pääkirjanpitoon.  
* Suorita **Poista laskutetut ostotilaukset** -eräajo.  

## <a name="fixed-assets"></a>Käyttöomaisuus

* Kirjaa kaikki kunnossapitokustannukset, jotka on kirjattu käyttöomaisuuspäiväkirjojen tai laskujen kautta.
* Kirjaa muutokset.
* Kirjaa arvonkorotus.
* Kirjaa arvonalennus.
* Päivitä ja kirjaa toistuva käyttöomaisuuspäiväkirja.

## <a name="intercompany"></a>Konserni

* Konsernin tapahtumien käsitteleminen

## <a name="calculate-and-process-sales-tax"></a>Arvonlisäveron laskeminen ja käsitteleminen

* Täytä ALV-ilmoitukset.  

## <a name="see-also"></a>Katso myös

[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[Kirjojen sulkeminen](year-close-books.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]