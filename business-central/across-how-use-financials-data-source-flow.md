---
title: Power Automate -työnkulkujen käyttö Business Centralissa
description: Määritä ja käytä Power Automate -työnkulkuja luodaksesi tai muuttaaksesi Business Centralin tietoja.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 5fe089c0330a8d2b7a71f4907212665722d27d38
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606519"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Power Automate -työnkulkujen käyttäminen [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksissa

Voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja työnkulun osana Microsoft Power Automate'ssa. Luo omia työnkulkuja ja yhdistä tiedot sisäisistä ja ulkoisista lähteistä [!INCLUDE [prod_short](includes/prod_short.md)] -yhdistimellä.

> [!NOTE]
> Sinulla on oltava sekä kelvollinen [!INCLUDE[prod_short](includes/prod_short.md)]- että Power Automate -tili.  

> [!TIP]
> Power Automaten lisäksi voi käyttää hyväksyntätyönkulkumalleja [!INCLUDE[prod_short](includes/prod_short.md)] -tuotteessa. Vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Power Automatessa luotu hyväksyntätyönkulkumalli lisätään työnkulkuluetteloon [!INCLUDE[prod_short](includes/prod_short.md)] -tuotteessa. Lisätietoja kohdassa [Työnkulut](across-workflow.md).

Power Automate -työnkulut käynnistyvät tapahtumien, kuten tietueiden ja asiakirjojen luonnin, muuttamisen tai poistamisen avulla (automaattiset työnkulut). Työnkulut voidaan myös suorittaa käyttäjän määrittämässä aikataulussa (aikataulutetut työnkulut) tai pyydettäessä (pikatyönkulut).

## <a name="power-automate-features-in-prod_short"></a>Power Automate -toiminnot [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa

