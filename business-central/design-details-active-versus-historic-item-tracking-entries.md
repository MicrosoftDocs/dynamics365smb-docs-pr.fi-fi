---
title: Rakennetiedot – Aktiivisen nimikkeen seurantatapahtumat verrattuna historiallisen nimikkeen seurantatapahtumiin | Microsoft Docs
description: Kun asiakirjarivin osia on kirjattu, vain tämä määrä siirretään nimiketapahtumiin ja sen nimikkeiden seurantanumeroihin. Haluat kuitenkin käyttää kaikkia asianmukaisia nimikkeen seurantatietoja suoraan aktiiviselta asiakirjariviltä. Eli ei ainoastaan silloin, kun haluat nähdä kirjaukset, jotka liittyvät jäljellä olevaan määrään, vaan myös silloin, kun haluat tietoa yksiköistä, jotka on tiliöity. Kun **Nimikkeen seurantarivit** -sivua tarkastellaan tai muokataan, **Seurannan määrittely** (T336)- ja **Varaustapahtuma** (T337) -taulukon yhteinen sisältö löytyy väliaikaisesta versiosta T336. Tämä varmistaa, että aiempia ja aktiivisia nimikkeen seurantatietoja voi käyttää yhtenä pakettina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: bbc2ed7ac5562820784db8c01bd25b2fd74726a0
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880662"
---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Rakennetiedot: aktiivisen nimikkeen seurantatapahtumat verrattuna historiallisen nimikkeen seurantatapahtumiin
Kun asiakirjarivin osia on kirjattu, vain tämä määrä siirretään nimiketapahtumiin ja sen nimikkeiden seurantanumeroihin. Haluat kuitenkin käyttää kaikkia asianmukaisia nimikkeen seurantatietoja suoraan aktiiviselta asiakirjariviltä. Eli ei ainoastaan silloin, kun haluat nähdä kirjaukset, jotka liittyvät jäljellä olevaan määrään, vaan myös silloin, kun haluat tietoa yksiköistä, jotka on tiliöity. Kun **Nimikkeen seurantarivit** -sivua tarkastellaan tai muokataan, **Seurannan määrittely** (T336)- ja **Varaustapahtuma** (T337) -taulukon yhteinen sisältö löytyy väliaikaisesta versiosta T336. Tämä varmistaa, että aiempia ja aktiivisia nimikkeen seurantatietoja voi käyttää yhtenä pakettina.  

 Seuraavassa taulukossa esitetään, kuinka T336 ja T337 käytetään ostoskenaariossa. Lihavoidut luvut edustavat arvoja, jotka käyttäjä antaa manuaalisesti **Nimikkeen seurantarivit** -sivulla.  

 Vaihe 1: luo seitsemän osan ostotilausrivi nimikkeenseurantanumeroineen.  

||**Määrä (perus)**|**Käsiteltävä määrä**|**Laskutettava määrä (perus)**|**Määrä käsitelty (perus)**|**Määrä laskutettu (perus)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Vaihe 2: vastaanota neljä osaa.  

||**Määrä (perus)**|**Käsiteltävä määrä**|**Laskutettava määrä (perus)**|**Määrä käsitelty (perus)**|**Määrä laskutettu (perus)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**F.var. nimikkeen seurantarivit** -sivu|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Vaihe 3: vastaanota kaksi osaa ja laskuta kaksi osaa.  

||**Määrä (perus)**|**Käsiteltävä määrä**|**Laskutettava määrä (perus)**|**Määrä käsitelty (perus)**|**Määrä laskutettu (perus)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**F.var. nimikkeen seurantarivit** -sivu|7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Vaihe 4: vastaanota yksi osa.  

||**Määrä (perus)**|**Käsiteltävä määrä**|**Laskutettava määrä (perus)**|**Määrä käsitelty (perus)**|**Määrä laskutettu (perus)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**F.var. nimikkeen seurantarivit** -sivu|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Lasku, 5 kappaletta.  

||**Määrä (perus)**|**Käsiteltävä määrä**|**Laskutettava määrä (perus)**|**Määrä käsitelty (perus)**|**Määrä laskutettu (perus)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**F.var. nimikkeen seurantarivit** -sivu|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md)   
 [Rakennetiedot: Nimikkeen seurantarivit -sivu](design-details-item-tracking-lines-window.md)
