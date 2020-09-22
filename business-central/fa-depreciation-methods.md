---
title: Poistomenetelmät| Microsoft Docs
description: Lisätietoja eri tavoista käyttöomaisuuden poistojen tai arvonalennusten toteuttamiseen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d6878413b4a3db077ffcd16f5f6939582fa57809
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787044"
---
# <a name="depreciation-methods"></a>Poistotavat
Saatavilla olevia poistomenetelmiä on kahdeksan:  

* Tasapoisto  
* Menojäännöspoisto 1  
* Menojäännöspoisto 2  
* MJP1/TP  
* MJP2/TP  
* Käyttäjäkohtainen  
* Manuaalinen  

  > [!NOTE]  
  >   Tätä menetelmää voidaan käyttää omaisuuserille, joille ei tehdä poistoja, kuten maa-alueille. Poisto on vietävä käyttöomaisuuserän KP-päiväkirjaan. **Laske poisto** -eräajo jättää huomiotta tätä poistomenetelmää käyttävät käyttöomaisuuserät.  
* Puolivuotissopimus  

  > [!NOTE]  
  >    Tätä menetelmää käytettäessä käyttöomaisuudesta poistetaan joka vuosi sama summa.  

## <a name="straight-line-depreciation"></a>Tasapoisto
Tasapoistomenetelmää käytettäessä käyttöomaisuuden poistokirjaan on määritettävä jokin seuraavista vaihtoehdoista:  

* Poistojakso (vuotta tai kuukautta) tai poiston lopetuspäivämäärä  
* Kiinteä vuosittainen prosentti  
* Kiinteä vuosittainen summa  
* Poistojakso  

### <a name="depreciation-period"></a>Poistojakso
Jos annat poistojakson (poistovuosien tai poistokuukausien lukumäärän tai poiston lopetuspäivämäärän), poistosumma lasketaan seuraavalla kaavalla:  

*Poistosumma = ((Kirjanpitoarvo - Jäännösarvo) x Poistopäivien lukumäärä) / Jäljellä olevat poistopäivät*  

Jäljellä oleviksi poistopäiviksi lasketaan poistopäivien lukumäärä miinus poiston aloituspäivän ja viimeisen käyttöomaisuustapahtuman päivän välisten päivien lukumäärä.  

Kirjanpitoarvoa voidaan vähentää kirjatulla arvonkorotuksella, arvonalennuksella, mukautettu 1- tai mukautettu 2 -summilla riippuen siitä, onko **Sisällytä poistolaskentaan** -kentästä poistettu aktivointi ja onko **Kirjanpitoarvon osa** -kenttä aktivoitu **KO:n kirjaustyypin asetukset** -sivulla. Laskenta takaa sen, että käyttöomaisuudelle tehdään kokonaispoisto poiston lopetuspäivämääränä.  

### <a name="fixed-yearly-percentage"></a>Kiinteä vuosittainen prosentti
Jos annat kiinteän vuosittaisen prosentin, sovellus käyttää poistosumman laskemiseen seuraavaa laskukaavaa:  

Poistosumma = (Tasapoisto-% x Poistopohja x Poistopäivien lkm) / (100 x 360)  

### <a name="fixed-yearly-amount"></a>Kiinteä vuosittainen summa
Jos annat kiinteän vuosittaisen summan, sovellus käyttää poistosumman laskemiseen seuraavaa laskukaavaa:  

Poistosumma = (Kiinteä poistosumma x Poistopäivien lukumäärä) / 360  

### <a name="example---straight-line-depreciation"></a>Esimerkki - Tasapoisto
Käyttöomaisuuden hankintameno on PVA 100 000. Arvioitu käyttöikä on kahdeksan vuotta. **Laske poisto** -eräajo suoritetaan kaksi kertaa vuodessa.  

Tässä esimerkissä käyttöomaisuustapahtuma näyttää seuraavalta:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 1.1.10 |Hankintameno |* |100,000.00 |100,000.00 |
| 30.6.10 |Arvonalennus |180 |-6.250,00 |93,750.00 |
| 31.12.10 |Arvonalennus |180 |-6.250,00 |87,500.00 |
| 30.6.11 |Arvonalennus |180 |-6.250,00 |81,250.00 |
| 31.12.11 |Arvonalennus |180 |-6.250,00 |75,000.00 |
| 30.6.17 |Arvonalennus |180 |-6.250,00 |6,250.00 |
| 31.12.17 |Arvonalennus |180 |-6.250,00 |0 |

