---
title: 'Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus'
description: 'Kaikkien Business Centralin tukemien analytiikka-, liiketoimintatieto- ja raportointiominaisuuksien yleiskatsaus.'
author: KennieNP
ms.topic: get-started
ms.devlang: al
ms.search.keywords: feature overview
ms.reviewer: bholtorf
ms.date: 09/22/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# <a name="analytics-business-intelligence-and-reporting-overview"></a>Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus

Pienet ja keskisuuret yritykset käyttävät valmista analytiikkaa ja raportointiominaisuuksia, joita ne voivat käyttää suoraan liiketoimintansa seuraamiseen. [!INCLUDE[prod_short](includes/prod_short.md)]issa raportteja ja analyysityökaluja, jotka kattavat kyseisten organisaatioiden perustason ja monimutkaiset liiketoimintaprosessit. Lisäksi tapahtumakohtaisia analyyseja voidaan tehdä suoraan aloitussivulla.  

## <a name="analytics-needs-in-organizations"></a>Organisaatioiden analyysitarpeet

Organisaatioiden analyysitarpeita pohdittaessa kannattaa ehkä käyttää mielikuvaa, joka perustuu ylätasolla kuvattuihin henkilötyyppeihin ja heidän vaihteleviin analyysitarpeisiinsa.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Kuvassa analytiikan eri henkilötyypit" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Tämä malli perustuu siihen tosiasiaan, että organisaation eri rooleilla on erilaisia tarpeita tietojen osalta. Mitä korkeammalla rooli on organisaatiokaaviossa, sitä enemmän kyseisten roolien töissä tarvitaan koostetietoja:

Rooleilla on usein ensisijaisia tapoja kuluttaa ja analysoida tietoja, ja nämä tavat vastaavat tarvittavaa tietojen koostetasoa.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Kuvassa erilaisten henkilöhahmojen erilaiset analytiikkatarpeet" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

Seuraavissa osissa on lisätietoja tavoista, joilla tietoja käsitellään [!INCLUDE[prod_short](includes/prod_short.md)]ista:

- Talousraportit
- Tunnusluvut ja koontinäytöt
- Tapahtumakohtainen analyysi
- Raportit

## <a name="using-financial-reports-to-produce-financial-statements-and-kpis"></a>Tilinpäätösten ja tunnuslukujen tuottaminen talousraporttien avulla

Talousraporttiominaisuuden avulla saadaan tietoja tilikarttaan sisältyvistä kirjanpitotiedoista. Talousraportit voidaan määrittää analysoimaan kirjanpitotilien lukuja ja vertaamaan pääkirjanpidon tapahtumia budjettitapahtumiin.

:::image type="content" source="media/acc_schedule_13_columns.jpg" alt-text="Näyttökuvassa talousraportti" lightbox="media/acc_schedule_13_columns.jpg":::

Dimensioilla on tärkeä tehtävä liiketoimintatiedoissa. Dimensio on tieto, joka voidaan lisätä tapahtumaan parametriksi. Dimensiot mahdollistavat sellaisten tapahtumien ryhmittelyn, joilla on samanlaiset ominaisuudet. Esimerkiksi asiakasryhmät, alueet, tuotteet ja myyjä. Ryhmät helpottavat tietojen hakemista analysoimista varten. Dimensioita voi käyttää esimerkiksi analyysinäkymien määrityksessä sekä talousraporttien luonnissa. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

Lisätietoja tilinpäätöksistä ja tunnusluvuista on kohdassa [Tilinpäätösten ja tunnuslukujen tuottaminen taloushallinnon raportoinnin avulla](bi.md).

## <a name="using-key-performance-indicators-to-meet-your-business-goals"></a>Tunnuslukujen käyttäminen liiketoimintatavoitteiden saavuttamiseen

Suorituskykymittari (tunnusluku) on mitattava arvo, joka ilmaisee, kuinka tehokkaasti tavoite toteutuu. Tunnusluvat ovat eräänlainen yrityksen tuloskortti eli tapa mitata, toteutuvatko tavoitteet.

