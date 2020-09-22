---
title: Huollon hinnoittelun ja kustannusten määrittäminen | Microsoft Docs
description: Lisätietoja huollon hintojen ja lisäkustannusten määrittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 5b80a2f89ae958a58b8cddd3c239df1a11e63a0f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784582"
---
# <a name="set-up-pricing-and-additional-costs-for-services"></a>Huollon hintojen ja lisäkustannusten määrittäminen
Voit käyttää [!INCLUDE[d365fin](includes/d365fin_md.md)] hinnoitteluominaisuuksia määrittääksesi ja mukauttaaksesi sovellusta niin, että voit käyttää ja säätää palvelunimikkeiden, korjausten ja tilausten hinnoittelun. Nämä hinnoittelupäätökset on sitten helppo siirtää laskutusprosessiin.  
  
Tarpeen mukaan voit määrittää hinnoitteluryhmiä ja liittää niitä ajanjaksoihin, asiakkaisiin tai valuuttaan. Asiakkaiden huoltosopimusten mukaan voi määrittää kiinteän hinnoittelun sekä vähimmäis- ja enimmäishinnat. Hintojen muutokset voi tarkistaa ja hyväksyä ennen muutosten käyttöönottoa.  

## <a name="to-set-up-a-service-price-group"></a>Huoltohintaryhmien määrittäminen
Voit määrittää huoltonimikkeitä sisältäviä ryhmiä, joissa haluat käyttää samoja erikoishuoltohinnoittelua. Huoltohintaryhmiä määritellään huoltonimikeriveillä oleville huoltonimikkeille. Huoltohintaryhmiä voidaan liittää myös huoltonimikeryhmiin.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltohintaryhmät** ja valitse sitten liittyvä linkki.  
2. Luo uusi huoltohintaryhmä.  
3. Täytä **Koodi**- ja **Kuvaus**-kentät.  
4. Valitse **Asetukset**-toiminto.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > **Muokkaustyyppi**- ja **Summa**-kenttiä käytetään yhdessä määrittämään, koskeeko muutos kiinteää summaa tai käytetäänkö sitä vain, kun kokonaishuoltohinta ylittää tai alittaa **Summa**-kentän summan.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Huoltohintamuutoksen ryhmien määrittäminen  
Voit muuttaa huoltonimikkeiden huoltohinnoittelua määrittämällä hinnan muutosryhmän. Voit määrittää esimerkiksi hinnanmuutosryhmiä, jotka muuttavat rahdin tai varaosien hintaa.  
  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltohintamuutoksen ryhmät** ja valitse sitten liittyvä linkki.  
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
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltokustannukset** ja valitse sitten liittyvä linkki. 
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Huoltotilausten oletuskustannusten määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huollon asetukset** ja valitse sitten liittyvä linkki. 
2. Valitse **Huoltotilauksen aloituspalkkio** -kentässä sopiva palvelukustannus.

## <a name="see-also"></a>Katso myös
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Huoltohallinto](service-service.md)  
