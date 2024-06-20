---
title: 'Business Central -sovellusten käyttäminen Power BI:ssa'
description: 'Analyysitietojen, liiketoimintatietojen ja tunnuslukujen hakeminen Business Centralin tiedoista on helppoa Power BI:n Business Central -sovelluksia.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 09/07/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="use-the--apps-in-power-bi"></a>[!INCLUDE [prod_short](includes/prod_short.md)] -sovellusten käyttäminen Power BI:ssa

> **KOHDE:** [!INCLUDE [prod_long](includes/prod_long.md)] online 

[!INCLUDE [prod_long](includes/prod_long.md)] julkaisee seuraavat Power BI -sovellukset, joilla saadaan yksityiskohtaiset koontinäytöt tietojen tarkastelua varten:

- [!INCLUDE [prod_long](includes/prod_long.md)] – CRM  
- [!INCLUDE [prod_long](includes/prod_long.md)] – Finance  
- [!INCLUDE [prod_long](includes/prod_long.md)] – Sales

## <a name="overview"></a>Yleiskuvaus

Kussakin sovelluksessa on useita raportteja, joihin voi porautua tarkastelemaan tietoja esimerkiksi seuraavasti:

- Valitse koontinäytöstä jokin visuaalinen kohde, kun haluat käsitellä jotakin perustana olevasta raportista.  
- Suodata raportti tai lisää seurattavia kenttiä.  
- Kiinnitä mukautettu näkymä koontinäyttöön, kun haluat jatkaa seuraamista.  
  Voit päivittää tiedot manuaalisesti ja määrittää päivitysaikataulun. Lisätietoja on kohdassa [Aikataulutetun päivityksen määrittäminen](/power-bi/refresh-scheduled-refresh).  

Sovellukset on suunniteltu käyttämään kaikkien [!INCLUDE[prod_short](includes/prod_short.md)]in yritysten tietoja. Power BI -sovelluksen asennuksen yhteydessä määritetään parametrit, joilla muodostetaan yhteys [!INCLUDE [prod_short](includes/prod_short.md)] -ratkaisuun.  

> [!NOTE]
> Voit myös luoda omia raportteja ja koontinäyttöjä Power BI:ssä [!INCLUDE[prod_short](includes/prod_short.md)]in tietojen perusteella. Lisätietoja on kohdassa [Liiketoimintatietojen yhdistäminen Power BI:hin](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Vaatimukset

Power BI -sovellukset tarvitsevat niiden taulukoiden käyttöoikeudet, joista tiedot noudetaan, ja tietojen noutamiseen käytettävät verkkopalvelut. Seuraavassa taulukossa on luettelo kunkin Power BI -sovelluksen tarvitsemista verkkopalveluista:
    
|Sovellus|Verkkopalvelut |
|--|-------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] – CRM| <ul><li>Myyntimahdollisuudet</li><li>Excel-malli Näytä yrityksen tiedot</li><li>Power BI -raporttien selitteet</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – rahoitus| <ul><li>PowerBIFinance</li><li>Excel-malli Näytä yrityksen tiedot</li><li>Power BI -raporttien selitteet</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – myynti| <ul><li>Asiakaskohtainen nimikemyynti</li><li>Myynnin koontinäyttö</li><li>Excel-malli Näytä yrityksen tiedot</li><li>Power BI -raporttien selitteet</li></ul>|

> [!TIP] 
> Verkkopalveluja voi etsiä kätevästi hakemalla *verkkopalveluja* [!INCLUDE[prod_short](includes/prod_short.md)]issa. Varmista **Verkkopalvelut**-sivulla, että **Julkaisu**-kenttä on valittuna edellä mainituissa verkkopalveluissa. Lisätietoja on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

## <a name="get-ready"></a>Valmistelut

