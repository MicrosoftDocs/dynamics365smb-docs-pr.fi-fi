---
title: Sovelluksen luominen omista tiedoista| Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla luot Power Apps -sovelluksen avulla yrityssovelluksen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 11/20/2019
ms.author: edupont
ms.openlocfilehash: 9cf587dca8224e742ecbde30bcabc35697bb6f2a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880998"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten Power Apps -sovellusten avulla

Voit käyttää [!INCLUDE[prodshort](includes/prodshort.md)]-tietoja Power Appsin tietolähteenä.  

> [!NOTE]  
> Sinulla on oltava kelvollinen [!INCLUDE[prodshort](includes/prodshort.md)]- ja Power Apps -tili.  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-apps"></a>[!INCLUDE[prodshort](includes/prodshort.md)]in lisääminen Power Appsin tietolähteeksi

1. Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/) ja kirjaudu sisään.
2. Luo uusi kaaviosovellus valitsemalla aloitussivulla **Sovellukset**, **Luo sovellus** ja **Kangas**. Tämä sovellus suunnitellaan mobiililaitekäyttöön, mutta voit valita myös toisenlaisen mallin.

    Power App -sovelluksen luonnin seuraavana vaiheena on tietojen valinta. Valitse sivun vasemmassa yläosassa ensin nuolikuvake ja sitten **Uusi yhteys** -asetus.
3. Tarjolla olevien yhteyksien joukosta, valitse **Business Central**, ja valitse sitten **Luo** nappula.

    Power Apps yhdistyy [!INCLUDE [prodshort](includes/prodshort.md)]in kanssa niillä tunnuksilla, joilla olet tällä hetkellä kirjautuneena sisään. Jos et ole järjestelmänvalvoja [!INCLUDE [prodshort](includes/prodshort.md)] sovelluksessa, sinun täytyy ehkä kirjautua toisella käyttäjällä.  

4. Power Apps näyttää luettelon *ympäristöistä ja yrityksistä*, jotka ovat käytettävissä [!INCLUDE [prodshort](includes/prodshort.md)]issa. Valitse ne tiedot sisältävä ympäristö ja yritys, joihin haluat muodostaa yhteyden. Seuraavaksi näyttöön tulee ohjelmointirajapintaluettelo. Valitse **Ohjelmointirajapinta**, johon haluat muodostaa yhteyden.

Nämä niin kutsutut taulukot ovat osa [!INCLUDE [prodshort](includes/prodshort.md)] API:a. Sinun ei tarvitse itse määrittää päätepisteitä - [!INCLUDE [prodshort](includes/prodshort.md)] yhdistäjä Power Appsille tekee sen puolestasi.  

> [!NOTE]
> Jos haluat sisällyttää muiden taulukoiden dataa [!INCLUDE [prodshort](includes/prodshort.md)] sovelluksessasi, sinun tulee työskennellä kehittäjän kanssa, jotta voitte määrittää mukautetun API:n [!INCLUDE [prodshort](includes/prodshort.md)]ille ja käyttää tätä mukautettua API:a mukautetun yhdistimen kautta Power Appsissa. Lisätietoja, katso [Mukautetun yhdistimen luominen tyhjästä](/connectors/custom-connectors/define-blank).  

Tässä kohtaa olet yhdistänyt [!INCLUDE [prodshort](includes/prodshort.md)] dataasi ja olet valmis aloittamaan PowerAppisi rakentamisen. Voit luoda lisää ruutuja ja yhdistää lisädataan [!INCLUDE [prodshort](includes/prodshort.md)]. Lisätietoja, katso [Luo kaaviosovellus mallista Power Appsissa](/powerapps/maker/canvas-apps/get-started-test-drive).  

Kun olet suunnitellut ja rakentanut sovelluseksi, voit jakaa sen kollegoidesi kanssa. Lisätietoja, katso [Tallenna ja julkaise kaaviosovelluksia Power Appsissa](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Jos haluat yhdistää [!INCLUDE [prodshort](includes/prodshort.md)]iin paikallisesti, sinun täytyy valita  **Business Central (paikallinen)** yhdistin vaiheessa 3.  

## <a name="see-also"></a>Katso myös

[Luo kaaviosovellus mallista Power Appsissa](/powerapps/maker/canvas-apps/get-started-test-drive).  
[Käytön aloittaminen](product-get-started.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  
[Yhdistinsovellusten Kehittäminen tuotteessa Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
