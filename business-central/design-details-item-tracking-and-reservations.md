---
title: Rakennetiedot – Nimikkeen seuranta ja varaukset | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään nimikkeen seurannasta ja varauksista sekä niihin liittyviä käsitteitä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2883ed1176f20cca289cb68d4f3839f8099c874f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380250"
---
# <a name="design-details-item-tracking-and-reservations"></a>Rakennetiedot: nimikkeen seuranta ja varaukset

Varauksen ja tietyn nimikeseurannan samanaikainen käyttö on epänormaalia, koska ne molemmat luovat kytkennän tarjonnan ja kysynnän välille. Lukuun ottamatta tilanteita, joissa asiakas tai tuotannon suunnittelija pyytää tiettyä erää, jolloin on harvoin järkevää varata varastonimikkeitä, joilla on jo tietyn sovelluksen nimikeseurantanumerot. Vaikka tietyn nimikkeen seurannan vaativia nimikkeitä on mahdollista varata, saatavuuden ristiriitojen välttämiseksi vaaditaan erityistä toiminnallisuutta niiden tilausten käsittelijöiden välillä, jotka pyytävät samoja nimikeseurattuja nimikkeitä.  
  
Late Binding -ohjelmoinnin konsepti varmistaa, että sarja- tai eränumeron epäspesifinen varaus säilyy löyhästi kytkettynä tiliöintiin saakka. Varausjärjestelmä saattaa järjestää epätarkat varaukset kirjaamishetkellä uudelleen varmistaakseen, että kiinteä kohdistus on mahdollista todellisuudessa poimitun sarja- tai eränumeron perusteella. Tänä aikana sarja- tai eränumero asetetaan käyttöön tietylle varaukselle muissa asiakirjoissa, jotka pyytävät tätä tiettyä sarja- tai eränumeroa.  
  
Epäspesifisessä varauksessa käyttäjä ei välitä mikä tietty nimike poimitaan ja erityisessä varauksessa käyttäjä välittää.  
  
> [!NOTE]  
> Late Binding -toiminto liittyy vain nimikkeisiin, jotka on määritetty tiettyyn nimikkeenseurantaan, ja sitä voidaan käyttää vain varastoon kohdistuviin varauksiin, ei tuleviin toimitustilauksiin.  
  
Nimikeseurantanumeroiden varaus jakaantuu kahteen luokaan, kuten seuraavassa taulukossa on esitetty.  
  
|Varaus|Description|  
|-----------------|---------------------------------------|  
|Määrätty|Valitse tietyt sarja- tai eränumerot, kun varaat varastonimikkeen kysynnästä, kuten myyntitilauksesta.<br /><br /> Tämä on tavallinen varaus. Se on kiinteä linkki tarjonnan ja kysynnän välillä, joilla molemmilla on sarja- tai eränumerot. **Huomautus:** Kysyntään kohdistuu sarja eränumeroita. <br /><br /> Haluat esimerkiksi varata purkin sinistä maalia erästä A, koska asiakas pyytää sitä. Erästä A toimitetaan asiakkaalle purkki sinistä maalia.|  
|Epäspesifinen|Et voi valita tiettyä sarja- tai eränumeroa, kun varaat varastonimikkeen kysynnästä, kuten myyntitilauksesta.<br /><br /> Tämä on tila, joka saadaan varattaessa sarja- tai eränumeroita, joita ei ole erityisesti valittu. **Huomautus:** Kysyntään ei kohdistu sarjaa eränumeroita. <br /><br /> Haluat esimerkiksi varata purkin sinistä maalia mistä tahansa erästä myyntitilauksellesi. Asiakkaalle toimitetaan purkki sinistä maalia satunnaisesta sarja- tai eränumerosta.|  
  
Pääero erityisen ja yleisen varauksen välillä on määritetty sarja- ja eränumeroiden olemassaololla kysyntäpuolella, kuten seuraavasta taulukosta ilmenee.  

