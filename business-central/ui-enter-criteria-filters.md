---
title: "Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen | Microsoft Docs"
description: "Voit tehostaa luetteloiden käsittelemistä hakemalla tietoja, lajittelemalla sarakkeita ja tarkentamalla tuloksia tehokkaiden suodatussymboleiden ja pikanäppäinten avulla."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: c6eb9465d07b702e545347cad5acf0a42f01d1de
ms.contentlocale: fi-fi
ms.lasthandoff: 01/22/2019

---
# <a name="sorting-searching-and-filtering-lists"></a>Luetteloiden lajitteleminen ja suodattaminen sekä luetteloista hakeminen
Luettelossa olevien tietueiden skannaamista, etsimistä ja rajaamista voi helpottaa muutamilla keinoilla. Näitä keinoja ovat esimerkiksi lajitteleminen, etsiminen ja suodattaminen. Voit käyttää samanaikaisesti joitakin keinoja tai kaikkia keinoja, kun haluat etsiä tai analysoida tiedot nopeasti.

> [!TIP]
> Kun tarkastelet tietoja ruutuina, voit hakea tietoja ja käyttää perussuodatusta. Jos haluat käyttää lajittelun, haun ja suodattamisen tehokkaita toimintoja, valitse ![Näytä luettelona](media/ui_show_as_list_icon.png "Näytä luettelona - vasen nuoli") -kuvake, jolloin ne näytetään luettelona.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Lajittelu
Lajittelun avulla tiedoista saa nopeasti ja kätevästi yleiskuvan. Jos asiakkaita on useita, saat tarvitsemasi yleiskuvan lajittelemalla heidät esimerkiksi **Asiakasnro**-, **Asiakkaan kirjausryhmä**-, **Valuuttakoodi**-, **Maa-/aluekoodi**- tai **ALV-rekisteröintinro**-kohdan avulla,

Voit lajitella luettelon joko valitsemalla sarakkeen otsikkotekstin ja vaihtelemalla nousevaa ja laskevaa lajittelua tai valitsemalla sarakeotsikossa olevilla pienillä nuolilla **Nouseva**- tai **Laskeva** -vaihtoehdon.  

> [!NOTE]  
>   Lajittelua ei tueta kuvissa, BLOB-kentissä ja FlowFilter-suodattimissa, jotka eivät kuulu taulukkoon.  

## <a name="searching"></a>Hakeminen
<!--## Searching by using the Quick Filter --> Kunkin luettelosivun yläosassa on ![Hakuluettelo](media/ui-search/search-list.png "Hakuluettelo-kuvake") **Haku**-kuvake, jonka avulla luettelon tietueiden määrää on helppo vähentää. Näin näkyvissä ovat vain tietueet, jotka sisältävät käyttäjää kiinnostavia tietoja.

Voit aloittaa haun yksinkertaisesti valitsemalla hakukuvakkeen ja kirjoittamalla ruutuun teksti, jota haetaan. Voit syöttää kirjaimia, numeroita ja muita symboleita.

### <a name="fine-tune-the-search"></a>Haun viimeisteleminen
Yleensä haussa yritetään hakea vastaavuuksia kaikista kentistä. Haussa ei erotella pieniä ja isoja kirjaimia (eli kirjainkoolla ei ole merkitystä) ja haussa otetaan huomioon kentän kaikissa kohdissa (alussa, lopussa tai keskellä) oleva teksti.

Voit kuitenkin tehdä tarkemman haun seuraavien erikoismerkkien avulla:

- Jos haluat etsiä vain ne kenttien arvot, jotka vastaavat koko tekstiä ja kirjainkokoa, aseta haettava teksti yksinkertaisten lainausmerkkien sisään (`''`, esimerkiksi `'man'`).

- Jos haluat etsiä arvoja, joiden alussa on tietty teksti ja jotka vastaavat tiettyä kirjainkokoa, aseta `*`-merkki hakutekstin jälkeen (esimerkiksi `man*`).

- Jos haluat etsiä arvoja, joiden lopussa on tietty teksti, ja jotka vastaavat tiettyä kirjainkokoa, aseta `*`-merkki hakutekstin eteen (esimerkiksi `*man`).

