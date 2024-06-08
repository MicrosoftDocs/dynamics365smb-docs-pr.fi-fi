---
title: Rakennetiedot – kysynnän ja tarjonnan täsmäytys
description: Tässä artikkelissa käsitellään tavoitteiden priorisointia kysynnän ja tarjonnan täsmäyttämisen avulla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# <a name="design-details-balancing-supply-and-demand"></a>Rakennetiedot: kysynnän ja tarjonnan täsmäytys

Suunnittelujärjestelmän toiminnan hahmottamisen kannalta on välttämätöntä ymmärtää tavoitteiden priorisointi:  

* Kaikki kysyntä täytetään riittävällä tarjonnalla.  
* Kaikki tarjonta palvelee tarkoitusta.  

Yleisesti ottaen nämä tavoitteet saavutetaan täsmäyttämällä tarjonta ja kysyntä.  

## <a name="supply-and-demand"></a>Kysyntä ja tarjonta

Termillä *tarjonta* viitataan kaikenlaiseen positiiviseen tai saapuvaan määrään. Kyse voi olla esimerkiksi seuraavista:

* Varasto
* Ostot
* Kokoonpano
* Tuotanto
* Saapuva siirto
* Myyntipalautukset  

Termillä *kysyntä* viitataan kaikenlaiseen bruttokysyntään. Kyse voi olla esimerkiksi seuraavista:

* Myyntitilauksen nimike
* Tuotantotilauksen komponentti

[!INCLUDE [prod_short](includes/prod_short.md)] sallii myös tekniset kysyntätyypit, kuten negatiivisen varaston ja ostopalautukset.

Suunnittelujärjestelmä lajittelee kysynnän ja tarjonnan lähteet järjestämällä ne kahdella aikajanalle, joita kutsutaan varastoprofiileiksi. Yksi profiili sisältää kysyntätapahtumat ja toinen vastaavat tarjontatapahtumat. Kukin tarjontatapahtuma ilmaisee yhden tilauksen entiteetin, kuten

* myyntitilausrivin
* nimiketapahtuman
* tuotantotilausrivin.

Kun varastoprofiilit ladataan, kysyntä- ja tarjontajoukot täsmäytetään, ja tällä tavoin saadaan luettelossa olevat tavoitteet täyttävä tarjontasuunnitelma.

