---
title: Rakennetiedot – suunnittelujärjestelmän keskeiset käsitteet
description: Suunnittelu ehdottaa käyttäjälle mahdollisia toimia kysyntä- ja tarjontatilanteen sekä nimikkeiden suunnitteluparametrien perusteella.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet

Suunnittelutoiminnot on sisällytetty eräajoon, joka ensin valitsee asiaankuuluvat nimikkeet ja ajanjaksot, jotka suunnitellaan. Erätyö kutsuu sitten kunkin nimikkeen alatason koodin mukaisen (sijainti tuoterakenteessa) codeunitin, joka laskee tarjontasuunnitelman. Codeunit täsmäyttää kysyntä- ja tarjontajoukot sekä ehdottaa käyttäjälle toimintoja. Ehdotetut toimenpiteet ilmestyvät riveinä suunnittelutaulukkoon tai tilaustaulukkoon.  

![Suunnittelutyökirjasivun sisältö.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Suunnittelutyökirja-sivun sisältö")  

Yrityksen suunnittelijan, kuten ostajan tai tuotantosuunnittelijan, oletetaan olevan suunnittelujärjestelmän käyttäjä. Suunnittelujärjestelmä auttaa käyttäjää suorittamaan laajat, mutta melko suoraviivaiset suunnitelman laskelmat. Tämän jälkeen käyttäjä voi keskittyä ratkaisemaan vaikeampia ongelmia, kuten esimerkiksi poikkeustilanteiden hallintaa.  

Suunnittelujärjestelmää ohjaa ennakoitu ja nykyinen asiakaskysyntä, kuten ennuste ja myyntitilaukset. Suunnittelun laskelmat ehdottavat toimintoja, joita voidaan tehdään toimittajilta saatavan tarjonnan, kokoonpanon tai tuotannon taikka muista varastoista tehtävien siirtojen osalta. Ehdotettu toiminto voi olla esimerkiksi uusien toimitustilausten, kuten osto- tai tuotantotilausten, luominen. Jos toimitustilauksia on jo tehty, ehdotettuja toimenpiteitä voivat olla tilausten lisääminen tai nopeuttaminen muuttuneen kysynnän mukaisiksi.  

Suunnittelujärjestelmän toinen tavoite on varmistaa, että varasto ei kasva tarpeettoman suureksi. Jos kysyntä vähenee, suunnittelujärjestelmä ehdottaa käyttäjälle aiemmin luotujen toimitustilausten lykkäämistä, pienentämistä tai peruuttamista.  

Codeunit sisältää suunnittelulogiikan ja seuraavat toiminnot:

* Tarvelaskenta ja tuotanto-ohjelma
* Laske nettomuutossuunnitelma
* Laske uudelleensuunnittelu

Tarjontasuunnitelman laskentaan liittyy kuitenkin eri alajärjestelmiä.  

Suunnittelujärjestelmä ei sisällä erityistä logiikkaa kapasiteetin tasaamiseen tai aikataulun tarkentamiseen. Tällainen ajoitustyö tehdään erikseen. Kahden alueen välisen suoran integroinnin puuttuminen tarkoittaa myös sitä, että merkittävät kapasiteetti- tai aikataulumuutokset edellyttävät suunnittelun suorittamista uudelleen.  

## <a name="planning-parameters"></a>Suunnittelun parametrit

Nimikkeelle tai nimikeryhmälle määritetyt suunnitteluparametrit hallitsevat sitä, mitä toimintoja suunnittelujärjestelmä ehdottaa eri tilanteissa. Kullekin nimikkeelle määritetään suunnitteluparametrit määrittämään täydennyksen ajankohtaa ja määrää sekä täydennystapaa.  

Suunnitteluparametreja voidaan myös määrittää mille tahansa nimikkeen, variantin ja sijainnin yhdistelmälle määrittämällä varastointiyksikkö (SKU) kullekin yhdistelmälle ja määrittämällä sitten yksittäiset parametrit. Lisätietoja on kohdissa [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md) ja [Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Suunnittelun aloituspäivämäärä

Suunnittelujärjestelmä auttaa välttämään tilausten avaaminen menneisyydessä ja ehdottamaan toimintoja, jotka eivät ole mahdollisia. Suunnittelu käsittelee kaikkia aloituspäivämäärää edeltäviä päivämääriä jäädytettynä alueena. Seuraava sääntö pätee jäädytettyyn alueeseen:  

* Kaikkea suunnittelujakson aloituspäivämäärää edeltävää kysyntää ja tarjotaan pidetään varaston osana tai toimitettuna. Se siis olettaa aiempi suunnitelma suoritetaan määritetyn suunnitelman mukaan. Lisätietoja on kohdassa [Suunnittelun aloituspäivämäärää edeltävien tilausten käsitteleminen](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).  

## <a name="dynamic-order-tracking-pegging"></a>Dynaaminen tilausseuranta (tarvekohdistus)

Dynaaminen tilausseuranta ja sen samanaikaisesti suunnittelutyökirjassa luomat toimenpideviestit eivät ole tarjonnan suunnittelujärjestelmän osa. Kun kysyntä ja tarjonta luodaan tai niitä muutetaan, dynaaminen tilauksen seuranta linkittää kysynnän ja sen kattavat määrät reaaliaikaisesti.  

Jos myyntitilaus esimerkiksi syötetään tai sitä muutetaan, dynaaminen tilauksen seuranta hakee heti kysynnän kattavan tarjonnan. Tarjonta voidaan saada varastosta tai odotetusta toimitustilauksesta (kuten osto- tai tuotantotilauksesta). Kun [!INCLUDE [prod_short](includes/prod_short.md)] löytää tarjontalähteen, kysyntä ja tarjonta linkitetään. Linkki on käytettävissä asiakirjarivien vain luku -sivuilla. Jos tarjontaa ei löydy, dynaaminen tilausten seurantajärjestelmä luo suunnittelutyökirjaan toimenpideviestejä, jotka sisältävät tarjontasuunnitelman ehdotuksia.  

Dynaaminen tilauksen seuranta auttaa arvioimaan toimitustilausehdotusten hyväksymistä. Tarjonnan puolella näkyvissä on tarjonnan luonut kysyntä. Kysynnän puolella määritetään kysynnän kattava tarjonta.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking.png" alt-text="Esimerkki dynaamisesta tilausten seurannasta.":::

Lisätietoja on kohdassa [Rakennetiedot: varaus, tilauksen seuranta ja toimenpideviestit](design-details-reservation-order-tracking-and-action-messaging.md).  

Jos yritysten nimikevirta on vähäinen ja tuoterakenteet yksinkertaisia, dynaaminen tilauksen seuranta saattaa olla riittävä ratkaisun tarjonnan suunnitteluun. Kiireisissä ympäristöissä on kuitenkin käytettävä suunnittelujärjestelmää varmistamaan, että toimitussuunnitelma on tasapainoinen.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Dynaaminen tilausseuranta verrattuna suunnittelujärjestelmään

Suunnittelujärjestelmän ja dynaamisen tilauksen seurannan erottaminen toisistaan voi olla hankalaa. Molemmat ominaisuudet näyttävät tulosteen suunnittelutyökirjalla ehdottamalla toimia, jotka suunnittelijan tulisi suorittaa. Tämän tuotoksen tuotantotapa kuitenkin poikkeaa.  

Suunnittelujärjestelmä käsittelee nimikkeen koko kysyntä- ja tarjontamallia. Se ottaa huomioon kaikki aikajanalle sijoitetut tuoterakennehierarkian tasot. Dynaaminen tilauksen seuranta käsittelee vain sen tilauksen tilanteen, joka aiheutti aktivoinnin. Suunnittelujärjestelmän tasapainottaa kysynnän ja tarjonnan luomalla linkkejä käyttäjän aktivoimassa erätilassa. Dynaaminen tilauksen seuranta luo linkit automaattisesti, kun kysyntä tai tarjonta syötetään. Näin tapahtuu esimerkiksi myynti- tai ostotilausta luotaessa.  

Dynaaminen tilauksen seuranta linkittää kysynnän ja tarjonnan saapumisjärjestyksen perusteella, kun tietoja syötetään. Tämä periaate voi muuttaa prioriteettien järjestystä. Esimerkiksi ensin syötetty myyntitilaus, jonka eräpäivä on seuraavassa kuussa, saatetaan linkittää varaston tarjontaan Seuraava huomenna erääntyvä myyntitilaus voi puolestaan aiheuttaa uuden ostotilauksen luovan toimenpideviestin. Seuraavassa kuvassa näkyy tämä skenaario.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking_graph.png" alt-text="Esimerkki tilausten seurannasta toimitusten suunnittelussa 1.":::

Suunnittelujärjestelmä käsittelee nimikkeiden kysyntää ja tarjontaa prioriteettijärjestyksessä. Järjestys priorisoidaan eräpäivien ja tilaustyyppien perusteella. Kyse on siis siitä, että ensimmäiseksi tarvittava käsitellään ensimmäiseksi. Se poistaa kaikki dynaamisesti luodut tilauksen seurantalinkit ja muodostaa ne uudelleen eräpäivän prioriteetin mukaisesti. Kun suunnittelujärjestelmän käyttö lopetetaan, se on ratkaissut kysynnän ja tarjonnan välisen epätasapainon. Tämä osoitetaan myös alla olevassa kuvassa.

:::image type="content" source="media/nav_app_supply_planning_1_planning_graph.png" alt-text="Esimerkki tilausten seurannasta toimitusten suunnittelussa 2.":::  

Suunnittelun suorittamisen jälkeen Toimenpideviestitapahtuma-taulukossa ei ole toimenpideviestejä. Näiden viestin tilalla on suunnittelutyökirjassa ehdotettuja toimenpiteitä. Lisätietoja on kohdassa [Tilauksen seurantalinkit suunnittelun aikana](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).  

## <a name="sequence-and-priority-in-planning"></a>Suunnittelun järjestys ja ensisijaisuus

Suunnitelman laskentajärjestys on tärkeä, sillä sen avulla työ voidaan tehdä kohtuullisessa ajassa. Myös tarpeiden ja resurssien priorisoinnilla on tärkeä merkitys parhaiden tulosten saamisessa.  

Suunnittelujärjestelmä on tarveperustainen. Korkean tason nimikkeet on suunniteltava ennen alatason nimikkeitä, koska korkean tason nimikkeet voivat luoda alatason nimekkeiden kysyntää. Esimerkiksi vähittäismyyntisijainnit kannatta suunnitella ennen jakelukeskusten sijaintia, koska vähittäismyyntisijainti saattaa kysyntää jakelukeskuksesta. Yksityiskohtaisella täsmäytystasolla puolestaan järjestelmän ei pitäisi luoda uutta toimitustilausta, jos vapautettu toimitustilaus kattaa myyntitilauksen. Tarjontaa, jolla on tietty eränumero, ei pitäisi kohdistaa kattamaan yleistä kysyntää, jos toinen kysyntä edellyttää kyseistä erää.  

### <a name="item-priority--low-level-code"></a>Nimikkeen prioriteetti/alatason koodi

Valmistusympäristössä valmiiden, myytävien nimikkeiden kysyntä aiheuttaa valmiin nimikkeen koostavien komponenttien johdettua kysyntää. Materiaalilasku-rakenne kontrolloi osan rakennetta ja voi kattaa useita puolivalmiiden nimikkeiden tasoja. Yhden nimikkeen suunnittelu yhdellä tasolla aiheuttaa epäsuoraa kysyntää seuraavan tason komponenteille. Tämä hierarkia johtaa lopulta ostettujen nimikkeiden epäsuoraan kysyntään. Suunnittelujärjestelmä tekee nimikkeille suunnitelmia siinä järjestyksessä, mikä on niiden sijoitus tuoterakenteen kokonaishierarkiassa. Ensimmäisenä järjestelmä käsittelee ylätasolla olevat valmiit myytävät tuotteet ja jatkaa sitten tuoterakenteessa alaspäin alempien tasojen nimikkeisiin (alatason koodin mukaisesti).  

Seuraavassa kuvassa on järjestys, jossa [!INCLUDE [prod_short](includes/prod_short.md)] ehdottaa toimitustilauksia ylätasolla. Siinä oletetaan, että ehdotukset hyväksyttiin. Myös alatason nimikkeet ovat näkyvissä.

:::image type="content" source="media/nav_app_supply_planning_1_bom_planning.png" alt-text="Tuoterakenteiden suunnitelma.":::

Lisätietoja tuotantonäkökohdista on kohdassa [Varastoprofiilien lataaminen](design-details-balancing-demand-and-supply.md#load-inventory-profiles).  

#### <a name="optimizing-performance-for-low-level-calculations"></a>Suorituskyvyn optimoiminen matalan tason laskelmissa

Alatason koodilaskelmat voivat vaikuttaa järjestelmän suorituskykyyn. Vaikutusta voi vähentää poistamalla **Dynaamisen matalan tason koodilaskennan** -ominaisuuden käytöstä vaihtopainikkeella **Tuotannon asetukset** -sivulla. Siinä tapauksessa [!INCLUDE[prod_short](includes/prod_short.md)] ehdottaa toistuva työjonotapahtuman luomista päivittämään alatason koodit päivittäin. Voit varmistaa, että työ suoritetaan työajan ulkopuolella, määrittämällä aloitusajan **Aikaisin alkamispäivä ja -aika** -kentässä.

Alatason koodilaskelmia voidaan toisaalta nopeuttaa ottamalla **Tuotannon asetukset** -sivulla **Optimoi alatason koodin laskenta** -vaihtoehdon käyttöön vaihtopainikkeella.

> [!IMPORTANT]
> Jos optimoit suorituskyvyn, [!INCLUDE[prod_short](includes/prod_short.md)] käyttää uusia laskentamenetelmiä alatason koodien määrittämiseen. Jos käytössä on laajennus, joka perustuu vanhojen laskelmien käyttämiin tapahtumiin, laajennus saattaa lakata toimimasta.

### <a name="locations--transfer-level-priority"></a>Sijainnit/siirtotason prioriteetti

Yritysten, jotka toimivat useissa sijainnissa, on ehkä tehtävä suunnittelu kullekin sijainnille erikseen. Esimerkiksi nimikkeen varmuusvaraston taso ja sen uusintatilaustapa saattavat vaihdella sijainnista toiseen. Suunnitteluparametrit on määritettävä nimike- ja sijaintikohtaisesti.  

Yksittäisiä suunnitteluparametreja voi määrittää varastointiyksiköiden avulla. Varastointiyksikkö voidaan tulkita nimikkeeksi tietyssä paikassa. Jos sijainnille ei ole määritetty varastointiyksikköä, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää nimikekortissa määritettyjä parametreja. [!INCLUDE [prod_short](includes/prod_short.md)] laskee suunnitelman vain aktiivisille sijainneille, joissa annetulle nimikkeelle on kysyntää tai tarjontaa.  

Vaikka mitä tahansa nimike voidaan käsitellä missä tahansa sijainnissa, [!INCLUDE [prod_short](includes/prod_short.md)] käyttää sijaintikäsitettä tarkkarajaisesti. Esimerkiksi yhdessä sijainnissa olevaa myyntitilausta ei voida täyttää toisessa sijainnissa olevasta varastosta. Varaston määrä tulee ensin siirtää myyntitilauksessa määritettyyn sijaintiin.

:::image type="content" source="media/nav_app_supply_planning_1_sku_planning.png" alt-text="Varastointiyksiköiden suunnittelu":::

Lisätietoja on kohdassa [Rakennetiedot: siirrot suunnittelussa](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Tilauksen prioriteetti

Pyydetty tai käytettävissä oleva päivämäärä edustaa annetun varastointiyksikön korkeinta prioriteettia. Tämän päivän kysyntä tulee käsitellä ennen tulevien päivien kysyntää. Tällaista prioriteettia lukuun ottamatta kysynnän ja tarjonnan eri tyypit järjestetään liiketoiminnan tärkeyden perusteella, sillä näin voidaan päätellä, mihin kysyntään vastataan ensin. Tarjontapuolella tilauksen prioriteetti määrittää ensimmäisenä käytettävän tarjontalähteen. Lisätietoja on kohdassa [Tilausten priorisointi](design-details-balancing-demand-and-supply.md#prioritize-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Kysyntäennusteet ja puitetilaukset

Sekä ennustukset ja puitetilaukset esittävät odotettavissa olevaa kysyntää. Kestotilaus, joka kattaa asiakkaan suunnitellut ostot tietyltä aikajaksolta, vähentää yleisennusteen epävarmuutta. Seuraavassa kuvassa on puitetilaus, joka on asiakkaan määrittämä ennuste määrittämättömien ennusteiden lisäksi.  

:::image type="content" source="media/nav_app_supply_planning_1_forecast_and_blanket.png" alt-text="Ennusteiden käyttäminen suunnitelussa.":::

Lisätietoja on kohdassa [Myyntitilaukset vähentävät ennustettua kysyntää](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## <a name="planning-assignment"></a>Suunnittelun tehtävä

Jos kysyntä- tai tarjontamalli on muuttunet suunnitelman edellisen laskentakerran jälkeen, kaikki nimikkeet on suunniteltava uudelleen. Suunnitelma on laskettava uudelleen, jos esimerkiksi uusi myyntitilaus syötetään tai aiemmin luotua tilausta muutetaan. Muita uudelleensuunnittelun syitä ovat ennusteeseen tai varmuusvaraston määrään tehty muutos. Tuoterakenteen muuttaminen lisäämällä tai poistamalla komponentti ilmaisisi todennäköisesti myös muutosta mutta vain komponenttinimikkeen osalta.  

Suunnittelujärjestelmä tarkkailee tällaisia tapahtumia ja määrittää nimikkeet suunnitelmalle.  

Jos kyse on useista sijainnista, määritys tapahtuu nimiketasolla sijaintiyhdistelmäkohtaisesti. Jos myyntitilaus on luotu vain yhdessä sijainnissa, [!INCLUDE [prod_short](includes/prod_short.md)] määrittää nimikkeen kyseisessä sijainnissa tapahtuvaan suunnitteluun.  

Syy valita nimikkeitä suunnittelua varten on järjestelmän toimintaseikka. Jos nimikkeen kysyntä- ja tarjontamalli ei ole muuttunut, suunnittelujärjestelmä ei ehdota toimenpiteitä. Ilman suunnittelun määritystä järjestelmän on suoritettava kaikkien nimikkeiden laskelmat suunnitelmaa määritettäessä. Lisätietoja syistä, joiden vuoksi nimikkeitä määritetään suunnitteluun, on kohdassa [Rakennetiedot: suunnittelun määritystaulukko](design-details-planning-assignment-table.md).  

Seuraavassa suunnitteluvaihtoehdot ovat käytettävissä:  

* **Laske uudelleensuunnittelu** laskee kaikki valitut nimikkeet riippumatta siitä, onko se tarpeen vai ei.  
* **Laske nettomuutossuunnitelma** laskee vain ne nimikkeet, joiden kysyntä- ja tarjontamalli on muuttunut jollain tavalla ja jotka on tämän vuoksi määritetty suunnitteluun.  

Jotkut ovat sitä mieltä, että nettomuutossuunnittelu on suoritettava lennossa esimerkiksi silloin, kun myyntitilaukset on syötetty. Lennossa suunnittelu voi kuitenkin olla sekavaa, koska myös dynaaminen tilauksen seuranta ja toimenpideviestit lasketaan lennossa. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää reaaliaikaisen luvattavissa olevan määrän ohjausobjektin. Se mahdollistaa ponnahdusikkunassa näkyvät varoitukset, kun myyntitilauksia syötettäessä nykyinen tarjontasuunnitelma ei voi täyttää kysyntää.  

Suunnittelujärjestelmä ottaa suunnittelussa huomioon vain nimikkeet, joiden valmistelussa on käytetty soveltuvia suunnitteluparametreja. Muutoin oletetaan, että nimikkeet suunnitellaan manuaalisesti tai puoliautomaattisesti käyttämällä Tilauksen suunnittelu -ominaisuutta. Lisätietoja automaattisista suunnittelumenetelmistä on kohdassa [Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Nimikedimensiot

Kysynnällä ja tarjonnalla saattaa olla varianttikoodeja, jotka on otettava huomioon, kun suunnittelujärjestelmä täsmäyttää kysyntää ja tarjontaa.  

[!INCLUDE [prod_short](includes/prod_short.md)] käsittelee variantti- ja sijaintikoodeja nimikedimensioina esimerkiksi myyntitilausrivillä ja inventointitapahtumassa. Näin ollen se laskee suunnitelman jokaisen variantin ja sijainnin yhdistelmän osalta kuin yhdistelmä olisi erillinen nimikenumero.  

Sen sijaan että [!INCLUDE [prod_short](includes/prod_short.md)] laskisi teoreettiset varianttien ja sijaintien yhdistelmät, se laskee vain ne yhdistelmät, jotka ovat jo tietokannassa. Lisätietoja suunnittelujärjestelmän tavasta käsitellä kysynnän sijaintikoodeja on kohdassa [Rakennetiedot: kysyntä tyhjä-sijainnissa](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Nimikkeen määritteet

Nimikkeillä on usein yleisiä määritteitä, kuten nimikenumero, varianttikoodi, sijaintikoodi ja tilaustyyppi. Kussakin kysyntä- ja tarjontatapahtumassa voi olla kuitenkin muita määrityksiä, kuten sarja- tai eränumeroita. Suunnittelujärjestelmä suunnittelee nämä ominaisuudet tietyillä tavoilla riippuen niiden yksityiskohtaisuuden tasosta.  

Tilauskohtainen linkki kysynnän ja tarjonnan välillä on toinen määritetyyppi, joka vaikuttaa suunnittelujärjestelmään. Lisätietoja on kohdassa [Tilausten väliset linkit](#order-to-order-links).

### <a name="specific-attributes"></a>Tietyt attribuutit

Jotkin kysyntämääritteet määritettyjä ja tarjonnan on vastattava niitä tarkasti.

* Sarja- tai eränumerot, jotka edellyttävät tiettyä sovellusta. (Nämä määritteet ovat pakollisia, jos **SN-kohtainen seuranta** tai **Eräkohtainen seuranta** otetaan käyttöön vaihtopainikkeella nimikkeen käyttämän nimikkeen seurantakoodin **Nimikk. seurantakoodin kortti** -sivulla.)  
* Manuaalisesti tai automaattisesti tietylle kysynnälle toimitustilauksiin luodut linkit (tilausten väliset linkit).  

Suunnittelujärjestelmä käyttää näissä määritteissä seuraavia sääntöjä:  

* Tietyillä määritteillä varustettu kysyntä voidaan täyttää vain tarjonnalla, jolla on vastaavat määritteet.  
* Määritettyjä määritteitä sisältävä tarjonta voi täyttää myös kysyntää, jossa kyseisiä määritteitä ei nimenomaisesti edellytetä.  

Jos varasto tai ennustetut toimitukset eivät täytä määritettyjen määritteiden kysyntää, suunnittelujärjestelmä ehdottaa uutta toimitustilausta ottamatta huomioon suunnitteluparametreja.  

### <a name="non-specific-attributes"></a>Epäspesifiset määritteet

Sarja- tai eränumeroiduissa nimikkeissä, joilla ei ole tiettyjä nimikeseurantamäärityksiä, voi olla määrittämättömiä sarja- tai eränumeroita. Näitä numerotyyppejä voidaan käyttää missä tahansa sarja- tai eränumerossa. Suunnittelujärjestelmä voikin kohdistaa vapaammin esimerkiksi sarjoitetun kysynnän sarjoitettuun tarjontaan, mikä tapahtuu yleensä varastossa.  

Sarja- ja eränumeroita sisältävän kysynnän ja tarjonnan prioriteetti on korkea riippumatta siitä, onko kyse määritetystä tai määrittämättömästä sarja- tai eränumerosta, minkä lisäksi jäädytetty alue ei koske niitä. Ne ovat mukana suunnittelussa, vaikka niiden eräpäivä olisi ennen suunnittelun aloituspäivämäärää. Lisätietoja on kohdassa [Sarja- ja eränumero ladataan määritystason mukaan](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).

Lisätietoja suunnittelujärjestelmän määritteiden täsmäyttämisestä on kohdassa [Sarja- ja eränumeroita sekä tilausten välisiä linkkejä ei koske poisjättäminen edeltävältä jaksolta](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period).  

## <a name="order-to-order-links"></a>Tilausten väliset linkit

Tilausten välisyys tarkoittaa sitä, että nimike ostetaan, kootaan tai tuotetaan tietyn kysynnän perusteella. Tämän käytännön valitsemiseen on useita syitä:

* Kysyntä on epäsäännöllistä.
* Toimitusajalla ei ole merkitystä.
* Pakolliset määritteet vaihtelevat.  

Tilaustenvälisiä linkkejä käytetään myös tilanteessa, jossa kokoonpanotilaus linkitetään myyntitilaukseen kokoonpano tilausta varten -skenaariossa.  

Tilausten välisiä linkkejä käytetään kysynnän ja tarjonnan välillä neljällä tavalla:  

* Kun suunniteltu nimike käyttää **Tilaus**-uudelleentilauskäytäntöä.  
* Kun usean tason tai projektityyppisiä tuotantotilauksia luodaan tilausohjatun tuotantokäytännön avulla (komponentit sisältyvät samaan tuotantotilaukseen).  
* Kun tuotantotilauksia luodaan myyntitilauksille myyntitilauksen suunnittelutoiminnolla.  
* Kun nimike kootaan myyntitilaukseen (**Kokoonpanokäytäntö**-määrityksenä on **Kokoonpano tilausta varten**).  

Suunnittelujärjestelmä ehdottaa vain tarvittavan määrän tilaamista. Osto-, tuotanto- tai kokoonpanotilaus vastaa edelleen kysyntää. Jos esimerkiksi myyntitilauksen aikaa tai määrää on muutettu, suunnittelujärjestelmä ehdottaa, että toimitustilausta muutetaan vastaavasti.  

Kun tilausten välisiä linkkejä on määritetty, suunnittelujärjestelmä ei käytä linkitettyä tarjontaa tai varastoa täsmäytyksessä. Suunnittelijat voivat päättää, käytetäänkö linkitettyä tarjontaa vai uutta kysyntää. Jälkimmäisessä tapauksessa he voivat poistaa toimitustilauksen tai varata linkitetyn tarjonnan manuaalisesti.  

Varaukset ja tilauksen seurantalinkit katkeavat, jos tilanne muuttuu mahdottomaksi. Kyse voi olla esimerkiksi kysynnän siirtäminen tarjontaa aikaisempaan päivämäärään. Tilausten väliset linkit mukautuvat kysynnän ja tarjonnan muutoksiin eivätkä katkea koskaan.  

## <a name="reservations"></a>Varaukset

Suunnittelujärjestelmä ei sisällytä varattuja määriä laskelmiin. Jos esimerkiksi myyntitilauksen määrä on kokonaan tai osittain varattu, määrää ei voi käyttää muun kysynnän kattamiseen.

Suunnittelujärjestelmä ei sisällytä mitään varattuja määriä suunniteltuun varastoprofiiliin. Sen on otettava huomioon kaikki määrät, kun määritetään, milloin uudelleentilauspiste ohitettiin ja kuinka suuri uudelleentilauksen on oltava enimmäisvarastomäärän saavuttamiseksi. Tarpeettomat varaukset lisätä sen riskiä, että varastomäärät ovat liian pieniä, koska suunnittelulogiikka ei havainnut varattuja määriä.  

Seuraava kuva osoittaa, miten varaukset voivat haitata suunnittelua.  

:::image type="content" source="media/nav_app_supply_planning_1_reservations.png" alt-text="Varausten suunnittelu.":::

Lisätietoja on kohdassa [Rakennetiedot: varaus, tilauksen seuranta ja toimenpideviestit](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Varoitukset

Ensimmäinen suunnittelutaulukon sarake on varoituskenttiä varten. Varoituskuvake näkyy, kun epätavalliselle tilanteelle on luotu suunnittelurivi.  

Varoituksia sisältävien suunnittelurivien tarjontaa ei yleensä muokata suunnitteluparametrien mukaan. Suunnittelujärjestelmä ehdottaa sen sijaan toimitusta, joka kattaa täsmälleen kysynnän määrän. Järjestelmä voidaan kuitenkin määrittää noudattamaan sellaisten suunnittelurivien suunnitteluparametreja, joihin liittyy tiettyjä varoituksia. Varoituksen tiedot näkyvät **Ei-seuratut suunnitteluelementit** -sivulla, jossa näkyvät myös niiden tilausverkon ulkopuolisten yksiköiden tilauksen seurantalinkit. Varoitustyyppejä on kolme:  

* Hätä  
* Poikkeus  
* Huomautus  

:::image type="content" source="media/nav_app_supply_planning_1_warnings.png" alt-text="Suunnittelutyökirjan varoitukset.":::

### <a name="emergency"></a>Hätä

Hätävaroitus näytetään kahdessa tilanteessa:  

* Varasto on negatiivinen suunnittelun aloituspäivämääränä.  
* Nykyhetkeä aikaisempia tarjonta- tai kysyntätapahtumia on olemassa.  

Jos nimikkeen varasto on negatiivinen suunnittelun aloituspäivämääränä, suunnittelujärjestelmä ehdottaa negatiiviselle määrälle hätätilausta, joka saapuu suunnittelun aloituspäivämääränä. Varoitustekstissä kerrotaan aloituspäivämäärä ja hätätilauksen määrä. Lisätietoja on kohdassa [Rakennetiedot: suunnitellun negatiivisen varaston käsittely](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Asiakirjan rivit, joiden eräpäivä on ennen suunnittelun aloituspäivämäärää, yhdistetään yhdeksi hätätoimitustilaukseksi. Tilaus suunnitellaan saapuvaksi suunnittelun aloituspäivämääränä.  

### <a name="exception"></a>Poikkeus

Poikkeus-varoitus näytetään, jos oletettu saatavilla oleva varasto pienenee varmuusvaraston määrää pienemmäksi. Suunnittelujärjestelmä ehdottaa toimitustilausta, joka täyttää kysynnän eräpäivänä. Varoitustekstissä kerrotaan nimikkeen varmuusvaraston määrä ja päivämäärä, jolloin se vähenee liian pieneksi.  

Varmuusvaraston tasorikkomus on poikkeus. Sen ei pitäisi olla mahdollista, jos uudelleentilauspiste on määritetty oikein. Lisätietoja on kohdassa [Uusintatilauspisteen rooli](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Poikkeustilausehdotukset auttavat varmistamaan, että arvioitu käytettävissä oleva varasto ei ole koskaan varmuusvaraston tasoa alhaisempi. Ehdotettu määrä kattaa varmuusvaraston ottamatta suunnitteluparametreja huomioon. Kuitenkin joissakin tilanteissa tilausmääritteet otetaan huomioon.  

> [!NOTE]  
> Suunnittelujärjestelmä on saattanut käyttää varmuusvaraston tarkoituksellisesti ja täydentää sen välittömästi. Lisätietoja on kohdassa [Varmuusvaraston käyttäminen](design-details-balancing-demand-and-supply.md#consume-safety-stock).

### <a name="attention"></a>Huomautus

Huomautus-varoitus tulee näkyviin kolmessa tilanteessa:  

* Suunnittelun aloituspäivämäärä on varhaisempi kuin käsittelypäivämäärä.  
* Suunnittelurivi ehdottaa vapautetun osto- tai tuotantotilauksen vaihtamista.  
* Käsitelty varasto ylittää ylitystason eräpäivänä. Lisätietoja on kohdassa [Sallitun ylityksen alapuolella pysytteleminen](design-details-handling-reordering-policies.md#stay-below-the-overflow-level).  

> [!NOTE]  
> Varoituksia sisältävillä suunnitteluriveillä ei valita **Hyväksy toimenpideviesti** -kenttää, koska suunnitteluohjelman oletetaan tarkistavan rivit ennen suunnitelman toteutusta.  

## <a name="error-logs"></a>Virhelokit

**Laske suunnitelma** -pyyntösivulla voidaan valita **Pysäytä ja näytä ensimmäinen virhe** -kenttä, jolloin suunnitteluajo pysähtyy, kun ensimmäinen virhe havaitaan. Avautuvassa sanomassa on tietoja virheestä. Virhetilanteessa vain ennen virheen ilmenemistä onnistuneesti suoritetut suunnittelurivit näytetään suunnittelutyökirjassa.  

Jos kenttää ei ole valittu, **Laske suunnitelma** -eräajo jatkuu valmistumiseen saakka. Virheet eivät keskeytä eräajoa. Sanoma ilmoittaa, kuinka montaa kohdetta mahdolliset virheet koskevat. **Suunnittelun virheloki** -sivulla on lisätietoja virheestä ja linkit asiakirjoihin tai määrityksiin, joita virhe koskee.  

:::image type="content" source="media/nav_app_supply_planning_1_error_log.png" alt-text="Virhesanomat suunnittelutyökirjassa.":::

## <a name="planning-flexibility"></a>Suunnittelun joustavuus

Aiemmin luodun toimitustilauksen suunnittelu ei ole aina järkevää. Kyse voi olla esimerkiksi siitä, että tuotanto on käynnistynyt tai työtä varten on palkattu tiettynä päivänä lisähenkilöstöä. Kaikilla toimitustilauksen riveillä on **Suunnittelun joustavuus** -kenttä, jossa on kaksi vaihtoehtoa: **Rajaton** tai **Ei mitään**. Tämän kentän avulla osoitetaan, voiko suunnittelujärjestelmä muuttaa aiemmin luotua tilausta. Jos kentän määrityksenä on **Ei mitään**, suunnittelujärjestelmä ei yritä muuttaa toimitustilauksen riviä.  

Vaihtoehto voidaan valita kentässä manuaalisesti, joskin joissakin tapauksissa [!INCLUDE [prod_short](includes/prod_short.md)] määrittää sen automaattisesti. Mahdollisuus määrittää suunnittelun joustavuus manuaalisesti on tärkeää, koska sen ansiosta on helppo mukauttaa ominaisuuden käyttöä erilaisten työnkulkujen ja liiketoimintatapausten perusteella. Lisätietoja tämän kentän käytöstä on kohdassa [Rakennetiedot: siirrot suunnittelussa](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Tilauksen suunnittelu

**Tilausten suunnittelu** -sivulla esitelty perustyökalu tarjonnan suunnitteluun on suunniteltu manuaaliseen päätöstentekoon. Se ei ota huomioon mitään suunnitteluparametreja, minkä vuoksi sitä ei käsitellä tarkemmin tässä artikkelissa. Lisätietoja on kohdassa [Uuden kysynnän tilauskohtainen suunnittelu](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
> Tilauksen suunnittelua ei kannata käyttää, jos yrityksessä jo käytetään suunnitellussa suunnittelutyökirjaa tai hankintalistaa. **Tilauksen suunnittelu** -sivun kautta luotuja toimitustilauksia voidaan muuttaa tai poistaa automaattisten suunnitteluajojen aikana. Nämä muutokset tapahtuvat sen vuoksi, että automaattisissa suunnitteluajoissa käytetään suunnitteluparametreja, joita ei välttämättä oteta huomioon, kun suunnitelma tehdään manuaalisesti Tilauksen suunnittelu -sivulla.  

## <a name="finite-loading"></a>Äärellinen kuormitus

[!INCLUDE[prod_short](includes/prod_short.md)] tuottaa karkean aikataulun resurssien järkevän käytön suunnittelua varten. Se ei automaattisesti luo ja ylläpidä tarkkoja prioriteetteihin tai optimointisääntöihin perustuvia aikatauluja.  

Kapasiteettirajoitetut resurssit -omaisuuden käyttötarkoitukset:

* Resurssien ylikuorittamisen välttäminen
* Tuotantotilauksen valmistumisajan mahdollinen lyhentäminen varmistamalla, ettei kapasiteettia jää kohdistamatta.

Kun kapasiteettirajoitettuja resursseja käytetään suunnittelussa, [!INCLUDE [prod_short](includes/prod_short.md)] varmistaa, ettei kuormitus ylitä resurssien kapasiteettia (kriittinen kuormitus). Se määrittää kullekin toiminnolle lähimmän mahdollisen ajankohdan. Jos ajankohta ei riitä toiminnon suorittamiseen, toiminto jaetaan vähintään kahdeksi osaksi lähimpiin käytettävissä oleviin ajankohtiin.  

> [!NOTE]  
> Jos toiminto jaetaan, määritysaika kohdistetaan vain kerran, koska oletetaan, että aikataulun optimointiin käytetään joitakin manuaalisia muutoksia.  

Resursseihin voidaan lisätä puskuriaika minimoimaan toiminnon jakamista. Tämä ajan ansiosta [!INCLUDE [prod_short](includes/prod_short.md)] voi aikatauluttaa kuormituksen viimeiselle mahdolliselle päivälle siten, että kriittinen kuormitusprosentti ylittyy hieman.  

## <a name="see-also"></a>Katso myös

[Rakennetiedot: siirrot suunnittelussa](design-details-transfers-in-planning.md)  
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)  
[Rakennetiedot: suunnittelun kohdistustaulukko](design-details-planning-assignment-table.md)  
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)  
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
