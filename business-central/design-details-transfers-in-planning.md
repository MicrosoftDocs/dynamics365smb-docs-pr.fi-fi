---
title: Rakennetiedot – siirrot suunnittelussa
description: Tietoja siirtotilausten käyttämisestä toimituslähteenä varastomääriä suunniteltaessa.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.keywords: 'design, transfer, sku, locations, warehouse'
---
# <a name="design-details-transfers-in-planning"></a>Rakennetiedot: siirrot suunnittelussa

Siirtotilaukset ovat myös tarjonnan lähde, kun työskennellään varastointiyksikön tasolla. Kun käytössä on useita sijainteja (fyysisiä varastoja), varastointiyksikön täydennysjärjestelmän arvoksi voi määrittää Siirto. Tällöin sijainnin täydennys tehdään siirtämällä tavaroita toisesta sijainnista. Jos fyysisiä varastoja on useita, siirrot voivat ketjuttua. Toimitus VIHREÄÄN sijaintiin siirretään KELTAISESTA sijainnista, toimitus KELTAISEEN siirretään PUNAISESTA ja niin edelleen. Ketjun alussa täydennysjärjestelmänä on **Tuotantotilaus** tai **Osto**.  

![Esimerkki siirtovirrasta.](media/nav_app_supply_planning_7_transfers1.png "Esimerkki siirtovirrasta")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Seuraavia tilanteita verrattaessa on selvää, että jälkimmäisen suunnittelutehtävä on monimutkaisempi:

* Toimitustilaus vastaa suoraan kysyntätilausta.
* Myyntitilaus toimitetaan ketjutettuina varastointiyksikkösiirtoina.

Kysynnän muuttuminen voi heijastua koko ketjuun. Kaikki siirtotilaukset sekä osto- ja tuotantotilauksen ketjun vastakkaisissa päissä on päivitettävä, jotta kysyntä ja tarjonta saadaan jälleen tasapainoon.  

![Esimerkki toimitusten/kysynnän tasapainosta siirroissa.](media/nav_app_supply_planning_7_transfers2.png "Esimerkki toimitusten/kysynnän tasapainosta siirroissa")  

## <a name="why-is-a-transfer-a-special-case"></a>Siirron erikoisasema

Siirtotilaukset muistuttavat muita tilauksia, kuten osto- ja tuotantotilauksia. Käytännössä ne ovat kuitenkin erilaisia.  

Yhtenä erona on se, että siirtorivi ilmaisee sekä kysynnän että tarjonnan. Toimitettu lähtevä osa on kysyntää. Uudessa sijainnissa vastaanotettu saapuva osa on tarjontaa kyseisessä sijainnissa.  

![Siirtotilaussivun sisältö.](media/nav_app_supply_planning_7_transfers3.png "Siirtotilaussivun sisältö")  

Kun [!INCLUDE [prod_short](includes/prod_short.md)] muuttaa siirron tarjontapuolta, sen on tehtävä samanlainen muutos kysyntäpuoleen.  

## <a name="transfers-are-dependent-demand"></a>Siirrot ovat riippuvaisia kysynnästä

Kysynnän ja tarjonnan suhde muistuttaa tuotantotilausrivien komponentteja. Erona on kuitenkin se, että tuotantotilausrivien komponentit ovat seuraavalla suunnittelutasolla ja että niillä on eri nimike. Siirron kaksi osaa ovat samalla tasolla oleva sama nimike.  

Tärkeä samankaltaisuus on se, että komponentit ja siirrot ovat riippuvaisia kysynnästä. Siirtorivin kysyntä määräytyy siirron tarjontapuolen mukaan. Tarjonnan muuttuminen vaikuttaa suoraan kysyntään.

Jos suunnittelun joustavuuden arvoksi ei ole määritetty Ei mitään, siirtoriviä ei saa koskaan käsitellä suunnittelussa itsenäisenä kysyntänä.  

Suunnittelutoimenpiteessä siirron kysyntä on otettava huomioon vasta, kun suunnittelujärjestelmä on käsitellyt tarjontapuolen. Todellista kysyntää ei tiedetä ennen käsittelyä. Muutosten järjestys on tärkeää siirtotilauksissa  