- Kun käytössä on `''` tai `*`, kirjainkoolla ei ole merkitystä haussa. Jos haluat, että kirjainkoolla ei ole merkitystä haussa, aseta `@`-merkki ennen hakutekstiä (esimerkiksi `@man*`).

Seuraavassa taulukossa on esimerkkejä haun käyttämisestä.


<!--
In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.-->

<!--
The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options. Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.  

* If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.  
* If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.
-->
<!--

|Search Criteria|Interpreted as...|Finds...|
|---------------|----------------|----------|
|`man`<br />or <br />`Man`|Contains the text; case insensitive|All records with fields that contain the text **man**, regardless of the case.|
|`'Man'`|Entire text match; case sensitive.|All records with fields that only contain **Man** exactly.|
|`Man*`|Starts with the text; case sensitive.|All records with fields that start with the text <b>Man</b> exactly.|
|`@Man*`|Starts with the text; case insensitive.|All records with fields that start with **man**, regardless of the case.|
|`@*man`|Ends with the text; case insensitive.|All records that end with **man**, regardless of the case.|
-->

|Hakuehdot|Etsii...|
|---------------|----------|
|`man`<br />tai <br />`Man`|Kaikki tietueet, joissa on **man**-tekstin sisältäviä kenttiä kirjankoosta riippumatta. Esimerkiksi **Manchester**, **manual** tai **Sportsman**. |
|`'Man'`|Kaikki tietueet, joissa on vain **Man**-tekstin sisältäviä kenttiä. Kirjainkoko on merkitsevä.|
|`Man*`|Kaikki tietueet, joissa on <b>Man</b>-tekstillä alkavia kenttiä. Kirjainkoko on merkitsevä. Esimerkiksi **Manchester**, mutta ei **manual** tai **Sportsman**.|
|`@Man*`|Kaikki tietueet, joissa on **man**-tekstillä alkavia kenttiä kirjainkoosta riippumatta. Esimerkiksi **Manchester** ja **manual**, mutta ei **Sportsman**.|
|`@*man`|Kaikki tietueet, joissa on **man**-tekstiin päättyviä kenttiä kirjainkoosta riippumatta. Esimerkiksi **Sportsman**, mutta ei **Manchester** tai **manual**.|

> [!TIP]
> Voit aktivoida hakuruudun ja poistaa aktivoinnin painamalla F3-näppäintä. Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).

## <a name="filtering"></a>Suodattaminen
Suodattaminen sisältää kehittyneitä ja monipuolisia toimintoja, joiden avulla määritetään luettelossa näkyvät tietueet. Hakemisella ja suodattamisella on kaksi pääeroa, jotka kerrotaan alla olevassa taulukossa.

|| **Hakeminen** | **Suodattaminen** |
|--|----------|------------|
| **Käytettävissä olevat kentät** | Hakee kaikista sivulla näkyvistä kentistä. | Suodattaa taulukon minkä tahansa kentän tai useita kenttiä mukaan lukien kentät, jotka eivät näy sivulla. |
| **Kohdistus** | Näyttää tietueet, joiden kentät vastaavat hakutekstiä tekstin kirjainkoosta tai sijoittelusta riippumatta. | Näyttää tietueet, joiden kentät vastaavat suodatinta täysin. Kirjainkoko on merkitsevä, jos erityisiä suodatussymboleita ei ole annettu.

Suodattaminen mahdollistaa tiettyjen tilien tai asiakkaiden, päivämäärien, summien ja muiden tietojen tietueiden näyttämisen suodatusehtojen määrittämisen avulla. Näyttöön tulevat tällöin vain ne tietueet, jotka vastaavat määritettyjä ehtoja. Jos määrität ehtoja usealle kentälle, vain kaikkia ehtoja vastaavat tietueet näytetään.

### <a name="working-in-the-filter-pane"></a>Suodatinruudun käsitteleminen
Suodatinruudussa näkyvät luettelon nykyiset suodattimet. Sen avulla voi määrittää omia suodattimia yhdelle tai usealle kentälle. Seuraavassa kuvassa on esimerkki myyntitarjousluettelon suodatinruudusta.

![Suodatinruudun yleiskatsaus ](media/filter-pane-overview.png "Suodatin-kuvake")

