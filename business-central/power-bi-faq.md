---
title: Power BI – usein kysytyt kysymykset
description: Hanki vastauksia joihinkin tyypillisiin kysymyksiin, jotka liittyvät Power BI:n ja Business Centralin käyttöön.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, reports, faq, errors
ms.date: 04/22/2021
ms.author: jswymer
ms.openlocfilehash: ef63963c7c37f36db34e3e8292e73d64c1b67538
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438750"
---
# <a name="power-bi--faq"></a>Power BI – usein kysytyt kysymykset

Tässä artikkelissa vastataan joihinkin kysymyksiin, joita sinulla voi olla, kun käytössä on Power BI ja [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Yleiset](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a>Olen valinnut raportin Business Centralin omalle roolikeskukselle. Jos myöhemmin teen muutoksia raportin visualisointeihin, päivittääkö roolikeskus muutokset automaattisesti?

Kyllä, koska raportit on upotettu Power BI:stä.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a>Ovatko Power BI:n Business Central -sovellukset saatavilla muilla kielillä kuin englanniksi?

Ei. Nämä sovellukset ovat tällä hetkellä saatavilla vain englanniksi.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a>Kun raportti on julkaistu oma powerbi.com -työtilassa, voinko ladata sen pbix-tiedoston? 

Kyllä. Lisätietoja on kohdassa [Raportin lataaminen Power BI -palvelusta Power BI Desktopiin](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files"></a>Voinko ladata sovellukset pbix-tiedostoina? 

Ei. Tällä hetkellä emme toimita virallisille Power BI -sovelluksille ladattavia pbix-tiedostoja, koska ne julkaistaan AppSourcessa.

## <a name="license"></a>[Käyttöoikeus](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a>Tarvitsenko Power BI Pro -käyttöoikeuden raporttien julkaisemisessa? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Ei. Pro-käyttöoikeutta ei tarvita raporttien julkaisemisessa. Power BI -vakiokäyttöoikeus (ilmainen) riittää. Lisätietoja on kohdassa [Power BI:n käyttöoikeudet](admin-powerbi-setup.md#license).

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license"></a>Mitä ilmaisen käyttöoikeuden omaava käyttäjä ei voi tehdä?

Et voi jakaa raportteja tai asentaa Power BI:n Business Central -sovelluksia. Muuten ilmainen käyttöoikeus mahdollistaa lähes kaikkien kaavio- ja raporttivaihtoehtojen luomisen.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a>Jos käyttäjä jakaa raportin toisen käyttäjän kanssa, myös toisella käyttäjällä on oltava Pro-käyttöoikeus nähdäkseen raportin. Tuleeko tämä ominaisuus tulevaisuudessa käyttöön ilmaisen käyttöoikeuden kanssa?

Emme voi tehdä tätä päätöstä. Sen tekee Power BI. Lisätietoja on kohdassa [Power BI -koontinäyttöjen ja -raporttien jakaminen työtovereiden ja muiden käyttäjien kanssa](/power-bi/collaborate-share/service-share-dashboards).  

## <a name="designer"></a>[Suunnitteluohjelma](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages"></a>Toimiiko yhdistin ohjelmointirajapinnan sivujen kanssa?

Kyllä. Vuoden 2021 kesäkuun jälkeen uusi Power BI -yhdistin tukee sekä Business Centralin verkkosivuja että ohjelmointirajapinnan sivuja. Lisätietoja on kohdassa [Power BI -yhdistimen käytön aloittaminen yhdessä Business Centralin ohjelmointirajapintojen kanssa pelkkien verkkopalveluiden sijaan](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### <a name="can-i-build-a-power-bi-report-using-the-sales-invoice-lines-or-journal-lines-apis"></a>Voinko luoda Power BI -raportin käyttämällä myyntilaskurivejä tai päiväkirjan rivien ohjelmointirajapintoja?

Yleisimmin käytetyt rivitietueet ovat käytettävissä [Business Central APIs v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/):ssa). Voit siis käyttää niitä raporttien rakentamiseen Power BI:ssä valitsemalla ne **Dynamics 365 Business Central** -yhdistimessä. **Rivit**-ohjelmointirajapinnat on kuitenkin suunniteltu käytettäviksi vain joidenkin erityisten suodattimien kanssa, eivätkä ne välttämättä toimi kaikissa skenaarioissa. Saatat saada virheen kuten "Sinun on määritettävä tunnus tai asiakirjatunnus saadaksesi rivit". Voit korjata tämän ongelman seuraavasti, kun saat Business Centralista Power BI Desktop -raportin tiedot:

1. Sen sijaan, että lisäisit rivientiteetin tietolähteen, lisää päätietolähde. Lisää esimerkiksi **Myyntilasku** sen sijaan, että lisäisit **Myyntilaskun rivit**.
2. Valitse **Muunna tiedot** Power BI Desktopin toimintopalkista.
3. Valitse juuri lisätty kysely, esimerkiksi **Myyntilaskut**.
4. Vähennä raporttiin ladattujen tietueiden määrää suodattamalla tietueita.
5. Vieritä oikealle, kunnes löydät riveiksi nimetyn sarakkeen, esimerkiksi **SalesInvoiceLines**.
6. Valitse laajennuspainike sarakkeen otsikossa, sarakenimen vieressä.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Näyttää SalesInvoiceLines-sarakkeen Power BI Desktopissa.":::
<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a>Onko mahdollista valita Business Central -ympäristö, josta tiedot haetaan Power BI:iin, esimerkiksi eristys- tai tuotantoympäristö? 

Kyllä. Tämän voi valita helposti. Kun yhteys Business Centraliin muodostetaan yhdistimen avulla, on valittava ympäristö ja yrityksen nimi.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a>Voiko useiden tuotantoympäristöjen tietoja yhdistää samaan vuokraajaan?

Kyllä. Power BI:ssä suoritetaan uudelleen toiminto tietojen hakemiseksi ja haetaan haluttu ympäristö.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part"></a>Millä Business Centralin sivuilla on Power BI -raportit -osa?  

Tällä hetkellä on joitakin tiettyjä sivuja, joilla on tietoruutu ja **Power BI -raportit**-osa tietojen näyttämiseksi. 

Luettelosivuilla **Power BI -raportit** -osa suodatetaan niin, että näkyvissä ovat raportit, joissa säilytetään luettelon tiedot. Tässä ovat luettelon tyypin sivut, jotka sisältävät **Power BI -raportit** -osan:

|Sivun tunnus|Name|
|-------|----|
|22|Asiakasluettelo|
|27|Toimittajaluettelo|
|31|Nimikeluettelo|
|9305|Myyntitilausluettelo|
|9308|Ostolaskut|

Tässä ovat muut sivut, jotka sisältävät laajemman, ei-suodatetun **Power BI -raportit** -osan:

|Sivun tunnus|Name|
|-------|----|
|1156|Yrityksen tiedot|
|4013|Intelligent Cloud Insights |
|9006|Tilausten käsittelijän roolikeskus|
|9008|F.var. Perusroolikeskus|
|9010|Tuotannon suunnittelijan roolikeskus|
|9015|Työn projektipäällikön roolikeskus|
|9016|Huollon aikatauluttajan roolikeskus|
|9022|Liiketoimintajohtajan roolikeskus|
|9024|Suojauksenvalvojan roolikeskus|
|9026|Myynnin ja kontaktien hallinta Roolikeskus|
|9027|Kirjanpitäjän roolikeskus|

> [!TIP]
> Tällä hetkellä suunnitelmissa ei ole lisätä tätä kaikille luettelosivuille. Voit kuitenkin luoda yksinkertaisen sivulaajennuksen, joka lisää **Power BI -raportit** osan tietoruutuun. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Power BI -raportit -osan lisääminen sivuille](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts).

<!-- 5 -->
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a>Voinko suodattaa Business Centralin tietojoukon *ennen* kuin haen tiedot Power BI:iin sen sijaan, että käytän suodattimia jälkikäteen?

Jos haluat suodattaa suuria tietojoukkoja, helpoin tapa on määrittää Power BI -raportin suodatin muokkaamalla suoraan Power Query -kaavaa. Suurin osa näin määritetyistä suodattimista välitetään Business Centraliin delegoimalla kysely lähteeseen. Katso [Tietojoukkojen lisäävä päivitys](/power-bi/admin/service-premium-incremental-refresh).

Tällä hetkellä ei ole mahdollista määrittää verkkopalveluiden tietojen suodatinta Business Centralissa. Jos sovelluksen on määritettävä suodatin Business Centralissa, sinun on luotava tätä varten mukautettu Business Central -sovellus.

<!-- 8 and 9 -->

### <a name="for-embedding-reports-in-business-central-pages-right-now-its-only-possible-to-get-reports-from-my-workspace-in-power-bi-are-there-plans-to-make-it-possible-to-get-them-from-custom-workspaces"></a>Business Centralin sivujen raporttien upottamista varten voidaan hakea raportteja vain Power BI:n *Oma työtila* -kohdassa. Onko niitä mahdollista saada mukautetuista työtiloista tulevaisuudessa?

Kyllä. Jaettujen työtilojen tuen lisääminen on suunnitelmissa, mutta tarkka ajankohta ei vielä ole tiedossa.  

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Voiko Power BI:ssa hakea tietoja kyselyn lisäksi myös muilla tavoilla sellaista Business Centralin taulukoista, joilla ei ole liitettyä sivua? Esimerkiksi *Nimikemääritteen arvon yhdistämismääritys* -taulukosta.

Ei. Ei vielä.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a>Ovatko julkaistavat kyselyt nopeampia käyttää kuin julkaistut sivut?

Verkkopalveluissa julkaistut kyselyt ovat yleensä nopeampia kuin vastaavat julkaistut sivut. Syy on se, että kyselyt on optimoitu tietojen lukemista varten. Ne eivät sisällä kalliita käynnistimiä, kuten OnAfterGetRecord-käynnistintä.

Uusi yhdistin on saatavilla vuoden 2021 kesäkuussa. Tämän jälkeen on suositeltavaa käyttää ohjelmointirajapinnan sivuja verkkopalveluina julkaistujen kyselyjen sijaan.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-the-developer-have-to-create-a-custom-query"></a>Voiko käyttäjä luoda verkkopalvelun sellaisen sarakkeen avulla, joka on Business Centralin taulukossa, mutta ei sivulla? Vai onko kehittäjän luotava mukautettu kysely? 

Kyllä. Kun uusi yhdistin on saatavilla vuoden 2021 kesäkuussa, kehittäjä voi luoda uuden API-sivun tämän vaatimuksen täyttämiseksi. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>Voinko yhdistää Power BI:n Business Central Onlinen vain luku -tilassa olevaan tietokantapalvelimeen? 

Ei. Mutta tämä toiminto on pitkän aikavälin toteutussuunnitelmassamme. 

### <a name="how-do-i-change-or-clear-the-user-account-im-currently-using-to-connect-to-business-central-from-power-bi-desktop"></a><a name="perms"></a>Miten muutan tai tyhjennän käyttäjän, jota tällä hetkellä käytän yhteyden muodostamiseen Business Centraliin Power BI Desktopista?

Tee Power BI Desktopissa seuraavat vaiheet:

1. Valitse Tiedosto-valikossa **Asetukset ja vaihtoehdot** > **Tietolähteen asetukset**.
2. Valitse luettelosta **Dynamics Business Central** ja valitse sitten **Tyhjennä käyttöoikeudet** > **Poista**.

Kun seuraavan kerran muodostat yhteyden Business Centraliin tietojen saamiseksi, sinua pyydetään kirjautumaan sisään.

## <a name="performance"></a>[Suoritustaso](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a>Onko nopeampaa hakea tiedot ohjelmointirajapinnan sivujen kuin verkkopalveluiden avulla?

Kyllä. Testimme osoittavat, että ohjelmointirajapinnan sivujen suorituskyky on 25 % parempi kuin verkkopalveluiden.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a>Onko suunnitelmissa määrittää Azure SQL Database -esiintymään peili, johon voin muodostaa yhteyden suoraan?

Ei. Ei vielä. Voit olla yhteydessä vain Business Centralin ohjelmointirajapintojen avulla.

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a>Tietojen lataaminen Business Centralin verkkopalveluista vaikuttaa hitaalta. Voiko tiedot hakea suoraan SQL-tietokantataulukosta jollakin tavalla?

Ei. Suora pääsy tietokantaan ei ole mahdollinen. Mutta siirtyminen ohjelmointirajapinnan sivuihin (kun uusi yhdistin ei ole käytettävissä) auttaa paljon.

## <a name="advanced"></a>[Lisäasetukset](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a>Tuleeko Power BI:n yhdistin tukemaan lisääviä päivitystoimintoja Power BI -palvelussa tulevaisuudessa?

Kyllä. Se on toteutussuunnitelmamme.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a>Jos Business Central on-premises ratkaisussa ei ole internet-yhteyttä, voinko silti käyttää Power BI:tä?
<!-- todo: please explain this one-->

Kyllä. Tässä tapauksessa voit käyttää Power BI Desktopia paikallisesti ja muodostaa yhteyden Business Central on-premises -ratkaisuun. Kun yhteys on muodostettu, voit luoda ja tarkastella raportteja. Ainoa mitä et voi tehdä, on julkaista niitä Power BI -palvelussa. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a>Voiko tulevaisuudessa replikoida Business Central Online -tietokannat niin, että niitä voi käyttää vain luku -tilassa olevissa SQL-kyselyissä? Tämä ominaisuus tukisi lisäävää päivitystä. Se on paljon nopeampi kuin ohjelmointirajapinnat ja verkkopalvelut.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Kyllä. Tämä toiminto on pitkän aikavälin toteutussuunnitelmassamme. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a>Parantaako suorituskykyä se, että käytän Azure Data Factorya tietojen hankkimiseksi Business Centralista ja kulutan tiedot Power BI:ssä? 

Kyllä. Tämä lisäskenaario auttaa Business Centralia pysymään suorituskykyisenä, koska tietojen käyttöoikeus määritetään Azure Data Factoryn kautta.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a>Onko suunnitelmissa tukea Power BI:n käyttöönottoputkia tai PBI-raporttien käyttöönottoputkien luomista samalla tavalla kuin laajennuksissa? Tai jopa määrittää yksinkertainen ohjelmointirajapinta Business Admin Centeriin? 

Tutkimme tätä ominaisuutta. Power BI sisältää monipuolisia ohjelmointirajapintoja raportin käyttöönottojen hallintaa varten. Lisätietoja on kohdassa [Käyttöönottoputkien esittely](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="ive-tried-the-preview-of-the-new-connector-which-will-be-live-in-june-2021-i-see-some-values-like-_x0020_-when-connecting-to-api-v20-what-are-these-values"></a>Olen yrittänyt käyttää uuden, vuoden 2021 kesäkuussa julkaistavan yhdistimen esiversiota. Näkyvissä on esimerkiksi arvo _x0020_, kun yhteyttä muodostetaan ohjelmointirajapintaan v2.0. Mitä nämä arvot ovat?

Seuraava Power BI:n yhdistimen version avulla on mahdollista muodostaa yhteys Business Centralin ohjelmointirajapinnan sivuille, myös ohjelmointirajapinnan v2.0. Nämä sivut sisältävät muutamia kenttiä, jotka perustuvat [AL Enum -objekteihin](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Kentillä, jotka perustuvat AL Enum-objekteihin, on oltava yhdenmukaiset ja aina samat nimet. Tällöin raporttien suodattimet toimivat aina &mdash; kielestä ja käyttöjärjestelmästä huolimatta. Tästä syystä AL Enum -objekteihin perustuvia kenttiä ei käännetä. Ne myös koodataan, jotta vältetään erikoismerkit, myös välilyönti. Erityisesti jos AL Enum -objektissa on tyhjä vaihtoehto, se arvoksi koodataan _x0020_. Voit pyytää aina Power BI:n tietojen muunnosta, jos haluat näyttää näissä kentissä eri arvoja, esimerkiksi Tyhjä-arvon.


---

## <a name="see-also"></a>Katso myös

[Power BI:n käyttöoikeudet](admin-powerbi-setup.md#license)
[Business Centralin ja Power BI:n esittely](admin-powerbi.md)  
[Power BI:n integroinnin yleiskatsaus](admin-powerbi-overview.md)  
[Power BI:n käyttöönotto Business Centralissa](admin-powerbi-setup.md)  
[Power BI -raporttien käyttäminen Business Centralissa](across-working-with-powerbi.md)  
[Business Centralin tietojen käyttäminen Power BI:ssa](across-working-with-business-central-in-powerbi.md)  
[Power BI -raporttien luominen Business Centralin tietojen näyttämiseksi](across-how-use-financials-data-source-powerbi.md)    
[Power BI -dokumentaatio](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]