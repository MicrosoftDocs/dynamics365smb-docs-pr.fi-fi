---
title: "Kokoonpano tilausta varten -nimikkeiden ja varastonimikkeiden myyminen yhdessä | Microsoft Docs"
description: "Jos kokoonpanon nimike on määritetty Kokoonpano varastoon -toimintoa varten, myyntitilauksen oletusprosessi olettaa, että nimike on jo koottu ja se voidaan poimia varastosta, jos sitä on saatavana. Mutta jos osa määrästä (tai koko määrä) ei ole saatavilla, voit luoda joustavasti kokoonpanotilauksen jäljellä olevalle määrälle."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2e9076dd26e84e56962bbdc70d722449d8506b7b
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Kokoonpano tilausta varten -nimikkeiden ja varastonimikkeiden myyminen yhdessä
Jos kokoonpanon nimikkeen kortin **Kokoonpanokäytäntö**-kenttä sisältää **Kokoonpano varastoon** -kohdan, myyntitilauksen oletusprosessi olettaa, että nimike on jo koottu ja se voidaan poimia varastosta, jos sitä on saatavana. Tämän vuoksi yhtään kokoonpanotilausta ei luoda automaattisesti ja linkitetä myyntitilauksen riviin. Jos koko (tai osa) määrästä ei ole saatavana, voit luoda kokoonpanotilauksen jäljellä olevalle määrälle täyttämällä myyntitilausrivin **Kokoonpantava määrä tilausta varten** -kenttään arvon. Tällä tavalla voit määrittää nimikkeen kokoonpanon tilausta varten, vaikka se on määritetty kokoonpantavaksi varastoon.  

Samanlainen joustavuus on olemassa, kun myyt tilaukseen koottavia nimikkeitä, joista osa on varastossa ja haluat vähentää kyseisen osan kokoonpanotilauksesta. Lisätietoja on kohdassa [Varastonimikkeiden myyminen Kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
>  Tietyt säännöt koskevat **Toimitettava määrä** -kenttää myyntitilauksen riveillä, jotka sisältävät Kokoonpano tilausta varten -määrien ja varaston määrien yhdistelmiä. Lisätietoja on ohjeaiheen [Tietoja Kokoonpano tilausta varten- tai Kokoonpano varastoon -toiminnoista](assembly-assemble-to-order-or-assemble-to-stock.md) kohdassa Skenaarioiden yhdistelmä.  

> [!NOTE]  
>  Seuraavassa toimenpiteessä ei tehdä myyntitilauksen vakiovaiheita, jotka on tehtävä ennen kuin luot kokoonpanotilauksen määrälle, joka ei ole käytettävissä.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Myy kokoonpano tilausta varten -nimikkeitä ja varastonimikkeitä yhdessä  
1.  Anna varastoon kokoonpantavan nimikkeen myyntitilausrivin **Määrä**-kenttään, määrä, joka on suurempi kuin varasto. **Tarkista saatavuus** -ikkuna tulee näyttöön. Lisätietoja on kohdassa [Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md). 
2.  Kiinnitä huomiota **Määrä yhteensä** -kenttään (negatiivinen arvo), joka syötetään seuraavassa vaiheessa.  
3.  Anna **Kokoonpantava määrä tilausta varten** -kentässä arvo edellisestä vaiheesta.  
4.  Tee muutokset kokoonpanon komponentteihin. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  
5.  Siirry vapauttamaan myyntitilaus, valmistelemaan se varastonimikkeiden poimintaan ja ei-saatavissa olevien nimikkeiden kokoonpanoon. Lisätietoja näistä vakiokokoonpanovaiheista on kohdassa [Nimikkeiden kokoaminen](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Myyntitilauksen **Varastopaikkakoodi**-kenttä voidaan tarvittaessa esitäyttää sijaintikortin **Kokoonpanot. toim. var.p.koodi**- tai **Kokoonpanosta-varastop.koodi** -kentästä. Tässä tapauksessa myyntitilauksen rivin **Varastopaikkakoodi** saattaa olla virheellinen tässä kokoonpano tilausta varten -määrän ja kokoonpano varastoon -määrän yhdistelmässä. On hyvä tarkistaa **Varastopaikkakoodi**-kenttä ja varmistaa, että paikka sopii kaikille määrille. Voit myös kirjoittaa kaksi eri määrää myyntitilauksen eri riveille.  

## <a name="see-also"></a>Katso myös  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

