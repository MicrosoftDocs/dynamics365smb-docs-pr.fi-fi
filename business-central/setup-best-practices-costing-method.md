---
title: Parhaiden käytäntöjen määrittäminen - arvostusmenetelmä
description: Arvostusmenetelmä-määrittää nimikkeen kortilla, miten nimikkeen kustannusvirta tallennetaan ja siirretäänkö todellinen tai budjetoitu arvo pääomaan ja käytetäänkö sitä kustannuslaskennassa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 537c99c5057dd5f810fe31848a8605417ae5e7dc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391447"
---
# <a name="setup-best-practices-costing-method"></a>Parhaiden käytäntöjen määrittäminen: Arvostusmenetelmä

**Arvostusmenetelmä**-määrittää nimikkeen kortilla, miten nimikkeen kustannusvirta tallennetaan ja siirretäänkö todellinen tai budjetoitu arvo pääomaan ja käytetäänkö sitä kustannuslaskennassa.  

 Oikean kustannusmenetelmän määrittäminen nimikkeen tyypin ja liiketoimintaympäristön mukaan on tärkeää edullisen vaihto-omaisuuden varmistamiseksi.  

 Seuraavassa taulukossa on parhaita käytäntöjä siitä, miten voit määrittää **Arvostusmenetelmä**-kentän. Katso lisätietoja kohdasta [Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md).  

|Asetusvaihtoehto|Parhaat käytännöt|Kommentti|  
|------------------|-------------------|-------------|  
|FIFO|Käytä, jos tuotteen kustannus on vakaa.<br /><br /> Käytä nimikkeille, joilla on rajoitettu varastointiaika, koska vanhimmat tavarat täytyy myydä ennen kuin niiden viimeinen myyntipäivä ohitetaan.|Nimikkeen yksikkökustannus on FIFO-säännön perusteella valitun nimikkeen vastaanoton todellinen arvo.<br /><br /> Varastonarvostuksessa oletetaan, että ensin varastoon sijoitetut nimikkeet myydään ensin. **Huomautus:**  Kun hinnat nousevat, taseessa näkyy suurempi arvo. Tämä tarkoittaa, että verovelat kasvavat, mutta luottoluokitus ja rahanlainauskyky paranevat.|  
|LIFO|Käytä, jos varastojen tasoja pidetään jatkuvasti yllä tai nostetaan ajan mittaan.|Nimikkeen yksikkökustannus on LIFO-säännön perusteella valitun nimikkeen vastaanoton todellinen arvo.<br /><br /> Varastonarvostuksessa oletetaan, että viimeiseksi varastoon sijoitetut nimikkeet myydään ensin. **Huomautus:**  Kun hinnat nousevat, tuloslaskelman arvo pienenee. Tämä tarkoittaa, että verovelat vähenevät, mutta rahanlainauskyky heikkenee. **Tärkeää:** Tätä ei sallita monissa maissa tai monilla alueilla, koska sitä voidaan käyttää voiton alas painamiseen.|  
|Keskiarvo|Käytä, jos tuotteen kustannus on epävakaa.<br /><br /> Käytä, jos vaihto-omaisuus on pinottu tai sekoitettu yhteen, eikä niitä voida erottaa, kuten kemikaalit.|Nimikkeen yksikkökustannus lasketaan kussakin vaiheessa keskimääräisenä yksikkökustannuksena oston jälkeen.<br /><br /> Varastonarvostus olettaa, että kaikki vaihto-omaisuus myydään samanaikaisesti.|
|Määrätty|Käytä tuotannon tai kaupan helposti tunnistettavissa nimikkeissä, joilla on suhteellisen korkeat yksikkökustannukset.<br /><br /> Käytä nimikkeisiin, jotka ovat säännön alainen.<br /><br /> Käytä nimikkeille, joilla on sarjanumero.|Nimikkeen yksikkökustannus on tarkka kustannus, jolloin tietty yksikkö vastaanotettiin.|
|Vakio|Käytä, jos kustannusten valvonta on erittäin tärkeää.<br /><br /> Käytä toistuvassa valmistuksessa arvostaaksesi suoria materiaali- ja resurssikustannuksia sekä valmistuksen yleiskustannuksia.<br /><br /> Käytä, jos käytössä on kurinalaisuutta ja henkilöstö ylläpitää standardeja.|Nimikkeen yksikkökustannus määritetty etukäteen arvion perusteella.<br /><br /> Kun todelliset kustannukset realisoituvat myöhemmin, vakiokustannus täytyy mukauttaa todellisiin kustannuksiin varianssin arvojen kautta.|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md)   
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
 [Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla](set-up-complex-application-areas-using-best-practices.md)  
 [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]