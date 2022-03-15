---
title: Word-mallien käyttö joukkoviestinnässä | Microsoft Docs
description: Word-mallit helpottavat tietyille entiteeteille mukautettujen asiakirjojen joukkoluontia.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: fe9717f871fdc1db782ceeda4cbad267abddca90
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2022
ms.locfileid: "8383425"
---
# <a name="using-word-templates-for-bulk-communication"></a>Word-mallien käyttö joukkoviestinnässä
Microsoft Word -mallit helpottavat entiteettien, kuten kontaktien, asiakkaiden ja toimittajien, kanssa tapahtuvaa joukkoviestintää postitse tai sähköpostitse. Voit luoda esimerkiksi esitteitä, joissa kerrotaan asiakkaille myyntikampanjoista, kirjeitä, joissa toimittajille kerrotaan uudesta ostokäytännöstä, tai kutsuja, joilla houkutellaan yhteyshenkilöitä tulevaan tapahtumaan.

> [!NOTE]
> Voit käyttää Word-malleja vain laitteissa, joissa on Microsoft Word 2019 ja Windows-käyttöjärjestelmä asennettuna.

[!INCLUDE[prod_short](includes/prod_short.md)]in entiteettejä voi käyttää mallin tietolähteinä, ja asiakirjat voidaan mukauttaa kullekin entiteetille lisäämällä yhdistämiskenttiä. Yhdistämiskentät saadaan [!INCLUDE[prod_short](includes/prod_short.md)]in entiteetistä. Kun Word-mallia käytetään entiteetissä, yhdistämiskenttien tiedot lisätään asiakirjaan.

Kun luot uuden mallin, **Word-mallit**-sivulla on asetusten ohjatun määrityksen opas, jolla voi ladata DataSource.xlsx-tiedoston ja entiteetin Word-mallitiedoston sisältävän ZIP-tiedoston. Tieto lähdetiedosto sisältää kentät, joita voidaan käyttää mallissa. Älä muokkaa tietolähdetiedostoa. Voit käyttää vain [!INCLUDE[prod_short](includes/prod_short.md)]ista ladattuja Word-malli- ja tietolähdetiedostoja, ja nämä tiedostot on tallennettava samaan sijaintiin.

Kun malli on määritetty ja yhdistämiskentät lisätty, mallin voi ladata takaisin samaa opasta käyttämällä.

## <a name="setting-up-the-template-in-word"></a>Mallin määrittäminen Wordissa
Kun mallia määritetään Wordissa, yhdistämiskentät voidaan lisätä **Postitukset**-välilehdessä valitsemalla **Lisää yhdistämiskenttä**. Käytettävissä olevat yhdistämiskentät ovat peräisin tietolähdetiedostosta, jonka latasit entiteetille. Ne toimivat paikkamerkkeinä, jotka kertovat Wordille, mihin asiakirjassa on tarkoitus sijoittaa entiteetin tiedot. 

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Yhdistämiskenttien lisääminen Microsoft Wordiin":::

## <a name="adding-related-entities"></a>Liittyvien entiteettien lisääminen
Sen lisäksi, että voit lisätä lähde-entiteetin tietoja eli sen entiteetin, jolle olet luomassa mallia, voit myös yhdistää siihen liittyvien entiteettien tietoja. Jos lähde on esimerkiksi Asiakas-entiteetti, voit myös yhdistää tietoja Asiakas/Ostaja-entiteetin kentistä, koska molemmilla entiteeteillä on yhteinen kenttä.

Liittyvät entiteetit jakavat kentän, joka on usein lähde-entiteetin tunniste, kuten nimi, koodi tai tunnus. Kun määrität mallin, liittyvien entiteettien valitsemiseen on yksinkertaisia ja edistyneitä asetuksia:

* Yksinkertainen – Lisää tunnetut suhteet, jotka [!INCLUDE[prod_short](includes/prod_short.md)] tuo käytettäväksi oletusarvoisesti.
* Edistynyt – lisää muita kuin vakiosuhteita, kuten laajennusten tai mukautusten lisäämiä. Tämä edellyttää, että tunnet entiteettien jakamat kentät.

Kun lisäät liittyvän entiteetin, sinun täytyy määrittää kentän nimelle etuliite. Kun lisäät kenttiä malliin, etuliite helpottaa lähde-entiteetin kenttien ja liittyvien entiteettien kenttien erottamista toisistaan.

## <a name="to-create-a-word-template-in-business-central"></a>Word-mallin luominen Business Centralissa
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Word-mallit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**, sitten **Luo malli** ja noudata sitten avustetun asennusoppaan ohjeita. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Voit myös luoda mallin suoraan entiteetin sivulta valitsemalla **Käytä Word-mallia** -toiminnon avataksesi avustetun asetusoppaan ja sitten **Uusi malli**. Kun teet näin, tietolähde valitaan entiteetin tyypin mukaan.

## <a name="applying-a-template"></a>Mallin käyttäminen
Kun Word-malli on valmis, asiakirjat voidaan luoda valitsemalla **Word-mallit**-sivulla **Käytä**. Kun Word-mallia käytetään entiteetissä, yhdistämiskenttien tiedot lisätään asiakirjaan. Voit luoda joko yhden asiakirjan, jossa on osa kullekin entiteetille, tai valita **Jaa**-toiminnon luomaan uuden asiakirjan kullekin entiteetille.

Voit käyttää malleja yhteen tai useampaan samantyyppiseen entiteettiin, kuten kontaktiin, suoraan kyseisen sivun kontekstissa tai Word-mallit -sivulla, kun haluat käyttää mallia kaikissa kyseisen tyypin entiteeteissä.

## <a name="using-word-templates-with-email"></a>Word-mallien käyttäminen sähköpostissa
Voit lisätä sisältöä sähköpostiviesteihin Word-mallien avulla. Kun kirjoitat sähköpostiviestiä, voit ottaa mallin sisällön käyttöön viestissä käyttämällä **Käytä Word-mallia** -toimintoa. Tämä edellyttää, että olet luonut vähintään yhden mallin entiteetille. Voit käyttää yhtä mallia kerrallaan ja siirryttäessä mallien välillä viesti muuttuu valitun mallin sisällön mukaiseksi.

Lisäksi voit liittää mallin sisällön sähköpostiin tiedostona käyttämällä **Lisää tiedosto Word-mallista** -toimintoa. Tiedosto käyttää mallin tulostuksessa määritettyä muotoa.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Wordin-mallin sisällön käyttövaihtoehdot sähköpostissa":::

## <a name="see-also"></a>Katso myös
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
