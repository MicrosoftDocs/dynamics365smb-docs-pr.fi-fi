---
title: Business Centralin talousraportit
description: Katso, mitkä talousraportit ovat saatavilla Business Centralin vakioversiossa, jotta voit seurata liiketoimintaasi.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 01/28/2021
ms.author: edupont
ms.openlocfilehash: b2eb04ed2589bd0af972ca49587f84c416204a28
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392147"
---
# <a name="financial-reports-in-business-central"></a>Business Centralin talousraportit

[!INCLUDE [prod_short](includes/prod_short.md)]in talousraportoinnin avulla talouden ja liiketoiminnan ammattilaiset voivat luoda, ylläpitää, ottaa käyttöön ja tarkastella taloudellisia raportteja. Se ylittää perinteisen raportoinnin rajoitukset, jotta voit suunnitella tehokkaasti erityyppisiä raportteja. [!INCLUDE [prod_short](includes/prod_short.md)] sisältää useita raportteja, jäljitystoimintoja ja työkaluja, joiden avulla tilintarkastajat tai valvojat ovat vastuussa talousosaston raportoinnista. Taloudelliseen raportointiin sisältyy dimensioiden tuki, joten tilisegmentit tai -dimensiot ovat heti saatavilla. Muita työkaluja tai määritysvaiheita ei edellytetä.  

## <a name="reports"></a>Raportit

Seuraavassa taulukossa kuvataan joitakin talousraportoinnin keskeisiä raportteja.

|Raportti |Kuvaus  |
|---------|---------|
|**Muuta kustannuksia – Nimiketapahtumat** | Muuttaa arvotapahtumien varastoarvoja niin, että pääkirjanpitoa päivitettäessä käytetään oikeaa muutettua kustannusta ja tuottotilastot ovat ajan tasalla. Kustannusten muuttaminen siirtää kustannusmuutokset saapuvista tapahtumista, esimerkiksi osto- tai tuotantotapahtumista, niihin liittyviin lähteviin tapahtumiin, esimerkiksi myynteihin tai siirtoihin.  |
|**Alustava tulos/tase**| Raportissa näkyy tilikartta saldoineen ja nettomuutoksineen. Voit haluta esimerkiksi tarkastella tiettyjen dimensioiden alustavia saldoja. Raporttia voi käyttää kirjanpitojakson tai tilikauden päättyessä. |
|**Alustava tulos jakson mukaan**  | Tässä raportissa on KP-tilikohtainen alkusaldo, valitun jakson (kuukauden, vuosineljänneksen tai vuoden) tapahtumat ja tuloksena oleva loppusaldo.         |
|**Alustava tulos/tase / Budjetti** | Raportissa näkyy alustava saldo verrattuna budjettiin. Voit haluta esimerkiksi tarkastella tiettyjen dimensioiden alustavia saldoja. Raporttia voi käyttää kirjanpitojakson tai tilikauden päättyessä.        |
|**Eritelty alustava saldo** |Raportissa näkyy eritelty alustava saldo valituilta KP-tileiltä. Raporttia voi käyttää kirjanpitojakson tai tilikauden päättyessä. Asettamalla suodattimia voit määrittää, mitkä tilit sisällytetään eräajoon.         |
|**Alust. saldo / Ed. vuosi**|Tässä raportissa näkyy alustava saldo verrattuna edellisen vuoden lukuihin. Voit haluta esimerkiksi tarkastella tiettyjen dimensioiden alustavia saldoja. Raporttia voi käyttää kirjanpitojakson tai tilikauden päättyessä. Huomaa, että *edellinen vuosi* tarkoittaa samaa jaksoa yhtä kalenterivuotta aikaisemmin.|
|**KP-raporttimalli**|KP-raporttimalleilla voidaan näyttää pääkirjanpidon tilit eri tavalla kuin tilikartassa. KP-raporttimalleja voidaan käyttää esimerkiksi tunnuslukuraportteja varten.|
<!--|**Tase** (KP-raporttimalli tai Excel) tai **Alustava saldo** |         |
|**Kassavirtalaskelma** (KP-raporttimalli) |         |
|**Alustavan taseen yhteenveto/erittely** |         |
|**Tuloslaskelma** (KP-raporttimalli tai Excel)||
|**Budjetti** ||-->

## <a name="tasks"></a>Tehtävät

Seuraavissa artikkeleissa kuvataan joitakin yrityksen tilan analysointiin liittyviä keskeisiä tehtäviä:

* [Todellisten summien analysointi budjetoituihin summiin nähden](bi-how-analyze-actual-versus-budget.md)  
* [Talousraportoinnin valmisteleminen KP-raporttimallien ja tililuokkien avulla](bi-how-work-account-schedule.md)  
* [KP-raporttimalleihin perustuvan KPI-verkkopalvelun määrittäminen ja julkaiseminen](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md)  
* [Tietojen analysointi dimensioiden mukaan](bi-how-analyze-data-dimension.md)  
* [Analyysiraporttien luominen](bi-how-create-analysis-views-reports.md)  
* [Luo raportteja XBRL-linkityksellä.](bi-create-reports-with-xbrl.md)  
* [Tietokannan käyttötarkoituksen hallinta](admin-data-access-intent.md)  

## <a name="see-also"></a>Katso myös

[Kustannusbudjettien luominen](finance-create-cost-budgets.md)  
[ALV:n raportointi veroviranomaisille](finance-how-report-vat.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[Sulkemista edeltävien raporttien käyttäminen](year-prepare-preclose-reports.md)  
[Tilinpäätöslaskelmien valmisteleminen](year-prepare-close-statement.md)  
[Rahoituslaskelmien analysointi Microsoft Excel:issä](finance-analyze-excel.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Rahoitus](finance.md)  
[Paikallisten toiminnallisuuksien yleiskatsaus](about-localization.md)  
[Kirjanpitäjän käyttökokemukset [!INCLUDE[prod_long](includes/prod_long.md)]issa](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]