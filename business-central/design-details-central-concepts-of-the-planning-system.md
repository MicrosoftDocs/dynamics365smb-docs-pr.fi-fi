---
title: 'Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet'
description: Suunnittelutoiminnot ehdottavat käyttäjälle mahdollisia toimia perustuen kysyntä/tarjontatilanteeseen ja nimikkeiden suunnitteluparametreihin.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: a9218bf8d8fa2c7f84b08380742df17bd7be7afe
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605162"
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet

Suunnittelutoiminnot on sisällytetty eräajoon, joka ensin valitsee asiaankuuluvat nimikkeet ja ajanjaksot, jotka suunnitellaan. Eräajo kutsuu codeunitia kunkin nimikkeen alatason koodin (tuotantorakenteen positio) mukaisesti ja laskee suunnitelman täsmäyttämällä tarjonta- ja kysyntäjoukot ja ehdottaa käyttäjälle mahdollisia toimintatapoja. Ehdotetut toimenpiteet ilmestyvät riveinä suunnittelutaulukkoon tai tilaustaulukkoon.  

![Suunnittelutyökirjasivun sisältö.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Suunnittelutyökirja-sivun sisältö")  

Yrityksen suunnittelijan, kuten ostaja tai tuotantosuunnittelija, oletetaan olevan suunnittelujärjestelmän käyttäjä. Suunnittelujärjestelmä auttaa käyttäjää suorittamaan laajat, mutta melko suoraviivaiset suunnitelman laskelmat. Tämän jälkeen käyttäjä voi keskittyä ratkaisemaan vaikeampia ongelmia, kuten esimerkiksi poikkeustilanteiden hallintaa.  

Suunnittelujärjestelmää ohjaa ennakoitu ja nykyinen asiakaskysyntä, kuten ennuste ja myyntitilaukset. Kun suunnitelma lasketaan, sovellus ehdottaa käyttäjälle tiettyjä toimenpiteitä, jotka liittyvät mahdollisiin toimittajien toimituksiin, kokoonpanoon tai tuotanto-osastoihin tai siirtoihin muista varastoista. Näiden ehdotettujen toimintojen avulla voi luoda uusia toimitustilauksia, kuten osto- tai tuotantotilauksia. Jos toimitustilauksia on jo tehty, ehdotettuja toimenpiteitä voivat olla tilausten lisääminen tai vauhdittaminen muuttuneen kysynnän mukaisiksi.  

Suunnittelujärjestelmän toinen tavoite on varmistaa, että varasto ei kasva tarpeettoman suureksi. Jos kysyntä vähenee, suunnittelujärjestelmä ehdottaa käyttäjälle olemassa olevien toimitustilausten lykkäämistä, pienentämistä tai peruuttamista.  

Tarvelaskenta ja tuotanto-ohjelma, Laske nettomuutossuunnitelma ja Laske uudelleensuunnittelu ovat kaikki toimintoja yhdessä codeunitissa, joka sisältää suunnittelulogiikan. Tarjontasuunnitelman laskentaan liittyy kuitenkin eri alajärjestelmiä.  

Huomaa, että suunnittelujärjestelmä ei sisällä erityistä logiikkaa kapasiteetin tasaamisen tai aikataulun tarkentamiseen. Tämän vuoksi ajoitustyö suoritetaan erillisenä toimintona. Kahden alueen välisen yhteyden puuttuminen tarkoittaa myös sitä, että olennainen kapasiteetti tai aikataulumuutokset vaativat suunnitelmaan uudelleenajoa.  

## <a name="planning-parameters"></a>Suunnittelun parametrit

Käyttäjän nimikkeelle tai nimikkeiden ryhmälle asettamat suunnitteluparametrit ohjaavat mitä toimintoja suunnittelujärjestelmä ehdottaa eri tilanteissa. Suunnitteluparametri on määritetty jokaisessa nimikekortissa. Niillä hallinnoidaan milloin, kuinka paljon ja kuinka varastoa täydennetään.  

Suunnitteluparametreja voidaan myös määrittää mille tahansa nimikkeen, variantin ja sijainnin yhdistelmälle asettamalla varastointiyksikkö (SKU) jokaiselle tarvittavalle yhdistelmälle ja määrittämällä sitten yksittäiset parametrit.  

Lisätietoja on kohdissa [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) ja [Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Suunnittelun aloituspäivämäärä

Voit välttää toimitussuunnitelmaa, joka käyttää aiempia avoimia tilauksia ja ehdottaa potentiaalisesti mahdottomia toimenpiteitä, suunnittelujärjestelmä kohtelee kaikkia suunnittelun alkupäivämäärää aiempia päivämääriä jäädytettynä alueena, jolla käytetään seuraavaa erityissääntöä:  

Kaikki kysyntä ja tarjonta ennen suunnittelujakson aloituspäivämäärää katsotaan osaksi varastoa tai toimitetuksi.  

Toisin sanoen se olettaa aiemman suunnitelman suorittamista määritetyn suunnitelman mukaan.  

Lisätietoja on kohdassa [Tilausten käsittely ennen suunnittelun aloituspäivää](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).  

## <a name="dynamic-order-tracking-pegging"></a>Dynaaminen tilausseuranta (tarvekohdistus)

Dynaaminen tilausseuranta, joka luo samanaikaisesti toimenpideviestit suunnittelutyökirjassa, ei ole osa tarjonnan suunnittelujärjestelmää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa Tämä toiminto linkittää reaaliaikaisesti kysynnän ja määrät, jotka voisivat kattaa sen, jos uusi kysyntä tai tarjonta luodaan tai sitä muutetaan.  

Esimerkiksi, jos käyttäjä syöttää tai muuttaa myyntitilausta, dynaaminen tilausten seurantajärjestelmä etsii sopivan tarjonnan kysynnän kattamiseksi. Tämä voi olla lähtöisin varastosta tai odotetusta toimitustilauksesta (kuten osto- tai tuotantotilauksesta). Kun tarjonnan lähde löytyy, järjestelmä luo linkin kysynnän ja tarjonnan välille ja näyttää sen vain luku -tilassa olevilla sivuilla, joita voi käyttää asiaan kuuluvilta asiakirjariveiltä. Jos asianmukaista tarjontaa ei löydy, dynaaminen tilausten seurantajärjestelmä luo suunnittelutyökirjaan toimenpideviestejä, joiden tarjontasuunnitelman ehdotukset kuvaavat dynaamista täsmäytystä. Näin ollen dynaaminen tilausten seurantajärjestelmä tarjoaa hyvin yksinkertaisen suunnittelujärjestelmän, joka voi auttaa sekä suunnittelijaa että muita rooleja sisäisessä toimitusketjussa.  

Näin ollen dynaamista tilausten seurantaa voidaan pitää työkaluna, joka auttaa käyttäjää arvioimaan tilausehdotusten hyväksymistä. Tarjontapuolelta käyttäjä voi nähdä, että mikä kysyntä on luonut tarjonnan ja kysyntäpuolelta, minkä tarjonnan tulisi kattaa kysyntä.  

![Esimerkki dynaamisesta tilausten seurannasta.](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Esimerkki dynaamisesta tilausten seurannasta")  

Lisätietoja on kohdassa [Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys](design-details-reservation-order-tracking-and-action-messaging.md).  

Dynaamisen tilausten hallinnan käyttäminen tarjonnan suunnitteluun saattaa riittää niissä yrityksissä, joissa on alhainen nimikevirta ja vähemmän laajennetut tuoterakenteet. Vilkkaammissa ympäristöissä suunnittelujärjestelmää tulisi kuitenkin käyttää täsmäytetyn toimitussuunnitelman varmistamiseksi.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Dynaaminen tilausseuranta verrattuna suunnittelujärjestelmään

Yhdellä silmäyksellä saattaa olla vaikea erottaa suunnittelujärjestelmää ja dynaamista tilauksen seurantaa. Molemmat ominaisuudet näyttävät tulosteen suunnittelutyökirjalla ehdottamalla toimia, jotka suunnittelijan tulisi suorittaa. Tämän tuotoksen tuotantotapa kuitenkin poikkeaa.  

Suunnittelujärjestelmä käsittelee nimikkeen koko kysyntä- ja tarjontamallin kaikilla BOM-hierarkian tasoilla aikajanalla, kun taas dynaaminen tilauksenseuranta tarttuu vain siihen tilauksen tilanteeseen, joka on aktivoinut sen. Suunnittelujärjestelmä luo kysynnän ja tarjonnan täsmäytyksen yhteydessä linkin käyttäjän aktivoimaan erätilaan, kun taas dynaaminen tilausseuranta luo linkit automaattisesti lennossa aina, kun käyttäjä syöttää sovellukseen kysynnän tai tarjonnan, kuten myynti- tai ostotilauksen.  

Dynaaminen tilausseuranta luo kysynnän ja tarjonnan väliset linkit tietojen kirjoituksen aikana saapumisjärjestyksen perusteella. Tämän vuoksi prioriteetit saattavat muuttua. Esimerkiksi ensin kirjoitettu myyntitilaus, jonka eräpäivä on seuraavassa kuussa, saatetaan linkittää varaston tarjontaan, kun taas seuraava huomenna erääntyvä myyntitilaus voi aiheuttaa toimenpideviestin uuden ostotilauksen luomiseksi, kuten alla on esitetty.  

![Esimerkki tilausten seurannasta toimitusten suunnittelussa 1.](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Esimerkki tilausten seurannasta toimitusten suunnittelussa 1")  

Sen sijaan suunnittelujärjestelmä käsittelee tietyn nimikkeen kaiken kysynnän ja tarjonnan priorisoidussa järjestyksessä eräpäivien ja tilaustyyppien mukaan eli tarpeen/saapumisjärjestyksen perusteella. Se poistaa kaikki dynaamisesti luodut tilauksen seurantalinkit ja luo ne uudelleen eräpäivän prioriteetin mukaisesti. Kun suunnittelujärjestelmän käyttö lopetetaan, se on ratkaissut kysynnän ja tarjonnan välisen epätasapainon. Tämä osoitetaan myös alla olevassa kuvassa.  

![Esimerkki tilausten seurannasta toimitusten suunnittelussa 2.](media/NAV_APP_supply_planning_1_planning_graph.png "Esimerkki tilausten seurannasta toimitusten suunnittelussa 2")  

Suunnitteluajon jälkeen Toimenpideviestitapahtuma-taulukossa ei ole toimenpideviestejä, koska ne on korvattu suunnittelutyökirjassa ehdotetuilla toimenpiteillä  

Katso lisätietoja kohdasta [Tilauksen seurantalinkit suunnittelun aikana](design-details-balancing-demand-and-supply.md#seriallot-numbers-are-loaded-by-specification-level).  

## <a name="sequence-and-priority-in-planning"></a>Suunnittelun järjestys ja ensisijaisuus

Laskentajärjestys on tärkeä suunnitelman muodostuksessa, koska sen avulla työ voidaan tehdä kohtuullisessa ajassa. Lisäksi vaatimusten ja resurssien priorisoinnilla on tärkeä merkitys parhaiden tulosten saamiseksi.  

[!INCLUDE[prod_short](includes/prod_short.md)]:in suunnittelujärjestelmä on kysyntä-ohjasteinen. Korkean tason nimikkeet tulisi suunnitella ennen alemman tason nimikkeitä, koska korkean tason nimikkeiden suunnitelma saattaa luoda lisäkysynnän alemman tason nimikkeille. Tämä tarkoittaa esimerkiksi sitä, että vähittäismyyntipaikat on suunniteltava ennen jakelukeskusten suunnittelua, koska vähittäismyyntipaikan suunnitelma saattaa sisältää lisäkysyntää jakelukeskuksesta. Yksityiskohtaisella täsmäytystasolla tämä tarkoittaa myös, että myyntitilauksen ei tulisi laukaista uutta toimitustilausta, jos jo vapautettu toimitustilaus voi kattaa myyntitilauksen. Vastaavasti tietyllä eränumerolla varustettua tarjontaa ei tulisi kohdistaa kattamaan yleistä kysyntää, jos toinen kysyntä vaatii tätä tiettyä erää.  

### <a name="item-priority--low-level-code"></a>Nimikkeen prioriteetti/alatason koodi

Valmistusympäristössä valmiiden, myytävien nimikkeiden kysyntä aiheuttaa valmiin nimikkeen koostavien komponenttien johdettua kysyntää. Materiaalilasku-rakenne kontrolloi osan rakennetta ja voi kattaa useita puolivalmiiden nimikkeiden tasoja. Yhden nimikkeen suunnittelu yhdellä tasolla aiheuttaa epäsuoran kysynnän seuraavan tason komponenteille ja niin edelleen. Lopulta tämä johtaa ostettujen nimikkeiden epäsuoraan kysyntään. Näin ollen suunnittelujärjestelmä suunnittelee nimikkeille niiden tuoterakenteen hierarkian luokituksen määräämässä järjestyksessä alkaen loppuneista myytävissä olevista nimikkeistä ylätasolla ja jatkuen alas tuoterakenteen läpi alemman tason nimikkeisiin (alatason koodin mukaisesti).  

![Tuoterakenteiden suunnitelma.](media/NAV_APP_supply_planning_1_BOM_planning.png "Tuoterakenteiden suunnitelma")  

Luvut osoittavat missä järjestyksessä järjestelmä tekee ehdotuksia toimitustilauksiin huipputasolla ja olettaen, että käyttäjä hyväksyy nämä ehdotukset, missä tahansa alemman tason nimikkeissä myös.  

Lisätietoja tuotantonäkökohdista on kohdassa [Varastoprofiilien lataaminen](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

#### <a name="optimizing-performance-for-low-level-calculations"></a>Suorituskyvyn optimoiminen matalan tason laskelmissa

Matalan tason koodilaskelmat voivat vaikuttaa järjestelmän suorituskykyyn. Vaikutusten lieventämiseksi voit poistaa **Dynaamisen matalan tason koodilaskennan** käytöstä **Tuotannon asetukset** -sivulla. Kun teet näin, [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelma ehdottaa, että luodaan toistuva työjonotapahtuma, joka päivittää matalan tason koodit päivittäin. Voit varmistaa, että työ suoritetaan työajan ulkopuolella, määrittämällä aloitusajan **Aikaisin alkamispäivä ja -aika** -kentässä.

Voit myös ottaa käyttöön logiikan, joka nopeuttaa alatason koodilaskentaa valitsemalla **Tuotannon asetukset**-sivulla **Optimoi matalan tason koodilaskenta**. 

> [!IMPORTANT]
> Jos optimoit suorituskyvyn, [!INCLUDE[prod_short](includes/prod_short.md)] käyttää uusia laskentamenetelmiä alatason koodien määrittämiseen. Jos sinulla on laajennus, joka perustuu vanhojen laskelmien käyttämiin tapahtumiin, laajennus voi lakata toimimasta.   

### <a name="locations--transfer-level-priority"></a>Sijainnit/siirtotason prioriteetti

Yritysten, jotka toimivat useammassa kuin yhdessä paikassa, on ehkä suunniteltava jokaiselle paikalle erikseen. Esimerkiksi nimikkeen varmuusvaraston taso ja sen uusintatilaustapa saattaa vaihdella sijainnista toiseen. Tässä tapauksessa suunnitteluparametrit on määritettävä nimike- ja sijaintikohtaisesti.  

Tätä tuetaan varastointiyksiköiden käytön kanssa silloin, kun yksittäisen suunnitteluparametrit voidaan määrittää varastointiyksikön tasolla. Varastointiyksikkö voidaan tulkita nimikkeeksi tietyssä paikassa. Jos käyttäjä ei ole määritetty varastointiyksikköä tälle sijainnille, sovellus käyttää nimikkeen kortissa määritettyjä oletusparametreja. Sovellus laskee suunnitelman vain aktiivisille sijainneille, joissa on olemassa oleva kysyntä tai tarjonta annetulle nimikkeelle.  

Periaatteessa mikä tahansa nimike voidaan käsitellä missä tahansa sijainnissa, mutta sovelluksen suhtautuminen sijaintikäsitteeseen on tiukka. Esimerkiksi myyntitilausta yhdessä sijainnissa ei voida täyttää jollakin toisessa sijainnissa olevalla varastomäärällä. Varaston määrä tulee ensin siirtää myyntitilauksessa määritettyyn sijaintiin.  

![Varastointiyksiköiden suunnittelu.](media/NAV_APP_supply_planning_1_SKU_planning.png "Varastointiyksiköiden suunnittelu")  

Lisätietoja on kohdassa [Rakennetiedot: siirrot suunnittelussa](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Tilauksen prioriteetti

Pyydetty tai käytettävissä oleva päivämäärä edustaa annetun varastointiyksikön korkeinta prioriteettia. Tämän päivän kysyntä tulee käsitellä ennen tulevien päivien kysyntää. Mutta lukuun ottamatta tämän kaltaista prioriteettia, eri kysynnän ja tarjonnan tyypit järjestetään liiketoiminnan tärkeyden perusteella jotta voidaan päättää mikä kysyntä on täytettävä ennen kuin täytetään toinen kysyntä. Tarjonnan puolella tilauksen prioriteetti kertoo mitä tarjontalähdettä tulisi soveltaa ennen muiden tarjontalähteiden käyttöä.  

Lisätietoja on kohdassa [Projektitilausten priorisointi](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Kysyntäennusteet ja puitetilaukset

Sekä ennustukset ja puitetilaukset esittävät odotettavissa olevaa kysyntää. Kestotilaus, joka kattaa asiakkaan suunnitellut ostot tietyltä aikajaksolta, vähentää yleisennusteen epävarmuutta. Kestotilaus on asiakkaan määrittämä ennuste määrittämättömien ennusteiden lisäksi, kuten kuvattu alla.  

![Ennusteiden käyttäminen suunnitelussa.](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Ennusteiden käyttäminen suunnitelussa")  

Katso lisätietoja: [Myyntitilaukset vähentävät ennustettua kysyntää](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## <a name="planning-assignment"></a>Suunnittelun tehtävä

Kaikki nimikkeet tulee suunnitella, mutta nimikkeelle ei ole syytä laskea suunnitelmaa ellei kysyntä- tai tarjontakuvio ole muuttunut edellisen suunnitelman laskemisen jälkeen.  

Jos käyttäjä on kirjoittanut uuden myyntitilauksen tai muuttanut olemassa olevaa, suunnitelman uudelleen laskeminen on tarpeellista. Muita syitä ovat muutos ennusteeseen tai haluttu varmuusvaraston määrä. Tuoterakenteen muuttaminen komponentin lisäyksellä tai poistolla ilmaisisi todennäköisesti muutosta, mutta vain komponenttinimikkeelle.  

Suunnittelujärjestelmä tarkkailee tällaisia tapahtumia ja määrittää nimikkeet suunnitelmalle.  

Useiden sijaintien kohdalla, määritys tapahtuu nimikkeen tasolla sijaintiyhdistelmää kohti. Jos esimerkiksi myyntitilaus on luotu vain yhdessä sijainnissa, sovellus määrittää suunnittelulle tässä tietyssä sijainnissa olevan nimikkeen.  

Syy valita nimikkeitä suunnittelua varten on järjestelmän toimintaseikka. Jos nimikkeen kysyntä–tarjonta-mallissa ei ole tapahtunut muutosta, suunnittelujärjestelmä ei ehdota toimenpiteitä. Ilman suunnittelun tehtävää järjestelmän on suoritettava laskennat kaikille nimikkeille suunnitelmaa ja järjestelmän resurssit kuluttavaa tilannetta määritettäessä.  

Täydellinen luettelo perusteista nimikkeen kohdistamisesta suunnittelussa on kohdassa [Rakennetiedot: suunnittelun kohdistustaulukko](design-details-planning-assignment-table.md).  

Suunnittelun asetukset [!INCLUDE[prod_short](includes/prod_short.md)]:ssa ovat:  

-   Laske uudelleensuunnittelu – laskee kaikki valitut nimikkeet riippumatta siitä, onko se tarpeen vai ei.  
-   Laske nettomuutossuunnitelma – laskee vain ne valitut kohteet, joiden kysyntä-tarjonta-malli on muuttunut jollain tavalla ja jotka on tämän vuoksi määritetty suunnitteluun.  

Jotkut käyttäjät uskovat, että nettomuutossuunnittelu tulee suorittaa kiireesti, esimerkiksi, kun myyntitilaukset on syötetty. Tämä voisi kuitenkin olla sekavaa, koska dynaaminen tilauksen seuranta ja toimenpideviestitys lasketaan myös lennossa. Sen lisäksi [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa reaaliaikaisen luvattavissa-ohjausobjektin, joka tarjoaa myyntitilauksia kirjoitettaessa varoitukset ponnahdusikkunassa, jos kysyntää ei voida täyttää nykyisen toimitussuunnitelman mukaisesti.  

Näiden lisäksi suunnittelujärjestelmä suunnittelee vain niille nimikkeille, jotka käyttäjä on valmistellut asianmukaisilla suunnitteluparametreilla. Muutoin oletetaan, että käyttäjä suunnittelee nimikkeet manuaalisesti tai puoliautomaattisesti käyttämällä Tilauksen suunnittelu -ominaisuutta.  

Lisätietoja automaattisista suunnittelumenetelmistä on kohdassa [Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Nimikedimensiot

Kysynnällä ja tarjonnalla saattaa olla varianttikoodeja, jotka on otettava huomioon, kun suunnittelujärjestelmä täsmäyttää kysyntää ja tarjontaa.  

Järjestelmä käsittelee variantti- ja sijaintikoodeja nimikedimensioina esimerkiksi myyntitilausrivillä ja inventointitapahtumassa. Näin ollen se laskee suunnitelman jokaisen variantin ja sijainnin yhdistelmän osalta kuin yhdistelmä olisi erillinen nimikenumero.  

Sen sijaan että laskettaisi teoreettinen varianttien ja sijaintien yhdistelmä, sovellus laskee vain ne yhdistelmät, jotka ovat todellisuudessa tietokannassa.  

Lisätietoja suunnittelujärjestelmän tavasta käsitellä kysynnän sijaintikoodeja on kohdassa [Rakennetiedot: kysyntä tyhjä-sijainnissa](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Nimikkeen määritteet

Yleisistä nimikedimensioista riippumatta, kuten nimikenumero, varianttikoodi, sijaintikoodi ja tilaustyyppi, jokainen kysyntä- ja tarjontatapahtuma voi sisältää lisämäärityksiä sarja- eränumeroiden muodossa. Suunnittelujärjestelmä suunnittelee nämä ominaisuudet tietyillä tavoilla riippuen niiden yksityiskohtaisuuden tasosta.  

Tilauskohtainen linkki kysynnän ja tarjonnan välillä on toinen määritetyyppi, joka vaikuttaa suunnittelujärjestelmään.  

### <a name="specific-attributes"></a>Tietyt attribuutit

Eräät kysynnän määritteet ovat erityisiä ja ne on kohdistettava tarkalleen vastaavan tarjonnan mukaan. Seuraavat kaksi erityisominaisuutta on olemassa:  

-   Pyydetyt sarja- tai eränumerot, jotka edellyttävät tiettyä sovellusta. ( Nimikkeen käyttämälle nimikkeen seurantakoodille on valittu **SN-kohtainen seuranta** tai **Eräkohtainen seuranta** -valintaruutu on valittu **Nimikk. seurantakoodin kortti** -sivulla.)  
-   Manuaalisesti tai automaattisesti tietylle kysynnälle toimitustilauksiin luodut linkit (tilausten väliset linkit).  

Näiden määritteiden osalta suunnittelujärjestelmä soveltaa seuraavia sääntöjä:  

-   Tietyillä määritteillä varustettu kysyntä voidaan täyttää vain tarjonnalla, jolla on vastaavat määritteet.  
-   Tarjonta, jossa on erityiset tunnusmerkit, voi myös tyydyttää kysynnän, jossa ei erityisesti vaadita kyseisiä tunnusmerkkejä.  

Näin ollen, jos varasto tai oletetut tarvikkeet eivät täytä tiettyjen määritteiden kysyntää, suunnittelujärjestelmä ehdottaa uutta toimitustilausta tietyn kysynnän kattamiseksi suunnitteluparametreja huomioimatta.  

### <a name="non-specific-attributes"></a>Epäspesifiset määritteet

Sarja-/eränumeroidut nimikkeet ilman erityistä nimikeseuranta-asetusta voi välittää sarja-/eränumeroita, joita ei tarvitse soveltaa täysin samaan sarja-/eränumeroon, mutta niitä voidaan soveltaa mihin tahansa sarja-/eränumeroon. Tämän avulla suunnittelujärjestelmä voi vapaammin kohdistaa esimerkiksi sarjanumeron omaavan kysynnän sarjanumeron omaavaan tarjontaan, joka on yleensä varasto.  

Kysyntä-tarjonta sarja- tai eränumeroiden kanssa, erityinen tai ei erityinen, määritetään korkean prioriteetin tilanteeksi ja tämän vuoksi vapautettu jäädytetystä vyöhykkeestä, joka tarkoittaa, että ne ovat osa suunnittelua, vaikka ne erääntyvät ennen suunnittelun aloituspäivää.  

Katso lisätietoja [Sarja-/ eränumerot ladataan määritystason mukaan](design-details-balancing-demand-and-supply.md#seriallot-numbers-are-loaded-by-specification-level) -osiosta.

Saat lisätietoja siitä, kuinka suunnittelujärjestelmä täsmäyttää määritteet kohdasta [Sarja- /eränumeroita ja tilausten välisiä linkkejä ei huomioida kiinnitetyillä alueilla](design-details-balancing-demand-and-supply.md#seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone).  

## <a name="order-to-order-links"></a>Tilausten väliset linkit

Tilausten välinen hankintaluokka tarkoittaa, että nimike ostetaan, kootaan tai tuotetaan erityisesti kattamaan tietty kysyntä. Yleensä tämä liittyy A-nimikkeisiin. Tämä tapa valitaan esimerkiksi silloin, kun kysyntä ei ole säännöllistä, toimitusajalla ei ole merkitystä tai pakolliset määritteet vaihtelevat.  

Toinen erityistapaus, joka käyttää tilaustenvälisiä linkkejä on kokoonpanotilauksen linkitys myyntitilaukseen kokoonpano tilausta varten -skenaariossa.  

Tilausten välisiä linkkejä käytetään kysynnän ja tarjonnan välillä neljällä tavalla:  

-   Kun suunniteltu nimike käyttää Tilaus-uusintatilaustapaa.  
-   Kun usean tason tai projektityyppisiä tuotantotilauksia luodaan tilausohjatun tuotantotavan avulla (tarvittavat komponentit sisältyvät samaan tuotantotilaukseen).  
-   Kun tuotantotilauksia luodaan myyntitilauksille, joilla on myyntitilauksen suunnittelutoiminto.  
-   Kun nimikettä määritetään myyntitilauksen kokoonpanoon. (Kokoonpanokäytännön asetus on kokoonpano tilausta varten.  

Näissä tapauksissa suunnittelujärjestelmä ehdottaa vain tarvittavan määrän tilaamista. Luonnin jälkeen osto-, tuotanto- tai kokoonpanotilaus kohdistuu edelleen vastaavaan kysyntään. Esimerkiksi jos myyntitilaus on vaihdettu ajan tai määrän osalta, suunnittelujärjestelmä ehdottaa, että vastaava toimitustilaus muutetaan vastaavasti.  

Kun tilausten välisiä linkkejä on määritetty, suunnittelujärjestelmä ei käytä linkitettyä tarjontaa tai varastoa täsmäytyksessä. Käyttäjän vastuulla on arvioida, tulisiko linkitettyä tarjontaa käyttää kattamaan toinen vai uusi kysyntä ja tässä tapauksessa poistaa toimitustilaus vai varata linkitetty tarjonta manuaalisesti.  

Varaukset ja tilausseurantalinkit katkeavat, jos tilanne menee mahdottomaksi, kuten jos vaatimusta siirretään aiemmalle päivälle kuin toimitus. Tilausten välinen linkki mukautuu kuitenkin kaikkiin muutoksiin vastaavassa kysynnässä tai tarjonnassa ja tämän vuoksi linkki ei katkea koskaan.  

## <a name="reservations"></a>Varaukset

Suunnittelujärjestelmä ei sisällytä mitään varattuja määriä laskelmaan. Esimerkiksi, jos myyntitilaus on kokonaan tai osittain varattu määrä varastossa olevaa määrää vastaan, varaston varattua määrää ei voida käyttää muun kysynnän kattamiseksi. Suunnittelujärjestelmä ei sisällytä tätä kysyntä-tarjonta-sarjaa laskelmaansa.  

Suunnittelujärjestelmä sisällyttää kuitenkin edelleen varatut määrät suunnitellussa varastoprofiilissa, koska kaikki määrät on otettava huomioon määritettäessä sitä hetkeä, jolloin uusintatilauspiste on ohitettu ja kuinka monta tilataan uudelleen enimmäisvarastotason saavuttamiseksi sitä ylittämättä. Näin ollen tarpeettomat varaukset johtavat kasvavaan riskiin, että varastomäärät vähenevät alhaisiksi, koska suunnittelulogiikka ei tunnistanut varattuja määriä.  

Seuraavassa kuvassa esitetään, kuinka varaukset voivat estää kaikista todennäköisimmän suunnitelman.  

![Varausten suunnittelu.](media/NAV_APP_supply_planning_1_reservations.png "Varausten suunnittelu")  

Lisätietoja on kohdassa [Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Varoitukset

Ensimmäinen suunnittelutaulukon sarake on varoituskenttiä varten. Kaikki epätavallisessa tilanteessa luodut suunnittelurivit tuottavat tähän kenttään varoituskuvakkeen, jota napsauttamalla käyttäjä saa lisätietoja.  

Tarjontaa suunnitteluriveillä, joilla on varoituksia, ei tavallisesti muokata suunnitteluparametrien mukaan. Suunnittelujärjestelmä ehdottaa sen sijaan vain toimitusmäärää, joka kattaa kysyntämäärän täsmällisesti. Järjestelmä voidaan kuitenkin määrittää noudattamaan tiettyjä suunnittelurivien suunnitteluparametreja, joihin liittyy tiettyjä varoituksia. Lisätietoja on seuraavien erätöiden vaihtoehtojen kuvauksissa: **Laske suunn. - Suunn.työk.** ja **Laske suun. - hankintatyök.** .  

Varoituksen tiedot näytetään **Ei-seuratut suunnitteluelementit** -sivulla, jossa näkyvät myös niiden yksiköiden tilauksen seurantalinkit, jotka eivät ole tilauksia. Varoitustyyppejä on kolme:  

-   Hätä  
-   Poikkeus  
-   Huomautus  

![Suunnittelutyökirjan varoitukset.](media/NAV_APP_supply_planning_1_warnings.png "Suunnittelutyökirjan varoitukset")  

### <a name="emergency"></a>Hätä

Hätä-varoitus tulee näkyviin kahdessa tilanteessa:  

-   Kun varasto on negatiivinen suunnittelun aloituspäivämääränä.  
-   Kun nykyhetkeä aikaisempia tarjonta- tai kysyntätapahtumia on olemassa.  

Jos nimikkeen varasto on negatiivinen suunnittelun aloituspäivämääränä, suunnittelujärjestelmä ehdottaa negatiiviselle määrälle hätätilausta, joka saapuu suunnittelun aloituspäivämääränä. Varoitustekstissä kerrotaan aloituspäivämäärä ja hätätilauksen määrä. Lisätietoja on kohdassa [Suunnitellun negatiivisen varaston käsittely](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Jos asiakirjassa on rivejä, joiden eräpäivä on ennen suunnittelun aloituspäivämäärää, rivit yhdistetään yhdeksi hätätoimitustilaukseksi, jotta nimike saapuisi suunnittelun aloituspäivämääränä.  

### <a name="exception"></a>Poikkeus

Poikkeus-varoitus näytetään, jos oletettu saatavilla oleva varasto pienenee varmuusvaraston määrää pienemmäksi. Suunnittelujärjestelmä ehdottaa toimitustilausta, joka täyttää kysynnän eräpäivänä. Varoitustekstissä kerrotaan nimikkeen varmuusvaraston määrä ja päivämäärä, jolloin se vähenee liian pieneksi.  

Varmuusvaraston tason alittaminen aiheuttaa poikkeuksen, koska näin ei pitäisi käydä, jos uusintatilauspiste on määritetty oikein. Lisätietoja on kohdassa [Uusintatilauspisteen rooli](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Yleisesti ottaen poikkeukselliset tilausehdotukset varmistavat, että arvioitu käytettävissä oleva varasto ei ole koskaan varmuusvaraston tasoa alhaisempi. Tämä tarkoittaa sitä, että ehdotettu määrä riittää kattamaan vain varmuusvaraston ottamatta suunnitteluparametreja huomioon. Kuitenkin joissakin tilanteissa tilausmääritteet otetaan huomioon.  

> [!NOTE]  
>  Suunnittelujärjestelmä on saattanut käyttää varmuusvaraston tarkoituksellisesti ja täydentää sen välittömästi. Lisätietoja on ohjeaiheessa [Varmuusvarastoa voidaan käyttää](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### <a name="attention"></a>Huomautus

Huomautus-varoitus tulee näkyviin kolmessa tilanteessa:  

-   Suunnittelun aloituspäivämäärä on varhaisempi kuin käsittelypäivämäärä.  
-   Suunnittelurivi ehdottaa vapautetun osto- tai tuotantotilauksen vaihtamista.  
-   Käsitelty varasto ylittää ylitystason eräpäivänä. Lisätietoja on kohdassa [Sallitun ylityksen alapuolella pysytteleminen](design-details-handling-reordering-policies.md#staying-under-the-overflow-level).  

> [!NOTE]  
>  Suunnitteluriveillä, joilla on varoituksia, ei valita **Hyväksy toimenpideviesti** -kenttää, koska suunnitteluohjelman oletetaan tutkivan tarkemmin näitä rivejä ennen suunnitelman toteutusta.  

## <a name="error-logs"></a>Virhelokit

Laske suunnitelma -pyyntösivulla käyttäjä voi valita **Pysäytä ja Näytä ensimmäinen virhe**-kentän, jotta suunnitelman ajo pysähtyy, kun se kohtaa ensimmäisen virheen. Samalla näyttöön tulee sanoma, jossa on tietoja virheestä. Virhetilanteessa vain ennen virheen ilmenemistä tehdyt onnistuneet suunnittelurivit esitetään suunnittelutyökirjassa.  

Jos kenttää ei ole valittu, Laske suunnitelma -eräajo jatkaa suoritusta loppuun asti. Virheet eivät keskeytä eräajoa. Jos virheitä ilmenee, sovellus tuo eräajon jälkeen näkyviin sanoman, jossa ilmoitetaan kuinka moneen nimikkeeseen virheet vaikuttavat. Tämän jälkeen avautuu **Suunnittelun virheloki** -sivu, jossa on lisätietoja virheestä ja linkit vaikutusalueeseen kuuluviin asiakirjoihin tai asetuskortteihin.  

![Virhesanomat suunnittelutyökirjassa.](media/NAV_APP_supply_planning_1_error_log.png "Virhesanomat suunnittelutyökirjassa")  

## <a name="planning-flexibility"></a>Suunnittelun joustavuus

Ei ole aina käytännöllistä suunnitella olemassa olevaa toimitustilausta, kuten silloin, kun tuotanto on käynnistynyt tai henkilöstöä on palkattu lisää tiettynä päivänä työn suorittamiseksi. Kaikilla toimitustilauksen riveillä on Suunnittelun joustavuus -kenttä, jolla on kaksi valintaa: Rajaton tai Ei mitään. Tämän kentän avulla osoitetaan, voiko suunnittelujärjestelmä muuttaa olemassa olevan tilauksen. Jos kentän arvoksi on asetettu Ei mitään, suunnittelujärjestelmä ei yritä muuttaa toimitustilauksen riviä.  

Käyttäjä voi manuaalisesti määrittää kentän, kuitenkin joissa tapauksissa järjestelmä määrittää sen automaattisesti. Se fakta, että käyttäjä voi määrittää manuaalisesti suunnittelun joustavuuden on tärkeä, koska sen ansiosta on helppoa mukauttaa ominaisuuden käyttö erilaisiin työnkulkuihin ja liiketoimintatapauksiin.  

Lisätietoja tämän kentän käytöstä on kohdassa [Rakennetiedot: siirrot suunnittelussa](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Tilauksen suunnittelu

**Tilausten suunnittelu** -sivulla esitelty perustyökalu tarjonnan suunnitteluun on suunniteltu manuaaliseen päätöstentekoon. Se ei ota huomioon mitään suunnitteluparametreja ja sitä ei näin ollen käsitellä tarkemmin tässä asiakirjassa. Lisätietoja on kohdassa [Uuden kysyntätilauksen suunnitteleminen tilauksen mukaan](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Ei ole suositeltavaa käyttää Tilauksen suunnittelu -toimintoa, jos yrityksessä jo käytetään suunnitelussa suunnittelutyökirjaa tai hankintalistaa. **Tilauksen suunnittelu** -sivun kautta luotuja toimitustilauksia voidaan muuttaa tai poistaa automaattisten suunnitteluajojen aikana. Tämä johtuu siitä, että automaattisissa suunnitteluajoissa käytetään suunnitteluparametreja, joita Tilauksen suunnittelu -sivulla manuaalisen suunnitelman laatinut käyttäjä ei välttämättä ole ottanut huomioon.  

## <a name="finite-loading"></a>Äärellinen kuormitus

[!INCLUDE[prod_short](includes/prod_short.md)] on tavallinen ERP-järjestelmä, ei lähetyksen tai työnohjauksen ohjausjärjestelmä. Se suunnittelee resurssien käytön tarjoamalla karkean aikataulun, mutta se ei luo ja ylläpidä automaattisesti tarkkoja aikatauluja prioriteetteihin tai optimointisääntöihin perustuen.  

Kapasiteettirajoitteisten resurssien suunniteltu käyttötoiminto käsittää: 1) välttää eritysresurssien ylikuormitusta ja 2) varmistaa, että kapasiteettia ei ole kohdentamatta, jos se voisi kasvattaa tuotantotilauksen paluuaikaa. Ominaisuus ei sisällä välineitä tai vaihtoehtoja priorisoida tai optimoida toimintoja, kuten voisi olettaa löytyvän lähetysjärjestelmästä. Se voi kuitenkin tarjota hyödyllisen karkean kapasiteettitiedon pullonkaulojen tunnistamiseksi ja resurssien ylikuormituksen estämiseksi.  

Kun suunnitellaan kapasiteettirajoitettuja resursseja, järjestelmä varmistaa, että resurssia ei ole kuormitettu enempää kuin sille määritetty kapasiteetti osoittaa (kriittinen kuormitus). Tämä tehdään määrittämällä jokaiselle toiminnolle lähin mahdollinen aika. Jos ajankohta ei ole tarpeeksi suuri koko toiminnon suorittamiseksi, toiminto jaetaan kahdeksi tai useammaksi osaksi, jotka sijoitetaan lähimpiin käytettävissä oleviin ajankohtiin.  

> [!NOTE]  
> Jos toiminto jaetaan, asetusaika kohdistetaan vain kerran, koska oletetaan, että jotkin manuaaliset muutokset suoritetaan aikataulun optimoimiseksi.  

Resursseihin voidaan lisätä puskuriaika toiminnon jaon minimoimiseksi. Tämän avulla järjestelmä ajoittaa kuormituksen viimeiseen mahdolliseen päivään niin, että kriittinen kuormitusprosentti ylittyy hieman. Tämä voi vähentää jaettavien toimintojen määrää.  

Tämä täydentää keskeisten konseptien luonnoksen, joka liittyy [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman tarjonnan suunnitteluun. Seuraavat osat tutkivat näitä konsepteja tarkemmin ja asettavat ne ydinsuunnitteluprosessien kontekstiin, tasapainottaen kysynnän ja tarjonnan sekä jälkitilausohjeiden käytön.  

## <a name="see-also"></a>Katso myös

[Rakennetiedot: siirrot suunnittelussa](design-details-transfers-in-planning.md)  
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)  
[Rakennetiedot: suunnittelun kohdistustaulukko](design-details-planning-assignment-table.md)  
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)  
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
