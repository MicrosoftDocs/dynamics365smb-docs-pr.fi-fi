---
title: Käyttöomaisuuden analyysi
description: 'Käyttöomaisuuserien tietojen kerääminen, analysointi ja jakaminen liiketoimintatietojen osalta.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5601, 5600, 5615, 5616, 5617'
ms.date: 04/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Käyttöomaisuuden analyysi

Yritykset, joilla on käyttöomaisuutta, keräävät niistä paljon tietoa päivittäisen toiminnan aikana. Nämä tiedot tukevat käyttöomaisuuspäälliköiden arvokasta liiketoimintatietoa (BI):

- Käyttöomaisuuden hankinta
- Käyttöomaisuuden poistot
- Vakuutus ja korjaukset
- Käyttöomaisuuden budjetit

[!INCLUDE[prod_short](includes/prod_short.md)]i tarjoaa toimintoja, joiden avulla voidaan kerätä, analysoida ja jakaa tietoja organisaation käyttöomaisuudesta:

- Financial reporting (tilinpäätöksille ja käyttöomaisuustilien KPI:lle)
- Tapauskohtainen luetteloissa tapahtuma analyysi
- Excelin tietojen tapauskohtainen analyysi (Avaa Excelissä -toiminnon avulla)
- Valmiit käyttöomaisuuden analytiikkatyökalut
- Valmiit käyttöomaisuusraportit

> [!NOTE]
> Käyttöomaisuuden analytiikka eroaa hieman muista alueista. Sinun on analysoitava jo olemassa olevia tietoja, kuten resurssien hankinnat, poistot ja vakuutukset, mutta myös tulevaisuuden tiedot, kuten poistot ja resurssien käytöstä poistaminen. Jälkimmäistä analyysityyppiä varten [!INCLUDE[prod_short](includes/prod_short.md)] sisältää sisäänrakennettuja raportteja, jotka voivat laskea nämä numerot.

Kullakin ominaisuudella on etunsa ja haittapuolensa tietojen analyysityypin ja käyttäjän roolin mukaan. Lisätietoja on kohdassa [Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md).

Tässä artikkelissa kuvataan tapoja käyttää näitä lisätoimintoja, kun halutaan saada tietoja käyttöomaisuudesta.

## Analytiikan tarpeet omaisuudenhallinnassa

Kun ajatellaan resurssien hallinnan analytiikan tarpeita, voisi olla hyödyllistä käyttää henkilökohtaista mallia, joka kuvaa heidän analytiikkatarpeitaan korkealla tasolla.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Kuvassa analytiikan eri henkilötyypit" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Mitä tietoihin tulee, eri tehtävissä toimivilla henkilöillä voi olla erilaisia tarpeita, minkä lisäksi he käyttävät tietoja eri tavoin. Esimerkiksi resurssinhallinnassa ja taloushallinnossa työskentelevät käyttävät tietoja eri tavalla kuin myynnissä työskentelevät.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Kuvassa erilaisten henkilöhahmojen erilaiset analytiikkatarpeet" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rooli              | Tietojen koostaminen  | Tyypilliset tietojen käyttötavat                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|Talousjohtaja/operatiivinen johtaja/toimitusjohtaja                 | Suoritustiedot  | Tunnusluvut <br> Koontinäytöt <br> Talousraportit           |
|Käyttöomaisuuden hallinta/talouspäällikkö   | Trendit, yhteenvedot | Valmiit johdon raportit <br> Tapahtumakohtainen analyysi      | 
|Kirjanpitäjä                      | Eritellyt tiedot     | Valmiit operatiiviset raportit <br> Näytöllä näkyvät tehtävän tiedot |

## Resurssien hallinnan KPI:t

Suorituskykymittari (tunnusluku) on mitattava arvo, joka ilmaisee, kuinka tehokkaasti tavoite toteutuu. Resurssien hallinnassa käytetään usein seuraavia tunnuslukuja seuraamaan organisaation resurssien käyttöä:

- Kokonaisliikevaihto
- Kokonaispääoman tuotto

