---
title: Liiketoimintatietojen ottaminen käyttöön Power BI:ssä| Microsoft Docs
description: Analyysitietojen, liiketoimintatietojen ja tunnuslukujen hakeminen Business Centralin tiedoista on helppoa Power BI:n Business Central -sovelluksia.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 01/13/2020
ms.author: bmeier
ms.openlocfilehash: 1450db26598da2f2735df1979cfacc16034fcf3a
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2020
ms.locfileid: "2952985"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Yritystietojen ottaminen käyttöön Power BI:tä varten

Lisätietojen hakeminen [!INCLUDE[prodshort](includes/prodshort.md)] -tietoihin on helppoa [!INCLUDE[prodshort](includes/prodshort.md)]in Power BI -sovelluksilla. Power BI hakee tiedot ja muodostaa näiden tietojen perusteella valmiin koontinäytön ja raportit.  

Sinulla on oltava kelvollinen [!INCLUDE[prodshort](includes/prodshort.md)]- ja Power BI -tili. Lisäksi [Power BI Desktop](https://powerbi.microsoft.com/desktop/) on ladattava, jos haluat luoda oman Power BI -raportteja. Power BI -sovellusten käyttöä varten tarvitaan niiden taulukoiden käyttöoikeus, joista tiedot noudetaan. Lisätietoja on vaatimuksista on jäljempänä.  

> [!IMPORTANT]
> Tässä artikkelissa käsiteltävät Power BI -sovellukset on suunniteltu käyttämään Azure Active Directorya todennukseen ellei muuta ilmoiteta. Power BI -sovelluksen asentamiseen tarvitaan Power BI Pro -käyttöoikeus.  Power BI -sovellus on asennettu, se voidaan jakaa käyttäjille riippumatta siitä, millainen käyttöoikeus heillä on.

[!INCLUDE [prodlong](includes/prodlong.md)] on julkaissut seuraavat Power BI:n sovellukset:

- [!INCLUDE [prodlong](includes/prodlong.md)] – CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] – Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] – Sales  
- [!INCLUDE [prodlong](includes/prodlong.md)](paikallinen) – CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)](paikallinen) – Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)](paikallinen) – Sales  

## <a name="using-the-include-prodshortincludesprodshortmd-dashboards-in-power-bi"></a>[!INCLUDE [prodshort](includes/prodshort.md)] -koontinäyttöjen käyttäminen Power BI:ssä

Kussakin sovelluksessa on raportteja, joilla voi porautua tietoihin:

- Valitse koontinäytöstä jokin visuaalinen kohde, kun haluat käsitellä jotakin perustana olevasta raportista.  
- Suodata raportti tai lisää seurattavia kenttiä.  
- Kiinnitä tämä mukautettu näkymä koontinäyttöön, kun haluat jatkaa seuraamista.  
  Voit päivittää tiedot manuaalisesti ja määrittää päivitysaikataulun. Lisätietoja on kohdassa [Aikataulutetun päivityksen määrittäminen](/power-bi/refresh-scheduled-refresh).  

Sovelluksen on suunniteltu käyttämään kaikkien [!INCLUDE[prodshort](includes/prodshort.md)]issa olevien yritysten tietoja. Power BI -sovelluksen asennuksen yhteydessä määritetään parametrit, joilla muodostetaan yhteys [!INCLUDE [prodshort](includes/prodshort.md)] -ratkaisuun.  

