---
title: "Tietojen yhdistäminen Flow'hun| Microsoft Docs"
description: "Voit tehdä Financials-tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla rakennat automaattisen työkulun."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 23e9ebbb75d23595d568d022526e551bf590a979
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen automaattisessa työnkulussa
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja työnkulun osana Microsoft Flow'ssa.  

> [!NOTE]  
>   Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Flow-tili.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen Flow'n tietolähteeksi
1. Siirry selaimessa osoitteeseen [flow.microsoft.com](https://flow.microsoft.com/en-us/) ja kirjaudu sisään.
2. Valitse sivun yläosan valintanauhassa **Omat Flow't**.
3. Valitse **Omat Flow't** -ikkunassa **Luo tyhjästä mallista** -asetus.
4. Valitse käytettävissä olevien käynnistimien luettelosta jokin [!INCLUDE[d365fin](includes/d365fin_md.md)] -käynnistin:  
    *Kun asiakkaan hyväksyntää on pyydetty*  
    *Kun yleisen päiväkirjan erän hyväksymistä on pyydetty*  
    *Kun yleisen päiväkirjan rivin hyväksymistä on pyydetty*  
    *Kun nimikkeen hyväksyntää on pyydetty*  
    *Kun ostoasiakirjan hyväksyntää on pyydetty*  
    *Kun myyntiasiakirjan hyväksyntää on pyydetty* tai  
    *Kun toimittajan hyväksyntää on pyydetty*.
5. Flow pyytää valitsemaan yrityksen [!INCLUDE[d365fin](includes/d365fin_md.md)] -vuokraajasta. Koska seuraavat vaiheet eivät vaikuta Flow'n vaiheisiin, saatat joutua määrittämään yrityksen useita kertoja [!INCLUDE[d365fin](includes/d365fin_md.md)] -mallissa.

Olet nyt muodostanut yhteyden Business Central -tietoihin ja olet valmis aloittamaan oman Flow'n luomisen. Lisätietoja on kohdassa [Flow-dokumentaatio](https://flow.microsoft.com/documentation/getting-started/).

Lisätietoja Microsoft Flow'n vianmäärityksestä on kohdassa [Microsoft Flow -integroinnin vianmääritys](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Katso myös
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](upload-data.md)  
[Käyttäjien ja käyttöoikeuksien hallinta](ui-how-users-permissions.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  

