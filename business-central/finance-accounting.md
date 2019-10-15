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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 79ed5e1b7200a668be2aa078531fd68e0131b6ff
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302585"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Kirjanpitäjän käyttökokemukset [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]issa
Kaikkien yritysten on pidettävä kirjanpitoa ja hyväksyttävä se. Jotkin yritykset käyttävät ulkoista kirjanpitäjää, ja joillain yrityksillä on oma kirjanpitäjä. Olit kummanlainen kirjanpitäjä tahansa, voit käyttää **kirjanpitäjän** roolikeskusta [!INCLUDE[d365fin](includes/d365fin_md.md)]in kotisivunasi. Siitä saat avattua kaikki sivut, joita tarvitset työssäsi.  

## <a name="accountant-role-center"></a>Kirjanpitäjän roolikeskus
Roolikeskus on koontinäyttö, joka sisältää reaaliaikaisia avainlukuja näyttäviä toimintoruutuja, joista saat nopean pääsyn tietoihin. Sivun yläreunassa on valintanauha, josta pääset käyttämään lisätoimintoja, kuten eniten käytettyjen raporttien ja laskelmien avaaminen Excelissä. Yläosassa olevan siirtymispalkin avulla voit vaihtaa eniten käyttämiesi luetteloiden välillä. Täällä näkyy muita alueita, kuten **Kirjatut asiakirjat** sekä eri tyyppisiä yrityksen kirjaamia asiakirjoja.  

Jos olet uusi [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjä, voit avata opetusvideoiden luettelon suoraan roolikeskuksesta. Voit avata myös **Aloitusoppaan**, joka osoittaa sovelluksen tärkeimmät osat.  

## <a name="accountant-hub"></a>Accountant Hub
Jos olet kirjanpitäjä, jolla on useita asiakkaita, saat [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]in avulla hyvän kokonaiskuvan asiakkaistasi. Koontinäytöstä saat pääsyn kunkin asiakkaan vuokraajaan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa ja voit käyttää kirjanpitäjän roolikeskusta edellä kuvatun mukaisesti. Lisätietoja on kohdassa [Tervetuloa ohjelmaan [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] on tällä hetkellä julkinen esiversio muutamilla markkina-alueilla.

## <a name="inviting-your-external-accountant-to-your-included365finincludesd365fin_mdmd"></a>Ulkoisen kirjanpitäjän kutsuminen [!INCLUDE[d365fin](includes/d365fin_md.md)]iin
Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, jolloin he saavat käyttöönsä kirjanpitotietosi.

Kun kirjanpitäjä on saanut [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeudet, hän voi käyttää **Kirjanpitäjä**-roolikeskusta. josta pääsee kätevästi kirjanpitäjän työssään eniten käyttämille sivuille.  

Ulkopuolisen kirjanpitäjän kutsumista on helpotettu. Avaa vain **Käyttäjät**-sivuta ja valitse sitten valintanauhassa **Kutsu ulkoinen kirjanpitäjä** -toiminto. Saat käyttöösi valmiin sähköpostiviestin, johon sinun tarvitsee vain lisätä kirjanpitäjän työsähköpostiosoite. Voit sitten lähettää kutsun.  

![Kirjanpitäjän kutsuminen](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
> Kutsun lähettäminen, edellyttää, että SMTP-sähköposti on määritetty. Voit tehdä sen itse tai pyytää [!INCLUDE[d365fin](includes/d365fin_md.md)]-kumppania tekemään sen. Lisäksi sinun on kirjauduttava [!INCLUDE[d365fin](includes/d365fin_md.md)]iin käyttäjien järjestelmänvalvojana eikä liiketoiminnan omistajana tai muuna käyttäjänä. Lopuksi sinun on jätettävä kokeiluyritys, jotta sinulla on Azure Active Directoryn järjestelmänvalvoja.  

> [!IMPORTANT]  
> Kirjanpitäjän sähköpostiosoitteen on oltava Azure Active Directoryyn perustuva työsähköpostiosoite. Jos kirjanpitäjä käyttää jotakin muuta sähköpostityyppiä, kutsua ei voi lähettää.  

### <a name="separate-license"></a>Erillinen käyttöoikeus
Kirjanpitäjä lisätään taustalla Active Directory-vuokraajaan. Järjestelmänvalvoja voi varmistaa, että kirjanpitäjä hyväksyy kutsun ja että hänelle määritetään soveltuva käyttöoikeus. Tämä toimenpiteen tekeminen käytännössä määräytyy sen tilin mukaan, jolla [!INCLUDE[d365fin](includes/d365fin_md.md)]iin kirjaudutaan. Tämän ohjeaiheen ohjeet perustuvat Office 365 -tiliin, jossa on käytössä Microsoft Azure Active Directory.  

Jos olet aktivoinut [!INCLUDE[d365fin](includes/d365fin_md.md)]in tilauksen etkä käytä enää arviointiyritystä, sinulla on Azure Active Directory -vuokraaja. Järjestelmänvalvoja tai [!INCLUDE[d365fin](includes/d365fin_md.md)]-kumppanin hallitsee tätä vuokraajaa [Azure-portaalissa](https://portal.azure.com). Uudet käyttäjät lisätään tässä portaalissa. Myös käyttöoikeudet otetaan käyttöön ja poistetaan siellä. Lisätietoja on [Microsoft Azure -portaalin yleiskatsauksessa](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

Yksi [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttöoikeustyypeistä on *ulkoisen kirjanpitäjän* käyttöoikeus. Tämä käyttöoikeustyyppi on tarkoitettu ulkoisen kirjanpitäjän kaltaisille käyttäjille. Tämä käyttöoikeustyyppi ei edellytä ylimääräisen asiakaskohtaisen käyttöoikeuden ostamista nykyiseen Active Directoryyn eikä nykyisen [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätilin käyttöä ulkoiselle kirjanpitäjälle. Jos esimerkiksi nykyinen Office 365 -tilaus sisältää 10 [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjää ja käytät tällä hetkellä 10 *täyttä* käyttöoikeutta, järjestelmänvalvoja voi lisätä ulkoisen kirjanpitäjän vieraskäyttäjänä Azure-portaaliin ja määrittää kyseiselle käyttäjälle *ulkoisen kirjanpitäjän* käyttöoikeuden ilman lisäkustannuksia. *Ulkoisen kirjanpitäjän* käyttöoikeudet voi kuitenkin olla vain yhdellä käyttäjällä. Jos haluat lisätä enemmän käyttäjiä, Office 365 -tilausta on päivitettävä vastaavasti.

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
[Dynamics 365 – Accountant Hub Microsoft.comissa](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
