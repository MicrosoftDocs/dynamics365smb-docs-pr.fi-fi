---
title: Varastoanalyysi
description: 'Business Central sisältää monia ominaisuuksia, joiden avulla voit kerätä, analysoida ja jakaa arvokasta varastotietoa organisaation liiketoimintatietoja ja päätöksentekoa varten.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="inventory-analytics"></a>Varastoanalyysi

Yritykset sieppaavat paljon tietoa päivittäisten toimintojen aikana, ja ne tukevat varastopäälliköille arvokkaita liiketoimintatietoja:

- Tavaroiden toimitus, kun myyntitilaukset täytetään.
- Nimikkeiden vastaanotot silloin, kun ostotilaukset täytetään.
- Nimikkeiden siirot sijaintien välillä.

[!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa monia toimintoja, joiden avulla voidaan kerätä, analysoida ja jakaa yrityksen varastotietoja:

- Tapauskohtainen luetteloissa tapahtuma analyysi
- Excelin tietojen tapauskohtainen analyysi (Avaa Excelissä -toiminnon avulla)
- Valmiit varastoanalytiikkatyökalut
- Valmiit varastoraportit

Kullakin näistä ominaisuuksista on etunsa ja haittapuolensa tietojen analyysityypin ja käyttäjän roolin mukaan. Lisätietoja on kohdassa [Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md).

Tässä artikkelissa esitellään, kuinka voit käyttää näitä analyyttisiä ominaisuuksia saadaksesi tietoa varastostasi.

## <a name="analytics-needs-in-inventory"></a>Varastojen analyysitarpeet

Varaston hallinnan analytiikkatarpeita pohdittaessa voi olla hyödyllistä käyttää persoonapohjaista mallia, joka kuvaa korkealla tasolla erilaisia analytiikan tarpeita.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Kuvassa analytiikan eri henkilötyypit" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Eri tehtävissä toimivilla henkilöillä voi olla erilaisia tietoja koskevia tarpeita, minkä lisäksi he käyttävät tietoja eri tavoin. Esimerkiksi resurssinhallinnassa ja taloushallinnossa työskentelevät käyttävät tietoja eri tavalla kuin myynnissä työskentelevät.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Kuvassa erilaisten henkilöhahmojen erilaiset analytiikkatarpeet" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rooli              | Tietojen koostaminen  | Tyypilliset tietojen käyttötavat                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|Operatiivinen johtaja/talousjohtaja/toimitusjohtaja    | Suoritustiedot  | Suorituskykyilmaisimia, koontinäyttöjä, talousraportteja           |
|Varastopäällikkö  | Trendit, yhteenvedot | Sisäiset johdon raportit, ad-hoc-analyysi      | 
|Varastotyöntekijä   | Eritellyt tiedot     | Sisäiset toimintaraportit, näyttötehtävätiedot |

<!-- 
## <a name="inventory-kpis"></a>Inventory KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In inventory management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-inventory"></a>Financial Reportingin käyttö tilinpäätösten ja varastoon liittyvien KPI:iden tuottamiseen

**Financial Reporting** -ominaisuus antaa merkityksellisiä tietoja tilikartassa näkyvistä taloudellisesta tiedoista. Talousraportit voidaan määrittää analysoimaan kirjanpitotilien lukuja ja vertaamaan pääkirjanpidon tapahtumia budjettitapahtumiin. Erityisesti varastonhallintaa varten voidaan määrittää talousraportteja pääkirjanpidon (KP-) tileille, joita käytetään varaston kirjausten seurantaan.

Dimensioilla on tärkeä tehtävä liiketoimintatiedoissa. Dimensio on tieto, joka voidaan lisätä tapahtumaan parametriksi. Dimensioiden avulla voidaan ryhmitellä samankaltaisia ominaisuuksia, kuten asiakkaita, alueita, tuotteita ja myyjiä. Dimensioita voi käyttää esimerkiksi analyysinäkymien määrityksessä sekä talousraporttien luonnissa. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

Lisätietoja talousraporteista on kohdassa [Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-inventory"></a>Taloushallinnon raportointi liiketoimintayksiköiden tai yritysten välillä (varastoihin liittyvät)

Jotkin organisaatiot käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa useassa liiketoimintayksikössä tai yrityksessä. Muut käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa tytäryhtiöissä, jotka raportoivat pääorganisaatioille. [!INCLUDE [prod_short](includes/prod_short.md)] antaa kirjanpitäjille työkalut, jotka auttavat heitä siirtämään pääkirjanpidon tapahtumia kahdesta tai useammasta yrityksestä (tytäryrityksistä) konsolidoituun yritykseen. Erityisesti varastonhallintaa varten pääkirjanpidon tapahtumat voidaan haluta konsolidoida varastotilien osalta, jotta ostojen KPI:iä voitaisiin seurata liiketoimintayksiköissä tai oikeushenkilöissä.

Lisätietoja on kohdassa [Yrityksen konsolidointi](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-inventory-data"></a>Varastotietojen ad-hoc-analyysi

Joskus on tarkistettava nopeasti, täsmäävätkö luvut, tai vahvistettava luku. Seuraavat ominaisuudet sopivat erinomaisesti tapauskohtaisiin analyyseihin:

- Tietojen analyysi tapahtumaluettelosivuilla
- Avaa Excelissä

Tietoanalyysiominaisuus mahdollistaa lähes minkä tahansa luettelosivun, kuten **Nimikekirjanpidon tapahtumat**- tai Käyttöomaisuuden kirjanpitotapahtumat -sivujen, analyysitilaan siirtymisen sekä tietojen ryhmittelyn, suodattamisen ja käyttämisen pivot-tilassa halutulla tavalla.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Esimerkki jäännöserän tietojen analysoinnista nimiketapahtumamerkintöjen sivulla." lightbox="media/data-analysis-inventory-dead-stock.png":::

Vastaavasti **Avaa Excelissä** -toiminnolla voi avata luettelosivun, suodattaa luettelon mahdollisesti tietojen alijoukoksi ja käsitellä sitten tietoja Excelissä. Se voidaan tehdä esimerkiksi käyttämällä tietojen analysoinnin, entä jos -analyysin ja ennustetaulukon kaltaisia ominaisuuksia.

<!-- :::image type="content" source="media/open-in-excel-item-ledger-entries.png" alt-text="Example of how to do data analysis on the Item Ledger Entries data using Excel." lightbox="media/open-in-excel-item-ledger-entries.png"::: -->

> [!TIP]
> Jos järjestelmän ominaisuudet määritetään OneDriveen, Excel-työkirja avautuu selaimeen.

Lisätietoja varastotietojen tapauskohtaisen analyysin tekemisestä on [varastotietojen ad hoc -analyysissä](ad-hoc-analysis-inventory.md).

## <a name="built-in-reports-for-inventory"></a>Valmiit varastoraportit

[!INCLUDE [prod_short](includes/prod_short.md)] sisältää useita sisäisiä raportteja, jäljitystoimintoja ja työkaluja, joiden avulla varasto-organisaatiot voivat raportoida tiedoistaan.

Saatavana olevien raporttien yleiskuvan saa valitsemalla **Kaikki raportit** aloitussivulla. Tämä toiminto avaa raporttienhallinta-sivun, joka on suodatettu näyttämään **Raportti ja analyysi** -vaihtoehdon ominaisuudet. Valitse **Myynti ja markkinointi** -otsikon alla **Tutki**. Lisätietoja on kohdassa [Raporttien etsiminen roolienhallinnan avulla](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-sales.png" alt-text="Esimerkki myyntiroolikeskuksen raporteista" lightbox="media/report-explorer-sales.png":::

<!-- The built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Jos haluat lisätietoja varastoihin liittyvistä raporteista, siirry kohtaan [Sisäiset varastot ja varastoraportit](inventory-WMS-reports.md).

## <a name="on-screen-inventory-analytics"></a>Varastojen analytiikka näytöllä

[!INCLUDE [prod_short](includes/prod_short.md)]issa on useita sivuja, joista saadaan varaston yleiskatsauksia ja tehtäviä töitä. Seuraavassa on joitakin esimerkkejä, joilla voit aloittaa:

- [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)
- [Sarja-, erä- ja pakettinumeroita sisältävien nimikkeiden seuraaminen](inventory-how-work-item-tracking.md)
- [Nimikeseurannassa olevien nimikkeiden jäljittäminen](inventory-how-to-trace-item-tracked-items.md)
- [Varastotapahtumien ja pääkirjanpidon välisen täsmäytyksen tarkistaminen](finance-how-to-post-inventory-costs-to-the-general-ledger.md#to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger)
- [Laituroitujen nimikkeiden tarkasteleminen toimituksessa tai poimintatyökirjassa](warehouse-how-to-cross-dock-items.md#to-view-cross-docked-items-in-a-shipment-or-pick-worksheet)

Myyntimoduuli sisältää myös varastoon liittyviä analytiikkasivuja:

- [Toimituksen lupaamisen päivämäärien laskeminen](sales-how-to-calculate-order-promising-dates.md)
- [Laske myyntitilausten toimituspäivämäärät](sales-date-calculation-for-sales.md)
- [Pakettien seuraaminen](sales-how-track-packages.md)

### <a name="show-inventory-related-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Varastoihin liittyvän pääkirjanpidon tapahtumien ja saldojen näyttäminen Tilikartta-sivulta

**Tilikartta**-sivulla on näkyvissä kaikki kirjanpitotilit ja kootut luvut pääkirjanpitoon tehdyistä kirjauksista. Seuraavat ovat mahdollisia tällä sivulla:  

- Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.  
- Voit tarkastella luetteloa kyseisen tilin kirjausryhmistä.
- Yhden tilin erillisten debet- ja kreditsaldojen näyttäminen.

Erityisesti varastonhallintaa varten Tilikartta-sivulla voidaan luoda näkymä, jossa näkyvät vain varastotapahtumien kirjaamiseen käytettävät tilit.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Esimerkki merkityksellisten taloustietojen näkymisestä Tilikartta-sivulla" lightbox="media/chart-of-accounts-page.png":::

Lisätietoja on kohdassa [Tilikartan ymmärtäminen](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-inventory-data-by-dimensions"></a>Analysoi varastotiedot dimensioiden mukaan

Dimensiot ovat tapahtumia luokittelevia arvoja, jotta voit seurata ja analysoida tapahtumia asiakirjoissa, kuten myyntitilauksissa. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin.  

Sen sijaan että kullekin osastolle ja sijainnille määritettäisiin erilliset kirjanpitotilit, dimensioita voidaan käyttää analyysin perustana ja välttää monimutkaisen tilikarttarakenteen luominen.

Lue lisätietoja kohdasta [Analysoi tietoja dimensioiden mukaan](bi-how-analyze-data-dimension.md).

## <a name="see-also"></a>Katso myös

[Yrityksen konsolidointi](finance-consolidated-company-reporting.md)   
[Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md)  
[Taloushallinnon raportoinnin käsitteleminen liiketoimintayksiköiden tai yritysten välillä](finance-consolidated-company-reporting.md)  
[Varastotietojen ad-hoc-analyysi](ad-hoc-analysis-inventory.md)  
[Valmiit varaston ja fyysisen varastoinnin raportit](inventory-WMS-reports.md)  
[Tilikartan ymmärtäminen](finance-general-ledger.md#the-chart-of-accounts)  
[Tietojen analysoiminen dimensioiden mukaan](bi-how-analyze-data-dimension.md)  
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)   
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