| Tyyppi            | Tarjonta                | Kysyntä                   |
|-----------------|-----------------------|--------------------------|
| **Määrätty**    | Sarja- tai eränumero. | Sarja- tai eränumero.    |
| **Epäspesifinen** | Sarja- tai eränumero. | Ei sarja- tai eränumeroa. |
  
Kun varastomääriä varataan lähtevästä asiakirjarivistä nimikkeelle, jolle on määritetty nimikkeen seurantanumerot ja tietyn nimikkeen seuranta, **Varaus**-sivu johtaa sinut eri työnkulkujen läpi sarja- tai eränumeroiden tarpeesta riippuen.s  
  
## <a name="specific-reservation"></a>Erityisvaraus  
Kun valitset lähtevän asiakirjarivin **Varaa**-kohdan, näyttöön tulee valintaikkuna, jossa kysytään, haluatko varata tiettyjä sarja- tai eränumeroita. Jos valitset **Kyllä**, näkyville avautuu luettelo kaikista asiakirjariville määritetyistä sarja- tai eränumeroista. **Varaus**-sivu avautuu, kun olet valinnut yhden eränumerosarjoista, ja voit sitten varata valittujen eränumerojen tai sarjanumeroiden joukosta tyypillisessä muodossa.  
  
Jos joitakin tietyn nimikkeen seurantanumeroita, joita yrität varata, pidetään määrittämättömissä varauksissa, **Varaus**-sivun alareunassa oleva viesti ilmoittaa, kuinka monia varatusta kokonaismäärästä on pidossa määrittämättömissä varauksissa ja ovatko ne vielä käytettävissä.  
  
## <a name="nonspecific-reservation"></a>Määrittämätön varaus  
Jos valitset avautuvassa valintaikkunassa **Ei**, **Varaus**-sivu avautuu ja voit varata kaikista varaston sarja- tai eränumeroista.  
  
Varausjärjestelmän rakenteen vuoksi epätarkan varauksen asettaminen nimikeseurannassa olevaan nimikkeeseen aiheuttaa sen, että järjestelmän on valittava tietyt nimiketapahtumat joita vastaan varataan. Koska nimiketapahtumissa on nimikkeen seurantanumerot, varaus varaa epäsuorasti tietyt sarja- tai eränumerot, vaikka sinulla ei ollut aikomusta. Varausjärjestelmä yrittää käsitellä tilanteen järjestämällä ei-spesifiset varaustapahtumat uudelleen ennen kirjausta.  
  
Järjestelmä varaa yhä tiettyjen tapahtumien mukaan, mutta se käyttää uudelleenjärjestelemistä aina, kun epäspesifinen varaus koskee erä- tai sarjanumeron tiettyä kysyntää. Näin voi olla, kun kirjaat kysyntätapahtuman, kuten myyntitilauksen, kulutuspäiväkirjan tai siirtotilauksen sarja- tai eränumerolle tai kun yrität varata tiettyä sarja- tai eränumeroa. Järjestelmä järjestää varaukset uudelleen, jolloin erä- ja sarjanumerot ovat kysynnän tai tietyn varauksen käytettävissä. Tällöin ei-spesifiselle varaukselle asetetaan eri erä- tai sarjanumero. Jos varastossa on riittämätön määrä, järjestelmä järjestää uudelleen niin paljon kuin mahdollista ja saat saatavuusvirheen, jos määrä on vielä riittämätön kirjaushetkellä.  
  
> [!NOTE]  
>  Epäspesifisessä varauksessa erä- tai sarjanumerokenttä on tyhjä sellaisessa varaustapahtumassa, joka osoittaa kysyntään, kuten myyntiin.  
  
## <a name="reshuffle"></a>Järjestä uudelleen  
Kun käyttäjä kirjaa lähtevän asiakirjan väärän sarja- tai eränumeron poimimisen jälkeen, muita epäspesifisiä varauksia järjestetään uudelleen vastaamaan poimittua todellista sarja- tai eränumeroa. Tämä täyttää kirjausohjelman tarpeet tarjonnan ja kysynnän välisen kiinteän kohdistuksen kanssa.  
  
