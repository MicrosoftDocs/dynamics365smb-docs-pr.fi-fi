---
title: Arvotapahtumien kirjauspäivämäärä
description: Lisätietoja siitä, miten Muuta kustannuksia - Nimiketapahtumat -eräajo tunnistaa ja määrittää niiden arvotapahtumien kirjauspäivämäärän, joita eräajo on luomassa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/19/2021
ms.author: edupont
ms.openlocfilehash: 3dcda7f44797f52e50babe4dbec90e3b2be6f19d
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440736"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Rakennetiedot: Muutoksen arvotapahtuman kirjauspäivämäärä  

Tässä artikkelissa on ohjeita [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen varaston arvostustoimintojen käyttäjille. Tässä artikkelissa on ohjeita siitä, miten **Muuta kustannuksia - Nimiketapahtumat** -eräajo tunnistaa ja määrittää niiden arvotapahtumien kirjauspäivämäärän, joita eräajo on luomassa.  

Ensin tarkistetaan prosessin käsite eli miten eräajo tunnistaa ja määrittää luotavan arvotapahtuman kirjauspäivämäärän. Tämän jälkeen jaetaan muutamia skenaarioita, joihin tukitiimit tärmäävät silloin tällöin. Lopuksi tutustutaan käsitteiden yhteenvetoon.  

## <a name="the-concept"></a>Käsite  

**Muuta kustannuksia - Nimiketapahtumat** -eräajo määrittää kirjauspäivämäärän arvotapahtumalle, jonka se luo seuraavien vaiheiden avulla:  

1.  Alussa luotavan tapahtuman kirjauspäivämäärä on sama kuin päivämäärän, jota se muuttaa.  

2.  Kirjauspäivämäärä vahvistetaan varastokausien ja/tai pääkirjanpidon asetusten avulla.  

3.  Kirjauspäivämäärän määritys: jos alkuperäinen kirjauspäivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen, eräajo määrittää sallitu kirjauspäivämäärän pääkirjanpidon asetuksista tai varastokausista. Jos pääkirjanpidon asetuksissa on määritetty sekä varastokaudet että sallitut kirjauspäivämäärät, muutoksen arvotapahtumalle määritetään myöhempi näistä kahdesta päivämäärästä.  

 Tarkastellaan tätä prosessia lähemmin. Oletetaan, että käsittelyssä on myynnin nimiketapahtuma. Nimike on toimitettu 5.9.2020 ja laskutettu päivää myöhemmin.  


**Nimiketapahtuma**  
Päivämäärän muoto YYYY-MM-DD

|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  | Asiakirjanumero |Sijaintikoodi   |määrä  |Kustannussumma (Tod.)  |Laskutettu määrä  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Myynti       |102033     |  Sininen       | -1    |    -11     |-1     |    0     |

Alla oleva ensimmäinen arvotapahtuma (379) edustaa toimitusta. Sen kirjauspäivämäärä on sama kuin päänimiketapahtuman päivämäärä.  
  
Toinen arvotapahtuma (381) edustaa laskua.  

Kolmas arvotapahtuma (391) on laskutuksen arvotapahtuman (381) muutos.  
  

|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  |Nimiketapahtuman nro  |Sijaintikoodi   |Nimiketapahtumien määrä  |Laskutettu määrä  |Kustannussumma (Tod.)  |Kustannussumma (oletettu)  |Muutos  |Kohdistetaan tapahtumaan  |Lähdekoodi  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Myynti     | Välitön kustannus   | 102033        |319     | Sininen        | -1       |0         |  0       |     -10   |Ei   |0    |Myynti          |
|381     |  A       |    2020-09-06     |    Myynti     | Välitön kustannus   | 103022        |319     | Sininen        |  0       |-1        |-10       |    10     | Ei  |0      |       Myynti   |
|391     |  A       |    2020-09-10     |    Myynti     | Välitön kustannus   | 103022        |319     | Sininen        |  0       |0         |-1        |    0     |Kyllä   |    181   | VARMUUTOS   |

Muutostapahtuman kirjauspäivämäärä on alun perin sama kuin muutettavan tapahtuman kirjauspäivämäärä.

 Vaihe 1: Luotava muutoksen arvotapahtuma on määritetty samaan kirjauspäivämäärään kuin tapahtuma, jota se muuttaa, kuten yläpuolella oleva arvotapahtuma 391 osoittaa.  
  
 Vaihe 2: Alussa määritetyn kirjauspäivämäärän tarkistus.  

**Muuta kustannuksia - Nimiketapahtumat** -eräajo määrittää, kuuluuko muutoksen arvotapahtuman alkuperäinen kirjauspäivämäärä sallittuun kirjauspäivämääräalueeseen varastokausien ja/tai pääkirjanpidon asetusten perusteella.  

Tarkistetaan yllämainittu myynti lisäämällä sallittujen kirjauspäivämääräalueiden asetukset.  
  
**Varastokaudet**

|Lopetuspvm  |Name  |Suljettu  |
|---------|---------|---------|
|2020-01-31     |Tammikuu 2020      |  Kyllä    |
|2020-02-28     |Helmikuu 2020     |  Kyllä    |
|2020-03-31     |Maaliskuu 2020        |  Kyllä    |
|2020-04-30     |Huhtikuu 2020        |  Kyllä    |
|2020-05-31     |Toukokuu 2020        |  Kyllä    |
|2020-06-30     |Heinäkuu 2020       |  Kyllä    |
|2020-07-31     |Heinäkuu 2020        |   Kyllä   |
|2020-08-31     |Elokuu 2020     |   Kyllä   |
|2020-09-30     |Syyskuu 2020  |         |
|2020-10-31     |Lokakuu 2020    |         |
|2020-11-30     |Marraskuu 2020   |         |
|2020-12-31     |Joulukuu 2020   |         |

Ensimmäinen sallittu kirjauspäivämäärä on ensimmäisen avoimen kauden ensimmäinen päivä. 1. syyskuuta 2020.  

**Pääkirjanpidon asetukset**

|Kenttä|Arvo  |
|---------|---------|
|Ensimm. sallittu kirjauspvm:  |  2020-09-10      |
|Viimeinen sallittu kirjauspvm:    |  2020-09-30      |
|Rekisteröi aika:       |         |
|Paikallinen osoitemuoto:|   Postinro      |  

 Ensimmäinen sallittu kirjauspäivämäärä on Ensimm. sallittu kirjauspvm -kentässä mainittu päivämäärä: 10.9.2020.  
 Jos pääkirjanpidon asetuksissa on määritetty sekä varastokaudet että sallitut kirjauspäivämäärät, jälkimmäinen päivämäärä määrittää sallitun kirjauspäivämäärän.  

 Vaihe 3: Sallitun kirjauspäivämäärän määrittäminen  

 Alkuperäinen määritetty kirjauspäivämäärä oli 6.9., kuten vaiheessa 1 kerrottiin. Toisessa vaiheessa kuitenkin Muuta kustannuksia - Nimiketapahtumat -eräajo määrittää, että aikaisin sallittu kirjauspäivämäärä on 10.9. ja tämän vuoksi määrittää alla muutoksen arvotapahtumalle päivämäärän 10.9.  

   
|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  |Nimiketapahtuman nro  |Sijaintikoodi   |Nimiketapahtumien määrä  |Laskutettu määrä  |Kustannussumma (Tod.)  |Kustannussumma (oletettu)  |Muutos  |Kohdistetaan tapahtumaan  |Lähdekoodi  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Myynti     | Välitön kustannus   | 102033        |319     | Sininen        | -1       |0         |  0       |     -10   |Ei   |0    |Myynti          |
|381     |  A       |    2020-09-06     |    Myynti     | Välitön kustannus   | 103022        |319     | Sininen        |  0       |-1        |-10       |    10     | Ei  |0      |       Myynti   |
|391     |  A       |    **2020-09-10**     |    Myynti     | Välitön kustannus   | 103022        |319     | Sininen        |  0       |0         |-1        |    0     |Kyllä   |    181   | VARMUUTOS   |

 Olemme nyt käyneet läpi kirjauspäivämäärien määrittämisen arvotapahtumille, jotka Muuta kustannuksia - Nimiketapahtumat -eräajo on luonut.  

 Jatketaan tutkimalla skenaarioita, joita tukitiimi tapaa ajoittain, kun Muuta kustannuksia - Nimiketapahtumat -eräajon ja liittyvien asetusten määritettyjen kirjauspäivämäärien kohdalla.  

## <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Skenaario I: Kirjauspäivämäärä ei kuulu sallittujen kirjauspäivämäärien alueeseen...  

 Tässä skenaariossa käyttäjä näkee mainitun virhesanoman, kun Muuta kustannuksia - Nimiketapahtumat -eräajo suoritetaan.  

 Edellisessä kirjauspäivämäärien määrittämistä koskevassa osassa Muuta kustannuksia - Nimiketapahtumat -eräajon tarkoitus on luoda arvotapahtuma, jonka kirjauspäivämäärä on 10.9.  

![Kirjauspäivämäärää koskeva virhesanoma.](media/helene/TechArticleAdjustcost6.png "Kirjauspäivämäärää koskeva virhesanoma")

 Seurataan käyttäjäasetuksia;  

**Käyttäjäasetukset**  

Lajittelu: Käyttäjätunnus  

|Käyttäjätunnus  |Ensimm. sallittu kirjauspvm  | Viimeinen sallittu kirjauspvm  |
|---------|---------|--------|
|EUROOPPA  |  2020-09-11      |2020-09-30      |

 Tässä tapauksessa käyttäjälle määritetty sallittu kirjauspäivämääräalue on 11.9.–30.9. Muutoksen arvotapahtuman kirjauspäivämäärä ei siis voi olla 10.9.  

### <a name="overview-of-involved-posting-date-setup"></a>Asiaankuuluvan kirjauspäivämäärän asetuksen yleiskuvaus:

**Varastokaudet**  

|Lopetuspvm  |Name  |Suljettu  |
|---------|---------|---------|
|2020-01-31     |Tammikuu 2020      |  Kyllä    |
|2020-02-28     |Helmikuu 2020     |  Kyllä    |
|2020-03-31     |Maaliskuu 2020        |  Kyllä    |
|2020-04-30     |Huhtikuu 2020        |  Kyllä    |
|2020-05-31     |Toukokuu 2020        |  Kyllä    |
|2020-06-30     |Heinäkuu 2020       |  Kyllä    |
|2020-07-31     |Heinäkuu 2020        |   Kyllä   |
|2020-08-31     |Elokuu 2020     |   Kyllä   |
|2020-09-30     |Syyskuu 2020  |         |
|2020-10-31     |Lokakuu 2020    |         |
|2020-11-30     |Marraskuu 2020   |         |
|2020-12-31     |Joulukuu 2020   |         |  

**Pääkirjanpidon asetukset**  

|Kenttä|Arvo|
|---------|---------|
|Ensimm. sallittu kirjauspvm:  |  2020-09-10      |
|Viimeinen sallittu kirjauspvm:    |  2020-09-30      |
|Rekisteröi aika:       |         |
|Paikallinen osoitemuoto:|   Postinro      |  

**Käyttäjäasetukset**    

|Käyttäjätunnus  |Ensimm. sallittu kirjauspvm  | Viimeinen sallittu kirjauspvm  |
|---------|---------|--------|
|KÄYTTÄJÄTUNNUS |  2020-09-10      |2020-09-30      |

 Jos käyttäjälle määritetään laajempi (tai sama) sallittu kirjauspäivämääräalue kuin varastokaudella tai kirjanpidon asetuksissa, mainittu ristiriita vältetään. Oikaisun arvotapahtuma, jonka kirjauspvm on 10. syyskuuta, kirjataan onnistuneesti näillä asetuksilla.

Vanhempi Knowledge Base -artikkeli [952996](https://support.microsoft.com/topic/information-about-inventory-adjustment-posting-dates-in-microsoft-dynamics-nav-99e22b2b-5b79-a9b2-3b43-7f3484fa31d9) sisältää lisää mainittuun virhesanomaan liittyviä skenaarioita.  

## <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Skenaario II: Kirjauspäivämäärään verratun muutoksen arvotapahtuman kirjauspäivämäärän vuoksi muutos voi olla uudelleenarvostus tai nimikekulu.  

### <a name="revaluation-scenario"></a>Uudelleenarvostusskenaario:  

 Vaatimukset:  

 Varastonhallinnan asetukset:  
omat
-   Automaattinen kustannusten kirjaus = Kyllä  

-   Automaattinen kustannusten muuttaminen = Aina  

-   Keskim. kust. laskentatyyppi = Nimike  

-   Keskimääräisen kustannuksen jakso = Päivä  

 Pääkirjanpidon asetukset:  

-   Ensimm. sallittu kirjauspvm = 1.1.2021  

-   Viimeinen sallittu kirjauspvm = tyhjä  

 Käyttäjäasetukset:  

-   Ensimm. sallittu kirjauspvm = 1.12.2020  

-   Viimeinen sallittu kirjauspvm = tyhjä  

### <a name="to-test-the-scenario"></a>Skenaarion testaaminen  

1.  Luo TESTI-nimike:  

     Perusmittayksikkö = Kpl  

     Arvostusmenetelmä = Keskiarvo  

     Valitse vaihtoehtoiset kirjausryhmät.  

2.  Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:  

     Kirjauspäivämäärä = 15.12.2020  

     Nimike = TESTI  

     Tapahtuman tyyppi = Osto  

     Määrä = 100  

     Yksikkösumma = 10  

3.  Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:  

     Päivämäärä = 20.12.2020  

     Nimike = TESTI  

     Tapahtuman tyyppi = Negatiivinen muutos  

     Määrä = 2  

4.  Avaa nimikepäiväkirja ja luo ja kirjaa rivit seuraavasti:  

     Päivämäärä = 15.1.2021  

     Nimike = TESTI  

     Tapahtuman tyyppi = Negatiivinen muutos  

     Määrä = 3  

5.  Avaa uudelleenarvostuspäiväkirja ja luo ja kirjaa rivit seuraavasti:  

     Nimike = TESTI  

     Kohdistetaan tapahtumaan = valitse vaiheessa 2 kirjattu ostotapahtuma. Uudelleenarvostuksen kirjauspäivämäärä on sama kuin tapahtuman, jota se muuttaa.  

     Uudelleenarvostettu yksikkökustannus = 40  

Seuraavat **nimikekirjaukset** ja **arvotapahtumat** on kirjattu:  

**Nimiketapahtuma – osto**:  
Päivämäärän muoto YYYY-MM-DD  

|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TESTI         |2020-12-15         |Osto         |T00001         |100         |4000         |95        |

**Arvotapahtumat**  

|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  |Nimikenumerotapahtumien määrä  |Kustannussumma (Tod.)  |KP:oon kirjattu kustannus  |Muutos  |Kohdistetaan tapahtumaan  |Lähdekoodi  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TESTI|   2020-12-15    |317         |Osto         |Välitön kustannus         |T00001         |100         |1 000,00          |1 000,00    |Ei         |0         |NIMIKENL         |
|379     |TESTI   |**2020-12-15**    |317         |Osto         |Uudelleenarvostus         |T04002         |0         |3 000,00         |3 000,00         |Ei         |0         |UUDARVINL         |

**Nimiketapahtuma - negatiivinen oikaisu, vaihe 3**  

|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TESTI      |2020-12-20   |Negatiivinen muutos  |T00002         |-2         |-80         | 0        |

**Arvotapahtumat**  

|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  |Nimikenumerotapahtumien määrä  |Kustannussumma (Tod.)  |KP:oon kirjattu kustannus  |Muutos  |Kohdistetaan tapahtumaan  |Lähdekoodi  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TESTI|   2020-12-20    |318         |Negatiivinen muutos         |Välitön kustannus         |T00002         |-2         |-20          |-20    |Ei         |0         |NIMIKENL         |
|380     |TESTI   |**2021-01-01**    |318         |Negatiivinen muutos         |Välitön kustannus         |T04002         |0         |-60         |-60         |Kyllä         |377         |VAROIK         |

**Nimiketapahtuma - negatiivinen oikaisu, vaihe 4**  

|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TESTI      |2021-01-15   |Negatiivinen muutos  |T00003         |-3         |-120         | 0        |

**Arvotapahtumat**  

|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  |Nimikenumerotapahtumien määrä  |Kustannussumma (Tod.)  |KP:oon kirjattu kustannus  |Muutos  |Kohdistetaan tapahtumaan  |Lähdekoodi  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TESTI|   2021-01-15    |319         |Negatiivinen muutos         |Välitön kustannus         |T00003         |-3         |-30          |-30    |Ei         |0         |NIMIKENL         |
|381     |TESTI   |**2021-01-15**    |319         |Negatiivinen muutos         |Välitön kustannus         |T04003         |0         |-90         |-90         |Kyllä         |378         |VAROIK         |

Muuta kustannuksia - Nimiketapahtumat -eräajo on tunnistavut muutokset kustannuksissa ja muuttanut negatiivisia muutoksia.  

**Luotujen muutoksen arvotapahtumien kirjauspäivämäärien tarkistaminen:** Muuta kustannuksia - Nimiketapahtumat -eräajon aikaisin sallittu kirjauspäivämäärä on 1.1.2021 pääkirjanpidon asetusten mukaan.  

**Negatiivinen muutos vaiheessa 3:** määritetty kirjauspäivämäärä on 1.1. pääkirjanpidon asetusten mukaan. Muutoksen arvotapahtuman kirjauspäivämäärä on 20.12.2020. Pääkirjanpidon asetusten mukaan päivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen. Tämän vuoksi muutoksen arvotapahtumalle on määritetty pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän kirjauspäivämäärä.  

**Negatiivinen muutos vaiheessa 4:** määritetty kirjauspäivämäärä on 15.1. Muutoksen arvotapahtuman kirjauspäivämäärä on 15.1., joka kuuluu sallittuun kirjauspäivämääräalueeseen pääkirjanpidon asetusten mukaan.  

Negatiiviseen muutokseen vaiheessa 3 tehty muutos aiheuttaa keskustelua. Muutoksen arvotapahtuman suositeltu kirjauspäivämäärä olisi ollut 20.12. tai jokin muu joulukuun päivämäärä, koska myytyjen tuotteiden kustannusten muutoksen aiheuttanut uudelleenarvostus kirjattiin joulukuussa.  

Jotta negatiiviseen muutokseen voidaan tehdä muutos joulukuussa vaiheessa 3, pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän päivämäärän on oltava joulukuussa.  

**Yhteenveto.**  

Tämän skenaarion kokemusten perusteella yritykselle parhaiten sopivin sallitun kirjauspäivämääräalueen asetus voisi olla noudattaa seuraavia periaatteita: niin kauan kuin varastoarvon muutokset voidaan kirjata kauden aikana, tässä tapauksessa joulukuussa, yrityksen sallitun kirjauspäivämääräalueen asetus tulee määrittää tämän mukaan. Pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kenttä, johon on määritetty 1.12., sallii joulukuussa tehdyn uudelleenarvostuksen ohjauksen edelleen saman kauden muuttuneisiin lähteviin tapahtumiin.  

Tässä skenaariossa ollut asetus, jonka mukaan käyttäjäryhmät, jotka eivät voi tehdä kirjauksia joulukuussa, voivat tehdä niitä tammikuussa, kannattaa määrittää käyttäjäasetuksissa pääkirjanpidon asetusten sijaan.  

### <a name="item-charge-scenario"></a>Nimikekulujen skenaario:  

 Vaatimukset:  

 Varastonhallinnan asetukset:  

-   Automaattinen kustannusten kirjaus = Kyllä  

-   Automaattinen kustannusten muuttaminen = Aina  

-   Keskim. kust. laskentatyyppi = Nimike  

-   Keskimääräisen kustannuksen jakso = Päivä  

 Pääkirjanpidon asetukset:  

-   Ensimm. sallittu kirjauspvm = 1.12.2020.  

-   Viimeinen sallittu kirjauspvm = tyhjä  

 Käyttäjäasetukset:  

-   Ensimm. sallittu kirjauspvm = 1.12.2020.  

-   Viimeinen sallittu kirjauspvm = tyhjä  


### <a name="to-test-the-scenario"></a>Skenaarion testaaminen  

1.  Luo nimikekulu:  

     Perusmittayksikkö = Kpl  

     Arvostusmenetelmä = Keskiarvo  

     Valitse vaihtoehtoiset kirjausryhmät.  

2.  Luo uusi ostotilaus  

     Tavarantoimittajan nro: 10 000  

     Kirjauspäivämäärä = 15.12.2020

     Toimittajan laskunro: 1 234  

     Ostotilausrivillä:  

     Nimike = KULU  

     Määrä = 1  

     Välitön yksikkökustannus = 100  

     Kirjaa vastaanottaminen ja lasku.  

3.  Luo uusi myyntitilaus:  

     Tilausasiakkaan nro: 10000  

     Kirjauspäivämäärä = 16.12.2020  

     Myytitilausrivillä:  

     Nimike = KULU  

     Määrä = 1  

     Yksikköhinta = 135  

     Kirjaa toimitus ja lasku.  

4.  Pääkirjanpidon asetukset:  

     Ensimm. sallittu kirjauspvm = 1.1.2021  

     Viimeinen sallittu kirjauspvm = tyhjä  

5.  Luo uusi ostotilaus:  

     Tavarantoimittajan nro: 10000  

     Kirjauspäivämäärä = 2.1.2021  

     Toimittajan laskunro: 2 345  

     Ostotilausrivillä:  

     Nimikekulu = JB-RAHTI  

     Määrä = 1  

     Välitön yksikkökustannus = 3  

     Määritä nimikekuluksi ostovastaanotto vaiheesta 2.  

     Kirjaa vastaanotto ja lasku.  


**Ostovaiheen 2 tilanimiketapahtuma**:  
  
|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |VELOITUS         |2020-12-15         |Osto         |107030         |1         |105         |0        |

**Arvotapahtumat**  

|Tapahtumanumero |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  | Nimikekulunro    |  Nimiketapahtumien määrä   |Kustannussumma (Tod.)     |KP:oon kirjattu kustannus |Muutos |Kohdistetaan tapahtumaan |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |VELOITUS|   2020-12-15    |324         |Osto         |Välitön kustannus         |108029         |         |1          |100    |100         |NRO         |0         |
|399      |VELOITUS   |2021-01-02    |324         |Osto         |Välitön kustannus         |108009         |JB-RAHTI         |0         |3         |3         |NRO         |0         |


**Tilanimiketapahtuma – myynti**:  
  
|Tapahtumanro  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |VELOITUS         |2020-12-16         |Myynti         |102035         |-1         |-105         |0        |

**Arvotapahtumat**  

|Tapahtumanumero |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  | Nimikekulunro    |  Nimiketapahtumien määrä   |Kustannussumma (Tod.)     |KP:oon kirjattu kustannus |Muutos |Kohdistetaan tapahtumaan |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |VELOITUS|   2020-12-16    |325         |Myynti         |Välitön kustannus         |109024         |         |-1          |-100    |-100         |NRO         |0         |
|400      |VELOITUS   |2021-01-01    |325         |Myynti         |Välitön kustannus         |109024         |         |0         |-3         |-3         |Kyllä         |398         |


6.  Ostolasku saapuu käsittelypäivänä 3.1. Ostolasku sisältää vaiheessa 2 ostoon tehdyn lisäkulun. Tämän laskun asiakirjan päivämäärä on 30.12. Tämän vuoksi sen kirjauspäivämääräksi tulee 30.12.2020.  

     Luo uusi ostotilaus:  

     Tavarantoimittajan nro: 10000  

     Kirjauspäivämäärä = 30.12.2020  

     Toimittajan laskunro: 3 456  

     Ostotilausrivillä:  

     Nimikekulu = JB-RAHTI  

     Määrä = 1  

     Välitön yksikkökustannus = 2  

     Määritä nimikekuluksi ostovastaanotto vaiheesta 2  

     Kirjaa vastaanotto ja lasku.  


**Oston tilanimiketapahtuma**:  

|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |VELOITUS         |2020-12-15         |Osto         |107030         |1         |105         |0        |

**Arvotapahtumat**  

|Tapahtumanro |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  | Nimikekulunro    |  Nimiketapahtumien määrä   |Kustannussumma (Tod.)     |KP:oon kirjattu kustannus |Muutos |Kohdistetaan tapahtumaan |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |VELOITUS   |2020-12-15    |324         |Osto         |Välitön kustannus         |108029         |            |1         |100    |100         |Ei         |0         |
|399      |VELOITUS   |2021-01-02    |324         |Osto         |Välitön kustannus         |108030         |JB-RAHTI   |0         |3         |3         |Ei         |0         |
|401      |VELOITUS   |**2020-12-30**    |324         |Osto         |Välitön kustannus         |108031         |JB-RAHTI   |0         |2         |2         |Ei         |0         |

**Tilanimiketapahtuma – myynti**:  
  
|Tapahtumanumero  |Nimikkeen nro  |Kirjauspäivämäärä  |Tapahtuman tyyppi  |Asiakirjanumero  |määrä  |Kustannussumma (Tod.)  |Jäljellä oleva määrä  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |VELOITUS         |2020-12-16         |Myynti         |102035         |-1         |-105         |0        |

**Arvotapahtumat**  

|Tapahtumanro |Nimikkeen nro  |Kirjauspäivämäärä  |Nimiketapahtuman nro  |Nimiketapahtuman tyyppi  |Tapahtuman tyyppi  |Asiakirjanumero  | Nimikekulunro    |  Nimiketapahtumien määrä   |Kustannussumma (Tod.)     |KP:oon kirjattu kustannus |Muutos |Kohdistetaan tapahtumaan |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |VELOITUS   |2020-12-16        |325         |Myynti         |Välitön kustannus         |103024         |            |-1         |-100       |-100         |Ei         |0         |
|400      |VELOITUS   |2021-01-01        |325         |Myynti         |Välitön kustannus         |103024         |            |0          |-3         |-3         |Kyllä         |398         |
|402      |VELOITUS   |**2021-01-01**    |325         |Myynti         |Välitön kustannus         |103024         |            |0          |-2         |-2         |Kyllä         |398         |

Varaston arvostus -raportti tulostetaan 31.12.2020

![Varaston arvostusraportin sisältö.](media/helene/TechArticleAdjustcost13.png "Varaston arvostusraportin sisältö")

 **Skenaarion yhteenveto:**  

 Kuvattu skenaario loppuu Varaston arvostus -raporttiin, jossa määrä = 0 ja arvo = 2. Vaiheessa 11 kirjattu nimikekulu on osa varaston arvon nousua joulukuussa. Saman kauden varaston arvon lasku ei ole muuttunut.  

 Pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän arvo 1.1. on sopiva ensimmäiselle nimikekululle. Varaston arvon nousun ja laskun kustannukset tallennettiin samaan kauteen. Pääkirjanpidon asetusten vuoksi toinen nimikekulu aiheuttaa kuitenkin muutoksen myytyjen tuotteiden kustannuksessa. Muutos otetaan huomioon seuraavan kauden aikana.  

 **Yhteenveto.**  

 On haastavaa, kun Varaston arvostus -raportissa määritetään, että määrä = 0 samalla, kun arvo <> 0. Tässä tapauksessa on vaikeaa kertoa optimaaliset asetukset, koska ostolaskut saapuvat samana päivänä mutta ne koskevat eri kausia tai jopa eri tilivuosia. Uuteen tilivuoteen siirtäminen vaatii yleensä suunnittelua. Muuta kustannuksia - Nimiketapahtumat -prosessin on myös otettava huomioon myytyjen tuotteiden kustannukset.  

 Tässä skenaariossa eräs vaihtoehto olisi ollut määrittää pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän arvoksi muutamaa päivää aikaisempi joulukuun päivämäärä ja kirjata ensimmäinen nimikekulu viiveellä, jolloin edellisen kauden/tilivuoden kaikki kustannukset tuloutettaisiin kaudelle, jolle ne alussa kuuluivat. Tämän jälkeen suoritettaisiin Muuta kustannuksia - Nimiketapahtumat -eräajo ja siirrettäisiin sallittu kirjauspäivämäärä seuraavaan kauteen\/tilivuoteen. Kirjatuksi olisi tullut ensimmäinen nimikekulu, jonka kirjauspäivämäärä on 2.1.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Muuta kustannuksia - Nimiketapahtumat -eräajon historia  

 Alla on Muuta kustannuksia - Nimiketapahtumat -eräajon muutoksen arvotapahtumien kirjauspäivämäärien määrittämisen yhteenveto.  

### <a name="about-the-request-form-posting-date"></a>Tietoja pyyntölomakkeen kirjauspäivämäärästä:  

 Muuta kustannuksia - Nimiketapahtumat -eräajon pyyntölomakkeessa ei ole enää ilmoitettavaa kirjauspäivämäärää. Eräajo käy läpi kaikki pakolliset muutokset ja luo arvotapahtumat, joilla on sen arvotapahtuman kirjauspäivämäärä, jonka eräajo muuttaa. Jos kirjauspäivämäärä ei kuulu sallittuun kirjauspäivämääräalueeseen, käytetään pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm -kentän kirjauspäivämäärä tai mahdollisesti käytössä olevien varastokausien kirjauspäivämäärää sen mukaan, kumpi on myöhempi. Katso edellä kuvattua käsitettä.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Kirjaa varaston kustannukset kirjanpitoon -eräajon historia  

 Kirjaa varaston kustannukset kirjanpitoon -eräajo liittyy läheisesti Muuta kustannuksia - Nimiketapahtumat -eräajoon. Tämän vuoksi kyseisen eräajon historiasta tehdään yhteenveto, joka jaetaan myös täällä.  
 
![Todelliset kustannukset vs. oletetut kustannukset.](media/helene/TechArticleAdjustcost14.png "Todelliset kustannukset vs. oletetut kustannukset")

### <a name="about-the-posting-date"></a>Tietoja kirjauspäivämäärästä  

 Kirjaa varaston kustannukset kirjanpitoon -eräajon pyyntölomakkeessa ei ole enää ilmoitettavaa kirjauspäivämäärää. Luodaan KP-tapahtuma, jolla on sama kirjauspäivämäärä kuin liittyvällä arvotapahtumalla. Jotta eräajo voidaan suorittaa, sallitun kirjauspäivämääräalueen on sallittava luodun KP-tapahtuman kirjauspäivämäärä. Muussa tapauksessa sallittu kirjauspäivämääräalue on avattava uudelleen tilapäisesti joko muuttamalla päivämääriä tai poistamalla niitä pääkirjanpidon asetusten Ensimm. sallittu kirjauspvm- ja Viimeinen sallittu kirjauspvm -kentissä. Vältät täsmäytysongelmat, kun KP-tapahtuman kirjauspäivämäärä vastaa arvotapahtuman kirjauspäivämäärää.  

 Kirjaa arvotapahtuma kirjanpitoon -eräajo skannaa taulukon 5811 ja tunnistaa alueeseen kuuluvat arvotapahtumat pääkirjanpitoon kirjaamista varten. Kun eräajo on suoritettu, taulukko tyhjennetään.

## <a name="see-also"></a>Katso myös  

[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  
[Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
