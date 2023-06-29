---
title: Kohdistuksen tila ja korjauksen tila | Microsoft Docs
description: Lisätietoja huoltonimikkeiden korjauksen tilan ja niiden kohdistustapahtumien kohdistuksen tilan välisestä suhteesta.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resources, allocation, status, repairs'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocation-status-and-repair-status-of-service-items"></a><a name="allocation-status-and-repair-status-of-service-items"></a>Huoltonimikkeen kohdistuksen tila ja korjauksen tila
Huoltonimikkeiden korjauksen tilalla ja huoltonimikkeiden kohdistustapahtumien kohdistuksen tilalla on tietty yhteys Huoltohallinnossa. Kohdistuksen tila muuttuu silloin kun huoltonimikkeen korjauksen tila muutetaan **Valmiiksi** tai **Osittain huolletuksi** ja kun huoltotarjous muunnetaan huoltotilaukseksi. Huoltonimikkeen korjauksen tila muuttuu, kun peruutat huoltonimikkeen kohdistuksen tai kohdistat sen toiseen resurssiin. Voit tarkastella huoltonimikkeiden korjauksen tilaa **Huoltotehtävät** -sivulla ja voit päivittää korjauksen tilan **Korjauksen tilakoodi** -kentässä **Huoltonimikkeen työkirja** -sivulla. Voit tarkastella kohdistuksen tilaa **Tila**-kentässä **Resurssin kohdistukset** -sivulla.  
  
## <a name="changing-repair-status"></a><a name="changing-repair-status"></a>Korjauksen tilan muuttaminen
Kun huoltonimikerivillä olevan huoltonimikkeen korjauksen tilaa muutetaan, ohjelma etsii huoltonimikkeelle vastaavaa kohdistustapahtumaa, jolla on tilana **Aktiivinen**. Jos tällainen kohdistustapahtuma löytyy, ohjelma päivittää sen tilan jollakin seuraavista tavoista:  
  
* Jos korjauksen tila muutetaan **Valmiiksi**, ohjelma muuttaa kohdistuksen tilan **Aktiivisesta** **Valmiiksi**.  
* Jos korjauksen tila muutetaan **Osittain huolletuksi** (osa huollosta on suoritettu loppuun) tai **Lykätyksi** (mitään huoltoa ei ole tehty), ohjelma muuttaa kohdistuksen tilan **Aktiivisesta** **Uudelleenkohdistamista tarvitaan** -tilaksi.  
* Kun huoltotilauksen kohdistustapahtuma on luotu (eli resursseja ei ole kohdistettu), ohjelma asettaa **Resurssin kohdistus** -sivun **Tila**-kentän arvoksi **Ei-aktiivinen**.  
* Ohjelma asettaa kohdistustapahtuman tilaksi  **Peruutettu**, kun kohdistat viitatun huoltonimikkeen uudelleen huoltotilauksen kohdistustapahtumaan. Se tarkoittaa, että kohdistettu resurssi tai resurssiryhmä ei ole yrittänyt suorittaa huoltotehtävää.  
  
Kohdistuksen tila kuvastaa, milloin huoltoprosessi on päättynyt, tai milloin toista resurssia tarvitaan huoltonimikkeen huollon loppuun suorittamiseksi.  
  
## <a name="converting-service-quotes-to-service-orders"></a><a name="converting-service-quotes-to-service-orders"></a>Huoltotarjousten muuntaminen huoltotilauksiksi
Kun huoltotarjous muunnetaan huoltotilaukseksi, ohjelma päivittää huoltotilauksen, tilauksessa olevat huoltonimikkeet sekä niiden kohdistustapahtumat seuraavalla tavalla:  
  
* Ohjelma muuttaa huoltonimikkeiden korjauksen tilaksi **Alku**.  
* Huoltotilauksen tilaksi muutetaan **Odottava**.  
* Ohjelma etsii kaikkien huoltotilauksessa olevien huoltonimikkeiden osalta kohdistustapahtumia, joiden tila on **Aktiivinen**. Jos tällaisia kohdistustapahtumia löytyy, ohjelma muuttaa niiden kohdistuksen tilaksi **Uudelleenkohdistamista tarvitaan** **Aktiivisen** sijaan.  
  