* Poiston aloituspvm  

## <a name="declining-balance-1-depreciation"></a>Menojäännöspoisto 1 -poisto
Tämä degressiivinen poistomenetelmä kohdistaa suurimman osan omaisuuserän kustannuksesta sen eliniän ensimmäisille vuosille. Tätä menetelmää käytettäessä tulee syöttää kiinteä vuosiprosentti.  

Poistosumma lasketaan seuraavalla kaavalla:  

*Poistosumma = (Menojäännöspoisto-% x Poistopäivien lkm x Poistopohja) / (100 x 360)*  

Poistopohjaksi lasketaan kirjanpitoarvo vähennettynä kirjatulla poistolla nykyisen tilikauden aloituspäivämäärästä lähtien.  

Kirjattu poistosumma voi sisältää tapahtumia, joilla on eri kirjaustyyppejä (arvonalennus, mukautettu 1 ja mukautettu 2), jotka on kirjattu nykyisen tilikauden aloituspäivämäärästä lähtien. Nämä kirjaustyypit sisältyvät kirjattuun poistosummaan, jos **Poistotyyppi**- ja **Osa kirjanpitoarvosta** -kentissä **KO:n kirjaustyypin asetukset** -sivulla on valintamerkki.  

### <a name="example---declining-balance-1-depreciation"></a>Esimerkki - Menojäännöspoisto 1 -poisto
Käyttöomaisuuden hankintameno on PVA 100 000. **Menojäännöspoisto-%** -kentässä on arvo 25. **Laske poisto** -eräajo suoritetaan kaksi kertaa vuodessa.  

Seuraavassa taulukossa on esimerkkejä käyttöomaisuustapahtumista.  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 1.1.10 |Hankintamenot |* |100,000.00 |100,000.00 |
| 30.6.10 |Arvonalennus |180 |-12.500,00 |87,500.00 |
| 31.12.10 |Arvonalennus |180 |-12.500,00 |75,000.00 |
| 30.6.11 |Arvonalennus |180 |-9.375,00 |65,625.00 |
| 31.12.11 |Arvonalennus |180 |-9.375,00 |56,250.00 |
| 30.6.12 |Arvonalennus |180 |-7.031,25 |49,218.75 |
| 31.12.12 |Arvonalennus |180 |-7.031,25 |42,187.50 |
| 30.6.13 |Arvonalennus |180 |-5.273,44 |36,914.06 |
| 31.12.13 |Arvonalennus |180 |-5.273,44 |31,640.62 |
| 30.6.14 |Arvonalennus |180 |-3.955,08 |27,685.54 |
| 31.12.14 |Arvonalennus |180 |-3.955,08 |23,730.46 |

* Poiston aloituspvm  

    Laskentamenetelmä:  

    *1. vuosi: 25 % 100 000:sta = 25 000 = 12 500 + 12 500*

    *2. vuosi: 25 % 75 000:sta = 18 750 = 9 375 + 9 375*

    *3. vuosi: 25 % 56 250:sta = 14 062,50 = 7 031,25 + 7 031,25*

    Laskenta jatkuu siihen asti, kun kirjanpitoarvo on yhtä kuin lopullinen pyöristyssumma tai jäännösarvo, jonka syötit.   

## <a name="declining-balance-2-depreciation"></a>Menojäännöspoisto 2 -poisto
Menojäännöspoisto 1- ja Menojäännöspoisto 2 -menetelmät laskevat saman kokonaispoistosumman kullekin vuodelle. Jos **Laske poisto** -eräajo suoritetaan useammin kuin kerran vuodessa, Menojäännöspoisto 1 -menetelmä johtaa samansuuruisiin poistosummiin kunkin poistojakson osalta. Menojäännöspoisto 2 -menetelmä sen sijaan johtaa poistosummiin, jotka vähenevät joka jaksolla.  

