---
title: "Päivämääräalueiden asettaminen Business Central -sovelluksessa | Microsoft Docs"
description: "Tutustu, miten luodaan raportti näyttämään tietyn ajanjakson tiedot käyttämällä Business Central -sovelluksen päivämääräalueita."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: fi-fi
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a>Päivämääräalueiden syöttäminen
Voit asettaa suodattimia, jotka sisältävät alkupäivämäärän ja loppupäivämäärän, jos haluat tarkastella vain kyseisen päivämääräalueen tai aikavälin tietoja. Päivämääräalueiden määrittämiseen liittyy erityissääntöjä: Käytetään esimerkkinä **10 pääasiakasta**:

![10 pääasiakkaan luettelon päivämääräalueen määrittäminen pyyntösivulla](./media/ui-enter-date-ranges/customer-top10-list.png)

Voit rajoittaa raportin päivämääräalueeksi viimeiset kaksi viikkoa, yhteensä kuusi viikkoa tai minkä tahansa sopivan alueen. Päivämääräalue määritetään antamalla päivämäärät ja määrittämällä alueen joko **..**- tai **|**-merkillä. Tässä esimerkissä 10 pääasiakkaan näyttäminen toukokuun kahdella ensimmäisellä viikolla edellyttää, että päivämääräsuodatin määritetään muotoon *05 01 17..05 14 17*.
Lisää esimerkkejä:

| Merkitys | Esimerkki | Sisällytetyt tapahtumat |
|---|---|---|
|Sama kuin| 12 15 16 |Vain tapahtumat, jotka on kirjattu 15.12.2016.|
|Väli| 12 15 16..01 15 17<br /><br />..12 15 16|Tapahtumat, jotka on kirjattu ajalla 15.12.2016–15.1.2017 (kyseiset päivämäärät mukaan lukien).<br /><br />Tapahtumat, jotka on kirjattu 15.12.2016 tai sitä aiemmin.|
|Joko/tai|12 15 16&#124;12 16 16|Tapahtumat, jotka on kirjattu joko 15.12. tai 16.12.2016. Jos molempina päivinä on kirjattu tapahtumia, kaikki kyseisten päivien tapahtumat näytetään.|

Eri muotoja voi myös yhdistellä:

| Esimerkki | Sisällytetyt tapahtumat |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Tapahtumat, jotka on kirjattu joko 15.12.2011 tai ajalla 1.12.2016– 31.5.2017 (kyseiset päivämäärät mukaan lukien). |
|..12 14 16&#124;12 30 16.. | Tapahtumat, jotka on kirjattu 14.12 tai sitä ennen, tai tapahtumat, jotka on kirjattu 30.12. tai sen jälkeen – toisin sanoen kaikki muut paitsi 15.–29.12. kirjatut tapahtumat. |

Huomaa, että tässä on käytetty yhdysvaltalaista päivämäärämuoto KKPPVV. Kun [!INCLUDE[d365fin](includes/d365fin_md.md)] on saatavana muilla markkina-alueilla, saat käyttöösi tutut päivämäärämuodot.

## <a name="using-date-formulas"></a>Päivämäärän kaavojen käyttäminen
Päivämäärän kaava on lyhyt kirjain- ja numeroyhdistelmä, joka kertoo ohjelmalle, miten päivämäärät lasketaan. Voit kirjoittaa päivämäärän kaavoja erilaisiin päivämäärän laskentakenttiin sekä toistuvien päiväkirjojen toistotiheyskenttiin.

> [!NOTE]
>  Kaikissa tietokaavakentissä yksi päivä sisällytetään automaattisesti edustamaan kuluvaa päivää kauden alkupäivänä. Jos näin ollen annat esimerkiksi **1V**, kausi on kahdeksan päivää, koska tämä päivä lasketaan mukaan. Määritä seitsemän päivän kausi (yksi kokonainen viikko), joka sisältää alkamispäivämäärän, ja syötä sitten **6D** tai **1W\-1D**.

Seuraavassa on joitakin esimerkkejä päivämäärän kaavojen käytöstä:

-   Toistuvien päiväkirjojen toistotiheys-kentän päivämäärän kaava määrittää, kuinka usein päiväkirjan rivin tapahtuma kirjataan.

-   **Ylityskausi**-kentän tietyn tason muistutusta koskeva päivämäärän kaava määrittelee ajanjakson, joka on kuluttava eräpäivästä (tai edellisen muistutuksen eräpäivästä), ennen kuin muistutus voidaan luoda.

-   **Eräpäivän laskenta** -kentän kaava määrittää, miten ohjelma laskee muistutuksen eräpäivän.

Eräpäivän laskentakaavassa voi olla enintään 20 merkkiä, sekä numeroita että kirjaimia. Voit käyttää seuraavia kirjaimia, jotka ovat aikamääreiden lyhenteitä:

|  Kirjain  |  Aikamääritys  |
|----------|----------------------|
|S|Nykyinen|
|P|Päivä|
|L|Viikko|
|M|Kuukausi|
|Q|Vuosineljännes|
|V|Vuosi|

Voit rakentaa päivämääräkaavan kolmella eri tavalla:

Seuraava esimerkki näyttää, miten käytetään kirjainta **C** (nykyinen) ja aikayksikköä.

|  Lauseke  |  Merkitys  |
|--------------|-----------|
|NVI|Nykyinen viikko|
|NK|Nykyinen kuukausi|

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
|CM\+10D|Nykyinen kuukausi \+ 10 päivää|

Miinus-merkin avulla pystyt ilmaisemaan menneitä päiviä. Esimerkiksi:

|  Lauseke  |  Merkitys  |
|--------------|-----------|
|-1 V.|1 vuosi taaksepäin tästä päivästä|

> [!IMPORTANT]
>  Jos sijainti käyttää peruskalenteria, sitten päivämääräkaava, jonka annat esimerkiksi **Toimitusaika** -kenttään, tulkitaan kalenterin mukaan työskentelypäiviksi. Esimerkiksi **1V** tarkoittaa seitsemää työpäivää.

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md)  
[Ostojen päivämäärälaskenta](purchasing-date-calculation-for-purchases.md)  
[Ehtojen antaminen suodattimiin](ui-enter-criteria-filters.md)  

