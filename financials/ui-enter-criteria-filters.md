---
title: Tietojen etsiminen ja suodatusehtojen antaminen | Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan, miten suodattimilla, kuten pikasuodattimella, voi tarkentaa tietojen hakutuloksia."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="searching-filtering-and-sorting-data"></a>Tietojen etsiminen, suodattaminen ja lajitteleminen
Luettelossa olevien tietojen etsimistä, paikallistamista ja skannaamista voi helpottaa muutamilla keinoilla. Näitä keinoja ovat esimerkiksi lajitteleminen, etsiminen ja suodattaminen.

Syötä ehtoja, kun haluat etsiä tiettyjä tietoja, kuten asiakkaiden nimiä, osoitteita tai tuoteryhmiä. Hakuehdoissa voi käyttää kaikkia numeroita ja kirjaimia, joita kentissä yleensä käytetään. Lisäksi voit käyttää tulosten suodatukseen erikoismerkkejä. Käytössä on kaksi hakutapaa: pikasuodatin ja sarakesuodattimet.

## <a name="sorting"></a>Lajittelu
Lajittelun avulla tiedoista saa nopeasti ja kätevästi yleiskuvan. Jos asiakkaita on useita, saat tarvitsemasi yleiskuvan lajittelemalla heidät esimerkiksi **Asiakasnro**-, **Asiakkaan kirjausryhmä**-, **Valuuttakoodi**-, **Maa-/aluekoodi**- tai **ALV-rekisteröintinro**-kohdan avulla,

Voit lajitella luettelon joko valitsemalla sarakkeen otsikkotekstin ja vaihtelemalla nousevaa ja laskevaa lajittelua tai valitsemalla sarakeotsikossa olevilla pienillä nuolilla **Nouseva**- tai **Laskeva** -vaihtoehdon.  

> [!NOTE]  
>   Lajittelua taulukkoon kuulumattomien kuvien, BLOB-kenttien ja FlowFilter-suodattimien lajittelua ei tueta.  

## <a name="searching-by-using-the-quick-filter"></a>Haku pikasuodattimen avulla
Pikasuodattimen avulla voit lisätä suodattimia kaikille sivuille. Pikasuodatin otetaan käyttöön valitsemalla sivun oikeassa yläkulmassa oleva suurennuslasikuvake. Tätä suodatustyyppiä käytetään ehtojen nopeassa syöttämisessä.

> [!IMPORTANT]  
>   Pikasuodatin tarjoaa helpon pääsyn tietojen suodatukseen kirjaamalla pelkkä teksti, mutta ei tarjoa paljoa hakukriteerivaihtoehtoja. Pikasuodatin toimii eri tavalla riippuen siitä, kirjoitatko tekstiä tai tekstiä symboleilla.  

* Jos kirjoitat hakuehtoon pelkän tekstin, hakuehto tulkitaan hauksi, joka ei huomioi kirjainkokoa ja joka sisältää tietyn tekstin.  
* Jos kirjoitat hakuehtoon tekstiä, joka sisältää symboleja, hakuehto tulkitaan juuri siten kuin kirjoitit sen ja haun kirjainkoko on merkitsevä.

### <a name="quick-filter-criteria"></a>Pikasuodattimen ehdot
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Hakuehdot</TH>
    <TH>Tulkinta...</TH>
    <TH>Palautukset...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;valm&#42;</TD>
    <TD>Kaikki tietueet, jotka sisältävät tekstin <b>mies</b> ja kirjainkokoa huomioimatta.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Kaikki tietueet, jotka sisältävät tekstin <b>se</b> ja kirjainkokoa huomioimatta.</TD>
  </TR>
  <TR>
    <TD>Valm&#42;</TD>
    <TD>Alussa <b>Valm</b> ja kirjainkoolla on merkitystä.</TD>
    <TD>Kaikki tietueet, jotka alkavat tekstillä <b>Mies</b>.</TD>
  </TR>
  <TR>
    <TD>'man'</TD>
    <TD>Täsmällinen teksti ja kirjainkoolla on merkitystä.</TD>
    <TD>Kaikki tietueet, jotka vastaavat täsmälleen tekstiä <b>mies</b>.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Alkaa ja kirjainkoolla ei ole merkitystä.</TD>
    <TD>Kaikki tietueet, jotka alkavat tekstillä <b>mies</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;valm</TD>
    <TD>Päättyy ja kirjainkoolla ei ole merkitystä.</TD>
    <TD>Kaikki tietueet, jotka päättyvät tekstiin <b>mies</b>.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   Yleismerkkejä ei voi käyttää luettelointikenttien suodattamiseen. Tällainen kenttä on esimerkiksi myyntitilausten **Tila**-kenttä. Voit syöttää suodattimen tämäntyyppiselle kentälle kirjoittamalla numeerisen arvon suodatusparametriksi. Esimerkiksi **Tila**-kenttä myyntitilauksessa, jolla on arvot **Avoin**, **vapautettu**,**Odottaa hyväksyntää** ja **Odottaa ennakkomaksua**, suodata nämä asetukset käyttämällä arvoja **0**,**1**,**2** ja **3**. 

## <a name="searching-by-using-column-filters"></a>Haku sarakkeen suodattimien avulla
Voit lisätä suodattimen vähintään yhteen luettelon sarakkeeseen. Sarakkeiden suodattaminen on pikasuodattimen käyttöä joustavampaa ja monipuolisempaa. 