Tunnuslukujen tunnistaminen ja seuraaminen ilmaisee, eteneekö liiketoiminta oikeaan suuntaan vai onko tehtävä muutoksia. Oikein käytettyinä tunnusluvut ovat tehokkaita työkaluja, joiden avulla voi

- seurata yrityksen taloudellista tilannetta
- mitata edistymistä strategisten tavoitteiden perusteella
- havaita ongelma hyvissä ajoin
- tehdä oikea-aikaisia taktiikan muutoksia
- motivoida ryhmän jäseniä
- parantaa ja nopeuttaa päätöksentekoa.

Lisätietoja tunnusluvuista on kohdassa [Tunnuslukujen käyttäminen liiketoimintatavoitteiden saavuttamiseen](./analytics-about-kpis.md)

## <a name="ad-hoc-data-analysis"></a>Ad-hoc-tietoanalyysi

Sinun on ehkä tarkistettava nopeasti, täsmäävätkö luvut, vahvistettava tai kumottava liiketoimintaa koskeva päätelmä tai ehkäpä etsittävä poikkeamia taloustiedoista. Tapauskohtaisia analyyseja varten ei ehkä ole valmiita raportteja, jotka auttavat vastaamaan kysymyksiin. Talouskohtaisissa analyyseissa käytetään kahta seuraavaa ominaisuutta:

- Tietojen analyysi tapahtumaluettelosivuilla
- Avaa Excelissä

Tietoanalyysiominaisuus mahdollistaa lähes minkä tahansa luettelosivun, kuten Pääkirjanpidon tapahtumat- tai Asiakastapahtumat-sivujen, analyysitilaan siirtymisen sekä tietojen ryhmittelyn, suodattamisen ja käyttämisen pivot-tilassa halutulla tavalla. 

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Esimerkki tietojen analysoinnista KP-tapahtumien sivulla" lightbox="media/data-analysis-gl-entries.png":::

Vastaavasti **Avaa Excelissä** -toiminnolla voi avata luettelosivun, suodattaa luettelon mahdollisesti tietojen alijoukoksi ja käsitellä sitten tietoja Excelissä. Se voidaan tehdä esimerkiksi käyttämällä tietojen analysoinnin, entä jos -analyysin ja ennustetaulukon kaltaisia ominaisuuksia.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Esimerkki KP-tapahtumien tietojen analysoinnista Excelin avulla" lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Jos järjestelmän ominaisuudet määritetään OneDriveen, Excel-työkirja avautuu selaimeen käyttämällä Exceliä verkossa.

Lisätietoja tapauskohtaisista analyyseista on kohdassa [Tapauskohtainen tietoanalyysi](reports-adhoc-analysis.md).

## <a name="reports"></a>Raportit

Raportti [!INCLUDE[prod_short](includes/prod_short.md)]issa kerää tietoja määritettyjen ehtosarjojen perusteella. Raporteissa tiedot järjestetään ja ilmaistaan helposti luettavassa muodossa, jota voi käyttää Excelissä ja jonka voi tulostaa tai tallentaa tiedostona.  

***Myyntisaatavien tilanne** -raportti on esimerkki Excelin vuorovaikutteisesta raportista, jonka avulla voidaan analysoida, mitä asiakkaat ovat velkaa ja milloin maksut erääntyvät.

:::image type="content" source="media/aged-accounts-receivables-excel.png" alt-text="Esimerkki vuorovaikutteista Myyntisaatavien tilanne -raportista Excelissä" lightbox="media/aged-accounts-receivables-excel.png":::

Myyntisaatavien tilannetta varten [!INCLUDE[prod_short](includes/prod_short.md)] sisältää myös tulostettavaksi suunnitellun raportin. Tulostusmahdollisuus on kätevä, jos tiedot halutaan saada .pdf-tiedostona.

:::image type="content" source="media/aged-accounts-receivables-pdf.png" alt-text="Esimerkki pdf-muotoisesta Myyntisaatavien tilanne -raportista" lightbox="media/aged-accounts-receivables-pdf.png":::

[!INCLUDE[prod_short](includes/prod_short.md)]issa on yli 300 valmista raporttia, joita voidaan käyttää liiketoimintaprosessien tukena ja joiden avulla saadaan tietopohjaisia merkityksellisiä tietoja. Kaikista roolin käytössä olevista raporteista saadaan nopea yleiskuva avaamalla raporttienhallinta roolikeskuksesta, kaikilta luettelosivuilta ja **Kerro, mitä haluat tehdä** -ominaisuudesta.

