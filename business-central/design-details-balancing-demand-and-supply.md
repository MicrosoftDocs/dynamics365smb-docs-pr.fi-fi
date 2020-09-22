---
title: Rakennetiedot – kysynnän ja tarjonnan täsmäyttäminen | Microsoft Docs
description: Suunnittelujärjestelmän priorisoitujen tavoitteiden ymmärtäminen edellyttää suunnittelujärjestelmän toiminnan ymmärtämistä. Tärkeimmät tavoitteet pyrkivät varmistamaan, että kaikki kysyntä täytetään riittävällä tarjonnalla ja että kaikki tarjonta palvelee tarkoitusta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b039c15a3e55135576dfe6341248bde936d58093
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788144"
---
# <a name="design-details-balancing-demand-and-supply"></a>Rakennetiedot: kysynnän ja tarjonnan täsmäytys
Suunnittelujärjestelmän priorisoitujen tavoitteiden ymmärtäminen edellyttää suunnittelujärjestelmän toiminnan ymmärtämistä. Tärkeimmät tavoitteet pyrkivät varmistamaan seuraavat seikat:  

- Kaikki kysyntä täytetään riittävällä tarjonnalla.  
- Kaikki tarjonta palvelee tarkoitusta.  

 Yleisesti ottaen nämä tavoitteet saavutetaan täsmäyttämällä tarjonta ja kysyntä.  

