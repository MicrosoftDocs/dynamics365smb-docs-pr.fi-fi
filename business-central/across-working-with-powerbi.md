---
title: Power BI -raporttien käyttäminen Business Centralissa | Microsoft Docs
description: 'Merkityksellisten tietojen, liiketoimintatietojen ja tunnuslukujen saaminen Business Central -tiedoista Power BI:n avulla.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/24/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="work-with-power-bi-reports-in-"></a>Power BI -raporttien käsittely [!INCLUDE [prod_short](includes/prod_short.md)]issa

Tässä artikkelissa on perustietoja raporttien käyttämisestä. Tämä sisältää Power BI -raporttien tarkastelemisen [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman sisällä (mukaan lukien tuloskortit ja koontinäytöt) ja [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa tietolähteenä käyttävien Power BI -raporttien muokkaamisen. Artikkelissa käsitellään seikkoja, jotka helpottavat [!INCLUDE[prod_short](includes/prod_short.md)] -käytön aloittamista käyttäjänä. Yleistä opastusta ja ohjeita Power BI:n käytöstä on kohdassa [Power BI:n kuluttajille suunnattu dokumentaatio](/power-bi/consumer).

## <a name="overview"></a>Yleiskuvaus

Power BI -raporteilla saadaan merkityksellisiä tietoja [!INCLUDE[prod_short](includes/prod_short.md)]ista. [!INCLUDE [prod_short](includes/prod_short.md)]in eri sivuilla on Power BI -raporttiosa, jossa voidaan näyttää Power BI -raportteja. Roolikeskus on tyypillinen sivu, jossa Power BI -raporttiosa on näkyvissä. Power BI -osa on näkyvissä myös joillakin luettelosivuille, kuten **Nimikkeet**.

[!INCLUDE [prod_short](includes/prod_short.md)]ia käytetään yhdessä Power BI -palvelun kanssa. [!INCLUDE [prod_short](includes/prod_short.md)]issa näytettävät raportit tallennetaan Power BI -palveluun. Voit vaihtaa [!INCLUDE [prod_short](includes/prod_short.md)]in Power BI -osassa näkyvän raportin mihin tahansa Power BI -palvelussa käytettävissä olevaan Power BI -raporttiin. Kun kirjaudut ensimmäisen kerran [!INCLUDE [prod_short](includes/prod_short.md)]iin etkä ole vielä muodostanut yhteyttä Power BI -palveluun, osat ovat tyhjiä, kuten seuraavassa kuvassa:

![Power BI osa Business Centralissa.](./media/power-bi-part.png)

## <a name="get-started"></a>Aloittaminen

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] online on jo määritetty Power BI -integrointia varten.

### <a name="sign-up-power-bi"></a>Rekisteröityminen Power BI:hin

Ennen kuin Power BI:ta voi käyttää [!INCLUDE[prod_short](includes/prod_short.md)]issa, Power BI -palveluun on rekisteröidyttävä. Jos et ole vielä rekisteröitynyt, siirry osoitteeseen [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Käytä rekisteröityessä työpaikan sähköpostiosoitetta ja salasanaa.

Kun olet saanut Power BI -tilin, voit kirjautua osoitteessa [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

Power BI -palvelu on kaikkien käytettävissä olevien raporttien isäntä. Jos haluat nähdä raportin henkilökohtaisen työtilasi yhteydessä, valitse **Oma työtila** > **raportit**. Valitse sitten raportti, jota haluat tarkastella. Jos sinulla on pääsy yhteen tai useampaan jaettuun Power BI työtilaan, voit nähdä raportteja myös noissa työtiloissa.

[!INCLUDE[prod_short](includes/prod_short.md)] online -versiossa työtilassa on automaattisesti joukko oletusraportteja. Jos haluat luoda omia raportteja, voit tehdä sen Power BI Desktopissa ja julkaista luodut raportit sitten työtilaan. Lisätietoja on kohdassa [[!INCLUDE [prod_long](includes/prod_long.md)] -tiedot näyttävien raporttien luonnin muodostamisen aloittaminen Power BI Desktopissa](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="connect-to-power-bi---one-time-only"></a><a name="connect"></a>Power BI -yhteyden muodostaminen – kerran

Kun [!INCLUDE [prod_short](includes/prod_short.md)]iin kirjaudutaan ensimmäisen kerran, eri sivuilla näkyy luultavasti tyhjä Power BI -osa (kuten edellisessä kuvassa). Ensimmäiseksi onkin muodostettava yhteys Power BI -tiliin. Kun yhteys on muodostettu, raportit ovat näkyvissä. Tämä vaihe tarvitsee tehdä vain kerran.

1. Valitse **Aloita Power BI:n käyttö** -linkki **Power BI -raportit** -osassa.
2. Asetusten ohjattu **Määritä Power BI -raportit Business Centralissa** -määritys käynnistyy. Jatka valitsemalla **Seuraava**.
3. **Tarkista Power BI -käyttöoikeus** -sivulla. Tee jompikumpi seuraavista:

    - Jos et ole vielä rekisteröitynyt Power BI:hin, valitse [Siirry Power BI -aloitussivulle](https://powerbi.microsoft.com). Rekisteröidy tilille, palaa sitten [!INCLUDE[prod_short](includes/prod_short.md)]iin ja viimeistele määritykset.

    - Jos sinulla on jo käyttöoikeus, valitse **Seuraava**.
4. [!INCLUDE[prod_short](includes/prod_short.md)] lataa nyt seuraavalla sivulla esittelyraportin Power BI:hin. Tämä vaihe kestää muutamia minuutteja, joten se tapahtuu taustalla. Viimeistele määritykset valitsemalla ensin **Seuraava** ja sitten **Valmis**.

Yhteysprosessi käynnistyy. [!INCLUDE [prod_short](includes/prod_short.md)] on yhteydessä Power BI -palveluun prosessin aikana ja selvittää, onko sinulla kelvollinen Power BI -tili ja -käyttöoikeus. Kun käyttöoikeus on tarkistettu, Power BI -raportti näkyy sivulla. Jos raportti ei tule näkyviin, voit valita raportin osassa.

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)] online -versiossa tämä vaihe lataa automaattisesti [!INCLUDE [prod_short](includes/prod_short.md)]issa käytettävät Power BI -oletusraportit Power BI -työtilaan.

<!--#### From [!INCLUDE [prod_short](includes/prod_short.md)] on-premises

Connecting to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] is similar to online. However, you might be prompted on the **MICROSOFT ENTRA SERVICE PERMISSIONS** page to grant access to Power BI Services. To grant access, select **Authorize Azure Services**, and then **Accept**.

Once connected, you can select a report from the Power BI part on pages.-->

## <a name="work-with-power-bi-reports"></a>Power BI -raporttien käyttö

### <a name="get-the-latest-data"></a>Viimeisten tietojen hakeminen

Kukin Power BI -raportti perustuu tietojoukkoon, joka saa tietoja [!INCLUDE[prod_short](includes/prod_short.md)] -lähteistä. Power BI -raporttien tietojen halutaan olevan aina ajantasaisia [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen kanssa. Tätä kutsutaan *päivittämiseksi*.  Sen perusteella, miten organisaatio on määrittänyt Power BI:n, päivitystä ei välttämättä tehdä automaattisesti. Tiedot voidaan päivittää kahdella tavalla: manuaalisesti tai ajoitetulla päivityksellä. Manuaalinen päivitys tehdään tarvittaessa. Ajoitetussa päivityksessä tiedot päivitetään automaattisesti määritetyn ajan kuluttua.

#### <a name="refresh-manually"></a>Manuaalinen päivitys

Valitse Power BI -onlinessa siirtymisruudussa **Tietojoukot**-kohdassa tietojoukon vieressä **Lisää vaihtoehtoja (...)** ja valitse sitten **Päivitä nyt**.

#### <a name="schedule-a-refresh"></a>Päivityksen ajoittaminen

Valitse Power BI -onlinessa siirtymisruudussa Tietojoukot-kohdassa tietojoukon vieressä Lisää vaihtoehtoja (...) ja valitse sitten **Ajoita päivitys**. Täytä **Ajoita päivitys** -osan tiedot ja valitse **Käytä**.

Lisätietoja on kohdassa [Aikataulutetun päivityksen määrittäminen](/power-bi/connect-data/refresh-scheduled-refresh)

### <a name="show-reports-on-list-pages"></a>Raporttien näyttäminen luettelosivuilla

[!INCLUDE[prod_long](includes/prod_long.md)] sisältää Power BI -tietoruudun useilla tärkeillä luettelosivuilla. Tässä luetteloruudussa on lisätietoja luettelon tiedoista. Raportti päivitetään ja suodatetaan valitun tapahtuman mukaan, kun siirryt luettelon riveillä.

Lisätietoja luettelosivujen raporttien luomisesta on kohdassa [Power BI -raporttien luominen näyttämään luettelotiedot [!INCLUDE[prod_short](includes/prod_short.md)]issa](across-how-use-powerbi-reports-factbox.md).

> [!TIP]
> Jos Power BI -tietoruutu ei ole näkyvissä, se voi olla piilossa työtilassa mukautuksen avulla. Valitse ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") -kuvake ja valitse sitten **Mukauta**-toiminto. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).
>
> Tai jos käytössäsi on Business Centralin vanhempi versio, siirry toimintopalkkiin ja valitse **Toiminnot** > **Näytä** > **Näytä/Piilota Power BI -raportit**.

### <a name="switch-reports"></a>Raporttien vaihtaminen

Sivun Power BI -osassa voi näyttää minkä tahansa käytettävissä olevan Power BI -raportin. Näkyvissä olevan raportin voi vaihtaa valitsemalla **Valitse raportti** -toiminnon osan yläreunassa olevasta avattavasta komentoluettelosta.  

**Power BI -raporttien valinta** -sivulla on luettelo on kaikista käytettävissä olevista Power BI -raporteista. Tämä luettelo haetaan kaikista omista työtiloistasi tai työtiloista, jotka on jaettu sinulle Power BI -palvelussa. Valitse kaikkien niiden raporttien **Ota käyttöön** -ruutu,, jotka haluat näyttää aloitussivulla, ja valitse sitten **OK**. Palaat sivulle ja viimeinen käyttöönotettu raportti tulee näkyviin. Voit siirtyä raporttien välillä käyttämällä avattavan komentoluettelon **Edellinen**- ja **Seuraava**-komentoja.  

### <a name="get-more-reports"></a>Lisäraporttien hakeminen

Jos **Power BI -raporttien valinta** -sivulla ei näy raportteja tai jos haluamasi raportti ei ole näkyvissä, valitse **Lataa raportit**. Voit etsiä tällä toiminnolla raportteja kahdesta sijainnista: *Oma organisaatio* ja *Palvelut*.

- Siirry Power BI -palveluihin valitsemalla **Oma organisaatio**. Voit tarkastella siellä niitä organisaation raportteja, joiden tarkasteluoikeudet sinulla on. Voit sitten lisätä ne työtilaan.
- Siirry Microsoft AppSourceeen, jossa voit asentaa Power BI -sovelluksia, valitsemalla **Palvelut**.  

> [!TIP]
> Jos sinulla on Power BI Desktop, voit myös luoda uusia Power BI -raportteja. Sitten kun nämä raportit on julkaistu Power BI -työtilaan, ne näkyvät **Power BI -raporttien valinta** -sivulla.  

### <a name="manage-and-modify-reports"></a>Raporttien hallinta ja muokkaaminen

Voit tehdä muutoksia raporttiin Power BI -osassa. Tehdyt muutokset julkaistaan sitten Power BI -palveluun. Jos raportti on jaettu muiden käyttäjien kanssa, myös he näkevät muutokset paitsi siinä tapauksessa, että olet tallentanut muutokset uuteen raporttiin.

Voit muokata raporttia valitsemalla **Raportin hallinta** -toiminnon avattavasta komentoluettelosta Power BI -osassa. Tee sitten muutokset. Kun olet tyytyväinen muutoksiin valitse **Tiedosto** > **Tallenna**. Jos kyse on jaetusta raportista eikä halua tehdä muutoksia kaikille käyttäjille, valitse **Tallenna nimellä**, jolloin tehty muutos ei koske kaikkia käyttäjiä.

Kun palaat roolikeskukseen, päivitetty raportti on näkyvissä. Jos valitsit **Tallenna nimellä**, uusi raportti on näkyvissä vasta, kun valitset **Valitse raportti** ja otat uuden raportin käyttöön.

> [!NOTE]
> Tämä ominaisuus ei ole käytettävissä paikallisessa [!INCLUDE [prod_short](includes/prod_short.md)] -versiossa.

### <a name="upload-reports"></a><a name="upload"></a>Raporttien lataaminen palvelimeen

Power BI -raportteja voi jakaa käyttäjille .pbix-tiedostoina. Jos sinulla on .pbix-tiedostoja, voit ladata ja jakaa ne kaikkien [!INCLUDE [prod_short](includes/prod_short.md)] -käyttäjien kanssa. Raportit jaetaan kussakin [!INCLUDE [prod_short](includes/prod_short.md)] -yrityksessä.  

Lataa raportti valitsemalla **Lataa raportti** -toiminto avattavasta komentoluettelosta **Power BI -raportit** -osassa. Etsi sitten .pbix-tiedosto, joka määrittää jaettavat raportit. Voit muuttaa tiedoston oletusnimeä.  

Kun raportti on latautunut Power BI -työtilaan, se latautuu automaattisesti muiden käyttäjien Power BI -työtiloihin.

> [!NOTE]
> Raportin lataaminen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman kautta edellyttää in SUPER-käyttäjän oikeuksia [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Et tarvitse erityislupaa raporttien lataamiseen työtilaan Power BI -palvelun kautta.

## <a name="upload-reports-from-files"></a><a name="upload"></a>Raporttien lataaminen tiedostoista

Power BI -raportteja voi jakaa käyttäjille .pbix-tiedostoina. .pbix-tiedoston voi puolestaan ladata työtilaan. Raportti ladataan seuraavasti:

1. Valitse uudessa työtilassa **Nouda tiedot**.

2. Valitse Tiedostot-ruudussa **Hae**.

3. Valitse **Paikallinen tiedosto**, siirry tiedoston tallennussijaintiin ja valitse **Avaa**.

Lisätietoja on kohdassa [Raportin lataaminen palveluun](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). -->

> [!TIP]
> Jos käytössä on [!INCLUDE[prod_short](includes/prod_short.md)] online, raportin voi ladata myös [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Power BI -raporttien käyttäminen [!INCLUDE [prod_short](includes/prod_short.md)]issa – raporttien lataaminen palvelimeen](across-working-with-powerbi.md#upload).

## <a name="share-reports-with-others"></a><a name="share"></a>Raporttien jakaminen muiden kanssa

Kun raportti on työtilassa, sen voi jakaa organisaatiossa muiden kanssa.

Voit jakaa raportin valitsemalla raporttiluettelossa tai avoimessa raportissa **Jaa**. Anna **Jaa raportti** -ruudussa niiden henkilöiden tai jakeluryhmien täydellinen sähköpostiosoite, joiden kanssa haluat jakaa raportin. Suorita jakaminen loppuun näytön ohjeiden mukaisesti. Lisätietoja on kohdassa [Koontinäytön tai raportin jakaminen](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Sekä sinulla että henkilöillä, joiden kanssa jaat raportin, on oltava [Power BI Pro -käyttöoikeus](/power-bi/service-features-license-type). Muussa tapauksessa sisällön on oltava [Premium-kapasiteettina](/power-bi/service-premium-what-is). Lisätietoja on kohdassa [Työn jakaminen Power BI:ssä](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## <a name="fixing-problems"></a>Ongelmien korjaaminen

Tämä osa sisältää ratkaisun tyypillisempiin ongelmiin.  

### <a name="you-dont-have-a-power-bi-account"></a>Power BI -tiliä ei ole

Power BI -tiliä ei ole määritetty. Kelvollisen Power BI -tilin saaminen edellyttää, että sinulla on käyttöoikeus ja että olet aiemmin kirjautunut Power BI:hin luomaan Power BI -työtilan.

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Sanoma: Käyttöönotettuja raportteja ei ole. Valitsemalla Valitse raportti saat näkyviin luettelon raporteista, joita voit tarkastella.

Tämä sanoma avautuu, jos oletusraporttia ei voitu ottaa käyttöön Power BI -työtilassa. Vaihtoehtoisesti se otettiin käyttöön mutta sen päivittäminen epäonnistui. Siirry raporttiin Power BI -työtilassa, valitse **Tietojoukko**, **Asetukset** ja päivitä sitten tunnistetiedot manuaalisesti. Kun tietojoukko on päivitetty, siirry takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin ja valitse raportti manuaalisesti **Valitse raportit** -sivulla.

#### <a name="you-cant-see-a-report-on-the-select-report-page-on-a-list-page"></a>Raportti ei näy luettelosivun Valitse raportti -sivulla

Syynä luultavasti se, että raportin nimi ei sisällä luettelosivun nimeä. Saat näkyviin luettelon kaikista Power BI:ssa käytettävistä raporteista tyhjentämällä suodattimen.

## <a name="see-also"></a>Katso myös

[Business Central ja Power BI](admin-powerbi.md)    
[Power BI -raporttien luominen näyttämään [!INCLUDE [prod_long](includes/prod_long.md)] -tietoja](across-how-use-financials-data-source-powerbi.md)    
[Power BI:in -integrointiosa ja arkkitehtuurin yleiskatsaus [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmalle](admin-powerbi-overview.md)    
[Yhdistä Power BI:hin paikallisesta [!INCLUDE [prod_short](includes/prod_short.md)] -versiosta](across-working-with-business-central-in-powerbi.md)    
[Power BI kuluttajille](/power-bi/consumer/end-user-consumer)     
[Power BI-palvelun uusi ulkoasu](/power-bi/service-new-look)    
[Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin](/power-bi/desktop-quickstart-connect-to-data)    
[Power BI -dokumentaatio](/power-bi/)    
[Business Intelligence](bi.md)    
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)    
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)    
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)    
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen Power BI:n tietolähteenä](across-how-use-financials-data-source-powerapps.md)    
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen Power Appsin tietolähteenä](across-how-use-financials-data-source-powerapps.md)    
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen Power Automatessa](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
