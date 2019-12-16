---
title: Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen | Microsoft Docs
description: Voit tehostaa luetteloiden käsittelemistä hakemalla tietoja, lajittelemalla sarakkeita ja tarkentamalla tuloksia tehokkaiden suodatussymboleiden ja pikanäppäinten avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 412c354313e571969c3ab7aa87210ff432ae0e91
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882180"
---
# <a name="sorting-searching-and-filtering"></a>Lajitteleminen, hakeminen ja suodattaminen
Luettelossa, raportissa tai XMLportissa olevien tietueiden skannaamista, etsimistä ja rajaamista voi helpottaa muutamilla keinoilla. Näitä keinoja ovat esimerkiksi lajitteleminen, etsiminen ja suodattaminen. Voit käyttää samanaikaisesti joitakin keinoja tai kaikkia keinoja, kun haluat etsiä tai analysoida tiedot nopeasti.

Raporteissa ja XMLporteissa suodattimet voidaan määrittää luetteloiden tavoin rajoittamaan raporttiin tai XMLportiin sisällytettäviä tietoja, mutta lajittelu ja haku ei ole mahdollista.

> [!TIP]
> Kun tarkastelet tietoja ruutuina, voit hakea tietoja ja käyttää perussuodatusta. Jos haluat käyttää lajittelun, haun ja suodattamisen tehokkaita toimintoja, valitse ![Näytä luettelona](media/ui_show_as_list_icon.png "Näytä luettelona – nuoli vasemmalle") -kuvake, jolloin tietueita voidaan tarkastella luettelona.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Lajittelu
Lajittelun avulla tiedoista saa nopeasti ja kätevästi yleiskuvan. Jos asiakkaita on useita, saat tarvitsemasi yleiskuvan lajittelemalla heidät esimerkiksi **Asiakasnro**-, **Asiakkaan kirjausryhmä**-, **Valuuttakoodi**-, **Maa-/aluekoodi**- tai **ALV-rekisteröintinro**-kohdan avulla,

Voit lajitella luettelon joko valitsemalla sarakkeen otsikkotekstin ja vaihtelemalla nousevaa ja laskevaa lajittelua tai valitsemalla sarakeotsikossa olevilla valintanuolilla **Nouseva**- tai **Laskeva**-toiminnon.  

> [!NOTE]  
>   Lajittelua ei tueta kuvissa, BLOB-kentissä ja FlowFilter-suodattimissa, jotka eivät kuulu taulukkoon.  

## <a name="searching"></a>Hakeminen
<!--## Searching by using the Quick Filter -->
Kunkin luettelosivun yläosassa on ![Hakuluettelon](media/ui-search/search-list.png "Hakuluettelon kuvake") **Haku**-toiminto, jonka avulla luettelon tietueiden määrää on helppo vähentää. Näin näkyvissä ovat vain tietueet, jotka sisältävät käyttäjää kiinnostavia tietoja.

Voit aloittaa haun kätevästi valitsemalla **Haku**-toiminnon ja kirjoittamalla ruutuun tekstin, jota haetaan. Voit syöttää kirjaimia, numeroita ja muita symboleita.

### <a name="fine-tuning-the-search"></a>Haun Hienosäätö
Yleensä haussa yritetään hakea vastaavuuksia kaikista kentistä. Haussa ei erotella pieniä ja isoja kirjaimia (eli kirjainkoolla ei ole merkitystä) ja haussa otetaan huomioon kentän kaikissa kohdissa (alussa, lopussa tai keskellä) oleva teksti.

Voit kuitenkin tarkentaa hakua erikoismerkkien avulla.

- Jos haluat etsiä vain ne kenttien arvot, jotka vastaavat koko tekstiä ja kirjainkokoa, aseta haettava teksti yksinkertaisten lainausmerkkien sisään (`''`, esimerkiksi `'man'`).

- Jos haluat etsiä arvoja, joiden alussa on tietty teksti ja jotka vastaavat tiettyä kirjainkokoa, aseta `*`-merkki hakutekstin jälkeen (esimerkiksi `man*`).

- Jos haluat etsiä arvoja, joiden lopussa on tietty teksti, ja jotka vastaavat tiettyä kirjainkokoa, aseta `*`-merkki hakutekstin eteen (esimerkiksi `*man`).

- Kun käytössä on `''` tai `*`, kirjainkoolla ei ole merkitystä haussa. Jos haluat, että kirjainkoolla ei ole merkitystä haussa, aseta `@`-merkki ennen hakutekstiä (esimerkiksi `@man*`).

