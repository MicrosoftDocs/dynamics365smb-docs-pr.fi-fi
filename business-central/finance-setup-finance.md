---
title: Talousprosessien määrittäminen| Microsoft Docs
description: Lisätietoja tehtävistä, joilla määritetään liiketoiminnan taloushallinto laskentatoimen, tilintarkastuksen tai kirjanpidon tarpeita varten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c64b58c036395764191c05f47f8327c6479a4c6f
ms.sourcegitcommit: dac212009aadf3227e54c99976c438f6e56f182a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/02/2019
ms.locfileid: "1447035"
---
# <a name="setting-up-finance"></a>Rahoituksen määrittäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää useimpien rahoitusprosessien vakiomääritykset, mikä nopeuttaa käytön aloittamista. Voit tarvittaessa muuttaa määrityksiä liiketoiminnan tarpeiden mukaisesti. Voit määrittää esimerkiksi roolikeskuksessa avustetun asennusoppaan avulla sijaintiin sopivan arvonlisäveron.  

Tietyt asiat on kuitenkin määritettävä itse. Esimerkki: haluat käyttää dimensioita BI-tietojen perustana.  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.

| Toiminta | Katso |
| --- | --- |
| Valitse, miten maksat toimittajille. |[Maksutapojen määrittäminen](finance-payment-methods.md) |
| Määritä kirjausryhmät, jotka yhdistävät objektit, kuten asiakkaat, toimittajat, nimikkeet, resurssit sekä myynti- ja ostoasiakirjat, pääkirjanpidon tileille. |[Kirjausryhmien määrittäminen](finance-posting-groups.md)|
|Luo KP-raporttimallit ja määritä tililuokat, jos haluat määrittää talouskaavioiden ja -raporttien, kuten tase- ja tuloslaskelmaraporttien, sisällön.|[Talousraportoinnin valmisteleminen KP-raporttimallien ja tililuokkien avulla](bi-how-work-account-schedule.md)|
|Määritä toleranssi, jonka mukaan järjestelmä sulkee laskun, vaikka maksu ja mahdolliset alennukset eivät täysin vastaa laskun koko summaa.|[Maksutoleranssien ja maksualennustoleranssien käsitteleminen](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Määritä tilikaudet. |[Uuden tilikauden avaaminen](finance-how-open-new-fiscal-year.md) |
| Määritä, miten myynnistä kerätyt arvonlisäverosummat raportoidaan veroviranomaisille. |[Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md)|
|Valmistele ei-realisoituneen ALV:n käsittely kassaperusteisen kirjanpidon yhteydessä.|[Ei-realisoituneen arvonlisäveron määrittäminen kassaperusteista kirjanpitoa varten](finance-setup-unrealized-vat.md)|
| Määritä myynti- ja ostotoiminnot käsittelemään maksut ulkomaan valuuttana.|[Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa](finance-how-enable-application-ledger-entries-different-currencies.md)
|Määritä ainakin yksi lisävaluutta, jotta summat raportoidaan automaattisesti sekä PVA:na että lisäraportointivaluuttana kussakin KP-tapahtumassa ja muissa tapahtumissa.|[Lisäraportointivaluutan määrittäminen](finance-how-setup-additional-currencies.md)|
|Säädä lisävaluutta-arvoja säännöllisesti vaihtokurssien vaihtelun vuoksi.|[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)|
|Määritä useita korkoprosentteja käytettäväksi kauppatapahtumien viivästyneissä maksuissa eri jaksoilla.|[Useiden korkoprosenttien määrittäminen](finance-how-to-set-up-multiple-interest-rates.md)|
|Valmistele laskujen summien automaattinen pyöristys laskujen luonnin yhteydessä.|[Laskun pyöristyksen määrittäminen](finance-set-up-invoice-rounding.md)|
| Lisää aiemmin luotuun tilikarttaan uusia tilejä. |[Tilikartan määrittäminen](finance-setup-chart-accounts.md) |
| Määritä BI-kaaviot analysoimaan kassavirtaa. |[Kassavirta-analyysin määrittäminen](finance-setup-cash-flow-analyses.md) |
|Ota käyttöön sellaisen asiakkaan laskutus, jota ei ole määritetty järjestelmässä.|[Käteisasiakkaiden määrittäminen](finance-how-to-set-up-cash-customers.md)|
| Intrastat-raportoinnin määrittäminen ja raportin lähettäminen viranomaisille | [Intrastat-ilmoituksen määrittäminen ja raportoiminen](finance-how-setup-report-intrastat.md)|
|Varmista, että tapahtuma kohdistetaan yleisessä päiväkirjassa useisiin eri tileihin päiväkirjan kirjauksen yhteydessä. Kohdistuksen voi tehdä määrän, prosentin tai summan mukaan.|[Kohdistustunnusten käyttäminen yleisissä päiväkirjoissa](ui-how-use-allocation-keys-general-journals.md)|

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Pankkitilien hallinta](bank-manage-bank-accounts.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
