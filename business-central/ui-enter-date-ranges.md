---
title: Päivämäärien ja aikojen syöttäminen Business Centralissa
description: 'Tietoja päivämäärien ja aikojen syöttämisestä sekä erilaisista tuottavuutta lisäävistä vihjeistä, jotka liittyvät esimerkiksi pikakirjoitukseen, lausekkeisiin ja alueisiin.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'dates, reporting, filter, calendar, shorthand, range'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 10/27/2023
ms.author: bholtorf
---

# Kalenterin päivämäärien ja aikojen käsitteleminen

Päivämäärät ja -ajat voi syöttää usealla eri tavalla. [!INCLUDE[prod_short](includes/prod_long.md)] sisältää tehokkaita toimintoja, jotka nopeuttavat tietojen syöttämistä ja helpottavat monimutkaisten kalenterilausekkeiden kirjoittamista. Sovelluksessa on useita kohtia, joissa voi syöttää päivämääriä ja aikoja kenttiin. Esimerkiksi myyntitilauksessa voi määrittää lähetyspäivämäärän. Voit syöttää päivämäärät ja ajat luetteloiden tai raportin tietojen suodattamisen yhteydessä ja etsiä vain tiedot, joista olet kiinnostunut.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Alueen ja kielen asetusten tarkistaminen

**Omat asetukset** -sivulla määritetään sovelluksessa käytettävä **alue** ja **kieli**. Nämä asetukset vaikuttavat päivämäärien ja aikojen syöttötapaan.

- **Alue**-asetus määrittää, miten päivämäärät, ajat, luvut ja valuutat näkyvät tai miten ne on muotoiltu.

- Jos päivämäärämallit sisältävät sanoja, sanojen kielen on oltava **Kieli**-asetuksessa määritetty kieli.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] käyttää gregoriaanista kalenterijärjestelmää.

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## Päivämäärien syöttäminen

Voit syöttää päivämääräkenttään päivämäärän alueasetuksen vakiomuodossa. Eri alueilla voidaan käyttää päivien, kuukausien ja vuosien välillä erilaisia erottimia. Esimerkiksi joillakin alueilla käytetään ajatusviivoja (kk-pp-vvvv) ja toisilla alueilla vinoviivoja (kk/pp/vvvv).  

> [!TIP]
> Voit käyttää mitä tahansa erottimia, jopa välilyöntiä. Päivämäärää muutetaan automaattisesti niin, että se sisältää aluettasi vastaavat erottimet.

> [!NOTE]
> Oma alueasetuksesi ei vaikuta päivämäärän näyttömuotoon tulostetuissa raporteissa ja sähköpostitse lähetetyissä asiakirjoissa.

Seuraavissa osissa esiteltyjen menetelmien ja muotojen avulla voit käyttää päivämääriä ja aikoja tuottavammin.

### Päivämäärien valitseminen kalenterista

Mitä tahansa kalenterikuvakkeen sisältävä kenttä voidaan määrittää kalenterin päivämäärän valitsimen avulla. Voit näyttää kalenterin päivämäärän valitsimen aktivoimalla kalenterikuvakkeen tai painamalla kentässä pikanäppäimiä <kbd>Ctrl</kbd>+<kbd>Home</kbd>.

![Pvm-kentät.](media/ui-date-field.png "Esimerkki päivämääräkentästä")

