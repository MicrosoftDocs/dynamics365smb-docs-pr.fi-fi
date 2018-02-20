---
title: "Rakennetiedot – varastokaudet | Microsoft Docs"
description: "Takautuvat tapahtumat tai kustannusten muutokset vaikuttavat usein varaston arvostukseen tilikausilla, joiden voidaan katsoa olevan suljettuja. Tällä voi olla kielteisiä vaikutuksia raportointiin erityisesti globaaleissa yrityksissä. Varastojaksot -toimintoa voidaan käyttää tällaisten ongelmien välttämiseen avaamalla tai sulkemalla varastokausia, jolloin voidaan rajata tiliöinti ajanjaksosarjaan."
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
ms.openlocfilehash: 742891cc8037696748b7beb459cc877ea482e2a1
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-inventory-periods"></a>Rakennetiedot: varastokausi
Takautuvat tapahtumat tai kustannusten muutokset vaikuttavat usein varaston arvostukseen tilikausilla, joiden voidaan katsoa olevan suljettuja. Tällä voi olla kielteisiä vaikutuksia raportointiin erityisesti globaaleissa yrityksissä. Varastojaksot -toimintoa voidaan käyttää tällaisten ongelmien välttämiseen avaamalla tai sulkemalla varastokausia, jolloin voidaan rajata tiliöinti ajanjaksosarjaan.  

 Varastokausi on tietty ajanjakso, joka määritetään päättymispäivämäärällä, johon kirjaat varastotapahtumia. Kun suljet varastokauden, siihen ei enää voi kirjata arvomuutoksia. Tämä sisältää uusien arvojen kirjaamiset, oletetut tai laskutetut kirjaamiset, olemassa olevien arvojen muutokset ja kustannusten muutokset. Voit kuitenkin edelleen käyttää avointa nimiketapahtumaa, joka on suljetulla ajanjaksolla. Katso lisätiedot kohdasta [Rakennetiedot: nimikkeen kohdistus](design-details-item-application.md).  

 Voit varmistaa, että kaikki suljetun kauden tapahtumat ovat lopullisia, tarkistamalla, että seuraavat ehdot täyttyvät ennen varastokauden sulkemista:  

-   Kaikki jakson lähtevät nimiketapahtumat on suljettava (ei negatiivista varastoa).  
-   Kaikki jakson nimikkeen kustannuksia on muutettava.  
-   Kaikkien jakson julkaistujen ja valmiiden tuotantotilausten kustannusta on muutettava.  

 Kun suljet varastokauden, varastokauden tapahtuma luodaan varastokauden edellisen nimiketapahtuman numeron avulla. Lisäksi varastokauden tapahtumaan tallennetaan aika, päivämäärä ja kauden sulkevan käyttäjän käyttäjäkoodi. Käyttämällä tätä tietoa edellisen kauden viimeisen nimikerekisterin kanssa voit nähdä mitkä varastotapahtumat kirjattiin varastokaudella. Varastojaksojen uudelleen avaaminen on myös mahdollista, jos sinun tarvitsee kirjata suljetulla kaudella. Varastokauden avaamisen yhteydessä luodaan varastokauden tapahtuma.  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: varaston arvostus](design-details-inventory-costing.md) [Varaston kustannusten hallinta](finance-manage-inventory-costs.md) [Rahoitus](finance.md)  
 [Financialsin käyttäminen](ui-work-product.md)

