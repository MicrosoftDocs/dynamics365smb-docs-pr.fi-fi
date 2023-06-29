---
title: Rakennetiedot – uusintatilauskäytäntöjen käsittely
description: Tässä on artikkelissa on yleiskatsaus toimitusten suunnittelussa käytettävistä uusintatilauskäytännöistä.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
---
# <a name="design-details-handling-reordering-policies"></a><a name="design-details-handling-reordering-policies"></a>Rakennetiedot: uusintatilauskäytäntöjen käsittely

Nimike sisällytetään toimitusten suunnitteluun määrittämällä sen uusintatilauskäytäntö **Nimikekortti**-sivulla. Käytettävissä on seuraavat uusintatilauskäytännöt:  

* Kiinteä uusintatil. määrä  
* Enimmäismäärä  
* Järjestys  
* Erä-erästä  

**Kiinteä uusintatil. määrä**- ja **Enimmäismäärä**-käytännöt liittyvät varaston suunnitteluun. Nämä käytännöt ovat käytössä samanaikaisesti vaiheittaisten toimitusten ja tilauksen suunnittelun seurannan täsmäytyksen kanssa.  

## <a name="the-role-of-the-reorder-point"></a><a name="the-role-of-the-reorder-point"></a>Uusintatilauspisteen tehtävä

Uusintatilauspiste edustaa kysyntää toimitusaikana. Kun varastomäärän arvioidaan alittavan uusintatilauspisteelle määritetyn määrän, on aika tilata lisää. Varasto vähenee vähitellen täydennyksen saapumiseen saakka. Varasto voi vähentyä nollaan tai varmuusvaraston tasolle. Suunnittelujärjestelmä ehdottaa eteenpäin aikataulutettua toimitustilausta kohdassa, jossa varasto alittaa uusintatilauspisteen.  

Varastomäärät voivat vaihdella merkittävästi aikavälin aikana. Suunnittelujärjestelmä seuraa varastoa tämän vuoksi jatkuvasti.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a><a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Suunnitellun varastomäärän ja uusintatilauspisteen seuranta

Varasto on tarjonnan tyyppi mutta varaston suunnittelussa suunnittelujärjestelmä erottaa kaksi varastotasoa:  

* Suunniteltu varasto  
* Oletettu saatavilla oleva varasto  

### <a name="projected-inventory"></a><a name="projected-inventory"></a>Suunniteltu varasto

Suunnitteluprosessin alussa suunniteltu varasto on varaston bruttomäärä. Bruttomäärä sisältää aiemman kirjatun ja kirjaamattoman kysynnän ja tarjonnan. Tästä määrästä tulee suunniteltu varastomäärä, jota ylläpidetään tulevan kysynnän ja tarjonnan bruttomäärien avulla. Tuleva kysyntä ja tarjonta otetaan käyttöön aikajanalla, jossa se on joko varattu tai kohdistettu muilla tavoin.  

Suunnittelujärjestelmä seuraa suunnitellun varaston avulla uusintatilauspistettä ja määrittää uusintatilausmäärän **Enimmäismäärä**-uusintatilauskäytännön avulla.  

### <a name="projected-available-inventory"></a><a name="projected-available-inventory"></a>Oletettu saatavilla oleva varasto

Oletettu saatavilla oleva varasto on varasto, joka on tiettyyn aikaan saatavilla kysynnän täyttämistä varten. Suunnittelujärjestelmä käyttää oletettua saatavilla olevaa varastoa varmuusvaraston tason seurantaan. Varmuusvarastoa on oltava aina saatavilla odottamatonta kysyntää varten.  

### <a name="time-buckets"></a><a name="time-buckets"></a>Aikavälit

Suunniteltu varasto on tärkeä uusintatilauspisteen tunnistamisessa sekä oikean tilausmäärän laskemisessa **Enimmäismäärä**-uusintatilauskäytäntöä käytettäessä.  

