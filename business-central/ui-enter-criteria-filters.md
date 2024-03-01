---
title: Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen
description: 'Voit tehostaa luetteloiden käsittelemistä hakemalla tietoja, lajittelemalla sarakkeita ja tarkentamalla tuloksia suodatussymboleiden ja pikanäppäinten avulla.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'delimit, FlowFilter, totals, limit, advanced'
ms.search.form: null
ms.date: 10/30/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Lajitteleminen, hakeminen ja suodattaminen

Luettelossa, raportissa tai XMLportissa olevien tietueiden skannaamista, etsimistä ja rajaamista voi helpottaa muutamilla keinoilla. Näitä keinoja ovat esimerkiksi lajitteleminen, etsiminen ja suodattaminen. Voit käyttää samanaikaisesti joitakin keinoja tai kaikkia keinoja, kun haluat etsiä tai analysoida tiedot nopeasti.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Raporteissa ja XMLporteissa suodattimet voidaan määrittää luetteloiden tavoin rajoittamaan raporttiin tai XMLportiin sisällytettäviä tietoja, mutta lajittelu ja haku ei ole mahdollista.

> [!TIP]
> Kun tarkastelet tietoja ruutuina, voit hakea tietoja ja käyttää suodatusta. Jos haluat käyttää lajittelun, haun ja suodattamisen tehokkaita toimintoja, valitse ![Näytä luettelona.](media/ui_show_as_list_icon.png "Näytä luettelona – nuoli vasemmalle") -kuvake, jos haluat tarkastella tietueita luettelona.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## Lajittelu

Lajittelun avulla tiedoista saa nopeasti ja kätevästi yleiskuvan. Jos esimerkiksi asiakkaita on useita, saat tarvitsemasi yleiskuvan lajittelemalla heidät esimerkiksi **Asiakasnro**-, **Valuuttakoodi**- tai **Maa-/aluekoodi** -kohdan avulla.

Voit lajitella luettelon seuraavasti:

- Valitse sarakkeen otsikkoteksti, mikä vaihtaa nousevan ja laskevan järjestyksen välillä.
- Valitse sarakeotsikossa avattava nuoli ja valitse **Nouseva** tai **Laskeva**-toiminto.  

> [!NOTE]  
> Lajittelua ei tueta kuvissa, BLOB-kentissä ja FlowFilter-suodattimissa, jotka eivät kuulu taulukkoon.  

## Hakeminen

<!--## Searching by using the Quick Filter -->
Jokaisen luettelosivun yläosassa on ![Hakuluettelo.](media/ui-search/search-list.png "Hakuluettelon kuvake") **Haku**-toiminto, jonka avulla luettelon tietueiden määrää on helppo vähentää. Näin näkyvissä ovat vain tietueet, jotka sisältävät käyttäjää kiinnostavia tietoja.

Voit aloittaa haun valitsemalla **Haku**-toiminnon ja kirjoittamalla ruutuun tekstin, jota haetaan. Voit syöttää kirjaimia, numeroita ja muita symboleita.

Yleensä haussa yritetään hakea vastaavuuksia kaikista kentistä. Haussa ei erotella pieniä ja isoja kirjaimia (eli kirjainkoolla ei ole merkitystä) ja haussa otetaan huomioon kentän kaikissa kohdissa (alussa, lopussa tai keskellä) oleva teksti.

> [!TIP]
> Voit aktivoida hakuruudun ja poistaa aktivoinnin <kbd>F3</kbd>-näppäimellä. Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).

> [!NOTE]  
> Hakua ei vastaa kuvien, BLOB-, FlowFilters-, FlowFields- ja muiden taulukon ulkopuolisten kenttien arvoja.


### Haun hienosäätäminen suodatusehdoilla

Voit tehdä täsmällisemään haun käyttämällä suodatusoperaattoreita, lausekkeita ja suodatustunnuksia. Toisin kuin suodattaminen, niitä käytetään kaikissa kentissä, kun niitä käytetään hakuruudussa, jolloin ne eivät ole yhtä tehokkaita kuin suodattaminen.

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


## <a name="filtering"></a>Suodattaminen

Suodattaminen sisältää kehittyneitä ja monipuolisia toimintoja, joiden avulla määritetään luetteloon, raporttiin tai XMLportiin sisällytettävät tietueet. Hakemisella ja suodattamisella on kaksi pääeroa, jotka kerrotaan alla olevassa taulukossa.

