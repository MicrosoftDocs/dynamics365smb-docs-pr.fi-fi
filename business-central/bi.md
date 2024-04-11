---
title: Business Centralin talousanalytiikka
description: 'Business Central sisältää useita ominaisuuksia, joiden avulla voit kerätä, analysoida ja jakaa arvokkaita yritystietoja liiketoimintatietoa ja päätöksentekoa varten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: kepontop
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '103, 108, 198, 490'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Business Centralin talousanalytiikka

Yritykset sieppaavat valtavan määrän tietoa päivittäisten toimintojen aikana, ja ne tukevat päätöksentekijöille arvokkaita liiketoimintatietoja: 

- Myyntiluvut
- Ostot
- Juoksevat kulut
- Työntekijöiden palkat
- Budjetit

[!INCLUDE[prod_short](includes/prod_short.md)]issa monia toimintoja, joiden avulla voidaan kerätä, analysoida ja jakaa yrityksen taloustietoja:

- Taloushallinnon raportointi (tilinpäätöksiä ja tunnuslukuja varten)
- Tapauskohtainen luetteloissa tapahtuma analyysi
- Excelin tietojen tapauskohtainen analyysi (Avaa Excelissä -toiminnon avulla)
- Valmiit talousraportit

Kullakin näistä ominaisuuksista omat etunsa ja haittapuolensa tietojen analyysityypin ja käyttäjän roolin mukaan. Lisätietoja on kohdassa [Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md).

Tässä artikkelissa käsitellään näiden analyysiominaisuuksien käyttämistä merkityksellisten taloustietojen tuottamiseen.

## Taloushallinnon analyysitarpeet

Taloushallinnon analyysitarpeita pohdittaessa kannattaa ehkä käyttää mielikuvaa, joka perustuu ylätasolla kuvattuihin henkilötyyppeihin ja heidän vaihteleviin analyysitarpeisiin.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Kuvassa analytiikan eri henkilötyypit" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Eri tehtävissä toimivilla henkilöillä voi olla erilaisia tietoja koskevia tarpeita, minkä lisäksi he käyttävät tietoja eri tavoin. Esimerkiksi taloushallinnossa työskentelevät käyttävät tietoja eri tavalla kuin myynnissä työskentelevät.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Kuvassa erilaisten henkilöhahmojen erilaiset analytiikkatarpeet" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rooli              | Tietojen koostaminen  | Tyypilliset tietojen käyttötavat                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|Talousjohtaja/toimitusjohtaja          | Suoritustiedot  | Tunnusluvut <br> Koontinäytöt <br> Talousraportit           |
|Rahoituksenhallinta | Trendit, yhteenvedot | Valmiit johdon raportit <br> Tapahtumakohtainen analyysi      | 
|Kirjanpitäjä         | Eritellyt tiedot     | Valmiit operatiiviset raportit <br> Näytöllä näkyvät tehtävän tiedot |

## Taloushallinnon tunnusluvut

Suorituskykymittari (tunnusluku) on mitattava arvo, joka ilmaisee, kuinka tehokkaasti tavoite toteutuu. Taloushallinnossa käytetään usein seuraavia tunnuslukuja seuraamaan organisaation taloudellista tilannetta:

- Bruttokate
- Nettovoittomarginaali
- Käyttöpääoma
- Käyttöpääoma- ja maksuvalmiussuhde
- Rahoituksen kerrannaisvaikutus eli velkavipu
- Velkaantumisaste
- Kokonaisliikevaihto
- Oman pääoman tuotto
- Kokonaispääoman tuotto

<!-- Not ready to publish yet
For more information, see [Financial KPIs in Business Central](bi-finance-kpis.md) 
-->

## Tilinpäätösten ja tunnuslukujen tuottaminen taloushallinnon raportoinnin avulla

**Talousraportit**-ominaisuus antaa merkityksellisiä tietoja tilikartassa näkyvistä taloudellisesta tiedoista. Talousraportit voidaan määrittää analysoimaan kirjanpitotilien lukuja ja vertaamaan pääkirjanpidon tapahtumia budjettitapahtumiin. Tulokset näkyvät aloitussivun kaavioissa ja raporteissa, kuten kassavirtakaaviossa sekä Tuloslaskelma- ja Tase-raporteissa.