### <a name="to-add-a-filter-on-a-column"></a>Suodattimen lisääminen sarakkeeseen
1.  Siirry ennen suodattimen lisäämistä luettelonäkymään valitsemalla ![Näytä luettelona](media/ui_show_as_list_icon.png "Näytä luettelona, vasen nuoli") -kuvake.
2. Valitse sarakkeen otsikossa ensin alanuoli ja sitten **Suodata**.
3. Tee jompikumpi seuraavista toimista: 
  -  Valitse luettelosta arvo valitsemalla ruudun vieressä *...*.
  -  Anna suodatusehdot ruudussa. Lisätietoja on seuraavassa osiossa.
4. Valitse **OK**-painike.

## <a name="filter-criteria-and-symbols"></a>Suodatusehdot ja merkit
Kun syötät kriteerejä, voit käyttää kaikkia numeroita ja kirjaimia, joita voi yleensäkin käyttää kentässä. Voit käyttää tulosten suodatukseen myös erikoismerkkejä. Seuraavassa taulukossa on esitelty symbolit, joita voi käyttää suodattimissa.  
  
> [!IMPORTANT]  
>  Joissakin tilanteissa kentät arvot voivat sisältää näitä merkkejä, ja haluat suodattaa niiden avulla. Siinä tapauksessa on merkki on lisättävä suodatuslausekkeeseen lainausmerkeissä (”). Jos haluat esimerkiksi suodattaa tietueita, joiden alussa on teksti *S&R*, suodatuslauseke on **'S&R*'**.  
  
### <a name="-interval"></a>(..) väli  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|1100..2100|Numerot 1100 - 2100|  
|..2500|Numeroon 2500 asti, 2500 mukaan lukien|  
|..12 31 00|Päivämäärät 31.12.00 asti, kyseinen päivämäärä mukaan lukien|  
|P8..|Tiedot kirjanpitojaksosta 8 ja siitä eteenpäin|  
|..23|Alkupäivämäärästä lähtien päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59|  
|23..|Päivästä 23 nykyistä kuukautta nykyistä vuotta klo 00:00:00 ajan loppuun asti|  
|22..23|Päivästä 22 nykyistä kuukautta nykyistä vuotta klo 0:00:00 päivään 23 nykyistä kuukautta nykyistä vuotta klo 23:59:59|  
  
### <a name="124-eitheror"></a>(&#124;) joko/tai  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|1200&#124;1300|Numerot, joissa on 1200 tai 1300|  
  
### <a name="-not-equal-to"></a>(<>) ei ole sama kuin  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|<>0|Kaikki numerot paitsi 0<br /><br /> SQL Server -vaihtoehto sallii tämän symbolin yhdistämisen yleismerkkihakuun. Esimerkiksi: <>A* - ei teksti, joka alkaa kirjaimella A.|  
  
### <a name="-greater-than"></a>(>) suurempi kuin  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|>1200|Numerot, jotka ovat suurempia kuin 1200|  
  
### <a name="-greater-than-or-equal-to"></a>(>=) Suurempi tai yhtä suuri  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|>=1200|Numerot, jotka ovat suurempia tai yhtä suuria kuin 1200|  
  
### <a name="-less-than"></a>(<) pienempi kuin  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|<1200|Numerot, jotka ovat pienempiä kuin 1200|  
  
### <a name="-less-than-or-equal-to"></a>(<=) Pienempi tai yhtä suuri  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|<=1200|Numerot, jotka ovat pienempiä tai yhtä suuria kuin 1200|  
  
### <a name="-and"></a>(&) ja  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|>200&<1200|Luvut, jotka ovat suurempia kuin 200 ja pienempiä kuin 1200.|  
  
### <a name="-an-exact-character-match"></a>('') Tarkka merkin vastine  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|'man'|Teksti, joka vastaa täysin "man"ia ja jossa isoilla ja pienillä kirjaimilla on merkitystä.|  
  
### <a name="-case-insensitive"></a>(@) Ei kirjainkokoon perustuva  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|@man*|Teksti, joka alkaa "man" ja jossa isoilla ja pienillä kirjaimilla ei ole merkitystä.|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Rajoittamaton määrä tuntemattomia merkkejä  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|*Co*|Teksti, joka sisältyy ”Co” ja jossa kirjainkoolla on merkitystä.|  
|*Oy|Teksti, jonka lopussa on ”Co” ja jossa kirjainkoolla on merkitystä.|  
|Oy*|Teksti, jonka alussa on ”Co” ja jossa kirjainkoolla on merkitystä.|  
  
### <a name="-one-unknown-character"></a>(?) yksi tuntematon merkki  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|Hans?n|Teksti, kuten Hansen tai Hanson|  
  
### <a name="combined-format-expressions"></a>Yhdistetyn muodon lausekkeet  
  
|Esimerkkimuoto|Näkyvät tietueet|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Sisällytä kaikki tietueet, joissa on numero 5999 tai numero väliltä 8100 ja 8490.|  
|..1299&#124;1400..|Sisällytä tietueet, joissa on numero, joka on pienempi tai yhtä suuri kuin 1299 tai suurempi tai yhtä suuri kuin 1400 (siis kaikki muut numerot paitsi 1300–1399).|  
|>50&<100|Sisällytä tietueet, joissa on numero, joka on suurempi kuin 50 ja pienempi kuin 100 (siis numerot 51–99).|  
 
## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