Jos haluat näyttää suodatinruudun, käytä **Vaihto+F3**-pikanäppäimiä. Voit valita roolikeskuksen luetteloissa sivun otsikon lähellä olevan alanuolen luettelon yläpuolella olevassa siirtymispalkissa ja valita sitten **Näytä suodatinruutu**.

![Näytä suodatinruutu](media/open-filter-pane.png "Näytä suodatinruutu")

Suodatinruutu on jaettu kolmeen osaan: **Näkymät**, **Luettelon suodatusperuste** ja **Kokonaisarvojen suodatusperuste**:

- **Näkymät**

  Joissakin luetteloissa on **Näkymät**-osa. Näkymät ovat luettelon muunnoksia, jotka on esimääritetty suodattimien kanssa. Voit vaihtaa luettelon toiseen näkymään yksinkertaisesti valitsemalla toisen linkin. Voit muuttaa näkymän suodattimia väliaikaisesti, mutta muutoksia ei tallenneta pysyvästi.

- **Luettelon suodatusperuste**

  **Luettelon suodatusperuste** -osassa lisätään suodattimet tietyille kentille ja vähennetään näin näytettävien tietueiden määrää. Voit lisätä suodattimen valitsemalla **+ suodatin**, valitsemalla sitten haluamasi suodattimen mistä tahansa taulukon kentästä ja syöttämällä suodatusehdot ruutuun.

