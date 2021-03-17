---
title: Tietojen yhdistäminen Power Automateeen | Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla rakennat automaattisen työkulun.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1608330b5d2b2955a144498e5c44d40072b22a8b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384197"
---
# <a name="using-prod_short-in-an-automated-workflow"></a>[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen automaattisessa työnkulussa

Voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja työnkulun osana Microsoft Power Automate'ssa.

> [!NOTE]
> Power Automate'n lisäksi voi käyttää työnkulkutoimintoa [!INCLUDE[prod_short](includes/prod_short.md)]issa. Huomaa, että vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Power Automatessa luotu työnkulkumalli lisätään työnkulkuluetteloon [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
> Sinulla on oltava kelvollinen [!INCLUDE[prod_short](includes/prod_short.md)]- ja Power Automate -tili.  

## <a name="to-add-prod_short-as-a-data-source-in-power-automate"></a>[!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen Power Automatein tietolähteeksi

1. Siirry selaimessa osoitteeseen [flow.microsoft.com](https://flow.microsoft.com) ja kirjaudu sisään.
2. Valitse sivun yläosan valintanauhassa **Omat työnkulut**.
3. Työnkulun luontiin on kolme tapaa: **Aloita mallista**, **Aloita tyhjästä** ja **Aloita yhdistimestä**. Malli on ennalta määritetty työnkulku, joka on luotu käyttäjälle. Mallin käyttö on helppoa: valitse malli ja luo yhteys jokaiseen mallin käyttämään palveluun. **Aloita tyhjästä**- ja **Aloita yhdistimestä** -vaihtoehdoissa uusi työnkulku voidaan luoda kokonaisuudessaan itse.
4. Voit luoda mallin tyhjästä valitsemalla **Omat työnkulut** -sivulla **Aloita tyhjästä**- ja **Automatisoitu työnkulku** -vaihtoehdot.
5. Etsi Connector for **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
6. Määritä nimi ja valitse työnkulussa käytettävä käynnistin.
7. Valitse käytettävissä olevien käynnistimien luettelosta jokin [!INCLUDE[prod_short](includes/prod_short.md)] -käynnistin:  

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

8. Power Automate pyytää sinua valitsemaan ympäristön ja yrityksen [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajassa sekä mahdollisesti kuunneltavien tietojen ehdot.

    > [!NOTE]
    > [!INCLUDE[prod_short](includes/prod_short.md)]in Power Automate -yhdistin tukee useita tuotanto- ja sandbox-ympäristöjä. Jos et ole luonut useaa tuotanto- tai sandbox-ympäristöjä, **Tuotanto** on ainoa valittavissa oleva vaihtoehto.  

    Olet nyt muodostanut yhteyden Business Centralin [!INCLUDE[prod_short](includes/prod_short.md)] -tietoihin ja olet valmis aloittamaan oman työnkulun luomisen.

9. Voit luoda mallin valitsemalla **Aloita mallista** -vaihtoehdon.
10. Etsi **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]** -malleja.
11. Valitse käytettävissä olevien mallien luettelosta ensin yksi malli ja valitse sitten **Luo**.  

    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -myyntitilauksen hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -myyntitarjouksen hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -myyntilaskun hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -myyntihyvityslaskun hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -asiakkaan hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -ostotilauksen hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -ostolaskun hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -ostohyvityslaskun hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -nimikkeen hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -toimittajan hyväksyntäpyyntö*  
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]in yleisen päiväkirjan erän hyväksyntäpyyntö* tai    
    *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] yleisen päiväkirjan rivien hyväksyntäpyyntö*.  
12. Power Automate näyttää luettelon työnkulkumallissa käytettävistä palveluista ja yrittää muodostaa automaattisesti yhteyden näihin palveluihin. Jos yhteyttä palvelimeen ei ole muodostettu aiemmin, sinua pyydetään kirjautumaan kuhunkin palveluun, johon yhteys on muodostettava. Vihreä valintamerkki tulee näkyviin palvelun viereen, kun yhteys on muodostettu. Valitse **Jatka**.
13. Power Automate pyytää valitsemaan ympäristön ja yrityksen [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajassa. Koska seuraavat vaiheet eivät vaikuta työnkulun vaiheisiin, saatat joutua määrittämään ympäristön ja yrityksen useita kertoja [!INCLUDE[prod_short](includes/prod_short.md)]n Power Automate -mallissa.

Lisätietoja on [Power Automate -dokumentaatiossa](/power-automate/getting-started).

## <a name="see-also"></a>Katso myös

[Käytön aloittaminen](product-get-started.md)  
[Työnkulku](across-workflow.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]in työnkulkujen hallinta](across-use-workflows.md)  
[Hyväksynnän käyttäjäasetukset](across-how-to-set-up-approval-users.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]