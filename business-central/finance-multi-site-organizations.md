---
title: 'Business Central kansainvälisille organisaatioille ja organisaatioille, joilla on useita toimipaikkoja | Microsoft Docs'
description: 'Business Central sisältää ominaisuuksia, jotka tukevat säteittäisen ryhmän liiketoimintamallia.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'hub-and-spoke, multi-site, headquarter, sites'
ms.date: 10/01/2020
ms.author: bholtorf
---

# <a name="business-central-for-multi-site-and-international-organizations"></a>Business Central kansainvälisille organisaatioille ja organisaatioille, joilla on useita toimipaikkoja
Organisaatiot, joilla on useita toimipaikkoja, käyttävät usein säteittäisen ryhmän mallia. Siinä pääyritys tai pääkonttori hallinnoi liiketoiminnan yleisiä toimintoja samalla, kun kukin toimipaikka toimii yksittäisenä, erillisenä yksikkönä. Alueet ovat usein maantieteellisesti jakautuneet ja niillä on erilaiset tiedon jakamisen tarpeet pääkonttorin yrityksen kanssa. Lisäksi toimipaikat eivät yleensä tarvitse kovin monimutkaisia toimintoja, eikä niillä ole resursseja ylläpitää suurta järjestelmää.

[!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa pienille ja keskisuurille yrityksille helppokäyttöisen ja edullisesti ylläpidettävän liiketoiminnan hallintaratkaisun.

Tässä artikkelissa kerrotaan joitakin tapoja, joilla [!INCLUDE[prod_short](includes/prod_short.md)] tukee säteittäisen ryhmän liiketoimintamallia.

## <a name="integrating-the-headquarter-company-and-the-sites"></a>Pääkonttorin yrityksen ja toimipaikkojen integroiminen

[!INCLUDE[prod_short](includes/prod_short.md)] voidaan integroida pääkonttorin yrityksen kirjanpitojärjestelmän kanssa samalla, kun eri toimipaikkojen tarpeet täytetään koosta, sijainnista ja toimialasta riippumatta.

Seuraava kaavio on esimerkki pääkonttorin yritykseen integroiduista eri toimipaikoista.

![Kaavion kuvaus luodaan automaattisesti.](media/multisite-headquarter-sites.png)

## <a name="meet-the-needs-of-domestic-and-international-sites"></a>Kansallisten ja kansainvälisten toimipaikkojen tarpeiden täyttäminen

Liiketoiminnan tarpeet toimipaikoissa eroavat usein toimialan, liiketoimintamenetelmien tai pääkonttorin yrityksen suhteen perusteella. [!INCLUDE[prod_short](includes/prod_short.md)] voidaan mukauttaa ja laajentaa helposti liiketoimintojen ja aluekohtaisten asetusten eri tyyppien perusteella. Microsoft AppSource sisältää Microsoftin ja kumppaneidemme useita sovelluksia. Kumppanit voivat nopeasti ottaa käyttöön tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] vain vähäisillä päivittäisten toimintojen keskeytyksillä.

[!INCLUDE[prod_short](includes/prod_short.md)] tukee kansainvälisten organisaatioiden aluekohtaisten asetusten lakisääteisiä vaatimuksia ja liiketoiminnan käytäntöjä.

* Online-versioissa on yli [40 lokalisoitua maaversiota](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json), jotka voi asentaa laajennuksina Microsoft AppSourcesta.  
* Paikallisten versioiden [maaversiot](/azure/architecture/solution-ideas/articles/business-central) ovat käytettävissä Microsoftin lokalisoimina versioina tai kumppanin lisäosien lokalisointeina.

Microsoftin kumppaneiden verkosto sisältää yli 4 000 kumppania maailmanlaajuisesti. Nämä tarjoavat paikallista asiantuntemusta.