Katso myös [Kalenterin päivämäärän valitsimen pikanäppäimet](keyboard-shortcuts.md#calendarshortcuts)

### Päivä\-viikko\-vuosi-malli

Voit syöttää päivämäärän viikonpäivänä, jonka jälkeen tulee viikon numero ja halutessasi vuosi. Esimerkiksi Ma25 tai ma25 tarkoittaa viikon 25 maanantaita. Jos et syötä vuotta, käytetään käsittelypäivämäärän vuotta.

Sen sijaan, että syötät koko sanan viikonpäivää varten, voit syöttää sanan alkuosan. Ristiriitatilanteissa, esimerkiksi kun s voi tarkoittaa sekä lauantaita (Saturday) tai sunnuntaita (Sunday), päivät arvioidaan alueasetuksen mukaan. Syöte arvioidaan ensin käsittelypäivämäärä- ja tänään-määritteiden avulla. Pidä tämä mielessä, kun lyhennät sanoja. Esimerkiksi _t_ merkitsee jo tämän päivän päivämäärää, joten se ei voi tarkoittaa tiistaita tai torstaita.

Viikon numeromalli on aina ISO 8601, jossa viikko 1 on viikko, joka sisältää tammikuun 4. päivän tai vuoden ensimmäisen torstain.

### Numeromallit

Päivämäärä-kenttään voi syöttää kaksi, neljä, kuusi tai kahdeksan numeroa:

- Jos syötät vain kaksi numeroa, ohjelma tulkitsee ne kuukaudeksi ja vuodeksi ja lisää käsittelypäivämäärän vuoden.

- Jos syötät neljä numeroa, ohjelma tulkitsee ne päiväksi ja kuukaudeksi ja lisää käsittelypäivämäärän vuoden. Päivän ja kuukauden järjestys riippuu alueasetuksista. Vaikka alueasetuksissa olisi vuosi ennen päivää ja kuukautta, neljä lukua tulkitaan päiväksi ja kuukaudeksi.

- Jos päivämäärä, jonka haluat syöttää, on välillä 1.1.1950 ja 31.12.2049, voit syöttää vuoden kaksinumeroisena. Muutoin vuosi täytyy syöttää nelinumeroisena.

  > [!NOTE]
  > Jos käytössä on paikallinen [!INCLUDE[prod_short](includes/prod_short.md)], kaksinumeroinen vuosiväli voi olla eri. Järjestelmänvalvojat voivat muuttaa aluetta muuttamalla **CalendarTwoDigitYearMax**-asetusta [!INCLUDE[prod_short](includes/prod_short.md)]-palvelimessa. Lisätietoja on kohdassa [Business Central Serverin määrittäminen](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General).
 
### Tänään

Syötä sana _today_ **Omat asetukset** -sivulla määritetyllä kielellä määrittääksesi tietueen päivämäärän tälle päivämäärälle. Sen sijaan, että syötät koko sanan, voit syöttää sanan alkuosan. Esimerkiksi suomeksi voit syöttää _t_ tai _tän_, kunhan se ei ole myös jonkin toisen sanan alku.

### Jakso

Voit suodattaa tietyn kirjanpitojakson antamalla päivämääräkentässä kirjaimen j tai sanan jakso ja lisäämällä sen perään luvun, joka yksilöi kirjanpitojakson, kuten j2 tai jakso4. Kirjapitojakso liittyy roolikeskuksessa määritetyn kuluvan käsittelypäivän tilikauteen. Jos esimerkiksi käsittelypäivämäärä on **21.3.22**, _j1_ tai vain _j_ suodattaa tilikauden 2022 ensimmäisen kirjanpitojakson (kuten 1.1.2022–31.1.2022). _j15_ suodattaa 15:nnen kirjanpitojakson tilikauden 2022 alusta (kuten 1.3.2023–31.3.2023).

Kirjanpitojaksot määritetään **Kirjanpitojaksot**-sivulla. Voit tarkastella tai muuttaa kirjanpitojaksoja avaamalla sivun [täällä](https://businesscentral.dynamics.com/?page=100).

### Käsittelypvm

Käytä käsittelypäivämäärää määrittääksesi päivämäärän, joka ei ole tietueissa tämä päivämäärä. Käsittelypäivämäärästä on hyötyä esimerkiksi tilanteessa, jossa useille tietueille on asetettava tietty päivämäärä. Käsittelypäivämäärä määritetään **Omat asetukset** -sivulla. 

Nopea tapa syöttää tietueiden käsittelypäivämäärä on syöttää sana _work_ tai osa siitä sanan alusta alkaen kielellä, jota käytät [!INCLUDE[prod_short](includes/prod_long.md)]issa. Esimerkiksi suomeksi voit syöttää _k_ tai _käsit_. Myös kieli määritetään **Omat asetukset** -sivulla.

Jos et ole määrittänyt käsittelypäivämäärää, käytetään tämän päivän päivämäärää. Lisätietoja on kohdassa [Perusasetusten, kuten käsittelypäivämäärän, muuttaminen](ui-change-basic-settings.md#work-date).

### Sulkemispvm

Kun suljet tilikauden, voit käyttää sulkemispäivämääriä osoittaaksesi, että tapahtuma on tilinpäätöstapahtuma. Sulkemispäivämäärä sijoittuu teknisesti kahden päivämäärän väliin, esimerkiksi joulukuun 31. päivän ja tammikuun 1. päivän väliin.

Jos haluat määrittää, että päivämäärä on sulkemispäivämäärä, kirjoita N päivämäärän edelle , esimerkiksi N31.12.01. Käytä tätä muotoa kaikkien päivämäärämallien kanssa.

### Esimerkkejä

Seuraavassa taulukossa on esimerkkejä kaikkia muotoja käyttävistä päivämääristä. Oletetaan, että alueasetukset muotoilevat päivämäärät näin: **vuosi.kuukausi.päivä.**, viikko alkaa maanantaista ja kieli on englanti.

|**Tapahtuma**      |**Tulkinta**      |
|---------------|------------------------|
|2022.12.31.|2022.12.31.|
|221231|2022.12.31.|
|22.12.31.|2022.12.31.|
|22.12.31.|2022.12.31.|
|20221231|2022.12.31.|
|22/12,31|2022.12.31.|
|11|käsittelypvm:n vuosi.käsittelypvm:n kuukausi.11.|
|11.12|käsittelypvm:n vuosi.11.12.|
|t tai tänään|tämän päivän päivämäärä|
|j4|päivämääräalue, joka sisältää neljännen kirjanpitojakson, kuten 1.4.20-30.4.20|
|k tai käsittelypvm|käsittelypvm|
|ma tai maanantai|Käsittelypvm:n viikon maanantai|
|ti tai tiistai|Käsittelypvm:n viikon tiistai|
|la tai lauantai|Käsittelypvm:n viikon lauantai|
|su tai sunnuntai|Käsittelypvm:n viikon sunnuntai|
|t23|Käsittelypvm:n vuoden viikon 23 tiistai|
|t 23|Käsittelypvm:n vuoden viikon 23 tiistai|
|t-1|Käsittelypvm:n vuoden viikon 1 tiistai|

##  <a name="BKMK_SettingDateRanges"></a> Alueiden asettaminen

Luetteloissa, kokonaissummissa ja raporteissa voi määrittää suodattimia päivämäärille, ajoille sekä päivämäärille ja ajoille, joilla on aloitusarvo ja vaihtoehtoisesti lopetusarvo, jolloin näytetään vain kyseisen alueen tiedot. Päivämääräalueiden määrittämisessä käytetään vakiosääntöjä.

|**Merkitys**|**Esimerkkilauseke (pvm)**|**Suodatukseen sisällytettävät tiedot**|
|-----------|---------------------|--------------------|
|Väli|15.12.00-15.1.01<br /><br />-15.12.00<br /><br />j1-j4|Tietueet, joiden päivämäärät ovat välillä 15.12.00 ja 15.1.01 kyseiset päivät mukaan lukien.<br /><br />Tietueet, joiden päivämäärä on 15.12.00 tai aiempi.<br /><br />Päivämääräalue, joka sisältää toisen, kolmannen ja neljännen kirjanpitojakson, kuten 1.1.20-30.4.20.|
|Joko/tai|12 15 00\|12 16 00|Tietueet, joiden päivämäärät ovat 15.12.00 tai 16.12.00. Myös tietueet, joilla on molemmat päivämäärät, näytetään.|
|Yhdistelmä|12 15 00\|12 01 00..12 10 00  <br /><br />..12 14 00\|12 30 00..|Tietueet, joiden päivämäärät ovat 15.12.00 tai 01.12.00 ja 10.12.00 sekä niiden välisenä aikana.  <br /><br />Tietueet, joiden päivämäärä on 12 14 00 tai sitä aiempi, tai 12 30 00 tai sitä myöhempi. Toisin sanoen kaikki tietueet paitsi ne, joiden päivämäärä sijoittuu välille 12 15 00 ja 12 29 00 kyseiset päivät mukaan lukien.|

Voit käyttää päivämääräalueiden suodattimissa mitä tahansa sallittua muotoa. Jos esimerkiksi päivämäärän ja ajan kentässä käytetään arvoa ma14 3..t 4j, tuloksena on suodatin, joka käsittää aikavälin kuluvan käsittelypäivämäärän vuoden viikon 14 maanantaista kello 3:00 kuluvaan päivään kello 16:00 kyseiset ajankohdat mukaan lukien.

## Päivämääräkaavojen käyttäminen

Päivämäärän kaava on lyhyt kirjain- ja numeroyhdistelmä, joka kertoo ohjelmalle, miten päivämäärät lasketaan. Voit syöttää päivämääräkaavat erilaisiin päivämäärien laskentakenttiin ja suodattimiin.

> [!NOTE]
> Kaikissa tietokaavakentissä yksi päivä sisällytetään automaattisesti edustamaan kuluvaa päivää kauden alkupäivänä. Jos siis syötät arvoksi esimerkiksi 1K, kausi on kahdeksan päivää, koska tämä päivä lasketaan mukaan. Määritä seitsemän päivän kausi \(yksi kokonainen viikko\) sisältäen alkamispäivämäärän ja syötä sitten 6P tai 1K-1P.

Seuraavassa on joitakin esimerkkejä päivämäärän kaavojen käytöstä:

- Toistuvien päiväkirjojen toistotiheys-kentän päivämäärän kaava määrittää, kuinka usein päiväkirjan rivin tapahtuma kirjataan.

- **Ylityskausi**-kentän tietyn tason muistutusta koskeva päivämäärän kaava määrittelee ajanjakson, joka täytyy kulua eräpäivästä \(tai edellisen muistutuksen päivämäärästä\), ennen kuin muistutus voidaan luoda.

- **Eräpäivän laskenta** -kentän kaava määrittää, miten ohjelma laskee muistutuksen eräpäivän.

Päivämäärän kaavassa voi olla enintään 20 merkkiä, sekä numeroita että kirjaimia. Voit käyttää seuraavia kirjaimia, jotka ovat kalenteriyksiköiden lyhenteitä:

|  Kirjain  |  Merkitys  |
|----------|----------------------|
|N|Nykyinen|
|P|Päivä\(päivät\)|
|VI|Viikko\(viikot\)|
|K|Kuukausi\(kuukaudet\)|
|Q |Vuosineljännes\(vuosineljännekset\)|
|V|Vuosi\(vuodet\)|

Voit rakentaa päivämääräkaavan kolmella eri tavalla:

Seuraava esimerkki näyttää, miten käytetään kirjainta N (nykyinen) ja aikayksikköä.

|  Lauseke  |  Merkitys  |
|--------------|-----------|
|NVI|Nykyinen viikko|
|KK|Nykyinen kuukausi (kuukauden viimeinen päivä)|

Seuraava esimerkki näyttää, miten käytetään numeroa ja aikayksikköä. Numero ei voi olla suurempi kuin 9999.

|  Lauseke  |  Merkitys  |
|--------------|-----------|
|10P|10 päivää tästä päivästä|
|2VI|2 viikkoa tämän päivän jälkeen|

Seuraava esimerkki näyttää, miten käytetään aikayksikköä ja numeroa.

|  Lauseke  |  Merkitys  |
|--------------|-----------|
|P10|Kuukauden seuraava 10. päivä|
|VIP4|Viikon seuraava 4. päivä \(torstai\)|

Seuraavassa esimerkissä näytetään, miten voit yhdistää nämä kolme eri muotoa tarvittaessa:

|  Lauseke  |  Merkitys  |
|--------------|-----------|
|NK+10P|Nykyinen kuukausi \+ 10 päivää|

Miinus-merkin avulla pystyt ilmaisemaan menneitä päiviä. Esimerkiksi:

|  Lauseke  |  Merkitys  |
|--------------|-----------|
|-1 V.|1 vuosi taaksepäin tästä päivästä|

> [!IMPORTANT]
> Jos sijainti käyttää peruskalenteria, sitten päivämääräkaava, jonka annat esimerkiksi **Toimitusaika** -kenttään, tulkitaan kalenterin mukaan työskentelypäiviksi. Esimerkiksi 1K tarkoittaa seitsemää käsittelypäivää.
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list.](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Use Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
> In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

- The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

- The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

- The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
> If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## Aikojen syöttäminen

Kun syötät aikoja, voit lisätä minkä tahansa erotinmerkin, paitsi välilyönnin yksiköiden väliin. Jos käytät kullekin yksikölle kaksinumeroisia merkkejä aina millisekunteihin saakka, sitä ei edellytetä.

Sinun on vain kirjoitettava suurimmat vaaditut yksiköt. Muiden arvoksi määritetään nolla. Voit myös jättää mahdollisen AM/PM-osoittimen pois.

Seuraavassa taulukossa on luettelo eri tavoista, joilla aikoja voi syöttää ja miten niitä tulkitaan: Oletusarvo on, että alueasetuksissa ajan muotoilu on **tunnit:minuutit:sekunnit:millisekunnit** ja asetuksissa käytetään vastaavasti AM- ja PM-osoittimia.

|**Tapahtuma**      |**Tulkinta**      |
|---------------|------------------------|
|05:23:17|05:23:17|
|5|05:00:00|
|5AM|05:00:00|
|5P|17:00:00|
|12|12:00:00|
|12A|00:00:00|
|12P|12:00:00|
|17|17:00:00|
|5:30|05:30:00|
|0530|05:30:00|
|5:30:5 |05:30:05|
|053005 |05:30:05|
|5:30:5,50|05:30:05.5|
|053005050 |05:30:05.05 |

> [!NOTE]
> Millisekunnit tulkitaan desimaalimuodoksi. Esimerkiksi 3, 30 ja 300 merkitsevät 300 millisekuntia, kun taas 03 tarkoittaa 30 ja 003 tarkoittaa 3 millisekuntia.

> [!IMPORTANT]
> Et voi käyttää arvoa 24:00, jos tarkoitat keskiyötä, etkä mitään arvoa, joka on suurempi kuin 24:00.

Aika-sana [!INCLUDE[prod_short](includes/prod_long.md)] -sovelluksen käyttämällä kielellä arvioidaan tietokoneen tai mobiililaitteen nykyiseksi ajaksi. Voit syöttää sanan minkä tahansa alkuosan, kuten a tai AIK.

## Yhdistettyjen päivämäärien ja aikojen syöttäminen

[!INCLUDE [datetimes](includes/datetimes.md)]

## Keston syöttäminen

Sovelluksen jotkin kentät edustavat kestoa tai kuluneen ajan määrää tietyn päivämäärän tai ajan sijaan. Kesto syötetään numerona, jota seuraa sen mittayksikkö.

Seuraavassa on muutamia esimerkkejä:

|**Kesto**|**Mittayksikkö**|
|------------|-------------------|
|2t|2 tuntia|
|6t 30 m|6 tuntia 30 minuuttia|
|6,5t|6 tuntia 30 minuuttia|
|90 m|1 tunti 30 minuuttia|
|2p 6t 30m|2 päivää 6 tuntia 30 minuuttia|
|2p 6t 30m 56s 600ms|2 päivää 6 tuntia 30 minuuttia 56 sekuntia 600 tuhannesosasekuntia|

Voit syöttää myös numeron, jonka ohjelma muuntaa automaattisesti kestoksi. Syöttämäsi numero muunnetaan kestokenttään määritellyn oletusmittayksikön mukaisesti.

Jos haluat nähdä, mitä mittayksikköä kesto-kentässä käytetään, syötä numero. Sen jälkeen voit nähdä, mihin mittayksikköön se on muunnettu.

Jos mittayksikkö on esimerkiksi Tunnit, numero 5 muunnetaan 5 tunniksi.

## Katso myös

[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)  
[Ostojen päivämäärien laskeminen](purchasing-date-calculation-for-purchases.md)  
[Ehtojen antaminen suodattimiin](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
