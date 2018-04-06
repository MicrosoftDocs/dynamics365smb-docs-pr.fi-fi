---
title: "Rakennetiedot – varastoprofiilien lataaminen | Microsoft Docs"
description: "Voit lajitella useita kysynnän ja tarjonnan lähteitä, kun suunnittelujärjestelmä järjestää ne kahdella aikajanalle, joita kutsutaan varastoprofiileiksi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5b47a898b7e1d574abaf521e917f780fd105c4a8
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-loading-the-inventory-profiles"></a>Rakennetiedot: varastoprofiilien lataaminen
Voit lajitella useita kysynnän ja tarjonnan lähteitä, kun suunnittelujärjestelmä järjestää ne kahdella aikajanalle, joita kutsutaan varastoprofiileiksi.  

 Normaalit kysyntä- ja tarjontatyypit eräpäivineen suunnittelun alkamispäivänä tai sen jälkeen ladataan jokaiseen varastoprofiiliin. Kun tämä on ladattu, erityyppinen kysyntä ja tarjonta lajitellaan yleisten prioriteettien, kuten eräpäivän, alatason koodien, sijainnin ja variantin, perusteella. Lisäksi tilauksen prioriteetit kohdistetaan erilaisiin tyyppeihin, jotta varmistutaan tärkeimmän kysynnän täyttämisestä ensin. Lisätietoja on ohjeaiheessa [Rakennetiedot: tilausten priorisointi](design-details-prioritizing-orders.md).  

 Kuten aiemmin mainittiin, kysyntä voi olla myös negatiivista. Tämä tarkoittaa sitä, että sitä tulee käsitellä tarjontana. Tavallisista tarjontatyypeistä poiketen negatiivista kysyntää käsitellään kuitenkin kiinteänä tarjontana. Suunnittelujärjestelmä voi ottaa sen huomioon mutta ei ehdota mitään muutoksia siihen.  

 Yleisesti suunnittelujärjestelmä katsoo, että kaikki suunnittelupäivämäärän jälkeiset toimitustilaukset saattavat muuttua kysynnän täyttämiseksi. Kuitenkin heti, kun määrä on kirjattu toimitustilauksesta, suunnittelujärjestelmä ei voi enää muuttaa sitä. Näin ollen seuraavia eri tilauksia ei voi suunnitella uudelleen:  

-   Julkaistut tuotantotilaukset, joihin kulutus tai tuotanto on tiliöity.  

-   Kokoonpanotilaukset, joissa kulutus tai tuotos on kirjattu.  

-   Siirrä tilaukset, joiden toimitus on kirjattu.  

-   Ostotilaukset, joissa vastaanotto on jo kirjattu.  

 Kysyntä ja tarjontatyyppien lataamisesta riippumatta, tietyt tyypit ladataan kiinnittäen huomiota erityisiin sääntöihin ja riippuvuuksiin, jotka on kuvattu seuraavassa.  

## <a name="item-dimensions-are-separated"></a>Nimikkeen dimensiot on erotettu  
 Tarjontasuunnitelma on laskettava nimikkeen dimensioiden, kuten variantin ja sijainnin, yhdistelmää kohti. Minkään teoreettisen yhdistelmän laskeminen ei ole kuitenkaan tarpeellista. Vain ne yhdistelmät tarvitsee laskea, joihin liittyy kysyntä ja/tai tarjonta.  

 Suunnittelujärjestelmä hallinnoi tätä ajamalla läpi varaston profiilin. Kun uusi yhdistelmä löytyy, ohjelma luo todellisen yhdistelmän tiedot sisältävän sisäisen ohjaustietueen. Ohjelma liittää SKU:n kontrollitietueena ja ulkoisena lenkkinä. Tämän vuoksi asetetaan asianmukaiset parametrit variantin ja sijainnin mukaan ja ohjelma voi jatkaa sisempään silmukkaan.  

> [!NOTE]  
>  Ohjelma ei vaadi käyttäjää kirjamaan SKU-tietuetta, kun tämä syöttää kysynnän ja/tai tarjonnan tietylle variantin ja sijainnin yhdistelmälle. Jos annetulla yhdistelmällä ei ole varastointiyksikköä, ohjelma luo oman väliaikaisen varastointiyksikön tietueen nimikekortin tietojen perusteella. Jos Sijainti pakollinen -asetuksen arvo on Kyllä Varastonhallinnan asetukset -ikkunassa, tällöin on luotava varastointiyksikkö tai Komponentit sijainnissa -asetuksen arvoksi on muutettava Kyllä. Katso lisätiedot kohdasta [Rakennetiedot: kysyntä tyhjä-sijainnissa](design-details-demand-at-blank-location.md).  