Dimensioilla on tärkeä tehtävä liiketoimintatiedoissa. Dimensio on tieto, jonka voi lisätä tapahtumaan parametriksi. Dimensioiden avulla voidaan ryhmitellä samankaltaisia ominaisuuksia, kuten asiakkaita, alueita, tuotteita ja myyjiä, ja noutaa nämä ryhmät helposti analyysia varten. Dimensioita voi käyttää esimerkiksi analyysinäkymien määrityksessä sekä talousraporttien luonnissa. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

> [!TIP]
> Tapahtumatietoja voi analysoida nopeasti suodattamalla tilikarttojen loppusummat ja kaikkien **Tapahtumat**-sivujen tapahtumat dimensioittain. Hae **Määritä dimension suodatus** -toiminto.  

Seuraavassa taulukossa on taloushallinnon raportoinnin tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.  

| Vastaanottaja | Katso |
| --- | --- |
| Luo uusia taloudellisia raportteja määrittääksesi tilinpäätöksiä raportointia tai taulukoina näyttämistä varten.| [Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md)|
| Kirjanpitoraporttien avulla voit täydentää tilastotietoja. Tilastolliset tilit mahdollistavat muihin kuin tapahtumatietoihin perustuvien tietojen lisäämisen. Muut kuin tapahtumapohjaiset tiedot voidaan lisätä numeropohjaisina yksiköinä, kuten työtekijöiden määränä, pinta-alana tai niiden asiakkaiden määränä, joilla on erääntyneitä tilejä. | [Tietojen analysoiminen tilastotilien avulla](bi-use-statistical-accounts.md) |
| Tietoja uuden talousraportin määrittämisestä esimerkkien avulla. | [Vaihekuvaus: kassavirtaennusteiden tekeminen taloushallinnon raportoinnin avulla](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Analysoi taloudellinen suorituskyky määrittämällä suorituskykyilmaisimet (KPI:t) perustuen taloudellisiin raportteihin, jotka sitten julkaiset verkkopalveluina. Julkaistujen taloudellisten raporttien KPI-tietoja voi tarkastella sivustossa tai ne voi tuoda Microsoft Exceliin OData-verkkopalvelujen avulla. |[Taloudellisiin raportteihin perustuvan KPI-verkkopalvelun määrittäminen ja julkaiseminen](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Näkymän määrittäminen tietojen analysointia varten dimensioiden avulla.|[Tietojen analysointi dimensioiden mukaan](bi-how-analyze-data-dimension.md)|
| Uusien analyysiraporttien luominen myyntejä, ostoja ja varastoa varten sekä analyysimallien määrittäminen. |[Analyysiraporttien luominen](bi-how-create-analysis-views-reports.md)|

## Taloushallinnon raportointi liiketoimintayksiköiden tai yritysten välillä

Jotkin organisaatiot käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa useassa liiketoimintayksikössä tai yrityksessä. Muut käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa tytäryhtiöissä, joiden tulee raportoida emo-organisaatioihin. [!INCLUDE [prod_short](includes/prod_short.md)] antaa kirjanpitäjille työkalut, jotka auttavat heitä siirtämään pääkirjanpidon tapahtumia kahdesta tai useammasta yrityksestä (tytäryrityksistä) konsolidoituun yritykseen.  

Lisätietoja on kohdassa [Yrityksen konsolidointi](finance-consolidated-company-reporting.md).

## Taloustietojen tapauskohtainen analyysi

Joskus on tarkistettava nopeasti, täsmäävätkö luvut, tai vahvistettava luku. Seuraavat ominaisuudet sopivat erinomaisesti tapauskohtaisiin analyyseihin:

- Tietojen analyysi tapahtumaluettelosivuilla
- Avaa Excelissä

Tietoanalyysiominaisuus mahdollista lähes minkä tahansa luettelosivun, kuten pääkirjanpidon tapahtumat, käyttöomaisuustapahtumat, sekkitapahtumat tai pankkitilitapahtumat, analyysitilaan siirtymisen sekä tietojen ryhmittelyn, suodattamisen ja käyttämisen pivot-tilassa halutulla tavalla.

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Esimerkki tietojen analysoinnista KP-tapahtumien sivulla" lightbox="media/data-analysis-gl-entries.png":::

Vastaavasti **Avaa Excelissä** -toiminnolla voi avata tapahtumien luettelosivun, suodattaa luettelon mahdollisesti tietojen alijoukoksi ja käsitellä sitten tietoja Excelissä. Se voidaan tehdä esimerkiksi käyttämällä tietojen analysoinnin, entä jos -analyysin ja ennustetaulukon kaltaisia ominaisuuksia.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Esimerkki KP-tapahtumien tietojen analysoinnista Excelin avulla" lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Jos järjestelmän ominaisuudet määritetään OneDriveen, Excel-työkirja avautuu selaimeen käyttämällä Exceliä verkossa. 

<!-- Not ready yet
For more information on how to do ad-hoc analysis on ledgers, see [Ad-hoc analysis on finance data](ad-hoc-analysis-finance.md). 
-->
## Valmiit talousraportit

[!INCLUDE [prod_short](includes/prod_short.md)] sisältää useita valmiita raportteja, jäljitystoimintoja ja työkaluja, joista on hyöytä talousosaston raportoinnista vastaaville tilintarkastajille tai valvojille.

Saatavana olevien raporttien yleiskuvan saa valitsemalla **Kaikki raportit** aloitussivun yläruudussa. Tämä avaa roolienhallinnan, joka on suodatettu näyttämään **Raportti ja analyysi** -vaihtoehdon ominaisuudet. Lisätietoja on kohdassa [Raporttien etsiminen roolienhallinnan avulla](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-finance.png" alt-text="Esimerkki taloushallinnon roolikeskuksen raporteista" lightbox="media/report-explorer-finance.png":::

Valmiita raportteja on kahdenlaisia:

- Tulostettavaksi suunniteltu (pdf).
- Excelissä analysoitavaksi suunniteltu.

Lisätietoja on seuraavissa taloushallintoon soveltuvien raporttien yleiskatsauksissa.

- [Excelin valmiit talousraportit](finance-analyze-excel.md)
- [Valmiit keskeiset talousraportit](finance-reports.md)
- [Valmiit käyttöomaisuusraportit](fa-reports.md)
- [Valmiit myyntireskontran raportit](receivables-reports.md)
- [Valmiit ostoreskontran raportit](payables-reports.md)

<!-- TODO: add when we have these articles
* [Built-in Cost Accounting reports](cost-accounting-reports.md) 
* [Built-in Cash Management reports](cost-accounting-reports.md) 
* [Built-in Tax and VAT reports](tax-and-vat-reports.md) 
-->

## Näytössä näkyvät taloushallinnon tehtäväsivut

[!INCLUDE [prod_short](includes/prod_short.md)]issa on useita sivuja, joista saadaan taloushallinnon yleiskatsauksia ja tehtäviä töitä.

### Pääkirjanpidon tapahtumien ja saldojen näyttäminen Tilikartta-sivulta

Tilikartta-sivulla on näkyvissä kaikki kirjanpitotilit ja kootut luvut pääkirjanpitoon tehdyistä kirjauksista. Seuraavat ovat mahdollisia tällä sivulla:  

- Voit tarkastella pääkirjanpitotapahtumat- ja saldot näyttäviä raportteja.  
- Voit tarkastella luetteloa kyseisen tilin kirjausryhmistä.
- Yhden tilin erillisten debet- ja kreditsaldojen näyttäminen.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Esimerkki merkityksellisten taloustietojen näkymisestä Tilikartta-sivulla" lightbox="media/chart-of-accounts-page.png":::

Lisätietoja on kohdassa [Tilikartan ymmärtäminen](finance-general-ledger.md#the-chart-of-accounts).

### Todellisten summien tarkasteleminen verrattuna kaikkien tilien budjetoituihin summiin useilta kausilta

Yrityksen tietojen keräämisen, analysoinnin ja jakamisen osana halutaan ehkä tarkastella todellisia summia sekä verrata niitä kaikkien tilien ja useiden ajanjaksojen budjetoituihin summiin. Se voidaan tehdä **Tilikartta**-sivulla valitsemalla **KP-saldo/-budjetti**-toiminto.

Lisätietoja on kohdassa [Todellisten summien analysointi budjetoituihin summiin nähden](bi-how-analyze-actual-versus-budget.md).

### Tietojen analysoiminen dimensioiden mukaan

Dimensiot ovat tapahtumia luokittelevia arvoja, jotta voit seurata ja analysoida tapahtumia asiakirjoissa, kuten myyntitilauksissa. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin.  

Sen sijaan että kullekin osastolle ja projektille määritettäisiin erilliset kirjanpitotilit, dimensioita voidaan käyttää analyysin perustana ja välttää monimutkaisen tilikarttarakenteen luominen.

Talousanalyysissa dimensio on tieto, joka lisätään KP-tapahtumaan eräänlaiseksi merkiksi. Tämän tiedon avulla voidaan yhdistää ryhmiksi KP-tapahtumia, joilla on samoja ominaisuuksia, kuten asiakkaita, alueita, tuotteita tai myyjiä, sekä noutaa nämä ryhmät helposti analysoitavaksi. Dimensioita voidaan käyttää päiväkirjojen tapahtumissa, asiakirjoissa ja budjeteissa. Lisätietoja on kohdassa [Tietojen analysointi dimensioittain](bi-how-analyze-data-dimension.md)

### Kassavirran analysoiminen

Kirjanpitäjän aloitussivun **Rahoituksen suorituskyky** -kohdan Käyttöpääomasykli-, Kassavirta- ja Tulot ja kulut -kaavioiden avulla voi analysoida kassavirtaa eri tavoin:

- Voit tarkastella kauden lukuja aikajanan liukusäätimellä.
- Voit suodattaa kaaviota valitsemalla selitteessä lähteen.
- Voit muuttaa kauden pituutta tai siirtyä edelliseen tai seuraavaan kauteen valitsemalla avattavasta Rahoituksen suorituskyky -luettelosta sopivan vaihtoehdon.

:::image type="content" source="media/cashflow-accountant-rolecentre.png" alt-text="Esimerkki kassavirran visualisoinneista kirjanpitäjän roolikeskuksessa" lightbox="media/cashflow-accountant-rolecentre.png":::

Ennusteeseen voi perehtyä tarkastelemalla ennustetapahtumien lisäksi myös kassavirtatyökirjaa. Saat tietoja esimerkiksi siitä, miten ennuste

- käsittelee vahvistetun myynnin ja ostot
- vähentää ostoreskontran ja lisää myyntireskontran
- ohittaa myynti- ja ostotilausten kaksoiskappaleet.

Lisätietoja on kohdassa [Yrityksen kassavirran analysoiminen](finance-analyze-cash-flow.md).

## Katso myös

[Taloushallinnon raportoinnin käsitteleminen liiketoimintayksiköiden tai yritysten välillä](finance-consolidated-company-reporting.md)  
<!-- [Financial KPIs in Business Central](bi-finance-kpis.md)    -->
[Talousraporttien valmisteleminen taloustietojen ja tililuokkien avulla](bi-how-work-account-schedule.md)  
<!-- [Ad-hoc analysis on finance data](ad-hoc-analysis-finance.md)   -->
[Tilikartan ymmärtäminen](finance-general-ledger.md#the-chart-of-accounts)  
[Excelin valmiit talousraportit](finance-analyze-excel.md)  
[Valmiit keskeiset talousraportit](finance-reports.md)  
[Valmiit käyttöomaisuusraportit](fa-reports.md)  
[Valmiit myyntireskontran raportit](receivables-reports.md)  
[Valmiit ostoreskontran raportit](payables-reports.md)  
[Talouden yleiskatsaus](finance.md)  
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)   
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
