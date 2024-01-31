---
title: Käyttöomaisuuden poistomenetelmät
description: Lisätietoja eri sisäänrakennetuista tavoista käyttöomaisuuden poistojen tai arvonalennusten toteuttamiseen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'write down, depreciate, depreciation'
ms.search.form: '5629, 5633'
ms.date: 09/22/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Käyttöomaisuuden poistomenetelmät

Kahdeksan poistomenetelmää on saatavilla kohdassa [!INCLUDE [prod_short](includes/prod_short.md)]:  

* Suora viiva  
* Menojäännöspoisto 1  
* Menojäännöspoisto 2  
* MJP1/TP  
* MJP2/TP  
* Käyttäjäkohtainen  

  Määritä oma poistotapa käyttämällä poistotaulukoita. Lisätietoja käyttäjän määrittämän poistomenetelmän soveltamisesta on kohdassa [Käyttäjän määrittämän poistomenetelmän määrittäminen](fa-how-setup-user-defined-depreciation-method.md).
* Manuaalinen  

  Tätä manuaalista menetelmää voidaan käyttää omaisuuserille, joille ei tehdä poistoja, kuten maa-alueille. Poisto on vietävä käyttöomaisuuserän KP-päiväkirjaan. **Laske poisto** -eräajo jättää huomiotta käyttöomaisuuserät, joille käytetään manuaalista poistomenetelmää.  
* Puolivuotissopimus  

  Tällä menetelmällä käyttöomaisuudesta poistetaan joka vuosi sama summa.  

## Tasapoisto

Tasapoistomenetelmää käytettäessä käyttöomaisuuden poistokirjaan on määritettävä jokin seuraavista vaihtoehdoista:  

* Poistojakso (vuotta tai kuukautta) tai poiston lopetuspäivämäärä  
* Kiinteä vuosittainen prosentti  
* Kiinteä vuosittainen summa  
* Poistojakso  

### Poistojakso

Jos annat poistojakson (poistovuosien tai poistokuukausien lukumäärän tai poiston lopetuspäivämäärän), poistosumma lasketaan seuraavalla kaavalla:  

*Poistosumma = ((Kirjanpitoarvo - Jäännösarvo) x Poistopäivien lukumäärä) / Jäljellä olevat poistopäivät*  

Jäljellä oleviksi poistopäiviksi lasketaan poistopäivien lukumäärä miinus poiston aloituspäivän ja viimeisen käyttöomaisuustapahtuman päivän välisten päivien lukumäärä.  

Kirjanpitoarvoa voidaan vähentää kirjatulla arvonkorotuksella, arvonalennuksella, mukautettu 1- tai mukautettu 2 -summilla riippuen siitä, onko **Sisällytä poistolaskentaan** -kentästä poistettu aktivointi ja onko **Kirjanpitoarvon osa** -kenttä aktivoitu **KO:n kirjaustyypin asetukset** -sivulla. Laskenta takaa sen, että käyttöomaisuudelle tehdään kokonaispoisto poiston lopetuspäivämääränä.  

### Kiinteä vuosittainen prosentti

Jos annat kiinteän vuosittaisen prosentin, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää poistosumman laskemiseen seuraavaa laskukaavaa:  

*Poistosumma = (Tasapoisto-% x Poistopohja x Poistopäivien lkm) / (100 x 360)*  

### Kiinteä vuosittainen summa

Jos annat kiinteän vuosittaisen summan, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää poistosumman laskemiseen seuraavaa laskukaavaa:  

* *Poistosumma = (Kiinteä poistosumma x Poistopäivien lukumäärä) / 360*  

### Esimerkki - Tasapoisto

Käyttöomaisuuden hankintameno on PVA 100 000. Arvioitu käyttöikä on kahdeksan vuotta. **Laske poisto** -eräajo suoritetaan kaksi kertaa vuodessa.  

