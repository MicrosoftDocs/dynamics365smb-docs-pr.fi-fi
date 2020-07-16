---
title: Sovelluksen luominen omista tiedoista| Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla luot Power Appsin avulla yrityssovelluksen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 06/22/2020
ms.author: edupont
ms.openlocfilehash: 8f0eb7a1562a8300bd7181ef6470c70f60934470
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528636"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Yhteyden muodostaminen Business Central -tietoihin yrityssovelluksen luomista varten Power Appsin avulla

Voit käyttää [!INCLUDE[prodshort](includes/prodshort.md)] -tietoja Power Appsin tietolähteenä.  

> [!NOTE]  
> Sinulla on oltava kelvollinen [!INCLUDE[prodshort](includes/prodshort.md)]- ja Power Apps -tili.  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a>[!INCLUDE[prodshort](includes/prodshort.md)]in lisääminen Power Appsin tietolähteeksi

1. Siirry selaimessa osoitteeseen [powerapps.microsoft.com](https://powerapps.microsoft.com/) ja kirjaudu sisään.
2. Valitse aloitussivun **Aloita tiedoista** -osassa **Muut tietolähteet** -ruutu.  

    Power Apps Studio avautuu. Ensimmäisellä kertaa kirjauduttaessa on määritettävä maa tai alue.  
3. Tarjolla olevien yhteyksien joukosta, valitse **Business Central**, ja valitse sitten **Luo** nappula.

    Power Apps muodostaa [!INCLUDE[prodshort](includes/prodshort.md)] -yhteyden niillä käyttäjätiedoilla, joilla olet kirjautunut sisään. Jos et ole järjestelmänvalvoja [!INCLUDE[prodshort](includes/prodshort.md)] sovelluksessa, sinun täytyy ehkä kirjautua toisella käyttäjällä.  

4. Power Apps näyttää luettelon *ympäristöistä ja yrityksistä*, jotka ovat käytettävissä [!INCLUDE[prodshort](includes/prodshort.md)]issa. Valitse ne tiedot sisältävä ympäristö ja yritys, joihin haluat muodostaa yhteyden, kuten *TUOTANTO – oma yritys*.  

5. Seuraavaksi näkyviin tulee taulukkoluettelo, jotka näkyvät ympäristön ohjelmointirajapinnan osana. Valitse taulukko, johon haluat muodostaa yhteyden ja valitse sitten **Yhdistä**.

Power Appsin [!INCLUDE[prodshort](includes/prodshort.md)] -yhdistin näyttää nämä niin kutsutut taulukot päätepisteinä.  

> [!NOTE]
> Jos haluat sisällyttää muiden taulukoiden dataa sovelluksessa [!INCLUDE[prodshort](includes/prodshort.md)], sinun tulee työskennellä kehittäjän kanssa, jotta voitte määrittää mukautetun API:n sovelluksessa [!INCLUDE[prodshort](includes/prodshort.md)] ja käyttää tätä mukautettua API:a mukautetun yhdistimen kautta Power Appsissa. Lisätietoja, katso [Mukautetun yhdistimen luominen tyhjästä](/connectors/custom-connectors/define-blank).  

Tässä kohtaa olet yhdistänyt [!INCLUDE[prodshort](includes/prodshort.md)] dataasi ja olet valmis aloittamaan PowerAppisi rakentamisen. Voit luoda lisää ruutuja ja yhdistää lisädataan [!INCLUDE[prodshort](includes/prodshort.md)]. Lisätietoja on kohdassa [Kaaviosovelluksen luominen Power Appsin mallista](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Kun olet suunnitellut ja rakentanut sovelluseksi, voit jakaa sen kollegoidesi kanssa. Lisätietoja on kohdassa [Kaaviosovelluksen tallentaminen julkaiseminen Power Appsissa](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Jos haluat yhdistää [!INCLUDE[prodshort](includes/prodshort.md)]iin paikallisesti, sinun täytyy valita  **Business Central (paikallinen)** yhdistin vaiheessa 3.  

## <a name="see-also"></a>Katso myös

[Kaaviosovelluksen luominen Power Appsin mallista](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Yhdistinsovellusten Kehittäminen tuotteessa Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