## <a name="planning-sequence"></a>Suunnittelujärjestys

Seuraavassa kuvassa on esimerkki siirtoketjusta.  

![Esimerkki yksinkertaisesta siirtovirrasta.](media/nav_app_supply_planning_7_transfers4.png "Esimerkki yksinkertaisesta siirtovirrasta")  

Tässä esimerkissä asiakas tilaa nimikkeen VIHREÄSTÄ sijainnista. VIHREÄ sijainti toimitetaan siirron kautta PUNAISESTA keskusvarastosta. Siirto toimittaa päävaraston RED:in tuotannosta sijainnissa BLUE.  

Tässä esimerkissä suunnittelujärjestelmä aloittaa asiakkaan kysynnästä ja siirtyy taaksepäin ketjussa. Kysynnät ja tarjonnat käsitellään sijainti kerrallaan.  

![Toimitusten suunnittelu siirtojen avulla.](media/nav_app_supply_planning_7_transfers5.png "Toimitusten suunnittelu siirtojen avulla")  

## <a name="transfer-level-code"></a>Siirtotason koodi

Varastointiyksikön siirtotason koodi määrittää järjestyksen, jossa suunnittelujärjestelmä käsittelee sijainnit.  

Siirtotason koodi on sisäinen kenttä. Kenttä lasketaan ja tallennetaan varastointiyksikköön, kun varastointiyksikkö luodaan tai kun sitä muokataan. Laskenta suoritetaan kaikissa annetun nimike- ja nimikevarianttiyhdistelmän varastointiyksiköissä. Laskenta käyttää sijaintikoodia ja Kohteesta-koodia määrittämään varastointiyksiköille käytettävän reitin. Laskenta varmistaa, että kaikki kysyntä käsitellään.  

Siirtotason koodi on 0, kun kyseessä ovat oston tai tuotantotilauksen täydennysjärjestelmän varastointiyksiköt. Ensimmäisellä siirtotasolla koodi on -1, toisella -2 jne. Edellisessä osassa käsitellyssä esimerkissä tasot olisivat -1 (PUNAINEN) ja -2 (VIHREÄ), kuten seuraavassa kuvassa.  

![SKU-kortti-sivun sisältö.](media/nav_app_supply_planning_7_transfers6.gif "SKU-kortti -sivun sisältö")  

Varastointiyksikköä päivitettäessä suunnittelujärjestelmä havaitsee, onko varastointiyksiköiden täydennysjärjestelmissä kehäviittauksia.  

## <a name="planning-transfers-without-sku"></a>Siirtojen suunnittelu ilman varastointiyksiköitä

Yksinkertaisemmissa fyysisen varaston määrityksissä voidaan käyttää sijainteja ja tehdä sijaintien välillä manuaalisia siirtoa, vaikka varastointiyksiköt eivät olisi käytössä. Siirto voi koskea esimerkiksi sijainnissa olevaa myyntitilausta. Suunnittelujärjestelmän reagoi kysynnän muutoksiin.  

Suunnittelujärjestelmä analysoi manuaalisissa siirroissa siirtotilaukset ja suunnittelee sitten järjestyksen, jossa sijainnit käsitellään. Suunnittelujärjestelmä käyttää sisäisesti väliaikaisia varastointiyksiköitä, joilla on siirtotason koodit.  

![Siirtotason koodi.](media/nav_app_supply_planning_7_transfers7.png "Siirtotason koodi")  

Jos sijainnissa on useita siirtoja, ensimmäinen siirtotilaus määrittää suunnittelun suunnan. Siirrot vastakkaiseen suuntaan peruutetaan.  

## <a name="changing-quantity-with-reservations"></a>Varauksia sisältävän määrän muuttaminen

Suunnittelujärjestelmä ottaa varaukset huomioon, kun tarjonnan määriä muutetaan. Varattu määrä ilmaisee alimman määrän, jolle tarjonnan voi vähentää.  

Tämä alaraja on otettava huomioon, kun siirtotilausrivin määrää muutetaan. Alaraja on lähtevien ja saapuvien siirtorivien suurin varattu määrä.

Siirtotilauksen rivillä on esimerkiksi varattu 117 kappaletta seuraaville riveille:

