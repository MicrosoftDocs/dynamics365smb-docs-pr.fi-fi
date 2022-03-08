---
title: Tietojen yhdistäminen Flow'hun| Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla rakennat automaattisen työkulun.
documentationcenter: ''
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: a46692503b19ddad57c4a68d0f29b588d84f5c9e
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775449"
---
# <a name="using-d365fin-in-an-automated-workflow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen automaattisessa työnkulussa
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja työnkulun osana Microsoft Flow'ssa.

> [!NOTE]
> Microsoft Flow'n lisäksi voi käyttää työnkulkutoimintoa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Huomaa, että vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Microsoft Flow'ssa luotu Flow-malli lisätään työnkulkuluetteloon [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
> Sinulla on oltava kelvollinen [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja Flow-tili.  

## <a name="to-add-d365fin-as-a-data-source-in-flow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in lisääminen Flow'n tietolähteeksi
1. Siirry selaimessa osoitteeseen [flow.microsoft.com](https://flow.microsoft.com/en-us/) ja kirjaudu sisään.
2. Valitse sivun yläosan valintanauhassa **Omat Flow't**.
3. Flow'n luontiin on kolme tapaa: **Aloita mallista**, **Aloita tyhjästä** ja **Aloita yhdistimestä**. Malli on ennalta määritetty Flow, joka on luotu käyttäjälle. Mallin käyttö on helppoa: valitse malli ja luo yhteys jokaiseen mallin käyttämään palveluun. **Aloita tyhjästä**- ja **Aloita yhdistimestä** -vaihtoehdoissa uusi Flow voidaan luoda kokonaisuudessaan itse.
4. Voit luoda mallin tyhjästä valitsemalla **Omat Flow't** -sivulla **Aloita tyhjästä**- ja **Automatisoitu työnkulku** -vaihtoehdot.
5. Etsi Connector for **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. Määritä nimi ja valitse Flow'ssa käytettävä käynnistin.
7. Valitse käytettävissä olevien käynnistimien luettelosta jokin [!INCLUDE[d365fin](includes/d365fin_md.md)] -käynnistin:  
    
    *Kun toimittajan hyväksyntää on pyydetty*    
    *Kun yleisen päiväkirjan rivin hyväksymistä on pyydetty*    
    *Kun tietue poistetaan*    
    *Kun tietuetta muutetaan*    
    *Kun tietue luodaan*    
    *Kun tietuetta muokataan*    
    *Kun yleisen päiväkirjan erän hyväksymistä on pyydetty*   
    *Kun asiakkaan hyväksyntää on pyydetty*   
    *Kun nimikkeen hyväksyntää on pyydetty*    
    *Kun ostoasiakirjan hyväksyntää on pyydetty*     
     *Kun myyntiasiakirjan hyväksyntää on pyydetty*.
     
8. Flow pyytää sinua valitsemaan ympäristön ja yrityksen [!INCLUDE[d365fin](includes/d365fin_md.md)] -vuokraajassa sekä mahdollisesti kuunneltavien tietojen ehdot.

> [!NOTE]  
>   [!INCLUDE[d365fin](includes/d365fin_md.md)]in Microsoft Flow -yhdistin tukee useita tuotanto- ja sandbox-ympäristöjä. Jos et ole luonut useaa tuotanto- tai sandbox-ympäristöjä, **Tuotanto** on ainoa valittavissa oleva vaihtoehto. 

Olet nyt muodostanut yhteyden Business Central -tietoihin ja olet valmis aloittamaan oman Flow'n luomisen.

9. Voit luoda mallin valitsemalla **Aloita mallista** -vaihtoehdon.
10. Etsi **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]** -malleja.
11. Valitse käytettävissä olevien mallien luettelosta ensin yksi malli ja valitse sitten **Luo**.  

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
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]in yleisen päiväkirjan erän hyväksyntäpyyntö* tai    
    *Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] yleisen päiväkirjan rivien hyväksyntäpyyntö*.  
12. Flow näyttää luettelon Flow-mallissa käytettävistä palveluista ja yrittää muodostaa automaattisesti yhteyden näihin palveluihin. Jos yhteyttä palvelimeen ei ole muodostettu aiemmin, sinua pyydetään kirjautumaan kuhunkin palveluun, johon yhteys on muodostettava. Vihreä valintamerkki tulee näkyviin palvelun viereen, kun yhteys on muodostettu. Valitse **Jatka**.
13. Flow pyytää valitsemaan ympäristön ja yrityksen [!INCLUDE[d365fin_md](includes/d365fin_md.md)] -vuokraajassa. Koska seuraavat vaiheet eivät vaikuta Flow'n vaiheisiin, saatat joutua määrittämään ympäristön ja yrityksen useita kertoja [!INCLUDE[d365fin_md](includes/d365fin_md.md)] Flow -mallissa.

Lisätietoja on kohdassa [Flow-ohjeistus](/flow/getting-started).

## <a name="see-also"></a>Katso myös
[Käytön aloittaminen](product-get-started.md)  
[Työnkulku](across-workflow.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)   
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in työnkulkujen hallinta](across-use-workflows.md)  
[Hyväksynnän käyttäjäasetukset](across-how-to-set-up-approval-users.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  