> [!NOTE]
> Voit myös luoda omia raportteja ja koontinäyttöjä Power BI:ssä [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietojen perusteella. Lisätietoja on kohdassa [Liiketoimintatietojen yhdistäminen Power BI:hin](across-how-use-financials-data-source-powerbi.md).  

### <a name="to-connect-your-data-in-power-bi"></a>Tietojen yhdistäminen Power BI:hin

1. Avaa selain, siirry sivustoon https://powerbi.microsoft.com ja kirjaudu tilille.
2. Valitse **Nouda tiedot** vasemman siirtymisruudun alareunassa.  

    ![Siirtyminen tietoja noudettaessa](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Voit aloittaa käyttämisen myös [!INCLUDE [prodshort](includes/prodshort.md)]ista. Siirry aloitussivulla Power BI -osan **raporttivalintaan**. Valitse valintanauhassa joko **Palvelu** tai **Oma organisaatio**. Kun jompikumpi vaihtoehto valitaan, siirry joko Power BI:n organisaatiovalikoimaan tai Microsoft AppSourceen, joka voidaan myös suodattaa näyttämään vain [!INCLUDE[prodshort](includes/prodshort.md)]iin liittyvät sovellukset.

3. Valitse **Palvelut**-ruudussa **Hae**. Avautuvalla sivulla näkyy **AppSource** ja **Power BI -sovellukset**.  

<!--    ![Choose apps from online services that you use.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)-->
4. Valitse ensin **Sovellukset** **Power BI -sovellukset** -välilehdessä ja sitten käytettävä **Microsoft Dynamics 365 Business Central** -sovellus. Valitse lopuksi **Hae se nyt**.  
<!--    ![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packspowerbi-dynamics365-for-financials-get-it-now.png)/-->
5. Anna pyydettäessä sen ympäristön ja yrityksen nimi [!INCLUDE[prodshort](includes/prodshort.md)] -sovelluksessa, johon haluat yhdistää. Jos olet luonut useita ympäristöjä, anna **Tuotanto**. Varmista yrityksen parametrin osalta, että annat nimen etkä näyttönimeä. Yrityksen nimi on [!INCLUDE[prodshort](includes/prodshort.md)] -esiintymän **Yritykset**-sivulla.  

    > [!NOTE]
    > Jos yhdistää paikalliseen [!INCLUDE [prodshort](includes/prodshort.md)] -versioon, *Verkkopalvelun URL-osoite* -parametri on määritettävä. Se löytyy [!INCLUDE [prodshort](includes/prodshort.md)]in **Verkkopalvelut**-sivulta. [!INCLUDE [server](includes/server.md)]in esiintymä on määritettävä perustason todennuksella. Lisäksi on määritettävä käyttäjä ja kyseisen käyttäjän verkkokäyttöavain tämän salasanaksi. Korvaa seuraavassa esimerkissä *myserver:7048* [!INCLUDE [server](includes/server.md)]in nimellä ja *CRONUS%20US* oman yrityksen nimellä.  
    > ```https://myserver:7048/BC140/ODataV4/Company('CRONUS%20US')/```

6. Kun yhteys on muodostettu, koontinäyttö ja raportit lisätään Power BI -työtilaan. Kun tämä on tehty, ruudut näyttävä [!INCLUDE[prodshort](includes/prodshort.md)] -yrityksen tiedot.

    ![Dynamics 365 Business Centralin ja Hae se nyt -vaihtoehdon valinta](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

### <a name="what-now"></a>Mitä seuraavaksi?

- Kokeile [kysymyksen kirjoittamista kysymys- ja vastausruutuun](/power-bi/service-q-and-a-tips) koontinäytön yläreunassa.
- [Vaihda ruutuja](/power-bi/service-dashboard-edit-tile) koontinäytössä.  
- [Avaa taustalla oleva raportti valitsemalla ruutu](/power-bi/service-dashboard-tiles).  
- Tietojoukko ei oletusarvoisesti sisälly päivitykseen. Voit muuttaa päivitysaikataulua tai yrittää päivittämistä tarvittaessa **Päivitä nyt** -toiminnolla. Lisätietoja on kohdassa [Aikataulutetun päivityksen määrittäminen](/power-bi/refresh-scheduled-refresh).

## <a name="power-bi-in-include-prodshortincludesprodshortmd"></a>Power BI [!INCLUDE [prodshort](includes/prodshort.md)] -ratkaisussa

[!INCLUDE [prodshort](includes/prodshort.md)] -aloitussivulla voi olla Power BI -hallintaelementti, joka voidaan määrittää näyttämään Power BI -raportteja aloitussivulla.

> [!IMPORTANT]
> Sinulla on oltava kelvollinen [!INCLUDE [prodshort](includes/prodshort.md)]- ja Power BI -tili. Jos haluat muokata raportteja, myös Power BI Desktop on ladattava. Lisätietoja on kohdassa [Business Centralin käyttäminen Power BI -tietolähteenä](across-how-use-financials-data-source-powerbi.md).  

### <a name="on-first-login"></a>Ensimmäinen kirjautuminen

Kun kirjaudut [!INCLUDE [prodshort](includes/prodshort.md)] -ratkaisuun ensimmäisen kerran, aloitussivun Power BI -osa on tyhjä. Raporttien näkemistä varten Power BI -yhteys on muodostettava ensin valitsemalla *Aloita Power BI:n käyttö* -linkki.

[!INCLUDE [prodshort](includes/prodshort.md)] on sitten yhteydessä Power BI:hin ja selvittää, onko sinulla kelvollinen Power BI -tili. Kun käyttöoikeus on tarkistettu, Power BI:n oletusraportit näkyvät aloitussivulla.

### <a name="selecting-power-bi-reports"></a>Power BI -raporttien valitseminen

Aloitussivun Power BI -ohjausobjekti voi näyttää minkä tahansa Power BI -raportin. Voit tarkastella aiemmin luotua raporttia valitsemalla **Valitse raportti** -toiminto avattavasta Power BI -komentoluettelosta.  

Raportin valintasivulla on luettelo on kaikista niistä Power BI -raporteista, joita voit käyttää. Tämä luettelo noudetaan Power BI -työtilasta. Ota käyttöön kaikki ne raportit, jotka haluat näyttää aloitussivulla, ja valitse sitten OK. Palaat aloitussivulle ja viimeinen käyttöönotettu raportti tulee näkyviin. Siirry raporttien välillä käyttämällä avattavan komentoluettelon edellinen- ja seuraava-komentoja.  

### <a name="get-reports"></a>Raporttien lataaminen

Jos Valitse raportit -sivulla ei näy raportteja tai jos et näe haluamaasi raporttia. Voit valita raporttien lataamisen *omasta organisaatiosta* tai *palveluista*.
Valitse *Oma organisaatio* siirtymällä Power BI -palveluihin, joissa voit tarkastella raportteja siinä organisaatiossa, jossa sinulla on raporttien tarkasteluoikeudet, ja lisää ne työtilaan. Siirry Microsoft AppSourceeen, jossa voit asentaa Power BI -sovelluksia, valitsemalla *Palvelut*.  

Voit myös valita uusien Power BI -raporttien luomisen. Kun nämä raportit on julkaistu Power BI -työtilaan, ne näkyvät tällä sivulla.  

### <a name="managing-reports"></a>Raporttien hallinta

Voit valita aloitussivun Power BI -osassa **Raportin hallinta** -toiminnon avattavasta ohjausobjektiluettelosta. Tällä tavoin voit muokata raporttia, joka oli roolikeskuksen keskiössä.  

Raporttia voi muokata ja sen voi tallentaa.  Raporttiin tehdyt muutokset näkyvät kaikille raportin jakaville käyttäjille, sillä muokkaat raporttia, joka on tallennettu Power BI -palveluun.  

Kun olet tehnyt muutokset, valitse Tallenna. Jos kyse on jaettu raportti, voit valita Tallenna nimellä, jolloin muutos ei koske kaikkia käyttäjiä.
Palaa roolikeskukseen, jossa päivitetty raportti tulee näkyviin. Jos käytit Tallenna nimellä -komentoa, valittu raportin sivu on avattava ja uusi raportti otettava käyttöön.

### <a name="uploading-reports"></a>Raporttien lataaminen

Voit ladata uusia Power BI -raportteja ja jakaa ne kaikkien [!INCLUDE [prodshort](includes/prodshort.md)] -käyttäjiesi kanssa. Raportit jaetaan kussakin [!INCLUDE [prodshort](includes/prodshort.md)] -yrityksessä.  

Lataa raportti valitsemalla **Lataa raportti** -toiminto avattavasta komentoluettelosta. Voit sitten ladata. pbix-tiedoston, joka määrittää jaettavat raportit. Voit muuttaa tiedoston oletusnimeä.  

Kun raportti on ladattu Power BI -työtilaan, se latautuu automaattisesti kaikkien kyseisen yrityksen käyttäjien Power BI-työtiloihin, kun he kirjautuvat seuraavan kerran [!INCLUDE [prodshort](includes/prodshort.md)]iin.

## <a name="system-requirements"></a>Järjestelmävaatimukset

Jos haluat tuoda [!INCLUDE[prodshort](includes/prodshort.md)]in tietoja Power BI:hin, sinulla on oltava tietojen noutamiseen käytettävien verkkopalvelujen käyttöoikeudet. Kullekin Power BI -sovellukselle tarvitaan esimerkiksi seuraavat verkkopalvelut:

### <a name="microsoft-dynamics-365-business-central--crm"></a>Microsoft Dynamics 365 Business Central – CRM

- Myyntimahdollisuudet
- Excel-malli Näytä yrityksen tiedot
- Power BI -raporttien selitteet

### <a name="microsoft-dynamics-365-business-central--finance"></a>Microsoft Dynamics 365 Business Central – Finance

- PowerBIFinance
- Excel-malli Näytä yrityksen tiedot
- Power BI -raporttien selitteet

### <a name="microsoft-dynamics-365-business-central---sales"></a>Microsoft Dynamics 365 Business Central – Sales

- Asiakaskohtainen nimikemyynti
- Myynnin koontinäyttö
- Excel-malli Näytä yritys
- Power BI -raporttien selitteet

> [!NOTE]
> Paikallinen [!INCLUDE [prodshort](includes/prodshort.md)] käyttää samaa verkkopalvelua ja päätepisteitä kuin [!INCLUDE [prodshort](includes/prodshort.md)] -verkkoversio.

## <a name="web-services"></a>WWW-palvelut

Verkkopalveluja voi etsiä kätevästi hakemalla *verkkopalveluja* [!INCLUDE[prodshort](includes/prodshort.md)]issa. Varmista **Verkkopalvelut**-sivulla, että **Julkaisu**-kenttä on valittuna edellä mainituissa verkkopalveluissa.

## <a name="troubleshooting"></a>Vianetsintä

Power BI:n koontinäyttö käyttää julkaistuja edellä mainittuja verkkopalveluita. Koontinäytössä ovat esittely-yrityksen tiedot tai oman yrityksesi tiedot, jos toit tiedot nykyisestä rahoitusratkaisustasi. Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.  

### <a name="you-do-not-have-a-power-bi-account"></a>Power BI -tiliä ei ole

Power BI -tiliä ei ole määritetty. Kelvollinen Power BI -tili edellyttää, että sinulla on käyttöoikeus ja että olet aiemmin kirjautunut Power BI:iin. Jos näin on, Power BI -työtila on voitu luoda.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Sanoma: Käyttöönotettuja raportteja ei ole. Valitsemalla Valitse raportti saat näkyviin luettelon raporteista, joita voit tarkastella.

Tämä sanoma avautuu, jos oletusraportin käyttöönotto Power BI -työtilassa epäonnistui tai jos raportti otettiin käyttöön mutta sen päivitys ei onnistunut. Jos näin tapahtuu, siirry raporttiin Power BI -työtilassa, valitse **Tietojoukko**, **Asetukset** ja päivitä tunnistetiedot sitten manuaalisesti. Kun tietojoukko on päivitetty, siirry takaisin Business Centraliin ja valitse raportti manuaalisesti **Valitse raportit** -sivulla.

### <a name="you-need-a-power-bi-pro-license-to-install-the-include-prodshortincludesprodshortmd-app-in-power-bi"></a>[!INCLUDE [prodshort](includes/prodshort.md)] -sovelluksen asentaminen Power BI:ihin edellyttää Power BI Pro -käyttöoikeutta.

Vain käyttäjät, joilla on Power BI Pro -käyttöoikeus, voivat asentaa Power BI -sovelluksia. Kun Power BI -sovellus on asennettu, voit jakaa sen sellaisten käyttäjien kanssa, joilla ei ole Power BI Pro -käyttöoikeutta.  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>Parametrin tarkistus epäonnistui. Varmista, että kaikki parametrit ovat sallittuja.

Tämä virhe ilmaisee, että vähintään yksi parametreista on virheellinen.

- Määritetty ympäristöparametri ei vastaa mitään aiemmin luotua [!INCLUDE [prodshort](includes/prodshort.md)]in tuotanto- tai sandbox-ympäristöä.
- Määritys yritysparametri ei vastaa mitään aiemmin luotua [!INCLUDE [prodshort](includes/prodshort.md)] -yritystä. Tarkista yrityksen nimi [!INCLUDE [prodshort](includes/prodshort.md)]in **Yritykset**-sivulla.
- Yhteys muodostetaan paikalliseen [!INCLUDE [prodshort](includes/prodshort.md)] -versioon. Antamasi URL-osoite ei kelpaa. Voit tarkistaa URL-osoitteen [!INCLUDE [prodshort](includes/prodshort.md)]in **Verkkopalvelut**-sivulla  
- Porttia ei ole avattu, joten pyyntö ei läpäise palomuuria.

### <a name="login-failed"></a>Sisäänkirjautuminen epäonnistui

Jos näyttöön tulee sisäänkirjautumisen epäonnistumista ilmoittava virhe sen jälkeen, kun kirjauduit [!INCLUDE [prodshort](includes/prodshort.md)] -tunnistetiedoilla, syynä on luultavasti jokin seuraavista:

- Käyttämälläsi tilillä ei ole [!INCLUDE [prodshort](includes/prodshort.md)]in tietojen hakuoikeuksia. Tarkista, että sinulla on tarvittavien [!INCLUDE [prodshort](includes/prodshort.md)] -tietojen oikeudet ja yritä uudelleen.
- Olet valinnut jonkin muun kuin perustason todennustyypin, jos yhteys on muodostettu paikalliseen [!INCLUDE [prodshort](includes/prodshort.md)] -versioon.
- Et ole antanut oikeaa käyttäjänimeä tai salasanaa.

### <a name="incorrect-company-name"></a>Virheellinen yrityksen nimi

Yleinen virhe on antaa yrityksen näyttönimi yrityksen nimen sijaan. Voit etsiä yrityksen nimen hakusanalla **Yritykset**. Anna sitten yrityksen nimi **Nimi**-kentässä.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Avain ei vastannut mitään taulukon riviä

Jos annat yhteydenmuodostusprosessin aikana yrityksen nimen, joka ei ole sallittu, näyttöön voi avautua virhesanoma, jonka mukaan avain ei vastannut mitään taulukon riviä. Anna oikea yrityksen nimi ja yritä muodostaa yhteys uudelleen.

### <a name="historical-data-appears-to-be-missing"></a>Historiatietoja näyttää puuttuvan

Kun Power BI -sovellus on asennettu ja tiedot näkyvät Power BI:ssä, olet ehkä huomannut, että kaikki tietosi eivät näy. Tietojoukot suodatetaan palauttamaan vain viimeisen 365 päivän tiedot. Tämä oletus on käytössä raporttien nopeuttamiseksi.  

### <a name="i-only-see-data-for-a-single-company"></a>Vain yhden yrityksen tiedot näkyvät

Power BI -sovellus näyttää vain sen [!INCLUDE [prodshort](includes/prodshort.md)] -yrityksen tiedot, joka määritettiin Power BI -sovelluksen asennuksen yhteydessä. Muiden yrityksen tietoja voidaan lisätä raporttiin lisäämällä uusi kyselyjä, jotka käyttävät eri yrityksiä tietolähteenä.  

## <a name="see-related-training-at-microsoft-learnlearnmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Power BI kuluttajille](/power-bi/consumer/end-user-consumer)  
[Power BI -palvelun uusi ulkoasu](/power-bi/service-new-look)  
[Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI -dokumentaatio](/power-bi/)  
[Business Intelligence](bi.md)  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power Apps:n tietolähteenä](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power Automate'ssa](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