Tässä esimerkissä käyttöomaisuustapahtuma näyttää seuraavalta:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 01/01/20 |Hankintameno |(Poiston aloituspvm) |100,000.00 |100,000.00 |
| 06/30/20 |Arvonalennus |180 |-6.250,00 |93,750.00 |
| 12/31/20 |Arvonalennus |180 |-6.250,00 |87,500.00 |
| 06/30/21 |Arvonalennus |180 |-6.250,00 |81,250.00 |
| 12/31/21 |Arvonalennus |180 |-6.250,00 |75,000.00 |
| 06/30/27 |Arvonalennus |180 |-6.250,00 |6,250.00 |
| 12/31/27 |Arvonalennus |180 |-6.250,00 |0 |

## Menojäännöspoisto 1 -poisto

Tämä poistomenetelmä kohdistaa suurimman osan omaisuuserän kustannuksesta sen eliniän ensimmäisille vuosille. Tätä menetelmää käytettäessä tulee syöttää kiinteä vuosiprosentti.  

Poistosumma lasketaan seuraavalla kaavalla:  

* *Poistosumma = (Menojäännöspoisto-% x Poistopäivien lkm x Poistopohja) / (100 x 360)*  

Poistettavissa olevaksi pohjaksi lasketaan kirjanpitoarvo vuoden alussa. Poistopäivien määrä on kirjauspäivän ja viimeisen poistopäivän välisten päivien lukumäärä. [!INCLUDE [prod_short](includes/prod_short.md)] laskee poiston olettaen, että tilikaudelle tehdyt poistot tehdään tällä laskukaavalla.  

Kirjattu poistosumma voi sisältää tapahtumia, joilla on eri kirjaustyyppejä (arvonalennus, mukautettu 1 ja mukautettu 2), jotka on kirjattu nykyisen tilikauden aloituspäivämäärästä lähtien. Nämä kirjaustyypit sisältyvät kirjattuun poistosummaan, jos **Poistotyyppi**- ja **Osa kirjanpitoarvosta** -kentissä **KO:n kirjaustyypin asetukset** -sivulla on valintamerkki.  

### Esimerkki 1 - Menojäännöspoisto 1 -poisto

Käyttöomaisuuden hankintameno on PVA 100 000. **Menojäännöspoisto-%** -kentässä on arvo 25. **Laske poisto** -eräajo suoritetaan kaksi kertaa vuodessa.  

Seuraavassa taulukossa on esimerkkejä käyttöomaisuustapahtumista.  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 01/01/20 |Hankintamenot |(Poiston aloituspvm) |100,000.00 |100,000.00 |
| 06/30/20 |Arvonalennus |180 |-12.500,00 |87,500.00 |
| 12/31/20 |Arvonalennus |180 |-12.500,00 |75,000.00 |
| 06/30/21 |Arvonalennus |180 |-9.375,00 |65,625.00 |
| 12/31/21 |Arvonalennus |180 |-9.375,00 |56,250.00 |
| 06/30/22 |Arvonalennus |180 |-7.031,25 |49,218.75 |
| 12/31/22 |Arvonalennus |180 |-7.031,25 |42,187.50 |
| 06/30/23 |Arvonalennus |180 |-5.273,44 |36,914.06 |
| 12/31/23 |Arvonalennus |180 |-5.273,44 |31,640.62 |
| 06/30/24 |Arvonalennus |180 |-3.955,08 |27,685.54 |
| 12/31/24 |Arvonalennus |180 |-3.955,08 |23,730.46 |

Laskentamenetelmä:  

* Vuosi 1: *25 % arvosta 100 000 = 25 000 = 12 500 + 12 500*

* Vuosi 2: *25 % arvosta 75 000 = 18 750 = 9 375 + 9 375*

* Vuosi 3: *25 % arvosta 56 250 = 14 062,50 = 7 031,25 + 7 031,25*

Laskenta jatkuu siihen asti, kun kirjanpitoarvo on yhtä kuin lopullinen pyöristyssumma tai jäännösarvo, jonka syötit.  

### Esimerkki 2 - Menojäännöspoisto 1 -poisto

