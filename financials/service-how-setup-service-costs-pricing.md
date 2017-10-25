---
title: "Huollon hinnoittelun ja kustannusten määrittäminen | Microsoft Docs"
description: "Lisätietoja huollon hintojen ja lisäkustannusten määrittämisestä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d0f0fcdff4a67df7542c5acb6d44f804997d1a2c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-pricing-and-additional-costs-for-services"></a>Toimintaohje: Huollon hintojen ja lisäkustannusten määrittäminen
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)] hinnoitteluominaisuuksia määrittääksesi ja mukauttaaksesi sovellusta niin, että voit käyttää ja säätää palvelunimikkeiden, korjausten ja tilausten hinnoittelun. Nämä hinnoittelupäätökset on sitten helppo siirtää laskutusprosessiin.  
  
Tarpeen mukaan voit määrittää hinnoitteluryhmiä ja liittää niitä ajanjaksoihin, asiakkaisiin tai valuuttaan. Asiakkaiden huoltosopimusten mukaan voi määrittää kiinteän hinnoittelun sekä vähimmäis- ja enimmäishinnat. Hintojen muutokset voi tarkistaa ja hyväksyä ennen muutosten käyttöönottoa.  

## <a name="to-set-up-a-service-price-group"></a>Huoltohintaryhmien määrittäminen
Voit määrittää huoltonimikkeitä sisältäviä ryhmiä, joissa haluat käyttää samoja erikoishuoltohinnoittelua. Huoltohintaryhmiä määritellään huoltonimikeriveillä oleville huoltonimikkeille. Huoltohintaryhmiä voidaan liittää myös huoltonimikeryhmiin.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltohintaryhmät** ja valitse sitten aiheeseen liittyvä linkki.  
2. Luo uusi huoltohintaryhmä.  
3. Täytä **Koodi**- ja **Kuvaus**-kentät.  
4. Valitse **Asetukset**-toiminto.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > **Muokkaustyyppi**- ja **Summa**-kenttiä käytetään yhdessä määrittämään, koskeeko muutos kiinteää summaa tai käytetäänkö sitä vain, kun kokonaishuoltohinta ylittää tai alittaa **Summa**-kentän summan.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Huoltohintamuutoksen ryhmien määrittäminen  
Voit muuttaa huoltonimikkeiden huoltohinnoittelua määrittämällä hinnan muutosryhmän. Voit määrittää esimerkiksi hinnanmuutosryhmiä, jotka muuttavat rahdin tai varaosien hintaa.  
  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltohintamuutoksen ryhmät** ja valitse sitten aiheeseen liittyvä linkki.  
2. Luo uusi huoltohintamuutoksen ryhmä.  
3. Täytä **Koodi**- ja **Kuvaus**-kentät.  
4. ANna **Tyyppi**-kentässä säädettävän tapahtuman tyyppi.  
  
    * Voit muuttaa vain yhtä tiettyä tapahtumaa antamalla tämän tapahtuman numeron **Nro** -kentässä. Jos kenttä jätetään tyhjäksi, huoltohinnan muutosryhmä muuttaa kaikkia kohteita, jotka ovat **Tyyppi**-kentässä määrittyä tyyppiä.  
    * Jos haluat muuttaa vain yhteen tiettyyn huoltoon liittyviä huoltohintoja, täytä **Työn tyyppi**-kenttä. Jos kenttä jätetään tyhjäksi, järjestelmä ei ota sitä huomioon.  
  
5. Voit antaa **Kuvaus**-kenttään lyhyen kuvauksen huoltohinnan muutoksesta.  
6. Voit muuttaa vain tiettyyn yleiseen tuotteen kirjausryhmään liittyviä huoltohintoja täyttämällä **Yleinen tuotteen kirjausryhmä** -kentän.

> [!Tip]
> Voit lisätä muutosryhmää koskevia lisätietoja valitsemalla **Tiedot**. Voit esimerkiksi määrittää, mikä nimike kuuluu huoltohintamuutoksen ryhmään ja onko se nimike, resurssi, resurssiryhmä vai palvelumaksu.  

## <a name="to-set-up-additional-costs-for-services"></a>Huollon lisäkustannusten määrittäminen
Kun käsittelet huoltonimikkeitä ja -tilauksia, on ehkä rekisteröitävä lisäkustannuksia, kuten matkakulut tietyille huoltoalueille tai aloitusmaksut. Kun luot huoltotilauksen, voit lisätä nämä kustannukset ja **Kustannus**-tyypin rivi lisätään tilaukseen. Jos puolestaan haluat kohdistaa kustannukset kaikkiin huoltotilauksiin, voit määrittää oletuskustannuksen. Voit esimerkiksi haluta aina käyttää aloitusmaksua.
  
### <a name="to-set-up-service-costs"></a>Huoltokustannusten määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huoltokustannukset** ja valitse sitten aiheeseen liittyvä linkki. 
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Huoltotilausten oletuskustannusten määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Huollon asetukset** ja valitse sitten aiheeseen liittyvä linkki. 
2. Valitse **Huoltotilauksen aloituspalkkio** -kentässä sopiva palvelukustannus.

## <a name="see-also"></a>Katso myös
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Service Management](service-service.md)  

