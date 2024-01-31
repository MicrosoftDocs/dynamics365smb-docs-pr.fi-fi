---
title: Jaksojen sulkemisen valinnaiset toiminnot
description: Tässä ohjeaiheessa kerrotaan Business Central -sovelluksen kirjanpitojaksojen sulkemisen valinnaisista prosesseista ja toiminnoista.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments'
ms.date: 08/29/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Kirjanpitojaksojen sulkemistehtävien yleiskatsaus

[!INCLUDE[prod_short](includes/prod_short.md)] ei pakota päättämään kausia, joskin on monia kauden lopussa (kuukauden lopussa) aktiviteetteja, jotka voit tehdä. Tässä ohjeaiheessa on yleiskatsaus kausien päättämiseen liittyvistä valinnaisista prosesseista ja aktiviteeteista.  

## Pääkirjanpito

* Määritä järjestelmänlaajuiset ja käyttäjäkohtaiset kirjausjaksot.  

    Tässä määritetään kirjausten sallittu päivämääräväli. Liiketoiminnan tarpeiden mukaan voit sallia kirjauksen jakson alussa tai jakson loppupuolella. Lisätietoja on kohdassa [Kirjausjaksojen määrittäminen](finance-how-specify-posting-periods.md).  
* Tee kaikki tarpeelliset pääkirjanpidon (KP) muutokset.  
* Päivitä ja kirjaa toistuvat päiväkirjat.  
  <!--* Process Consolidations-->
* Suorita talousraportit seuraavasti:  
  * Avaa **Talousraportit**-sivu ja valitse **Tulosta**-toiminto.  

## Myynnit ja myyntisaamiset

* Kirjaa kaikki myyntitilaukset, laskut, hyvityslaskut ja palautustilaukset.  
* Kirjaa kaikki kassapäiväkirjat.  
* Päivitä ja kirjaa myynteihin ja myyntisaamisiin liittyvät toistuvat kirjaukset.  
* Täsmäytä myyntisaatavat pääkirjanpitoon.  
* Suorita **Poista laskutetut myyntitilaukset** -eräajo.  

## Ostot ja ostovelat

* Kirjaa kaikki ostotilaukset, laskut, hyvityslaskut ja palautustilaukset.  
* Kirjaa kaikki maksupäiväkirjat.  
* Päivitä ja kirjaa ostoihin ja ostovelkoihin liittyvät toistuvat kirjaukset.  
* Suorita **Ostovelkojen tilanne** -raportti ja täsmäytä ostovelat pääkirjanpitoon.  
* Suorita **Poista laskutetut ostotilaukset** -eräajo.  

## Käyttöomaisuus

* Kirjaa kaikki kunnossapitokustannukset, jotka on kirjattu käyttöomaisuuspäiväkirjojen tai laskujen kautta.
* Kirjaa muutokset.
* Kirjaa arvonkorotus.
* Kirjaa arvonalennus.
* Päivitä ja kirjaa toistuva käyttöomaisuuspäiväkirja.

## Konserni

* Käsittele konsernin tapahtumat.

## Arvonlisäveron laskeminen ja käsitteleminen

* Täytä ALV-ilmoitukset.  

## Katso myös

[Vuosien ja kausien sulkeminen](year-close-years-periods.md)  
[Kirjojen sulkeminen](year-close-books.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