Seuraavassa taulukossa on esimerkkejä haun käyttämisestä.

|Hakuehdot|Etsii...|
|---------------|----------|
|`man`<br />tai <br />`Man`|Kaikki tietueet, joissa on **man**-tekstin sisältäviä kenttiä kirjankoosta riippumatta. Esimerkiksi **Manchester**, **manual** tai **Sportsman**. |
|`'Man'`|Kaikki tietueet, joissa on vain **Man**-tekstin sisältäviä kenttiä. Kirjainkoko on merkitsevä.|
|`Man*`|Kaikki tietueet, joissa on <b>Man</b>-tekstillä alkavia kenttiä. Kirjainkoko on merkitsevä. Esimerkiksi **Manchester**, mutta ei **manual** tai **Sportsman**.|
|`@Man*`|Kaikki tietueet, joissa on **man**-tekstillä alkavia kenttiä kirjainkoosta riippumatta. Esimerkiksi **Manchester** ja **manual**, mutta ei **Sportsman**.|
|`@*man`|Kaikki tietueet, joissa on **man**-tekstiin päättyviä kenttiä kirjainkoosta riippumatta. Esimerkiksi **Sportsman**, mutta ei **Manchester** tai **manual**.|

> [!TIP]
> Voit aktivoida hakuruudun ja poistaa aktivoinnin painamalla **F3**-näppäintä. Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).

## <a name="Filtering"> </a>Suodattaminen
Suodattaminen sisältää kehittyneitä ja monipuolisia toimintoja, joiden avulla määritetään luettelossa näkyvät tai raporttiin tai XMLportiin sisällytettävät tietueet. Hakemisella ja suodattamisella on kaksi pääeroa, jotka kerrotaan alla olevassa taulukossa.

|| **Hakeminen** | **Suodattaminen** |
|--|----------|------------|
| **Käytettävissä olevat kentät** | Hakee kaikista sivulla näkyvistä kentistä. | Suodattaa taulukon minkä tahansa kentän tai useita kenttiä mukaan lukien kentät, jotka eivät näy sivulla. |
| **Kohdistus** | Näyttää tietueet, joiden kentät vastaavat hakutekstiä tekstin kirjainkoosta tai sijoittelusta riippumatta. | Näyttää tietueet, joiden kentät vastaavat suodatinta täysin. Kirjainkoko on merkitsevä, jos erityisiä suodatussymboleita ei ole annettu.

Suodattaminen mahdollistaa tiettyjen tilien tai asiakkaiden, päivämäärien, summien ja muiden tietojen tietueiden näyttämisen suodatusehtojen määrittämisen avulla. Vain määritettyjä ehtoja vastaavat tietueet näytetään luettelossa tai sisällytetään raporttiin, erätyöhön tai XMLportiin. Jos määrität ehtoja usealle kentälle, vain kaikkia ehtoja vastaavat tietueet näytetään.

Luetteloiden suodattimet näkyvät suodatinruudussa luettelon vasemmalla puolella, kun se aktivoidaan. Raporttien, erätöiden ja XMLportien suodattimet näkyvät suoraan pyyntösivulla.