Omaisuuserän kirjanpitoarvo on 100 000 31.12.2022. Poisto 1 778 kirjataan 2.2.23. Se on odotettu (suhteellinen) määrä vuoden poistoista 32 päivän kohdalla. Jos poisto suoritetaan 30.6.2023, [!INCLUDE [prod_short](includes/prod_short.md)] ehdottaa 8 222:a, koska päivämäärien 2.2.2023 ja 30.6.2023 ero on 148 päivää. 30.6.2023 oletettu jäljellä oleva poisto lasketaan seuraavaa laskukaavaa käyttäen:

* *148/360 x 0,20 x 100 000 = 8 222*

### Esimerkki 3 - Menojäännöspoisto 1 -poisto

Jos kirjaat summan, joka ei vastaa menojäännöspoisto 1 -poistomenetelmää, esimerkiksi 5 000, [!INCLUDE [prod_short](includes/prod_short.md)] ehdottaa odotetun summaa jäljellä olevaa määrää.

Omaisuuserän kirjanpitoarvo on 100 000 31.12.2022. Poisto 5 000 kirjataan 2.2.23. Se on enemmän kuin odotettu (suhteellinen) määrä 2.2.2023 32 päivän kohdalla. Jos poisto suoritetaan 30.6.2023, [!INCLUDE [prod_short](includes/prod_short.md)] ehdottaa 8 222:a, koska päivämäärien 2.2.2023 ja 30.6.2023 ero on 148 päivää. 30.6.2023 oletettu jäljellä oleva poisto lasketaan seuraavaa laskukaavaa käyttäen:

* *148/360 x 0,20 x 100 000 = 8 222*

### Esimerkki 4 - Menojäännöspoisto 1 -poisto

Omaisuuserän kirjanpitoarvo on 100 000 31.12.2023. Poisto 95 000 kirjataan 2.2.23. Se ylittää vuoden sallitun poistosumman. Jos poisto suoritetaan 30.6.2023, [!INCLUDE [prod_short](includes/prod_short.md)] ehdottaa 5 000:a, koska päivämäärien 2.2.2023 ja 30.6.2023 ero on 148 päivää. 30.6.2023 oletettu jäljellä oleva poisto lasketaan seuraavaa laskukaavaa käyttäen: 

* *148/360 x 0,20 x 100 000 = 8 222*

Jäljellä oleva kirjanpitoarvo on kuitenkin vain 5 000, joten [!INCLUDE [prod_short](includes/prod_short.md)] ehdottaa 5 000:aa, koska kirjanpitoarvo ei voi olla negatiivinen.

## Menojäännöspoisto 2 -poisto

Menojäännöspoisto 1- ja Menojäännöspoisto 2 -menetelmät laskevat saman kokonaispoistosumman kullekin vuodelle. Jos **Laske poisto** -eräajo suoritetaan useammin kuin kerran vuodessa, Menojäännöspoisto 1 -menetelmä johtaa samansuuruisiin poistosummiin kunkin poistojakson osalta. Menojäännöspoisto 2 -menetelmä sen sijaan johtaa poistosummiin, jotka vähenevät joka jaksolla.  

### Esimerkki - Menojäännöspoisto 2 -poisto

Käyttöomaisuuden hankintameno on PVA 100 000. **Menojäännöspoisto-%** -kentässä on arvo 25. **Laske poisto** -eräajo suoritetaan kaksi kertaa vuodessa. Käyttöomaisuustapahtumat näyttävät seuraavalta:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 01/01/20 |Hankintamenot |(Poiston aloituspvm)|100,000.00 |100,000.00 |
| 06/30/20 |Arvonalennus |180 |-13.397,46 |86,602.54 |
| 12/31/20 |Arvonalennus |180 |-11.602,54 |75,000.00 |
| 06/30/21 |Arvonalennus |180 |-10.048,09 |64,951.91 |
| 12/31/21 |Arvonalennus |180 |-8.701,91 |56,250.00 |

Laskentamenetelmä:  

* *KP* = kirjanpitoarvo  
* *PM* = Poistopäivien määrä  
* *MJPP* = Menojäännöspoistoprosentti  
* *P* = *MJPP*/100  
* *P* = *PM*/360  

Poistosumman laskennan kaava on:  

