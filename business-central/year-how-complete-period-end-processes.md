---
title: Valinnaiset toimenpiteet tilikauden päättämiskausia varten
description: Tässä artikkelissa hahmotellaan Business Centralin kirjanpitojaksojen päättämisen valinnaiset prosessit ja aktiviteetit.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments'
ms.date: 08/02/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="overview-of-tasks-to-close-accounting-periods"></a>Kirjanpitojaksojen päättämiseen tehtävien yleiskuvaus

[!INCLUDE[prod_short](includes/prod_short.md)] Jaksoja ei pakoteta sulkemaan, mutta kauden lopussa (kuukauden lopussa) on monia toimenpiteitä, joita voi tehdä. Tässä artikkelissa on yleiskuvaus valinnaisista prosesseista ja aktiviteeteista tilinpäätösjaksoja varten.  

## <a name="general-ledger"></a>Pääkirjanpito

* Määritä järjestelmänlaajuiset ja käyttäjäkohtaiset kirjausjaksot.  

    Tässä määritetään kirjausten sallittu päivämääräväli. Liiketoimintasi mukaan haluat ehkä sallia kirjauksen jakson alussa tai loppupuolella. Lisätietoja on kohdassa [Kirjausjaksojen määrittäminen](finance-how-specify-posting-periods.md).  
* Tee kaikki tarpeelliset pääkirjanpidon (KP) muutokset.  
* Päivitä ja kirjaa toistuvat päiväkirjat.  
  <!--* Process Consolidations-->
* Suorita talousraportit seuraavasti:  
  * Avaa **Talousraportit**-sivu ja valitse **Tulosta**-toiminto.  

## <a name="sales-and-receivables"></a>Myynnit ja myyntisaamiset

* Kirjaa kaikki myyntitilaukset, laskut, hyvityslaskut ja palautustilaukset.  
* Kirjaa kaikki kassapäiväkirjat.  
* Päivitä ja kirjaa myynteihin ja myyntisaamisiin liittyvät toistuvat kirjaukset.  
* Täsmäytä myyntisaatavat pääkirjanpitoon.  
* Suorita **Poista laskutetut myyntitilaukset** -eräajo.  

## <a name="purchases-and-payables"></a>Ostot ja ostovelat

* Kirjaa kaikki ostotilaukset, laskut, hyvityslaskut ja palautustilaukset.  
* Kirjaa kaikki maksupäiväkirjat.  
* Päivitä ja kirjaa ostoihin ja ostovelkoihin liittyvät toistuvat kirjaukset.  
* Suorita **Ostovelkojen tilanne** -raportti ja täsmäytä ostovelat pääkirjanpitoon.  
* Suorita **Poista laskutetut ostotilaukset** -eräajo.  

## <a name="fixed-assets"></a>Käyttöomaisuus

* Kirjaa kaikki kunnossapitokustannukset, jotka on kirjattu käyttöomaisuuspäiväkirjojen tai laskujen kautta.
* Kirjaa muutokset.
* Kirjaa arvonkorotus.
* Kirjaa arvonalennus.
* Päivitä ja kirjaa toistuva käyttöomaisuuspäiväkirja.

## <a name="intercompany"></a>Konserni

* Käsittele konsernin tapahtumat.

## <a name="calculate-and-process-sales-tax"></a>Arvonlisäveron laskeminen ja käsitteleminen

* Täytä ALV-ilmoitukset.  

## <a name="see-also"></a>Katso myös

[Vuosien ja kausien sulkeminen](year-close-years-periods.md)  
[Kirjojen sulkeminen](year-close-books.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
