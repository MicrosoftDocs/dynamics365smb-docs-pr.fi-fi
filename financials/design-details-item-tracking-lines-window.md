---
title: "Rakennetiedot – Nimikkeen seurantarivit -ikkuna | Microsoft Docs"
description: "Lisätietoja varaston sarja- ja eränumerovirran hallinnasta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 62070ef4e580a3bd665130c9b017bf164bbe2142
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-item-tracking-lines-window"></a>Rakennetiedot: nimikkeen seurantarivit -ikkuna
Nimikkeen seurantatietueet ja varaustietueet luodaan varausjärjestelmässä ja niiden saatavuus lasketaan dynaamisesti. **Nimikkeen seurantarivit** -ikkunassa kirjoitettuja tietoja hallitaan väliaikaisella **Seurannan määrittely** -taulukon versiolla. Kun ikkuna suljetaan, aktiiviset tiedot lisätään **Varaustapahtuma**-taulukkoon ja historialliset tiedot **Seurannan määrittely** -taulukkoon. Lisätietoja on kohdassa [Rakennetiedot: aktiivisen nimikkeen seurantatapahtumat verrattuna historiallisen nimikkeen seurantatapahtumiin](design-details-active-versus-historic-item-tracking-entries.md).  
  
**Sarjanumero**- ja **Eränro**-kentissä suoritettu haku näyttää saatavuuden perustuen sekä **Nimiketapahtuma**-taulukkoon että **Varaustapahtuma**-taulukkoon ilman päivämääräsuodatinta. Määräkenttien taulukko **Nimikkeen seurantarivit** -ikkunan otsikossa näyttää dynaamisesti nimikkeen seurantanumeroiden määrät ja summat, jotka syötetään ikkunan riveille. Määrien tulee vastata asiakirjarivillä olevia määriä, joka ilmaistaan ikkunan otsikossa olevalla arvolla **0** **Määrittämätön**-kentissä.  
  
Sarja- ja eränumeroiden varaston läpi kulkevan virran koordinoinnissa käytetään seuraavia **Nimikkeen seurantarivit** -ikkunassa olevia tietojen syöttämisen sääntöjä:  
  
* Sekä saapuviin että lähteviin nimikkeen seurantariveihin ei voi syöttää sarja- tai eränumeroa, eränumeron kanssa tai ilman, useammin kuin yhden kerran **Nimikkeen seurantarivit** -ikkunan samassa esiintymässä. Jos yrität kirjoittaa minkä tahansa jo ikkunassa olevan sarja- ja eränumeroiden yhdistelmän, virhesanoma estää tietojen kirjoittamisen.  
* Et voi kirjata saapuvan nimikkeen seurantariveille liittyvää asiakirjaa, jos varastossa on jo nimike, jolla on sama variantti ja sama sarjanumero. Jos yrität kirjata positiivisen rivin varastonimikkeelle samalla variantilla ja sarjanumerolla, virhesanoma estää kirjauksen. Avointen asiakirjojen sekä saapuvan että lähtevän nimikkeen seurantariveillä voi kuitenkin olla sama sarja- tai eränumeroiden yhdistelmä, joka liittyy eri lähdeasiakirjan riveihin, eli joka on olemassa **Nimikkeen seurantarivit** -ikkunan eri esiintymissä, kunnes liittyvä asiakirja kirjataan.  
* Jos nimikkeelle on määritetty sarjanumerokohtainen seuranta tai eränumerokohtainen seuranta, et voi kirjata lähtevää asiakirjariviä, ellei varastossa ole nimikettä, jolle on määritetty sarja- tai eränumero. Jos yrität kirjata lähtevän asiakirjarivin nimikkeelle sarja- tai eränumerolla jota ei ole varastossa, virhesanoma estää kirjauksen.  
  
Tietojen kirjauksen säännöt **Nimikkeen seurantarivit** -ikkunassa tukevat myös kytkentäperiaatteita, jotka kattavat tilausseurannan, suunnittelun ja varauksen. Katso lisätiedot kohdasta [Rakennetiedot: nimikkeen seuranta ja suunnittelu](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Katso myös  
[Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md)
