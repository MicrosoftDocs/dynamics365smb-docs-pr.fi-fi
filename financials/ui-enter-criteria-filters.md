---
title: "Suodattimien hakuehtojen määrittäminen | Microsoft Docs"
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="entering-criteria-in-filters"></a>Ehtojen syöttäminen suodattimiin
Syötä ehtoja, kun haluat etsiä tiettyjä tietoja, kuten asiakkaiden nimiä, osoitteita tai tuoteryhmiä. Hakuehdoissa voi käyttää kaikkia numeroita ja kirjaimia, joita kentissä yleensä käytetään. Lisäksi voit käyttää tulosten suodatukseen erikoismerkkejä.

## <a name="searching-using-the-quick-filter"></a>Haku pikasuodattimen avulla
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

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