## <a name="demand-and-supply"></a>Kysyntä ja tarjonta
 Kysyntä on yleinen termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta. Lisäksi sovellus sallii tekniset kysyntätyypit, kuten negatiivisen varaston ja ostopalautukset.  

  Tarjonta on yleinen termi, jota käytetään mille tahansa positiiviselle tai tulevalle määrälle, kuten varasto, ostot, kokoonpano, tuotanto tai tulevat siirrot. Lisäksi myyntipalautus voi myös kuvata tarjontaa.  

  Voit lajitella useita kysynnän ja tarjonnan lähteitä, kun suunnittelujärjestelmä järjestää ne kahdelle aikajanalle, joita kutsutaan varastoprofiileiksi. Yksi profiili sisältää kysyntätapahtumat ja toinen sisältää vastaavat tarjontatapahtumat. Kukin tapahtuma edustaa yhtä tilausverkon kokonaisuutta, kuten myyntitilausriviä, nimiketapahtumaa tai tuotantotilausriviä.  

  Kun varaston profiilit ladataan, erilaiset kysyntä- ja tarjontajoukot täsmäytetään listatut tavoitteet täyttävän tarjontasuunnitelman tuotoksen saamiseksi.  

  Suunnitteluparametrit ja varastotasot ovat muita kysynnän ja tarjonnan tyyppejä, jotka käyvät läpi integroidun täsmäytyksen varastonimikkeiden täydentämiseksi. Lisätietoja on kohdassa [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Täsmäytyksen käsite lyhyesti
  Yrityksen asiakkaat antavat kysynnän. Yritys voi luoda ja poistaa tarjontaa luodakseen tasapainon. Suunnittelujärjestelmä aloittaa riippumattomasta kysynnästä ja jäljittää sitten taaksepäin tarjontaan.  

   Varastoprofiileja käytetään sisältämään tietoa kysynnästä ja tarjonnasta, määristä ja ajoituksista. Nämä profiilit muodostavat käytännössä täsmäytysasteikon kaksi eri puolta.  

   Suunnittelumekanismin päämäärä on tasapainottaa nimikkeen kysyntää ja tarjontaa, jolloin varmistetaan se, että tarjonta vastaa kysyntää toteuttamiskelpoisella tavalla, kuten määritetty suunnitteluparametreissa ja säännöissä.  

   ![Yleiskatsaus kysynnän ja tarjonnan tasapainottamiseen](media/nav_app_supply_planning_2_balancing.png "Yleiskatsaus kysynnän ja tarjonnan tasapainottamiseen")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Tilausten käsittely ennen suunnittelun aloituspäivää
Voit estää mahdottomien ja sen vuoksi hyödyttömien ehdotusten näkymisen toimitussuunnitelmassa niin, että suunnittelujärjestelmä pitää suunnittelun alkupäivämäärää aiemman jakson jäädytetyksi alueeksi, joka ei sisällä suunnitelmia. Seuraava sääntö pätee jäädytettyyn alueeseen:  

Kaikki kysyntä ja tarjonta ennen suunnittelujakson aloituspäivämäärää katsotaan osaksi varastoa tai toimitetuksi.  

Näin ollen suunnittelujärjestelmä ei muutamia poikkeuksia lukuun ottamatta ehdota mitään muutoksia toimitustilauksiksi jäädytetyllä alueella ja tilauksen seurantalinkkejä ei luoda tai ylläpidetä tämän ajanjakson osalta.  

Poikkeukset tähän sääntöön ovat seuraavat:  

   * Jos oletettu saatavilla oleva varasto, mukaan lukien kysynnän ja tarjonnan summa jäädytetyllä alueella, on nollan alapuolella.  
   * Jos takautuvissa tilauksissa vaaditaan sarja-/eränumerot.  
   * Jos tarjonta-kysyntä-yhdistelmä on linkitetty tilausten välisellä käytännöllä.  

Jos ensimmäinen käytettävissä oleva varasto on alle nollan, suunnittelujärjestelmä ehdottaa puuttuvan määrän kattamiseksi hätätoimitustilausta suunnittelujaksoa edeltävänä päivänä. Näin ollen suunnitellun ja käytettävissä olevan varaston on oltava aina vähintään nolla, kun tulevan kauden suunnittelu alkaa. Tämän toimitustilauksen suunnittelurivillä näytetään Hätävaroituskuvake ja lisätietoa annetaan sitä haettaessa.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Sarja-/eränumerot ja Tilauksesta tilaukseen -linkit on vapautettu jäädytetyltä alueelta  
   Jos sarja-/eränumerot vaaditaan tai tilausten välinen linkki on olemassa, suunnittelujärjestelmä jättää huomioimatta jäädytetyn vyöhykkeen ja sisällyttää nämä takautuvat määrät aloituspäivämäärästä alkaen ja ehdottaa mahdollisesti korjaavia toimenpiteitä, jos kysyntää ja tarjontaa ei synkronoida. Liiketoimintasyy tälle periaatteelle on se, että tällaisten erityisten kysyntä-tarjonta-asetusten täytyy vastata toisiaan, jotta varmistetaan että tämä erityiskysyntä täyttyy.

## <a name="loading-the-inventory-profiles"></a>Varastoprofiilien lataaminen
Voit lajitella useita kysynnän ja tarjonnan lähteitä, kun suunnittelujärjestelmä järjestää ne kahdella aikajanalle, joita kutsutaan varastoprofiileiksi.  

Normaalit kysyntä- ja tarjontatyypit eräpäivineen suunnittelun alkamispäivänä tai sen jälkeen ladataan jokaiseen varastoprofiiliin. Kun tämä on ladattu, erityyppinen kysyntä ja tarjonta lajitellaan yleisten prioriteettien, kuten eräpäivän, alatason koodien, sijainnin ja variantin, perusteella. Lisäksi tilauksen prioriteetit kohdistetaan erilaisiin tyyppeihin, jotta varmistutaan tärkeimmän kysynnän täyttämisestä ensin. Lisätietoja on kohdassa [Projektitilausten priorisointi](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

Kuten aiemmin mainittiin, kysyntä voi olla myös negatiivista. Tämä tarkoittaa sitä, että sitä tulee käsitellä tarjontana. Tavallisista tarjontatyypeistä poiketen negatiivista kysyntää käsitellään kuitenkin kiinteänä tarjontana. Suunnittelujärjestelmä voi ottaa sen huomioon mutta ei ehdota mitään muutoksia siihen.  

Yleisesti suunnittelujärjestelmä katsoo, että kaikki suunnittelupäivämäärän jälkeiset toimitustilaukset saattavat muuttua kysynnän täyttämiseksi. Kuitenkin heti, kun määrä on kirjattu toimitustilauksesta, suunnittelujärjestelmä ei voi enää muuttaa sitä. Näin ollen seuraavia eri tilauksia ei voi suunnitella uudelleen:  

- Julkaistut tuotantotilaukset, joihin kulutus tai tuotanto on tiliöity.  
- Kokoonpanotilaukset, joissa kulutus tai tuotos on kirjattu.  
- Siirrä tilaukset, joiden toimitus on kirjattu.  
- Ostotilaukset, joissa vastaanotto on jo kirjattu.  

Kysyntä ja tarjontatyyppien lataamisesta riippumatta, tietyt tyypit ladataan kiinnittäen huomiota erityisiin sääntöihin ja riippuvuuksiin, jotka on kuvattu seuraavassa.  

### <a name="item-dimensions-are-separated"></a>Nimikkeen dimensiot on erotettu  
Tarjontasuunnitelma on laskettava nimikkeen dimensioiden, kuten variantin ja sijainnin, yhdistelmää kohti. Minkään teoreettisen yhdistelmän laskeminen ei ole kuitenkaan tarpeellista. Vain ne yhdistelmät tarvitsee laskea, joihin liittyy kysyntä ja/tai tarjonta.  

Suunnittelujärjestelmä hallinnoi tätä ajamalla läpi varaston profiilin. Kun uusi yhdistelmä löytyy, sovellus luo todellisen yhdistelmän tiedot sisältävän sisäisen ohjaustietueen. Sovellus liittää SKU:n ohjaustietueena ja ulkoisena lenkkinä. Tämän vuoksi määritetään asianmukaiset parametrit variantin ja sijainnin mukaan ja sovellus voi jatkaa sisäsilmukkaan.  

> [!NOTE]  
>  Sovellus ei vaadi käyttäjää kirjamaan SKU-tietuetta, kun käyttäjä antaa kysynnän ja/tai tarjonnan tietylle variantin ja sijainnin yhdistelmälle. Jos annetulla yhdistelmällä ei ole varastointiyksikköä, sovellus luo oman väliaikaisen varastointiyksikön tietueen nimikekortin tietojen perusteella. Jos Sijainti pakollinen -asetuksen arvo on Kyllä Varastonhallinnan asetukset -sivulla, tällöin on luotava varastointiyksikkö tai Komponentit sijainnissa -asetuksen arvoksi on muutettava Kyllä. Katso lisätiedot kohdasta [Rakennetiedot: kysyntä tyhjä-sijainnissa](design-details-demand-at-blank-location.md).  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Erittelytaso lataa sarja-/eränumerot  
Määritteet sarja-/eränumeroiden lomakkeella ladataan varastoprofiileihin yhdessä niihin kohdistetun kysynnän ja tarjonnan kanssa.  

Kysynnän ja tarjonnan määritteet järjestetään tilauksen prioriteetin sekä niiden määrityksen tason perusteella. Koska sarja-/ eränumeroiden vastaavuudet kuvaavat määritystasoa, tarkempi pyyntö, kuten myyntirivillä erityisesti valittu eränumero etsii vastineen ennen tarkempaa pyyntöä, kuten esimerkiksi myynti mistä tahansa valitusta eränumerosta.  

> [!NOTE]  
>  Sarja-/eränumeroidulla kysynnälle ja tarjonnalle ei ole muita määritettyjä priorisointisääntöjä kuin erä- ja sarjanumeroiden ja liittyvien nimikkeiden nimikeseurannan asetusten yhdistelmien määrittämää määrityksen tasoa.  

Täsmäytyksen aikana suunnittelujärjestelmä ottaa huomioon tarjonnan, jolla on joustamattomia sarja-/ eränumeroita, eikä yritä kasvattaa tai aikatauluttaa näitä toimitustilauksia uudelleen (paitsi jos niitä käytetään tilausten välillä). Katso Tilauksesta tilaukseen (linkit eivät ole koskaan rikki). Tämän avulla vältytään tarjonnan saamista useista ja mahdollisesti ristiriitaisista toimenpideviesteistä, jotka voisivat aiheutua tarjonnan erilaisista määritteistä, kuten erilaisten sarjanumeroiden kokoelmasta.  

Toinen syy sarja- ja eränumeroiden tarjonnan joustamattomuuteen on se, että eränumerot kohdistetaan prosessissa yleisesti niin myöhään, että muutosten ehdottaminen aiheuttaisi sekaannusta.  

Sarja-/eränumeroiden tasapainotus ei ota huomioon *jäädytettyä aluetta*. Jos kysyntää ja tarjontaa ei synkronoida, suunnittelujärjestelmä ehdottaa muutoksia tai ehdotti uusia tilauksia, suunnittelun aloituspäivämäärästä riippumatta.  

### <a name="order-to-order-links-are-never-broken"></a>Tilausten välisiä linkkejä ei katkaista koskaan  
Kun suunnitellaan tilausten välistä nimikettä, linkitettyä tarjontaa ei saa käyttää muussa kuin alkuperäisessä kysynnässä. Liitettyä kysyntää ei koskaan pidä kattaa toisella satunnaistarjonnalla, ei edes silloin, kuin sen tämänhetkisen tilanteen mukaan se on käytettävissä ajallisesti ja määrällisesti. Esimerkiksi kokoonpano tilausta varten -skenaariossa myyntitilaukseen linkitettyä kokoonpanotilausta ei voida käyttää muun kysynnän kattamiseen.  

Tilausten välinen kysyntä ja tarjonta tulee täsmäyttää tarkasti. Suunnittelujärjestelmä varmistaa tarjonnan kaikissa olosuhteissa kiinnittämättä huomiota tilauksen mitoitusparametreihin, muokkaajiin ja varaston määriin (muut kuin määrät liittyen liittyviin tilauksiin). Samasta syystä järjestelmä ehdottaa ylimääräisen tarjonnan vähentämistä, jos linkitetty kysyntä on vähenee.  

Tämä täsmäytys vaikuttaa myös ajoitukseen. Rajoitettua näköpiiriä, jonka ajanjakso on antanut, ei huomioida; tarjonta aikataulutetaan uudelleen, jos kysynnän ajoitus on muuttunut. Vaimentimen aika otetaan kuitenkin huomioon ja se estää tilausten välisten toimitusten ulos aikatauluttamisen, lukuun ottamatta monitasoisen tuotantotilauksen (projektitilaus) sisäisiä toimituksia.  

> [!NOTE]  
>  Sarja-/eränumerot voidaan myös määrittää Tilauksesta tilaukseen -kysynnässä. Tässä tapauksessa tarjonnan ei katsota olevan oletusarvoisesti joustamatonta, kuten yleensä sarja-/ eränumeroiden kanssa. Tässä tapauksessa järjestelmä kasvattaa/vähentää kysynnän muutosten mukaan. Lisäksi, jos yksi kysyntä sisältää vaihtelevia sarja- tai eränumeroita, kuten esimerkiksi useita eränumeroita, järjestelmä suosittelee yhtä toimitustilausta jokaiselle erälle.  

> [!NOTE]  
>  Ennusteiden ei tulisi johtaa sellaisten toimitustilausten luontiin, jotka on sidottu tilausten välisellä linkillä. Jos ennuste on käytössä, sitä tulisi käyttää vain riippuvaisen tarpeen luomiseen valmistusympäristössä.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponenttitarve ladataan tuotantotilausten muutosten mukaan  
Suunnittelujärjestelmän on valvottava tarvittavia komponentteja tuotantotilausten käsittelyn yhteydessä ennen komponenttien lataamista kysynnän profiiliin. Muutetusta tuotantotilauksesta aiheutuvat komponenttirivit korvaavat alkuperäisen tilauksen vastaavat. Tämä varmistaa, että suunnittelujärjestelmän muodostamista komponenttitarpeen suunnitteluriveistä ei koskaan tehdä kaksoiskappaleita.  

###  <a name="safety-stock-may-be-consumed"></a><a name="BKMK_SafetyStockMayBeConsumed"></a> Varmuusvarastoa voidaan käyttää  
Varmuusvaraston määrä on ensisijaisesti kysyntätyyppi ja siksi ladattu varastoprofiiliin suunnittelun aloituspäivänä.  

Varmuusvarasto on varaston määrä, joka on asetettu sivuun ja jonka avulla tasapainotetaan kysynnän epävarmuutta täytön läpimenoaikana. Se voidaan kuitenkin kuluttaa, jos se on otettava kysynnän täyttämiseksi. Tällöin suunnittelujärjestelmä varmistaa, että varmuusvarasto korvataan nopeasti, ehdottamalla toimitustilausta varmuusvarastomäärän täydentämistä varten päivämääränä, jolloin se kulutetaan. Tällä suunnittelurivillä näkyy poikkeusvaroituksen kuvake. Se kertoo suunnittelijalle, että puuttuvan määrän poikkeustilaus on kuluttanut varmuusvaraston osittain tai kokonaan.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Myyntitilaukset vähentävät ennustettua kysyntää  
Kysyntäennuste ilmaisee tulevan ennakkokysynnän. Kun todellinen tarve syötetään, yleensä myyntitilausten tuotettujen nimikkeiden kuluttaa ennuste.  

Myyntitilaukset eivät pienennä itse ennustetta; se pysyy samana. Suunnittelun laskennassa käytettyjä ennustemääriä kuitenkin vähennetään (myyntitilausten määrillä) ennen kuin jäljellä oleva määrä, jos sitä on, siirtyy kysynnän varastoprofiiliin. Kun suunnittelujärjestelmä tutkii kauden todellista myyntiä, sekä avoimet myyntitilaukset että toimitetun myynnin nimiketapahtumat, ellei niitä ole johdettu puitetilauksesta.  

Käyttäjän on määritettävä kelvollinen ennusteajanjakso. Ennustetun määrän päivämäärä määrittää ajanjakson alun ja seuraavan ennusteen päivämäärä määrittää ajanjakson lopun.  

Ennustetta ajanjaksoille ennen suunnittelujaksoa ei käytetä huolimatta siitä, oliko se käytössä vai ei. Ensimmäinen hyödyn ennusteluku on joko päivämäärä tai lähin päivämäärä ennen suunnittelun alkamispäivää.  

Ennuste voi olla riippumattomalle kysynnälle, kuten myyntitilaukset, tai riippuvalle kysynnälle, kuten tuotantotilausosat (moduuliennuste). Nimikkeellä voi olla molemmat ennusteen tyypit. Suunnittelun aikana kulutus tapahtuu erikseen, ensin riippumattomalle kysynnälle ja sitten riippuvaiselle kysynnälle.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Myyntitilaukset vähentävät puitetilauksen kysyntää  
Puitemyyntitilaus täydentää ennustetta määrittämällä tulevan kysynnän tietyltä asiakkaalta. Kuten (määrittelemättömän) ennusteen tapauksessa, toteutuneiden myyntien tulisi kuluttaa oletettu kysyntä ja jäljelle jäävän määrän tulisi siirtyä varastoprofiiliin. Vielä uudelleen, kulutus ei vähennä todellisuudessa puitetilausta.  

Suunnittelulaskelma käsittää avoimet myyntitilaukset liitettyinä erityiseen kestotilausriviin, mutta se ei käsitä mitään voimassaolevaa ajanjaksoa. Eikä se ota huomioon kirjattuja tilauksia, koska kirjausmenettely on jo vähentänyt puitetilauksen avointa määrää.

## <a name="prioritizing-orders"></a>Tilausten priorisointi
Pyydetty tai käytettävissä oleva päivämäärä edustaa annetun varastointiyksikön korkeinta prioriteettia. Tämän päivän kysyntä tulee käsitellä ennen seuraavan viikon kysyntää. Mutta tämän kokonaisprioriteetin lisäksi suunnittelujärjestelmä suosittelee myös kysynnän tyyppiä, joka olisi täytettävä ennen toisen kysynnän täyttämistä. Vastaavasti se ehdottaa mitä tarjontalähdettä olisi sovellettava ennen muiden tarjontalähteiden käyttämistä. Tämä tehdään tilauksen prioriteettien mukaan.  

Ladattu kysyntä ja tarjonta lisätään arvioidun varaston profiiliin seuraavilla prioriteeteilla:  

### <a name="priorities-on-the-demand-side"></a>Kysyntäpuolen prioriteetit  
1. Jo toimitettu: nimiketapahtuma  
2. Ostopalautustilaus  
3. Myyntitilaus  
4. Huoltotilaus  
5. Tuotannon komponenttitarve  
6. Kokoonpanotilauksen rivi  
7. Lähtevä siirtotilaus  
8. Puitetilaus (jota liittyvä myyntitilaukset eivät ole vielä käyttäneet)  
9. Ennuste (jota muut myyntitilaukset eivät ole vielä kuluttaneet)  

> [!NOTE]  
>  Ostopalautuksia ei tavallisesti sisällytetä tarjonnan suunnittelun, ne tulisi aina varata erästä,joka aiotaan palauttaa. Jos se ei ole varattuna, ostopalautukset vaikuttavat saatavuuteen ja ne priorisoidaan erittäin korkealle, jotta vältetään mahdollisuus, että suunnittelujärjestelmä ehdottaa toimitustilausta vain ostopalautuksen käsittelemiseksi.  

### <a name="priorities-on-the-supply-side"></a>Tarjontapuolen prioriteetit  
1. Jo varastossa: nimiketapahtuma (suunnittelun joustavuus = ei mitään)  
2. Myynnin palautustilaus (suunnittelun joustavuus = ei mitään)  
3. Tuleva siirtotilaus  
4. Tuotantotilaus  
5. Kokoonpanotilaus  
6. Ostotilaus  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Kysynnän ja tarjonnan tilaan liittyvä prioriteetti  
Riippumatta kysynnän ja tarjonnan määrittämistä prioriteeteista, nykyinen tila suoritusprosessissa määrittää myös prioriteetin. Esimerkiksi varastoinnin aktiviteeteilla on vaikutus ja myyntien tila, osto-, siirto-, kokoonpano- ja tuotantotilaukset otetaan huomioon:  

1. Osittain käsitelty (suunnittelun joustavuus = ei mitään)  
2. Jo käsittelyssä varastossa (suunnittelun joustavuus = ei mitään)  
3. Julkaistu - kaikki tilaustyypit (suunnittelun joustavuus = rajoittamaton)  
4. Sitovasti suunniteltu tuotantotilaus (suunnittelun joustavuus = rajoittamaton)  
5. Suunniteltu/avoin – kaikki tilaustyypit (suunnittelun joustavuus = rajoittamaton)

## <a name="balancing-supply-with-demand"></a>Tarjonnan ja kysynnän tasapainottaminen
Suunnittelujärjestelmän ydin vaatii kysynnän ja tarjonnan tasapainotusta ehdottamalla käyttäjän toimenpiteitä tarkastamaan varastotilaukset epätasapainon välttämiseksi. Tämä tapahtuu variantin ja sijainnin yhdistelmän perusteella.  

Kuvittele, että jokainen varastoprofiili sisältää kysyntätapahtumien joukon (lajiteltuna päivämäärän ja prioriteetin mukaan) ja vastaavan tarjontatapahtumien joukon. Jokainen tapahtuma viittaa takaisin sen lähdetyyppiin ja tunnukseen. Nimikkeen tasapainotussäännöt ovat suoraviivaiset. Prosessin missä tahansa vaiheessa voi ilmetä neljä kohdistetun kysynnän ja tarjonnan esiintymää:  

1. Nimikkeellä ei ole kysyntää tai tarjontaa = > suunnittelu on päättynyt (tai sen ei pitäisi käynnistyä).  
2. Kysyntä on olemassa mutta ei ole tarjontaa => tarjontaa tulee ehdottaa.  
3. Tarjonta on olemassa mutta sille ei ole kysyntää => tarjonta tulee peruuttaa.  
4. Sekä kysyntä että tuotanto on olemassa = > kysymyksiin tulee vastata ennen kuin järjestelmä voi varmistaa, että kysyntä täyttyy ja tuotanto on riittävä.  

    Jos toimituksen ajankohta ei ole sopiva, ehkä toimitus voidaan aikatauluttaa uudelleen seuraavasti:  

    1.  Jos tarjonta on asetettu kysyntää aiemmin, tarjonta voidaan ehkä aikatauluttaa uudelleen niin, että varasto on mahdollisimman pieni.  
    2.  Jos tarjonta tapahtuu kysyntää ennen, tarjonnan voi mahdollisesti aikatauluttaa uudelleen. Muussa tapauksessa järjestelmä ehdottaa uutta tarjontaa.  
    3.  Jos tarjonta vastaa kysyntää kyseisenä päivämääränä, suunnittelujärjestelmä voi tutkia edelleen, voiko tarjonnan määrä kattaa kysynnän.  

    Kun ajoitus on valmis, riittävä toimitettava määrä voidaan laskea seuraavasti:  

    1.  Jos tarjonnan määrä on pienempi kuin kysyntä, on mahdollista, että tarjonnan määrää voidaan kasvattaa (tai ei, jos vähimmäismääräkäytäntö rajoittaa sitä).  
    2.  Jos tarjonnan määrä on suurempi kuin kysyntä, on mahdollista, että tarjonnan määrää voidaan vähentää (tai ei, jos vähimmäismääräkäytäntö rajoittaa sitä).  

    Tässä vaiheessa on olemassa yksi näistä kahdesta tilanteesta:  

    1.  Nykyiseen kysyntään voidaan vastata, jolloin se voidaan sulkea ja seuraavan kysynnän suunnittelu voidaan aloittaa.  
    2.  Tarjonta on saavuttanut enimmäismäärän, ja osa kysyntämäärästä on jäänyt kattamatta. Tässä tapauksessa suunnittelujärjestelmä voi sulkea nykyisen tarjonnan ja siirtyä seuraavaan.  

 Toimenpide alkaa tyypillisesti seuraavasta kysynnästä ja nykyisestä tarjonnasta tai päinvastoin. Nykyinen tarjonta voi pystyä kattamaan myös tämän seuraavan kysynnän tai nykyiseen kysyntään ei ole vielä täysin vastattu.  

### <a name="rules-concerning-actions-for-supply-events"></a>Säännöt, jotka koskevat toimitustapahtumien toimintoja  
Kun suunnittelujärjestelmä suorittaa ylhäältä alaspäin tehtävän laskennan, jossa tarjonnan on täytettävä kysyntä, kysyntä saadaan muualta valmiina, eikä suunnittelujärjestelmä valvo sitä. Tarjontapuolta voidaan kuitenkin hallita. Tämän vuoksi suunnittelujärjestelmä ehdottaa uuden toimitustilauksen luomista, olemassa olevien uudelleenajoittamista ja/tai tilausmäärän muuttamista. Jos olemassa oleva toimitustilaus muuttuu tarpeettomaksi, suunnittelujärjestelmä ehdottaa, että käyttäjä peruuttaa sen.  

Jos käyttäjä haluaa jättää pois olemassa olevan toimitustilauksen suunnitteluehdotuksista, hän voi ilmoittaa, että sillä ei ole suunnittelun joustavuutta (suunnittelun joustavuus = ei mitään). Tilauksen ylimääräinen tarjonta käytetään kysynnän kattamisessa, mutta toimintoa ei ehdoteta.  

Yleisesti koko tarjonnalla on suunnittelun joustavuus, jota rajoittaa jokaisen ehdotetun toiminnon ehdot.  

-   **Aikatauluta uudelleen ulos**: olemassa olevan toimitustilauksen päivämäärä voidaan aikatauluttaa ulos, jotta se vastaa kysynnän eräpäivää, ellei:  

    -   Se kuvaa varastoa (aina päivänä nolla).  
    -   Sillä on tilausten välinen linkki toiseen kysyntään.  
    -   Se on aikavälin määrittämän uudelleenaikataulutussivun ulkopuolella.  
    -   Voit käyttää myös paremmin sopivaa tarjontaa.  
    -   Toisaalta käyttäjä voi päättää, että aikataulutusta ei suoriteta uudelleen, koska:  
    -   Toimitustilaus on jo sidottu edellisen päivän toiseen kysyntään.  
    -   Tarvittu uudelleenaikataulutus on niin minimaalinen, että käyttäjä katsoo sen merkityksettömäksi.  

-   **Aikatauluta uudelleen sisään**: olemassa olevan toimitustilauksen päivämäärä voidaan aikatauluttaa sisään lukuun ottamatta seuraavia olosuhteita:  

    -   Se on linkitetty suoraan johonkin toiseen kysyntään.  
    -   Se on aikavälin määrittämän uudelleenaikataulutussivun ulkopuolella.  

> [!NOTE]  
>  Kun suunnitellaan uusintatilauspistettä käyttävää nimikettä, toimitustilaus voidaan ajoittaa tarvittaessa, Tämä on normaalia eteenpäin ajastetuille toimitustilauksille, jotka uusintatilauspiste käynnistää.  

-   **Kasvatusmäärä**: olemassa olevan toimitustilauksen määrää voidaan kasvattaa vastaamaan kysyntää, ellei toimitustilausta linkitetä suoraan kysyntään tilausten välisellä linkillä.  

> [!NOTE]  
>  Vaikka toimitustilausta on mahdollista kasvattaa, se voi olla rajoitettu määritetyn enimmäistilausmäärän vuoksi.  

-   **Vähennysmäärä**: aiemmin luodun toimitustilauksen määrä, joka on ylijäämäinen verrattuna olemassa olevaan kysyntään, on vähennettävissä kysynnän täyttämiseksi.  

> [!NOTE]  
>  Vaikka määrää on mahdollista vähentää, kysyntäarvoon verrattuna saattaa vielä olla ylijäämää määritetystä vähimmäistilausmäärästä tai tilauskerrannaisesta johtuen.  

-   **Peruuta**: erityinen vähennä määrää -toiminnon tapahtuma, toimitustilaus voidaan peruuttaa, jos se on vähentynyt nollaan.  
-   **Uusi**: jos toimitustilausta ei ole jo olemassa tai olemassa olevaa ei voida muuttaa täyttämään tarvittavaa määrää vaadittuna eräpäivänä, järjestelmä ehdottaa uutta toimitustilausta.  

### <a name="determining-the-supply-quantity"></a>Tarjonnan määrän määrittäminen  
Käyttäjän määrittämät suunnitteluparametrit ohjaavat jokaisen toimitustilauksen ehdotettua määrää.  

Kun suunnittelujärjestelmä laskee uuden toimitustilauksen määrän tai olemassa olevan tilauksen määrä muuttuu, ehdotettu määrä voi olla eri kuin alkuperäisen kysynnän määrä.  

Jos enimmäisvarasto tai kiinteä tilausmäärä on valittuna, järjestelmä saattaa kasvattaa ehdotettua määrää tämän kiinteän määrän tai enimmäisvaraston täyttämiseksi. Jos uusintatilaustapa käyttää uusintatilauspistettä, määrää voidaan kasvattaa vähintään uusintatilauspisteen täyttämiseksi.  

 Ehdotettua määrää voidaan muokata tässä sarjassa:  

1. Alaspäin enimmäistilausmäärään (jos sellainen on).  
2. Ylöspäin seuraavaan tilausmäärään.  
3. Ylöspäin seuraavaan tilauskerrannaisen. (Jos asetukset ovat virheelliset, tämä voi vahingoittaa enimmäistilausmäärä.)  

### <a name="order-tracking-links-during-planning"></a>Tilauksen seurantalinkit suunnittelun aikana  
Suunnittelun aikaiseen tilauksen seurantaan liittyen on tärkeää mainita, että suunnittelujärjestelmä järjestää uudelleen dynaamisesti luodut tilauksen seurantalinkit nimike/variantti/sijainti-yhdistelmille.  

Tälle on kaksi syytä:  

-   Suunnittelujärjestelmän täytyy pystyä osoittamaan ehdotuksensa oikeiksi; että kaikki kysyntä katetaan ja että toimitustilukset ovat tarpeettomia.  
-   Dynaamisesti luodut tilauksen seurantalinkit on täsmäytettävä uudelleen säännöllisesti.  

Ajan myötä dynaamisen tilauksen seurannan linkit ovat epätasapainossa, koska koko tilauksen seurantaverkko järjestetään uudelleen, kunnes kysyntä tai tarjonta suljetaan.  

Ennen tarjonnan ja kysynnän täsmäytystä sovellus poistaa kaikki olemassa olevat tilauksen seurantalinkit. Kun kysyntä- tai tarjontatapahtuma on suljettu, täsmäytyksen aikana muodostetaan uudet tilauksen seurantalinkit kysynnän ja tarjonnan välille.  

> [!NOTE]  
>  Vaikka nimikettä ei ole asetettu dynaamiseen tilauksen seurantaan, suunnittelujärjestelmä luo täsmäytetyt tilauksen seurantalinkit yllä kuvatulla tavalla.
## <a name="closing-demand-and-supply"></a>Kysynnän ja tarjonnan sulkeminen
Kun tarjonnan tasapainotusmenetelmät on suoritettu, tulos voi olla jokin seuraavista kolmesta vaihtoehdosta:  

* Vaadittu kysyntätapahtumien määrä ja päivämäärä on kohdattu ja niiden suunnittelu voidaan sulkea,. Tarjontatapahtuma on yhä avoinna ja se voi kattaa seuraavan kysynnän, joten täsmäytys voi alkaa nykyisestä tarjontatapahtumasta ja seuraavasta kysynnästä.  
* Toimitustilausta ei voi muokata niin, että se kattaa koko kysynnän. Kysyntätapahtuma on edelleen avoinna. Siinä on jokin katteeton määrä, joka voidaan kattaa seuraavalla tuotantotapahtumalla. Nykyinen tarjontatapahtuma siis suljetaan ja täsmäytystoiminto alkaa alusta nykyisestä kysynnästä ja seuraavasta tarjontatapahtumasta.  
* Kaikki kysyntä on otettu huomioon; kysyntää ei ole myöhemmin (tai kysyntää ei ole lainkaan). Jos olemassa on ylimääräistä tarjontaa, se voidaan vähentää (tai peruuttaa) ja sitten sulkea. On mahdollista, että myöhempänä ketjussa on lisää tarjontatapahtumia ja myös ne tulisi peruuttaa.  

Viimeiseksi suunnittelujärjestelmä luo tilauksen seurantalinkin tarjonnan ja kysynnän välille.  

### <a name="creating-the-planning-line-suggested-action"></a>Suunnittelurivin luonti (ehdotettu toimenpide)  
Jos toimitustilauksen korjaamista ehdotetaan jollakin toiminnolla, kuten uusi, muuta määrä, aikatauluta uudelleen, aikatauluta uudelleen ja muuta määrää tai peruuta, suunnittelujärjestelmä luo suunnittelurivin suunnittelutyökirjassa. Tilauksen seurannasta johtuen suunnitteluriviä ei luoda vain tarjontatapahtuman lopuksi mutta myös siinä tapauksessa, jos kysyntätapahtuma suljetaan, vaikka tarjontatapahtuma on yhä avoinna ja siihen saattaa kohdistua muita muutoksia seuraavan kysyntätapahtuman käsittelyn yhteydessä. Tämä tarkoittaa sitä, että jos suunnittelurivi on luotu ensimmäisenä, sitä voidaan muuttaa uudelleen.  

Tuotantotilausten käsittelyn aikaista tietokantayhteyden käyttöä voi minimoida ylläpitämällä suunnittelurivejä kolmella tasolla ja pyrkimällä käyttämään vähiten kuormittava ylläpitotasoa.  

* Luo vain suunnittelurivi nykyisellä eräpäivällä ja määrällä, mutta ilman reititystä ja komponentteja.  
* Sisällytä reititys: suunniteltu reititys asetellaan aloitus- ja lopetuspäivämäärät ja kellonajat mukaan lukien. Tämä on vaativaa tietokannan käyttöoikeuksia ajatellen. Kun haluat määrittää loppupäivämäärän ja eräpäivän, tämä on ehkä laskettava, vaikka tarjontatapahtumaa ei ole suljettu (jos kyseessä on aikataulutus eteenpäin).  
* Sisällytä tuoterakenteen purku: tämä voi odottaa hetkeä ennen tarjontatapahtuman sulkemista.  

Tämä päättää suunnittelujärjestelmän suorittaman kysynnän ja tarjonnan lataamisen, priorisoinnin ja täsmäytyksen kuvaukset. Järjestelmän on varmistettava yhdessä tämän tarjonnan suunnittelutehtävän kanssa, että jokaisen suunnitellun nimikkeen vaadittava varastotaso säilytetään sen uusintatilauskäytännön mukaisesti.

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
 [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
 [Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)
