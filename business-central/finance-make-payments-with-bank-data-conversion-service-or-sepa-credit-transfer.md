---
title: Maksujen suorittaminen pankkitietojen muunnospalvelulla tai SEPA-tilisiirrolla | Microsoft Docs
description: "Käsittele maksut toimittajille viemällä tiedoston yhdessä maksutietojen kanssa päiväkirjan riveiltä."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 99277cb2daf37fbce4548cf637e8967fa6688dbc
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a>Maksujen suorittaminen pankkitietojen muunnospalvelulla tai SEPA-tilisiirrolla
**Maksupäiväkirja**-ikkunassa voit käsitellä maksut toimittajillesi viemällä tiedoston yhdessä maksutietojen kanssa päiväkirjan riveiltä. Voit sitten ladata tiedoston verkkopankkiin, jossa liittyvät rahansiirrot käsitellään. [!INCLUDE[d365fin](includes/d365fin_md.md)] tukee SEPA-hyvitysten siirtomuotoa, mutta maa- tai aluekohtaisesti voi olla käytettävissä muita sähköisiä maksumuotoja.   

 Kun haluat ottaa SEPA-hyvityksen siirrot käyttöön, määritä ensin pankkitili, toimittaja ja yleinen päiväkirja, johon maksupäiväkirja perustuu. Tämän jälkeen maksut valmistellaan toimittajia varten automaattisesti täyttämällä erääntyneet maksut ja määritetyt kirjauspäivämäärät **Maksupäiväkirja**-ikkunaan.  

> [!NOTE]  
>  Kun olet varmistanut, että pankki on käsitellyt maksut onnistuneesti, voit jatkaa maksupäiväkirjan rivien kirjaamista.  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.   

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Voit aktivoida pankkitietojen muuntopalvelun minkä tahansa pankin tiliotteen muuttamiseksi tuotavaan muotoon, tai voit muuttaa viedyt maksutiedostot pankkisi vaatimaan muotoon.|[Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-statement-service.md)|  
|Määritä pankkitili, myyjä ja maksuloki SEPA-tilisiirrolle.|[SEPA-hyvityksen siirron määrittäminen](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Täytä maksupäiväkirja toimittajiin kohdistuvilla erääntyvillä maksuriveillä ja vaihtoehdolla lisätä kirjauspäivämäärät perustuen liittyvien ostoasiakirjojen eräpäivään.|[Ostovelkojen hallinta](payables-manage-payables.md)|  
|Vie maksupäiväkirjan rivit tiedostoon SEPA-hyvityksen siirtomuodossa.|[Maksujen vienti pankkitiedostoon](payables-how-export-payments-bank-file.md)|  
|Kirjaa maksut sen jälkeen, kun pankki on käsitellyt ne onnistuneesti.|[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)|  

## <a name="see-also"></a>Katso myös  
[Pankkitietojen muuntopalvelun määrittäminen](bank-how-setup-bank-statement-service.md)  
[SEPA-hyvityksen siirron määrittäminen](finance-how-to-set-up-sepa-credit-transfer.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)   
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)   
