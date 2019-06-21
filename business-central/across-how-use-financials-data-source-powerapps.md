---
title: Sovelluksen luominen omista tiedoista| Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla luot PowerApps-sovelluksen avulla yrityssovelluksen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 05/13/2019
ms.author: edupont
ms.openlocfilehash: 67d7129e32ccde3154a02dd12b806d712f470833
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540267"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten PowerApps-sovellusten avulla
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoja PowerAppsin tietolähteenä.  

> [!NOTE]  
>   Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja PowerApps-tili.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen PowerAppsin tietolähteeksi
1. Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) ja kirjaudu sisään.
2. Kotisivulla, valitse **Aloita tiedoista** malli luodaksesi uuden kaaviosovelluksen. Tämä sovellus suunnitellaan mobiililaitekäyttöön, mutta voit valita myös toisenlaisen mallin.

    PowerApp-sovelluksen luonnin seuraavana vaiheena on tietojen valinta. Valitse sivun vasemmassa yläosassa ensin nuolikuvake ja sitten **Uusi yhteys** -asetus.
3. Tarjolla olevien yhteyksien joukosta, valitse **Business Central**, ja valitse sitten **Luo** nappula.

    PowerApps yhdistyy [!INCLUDE [prodshort](includes/prodshort.md)]in kanssa niillä tunnuksilla, joilla olet tällä hetkellä kirjautuneena sisään. Jos et ole järjestelmänvalvoja [!INCLUDE [prodshort](includes/prodshort.md)] sovelluksessa, sinun täytyy ehkä kirjautua toisella käyttäjällä.  

4. Jos [!INCLUDE [prodshort](includes/prodshort.md)] sisältää useamman kuin yhden yrityksen, sinun pitää valita mihin yritykseen haluat yhdistää.  Sitten, PowerApps näyttää listan *taulukoista*, jotka ovat saatavilla [!INCLUDE [prodshort](includes/prodshort.md)]in kautta. Nämä niin kutsutut taulukot ovat osa [!INCLUDE [prodshort](includes/prodshort.md)] API:a. Sinun ei tarvitse itse määrittää päätepisteitä - [!INCLUDE [prodshort](includes/prodshort.md)] yhdistäjä PowerAppsille tekee sen puolestasi.  

    Jos haluat sisällyttää muiden taulukoiden dataa [!INCLUDE [prodshort](includes/prodshort.md)] sovelluksessasi, sinun tulee työskennellä kehittäjän kanssa, jotta voitte määrittää mukautetun API:n [!INCLUDE [prodshort](includes/prodshort.md)]ille ja käyttää tätä mukautettua API:a mukautetun yhdistimen kautta PowerAppsissa. Lisätietoja, katso [Mukautetun yhdistimen luominen tyhjästä](/connectors/custom-connectors/define-blank).  

Tässä kohtaa olet yhdistänyt [!INCLUDE [prodshort](includes/prodshort.md)] dataasi ja olet valmis aloittamaan PowerAppisi rakentamisen. Voit luoda lisää ruutuja ja yhdistää lisädataan [!INCLUDE [prodshort](includes/prodshort.md)]. Lisätietoja, katso [Luo kaaviosovellus mallista PowerAppsissa](/powerapps/maker/canvas-apps/get-started-test-drive).  

Kun olet suunnitellut ja rakentanut sovelluseksi, voit jakaa sen kollegoidesi kanssa. Lisätietoja, katso [Tallenna ja julkaise kaaviosovelluksia PowerAppsissa](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Jos haluat yhdistää [!INCLUDE [prodshort](includes/prodshort.md)]iin paikallisesti, sinun täytyy valita  **Business Central (paikallinen)** yhdistin vaiheessa 3.  

## <a name="see-also"></a>Katso myös

[Luo kaaviosovellus mallista PowerAppsissa](/powerapps/maker/canvas-apps/get-started-test-drive).  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  
[Yhdistinsovellusten Kehittäminen tuotteessa Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
