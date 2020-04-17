---
title: Tietojen yhdistäminen Power Automateeen | Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla rakennat automaattisen työkulun.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, OData, Power App, SOAP
ms.date: 04/01/2020
ms.author: bmeier
ms.openlocfilehash: 6dbc2fd67b5156c47690661016d4e7d3aae64a09
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187938"
---
# <a name="using-prodshort-in-an-automated-workflow"></a>[!INCLUDE[prodshort](includes/prodshort.md)]in käyttäminen automaattisessa työnkulussa

Voit käyttää [!INCLUDE[prodshort](includes/prodshort.md)]in tietoja työnkulun osana Microsoft Power Automatessa.

> [!NOTE]
> Power Automate'n lisäksi voi käyttää työnkulkutoimintoa [!INCLUDE[prodshort](includes/prodshort.md)]issa. Huomaa, että vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Power Automatessa luotu työnkulkumalli lisätään työnkulkuluetteloon [!INCLUDE[prodshort](includes/prodshort.md)]issa. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
> Sinulla on oltava kelvollinen [!INCLUDE[prodshort](includes/prodshort.md)]- ja Power Automate -tili.  

## <a name="to-add-prodshort-as-a-data-source-in-power-automate"></a>[!INCLUDE[prodshort](includes/prodshort.md)]in lisääminen Power Automatein tietolähteeksi

1. Siirry selaimessa osoitteeseen [flow.microsoft.com](https://flow.microsoft.com) ja kirjaudu sisään.
2. Valitse sivun yläosan valintanauhassa **Omat työnkulut**.
3. Työnkulun luontiin on kolme tapaa: **Aloita mallista**, **Aloita tyhjästä** ja **Aloita yhdistimestä**. Malli on ennalta määritetty työnkulku, joka on luotu käyttäjälle. Mallin käyttö on helppoa: valitse malli ja luo yhteys jokaiseen mallin käyttämään palveluun. **Aloita tyhjästä**- ja **Aloita yhdistimestä** -vaihtoehdoissa uusi työnkulku voidaan luoda kokonaisuudessaan itse.
4. Voit luoda mallin tyhjästä valitsemalla **Omat työnkulut** -sivulla **Aloita tyhjästä**- ja **Automatisoitu työnkulku** -vaihtoehdot.
5. Etsi Connector for **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]**.
6. Määritä nimi ja valitse työnkulussa käytettävä käynnistin.
7. Valitse käytettävissä olevien käynnistimien luettelosta jokin [!INCLUDE[prodshort](includes/prodshort.md)] -käynnistin:  

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

8. Power Automate pyytää sinua valitsemaan ympäristön ja yrityksen [!INCLUDE[prodshort](includes/prodshort.md)] -vuokraajassa sekä mahdollisesti kuunneltavien tietojen ehdot.

    > [!NOTE]
    > [!INCLUDE[prodshort](includes/prodshort.md)]in Power Automate -yhdistin tukee useita tuotanto- ja sandbox-ympäristöjä. Jos et ole luonut useaa tuotanto- tai sandbox-ympäristöjä, **Tuotanto** on ainoa valittavissa oleva vaihtoehto.  

    Olet nyt muodostanut yhteyden Business Centralin [!INCLUDE [prodshort](includes/prodshort.md)] -tietoihin ja olet valmis aloittamaan oman työnkulun luomisen.

9. Voit luoda mallin valitsemalla **Aloita mallista** -vaihtoehdon.
10. Etsi **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]** -malleja.
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
12. Power Automate näyttää luettelon työnkulkumallissa käytettävistä palveluista ja yrittää muodostaa automaattisesti yhteyden näihin palveluihin. Jos yhteyttä palvelimeen ei ole muodostettu aiemmin, sinua pyydetään kirjautumaan kuhunkin palveluun, johon yhteys on muodostettava. Vihreä valintamerkki tulee näkyviin palvelun viereen, kun yhteys on muodostettu. Valitse **Jatka**.
13. Power Automate pyytää valitsemaan ympäristön ja yrityksen [!INCLUDE[prodshort](includes/prodshort.md)] -vuokraajassa. Koska seuraavat vaiheet eivät vaikuta työnkulun vaiheisiin, saatat joutua määrittämään ympäristön ja yrityksen useita kertoja [!INCLUDE[prodshort](includes/prodshort.md)]n Power Automate -mallissa.

Lisätietoja on [Power Automate -dokumentaatiossa](/power-automate/getting-started).

## <a name="see-also"></a>Katso myös

[Käytön aloittaminen](product-get-started.md)  
[Työnkulku](across-workflow.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[[!INCLUDE[prodlong](includes/prodlong.md)]in työnkulkujen hallinta](across-use-workflows.md)  
[Hyväksynnän käyttäjäasetukset](across-how-to-set-up-approval-users.md)  
[[!INCLUDE[prodshort](includes/prodshort.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  