Uudelleen järjestäminen on mahdollista kaikille tuetuille liiketoimintaskenaarioille vain niiden positiivisten nimiketapahtumien osalta, joilla on varaus- ja sarja- tai eränumerot, mutta joille ei ole määritetty sarja- tai eränumeroita kysynnän puolella.  
  
## <a name="supported-business-scenarios"></a>Tuetut liiketoimintaskenaariot  
Late Binding -toiminto tukee seuraavia liiketoimintaskenaarioita:  
  
* Tietyn sarja- ja eränumeron kirjoittaminen lähtevään asiakirjaan epätarkalla väärän sarja- tai eränumeron varauksella.  
* Varaa tietyn sarja- tai eränumeron.  
* Lähtevän asiakirjan kirjaaminen ei-spesifisellä sarja- tai eränumeron varauksella.  
  
### <a name="entering-serial-or-lot-numbers-on-an-outbound-document-with-wrong-nonspecific-reservation"></a>Sarja- tai eränumeroiden kirjoittaminen lähtevään asiakirjaan väärällä epätarkalla varauksella  
Tämä on yleisin kolmesta tuetusta skenaariosta. Tässä tapauksessa myöhäisen sidonnan toiminto varmistaa, että käyttäjä voi kirjoittaa sarja- tai eränumeron, joka todella poimitaan, lähtevään asiakirjaan, jolla on jo toisen sarja- tai eränumeron ei-spesifinen varaus.  
  
Tarve syntyy esimerkiksi silloin, kun tilauksen käsittelijä on ensin tehnyt minkä tahansa sarja- tai eränumeron epäspesifisen varauksen. Myöhempi kuin nimikkeen todellinen poiminta varastosta, poimitun sarja- tai eränumero on kirjoitettava tilaukseen ennen kuin se kirjataan. Yleinen varaus järjestetään uudelleen tiliöintiaikana, jotta varmistetaan, että poimitut sarja- tai eränumerot voidaan syöttää hävittämättä varausta, ja jotta varmistetaan, että poimittuja sarja- tai eränumeroita voidaan käyttää ja tiliöidä.  
  
### <a name="reserve-specific-serial-or-lot-numbers"></a>Varaa tietyt sarja- tai eränumerot  
Tässä liiketoimintaskenaariossa myöhäinen sidonta -toiminnallisuus varmistaa, että tietyn epäspesifisesti tällä hetkellä varatun sarja- tai eränumeron varausta yrittävä käyttäjä voi tehdä näin. Epäspesifinen varaus kierrätetään varaushetkellä sarja- tai eränumeron vapauttamiseksi tietylle pyynnölle.  
  
Uudelleenjärjestely tapahtuu automaattisesti, mutta upotettu apu (Help) näytetään **Varaus**-sivun alareunassa ja siinä näkyy seuraava teksti:  
  
**Varatun kokonaismäärän osuus XX on epäspesifistä. Se saattaa olla saatavilla.**  
  
Lisäksi **Määrittämätön varattu määrä** -kentässä näkyy, kuinka monta varaustapahtumaa ei ole määritetty. Oletusarvon mukaan tämä kenttä ei näy käyttäjille.  
  
### <a name="posting-an-outbound-document-with-nonspecific-reservation-of-serial-or-lot-numbers"></a>Lähtevän asiakirjan kirjaaminen ei-spesifisellä sarja- tai eränumeron varauksella  
Myöhäisen sitomisen toiminnallisuus tukee tätä liiketoimintaskenaariota. Sen avulla voidaan tehdä kiinteä kohdistus ja lähtevä kirjaus, joka poimitaan sarja- tai eränumeron toisen ei-spesifisen varauksen uudelleenjärjestelemisen avulla. Jos uudelleen järjestäminen ei ole mahdollista, seuraava vakiovirhesanoma ilmestyy näkyville, kun käyttäjä yrittää kirjata toimituksen:  
  
**Nimike XX ei ole täysin käytettävissä.**  
  
## <a name="see-also"></a>Katso myös  
[Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]