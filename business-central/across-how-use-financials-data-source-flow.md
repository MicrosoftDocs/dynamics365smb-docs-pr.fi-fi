---
title: "Tietojen yhdistäminen Flow'hun| Microsoft Docs"
description: "Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla rakennat automaattisen työkulun."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6f79bd9a5e3f79d4366a1a43411fe39942ac4e4f
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen automaattisessa työnkulussa
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja työnkulun osana Microsoft Flow'ssa.

> [!NOTE]
> Microsoft Flow'n lisäksi voi käyttää työnkulkutoimintoa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Huomaa, että vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Microsoft Flow'ssa luotu Flow-malli lisätään työnkulkumallien luetteloon [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
>   Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Flow-tili.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen Flow'n tietolähteeksi
1. Siirry selaimessa osoitteeseen [flow.microsoft.com](https://flow.microsoft.com/en-us/) ja kirjaudu sisään.
2. Valitse sivun yläosan valintanauhassa **Omat Flow't**.
3. Flow'n voi luoda kahdella tavalla: **Luo mallista** ja **Luo tyhjästä mallista**. Malli on ennalta määritetty Flow, joka on luotu käyttäjälle.  Mallin käyttö on helppoa: valitse malli ja luo yhteys jokaiseen mallin käyttämään palveluun. Tyhjän mallin avulla voit luoda uuden Flow'n alusta alkaen.
4. Voit luoda mallin tyhjästä valitsemalla **Omat Flow't** -sivulla **Luo tyhjästä mallista** -asetus.
5. Etsi Connector for **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. Valitse käytettävissä olevien käynnistimien luettelosta jokin [!INCLUDE[d365fin](includes/d365fin_md.md)] -käynnistin:  
    *Kun asiakkaan hyväksyntää on pyydetty*  
    *Kun yleisen päiväkirjan erän hyväksymistä on pyydetty*  
    *Kun yleisen päiväkirjan rivin hyväksymistä on pyydetty*  
    *Kun nimikkeen hyväksyntää on pyydetty*  
    *Kun ostoasiakirjan hyväksyntää on pyydetty*  
    *Kun myyntiasiakirjan hyväksyntää on pyydetty* tai  
    *Kun toimittajan hyväksyntää on pyydetty*.
7. Flow pyytää sinua valitsemaan yrityksen [!INCLUDE[d365fin](includes/d365fin_md.md)] -vuokraajassa sekä mahdollisesti kuunneltavat tietojen ehdot.

Olet nyt muodostanut yhteyden Business Central -tietoihin ja olet valmis aloittamaan oman Flow'n luomisen.

8. Voit luoda mallin mallista valitsemalla **Luo mallista** -asetuksen.
9. Etsi **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]** -malleja.
10. Valitse käytettävissä olevien mallien luettelosta yksi malli.  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -myyntitilauksen hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -myyntitarjouksen hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -myyntilaskun hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -myyntihyvityslaskun hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -asiakkaan hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -ostotilauksen hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -ostolaskun hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -ostohyvityslaskun hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -nimikkeen hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] -toimittajan hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] yleisen päiväkirjan erän hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] yleisen päiväkirjan rivien hyväksyntäpyyntö*.  
11. Flow pyytää valitsemaan yrityksen [!INCLUDE[d365fin_md](includes/d365fin_md.md)] -vuokraajasta. Koska seuraavat vaiheet eivät vaikuta Flow'n vaiheisiin, saatat joutua määrittämään yrityksen useita kertoja [!INCLUDE[d365fin_md](includes/d365fin_md.md)] Flow -mallissa.

Lisätietoja on kohdassa [Flow-ohjeistus](https://docs.microsoft.com/en-us/flow/getting-started).

Lisätietoja Microsoft Flow'n vianmäärityksestä on kohdassa [Microsoft Flow -integroinnin vianmääritys](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Katso myös
[Käytön aloittaminen](product-get-started.md)  
[Työnkulku](across-workflow.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)   
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in työnkulkujen hallinta](across-use-workflows.md)  
[Hyväksynnän käyttäjäasetukset](across-how-to-set-up-approval-users.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  

