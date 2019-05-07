---
title: Kentän tietojen antaminen| Microsoft Docs
description: Tietoja yleisistä ominaisuuksista, jotka auttavat antamaan tietoja kenttiin.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "929071"
---
# <a name="entering-data"></a>Tietojen antaminen

Käytettävissä on monia yleisiä ominaisuuksia, jotka helpottavat, nopeuttavat ja tarkentavat tietojen antamista. Tässä artikkelissa käsitellään tietojen antamisen yleisiä ominaisuuksia.  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a>Pikanäppäimet

Käytettävissä on useita pikanäppäimiä, joiden ansiosta hiiren käyttö ei ole välttämätöntä ja jotka nopeuttavat tietojen antamista etenkin jos annettavia tietoja on paljon ja jos samat tiedot kirjoitetaan toistuvasti.

Lisätietoja pikanäppäimissä on kohdassa [Pikanäppäimet](keyboard-shortcuts.md). Tässä artikkelissa käsitellään muutamia pikanäppäimiä.

## <a name="QuickEntry"></a>Tietojen syöttämisen helpottaminen pikatapahtuman avulla

Pikatapahtuma on näppäimistön avulla tapahtuvaa tietojen antamista varten suunniteltu ominaisuus. Pikatapahtumia voi käyttää kentissä (kuten korttisivuilla) ja luetteloissa (rivit ja sarakkeet). Siitä on hyötyä, jos kyse on toistuvista kirjoitustehtävistä, joissa on luotava peräkkäin toistuvia tietueita. Tällaisia ovat esimerkiksi myyntitilauserät tai uusien nimikkeiden rekisteröiminen.

Osaat jo ehkä siirtyä sivulla kentästä seuraavaan muokattavaan kenttään sarkainnäppäimellä. Sarkaimen käytön haittapuolena on kuitenkin se, että se siirtyy aina seuraavaan kenttään. <!-- even if the field is non-editable or seldom filled it in.-->Voit muuttaa tätä polkua pikatapahtuman avulla. Pikatapahtuman avulla voit siirtyä Enter-näppäimellä vain haluamiisi kenttiin. Tällä tavoin voit ohittaa kentät, joita ei voi muokata, ja kentät, joita et yleensä täytä. Olet ehkä jo havainnut tämän toiminnan joillakin sivuilla. Tämä johtuu siitä, että sovellus määrittää valmiiksi, mihin kenttiin Enter-näppäimellä siirrytään ja mitkä ohitetaan. Voit mukauttaa pikatapahtumaa mukauttamalla työtilaa ja optimoimalla tietojen antamistavan kullakin sivulla.

### <a name="how-quick-entry-works"></a>Pikatapahtuman toimintaperiaate

Jokainen kenttää voidaan merkitä joko *pikatapahtumaan sisällytetyksi* tai *pikatapahtumasta poissuljetuksi*. Pikatapahtumaan sisällytetyt kentät sisällytetään polkuun, johon Enter-näppäimellä siirrytään, kun taas pikatapahtumasta poissuljettuja kenttiä ei sisällytetä siihen.

