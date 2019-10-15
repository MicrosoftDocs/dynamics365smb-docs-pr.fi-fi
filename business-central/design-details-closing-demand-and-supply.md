---
title: Rakennetiedot – kysynnän ja tarjonnan sulkeminen | Microsoft Docs
description: Tässä ohjeaiheessa on ehdotuksia siitä, mitä voit tehdä tarjonnan tasapainotusmenetelmien suorittamisen jälkeen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, planning, example, closing, supply
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 19bc8ee3ec35a493273a1f80d076e948235c6f8a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307370"
---
# <a name="design-details-closing-demand-and-supply"></a>Rakennetiedot: kysynnän ja tarjonnan sulkeminen
Kun tarjonnan tasapainotusmenetelmät on suoritettu, tulos voi olla jokin seuraavista kolmesta vaihtoehdosta:  

* Vaadittu kysyntätapahtumien määrä ja päivämäärä on kohdattu ja niiden suunnittelu voidaan sulkea,. Tarjontatapahtuma on yhä avoinna ja se voi kattaa seuraavan kysynnän, joten täsmäytys voi alkaa nykyisestä tarjontatapahtumasta ja seuraavasta kysynnästä.  
* Toimitustilausta ei voi muokata niin, että se kattaa koko kysynnän. Kysyntätapahtuma on edelleen avoinna. Siinä on jokin katteeton määrä, joka voidaan kattaa seuraavalla tuotantotapahtumalla. Nykyinen tarjontatapahtuma siis suljetaan ja täsmäytystoiminto alkaa alusta nykyisestä kysynnästä ja seuraavasta tarjontatapahtumasta.  
* Kaikki kysyntä on otettu huomioon; kysyntää ei ole myöhemmin (tai kysyntää ei ole lainkaan). Jos olemassa on ylimääräistä tarjontaa, se voidaan vähentää (tai peruuttaa) ja sitten sulkea. On mahdollista, että myöhempänä ketjussa on lisää tarjontatapahtumia ja myös ne tulisi peruuttaa.  

Viimeiseksi suunnittelujärjestelmä luo tilauksen seurantalinkin tarjonnan ja kysynnän välille.  

## <a name="creating-the-planning-line-suggested-action"></a>Suunnittelurivin luonti (ehdotettu toimenpide)  
Jos toimitustilauksen korjaamista ehdotetaan jollakin toiminnolla, kuten uusi, muuta määrä, aikatauluta uudelleen, aikatauluta uudelleen ja muuta määrää tai peruuta, suunnittelujärjestelmä luo suunnittelurivin suunnittelutyökirjassa. Tilauksen seurannasta johtuen suunnitteluriviä ei luoda vain tarjontatapahtuman lopuksi mutta myös siinä tapauksessa, jos kysyntätapahtuma suljetaan, vaikka tarjontatapahtuma on yhä avoinna ja siihen saattaa kohdistua muita muutoksia seuraavan kysyntätapahtuman käsittelyn yhteydessä. Tämä tarkoittaa sitä, että jos suunnittelurivi on luotu ensimmäisenä, sitä voidaan muuttaa uudelleen.  

Tuotantotilausten käsittelyn aikaista tietokantayhteyden käyttöä voi minimoida ylläpitämällä suunnittelurivejä kolmella tasolla ja pyrkimällä käyttämään vähiten kuormittava ylläpitotasoa.  

* Luo vain suunnittelurivi nykyisellä eräpäivällä ja määrällä, mutta ilman reititystä ja komponentteja.  
* Sisällytä reititys: suunniteltu reititys asetellaan aloitus- ja lopetuspäivämäärät ja kellonajat mukaan lukien. Tämä on vaativaa tietokannan käyttöoikeuksia ajatellen. Kun haluat määrittää loppupäivämäärän ja eräpäivän, tämä on ehkä laskettava, vaikka tarjontatapahtumaa ei ole suljettu (jos kyseessä on aikataulutus eteenpäin).  
* Sisällytä tuoterakenteen purku: tämä voi odottaa hetkeä ennen tarjontatapahtuman sulkemista.  

Tämä päättää suunnittelujärjestelmän suorittaman kysynnän ja tarjonnan lataamisen, priorisoinnin ja täsmäytyksen kuvaukset. Järjestelmän on varmistettava yhdessä tämän tarjonnan suunnittelutehtävän kanssa, että jokaisen suunnitellun nimikkeen vaadittava varastotaso säilytetään sen uusintatilauskäytännön mukaisesti.  

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)
