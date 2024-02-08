---
title: Taloudelliset liiketoimintatiedot
description: 'Business Central sisältää useita ominaisuuksia, joiden avulla voit kerätä, analysoida ja jakaa arvokkaita yritystietoja liiketoimintatietoa ja päätöksentekoa varten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '103, 108, 198, 490'
ms.date: 09/22/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Taloudelliset liiketoimintatiedot

Yritykset hankkivat päivittäisen toiminnan aikana valtavia määriä tietoja. Nämä tiedot voivat kuvata esimerkiksi organisaation myyntilukuja, ostoja, toimintakuluja, työntekijöiden palkkoja ja budjetteja, ja ne voivat antaa päätöksentekijöille arvokasta liiketoimintatietoa (BI). [!INCLUDE[prod_short](includes/prod_short.md)] sisältää erinäisiä toimintoja, joiden avulla voit kerätä, analysoida ja jakaa yrityksen tietoja.

**Dimensio**-toiminnallisuudella on tärkeä osa liiketoimintatietojen kannalta. Dimensio on tieto, jonka voi lisätä tapahtumaan parametriksi. Sen avulla voit ryhmitellä samankaltaisia ominaisuuksia, kuten asiakkaita, alueita, tuotteita ja myyjiä, ja hakea näitä ryhmiä helposti analyysia varten. Dimensioita voi käyttää esimerkiksi analyysinäkymien määrityksessä sekä taloudellisten raporttien luonnissa. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

> [!TIP]
> Tapahtumatietoja voi analysoida nopeasti suodattamalla tilikarttojen loppusummat ja kaikkien **Tapahtumat**-sivujen tapahtumat dimensioittain. Hae **Määritä dimension suodatus** -toiminto.  

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.  

| Vastaanottaja | Katso |
| --- | --- |
|Tarkastele todellisia summia verrattuna kaikkien tilien budjetoituihin summiin useilta kausilta.|[Todellisten summien analysointi budjetoituihin summiin nähden](bi-how-analyze-actual-versus-budget.md)|
|Luo uusia taloudellisia raportteja määrittääksesi tilinpäätöksiä raportointia tai taulukoina näyttämistä varten.|[Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md)|
|Analysoi taloudellinen suorituskyky määrittämällä suorituskykyilmaisimet (KPI:t) perustuen taloudellisiin raportteihin, jotka sitten julkaiset verkkopalveluina. Julkaistujen taloudellisten raporttien KPI-tietoja voi tarkastella sivustossa tai ne voi tuoda Microsoft Exceliin OData-verkkopalvelujen avulla.|[Taloudellisiin raportteihin perustuvan KPI-verkkopalvelun määrittäminen ja julkaiseminen](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md)|
|Näkymän määrittäminen tietojen analysointia varten dimensioiden avulla.|[Tietojen analysointi dimensioiden mukaan](bi-how-analyze-data-dimension.md)|
|Uusien analyysiraporttien luominen myyntejä, ostoja ja varastoa varten sekä analyysimallien määrittäminen.|[Analyysiraporttien luominen](bi-how-create-analysis-views-reports.md)|
|Ota käyttöön kansainvälisten kirjanpitojärjestöjen maailmanlaajuinen taloushallinnon raportointi eXtensible Business Reporting Language (XBRL) -kielen avulla.|[Luo raportteja XBRL-linkityksellä.](bi-create-reports-with-xbrl.md)|
|Tietokannan käyttötarkoituksen muuttaminen raporteissa, API-tyyppisillä sivuilla ja kyselyissä, jotta latauskuorma vähenee ja suorituskyky paranee.|[Tietokannan käyttötarkoituksen hallinta](admin-data-access-intent.md)|

## Katso myös

[Rahoitus](finance.md)  
[Business Centralin käyttäminen Power BI -tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[Kirjanpitokausien sulkeminen](year-close-years-periods.md)  
[Tietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Business Intelligencen ja raportoinnin yleiskuva](reports-bi-reporting.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