## <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Erittelytaso lataa sarja-/eränumerot  
 Määritteet sarja-/eränumeroiden lomakkeella ladataan varastoprofiileihin yhdessä niihin kohdistetun kysynnän ja tarjonnan kanssa.  

 Kysynnän ja tarjonnan määritteet järjestetään tilauksen prioriteetin sekä niiden määrityksen tason perusteella. Koska sarja-/ eränumeroiden vastaavuudet kuvaavat määritystasoa, tarkempi pyyntö, kuten myyntirivillä erityisesti valittu eränumero etsii vastineen ennen tarkempaa pyyntöä, kuten esimerkiksi myynti mistä tahansa valitusta eränumerosta.  

> [!NOTE]  
>  Sarja-/eränumeroidulla kysynnälle ja tarjonnalle ei ole muita määritettyjä priorisointisääntöjä kuin erä- ja sarjanumeroiden ja liittyvien nimikkeiden nimikeseurannan asetusten yhdistelmien määrittämää määrityksen tasoa.  

 Täsmäytyksen aikana suunnittelujärjestelmä ottaa huomioon tarjonnan, jolla on joustamattomia sarja-/ eränumeroita, eikä yritä kasvattaa tai aikatauluttaa näitä toimitustilauksia uudelleen (paitsi jos niitä käytetään tilausten välillä). Katso Tilauksesta tilaukseen (linkit eivät ole koskaan rikki). Tämän avulla vältytään tarjonnan saamista useista ja mahdollisesti ristiriitaisista toimenpideviesteistä, jotka voisivat aiheutua tarjonnan erilaisista määritteistä, kuten erilaisten sarjanumeroiden kokoelmasta.  

 Toinen syy sarja- ja eränumeroiden tarjonnan joustamattomuuteen on se, että eränumerot kohdistetaan prosessissa yleisesti niin myöhään, että muutosten ehdottaminen aiheuttaisi sekaannusta.  

 Sarja-/eränumeroiden tasapainotus ei ota huomioon aluetta [Jäädytetty alue](design-details-dealing-with-orders-before-the-planning-starting-date.md). Jos kysyntää ja tarjontaa ei synkronoida, suunnittelujärjestelmä ehdottaa muutoksia tai ehdotti uusia tilauksia, suunnittelun aloituspäivämäärästä riippumatta.  

## <a name="order-to-order-links-are-never-broken"></a>Tilausten välisiä linkkejä ei katkaista koskaan  
 Kun suunnitellaan tilausten välistä nimikettä, linkitettyä tarjontaa ei saa käyttää muussa kuin alkuperäisessä kysynnässä. Liitettyä kysyntää ei koskaan pidä kattaa toisella satunnaistarjonnalla, ei edes silloin, kuin sen tämänhetkisen tilanteen mukaan se on käytettävissä ajallisesti ja määrällisesti. Esimerkiksi kokoonpano tilausta varten -skenaariossa myyntitilaukseen linkitettyä kokoonpanotilausta ei voida käyttää muun kysynnän kattamiseen.  

 Tilausten välinen kysyntä ja tarjonta tulee täsmäyttää tarkasti. Suunnittelujärjestelmä varmistaa tarjonnan kaikissa olosuhteissa kiinnittämättä huomiota tilauksen mitoitusparametreihin, muokkaajiin ja varaston määriin (muut kuin määrät liittyen liittyviin tilauksiin). Samasta syystä järjestelmä ehdottaa ylimääräisen tarjonnan vähentämistä, jos linkitetty kysyntä on vähenee.  

 Tämä täsmäytys vaikuttaa myös ajoitukseen. Rajoitettua näköpiiriä, jonka ajanjakso on antanut, ei huomioida; tarjonta aikataulutetaan uudelleen, jos kysynnän ajoitus on muuttunut. Vaimentimen aika otetaan kuitenkin huomioon ja se estää tilausten välisten toimitusten ulos aikatauluttamisen, lukuun ottamatta monitasoisen tuotantotilauksen (projektitilaus) sisäisiä toimituksia.  

> [!NOTE]  
>  Sarja-/eränumerot voidaan myös määrittää Tilauksesta tilaukseen -kysynnässä. Tässä tapauksessa tarjonnan ei katsota olevan oletusarvoisesti joustamatonta, kuten yleensä sarja-/ eränumeroiden kanssa. Tässä tapauksessa järjestelmä kasvattaa/vähentää kysynnän muutosten mukaan. Lisäksi, jos yksi kysyntä sisältää vaihtelevia sarja- tai eränumeroita, kuten esimerkiksi useita eränumeroita, järjestelmä suosittelee yhtä toimitustilausta jokaiselle erälle.  

