---
title: Rakennetiedot – uusintatilauskäytäntöjen käsittely | Microsoft Docs
description: Yleiskatsaus tehtävistä, joilla määritetään tuotantosuunnittelun uusintatilauskäytäntö.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dbe63d653120eb9e6450af401558414cf2057b1d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922240"
---
# <a name="design-details-handling-reordering-policies"></a>Rakennetiedot: uusintatilauskäytäntöjen käsittely
Uusintatilausväli on määritettävä, jotta nimike voi osallistua tarjonnan suunnitteluun. Seuraavat neljä jälkitilausohjetta on olemassa:  

* Kiinteä uusintatil. määrä  
* Enimmäismäärä  
* Tilaus  
* Erä-erästä  

Kiinteä uusintatil. määrä- ja enimmäismäärä-käytännöt liittyvät varaston suunnittelu. Vaikka varaston suunnittelu on teknisesti helpompaa kuin täsmäytys, näiden käytäntöjen tulee toimia yhdessä tarjonnan vaiheittaiseksi täsmäyttämiseksi ja tilausten seuraamiseksi. Jotta näiden kahden välisen integroinnin valvonta ja Käytetyn suunnittelulogiikan näkyvyyden määritys onnistuu, uudelleentilausmenetelmiä käsitellään tiukkojen periaatteiden avulla.  

## <a name="the-role-of-the-reorder-point"></a>Uusintatilauspisteen rooli
Yleisen kysynnän ja tarjonnan täsmäytyksen lisäksi suunnittelujärjestelmän on myös valvottava liittyvien nimikkeiden varastomääriä suhteessa määritettyihin uudelleenjärjestelykäytäntöihin.  

Uusintatilauspiste edustaa kysyntää toimitusaikana. Kun oletetun varaston arvo laskee uusintatilauspisteen määrittämän varaston tason alapuolelle, on aika tilata lisää. Tänä aikana varaston arvon oletetaan laskevan asteittain ja saavuttavan mahdollisesti nollan (tai varmuusvaraston tason), kunnes täydennys saapuu.  

Näin ollen suunnittelujärjestelmä ehdottaa tulevaa ajastettua toimitustilausta, kun oletettu varasto vähenee uusintatilauspisteen alapuolelle.  

Jälkitilauspiste heijastaa tiettyä varaston tasoa. Varastotasot voivat kuitenkin siirtyä aikavälillä huomattavasti, ja tämän vuoksi suunnittelujärjestelmän tulisi valvoa jatkuvasti oletettua saatavilla olevaa varastoa.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Arvioidun varastotason ja uusintatilauspisteen valvonta
Varasto on tarjonnan tyyppi mutta varaston suunnittelussa suunnittelujärjestelmä erottaa kaksi varastotasoa:  

* Suunniteltu varasto  
* Oletettu saatavilla oleva varasto  

### <a name="projected-inventory"></a>Suunniteltu varasto  
Aluksi arvioitu varasto on bruttovaraston määrä, mukaan lukien kysyntä ja tarjonta menneisyydessä vaikka sitä ei ole kirjattu, kun suunnitteluprosessi aloitetaan. Tulevaisuudessa tästä tulee liikkuva arvioitu varastotaso, jota ylläpidetään tulevan tarjonnan ja kysynnän bruttomäärillä, koska nämä tulevat mukaan ajan kuluessa (joko varattu tai muulla tavoin kohdistettu).  

Suunnittelujärjestelmä käyttää käsiteltyä varastoa tarkkailemaan jälkitilauspistettä ja määrittämään jälkitilausmäärän, kun käytetään jälkitilauksen maksimimäärätapaa.  

### <a name="projected-available-inventory"></a>Oletettu saatavilla oleva varasto  
Käsitelty käytettävissä oleva varasto on osa käsiteltyä varastoa, joka tiettyyn aikaan on käytettävissä täyttämään kysyntää. Suunnittelumoottori käyttää käsiteltyä käytettävissä olevaa varastoa, kun varmuusvaraston tasoa tarkkaillaan.  

Suunnittelujärjestelmä käyttää käsiteltyä käytettävissä olevaa varastoa tarkkaillakseen varmuusvarastoa, koska varmuusvaraston täytyy aina olla käytettävissä palvelemaan odottamatonta kysyntää.  

