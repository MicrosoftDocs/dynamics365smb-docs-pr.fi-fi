---
title: Projektien, hintojen ja projektin kirjausryhmien määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten yleiset projektitiedot määritetään, sekä määritetään projektin nimikkeiden, resurssien sekä KP-tilien ja projektien kirjausryhmien hinnat.
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management
ms.search.form: 211, 463, 1012
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 369e47e5bb8d30f2042b7051ed5bc0a1124a0797
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079036"
---
# <a name="set-up-jobs-prices-and-job-posting-groups"></a>Projektien, hintojen ja projektin kirjausryhmien määrittäminen

Määrität projektipäällikkönä projektit, jotka määrittävät jokaisen [!INCLUDE[prod_short](includes/prod_short.md)]issa hallittavan projektin. Määritä **Projektienhallinnan asetukset** -sivulla projektin tiettyjen toimintojen asetukset.

Kullekin projektille määritetään sitten yksittäiset projektikortit, joissa on tietoja projektinimikkeiden hinnoista, projektin resursseista ja KP-tileistä. Määritä myös projektin kirjausryhmät.

## <a name="to-set-general-information-for-jobs"></a>Projektien yleistietojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektienhallinnan asetukset** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> **Käytä käyttölinkkiä oletusarvoisesti** -kenttä osoittaa, ovatko projektitapahtumat linkitetty projektin suunnitteluriveihin oletusarvoisesti. Valitse kenttä, jos haluat ottaa tämän asetuksen käyttöön kaikkiin luomiisi projekteihin. Voit ottaa käyttöön projektin käytön seurannan tietyssä projektissa tai poistaa sen käytöstä muuttamalla **Käytä käyttölinkkiä** -kentän arvoa yksittäisessä projektikortissa. Seurauksista kerrotaan seuraavassa osassa.

### <a name="to-set-up-job-usage-tracking"></a>Projektin käytön seurannan määrittäminen

Kun työskentelet projektin parissa, haluat ehkä tietää, miten käyttöäsi seurataan suunnitelmaasi. Voit tehdä tämän helposti luomalla linkin työsuunnittelurivien ja toteutuneen käytön välille. Tämän avulla voi seurata kustannuksia ja helposti nähdä, miten paljon työtä on vielä jäljellä. Oletusarvon mukaan työn suunnittelurivin tyyppi on *Budjetti*, mutta käyttämällä rivin tyyppiä **Sekä budjetti että laskutettava** on samanlainen vaikutus.

Kun olet valinnut käytön seurannan valitsemalla **Käytä käyttölinkkiä** -kentän, voit tarkastella tietoja projektin suunnittelurivillä. Voit määrittää resurssin, nimikkeen tai pääkirjanpidon tilin määrän ja ilmaista projektipäiväkirjaan siirrettävän määrän. Projektin suunnittelurivin **Jäljellä oleva määrä** -kenttä osoittaa projektipäiväkirjaan siirrettävän ja kirjattavan jäljellä olevan määrän.