| **Liiketoiminnan vaatimus** | **Miten Business Central tukee sitä** | **Lisätietoja** |
|-------------------------|-------------------------|-------------------------|
| Räätälöi järjestelmä liiketoimintaa vastaavaksi. | Nauti järjestelmästä, joka on suunniteltu alusta lähtien keskisuurille yrityksille. | [Yleiskuvaus](https://dynamics.microsoft.com/business-central/overview/) |
| Ota huomioon lakisääteiset vaatimukset ja paikalliset käytännöt. | Noudata paikallisia lakisääteisiä vaatimuksia ja liiketoiminnan käytäntöjä. | [Paikalliset toiminnot](about-localization.md) |
| Käytä useiden yritysten tietoja yhdeltä sivulta. | Voit käyttää Business Centralin yrityksen tietoja nopeasti organisaatiossa. | [Yritystoiminto](ui-extensions-company-hub.md) |
| Käsittele useita kieliä ja valuuttoja. | Usean kielen ja valuutan tuki auttaa paikallisten vaatimusten täyttämisessä. | [Usean kielen ominaisuudet](about-locale-language.md)<br></br>[Usean valuutan ominaisuudet](finance-how-setup-additional-currencies.md) |


## <a name="consolidate-financial-data"></a>Taloustietojen konsolidointi

Säteittäisen ryhmän liiketoimintamallin perusfasetti on pääkonttorin yrityksen ja toimipaikkojen kyky vaihtaa taloustietoja myös silloin, kun pääkonttorin yritys ja toimipaikat käyttävät eri järjestelmiä, kirjanpitorakenteita, kieliä ja valuuttoja.

| **Liiketoiminnan vaatimus** | **Miten Business Central tukee sitä** | **Lisätietoja** |
|-------------------------|-------------------------|-------------------------|
| Konsolidoi taloustiedot toimipaikoista. | Konsolidoi tilinpäätökset toimipaikoista yhteen liiketoimintayksikköön (yritykseen) siitä huolimatta, käytetäänkö niissä Business Centralia vai toista sovellusta. | [Usean yrityksen kirjanpitotietojen konsolidoiminen](finance-consolidated-company-reporting.md) |
| Integroi kirjanpitorakenteet. | Siirrä konsolidointitiedot eri kirjanpitorakenteista omaan järjestelmään. F&O:n sisäänrakennettu tiedostomuoto (käytettävissä aallossa 2, 2020) | [Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)<br></br>[Valmistele kirjanpitotilit konsolidointia varten](finance-consolidated-company-reporting-setup.md#glacc) |
| Käsittele tietoja useissa valuutoissa. | Auta varmistamaan, että tilipäätökset eri valuutoissa ovat tarkkoja ja että niissä käytetään oikeita vaihtokursseja. | [Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md) |

## <a name="share-business-insight-with-integrated-analytics"></a>Liiketoimintatietojen jakaminen integroitujen analyysien kanssa

Linjaa organisaation liiketoiminnan tavoitteet antamalla tietoja nykyisestä tilanteesta. Integroidut analyysit voivat auttaa ihmisiä perustamaan päätöksensä samoihin tosiasioihin.

| **Liiketoiminnan vaatimus** | **Miten Business Central tukee sitä** | **Lisätietoja** |
|-------------------------|-------------------------|-------------------------|
| Jaa tietoja sellaisten toimipaikkojen kanssa, joilla ei ole laajaa IT-tukea. | Luo KPI-luvut ja Power BI:n liiketoimintatietojen koontinäytöt tietojesi perusteella. | [Business Centralin tietojen käyttäminen Power BI:ssa](across-working-with-business-central-in-powerbi.md) |
| Kehitä mukautettuja talousraportteja. | Luo parametreihin perustuvia talousraportteja. | [Business Intelligence](bi.md) |
| Linjaa tosiasiat. | Luo, tarkastele ja jaa raportteja sisäisten ja ulkoisten sidosryhmien kanssa. | [Talousraportit](finance-reports.md) |
| Analysoi tietoja Excelissä. | Etsi tosiasioita ja tee vianmääritys ja ad hoc -analyyseja Microsoft Excelissä. | [Rahoituslaskelmien analysoiminen Excelissä](finance-analyze-excel.md) |


## <a name="exchange-data-using-apis-and-xmlports"></a>Tietojen vaihtaminen ohjelmointirajapintojen ja XMLport-objektien avulla

Ohjelmointirajapinnat ja XMLport-objektit yksinkertaistavat tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] esiintymien yhteyksien muodostamista. Tämä koskee myös kunkin toimipaikan mukautettujen esiintymiä.

| **Liiketoiminnan vaatimus** | **Miten Business Central tukee sitä** | **Lisätietoja** |
|-------------------------|-------------------------|-------------------------|
| Yhdistä mukautetut versiot toimipaikkojen ja pääkonttorin yrityksen välillä. | Ohjelmointirajapinnan sivut voivat näyttää entiteetin minkä tahansa esityksen, myös sen mukautukset. | [Business Centralin ohjelmointirajapintojen käyttöönotto](/dynamics-nav/enabling-apis-for-dynamics-nav) |
| Versiointi ja suojaus. | Ohjelmointirajapintojen käytössä on ODataV4, joka sisältää versionhallinnan, webhook-objektit ja muutosten seurannan. | [Tietosuoja ja tietoturva](/dynamics365/business-central/dev-itpro/security/security-and-protection) |
| Kirjaa ja tuo XML-asiakirjoja. | Codeunitia voidaan käyttää sitoutumattomana toimintoja, joka tukee XML-asiakirjojen kirjaamista ja käsittelemistä. XML-asiakirjojen käsittelemistä varten voidaan kohdistaa XMLport-objektit. Sitoutumattomat toiminnot voivat myös luoda XML- tai JSON-asiakirjoja. | [XMLport-objektit](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-object) |
| Helpota ylläpitoa sähköisen tiedonvaihdon avulla. | Sähköisen tietojenvaihdon ratkaisu voidaan lisätä integrointitasoksi pääkonttorin yrityksen ja toimipaikkojen välille. | [Tietojen vaihtokehys](across-about-the-data-exchange-framework.md) |
| Vaihda tietoja eri järjestelmien välillä. | Käytä XMLport-objekteja luodessasi XML-asiakirjoja, joita voidaan vuorostaan siirtää yhtä järjestelmää käyttävän pääkonttorin yrityksen ja Business Centralia käyttävien toimipaikkojen välillä. | [XMLport-yleiskuvaus](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-overview) |
| Orkestroi monimutkaista tietojenvaihtoa. | Käytä XMLport-objektien ja Business Centralin sekä Microsoft BizTalk Serverin yhdistelmää, jotta voit täyttää toimipaikkojen yksilölliset tarpeet.</br>Voit täyttää vaativat tarpeet käyttämällä Business Centralin BizTalk Server- ja Commerce Gateway -ratkaisuihin perustuvaa sähköistä tietojenvaihdon ratkaisua yhdessä XMLport-objektien kanssa. | [Raporttien, eräajojen ja XMLportien käsitteleminen](ui-work-report.md) |
| Muodosta yhteys kolmannen<sup></sup> osapuolen ratkaisuihin ja palveluihin. | Ohjelmointirajapinnat muodostavat pisteestä pisteeseen -yhteyden Business Centralin ja kolmannen <sup></sup>  osapuolen ratkaisujen ja palveluiden välille. | [Ohjelmointirajapinta v2.0](/dynamics-nav/api-reference/v2.0/) |


## <a name="promote-an-efficient-intercompany-supply-chain"></a>Konsernin tehokkaan toimitusketjun määrittäminen

Toimipaikoissa tarvitaan usein toimitusketjun käyttöoikeus sekä oikeus hallinnoida sen tiettyjä osia. Toimipaikat voivat esimerkiksi käyttää samaa toimittajaa, mutta hallinnoida resursseja ja fyysisiä sijainteja erikseen.

| **Liiketoiminnan vaatimus** | **Miten Business Central tukee sitä** | **Lisätietoja** |
|-------------------------|-------------------------|-------------------------|
| Käsittele osastojen välisiä tapahtumia tavallisina myynti- ja ostotapahtumina. | Käytä konsernin kirjauksia luodessasi myynti- ja ostoasiakirjoja ja pääkirjanpidon tapahtumia koko työnkuluille ja useammille kuin yhdelle yritykselle kerralla, jotta voidaan välttää tietojen tallentamisen kaksoiskappaleet. | [Konsernitapahtumien hallinta](intercompany-manage.md) |
| Käytä paperittomia prosesseja. | Vältä asiakirjojen lähettämisen, vastaanottamisen ja tulostamisen kustannukset. | [Saapuvat asiakirjat](across-income-documents.md)<br><br> [Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta](ui-how-add-link-to-record.md) |

## <a name="respond-quickly-to-new-business-conditions"></a>Nopea reagoiminen liiketoiminnan uusiin olosuhteisiin

Pääkonttorin yrityksen on reagoitava nopeasti liiketoiminnan muutoksiin kussakin toimipaikassa. [!INCLUDE[prod_short](includes/prod_short.md)] voi toimia ennakoivana varoitusmekanismina yhdessä Power Automaten kanssa.

![Yhteisöpalveluiden viestin automaattisesti luodun kuvauksen näyttökuva.](media/multisite-apps.png)

| **Liiketoiminnan vaatimus** | **Miten Business Central tukee sitä** | **Lisätietoja** |
|-------------------------|-------------------------|-------------------------|
| Luo sähköposti-ilmoituksia automaattisesti. | Määritä hälytykset Power Automatessa niin, että saat sähköposti-ilmoitukset kriittisistä liiketoiminnan olosuhteista toimipaikoissa tai toimitusketjun kumppaneilla. | [Business Central ja Power BI](admin-powerbi.md) |
| Käytä vakiohälytyksiä tai mukautettuja hälytyksiä. | Käytä Business Centralin 12 erilaista mallia tai määritä omat hälytykset liiketoiminnan vaatimusten mukaan. | [Business Centralin käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md) |

## <a name="see-also"></a>Katso myös
[Business Central Onlinen hallintatehtävät](/dynamics365/business-central/dev-itpro/administration/tenant-administration)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
