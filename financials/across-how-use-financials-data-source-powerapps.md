---
title: "Dynamics 365 for Financialsin käyttäminen PowerAppsin tietolähteenä | Microsoft Docs"
description: "Voit käyttää Financials-tietoja PowerAppsin tietolähteenä."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 12/02/2016
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: cedc95b23481b8cb76da85e8459a97b1880a4218
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-as-a-powerapps-data-source"></a>Dynamics 365 for Financialsin käyttäminen PowerAppsin tietolähteenä
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoja PowerAppsin tietolähteenä.  

**Huomautus**: sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja PowerApps-tili.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen PowerAppsin tietolähteeksi
1. Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) ja kirjaudu sisään.
2. Valitse vasemmassa siirtymisruudussa **Uusi sovellus**.
3. Valitse editori: joko Windowsin PowerApps Studio tai Verkon PowerApps Studio.

   Windowsin PowerApps Studio on työpöytäsovellus, jolla luodaan ja julkaistaan PowerApp-sovelluksia. Verkon PowerApps Studio on verkkoratkaisu, jolla luodaan ja julkaistaan PowerApp-sovelluksia.
4. PowerApp-sovelluksen luonnin seuraavana vaiheena on tietojen valinta. Valitse sivun vasemmassa yläosassa ensin nuolikuvake ja sitten **Uusi yhteys** -asetus.
5. Valitse käytettävissä olevien yhteyksien luettelossa **Dynamics 365 for Financials**.
6. PowerApps näyttää yhteyssivun, joka kysyy sinulta tietoja, jotka on yhdistettävä [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoihin. Yhteyttä varten on määritettävä ODatan URL-osoite, käyttäjänimi, salasana ja yrityksen nimi.

   Voit kopioida *OData URL* -osoitteeksi minkä tahansa [!INCLUDE[d365fin](includes/d365fin_md.md)]in **WWW-palvelut**-sivulla mainitun verkkopalvelun OData V4 URL-osoitteen, kuten `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Käytä *yrityksen nimenä* nimeä, joka näkyy [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Oman yrityksen tiedot** -ikkunan **Nimi**-kentässä. Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on useita yrityksiä, valitse sopiva yrityksen nimi **Yritykset**-ikkunassa olevasta luettelosta. Varmista kummassakin tapauksessa, että ohjatussa PowerApps-toiminnossa määrittämäsi nimi on kirjoitettu täsmälleen samoin kuin [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Esimerkki: `My Company`.

   Käytä käyttäjänimenä ja salasanana tilille [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Käyttäjät**-ikkunassa määritettyä nimeä ja verkkopalvelun käyttöoikeusavainta. Käyttäjänimesi on esimerkiksi *JÄRJESTELMÄNVALVOJA* ja salasanana toimiva verkkopalvelun käyttöoikeusavain on *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Jatka valitsemalla **Yhteys**-painike. PowerApps näyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in oletustietojoukon. Valitse **Oletus**-tietojoukko.

   PowerApps näyttää luettelon taulukoista, joita voi käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Nämä taulukot tai päätepisteet viittaavat kaikkiin [!INCLUDE[d365fin](includes/d365fin_md.md)]ista julkaistuihin verkkopalveluihin.

   Voit vaihtoehtoisesti luoda uuden verkkopalvelun URL-osoitteen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käyttämällä **Luo tietojoukko** -toimintoa **WWW-palvelut**-sivulla tai avustettua **Määritä raportointi** -asetusopasta tai valitsemalla **Muokkaa Excelissä** -toiminnon missä tahansa luettelossa.
8. Valitse ensin PowerApp-sovelluksessa käytettävä taulukko ja sitten **Yhteys**-painike.
9. Lisää muita [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoja Power BI -tietomalliin toistamalla edellä olevat vaiheet.

   **Huomautus**: kun [!INCLUDE[d365fin](includes/d365fin_md.md)]-yhteys on muodostettu, ODatan URL-osoitetta, käyttäjänimeä tai salasanaa ei enää kysytä.

Olet nyt muodostanut yhteyden Dynamics 365 -tietoihin ja olet valmis aloittamaan oman PowerApp-sovelluksen luomisen. Lisätietoja on kohdassa [PowerApps-dokumentaatio](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>Katso myös
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin](index.md)  
[Yritystietojen tuonti muista rahoitusjärjestelmistä] (upload-data.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  

