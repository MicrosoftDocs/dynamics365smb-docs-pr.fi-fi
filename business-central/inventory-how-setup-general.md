---
title: Yleisten varastonhallinnan asetusten määrittäminen
description: Kuvaus siitä, miten fyysisen varaston ja varaston hallinta voidaan määrittää.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 73fbf09cff59556c04b43383c507a01883bbb071
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923743"
---
# <a name="set-up-general-inventory-information"></a>Yleisten varastotietojen määrittäminen

Yleiset varastoasetukset määritetään **Varastonhallinnan asetukset** -sivulla.

## <a name="to-set-up-general-inventory-information"></a>Yleisten varastotietojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten liittyvä linkki.
2. Täytä **Varastonhallinnan asetukset** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Lisätietoja kustannuslaskentakentistä, **Automaattisesta kustannusten kirjaamisesta**, **Oletetusta kustannusten kirjaamisesta KP:oon** ja **Oletuskustannuslaskentamenetelmästä** on kohdassa [Varaston kustannusten täsmäyttäminen pääkirjanpitoon](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Suunnittelun tiedot: varaston kustannuslaskelma](design-details-inventory-costing.md) ja [Suunnittelun tiedot: oletettu kustannuskirjaus](design-details-expected-cost-posting.md). Lisätietoja yleisestä kustannuslaskennasta on kohdassa [Varastokustannusten hallinta](finance-manage-inventory-costs.md).  

Jos haluat sisällyttää fyysisen varastoinnin käsittelyajan ostorivin toimituksen lupaamisen laskentaan, voit määrittää sen oletusarvoksi varastolle ja sijainnille **Varastonhallinnan asetukset** -sivulla. Lisätietoja on kohdassa [Toimituksen lupaamisen päivämäärän laskeminen](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> **Automaattinen kustannusten oikaisu** -näppäin otetaan oletusarvoisesti käyttöön, jotta varaston arvot ovat aina oikeat kirjanpidossa, mikä puolestaan pitää myynti- ja tuottotilastot ajan tasalla. Kustannusten muutokset saapuvista merkinnöistä, kuten ostoista tai tuotannosta, kohdistetaan niihin liittyviin lähteviin tietoihin, kuten myynteihin tai siirtoihin. Tämä on hyödyllistä uusille [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakkaille ja pienille yrityksille, joilla on suhteellisen alhaiset varastotransaktiotasot. Yrityksen kasvaessa ja varastotasojen kasvaessa tämä voi kuitenkin hidastaa järjestelmän suorituskykyä. Jos haluat vähentää suorituskykyä kirjauksen aikana, valitse ajan asetus, joka määrittää, kuinka kauas taaksepäin käsittelypäivämäärästä lähtien saapuva tapahtuma voi aiheuttaa liittyvien lähtevien arvotapahtumien muuttamisen. Vaihtoehtoisesti voit muuttaa kustannuksia säännöllisin väliajoin Muuta kust.-nimike tapahtumat -eräajon avulla.

## <a name="see-also"></a>Katso myös
[Varastonhallinnan määrittäminen](inventory-setup-inventory.md)  
[Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md)    
[Varaston hallinta](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)