Suunniteltu varastomäärä lasketaan suunnittelujakson alussa. Se on bruttotaso, joka ei ota huomioon varauksia tai muita kohdistuksia. Suunniteltujärjestelmä seuraa tätä varastomäärää suunnittelujakson aikana seuraamalla tietyn ajan aikana koottuja muutoksia. Tätä jatkoa kutsutaan *aikaväliksi*. Lisätietoja aikaväleistä on kohdassa [Aikavälit](#time-buckets). Suunnittelujärjestelmä varmistaa, että aikaväli on vähintään yksi päivä. Yksi päivä on kysyntä- tai tarjontatapahtumien vähimmäisaika.  

### <a name="determining-the-projected-inventory-level"></a><a name="determining-the-projected-inventory-level"></a>Suunnittelun varastomäärän määrittäminen

Seuraavaksi käsitellään tapaa, jolla suunnittelujärjestelmä määrittää suunnitellun varastomäärän:  

* Kun tarjontatapahtuma, kuten ostotilaus, on kokonaan suunniteltu, se kasvattaa suunniteltua varastoa tapahtuman eräpäivänä.  
* Kokonaan täytetty kysyntätapahtuma ei vähennä suunniteltua varastoa heti. Se kirjaa sen sijaan vähennysmuistutuksen eli sisäisen tietueen, joka sisältää päivämäärän ja suunniteltuun varastoon lisättävän määrän.  
* Kun tarjontatapahtuma suunnitellaan ja lisätään aikajanalle myöhemmin, järjestelmä tarkistaa suunnitellulle toimituspäivälle kirjatut vähennysmuistutukset yksi kerrallaan. Tämän prosessin aikana sisäisen lisäysmuistutuksen uusintatilaustaso saatetaan saavuttaa tai ylittää.  
* Jos uusi toimitustilaus otetaan käyttöön, se tarkistaa, onko se syötetty ennen nykyistä tarjousta. Jos näin on, uudesta tarjonnasta tulee nykyinen tarjonta ja täsmäytys käynnistyy uudelleen.  

Seuraavassa kuvassa käytetään tätä periaatetta.  

![Arvioidun varastomäärän määrittäminen.](media/nav_app_supply_planning_2_projected_inventory.png "Arvioidun varastotason määrittäminen")  

1. Määrän 4 tarjonta **Sa** (kiinteä) sulkee kysynnän **Da** määrällä -3.  
2. CloseDemand: Luo vähennyksen muistutus -3 (ei näkyvillä).  
3. Tarjonta **Sa** on suljettu ylijäämällä 1 (ei enää kysyntää).  

     Suunniteltu varastomäärä kasvaa arvoon  +4, kun taas oletetun **saatavilla** olevan varaston arvoksi tulee -1.  

4. Seuraava määrältään 2 tarjonta **Sb** (toinen tilaus) on jo asetettu aikajanalle.  
5. Suunnittelujärjestelmä tarkistaa mahdolliset vähennysmuistutukset tarjontaa **Sb** (tässä esimerkissä sitä ei ole, joten mitään ei tehdä).  
6. Suunnittelujärjestelmä sulkee tarjonnan **Sb** (ei enää kysyntää) joko A: vähentämällä sen nollaan (peruutus) tai B: jättämällä sen ennalleen.  

     Suunniteltu varastomäärä kasvaa (A: +0 => +4 tai B: +2 = +6).  

7. Suunnitelmajärjestelmä tekee viimeisen tarkistuksen. Onko käsiteltäviä vähennysmuistutuksia? Kyllä, löytyy yksi päivämääränä **Da**.  
8. Suunnittelujärjestelmä lisää vähennysmuistutuksen (-3) suunniteltuun varastomäärään seuraavasti: A: +4 -3 = 1 tai B: +6 -3 = +3.  
9. Tapauksessa A suunnittelujärjestelmä luo eteenpäin aikataulutetun tilauksen, jonka aloituspäivämäärä on **Da**. Tapauksessa B uusintatilauspiste on saavutettu ja uusi tilaus luodaan.

## <a name="the-role-of-the-time-bucket"></a><a name="the-role-of-the-time-bucket"></a>Aikavälin tehtävä

Aikavälin tarkoitus on kerätä kysyntätapahtumia aikaikkunan sisällä, jotta yhteinen toimitustilaus voidaan tehdä.  

Uusintatilauspistettä käyttävien uusintatilaustapojen kohdalla voit määrittää aikavälin. Aikavälien avulla voidaan varmistaa, että samalle aikajaksolle sijoittuvat kysynnät kootaan. Järjestelmä tarkistaa sitten vaikutuksen suunniteltuun varastoon ja mahdollisen uusintatilauspisteen ohituksen.

Jos uusintatilauspiste ohitetaan, järjestelmä aikatauluttaa tulevaisuuteen uuden toimitustilauksen aikavälin lopusta. Aikavälit alkavat suunnittelun aloituspäivämäärästä.  

Aikavälikäsite vastaa varastomäärän manuaalisesti tehtävää säännöllistä tarkistusprosessia; se ei siis tarkoita tarkistamista kunkin tapahtuman osalta. Tarkistusväli (aikaväli) määritetään itse. Esimerkiksi kaikki toimittajan nimiketarpeet voidaan kerätä viikoittaiseen tilaukseen.  

![Esimerkki aikavälistä suunnittelussa.](media/nav_app_supply_planning_2_reorder_cycle.png "Esimerkki aikavälistä suunnittelussa")  

Aikavälejä käytetään usein limittäisyyden välttämiseksi. Esimerkiksi täsmäytetty kysynnän ja tarjonnan rivi, jossa aikainen kysyntä on peruutettu tai uusi luodaan. Tuloksena on, että jokainen toimitustilaus (paitsi viimeisin) aikataulutetaan uudelleen.

## <a name="stay-below-the-overflow-level"></a><a name="stay-below-the-overflow-level"></a>Sallitun ylityksen alapuolella pysyminen

**Enimmäismäärä**- ja **Kiinteä uusintatil. määrä** -uusintatilauskäytäntöjä käytettäessä suunnittelujärjestelmä keskittyy suunniteltuun varastoon vain annetulla aikavälillä. On mahdollista, että lisätarjontaa ehdotetaan, kun aikavälin ulkopuolella tapahtuu negatiivisia kysynnän tai positiivisia tarjonnan muutoksia. Lisätarjontaa varten suunnittelujärjestelmä laskee määrän, jolla tarjontaa on vähennettävä. Tätä määrää kutsutaan ylivuototasoksi. Ylitys on käytettävissä suunnittelurivinä, jossa on **Muuta määrä (vähennys)**- tai **Peruuta**-toiminto ja seuraava varoitus:  

* Huomio: arvioitu varastomäärä [xx] on korkeampi kuin sallittu ylitys [xx] eräpäivänä [xx].*  

![Varaston sallittu ylitys.](media/supplyplanning_2_overflow1_new.png "Varaston sallittu ylitys")  

### <a name="calculating-the-overflow-level"></a><a name="calculating-the-overflow-level"></a>Sallitun ylityksen laskeminen

Sallittu ylitys lasketaan eri tavoin uusintatilauskäytännön mukaan.  

#### <a name="maximum-qty"></a><a name="maximum-qty"></a>Enimmäismäärä

Sallittu ylitys = enimmäisvarasto  

> [!NOTE]  
> Jos käytössä on vähimmäistilausmäärä, se lisätään seuraavasti:
>
> sallittu ylitys = enimmäisvarasto + vähimmäistilausmäärä.  

#### <a name="fixed-reorder-qty"></a><a name="fixed-reorder-qty"></a>Kiinteä uusintatil. määrä

sallittu ylitys = uusintatilausmäärä + uusintatilauspiste  

> [!NOTE]  
> Jos vähimmäistilausmäärä on suurempi kuin uusintatilauspiste, se korvataan seuraavasti:
>
> sallittu ylitys = uusintatilausmäärä + vähimmäistilausmäärä  

#### <a name="order-multiple"></a><a name="order-multiple"></a>Tilauskerrannainen

Jos tilauskerrannainen on olemassa, se säätää sekä enimmäismäärän että kiinteän uusintatilausmäärän uusintatilauskäytännön sallittua ylitystä.  

### <a name="creating-the-planning-line-with-an-overflow-warning"></a><a name="creating-the-planning-line-with-an-overflow-warning"></a>Ylitysvaroituksen sisältävän suunnittelurivin luominen

Suunnittelurivi luodaan, kun suunniteltu varasto on aikavälin lopussa tarjonnan vuoksi suurempi kuin sallittu ylitys. Ylimääräisestä tarjonnasta varoitettaessa suunnittelurivillä on varoitussanoma, **Hyväksy toimenpideviesti** -kenttää ei ole valittu ja toimenpidesanoma on joko **Peruuta** tai **Muuta määrä**.  

#### <a name="calculating-the-planning-line-quantity"></a><a name="calculating-the-planning-line-quantity"></a>Suunnittelurivin määrän laskeminen

Suunnittelurivillä oleva määrä lasketaan seuraavasti:

suunnittelurivin määrä = nykyisen tarjonnan määrä – (suunniteltu varasto – sallittu ylitys)  

> [!NOTE]  
> Kaikkien muiden varoitusrivien tavoin tilauksen enimmäis- ja vähimmäismäärät sekä tilauskerrannainen ohitetaan.  

#### <a name="defining-the-action-message-type"></a><a name="defining-the-action-message-type"></a>Toimenpidesanoman tyypin määrittäminen

* Jos suunnittelurivin määrä on suurempi kuin 0, toimenpidesanoma on **Muuta määrä.**  
* Jos suunnittelurivin määrä on yhtä suuri tai pienempi kuin 0, toimenpidesanoma on **Peruuta**  

#### <a name="composing-the-warning-message"></a><a name="composing-the-warning-message"></a>Varoitussanoman luominen

Ylivuototilanteessa **Ei-seuratut suunnitteluelementit** -sivulla on varoitussanoma, jossa on seuraavat tiedot:  

* Käsitelty varastotaso, joka laukaisi varoituksen  
* Laskettu ylitystaso  
* Tarjontatapahtuman eräpäivä  

Esimerkki: Suunniteltu varasto 120 on suurempi kuin sallittu ylitys 60 kohteessa 01-28-23.  

### <a name="example-scenario"></a><a name="example-scenario"></a>Esimerkkiskenaario

Tässä tilanteessa asiakas muuttaa myyntitilauksen arvosta 70 kappaletta arvoksi 40 kappaletta suunnitteluajojen välillä. Ylitystoiminto vähentää ostoa, jota ehdotettiin alkuperäiselle myyntimäärälle.  

#### <a name="item-setup"></a><a name="item-setup"></a>Nimikkeen asetus

|Uusintatilaustapa|Enimmäismäärä|  
|-----------------------|------------------|  
|Enimmäistilausmäärä|100|  
|Uusintatilauspiste|50|  
|Varasto|80|  

#### <a name="situation-before-sales-decrease"></a><a name="situation-before-sales-decrease"></a>Tilanne ennen myynnin vähenemistä

|Tapahtuma|Muuta määrä|Suunniteltu varasto|  
|-----------|-----------------|-------------------------|  
|Yksi päivä|Ei mitään|80|  
|Myynti|-70|10|  
|Aikavälin loppu|Ei mitään|10|  
|Ehdota uutta ostopalautustilausta|+90|100|  

#### <a name="situation-after-sales-decrease"></a><a name="situation-after-sales-decrease"></a>Tilanne myynnin vähenemisen jälkeen

|Vaihtoraha|Muuta määrä|Suunniteltu varasto|  
|------------|-----------------|-------------------------|  
|Yksi päivä|Ei mitään|80|  
|Myynti|-40|40|  
|Osto|+90|130|  
|Aikavälin loppu|Ei mitään|130|  
|Ehdotus tilauksen pienentämiseksi<br><br> tilaus arvosta 90 arvoon 60|-30|100|  

#### <a name="resulting-planning-lines"></a><a name="resulting-planning-lines"></a>Tuloksena olevat suunnittelurivit

Järjestelmä luo varoitussuunnittelurivin vähentämään ostoa 30 yksiköllä 90 yksiköstä 60 yksikköön, jotta suunniteltu varasto pysyy 100 yksikössä sallitun ylityksen mukaisesti.  

![Suunnitelu sallitun ylityksen mukaan.](media/nav_app_supply_planning_2_overflow2.png "Suunnitelu sallitun ylityksen mukaan")  

> [!NOTE]  
> Jos ylitystoiminta ei ole, varoitusta ei luoda suunnitellun varastomäärän ylittäessä enimmäismäärän, minkä seurauksena voi olla 30 yksikön ylitarjonta.

## <a name="handling-projected-negative-inventory"></a><a name="handling-projected-negative-inventory"></a>Suunnitellun negatiivisen varaston käsittely

Jälkitilauspiste ilmaisee ennakkokysynnän nimikkeen läpimenoajan aikana. Suunnittelun varaston on oltava riittävän suuri kattamaan kysyntä uuden tilauksen vastaanottamiseen saakka. Tänä aikana varmuusvaraston tulisi huolehtia kysynnän vaihteluista palvelun kohdetasolle asti.  

Suunnittelujärjestelmä pitää hätätilanteena sitä, että tulevaa kysyntää ei voida täyttää suunnittelusta varastosta. Asia voidaan ilmaista myös toteamalla, että suunniteltu varasto muuttuu negatiiviseksi. Järjestelmä ehdottaa uuden toimitustilauksen luomista kattamaan se kysynnän osa, jota ei voida täyttää. Uuden toimitustilauksen koko ei ota huomioon enimmäisvarastoa tai uudelleentilausmäärää eikä seuraavia tilausmääritteitä:

* Enimmäistilausmäärä
* Vähimmäistilausmäärä
* Tilauskerrannainen 

Se vastaa sen sijaan täsmälleen puutetta.  

Tämän tyyppisen toimitustilauksen suunnittelurivillä näkyy **Hätätilanne**-varoituskuvake ja lisätietoja tilanteesta.  

Seuraavassa kuvassa tarjonta D vastaa negatiivisen varaston oikaisevaa hätätilausta.  

![Hätäsuunnitelmaehdotus negatiivisen varaston välttämiseksi.](media/nav_app_supply_planning_2_negative_inventory.png "Hätäsuunnitelmaehdotus negatiivisen varaston välttämiseksi")  

1. Tarjonta **A**, alunperin suunniteltu varasto, on jälkitilauspisteen alapuolella.  
2. Luodaan uusi eteenpäin aikataulutettu tarjonta (**C**).  

     (määrä = enimmäisvarasto – suunniteltu varastomäärä)  
3. Tarjonta **A** on suljettu kysynnän **B** johdosta, jota ei täysin katettu.  

     (Kysyntä **B** voi yrittää aikatauluttaa tarjontaa C, mutta aikaväli estää sen.)  
4. Uusi tarjonta (**D**) on luotu kattamaan jäljellä olevan määrän kysynnässä **B**.  
5. Kysyntä **B** on suljettu (luodaan muistutusta suunniteltuun varastoon).  
6. Uusi tarjonta **D** on suljettu.  
7. Suunniteltu varasto tarkistetaan. Uusintatilauspistettä ei ole ylitetty.  
8. Tarjonta **C** on suljettu (ei enää kysyntää).  
9. Viimeinen tarkistus. Avoimia varastomäärämuistutuksia ei ole.  

Seuraavassa osassa kuvataan neljän tuetun jälkitilausohjeen ominaisuudet.

## <a name="reordering-policies"></a><a name="reordering-policies"></a>Uusintatilauskäytännöt

Uusintatilausohjeet määrittävät sen, kuinka paljon tilataan, kun nimikkeitä tarvitaan lisää. Käytössä on neljä erilaista uusintatilaustapaa.  

### <a name="fixed-reorder-quantity"></a><a name="fixed-reorder-quantity"></a>Kiinteä uusintatilausmäärä

Kiinteän uusintatilausmäärän käytäntöä käytetään yleensä, kun varastosuunnittelun kohteena olevilla nimikkeillä on seuraavat ominaisuudet:

* Alhaiset varastokustannukset
* Vähäinen vanhentumisriski
* Vähäinen nimikkeiden määrä

Tätä käytäntöä käytetään yleensä silloin, kun uusintatilauspiste vastaa odotettua kysyntää nimikkeen toimitusajan aikana.  

#### <a name="calculated-per-time-bucket"></a><a name="calculated-per-time-bucket"></a>Laskettu aikavälikohtaisesti

Jos uusintatilauspiste saavutetaan tai ylitetään aikavälillä (uusintatilausvälillä), järjestelmä ehdottaa kahta toimenpidettä:

* Uuden toimitustilauksen luontia uusintatilausmäärälle
* Tilauksen aikatauluttamista tulevaisuuteen ensimmäisenä aikavälin päättymisen jälkeisenä päivänä  

Aikavälin uudelleentilauspiste vähentää tarjontaehdotusten määrää. Se vastaa prosessia, jossa varaston varastopaikkojen todellinen sisältö tarkistetaan manuaalisesti.  

#### <a name="creates-only-necessary-supply"></a><a name="creates-only-necessary-supply"></a>Vain tarvittavan tarjonnan luonti

Suunnittelujärjestelmä tarkistaa seuraavat tarjonnan osalta ennen uudelleentilauspistettä vastaavan uuden toimitustilauksen ehdottamista:

* Onko tarjonta jo tilattu?
* Odotetaanko tarjonnan saapuvan nimikkeen toimitusajan aikana?

Järjestelmä ei ehdota uutta toimitustilausta, jos tarjonta tuo suunnittelun varaston uusintatilauspisteeseen toimitusajan aikana.  

Nimenomana uusintatilauspisteeseen kohdistuvat toimitustilaukset jätetään tarjonnan täsmäytyksen ulkopuolelle, eikä niitä muuteta. Jos uudelleentilauspisteen sisältävä nimike halutaan poistaa vähitellen käytöstä, avoimet toimitustilaukset on tarkistettava manuaalisesti tai uusintatilauskäytännöksi on vaihdetta **Erä-erästä**. Järjestelmä vähentää tai peruuttaa ylimääräisen tarjonnan.  

#### <a name="combines-with-order-modifiers"></a><a name="combines-with-order-modifiers"></a>Yhdistää tilausmääritteiden kanssa

Vähimmäistilausmäärä, enimmäistilausmäärä ja tilauskerrannainen ovat tilausmääritteitä, joilla ei pitäisi olla merkittävää vaikutusta kiinteän uusintatilausmäärän käytäntöä käytettäessä. Suunnittelujärjestelmä ottaa ne kuitenkin huomioon:

* Määrän vähentäminen määritettyyn enimmäistilausmäärään (ja vähintään kahden toimituksen luominen kokonaistilausmäärän saavuttamiseksi)
* Tilauksen kasvattaminen määritettyyn vähimmäistilausmäärään.
* Tilausmäärän pyöristäminen määritettyä tilauskerrannaista vastaavaksi.  

#### <a name="combines-with-calendars"></a><a name="combines-with-calendars"></a>Yhdistäminen kalentereihin

Ennen kuin suunnittelujärjestelmä ehdottaa uusintatilauspistettä vastaavaa uutta toimitustilausta, se tarkistaa, onko tilaus aikataulutettu muulle kuin työpäivälle. Se käyttää kalenteria, joka määritetään **Yritystiedot**- ja **Sijaintikortti**-sivujen **Peruskalenterin koodi** -kentässä.  

Jos aikataulutettu päivämäärä ei ole työpäivä, suunnittelujärjestelmä siirtää tilauksen seuraavaan työpäivään. Päivämäärän siirtäminen voi johtaa tilaukseen, joka täyttää uusintatilauspisteen mutta ei täytä tiettyä kysyntää. Suunnittelujärjestelmä luo ylimääräisen tarjonnan vastaamaan epätasapainoiseen kysyntään.  

#### <a name="shouldnt-be-used-with-forecasts"></a><a name="shouldnt-be-used-with-forecasts"></a>Ei tule käyttää ennusteen kanssa

Koska oletettu kysyntä on jo ilmaistu uusintatilauspisteen tasolla, ennustetta ei tarvitse sisällyttää suunnitteluun. Jos suunnitelman on syytä pohjautua ennusteeseen, käytettävissä on **Erä-erästä**-käytäntö.  

#### <a name="must-not-be-used-with-reservations"></a><a name="must-not-be-used-with-reservations"></a>Ei tule käyttää varausten kanssa

Jos esimerkiksi varastossa oleva määrä on varattu kaukana tulevaisuudessa olevaa kysyntää varten, suunnittelun perusta voi häiriintyä. Vaikka oletettu saatavilla oleva varasto on hyväksyttävä suhteessa uusintatilauspisteeseen, määrät eivät ehkä ole käytettävissä varauksen vuoksi. Järjestelmä voi yrittää korjata tilannetta luomalla poikkeustilauksia. Sellaisten nimikkeiden **Varaa**-kentän arvoksi kannattaa määrittää **Ei koskaan**, jotka on suunniteltu käyttämällä uusintatilauspistettä.

### <a name="maximum-quantity"></a><a name="maximum-quantity"></a>Enimmäismäärä

Maksimimääräohjeet on tapa ylläpitää varastoa käyttämällä jälkitilauspistettä.  

Kaikki kiinteää uusintatilausmäärän käytäntöä koskeva koskee myös tätä käytäntöä. Ainoa ero on ehdotetun tarjonnan määrä. Enimmäismääräkäytäntöä käytettäessä uusintatilausmäärä määritetään dynaamisesti suunnitellun varastomäärän perusteella. Tämän vuoksi se yleensä vaihtelee tilauskohtaisesti.  

#### <a name="calculate-per-time-bucket"></a><a name="calculate-per-time-bucket"></a>Laskettu aikavälikohtaisesti

Kun uudelleentilauspiste saavutetaan tai ylitetään, järjestelmä määrittää uudelleentilausmäärän aikavälin päättyessä. Se mittaa tämän hetkisen varastomäärän ja määritetyn enimmäismäärän välisen eron sekä määrittää näin tilattavan määrän. Sen jälkeen järjestelmä tarkistaa seuraavat:

* Onko tarjonta jo tilattu?
* Odotetaanko tarjonnan saapuvan nimikkeen toimitusajan aikana?

Siinä tapauksessa järjestelmä vähentää uuden toimitustilauksen määrää jo tilatulla määrällä.  

Jos varaston enimmäismäärää ei määritetä, suunnittelujärjestelmä varmistaa, että suunniteltu varasto saavuttaa uudelleentilausmäärän.

#### <a name="combine-with-order-modifiers"></a><a name="combine-with-order-modifiers"></a>Yhdistäminen tilausmääritteiden kanssa

Määritysten mukaan saattaa on järkevintä yhdistää enimmäismääräkäytäntö muihin tilausmääritteisiin: 

* Vähimmäistilausmäärän varmistaminen
* Määrän pyöristäminen oston mittayksikön kokonaislukuun
* Määrän jakaminen enimmäistilausmäärän määrittämiin eriin  

### <a name="combine-with-calendars"></a><a name="combine-with-calendars"></a>Yhdistäminen kalentereihin

Ennen kuin suunnittelujärjestelmä ehdottaa uusintatilauspistettä vastaavaa uutta toimitustilausta, se tarkistaa, onko tilaus aikataulutettu muulle kuin työpäivälle. Se käyttää kalenteria, joka määritetään **Yritystiedot**- ja **Sijaintikortti**-sivujen **Peruskalenterin koodi** -kentässä.  

Jos aikataulutettu päivämäärä ei ole työpäivä, suunnittelujärjestelmä siirtää tilauksen seuraavaan työpäivään. Päivämäärän siirtäminen voi johtaa tilaukseen, joka täyttää uusintatilauspisteen mutta ei täytä tiettyä kysyntää. Suunnittelujärjestelmä luo ylimääräisen tarjonnan vastaamaan epätasapainoiseen kysyntään.

### <a name="order"></a><a name="order"></a>Järjestys

Tilausohjautuvassa ympäristössä nimike ostetaan tai tuotetaan kattamaan tietty kysyntä. Tilauksen uusintatilauskäytäntöä käytetään nimikkeissä, joilla on seuraavat ominaisuudet:

* Kysyntä on epäsäännöllistä
* Toimitusajalla ei ole merkitystä
* Pakolliset määritteet vaihtelevat  

[!INCLUDE [prod_short](includes/prod_short.md)] tilausten välisen linkin, joka toimii alustavana tarjonnan (toimitustilaus tai varasto) ja kysynnän välisenä yhteytenä. Tilausten välistä linkkiä voi käyttää suunnittelun aikana seuraavasti:  

* Kun usean tason tai projektityyppisiä tuotantotilauksia luodaan tilausohjatun tuotantokäytännön avulla (tarvittavat komponentit tuotetaan samassa tuotantotilaukseen).  
* Kun myyntitilauksen suunnittelua käytetään luomaan tuotantotilaus luomiseksi myyntitilauksesta.  

> [!TIP]
> Jos nimikemääritteet eivät vaihtele, paras vaihtoehto voi olla Erä-erästä-uudelleentilauskäytäntö. Tämän vuoksi järjestelmä käyttää suunnittelematonta varastoa ja kasvattaa vain myyntitilauksia, joilla on sama toimituspäivämäärä tai jotka ovat määritetyllä aikavälillä.  

#### <a name="order-to-order-links-and-past-due-dates"></a><a name="order-to-order-links-and-past-due-dates"></a>Tilausten väliset linkit ja erääntyneet määräpäivät

Toisin kuin useimmat tarjonta- ja kysyntäjoukot, järjestelmä suunnittelee kokonaan linkitetyt tilaukset, joiden eräpäivä on ennen suunnittelun alkupäivämäärää. Tämän poikkeuksen syynä on se, että tietyt kysyntä- ja tarjontajoukot on synkronoitava. Lisätietoja useimmissa kysyntä- ja tarjontatyypeissä käytettävästä jäädytetystä alueesta on kohdassa [Suunnittelun aloituspäivämäärää edeltävien tilausten käsitteleminen](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).

### <a name="lot-for-lot"></a><a name="lot-for-lot"></a>Erä-erästä

Erä-erästä on joustavin käytäntö, sillä järjestelmä reagoi vain toteutuneeseen kysyntään. Se toimii ennusteiden ja puitetilausten odotetun kysynnän perusteella ja ratkaisee sitten tilausmäärän kysynnän perusteella. Käytäntö on tarkoitettu nimikkeille, joissa varasto voidaan hyväksyä, joskin sitä pitäisi välttää.  

Erä-erästä-käytäntö muistuttaa osittain tilauskäytäntöä, mutta se käsittelee nimikkeitä yleisesti. Se voi hyväksyä määriä varastossa, minkä lisäksi se niputtaa kysynnän ja tarjonnan määritetyllä aikavälillä.  

Aikaväli määritetään **Nimikekortti**-sivun **Aikaväli**-kentässä. Aikavälin vähimmäiskoko on yksi päivä, sillä se on [!INCLUDE [prod_short](includes/prod_short.md)]in kysyntä- ja tarjontatapahtumien pienen mittayksikkö.  

Aikaväli rajoittaa myös sitä, milloin toimitustilaus on ajoitettava uudelleen annettua kysyntää vastaavaksi. Aikavälillä oleva tarjonta aikataulutetaan uudelleen sisään tai ulos kysynnän täyttämiseksi. Aiempi kysyntä aiheuttaa ylimääräisä varastoa, ja se on peruutettava. Myöhempää tarjontaa varten luodaan uusi toimitustilaus.  

Tämän käytännön avulla voidaan määrittää varmuusvarasto kompensoimaan tarjonnan muutoksia tai äkillisen kysynnän täyttämistä.  

Koska toimitustilauksen määrä perustuu todelliseen kysyntään, tilausmääritteitä kannattaa käyttää:

* Tilausmäärän pyöristäminen tilauskerrannaista (tai oston mittayksikköä) vastaavaksi.
* Tilauksen kasvattaminen määritettyyn vähimmäistilausmäärään.
* Määrän vähentäminen määritettyyn enimmäistilausmäärään (ja näin vähintään kahden toimituksen luominen tarvittavan kokonaismäärän saavuttamiseksi)

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)  
[Rakennetiedot: suunnittelun kohdistustaulukko](design-details-planning-assignment-table.md)  
[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)  
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)  
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