## Financial Reportingin käyttö käyttöomaisuuteen liittyvien tilinpäätösten ja KPI:iden tuottamiseen

**Financial Reporting** -ominaisuus antaa merkityksellisiä tietoja tilikartassa näkyvistä taloudellisesta tiedoista. Talousraportit voidaan määrittää analysoimaan kirjanpitotilien lukuja ja vertaamaan pääkirjanpidon tapahtumia budjettitapahtumiin. Erityisesti resurssienhallintaa varten voidaan määrittää talousraportteja pääkirjanpidon (KP-) tileille, joita käytetään käyttöomaisuuden kirjausten seurantaan.

Dimensioilla on tärkeä tehtävä liiketoimintatiedoissa. Dimensio on tieto, joka voidaan lisätä tapahtumaan parametriksi. Dimensioiden avulla voidaan ryhmitellä samankaltaisia ominaisuuksia, kuten asiakkaita, tuotteita ja myyjiä, ja noutaa nämä ryhmät helposti analyysia varten. Dimensioita voi käyttää esimerkiksi analyysinäkymien määrityksessä sekä talousraporttien luonnissa. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

Lisätietoja talousraportoinnista on kohdassa [Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md).

## Taloushallinnon raportointi liiketoimintayksiköiden tai yritysten välillä (käyttöomaisuuteen liittyvät)

Jotkin organisaatiot käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa useassa liiketoimintayksikössä tai yrityksessä. Muut käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa tytäryhtiöissä raportoidakseen emo-organisaatioihin. [!INCLUDE [prod_short](includes/prod_short.md)] antaa kirjanpitäjille työkalut, jotka auttavat heitä siirtämään pääkirjanpidon tapahtumia kahdesta tai useammasta yrityksestä (tytäryrityksistä) konsolidoituun yritykseen. Erityisesti resurssienhallintaa varten pääkirjanpidon tapahtumat voidaan haluta konsolidoida käyttöomaisuustilien osalta, jotta käyttöomaisuuden KPI:iä voitaisiin seurata liiketoimintayksiköissä tai oikeushenkilöissä.

Lisätietoja on kohdassa [Yrityksen konsolidointi](finance-consolidated-company-reporting.md).

## Käyttöomaisuuden tapauskohtainen analyysi

Joskus on tarkistettava nopeasti, täsmäävätkö luvut, tai vahvistettava luku. Seuraavat ominaisuudet sopivat erinomaisesti tapauskohtaisiin analyyseihin:

- Tietojen analyysi tapahtumaluettelosivuilla
- Avaa Excelissä

Tietoanalyysiominaisuus mahdollistaa lähes minkä tahansa luettelosivun, kuten **Pääkirjanpidon tapahtumat**- tai **Käyttöomaisuuden kirjanpitotapahtumat** -sivujen, analyysitilaan siirtymisen sekä tietojen ryhmittelyn, suodattamisen ja käyttämisen pivot-tilassa halutulla tavalla.

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Esimerkki tietojen analysoinnista KP-tapahtumien sivulla" lightbox="media/data-analysis-gl-entries.png":::

Vastaavasti **Avaa Excelissä** -toiminnolla voi avata tapahtumien luettelosivun, suodattaa luettelon mahdollisesti tietojen alijoukoksi ja käsitellä sitten tietoja Excelissä. Se voidaan tehdä esimerkiksi käyttämällä tietojen analysoinnin, entä jos -analyysin ja ennustetaulukon kaltaisia ominaisuuksia.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Esimerkki KP-tapahtumien tietojen analysoinnista Excelin avulla" lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Jos järjestelmän ominaisuudet määritetään OneDriveen, Excel-työkirja avautuu selaimeen käyttämällä Exceliä verkossa. 

<!-- Not ready yet
For more information on how to do ad-hoc analysis on ledgers, see [Ad-hoc analysis on finance data](ad-hoc-analysis-finance.md). 
-->

## Käyttöomaisuuden valmiit raportit

[!INCLUDE [prod_short](includes/prod_short.md)] sisältää useita valmiita raportteja, jäljitystoimintoja ja työkaluja, joista on hyötyä käyttöomaisuudesta raportoiville talouspäälliköille.