### <a name="time-buckets"></a>Aikavälit  
Ennustetun varastosaldon tiukka hallinta on tärkeää lisätilauspisteen tunnistamiseksi sekä oikean tilausmäärän laskemiseksi, kun enimmäistilausmäärän sääntö on käytössä.  

Kuten aiemmin mainittiin, arvioitu varastotaso lasketaan suunnittelujakson alussa. Se on bruttotaso, joka ei huomioi varauksia ja vastaavia kohdistuksia. Järjestelmä valvoo aikavälin koottuja muutoksia ja valvoo tätä varaston tasoa suunnitteluvaiheen aikana. Järjestelmä varmistaa, että aikaväli on vähintään yksi päivä, koska se on kysyntä- tai tarjontatapahtuman tarkin aikayksikkö.  

### <a name="determining-the-projected-inventory-level"></a>Arvioidun varastotason määrittäminen  
Seuraava jakso kuvaa sitä, kuinka suunniteltu varaston taso määritellään:  

* Kun tarjontatapahtuma, kuten ostotilaus, on kokonaan suunniteltu, se nostaa oletetun varaston arvoa eräpäivänä.  
* Kokonaan täytetty kysyntätapahtuma ei vähennä oletetun varaston arvoa heti. Sen sijaan se kirjaa vähennyksen muistutuksen, joka on sisäinen tietue, joka sisältää päivämäärän ja arvioituun varastoon lisättävän määrän.  
* Kun seuraavaa tarjontatapahtumaa suunnitellaan ja se asetetaan aikajanalle, kirjatut vähennyksen muistutukset tutkitaan yksi kerrallaan tarjonnan suunniteltuun päivämäärään asti oletetun varaston päivityksen aikana. Tämän prosessin aikana sisäisen noston lisätilaustaso voidaan saavuttaa tai ylittää.  
* Jos uusi toimitustilaus otetaan käyttöön, järjestelmä tarkistaa, onko se kirjoitettu ennen nykyistä tarjontaa. Jos se on, uudesta tarjonnasta tulee nykyinen tarjonta ja täsmäytys käynnistyy uudelleen.  

Seuraavassa esitetään graafinen kuvaus tästä periaatteesta:  

![Arvioidun varastotason määrittäminen](media/nav_app_supply_planning_2_projected_inventory.png "Arvioidun varastotason määrittäminen")  

1. Määrän 4 tarjonta **Sa** (kiinteä) sulkee kysynnän **Da** määrällä -3.  
2. CloseDemand: Luo vähennyksen muistutus -3 (ei näkyvillä).  
3. Tarjonta **Sa** on suljettu ylijäämällä 1 (kysyntää ei enää ole).  

     Tämä nostaa oletetun varaston tasoksi +4, kun taas oletetun **saatavilla** olevan varaston tasoksi tulee -1.  

4. Seuraava määrältään 2 tarjonta **Sb** (toinen tilaus) on jo asetettu aikajanalle.  
5. Järjestelmä tarkistaa, onko mitään vähenemismuistutusta ennen **Sb:tä** (ei ole, joten mitään toimintoa ei suoriteta).  
6. Järjestelmä sulkee tarjonnan **Sb** (kysyntää ei enää ole) – joko A: vähentämällä sen nollaan (peruutus) tai B: jättämällä sen ennalleen.  

     Tämä kasvattaa ennustettua varastosaldoa (A: +0 => +4 tai B: +2 = +6).  

7. Järjestelmä tekee lopullisen tarkastuksen: onko mitään vähenemismuistutusta? Kyllä, löytyy yksi päivämääränä **Da**.  
8. Järjestelmä lisää muistutuslaskun (-3) ennustettuun varastosaldoon, joko A: +4 -3 = 1 tai B: +6 -3 = +3.  
9. Tapauksessa A järjestelmä luo tulevaisuuteen aikataulutetun tilauksen aloituspäivämäärällä **Da**.  

     Tapauksessa B lisätilauspiste on saavutettu ja uusi tilaus luodaan.

