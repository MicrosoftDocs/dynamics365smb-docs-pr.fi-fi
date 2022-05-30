---
title: Business Centralin käyttö Power Automate -työnkuluissa
description: Määritä ja käytä Power Automate -työnkulkuja, jotka luovat tai muuttavat Business Centralin tietoja.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: 93eb177ff9ba102277a50f9686ea941df33d5563
ms.sourcegitcommit: 13ac10624bee47c73989b2b20942a01c849b4a6a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2022
ms.locfileid: "8744108"
---
# <a name="use-prod_short-in-power-automate-flows"></a>[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen käyttäminen Power Automate -työnkuluissa

Voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja työnkulun osana Microsoft Power Automate'ssa. Luo omia työnkulkuja ja yhdistä tiedot [!INCLUDE [prod_short](includes/prod_short.md)] -yhdistimellä.  

> [!NOTE]  
> Sinulla on oltava kelvollinen [!INCLUDE[prod_short](includes/prod_short.md)]- ja Power Automate -tili.  

> [!TIP]
> Power Automaten lisäksi voi käyttää hyväksyntätyönkulkumalleja [!INCLUDE[prod_short](includes/prod_short.md)] -tuotteessa. Vaikka kyse on erillisistä työnkulkujärjestelmistä, jokainen Power Automatessa luotu hyväksyntätyönkulkumalli lisätään työnkulkuluetteloon [!INCLUDE[prod_short](includes/prod_short.md)] -tuotteessa. Lisätietoja on kohdassa [Työnkulut](across-workflow.md).  

## <a name="automated-workflows"></a>Automaattiset työnkulut

Power Automaten kanssa, voit luoda liiketoimintatyönkulkuja suoraan talon sisällä ja luottaa citizen developereihin. Lisätietoja on hallintasisällön kohdassa [Automaattisten työnkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows).  

## <a name="manual-instant-flows"></a>Manuaaliset välittömät työnkulut

Toukokuusta 2022 alkaen [!INCLUDE [prod_short](includes/prod_short.md)] online-järjestelmänvalvoja voi [ottaa käyttöön ominaisuuden](admin-feature-management.md), jotta voidaan suorittaa Power Automate -työnkulkuja useimmilta sivuilta. Lisätietoja on hallintasisällön kohdassa [Automaattisten työnkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows).  

Kun järjestelmänvalvoja on muodostanut yhteyden [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman ja Power Automaten välille, näet kaikki työnkulut, jotka organisaatiosi on lisännyt, kun valitset **automatisoi**-toiminnon asiaankuuluvilla sivuilla. Suoritat työnkulut poistumatta [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmasta.  

Nämä automaattiset työnkulut avautuvat [!INCLUDE [prod_short](includes/prod_short.md)] online-ruudussa niin, että ne säilyvät sen liiketoimintaprosessin kontekstissa, jonka keskellä olet. Joillakin sivuilla **automaattinen** toiminto piilotetaan **Lisää asetuksia** -valikossa, mutta etsi se, valitse **Power Automate** -valikkovaihtoehto ja valitse sitten asianmukainen linkki, joka käynnistää työnkulun. Power Automate -yhteys on muodostettu valmiiksi.  

Useimmat työnkulut edellyttävät, että täytät kentän tai kaksi, ennen kuin valitset **Suorita työnkulku** -toiminnon.  

> [!TIP]
> Jos et näe **automaatti**-toimintoa, sinun [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaasi ei luultavasti ole vielä määritetty käyttämään Power Automatea. Pyydä lisätietoja järjestelmänvalvojaltasi.

## <a name="add-more-automated-flows-and-manual-instant-flows"></a>Lisää automaattisia työnkulkuja ja manuaalisia välittömiä työnkulkuja

Voit luoda työnkulkuja [powerautomate.microsoft.com ](https://powerautomate.microsoft.com) -sivustossa. Jos järjestelmänvalvojasi on kuitenkin ottanut käyttöön mahdollisuuden suorittaa Power Automate -työnkulkuja [!INCLUDE [prod_short](includes/prod_short.md)] online-tilassa, voit aloittaa prosessin luomisen **Automatisoi**-toiminnosta asiaankuuluvilla sivuilla. Joillakin sivuilla **automaattinen** toiminto piilotetaan **Lisää asetuksia** -valikossa, mutta etsi se, valitse **Power Automate** -valikkovaihtoehto ja valitse sitten **Luo työnkulku** -toiminto. Power Automate avautuu sitten uuteen selainvälilehteen, ja kirjaudut sisään automaattisesti.

## <a name="manage-workflows"></a>Työnkulkujen hallinta

Voit saada yleiskuvan kaikista työnkuluista, joihin sinulla on käyttöoikeus, valitsemalla valikosta **Hallitse työnkulkuja** -toiminnon **Power Automate** -valikosta. Luettelo avautuu uuteen selainvälilehteen, ja kirjaudut sisään Power Automateen automaattisesti. Siellä voit nähdä, milloin jokainen työnkulku viimeksi suoritettiin.  

## <a name="see-also"></a>Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman automaattisten työnkulkujen vianmääritys](across-flow-troubleshoot.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Työnkulut](across-workflow.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Määritä [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Rahoitus](finance.md)  
[Automaattisten työnkulkujen määrittäminen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]