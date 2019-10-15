---
title: Sovelluksen luominen omista tiedoista| Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla luot PowerAppsin avulla yrityssovelluksen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305019"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten PowerAppsin avulla
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietoja PowerAppsin tietolähteenä.  

> [!NOTE]  
>   Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja PowerApps -tili.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen PowerAppsin tietolähteeksi
1. Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) ja kirjaudu sisään.
2. Luo uusi kaaviosovellus valitsemalla aloitussivulla **Sovellukset**, **Luo sovellus** ja **Kangas**. Tämä sovellus suunnitellaan mobiililaitekäyttöön, mutta voit valita myös toisenlaisen mallin.

    PowerApp-sovelluksen luonnin seuraavana vaiheena on tietojen valinta. Valitse sivun vasemmassa yläosassa ensin nuolikuvake ja sitten **Uusi yhteys** -asetus.
3. Tarjolla olevien yhteyksien joukosta, valitse **Business Central**, ja valitse sitten **Luo** nappula.

    PowerApps muodostaa [!INCLUDE [prodshort](includes/prodshort.md)] -yhteyden niillä käyttäjätiedoilla, joilla olet kirjautunut sisään. Jos et ole järjestelmänvalvoja [!INCLUDE [prodshort](includes/prodshort.md)] sovelluksessa, sinun täytyy ehkä kirjautua toisella käyttäjällä.  

4.  PowerApps näyttää luettelon *ympäristöistä ja yrityksistä*, jotka ovat käytettävissä [!INCLUDE [prodshort](includes/prodshort.md)]issa. Valitse ne tiedot sisältävä ympäristö ja yritys, joihin haluat muodostaa yhteyden. Seuraavaksi näyttöön tulee ohjelmointirajapintaluettelo. Valitse **Ohjelmointirajapinta**, johon haluat muodostaa yhteyden.

Nämä niin kutsutut taulukot ovat osa [!INCLUDE [prodshort](includes/prodshort.md)] API:a. Sinun ei tarvitse määrittää päätepisteitä itse – [!INCLUDE [prodshort](includes/prodshort.md)]in PowerApps-yhdistin tekee sen puolestasi.  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

Tässä kohtaa olet yhdistänyt [!INCLUDE [prodshort](includes/prodshort.md)] dataasi ja olet valmis aloittamaan PowerAppisi rakentamisen. Voit luoda lisää ruutuja ja yhdistää lisädataan [!INCLUDE [prodshort](includes/prodshort.md)]. Lisätietoja on kohdassa [Kaaviosovelluksen luominen PowerAppsin mallista](/powerapps/maker/canvas-apps/get-started-test-drive).  

Kun olet suunnitellut ja rakentanut sovelluseksi, voit jakaa sen kollegoidesi kanssa. Lisätietoja on kohdassa [Kaaviosovelluksen tallentaminen julkaiseminen PowerAppsissa](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Jos haluat yhdistää [!INCLUDE [prodshort](includes/prodshort.md)]iin paikallisesti, sinun täytyy valita  **Business Central (paikallinen)** yhdistin vaiheessa 3.  

## <a name="see-also"></a>Katso myös

[Kaaviosovelluksen luominen PowerAppsin mallista](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  
[Yhdistinsovellusten Kehittäminen tuotteessa Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