## <a name="the-role-of-the-time-bucket"></a>Aikavälin rooli
Aikavälin tarkoitus on kerätä kysyntätapahtumia aikaikkunan sisällä, jotta yhteinen toimitustilaus voidaan tehdä.  

Uusintatilauspistettä käyttävien uusintatilaustapojen kohdalla voit määrittää aikavälin. Tämä varmistaa, että saman ajanjakson kysyntä kertyy, ennen vaikutuksen oletettuun varastoon ja uusintatilauspisteen mahdollisen ohituksen tarkistusta. Jos uusintatilauspiste on ohitettu, uusi toimitustilaus ajoitetaan eteenpäin aikavälin määrittämän jakson lopusta. Aikavälit alkavat suunnittelun aloituspäivämäärästä.  

Konsepti, jolle on määritetty aikavälit, osoittaa manuaalisen varastotason tarkistuksen prosessin säännöllisin väliajoin, ei jokaisen tapahtuman kohdalla. Käyttäjän on määritettävä toistoväli (aikaväli). Esimerkiksi käyttäjä kerää kaikki nimikkeen tarpeet yhdeltä toimittajalta viikoittaisen tilauksen asettamiseksi.  

![Esimerkki aikavälistä suunnittelussa](media/nav_app_supply_planning_2_reorder_cycle.png "Esimerkki aikavälistä suunnittelussa")  

Aikaväliä käytetään yleensä limittäisyyden välttämiseksi. Esimerkiksi täsmäytetty kysynnän ja tarjonnan rivi, jossa aikainen kysyntä on peruutettu tai uusi luodaan. Tuloksena on, että jokainen toimitustilaus (paitsi viimeisin) aikataulutetaan uudelleen.

## <a name="staying-under-the-overflow-level"></a>Sallitun ylityksen alapuolella pysytteleminen
Kun Enimmäismäärä- ja Kiinteä uusintatil. määrä -käytäntöjä käytetään, suunnittelujärjestelmä keskittyy oletettuun varastoon vain annetulla aikavälillä. Tämä tarkoittaa sitä, että suunnittelujärjestelmä voi ehdottaa tarpeetonta tarjontaa, kun annetun aikavälin ulkopuolella tapahtuu negatiivisia tai positiivisia tarjonnan muutoksia. Jos tästä syystä ehdotetaan tarpeetonta tarjontaa, suunnittelujärjestelmä laskee mihin määrään tarjonta tulee vähentää (tai poistaa) tarpeettoman tarjonnan välttämiseksi. Tätä määrää kutsutaan ylivuototasoksi. Ylitys ilmoitetaan suunnittelurivinä, jossa on **Muuta määrä (vähennys)**- tai **Peruuta**-toiminto, ja seuraava varoitusviesti:  

*Huomio: arvioitu varastomäärä [xx] on korkeampi kuin sallittu ylitys [xx] [xx] eräpäivänä [xx].*  

![Varaston sallittu ylitys](media/supplyplanning_2_overflow1_new.png "Varaston sallittu ylitys")  

###  <a name="calculating-the-overflow-level"></a>Lasketaan sallittua ylitystä  
Ylitystaso lasketaan eri tavoin riippuen suunnitteluasetuksista.  

#### <a name="maximum-qty-reordering-policy"></a>Enimmäismäärä-uusintatilaustapa  
Sallittu ylitys = enimmäisvarasto  

> [!NOTE]  
>  Jos vähimmäistilausmäärä on olemassa, se lisätään seuraavasti: sallittu ylitys = enimmäisvarasto + vähimmäistilausmäärä.  

#### <a name="fixed-reorder-qty-reordering-policy"></a>Kiinteän uusintatilausmäärän uusintatilaustapa  
Sallittu ylitys = uusintatilausmäärä + uusintatilauspiste  

> [!NOTE]  
>  Jos vähimmäistilausmäärä on korkeampi kuin uusintatilauspiste, se korvaa seuraavasti: sallittu ylitys = uusintatilausmäärä + vähimmäistilausmäärä  

#### <a name="order-multiple"></a>Tilauskerrannainen  
Jos tilauskerrannainen on olemassa, se säätää sekä enimmäismäärän että kiinteän uusintatilaustavan sallittua ylitystä.  

