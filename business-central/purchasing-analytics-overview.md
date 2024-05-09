---
title: Ostamisen analyysi
description: 'Business Central sisältää monia ominaisuuksia, joiden avulla voit kerätä, analysoida ja jakaa arvokasta myyntitietoa osto-organisaation liiketoimintatietoja ja päätöksentekoa varten.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ostamisen analyysi

Yritykset sieppaavat paljon tietoa päivittäisten toimintojen aikana, ja ne tukevat ostopäälliköille arvokkaita liiketoimintatietoja:

- Ostotarjoukset
- Ostotilaukset
- Ostolaskut

[!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa monia toimintoja, joiden avulla voidaan kerätä, analysoida ja jakaa yrityksen ostotietoja:

- Tapauskohtainen luetteloissa tapahtuma analyysi
- Excelin tietojen tapauskohtainen analyysi (Avaa Excelissä -toiminnon avulla)
- Valmiit myyntiraportit

Kullakin näistä ominaisuuksista on etunsa ja haittapuolensa tietojen analyysityypin ja käyttäjän roolin mukaan. Lisätietoja on kohdassa [Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md).

Tässä artikkelissa esitellään, kuinka voit käyttää näitä analyyttisiä ominaisuuksia saadaksesi tietoa ostoksista.

## Ostojen analyysitarpeet

Myynnin analyysitarpeita pohdittaessa kannattaa käyttää persoonapohjaista mallia, joka kuvaa korkealla tasolla erilaisia analytiikkatarpeita.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Kuvassa analytiikan eri henkilötyypit" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Eri tehtävissä toimivilla henkilöillä voi olla erilaisia tietoja koskevia tarpeita, minkä lisäksi he käyttävät tietoja eri tavoin. Esimerkiksi resurssinhallinnassa ja taloushallinnossa työskentelevät käyttävät tietoja eri tavalla kuin myynnissä työskentelevät.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Kuvassa erilaisten henkilöhahmojen erilaiset analytiikkatarpeet" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rooli              | Tietojen koostaminen  | Tyypilliset tietojen käyttötavat                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO / CSO / CFO / CEO    | Suoritustiedot  | Tunnusluvut <br> Koontinäytöt <br> Talousraportit           |
|ostopäällikkö.      | Trendit, yhteenvedot | Valmiit johdon raportit <br> Tapahtumakohtainen analyysi      | 
|Hankintavastaava/ostaja | Eritellyt tiedot     | Valmiit operatiiviset raportit <br> Näytöllä näkyvät tehtävän tiedot |

<!-- 
## Purchasing KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In purchasing management, people often use the following KPIs to monitor their organization's purchasing performance:

- TODO  
-->

## Financial Reportingin käyttö tilinpäätösten ja KPI:iden tuottamiseen (ostoihin liittyvä)

**Financial Reporting** -ominaisuus antaa merkityksellisiä tietoja tilikartassa näkyvistä taloudellisesta tiedoista. Talousraportit voidaan määrittää analysoimaan kirjanpitotilien lukuja ja vertaamaan pääkirjanpidon tapahtumia budjettitapahtumiin. Erityisesti ostoja varten voidaan määrittää talousraportteja pääkirjanpidon (KP-) tileille, joita käytetään ostokirjausten seurantaan.

Dimensioilla on tärkeä tehtävä liiketoimintatiedoissa. Dimensio on tieto, joka voidaan lisätä tapahtumaan parametriksi. Dimensioiden avulla voidaan ryhmitellä samankaltaisia ominaisuuksia, kuten asiakkaita, alueita ja tuotteita ja noutaa nämä ryhmät helposti analyysia varten. Dimensioita voi käyttää esimerkiksi analyysinäkymien määrityksessä sekä talousraporttien luonnissa. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

Lisätietoja talousraporteista on kohdassa [Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md).

## Taloushallinnon raportointi liiketoimintayksiköiden tai yritysten välillä (ostoihin liittyvät)

Jotkin organisaatiot käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa useassa liiketoimintayksikössä tai yrityksessä. Muut käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa tytäryhtiöissä, jotka raportoivat pääorganisaatioille. [!INCLUDE [prod_short](includes/prod_short.md)] antaa kirjanpitäjille työkalut, jotka auttavat heitä siirtämään pääkirjanpidon tapahtumia kahdesta tai useammasta yrityksestä (tytäryrityksistä) konsolidoituun yritykseen. Erityisesti ostojenhallintaa varten pääkirjanpidon tapahtumat voidaan haluta konsolidoida ostotilien osalta, jotta ostojen KPI:iä voitaisiin seurata liiketoimintayksiköissä tai oikeushenkilöissä.

Lisätietoja on kohdassa [Yrityksen konsolidointi](finance-consolidated-company-reporting.md).

## Ostotietojen ad-hoc-analyysi

Joskus on tarkistettava nopeasti, täsmäävätkö luvut, tai vahvistettava luku. Seuraavat ominaisuudet sopivat erinomaisesti tapauskohtaisiin analyyseihin:

- Tietojen analyysi tapahtumaluettelosivuilla
- Avaa Excelissä

**Tietoanalyysi**-ominaisuuden avulla voit avata melkein minkä tahansa luettelosivun, kuten **Ostotilaukset**, **Kirjatut ostolaskut**, **Toimittajan kirjanpidon merkinnät** tai **Pääkirjanpidon merkinnät**, siirry analyysitilaan ja ryhmittele, suodata ja pivot-tiedot parhaaksi katsomallasi tavalla.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Esimerkki tietojen analysoinnista asiakastapahtumien sivulla" lightbox="media/data-analysis-vendor-ledger-entries.png":::

Vastaavasti **Avaa Excelissä** -toiminnolla voi avata luettelosivun, suodattaa luettelon mahdollisesti tietojen alijoukoksi ja käsitellä sitten tietoja Excelissä. Se voidaan tehdä esimerkiksi käyttämällä tietojen analysoinnin, entä jos -analyysin ja ennustetaulukon kaltaisia ominaisuuksia.

:::image type="content" source="media/open-in-excel-vendor-ledger-entries.png" alt-text="Esimerkki asiakastapahtumien merkintöjen tietojen analysoinnista Excelin avulla." lightbox="media/open-in-excel-vendor-ledger-entries.png":::

> [!TIP]
> Jos järjestelmän ominaisuudet määritetään OneDriveen, Excel-työkirja avautuu selaimeen.

Lisätietoja ostotietojen tapauskohtaisen analyysin tekemisestä on [ostotietojen ad hoc -analyysissä](ad-hoc-analysis-purchasing.md).

## Valmiit ostoraportit

[!INCLUDE [prod_short](includes/prod_short.md)] sisältää useita sisäisiä raportteja, jäljitystoimintoja ja työkaluja, joiden avulla osto-organisaatiot voivat raportoida tiedoistaan.

Saatavana olevien raporttien yleiskuvan saa valitsemalla **Kaikki raportit** aloitussivun yläosassa. Tämä toiminto avaa roolienhallinta-sivun, joka on suodatettu näyttämään **Raportti ja analyysi** -vaihtoehdon ominaisuudet. Lisätietoja on kohdassa [Raporttien etsiminen roolienhallinnan avulla](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-purchasing.png" alt-text="Esimerkki XXX-roolikeskuksen raporteista" lightbox="media/report-explorer-purchasing.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Jos haluat lisätietoja ostoihin liittyvistä raporteista, siirry kohtaan [Sisäiset ostoraportit](purchase-reports.md).

## Ostojen analytiikka näytöllä

[!INCLUDE [prod_short](includes/prod_short.md)]issa on useita sivuja, joista saadaan ostojen yleiskatsauksia ja tehtäviä töitä. Seuraavassa on esimerkki siitä, miten pääset aloittamaan:

- [Ostojen päivämäärien laskeminen](purchasing-date-calculation-for-purchases.md)

### Ostoihin liittyvän pääkirjanpidon tapahtumien ja saldojen näyttäminen Tilikartta-sivulta

Tilikartta-sivulla on näkyvissä kaikki kirjanpitotilit ja kootut luvut pääkirjanpitoon tehdyistä kirjauksista. Seuraavat ovat mahdollisia tällä sivulla:  

- Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.  
- Voit tarkastella luetteloa kyseisen tilin kirjausryhmistä.
- Yhden tilin erillisten debet- ja kreditsaldojen näyttäminen.

Erityisesti ostoja varten Tilikartta-sivulla voidaan luoda näkymä, jossa näkyvät vain ostotapahtumien kirjaamiseen käytettävät tilit.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Esimerkki merkityksellisten taloustietojen näkymisestä Tilikartta-sivulla" lightbox="media/chart-of-accounts-page.png":::

Lisätietoja on kohdassa [Tilikartan ymmärtäminen](finance-general-ledger.md#the-chart-of-accounts).

### Analysoi tiedot dimensioiden mukaan (liittyvät ostoihin)

Dimensiot ovat tapahtumia luokittelevia arvoja, jotta voit seurata ja analysoida tapahtumia asiakirjoissa, kuten ostotilauksissa. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin.  

Sen sijaan että kullekin osastolle ja sijainnille määritettäisiin erilliset kirjanpitotilit, dimensioita voidaan käyttää analyysin perustana ja välttää monimutkaisen tilikarttarakenteen luominen.

Lue lisätietoja kohdasta [Analysoi tietoja dimensioiden mukaan](bi-how-analyze-data-dimension.md).

## Katso myös

[Yrityksen konsolidointi](finance-consolidated-company-reporting.md)  
[Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md)  
[Taloushallinnon raportoinnin käsitteleminen liiketoimintayksiköiden tai yritysten välillä](finance-consolidated-company-reporting.md)  
[Ostotietojen ad-hoc-analyysi](ad-hoc-analysis-purchasing.md)  
[Valmiit ostoraportit](purchase-reports.md)  
[Tilikartan ymmärtäminen](finance-general-ledger.md#the-chart-of-accounts)  
[Tietojen analysoiminen dimensioiden mukaan](bi-how-analyze-data-dimension.md)  
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]