- **Kokonaisarvojen suodatusperuste**

  Jotkin laskettuja kenttiä, kuten summia ja määriä, näyttävät luettelot sisältävät **Kokonaisarvojen suodatusperuste** -osan. Siinä voi muokata erilaisia laskelmiin vaikuttavia dimensioita. Voit esimerkiksi nopeasti analysoida tilikarttoja suodattamalla tietyn kauden summat tai tarkastella tietyn varaston myyntitilausten kokonaissummia.

  Voit lisätä suodattimen valitsemalla **+ suodatin** valitsemalla esimääritetyt dimensiot ja lisäämällä suodatusehdot ruutuun.

  > [!NOTE]
  > FlowFilter-suodattimet ohjaavat **Kokonaisarvojen suodatusperuste** -osan suodattimia sivun rakenteessa. Teknisiä lisätietoja on kohdassa [FlowFilter-suodattimet](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Suodatusehtojen syöttäminen suodatinruutuun
Jos haluat valita suodatettavan kentän, tee jokin seuraavista toiminnoista:
  - Valitse suodatinruudussa **+ kenttä**. Kirjoita suodatettavan kentän nimi tai valitse kenttä valikosta, jossa ovat kaikki taulukon kentät.

  - Valitse sarakeotsikossa alanuoli ja valitse sitten **Suodata...**. Näyttöön avautuu suodatinruutu, johon lisätään sarake.

Nyt voit kirjoittaa tai valita suodatusehdot ruutuun. Suodatettavan kentän tyyppi määrittää, millaisia ehtoja voi syöttää. Jos esimerkiksi suodatetaan kenttä, jossa on kiinteitä arvoja, valittavissa on vain nämä arvot. Lisätietoja erityisistä suodatussymboleista on kohdissa [Suodatusehdot](#FilterCriteria) ja [Suodatuksen tunnukset](#FilterTokens).

Sarakkeet, joilla on jo suodattimia, löytyvät, kun käytössä on sarakeotsikon ![Suodatus-kuvake](media/ui-search/filter-icon.png "Suodatus-kuvake"). Voit poistaa suodattimen valitsemalla sarakeotsikon ja valitsemalla sitten **Tyhjennä suodatin**.


### <a name="entering-filter-criteria-without-the-filter-pane"></a>Suodatusehtojen syöttäminen ilman suodatinruutua
Voit määrittää yksinkertaisia suodattimia suoraan luettelosta ilman suodatinruutua.
Kun rivillä on valittu mikä tahansa kenttä, voit näyttää vain saman arvon sisältävät tietueet valitsemalla **Alt+F3**-pikanäppäimet. Tämän jälkeen voit valita toisen kentän ja käyttää samoja pikanäppäimiä, kun haluat jatkaa suodattimien tarkentamista. Jos valittu kenttä on jo suodatettu, **Alt+F3** tyhjentää kyseisen suodattimen.

> [!TIP]
> Nopeuta tietojen etsimistä ja analysoimista pikanäppäinyhdistelmien avulla. Voit esimerkiksi valita kentän ja lisätä kentän suodatinruutuun **Vaihto+Alt+F3**-pikanäppäinten avulla, kirjoittaa suodatinehdot ja palata riveille **Ctrl+Enter**-pikanäppäinten avulla. Valitse toinen kenttä ja suodata sen arvot **Alt+F3**-pikanäppäimillä.
Lisätietoja on kohdassa [Pikanäppäimet](keyboard-shortcuts.md#KeyboardFilter).


## <a name="FilterCriteria"> </a>Suodatusehdot ja merkit
Kun syötät kriteerejä, voit käyttää kaikkia numeroita ja kirjaimia, joita voi yleensäkin käyttää kentässä. Voit käyttää tulosten suodatukseen myös erikoismerkkejä. Seuraavassa taulukossa on esitelty symbolit, joita voi käyttää suodattimissa. Lisätietoja päivämääristä ja ajoista on myös kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

> [!IMPORTANT]  
>  Joissakin tilanteissa kentät arvot voivat sisältää näitä merkkejä, ja haluat suodattaa niiden avulla. Siinä tapauksessa on merkki on lisättävä suodatuslausekkeeseen lainausmerkeissä (”). Jos haluat esimerkiksi suodattaa tietueita, joiden alussa on teksti *S&R*, suodatuslauseke on `'S&R*'`.  

### <a name="-interval"></a>(..) väli

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`1100..2100`|Numerot 1100 - 2100|  
|`..2500`|Numeroon 2500 asti, 2500 mukaan lukien|  
|`..12 31 00`|Päivämäärät 31.12.00 asti, kyseinen päivämäärä mukaan lukien|  
|`P8..`|Tiedot kirjanpitojaksosta 8 ja siitä eteenpäin|  
|`..23`|Alkupäivämäärästä lähtien päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59|  
|`23..`|Päivästä 23 nykyistä kuukautta nykyistä vuotta klo 00:00:00 ajan loppuun asti|  
|`22..23`|Päivästä 22 nykyistä kuukautta nykyistä vuotta klo 0:00:00 päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) joko/tai  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`1200|1300`|Numerot, joissa on 1200 tai 1300|  

### <a name="-not-equal-to"></a>(<>) ei ole sama kuin  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`<>0`|Kaikki numerot paitsi 0<br /><br /> SQL Server -vaihtoehto sallii tämän symbolin yhdistämisen yleismerkkihakuun. Esimerkiksi: <>A* - ei teksti, joka alkaa kirjaimella A.|  

### <a name="-greater-than"></a>(>) suurempi kuin  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`>1200`|Numerot, jotka ovat suurempia kuin 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Suurempi tai yhtä suuri  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`>=1200`|Numerot, jotka ovat suurempia tai yhtä suuria kuin 1200|  

### <a name="-less-than"></a>(<) pienempi kuin  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`<1200`|Numerot, jotka ovat pienempiä kuin 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Pienempi tai yhtä suuri  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`<=1200`|Numerot, jotka ovat pienempiä tai yhtä suuria kuin 1200|  

### <a name="-and"></a>(&) ja  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`>200&<1200`|Luvut, jotka ovat suurempia kuin 200 ja pienempiä kuin 1200.|  

### <a name="-an-exact-character-match"></a>('') Tarkka merkin vastine  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`'man'`|Teksti, joka vastaa täysin "man"ia ja jossa isoilla ja pienillä kirjaimilla on merkitystä.|  

### <a name="-case-insensitive"></a>(@) Ei kirjainkokoon perustuva  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`@man*`|Teksti, joka alkaa "man" ja jossa isoilla ja pienillä kirjaimilla ei ole merkitystä.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Rajoittamaton määrä tuntemattomia merkkejä

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`*Co*`|Teksti, joka sisältyy ”Co” ja jossa kirjainkoolla on merkitystä.|  
|`*Co`|Teksti, jonka lopussa on ”Co” ja jossa kirjainkoolla on merkitystä.|  
|`Co*`|Teksti, jonka alussa on ”Co” ja jossa kirjainkoolla on merkitystä.|  

> [!NOTE]  
>   Ei voi käyttää `*`-merkkiä käyttäessäsi suodattamisessa asetuskenttiä (luettelointikenttiä), kuten myyntitilausten **Tila**-kenttää. Voit syöttää suodattimen tämäntyyppiselle kentälle kirjoittamalla numeerisen arvon suodatusparametriksi. Jos esimerkiksi myyntitilauksen **Tila**-kentällä on arvot **Avoin**, **Vapautettu**, **Odottaa hyväksyntää** ja **Odottaa ennakkomaksua**, suodata vaihtoehdot arvojen `0`, `1`, `2` ja `3` avulla.

### <a name="-one-unknown-character"></a>(?) yksi tuntematon merkki  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`Hans?n`|Teksti, kuten Hansen tai Hanson|  

### <a name="combined-format-expressions"></a>Yhdistetyn muodon lausekkeet  

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Sisällytä kaikki tietueet, joissa on numero 5999 tai numero väliltä 8100 ja 8490.|  
|`..1299|1400..`|Sisällytä tietueet, joissa on numero, joka on pienempi tai yhtä suuri kuin 1299 tai suurempi tai yhtä suuri kuin 1400 (siis kaikki muut numerot paitsi 1300–1399).|  
|`>50&<100`|Sisällytä tietueet, joissa on numero, joka on suurempi kuin 50 ja pienempi kuin 100 (siis numerot 51–99).|  


## <a name="FilterTokens"> </a>Suodatuksen tunnukset
Kun syötät suodatusehtoja, voit kirjoittaa myös sanoja, joilla on erityinen tarkoitus. Niitä kutsutaan suodatuksen tunnuksiksi. Kun olet syöttänyt tunnussanan, sana korvataan arvolla tai arvoilla, joita se edustaa. Tämä helpottaa suodattamista ja vähentää muille sivuille siirtymistä ja suodattimeen lisättävien arvojen etsimistä. Taulukossa on joitakin tunnuksia, joita voit käyttää suodatusehtoina.

> [!TIP]
> Organisaatio voi käyttää mukautettuja tunnuksia. Järjestelmänvalvojalta saa lisätietoja käytettävissä olevista tunnuksista ja mukautettujen tunnusten lisäämisestä. Teknisiä lisätietoja on kohdassa [Suodatuksen tunnusten lisääminen](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)


### <a name="me-or-userid-records-assigned-to-you"></a>(%me tai %userid) Sinulle liitetyt tietueet

Käytä `%me`- tai `%userid`-tunnusta suodattaessasi kenttiä, jotka sisältävät käyttäjätunnuksen. Tällainen kenttä on esimerkiksi **Liitetty käyttäjätunnukseen**, jossa näytetään kaikki käyttäjälle liitetyt kentät.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%me`<br />tai<br />`%userid`|Tietueet, jotka on liitetty käyttäjätiliisi. |  

### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Omat asiakkaat -kohdan asiakkaat

Käytä `%mycustomers`-tunnusta asiakkaan **Nro**-kentässä, kun haluat näyttää asiakkaan kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat asiakkaat** -luetteloon.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%mycustomers`|Roolikeskuksen **Omat asiakkaat** -kohdan asiakkaat. |  

### <a name="myitems-items-in-my-items"></a>(%myitems) Omat nimikkeet -kohdan nimikkeet

Käytä `%myitems`-tunnusta nimikkeen **Nro**-kentässä, kun haluat näyttää nimikkeiden kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat nimikkeet** -luetteloon.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%myitems`|Roolikeskuksen **Omat nimikkeet** -kohdan nimikkeet. |  

### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Omat toimittajat -kohdan toimittajat

Käytä `%myvendors`-tunnusta toimittajan **Nro**-kentässä, kun haluat näyttää toimittajien kaikki tietueet, jotka sisältyvät roolikeskuksen **Omat toimittajat** -luetteloon.

|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|`%myvendors`|Roolikeskuksen **Omat toimittajat** -kohdan toimittajat. |  


## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Hakemista ja suodattamista koskevat yleiset kysymykset](ui-search-filter-faq.md)

