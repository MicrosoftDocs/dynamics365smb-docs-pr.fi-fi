---
title: Tietojen yhdistäminen Power Automateeen | Microsoft Docs
description: Voit tehdä Business Central -tiedoistasi tietolähteen ja määrittää verkkopalveluidesi OData-osoitteen, jolla rakennat automaattisen työkulun.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 07/27/2021
ms.author: edupont
author: jswymer
ms.openlocfilehash: 7335092e74c0f681ba14a81a7045f2688fbb1df4
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133354"
---
# <a name="using-prod_short-in-an-automated-workflow"></a>[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen automaattisessa työnkulussa

Voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja työnkulun osana Microsoft Power Automate'ssa.

> [!NOTE]
> Power Automate'n lisäksi voi käyttää työnkulkutoimintoa [!INCLUDE[prod_short](includes/prod_short.md)]issa. Huomaa, että vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Power Automatessa luotu työnkulkumalli lisätään työnkulkuluetteloon [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Työnkulku](across-workflow.md).  

> [!NOTE]  
> Sinulla on oltava kelvollinen [!INCLUDE[prod_short](includes/prod_short.md)]- ja Power Automate -tili.  

## <a name="add-prod_short-as-a-data-source-in-power-automate"></a>[!INCLUDE[prod_short](includes/prod_short.md)] -ratkaisun lisääminen Power Automaten tietolähteeksi

1. Siirry selaimessa osoitteeseen [flow.microsoft.com](https://flow.microsoft.com) ja kirjaudu sisään.
2. Valitse sivun yläosan valintanauhassa **Omat työnkulut**.
3. Työnkulun luontiin on kolme tapaa: **Aloita mallista**, **Aloita tyhjästä** ja **Aloita yhdistimestä**. Malli on ennalta määritetty työnkulku, joka on luotu käyttäjälle. Mallin käyttö on helppoa: valitse malli ja luo yhteys jokaiseen mallin käyttämään palveluun. **Aloita tyhjästä**- ja **Aloita yhdistimestä** -vaihtoehdoissa uusi työnkulku voidaan luoda kokonaisuudessaan itse.
4. Voit luoda mallin tyhjästä valitsemalla **Omat työnkulut** -sivulla **Aloita tyhjästä**- ja **Automatisoitu työnkulku** -vaihtoehdot.
5. Etsi Connector for **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
6. Määritä nimi ja valitse työnkulussa käytettävä käynnistin.
7. Valitse käytettävissä olevien käynnistimien luettelosta jokin [!INCLUDE[prod_short](includes/prod_short.md)] -käynnistin:  

    - *Kun toimittajan hyväksyntää on pyydetty*  
    - *Kun yleisen päiväkirjan rivin hyväksymistä on pyydetty* 
    - *Kun tietue poistetaan*
    - *Kun tietuetta muutetaan*
    - *Kun tietue luodaan*
    - *Kun tietuetta muokataan*
    - *Kun yleisen päiväkirjan erän hyväksymistä on pyydetty* 
    - *Kun asiakkaan hyväksyntää on pyydetty*
    - *Kun nimikkeen hyväksyntää on pyydetty*
    - *Kun ostoasiakirjan hyväksyntää on pyydetty*
    - *Kun myyntiasiakirjan hyväksyntää on pyydetty*

8. Power Automate pyytää sinua valitsemaan ympäristön ja yrityksen [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajassa sekä mahdollisesti kuunneltavien tietojen ehdot.

    > [!NOTE]
    > [!INCLUDE[prod_short](includes/prod_short.md)]in Power Automate -yhdistin tukee useita tuotanto- ja sandbox-ympäristöjä. Jos et ole luonut useaa tuotanto- tai sandbox-ympäristöjä, **Tuotanto** on ainoa valittavissa oleva vaihtoehto.  

    Olet nyt muodostanut yhteyden Business Centralin [!INCLUDE[prod_short](includes/prod_short.md)] -tietoihin ja olet valmis aloittamaan oman työnkulun luomisen.

9. Voit luoda mallin valitsemalla **Aloita mallista** -vaihtoehdon.
10. Etsi **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]** -malleja.
11. Valitse käytettävissä olevien mallien luettelosta ensin yksi malli ja valitse sitten **Luo**.  

    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -myyntitilauksen hyväksyntäpyyntö*
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -myyntitarjouksen hyväksyntäpyyntö*
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -myyntilaskun hyväksyntäpyyntö*
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -myyntihyvityslaskun hyväksyntäpyyntö*
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -asiakkaan hyväksyntäpyyntö*
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -ostotilauksen hyväksyntäpyyntö*
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -ostolaskun hyväksyntäpyyntö*
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -ostohyvityslaskun hyväksyntäpyyntö*  
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -nimikkeen hyväksyntäpyyntö*
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] -toimittajan hyväksyntäpyyntö*
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] yleisen päiväkirjan erän hyväksyntäpyyntö*  
    - *Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] yleisen päiväkirjan rivien hyväksyntäpyyntö*