### <a name="filtering-with-option-fields"></a>Vaihtoehtokenttien käyttäminen suodattamiseen
Tavallisissa tietoja, määrityspäivämäärän tai liiketoimintatietoja sisältävissä kentissä suodattimia voi määrittää sekä valitsemalla tietoja ja kirjoittamalla suodatinarvoja. Suodatusehtoja voi lisäksi tarkentaa symbolien avulla. Lisätietoja on kohdassa [Suodatusehtojen antaminen](ui-enter-criteria-filters.md#entering-filter-criteria).

**Vaihtoehto**-tyyppisissä kentissä suodatin voidaan kuitenkin määrittää vain valitsemalla yhden vaihtoehdon tai useita vaihtoehtoja avattavasta käytettävissä olevien vaihtoehtojen luettelosta. Esimerkki vaihtoehtokentästä on **Myyntitilaukset**-sivun **Tila**-kenttä.

> [!NOTE]
> Jos valitset suodatusarvoksi useita vaihtoehtoja, vaihtoehtojen välille määritetään *TAI*-suhde. Jos valitset esimerkiksi sekä **Avoin**- ja **Vapautettu**-valintaruudun **Tila**-suodatuskentän **Myyntitilaukset**-sivulla, silloin näytetään myyntitilaukset, jotka ovat joko avoimia tai vapautettuja.

### <a name="setting-filters-on-lists"></a>Suodattimien määrittäminen luetteloissa
Luetteloiden suodattimet määritetään suodatinruudussa. Avaa luettelon suodatinruutu valitsemalla sivun nimen vieressä oleva avattavan luettelon nuoli ja valitse sitten **Näytä suodatinruutu** -toiminto. Vaihtoehtoisesti voit painaa näppäinyhdistelmää **Vaihto+F3**.

Avaa luettelon sarakkeen suodatinruutu valitsemalla avattavan luettelon nuoli ja valitse sitten **Suodatus**-toiminto. Vaihtoehtoisesti voit painaa näppäinyhdistelmää **Vaihto+F3**. Valittu sarake näkyy avautuvassa suodatinruudussa suodatuskenttänä **Luettelon suodatusperuste** -osana.

Suodatinruudussa näkyvät luettelon nykyiset suodattimet. Sen avulla voi määrittää omia suodattimia yhdelle tai usealle kentälle **+ Suodatus** -toiminnolla.

 Suodatinruutu on jaettu kolmeen osaan: **Näkymät**, **Luettelon suodatusperuste** ja **Kokonaisarvojen suodatusperuste**:

- **Näkymät**

  Joissakin luetteloissa on **Näkymät**-osa. Näkymät ovat luettelon muunnoksia, jotka on esimääritetty suodattimien kanssa. Voit määrittää tallentaa kuhunkin luetteloon haluamasi määrän näkymiä, ja voit käyttää näitä näkymiä riippumatta siitä, millä laitteella kirjaudut sisään. Lisätietoja on kohdassa [Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md).

- **Luettelon suodatusperuste**

  Tässä osassa lisätään suodattimet tietyille kentille ja vähennetään näin näytettävien tietueiden määrää. Lisää suodatin valitsemalla **+ Suodatus** -toiminto, kirjoittamalla luettelon suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.

- **Kokonaisarvojen suodatusperuste**

  Jotkin laskettuja kenttiä, kuten summia ja määriä, näyttävät luettelot sisältävät **Kokonaisarvojen suodatusperuste** -osan. Siinä voi muokata erilaisia laskelmiin vaikuttavia dimensioita. Lisää suodatin valitsemalla **+ Suodatus** -toiminto, kirjoittamalla luettelon suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.

  > [!NOTE]
  > FlowFilter-suodattimet ohjaavat **Kokonaisarvojen suodatusperuste** -osan suodattimia sivun rakenteessa. Teknisiä lisätietoja on kohdassa [FlowFilter-suodattimet](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

Voit määrittää yksinkertaisen suodattimen suoraan luettelossa käyttämällä suodatinruutua. Tällainen suodatin näyttää vain tietueet, joilla on sama arvo kuin valitussa solussa. Valitse solu luettelossa valitsemalla ensin avattavan luettelon nuoli ja sitten **Suodata tähän arvoon** -toiminto. Vaihtoehtoisesti voit painaa näppäinyhdistelmää **Alt+F3**.

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a>Raporttien, erätöiden ja XMLportien suodattimien määrittäminen
Raporttien ja XMLportien suodattimet näkyvät suoraan pyyntösivulla. Viimeksi käytetyt suodattimet näkyvät pyyntösivulla **Käytä oletusarvoja kohteesta:** -kentän valinnan mukaisesti. Lisätietoja on kohdassa [Tallennettujen asetusten käyttäminen](ui-work-report.md#SavedSettings).

**Suodatuksen** pääosassa näkyy oletussuodatuskentät, joilla rajoitetaan raporttiin tai XMLportiin sisällytettäviä tietueita. Lisää suodatin valitsemalla **+ Suodatus** -toiminto, kirjoittamalla suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.

Voit säätää **Kokonaisarvojen suodatusperuste** -osassa erilaisia dimensioita, jotka vaikuttavat raportin tai XMLportin laskelmiin. Lisää suodatin valitsemalla **+ Suodatus** -toiminto, kirjoittamalla suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.

## <a name="entering-filter-criteria"></a>Suodatusehtojen antaminen
Voit antaa suodatinruudussa ja pyyntösivulla suodatusehdot suodatuskentän ruudussa.

Suodatettavan kentän tyyppi määrittää, millaisia ehtoja voi antaa. Jos esimerkiksi suodatetaan kenttä, jossa on kiinteitä arvoja, valittavissa on vain nämä arvot. Lisätietoja erityisistä suodatussymboleista on kohdissa [Suodatusehdot](#FilterCriteria) ja [Suodatuksen tunnukset](#FilterTokens).

Sarakkeet, joilla on jo suodattimia, löytyvät, kun käytössä on sarakeotsikon ![Suodatus-kuvake](media/ui-search/filter-icon.png "Suodatin-kuvake"). Voit poistaa suodattimen valitsemalla avattavan luettelon nuolen ja valitsemalla sitten **Tyhjennä suodatin** -toiminnon.

> [!TIP]
> Nopeuta tietojen etsimistä ja analysoimista pikanäppäinyhdistelmien avulla. Voit esimerkiksi valita kentän ja lisätä kentän suodatinruutuun **Vaihto+Alt+F3**-pikanäppäinten avulla, kirjoittaa suodatinehdot ja palata riveille **Ctrl+Enter**-pikanäppäinten avulla. Valitse toinen kenttä ja suodata sen arvot **Alt+F3**-pikanäppäimillä. Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).

### <a name="FilterCriteria"> </a>Suodatusehdot ja merkit
Kun syötät kriteerejä, voit käyttää kaikkia numeroita ja kirjaimia, joita voi yleensäkin käyttää kentässä. Voit käyttää tulosten suodatukseen myös erikoismerkkejä (tai operaattoreita). Seuraavassa taulukossa on esitelty symbolit, joita voi käyttää suodattimissa. Lisätietoja päivämääristä ja ajoista on myös kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

> [!IMPORTANT]  
>  Joissakin tilanteissa kentät arvot voivat sisältää näitä merkkejä, ja haluat suodattaa niiden avulla. Siinä tapauksessa on merkki on lisättävä suodatuslausekkeeseen lainausmerkeissä (”). Jos haluat esimerkiksi suodattaa tietueita, joiden alussa on teksti *S&R*, suodatuslauseke on `'S&R*'`.

Seuraavissa osissa käsitellään eri operaattoreiden käyttöä.

> [!NOTE]
> Jos yhdessä suodattimessa on yli 200 operaattoria, järjestelmä ryhmittää jotkin lausekkeet sulkeisiin `()` käsittelyä varten. Se ei vaikuta suodattimeen eikä tuloksiin.  

#### <a name="-interval"></a>(..) väli

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`1100..2100`|Numerot 1100 - 2100|  
|`..2500`|Numeroon 2500 asti, 2500 mukaan lukien|  
|`..12 31 00`|Päivämäärät 31.12.00 asti, kyseinen päivämäärä mukaan lukien|  
|`P8..`|Tiedot kirjanpitojaksosta 8 ja siitä eteenpäin|  
|`..23`|Alkupäivämäärästä lähtien päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59|  
|`23..`|Päivästä 23 nykyistä kuukautta nykyistä vuotta klo 00:00:00 ajan loppuun asti|  
|`22..23`|Päivästä 22 nykyistä kuukautta nykyistä vuotta klo 0:00:00 päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59|  

#### <a name="124-eitheror"></a>(&#124;) Joko/tai

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`1200|1300`|Numerot, joissa on 1200 tai 1300|  

#### <a name="-not-equal-to"></a>(<>) ei ole sama kuin  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`<>0`|Kaikki numerot paitsi 0<br /><br /> SQL Server -vaihtoehto sallii tämän symbolin yhdistämisen yleismerkkihakuun. Esimerkiksi: <>A* - ei teksti, joka alkaa kirjaimella A.|  

#### <a name="-greater-than"></a>(>) suurempi kuin  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`>1200`|Numerot, jotka ovat suurempia kuin 1200|  

#### <a name="-greater-than-or-equal-to"></a>(>=) Suurempi tai yhtä suuri  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`>=1200`|Numerot, jotka ovat suurempia tai yhtä suuria kuin 1200|  

#### <a name="-less-than"></a>(<) pienempi kuin  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`<1200`|Numerot, jotka ovat pienempiä kuin 1200|  

#### <a name="-less-than-or-equal-to"></a>(<=) Pienempi tai yhtä suuri  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`<=1200`|Numerot, jotka ovat pienempiä tai yhtä suuria kuin 1200|  

#### <a name="-and"></a>(&) ja  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`>200&<1200`|Luvut, jotka ovat suurempia kuin 200 ja pienempiä kuin 1200.|  

#### <a name="-an-exact-character-match"></a>('') Tarkka merkin vastine  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`'man'`|Teksti, joka vastaa täysin "man"ia ja jossa isoilla ja pienillä kirjaimilla on merkitystä.|  

#### <a name="-case-insensitive"></a>(@) Ei kirjainkokoon perustuva  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`@man*`|Teksti, joka alkaa "man" ja jossa isoilla ja pienillä kirjaimilla ei ole merkitystä.|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Rajoittamaton määrä tuntemattomia merkkejä

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`*Co*`|Teksti, joka sisältyy ”Co” ja jossa kirjainkoolla on merkitystä.|  
|`*Co`|Teksti, jonka lopussa on ”Co” ja jossa kirjainkoolla on merkitystä.|  
|`Co*`|Teksti, jonka alussa on ”Co” ja jossa kirjainkoolla on merkitystä.|  

#### <a name="-one-unknown-character"></a>(?) yksi tuntematon merkki  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`Hans?n`|Teksti, kuten Hansen tai Hanson|  

#### <a name="combined-format-expressions"></a>Yhdistetyn muodon lausekkeet  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Sisällytä kaikki tietueet, joissa on numero 5999 tai numero väliltä 8100 ja 8490.|  
|`..1299|1400..`|Sisällytä tietueet, joissa on numero, joka on pienempi tai yhtä suuri kuin 1299 tai suurempi tai yhtä suuri kuin 1400 (siis kaikki muut numerot paitsi 1300–1399).|  
|`>50&<100`|Sisällytä tietueet, joissa on numero, joka on suurempi kuin 50 ja pienempi kuin 100 (siis numerot 51–99).|  

### <a name="FilterTokens"> </a>Suodatuksen tunnukset
Kun syötät suodatusehtoja, voit kirjoittaa myös sanoja, joilla on erityinen tarkoitus. Niitä kutsutaan suodatuksen tunnuksiksi. Kun olet syöttänyt tunnussanan, sana korvataan arvolla tai arvoilla, joita se edustaa. Tämä helpottaa suodattamista ja vähentää muille sivuille siirtymistä ja suodattimeen lisättävien arvojen etsimistä. Taulukossa on joitakin tunnuksia, joita voit käyttää suodatusehtoina.

> [!TIP]
> Organisaatio voi käyttää mukautettuja tunnuksia. Järjestelmänvalvojalta saa lisätietoja käytettävissä olevista tunnuksista ja mukautettujen tunnusten lisäämisestä. Teknisiä tietoja on kohdassa [Suodatuksen tunnusten lisääminen](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### <a name="me-or-userid-records-assigned-to-you"></a>(%me tai %userid) Sinulle määritetyt tietueet

Käytä `%me`- tai `%userid`-tunnusta suodattaessasi kenttiä, jotka sisältävät käyttäjätunnuksen. Tällainen kenttä on esimerkiksi **Liitetty käyttäjätunnukseen**, jossa näytetään kaikki käyttäjälle liitetyt kentät.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%me`<br />tai<br />`%userid`|Tietueet, jotka on liitetty käyttäjätiliisi. |  

#### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Omat asiakkaat -kohdan asiakkaat

Käytä `%mycustomers`-tunnusta asiakkaan **Nro**-kentässä, kun haluat näyttää asiakkaan kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat asiakkaat** -luetteloon.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%mycustomers`|Roolikeskuksen **Omat asiakkaat** -kohdan asiakkaat. |  

#### <a name="myitems-items-in-my-items"></a>(%myitems) Omat nimikkeet -kohdan nimikkeet

Käytä `%myitems`-tunnusta nimikkeen **Nro**-kentässä, kun haluat näyttää nimikkeiden kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat nimikkeet** -luetteloon.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%myitems`|Roolikeskuksen **Omat nimikkeet** -kohdan nimikkeet. |  

#### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Omat toimittajat -kohdan toimittajat

Käytä `%myvendors`-tunnusta toimittajan **Nro**-kentässä, kun haluat näyttää toimittajien kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat toimittajat** -luetteloon.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%myvendors`|Roolikeskuksen **Omat toimittajat** -kohdan toimittajat. |  

## <a name="see-also"></a>Katso myös
[Usein kysyttyjen kysymysten haku ja suodatus](ui-search-filter-faq.md)  
[Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
