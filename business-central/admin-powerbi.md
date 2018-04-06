---
title: "Business Central- ja Power BI Content Pack -sisältöpaketit | Microsoft Docs"
description: "Analyysitietojen, liiketoimintatietoja ja tunnuslukujen hakeminen Business Central -tiedoista on helppoa Power BI- ja Business Central -sisältöpakettien avulla."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6b72de70da67a7401bad90bd55d1a31a1ae6d880
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="enabling-your-business-data-for-power-bi"></a>Yritystietojen ottaminen käyttöön Power BI:tä varten
Lisätietojen hakeminen [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoihin on helppoa Power BI- ja [!INCLUDE[d365fin](includes/d365fin_md.md)]-sisältöpakettien avulla. Power BI hakee tiedot ja muodostaa näiden tietojen perusteella valmiin koontinäytön ja raportit.  

Microsoft on julkaissut seuraavat sisältöpaketit:

| Sovellus | Description |
| --- | --- |
| Microsoft Business Central | Sisältää koontinäytön, jossa on tärkeitä aikaperusteisia taloustietoja, kuten tulojen ja menojen vertailu, käyttökate ja käyttöpääomasykli.|
| Microsoft Business Central - CRM | Sisältää koontinäytön, jossa on tärkeitä tietoja myyntimahdollisuuksista ja kontakteista.  |
| Microsoft Business Central - Myynti | Sisältää koontinäytön, jossa on tärkeitä tietoja myynnistä ja varastosta. |

## <a name="using-the-dashboards"></a>Koontinäyttöjen käyttäminen
Kussakin sisältöpaketissa on raportteja, joilla voi porautua tietoihin:

* Valitse koontinäytöstä jokin visuaalinen kohde, kun haluat käsitellä jotakin perustana olevasta raportista.  
* Suodata raportti tai lisää seurattavia kenttiä.  
* Kiinnitä tämä mukautettu näkymä koontinäyttöön, kun haluat jatkaa seuraamista.  
  Voit päivittää tiedot manuaalisesti ja määrittää päivitysaikataulun. Lisätietoja on kohdassa [Aikataulutetun päivityksen määrittäminen](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Sisältöpaketit on määritetty etukäteen niin, että niitä voidaan käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]iin rekisteröityessä saatavan esittely-yrityksen tietojen kanssa. Kun asennat sovelluksia Power BI:hin ja yhdistät ne omiin tietoihisi, jotkin raportit eivät ehkä toimi, koska ne perustuvat tietoihin, joita yrityksellä ei ole. Voit siinä tapauksessa poistaa raportin koontinäytöstä.  

> [!NOTE]  
>   Voit myös luoda omia raportteja ja koontinäyttöjä Power BI:ssä [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietojen perusteella. Lisätietoja on ohjeaiheessa [Liiketoimintatietojen yhdistäminen Power BI:hin](across-how-use-financials-data-source-powerbi.md).  

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power BI:ssä
Voit tarkastella [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja Power BI:ssä, kun seuraavat vaatimukset toteutuvat:  

* [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeus. Lisätietoja on kohdassa [Business Central](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Power BI:n käyttöoikeus. Lisätietoja on kohdassa [Power BI](https://powerbi.microsoft.com).

Power BI -sivustossa on lisätietoja [sisältöpaketteja sisältävien palvelujen yhdistämisestä Power BI:hin](http://go.microsoft.com/fwlink/?LinkID=760850).  

[!INCLUDE[d365fin](includes/d365fin_md.md)]in tietojen käyttö Power BI:ssä edellyttää, että yhteyssivulla on määritetty seuraavat tiedot:

| Kenttä | Kuvaus |
| --- | --- |
| **OData-syötteen URL-osoite** |OData-palvelun URL-osoite, jotta Power BI voi käyttää yrityksen tietoja, esimerkiksi https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('My%2Business'). |
| **Todennusmenetelmä** |Valitse **Perus**. |
| **Käyttäjänimi** |Nimi siinä muodossa, kun näkyy [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilillä, kuten *Matti Virtanen*. |
| **Salasana** |Tämä on [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätilin verkkopalvelun käyttöoikeusavain. |

[!INCLUDE[d365fin](includes/d365fin_md.md)]ista on siis haettava kaksi tietoa: *ODatan URL-osoite* ja käyttäjätilin *verkkopalvelun käyttöoikeusavain*.  

### <a name="getting-the-url"></a>URL-osoitteen hakeminen
Kun lisäät [!INCLUDE[d365fin](includes/d365fin_md.md)]in Power BI:hin, URL-osoite on määritettävä, jotta Power BI voi käyttää yrityksen tietoja. URL-osoitteeseen viitataan yhteyssivulla **OData-syötteen URL-osoite** -nimellä. Sen on oltava seuraavassa muodossa:

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
Tässä esimerkissä *mybusiness* on [!INCLUDE[d365fin](includes/d365fin_md.md)]-palvelun nimi ja *CRONUS US* esittely-yrityksen nimi. *%20* tarkoittaa nimessä olevaa väliä.   
Voit hakea URL-osoitteen hakemalla [!INCLUDE[d365fin](includes/d365fin_md.md)]in **WWW-palvelut**-ikkunan ja avaamalla sen. Ikkuna sisältää tällä hetkellä käytettävissä olevat WWW-palvelut. Voit kopioida **ODatan URL-osoite** -kentän linkin johonkin ODatan oletus-WWW-palveluun.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Käyttäjänimen ja verkkopalvelun käyttöoikeusavaimen hakeminen
Jotta [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja voisi käyttää Power BI:tä, käyttäjänimi ja salasana on määritettävä **Muodosta Financials-yhteys** -ikkunassa. Käyttäjänimi on nimesi siinä muodossa kuin se näkyy [!INCLUDE[d365fin](includes/d365fin_md.md)]in tilillä, jotta Power BI voit kirjautua [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Salasana on [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätilillä määritetty verkkopalvelun käyttöoikeusavain.  

Voit etsiä nämä tiedot etsimällä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa **Käyttäjät**-ikkunan ja avaamalla käyttäjätilin kortin. Kopioi **Yleiset**-pikavälilehdessä **Käyttäjänimi**-kentän sisältö ja **Verkkopalvelun käyttö**-pikavälilehdessä **Verkkopalvelun käyttöoikeusavain** -kentän sisältö. Jos **Verkkopalvelun käyttöoikeusavain** -kenttä on tyhjä, valitse valintanauhassa ensin **Muuta verkkopalvelun käyttöoikeusavainta**, sitten **Avain ei vanhene koskaan** -kenttä ja lopuksi OK-painike. Tämän jälkeen voit kopioida avaimen.  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Tietojen hakeminen [!INCLUDE[d365fin](includes/d365fin_md.md)]ista
[!INCLUDE[d365fin](includes/d365fin_md.md)]in koontinäyttö sisältää tavallisimmat liiketoiminnan seuraamisessa käytettävät raportit. Tiedot puretaan [!INCLUDE[d365fin](includes/d365fin_md.md)]in yrityksestä verkkopalveluiden avulla oikeiden tietojen lukemista varten. [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Verkkopalvelut**-ikkunassa on luettelo määritetyistä verkkopalveluista.

> [!NOTE]  
>   Jos muutat näiden verkkopalveluiden nimet, tiedot eivät näy Power BI:ssä.  
Jos haluat lisätä muiden tietojen käytön Power BI:ssä, etsi taulukot [!INCLUDE[d365fin](includes/d365fin_md.md)]ista, näytä ne verkkopalveluina ja lisää ne sisältöpakettiin. Tämä on lisäskenaario. Suosittelemme, että aloitat käsittelemisen Power BI:n valmiilla tiedoilla.  

## <a name="troubleshooting"></a>Vianetsintä
Power BI:n koontinäyttö käyttää julkaistuja yllä mainittuja WWW-palveluita. Koontinäytössä ovat esittely-yrityksen tiedot tai oman yrityksesi tiedot, jos toit tiedot nykyisestä rahoitusratkaisustasi. Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.  

**"Parametrin tarkistus epäonnistui. Varmista, että kaikki parametrit ovat sallittuja."**  
Jos näyttöön tulee tämä virhe [!INCLUDE[d365fin](includes/d365fin_md.md)]in URL-osoitteen antamisen jälkeen, varmista, että seuraavat vaatimukset täyttyvät:  

* URL-osoitteen muodon on oltava täsmälleen tämä:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Poista teksti, joka on sulkeissa olevan yrityksen nimen jälkeen  
* Varmista, että URL-osoitteen lopussa ei ole vinoviivaa.  
* Varmista, että URL-osoitteen alussa on suojatun yhteyden osoittava merkkijono *https*.  

**"Sisäänkirjautuminen epäonnistui"**  
Jos näyttöön tulee sisäänkirjautumisen epäonnistumista ilmoittava virhe, kun kirjaudut koontinäyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]in tunnistetiedoilla, syy voi olla jonkin seuraavista:

* Käyttämälläsi tilillä ei ole [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietojen lukuoikeuksia.

    Tarkista [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätili ja varmista, että olet käyttänyt oikeaa verkkopalvelun käyttöoikeusavainta salasanana. Yritä tämän jälkeen uudelleen.  
* [!INCLUDE[d365fin](includes/d365fin_md.md)]in ilmentymällä, johon yrität muodostaa yhteyden, ei ole sallittua SSL-varmennetta. Tällöin näyttöön tulee eritellympi virhesanoma ("luotetun SSL-suhteen muodostaminen ei onnistu").

    > [!NOTE]  
>   Itse allekirjoitettuja varmenteita ei tueta.  

**"Jokin meni vikaan"**  
Jos näet "Jokin meni vikaan" -virhevalintaikkunan sen jälkeen, kun todentamisvalintaikkuna on ohitettu, syy on todennäköisesti ongelma muodostettaessa yhteyttä sisältöpaketin tietoihin.

* Varmista, että URL-osoitteella on seuraava aiemmin määritetty muoto:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')`  
* Yleinen virhe on määrittää tietyn WWW-palvelun koko URL-osoite.

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance`
* Myös yrityksen nimi on saattanut unohtua.

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/`

## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)  
[Liiketoiminnan tietojen siirtäminen muista rahoitusjärjestelmistä](upload-data.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Power BI -tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen PowerApps-tietolähteenä](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen Microsoft Flow'ssa](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