###  <a name="creating-the-planning-line-with-overflow-warning"></a>Suunnittelurivin luominen ylitys-varoituksella  
Suunnittelurivi luodaan, kun oletettu varasto on aikavälin lopussa suurempi kuin sallittu ylitys olemassa olevan tarjonnan vuoksi. Kun mahdollisesta tarpeettomasta tarjonnasta varoitetaan, suunnittelurivillä on varoitusviesti, **Hyväksy toimenpideviesti** -kenttää ei ole valittu ja toimenpideviesti on Peruuta tai Muuta määrä.  

#### <a name="calculating-the-planning-line-quantity"></a>Lasketaan suunnittelurivin määrää  
Suunnittelurivin määrä = nykyisen tarjonnan määrä (oletettu varasto – sallittu ylitys)  

> [!NOTE]  
>  Kuten kaikkien varoitusrivien kohdalla, kaikki tilauksen enimmäis-/vähimmäismäärät ohitetaan.  

#### <a name="defining-the-action-message-type"></a>Toimintoviestin tyypin määrittäminen  

-   Jos suunnittelurivin määrä on suurempi kuin 0, toimenpideviesti on Muuta määrä  
-   Jos suunnittelurivin määrä on yhtä suuri tai pienempi kuin 0, toimenpideviesti on Peruuta  

#### <a name="composing-the-warning-message"></a>Varoitusviestin luonti  
Ylivuodon tapauksessa **Ei-seuratut suunnitteluelementit** -sivulla on varoitusviesti, jossa on seuraavat tiedot:  

-   Käsitelty varastotaso, joka laukaisi varoituksen  
-   Laskettu ylitystaso  
-   Tarjontatapahtuman eräpäivä.  

Esimerkki: Suunniteltu varasto 120 on suurempi kuin sallittu ylitys 60 kohteessa 28-01-11.  

### <a name="scenario"></a>Esimerkkitilanne  
Tässä tilanteessa asiakas muuttaa myyntitilauksen arvosta 70 kappaletta arvoksi 40 kappaletta suunnitteluajojen välillä. Ylitystoiminto alkaa vähentämään tilausta, jota ehdotettiin alkuperäiselle myyntimäärälle.  

#### <a name="item-setup"></a>Nimikkeen asetus  

|Uusintatilaustapa|Enimmäismäärä|  
|-----------------------|------------------|  
|Enimmäistilausmäärä|100|  
|Uusintatilauspiste|50|  
|Vaihto-omaisuus|80|  

#### <a name="situation-before-sales-decrease"></a>Tilanne ennen myynnin vähenemistä  

|Tapahtuma|Muuta määrä|Suunniteltu varasto|  
|-----------|-----------------|-------------------------|  
|Yksi päivä|Ei yhtään|80|  
|Myynti|-70|10|  
|Aikavälin loppu|Ei yhtään|10|  
|Ehdota uutta ostopalautustilausta|+90|100|  

#### <a name="situation-after-sales-ddecrease"></a>Tilanne myynnin vähenemisen jälkeen  

|Vaihtoraha|Muuta määrä|Suunniteltu varasto|  
|------------|-----------------|-------------------------|  
|Yksi päivä|Ei yhtään|80|  
|Myynti|-40|40|  
|Osto|+90|130|  
|Aikavälin loppu|Ei mitään|130|  
|Ehdotus tilauksen pienentämiseksi<br /><br /> tilaus arvosta 90 arvoon 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Tuloksena suunnittelurivit  
 Järjestelmä luo yhden suunnittelurivin (varoitus) oston vähentämiseksi 30 yksiköllä 90 yksiköstä 60 yksikköön, jotta arvioitu varasto on 100 sallitun ylityksen mukaan.  

![Suunnitelu sallitun ylityksen mukaan](media/nav_app_supply_planning_2_overflow2.png "Suunnitelu sallitun ylityksen mukaan")  

> [!NOTE]  
>  Ilman ylivuototoimintoa varoitusta ei luoda, jos oletetun varaston taso ylittää enimmäisvaraston. Tämä voi aiheuttaa tarpeettoman tarjonnan, joka on 30.

