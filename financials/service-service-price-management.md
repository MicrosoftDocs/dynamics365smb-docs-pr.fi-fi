---
title: Huoltohinnan hallinta | Microsoft Docs
description: "Tässä ohjeaiheessa käsitellään parhaiden hintojen käyttämistä huoltotilauksissa, yksilöllisten huoltohintasopimusten määrittämistä asiakkaille, huoltohenkilöstön toiminnan tehostamista ja laskutusprosessin nopeuttamista."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/28/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b2607dce0b62a3a1433362491692687d4c868d06
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="service-price-management"></a>huoltohallinnan asetukset
Huoltohinnan hallinnan toimintojen avulla voidaan soveltaa oikeita hintoja huoltotilauksiin, määrittää asiakkaille yksilöllisiä huoltohintasopimuksia, parantaa huoltohenkilöstön tehokkuutta ja nopeuttaa laskutusprosessia.  
  
Huoltohinnan hallinnassa voidaan määrittää erilaisia huoltohintaryhmiä sen mukaan, mistä huoltonimikkeestä (tai huoltonimikeryhmästä) ja minkä tyyppisestä viasta huoltotehtävässä on kyse. Huoltohintaryhmä voidaan määrittää rajalliseksi ajaksi ja/tai tietylle asiakkaalle tai valuutalle. Kun huoltotehtävälle määritetään hintaa, voidaan näitä hinnoittelurakenteita käyttää mallina.  
  
Käyttäjä voi esimerkiksi määrittää huoltohintaan kuuluvat nimikkeet sekä hintaan sisältyvän työn tyypin. Samoin voidaan määrittää eri huoltohintaryhmiä eri arvonlisäverokannoille ja alennussummille. Oikeiden hintojen varmistamiseksi voidaan asettaa kiinteä, pienin tai suurin hinta sen mukaan, millainen sopimus asiakkaan kanssa on tehty.  
  
Ennen kuin huoltonimikkeen hintaa muutetaan huoltotilauksessa, ohjelma näyttää, millaisen lopputuloksen hinnanmuutos tuottaa. Tämä voidaan joko hyväksyä tai, jos halutaan erilainen lopputulos, voidaan tuloksia vielä muokata. Koko muutos tehdään rivi kerrallaan eli ylimääräisiä rivejä ei luoda.  
  
Huoltohintaryhmien tilastoiden ja vakioraporttien avulla voidaan seurata myös eri huoltohintaryhmien kannattavuutta.  
  
## <a name="service-price-adjustment-groups"></a>Huoltohintamuutoksen ryhmät  
Huoltohinnan muutosryhmiä voidaan käyttää erityyppisten hinnanmuutosten määrittämiseen. On mahdollista esimerkiksi määrittää yksi huoltohinnan muutosryhmä, joka muuttaa varaosien hintoja, toinen, joka muuttaa työn hintoja, kolmas, joka muuttaa kulujen hintoja, ja niin edelleen. Lisäksi voidaan määrittää, sovelletaanko huoltohinnanmuutosta vain yhteen tiettyyn nimikkeeseen tai resurssiin vai kaikkiin nimikkeisiin ja resursseihin.  
  
Kussakin huoltohinnan muutosryhmässä on tiedot muutoksista, jotka halutaan tehdä huoltoriveillä.  
  
Huoltohintojen muutostoimintoa ei voida käyttää huoltosopimuksiin kuuluviin huoltonimikkeisiin. Voit muuttaa vain huoltotilauksen nimikkeiden huoltohintoja. Et voi muuttaa huoltonimikkeen hintaa, jos nimikkeellä on takuu. Et voi muuttaa huoltotilauksen huoltonimikkeen hintaa, jos siihen liitetyt huoltorivit on kirjattu laskuna (kokonaan tai osittain).  
  
Kun huoltohintojen muutostoiminto käynnistetään, kaikki tilauksen sisältämät alennukset korvataan huoltohinnanmuutoksen arvoilla.  
  