> [!NOTE]  
>  Ennusteiden ei tulisi johtaa sellaisten toimitustilausten luontiin, jotka on sidottu tilausten välisellä linkillä. Jos ennuste on käytössä, sitä tulisi käyttää vain riippuvaisen tarpeen luomiseen valmistusympäristössä.  

## <a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponenttitarve ladataan tuotantotilausten muutosten mukaan  
 Suunnittelujärjestelmän on valvottava tarvittavia komponentteja tuotantotilausten käsittelyn yhteydessä ennen komponenttien lataamista kysynnän profiiliin. Muutetusta tuotantotilauksesta aiheutuvat komponenttirivit korvaavat alkuperäisen tilauksen vastaavat. Tämä varmistaa, että suunnittelujärjestelmän muodostamista komponenttitarpeen suunnitteluriveistä ei koskaan tehdä kaksoiskappaleita.  

##  <a name="BKMK_SafetyStockMayBeConsumed"></a> Varmuusvarastoa voidaan käyttää  
 Varmuusvaraston määrä on ensisijaisesti kysyntätyyppi ja siksi ladattu varastoprofiiliin suunnittelun aloituspäivänä.  

 Varmuusvarasto on varaston määrä, joka on asetettu sivuun ja jonka avulla tasapainotetaan kysynnän epävarmuutta täytön läpimenoaikana. Se voidaan kuitenkin kuluttaa, jos se on otettava kysynnän täyttämiseksi. Tällöin suunnittelujärjestelmä varmistaa, että varmuusvarasto korvataan nopeasti, ehdottamalla toimitustilausta varmuusvarastomäärän täydentämistä varten päivämääränä, jolloin se kulutetaan. Tällä suunnittelurivillä näkyy poikkeusvaroituksen kuvake. Se kertoo suunnittelijalle, että puuttuvan määrän poikkeustilaus on kuluttanut varmuusvaraston osittain tai kokonaan.  

## <a name="forecast-demand-is-reduced-by-sales-orders"></a>Myyntitilaukset vähentävät ennustettua kysyntää  
 Tuotantoennuste ilmaisee tulevan ennakkokysynnän. Kun todellinen tarve syötetään, yleensä myyntitilausten tuotettujen nimikkeiden kuluttaa ennuste.  

 Myyntitilaukset eivät pienennä itse ennustetta; se pysyy samana. Suunnittelun laskennassa käytettyjä ennustemääriä kuitenkin vähennetään (myyntitilausten määrillä) ennen kuin jäljellä oleva määrä, jos sitä on, siirtyy kysynnän varastoprofiiliin. Kun suunnittelujärjestelmä tutkii kauden todellista myyntiä, sekä avoimet myyntitilaukset että toimitetun myynnin nimiketapahtumat, ellei niitä ole johdettu puitetilauksesta.  

 Käyttäjän on määritettävä kelvollinen ennusteajanjakso. Ennustetun määrän päivämäärä määrittää ajanjakson alun ja seuraavan ennusteen päivämäärä määrittää ajanjakson lopun.  

 Ennustetta ajanjaksoille ennen suunnittelujaksoa ei käytetä huolimatta siitä, oliko se käytössä vai ei. Ensimmäinen hyödyn ennusteluku on joko päivämäärä tai lähin päivämäärä ennen suunnittelun alkamispäivää.  

 Ennuste voi olla riippumattomalle kysynnälle, kuten myyntitilaukset, tai riippuvalle kysynnälle, kuten tuotantotilausosat (moduuliennuste). Nimikkeellä voi olla molemmat ennusteen tyypit. Suunnittelun aikana kulutus tapahtuu erikseen, ensin riippumattomalle kysynnälle ja sitten riippuvaiselle kysynnälle.  

## <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Myyntitilaukset vähentävät puitetilauksen kysyntää  
 Puitemyyntitilaus täydentää ennustetta määrittämällä tulevan kysynnän tietyltä asiakkaalta. Kuten (määrittelemättömän) ennusteen tapauksessa, toteutuneiden myyntien tulisi kuluttaa oletettu kysyntä ja jäljelle jäävän määrän tulisi siirtyä varastoprofiiliin. Vielä uudelleen, kulutus ei vähennä todellisuudessa puitetilausta.  

 Suunnittelulaskelma käsittää avoimet myyntitilaukset liitettyinä erityiseen kestotilausriviin, mutta se ei käsitä mitään voimassaolevaa ajanjaksoa. Eikä se ota huomioon kirjattuja tilauksia, koska kirjausmenettely on jo vähentänyt puitetilauksen avointa määrää.  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
 [Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
 [Rakennetiedot: tarjonnan suunnittelu](design-details-supply-planning.md)   
 [Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)

