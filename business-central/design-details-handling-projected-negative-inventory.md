---
title: "Rakennetiedot –Suunnitellun negatiivisen varaston käsittely | Microsoft Docs"
description: "Jälkitilauspiste ilmaisee ennakkokysynnän nimikkeen läpimenoajan aikana. Kun uusintatilauspiste on ohitettu, on aika tilata lisää. Mutta arvioidun varaston on oltava riittävän suuri kysynnän kattamiseksi, kunnes uusi tilaus vastaanotetaan. Tänä aikana varmuusvaraston tulisi huolehtia kysynnän vaihteluista palvelun kohdetasolle asti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 19d7e142ebe10926b2caa6da2ddf6faae486bebd
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-handling-projected-negative-inventory"></a>Rakennetiedot: suunnitellun negatiivisen varaston käsittely
Jälkitilauspiste ilmaisee ennakkokysynnän nimikkeen läpimenoajan aikana. Kun uusintatilauspiste on ohitettu, on aika tilata lisää. Mutta arvioidun varaston on oltava riittävän suuri kysynnän kattamiseksi, kunnes uusi tilaus vastaanotetaan. Tänä aikana varmuusvaraston tulisi huolehtia kysynnän vaihteluista palvelun kohdetasolle asti.  

 Näin ollen suunnittelujärjestelmä katsoo sen hätätapaukseksi, jos tulevaa kysyntää ei voida toimittaa suunnitellusta varastosta tai toisella tavalla ilmaistuna, suunniteltu varasto muuttuu negatiiviseksi. Tällaisen poikkeuksen tapahtuessa järjestelmä ehdottaa uutta toimitustilausta, joka vastaa kysyntää, jota varasto tai toinen tarjonta ei täytä. Uuden toimitustilauksen koko ei ota huomioon maksimivarastoa tai jälkitilausmäärää, eikä se ota huomioon tilauksen muokkaajia maksimitilausmäärä, minimitilausmäärä ja tilauksen moninkertaistaminen. Sen sijaan se vastaa täsmällistä puutetta.  

 Tämän tyyppisen toimitustilauksen suunnittelurivillä näytetään Hätävaroituskuvake ja lisätietoa annetaan sitä haettaessa tiedottamaan käyttäjää tilanteesta.  

 Seuraavassa kuvassa tarjonta D vastaa hätätilausta negatiivisen varaston muuttamiseksi.  

 ![](media/nav_app_supply_planning_2_negative_inventory.png "NAV_APP_supply_planning_2_negative_inventory")  

1.  Tarjonta **A**, alunperin suunniteltu varasto, on jälkitilauspisteen alapuolella.  

2.  Luodaan uusi eteenpäin aikataulutettu tarjonta (**C**).  

     (Määrä = enimmäisvarasto – suunniteltu varastotaso)  

3.  Tarjonta **A** on suljettu kysynnän **B** johdosta, jota ei täysin katettu.  

     (Tarjonta **B** voi yrittää aikatauluttaa tarjontaa C, mutta se ei tapahdu aikavälikäsitteen mukaisesti.)  

4.  Uusi tarjonta (**D**) on luotu kattamaan jäljellä olevan määrän kysynnässä **B**.  

5.  Kysyntä **B** on suljettu (luodaan muistutusta suunniteltuun varastoon).  

6.  Uusi tarjonta **D** on suljettu.  

7.  Suunniteltu varasto on valittuna; uusintatilauspistettä ei ole ylitetty.  

8.  Tarjonta **C** on suljettu (kysyntää ei enää ole).  

9. Lopullinen tarkastus: avoimia varaston tason muistutuksia ei ole olemassa.  

> [!NOTE]  
>  Vaihe 4 kuvaa sitä, miten järjestelmä reagoi versiota Microsoft Dynamics NAV 2009 SP1 edeltävissä versioissa.  

 Tämä päättää uusintatilaustapoihin perustuvaan varaston suunnitteluun liittyvien keskeisten periaatteiden kuvauksen. Seuraavassa osassa kuvataan neljän tuetun jälkitilausohjeen ominaisuudet.  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md)   
 [Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
 [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
 [Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)

