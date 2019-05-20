---
title: Projektihintojen ja projektin kirjausryhmien määrittäminen| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten yleiset projektitiedot määritetään, sekä määritetään projektin nimikkeiden, resurssien sekä KP-tilien ja projektien kirjausryhmien hinnat.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: project management
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 34dfdb463d3423d823b8f1439361d05296ca3c8a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253816"
---
# <a name="set-up-jobs"></a>Projektien määrittäminen

Määrität projektipäällikkönä projektit, jotka määrittävät jokaisen [!INCLUDE [prodshort](includes/prodshort.md)]issa hallittavan projektin. Määritä **Projektienhallinnan asetukset** -sivulla projektin tiettyjen toimintojen asetukset.

Kullekin projektille määritetään sitten yksittäiset projektikortit, joissa on tietoja projektinimikkeiden hinnoista, projektin resursseista ja KP-tileistä. Määritä myös projektin kirjausryhmät.

## <a name="to-set-general-information-for-jobs"></a>Projektien yleistietojen määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektienhallinnan asetukset** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> **Käytä käyttölinkkiä oletusarvoisesti** -kentän vaikutus on varsin monisyinen. Seuraavassa osassa kerrotaan siitä enemmän.

### <a name="to-set-up-job-usage-tracking"></a>Projektin käytön seurannan määrittäminen

Kun suoritat työtä, haluat ehkä tietää, miten käyttöäsi seurataan suunnitelmaasi. Voit tehdä tämän helposti luomalla linkin työsuunnittelurivien ja toteutuneen käytön välille. Tämän avulla voi seurata kustannuksia ja helposti nähdä, miten paljon työtä on vielä jäljellä. Oletusarvon mukaan työn suunnittelurivin tyyppi on **Budjetti**, mutta käyttämällä rivin tyyppiä **Sekä budjetti että laskutettava** on samanlainen vaikutus.

Jos valitset **Käytä käyttölinkkiä oletusarvoisesti** -kentän, voit tarkastella tietoja projektin suunnittelurivillä. Voit määrittää resurssin, nimikkeen tai pääkirjanpidon tilin määrän ja ilmaista projektipäiväkirjaan siirrettävän määrän. Projektin suunnittelurivin **Jäljellä oleva määrä** -kenttä osoittaa projektipäiväkirjaan siirrettävän ja kirjattavan jäljellä olevan määrän.

> [!TIP]  
> Voit ottaa käyttöön tietyn projektin projektin käytön seurannan tai poistaa sen käytöstä. Yksittäisen projektin kortin **Käytä käyttölinkkiä** -kenttä korvaa **Projektienhallinnan asetukset** -sivun asetuksen.  

Kun **Käytä käyttölinkkiä oletusarvoisesti** -valintaruutu on valittuna ja projektin suunnittelurivin tyyppi on **Laskutettava**, **Budjetti**-tyyppisen projektin suunnittelurivi luodaan projektin päiväkirjarivin kirjaamisen jälkeen.

> [!IMPORTANT]
> Jos projektin käytön seuranta on otettu käyttöön **Projektienhallinnan asetukset** -sivulla tai yksittäisessä projektissa ja päiväkirjarivin **Rivityyppi**-kenttä on tyhjä, **Budjetti**-tyyppiset projektin uudet suunnittelurivit luodaan projektipäiväkirjan rivien kirjaamisen yhteydessä.  
>  
> Jos projektin käytön seurantaa *ei* ole otettu käyttöön **Projektienhallinnan asetukset** -sivulla tai yksittäisessä projektissa ja päiväkirjarivin **Rivityyppi**-kenttä on tyhjä, mitään projektin suunnittelurivejä ei luoda projektipäiväkirjan rivien kirjaamisen yhteydessä. Lisätietoja on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektienhallinnan asetukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Käytä käyttölinkkiä oletusarvoisesti** -valintaruutu.

## <a name="to-set-up-prices-for-job-resources"></a>Projektin resurssien hintojen määrittäminen
Voit määrittää projektin resursseja varten tietyt hinnat. Tähän käytetään **Projektiresurssien hinnat** -sivua.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Projektit** ja valitse sitten liittyvä linkki.  
2. Valitse asianmukainen projekti ja valitse sitten **Resurssi**-toiminto.
3. Täytä **Projektiresurssien hinnat** -sivulla tarvittavat kentät.

**Projektitehtävän nro**-, **Työtyyppi**-, **Valuutan koodi**-, **Rivialennus-%**- ja **Yksikkökustannustekijä**-kentän valinnaisia tietoja käytetään projektin suunnitteluriveillä ja käyttöpäiväkirjoissa, kun tämä resurssi syötetään ja lisätään projektiin.  

Resurssin **Yksikköhinta**-kentän arvoa käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun tämä resurssi, resurssiryhmään liitetty resurssi tai mikä tahansa resurssi määritetään.  

> [!NOTE]  
>   Tämä hinta ohittaa aina aiemmin määritetyissä **Resurssihinta / resurssiryhmän hinta** -sivulla olevat hinnat.

## <a name="to-set-up-prices-for-job-items"></a>Projektinimikkeiden hintojen määrittäminen
Voit määrittää projektin nimikkeille tietyt hinnat. Tähän käytetään **Projektinimikkeiden hinnat** -sivua.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Projektit** ja valitse sitten liittyvä linkki.  
2. Valitse asianmukainen projekti ja valitse sitten **Nimike**-toiminto.
3. Täytä **Projektinimikkeen hinnat** -sivulla tarvittavat kentät.