## <a name="handling-projected-negative-inventory"></a>Arvioidun negatiivisen varaston käsittely
Jälkitilauspiste ilmaisee ennakkokysynnän nimikkeen läpimenoajan aikana. Kun uusintatilauspiste on ohitettu, on aika tilata lisää. Mutta arvioidun varaston on oltava riittävän suuri kysynnän kattamiseksi, kunnes uusi tilaus vastaanotetaan. Tänä aikana varmuusvaraston tulisi huolehtia kysynnän vaihteluista palvelun kohdetasolle asti.  

 Näin ollen suunnittelujärjestelmä katsoo sen hätätapaukseksi, jos tulevaa kysyntää ei voida toimittaa suunnitellusta varastosta tai toisella tavalla ilmaistuna, suunniteltu varasto muuttuu negatiiviseksi. Tällaisen poikkeuksen tapahtuessa järjestelmä ehdottaa uutta toimitustilausta, joka vastaa kysyntää, jota varasto tai toinen tarjonta ei täytä. Uuden toimitustilauksen koko ei ota huomioon maksimivarastoa tai jälkitilausmäärää, eikä se ota huomioon tilauksen muokkaajia maksimitilausmäärä, minimitilausmäärä ja tilauksen moninkertaistaminen. Sen sijaan se vastaa täsmällistä puutetta.  

 Tämän tyyppisen toimitustilauksen suunnittelurivillä näytetään Hätävaroituskuvake ja lisätietoa annetaan sitä haettaessa tiedottamaan käyttäjää tilanteesta.  

 Seuraavassa kuvassa tarjonta D vastaa hätätilausta negatiivisen varaston muuttamiseksi.  

 ![Hätäsuunnitelmaehdotus negatiivisen varaston välttämiseksi](media/nav_app_supply_planning_2_negative_inventory.png "Hätäsuunnitelmaehdotus negatiivisen varaston välttämiseksi")  

1.  Tarjonta **A**, alunperin suunniteltu varasto, on jälkitilauspisteen alapuolella.  
2.  Luodaan uusi eteenpäin aikataulutettu tarjonta (**C**).  

     (Määrä = enimmäisvarasto – suunniteltu varastotaso)  
3.  Tarjonta **A** on suljettu kysynnän **B** johdosta, jota ei täysin katettu.  

     (Tarjonta **B** voi yrittää aikatauluttaa tarjontaa C, mutta se ei tapahdu aikavälikäsitteen mukaisesti.)  
4.  Uusi tarjonta (**D**) on luotu kattamaan jäljellä olevan määrän kysynnässä **B**.  
5.  Kysyntä **B** on suljettu (luodaan muistutusta suunniteltuun varastoon).  
6.  Uusi tarjonta **D** on suljettu.  
7.  Suunniteltu varasto on valittuna; uusintatilauspistettä ei ole ylitetty.  
8.  Tarjonta **C** on suljettu (kysyntää ei enää ole).  
9. Lopullinen tarkastus: avoimia varaston tason muistutuksia ei ole olemassa.  

> [!NOTE]  
>  Vaihe 4 kuvaa sitä, miten järjestelmä reagoi versiota Microsoft Dynamics NAV 2009 SP1 edeltävissä versioissa.  

Tämä päättää uusintatilaustapoihin perustuvaan varaston suunnitteluun liittyvien keskeisten periaatteiden kuvauksen. Seuraavassa osassa kuvataan neljän tuetun jälkitilausohjeen ominaisuudet.

## <a name="reordering-policies"></a>Uusintatilauskäytännöt
Uusintatilausohjeet määrittävät sen, kuinka paljon tilataan, kun nimikkeitä tarvitaan lisää. Käytössä on neljä erilaista uusintatilaustapaa.  

### <a name="fixed-reorder-qty"></a>Kiinteä uusintatil. määrä
Kiinteä uusintatilausmäärän menettely liittyy tyypillisten C-nimikkeiden varaston suunnitteluun (alhaiset varastokustannukset, vanhenemisriski ja/tai useita nimikkeitä) Tätä menetelmää käytetään yleensä silloin, kun tilauspiste vaikuttaa odotettuun kysyntään nimikkeen toimitusajan aikana.  

