---
title: Power BI -raporttien käyttäminen Business Centralissa | Microsoft Docs
description: Analyysitietojen, liiketoimintatietojen ja tunnuslukujen hakeminen Business Centralin tiedoista on helppoa Power BI:n Business Central -sovelluksia.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: a747a0bdb67187597cc33185b418844247b2e2b2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752973"
---
# <a name="working-with-power-bi-reports-in-prod_short"></a>Power BI -raporttien käyttäminen [!INCLUDE [prod_short](includes/prod_short.md)]issa

Tässä artikkelissa on perustietoja Power BI -raporttien näyttämisestä [!INCLUDE [prod_short](includes/prod_short.md)]issa.

## <a name="overview"></a>Yleiskuvaus

Power BI -raporteilla saadaan merkityksellisiä tietoja [!INCLUDE[prod_short](includes/prod_short.md)]ista. [!INCLUDE [prod_short](includes/prod_short.md)]in eri sivuilla on Power BI -raporttiosa, jossa voidaan näyttää Power BI -raportteja. Roolikeskus on tyypillinen sivu, jossa Power BI -raporttiosa on näkyvissä. Power BI -osa on näkyvissä myös joillakin luettelosivuille, kuten **Nimikkeet**.

[!INCLUDE [prod_short](includes/prod_short.md)]ia käytetään yhdessä Power BI -palvelun kanssa. [!INCLUDE [prod_short](includes/prod_short.md)]issa näytettävät raportit tallennetaan Power BI -palveluun. Voit vaihtaa [!INCLUDE [prod_short](includes/prod_short.md)]in Power BI -osassa näkyvän raportin mihin tahansa Power BI -palvelussa käytettävissä olevaan Power BI -raporttiin. Kun kirjaudut ensimmäisen kerran [!INCLUDE [prod_short](includes/prod_short.md)]iin etkä ole vielä muodostanut yhteyttä Power BI -palveluun, osat ovat tyhjiä, kuten seuraavassa kuvassa:

![Business Centralin Power BI -osa](./media/power-bi-part.png)

## <a name="prerequisites"></a>Vaatimukset

Jos käytössä on paikallinen [!INCLUDE[prod_short](includes/prod_short.md)], Power BI -integraation on oltava siinä käytössä. Yleensä järjestelmänvalvoja tekee tämän tehtävän. Lisätietoja on kohdassa [Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -version Power BI -integraation määrittäminen](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] online on jo määritetty Power BI -integrointia varten.

## <a name="get-ready"></a>Valmistelut

Rekisteröidy Power BI -palveluun. Jos et ole vielä rekisteröitynyt, siirry osoitteeseen [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Käytä rekisteröityessä työpaikan sähköpostiosoitetta ja salasanaa.

## <a name="connect-to-power-bi---one-time-only"></a>Power BI -yhteyden muodostaminen – kerran

Kun [!INCLUDE [prod_short](includes/prod_short.md)]iin kirjaudutaan ensimmäisen kerran, jollakin sivulla voi näkyä tyhjä Power BI -osa, kuten edellisessä kuvassa. Ensimmäiseksi onkin muodostettava yhteys Power BI -tiliin. Kun yhteys on muodostettu, raportit ovat näkyvissä. Tämä vaihe tarvitsee tehdä vain kerran.

Muodosta yhteys Power BI:hin valitsemalla **Aloita Power BI:n käyttö** -linkki **Power BI -raportit** -osassa.

[!INCLUDE [prod_short](includes/prod_short.md)] on yhteydessä Power BI -palveluun yhdistämisprosessin aikana ja selvittää, onko sinulla kelvollinen Power BI -tili ja -käyttöoikeus. Kun käyttöoikeus on tarkistettu, Power BI -raportti näkyy sivulla. Jos raportti ei tule näkyviin, voit valita raportin osassa.

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)] online -versiossa tämä vaihe lataa automaattisesti [!INCLUDE [prod_short](includes/prod_short.md)]issa käytettävät Power BI -oletusraportit Power BI -työtilaan.

##### <a name="from-prod_short-on-premises"></a>Paikallinen [!INCLUDE [prod_short](includes/prod_short.md)]

