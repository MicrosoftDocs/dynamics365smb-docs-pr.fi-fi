---
title: Sovelluksen luominen omista tiedoista| Microsoft Docs
description: "Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla luot PowerApps-sovelluksen avulla yrityssovelluksen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d7738991133baac735586fd7e25b0d9866a3a42f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten PowerApps-sovellusten avulla
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoja PowerAppsin tietolähteenä.  

> [!NOTE]  
>   Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja PowerApps-tili.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen PowerAppsin tietolähteeksi
1. Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) ja kirjaudu sisään.
2. Valitse vasemmassa siirtymisruudussa **Uusi sovellus**.
3. Valitse editori: joko Windowsin PowerApps Studio tai Verkon PowerApps Studio.

   Windowsin PowerApps Studio on työpöytäsovellus, jolla luodaan ja julkaistaan PowerApp-sovelluksia. Verkon PowerApps Studio on verkkoratkaisu, jolla luodaan ja julkaistaan PowerApp-sovelluksia.
4. PowerApp-sovelluksen luonnin seuraavana vaiheena on tietojen valinta. Valitse sivun vasemmassa yläosassa ensin nuolikuvake ja sitten **Uusi yhteys** -asetus.
5. Valitse käytettävissä olevien yhteyksien luettelosta **Dynamics 365 Business Central**.
6. PowerApps näyttää yhteyssivun, joka kysyy sinulta tietoja, jotka on yhdistettävä [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoihin. Yhteyttä varten on määritettävä ODatan URL-osoite, käyttäjänimi, salasana ja yrityksen nimi.

   Voit kopioida *OData URL* -osoitteeksi minkä tahansa [!INCLUDE[d365fin](includes/d365fin_md.md)]in **WWW-palvelut**-ikkunassa mainitun verkkopalvelun OData V4 URL-osoitteen, kuten `https://mycompany.businesscentral.dynamics.com:7048/MS/ODataV4/`.  

   Käytä *yrityksen nimenä* nimeä, joka näkyy [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Oman yrityksen tiedot** -ikkunan **Nimi**-kentässä. Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on useita yrityksiä, valitse sopiva yrityksen nimi **Yritykset**-ikkunassa olevasta luettelosta. Varmista kummassakin tapauksessa, että ohjatussa PowerApps-toiminnossa määrittämäsi nimi on kirjoitettu täsmälleen samoin kuin [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Esimerkki: `My Company`.

   Käytä käyttäjänimenä ja salasanana tilille [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Käyttäjät**-ikkunassa määritettyä nimeä ja verkkopalvelun käyttöoikeusavainta. Käyttäjänimesi on esimerkiksi *JÄRJESTELMÄNVALVOJA* ja salasanana toimiva verkkopalvelun käyttöoikeusavain on *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Jatka valitsemalla **Yhteys**-painike. PowerApps näyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in oletustietojoukon. Valitse **Oletus**-tietojoukko.

   PowerApps näyttää luettelon taulukoista, joita voi käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Nämä taulukot tai päätepisteet viittaavat kaikkiin [!INCLUDE[d365fin](includes/d365fin_md.md)]ista julkaistuihin verkkopalveluihin.

   Voit vaihtoehtoisesti luoda uuden verkkopalvelun URL-osoitteen [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa käyttämällä **Luo tietojoukko** -toimintoa **WWW-palvelut**-ikkunassa tai asetusten ohjattua **Määritä raportointi** -määritystä tai valitsemalla **Muokkaa Excelissä** -toiminnon jossakin luettelossa.
8. Valitse ensin PowerApp-sovelluksessa käytettävä taulukko ja sitten **Yhteys**-painike.
9. Lisää muita [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoja Power BI -tietomalliin toistamalla edellä olevat vaiheet.

   > [!NOTE]  
   >    Kun [!INCLUDE[d365fin](includes/d365fin_md.md)] -yhteys on muodostettu, ODatan URL-osoitetta, käyttäjänimeä tai salasanaa ei enää kysytä.

Olet nyt muodostanut yhteyden Business Central -tietoihin ja olet valmis aloittamaan oman PowerApp:n luomisen. Lisätietoja on kohdassa [PowerApps-dokumentaatio](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>Katso myös
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  