## <a name="service-price-groups"></a>Huoltohintaryhmät  
Huoltohintaryhmiä määrittämällä voidaan luoda huoltonimikkeiden ryhmiä, joita koskee sama erikoishinnoittelu. Kun huoltohintaryhmät on määritetty, voidaan niitä liittää huoltonimikerivin huoltonimikkeisiin. Huoltohintaryhmiä voidaan liittää myös huoltonimikeryhmiin.  
  
Ennen kuin huoltohintaryhmä liitetään huoltonimikkeeseen, on päätettävä, mitä vian aluetta, valuuttaa ja huoltohinnan muutosryhmää huoltohintaryhmä koskee. On myös päätettävä, miksi summaksi huoltohinta muutetaan sekä sisältyykö tähän summaan ALV ja alennukset. Samoin on päätettävä, koskeeko muutos kiinteää summaa ja onko muutoksen soveltamiselle ehtoja.  
  
Kun huoltohintaryhmä liitetään huoltonimikkeeseen, kaikki ryhmälle määritetyt erikoishinnoittelut tulevat voimaan kyseiselle huoltonimikkeelle.  
  
## <a name="service-pricing"></a>Huoltohinnoittelu  
Todelliset huoltohinnoittelun tyypit (hinnanmuutoksen tyyppi ja hinta) määritetään huoltohintaryhmien ja asiakashintaryhmien yhdistelmälle. Kullekin huoltohinnoittelun tyypille valitaan huoltohinnan muutosryhmä. Lisäksi määritetään huoltohinnan muutoksen tyyppi (kiinteä, maksimi tai minimi) ja todellinen hinta.  
  
Huoltohinnoittelun tyyppejä voi määrittää esimerkiksi radioiden huoltohintaryhmälle. Asiakkaille, joilla ei ole hintaryhmää, voidaan määritellä huoltohinnoittelu, jossa työllä on enimmäishinta (työn hinnanmuutosryhmä). Asiakkaille, joilla on tietty hintaryhmä, voidaan määritellä huoltohinnoittelu, jossa työllä on kiinteä hinta (sama työn hinnanmuutosryhmä).  
  
## <a name="service-price-adjustment"></a>huoltohintojen oikaisu  
Huoltohinnan muutoksella voidaan muuttaa nimikkeen, resurssin, KP-tilin tai kulun hintaa huoltotilauksessa.  
  
Kun huoltonimikeriveille on annettu nimike, annetaan kaikki tämän nimekkeen kustannustiedot huoltoriveille. Kun suoritat Muokkaa huoltohinta -toimintoa, voit esikatsella hintojen muutoksia. Tietoja voidaan tarvittaessa muokata. Kun muokatut tiedot hyväksytään, ohjelma laskee muutokset ja siirtää tiedot huoltoriveille. Tämän jälkeen huoltotilaus kirjataan.  
  
Ohjelma laskee muutosten kokonaissumman huoltohintamuutoksen tyypin mukaan seuraavasti:  
  
Asetukset kuvaillaan seuraavassa taulukossa.  
  
|Asetus | Description |  
|----------------------------------|---------------------------------------|  
|**Kiinteä hinta:**|Tämä tarkoittaa, että huoltonimikkeestä, resurssista, KP-tilistä tai kulusta laskutetaan kiinteä hinta todellisista kuluista tai vakioveloituksista välittämättä. Kun valitaan tämä vaihtoehto, huoltohinnan muutos tuottaa tarkalleen huoltohintaryhmässä määritetyn summan.|  
|**Suurin**|Tämä tarkoittaa, että asiakkaalta veloitettavalle summalle asetetaan yläraja todellisista kustannuksista tai vakioveloituksista välittämättä. Kun valitaan tämä vaihtoehto, huoltohinnan muutos tehdään vain, jos yhteishinta ylittää huoltohintaryhmälle määritetyn summan.|  
|**Pienin**|Tämä tarkoittaa, että asiakkaalta veloitettavalle summalle asetetaan alaraja todellisista kustannuksista tai vakioveloituksista välittämättä. Kun valitaan tämä vaihtoehto, huoltohinnan muutos tehdään vain, jos yhteishinta alittaa huoltohintaryhmälle määritetyn summan.|  
  
## <a name="see-also"></a>Katso myös  
[Huollon hintojen ja lisäkustannusten määrittäminen](service-how-setup-service-costs-pricing.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  

