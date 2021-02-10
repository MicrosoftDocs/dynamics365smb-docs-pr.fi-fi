---
title: Raporttien luominen Power BI Desktopissa näyttämään Business Central -tietoja | Microsoft Docs
description: Määritä tiedot käytettäviksi Power BI:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: ce1ce3039758d5991eb3a770713d2f1e273bbe0c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754515"
---
# <a name="building-power-bi-reports-to-display-prod_long-data"></a>Power BI -raporttien luominen näyttämään [!INCLUDE [prod_long](includes/prod_long.md)] -tietoja

Voit määrittää [!INCLUDE[prod_long](includes/prod_long.md)]in tiedot käytettäviksi Power BI Desktop:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten.

Tässä artikkelissa käsitellään Power BI Desktopin käytön aloittamista luomaan [!INCLUDE[prod_long](includes/prod_long.md)] -tiedot näyttäviä raportteja.  Kun raportit on luotu, voit julkaista ne Power BI -palveluun tai jakaa ne organisaation kaikkien käyttäjien kanssa. Kun nämä raportit ovat Power BI -palvelussa, käyttäjät, joilla on raporttien tarkasteluoikeudet, voivat tarkastella niitä [!INCLUDE[prod_long](includes/prod_long.md)]issa.

## <a name="get-ready"></a>Valmistelut