*PS* = *KP* x (1 – (1 –P)<sup>P</sup>)

Poistojen arvot ovat:  

| Pvm | Laskenta |
| --- | --- |
| 06/30/20 |PS = 100 000,00 x (1 -(1 - 0,25)<sup>0,5</sup>) = 13 397,46 |
| 12/31/20 |PS = 86 602,54 x (1 - (1 - 0,25)<sup>0,5</sup>) = 11 602,54 |
| 06/30/21 |PS = 75 000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 10 048,09 |
| 12/31/21 |PS = 64 951,91 x (1 - (1 - 0,25)<sup>0,5</sup>) = 8 701,91 |

## MJP1/TP-poisto

MJP1/TP on lyhenne Menojäännöspoiston 1 ja Tasapoiston yhdistelmästä. Laskenta jatkuu siihen asti, kun kirjanpitoarvo on yhtä kuin lopullinen pyöristyssumma tai jäännösarvo, jonka annoit.  

**Laske poisto** -eräajolla lasketaan sekä tasapoistosumma että menojäännöspoistosumma, mutta vain suurempi summista siirretään päiväkirjaan.  

Voit laskea menojäännöspoiston käyttämällä eri prosentteja.  

Jos tätä menetelmää käytetään, **KO-poistokirjat** -sivulla on annettava arvioitu käyttöikä ja menojäännöspoistoprosentti  

> [!NOTE]
> Jos käytät jotakin menojäännöspoistomenetelmää ja haluat suorittaa poiston usean vuoden ajalta, kunkin vuoden poisto tulee suorittaa erikseen. Jos poisto suoritetaan koko jaksolta hankintapäivämäärästä viimeisen tilikauden tai viimeisen kirjanpitojakson loppuun, tulokset ovat todennäköisesti virheellisiä. Voit esimerkiksi haluta suorittaa sen useilta vuosilta, jos olet tuonut vanhoja tietoja ja käytät käyttöomaisuuserille todellisia hankintapäivämääriä ja haluat saada kiinni kumulatiivisen poiston. Menojäännöspoistomenetelmien osalta [!INCLUDE [prod_short](includes/prod_short.md)] laskee sallitun poiston vuodessa alkaen kunkin vuoden rekisteröidystä kirjanpitoarvosta. Se ei voi tehdä usean vuoden poistoa yhden vaiheen aikana.
>
> **Käyttöomaisuus - Suunnit. arvo** -raportissa voidaan projisoida usean vuoden jaksojen poistoja, mikä saattaa olla hämmentävää verrattuna saamiisi tuloksiin, jos poistot suoritetaan usean vuoden ajalta käyttämällä yhtä menojäännöspoistomenetelmistä. 

### Esimerkki - MJP1/TP-poisto

Käyttöomaisuuden hankintameno on PVA 100 000. **KO-poistokirjat** -sivun **Menojäännöspoisto-%** -kentässä on 25 ja **Poistovuosien lukumäärä** -kentässä on 8. **Laske poisto** -eräajo suoritetaan kaksi kertaa vuodessa.  

Käyttöomaisuustapahtumat näyttävät seuraavalta:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 01/01/20 |Hankintamenot |(Poiston aloituspvm) |100,000.00 |100,000.00 |
| 06/30/20 |Arvonalennus |180 |-12.500,00 |87,500.00 |
| 12/31/20 |Arvonalennus |180 |-12.500,00 |75,000.00 |
| 06/30/21 |Arvonalennus |180 |-9.375,00 |65,625.00 |
| 12/31/21 |Arvonalennus |180 |-9.375,00 |56,250.00 |
| 06/30/22 |Arvonalennus |180 |-7.031,25 |49,218.75 |
| 12/31/22 |Arvonalennus |180 |-7.031,25 |42,187.50 |
| 06/30/23 |Arvonalennus |180 |-5.273,44 |36,914.06 |
| 12/31/23 |Arvonalennus |180 |-5.273,44 |31,640.62 |
| 06/30/24 |Arvonalennus |180 |-3.955,08 |27,685.54 |
| 12/31/24 |Arvonalennus |180 |-3.955,08 |23,730.46 |
| 06/30/25 |Arvonalennus |180 |-3.955,08 |19 775,38 TP |
| 12/31/25 |Arvonalennus |180 |-3.955,08 |15 820,30 TP |
| 06/30/26 |Arvonalennus |180 |-3.955,08 |11 865,22 TP |
| 12/31/26 |Arvonalennus |180 |-3.955,07 |7 910,15 TP |
| 06/30/27 |Arvonalennus |180 |-3.955,08 |3 955,07 TP |
| 12/31/27 |Arvonalennus |180 |-3.955,07 |0,00 TP |

