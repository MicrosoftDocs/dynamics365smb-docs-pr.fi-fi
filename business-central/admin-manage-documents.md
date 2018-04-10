---
title: Asiakirjojen hallinta, poistaminen tai pakkaaminen | Microsoft Docs
description: "Säilytä vanhat historiatiedot tai poista ne."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 696100bfbcc987b1d684e7987e7fd43979813282
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a>Asiakirjojen hallinta
Keskitetyn roolin, kuten sovelluksen järjestelmänvalvojan, on huolehdittava säännöllisesti siitä, että vanhat asiakirjat joko poistetaan tai tiivistetään.  

## <a name="delete-documents"></a>Asiakirjojen poistaminen
Jossain tapauksissa voi olla tarpeen poistaa laskutettuja ostotilauksia, joita ei ole poistettu. [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa, että poistetut ostotilaukset on laskutettu kokonaan. Tilauksia, joita ei ole kokonaan laskutettu ja vastaanotettu, ei voi poistaa.  

Ohjelma poistaa palautustilaukset tavallisesti sen jälkeen, kun ne on laskutettu. Kun kirjaat laskun, se siirretään **Kirjattu ostohyvityslasku** -ikkunaan. Jos kuitenkin olet valinnut  **Palautustoimitus hyvityslaskutettaessa** -valintaruudun **Ostojen ja ostovelkojen asetukset** -ikkunassa, lasku siirretään **Kirjattu palautustoimitus** -ikkunaan. Voit poistaa asiakirjat **Poista laskutetut ostopal.til.** -eräajolla. Eräajo tarkistaa ennen poistamista, onko ostopalautustilaukset toimitettu ja laskutettu kokonaan.  

Puiteostotilauksia ei poisteta sen jälkeen, kun kaikki liittyvät ostotilaukset on käsitelty ja laskutettu. Puitetilaukset voi poistaa **Poista lask. puiteostotilaukset** -eräajolla.  

Laskutetut huoltotilaukset poistetaan ohjelmasta automaattisesti sen jälkeen, kun ne on laskutettu kokonaan. Kun lasku on kirjattu, vastaava tapahtuma luodaan **Kirjatut huoltolaskut** -ikkunassa. Kirjattua asiakirjaa voi katsella **Kirjattu huoltolasku** -ikkunassa.  

Ohjelma ei poista huoltotilauksia automaattisesti, jos tilauksen kokonaismäärä on kirjattu **Huoltolasku**-ikkunassa itse huoltotilauksen sijaan. Tällöin sinun on ehkä poistettava laskutetut tilaukset, joita ei poistettu. Voit tehdä sen suorittamalla **Poista laskutetut huoltotilaukset** -eräajon.  

## <a name="see-also"></a>Katso myös  
[Hallinta](admin-setup-and-administration.md)  