:::image type="content" source="media/report-explorer-finance.png" alt-text="Esimerkki kaikkien roolin raporttien näyttämisestä raporttienhallinnassa" lightbox="media/report-explorer-finance.png":::

Lisätietoja kaikkien valmiiden raporttien tarkastelemisesta raporttienhallinnan avulla on kohdassa [Raportteihin tutustuminen roolikohtaisesti](ui-role-explorer.md).

Seuraavassa taulukossa on luettelo artikkeleista, joissa käsitellään [!INCLUDE[prod_short](includes/prod_short.md)]in valmiiden raporttien käyttämistä.

| Vastaanottaja  | Katso |
| --- | --- |
| Tietoja raporttien käyttämisestä (kirjamerkit, suoritus, tulostus, aikataulutus ja asettelun muuttaminen). | [Raporttien käyttäminen päivittäisessä työssä](reports-use-reports.md) |
| Tietoja [!INCLUDE[prod_short](includes/prod_short.md)]issa käytettävissä olevista valmiista raporteista. |[Raportin yleiskatsaus](reports-available-reports.md)| 
| Kaikkien valmiiden raporttien näyttäminen raporttienhallinnan avulla. | [Raportteihin tutustuminen roolikohtaisesti](ui-role-explorer.md) |

## <a name="external-business-intelligence-and-reporting-tools"></a>Ulkoiset liiketoimintatieto- ja raportointityökalut

Halutessasi voit käyttää liiketoimintatietojen työkaluja, joita ei ole upotettu [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Seuraavassa taulukossa on linkkejä ohjeisiin ja ulkoisten työkalujen käyttötapoihin.

| Vastaanottaja  | Katso |
| --- | --- |
| Power BI:n käyttäminen Business Centralin tietojen kanssa | [Power BI:n käyttäminen Business Centralin kanssa](admin-powerbi.md) |
| Integroi ulkoiset liiketoimintatietotyökalut sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] kanssa.| [Ulkoiset liiketoimintatietotyökalut](reports-external-analysis.md) |
| Tietojen poimiminen tietovarastoon tai Data Lake ‑tallennustilaan| [Tietojen poimiminen tietovarastoon tai Data Lakeen](/dynamics365/business-central/dev-itpro/performance/performance-developer#efficient-extracts-to-data-lakes-or-data-warehouses) |
| Business Centralin tietojen analysointi Microsoft Fabricin avulla| [Microsoft Fabricin ja Business Centralin esittely](admin-fabric.md) |
| Tietojen lukeminen Business Centralista ohjelmointirajapintojen avulla | [Business Centralin ohjelmointirajapinta v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) |

## <a name="analytics-by-functional-area"></a>Analytiikka toiminnallisten alueitten mukaan

Tämän artikkelin yleinen sisältö on saatavilla myös erikoisversioina monille [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman toiminnallisille alueille.

| Jos työskentelet... | Katso |
| --- | --- |
| Taloushallinto | [Talousanalytiikka](bi.md) |
| Myynti | [Myynnin analyysi](sales-analytics-overview.md) |
| Ostaminen | [Ostamisen analyysi](purchasing-analytics-overview.md) |
| Käyttöomaisuuden hallinta | [Käyttöomaisuuden analyysi](fa-analytics-overview.md) |


## <a name="see-also"></a>Katso myös

[Tilinpäätösten ja tunnuslukujen tuottaminen taloushallinnon raportoinnin avulla](bi.md)  
[Tunnuslukujen käyttäminen liiketoimintatavoitteiden saavuttamiseen](analytics-about-kpis.md)  
[Tapahtumakohtaisen tietoanalyysi tekeminen](reports-adhoc-analysis.md)  
[Raporttien käyttäminen päivittäisessä työssä](reports-use-reports.md)  
[Valmiiden raporttien yleiskuvaus](reports-available-reports.md)  
[Raportteihin tutustuminen roolikohtaisesti](ui-role-explorer.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