#### <a name="calculated-per-time-bucket"></a>Laskettu aikavälikohtaisesti  
Jos suunnittelujärjestelmä havaitsee, että lisätilauspiste on saavutettu tai se ylitetään määritetyllä aikajaksolla (lisätilausjaksolla) (arvo ylittää lisätilauspisteen tai on sen tasolla jakson alussa tai arvo on lisätilauspisteen alapuolella tai sen tasolla jakson lopussa), järjestelmä ehdottaa uuden toimitustilauksen luomista määritetyllä lisätilausmäärällä. Järjestelmä ehdottaa myös aikataulun siirtämistä eteenpäin aikajakson loppumista seuraavasta päivästä.  

Jaksotettu jälkitilauspisteen konsepti vähentää tarjontaehdotusten määrää. Tämä vaikuttaa säännöllisesti suoritettavaan manuaaliseen prosessiin eli varaston läpi kävelyyn ja eri varastopaikkojen todellisen sisällön tarkistamiseen.  

#### <a name="creates-only-necessary-supply"></a>Luo vain tarvittavan kysynnän  
Ennen uuden toimitustilauksen ehdottamista uusintatilauspisteen täyttämiseksi suunnittelujärjestelmä tarkistaa, onko toimitus jo tilattu vastaanotettavaksi nimikkeen toimitusaikana. Jos olemassa oleva toimitustilaus ratkaisee ongelman muuttamalla suunnitellun varaston uusintatilauspisteeseen tai sen yläpuolelle toimitusaikana, järjestelmä ei ehdota uutta toimitustilausta.  

Toimitustilaukset, jotka on luoto erityisesti kohtaamaan jälkitilaustarve, poistetaan tavanomaisesta tarjonnan tasapainotuksesta, eikä niitä voida mitenkään muuttaa jälkeenpäin. Näin ollen, jos uusintatilauspiste poistetaan (ei uusita), tällöin on suositeltavaa tarkistaa avoimet toimitustilaukset manuaalisesti tai muuttaa uusintatilaustapa arvoon erä-erästä, jolloin järjestelmä vähentää tai peruuttaa tarpeettoman tarjonnan.  

#### <a name="combines-with-order-modifiers"></a>Yhdistää tilausmääritteiden kanssa  
Tilauksen muokkaajien, minimitilausmäärä, maksimitilausmäärä ja tilauksen moninkertaistaminen, ei tulisi näytellä isoa roolia, kun käytetään kiinteää jälkitilausmäärätapaa. Koska suunnittelujärjestelmä ottaa edelleen nämä muuttujat huomioon ja vähentää määrän määritettyyn enimmäistilausmäärään (ja luo kaksi toimitusta tai useampia kokonaistilausmäärän saavuttamiseksi), kasvata tilausta määritettyyn vähimmäistoimituksen määrään tai pyöristä tilausmäärä ylös määritetyn tilauskerrannaisen kattamiseksi.  

#### <a name="combines-with-calendars"></a>Yhdistäminen kalentereihin  
Ennen kuin uusintatilauspisteen täyttämiseen ehdotetaan uutta toimitustilausta, suunnittelujärjestelmä tarkistaa, onko tilaus ajoitettu **Yritystiedot**- ja **Sijaintikortti**-sivujen **Peruskalenterin koodi** -kentässä määritettyjen kalenterien mukaiselle ei-työskentelypäivälle.  

Jos suunniteltu päivämäärä ei ole työpäivä, suunnittelujärjestelmä siirtää tilauksen seuraavalle työpäivälle. Tämä voi johtaa tilaukseen, joka täyttää uusintatilauspisteen, mutta ei täytä mitään tiettyä kysyntää. Suunnittelujärjestelmä luo ylimääräisen tarjonnan vastaamaan epätasapainoiseen kysyntään.  

#### <a name="should-not-be-used-with-forecast"></a>Ei tule käyttää ennusteen kanssa  
Koska oletettu kysyntä on jo ilmaistu uusintatilauspisteen tasolla, ennusteen liittäminen nimikkeen suunnitteluun uusintatilauspisteen avulla ei ole tarpeellista. Jos suunnitelman perustaminen ennusteeseen on asianmukaista, käytä erä-erästä-käytäntöä.  

