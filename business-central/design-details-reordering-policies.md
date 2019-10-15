---
title: Rakennetiedot – uusintatilauskäytännöt | Microsoft Docs
description: Tässä ohjeaiheessa on yleiskuvaus nimikkeiden täydennyskäytännöistä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: a48e2998195bccb4ac877e8339612f6cfabb0f3b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303046"
---
# <a name="design-details-reordering-policies"></a>Rakennetiedot: uusintatilauskäytännöt
Uusintatilausohjeet määrittävät sen, kuinka paljon tilataan, kun nimikkeitä tarvitaan lisää. Käytössä on neljä erilaista uusintatilaustapaa.  

## <a name="fixed-reorder-qty"></a>Kiinteä uusintatil. määrä
Kiinteä uusintatilausmäärän menettely liittyy tyypillisten C-nimikkeiden varaston suunnitteluun (alhaiset varastokustannukset, vanhenemisriski ja/tai useita nimikkeitä) Tätä menetelmää käytetään yleensä silloin, kun tilauspiste vaikuttaa odotettuun kysyntään nimikkeen toimitusajan aikana.  

### <a name="calculated-per-time-bucket"></a>Laskettu aikavälikohtaisesti  
 Jos suunnittelujärjestelmä havaitsee, että lisätilauspiste on saavutettu tai se ylitetään määritetyllä aikajaksolla (lisätilausjaksolla) (arvo ylittää lisätilauspisteen tai on sen tasolla jakson alussa tai arvo on lisätilauspisteen alapuolella tai sen tasolla jakson lopussa), järjestelmä ehdottaa uuden toimitustilauksen luomista määritetyllä lisätilausmäärällä. Järjestelmä ehdottaa myös aikataulun siirtämistä eteenpäin aikajakson loppumista seuraavasta päivästä.  

 Jaksotettu jälkitilauspisteen konsepti vähentää tarjontaehdotusten määrää. Tämä vaikuttaa säännöllisesti suoritettavaan manuaaliseen prosessiin eli varaston läpi kävelyyn ja eri varastopaikkojen todellisen sisällön tarkistamiseen.  

### <a name="creates-only-necessary-supply"></a>Luo vain tarvittavan kysynnän  
 Ennen uuden toimitustilauksen ehdottamista uusintatilauspisteen täyttämiseksi suunnittelujärjestelmä tarkistaa, onko toimitus jo tilattu vastaanotettavaksi nimikkeen toimitusaikana. Jos olemassa oleva toimitustilaus ratkaisee ongelman muuttamalla suunnitellun varaston uusintatilauspisteeseen tai sen yläpuolelle toimitusaikana, järjestelmä ei ehdota uutta toimitustilausta.  

 Toimitustilaukset, jotka on luoto erityisesti kohtaamaan jälkitilaustarve, poistetaan tavanomaisesta tarjonnan tasapainotuksesta, eikä niitä voida mitenkään muuttaa jälkeenpäin. Näin ollen, jos uusintatilauspiste poistetaan (ei uusita), tällöin on suositeltavaa tarkistaa avoimet toimitustilaukset manuaalisesti tai muuttaa uusintatilaustapa arvoon erä-erästä, jolloin järjestelmä vähentää tai peruuttaa tarpeettoman tarjonnan.  

### <a name="combines-with-order-modifiers"></a>Yhdistää tilausmääritteiden kanssa  
 Tilauksen muokkaajien, minimitilausmäärä, maksimitilausmäärä ja tilauksen moninkertaistaminen, ei tulisi näytellä isoa roolia, kun käytetään kiinteää jälkitilausmäärätapaa. Koska suunnittelujärjestelmä ottaa edelleen nämä muuttujat huomioon ja vähentää määrän määritettyyn enimmäistilausmäärään (ja luo kaksi toimitusta tai useampia kokonaistilausmäärän saavuttamiseksi), kasvata tilausta määritettyyn vähimmäistoimituksen määrään tai pyöristä tilausmäärä ylös määritetyn tilauskerrannaisen kattamiseksi.  

### <a name="combines-with-calendars"></a>Yhdistäminen kalentereihin  
 Ennen kuin uusintatilauspisteen täyttämiseen ehdotetaan uutta toimitustilausta, suunnittelujärjestelmä tarkistaa, onko tilaus ajoitettu **Yritystiedot**- ja **Sijaintikortti**-sivujen **Peruskalenterin koodi** -kentässä määritettyjen kalenterien mukaiselle ei-työskentelypäivälle.  

 Jos suunniteltu päivämäärä ei ole työpäivä, suunnittelujärjestelmä siirtää tilauksen seuraavalle työpäivälle. Tämä voi johtaa tilaukseen, joka täyttää uusintatilauspisteen, mutta ei täytä mitään tiettyä kysyntää. Suunnittelujärjestelmä luo ylimääräisen tarjonnan vastaamaan epätasapainoiseen kysyntään.  

