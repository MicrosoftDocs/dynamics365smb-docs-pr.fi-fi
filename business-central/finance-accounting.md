---
title: Business Centralin kirjanpitäjän käyttökokemukset | Microsoft Docs
description: Lisätietoja Business Central -sovelluksen kirjanpitäjäportaalista ja kirjanpitäjän roolikeskusta, joka tukee asiakasyrityksen omia ja ulkopuolisia kirjanpitäjää.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 12/02/2019
ms.author: edupont
ms.openlocfilehash: c575c0e482ebe4d34c9b699b22747486651efe04
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896131"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Kirjanpitäjän käyttökokemukset [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]issa
Kaikkien yritysten on pidettävä kirjanpitoa ja hyväksyttävä se. Jotkin yritykset käyttävät ulkoista kirjanpitäjää, ja joillain yrityksillä on oma kirjanpitäjä. Olit kummanlainen kirjanpitäjä tahansa, voit käyttää **kirjanpitäjän** roolikeskusta [!INCLUDE[d365fin](includes/d365fin_md.md)]in kotisivunasi. Siitä saat avattua kaikki sivut, joita tarvitset työssäsi.  

## <a name="accountant-role-center"></a>Kirjanpitäjän roolikeskus
Roolikeskus on koontinäyttö, joka sisältää reaaliaikaisia avainlukuja näyttäviä toimintoruutuja, joista saat nopean pääsyn tietoihin. Sivun yläreunassa on valintanauha, josta pääset käyttämään lisätoimintoja, kuten eniten käytettyjen raporttien ja laskelmien avaaminen Excelissä. Yläosassa olevan siirtymispalkin avulla voit vaihtaa eniten käyttämiesi luetteloiden välillä. Täällä näkyy muita alueita, kuten **Kirjatut asiakirjat** sekä eri tyyppisiä yrityksen kirjaamia asiakirjoja.  

Jos olet uusi [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjä, voit avata opetusvideoiden luettelon suoraan roolikeskuksesta. Voit avata myös **Aloitusoppaan**, joka osoittaa sovelluksen tärkeimmät osat.  

## <a name="inviteaccountant"></a>Ulkoisen kirjanpitäjän kutsuminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin
Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, jolloin he saavat käyttöönsä kirjanpitotietosi.

Kun kirjanpitäjä on saanut [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeudet, hän voi käyttää **Kirjanpitäjä**-roolikeskusta. josta pääsee kätevästi kirjanpitäjän työssään eniten käyttämille sivuille.  

Ulkopuolisen kirjanpitäjän kutsumista on helpotettu. Avaa vain **Käyttäjät**-sivuta ja valitse sitten valintanauhassa **Kutsu ulkoinen kirjanpitäjä** -toiminto. Saat käyttöösi valmiin sähköpostiviestin, johon sinun tarvitsee vain lisätä kirjanpitäjän työsähköpostiosoite. Voit sitten lähettää kutsun.  
> [!Note]  
> Kutsun lähettäminen, edellyttää, että SMTP-sähköposti on määritetty. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).   

![Kirjanpitäjän kutsuminen](./media/finance-invite-accountant/invite-accountant.png)

> [!IMPORTANT]  
> Kirjanpitäjän sähköpostiosoitteen on oltava Azure Active Directoryyn perustuva työsähköpostiosoite. Jos kirjanpitäjä käyttää jotakin muuta sähköpostityyppiä, kutsua ei voi lähettää.  

### <a name="behind-the-scenes"></a>Kulissien takana
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää kolme lisenssiä, joiden tyyppi on ulkopuolinen kirjanpitäjä. Jos yrityksesi käyttää ulkoista kirjanpitäjä, voit antaa käyttö oikeudet omaan [!INCLUDE[d365fin](includes/d365fin_md.md)] -ratkaisuusi määrittämällä heille tällainen lisenssi. Lisätietoja käyttöoikeuksista on [Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa.](https://go.microsoft.com/fwlink/?LinkId=871590) 

Jos tilauksessasi on vielä käytettävänä oleva käyttöoikeus, järjestelmänvalvoja tai jälleenmyyjäkumppani voi lisätä ulkoisen käyttäjän Azure-portaalin kautta ja määrittää tälle käyttäjälle ulkoisen kirjanpitäjän käyttöoikeuden. Lisätietoja on kohdassa [Azure Active Directoryn B2B-yhteistyökäyttäjien lisääminen Azure-portaalissa](/azure/active-directory/b2b/add-users-administrator).

Tämän jälkeen voit kutsua kirjanpitäjän [!INCLUDE[d365fin](includes/d365fin_md.md)]ista käyttämällä ohjattua **Kutsu ulkoinen kirjanpitäjä** -käyttöönotto-opasta. Koska tämä tehtävä edellyttää käyttäjien ja käyttö oikeuksien hallintaa Azure Active Directoryssä, tämän kutsun lähettäneen käyttäjällä on oltava **Yleinen järjestelmänvalvoja** -rooli tai **Käyttäjien hallinnoija** -rooli Office 365 -hallintakeskuksessa. Lisätietoja on kohdassa [Tietoja järjestelmänvalvojarooleista](/office365/admin/add-users/about-admin-roles)(Office 365:n järjestelmänvalvojasisältö). 

## <a name="accountant-hub"></a>Accountant Hub
Jos olet kirjanpitäjä, jolla on useita asiakkaita, saat [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]in avulla hyvän kokonaiskuvan asiakkaistasi. Koontinäytöstä saat pääsyn kunkin asiakkaan vuokraajaan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa ja voit käyttää kirjanpitäjän roolikeskusta edellä kuvatun mukaisesti. Lisätietoja on kohdassa [Tervetuloa ohjelmaan [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] on tällä hetkellä julkinen esiversio muutamilla markkina-alueilla.

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[Dimensioiden käyttäminen](finance-dimensions.md)  
[Rahoituslaskelmien analysointi Excelissä](finance-analyze-excel.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Kassavirta-analyysin määrittäminen](finance-setup-cash-flow-analyses.md)  
[Tervetuloa [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]iin!](/dynamics365/accountants/index)  
[Dynamics 365 – Accountant Hub Microsoft.comissa](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)  
