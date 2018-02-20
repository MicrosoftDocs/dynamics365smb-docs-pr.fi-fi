---
title: "Rakennetiedot – Kiinteä uusintatilauksen määrä | Microsoft Docs"
description: "Kiinteä uudelleenjärjestysmäärän menettely liittyy tyypillisten C-nimikkeiden varaston suunnitteluun (alhaiset varastokustannukset, vanhenemisriski ja/tai useita nimikkeitä) Tätä menetelmää käytetään yleensä silloin, kun tilauspiste vaikuttaa odotettuun kysyntään nimikkeen toimitusajan aikana."
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
ms.openlocfilehash: 7726a1b5749aa4da14d06d3484ee83668531f84f
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-fixed-reorder-qty"></a>Rakennetiedot: Kiinteä uusintatil. määrä
Kiinteä uusintatilausmäärän menettely liittyy tyypillisten C-nimikkeiden varaston suunnitteluun (alhaiset varastokustannukset, vanhenemisriski ja/tai useita nimikkeitä) Tätä menetelmää käytetään yleensä silloin, kun tilauspiste vaikuttaa odotettuun kysyntään nimikkeen toimitusajan aikana.  

## <a name="calculated-per-time-bucket"></a>Laskettu aikavälikohtaisesti  
 Jos suunnittelujärjestelmä havaitsee, että lisätilauspiste on saavutettu tai se ylitetään määritetyllä aikajaksolla (lisätilausjaksolla) (arvo ylittää lisätilauspisteen tai on sen tasolla jakson alussa tai arvo on lisätilauspisteen alapuolella tai sen tasolla jakson lopussa), järjestelmä ehdottaa uuden toimitustilauksen luomista määritetyllä lisätilausmäärällä. Järjestelmä ehdottaa myös aikataulun siirtämistä eteenpäin aikajakson loppumista seuraavasta päivästä.  

 Jaksotettu jälkitilauspisteen konsepti vähentää tarjontaehdotusten määrää. Tämä vaikuttaa säännöllisesti suoritettavaan manuaaliseen prosessiin eli varaston läpi kävelyyn ja eri varastopaikkojen todellisen sisällön tarkistamiseen.  

## <a name="creates-only-necessary-supply"></a>Luo vain tarvittavan kysynnän  
 Ennen uuden toimitustilauksen ehdottamista uusintatilauspisteen täyttämiseksi suunnittelujärjestelmä tarkistaa, onko toimitus jo tilattu vastaanotettavaksi nimikkeen toimitusaikana. Jos olemassa oleva toimitustilaus ratkaisee ongelman muuttamalla suunnitellun varaston uusintatilauspisteeseen tai sen yläpuolelle toimitusaikana, järjestelmä ei ehdota uutta toimitustilausta.  

 Toimitustilaukset, jotka on luoto erityisesti kohtaamaan jälkitilaustarve, poistetaan tavanomaisesta tarjonnan tasapainotuksesta, eikä niitä voida mitenkään muuttaa jälkeenpäin. Näin ollen, jos uusintatilauspiste poistetaan (ei uusita), tällöin on suositeltavaa tarkistaa avoimet toimitustilaukset manuaalisesti tai muuttaa uusintatilaustapa arvoon erä-erästä, jolloin järjestelmä vähentää tai peruuttaa tarpeettoman tarjonnan.  

## <a name="combines-with-order-modifiers"></a>Yhdistää tilausmääritteiden kanssa  
 Tilauksen muokkaajien, minimitilausmäärä, maksimitilausmäärä ja tilauksen moninkertaistaminen, ei tulisi näytellä isoa roolia, kun käytetään kiinteää jälkitilausmäärätapaa. Koska suunnittelujärjestelmä ottaa edelleen nämä muuttujat huomioon ja vähentää määrän määritettyyn enimmäistilausmäärään (ja luo kaksi toimitusta tai useampia kokonaistilausmäärän saavuttamiseksi), kasvata tilausta määritettyyn vähimmäistoimituksen määrään tai pyöristä tilausmäärä ylös määritetyn tilauskerrannaisen kattamiseksi.  

## <a name="combines-with-calendars"></a>Yhdistäminen kalentereihin  
 Ennen kuin uusintatilauspisteen täyttämiseen ehdotetaan uutta toimitustilausta, suunnittelujärjestelmä tarkistaa, onko tilaus ajoitettu **Yritystiedot**- ja **Sijaintikortti**-ikkunoiden **Peruskalenterin koodi** -kentässä määritettyjen kalenterien mukaiselle ei-työskentelypäivälle.  

 Jos suunniteltu päivämäärä ei ole työpäivä, suunnittelujärjestelmä siirtää tilauksen seuraavalle työpäivälle. Tämä voi johtaa tilaukseen, joka täyttää uusintatilauspisteen, mutta ei täytä mitään tiettyä kysyntää. Suunnittelujärjestelmä luo ylimääräisen tarjonnan vastaamaan epätasapainoiseen kysyntään.  

## <a name="should-not-be-used-with-forecast"></a>Ei tule käyttää ennusteen kanssa  
 Koska oletettu kysyntä on jo ilmaistu uusintatilauspisteen tasolla, ennusteen liittäminen nimikkeen suunnitteluun uusintatilauspisteen avulla ei ole tarpeellista. Jos suunnitelman perustaminen ennusteeseen on asianmukaista, käytä erä-erästä-käytäntöä.  

## <a name="must-not-be-used-with-reservations"></a>Ei tule käyttää varausten kanssa  
 Jos käyttäjä on varannut määrän, esimerkiksi varastossa olevan määrän jollekin tulevaisuudessa tapahtuvalle kysynnälle, suunnitelman perusta häiriintyy. Vaikka oletettu saatavilla oleva varasto on hyväksyttävä suhteessa uusintatilauspisteeseen, määrät eivät ehkä ole käytettävissä varauksen vuoksi. Järjestelmä voi yrittää korjata tilannetta luomalla poikkeustilauksia. On kuitenkin suositeltavaa määrittää niiden nimikkeiden Varaa-kentän arvoksi Ei koskaan, jotka on suunniteltu käyttämällä uusintatilauspistettä.  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md)   
 [Rakennetiedot: enimmäismäärä](design-details-maximum-qty.md)   
 [Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
 [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
 [Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)