### <a name="should-not-be-used-with-forecast"></a>Ei tule käyttää ennusteen kanssa  
 Koska oletettu kysyntä on jo ilmaistu uusintatilauspisteen tasolla, ennusteen liittäminen nimikkeen suunnitteluun uusintatilauspisteen avulla ei ole tarpeellista. Jos suunnitelman perustaminen ennusteeseen on asianmukaista, käytä erä-erästä-käytäntöä.  

### <a name="must-not-be-used-with-reservations"></a>Ei tule käyttää varausten kanssa  
 Jos käyttäjä on varannut määrän, esimerkiksi varastossa olevan määrän jollekin tulevaisuudessa tapahtuvalle kysynnälle, suunnitelman perusta häiriintyy. Vaikka oletettu saatavilla oleva varasto on hyväksyttävä suhteessa uusintatilauspisteeseen, määrät eivät ehkä ole käytettävissä varauksen vuoksi. Järjestelmä voi yrittää korjata tilannetta luomalla poikkeustilauksia. On kuitenkin suositeltavaa määrittää niiden nimikkeiden Varaa-kentän arvoksi Ei koskaan, jotka on suunniteltu käyttämällä uusintatilauspistettä.

## <a name="maximum-qty"></a>Enimmäismäärä
Enimmäismääräkäytäntö on tapa ylläpitää varastoa uudelleentilauspisteen avulla.  

Kaikki kiinteää uusintatilausmäärän käytäntöä koskeva koskee myös tätä käytäntöä. Ainoa ero on ehdotetun tarjonnan määrä. Kun käytetään enimmäismääräkäytäntöä, uusintatilausmäärä määritetään dynaamisesti oletetun varaston tason perusteella. Sen vuoksi se yleensä on eri kuin tilausten välinen määrä.  

### <a name="calculated-per-time-bucket"></a>Laskettu aikavälikohtaisesti  
Jälkitilausmäärä määritetään siihen ajankohtaan (ajanjakson loppu), kun suunnittelujärjestelmä havaitsee, että jälkitilauspiste on ylitetty. Tällä hetkellä järjestelmä mittaa välin nykyisestä arvioidusta varastotasosta määritettyyn enimmäisvarastoon asti. Tämä kuvaa määrää, joka tulisi järjestää uudelleen. Järjestelmä tarkistaa, onko tarjonta jo tilattu muualle vastaanotettavaksi nimikkeen toimitusaikana. Jos näin on, järjestelmä pienentää uuden toimitustilauksen määrää jo tilattujen määrien verran.  

Järjestelmä varmistaa, että oletettu varasto saavuttaa vähintään uusintatilauspisteen tason. Tämä tehdään siltä varalta, että käyttäjä unohtaa määrittää varaston enimmäismäärän.  

### <a name="combines-with-order-modifiers"></a>Yhdistää tilausmääritteiden kanssa  
Asetuksesta riippuen saattaa olla parasta yhdistää enimmäismäärän käytäntö tilauksen muuttujien kanssa, jotta varmistetaan tilauksen vähimmäismäärä tai sen pyöristäminen oston mittayksikön kokonaislukuun, tai jotta se jaetaan useampiin eriin tilauksen enimmäismäärän määrityksen mukaan.  

### <a name="combines-with-calendars"></a>Yhdistäminen kalentereihin  
Ennen kuin uusintatilauspisteen täyttämiseen ehdotetaan uutta toimitustilausta, suunnittelujärjestelmä tarkistaa, onko tilaus ajoitettu **Yritystiedot**- ja **Sijaintikortti**-sivujen **Peruskalenterin koodi** -kentässä määritettyjen kalenterien mukaiselle ei-työskentelypäivälle.  

Jos suunniteltu päivämäärä ei ole työpäivä, suunnittelujärjestelmä siirtää tilauksen seuraavalle työpäivälle. Tämä voi johtaa tilaukseen, joka täyttää uusintatilauspisteen, mutta ei täytä mitään tiettyä kysyntää. Suunnittelujärjestelmä luo ylimääräisen tarjonnan vastaamaan epätasapainoiseen kysyntään.

## <a name="order"></a>Järjestys
Tilausohjautuvassa ympäristössä nimike ostetaan tai tuotetaan yksinomaan kattamaan tiettyä kysyntää. Yleensä tämä liittyy A-nimikkeisiin. Tämä uusintatilaustapa valitaan esimerkiksi silloin, kun kysyntä ei ole säännöllistä, toimitusajalla ei ole merkitystä tai pakolliset määritteet vaihtelevat.  