|| **Hakeminen** | **Suodattaminen** |
|--|----------|------------|
| **Käytettävissä olevat kentät** | Hakee kaikista sivulla näkyvistä kentistä. | Suodattaa taulukon minkä tahansa kentän tai useita kenttiä mukaan lukien kentät, jotka eivät näy sivulla. |
| **Kohdistus** | Näyttää tietueet, joiden kentät vastaavat hakutekstiä tekstin kirjainkoosta tai sijoittelusta riippumatta. | Näyttää tietueet, joiden kentät vastaavat suodatinta täysin. Kirjainkoko on merkitsevä, jos erityisiä suodatussymboleita ei ole annettu.

Suodattaminen mahdollistaa tiettyjen tilien tai asiakkaiden, päivämäärien, summien ja muiden tietojen tietueiden näyttämisen suodatusehtojen määrittämisen avulla. Vain määritettyjä ehtoja vastaavat tietueet näytetään luettelossa tai sisällytetään raporttiin, erätyöhön tai XMLportiin. Jos määrität ehtoja usealle kentälle, vain kaikkia ehtoja vastaavat tietueet näytetään.

Luetteloiden suodattimet näkyvät suodatinruudussa luettelon vasemmalla puolella, kun se aktivoidaan. Raporttien, erätöiden ja XMLportien suodattimet näkyvät suoraan pyyntösivulla.

### Vaihtoehtokenttien käyttäminen suodattamiseen