#### <a name="must-not-be-used-with-reservations"></a>Ei tule käyttää varausten kanssa  
Jos käyttäjä on varannut määrän, esimerkiksi varastossa olevan määrän jollekin tulevaisuudessa tapahtuvalle kysynnälle, suunnitelman perusta häiriintyy. Vaikka oletettu saatavilla oleva varasto on hyväksyttävä suhteessa uusintatilauspisteeseen, määrät eivät ehkä ole käytettävissä varauksen vuoksi. Järjestelmä voi yrittää korjata tilannetta luomalla poikkeustilauksia. On kuitenkin suositeltavaa määrittää niiden nimikkeiden Varaa-kentän arvoksi Ei koskaan, jotka on suunniteltu käyttämällä uusintatilauspistettä.

### <a name="maximum-qty"></a>Enimmäismäärä
Enimmäismääräkäytäntö on tapa ylläpitää varastoa uudelleentilauspisteen avulla.  

Kaikki kiinteää uusintatilausmäärän käytäntöä koskeva koskee myös tätä käytäntöä. Ainoa ero on ehdotetun tarjonnan määrä. Kun käytetään enimmäismääräkäytäntöä, uusintatilausmäärä määritetään dynaamisesti oletetun varaston tason perusteella. Sen vuoksi se yleensä on eri kuin tilausten välinen määrä.  

#### <a name="calculated-per-time-bucket"></a>Laskettu aikavälikohtaisesti  
Jälkitilausmäärä määritetään siihen ajankohtaan (ajanjakson loppu), kun suunnittelujärjestelmä havaitsee, että jälkitilauspiste on ylitetty. Tällä hetkellä järjestelmä mittaa välin nykyisestä arvioidusta varastotasosta määritettyyn enimmäisvarastoon asti. Tämä kuvaa määrää, joka tulisi järjestää uudelleen. Järjestelmä tarkistaa, onko tarjonta jo tilattu muualle vastaanotettavaksi nimikkeen toimitusaikana. Jos näin on, järjestelmä pienentää uuden toimitustilauksen määrää jo tilattujen määrien verran.  

Järjestelmä varmistaa, että oletettu varasto saavuttaa vähintään uusintatilauspisteen tason. Tämä tehdään siltä varalta, että käyttäjä unohtaa määrittää varaston enimmäismäärän.  

#### <a name="combines-with-order-modifiers"></a>Yhdistää tilausmääritteiden kanssa  
Asetuksesta riippuen saattaa olla parasta yhdistää enimmäismäärän käytäntö tilauksen muuttujien kanssa, jotta varmistetaan tilauksen vähimmäismäärä tai sen pyöristäminen oston mittayksikön kokonaislukuun, tai jotta se jaetaan useampiin eriin tilauksen enimmäismäärän määrityksen mukaan.  

### <a name="combines-with-calendars"></a>Yhdistäminen kalentereihin  
Ennen kuin uusintatilauspisteen täyttämiseen ehdotetaan uutta toimitustilausta, suunnittelujärjestelmä tarkistaa, onko tilaus ajoitettu **Yritystiedot**- ja **Sijaintikortti**-sivujen **Peruskalenterin koodi** -kentässä määritettyjen kalenterien mukaiselle ei-työskentelypäivälle.  

Jos suunniteltu päivämäärä ei ole työpäivä, suunnittelujärjestelmä siirtää tilauksen seuraavalle työpäivälle. Tämä voi johtaa tilaukseen, joka täyttää uusintatilauspisteen, mutta ei täytä mitään tiettyä kysyntää. Suunnittelujärjestelmä luo ylimääräisen tarjonnan vastaamaan epätasapainoiseen kysyntään.

### <a name="order"></a>Järjestys
Tilausohjautuvassa ympäristössä nimike ostetaan tai tuotetaan yksinomaan kattamaan tiettyä kysyntää. Yleensä tämä liittyy A-nimikkeisiin. Tämä uusintatilaustapa valitaan esimerkiksi silloin, kun kysyntä ei ole säännöllistä, toimitusajalla ei ole merkitystä tai pakolliset määritteet vaihtelevat.  

Sovellus luo tilaus tilauksesta -linkin, joka toimii alustavana yhteytenä tarjonnan, toimitustilauksen tai varaston ja sen kysynnän välillä, jonka tarjonta täyttää.  

