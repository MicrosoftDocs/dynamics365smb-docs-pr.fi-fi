---
title: "Rakennetiedot – Arvioidun varastomäärän ja uusintatilauspisteen valvonta | Microsoft Docs"
description: "Lisätietoja tavasta, jolla varaston suunnittelu erottaa suunnitellun varaston ja suunnitellun saatavilla olevan varastomäärän."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5ee71f3c0a677115bba920e4b6d25eee6342e87e
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Rakennetiedot: arvioidun varastotason ja uusintatilauspisteen valvonta
Varasto on tarjonnan tyyppi mutta varaston suunnittelussa suunnittelujärjestelmä erottaa kaksi varastotasoa:  

* Suunniteltu varasto  
* Oletettu saatavilla oleva varasto  

## <a name="projected-inventory"></a>Suunniteltu varasto  
Aluksi arvioitu varasto on bruttovaraston määrä, mukaan lukien kysyntä ja tarjonta menneisyydessä vaikka sitä ei ole kirjattu, kun suunnitteluprosessi aloitetaan. Tulevaisuudessa tästä tulee liikkuva arvioitu varastotaso, jota ylläpidetään tulevan tarjonnan ja kysynnän bruttomäärillä, koska nämä tulevat mukaan ajan kuluessa (joko varattu tai muulla tavoin kohdistettu).  

Suunnittelujärjestelmä käyttää käsiteltyä varastoa tarkkailemaan jälkitilauspistettä ja määrittämään jälkitilausmäärän, kun käytetään jälkitilauksen maksimimäärätapaa.  

## <a name="projected-available-inventory"></a>Oletettu saatavilla oleva varasto  
Käsitelty käytettävissä oleva varasto on osa käsiteltyä varastoa, joka tiettyyn aikaan on käytettävissä täyttämään kysyntää. Suunnittelumoottori käyttää käsiteltyä käytettävissä olevaa varastoa, kun varmuusvaraston tasoa tarkkaillaan.  

Suunnittelujärjestelmä käyttää käsiteltyä käytettävissä olevaa varastoa tarkkaillakseen varmuusvarastoa, koska varmuusvaraston täytyy aina olla käytettävissä palvelemaan odottamatonta kysyntää.  

## <a name="time-buckets"></a>Aikavälit  
Ennustetun varastosaldon tiukka hallinta on tärkeää lisätilauspisteen tunnistamiseksi sekä oikean tilausmäärän laskemiseksi, kun enimmäistilausmäärän sääntö on käytössä.  

Kuten aiemmin mainittiin, arvioitu varastotaso lasketaan suunnittelujakson alussa. Se on bruttotaso, joka ei huomioi varauksia ja vastaavia kohdistuksia. Järjestelmä valvoo aikavälin koottuja muutoksia ja valvoo tätä varaston tasoa suunnitteluvaiheen aikana. Järjestelmä varmistaa, että aikaväli on vähintään yksi päivä, koska se on kysyntä- tai tarjontatapahtuman tarkin aikayksikkö.  

## <a name="determining-the-projected-inventory-level"></a>Arvioidun varastotason määrittäminen  
Seuraava jakso kuvaa sitä, kuinka suunniteltu varaston taso määritellään:  

* Kun tarjontatapahtuma, kuten ostotilaus, on kokonaan suunniteltu, se nostaa oletetun varaston arvoa eräpäivänä.  
* Kokonaan täytetty kysyntätapahtuma ei vähennä oletetun varaston arvoa heti. Sen sijaan se kirjaa vähennyksen muistutuksen, joka on sisäinen tietue, joka sisältää päivämäärän ja arvioituun varastoon lisättävän määrän.  
* Kun seuraavaa tarjontatapahtumaa suunnitellaan ja se asetetaan aikajanalle, kirjatut vähennyksen muistutukset tutkitaan yksi kerrallaan tarjonnan suunniteltuun päivämäärään asti oletetun varaston päivityksen aikana. Tämän prosessin aikana sisäisen noston lisätilaustaso voidaan saavuttaa tai ylittää.  
* Jos uusi toimitustilaus otetaan käyttöön, järjestelmä tarkistaa, onko se kirjoitettu ennen nykyistä tarjontaa. Jos se on, uudesta tarjonnasta tulee nykyinen tarjonta ja täsmäytys käynnistyy uudelleen.  

Seuraavassa esitetään graafinen kuvaus tästä periaatteesta:  

![](media/nav_app_supply_planning_2_projected_inventory.png "NAV_APP_supply_planning_2_projected_inventory")  

1. Määrän 4 tarjonta **Sa** (kiinteä) sulkee kysynnän **Da** määrällä -3.  
2. CloseDemand: Luo vähennyksen muistutus -3 (ei näkyvillä).  
3. Tarjonta **Sa** on suljettu ylijäämällä 1 (kysyntää ei enää ole).  

     Tämä nostaa oletetun varaston tasoksi +4, kun taas oletetun **saatavilla** olevan varaston tasoksi tulee -1.  

4. Seuraava määrältään 2 tarjonta **Sb** (toinen tilaus) on jo asetettu aikajanalle.  
5. Järjestelmä tarkistaa, onko mitään vähenemismuistutusta ennen **Sb:tä** (ei ole, joten mitään toimintoa ei suoriteta).  
6. Järjestelmä sulkee tarjonnan **Sb** (kysyntää ei enää ole) – joko A: vähentämällä sen nollaan (peruutus) tai B: jättämällä sen ennalleen.  

     Tämä kasvattaa ennustettua varastosaldoa (A: +0 => +4 tai B: +2 = +6).  

7. Järjestelmä tekee lopullisen tarkastuksen: onko mitään vähenemismuistutusta? Kyllä, löytyy yksi päivämääränä **Da**.  
8. Järjestelmä lisää muistutuslaskun (-3) ennustettuun varastosaldoon, joko A: +4 -3 = 1 tai B: +6 -3 = +3.  
9. Tapauksessa A järjestelmä luo tulevaisuuteen aikataulutetun tilauksen aloituspäivämäärällä **Da**.  

     Tapauksessa B lisätilauspiste on saavutettu ja uusi tilaus luodaan.  

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md)   
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)

