---
title: Huollon hinnoittelun ja kustannusten määrittäminen
description: Tietoja siitä, miten voit käyttää hinnoitteluominaisuuksia määrittääksesi ja mukauttaaksesi sovellusta niin, että voit käyttää ja säätää huoltonimikkeiden, korjausten ja tilausten hinnoittelun.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 52ffc9d1d0ebce87a4e0f952e3f742a0159e1cc1
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136949"
---
# <a name="set-up-pricing-and-additional-costs-for-services"></a>Huollon hintojen ja lisäkustannusten määrittäminen
Voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)] hinnoitteluominaisuuksia määrittääksesi ja mukauttaaksesi sovellusta niin, että voit käyttää ja säätää palvelunimikkeiden, korjausten ja tilausten hinnoittelun. Nämä hinnoittelupäätökset on sitten helppo siirtää laskutusprosessiin.  
  
Tarpeen mukaan voit määrittää hinnoitteluryhmiä ja liittää niitä ajanjaksoihin, asiakkaisiin tai valuuttaan. Asiakkaiden huoltosopimusten mukaan voi määrittää kiinteän hinnoittelun sekä vähimmäis- ja enimmäishinnat. Hintojen muutokset voi tarkistaa ja hyväksyä ennen muutosten käyttöönottoa.  

## <a name="to-set-up-a-service-price-group"></a>Huoltohintaryhmien määrittäminen
Voit määrittää huoltonimikkeitä sisältäviä ryhmiä, joissa haluat käyttää samoja erikoishuoltohinnoittelua. Huoltohintaryhmiä määritellään huoltonimikeriveillä oleville huoltonimikkeille. Huoltohintaryhmiä voidaan liittää myös huoltonimikeryhmiin.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltohintaryhmät** ja valitse sitten vastaava linkki.  
2. Luo uusi huoltohintaryhmä.  
3. Täytä **Koodi**- ja **Kuvaus**-kentät.  
4. Valitse **Asetukset**-toiminto.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > **Muokkaustyyppi**- ja **Summa**-kenttiä käytetään yhdessä määrittämään, koskeeko muutos kiinteää summaa tai käytetäänkö sitä vain, kun kokonaishuoltohinta ylittää tai alittaa **Summa**-kentän summan.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Huoltohintamuutoksen ryhmien määrittäminen  
Voit muuttaa huoltonimikkeiden huoltohinnoittelua määrittämällä hinnan muutosryhmän. Voit määrittää esimerkiksi hinnanmuutosryhmiä, jotka muuttavat rahdin tai varaosien hintaa.  
  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltohintamuutoksen ryhmät** ja valitse sitten vastaava linkki.  
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
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltokustannukset** ja valitse sitten vastaava linkki. 
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Huoltotilausten oletuskustannusten määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huollon asetukset** ja valitse sitten vastaava linkki. 
2. Valitse **Huoltotilauksen aloituspalkkio** -kentässä sopiva palvelukustannus.

## <a name="see-also"></a>Katso myös
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Huoltohallinto](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]