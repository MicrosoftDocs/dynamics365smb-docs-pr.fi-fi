---
title: Kentän tietojen antaminen| Microsoft Docs
description: Tietojen antamiseen nopeasti ja helposti on useita yleisiä toimintoja.. Tässä ohjeaiheessa kuvataan nämä tietojen syötön perustoiminnot.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: f1bd2fb92f787d52c5bbab8c2210b9d424c1ffd5
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "852491"
---
# <a name="entering-data"></a>Tietojen antaminen
Tietojen antamiseen nopeasti ja helposti on useita yleisiä toimintoja.. Tässä artikkelissa käsitellään tietojen antamisen perustoiminnot.  

Tämän artikkelin esimerkeissä käytetään esimerkkitietoja.

## <a name="mandatory-fields"></a>Pakolliset kentät
Kun annat tietoja sivuilla, tietyt kentät on merkitty punaisella tähtimerkillä. Punainen tähti tarkoittaa, että kenttä on täytettävä, jotta tietty kenttää käyttävä prosessi voidaan suorittaa, kuten kentässä olevaa arvoa käyttävän tapahtuman kirjaus.  

Vaikka kentässä on punainen tähti, et joudu täyttämään kenttää ennen kuin jatkat muihin kenttiin tai suljet sivun. Punainen tähti toimii vain muistutuksena siitä, että sinua estetään suorittamasta tiettyä prosessia.  


## <a name="finding-data-as-you-type"></a>Tietojen etsiminen kirjoitettaessa  
 Kun alat kirjoittaa merkkejä kenttään, näyttöön tulee avattava luettelo, joka sisältää kentän mahdollisia arvoja. Luettelon sisältö muuttuu, kun kirjoitat lisää merkkejä, ja voit valita luettelosta haluamasi vaihtoehdon, kun luettelo on näkyvissä.  

 Monissa kentissä on alanuolipainike, jonka voi valita. Napsauttamalla tätä painiketta saat näyttöön luettelon arvoista, jotka ovat määritettävissä kyseiseen kenttään. Painikkeella on kaksi eri tehtävää kentän tyypin mukaan:  

-   Haku - Ohjelma näyttää toisen taulukon tietoja, joita voi syöttää kenttään. Voit valita yhden tiedon kerrallaan.  

-   Avattava luettelo - Ohjelma näyttää kentän eri vaihtoehdot. Voit valita vain yhden vaihtoehdoista.  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards on the **Items** page, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a>Määrien antaminen laskutoimituksia käyttämällä  
 Kun syötät lukuja määräkenttiin, kuten nimikepäiväkirjan rivin **Määrä**-kenttään, voit syöttää summan asemesta kaavan. Seuraavassa on esimerkkejä:  

## <a name="examples"></a>Esimerkkejä  

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
 Päivämäärä-kenttään voi syöttää kaksi, neljä, kuusi tai kahdeksan numeroa:  

-   Jos syötät vain kaksi numeroa, ohjelma tulkitsee ne kuukaudeksi ja vuodeksi ja lisää käsittelypäivämäärän vuoden.  

-   Jos syötät neljä numeroa, ohjelma tulkitsee ne päiväksi ja kuukaudeksi ja lisää käsittelypäivämäärän vuoden.  

-   Jos päivämäärä, jonka haluat syöttää, on välillä 1.1.1930 ja 31.12.2029, voit syöttää vuoden kaksinumeroisena. Muutoin vuosi täytyy syöttää nelinumeroisena.  

 Voit myös syöttää päivämäärän viikonpäivänä, jota seuraa viikon numero tai vaihtoehtoisesti vuosi (esimerkiksi Ma25 tai ma25 tarkoittaa maanantaita viikolla 25).  

 Tietyn päivämäärän syöttämisen sijaan voit syöttää jommankumman seuraavista koodeista.  

|koodi|Tulos|  
|--------------|----------------|  
|t|Tämä on tämän päivän päivämäärä (tietokoneen järjestelmäpäivämäärä).|  
|k|Tämä on sovelluksessa määritettävä käsittelypäivämäärä. Lisätietoja käsittelypäivämäärän muuttamisesta on kohdassa [Perusasetusten muuttaminen](ui-change-basic-settings.md). Haluat ehkä käyttää käsittelypäivämäärää, jos sellaisia tapahtumia on paljon, joissa on jokin muu kuin tämän päivän päivämäärä.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

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
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Päivämäärän kaavojen käyttäminen  
 Päivämäärän kaava on lyhyt kirjain- ja numeroyhdistelmä, joka kertoo ohjelmalle, miten päivämäärät lasketaan. Voit kirjoittaa päivämäärän kaavoja erilaisiin päivämäärän laskentakenttiin sekä toistuvien päiväkirjojen toistotiheyskenttiin.  

> [!NOTE]  
>  Kaikissa tietokaavakentissä yksi päivä sisällytetään automaattisesti edustamaan kuluvaa päivää kauden alkupäivänä. Näin ollen jos määrität esimerkiksi 1V, kausi on kahdeksan päivää, koska tämä päivä lasketaan mukaan. Määritä seitsemän päivän kausi (yksi kokonainen viikko) sisältäen alkamispäivämäärän ja syötä sitten 6D tai 1W-1D.  

 Seuraavassa on joitakin esimerkkejä päivämäärän kaavojen käytöstä:  

-   Toistuvien päiväkirjojen toistotiheys-kentän päivämäärän kaava määrittää, kuinka usein päiväkirjan rivin tapahtuma kirjataan.  

-   Ylityskausi-kentän tietyn tason muistutusta koskeva päivämäärän kaava määrittelee ajanjakson, joka täytyy kulua eräpäivästä (tai edellisen muistutuksen päivämäärästä), ennen kuin muistutus voidaan luoda.  

-   Eräpäivän laskenta -kentän kaava määrittää, miten ohjelma laskee muistutuksen eräpäivän.  

 Eräpäivän laskentakaavassa voi olla enintään 20 merkkiä, sekä numeroita että kirjaimia. Voit käyttää seuraavia kirjaimia, jotka ovat aikamääreiden lyhenteitä:  

|||  
|-|-|  
|N|Nykyinen|  
|P|Päivä(t)|  
|VI|Viikko (viikot)|  
|K|Kuukausi (kuukaudet)|  
|Q |Neljännesvuosi|  
|V|Vuosi (vuodet)|  

 Voit rakentaa päivämääräkaavan kolmella eri tavalla:  

 Seuraava esimerkki näyttää, miten nykyinen ja numero.  

|||  
|-|-|  
|NVI|Nykyinen viikko|  
|NK|Nykyinen kuukausi|  

 Seuraava esimerkki näyttää, miten numero ja aikayksikkö. Numero ei voi olla suurempi kuin 9999.  

|||  
|-|-|  
|10P|10 päivää tästä päivästä|  
|2VI|2 viikkoa tämän päivän jälkeen|  

 Seuraava esimerkki näyttää, miten aikayksikkö ja numero.  

|||  
|-|-|  
|P10|Kuukauden seuraava 10. päivä|  
|VIP4|Viikon seuraava 4. päivä (torstai)|  

 Seuraavassa esimerkissä näytetään, miten voit yhdistää nämä kolme eri muotoa tarvittaessa:  

|||  
|-|-|  
|NK+10P|Nykyinen kuukausi + 10 päivää|  

 Miinus-merkin avulla pystyt ilmaisemaan menneitä päiviä. Esimerkiksi:  

|||  
|-|-|  
|-1 V.|1 vuosi taaksepäin tästä päivästä|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Katso myös  
 [Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen](ui-enter-criteria-filters.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