>[!NOTE]
> Jos yksittäisen projektin **Käytä käyttölinkkiä** -valintaruutu on valittu ja päiväkirjarivin **Rivityyppi**-kenttä tai ostorivi on *Laskutettava*, *Budjetti*-tyyppiset projektin uudet suunnittelurivit luodaan projektipäiväkirjan tai ostoasiakirjan kirjaamisen yhteydessä.  
> Lisätietoja on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md) ja [Projektin tarvikkeiden hallinta](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Jos projektipäiväkirjarivin tai ostorivin **Rivityyppi**-kenttä on tyhjä, projektin suunnittelurivejä ei luoda, kun projektipäiväkirja tai ostoasiakirja kirjataan.

<!--
>[!Important]
If job usage tracking is enabled on the individual job and the **Line Type** field on the job journal or purchase line line is blank, then new job planning lines of line type *Budget* are created when you post job journal or purchase document.
If job usage tracking is not enabled and the **Line Type** field on the job journal line or purchase line is blank, then no job planning lines are created when you post job journal or purchase document.
-->


## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs"></a>Hintojen määrittäminen töiden nimikkeille, resursseille ja KP-tileille

> [!NOTE]
> Vuoden 2020 julkaisuaallossa 2 julkaisimme uudet prosessit hintojen ja alennusten määritykseen ja hallintaan. Jos olet uusi asiakas, käytät uutta käyttökokemusta. Jos olet jo asiakas, uuden käyttöokemuksen käyttö riippuu siitä, onko järjestelmänvalvoja ottanut käyttöön **Uusi myyntihinnoittelukokemus** -ominaisuuden päivityksen **ominaisuuksien hallinnassa**. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

Voit määrittää hintoja työhön liittyville nimikkeille, resursseille ja KP-tileille. 

#### <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience)

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse projekti ja valitse sitten **Resurssi**- **Nimike**- tai **KP-tili**-toiminto.
3. Täytä **Projektiresurssien hinnat**-, **Projektinimikkeiden hinnat**- tai **Projektin kirjanpitotilin hinnat** -sivulla tarvittavat kentät.

Seuraavasta taulukosta näkee, miten valinnaisten kenttien tietoja käytetään projektin suunnitelma riveillä ja päiväkirjoissa, kun projektille valitaan resurssi, nimike tai kirjanpitotili.

|Sarake1  |Sarake2  |
|---------|---------|
|**Projektiresurssit**|**Projektitehtävänro**-, **Työtyyppi**-, **Valuuttakoodi**-, **Rivialennus-%**- ja **Yksikkökustannustekijä**-kentät. Resurssin **Yksikköhinta**-kentän arvoa käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun tämä resurssi, resurssiryhmään liitetty resurssi tai mikä tahansa resurssi määritetään. Huomaa, että tämä hinta ohittaa aina aiemmin määritetyissä **Resurssihinta / resurssiryhmän hinta** -sivulla olevat hinnat.|
|**Projektinimikkeet**|**Projektitehtävänro**-, **Valuuttakoodi**- ja **Rivialennus-%**-kentät. Nimikkeen **Yksikköhinta**-kentän arvoa käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa tämän nimikkeen syöttämisen yhteydessä. Huomaa, että tämä hinta ohittaa aina nimikkeiden normaalin asiakashinnan (parhaan hinnan mekanismi). Jos haluat käyttää säännöllisiä asiakashintamekanismeja, älä luo projektille projektinimikkeiden hintoja.|
|**Kirjanpitotilit**|**Projektitehtävän nro**-, **Valuutan koodi**-, **Rivialennus-%**-, **Yksikkökustannustekijä**- ja **Yksikkökustannus**-kentän tietoja käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun tämä kirjapitotili syötetään ja lisätään projektiin. Pääkirjanpidon projektikulujen **Yksikköhinta**-kentän arvoa käytetään projektin suunnitteluriveillä ja projektipäiväkirjoissa, kun tämä kirjanpitotili syötetään.|

#### <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience)

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse soveltuva projekti ja valitse sitten **Myyntihinnastot**-toiminto.

---

## <a name="to-set-up-job-posting-groups"></a>Projektin kirjausryhmien määrittäminen

Yksi näkökulma projektien suunnittelussa on sen päättäminen, mitä kirjaustilejä projektin kustannuslaskentaan käytetään. Projektien kirjaus edellyttää, että määrität kullekin projektin kirjausryhmälle tilit kirjausta varten. Kirjausryhmä edustaa linkkiä työn ja sen kirjanpitokäsittelyn välillä. Kun luot työn, määrität kirjausryhmän ja oletusarvon mukaan jokainen tehtävä, jonka luot työlle, liittyy kyseiseen kirjausryhmään. Voit kuitenkin ohittaa oletusarvon tehtävien luonnin yhteydessä ja valita sopivamman kirjausryhmän.  

> [!NOTE]  
>   Tarvittavat tilikartat tulee määrittää Tilikartta-taulukossa ennen kirjausryhmien määrittämistä. Lisätietoja on kohdassa [Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md).  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektin kirjausryhmät** ja valitse sitten vastaava linkki.  
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

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/paths/set-up-jobs-resources/)

## <a name="see-also"></a>Katso myös

[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Video: Projektin luonti Dynamics 365 Business Centralissa](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projektien hallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