**Projektitehtävän nro**-, **Valuutan koodi**- ja **Rivialennus-%**-kentän valinnaisia tietoja käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun kyseessä oleva nimike syötetään tai lisätään projektiin.  

Nimikkeen **Yksikköhinta**-kentän arvoa käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa tämän nimikkeen syöttämisen yhteydessä.  

> [!NOTE]  
>   Tämä hinta ohittaa aina nimikkeiden normaalin asiakashinnan (parhaan hinnan mekanismi). Jos haluat käyttää säännöllisiä asiakashintamekanismeja, älä luo projektille projektinimikkeiden hintoja.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>Kirjanpitotilin hintojen määrittäminen
Määritä hinnat projektin kirjanpidon kuluille. Tähän käytetään **Projektin kirjanpitotilin hinnat** -sivua.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Projektit** ja valitse sitten liittyvä linkki.  
2. Valitse asianmukainen projekti ja valitse sitten **KP-tili**-toiminto.  
3. Täytä **Projektin kirjanpitotilin hinnat** -sivulla tarvittavat kentät.

**Projektitehtävän nro**-, **Valuutan koodi**-, **Rivialennus-%**-, **Yksikkökustannustekijä**- ja **Yksikkökustannus**-kentän valinnaisia tietoja käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun tämä kirjapitotili syötetään ja lisätään projektiin.  

Pääkirjanpidon projektikulujen **Yksikköhinta**-kentän arvoa käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun tämä kirjanpitotili syötetään.

## <a name="to-set-up-job-posting-groups"></a>Projektin kirjausryhmien määrittäminen
Yksi näkökulma projektien suunnittelussa on sen päättäminen, mitä kirjaustilejä projektin kustannuslaskentaan käytetään. Projektien kirjaus edellyttää, että määrität kullekin projektin kirjausryhmälle tilit kirjausta varten. Kirjausryhmä edustaa linkkiä työn ja sen kirjanpitokäsittelyn välillä. Kun luot työn, määrität kirjausryhmän ja oletusarvon mukaan jokainen tehtävä, jonka luot työlle, liittyy kyseiseen kirjausryhmään. Voit kuitenkin ohittaa oletusarvon tehtävien luonnin yhteydessä ja valita sopivamman kirjausryhmän.  

> [!NOTE]  
>   Tarvittavat tilikartat tulee määrittää Tilikartta-taulukossa ennen kirjausryhmien määrittämistä. Lisätietoja on kohdassa [Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md).  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektin kirjausryhmät** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

| Summakentät | Kuvaus |
| --- | --- |
| **Koodi** |Anna koodi kirjausryhmää varten. Voit kirjoittaa enintään 10 merkkiä (välilyönnit mukaan lukien). |
| **KET-kustannusten tili** |Projektin keskeneräisen työn laskettujen kustannusten KET-tili, joka on käyttöomaisuuden tasetili. |
| **Kertyneiden KET-kustannusten tili** |Keskeneräisen työn laskennan kustannusarvon tai myyntikustannusmenetelmän tili, joka on taseen kertyneiden kustannusten velkatili. Kirjaus tapahtuu tälle tilille, kun keskeneräisen työn muutos edellyttää tuloslaskelmaan kirjattavien käyttökustannusten lisäystä. |
| **Projektin kohdistettujen kustannusten tili** |KET-kustannusten tilin vastatili eli negatiivisten kustannusten tilin vastatili. |
| **Nimikkeiden kohdistettujen kustannusten tili** |KET-kustannusten tilin vastatili eli negatiivisten kustannusten tilin vastatili. |
| **Resurssien kohdistettujen kustannusten tili** |KET-kustannusten tilin vastatili eli negatiivisten kustannusten tilin vastatili. |
| **Kohdistettujen kustannusten tili** |KET-kustannusten tilin vastatili eli negatiivisten kustannusten tilin vastatili. |
| **Projektin kustannusten muutostili** |Kertyneiden KET-kustannusten tilin vastatili, joka on kustannustili. |
| **Kirjanpidon kustannustili (budjetti)** |Tässä kentässä on myyntitili, jota käytetään tämän kirjausryhmän projektitehtävien kirjanpitokustannuksille. Jos kenttä on tyhjä, ohjelma käyttää projektin suunnittelurivillä määritettyä kirjanpitotiliä. |
| **Kertyneen KET-myynnin tili** |Keskeneräisen työn lasketun myyntiarvon KET-tili, joka on taseen kertyneen tuoton tili. Kirjaus tapahtuu tälle tilille, kun keskeneräisen työn muutos edellyttää tuloutetun tuoton lisäystä. |
| **Laskutetun KET-myynnin tili** |Keskeneräisen työn sen laskutetun myyntiarvon tili, jota ei voi tulouttaa. Tämä on taseen ansaitsemattoman tuoton tili. |
| **Projektin myynnin kohdistuksen tili** |Laskutetun KET-myynnin tilin vastatili, joka on tuottotilin vastatili. |
| **Projektin myynnin muutostili** |KET-myyntitilin vastatili, joka on tuottotili. |
| **Tuloutettujen kustannusten tili** |Kustannustili, joka sisältää projektin tuloutetut kustannukset. Yleensä tili on debetkustannustili. |
| **Tuloutetun myynnin tili** |Tulotili, joka sisältää projektin tuloutetut tuotot. Yleensä tili on kredittulotili. |

## <a name="see-also"></a>Katso myös

[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Video: Projektin luonti Dynamics 365 Business Centralissa](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projektien hallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