Varastomäärät ja suunnitteluparametrit ovat muita kysyntä- ja tarjontatyyppejä. Näissä tyypeissä tehdään integroitu täsmäytys varastonimikkeitä täytettäessä. Lisätietoja on kohdassa [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Täsmäytyskäsite lyhyesti

Kysyntää tulee asiakkailta. Täsmäytys tapahtuu luomalla ja poistamalla tarjontaa. Suunnittelujärjestelmä aloittaa kysynnästä ja siirtyy sitten taaksepäin tarjontaan.  

Varastoprofiilit sisältävät tietoja kysynnästä ja tarjonnasta, määristä ja ajoituksista. Nämä profiilit muodostavat täsmäytysasteikon kaksi puolta.  

Suunnittelun päämäärä on tasapainottaa nimikkeen kysyntä ja tarjonta sekä varmistaa näin, että tarjonta vastaa kysyntää toteuttamiskelpoisella tavalla suunnitteluparametreissa ja säännöissä tehtyjen määritysten mukaisesti.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Kysynnän ja tarjonnan tasapainottamisen yleiskatsaus":::

## <a name="process-orders-before-the-planning-start-date"></a>Suunnittelun aloituspäivämäärää edeltävien tilausten käsitteleminen

Suunnittelujärjestelmä välttää käyttökelvottomien ehdotusten näyttämisen siten, ettei se suunnittele mitään suunniteltua aloituspäivämäärää edeltävälle ajalle. Seuraava sääntö koskee kyseistä ajanjaksoa:

* Kaikki kysyntä ja tarjonta ennen suunnittelujakson aloituspäivämäärää katsotaan osaksi varastoa tai toimitetuksi.  

Muutamia poikkeuksia lukuun ottamatta suunnittelujärjestelmä ei ehdota mitään muutoksia toimitustilauksiin tänä ajanjaksona eikä luo tilauksen seurantalinkkejä kyseiselle ajanjaksolle. Säännössä on seuraavat poikkeukset:  

* Jos oletetun saatavilla olevan varaston, mukaan lukien ajankohdan kysynnän ja tarjonnan summa, on nollan alapuolella.  
* Takautuvissa tilauksissa on käytettävä sarja- tai eränumeroita.  
* Tarjonnan ja kysynnän yhdistelmä on linkitetty tilausten välisellä käytännöllä. 

Jos ensimmäinen käytettävissä oleva varasto on alle nollan, suunnittelujärjestelmä ehdottaa puuttuvan määrän kattamiseksi hätätoimitustilausta suunnittelujaksoa edeltävänä päivänä. Niinpä suunnitellun ja käytettävissä olevan varaston on oltava aina vähintään nolla, kun tulevan kauden suunnittelu alkaa. Tämän toimitustilauksen suunnittelurivillä näytetään hätävaroituskuvake ja annetaan lisätietoja.

### <a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period"></a>Sarja- ja eränumeroita sekä tilausten välisiä linkkejä ei koske poisjättäminen edeltävältä jaksolta

Jos sarja- tai eränumerot ovat pakollisia tai aiemmin on luotu tilausten välinen linkki, suunnittelujärjestelmä ohittaa edeltävää jaksoa koskevan säännön. Se sisällyttää takautuvat määrät aloituspäivämäärästä alkaen ja saattaa ehdottaa korjaamia toimenpiteitä, jos kysyntää ja tarjontaa ei synkronoida. Kysyntä- ja tarjontajoukkojen on vastattava toisiaan, mikä varmistaa tietyn kysynnän täyttämisen.

## <a name="load-inventory-profiles"></a>Varastoprofiilien lataaminen

Suunnittelujärjestelmä lajittelee kysynnän ja tarjonnan lähteet järjestämällä ne kahdella aikajanalle, joita kutsutaan varastoprofiileiksi.  

Kysyntä ja tarjonta, joiden eräpäivä on suunnittelun aloituspäivämääränä tai sen jälkeen, ladataan jokaiseen varastoprofiiliin. Ladatut kysyntä- ja tarjoustyypit lajitellaan kokonaisprioriteetin mukaan. Niitä ovat esimerkiksi seuraavat:

* Eräpäivä
* Alatason koodit
* Sijainti
* Variantti

Tilauksen prioriteetteja käytetään erilaisissa tyypeissä, sillä näin varmistetaan tärkeimmän kysynnän täyttäminen ensin. Lisätietoja on kohdassa [Tilausten priorisointi](design-details-balancing-demand-and-supply.md#prioritize-orders).  

Kysyntä voi olla myös negatiivista. Negatiivista kysyntää käsitellään tarjontana. Tavanomaisesta kysynnästä poiketen negatiivista kysyntää pidetään kiinteänä tarjontana. Vaikka suunnittelujärjestelmä voi ottaa sen huomioon, siihen ei ehdota muutoksia.  

Yleisesti suunnittelujärjestelmä katsoo, että kaikki suunnittelupäivämäärän jälkeiset toimitustilaukset saattavat muuttua kysynnän täyttämiseksi. Suunnittelujärjestelmä ei kuitenkaan voi muuttaa sitä sen jälkeen, kun määrä on kirjattu toimitustilauksesta. Seuraavia tilauksia ei voi suunnitella uudelleen:  

* Julkaistut tuotantotilaukset, joihin kulutus tai tuotanto on tiliöity.  
* Kokoonpanotilaukset, joissa kulutus tai tuotos on kirjattu.  
* Siirrä tilaukset, joiden toimitus on kirjattu.  
* Ostotilaukset, joissa vastaanotto on jo kirjattu.  

Kysyntä- ja tarjontatyyppien lataamisen lisäksi tietyt tyypit ladataan ottamalla erikoissäännöt ja riippuvuuden huomioon. Artikkelin seuraavissa osissa käsitellään näitä sääntöjä ja riippuvuuksia.  

### <a name="item-dimensions-are-separated"></a>Nimikedimensiot erotetaan

Tarjontasuunnitelma on laskettava kullekin nimikedimensioyhdistelmälle. Yhdistelmässä voi muodostua esimerkiksi variantista ja sijainnista. Vain kysynnän ja/tai tarjonnan sisältävät yhdistelmät on laskettava.  

Suunnittelujärjestelmä etsii yhdistelmiä varastoprofiilissa. Kun uusi yhdistelmä löytyy, se luo yhdistelmän tiedot sisältävän sisäisen ohjaustietueen. Suunnittelujärjestelmä liittää sitten varastointiyksikön ohjaustietueena ja ulkoisena silmukkana. Tämän vuoksi suunnitteluparametrit määritetään variantti- ja sijaintiyhdistelmän mukaan, jonka jälkeen järjestelmä voi jatkaa sisäsilmukkaan. 

> [!NOTE]  
> Varastointiyksikkötietuetta ei tarvitse syöttää, kun tietyn variantti- ja sijaintiyhdistelmän kysyntä ja/tai tarjonta syötetään. Niinpä jos tietyllä yhdistelmällä ei ole varastointiyksikköä, [!INCLUDE [prod_short](includes/prod_short.md)] luo väliaikaisen varastointiyksikkötietueen nimikkeen tietojen perusteella. Jos **Sijainti pakollinen** on otettu käyttöön vaihtopainikkeella **Varastonhallinnan asetukset** -sivulla, varastointiyksikkö on luotava tai **Komponentit sijainnissa** on otettava käyttöön vaihtopainikkeella. Lisätietoja on kohdassa [Suunnitelman luominen sijaintien avulla tai ilman sijainteja](production-planning-with-without-locations.md).  

### <a name="serial-and-lot-numbers-are-loaded-by-specification-level"></a>Sarja- ja eränumerot ladataan erittelytason mukaan

Sarja- ja eränumerot ladataan varastoprofiileihin sen kysynnän ja tarjonnan ohella, joihin kyseiset numerot määritettiin.  

Kysynnän ja tarjonnan määritteet järjestetään tilauksen prioriteetin sekä niiden määrityksen tason perusteella. Koska sarja- ja eränumeroiden vastaavuudet ilmaisevat erittelytason, mitä tarkempi kysyntä on, sitä aikaisemmin sille etsitään vastine. Eritelty kysyntä voi olla esimerkiksi myyntiriville määritetty eränumero. Vähemmän eritelty kysyntä voi olla myynti eränumerosta riippumatta.

> [!NOTE]  
> Ainoa kysynnän ja tarjonnan sarja- ja eränumeroita koskeva priorisointisääntö on niiden yhdistelmien määrittämä erittelytaso ja nimikkeille määritetty nimikeseurantatapa.  

Suunnittelujärjestelmä käsittelee sarja- ja eränumeroita sisältävää tarjontaa täsmäytyksen aikana joustamattomana tarjontana. Järjestelmä ei kasvata eikä uudelleenajoita tällaisia toimitustilauksia. Poikkeus tähän sääntöön on niiden käyttäminen tilausten välisessä suhteessa. Lisätietoja on kohdassa [Tilausten välisiä linkkejä ei katkaista koskaan](#order-to-order-links-are-never-broken). Tämän poikkeus suojaa tarjontaa useiden ja mahdollisten ristiriitaisten toimenpidesanomien vastaanottamisesta silloin, kun siinä on erilaisia määritteitä. Erilaisia määritteitä voi olla käytössä esimerkiksi silloin, kun tarjonnassa on erilaisten sarjanumeroiden kokoelma.  

Toinen syy sarja- ja eränumeroita käyttävän tarjonnan joustamattomuudelle on se, että sarja- ja eränumerot määritetään usein prosessin myöhäisessä vaiheessa. Muutosten ehdottaminen tässä vaiheessa voisi aiheuttaa sekaannuksia.  

Sarja- ja eränumeroiden täsmäytys ei ota huomioon sääntöä, joka estää suunnittelun suunnittelun aloituspäivämäärää edeltävälle ajalle. Jos kysyntää ja tarjontaa ei synkronoida, suunnittelujärjestelmä ehdottaa muutoksia tai uusia tilauksia suunnittelun aloituspäivämäärästä riippumatta.  

### <a name="order-to-order-links-are-never-broken"></a>Tilausten välisiä linkkejä ei katkaista koskaan

Tilausten välistä nimikettä suunniteltaessa linkitettyä tarjontaa saa käyttää vain alkuperäisessä tarkoituksessa. Linkitettyä kysyntää ei saa koskaan kattaa toisella tarjonnalla, vaikka tarjous olisi saatavana ajallisesti ja määrällisesti. Esimerkiksi myyntitilaukseen linkitettyä kokoonpanoa tilausta varten ei saa käyttää kokoonpano tilausta varten -skenaariossa muun kysynnän kattamiseen.  

Tilausten välinen kysyntä ja tarjonta on täsmäytettävä tarkasti. Suunnittelujärjestelmä varmistaa tarjonnan kiinnittämättä huomiota tilauksen kokoparametreihin, muokkaajiin ja varaston määriin (muutoin kuin linkitettyihin tilauksiin liittyvissä määrissä). Samasta syystä järjestelmä ehdottaa ylimääräisen tarjonnan vähentämistä, jos linkitetty kysyntä on vähenee.  

Tämä täsmäytys vaikuttaa myös ajoitukseen. Rajoitettua näköpiiriä, jonka ajanjakso on antanut, ei huomioida; tarjonta aikataulutetaan uudelleen, jos kysynnän ajoitus on muuttunut. Vaimentimen aika otetaan kuitenkin huomioon ja se estää tilausten välisten toimitusten ulos aikatauluttamisen, lukuun ottamatta monitasoisen tuotantotilauksen (projektitilaus) sisäisiä toimituksia.  

> [!NOTE]  
> Sarja- ja eränumerot voidaan määrittää tilausten välisessä kysynnässä. Siinä tapauksessa tarjonnan ei katsota olevan joustamatonta, kuten yleensä sarja- ja eränumeroita käytettäessä. Tässä tapauksessa järjestelmä tekee lisäyksiä tai vähennyksiä kysynnän muutosten mukaan. Jos yksi kysyntä sisältää vaihtelevia sarja- tai eränumeroita, kuten useita eränumeroita, kullekin erälle suositellaan yhtä toimitustilausta.  

> [!NOTE]  
> Ennusteiden ei tulisi johtaa sellaisten toimitustilausten luontiin, jotka on sidottu tilausten välisellä linkillä. Jos ennuste on käytössä, sitä tulisi käyttää vain riippuvaisen tarpeen luomiseen valmistusympäristössä.

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponenttitarve ladataan tuotantotilausten muutosten mukaan

Suunnittelujärjestelmän on valvottava tarvittavia komponentteja tuotantotilausten käsittelyn yhteydessä ennen komponenttien lataamista kysynnän profiiliin. Muutetusta tuotantotilauksesta syntyvät komponenttirivit korvaavat alkuperäisen tilauksen rivit. Muutos varmistaa, että suunnittelujärjestelmään ei muodostu komponenttitarpeen suunnittelurivien kaksoiskappaleita.  

### <a name="consume-safety-stock"></a>Varmuusvaraston käyttäminen

Varmuusvaraston määrä on varastoprofiiliin suunnittelun aloituspäivänä ladattu kysyntä.  

Varmuusvarasto on varaston määrä, joka varataan kysynnän epävarmuuksia varten täytön aikana. Sitä voidaan kuitenkin käyttää kysynnän täyttämiseen. Siinä tapauksessa suunnittelujärjestelmä varmistaa, että varmuusvarasto täytetään nopeasti takaisin. Järjestelmä ehdottaa varmuusvaraston määrän täydentävää toimitustilausta päivämäärälle, jolloin se käytetään. Suunnittelurivillä näkyy poikkeusvaroituksen kuvake, joka ilmaisee, että puuttuvan määrän poikkeustilaus on käyttänyt varmuusvaraston osittain tai kokonaan.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Myyntitilaukset vähentävät ennustettua kysyntää

Kysyntäennusteet ilmaisevat odotetun kysynnän. Kun todellinen tarve syötetään, yleensä myyntitilausten tuotettujen nimikkeiden kuluttaa ennuste.

Myyntitilaukset eivät vähennä ennustetta. Suunnittelun laskennassa käytettyjä ennustemääriä kuitenkin vähennetään myyntitilausten määrillä, ennen kuin jäljellä oleva määrä siirtyy kysyntäprofiiliin. Suunnittelu sisällyttää jakson aikaiseen myyntiin sekä avoimet myyntitilaukset että toimitetun myynnin nimiketapahtumat. Poikkeuksen sääntöön muodostavat puitetilauksesta tulevat tilaukset.  

Kelvollinen ennustejakso on määritettävä. Ennustetun määrän päivämäärä määrittää ajanjakson alun ja seuraavan ennusteen päivämäärä määrittää ajanjakson lopun.  

Suunnittelujaksoa edeltävien ajanjaksojen ennustetta ei käytetä riippumatta, käytettiinkö sitä vai ei. Ensimmäinen kiinnostava ennusteajankohta on joko suunnittelun aloituspäivämäärä tai sitä lähinnä oleva päivämäärä.  

Ennuste voidaan tehdä erilaisille kysyntätyypeille:

* Itsenäinen kysyntä, kuten myyntitilaukset
* Riippuvainen kysyntä, kuten tuotantotilauksen komponentit.

Nimikkeellä voi olla molemmat ennusteen tyypit. Suunnittelun aikana kulutus tehdään erikseen ensin itsenäiselle kysynnälle ja sitten riippuvaiselle kysynnälle.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Myyntitilaukset vähentävät puitetilauksen kysyntää

Puitemyyntitilaus täydentää ennustetta tapana määrittää tietyn asiakkaan tuleva kysyntä. Kuten (määrittelemättömän) ennusteen tapauksessa, toteutuneiden myyntien tulisi kuluttaa oletettu kysyntä ja jäljelle jäävän määrän tulisi siirtyä varastoprofiiliin. Kulutus ei vähennä puitetilauksen määrää.

Suunnittelulaskelma sisältää avoimet tiettyyn puitetilausriviin linkitetyt myyntitilaukset, mutta se ei sisällä mitään voimassaolevaa ajanjaksoa. Se ei myöskään sisällä kirjattuja tilauksia, koska kirjausmenettely on jo vähentänyt puitetilauksen avointa määrää.

## <a name="prioritize-orders"></a>Tilausten priorisointi

Pyydetty tai käytettävissä oleva päivämäärä ilmaisee annetun varastointiyksikön korkeimman prioriteetin. Kuluvan päivän kysyntä on käsiteltävä ennen seuraavan viikon kysyntää. Tämä yleisen prioriteetin lisäksi suunnittelujärjestelmä ottaa seuraavat ehdotukset huomioon tilausten prioriteettien mukaisesti:

* Ensimmäiseksi täytettävä kysyntätyyppi.
* Ennen muita tarjontalähteitä käytettävä tarjontalähde.  

Ladattu kysyntä ja tarjonta lisätään arvioidun varastoprofiiliin prioriteettien mukaisesti:  

### <a name="priorities-on-the-demand-side"></a>Kysyntäpuolen prioriteetit

1. Jo toimitettu: nimiketapahtuma  
2. Ostopalautustilaus  
3. Myyntitilaus  
4. Huoltotilaus  
5. Tuotannon komponenttitarpeet  
6. Kokoonpanotilauksen rivi  
7. Lähtevä siirtotilaus  
8. Puitetilaus (jota liittyvä myyntitilaukset eivät ole vielä käyttäneet)  
9. Ennuste (jota muut myyntitilaukset eivät ole vielä kuluttaneet)  

> [!NOTE]  
> Ostopalautuksia ei tavallisesti sisällytetä tarjonnan suunnittelun; ne on aina varattava palautettavasta erästä. Jos varausta ei ole tehty, ostopalautukset vaikuttavat saatavuuteen ja ne priorisoidaan erittäin korkealle, sillä niin voidaan välttää mahdollisuus, että suunnittelujärjestelmä ehdottaa toimitustilausta vain ostopalautuksen käsittelemistä varten.  

### <a name="priorities-on-the-supply-side"></a>Tarjontapuolen prioriteetit

1. Jo varastossa: nimiketapahtuma (suunnittelun joustavuus = ei mitään)  
2. Myyntipalautustilaus (suunnittelun joustavuus = ei mitään)  
3. Tuleva siirtotilaus  
4. Tuotantotilaus  
5. Kokoonpanotilaus  
6. Ostotilaus  

### <a name="priority-related-to-the-state-of-supply-and-demand"></a>Kysynnän ja tarjonnan tilaan liittyvä prioriteetti

Tarjonnan ja kysynnän tyypin prioriteettien lisäksi muut tekijät vaikuttavat suunnittelun joustavuuteen. Niitä ovat esimerkiksi varastointiaktiviteetit ja seuraavien tilausten tila:

* Myynti
* Ostot
* Siirto
* Kokoonpano
* Tuotanto

Näiden tilausten tilalla on seuraavat vaikutukset: 

1. Osittain käsitelty (suunnittelun joustavuus = ei mitään)  
2. Jo käsittelyssä varastossa (suunnittelun joustavuus = ei mitään)  
3. Julkaistu - kaikki tilaustyypit (suunnittelun joustavuus = rajoittamaton)  
4. Sitovasti suunniteltu tuotantotilaus (suunnittelun joustavuus = rajoittamaton)  
5. Suunniteltu/avoin – kaikki tilaustyypit (suunnittelun joustavuus = rajoittamaton)

## <a name="balancing-supply-with-demand"></a>Tarjonnan ja kysynnän täsmäyttäminen

Suunnittelujärjestelmä täsmäyttää kysynnän ja tarjonnan ehdottamalla toimenpiteitä täsmäyttämättömien toimitustilausten tarkistamista varten. Tämä täsmäytys tehdään kullekin variantti- ja sijaintiyhdistelmälle.  

Oletetaan, että kussakin varastoprofiilissa on kaksi ketjua:

* Kysyntätapahtumien päivämäärän ja prioriteetin mukaan lajiteltu ketju
* Vastaava tarjontatapahtumien ketju

Kukin tapahtuma viittaa lähdetyyppiin ja tunnukseen. Nimikkeen täsmäytyssäännöt ovat yksinkertaiset. Kysyntä ja tarjonta voidaan täsmäyttää seuraavasti koska tahansa prosessin aikana:  

1. Nimikkeellä ei ole kysyntää tai tarjontaa = > suunnittelu on päättynyt (tai sen ei pitäisi käynnistyä).  
2. Kysyntää on mutta tarjontaa ei => tarjontaa on ehdotettava.  
3. Tarjontaa on mutta sille ei ole kysyntää => tarjonta on peruutettava.  
4. Sekä kysyntää että tarjontaa on => kysymyksiä on esitettävä ja niihin on vastata, ennen kuin [!INCLUDE [prod_short](includes/prod_short.md)] voi varmistaa, että tarjonta vastaa kysyntää.

    Jos tarjonnan ajankohta ei ole sopiva, tarjonta on ehkä mahdollista aikatauluttaa uudelleen seuraavasti:  

    1. Jos tarjonta edeltää kysyntää, tarjonta voidaan ehkä aikatauluttaa siten, että varasto on mahdollisimman pieni.  
    2. Jos kysyntä edeltää tarjontaa, tarjonnan aikataulutusta voidaan ehkä siirtää eteenpäin. Muussa tapauksessa järjestelmä ehdottaa uutta tarjontaa.  
    3. Jos tarjonta vastaa kysyntää kyseisenä päivämääränä, suunnittelujärjestelmä voi selvittää, kattaako tarjonnan määrä kysynnän.  

    Kun ajoitus on valmis, tarjonnan määrä voidaan laskea seuraavasti:  

    1. Jos tarjonnan määrä alittaa kysynnän, tarjonnan määrää voidaan lisätä (tai ei, jos käytössä on enimmäismääräkäytäntö).  
    2. Jos tarjonnan määrä ylittää kysynnän, tarjonnan määrää voidaan vähentää (tai ei, jos käytössä on vähimmäismääräkäytäntö).  

    Tässä vaiheessa kyse on jommastakummasta tilanteesta:  

    1. Nykyiseen kysyntään voidaan vastata, jolloin se voidaan sulkea ja seuraavan kysynnän suunnittelu voidaan aloittaa.  
    2. Tarjonta on saavuttanut enimmäismäärän, ja osa kysyntämäärästä on jäänyt kattamatta. Tässä tapauksessa suunnittelujärjestelmä voi sulkea nykyisen tarjonnan ja siirtyä seuraavaan.  

 Toimenpide alkaa uudelleen seuraavasta kysynnästä ja nykyisestä tarjonnasta tai päinvastoin. Nykyinen tarjonta voi pystyä kattamaan myös tämän seuraavan kysynnän tai nykyiseen kysyntään ei ole vielä täysin vastattu.  

### <a name="rules-for-actions-for-supply-events"></a>Tarjoustapahtumien toimenpiteitä koskevat säännöt

Jos kyse on ylhäältä alaspäin tehtävistä laskelmista, joissa tarjonnan on täytettävä kysyntä, kysyntä otetaan annettuna. Se on siis suunnittelujärjestelmän ulkopuolella. Suunnittelujärjestelmä voi kuitenkin hallita tarjonnan puolta ja tehdä seuraavia ehdotuksia:

* uusien toimitustilausten luominen
* aiemmin luotujen tilausten uudelleenajoittaminen tai niiden määrien muuttaminen
* tarpeettomien toimitustilausten peruuttaminen.  

Toimitustilaus voidaan jättää pois suunnitteluehdotuksista ilmoittamalla, ettei suunnittelussa ole joustavuutta (suunnittelun joustavuus = ei mitään). Tilauksen ylimääräinen tarjonta käytetään kysynnän kattamisessa, mutta toimintoa ei ehdoteta. 

Yleisesti ottaen suunnittelun joustavuus koko tarjontaa, joskin kunkin ehdotetun toimenpiteet edot rajoittavat tätä joustavuutta.  

* **Aikatauluta uudelleen ulos**: olemassa olevan toimitustilauksen päivämäärä voidaan aikatauluttaa ulos, jotta se vastaa kysynnän eräpäivää, ellei:

  * Se kuvaa varastoa (aina päivänä nolla).  
  * Sillä on tilausten välinen linkki toiseen kysyntään.  
  * Se on aikavälin uudelleenajoitusikkunan ulkopuolella.
  * Myös lähempänä olevaa tarjontaa voidaan käyttää.  
  * Toisaalta käyttäjä voi päättää, että aikataulutusta ei suoriteta uudelleen, koska:
  * Toimitustilaus on sidottu edellisen päivän toiseen kysyntään.  
  * Tarvittava uudelleenaikataulutus on niin vähäistä, ettei sillä ole merkitystä.  

* **Aikatauluta uudelleen sisään**: aiemmin luodun toimitustilauksen päivämäärä voidaan aikatauluttaa sisään seuraavia tilanteita lukuun ottamatta:

  * Se on linkitetty suoraan johonkin toiseen kysyntään.  
  * Se on aikavälin määrittämän uudelleenajoitusikkunan ulkopuolella.

> [!NOTE]  
> Uusintatilauspistettä käyttävää nimikettä suunniteltaessa toimitustilaus voidaan ajoittaa uudelleen. Näin tehdään usein eteenpäin ajastetuissa toimitustilauksissa, jotka uusintatilauspiste käynnistää.

* **Kasvatusmäärä**: olemassa olevan toimitustilauksen määrää voidaan kasvattaa vastaamaan kysyntää, ellei toimitustilausta linkitetä suoraan kysyntään tilausten välisellä linkillä.  

> [!NOTE]  
> Vaikka toimitustilausta voidaan kasvattaa, kasvattaminen voi olla rajallista määritetyn enimmäistilausmäärän vuoksi.  

* **Vähennysmäärä**: aiemmin luodun toimitustilauksen määrä, joka on ylijäämäinen verrattuna olemassa olevaan kysyntään, on vähennettävissä kysynnän täyttämiseksi.  

> [!NOTE]  
> Vaikka määrää voidaan vähentää, kysyntään verrattuna saattaa vielä olla ylijäämää määritetyn vähimmäistilausmäärän tai tilauskerrannaisen vuoksi. 

* **Peruuta**: toimitustilaus voidaan peruuttaa erityisenä määrän vähennystoiminnon tapahtumana, jos se on vähennetty nollaan. 
* **Uusi**: jos toimitustilauksia ei ole tai jos aiemmin luotua tilausta ei voi muuttaa täyttämään tarvittavaa määrää kysynnän eräpäivänä, uutta toimitustilausta ehdotetaan.  

### <a name="determine-the-supply-quantity"></a>Tarjonnan määrän määrittäminen

Määritettävät suunnitteluparametrit ohjaavat kunkin toimitustilauksen ehdotettua määrää.  

Kun suunnittelujärjestelmä laskee uuden toimitustilauksen määrän tai aiemmin luodun tilauksen muutettavan määrän, ehdotettu määrä voi poiketa toteutuneesta kysynnästä.  

Jos enimmäisvarasto tai kiinteä tilausmäärät ovat valittuna, ehdotettua määrää saatetaan kasvattaa kiinteän määrän tai enimmäisvaraston täyttämiseksi. Jos uusintatilaustapa käyttää uusintatilauspistettä, määrää voidaan kasvattaa vähintään uusintatilauspisteen täyttämiseksi. 

Ehdotettua määrää saatetaan muokata tässä järjestyksessä:  

1. Alaspäin enimmäistilausmäärään.  
2. Ylöspäin seuraavaan tilausmäärään.  
3. Ylöspäin seuraavaan tilauskerrannaisen.

### <a name="order-tracking-links-during-planning"></a>Tilauksen seurantalinkit suunnittelun aikana

Suunnittelun aikaisessa tilauksen seurannassa suunnittelujärjestelmä järjestää uudelleen nimike-, variantti- ja sijaintiyhdistelmien tilauksen seurantalinkit. Järjestelmä järjestää seurantalinkit uudelleen seuraavista syistä:

* Varmistetaan, että ehdotukset kattavat koko kysynnän ja kaikkia toimitustilauksia tarvitaan.  
* Tilauksen seurantalinkit on tasapainotettava säännöllisesti uudelleen.  

Tilauksen seurantalinkkien tasapaino häviää ajan mittaan. Linkit tasapaino häviää, koska tilauksen seurantaverkkoa ei järjestetä uudelleen, ennen kuin kysyntä tai tarjonta suljetaan.

Suunnittelujärjestelmä poistaa kaikki aiemmin luodut tilauksen seurantalinkit ennen kysynnän ja tarjonnan täsmäyttämistä. Kun kysyntä- tai tarjontatapahtuma ollessa suljettu, täsmäytyksen aikana luodaan uudet tilauksen seurantalinkit kysynnän ja tarjonnan välille.  

> [!NOTE]  
> Vaikka dynaamista tilauksen seurantaa ei olisi määritetty nimikkeeseen, suunnittelujärjestelmä luo tasapainotetut tilauksen seurantalinkit.

## <a name="close-balanced-supply-and-demand"></a>Kysynnän ja tarjonnan täsmäytyksen sulkeminen

Tarjonnan täsmäytyksellä on kolme mahdollista tulosta:

* Kysyntätapahtumien edellyttämä määrä ja päivämäärä toteutuvat ja niiden suunnittelu voidaan sulkea,. Tarjoustapahtuma jää avoimeksi ja voi mahdollisesti kattaa seuraavan kysynnän. Tarjontatapahtuman pitäminen avoimena mahdollistaa täsmäytysmenettelyn aloittamisen uudelleen nykyisen tarjoustapahtuman ja seuraavan kysynnän osalta.  
* Toimitustilausta ei voi muokata kattamaan koko kysyntää. Kysyntätapahtuma on edelleen avoinna, ja siinä on jokin kattamaton määrä, jonka seuraava tarjontatapahtuma ehkä kattaa. Niinpä nykyinen tarjontatapahtuma suljetaan ja täsmäytys voi alkaa alusta nykyisen kysynnästä ja seuraavasta tarjontatapahtuman osalta.  
* Koko kysyntä katetaan eikä seuraavaa kysyntää ole (tai kysyntää ei ole lainkaan). Ylimääräistä tarjontaa saatetaan vähentää (tai peruuttaa) ja sitten sulkea. Myös muut mahdolliset tarjontatapahtumat on peruutettava.  

Suunnittelujärjestelmä luo lopuksi tilauksen seurantalinkin tarjonnan ja kysynnän välille.  

### <a name="create-the-planning-line-suggested-action"></a>Suunnittelurivin luominen (ehdotettu toimenpide)

Jos toimitustilauksen korjaamista ehdotetaan **Uusi**-, **Muuta määrä**-, **Aikatauluta uudelleen**-, **Aikatauluta uudelleen ja muuta määrää**- tai **Peruuta**-toimenpiteellä, suunnittelujärjestelmä luo suunnittelurivin suunnittelutyökirjassa. Tilauksen seurannassa suunnitteluriviä ei luoda ainoastaan silloin, kun tarjontatapahtuma suljetaan vaan myös kysyntätapahtuman sulkemisen yhteydessä. Näin tehdään myös silloin, kun tarjontatapahtuma on edelleen avoin ja sitä ehkä muutetaan, kun seuraava kysyntätapahtuma käsitellään. Suunnitteluriviä voidaan muuttaa uudelleen, kun se luodaan.

Tietokannan kuormitus tuotantotilauksia käsiteltäessä voidaan vähentää ylläpitämällä suunnitteluriviä kolmella tasolla:

* Luo vain suunnittelurivi nykyisellä eräpäivällä ja määrällä, mutta ilman reititystä ja komponentteja.  
* Sisällytä reititys: suunniteltu reititys sisältää aloitus- ja lopetuspäivämäärät sekä kellonajat. Reitityksen sisällyttäminen vaativaa tietokannan käyttöoikeuksien kannalta. Loppupäivämäärää ja eräpäivää määritettäessä reititys on ehkä laskettava, vaikka tarjontatapahtumaa ei ole suljettu. Kyse voi olla esimerkiksi aikataulutuksesta eteenpäin.  
* Sisällytä tuoterakenteen purku: voi tapahtua juuri ennen tarjontatapahtuman sulkemista.

## <a name="see-also"></a>Katso myös

[Rakennetiedot: Suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)  
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)  
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