## <a name="canceling-allocations"></a><a name="canceling-allocations"></a>Kohdistusten peruuttaminen
Kun huoltonimikkeen kohdistus peruutetaan, [!INCLUDE[prod_short](includes/prod_short.md)] päivittää vastaavan kohdistustapahtuman kohdistuksen tilan tilasta **Aktiivinen** tilaan **Uudelleenkohdistus tarvitaan**.

Ohjelma päivittää kohdistustapahtumassa olevan huoltonimikkeen korjauksen tilan seuraavilla tavoilla:  
  
* Jos korjauksen tila on **Alku**, ohjelma muuttaa korjauksen tilaksi **Lykätty** (huoltoa ei ole aloitettu).  
* Jos korjauksen tila on **Työn alla**, ohjelma muuttaa korjauksen tilaksi **Osittain huollettu** (osa huollosta on suoritettu loppuun).  
  
## <a name="reallocating-an-active-allocation-entry"></a><a name="reallocating-an-active-allocation-entry"></a>Aktiivisen kohdistustapahtuma uudelleenkohdistaminen
Kun huoltonimike uudelleenkohdistetaan kohdistustapahtumassa, jonka tila on **Aktiivinen**, ohjelma päivittää kohdistustapahtuman seuraavilla tavoilla:  
  
* Jos huolto aloitettiin silloin, kun kohdistus oli **Aktiivinen** (eli tapahtumassa olevan huoltonimikkeen korjauksen tilaksi muutettiin **Työn alla**), ohjelma muuttaa kohdistuksen tilan **Aktiivisesta** **Valmiiksi**.  
* Jos huoltoa ei aloitettu silloin, kun kohdistus oli **Aktiivinen**, ohjelma muuttaa kohdistuksen tilan **Aktiivisesta** **Peruutetuksi**.  
  
Ohjelma päivittää kohdistustapahtumassa olevan huoltonimikkeen korjauksen tilan samalla tavalla kuin olisit peruuttanut kohdistuksen:  
  
* Jos korjauksen tila on **Alku**, ohjelma muuttaa korjauksen tilaksi **Lykätty** (huoltoa ei ole aloitettu).  
* Jos korjauksen tila on **Työn alla**, ohjelma muuttaa korjauksen tilaksi **Osittain huollettu** (osa huollosta on suoritettu loppuun).  
  
Ohjelma luo uuden kohdistustapahtuman, joka sisältää uuden resurssin ja jonka tila on  **Aktiivinen**.  
  
## <a name="reallocating-a-service-item"></a><a name="reallocating-a-service-item"></a>Huoltonimikkeen uudelleenkohdistaminen
Kun huoltonimike uudelleenkohdistetaan kohdistustapahtumassa, jonka tilana on **Uudelleenkohdistamista tarvitaan**, ohjelma päivittää kohdistustapahtuman seuraavilla tavoilla:  
  
* Jos huolto aloitettiin silloin, kun kohdistus oli **Aktiivinen** (eli tapahtumassa olevan huoltonimikkeen korjauksen tilaksi muutettiin **Työn alla**), ohjelma muuttaa kohdistuksen tilan **Uudelleenkohdistus tarvitaan** **Valmiiksi**.  
* Jos huoltoa ei aloitettu silloin, kun kohdistus oli **Aktiivinen**, ohjelma muuttaa kohdistuksen tilan **Uudelleenkohdistus tarvitaan** **Peruutetuksi**.  
  
Uusi kohdistustapahtuma sisältää uuden resurssin ja sen tila on **Aktiivinen**.  
  
## <a name="see-also"></a><a name="see-also"></a>Katso myös
[Resurssien kohdistamisen määrittäminen](service-how-setup-resource-allocation.md)  
[Resurssien kohdistaminen](service-how-to-allocate-resources.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