Rekisteröidy Power BI -palveluun. Jos et ole vielä rekisteröitynyt, siirry osoitteeseen [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Käytä rekisteröityessä työpaikan sähköpostiosoitetta ja salasanaa.

## <a name="install-a--app-in-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] -asentaminen Power BI:ssa

1. Avaa selain, siirry sivustoon [https://powerbi.microsoft.com](https://powerbi.microsoft.com) ja kirjaudu tilille.
2. Valitse siirtymisruudussa **Sovellukset**.
    
    **Sovellukset**-sivu avautuu.

3. Valitse **Sovellukset**-sivulta **Hae sovellukset** sivun oikeasta yläkulmasta.
    
    Avautuvalla **Power BI -sovellukset** -sivulla voit selata kohteelle [!INCLUDE[prod_short](includes/prod_short.md)] käytettävissä olevia sovelluksia.

    ![Siirtyminen sovelluksia noudettaessa.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

> [!TIP] 
> Voit käyttää **Power BI -raporttia** myös kohteesta [!INCLUDE [prod_short](includes/prod_short.md)]. Siirry Power BI -raportit -osaan ja **valitse raportit** aloitussivulla. Valitse **Hae raportit** -kohdasta Joko **Palvelut** tai **Oma organisaatio**. Näkyviin tulee organisaatiogalleria Power BI:ssa tai Microsoft AppSourcessa, ja näkyvissä ovat vain kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)] liittyvät sovellukset.

5. Kirjoita **Haku**-ruutuun **Dynamics 365 Business Central**.
6. Valitse ensin käytettävä sovellus, sitten **Hae se nyt** ja lopuksi **Asenna**.  

    Tämän jälkeen sovellus on käytettävissä Power BI:n siirtymisvalikon **Sovellukset**-kohdassa.

## <a name="connect-the--app-to-your-data"></a>[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen yhdistäminen tietoihin

1. Valitse **Sovellukset**-kohdassa ensin Business Central -sovellus ja sitten **Yhdistä**.
2. Lisää pyydettäessä **Yrityksen nimi**- ja **Ympäristö**-kohtiin sitä [!INCLUDE[prod_short](includes/prod_short.md)] -esiintymää koskevat tiedot, johon haluat muodostaa yhteyden.

    - Varmista, että **Yrityksen nimi** -kohdassa on yrityksen koko nimi eikä näyttönimi. Yrityksen nimen voi tarkistaa [!INCLUDE[prod_short](includes/prod_short.md)] in **Yritykset**-sivulta. 
    - Anna **Ympäristö**-kohdassa **Tuotanto**, jos et ole luonut useita ympäristöjä.

3. Valitse **Seuraava**.
4. Valitse **Kirjaudu sisään**.
5. Anna pyydettäessä käyttäjänimi ja salasana, jolla kirjaudutaan [!INCLUDE[prod_short](includes/prod_short.md)]iin.
6. Kun yhteys on muodostettu, koontinäyttö ja raportit lisätään Power BI -työtilaan. Kun tämä on tehty, ruudut näyttävä [!INCLUDE[prod_short](includes/prod_short.md)] -yrityksen tiedot.

    ![Valitse Dynamics 365 Business Central ja valitse Hanki se nyt.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="fixing-problems"></a>Ongelmien korjaaminen

Power BI -koontinäytön toiminta perustuu edellä lueteltuihin julkaistuihin verkkopalveluihin. Siinä on tietoja esittely-yrityksestä tai omasta yrityksestä, jos tuot tietoja nykyisestä rahoitusratkaisusta. Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.  

### <a name="you-dont-have-a-power-bi-account"></a>Power BI -tiliä ei ole

Power BI -tiliä ei ole määritetty. Kelvollinen Power BI -tili edellyttää käyttöoikeutta. Lisäksi on oltava kirjautuneena sisään Power BI:hiin Power BI -työtilan luontia varten.  

### <a name="message-there-are-no-enabled-reports-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Sanoma: Käyttöönotettuja raportteja ei ole. Valitse raportti ja saat näkyviin luettelon raporteista, joita voit tarkastella.

Tämä sanoma avautuu, jos oletusraporttia ei voitu ottaa käyttöön Power BI -työtilassa. Vaihtoehtoisesti raportti otettiin käyttöön mutta sen päivittäminen ei onnistunut. Jos tämä ongelma esiintyy, siirry raporttiin Power BI -työtilassa, valitse **Tietojoukko**, **Asetukset** ja päivitä tunnistetiedot sitten manuaalisesti. Kun tietojoukko on päivitetty, siirry takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin ja valitse raportti manuaalisesti **Valitse raportit** -sivulla.

### <a name="you-need-a-power-bi-pro-license-to-install-the--app-in-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen asentaminen Power BI:ihin edellyttää Power BI Pro -käyttöoikeutta.

Tarvitse sisällön jakamiseen [Power BI Pro -käyttöoikeuden](/power-bi/service-features-license-type), joka on oltava myös henkilöillä, joiden kanssa sisältö jaetaan. Sisällön on oltava työtilassa [Premium-kapasiteettina](/power-bi/service-premium-what-is). Lisätietoja on kohdassa [Työn jakaminen Power BI:ssä](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>Parametrin tarkistus epäonnistui. Varmista, että kaikki parametrit ovat sallittuja.

Tämä virhe ilmaisee, että vähintään yksi parametreista on virheellinen.

- Määritetty ympäristöparametri ei vastaa mitään aiemmin luotua [!INCLUDE[prod_short](includes/prod_short.md)]in tuotanto- tai eritysympäristöä.
- Määritys yritysparametri ei vastaa mitään aiemmin luotua [!INCLUDE[prod_short](includes/prod_short.md)] -yritystä. Tarkista yrityksen nimi [!INCLUDE[prod_short](includes/prod_short.md)]in **Yritykset**-sivulla.
- URL-osoite, joka annettiin muodostettaessa yhteyttä paikalliseen [!INCLUDE[prod_short](includes/prod_short.md)] -versioon, ei kelpaa. Voit tarkistaa URL-osoitteen [!INCLUDE[prod_short](includes/prod_short.md)]in **Verkkopalvelut**-sivulla  
- Porttia ei ole avattu, joten pyyntö ei läpäise palomuuria.

### <a name="cant-sign-in"></a>Sisäänkirjautuminen ei onnistu

Jos näyttöön tulee sisäänkirjautumisen epäonnistumista ilmoittava virhe sen jälkeen, kun kirjauduit käyttäjän [!INCLUDE[prod_short](includes/prod_short.md)] -tunnistetiedoilla, syynä on luultavasti jokin seuraavista:

- Käytetyllä tilillä ei ole [!INCLUDE[prod_short](includes/prod_short.md)]in tietojen nouto-oikeuksia. Tarkista, että sinulla on tarvittavien [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen oikeudet ja yritä uudelleen.
- Olet valinnut jonkin muun kuin perustason todennustyypin, jos yhteys on muodostettu paikalliseen [!INCLUDE[prod_short](includes/prod_short.md)] -versioon.
- Et ole antanut oikeaa käyttäjänimeä tai salasanaa.

### <a name="message-your-data-source-cant-be-refreshed-because-the-credentials-are-invalid-please-update-your-credentials-and-try-again"></a>Sanoma: Tietolähdettäsi ei voi päivittää, koska tunnistetiedot ovat virheelliset. Päivitä tunnistetietosi ja yritä uudelleen.

Paikallisessa [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa ongelmana voi olla se, että OData-URL-osoite näkyy vain paikallisessa verkossa.

### <a name="incorrect-company-name"></a>Virheellinen yrityksen nimi

Yleinen virhe on antaa yrityksen näyttönimi yrityksen nimen sijaan. Voit etsiä yrityksen nimen hakusanalla **Yritykset**. Anna sitten yrityksen nimi **Nimi**-kentässä.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Avain ei vastannut mitään taulukon riviä

Jos annat yhteydenmuodostusprosessin aikana yrityksen nimen, joka ei ole sallittu, näyttöön voi avautua virhesanoma, jonka mukaan avain ei vastannut mitään taulukon riviä. Anna oikea yrityksen nimi ja yritä muodostaa yhteys uudelleen.

### <a name="historical-data-appears-to-be-missing"></a>Historiatietoja näyttää puuttuvan

Kun Power BI -sovellus asentuu ja tiedot näkyvät Power BI:ssa, kaikki tiedot eivät ole näkyvissä. Tietojoukot suodatetaan palauttamaan vain viimeisen 365 päivän tiedot. Tämä oletus on käytössä raporttien nopeuttamiseksi.  

### <a name="i-only-see-data-for-a-single-company"></a>Vain yhden yrityksen tiedot näkyvät

Power BI -sovellus näyttää vain sen [!INCLUDE[prod_short](includes/prod_short.md)] -yrityksen tiedot, joka määritettiin Power BI -sovelluksen asennuksen yhteydessä. Muiden yrityksen tietoja voidaan lisätä raporttiin lisäämällä uusi kyselyjä, jotka käyttävät eri yrityksiä tietolähteenä.  

### <a name="what-now"></a>Mitä seuraavaksi?

- Kokeile [kysymyksen kirjoittamista kysymys- ja vastausruutuun](/power-bi/service-q-and-a-tips) koontinäytön yläreunassa.
- [Vaihda ruutuja](/power-bi/service-dashboard-edit-tile) koontinäytössä.  
- [Avaa taustalla oleva raportti valitsemalla ruutu](/power-bi/service-dashboard-tiles).  
- Tietojoukko ei oletusarvoisesti sisälly päivitykseen. Voit muuttaa päivitysaikataulua tai yrittää päivittämistä tarvittaessa **Päivitä nyt** -toiminnolla. Lisätietoja on kohdassa [Aikataulutetun päivityksen määrittäminen](/power-bi/refresh-scheduled-refresh).

## <a name="see-also"></a>Katso myös

[Business Central ja Power BI](admin-powerbi.md)  
[Power BI -integrointiosa ja [!INCLUDE[prod_short](includes/prod_short.md)] -arkkitehtuurin yleiskatsaus](admin-powerbi-overview.md)  
Yhdistä [Power BI:hin paikallisesta [!INCLUDE [prod_short](includes/prod_short.md)] -versiosta](across-working-with-business-central-in-powerbi.md)  
[Power BI -raporttien luominen näyttämään [!INCLUDE [prod_long](includes/prod_long.md)] -tietoja](across-how-use-financials-data-source-powerbi.md)  
[Business Intelligence](bi.md)  
[Liiketoimintaan valmistautuminen](ui-get-ready-business.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Määritä [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Apps:n tietolähteenä](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Automatessa](across-how-use-financials-data-source-flow.md)  
[Power BI -dokumentaatio](/power-bi/)  
[Power BIn kuvaus](/power-bi/fundamentals/power-bi-overview)  
[Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin](/power-bi/desktop-quickstart-connect-to-data)  
[Johdatus tietovarastoihin](/power-bi/transform-model/datamarts/datamarts-overview)  
[Tietovoiden ja itsepalvelutietojen valmistelun esittely](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