* Myyntitilausrivillä 46
* Ostorivillä 24

Vaikka saapuvalla puolella voi olla ylimääräistä tarjontaa, siirtorivin määrän on oltava vähintään 46.  

![Varaukset siirron suunnittelussa.](media/nav_app_supply_planning_7_transfers8.png "Varaukset siirron suunnittelussa")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Määrän muuttaminen siirtoketjussa

Seuraava esimerkki osoittaa, mitä tapahtuu, kun siirron määrää muutetaan.

Alussa tilanne on tasapainossa, kun siirtoketju toimittaa myyntitilauksen, jonka määrä on 27, PUNAISESSA sijainnissa. SINISESSÄ sijainnissa on vastaava ostotilaus. Kumpikin siirto kulkee VAALEANPUNAISEN sijainnin kautta. Siirtotilauksia on kaksi: SININEN-VAALEANPUNAINEN ja VAALEANPUNAINEN-PUNAINEN  

![Määrän muuttaminen siirron suunnittelussa 1.](media/nav_app_supply_planning_7_transfers9.png "Määrän muuttaminen siirron suunnittelussa 1")  

Suunnittelija valitsee nyt VAALEANPUNAISESSA sijainnissa oston varaamisen.  

![Määrän muuttaminen siirron suunnittelussa 2.](media/nav_app_supply_planning_7_transfers10.png "Määrän muuttaminen siirron suunnittelussa 2")  

Varaus tarkoittaa yleensä sitä, että suunnittelujärjestelmä ohittaa ostotilauksen ja siirron kysynnän. Tämä ei ole ongelma, kunhan tasapaino säilyy. Mitä tapahtuu siinä tapauksessa, että PUNAINEN sijainti muuttaa tilauksen määrän 27 määräksi 22?  

![Määrän muuttaminen siirron suunnittelussa 3.](media/nav_app_supply_planning_7_transfers11.png "Määrän muuttaminen siirron suunnittelussa 3")  

Kun suunnittelujärjestelmä toimii jälleen, sen tulisi päästä eroon ylimääräisestä tarjonnasta. Varaus lukitsee oston ja siirron kuitenkin määrään 27.  

![Määrän muuttaminen siirron suunnittelussa 4.](media/nav_app_supply_planning_7_transfers12.png "Määrän muuttaminen siirron suunnittelussa 4")  

PINK-RED-siirto on vähennetty 22:een. Vaikka SININEN-VAALEANPUNAINEN-siirron saapuvaa osaa ei varattu, lähtevä osa on. Varauksen vuoksi määrää ei vähentää pienemmäksi kuin 27.  

## <a name="lead-time-calculation"></a>Toimitusajan laskenta

Siirtotilauksen eräpäivän laskennassa otetaan huomioon erilaisia toimitusaikoja.  

Seuraavat toimitusajat ovat aktiivisia siirtotilausta suunniteltaessa:  

* Lähtevä fyysisen varastoinnin käsittelyaika  
* Toimitusaika  
* Saapuva fyysisen varastoinnin käsittelyaika  

Suunnittelurivien seuraavilla kentillä on tietoja laskennasta.  

* Siirtotoimituksen pvm  
* Aloituspvm  
* Lopetuspvm  
* Eräpäivä  

Siirtorivin toimituspäivämäärä näkyy **Siirtotoimituksen pvm** -kentässä. Siirtorivin vastaanottopäivämäärä näkyy **Eräpäivä**-kentässä.  

Aloitus- ja lopetuspäivämääriä käytetään kuvaamaan todellista kuljetusjaksoa.  

Seuraavassa kuvassa ilmaistaan aloituspäivämäärä ja -aika sekä lopetuspäivämäärä ja -aika siirtotilausten suunnitteluriveillä.  

![Keskitetyt päivämäärät ja ajat siirron suunnitelmassa.](media/nav_app_supply_planning_7_transfers13.png "Keskitetyt päivämäärät ja ajat siirron suunnitelmassa")  

Seuraavat laskelmat näkyvät esimerkissä:  

* Toimituspvm + Lähtevä käsittely = Aloituspvm  
* Aloituspvm + Toimitusaika = Lopetuspvm  
* Lopetuspvm + Saapuva käsittely = Vast.ott. pvm  