Power BI -yhteyden muodostaminen [!INCLUDE [prod_short](includes/prod_short.md)]ista muistuttaa online-version yhteydenmuodostusta. Sinua kuitenkin pyydetään myöntämään Power BI -palvelujen käyttöoikeus **AZURE ACTIVE DIRECTORY -PALVELUN KÄYTTÖOIKEUDET** -sivulla. Voit myöntää käyttöoikeuden valitsemalla ensin **Valtuuta Azure-palvelut** ja sitten **Hyväksy**.

Kun yhteys on muodostettu, voit valita Power BI -osan sivuilla.

## <a name="show-power-bi-reports-on-list-pages"></a>Power BI -raporttien näyttäminen luettelosivuilla

[!INCLUDE[prod_long](includes/prod_long.md)] sisältää Power BI -tietoruudun useilla tärkeillä luettelosivuilla. Tässä luetteloruudussa on lisätietoja luettelon tiedoista. Raportti päivitetään ja suodatetaan valitun tapahtuman mukaan, kun siirryt luettelon riveillä. Jos tämä osa ei ole näkyvissä, valitse siinä tapauksessa toimintorivillä **Toiminnot** > **Näytä** > **Näytä tai piilota Power BI -raportit**. Lisätietoja on kohdassa [Power BI -raporttien luominen näyttämään luettelotietoja [!INCLUDE[prod_short](includes/prod_short.md)]issa](across-how-use-powerbi-reports-factbox.md).

## <a name="select-power-bi-reports"></a>Power BI -raporttien valitseminen

Sivun Power BI -osassa voi näyttää minkä tahansa käytettävissä olevan Power BI -raportin. Näkyvissä olevan raportin voi vaihtaa valitsemalla **Valitse raportti** -toiminnon osan yläreunassa olevasta avattavasta komentoluettelosta.  

**Power BI -raporttien valinta** -sivulla on luettelo on kaikista käytettävissä olevista Power BI -raporteista. Tämä luettelo noudetaan Power BI -työtilasta. Valitse kaikkien niiden raporttien **Ota käyttöön** -ruutu,, jotka haluat näyttää aloitussivulla, ja valitse sitten **OK**. Palaat sivulle ja viimeinen käyttöönotettu raportti tulee näkyviin. Voit siirtyä raporttien välillä käyttämällä avattavan komentoluettelon **Edellinen**- ja **Seuraava**-komentoja.  

## <a name="get-reports"></a>Raporttien lataaminen

Jos **Power BI -raporttien valinta** -sivulla ei näy raportteja tai jos haluamasi raportti ei ole näkyvissä, valitse **Lataa raportit**. Voit etsiä tällä toiminnolla raportteja kahdesta sijainnista: *Oma organisaatio* ja *Palvelut*.

- Siirry Power BI -palveluihin valitsemalla **Oma organisaatio**. Voit tarkastella siellä niitä organisaation raportteja, joiden tarkasteluoikeudet sinulla on. Voit sitten lisätä ne työtilaan.
- Siirry Microsoft AppSourceeen, jossa voit asentaa Power BI -sovelluksia, valitsemalla **Palvelut**.  

> [!TIP]
> Jos sinulla on Power BI Desktop, voit myös luoda uusia Power BI -raportteja. Sitten kun nämä raportit on julkaistu Power BI -työtilaan, ne näkyvät **Power BI -raporttien valinta** -sivulla.  

## <a name="manage-and-modify-reports"></a>Raporttien hallinta ja muokkaaminen

Voit tehdä muutoksia raporttiin Power BI -osassa. Tehdyt muutokset julkaistaan sitten Power BI -palveluun. Jos raportti on jaettu muiden käyttäjien kanssa, myös he näkevät muutokset paitsi siinä tapauksessa, että olet tallentanut muutokset uuteen raporttiin.

Voit muokata raporttia valitsemalla **Raportin hallinta** -toiminnon avattavasta komentoluettelosta Power BI -osassa. Tee sitten muutokset. Kun olet tyytyväinen muutoksiin valitse **Tiedosto** > **Tallenna**. Jos kyse on jaetusta raportista eikä halua tehdä muutoksia kaikille käyttäjille, valitse **Tallenna nimellä**, jolloin tehty muutos ei koske kaikkia käyttäjiä.