Saatavana olevien raporttien yleiskuvan saa valitsemalla **Kaikki raportit** aloitussivun yläosassa. Tämä toiminto avaa roolienhallinta-sivun, joka on suodatettu näyttämään **Raportti ja analyysi** -vaihtoehdon ominaisuudet. Voit etsiä käyttöomaisuuteen liittyviä raportteja määrittämällä **Etsi**-kenttään **käyttöomaisuuserät**. Lisätietoja on kohdassa [Raporttien etsiminen roolienhallinnan avulla](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-fixed-assets.png" alt-text="Esimerkki taloushallinnon roolikeskuksen raporteista" lightbox="media/report-explorer-fixed-assets.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Lisätietoja käyttöomaisuuden kannalta olennaisista raporteista on kohdassa [Sisäänrakennettu käyttöomaisuus -raportit](fa-reports.md).

## Näytöllä näkyvät käyttöomaisuuden analyysit

[!INCLUDE [prod_short](includes/prod_short.md)]issa on useita sivuja, joista saadaan käyttöomaisuuden yleiskatsauksia ja tehtäviä töitä. Seuraavassa on joitakin esimerkkejä, joilla voit aloittaa:

- [Laske poisto, kirjaa poisto ja analysoi poisto](fa-how-depreciate-amortize.md)
- [Kunnossapitokustannusten valvonta](fa-how-maintain.md#to-monitor-maintenance-costs)
- [Vakuutuksen kattavuuden tarkkailu](fa-how-insure.md#to-monitor-insurance-coverage)
- [Muuttuneiden poistokirja-arvojen tarkasteleminen](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification)
- [Luovutustapahtumien tarkasteleminen](fa-how-dispose-retire.md#to-view-disposal-ledger-entries)
- [Suunniteltujen luovutusarvojen tarkasteleminen](fa-how-manage-budgets.md#to-view-projected-disposal-values)

### Käyttöomaisuuden pääkirjanpidon tapahtumien ja saldojen näyttäminen Tilikartta-sivulta

Tilikartta-sivulla on näkyvissä kaikki pääkirjanpidon kirjanpitotilit ja kootut luvut. Seuraavat ovat mahdollisia tällä sivulla:  

- Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.  
- Voit tarkastella luetteloa kyseisen tilin kirjausryhmistä.
- Yhden tilin erillisten debet- ja kreditsaldojen näyttäminen.

Erityisesti käyttöomaisuutta varten Tilikartta-sivulla voidaan luoda näkymä, jossa näkyvät vain käyttöomaisuustapahtumien kirjaamiseen käytettävät tilit.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Esimerkki merkityksellisten taloustietojen näkymisestä Tilikartta-sivulla" lightbox="media/chart-of-accounts-page.png":::

Lisätietoja on kohdassa [Tilikartan ymmärtäminen](finance-general-ledger.md#the-chart-of-accounts).

### Tietojen analysointi dimensioittain (käyttöomaisuuteen liittyen)

Dimensiot ovat tapahtumia luokittelevia arvoja, jotta voit seurata ja analysoida tapahtumia asiakirjoissa, kuten KO-päiväkirjoissa. Dimensiot voivat esimerkiksi ilmaista, mistä osastosta tai sijainnista tapahtuma on lähtöisin.  

Sen sijaan että kullekin osastolle ja sijainnille määritettäisiin erilliset kirjanpitotilit, dimensioita voidaan käyttää analyysin perustana ja välttää monimutkaisen tilikarttarakenteen luominen.

Lue lisätietoja kohdasta [Analysoi tietoja dimensioiden mukaan](bi-how-analyze-data-dimension.md)

## Katso myös

[Taloushallinnon raportoinnin käsitteleminen liiketoimintayksiköiden tai yritysten välillä](finance-consolidated-company-reporting.md)  
[Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md)  
[Tilikartan ymmärtäminen](finance-general-ledger.md#the-chart-of-accounts)  
[Valmiit käyttöomaisuusraportit](fa-reports.md)  
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
