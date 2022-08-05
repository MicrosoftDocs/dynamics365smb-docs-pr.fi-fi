---
title: Työnkulut Dynamic 365 Business Centralissa
description: Sisäisen työnkulun ominaisuuksien avulla voit määrittää hyväksyntätyönkulkuja, jotka täydentävät Power Automateen perustuvia automatisoituja työnkulkuja. Voit määrittää vaiheet, joiden avulla tehtäviä määritetään eri henkilöille osana liiketoimintaprosessien eri tehtäviä.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: ab7d131e965b0698c6e33a0b1a43c8f408a7b1b2
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129900"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Dynamics 365 Business Centralin työnkulut

Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.  

[!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman oletusversio tukee kolmentyyppisiä työnkulkuja:

* Sisäisiin työnkulkumalleihin perustuvat automaattiset hyväksyntätyönkulut  

  **Työnkulkumallit**-sivulla näkyvät kaikki käytettävissä olevat työnkulut. [!INCLUDE[prod_short](includes/prod_short.md)]in kokeiluversio sisältää useita valmiiksi määritettyjä työnkulkuja ja työnkulkumalleja, joita kopioimalla voit luoda työnkulkuja. Kun avaat työnkulkumallin **Työnkulunmallit**-sivulta ja työnkulun nimi alkaa kirjaimilla *MS-*, Microsoft lisää työnkulkumallin.  
* Itse määrittämäsi automaattiset työnkulut  

  Power Automatella luodut työnkulkumallit lisätään [!INCLUDE[prod_short](includes/prod_short.md)]in työkulkumalleihin. Lisätietoja on kohdassa [Business Centralin käyttäminen Power Automate -työnkuluissa](across-how-use-financials-data-source-flow.md).  
* Manuaalisesti käynnistetyt työnkulut **automaattisesta** toiminnosta (vain [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa). Lisätietoja on kohdassa [Manuaaliset välittömät työnkulut](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Power Automate -työnkulut

[!INCLUDE [prod_short](includes/prod_short.md)] onlinen avulla voit rekisteröityä Power Automateen ja luoda sitten tehokkaita automatisoituja työnkulkuja, joita voit suorittaa [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman sisältä. Lisätietoja on kohdassa [Käytä [!INCLUDE[prod_short](includes/prod_short.md)] ohjelmaa Power Automate -työnkuluissa](across-how-use-financials-data-source-flow.md).  

## <a name="automated-approval-workflows"></a>Automaattiset hyväksymistyönkulut

Voit luoda hyväksymistyönkulun luettelemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.  

[!INCLUDE[workflow](includes/workflow.md)]

Voit määrittää ja käyttää työnkulkuja, joita ei ole määritetty Power Automatessa tarkistamalla seuraavat artikkelit:  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Luo työnkulun käyttäjiä, määriä, kuinka käyttäjät saavat ilmoituksia, ja luo uusia työnkulkuja. Jos haluat määrittää uusia työnkulkuja skenaarioille, joita ei tueta, työnkulun elementit on otettava käyttöön mukauttamalla sovelluskoodia.|[Työnkulkujen määrittäminen](across-set-up-workflows.md)|  
|Ota käyttöön työnkulkuja ja käsittele työnkulun ilmoituksia, joihin kuuluvat myös hyväksyntöjen pyytäminen sekä työnkulun osavaiheen suorituspyyntöjen hyväksyminen. Arkistoi ja poista työnkulkuja.|[Käytä työnkulkuja](across-use-workflows.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/create-workflows/)

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Projektien hallinta](projects-manage-projects.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen käyttäminen Power Automate -työnkuluissa](across-how-use-financials-data-source-flow.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman automaattisten työnkulkujen vianmääritys](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]