12. Power Automate näyttää luettelon työnkulkumallissa käytettävistä palveluista ja yrittää muodostaa automaattisesti yhteyden näihin palveluihin. Jos yhteyttä palvelimeen ei ole muodostettu aiemmin, sinua pyydetään kirjautumaan kuhunkin palveluun, johon yhteys on muodostettava. Vihreä valintamerkki tulee näkyviin palvelun viereen, kun yhteys on muodostettu. Valitse **Jatka**.
13. Power Automate pyytää valitsemaan ympäristön ja yrityksen [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraajassa. Koska seuraavat vaiheet eivät vaikuta työnkulun vaiheisiin, saatat joutua määrittämään ympäristön ja yrityksen useita kertoja [!INCLUDE[prod_short](includes/prod_short.md)]n Power Automate -mallissa.

Lisätietoja on [Power Automate -dokumentaatiossa](/power-automate/getting-started).

## <a name="troubleshooting"></a>Vianetsintä

### <a name="entity-set-not-found-error"></a>"Entiteettijoukkoa ei löydy" -virhe

#### <a name="problem"></a>Ongelma

Kun luot uuden Power Automate -työnkulun [!INCLUDE[prod_short](includes/prod_short.md)] -hyväksymiskäynnistimen avulla, esimerkiksi *Kun ostoasiakirjan hyväksyntää pyydetään*, näyttöön tulee seuraavan kaltainen virhesanoma:

**Entiteettijoukkoa ei löydy: \<name\>**

missä **\<name\>** on puuttuvan Web-palvelun palvelun nimi, kuten **workflowWebhookSubscriptions** tai **workflowPurchaseDocumentLines**.

#### <a name="possible-cause"></a>Mahdollinen syy

Jos käytät Power Automatea integrointiin [!INCLUDE[prod_short](includes/prod_short.md)]:n kanssa, hyväksynnät edellyttävät, että tietyt sivu-ja koodiyksikköobjektit julkaistaan Web-palveluina. Oletusarvon mukaan useimmat tarvittavista objekteista julkaistaan Web-palveluina. Joissakin tapauksissa ympäristösi on ehkä mukautettu siten, että näitä objekteja ei enää julkaista.

#### <a name="fix"></a>Korjaa

Siirry **Verkkopalvelut**-sivulle ja varmista, että seuraavat objektit on julkaistu Web-palveluina. Kaikille objekteille tulisi olla merkintä luettelossa , ja **Julkaistu**-valintaruutu valittuna. 

|Objektityyppi|Objektin tunnus|Objektin nimi|Palvelun nimi|
|-----------|---------|-----------|------------|
|Codeunit|  1544    |WorkflowWebhookSubscription|WorkflowActionResponse|
|Sivu|  6408|   workflowCustomers|  workflowCustomers|
|Sivu   |6406   |workflowGenJournalBatches| workflowGenJournalBatches|
|Sivu   |6407   |workflowGenJournalLines|workflowGenJournalLines|
|Sivu   |6409   |workflowItems| workflowItems|
|Sivu   |6405   |Ostoasiakirjarivin entiteetti|workflowPurchaseDocumentLines|
|Sivu|  6404    |workflowPurchaseDocuments| workflowPurchaseDocuments|
|Sivu|  6403    |Myyntiasiakirjarivin entiteetti |workflowSalesDocumentLines|
|Sivu|  6402|   workflowSalesDocuments| workflowSalesDocuments|
|Sivu|  6410    |workflowVendors|   workflowVendors|
|Sivu|  831 |workflowWebhookSubscriptions|  workflowWebhookSubscriptions|

> [!NOTE]
> **Palvelun nimi** -arvon täytyy olla täsmälleen sama kuin taulukossa on esitetty. Älä muuta tai käännä palvelun nimeä.

Lisätietoja verkkopalvelujen julkaisemisesta on kohdassa [Verkkopalvelun julkaiseminen](across-how-publish-web-service.md).

## <a name="see-also"></a>Katso myös

[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Työnkulku](across-workflow.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]in työnkulkujen hallinta](across-use-workflows.md)  
[Hyväksynnän käyttäjäasetukset](across-how-to-set-up-approval-users.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]