`SL` kirjanpitoarvon jälkeen tarkoittaa sitä, että käytettiin tasapoistomenetelmää.  

Laskentamenetelmä:  

* Vuosi 1 (2020):  

    *Menojäännöspoistosumma: 25 % 100 000:sta = 25 000 = 12 500 + 12 500*  

    *Tasapoistosumma = 100 000/8=12 500=6 250+6 250*  

    Tässä käytetään menojäännöspoistosummaa, koska se on suurempi.  

* Vuosi 5 (2025):  

    *Menojäännöspoistosumma: 25 % 23 730,46:sta = 4 943,85 = 2 471,92 + 2 471,92*  

    *Tasapoistosumma = 23 730,46/3 = 7 910,15=3 995,07+3 995,08*  

    Tässä käytetään tasapoistosummaa, koska se on suurempi.  

## Poisto puolivuotissopimusta käyttämällä

Puolivuotissopimus-menetelmää käytetään vain, jos **KO-poistokirja**-sivun **Käytä puolivuotissopimusta** -kentässä on valintamerkki.  

Tätä poistomenetelmää voidaan käyttää seuraavien sovelluksen poistomenetelmien kanssa:  

* Suora viiva  
* Menojäännöspoisto 1  
* MJP1/TP  

Kun käytetään Puolivuotissopimusta, käyttöomaisuudelle tehdään kuuden kuukauden poisto ensimmäisenä tilikautena **Poiston aloituspvm** -kentän sisällöstä huolimatta.  

> [!NOTE]  
> Käyttöomaisuuden arvioitu ikä, joka on jäljellä ensimmäisen tilikauden jälkeen, on aina puoli vuotta silloin, kun käytetään Puolivuotissopimus-menetelmää. Jotta Puolivuotissopimus-menetelmää voitaisiin käyttää oikein, **KO-poistokirja**-sivun **Poiston lopetuspvm** -kentässä tulee aina olla päivämäärä, joka on tasan kuusi kuukautta ennen sen tilikauden viimeistä päivämäärä, jolloin käyttöomaisuudelle tehdään kokonaispoisto.  

### Esimerkki – Poisto puolivuotissopimusta käyttämällä

Käyttöomaisuuden hankintameno on PVA 100 000. **Poiston aloituspvm** on 1.3.20. Arvioitu käyttöikä on viisi vuotta, joten **Poiston lopetuspvm** -kohdan arvon on oltava 30.6.25. **Laske poisto** -eräajo suoritetaan vuosittain. Tämä esimerkki perustuu kalenteritilikauteen.  

Käyttöomaisuustapahtumat näyttävät seuraavalta:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 03/01/20 |Hankintameno |(Poiston aloituspvm) |100,000.00 |100,000.00 |
| 12/31/20 |Arvonalennus |270 |-10.000,00 |90,000.00 |
| 12/31/21 |Arvonalennus |360 |-20.000,00 |70,000.00 |
| 12/31/22 |Arvonalennus |360 |-20.000,00 |50,000.00 |
| 12/31/23 |Arvonalennus |360 |-20.000,00 |30,000.00 |
| 12/31/24 |Arvonalennus |360 |-20.000,00 |10,000.00 |
| 12/31/25 |Arvonalennus |180 |-10.000,00 |0.00 |

## Esimerkki – MJP1/TP-poisto puolivuotissopimusta käyttämällä

