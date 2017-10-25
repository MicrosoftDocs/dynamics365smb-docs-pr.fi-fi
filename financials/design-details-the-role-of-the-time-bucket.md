---
title: "Rakennetiedot – aikavälin rooli | Microsoft Docs"
description: "Ajanjakson tarkoitus on kerätä kysyntätapahtumia aikaikkunan sisällä, jotta voidaan tehdä yhteinen toimitustilaus."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: eb1b1a401dabe09a77c44558e9f5a83388078aaa
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-the-role-of-the-time-bucket"></a>Rakennetiedot: aikavälin rooli
Aikavälin tarkoitus on kerätä kysyntätapahtumia aikaikkunan sisällä, jotta yhteinen toimitustilaus voidaan tehdä.  
  
 Uusintatilauspistettä käyttävien uusintatilaustapojen kohdalla voit määrittää aikavälin. Tämä varmistaa, että saman ajanjakson kysyntä kertyy, ennen vaikutuksen oletettuun varastoon ja uusintatilauspisteen mahdollisen ohituksen tarkistusta. Jos uusintatilauspiste on ohitettu, uusi toimitustilaus ajoitetaan eteenpäin aikavälin määrittämän jakson lopusta. Aikavälit alkavat suunnittelun aloituspäivämäärästä.  
  
 Konsepti, jolle on määritetty aikavälit, osoittaa manuaalisen varastotason tarkistuksen prosessin säännöllisin väliajoin, ei jokaisen tapahtuman kohdalla. Käyttäjän on määritettävä toistoväli (aikaväli). Esimerkiksi käyttäjä kerää kaikki nimikkeen tarpeet yhdeltä toimittajalta viikoittaisen tilauksen asettamiseksi.  
  
 ![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")  
  
 Aikaväliä käytetään yleensä limittäisyyden välttämiseksi. Esimerkiksi täsmäytetty kysynnän ja tarjonnan rivi, jossa aikainen kysyntä on peruutettu tai uusi luodaan. Tuloksena on, että jokainen toimitustilaus (paitsi viimeisin) aikataulutetaan uudelleen.  
  
## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Uusintatilauskäytännöt](design-details-reordering-policies.md)   
 [Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
 [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
 [Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)