Kun tiedot on annettu kenttään, vahvista muutokset Enter-näppäimellä ja siirry samalla seuraavaan kenttään. Jos haluat palata taaksepäin ja siirtyä edelliseen kenttään, paina näppäinyhdistelmää Vaihto+Enter. Lisätietoja pikanäppäimissä on kohdassa [Pikatapahtuman pikanäppäimet](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Vihjeitä
Seuraavassa luettelossa on joitakin hyödyllisiä tietoja pikatapahtumien käyttämisestä.

- Se on käytössä muokattavissa kentissä.
- Sitä voi käyttää myös sarakkeissa ja riveillä.
- Se ei estä sivun muiden osien, kuten toimintojen, käyttämistä, sillä niitä voi edelleen käyttää sarkaimella ja Vaihto+Sarkain-näppäinyhdistelmällä.  
- Pikatapahtumaa voi käyttää myös laajentamattomissa pikavälilehdissä. Jos seuraava pikatapahtumakenttä sijaitsee tiivistetyssä pikavälilehdessä, pikavälilehti laajentuu automaattisesti ja kohdistus on määritetyssä kentässä.
- Pikatapahtuma on käytettävissä riippumatta siitä, ovatko kentät pakollisia vai eivät. Tämän vuoksi kannattaa varmistaa, että pakolliset kentät sisällytetään pikatapahtumaan.
- Oletusarvoisesti useimmat kentät sisällytetään automaattisesti pikatapahtumaan. Tämän vuoksi joudutkin luultavasti aluksi sulkemaan kenttiä pois pikatapahtumasta.

### <a name="how-to-change-quick-entry-fields"></a>Pikatapahtumakenttien muuttaminen

Pikatapahtumaan sisällytettyjen tai poissuljettujen kenttien muuttaminen tehdään mukauttamisen avulla.

1. Aloita mukauttaminen valitsemalla ensin ![Asetukset](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") -kuvake ja sitten **Mukauta**.
2. Valitse muutettava kenttä tai luettelossa vastaava sarakeotsikko ja valitse sitten joko **Sisällytä pikatapahtumaan** tai **Sulje pois pikatapahtumasta**.

Lisätietoja mukauttamisesta on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Pakolliset kentät

Kun annat tietoja sivuilla, tietyt kentät on merkitty punaisella tähtimerkillä. Punainen tähti tarkoittaa, että kenttä on täytettävä, jotta tietty kenttää käyttävä prosessi voidaan suorittaa, kuten kentässä olevaa arvoa käyttävän tapahtuman kirjaus.  

Vaikka kentässä on punainen tähti, et joudu täyttämään kenttää ennen kuin jatkat muihin kenttiin tai suljet sivun. Punainen tähti toimii vain muistutuksena siitä, että sinua estetään suorittamasta tiettyä prosessia.  

## <a name="finding-data-as-you-type"></a>Tietojen etsiminen kirjoitettaessa

 Kun alat kirjoittaa merkkejä kenttään, näyttöön tulee avattava luettelo, joka sisältää kentän mahdollisia arvoja. Luettelon sisältö muuttuu, kun kirjoitat lisää merkkejä, ja voit valita luettelosta haluamasi vaihtoehdon, kun luettelo on näkyvissä.  

 Monissa kentissä on alanuolipainike, jonka voi valita. Napsauttamalla tätä painiketta saat näyttöön luettelon arvoista, jotka ovat määritettävissä kyseiseen kenttään. Painikkeella on kaksi eri tehtävää kentän tyypin mukaan:  

-   Haku - Ohjelma näyttää toisen taulukon tietoja, joita voi syöttää kenttään. Voit valita yhden tiedon kerrallaan.  

-   Avattava luettelo - Ohjelma näyttää kentän eri vaihtoehdot. Voit valita vain yhden vaihtoehdoista.  

## <a name="copying-and-pasting-fields-and-lines"></a>Kenttien ja rivien kopioiminen ja liittäminen

Voit kopioida yhden rivin tai useita rivejä luettelosta tai yhden kentän sivulta ja liittää kopioidut kohteet samalle sivulle, toiselle sivulle tai ulkoiseen asiakirjaan (kuten Microsoft Excel -asiakirjaan tai Outlook-sähköpostiin). Jos haluat kopioida, paina näppäimiä CTRL+C (cmd+C macOS-käyttöjärjestelmässä). Jos haluat liittää, paina näppäimiä CTRL+V (cmd+V macOS-käyttöjärjestelmässä).

Kopioi luettelossa kenttä yläpuolella olevan rivin samasta sarakkeesta ja liitä se nykyiselle riville painamalla F8-näppäintä.

Lisätietoja on kohdassa [Kopioiminen ja liittäminen Business Centralissa](ui-copy-paste.md).

## <a name="Focus"></a>Kohdistaminen rivinimikkeisiin

Jos käsittelet rivinimikeosan, kuten myyntitilaus- tai laskusivun, sisältäviä asiakirjoja, voit vaihtaa näkymän kohdistuksen rivinimikkeisiin. Käytännössä tämä tarkoittaa rivinimikkeen laajentamista siten, että se täyttää lähes koko työtilan, jolloin sivun muut osat piilotetaan yläreunassa olevia toimintoja lukuun ottamatta. Saat tällä tavoin hyvän yleiskuvan rivinimikkeistä, ja sinulla on enemmän tilaa niiden käsittelemiseen. Tämä on erityisen kätevää silloin, kun käsittelet suuria rivinimikeluetteloita ja tiedot pitäisi antaa nopeasti.

Lisäetuna on mahdollisuus käyttää suodatuksen lisäominaisuuksien, kuten muissakin luetteloissa, mikä helpottaa rivinimikkeiden selaamista ja hakemista.

### <a name="switch-the-focus-on-and-off"></a>Kohdistuksen ottaminen käyttöön ja poistaminen käytöstä

Jos haluat siirtää kohdistuksen rivinimikkeisiin, tee valinta jossakin rivinimikeosassa ja valitse sitten oikeassa yläkulmassa ![Kohdistustilan kuvake](media/focus-mode.png "Kohdistustilan kuvake") tai paina näppäinyhdistelmää Ctrl+Vaihto+F12.

Voit palata takaisin normaalinäkymään valitsemalla ![Kohdistustilan kuvake](media/focus-mode.png "Kohdistustilan kuvake") tai painamalla uudelleen näppäinyhdistelmää Ctrl+Vaihto+F12.

### <a name="filtering-the-line-items"></a>Rivinimikkeiden suodattaminen

Aloita suodatus avaamalla suodatinruutu valitsemalla ![Suodatinruutukuvake](media/open-filter-pane-icon.png "Suodatinruutukuvake") luettelon yläreunassa tai painamalla näppäinyhdistelmää **Vaihto+F3**. Voit käyttää suodatinruutua samalla tavoin kuin muitakin luetteloita. Lisätietoja on kohdassa [Suodattaminen](ui-enter-criteria-filters.md#Filtering).

Suodatuksesta on apua erityisesti silloin, kun tarkasteltava ja analysoitava asiakirja on pitkä. Oletetaan esimerkiksi, että avaat kirjatun myyntilaskun ja suodatat rivinimikkeet näyttämään kaikki rivinimikkeet, joilla on yli 5 %:n yksittäinen alennus, tai näytät suodatuksen avulla vain pyörän varusteet, joiden nimi sisältää sanan pro.

## <a name="entering-quantities-by-calculation"></a>Määrien antaminen laskutoimituksia käyttämällä

Kun syötät lukuja määräkenttiin, kuten nimikepäiväkirjan rivin **Määrä**-kenttään, voit syöttää summan asemesta kaavan. Seuraavassa on esimerkkejä:  

### <a name="examples"></a>Esimerkkejä  

-   Jos syötät 19+19, kentän arvoksi lasketaan 38.  

-   Jos syötät 41-9, kentän arvoksi lasketaan 32.  

-   Jos syötät 12*4, kentän arvoksi lasketaan 48.  

-   Jos syötät 12/4, kentän arvoksi lasketaan 3.  

## <a name="entering-negative-numbers"></a>Negatiivisten lukujen syöttäminen

Voit antaa negatiivisia lukuja kahdella tavalla. Numero -20.5 voidaan syöttää seuraavasti:  

-   -20.5  

    tai
-   20.5-  

 Kummassakin tapauksessa summa kirjataan arvona -20,5.  

 Jos lausekkeen viimeinen merkki on **+** tai **-**, koko lauseke kirjataan kyseisen merkin kanssa. Esimerkiksi **10-20+** johtaa tulokseen 10, ei tulokseen -10.  

## <a name="entering-dates-and-times"></a>Päivämäärien ja aikojen syöttäminen

Päivämääriä ja aikoja voi määrittää kaikissa päivämääräkentissä. Voit syöttää päivämäärät käyttäen erottimia tai ilman niitä.

> [!NOTE]  
> Päivämäärien ja kellonaikojen antaminen määräytyy **Alue**-asetusten mukaan. Lisätietoja on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Päivämäärien syöttäminen

Voit käyttää päivämääräkentissä joko päivämäärän valitsinta, joilla voit valita päivämäärän kalenterista, tai antaa päivämäärät manuaalisesti. Tässä osassa käsitellään lyhyesti päivämäärien antamista. Lisätietoja on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

Kun päivämäärä annetaan manuaalisesti, voit käyttää kahta, neljää, kuutta tai kahdeksaan numeroa:  

-   Jos syötät vain kaksi numeroa, ohjelma tulkitsee ne kuukaudeksi ja vuodeksi ja lisää käsittelypäivämäärän vuoden.  

-   Jos syötät neljä numeroa, ohjelma tulkitsee ne päiväksi ja kuukaudeksi ja lisää käsittelypäivämäärän vuoden.  

-   Jos päivämäärä, jonka haluat syöttää, on välillä 1.1.1930 ja 31.12.2029, voit syöttää vuoden kaksinumeroisena. Muutoin vuosi täytyy syöttää nelinumeroisena.  

Voit myös syöttää päivämäärän viikonpäivänä, jota seuraa viikon numero tai vaihtoehtoisesti vuosi (esimerkiksi Ma25 tai ma25 tarkoittaa maanantaita viikolla 25).  

Tietyn päivämäärän antamisen sijaan voit antaa jonkin seuraavista koodeista.  

|Koodi|Tulos|  
|--------------|----------------|  
|t|Tämä määrittää kuluvan päivän päivämäärän (tietokoneen järjestelmäpäivämäärä).|  
|p|Tämä määrittää kirjanpitojakson, jossa `p`tarkoittaa ensimmäistä kirjanpitojaksoa, `p2` toista kirjanpitojaksoa ja niin edelleen. |
|k|Tämä määrittää sovelluksessa määritettävän käsittelypäivämäärän. Lisätietoja käsittelypäivämäärän muuttamisesta on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md). Haluat ehkä käyttää käsittelypäivämäärää, jos sellaisia tapahtumia on paljon, joissa on jokin muu kuin tämän päivän päivämäärä.|
|n|Tämä määrittää, että `c`:n jälkeinen päivämäärä on sulkemispäivämäärä, kuten `C123101`.|  

## <a name="entering-times"></a>Aikojen syöttäminen

Kun syötät aikoja, voit lisätä minkä tahansa erotinmerkin yksiköiden väliin, mutta se ei ole tarpeen. Minuutteja, sekunteja tai AM/PM-merkintää (aamupäivä/iltapäivä) ei tarvitse kirjoittaa.  

Seuraavassa taulukossa on luettelo eri tavoista, joilla aikoja voi syöttää ja miten niitä tulkitaan:  

|Tapahtuma|Tulkinta|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30 |05:30:00|  
|0530|05:30:00|  
|5:30:5 |05:30:05|  
|053005 |05:30:05|  
|5:30:5,50|05:30:05.5|  
|053005050 |05:30:05.05 |  

 Jos et käytä erotinmerkkiä, jokaiselle aikayksikölle tulee syöttää kaksi numeroa.  

## <a name="entering-datetimes"></a>Päivämäärien ja aikojen syöttäminen

Kun syötät päivämääriä ja aikoja, päivämäärän ja ajan väliin on lisättävä tyhjätilamerkki.  

Seuraavassa taulukossa on luettelo eri tavoista, joilla päivämääriä ja aikoja voi syöttää ja miten niitä tulkitaan:  

|Tapahtuma|Tulkinta|  
|---------------|------------------------|  
|131202 132455|13.12.02 13:24:55|  
|1-12-02 10|01-12-02 10:00:00|  
|1.12.02 5|12.1.2002 05:00:00|  
|1.12.02|12.1.2013 00:00:00|  
|11 12|11-nykyinen kuukausi-nykyinen vuosi 12:00:00|  
|1112 12 |11-12-nykyinen vuosi 12:00:00|  
|t tai tänään|tämän päivän päivämäärä 00:00:00|  
|a aika|tämän päivän pvm tämänhetkinen aika|  
|t 10:30:00|tämän päivän päivämäärä 10:30:00|  
|t 3:3:3|tämän päivän päivämäärä 03:03:03|  
|k tai käsittelypvm|käsittelypvm 00:00:00|  
|ma tai maanantai|nykyisen viikon maanantai 00:00:00|  
|ti tai tiistai|nykyisen viikon tiistai 00:00:00|  
|ke tai keskiviikko|nykyisen viikon keskiviikko 00:00:00|  
|to tai torstai|nykyisen viikon torstai 00:00:00|  
|pe tai perjantai|nykyisen viikon perjantai 00:00:00|  
|la tai lauantai|nykyisen viikon lauantai 00:00:00|  
|su tai sunnuntai|nykyisen viikon sunnuntai 00:00:00|  
|ti 10:30:00|nykyisen viikon tiistai 10:30:00|  
|ti 3:3:3|nykyisen viikon tiistai 03:03:03|  

## <a name="entering-duration"></a>Keston syöttäminen

Kesto syötetään numerona, jota seuraa sen mittayksikkö.  

Seuraavassa on muutamia esimerkkejä:  

|Kesto|Mittayksikkö**|  
|------------------|-------------------------|  
|2t|2 tuntia|  
|6t 30 m|6 tuntia 30 minuuttia|  
|6,5t|6 tuntia 30 minuuttia|  
|90 m|1 tunti 30 minuuttia|  
|2p 6t 30m|2 päivää 6 tuntia 30 minuuttia|  
|2p 6t 30m 56s 600ms|2 päivää 6 tuntia 30 minuuttia 56 sekuntia 600 tuhannesosasekuntia|  

 Voit syöttää myös numeron, jonka ohjelma muuntaa automaattisesti kestoksi. Syöttämäsi numero muunnetaan kestokenttään määritellyn oletusmittayksikön mukaisesti.  

 Voit tarkastaa, mitä mittayksikköä kestokentässä käytetään, syöttämällä numeron ja katsomalla, mihin mittayksikköön ohjelma muuntaa sen.  

 Numero 5 muunnetaan 5 tunniksi, jos mittayksikkö on tunti.  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a>Katso myös  
 [Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen](ui-enter-criteria-filters.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
