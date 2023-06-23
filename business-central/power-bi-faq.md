---
title: Power BI – usein kysytyt kysymykset
description: 'Hanki vastauksia joihinkin tyypillisiin kysymyksiin, jotka liittyvät Power BI:n ja Business Centralin käyttöön.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power BI, reports, faq, errors'
ms.date: 04/22/2021
ms.author: jswymer
---
# <a name="power-bi--faq" />Power BI – usein kysytyt kysymykset

Tässä artikkelissa vastataan joihinkin kysymyksiin, joita sinulla voi olla, kun käytössä on Power BI ja [!INCLUDE [prod_short](includes/prod_short.md)].

## [Yleiset](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes" />Olen valinnut raportin Business Centralin omalle roolikeskukselle. Jos myöhemmin teen muutoksia raportin visualisointeihin, päivittääkö roolikeskus muutokset automaattisesti?

Kyllä, koska raportit on upotettu Power BI:stä.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english" />Ovatko Power BI:n Business Central -sovellukset saatavilla muilla kielillä kuin englanniksi?

Ei. Nämä sovellukset ovat tällä hetkellä saatavilla vain englanniksi.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix" />Kun raportti on julkaistu oma powerbi.com -työtilassa, voinko ladata sen pbix-tiedoston?

Kyllä. Lisätietoja on kohdassa [Raportin lataaminen Power BI -palvelusta Power BI Desktopiin](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files" />Voinko ladata sovellukset pbix-tiedostoina?

Ei. Tällä hetkellä emme toimita virallisille Power BI -sovelluksille ladattavia pbix-tiedostoja, koska ne julkaistaan AppSourcessa.

## [Käyttöoikeus](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports" />Tarvitsenko Power BI Pro -käyttöoikeuden raporttien julkaisemisessa?

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Ei. Pro-käyttöoikeutta ei tarvita raporttien julkaisemisessa. Power BI -vakiokäyttöoikeus (ilmainen) riittää. Lisätietoja on kohdassa [Power BI:n käyttöoikeudet](admin-powerbi-setup.md#license).

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license" />Mitä ilmaisen käyttöoikeuden omaava käyttäjä ei voi tehdä?

Et voi jakaa raportteja tai asentaa Power BI:n Business Central -sovelluksia. Muuten ilmainen käyttöoikeus mahdollistaa lähes kaikkien kaavio- ja raporttivaihtoehtojen luomisen.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license" />Jos käyttäjä jakaa raportin toisen käyttäjän kanssa, myös toisella käyttäjällä on oltava Pro-käyttöoikeus nähdäkseen raportin. Tuleeko tämä ominaisuus tulevaisuudessa käyttöön ilmaisen käyttöoikeuden kanssa?

Emme voi tehdä tätä päätöstä. Sen tekee Power BI. Lisätietoja on kohdassa [Power BI -koontinäyttöjen ja -raporttien jakaminen työtovereiden ja muiden käyttäjien kanssa](/power-bi/collaborate-share/service-share-dashboards).  

## [Suunnitteluohjelma](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages" />Toimiiko yhdistin ohjelmointirajapinnan sivujen kanssa?

Kyllä. Vuoden 2021 kesäkuun jälkeen uusi Power BI -yhdistin tukee sekä Business Centralin verkkosivuja että ohjelmointirajapinnan sivuja. Lisätietoja on kohdassa [Power BI -yhdistimen käytön aloittaminen yhdessä Business Centralin ohjelmointirajapintojen kanssa pelkkien verkkopalveluiden sijaan](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### <a name="can-i-build-a-power-bi-report-using-the-sales-invoice-lines-or-journal-lines-apis" />Voinko luoda Power BI -raportin käyttämällä myyntilaskurivejä tai päiväkirjan rivien ohjelmointirajapintoja?

Yleisimmin käytetyt rivitietueet ovat käytettävissä [Business Central APIs v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/):ssa). Voit siis käyttää niitä raporttien rakentamiseen Power BI:ssä valitsemalla ne **Dynamics 365 Business Central** -yhdistimessä. **Rivit**-ohjelmointirajapinnat on kuitenkin suunniteltu käytettäviksi vain joidenkin erityisten suodattimien kanssa, eivätkä ne välttämättä toimi kaikissa skenaarioissa. Saatat saada virheen kuten "Sinun on määritettävä tunnus tai asiakirjatunnus saadaksesi rivit". Voit korjata tämän ongelman seuraavasti, kun saat Business Centralista Power BI Desktop -raportin tiedot:

1. Sen sijaan, että lisäisit rivientiteetin tietolähteen, lisää päätietolähde. Lisää esimerkiksi **Myyntilasku** sen sijaan, että lisäisit **Myyntilaskun rivit**.
2. Valitse **Muunna tiedot** Power BI Desktopin toimintopalkista.
3. Valitse juuri lisätty kysely, esimerkiksi **Myyntilaskut**.
4. Vähennä raporttiin ladattujen tietueiden määrää suodattamalla tietueita.
5. Vieritä oikealle, kunnes löydät riveiksi nimetyn sarakkeen, esimerkiksi **SalesInvoiceLines**.
6. Valitse laajennuspainike sarakkeen otsikossa, sarakenimen vieressä.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Näyttää SalesInvoiceLines-sarakkeen Power BI Desktopissa.":::
<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment" />Onko mahdollista valita Business Central -ympäristö, josta tiedot haetaan Power BI:iin, esimerkiksi eristys- tai tuotantoympäristö?

Kyllä. Tämän voi valita helposti. Kun yhteys Business Centraliin muodostetaan yhdistimen avulla, on valittava ympäristö ja yrityksen nimi.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant" />Voiko useiden tuotantoympäristöjen tietoja yhdistää samaan vuokraajaan?

Kyllä. Power BI:ssä suoritetaan uudelleen toiminto tietojen hakemiseksi ja haetaan haluttu ympäristö.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part" />Millä Business Centralin sivuilla on Power BI -raportit -osa?

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
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards" />Voinko suodattaa Business Centralin tietojoukon *ennen* kuin haen tiedot Power BI:iin sen sijaan, että käytän suodattimia jälkikäteen?

Jos haluat suodattaa suuria tietojoukkoja, helpoin tapa on määrittää Power BI -raportin suodatin muokkaamalla suoraan Power Query -kaavaa. Suurin osa näin määritetyistä suodattimista välitetään Business Centraliin delegoimalla kysely lähteeseen. Katso [Tietojoukkojen lisäävä päivitys](/power-bi/admin/service-premium-incremental-refresh).

Tällä hetkellä ei ole mahdollista määrittää verkkopalveluiden tietojen suodatinta Business Centralissa. Jos sovelluksen on määritettävä suodatin Business Centralissa, sinun on luotava tätä varten mukautettu Business Central -sovellus.

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table" />Voiko Power BI:ssa hakea tietoja kyselyn lisäksi myös muilla tavoilla sellaista Business Centralin taulukoista, joilla ei ole liitettyä sivua? Esimerkiksi *Nimikemääritteen arvon yhdistämismääritys* -taulukosta.

Ei. Ei vielä.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages" />Ovatko julkaistavat kyselyt nopeampia käyttää kuin julkaistut sivut?

Verkkopalveluissa julkaistut kyselyt ovat yleensä nopeampia kuin vastaavat julkaistut sivut. Syy on se, että kyselyt on optimoitu tietojen lukemista varten. Ne eivät sisällä kalliita käynnistimiä, kuten OnAfterGetRecord-käynnistintä.

Verkkopalvelut perustuvat sivuihin tai kyselyihin, jotka on suunniteltu käytettäväksi verkosta käsin eikä yleensä optimoitu käytettäväksi ulkoisten palvelujen kautta. Vaikka Business Central -yhdistin tukee edelleen tietojen hakemista verkkopalveluista, suosittelemme käyttämään ohjelmistorajapintasivuja verkkopalvelujen sijaan aina, kun se on mahdollista.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-the-developer-have-to-create-a-custom-query" />Voiko käyttäjä luoda verkkopalvelun sellaisen sarakkeen avulla, joka on Business Centralin taulukossa, mutta ei sivulla? Vai onko kehittäjän luotava mukautettu kysely?

Verkkopalveluun ei tällä hetkellä pysty lisäämään uutta kenttää. Ohjelmointirajapintasivut tarjoavat täyden joustavuuden sivun rakenteen osalta, joten kehittäjä voi luoda uuden ohjelmistorajapintasivun tämän vaatimuksen täyttämiseksi. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online" />Voinko yhdistää Power BI:n Business Central Onlinen vain luku -tilassa olevaan tietokantapalvelimeen?

Tämä toiminto on saatavilla pian. Helmikuusta 2022 lähtien uudet Business Central Online -tietojen perusteella luotavat raportit yrittävät automaattisesti muodostaa yhteyden vain luku -tyyppiseen tietokantareplikaan. Tämän ansiosta raportit päivittyvät nopeammin ja ne vaikuttavat suorituskykyyn vähemmän, jos käytät Business Centralia, kun raporttia päivitetään. Suosittelemme edelleen, että raportit ajastetaan päivittymään tavanomaisten työtuntien ulkopuolella aina, kun se on mahdollista.

Jos sinulla on vanhoja Business Central -tietoihin perustuvia raportteja, ne eivät muodosta yhteyttä vain luku -tyyppisiin tietokantareplikoihin.

### <a name="a-namedatabasemodsaive-tried-the-preview-of-the-new-connector-for-the-february-2022-update-when-i-connect-to-my-custom-business-central-api-page-i-get-the-error-cannot-insert-a-record-current-connection-intent-is-read-only-how-can-i-fix-it" /><a name="databasemods"></a>Olen kokeillut helmikuun 2022 päivityksen uuden yhdistimen esikatselua. Kun muodostan yhteyden mukautettuun Business Central -ohjelmointirajapintasivuun, näkyviin tulee virhe Tietuetta ei voi lisätä. Nykyinen yhteystarkoitus on vain luku -muodossa.". Miten voin korjata asian?

Uuden yhdistimen myötä uudet Business Central -tietoja käyttävät raportit muodostavat oletusarvoisesti yhteyden Business Central -tietokannan replikaan. Tämä muutos parantaa suorituskykyä. Joissakin harvoissa tapauksissa se voi kuitenkin aiheuttaa virheen. Tämä virhe johtuu yleensä siitä, että mukautettu ohjelmointirajapinta tekee muutoksia Business Central -tietueisiin, kun Power BI yrittää noutaa kyseisiä tietoja. Erityisesti virhettä esiintyy osana AL-käynnistimiä: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord ja OnAfterGetCurrRecord.

Katso ohjeet tämän ongelman korjaamiseen pakottamalla Business Central -yhdistimen sallimaan tämän toiminnan: [Power BI -raporttien koostaminen näyttämään Business Central -tietoja – Ongelmien korjaaminen](across-how-use-financials-data-source-powerbi.md#fixing-problems).

<!--
In general, we recommend avoiding any database modifications in API pages when they're opening or loading records, because they cause performance issues and might cause your report refresh to fail. In some cases, you might still need to make a database modification when your custom API page opens or loads records. You can force the Business Central connector to allow this behavior. Do the following steps when getting data from Business Central for the report in Power BI Desktop:

1. Start Power BI Desktop.
2. In the ribbon, select **Get Data** > **Online Services**.
3. In the **Online Services** pane, select **Dynamics 365 Business Central**, then **Connect**.
4. In the **Navigator** window, select the API endpoint that you want to load data from.
5. In the preview pane on the right, you'll see the following error:

   *Dynamics365BusinessCentral: Request failed: The remote server returned an error: (400) Bad Request. (Cannot insert a record. Current connection intent is Read-Only. CorrelationId: [...])".*

6.  Select **Transform Data** instead of **Load** as you might normally do.
7. In **Power Query Editor**, select **Advanced Editor** from the ribbon.
8.  Replace the following line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null),
   ```

   with the line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false]),
   ```

9.  Select **Done**.
10. Select **Close & Apply** from the ribbon to save the changes and close Power Query Editor.

-->
### <a name="a-namepermsahow-do-i-change-or-clear-the-user-account-im-currently-using-to-connect-to-business-central-from-power-bi-desktop" /><a name="perms"></a>Miten muutan tai tyhjennän käyttäjän, jota tällä hetkellä käytän yhteyden muodostamiseen Business Centraliin Power BI Desktopista?

Tee Power BI Desktopissa seuraavat vaiheet:

1. Valitse Tiedosto-valikossa **Asetukset ja vaihtoehdot** > **Tietolähteen asetukset**.
2. Valitse luettelosta **Dynamics Business Central** ja valitse sitten **Tyhjennä käyttöoikeudet** > **Poista**.

Kun seuraavan kerran muodostat yhteyden Business Centraliin tietojen saamiseksi, sinua pyydetään kirjautumaan sisään.

## [Suoritustaso](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services" />Onko nopeampaa hakea tiedot ohjelmointirajapinnan sivujen kuin verkkopalveluiden avulla?

Kyllä. Testimme osoittavat, että ohjelmointirajapinnan sivujen suorituskyky on 25 % parempi kuin verkkopalveluiden.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly" />Onko suunnitelmissa määrittää Azure SQL Database -esiintymään peili, johon voin muodostaa yhteyden suoraan?

Ei. Ei vielä. Voit olla yhteydessä vain Business Centralin ohjelmointirajapintojen avulla.

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table" />Tietojen lataaminen Business Centralin verkkopalveluista vaikuttaa hitaalta. Voiko tiedot hakea suoraan SQL-tietokantataulukosta jollakin tavalla?

Ei. Suora pääsy tietokantaan ei ole mahdollinen. Mutta siirtyminen ohjelmointirajapinnan sivuihin (kun uusi yhdistin ei ole käytettävissä) auttaa paljon.

## [Lisäasetukset](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service" />Tuleeko Power BI:n yhdistin tukemaan lisääviä päivitystoimintoja Power BI -palvelussa tulevaisuudessa?

Kyllä. Se on toteutussuunnitelmamme.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi" />Jos Business Central on-premises ratkaisussa ei ole internet-yhteyttä, voinko silti käyttää Power BI:tä?
<!-- todo: please explain this one-->

Kyllä. Tässä tapauksessa voit käyttää Power BI Desktopia paikallisesti ja muodostaa yhteyden Business Central on-premises -ratkaisuun. Kun yhteys on muodostettu, voit luoda ja tarkastella raportteja. Ainoa mitä et voi tehdä, on julkaista niitä Power BI -palvelussa. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services" />Voiko tulevaisuudessa replikoida Business Central Online -tietokannat niin, että niitä voi käyttää vain luku -tilassa olevissa SQL-kyselyissä? Tämä ominaisuus tukisi lisäävää päivitystä. Se on paljon nopeampi kuin ohjelmointirajapinnat ja verkkopalvelut.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Kyllä. Tämä toiminto on pitkän aikavälin toteutussuunnitelmassamme. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance" />Parantaako suorituskykyä se, että käytän Azure Data Factorya tietojen hankkimiseksi Business Centralista ja kulutan tiedot Power BI:ssä?

Kyllä. Tämä lisäskenaario auttaa Business Centralia pysymään suorituskykyisenä, koska tietojen käyttöoikeus määritetään Azure Data Factoryn kautta.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center" />Onko suunnitelmissa tukea Power BI:n käyttöönottoputkia tai PBI-raporttien käyttöönottoputkien luomista samalla tavalla kuin laajennuksissa? Tai jopa määrittää yksinkertainen ohjelmointirajapinta Business Admin Centeriin?

Tutkimme tätä ominaisuutta. Power BI sisältää monipuolisia ohjelmointirajapintoja raportin käyttöönottojen hallintaa varten. Lisätietoja on kohdassa [Käyttöönottoputkien esittely](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="when-i-get-data-from-business-central-to-use-in-my-power-bi-reports-i-see-some-values-like-x0020-what-are-these-values" />Kun noudan tietoja Business Centralista käytettäväksi Power BI -raporteissa, näkyviin tulee tämänkaltaisia arvoja: _x0020_. Mitä nämä arvot ovat?

Jotkut ohjelmointirajapintasivut, kuten useimmat API v2.0 -sivut, sisältävät [AL Enum -objekteihin](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums) perustuvia kenttiä. Kentillä, jotka perustuvat AL enum -objekteihin, on oltava yhdenmukaiset ja aina samat nimet. Tällöin raporttien suodattimet toimivat aina &mdash; kielestä ja käyttöjärjestelmästä huolimatta. Tästä syystä AL enum -objekteihin perustuvia kenttiä ei käännetä. Ne myös koodataan, jotta vältetään erikoismerkit, myös välilyönti. Erityisesti jos AL Enum -objektissa on tyhjä vaihtoehto, se arvoksi koodataan _x0020_. Voit pyytää aina Power BI:n tietojen muunnosta, jos haluat näyttää näissä kentissä eri arvoja, esimerkiksi Tyhjä-arvon.


---

## <a name="see-related-microsoft-trainingtrainingmoduleschange-documents-dynamics-365-business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/change-documents-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Power BI:n käyttöoikeudet](admin-powerbi-setup.md#license)  
[Johdatus Business Centraliin ja Power BI:hin](admin-powerbi.md)  
[Power BI:n integroinnin yleiskatsaus](admin-powerbi-overview.md)  
[Power BI:n käyttöönotto Business Centralissa](admin-powerbi-setup.md)  
[Power BI -raporttien käyttäminen Business Centralissa](across-working-with-powerbi.md)  
[Business Centralin tietojen käyttäminen Power BI:ssa](across-working-with-business-central-in-powerbi.md)  
[Power BI -raporttien luominen Business Centralin tietojen näyttämiseksi](across-how-use-financials-data-source-powerbi.md)  
[Power BI -dokumentaatio](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