Työnkulut laajenevat sisäänrakennettujen hyväksyntätyönkulkujen ominaisuuksiin, jotka ovat käytettävissä [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa ilman koodausosaamista, ja ne voivat liittyä moniin tapahtumiin ja vastauksiin, kuten tietueiden muutoksiin, ulkoisten tiedostojen päivityksiin, julkaistuihin asiakirjoihin sekä erilaisiin Microsoftin ja kolmannen osapuolen palveluihin, kuten Microsoft Outlook, Microsoft Excel, Microsoft Dataverse, Microsoft Teams Microsoft SharePoint, Microsoft Power Apps ja moniin muihin.

Esimerkiksi uusi myyntilasku voi käynnistää hyväksymispyynnön työnkulun, jolla voi olla erilaisia tapahtumia määritettynä hyväksyjän vastauksen mukaan. Negatiivinen vastaus lähettää ilmoituksen ja sähköpostin hyväksynnän pyytäjälle. Positiivinen vastaus päivittää samanaikaisesti SharePoint-kansiossa sijaitsevan Excel-taulukon ja lähettää päivityksen Teams-keskusteluun.

Pikatyönkulut toimivat samalla tavalla kuin eräajot, suorittavat useita pitkiä vaiheita muutamalla näppäimen painalluksella ja ne käynnistetään tietyiltä sivuilta tai taulukoista. Työnkulun avulla voit esimerkiksi lisätä painikkeen toimintovalikkoon **Toimittajat**-sivulla, jos haluat estää toimittajalle suoritettavat maksut ja samaan aikaan lähettää mukautettavia sähköposteja myyjän kontaktille ja yrityksesi ostajille sekä päivittää kontaktin Outlookissa.

## <a name="automated-workflows"></a>Automaattiset työnkulut

Power Automaten kanssa, voit luoda liiketoimintatyönkulkuja suoraan talon sisällä ja luottaa citizen developereihin. Automatisoituja työnkulkuja voi käynnistää sekä sisäisillä että ulkoisilla tapahtumilla [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa ja ne voidaan myös määrittää suoritettavaksi ajoittain. Lisätietoja ja ohjeita työnkulkujen luomisesta hallinnan sisällön [Määritä automaattiset työnkulut](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) -artikkelissa.

## <a name="instant-flows"></a>Pikatyönkulut

[!INCLUDE [prod_short](includes/prod_short.md)] voi suorittaa Power Automate -työnkulun useimmilta luettelo-, kortti- ja asiakirjasivuilta. Kun järjestelmänvalvoja on muodostanut yhteyden [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman ja Power Automaten välille, näet kaikki työnkulut, jotka organisaatiosi on lisännyt, kun valitset **automatisoi**-toiminnon asiaankuuluvilla sivuilla. Pikatyönkulut suoritetaan poistumatta [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmasta. Lisätietoja on hallintasisällön [Automaattisten työnkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) -artikkelissa.

Nämä pikatyönkulut avautuvat [!INCLUDE [prod_short](includes/prod_short.md)] online-sivilla niin, että ne säilyvät sen liiketoimintaprosessin kontekstissa, jonka keskellä olet. Valitse **automaattinen**-toiminto –joillakin sivuilla piilotettuna **Lisää asetuksia** -valikossa – valitse **Power Automate** -valikkovaihtoehto ja valitse sitten asianmukainen linkki, joka käynnistää työnkulun. Power Automate -yhteys on muodostettu valmiiksi.

Useimmat työnkulut edellyttävät, että täytät kentän tai kaksi, ennen kuin valitset **Suorita työnkulku** -toiminnon.

> [!TIP]
> Jos et näe **automaatti**-toimintoa, sinun [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaasi ei luultavasti ole vielä määritetty käyttämään Power Automatea. Saat lisätietoja järjestelmänvalvojalta.

## <a name="add-more-automated-flows-and-instant-flows"></a>Lisää automaattisia työnkulkuja ja pikatyönkulkuja

Voit luoda työnkulkuja [powerautomate.microsoft.com ](https://powerautomate.microsoft.com) -sivustossa. Jos järjestelmänvalvojasi on kuitenkin ottanut käyttöön mahdollisuuden suorittaa Power Automate -työnkulkuja [!INCLUDE [prod_short](includes/prod_short.md)] online -tilassa, voit aloittaa työnkulun rakentamisen asianomaisten sivujen **Automatisointi**-toiminnolla, joka löytyy **Lisää vaihtoehtoja** -valikosta riippuen sivusta. Valitse sitten **Power Automate**-valikkonimike ja valitse sitten **Luo työnkulku** -toiminto. Power Automate avautuu sitten uuteen selainvälilehteen, ja kirjaudut sisään automaattisesti.

Voit etsiä malleja, jotka mukautuvat yritykseesi ja kaikkiin käytettävissä oleviin käynnistimiin, käyttämällä sekä [!INCLUDE [prod_short](includes/prod_short.md)] -sovellusta että ulkoisia työkaluja, valitsemalla Power Automate -verkkosivuston **Yhdistimet**-valikon. Lisätietoja saatavilla olevista malleista ja käynnistimistä on hallintasisällön [Automaattisten työnkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) -artikkelissa.

## <a name="manage-automated-workflows"></a>Automaattisten työnkulkujen hallinta

Voit luoda uusia työnkulkuja tai hallita aiemmin luotuja Power Automate -työnkulkuja [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksessa **Hallitse Power Automate -työnkulkuja** -sivulla. Lisätietoja on hallintasisällön [Power Automate -työnkulkujen hallinta](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) -artikkelissa.

Voit myös hallita saatavilla olevia Power Automate -työnkulkuja **Työnkulut**-sivulla [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa. Sivulla on sekä sisäänrakennettu hyväksyntä että Power Automate -työnkulkuja, joiden vaihtoehdot mahdollistavat sen, että voit ottaa käyttöön/poistaa käytöstä, poistaa ja tarkastella työnkulkua Power Automate -sivustossa.

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/use-power-automate/)

## <a name="see-also"></a>Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman automaattisten työnkulkujen vianmääritys](across-flow-troubleshoot.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Työnkulut](across-workflow.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Määritä [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Rahoitus](finance.md)  
[Power Automate -työnkulkujen hallinta](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Automaattisten työnkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Ota pikatyönkulut käyttöön](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
