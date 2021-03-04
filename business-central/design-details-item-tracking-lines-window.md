---
title: Rakennetiedot – Nimikkeen seurantarivit -sivu | Microsoft Docs
description: Lisätietoja varaston sarja- ja eränumerovirran hallinnasta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a577d1fbb3744a7af899957af5ecb3b714bd8296
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917349"
---
# <a name="design-details-item-tracking-lines-page"></a>Rakennetiedot: Nimikkeen seurantarivit -sivu
Nimikkeen seurantatietueet ja varaustietueet luodaan varausjärjestelmässä ja niiden saatavuus lasketaan dynaamisesti. **Nimikkeen seurantarivit** -sivulla kirjoitettuja tietoja hallitaan väliaikaisella **Seurannan määrittely** -taulukon versiolla. Kun sivu suljetaan, aktiiviset tiedot lisätään **Varaustapahtuma**-taulukkoon ja historialliset tiedot **Seurannan määrittely** -taulukkoon. Lisätietoja on kohdassa [Rakennetiedot: aktiivisen nimikkeen seurantatapahtumat verrattuna historiallisen nimikkeen seurantatapahtumiin](design-details-active-versus-historic-item-tracking-entries.md).  
  
**Sarjanumero**- ja **Eränro**-kentissä suoritettu haku näyttää saatavuuden perustuen sekä **Nimiketapahtuma**-taulukkoon että **Varaustapahtuma**-taulukkoon ilman päivämääräsuodatinta. Määräkenttien taulukko **Nimikkeen seurantarivit** -sivun otsikossa näyttää dynaamisesti nimikkeen seurantanumeroiden määrät ja summat, jotka syötetään sivun riveille. Määrien tulee vastata asiakirjarivillä olevia määriä, joka ilmaistaan sivun otsikossa olevalla arvolla **0** **Määrittämätön**-kentissä.  
  
Sarja- ja eränumeroiden varaston läpi kulkevan virran koordinoinnissa käytetään seuraavia **Nimikkeen seurantarivit** -sivulla olevia tietojen syöttämisen sääntöjä:  
  
* Sekä saapuviin että lähteviin nimikkeen seurantariveihin ei voi syöttää sarja- tai eränumeroa, eränumeron kanssa tai ilman, useammin kuin yhden kerran **Nimikkeen seurantarivit** -sivun samassa esiintymässä. Jos yrität kirjoittaa minkä tahansa sivulla jo olevan sarja- ja eränumeroiden yhdistelmän, virhesanoma estää tietojen kirjoittamisen.  
* Et voi kirjata saapuvan nimikkeen seurantariveille liittyvää asiakirjaa, jos varastossa on jo nimike, jolla on sama variantti ja sama sarjanumero. Jos yrität kirjata positiivisen rivin varastonimikkeelle samalla variantilla ja sarjanumerolla, virhesanoma estää kirjauksen. Avointen asiakirjojen sekä saapuvan että lähtevän nimikkeen seurantariveillä voi kuitenkin olla sama sarja- tai eränumeroiden yhdistelmä, joka liittyy eri lähdeasiakirjan riveihin, eli joka on olemassa **Nimikkeen seurantarivit** -sivun eri esiintymissä, kunnes liittyvä asiakirja kirjataan.  
* Jos nimikkeelle on määritetty sarjanumerokohtainen seuranta tai eränumerokohtainen seuranta, et voi kirjata lähtevää asiakirjariviä, ellei varastossa ole nimikettä, jolle on määritetty sarja- tai eränumero. Jos yrität kirjata lähtevän asiakirjarivin nimikkeelle sarja- tai eränumerolla jota ei ole varastossa, virhesanoma estää kirjauksen.  
  
Tietojen kirjauksen säännöt **Nimikkeen seurantarivit** -sivulla tukevat myös kytkentäperiaatteita, jotka kattavat tilausseurannan, suunnittelun ja varauksen. Katso lisätiedot kohdasta [Rakennetiedot: nimikkeen seuranta ja suunnittelu](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Katso myös  
[Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]