Riippumatta tilauskäytännön käyttämisestä, tilausten välistä linkkiä voidaan käyttää suunnittelun aikana seuraavilla tavoilla:  

* Kun usean tason tai projektityyppisiä tuotantotilauksia luodaan tilausohjatun tuotantotavan avulla (tarvittavat komponentit sisältyvät samaan tuotantotilaukseen).  
* Kun myyntitilauksen suunnittelutoimintoa käytetään tuotantotilauksen luomiseksi myyntitilauksesta.  

Vaikka valmistava yritys on mielestään tilausohjattu ympäristö, on ehkä parasta käyttää erä-erästä uusintatilaustapaa, jos nimikkeet ovat täysin vakiomuotoisia ilman määritteiden variaatioita. Tämän vuoksi järjestelmä käyttää suunnittelematonta varastoa ja vain kasvattaa myyntitilauksia samalla toimituspäivämäärällä tai määritetyllä aikavälillä.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Tilausten väliset linkit ja erääntyneet määräpäivät  
Toisin kuin useimmat tarjonta- ja kysyntäjoukot, järjestelmä suunnittelee kokonaan linkitetyt tilaukset, joiden eräpäivä on ennen suunnittelun alkupäivämäärää. Liiketoimintasyy tälle poikkeukselle on se, että erityiset kysyntä-tarjonta-asetukset täytyy synkronoida tämän toimeenpanon välityksellä. Lisätietoja useimmissa kysyntä–tarjonta-tyypeissä käytettävissä jäädytetystä alueesta on kohdassa [Tilausten käsittely ennen suunnittelun aloituspäivää](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).

### <a name="lot-for-lot"></a>Erä-erästä
Erä erästä -toiminto on kaikkein joustavin, koska järjestelmä reagoi vain ajankohtaiseen kysyntään, ja se toimii ennakkokysyntänä ennusteesta ja kestotilauksista, ja ratkaisee sitten tilausmäärän perustuen kysyntään. Erä erästä -toiminto on kohdistettu A- ja B-nimikkeille, joissa varasto voidaan hyväksyä, mutta tätä tulee välttää.  

Monilla tavoilla erä-erästä käytäntö näyttää tilauskäytännöltä, mutta sillä on yleinen lähestymistapa nimikkeisiin – se voi hyväksyä varastossa olevat määrät ja se kokoaa kysynnän ja vastaavan tarjonnan käyttäjän määrittämiin aikaväleihin.  

Aikaväli määritetään **Aikaväli**-kentässä. Järjestelmän käyttämä pienin aikaväli on yksi päivä. Se on kysyntä- ja tarjontatapahtumien ajan pienin mittayksikkö järjestelmässä. Käytännössä tosin tuotantotilausten ja komponenttitarpeiden ajan mittayksikkö voidaan määrittää sekunteina.  

Aikaväli määrittää myös rajat sille, milloin olemassa oleva toimitustilaus on ajoitettava uudelleen annettua kysyntää vastaavaksi. Jos tarjonta sijoittuu aikavälille, se aikataulutetaan uudelleen sisään tai ulos kysynnän täyttämiseksi. Muussa tapauksessa, jos se on aiemmin, se aiheuttaa tarpeetonta varaston kerääntymistä ja se tulisi peruuttaa. Jos se on myöhemmin, uusi toimitustilaus luodaan sen sijaan.  

Tämän käytännön avulla voi myös määrittää varmuusvaraston mahdollisten tarjonnan vaihteluiden kompensointia tai äkillisen kysynnän täyttämistä varten.  

Koska toimitustilauksen määrä perustuu todelliseen kysyntään, voi olla järkevää käyttää tilauksen muuttujakenttiä: pyöristä tilausmäärä ylös tietyn tilauskerrannaisen määrittämiseksi (tai mitan ostoyksikön), kasvata tilausta tiettyyn tilauksen vähimmäismäärään tai vähennä määrää määritettyyn enimmäismäärään (ja luo näin kaksi tai useampia toimituksia vaadittavan kokonaismäärän saavuttamiseksi).

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
[Rakennetiedot: suunnittelun kohdistustaulukko](design-details-planning-assignment-table.md)   
[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)