Sovellus luo tilaus tilauksesta -linkin, joka toimii alustavana yhteytenä tarjonnan, toimitustilauksen tai varaston ja sen kysynnän välillä, jonka tarjonta täyttää.  

Riippumatta tilauskäytännön käyttämisestä, tilausten välistä linkkiä voidaan käyttää suunnittelun aikana seuraavilla tavoilla:  

* Kun usean tason tai projektityyppisiä tuotantotilauksia luodaan tilausohjatun tuotantotavan avulla (tarvittavat komponentit sisältyvät samaan tuotantotilaukseen).  
* Kun myyntitilauksen suunnittelutoimintoa käytetään tuotantotilauksen luomiseksi myyntitilauksesta.  

Vaikka valmistava yritys on mielestään tilausohjattu ympäristö, on ehkä parasta käyttää erä-erästä uusintatilaustapaa, jos nimikkeet ovat täysin vakiomuotoisia ilman määritteiden variaatioita. Tämän vuoksi järjestelmä käyttää suunnittelematonta varastoa ja vain kasvattaa myyntitilauksia samalla toimituspäivämäärällä tai määritetyllä aikavälillä.  

### <a name="order-to-order-links-and-past-due-dates"></a>Tilausten väliset linkit ja erääntyneet määräpäivät  
Toisin kuin useimmat tarjonta- ja kysyntäjoukot, järjestelmä suunnittelee kokonaan linkitetyt tilaukset, joiden eräpäivä on ennen suunnittelun alkupäivämäärää. Liiketoimintasyy tälle poikkeukselle on se, että erityiset kysyntä-tarjonta-asetukset täytyy synkronoida tämän toimeenpanon välityksellä. Lisätietoja useimmissa kysyntä–tarjonta-tyypeissä käytettävissä jäädytetystä alueesta on kohdassa [Rakennetiedot: Tilausten käsittely ennen suunnittelun aloituspäivää](design-details-dealing-with-orders-before-the-planning-starting-date.md).

## <a name="lot-for-lot"></a>Erä-erästä
Erä erästä -toiminto on kaikkein joustavin, koska järjestelmä reagoi vain ajankohtaiseen kysyntään, ja se toimii ennakkokysyntänä ennusteesta ja kestotilauksista, ja ratkaisee sitten tilausmäärän perustuen kysyntään. Erä erästä -toiminto on kohdistettu A- ja B-nimikkeille, joissa varasto voidaan hyväksyä, mutta tätä tulee välttää.  

Monilla tavoilla erä-erästä käytäntö näyttää tilauskäytännöltä, mutta sillä on yleinen lähestymistapa nimikkeisiin – se voi hyväksyä varastossa olevat määrät ja se kokoaa kysynnän ja vastaavan tarjonnan käyttäjän määrittämiin aikaväleihin.  

Aikaväli määritetään **Aikaväli**-kentässä. Järjestelmän käyttämä pienin aikaväli on yksi päivä. Se on kysyntä- ja tarjontatapahtumien ajan pienin mittayksikkö järjestelmässä. Käytännössä tosin tuotantotilausten ja komponenttitarpeiden ajan mittayksikkö voidaan määrittää sekunteina.  

Aikaväli määrittää myös rajat sille, milloin olemassa oleva toimitustilaus on ajoitettava uudelleen annettua kysyntää vastaavaksi. Jos tarjonta sijoittuu aikavälille, se aikataulutetaan uudelleen sisään tai ulos kysynnän täyttämiseksi. Muussa tapauksessa, jos se on aiemmin, se aiheuttaa tarpeetonta varaston kerääntymistä ja se tulisi peruuttaa. Jos se on myöhemmin, uusi toimitustilaus luodaan sen sijaan.  

Tämän käytännön avulla voi myös määrittää varmuusvaraston mahdollisten tarjonnan vaihteluiden kompensointia tai äkillisen kysynnän täyttämistä varten.  

Koska toimitustilauksen määrä perustuu todelliseen kysyntään, voi olla järkevää käyttää tilauksen muuttujakenttiä: pyöristä tilausmäärä ylös tietyn tilauskerrannaisen määrittämiseksi (tai mitan ostoyksikön), kasvata tilausta tiettyyn tilauksen vähimmäismäärään tai vähennä määrää määritettyyn enimmäismäärään (ja luo näin kaksi tai useampia toimituksia vaadittavan kokonaismäärän saavuttamiseksi).

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)
