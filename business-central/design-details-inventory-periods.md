---
title: Rakennetiedot – varastokaudet | Microsoft Docs
description: Takautuvat tapahtumat tai kustannusten muutokset vaikuttavat usein varaston arvostukseen tilikausilla, joiden voidaan katsoa olevan suljettuja. Tällä voi olla kielteisiä vaikutuksia raportointiin erityisesti globaaleissa yrityksissä. Varastojaksot -toimintoa voidaan käyttää tällaisten ongelmien välttämiseen avaamalla tai sulkemalla varastokausia, jolloin voidaan rajata tiliöinti ajanjaksosarjaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 2231fcd34d45ae487bf3344a1efe2e317c75c89a
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215076"
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
 [Business Central -sovelluksen käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]