Käyttöomaisuuden hankintameno on PVA 100 000. **Poiston aloituspvm** on 11.1.20. Arvioitu käyttöikä on viisi vuotta, joten **Poiston lopetuspvm** -kohdan arvon on oltava 30.6.25. **KO-poistokirjat**-sivun **Menojäännöspoisto-%**-kentässä on 40. **Laske poisto** -eräajo suoritetaan vuosittain. Tämä esimerkki perustuu kalenteritilikauteen.  

Käyttöomaisuustapahtumat näyttävät seuraavalta:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 11/01/20 |Hankintameno |(Poiston aloituspvm) |100,000.00 |100,000.00 |
| 12/31/20 |Arvonalennus |60 |-20.000,00 |80,000.00 |
| 12/31/21 |Arvonalennus |360 |-32.000,00 |48,000.00 |
| 12/31/22 |Arvonalennus |360 |-19.200,00 |28,800.00 |
| 12/31/23 |Arvonalennus |360 |-11.520,00 |17,280.00 |
| 12/31/24 |Arvonalennus |360 |-11.520,00 |5 760,00 TP |
| 12/31/25 |Arvonalennus |180 |-5,760.00 |0,00 TP |

`SL` kirjanpitoarvon jälkeen tarkoittaa sitä, että käytettiin tasapoistomenetelmää.  

Laskentamenetelmä:  

* Vuosi 1:  

    *Menojäännöspoistosumma = Koko vuoden summa = 40 % arvosta 100 000 = 40 000.* Joten puolen vuoden summa on 40 000 / 2 = 20 000  

    *Tasapoistosumma = Koko vuoden summa = 100 000 / 5 = 20 000.* Joten puolen vuoden summa = 20 000 / 2 =10 000  

    Tässä käytetään menojäännöspoistosummaa, koska se on suurempi.  

* Vuosi 5 (2024):  

    *Menojäännöspoistosumma = 40 % 17 280,00:sta = 6 912,00*  

    *Tasapoistosumma = 28 800 / 1,5 = 11 520,00*  

    Tässä käytetään tasapoistosummaa, koska se on suurempi.  

## Tapahtumien monistaminen lisäpoistokirjoihin

Jos poistokirjoja on kolme – B1, B2 ja B3 – ja jos haluat monistaa tapahtumia B1:stä B2:een ja B3:een, valitse B2:n ja B3:n poistokirjakorttien **Osa monistusluettelosta** -valintaruutu. Tästä asetuksesta voi olla hyötyä esimerkiksi seuraavissa tapauksissa:

* Poistokirja B1 integroituu pääkirjanpitoon ja käyttää käyttöomaisuuden KP-päiväkirjaa.
* Poistokirjat B2 ja B3 eivät integroidu pääkirjanpitoon ja käytä käyttöomaisuuden käyttöomaisuuspäiväkirjaa.  

Kun käyttöomaisuuskirjanpidon B1-kirjaan pääkirjanpidossa tehdään kirjaus ja valitaan **Käytä monistusluetteloa** -valintaruudun, [!INCLUDE [prod_short](includes/prod_short.md)] monistaa kirjauksen B2- ja B3-kirjaan käyttöomaisuuskirjanpidossa, kun kirjaus kirjataan.  

> [!NOTE]  
> Samaan päiväkirjaan tai päiväkirjan erään, josta olet monistamassa, ei voi monistaa. Jos tapahtumia kirjataan käyttöomaisuuden KP-päiväkirjaan, ne voidaan monistaa KO-päiväkirjaan tai käyttöomaisuuden KP-päiväkirjaan muuta erää käyttämällä.  

> [!NOTE]  
> Samaa numerosarjaa ei voi käyttää sekä käyttöomaisuuden KP-päiväkirjassa että KO-päiväkirjassa. Kun kirjaat tapahtumia KO/KP-päiväkirjaan, jätä **Asiakirjan nro** -kenttä tyhjäksi. Jos annat kenttään numeron, numero monistetaan KO-päiväkirjaan. Asiakirjanumero on muutettava manuaalisesti ennen päiväkirjan kirjaamista.  

## Katso myös

[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Taloushallinto](finance.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