Kun palaat roolikeskukseen, päivitetty raportti on näkyvissä. Jos valitsit **Tallenna nimellä**, uusi raportti on näkyvissä vasta, kun valitset **Valitse raportti** ja otat uuden raportin käyttöön.

> [!NOTE]
> Tämä ominaisuus ei ole käytettävissä paikallisessa [!INCLUDE [prod_short](includes/prod_short.md)] -versiossa.

## <a name="upload-reports"></a><a name="upload"></a>Raporttien lataaminen palvelimeen

Power BI -raportteja voi jakaa käyttäjille .pbix-tiedostoina. Jos sinulla on .pbix-tiedostoja, voit ladata ja jakaa ne kaikkien [!INCLUDE [prod_short](includes/prod_short.md)] -käyttäjien kanssa. Raportit jaetaan kussakin [!INCLUDE [prod_short](includes/prod_short.md)] -yrityksessä.  

Lataa raportti valitsemalla **Lataa raportti** -toiminto avattavasta komentoluettelosta **Power BI -raportit** -osassa. Etsi sitten .pbix-tiedosto, joka määrittää jaettavat raportit. Voit muuttaa tiedoston oletusnimeä.  

Kun raportti on latautunut Power BI -työtilaan, se latautuu automaattisesti muiden käyttäjien Power BI -työtiloihin.

> [!NOTE]
> Raportin lataaminen edellyttää [!INCLUDE[prod_short](includes/prod_short.md)]in SUPER-käyttäjän oikeuksia. Raportteja ei voi ladata paikallisella [!INCLUDE [prod_short](includes/prod_short.md)] -versiolla. Paikallisessa versiossa raportit ladataan suoraan Power BI -työtilaan. Lisätietoja on kohdassa [[!INCLUDE [prod_short](includes/prod_short.md)] -tietojen käyttäminen Power BI:ssa](across-working-with-business-central-in-powerbi.md).

## <a name="fixing-problems"></a>Ongelmien korjaaminen

Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.  

### <a name="you-dont-have-a-power-bi-account"></a>Power BI -tiliä ei ole

Power BI -tiliä ei ole määritetty. Kelvollisen Power BI -tilin saaminen edellyttää, että sinulla on käyttöoikeus ja että olet aiemmin kirjautunut Power BI:hin luomaan Power BI -työtilan.   

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Sanoma: Käyttöönotettuja raportteja ei ole. Valitsemalla Valitse raportti saat näkyviin luettelon raporteista, joita voit tarkastella.

Tämä sanoma avautuu, jos oletusraporttia ei voitu ottaa käyttöön Power BI -työtilassa. Vaihtoehtoisesti se otettiin käyttöön mutta sen päivittäminen epäonnistui. Siirry raporttiin Power BI -työtilassa, valitse **Tietojoukko**, **Asetukset** ja päivitä sitten tunnistetiedot manuaalisesti. Kun tietojoukko on päivitetty, siirry takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin ja valitse raportti manuaalisesti **Valitse raportit** -sivulla.


## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Business Central ja Power BI](admin-powerbi.md)  
[Power BI -raporttien luominen näyttämään [!INCLUDE [prod_long](includes/prod_long.md)] -tietoja](across-how-use-financials-data-source-powerbi.md)  
[Power BI:n -integrointiosa ja [!INCLUDE[prod_short](includes/prod_short.md)] -arkkitehtuurin yleiskatsaus](admin-powerbi-overview.md)  
[[!INCLUDE [prod_short](includes/prod_short.md)] -tietojen käyttäminen Power BI:ssa](across-working-with-business-central-in-powerbi.md)  
[Power BI kuluttajille](/power-bi/consumer/end-user-consumer)  
[Power BI -palvelun uusi ulkoasu](/power-bi/service-new-look)  
[Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI -dokumentaatio](/power-bi/)  
[Business Intelligence](bi.md)  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Apps:n tietolähteenä](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Automate'ssa](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]