## <a name="safety-lead-time"></a>Toimitusajan varmistus

**Oletus toimitusajan varmistus** -kenttä **Tuotannon asetukset** -sivulla ja **Toimitusajan varmistus** -kenttää **Nimikekortti**-sivulla ei sisällytetä siirtotilauksen laskelmiin. Toimitusajan varmistus vaikuttaa kuitenkin kokonaissuunnitelmaan. Toimitusajan varmistus vaikuttaa täydennystilaukseen (osto tai tuotanto) siirtoketjun alussa. Tässä vaiheessa nimikkeet asetetaan sijaintiin, josta ne siirretään.  

![Siirron eräpäivämäärän elementit.](media/nav_app_supply_planning_7_transfers14.png "Siirron eräpäivämäärän elementit")  

Tuotantoitilausrivillä Lopetuspvm + Toimitusajan varmistus + Saapuvan f.var. käsittelyaika = Eräpäivä.  

Ostotilausrivillä Suunniteltu vast.otto pvm + Toimitusajan varmistus + Saapuvan f.var. käsittelyaika = Oletettu vast.otto pvm.  

## <a name="reschedule"></a>Aikataul. uud.

Kun siirtorivi ajoitetaan uudelleen, suunnittelujärjestelmä etsii lähtevän osa ja muuttaa päivämäärän ja ajan.

> [!NOTE]
> Jos toimitusaika on määritetty, toimituksen ja vastaanoton välillä on aukko. Toimitusaika voi koostua useista elementeistä, kuten kuljetusajasta ja fyysisen varastoinnin käsittelyajasta. Suunnittelujärjestelmä siirtyy aikajanalla taaksepäin, kun se tasapainottaa elementtejä.  

![Eräpäivän muuttaminen siirron suunnittelussa.](media/nav_app_supply_planning_7_transfers15.png "Eräpäivän muuttaminen siirron suunnittelussa")  

Siirtorivin eräpäivän muutettaessa toimitusaika on laskettava, jotta siirron lähtevä osuus päivittyy.  

## <a name="serial-and-lot-numbers-in-transfer-chains"></a>Sarja- ja eränumerot siirtoketjuissa

Jos kysyntä käyttää sarja- tai eränumeroita ja suunnittelujärjestelmä suoritetaan, se luo siirtotilaukset. Katso lisätietoja tästä käsitteestä Nimikkeen määritteet -kohdasta. Jos sarja- tai eränumerot kuitenkin poistetaan kysynnästä, siirtotilaukset käyttävät edelleen sarja- ja eränumeroita ja suunnittelu ohittaa ne (niitä ei poisteta).  

## <a name="order-to-order-links"></a>Tilausten väliset linkit

Tässä esimerkissä SINISEEN varastointiyksikköön määritetään **tilauksen** uusintatilauskäytäntö. VAALEANPUNAISILLA JA PUNAISILLA varastointiyksilöillä on **Erä-erästä**-uudelleentilauskäytäntö. Kun PUNAISESSA sijainnissa luodaan myyntitilaus määrälle 27, seurauksena on siirtoketju. Viimeinen siirto on SINISESSÄ sijainnissa, ja se on varattu sidonnan avulla. Tässä esimerkissä varaukset eivät ole kiinteitä suunnittelijan VAALEANPUNAISESSA sijainnissa luomia varauksia. Suunnittelujärjestelmä luo sidonnat. Oleellinen ero on se, että suunnittelujärjestelmä voi vaihtaa jälkimmäisen.  

![Tilaus-tilaus-linkit siirron suunnittelussa.](media/nav_app_supply_planning_7_transfers16.png "Tilaus-tilaus-linkit siirron suunnittelussa")  

Jos kysyntä muutetaan arvosta 27 arvoon 22, suunnittelujärjestelmä vähentää määrä koko ketjussa. Myös sitova varaus vähenee.  

## <a name="see-also"></a>Katso myös

[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
[Rakennetiedot: suunnittelun kohdistustaulukko](design-details-planning-assignment-table.md)   
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
[Rakennetiedot: suunnitelman luominen sijaintien avulla tai ilman sijainteja](production-planning-with-without-locations.md)   
[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
