---
title: Myynnin analyysi
description: 'Business Central sisältää monia ominaisuuksia, joiden avulla voit kerätä, analysoida ja jakaa arvokasta myyntitietoa myyntiorganisaation liiketoimintatietoja ja päätöksentekoa varten.'
author: kennienp
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="sales-analytics"></a>Myynnin analyysi

Yritykset sieppaavat paljon tietoa päivittäisten toimintojen aikana, ja ne tukevat myyntipäälliköille arvokkaita liiketoimintatietoja:

- Mahdollisuudet
- Myyntitarjoukset
- Myyntitilaukset
- Myyntilaskut

[!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa monia toimintoja, joiden avulla voidaan kerätä, analysoida ja jakaa yrityksen myyntitietoja:

- Tapauskohtainen luetteloissa tapahtuma analyysi
- Excelin tietojen tapauskohtainen analyysi (Avaa Excelissä -toiminnon avulla)
- Valmiit myyntianalytiikkatyökalut
- Valmiit myyntiraportit

Kullakin näistä ominaisuuksista on etunsa ja haittapuolensa tietojen analyysityypin ja käyttäjän roolin mukaan. Lisätietoja on kohdassa [Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md).

Tässä artikkelissa käsitellään miten näitä analyysiominaisuuksia käytetään merkityksellisten myyntitietojen hankkimiseen.

## <a name="analytics-needs-in-sales"></a>Myynnin analyysitarpeet

Myynnin hallinnan analytiikkatarpeita pohdittaessa voi olla hyödyllistä käyttää persoonapohjaista mallia, joka kuvaa korkealla tasolla erilaisia analytiikan tarpeita.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Kuvassa analytiikan eri henkilötyypit" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Eri tehtävissä toimivilla henkilöillä voi olla erilaisia tietoja koskevia tarpeita, minkä lisäksi he käyttävät tietoja eri tavoin. Esimerkiksi resurssinhallinnassa ja taloushallinnossa työskentelevät käyttävät tietoja eri tavalla kuin myynnissä työskentelevät.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Kuvassa erilaisten henkilöhahmojen erilaiset analytiikkatarpeet" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rooli              | Tietojen koostaminen  | Tyypilliset tietojen käyttötavat                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CCO / CFO / CEO    | Suoritustiedot  | Tunnusluvut <br> Koontinäytöt <br> Talousraportit           |
|Myyntipäällikkö      | Trendit, yhteenvedot | Valmiit johdon raportit <br> Tapahtumakohtainen analyysi      | 
|Asiakaspäällikkö/Myyjä | Eritellyt tiedot     | Valmiit operatiiviset raportit <br> Näytöllä näkyvät tehtävän tiedot |

<!-- 
## <a name="sales-kpis"></a>Sales KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In sales management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-sales"></a>Financial Reportingin käyttö myyntiin liittyvien tilinpäätösten ja KPI:iden tuottamiseen

**Financial Reporting** -ominaisuus antaa merkityksellisiä tietoja tilikartassa näkyvistä taloudellisesta tiedoista. Talousraportit voidaan määrittää analysoimaan kirjanpitotilien lukuja ja vertaamaan pääkirjanpidon tapahtumia budjettitapahtumiin. Erityisesti myynninhallintaa varten voidaan määrittää talousraportteja pääkirjanpidon (KP-) tileille, joita käytetään myynnin kirjausten seurantaan.

Dimensioilla on tärkeä tehtävä liiketoimintatiedoissa. Dimensio on tieto, joka voidaan lisätä tapahtumaan parametriksi. Dimensioiden avulla voidaan ryhmitellä samankaltaisia ominaisuuksia, kuten asiakkaita, alueita, tuotteita ja myyjiä. Dimensioita voi käyttää esimerkiksi analyysinäkymien määrityksessä sekä talousraporttien luonnissa. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

Lisätietoja talousraporteista on kohdassa [Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-sales"></a>Taloushallinnon raportointi ostoihin liittyvien liiketoimintayksiköiden tai yritysten välillä

Jotkin organisaatiot käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa useassa liiketoimintayksikössä tai yrityksessä. Muut käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa tytäryhtiöissä, jotka raportoivat pääorganisaatioille. [!INCLUDE [prod_short](includes/prod_short.md)] antaa kirjanpitäjille työkalut, jotka auttavat heitä siirtämään pääkirjanpidon tapahtumia kahdesta tai useammasta yrityksestä (tytäryrityksistä) konsolidoituun yritykseen. Erityisesti myynninhallintaa varten pääkirjanpidon tapahtumat voidaan haluta konsolidoida myyntitilien osalta, jotta ostojen KPI:iä voitaisiin seurata liiketoimintayksiköissä tai oikeushenkilöissä.

Lisätietoja on kohdassa [Yrityksen konsolidointi](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-sales-data"></a>Myyntitietojen ad-hoc-analyysi

Joskus on tarkistettava nopeasti, täsmäävätkö luvut, tai vahvistettava luku. Seuraavat ominaisuudet sopivat erinomaisesti tapauskohtaisiin analyyseihin:

- Tietojen analyysi tapahtumaluettelosivuilla
- Avaa Excelissä

Tietojen analysointiominaisuuden avulla voit avata lähes minkä tahansa luettelosivun, kuten **Pääkirjanpidon merkinnät**, **Asiakastapahtumien merkinnät**, **Nimikekirjauksen merkinnät** tai **Kirjatut laskut**, siirry analyysitilaan ja ryhmittele, suodata ja pivotoi tiedot haluamallasi tavalla.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Esimerkki tietojen analysoinnista asiakastapahtumamerkintöjen sivulla." lightbox="media/data-analysis-customer-ledger-entries.png":::

Vastaavasti **Avaa Excelissä** -toiminnolla voi avata luettelosivun, suodattaa luettelon mahdollisesti tietojen alijoukoksi ja käsitellä sitten tietoja Excelissä. Se voidaan tehdä esimerkiksi käyttämällä tietojen analysoinnin, entä jos -analyysin ja ennustetaulukon kaltaisia ominaisuuksia.

:::image type="content" source="media/open-in-excel-customer-ledger-entries.png" alt-text="Esimerkki asiakastapahtumien merkintöjen tietojen analysoinnista Excelin avulla." lightbox="media/open-in-excel-customer-ledger-entries.png":::

> [!TIP]
> Jos järjestelmän ominaisuudet määritetään OneDriveen, Excel-työkirja avautuu selaimeen.

Lisätietoja myyntitietojen tapauskohtaisen analyysin tekemisestä on [myyntitietojen ad hoc -analyysissä](ad-hoc-analysis-sales.md). 

## <a name="built-in-reports-for-sales"></a>Valmiit myyntiraportit

[!INCLUDE [prod_short](includes/prod_short.md)] sisältää useita sisäisiä raportteja, jäljitystoimintoja ja työkaluja, joiden avulla myyntiorganisaatiot voivat raportoida tiedoistaan.

Saatavana olevien raporttien yleiskuvan saa valitsemalla **Kaikki raportit** aloitussivun yläruudussa. Tämä toiminto avaa roolienhallinta-sivun, joka on suodatettu näyttämään **Raportti ja analyysi** -vaihtoehdon ominaisuudet. Lisätietoja on kohdassa [Raporttien etsiminen roolienhallinnan avulla](ui-role-explorer.md). 

:::image type="content" source="media/report-explorer-sales.png" alt-text="Esimerkki taloushallinnon roolikeskuksen raporteista" lightbox="media/report-explorer-sales.png":::

Valmiita raportteja on kahdenlaisia:

- Tulostettavaksi suunniteltu (pdf).
- Excelissä analysoitavaksi suunniteltu.

Jos haluat lisätietoja myynteihin liittyvistä raporteista, siirry kohtaan [Sisäiset myyntiraportit](sales-reports.md).

## <a name="on-screen-sales-analytics"></a>Myynnin analytiikka näytöllä

[!INCLUDE [prod_short](includes/prod_short.md)]issa on useita sivuja, joista saadaan myynnin yleiskatsauksia ja tehtäviä töitä. Seuraavassa on joitakin esimerkkejä, joilla voit aloittaa:

- [Avaa **myyntitarjous**-luettelo](https://businesscentral.dynamics.com/?page=9300)
- [Avaa **myyntitilaukset**-luettelo](https://businesscentral.dynamics.com/?page=9305)
- [Avaa **Kirjatut myyntilaskut** -luettelo](https://businesscentral.dynamics.com/?page=143)
- [Avaa **myyntipalautustilaukset**-luettelo](https://businesscentral.dynamics.com/?page=9304)
- [Toimituksen lupaamisen päivämäärien laskeminen](sales-how-to-calculate-order-promising-dates.md)
- [Laske myyntitilausten toimituspäivämäärät](sales-date-calculation-for-sales.md)
- [Pakettien seuraaminen](sales-how-track-packages.md)

### <a name="show-sales-related-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Näytä pääkirjanpidon myyntiin liittyvät tapahtumat ja saldot Tilikartta-sivulta

Tilikartta-sivulla on näkyvissä kaikki kirjanpitotilit ja kootut luvut pääkirjanpitoon tehdyistä kirjauksista. Seuraavat ovat mahdollisia tällä sivulla:  

- Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.  
- Voit tarkastella luetteloa kyseisen tilin kirjausryhmistä.
- Yhden tilin erillisten debet- ja kreditsaldojen näyttäminen.

Erityisesti myyntejä varten Tilikartta-sivulla voidaan luoda näkymä, jossa näkyvät vain myyntitapahtumien kirjaamiseen käytettävät tilit.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Esimerkki merkityksellisten taloustietojen näkymisestä Tilikartta-sivulla" lightbox="media/chart-of-accounts-page.png":::

Lisätietoja on kohdassa [Tilikartan ymmärtäminen](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-data-by-dimensions-related-to-sales"></a>Analysoi tiedot dimensioiden mukaan (liittyvät myynteihin)

Dimensiot ovat tapahtumia luokittelevia arvoja, jotta voit seurata ja analysoida tapahtumia asiakirjoissa, kuten myyntitilauksissa. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin.  

Sen sijaan että kullekin osastolle ja sijainnille määritettäisiin erilliset kirjanpitotilit, dimensioita voidaan käyttää analyysin perustana ja välttää monimutkaisen tilikarttarakenteen luominen.

Lue lisätietoja kohdasta [Analysoi tietoja dimensioiden mukaan](bi-how-analyze-data-dimension.md).

## <a name="see-also"></a>Katso myös

[Yrityksen konsolidointi](finance-consolidated-company-reporting.md)   
[Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md)  
[Taloushallinnon raportoinnin käsitteleminen liiketoimintayksiköiden tai yritysten välillä](finance-consolidated-company-reporting.md)  
[Myyntitietojen ad-hoc-analyysi](ad-hoc-analysis-sales.md)   
[Valmiit myyntiraportit](sales-reports.md)   
[Tilikartan ymmärtäminen](finance-general-ledger.md#the-chart-of-accounts)  
[Tietojen analysoiminen dimensioiden mukaan](bi-how-analyze-data-dimension.md)  
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)   
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