- Rekisteröidy Power BI -palveluun.

    Jos et ole vielä rekisteröitynyt, siirry osoitteeseen [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Käytä rekisteröityessä työpaikan sähköpostiosoitetta ja salasanaa.

- Lataa [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

   Power BI Desktop on maksuton tietokoneeseen paikallisesti asennettava sovellus. Lisätietoja on kohdassa [Pika-aloitus: Power BI Desktopin tietoihin yhdistäminen](/power-bi/desktop-quickstart-connect-to-data).

- Varmista, että raportissa käytettävät tiedot julkaistaan verkkopalveluna.
    
    Useita verkkopalveluja julkaistaan oletusarvoisesti. Verkkopalveluja voi etsiä kätevästi hakemalla *verkkopalveluja* [!INCLUDE[prod_short](includes/prod_short.md)]issa. Varmista, että **Julkaise**-kenttä on valittu **Verkkopalvelut**-sivulla. Tämä on yleensä järjestelmänvalvojan tehtävä.
    
    Lisätietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

- Paikallista [!INCLUDE[prod_short](includes/prod_short.md)] -versiota varten tarvitaan seuraavat tiedot:

    - [!INCLUDE[prod_short](includes/prod_short.md)]in ODatan URL-osoite. Tämän URL-osoitteen muoto on yleensä `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, kuten `https://localhost:7048/BC160/ODataV4`. Jos kyse on monen vuokraajan käyttöönotossa, URL-osoitteen on sisällettävä vuokraaja, kuten `https://localhost:7048/BC160/ODataV4?tenant=tenant1`.
    - [!INCLUDE[prod_short](includes/prod_short.md)] -tilin käyttäjänimi ja verkkopalvelun käyttöoikeusavain.

      Power BI käyttää perustodennusta [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen hakemiseen. Yhteyttä varten tarvitaan tämän vuoksi käyttäjänimi ja verkkopalvelun käyttöoikeusavain. Tili voi olla oma käyttäjänimi. Organisaatiolla voi olla myös erillinen tili tätä tarkoitusta varten.

- Lataa [!INCLUDE [prod_short](includes/prod_short.md)] -raportin teema (valinnainen).

    Lisätietoja on tämän artikkelin kohdassa [[!INCLUDE [prod_short](includes/prod_short.md)] -raportin teeman käyttäminen](#theme).

## <a name="add-prod_short-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen Power BI Desktopin tietolähteeksi

Raporttien luomisen ensimmäinen tehtävä on [!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen Power BI Desktopin tietolähteeksi. Raportin luonnin voi aloittaa, kun yhteys on muodostettu.

1. Käynnistä Power BI Desktop.
2. Valitse **Nouda tiedot**.

    Jos **Nouda tiedot** ei ole näkyvissä, valitse ensin **Tiedosto** ja sitten **Nouda tiedot**.
2. Valitse **Nouda tiedot** -sivulla **Verkkopalvelut**.
3. Tee **Verkkopalvelut**-ruudussa jokin seuraavista:

    1. Jos muodostat yhteyttä [!INCLUDE [prod_short](includes/prod_short.md)] online -versioon, valitse ensin **Dynamics 365 Business Central** ja sitten **Muodosta yhteys**.
    2. Jos muodostat yhteyttä paikalliseen [!INCLUDE [prod_short](includes/prod_short.md)] -versioon, valitse ensin **Dynamics 365 Business Central (on-premises)** ja sitten **Muodosta yhteys**.

4. Power BI avaa ohjatun toiminnon, joka auttaa yhteyden muodostusprosessissa. Tähän kuuluu myös sovellukseen [!INCLUDE [prod_short](includes/prod_short.md)] kirjautuminen.

    Valitse online-versiossa **Kirjaudu sisään** ja valitse sitten tili. Käytä samaa tiliä, jolla kirjaudut [!INCLUDE [prod_short](includes/prod_short.md)]iin.
    
    Anna paikallisessa versiossa [!INCLUDE[prod_short](includes/prod_short.md)]in ODatan URL-osoite ja valinnaisesti yrityksen nimi. Anna sitten pyydettäessä sen tilin käyttäjänimi ja salasana, jolla muodostetaan yhteys [!INCLUDE[prod_short](includes/prod_short.md)]iin. Anna **Salasana**-ruudussa verkkopalvelun käyttöoikeusavain.

    > [!NOTE]  
    > Kun yhteys [!INCLUDE[prod_short](includes/prod_short.md)]iin on muodostettu, sinua ei pyydetä kirjautumaan uudelleen.
    
5. Jatka valitsemalla **Muodosta yhteys**.

    Ohjatussa Power BI -toiminnossa on luettelo Microsoft [!INCLUDE[prod_short](includes/prod_short.md)]:n ympäristöistä, yrityksistä ja tietolähteistä. Nämä tietolähteet viittaavat kaikkiin [!INCLUDE [prod_short](includes/prod_short.md)]iin julkaistuihin verkkopalveluihin.
6. Määritä tietomalliin lisättävät tiedot ja valitse sitten **Lataa**-painike.
7. Lisää uusia [!INCLUDE [prod_short](includes/prod_short.md)]in tai muita tietoja Power BI -tietomalliin toistamalla edellä olevat vaiheet.

Kun tiedot on ladattu, ne näkyvät sivun oikeassa siirtymisruudussa. Olet nyt muodostanut yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] -tietoihin ja voit aloittaa Power BI -raportin luomisen.  

> [!TIP]
> Lisätietoja Power BI Desktopin käytöstä on kohdassa [Power BI Desktopin käytön aloittaminen](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Raporttien luominen näyttämään luetteloon liitetyt tiedot

Voit luoda [!INCLUDE [prod_short](includes/prod_short.md)] -luettelosivun tietoruudussa näytettäviä raportteja. Raporteissa voi olla tietoja luettelossa valitusta tietueesta. Vaikka näiden raporttien luominen muistuttaa muiden raporttien luontia, raporttien näkyminen odotetusti edellyttää muutamia toimintoja. Lisätietoja on kohdassa [Power BI -raporttien luominen näyttämään luettelotietoja [!INCLUDE[prod_short](includes/prod_short.md)]issa](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the-prod_short-report-theme-optional"></a><a name="theme"></a>[!INCLUDE [prod_short](includes/prod_short.md)] -raportin teeman käyttäminen (valinnainen)

[!INCLUDE [prod_short](includes/prod_short.md)] -teematiedosto kannattaa ladata ja tuoda ennen raportin luontia. Teematiedosto luo värivalikoiman, jonka avulla voit luoda raportteja samalla värityylillä kuin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksissa ilman, että kunkin visuaalisen ominaisuuden mukautetut värit on määritettävä erikseen.

> [!NOTE]
> Tämä tehtävä on valinnainen. Voit aina luoda omia raportteja ja ladata ja käyttää tyylimallia myöhemmin.

### <a name="download-the-theme"></a>Teeman lataaminen

Teematiedosto on saatavana json-tiedostona Microsoft Power BI -yhteisön teemavalikoimassa. Teematiedosto ladataan seuraavasti:

1. Siirry [Microsoft Dynamics 365 Business Centralin Microsoft Power BI -yhteisön teemavalikoimaan](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Valitse ladattava liite **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report"></a>Teeman tuominen raporttiin

Kun [!INCLUDE [prod_short](includes/prod_short.md)] -raportin teema on ladattu, voit luoda sen raportteihin. Tuo teema valitsemalla **Näkymä** > **Teema** > **Teemojen selaus**. Lisätietoja on kohdassa [Power BI Desktop – mukautettujen raportin teemojen tuominen](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Raporttien julkaiseminen

Kun raportti on luotu tai sitä on muokattu, voit julkaista raportin Power BI -palveluun sekä jakaa sen organisaatiossa muiden kanssa. Raportti näkyy julkaisun jälkeen Power BI:ssa. Raportti on lisäksi valittavana [!INCLUDE[prod_short](includes/prod_short.md)]issa.

Voit julkaista raportin valitsemalla **Julkaise** valintanauhan **Aloitus**-välilehdessä tai **Tiedosto**-valikossa. Jos olet kirjautunut Power BI -palveluun, raportti on julkaistava tähän palveluun. Muussa tapauksessa sinua pyydetään kirjautumaan sisään. 

## <a name="distribute-or-share-a-report"></a>Raportin jakaminen tai jakelu

Raportit voi toimittaa työtovereille ja muille kahdella tavalla:

- Raporttien jakaminen .pbix-tiedostoina.

    Raportit tallennetaan tietokoneeseen .pbix-tiedostoina. Voit jakaa raportin käyttäjille .pbix-tiedostona muiden tiedostojen tavoin. Käyttäjät voivat sitten ladata tiedoston Power BI -palveluun. Lisätietoja on kohdassa [Raporttien lataaminen tiedostoista](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > Kun raportit jaetaan tällä tavoin, kukin käyttäjä päivittää raportin tiedot itse. Tämä voi vaikuttaa [!INCLUDE[prod_short](includes/prod_short.md)]in suorituskykyyn.

- Raporttien jakaminen Power BI -palvelusta

    Jos sinulla on Power BI Pro -käyttöoikeus, voit jakaa raportin muille suoraan Power BI -palvelusta. Lisätietoja on kohdassa [Power BI – koontinäytön tai raportin jakaminen](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Yritystietojen ottaminen käyttöön Power BI:tä varten](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  
[Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin](/power-bi/desktop-quickstart-connect-to-data)  
