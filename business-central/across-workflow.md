---
title: Työnkulku | Microsoft Docs
description: Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamia liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d8dac033ad2f4573d8a7f0047c44ac04eb8e6eb0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773409"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Dynamics 365 Business Centralin työnkulut

Voit määrittää ja käyttää työnkulkuja, jotka yhdistävät eri käyttäjien suorittamista liiketoimintaprosessin tehtäviä. Järjestelmätehtäviä (kuten automaattinen kirjaus) voidaan sisällyttää työnkulkuihin, joita käyttäjän tehtävät edeltävät tai seuraavat. Uusien tietueiden luontiin liittyvien hyväksyntöjen pyytäminen ja antaminen ovat tyypillisiä työnkulun osavaiheita.  

 Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita.  

 [!INCLUDE[prod_short](includes/prod_short.md)]in yleinen versio sisältää useita valmiiksi määritettyjä työnkulkuja ja työnkulkumalleja, joita kopioimalla voit luoda työnkulkuja. Työnkulkumallien koodit, jotka Microsoft on lisännyt, sisältävät etuliitteen "MS-". Lisätietoja on Työnkulkumallit-sivun työnkulkumallien luettelossa.  

 Jos liiketoimintaskenaario edellyttää työnkulun tapahtumaa tai vastausta, joka ei ole tuettu, voit mukauttaa sovelluskoodia Power Automaten avulla tai tekemällä yhteistyöt Microsoft-kumppanin kanssa. Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md).

Power Automatella luodut työnkulkumallit lisätään [!INCLUDE[prod_short](includes/prod_short.md)]in työkulkumalleihin. Lisätietoja on kohdassa [Business Centralin käyttäminen automaattisessa työnkulussa](across-how-use-financials-data-source-flow.md).  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Luo työnkulun käyttäjiä, määriä, kuinka käyttäjät saavat ilmoituksia, ja luo uusia työnkulkuja. Jos haluat määrittää uusia työnkulkuja skenaarioille, joita ei tueta, työnkulun elementit on otettava käyttöön mukauttamalla sovelluskoodia.|[Työnkulkujen määrittäminen](across-set-up-workflows.md)|  
|Ota käyttöön työnkulkuja ja käsittele työnkulun ilmoituksia, joihin kuuluvat myös hyväksyntöjen pyytäminen sekä työnkulun osavaiheen suorituspyyntöjen hyväksyminen. Arkistoi ja poista työnkulkuja.|[Työnkulkujen käyttäminen](across-use-workflows.md)|  

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Projektien hallinta](projects-manage-projects.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]