Tavallisissa tietoja, määrityspäivämäärän tai liiketoimintatietoja sisältävissä kentissä suodattimia voi määrittää sekä valitsemalla tietoja ja kirjoittamalla suodatinarvoja. Suodatusehtoja voi lisäksi tarkentaa symbolien avulla. Lisätietoja on kohdassa [Suodatusehtojen antaminen](ui-enter-criteria-filters.md#entering-filter-criteria).

**Vaihtoehto**-tyyppisissä kentissä suodatin voidaan kuitenkin määrittää vain valitsemalla yhden vaihtoehdon tai useita vaihtoehtoja avattavasta käytettävissä olevien vaihtoehtojen luettelosta. Esimerkki vaihtoehtokentästä on **Myyntitilaukset**-sivun **Tila**-kenttä.

> [!NOTE]
> Jos valitset suodatusarvoksi useita vaihtoehtoja, vaihtoehtojen välille määritetään *TAI*-suhde. Jos valitset esimerkiksi sekä **Avoin**- ja **Vapautettu**-valintaruudun **Tila**-suodatuskentän **Myyntitilaukset**-sivulla, silloin näytetään myyntitilaukset, jotka ovat joko avoimia tai vapautettuja.

### Suodattimien määrittäminen luetteloissa

Luetteloiden suodattimet määritetään suodatinruudussa. Avaa luettelon suodatinruutu valitsemalla sivun nimen vieressä oleva avattavan luettelon nuoli ja valitse sitten **Näytä suodatinruutu** -toiminto. Vaihtoehtoisesti voit käyttää näppäinyhdistelmää <kbd>Vaihto</kbd>+<kbd>F3</kbd>.

Avaa luettelon sarakkeen suodatinruutu valitsemalla avattavan luettelon nuoli ja valitse sitten **Suodatus**-toiminto. Vaihtoehtoisesti voit käyttää näppäinyhdistelmää <kbd>Vaihto</kbd>+<kbd>F3</kbd>. Valittu sarake näkyy avautuvassa suodatinruudussa suodatuskenttänä **Luettelon suodatusperuste** -osana.

Suodatinruudussa näkyvät luettelon nykyiset suodattimet. Sen avulla voi määrittää omia suodattimia yhdelle tai usealle kentälle **+ Suodatus** -toiminnolla.

 Suodatinruutu on jaettu kolmeen osaan: **Näkymät**, **Luettelon suodatusperuste** ja **Kokonaisarvojen suodatusperuste**:

- **Näkymät**

  Joissakin luetteloissa on **Näkymät**-osa. Näkymät ovat luettelon muunnoksia, jotka on esimääritetty suodattimien kanssa. Voit määrittää ja tallentaa niin monta näkymää luetteloa kohti kuin haluat. Näkymät ovat käytettävissäsi kaikissa laitteissa, joihin kirjaudut. Lisätietoja on kohdassa [Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md).

- **Luettelon suodatusperuste**

  Tässä osassa lisätään suodattimet tietyille kentille ja vähennetään näin näytettävien tietueiden määrää. Lisää suodatin valitsemalla **+ Suodatin** -toiminto. Kirjoita sitten luettelon suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.

- **Kokonaisarvojen suodatusperuste**

  Jotkin laskettuja kenttiä, kuten summia ja määriä, näyttävät luettelot sisältävät **Kokonaisarvojen suodatusperuste** -osan. Siinä voi muokata erilaisia laskelmiin vaikuttavia dimensioita. Lisää suodatin valitsemalla **+ Suodatin** -toiminto. Kirjoita sitten luettelon suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.

  > [!NOTE]
  > FlowFilter-suodattimet ohjaavat **Kokonaisarvojen suodatusperuste** -osan suodattimia sivun rakenteessa. Teknisiä lisätietoja on kohdassa [FlowFilter-suodattimet](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

Voit määrittää yksinkertaisen suodattimen suoraan luettelossa käyttämällä suodatinruutua. Tällainen suodatin näyttää vain tietueet, joilla on sama arvo kuin valitussa solussa. Valitse solu luettelossa valitsemalla ensin avattavan luettelon nuoli ja sitten **Suodata tähän arvoon** -toiminto. Vaihtoehtoisesti voit käyttää näppäinyhdistelmää <kbd>Alt</kbd>+<kbd>F3</kbd>.

### Raporttien, erätöiden ja XMLportien suodattimien määrittäminen

Raporttien ja XMLportien suodattimet näkyvät suoraan pyyntösivulla. Viimeksi käytetyt suodattimet näkyvät pyyntösivulla **Käytä oletusarvoja kohteesta:** -kentän valinnan mukaisesti. Lisätietoja on kohdassa [Tallennettujen asetusten käyttäminen](ui-work-report.md#SavedSettings).

**Suodatuksen** pääosassa näkyy oletussuodatuskentät, joilla rajoitetaan raporttiin tai XMLportiin sisällytettäviä tietueita. Lisää suodatin valitsemalla **+ Suodatin** -toiminto. Kirjoita sitten suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.

Voit säätää **Kokonaisarvojen suodatusperuste** -osassa erilaisia dimensioita, jotka vaikuttavat raportin tai XMLportin laskelmiin. Lisää suodatin valitsemalla **+ Suodatin** -toiminto. Kirjoita sitten suodatusperusteena käytettävän kentän nimi tai valitsemalla kenttä avattavasta luettelosta.

## Suodatusehtojen antaminen

Voit antaa suodatinruudussa ja pyyntösivulla suodatusehdot suodatuskentän ruudussa.

Suodatettavan kentän tyyppi määrittää, millaisia ehtoja voi antaa. Jos esimerkiksi suodatetaan kenttä, jossa on kiinteitä arvoja, valittavissa on vain nämä arvot. Lisätietoja erityisistä suodatussymboleista on kohdissa [Suodatusehdot](#FilterCriteria) ja [Suodatuksen tunnukset](#FilterTokens).

Sarakkeita, joilla on jo suodattimia, ilmaisee ![Suodatin-kuvake.](media/ui-search/filter-icon.png "Suodatin-kuvake") -kuvake sarakeotsikossa. Voit poistaa suodattimen valitsemalla avattavan luettelon nuolen ja valitsemalla sitten **Tyhjennä suodatin** -toiminnon.

> [!TIP]
> Nopeuta tietojen etsimistä ja analysoimista pikanäppäinyhdistelmien avulla. Voit esimerkiksi valita kentän ja lisätä kentän suodatinruutuun näppäinyhdistelmällä <kbd>Vaihto</kbd>+<kbd>Alt</kbd>+<kbd>F3</kbd>, kirjoittaa suodatinehdot ja palata riveille näppäinyhdistelmällä <kbd>Ctrl</kbd>+<kbd>Enter</kbd>. Valitse toinen kenttä ja suodata sen arvot näppäinyhdistelmällä <kbd>Alt</kbd>+<kbd>F3</kbd>. Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).

### <a name="FilterCriteria"> </a>Suodatusehdot ja operaattorit

Kun syötät kriteerejä, voit käyttää kaikkia numeroita ja kirjaimia, joita voi yleensäkin käyttää kentässä. Mutta on olemassa myös joukko erikoismerkkejä, joita voit käyttää operaattoreina suodattaaksesi tuloksia edelleen. Seuraavissa osissa on kuvattu nämä symbolit ja niiden käyttö suodattimien operaattoreina.

> [!TIP]
> Lisätietoja päivämäärien ja aikojen suodatuksesta on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

> [!IMPORTANT]
> - Voi olla tilanteita, joissa suodatettava arvo sisältää symbolin, joka on operaattori. Lisätietoja näiden tilanteiden käsittelemiseksi on kohdassa [Symboleja sisältävien arvojen suodattaminen](#symbols).
>
> - Jos yhdessä suodattimessa on yli 200 operaattoria, järjestelmä ryhmittää jotkin lausekkeet sulkeisiin `()` käsittelyä varten. Se ei vaikuta suodattimeen eikä tuloksiin.  

#### (..) väli

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`1100..2100`|Numerot 1100 - 2100|  
|`..2500`|Numeroon 2500 asti, 2500 mukaan lukien|  
|`..12 31 00`|Päivämäärät 31.12.00 asti, kyseinen päivämäärä mukaan lukien|  
|`Bicycle..Car`| Merkkijonot B:stä C:hen, kun ne on järjestetty leksikografisesti|  
|`P8..`|Tiedot kirjanpitojaksosta 8 ja siitä eteenpäin|  
|`..23`|Alkupäivämäärästä lähtien päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59|  
|`23..`|Päivästä 23 nykyistä kuukautta nykyistä vuotta klo 00:00:00 ajan loppuun asti|  
|`22..23`|Päivästä 22 nykyistä kuukautta nykyistä vuotta klo 0:00:00 päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59| 

> [!TIP]
> Jos käytät numeronäppäimistöä, desimaalierotin voi tuottaa jonkin muun merkin kuin pisteen (.). Voit vaihtaa pisteeseen numeronäppäimistön näppäinyhdistelmällä <kbd>Alt</kbd>+<kbd>desimaalierotin</kbd>. Kun haluat vaihtaa takaisin, paina <kbd>Alt</kbd>+<kbd>desimaalierotin</kbd>-näppäimiä uudelleen. Lisätietoja on kohdassa [Numeeristen näppäimistöjen käyttämän desimaalierottimen asettaminen](ui-enter-data.md#decimal).

> [!NOTE]  
> Jos suodattamasi kenttä on tyyppiä Teksti, leksikografista järjestystä käytetään määrittämään, mitä väliin sisältyy. Tällaisten kenttien osalta, joita käytetään kokonaislukujen tallentamiseen, tämä voi johtaa (odottamattomaan) tulokseen, että suodatin kohdassa 10000..10042 sisältää myös arvot 100000 ja 1000042.

#### (&#124;) Joko/tai

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`1200|1300`|Numerot, joissa on 1200 tai 1300|  

#### (<>) ei ole sama kuin  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`<>0`|Kaikki numerot paitsi 0<br /><br /> SQL Server -vaihtoehto sallii tämän symbolin yhdistämisen yleismerkkihakuun. Esimerkiksi: <>A* - ei teksti, joka alkaa kirjaimella A.|  

#### (>) suurempi kuin  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`>1200`|Numerot, jotka ovat suurempia kuin 1200|  

#### (>=) Suurempi tai yhtä suuri  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`>=1200`|Numerot, jotka ovat suurempia tai yhtä suuria kuin 1200|  

#### (<) pienempi kuin  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`<1200`|Numerot, jotka ovat pienempiä kuin 1200|  

#### (<=) Pienempi tai yhtä suuri  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`<=1200`|Numerot, jotka ovat pienempiä tai yhtä suuria kuin 1200|  

#### (&) ja  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`>200&<1200`|Luvut, jotka ovat suurempia kuin 200 ja pienempiä kuin 1200.|  

#### ('') Tarkka merkin vastine  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`'man'`|Teksti, joka vastaa täysin merkkijonoa **man** ja jossa isoilla ja pienillä kirjaimilla on merkitystä.|  
|`''`|Tyhjä teksti.|  

#### (@) Ei kirjainkokoon perustuva  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`@man*`|Teksti, joka alkaa **man** ja jossa isoilla ja pienillä kirjaimilla ei ole merkitystä.|  

#### (*) Rajoittamaton määrä tuntemattomia merkkejä

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`*Co*`|Teksti, joka sisältää **Co** ja jossa kirjainkoolla on merkitystä.|  
|`*Co`|Teksti, jonka lopussa on **Co** ja jossa kirjainkoolla on merkitystä.|  
|`Co*`|Teksti, jonka alussa on **Co** ja jossa kirjainkoolla on merkitystä.|  

#### (?) yksi tuntematon merkki  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`Hans?n`|Teksti, kuten **Hansen** tai **Hanson**|  

#### Yhdistetyn muodon lausekkeet  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Sisällytä kaikki tietueet, joissa on numero 5999 tai numero väliltä 8100 ja 8490.|  
|`..1299|1400..`|Sisällytä tietueet, joissa on numero, joka on pienempi tai yhtä suuri kuin 1299 tai suurempi tai yhtä suuri kuin 1400 (siis kaikki muut numerot paitsi 1300–1399).|  
|`>50&<100`|Sisällytä tietueet, joissa on numero, joka on suurempi kuin 50 ja pienempi kuin 100 (siis numerot 51–99).|  

### <a name="symbols"></a>Symboleita sisältävien arvojen suodattaminen

Joissakin tapauksissa kenttäarvot sisältävät jonkin seuraavista symboleista:

- &
- (
- )
- =
- &#124;

Jos haluat suodattaa jonkin näistä symboleista, sijoita suodatinlauseke heittomerkkeihin (`'<expression with symbol>'`). Jos haluat esimerkiksi suodattaa tietueita, joiden alussa on teksti *J & V*, suodatuslauseke on `'J & V*'`.

Tämä vaatimus ei ole välttämätön muille symboleille.

### <a name="FilterTokens"> </a>Suodatuksen tunnukset

Kun syötät suodatusehtoja, voit kirjoittaa myös sanoja, joilla on erityinen tarkoitus. Niitä kutsutaan suodatuksen tunnuksiksi. Kun olet syöttänyt tunnussanan, sana korvataan arvolla tai arvoilla, joita se edustaa. Suodatuksen tunnukset helpottavat suodattamista ja vähentää muille sivuille siirtymistä ja suodattimeen lisättävien arvojen etsimistä. Taulukossa on joitakin tunnuksia, joita voit käyttää suodatusehtoina.

> [!TIP]
> Organisaatio voi käyttää mukautettuja tunnuksia. Järjestelmänvalvojalta saa lisätietoja käytettävissä olevista tunnuksista ja mukautettujen tunnusten lisäämisestä. Teknisiä tietoja on kohdassa [Suodatuksen tunnusten lisääminen](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### (%me tai %userid) Sinulle määritetyt tietueet

Käytä `%me`- tai `%userid`-tunnusta suodattaessasi kenttiä, jotka sisältävät käyttäjätunnuksen. Tällainen kenttä on esimerkiksi **Liitetty käyttäjätunnukseen**, jossa näytetään kaikki käyttäjälle liitetyt kentät.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%me`<br />tai<br />`%userid`|Tietueet, jotka on liitetty käyttäjätiliisi. |  

#### (%mycustomers) Omat asiakkaat -kohdan asiakkaat

Käytä `%mycustomers`-tunnusta asiakkaan **Nro**-kentässä, kun haluat näyttää asiakkaan kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat asiakkaat** -luetteloon.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%mycustomers`|Roolikeskuksen **Omat asiakkaat** -kohdan asiakkaat. |  

#### (%myitems) Omat nimikkeet -kohdan nimikkeet

Käytä `%myitems`-tunnusta nimikkeen **Nro**-kentässä, kun haluat näyttää nimikkeiden kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat nimikkeet** -luetteloon.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%myitems`|Roolikeskuksen **Omat nimikkeet** -kohdan nimikkeet. |  

#### (%myvendors) Omat toimittajat -kohdan toimittajat

Käytä `%myvendors`-tunnusta toimittajan **Nro**-kentässä, kun haluat näyttää toimittajien kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat toimittajat** -luetteloon.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%myvendors`|Roolikeskuksen **Omat toimittajat** -kohdan toimittajat. |  

## Katso myös

[Usein kysyttyjen kysymysten hakeminen ja suodattaminen](ui-search-filter-faq.yml)  
[Luettelonäkymien tallentaminen ja mukauttaminen](ui-views.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
