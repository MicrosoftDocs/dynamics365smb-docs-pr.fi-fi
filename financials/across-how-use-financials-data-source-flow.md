---
title: "Dynamics 365 for Financialsin käyttäminen Microsoft Flow&quot;ssa | Microsoft Docs"
description: "Voit käyttää Financials-tietoja PowerAppsin tietolähteenä."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 76d24ed80adb08083c6167040be8cc6a4bcc3167
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-in-microsoft-flow"></a>Dynamics 365 for Financialsin käyttäminen Microsoft Flow'ssa
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja työnkulun osana Microsoft Flow'ssa.  

**Huomautus**: sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Flow-tili.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen Flow'n tietolähteeksi
1. Siirry selaimessa osoitteeseen [flow.microsoft.com](https://flow.microsoft.com/en-us/) ja kirjaudu sisään.
2. Valitse sivun yläosan valintanauhassa **Omat Flow't**.
3. Valitse **Omat Flow't** -ikkunassa **Luo tyhjästä mallista** -asetus.
4. Valitse käytettävien käynnistimien luettelosta jompikumpi kahdesta [!INCLUDE[d365fin](includes/d365fin_md.md)]-käynnistimestä: *Kun tietue on luotu* tai *Kun tietuetta on muutettu*.
5. Flow näyttää yhteyssivun, joka kysyy sinulta tietoja, jotka on yhdistettävä [!INCLUDE[d365fin](includes/d365fin_md.md)]-tietoihin. Yhteyttä varten on määritettävä yhteyden nimi, ODatan URL-osoite, käyttäjänimi, salasana ja yrityksen nimi.

   Voit kopioida *OData URL* -osoitteeksi minkä tahansa [!INCLUDE[d365fin](includes/d365fin_md.md)]in **WWW-palvelut**-sivulla mainitun verkkopalvelun OData V4 URL-osoitteen, kuten `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Käytä *yrityksen nimenä* nimeä, joka näkyy [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Oman yrityksen tiedot** -ikkunan **Nimi**-kentässä. Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]issa on useita yrityksiä, valitse sopiva yrityksen nimi **Yritykset**-ikkunassa olevasta luettelosta. Varmista kummassakin tapauksessa, että ohjatussa PowerApps-toiminnossa määrittämäsi nimi on kirjoitettu täsmälleen samoin kuin [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Esimerkki: `My Company`.

   Käytä käyttäjänimenä ja salasanana tilille [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Käyttäjät**-ikkunassa määritettyä nimeä ja verkkopalvelun käyttöoikeusavainta. Käyttäjänimesi on esimerkiksi *JÄRJESTELMÄNVALVOJA* ja salasanana toimiva verkkopalvelun käyttöoikeusavain on *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*. Lisätietoja on kohdassa [Toimintaohje: Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md).
6. Jatka valitsemalla sivun alareunassa **Luo**-painike.

   Flow näyttää luettelon taulukoista, joita voi käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Nämä taulukot tai päätepisteet viittaavat kaikkiin [!INCLUDE[d365fin](includes/d365fin_md.md)]ista julkaistuihin verkkopalveluihin.

   Voit vaihtoehtoisesti luoda uuden verkkopalvelun URL-osoitteen [!INCLUDE[d365fin](includes/d365fin_md.md)]issa käyttämällä **Luo tietojoukko** -toimintoa **WWW-palvelut**-sivulla tai avustettua **Määritä raportointi** -asetusopasta tai valitsemalla **Muokkaa Excelissä** -toiminnon missä tahansa luettelossa.
7. Valitse Flow'ssa käytettävät tiedot.

Olet nyt muodostanut yhteyden Dynamics 365 -tietoihin ja olet valmis aloittamaan oman Flow'n luomisen. Lisätietoja on kohdassa [Flow-dokumentaatio](https://flow.microsoft.com/documentation/getting-started/).

## <a name="see-also"></a>Katso myös
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin](index.md)  
[Yritystietojen tuonti muista rahoitusjärjestelmistä] (upload-data.md)  
[Toimintaohje: Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  