### <a name="example---declining-balance-2-depreciation"></a>Esimerkki - Menojäännöspoisto 2 -poisto
Käyttöomaisuuden hankintameno on PVA 100 000. **Menojäännöspoisto-%** -kentässä on arvo 25. **Laske poisto** -eräajo suoritetaan kaksi kertaa vuodessa. Käyttöomaisuustapahtumat näyttävät seuraavalta:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 1.1.10 |Hankintamenot |* |100,000.00 |100,000.00 |
| 30.6.10 |Arvonalennus |180 |-13.397,46 |86,602.54 |
| 31.12.10 |Arvonalennus |180 |-11.602,54 |75,000.00 |
| 30.6.11 |Arvonalennus |180 |-10.048,09 |64,951.91 |
| 31.12.11 |Arvonalennus |180 |-8.701,91 |56,250.00 |

* Poiston aloituspvm  

Laskentamenetelmä:  

* KP = kirjanpitoarvo  
* PM = Poistopäivien määrä  
* MJPP = Menojäännöspoistoprosentti  
* P = DBP/100  
* D = ND/360  

Poistosumman laskennan kaava on:  

*PS = KP x (1 – (1 –P)<sup>P<sup>*  

Poistojen arvot ovat:  

| Pvm | Laskenta |
| --- | --- |
| 30.6.10 |PS = 100 000,00 x (1 -(1 - 0.25)<sup>0,5<sup>) = 13 397,46 |
| 31.12.10 |PS = 86 602,54 x (1 - (1 - 0,25)<sup>0,5<sup>) = 11 602,54 |
| 30.6.11 |PS = 75 000,00 x (1 - (1 - 0,25)<sup>0,5<sup>) = 10 048,09 |
| 31.12.11 |PS = 64 951,91 x (1 - (1 - 0,25)<sup>0,5<sup>) = 8 701,91 |

## <a name="db1sl-depreciation"></a>MJP1/TP-poisto
MJP1/TP on lyhenne Menojäännöspoiston 1 ja Tasapoiston yhdistelmästä. Laskenta jatkuu siihen asti, kun kirjanpitoarvo on yhtä kuin lopullinen pyöristyssumma tai jäännösarvo, jonka annoit.  

**Laske poisto** -eräajolla lasketaan sekä tasapoistosumma että menojäännöspoistosumma, mutta vain suurempi summista siirretään päiväkirjaan.  

Voit laskea menojäännöspoiston käyttämällä eri prosentteja.  

Jos tätä menetelmää käytetään, **KO-poistokirjat** -sivulla on annettava arvioitu käyttöikä ja menojäännöspoistoprosentti  

### <a name="example---db1-sl-depreciation"></a>Esimerkki - MJP1/TP-poisto
Käyttöomaisuuden hankintameno on PVA 100 000. **KO-poistokirjat** -sivun **Menojäännöspoisto-%** -kentässä on 25 ja **Poistovuosien lukumäärä** -kentässä on 8. **Laske poisto** -eräajo suoritetaan kaksi kertaa vuodessa.  

Käyttöomaisuustapahtumat näyttävät seuraavalta:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 1.1.10 |Hankintamenot |* |100,000.00 |100,000.00 |
| 30.6.10 |Arvonalennus |180 |-12.500,00 |87,500.00 |
| 31.12.10 |Arvonalennus |180 |-12.500,00 |75,000.00 |
| 30.6.11 |Arvonalennus |180 |-9.375,00 |65,625.00 |
| 31.12.11 |Arvonalennus |180 |-9.375,00 |56,250.00 |
| 30.6.12 |Arvonalennus |180 |-7.031,25 |49,218.75 |
| 31.12.12 |Arvonalennus |180 |-7.031,25 |42,187.50 |
| 30.6.13 |Arvonalennus |180 |-5.273,44 |36,914.06 |
| 31.12.13 |Arvonalennus |180 |-5.273,44 |31,640.62 |
| 30.6.14 |Arvonalennus |180 |-3.955,08 |27,685.54 |
| 31.12.14 |Arvonalennus |180 |-3.955,08 |23,730.46 |
| 30.6.15 |Arvonalennus |180 |-3.955,08 |19 775,38 TP |
| 31.12.15 |Arvonalennus |180 |-3.955,08 |15 820,30 TP |
| 30.6.16 |Arvonalennus |180 |-3.955,08 |11 865,22 TP |
| 31.12.16 |Arvonalennus |180 |-3.955,07 |7 910,15 TP |
| 30.6.17 |Arvonalennus |180 |-3.955,08 |3 955,07 TP |
| 31.12.17 |Arvonalennus |180 |-3.955,07 |0,00 TP |

* Poiston aloituspvm  

"TP" kirjanpitoarvon jälkeen tarkoittaa sitä, että käytettiin tasapoistomenetelmää.  

Laskentamenetelmä:  

vuosi:  

*Menojäännöspoistosumma: 25 % 100 000:sta = 25 000 = 12 500 + 12 500*  

*Tasapoistosumma = 100 000/8=12 500=6 250+6 250*  

Tässä käytetään menojäännöspoistosummaa, koska se on suurempi.  

vuosi (2015):  

*Menojäännöspoistosumma: 25 % 23 730,46:sta = 4 943,85 = 2 471,92 + 2 471,92*  

*Tasapoistosumma = 23 730,46/3 = 7 910,15=3 995,07+3 995,08*  

Tässä käytetään tasapoistosummaa, koska se on suurempi.  

## <a name="user-defined-depreciation"></a>Käyttäjän määrittämä poisto
Sovelluksessa on ominaisuus, joka mahdollistaa käyttäjäkohtaisten poistomenetelmien määrittämisen.  

Käyttäjäkohtaisessa menetelmässä käytetään **Poistotaulukot**-sivu, johon tulee syöttää poistoprosentti kullekin jaksolle (kuukaudelle, vuosineljännekselle tai kirjanpitojaksolle).  

Poistosumman laskennan kaava on:  

Poistosumma = (Poisto-% x Poistopäivien lkm x Poistopohja) / (100 x 360)  

### <a name="depreciation-based-on-number-of-units"></a>Yksiköiden lukumäärään perustuvat poistot
Tätä käyttäjäkohtaista menetelmää voidaan käyttää myös poistoissa, jotka perustuvat yksiköiden lukumäärään, esimerkiksi sellaisten tuotantokoneiden kohdalla, joiden eliniän kapasiteetti on vakio. **Poistotaulukot**-sivulle voidaan syöttää yksiköiden lukumäärä, joka voidaan tuottaa kullakin ajanjaksolla (kuukaudessa, neljännesvuodessa, vuodessa tai kirjanpitojakson aikana).  

### <a name="to-set-up-user-defined-depreciation-methods"></a>Käyttäjäkohtaisten poistomenetelmien määrittäminen
**Poistotaulukon kortti** -sivulla voidaan määrittää käyttäjäkohtaiset poistomenetelmät. Voit esimerkiksi määrittää poiston yksiköiden määrän perusteella.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poistotaulukot** ja valitse sitten liittyvä linkki.  
2. Valitse **Poistotaulukkoluettelo**-sivulla **Uusi**-toiminto.  
3. Täytä **Poistotaulukon kortti** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="example---user-defined-depreciation"></a>Esimerkki - käyttäjän määrittämä poisto
Käytä poistomenetelmää, joka mahdollistaa poistojen tekemisen käyttöomaisuuseriin nopeutetusti tuloverotarkoituksia varten.  

Voit käyttää seuraavia poistoarvoja verotustarkoituksia varten käyttöomaisuudelle, jonka ikä on kolme vuotta:  

* 1. vuosi: 25%  
* 2. vuosi: 38%  
* 3. vuosi: 37%  

Hankintameno on 100 000 PVA ja poistoaika on viisi vuotta. Poisto lasketaan vuosittain.  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 1.1.10 |Hankintameno |* |100,000.00 |100,000.00 |
| 31.12.10 |Arvonalennus |360 |-25.000,00 |75,000.00 |
| 31.12.11 |Arvonalennus |360 |-38.000,00 |37,000.00 |
| 31.12.12 |Arvonalennus |360 |-37.000,00 |0 |
| 31.12.13 |Arvonalennus |Ei yhtään |Ei yhtään |0 |
| 31.12.14 |Arvonalennus |Ei yhtään |Ei yhtään |0 |

* Poiston aloituspvm  

Jos käytät käyttäjäkohtaista menetelmää, **Ens. käyttäjäkoht. poistopvm**- ja **Poiston aloituspvm**-kenttä tulee olla täytettynä **KO-poistokirjat**-sivulla. **Ens. käyttäjäkoht. poistopvm** -kenttää ja **Poistotaulukot**-sivun **Jakson pituus** -kentän sisältöä käytetään määrittämään poistolaskennassa käytettäviä aikavälejä. Näin varmistetaan, että sovellus aloittaa määritetyn prosenttiosuuden käyttämisen samana päivinä kaikissa omaisuuserissä. **Poiston aloituspvm** -kenttää käytetään laskemaan poistopäivien lukumäärä.  

Edellisessä esimerkissä sekä **Ens. käyttäjäkoht. poistopvm**- ja **Poiston aloituspvm** -kentissä on 1.1.01. Jos kuitenkin **Ens. käyttäjäkoht. poistopvm** -kentässä oli 1.1.10 ja **Poiston aloituspvm** -kentässä oli 1.4.11, tuloksena olisi:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 1.1.10 |Hankintameno |* |100,000.00 |100,000.00 |
| 31.12.10 |Arvonalennus |270 |-18.750,00 |81,250.00 |
| 31.12.11 |Arvonalennus |360 |-38.000,00 |42,250.00 |
| 31.12.12 |Arvonalennus |360 |-37.000,00 |6,250.00 |
| 31.12.13 |Arvonalennus |90 |-6.250,00 |0 |
| 31.12.14 |Arvonalennus |Ei yhtään |Ei yhtään |0 |

* Poiston aloituspvm  

## <a name="half-year-convention-depreciation"></a>Poisto puolivuotissopimusta käyttämällä
Puolivuotissopimus-menetelmää käytetään vain, jos **KO-poistokirja**-sivun **Käytä puolivuotissopimusta** -kentässä on valintamerkki.  

Tätä poistomenetelmää voidaan käyttää yhdessä seuraavien sovelluksen poistomenetelmien kanssa:  

* Tasapoisto  
* Menojäännöspoisto 1  
* MJP1/TP  

Kun käytetään Puolivuotissopimusta, käyttöomaisuudelle tehdään kuuden kuukauden poisto ensimmäisenä tilikautena **Poiston aloituspvm** -kentän sisällöstä huolimatta.  

> [!NOTE]  
>   Käyttöomaisuuden arvioitu ikä, joka on jäljellä ensimmäisen tilikauden jälkeen, on aina puoli vuotta silloin, kun käytetään Puolivuotissopimus-menetelmää. Jotta Puolivuotissopimus-menetelmää voitaisiin käyttää oikein, **KO-poistokirja**-sivun **Poiston lopetuspvm** -kentässä tulee aina olla päivämäärä, joka on tasan kuusi kuukautta ennen sen tilikauden viimeistä päivämäärä, jolloin käyttöomaisuudelle tehdään kokonaispoisto.  

### <a name="example---half-year-convention-depreciation"></a>Esimerkki – Poisto puolivuotissopimusta käyttämällä
Käyttöomaisuuden hankintameno on PVA 100 000. **Poiston aloituspvm** on 1.3.10. Arvioitu käyttöikä on viisi vuotta, joten **Poiston lopetuspvm** -kohdan arvon on oltava 30.6.15. **Laske poisto** -eräajo suoritetaan vuosittain. Tämä esimerkki perustuu kalenteritilikauteen.  

Käyttöomaisuustapahtumat näyttävät seuraavalta:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 1.3.10 |Hankintameno |* |100,000.00 |100,000.00 |
| 31.12.10 |Arvonalennus |270 |-10.000,00 |90,000.00 |
| 31.12.11 |Arvonalennus |360 |-20.000,00 |70,000.00 |
| 31.12.12 |Arvonalennus |360 |-20.000,00 |50,000.00 |
| 31.12.13 |Arvonalennus |360 |-20.000,00 |30,000.00 |
| 31.12.14 |Arvonalennus |360 |-20.000,00 |10,000.00 |
| 31.12.15 |Arvonalennus |180 |-10.000,00 |0.00 |

* Poiston aloituspvm  

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Esimerkki – MJP1/TP-poisto puolivuotissopimusta käyttämällä
Käyttöomaisuuden hankintameno on PVA 100 000. **Poiston aloituspvm** on 1.11.10. Arvioitu käyttöikä on viisi vuotta, joten **Poiston lopetuspvm** -kohdan arvon on oltava 30.6.15. **KO-poistokirjat**-sivun **Menojäännöspoisto-%**-kentässä on 40. **Laske poisto** -eräajo suoritetaan vuosittain. Tämä esimerkki perustuu kalenteritilikauteen.  

Käyttöomaisuustapahtumat näyttävät seuraavalta:  

| Pvm | KO:n kirjaustyyppi | Päivää | Summa | Kirjanpitoarvo |
| --- | --- | --- | --- | --- |
| 1.11.10 |Hankintameno |* |100,000.00 |100,000.00 |
| 31.12.10 |Arvonalennus |60 |-20.000,00 |80,000.00 |
| 31.12.11 |Arvonalennus |360 |-32.000,00 |48,000.00 |
| 31.12.12 |Arvonalennus |360 |-19.200,00 |28,800.00 |
| 31.12.13 |Arvonalennus |360 |-11.520,00 |17,280.00 |
| 31.12.14 |Arvonalennus |360 |-11.520,00 |5 760,00 TP |
| 31.12.15 |Arvonalennus |180 |-5,760.00 |0,00 TP |

* Poiston aloituspvm  

"TP" kirjanpitoarvon jälkeen tarkoittaa sitä, että käytettiin tasapoistomenetelmää.  

Laskentamenetelmä:  

vuosi:  

*Menojäännöspoistosumma = Koko vuoden summa = 40 % 100 000:sta = 40 000. Puolen vuoden summa on siis 40 000 / 2 = 20 000.*  

*Tasapoistosumma = Koko vuoden summa = 100 000 / 5 = 20 000. Puolen vuoden summa on siis = 20 000 / 2 = 10 000.*  

Tässä käytetään menojäännöspoistosummaa, koska se on suurempi.  

vuosi (2004):  

*Menojäännöspoistosumma = 40 % 17 280,00:sta = 6 912,00*  

*Tasapoistosumma = 28 800 / 1,5 = 11 520,00*  

Tässä käytetään tasapoistosummaa, koska se on suurempi.  

## <a name="duplicating-entries-to-more-depreciation-books"></a>Tapahtumien monistaminen lisäpoistokirjoihin
Jos poistokirjoja on kolme – B1, B2 ja B3 – ja jos haluat monistaa tapahtumia B1:stä B2:een ja B3:een, B2:n ja B3:n poistokirjakorttien **Osa monistusluettelosta** -kenttään voi lisätä rastin. Tämä voi olla hyödyllistä, jos poistokirja B1 on integroitu pääkirjanpidon kanssa, ja se käyttää käyttöomaisuuden KP-päiväkirjaa, eikä poistokirjoja B2 ja B3 ole integroitu pääkirjanpidon kanssa, ja ne käyttävät käyttöomaisuuden päiväkirjaa.  

Kun käyttöomaisuuden KP-päiväkirjan B1:een annetaan tapahtuma ja **Käytä monistusluetteloa** -kenttään lisätään valintamerkki, sovellus monistaa KO-päiväkirjan kirjassa B2 ja B3 olevan tapahtuman silloin, kun tapahtuma kirjataan.  

> [!NOTE]  
>   Samaan päiväkirjaan tai päiväkirjan erään, josta olet monistamassa, ei voi monistaa. Jos tapahtumia kirjataan käyttöomaisuuden KP-päiväkirjaan, ne voidaan monistaa KO-päiväkirjaan tai käyttöomaisuuden KP-päiväkirjaan muuta erää käyttämällä.  

> [!NOTE]  
>   Samaa numerosarjaa ei voi käyttää sekä käyttöomaisuuden KP-päiväkirjassa että KO-päiväkirjassa. Kun kirjaat tapahtumia KO/KP-päiväkirjaan, jätä **Asiakirjan nro** -kenttä tyhjäksi. Jos annat kenttään numeron, numero monistetaan KO-päiväkirjaan. Asiakirjanumero on muutettava manuaalisesti ennen päiväkirjan kirjaamista.  

## <a name="see-also"></a>Katso myös
[Käyttöomaisuus](fa-manage.md)  
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Rahoitus](finance.md)  
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
