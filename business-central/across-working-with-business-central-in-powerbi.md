---
title: 'Yhdistä Power BI:hin paikallisesta Business Centralista | Microsoft Docs'
description: 'Merkityksellisten tietojen, liiketoimintatietoja ja tunnuslukujen saaminen Business Central -tiedoista Power BI:n avulla.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/22/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Yhdistä Power BI:hin paikallisesta Business Centralista

<!--In this article, you learn some of the basics about working with reports and dashboards in Power BI that use [!INCLUDE [prod_short](includes/prod_short.md)] as a data source. The article discusses some aspects that will help you get started as a [!INCLUDE[prod_short](includes/prod_short.md)] user. For general guidelines and instructions about using Power BI, see [Power BI documentation for consumers](/power-bi/consumer).

## Get ready

Sign up for the Power BI service. If you haven't already signed up, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). When you sign up, use a work email address and password.-->

## Aloittaminen

Käyttääksesi paikallista [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa, Power BI -integraation on oltava siinä käytössä. Yleensä järjestelmänvalvoja tekee tämän tehtävän. Lisätietoja Business Central Onlinen Power BI -integraation käyttöönotosta internetissä on kohdassa [Business Centralin määrittäminen yrityksen tiloissa Power BI -integrointia varten](admin-powerbi-setup.md).

Osa ominaisuuksista on käytössä vain Business Central Online -versiossa mutta ei paikallisessa versiossa. Lisätietoja, katso [Tietoja Business Centralista ja Power BI:stä](admin-powerbi.md#what-you-can-do-with-power-bi-and-business-central)

## <a name="setup"></a>Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -version Power BI -integroinnin valmistelu

Tässä osassa käsitellään paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -käyttöönoton edellytyksiä Power BI -integrointia varten.

1. Määritä joko [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) tai [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) käyttöönoton todennusmenetelmäksi.  
    
    > [!NOTE]
    > Power BI -integrointi ei tue Windows-todennusta eikä sitä tueta Windows-asiakasohjelmassa.

2. Ota OData-verkkopalvelut ja ODataV4-päätepiste käyttöön.

    OData-verkkopalvelu on otettava käyttöön [!INCLUDE[server](includes/server.md)]issä ja OData-portti avattava palomuurissa. Lisätietoja on kohdassa [Business Central Serverin määrittäminen – OData-verkkopalvelut](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Internet-yhteys on voitava muodostaa paikalliseen palvelimeen.

3. Anna [!INCLUDE[prod_short](includes/prod_short.md)] -käyttäjätileille verkkopalvelun käyttöoikeusavain.

    Verkkopalvelun käyttöoikeusavain tarvitaan vain [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen tarkastelemiseen Power BI:ssa. Verkkopalvelun käyttöoikeusavain voidaan määrittää kullekin käyttäjätilille. Vaihtoehtoisesti voidaan luoda tietty tili, jonka verkkopalvelun käyttöoikeusavainta kaikki käyttäjät voivat käyttää. Lisätietoja on kohdassa [Verkkopalvelujen todennus](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Luo sovelluksen rekisteröinti [!INCLUDE[prod_short](includes/prod_short.md)]ille Microsoft Azuressa.

    [!INCLUDE[prod_short](includes/prod_short.md)] -sivuille upotettujen Power BI -raporttien näyttämistä varten sovellus on rekisteröitävä [!INCLUDE[prod_short](includes/prod_short.md)]ia varten Microsoft Azuressa. Rekisteröity sovellus tarvitsee Power BI -palvelujen käyttöoikeuden. Sovellus vaatii vähintään **User.ReadWrite.All**-käyttöoikeuden. Jotta käyttäjät voivat tarkastella raportteja jaetuissa Power BI -työtiloissa, sovellus tarvitsee **Workspace.Read.All**-käyttöoikeuden. Lisätietoja on kohdassa [Paikallisen [!INCLUDE[prod_short](includes/prod_short.md)] -version rekisteröinti Microsoft Entra ID:ssä muiden palvelujen integrointia varten](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Jos käyttöönotto käyttää NavUserPassword-todennusta, [!INCLUDE[prod_short](includes/prod_short.md)] muodostaa yhteyden samaan Power BI -palveluun kaikilla käyttäjillä. Tämä palvelu määritetään sovelluksen rekisteröinnin yhteydessä. Microsoft Entra -todennuksessa [!INCLUDE[prod_short](includes/prod_short.md)] muodostaa yhteyden yksittäisiin käyttäjätileihin liitettyyn Power BI -palveluun.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Luo ensimmäinen yhteys Business Centralista Power BI -palveluun.

    Ennen kuin loppukäyttäjät voivat käyttää Power BI:tä [!INCLUDE[prod_short](includes/prod_short.md)]issa, Azure-sovelluksen järjestelmänvalvojan täytyy antaa suostumuksensa Power BI-palvelulle.

    Voit muodostaa ensimmäisen yhteyden avaamalla [!INCLUDE[prod_short](includes/prod_short.md)]in ja suorittamalla aloitussivulla **Aloita Power BI:n käyttö** -toiminnon. Tämä toiminto opastaa hyväksyntäprosessin läpi ja tarkistaa Power BI -käyttöoikeutesi. Ohjelma pyytää kirjautumaan sisään käyttämällä Microsoft Entra -järjestelmänvalvojatiliä. Lisätietoja on kohdassa [Power BI -yhteyden muodostaminen – kerran](across-working-with-powerbi.md#connect).

## Power BI -raporttien luominen näyttämään [!INCLUDE [prod_long](includes/prod_long.md)] -tietoja

Voit määrittää Dynamics 365 Business Centralin tiedot käytettäviksi Power BI Desktop:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten.

Käytä Power BI Desktopia luodaksesi raportteja, jotka näyttävät Dynamics 365 Business Central -tietoja. Kun raportit on luotu, voit julkaista ne Power BI -palveluun tai jakaa ne organisaation kaikkien käyttäjien kanssa. Kun nämä raportit ovat Power BI -palvelussa, käyttäjät, joilla on raporttien tarkasteluoikeudet, voivat tarkastella niitä Dynamics 365 Business Centralissa.

- Paikallista [!INCLUDE[prod_short](includes/prod_short.md)] -versiota varten tarvitaan seuraavat tiedot:

  - [!INCLUDE[prod_short](includes/prod_short.md)]in ODatan URL-osoite.
  
    Tämän URL-osoitteen muoto on yleensä `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, kuten `https://localhost:7048/BC190/ODataV4`. Jos kyse on monen vuokraajan käyttöönotossa, URL-osoitteen on sisällettävä vuokraaja, kuten `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - [!INCLUDE[prod_short](includes/prod_short.md)] -tilin käyttäjänimi ja verkkopalvelun käyttöoikeusavain.

    Power BI käyttää perustodennusta [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen hakemiseen. Yhteyttä varten tarvitaan tämän vuoksi käyttäjänimi ja verkkopalvelun käyttöoikeusavain. Tili voi olla oma käyttäjänimi. Organisaatiolla voi olla myös erillinen tili tätä tarkoitusta varten.

## <a name="getdata"></a>[!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen Power BI Desktopin tietolähteeksi

Raporttien luomisen ensimmäinen tehtävä on [!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen Power BI Desktopin tietolähteeksi. Raportin luonnin voi aloittaa, kun yhteys on muodostettu.

1. Käynnistä Power BI Desktop.
2. Valitse **Nouda tiedot**.

    Jos **Nouda tiedot** ei ole näkyvissä, valitse ensin **Tiedosto** ja sitten **Nouda tiedot**.
3. Valitse **Nouda tiedot** -sivulla **Verkkopalvelut**.
4. Muodosta yhteys paikalliseen [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan valitsemalla **Dynamics 365 Business Central (paikallinen)** **Verkkopalvelut**-kohdassa ja sitten **Yhdistä**.
5. Kirjaudu sisään [!INCLUDE [prod_short](includes/prod_short.md)]iin (vain kerran).

    Jos et ole aiemmin kirjautunut sisään [!INCLUDE [prod_short](includes/prod_short.md)]iin Power BI desktopista, sinua pyydetään kirjautumaan sisään.

   - Paikallisessa [!INCLUDE [prod_short](includes/prod_short.md)]issa syötä ensin [!INCLUDE[prod_short](includes/prod_short.md)]in OData-URL-osoite ja valitse sitten **OK**. Anna pyydettäessä sen tilin käyttäjänimi ja salasana, jolla muodostetaan yhteys [!INCLUDE[prod_short](includes/prod_short.md)]iin. Anna **Salasana**-ruudussa verkkopalvelun käyttöoikeusavain. Kun olet valmis, valitse **Yhdistä**.
   
    > [!NOTE]  
    > Kun yhteys [!INCLUDE[prod_short](includes/prod_short.md)]iin on muodostettu, sinua ei pyydetä kirjautumaan uudelleen. [Miten muutan tai tyhjennän tilin, jota tällä hetkellä käytän yhteyden muodostamiseen Business Centraliin Power BI Desktopista?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Kun yhteys on muodostettu, Power BI muodostaa yhteyden Business Central -palveluun. **Navigator**-ikkunat tulevat näkyviin ja näyttävät käytettävissä olevat tietolähteet raporttien rakentamista varten. Laajenna kansio valitsemalla se ja tarkastele käytettävissä olevia tietolähteitä. 

   Nämä tietolähteet viittaavat kaikkiin [!INCLUDE [prod_short](includes/prod_short.md)]iin julkaistuihin verkkopalveluihin ja API-sivuihin. Tietolähteet on ryhmitelty Business Central -ympäristöjen ja yritysten mukaan.

   > [!NOTE]
    > Paikallisen Business Centralin rakenne on erilainen, koska se ei tue API-sivuja.

7. Valitse tietomalliin lisättävä tietolähde tai lisättävät tietolähteet ja valitse sitten **Lataa**-painike.
8. Jos haluat myöhemmin lisätä Business Central -tietoja, voit toistaa edelliset vaiheet.

Kun tiedot on ladattu, ne näkyvät sivun oikeassa siirtymisruudussa. Olet nyt muodostanut yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] -tietoihin ja voit aloittaa Power BI -raportin luomisen.  

> [!TIP]
> Lisätietoja Power BI Desktopin käytöstä on kohdassa [Power BI Desktopin käytön aloittaminen](/power-bi/fundamentals/desktop-getting-started).

## Raporttien hallinta ja muokkaaminen

> [!NOTE]
> Et voi hallita ja muokata raportteja. 

## Raporttien lataaminen palvelimeen

Paikallisissa [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmissa ei ole käytettävissä demoraportteja, joten aloitat alusta käyttämällä Power BI Desktopia. Vaihtoehtoiesti Power BI -raportit voidaan jakaa palvelimeen ladattavina tiedostoina suoraan Power BI -verkkopalvelusta. Lisätietoja on kohdassa [Raportin lataaminen palveluun](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have SUPER user permissions in [!INCLUDE[prod_short](includes/prod_short.md)]. Also, you can't upload reports with [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. With on-premises, you upload reports directly to your Power BI workspace. For more information, see [Connect to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md).

<!--Once you have a Power BI account, you can sign in at [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

The Power BI service hosts all the reports available to you. To see the report, select **My Workspace** > **Reports**. Then just select the report that you want to view.

With [!INCLUDE[prod_short](includes/prod_short.md)] online, you'll automatically have a set of default reports on your workspace. If you want to create your own reports, you can use Power BI Desktop to create reports, and then publish them to your workspace. For more information, see [Getting Started Building Reports in Power BI Desktop to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, you'll have to start from scratch by using Power BI Desktop. Optionally, Power BI reports can be distributed as files, that you can upload.

<!--## Get the latest data

Each Power BI report is based on a dataset that gets data from the [!INCLUDE[prod_short](includes/prod_short.md)] sources. You want to make sure that the data in your Power BI reports is up to date with the data in [!INCLUDE[prod_short](includes/prod_short.md)]. This concept is referred to as *refreshing*.  Depending on how your organization has set up Power BI, refreshing might not happen automatically. There are two ways to refresh data: manually or by scheduling a refresh. Manual refreshing is done on-demand, as needed. Scheduled refreshing lets you refresh automatically at defined time intervals.

### Refresh manually

In the navigation pane, under **Datasets**, select **More options (...)** next to the dataset, then select **Refresh now**.

### Schedule a refresh

In the navigation pane, under Datasets, select More options (...) next to the dataset, then select **Schedule refresh**. Fill in the information under the **Schedule refresh** section, and select **Apply**.

For more information, see [Configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh)-->

<!--## <a name="upload"></a>Upload reports from files

Power BI Reports can be distributed among users as .pbix files. If you have a .pbix file, you can upload the file to a workspace. To upload a report, do the following steps:

1. In your new workspace, select **Get Data**.

2. In the Files box, select **Get**.

3. Select **Local File**, navigate to where you saved the file, and select **Open**.

For more information, see [Upload the report to the service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> If you're using [!INCLUDE[prod_short](includes/prod_short.md)] online, you can also upload a report from within [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Work with Power BI Reports in [!INCLUDE [prod_short](includes/prod_short.md)] - Upload Reports](across-working-with-powerbi.md#upload).

## <a name="share"></a>Share reports with others

Once a report is in your workspace, you can share it with others in your organization.

To share a report, in a list reports, or in an open report, select **Share**. In the **Share report** pane, enter the full email addresses for individuals or distribution groups you want to share with. Follow the instructions on screen to complete the sharing. For more information, see [Share a dashboard or report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> You must have  [Power BI Pro license](/power-bi/service-features-license-type), and the people you share with do too. The content must be in a workspace in a [Premium capacity](/power-bi/service-premium-what-is). For more information, see [Ways to share your work in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).-->

## Katso myös

[Business Central ja Power BI](admin-powerbi.md)  
[Raportin lataaminen tiedostoista](across-working-with-powerbi.md#upload-reports)  
 
[!INCLUDE[footer-include](includes/footer-banner.md)]
