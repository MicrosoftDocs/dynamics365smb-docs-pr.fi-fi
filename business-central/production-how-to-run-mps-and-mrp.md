---
title: Kokonaisvaltaisen suunnittelun, tuotanto-ohjelman tai tarvelaskennan suorittaminen
description: Suunnittelujärjestelmä voi laskea tuotanto-ohjelman tai tarvelaskennan pyydettäessä, tai se voi laskea molemmat samanaikaisesti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000852, 99000860
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 35263f54400865c88694a483bda195957a8f8db4
ms.sourcegitcommit: 55f42d2407e109b4924218cb22129467b53deb08
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557247"
---
# <a name="run-full-planning-mps-or-mrp"></a>Kokonaisvaltaisen suunnittelun, tuotanto-ohjelman tai tarvelaskennan suorittaminen

Suunnittelutyökirjan suorittaminen ja tarvelaskennan suorittaminen tarkoitetaan tuotanto-ohjelman ja materiaalitarpeen laskemista todellisen ja ennustetun tarpeen perusteella. Suunnittelujärjestelmä voi laskea tuotanto-ohjelman tai tarvelaskennan pyydettäessä, tai se voi laskea molemmat samanaikaisesti.  

-   Tuotanto-ohjelma tarkoittaa todelliseen tarpeeseen ja kysyntäennusteeseen perustuvaa tuotanto-ohjelman laskentaa. Tuotanto-ohjelman laskenta tehdään lopullisille nimikkeille, joilla on ennuste ja/tai myyntitilauksen rivi. Näitä nimikkeitä kutsutaan tuotanto-ohjelmanimikkeiksi, ja ne tunnistetaan dynaamisesti laskennan alkaessa.  
-   MRP tarkoittaa komponenttien todelliseen tarpeeseen ja komponenttitason kysyntäennusteeseen perustuvaa materiaalitarpeen laskentaa. Tarvelaskenta tehdään vain nimikkeille, jotka eivät ole tuotanto-ohjelmanimikkeitä. Tuotanto-ohjelman yleistavoitteena on tuottaa aikavaiheistetut, viralliset nimikekohtaiset suunnitelmat, jotta oikeaa tuotetta voidaan toimittaa oikea nimike ja oikea määrä oikeaan aikaan ja oikeassa paikassa.  

Tuotanto-ohjelmassa ja tarvelaskennassa käytetään identtisiä suunnittelualgoritmeja. Suunnittelualgoritmit liittyvät nettouttamiseen, aiempien täydennystilausten uudelleenkäyttöön ja toimenpideviesteihin. Suunnittelujärjestelmä selvittää, mitä nyt tai vastaisuudessa tarvitaan (kysyntä) sekä mitä on käsivarastossa ja mitä tulossa (tarjonta). Kun nämä määrät nettoutetaan, [!INCLUDE[prod_short](includes/prod_short.md)] näyttää toimenpideviestejä. Toimenpideviestit ovat ehdotuksia, jotka kehottavat luomaan uuden tilauksen, muuttamaan tilausta (määrää tai päivämäärää) tai peruuttamaan jo tilauksessa olevan tilauksen. Tilauksella tarkoitetaan ostotilauksia, kokoonpanotilauksia, tuotantotilauksia ja siirtotilauksia.

Suunnittelumoduulin kysynnän ja tarjonnan välille luodut linkit ja niihin liittyvää toimitusta voidaan seurata **Tilauksen seuranta** -sivu. Lisätietoja on kohdassa [Kysynnän ja tarjonnan välisten suhteiden seuranta](production-how-track-demand-supply.md).   

Suunnitelmasta saadaan asianmukaisia tuloksia sen mukaan, kuinka nimikkeen kortit, tuotannon tuoterakenteet ja reititykset on määritetty.  

## <a name="methods-for-generating-a-plan"></a>Suunnitelman luomismenetelmät  

-   **Laske uudelleensuunnittelu:** Tämä toiminto käsittelee tai uudistaa materiaalisuunnitelman. Prosessin aluksi kaikki ladatut suunnitellut toimitustilaukset poistetaan. Tietokannan kaikki nimikkeet suunnitellaan uudelleen.  
-   **Laske nettomuutossuunnitelma**: Tämä toiminto käsittelee nettomuutossuunnitelman. Kun nimikkeitä käsitellään nettomuutossuunnitelmassa kahden tyyppisistä muutoksista:  
    - **Kysynnän/tarjonnan muutokset:** Tällaisia muutoksia ovat myyntitilausten, kysyntäennusteiden, tuotantotilausten, kokoonpanotilausten ja ostotilausten määrien muutokset. Myös suunnittelematon varastotason muutos katsotaan määrän muutokseksi.  
    - **Suunnitteluparametrien muutokset**: Tällaisia muutoksia ovat varmuusvaraston, uusintatilauspisteen, reitityksen ja tuoterakenteen muutokset sekä aikavälin ja toimitusajan laskennan muutokset.  
-   **Hae toimenpideviestit**: Tänä toiminto toimii lyhyen aikavälin suunnittelutyökaluna. Se tuottaa toimenpideviestejä, jotka ilmoittavat käyttäjälle edellisen uudelleensuunnittelun tai nettomuutossuunnittelun laskemisen jälkeen tehdyistä muutoksista.  

Jokaisen suunnitellun menetelmän kanssa, [!INCLUDE[prod_short](includes/prod_short.md)] luo työkirjatapahtumat olettaen, että kapasiteetti on ääretön. Tuotantosolun ja kuormitusryhmän kapasiteettia ei huomioida laadittaessa aikatauluja.  

> [!IMPORTANT]  
>  Laske uudelleensuunnittelu -toiminto on yleisin prosessi. Suunnitelman laskennan ja toimenpideviestin toteuttamisen prosesseja voidaan kuitenkin käyttää Laske nettomuutossuunnitelma -toiminnon suorittamiseen.  
>   
>  Hae toimenpideviestit -suunnitelma voidaan suorittaa nettomuutossuunnittelu- ja uudelleensuunnitteluajojen välissä. Tällöin saadaan välitön käsitys aikataulumuutosten vaikutuksista. Tätä suunnitelmaa ei kuitenkaan ole tarkoitettu nettomuutossuunnittelun tai uudelleensuunnittelun korvaajaksi.  

## <a name="to-calculate-the-planning-worksheet"></a>Suunnittelutyökirjan laskeminen  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Suunnittelutyökirjat** ja valitse sitten vastaava linkki.  
2.  Avaa **Laske suunnitelma** -sivu valitsemalla **Laske uudelleensuunnittelu** -toiminto.  
3.  Täytä **Vaihtoehdot**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Tuotanto-ohjelma**|Valitse tämä, jos haluat käynnistää tuotanto-ohjelman laskennan. Tässä ajossa otetaan huomioon nimikkeet, joilla on avoimia myyntitilauksia tai kysyntäennusteita.|  
    |**Tarvelaskenta**|Valitse tämä, jos haluat käynnistää materiaalitarpeiden suunnittelun laskennan. Tässä ajossa otetaan huomioon nimikkeet, joilla on riippuvuusedellytyksiä. Yleensä tuotanto-ohjelma ja tarvelaskenta suoritetaan samanaikaisesti. Tuotanto-ohjelman ja tarvelaskennan samanaikainen suorittaminen edellyttää, että **Yhdistetty tuot-ohj/tarvelask.** -valintaruutu on valittuna **Tuotannon asetukset** -sivun **Suunnittelu**-pikavälilehdessä.|  
    |**Aloituspvm**|Varastosaatavuus arvioidaan tämän päivämäärän perusteella. Jos nimikkeen käsivarastomäärä alittaa uusintatilauspisteen, järjestelmä aikatauluttaa täydennystilauksen ennakkotilauksena tämän päivämäärän perusteella. Jos nimikkeen määrä alittaa varmuusvaraston määrän (aloituspäivänä), järjestelmä aikatauluttaa takautuvasti täydennystilauksen, jonka eräpäivä on sunnittelun aloituspäivämäärä.|  
    |**Lopetuspvm**|Tämä on suunnitteluhorisontin päättymispäivämäärä. Kysyntää ja tarjontaa ei lasketa tätä päivämäärää edemmäs. Jos nimikkeen uusintatilausväli ulottuu lopetuspäivämäärän jälkeiselle ajalle, kyseisen nimikkeen suunnitteluhorisontin voimassaoloaika on Tilauspvm- ja Uusintatilausväli-arvojen summa.<br /><br /> Suunnitteluhorisontti tarkoittaa aikaa, jonka suunnitelma kattaa. Jos horisontti on liian lyhyt, pitkän toimitusajan nimikkeiden tilaukset myöhästyvät. Jos horisontti on liian pitkä, sellaisia tietoja tarkistetaan ja käsitellään liian kauan, jotka todennäköisesti ehtivät muuttua, ennen kuin niitä tarvitaan. Tuotantoa varten voi määrittää toisen ja ostoja varten toisen, pidemmän suunnitteluhorisontin, vaikka tämä ei olekaan välttämätöntä. Ostojen ja tuotannon suunnitteluhorisontit täytyy määrittää siten, että ne kattavat komponenttien kumulatiivisen toimitusajan.|  
    |**Pysäytä ja näytä ensimmäinen virhe**|Valitse, jos haluat suunnitteluajon keskeytyvän heti, kun siinä ilmenee virhe. Samalla näyttöön tulee sanoma, jossa on tietoja (ensimmäisestä) virheestä. Virhetilanteessa vain ennen virheen ilmenemistä tehdyt onnistuneet suunnittelurivit esitetään suunnittelutyökirjassa. Jos et ole lisännyt valintamerkkiä tähän kenttään, **Laske suunnitelma** -eräajoa jatketaan mahdollisista virheistä huolimatta loppuun saakka. Jos virheitä ilmenee, ohjelma tuo eräajon jälkeen näkyviin sanoman, jossa ilmoitetaan virheiden vaikutusalueeseen kuuluvien nimikkeiden määrä. Jos virheitä ilmenee, ohjelma tuo eräajon jälkeen näkyviin sanoman, jossa ilmoitetaan virheiden vaikutusalueeseen kuuluvien nimikkeiden määrä. Näkyviin tulee sitten **Suunnittelun virheloki** -sivu, jossa on lisätietoja virheestä ja linkit virheen vaikutusalueeseen kuuluvien nimikkeiden kortteihin.|  
    |**Käytä ennustetta**|Valitse ennuste, jonka haluat ohjelman sisällyttävän kysyntään suunnittelueräajon yhteydessä. Oletusennuste määritetään **Tuotannon asetukset** -sivun **Suunnittelu**-pikavälilehdessä.|  
    |**Sulje ennuste pois ennen**|Tässä kentässä voit määrittää, kuinka suuri valitun ennusteen osa suunnitteluajoon sisällytetään. Tämä tehdään lisäämällä päivämäärä, jota edeltävää ennustettua kysyntää ei oteta mukaan. Tällä tavoin voit jättää vanhat tiedot pois.|  
    |**Noudata suunnitteluparametreja poikkeusvaroituksille**|Tämä kenttä on oletusarvoisesti piilotettuna.<br /><br /> Tarjontaa suunnitteluriveillä, joilla on varoituksia, ei yleensä muokata suunnitteluparametrien mukaan. Suunnittelujärjestelmä ehdottaa sen sijaan vain toimitusmäärää, joka kattaa kysyntämäärän täsmällisesti. Voit kuitenkin määrittää suunnitteluriveille tiettyjä suunnitteluparametreja, joihin liittyy tiettyjä varoituksia.<br /><br />|  

4.  **Nimike**-pikavälilehdessä voit suodattaa ja suorittaa suunnittelutoimia nimikkeen, nimikkeen kuvauksen tai sijainnin perusteella.  
5.  Valitse **OK**-painike. Eräajo suoritetaan ja suunnittelurivit täytetään suunnittelutyökirjaan.  

## <a name="to-perform-action-messages"></a>Suorita toimenpideviestit  
1.  Valitse **Suunnittelutyökirja**-sivulla **Toteuta toimenpideviesti** -toiminto.  
2.  Määritä **Asetukset**-pikavälilehdessä, miten toimitukset luodaan. Täytä tilikentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Tuotantotilaus**|Määrittää, miten tuotantotilaukset luodaan. Nämä toimet voit tehdä suoraan suunnittelurivin ehdotuksista. Voit luoda sekä suunniteltuja että sitovasti suunniteltuja tuotantotilauksia.|  
    |**Kokoonpanotilaus**|Määrittää, miten kokoonpanotilaukset luodaan. Nämä toimet voit tehdä suoraan suunnittelurivin ehdotuksista.|  
    |**Ostotilaus**|Määrittää, miten ostotilaukset luodaan. Nämä toimet voit tehdä suoraan suunnittelurivin ehdotuksista.<br /><br /> Jos olet valinnut kopioivasi suunnitteluriviehdotukset ostotilauksia varten hankintalistaan, valitse mallin ja työkirjan nimi.|  
    |**Siirtotilaus**|Määrittää, miten siirtotilaukset luodaan. Nämä toimet voit tehdä suoraan suunnittelurivin ehdotuksista.<br /><br /> Jos olet valinnut kopioivasi suunnitteluriviehdotukset siirtotilauksia varten hankintalistaan, valitse mallin ja työkirjan nimi.|  
    |**Yhdistä siirtotilaukset**|Valitse, jos haluat yhdistää siirtotilauksia.|  
    |**Pysäytä ja näytä ensimmäinen virhe**|Valitse, jos haluat, että **Toteuta toim.pidviesti - Suun.** -erä-ajo pysähtyy heti, kun se havaitsee virheen. Samalla näyttöön tulee sanoma, jossa on tietoja (ensimmäisestä) virheestä. Virhetilanteessa vain virhettä ennen käsitellyistä suunnitteluriveistä luodaan toimitustilauksia.|  

3.  **Suunnittelurivi**-pikavälilehdessä voit määrittää toimenpideviestien luomista rajoittavia suodattimia.  
4.  Valitse **OK**-painike.  

Eräajo poistaa työkirjan rivit toimenpideviestin suorittamisen jälkeen. Muut rivit jäävät suunnittelutyökirjaan, kunnes ne joko hyväksytään myöhemmin tai muuten poistetaan. Rivit voi poistaa myös manuaalisesti.  

## <a name="action-messages"></a>Toimenpideviestit  
Tilausten seurantajärjestelmä tuottaa toimenpideviestejä, kun nykyisessä tilausverkossa ei päästä tasapainoon. Ne ovat sellaisiin muutoksiin kehottavia ehdotuksia, jotka tasapainottavat kysynnän ja tarjonnan uudelleen.  

Toimenpideviestejä luodaan taso kerrallaan kunkin nimikkeen alatason koodin mukaan. Näin varmistetaan, että kaikki nimikkeet, joiden kysyntään tai tarjontaan on tullut tai tulee muutoksia, otetaan huomioon.  

Pieniltä, tarpeettomilta tai merkityksettömiltä toimenpideviesteiltä voidaan välttyä käyttämällä toimenpideviestien luomista rajoittavia vaimentimia. Niitä käytettäessä vain sellaiset muutokset aiheuttavat toimenpideviestin, jotka ylittävät määritetyn määrän tai määritetyn päivien määrän.  

Kun toimenpideviestit on käyty läpi ja ehdotetut muutokset on päätetty hyväksyä osittain tai kokonaan (lisäämällä valintamerkki **Hyväksy toimenpideviesti** -kenttään tai poistamalla valintamerkki kentästä), voit tehdä aikatauluun päivitykset.  

> [!NOTE]  
>  Toimenpideviesti on ehdotus, joka kehottaa luomaan uuden tilauksen, peruuttamaan tilauksen tai muuttamaan tilauksen määrää tai päivämäärää. Tilaus voi olla ostotilaus, siirtotilaus tai tuotantotilaus.  

Ohjelma luo seuraavia toimenpideviestejä, jos kysyntä ja tarjonta menevät epätasapainoon:  

|Toimenpideviesti|Kuvaus|  
|--------------------|---------------------------------------|  
|**Uusi**|Jos olemassa olevia tilauksia koskevien toimenpideviestien **Muuta määrä**, **Aikataul. uud.** tai **Aikataul. uud. ja Muuta määrä** ehdotukset eivät riitä täyttämään kysyntää, järjestelmä luo uuteen tilaukseen kehottavan toimenpideviestin **Uusi**. Järjestelmä luo toimenpideviestin **Uusi** myös, jos kyseisen nimikkeen uusintatilausvälissä ei ole toimitustilauksia. Tämä parametri määrittää saatavuusprofiilin jaksojen määrän eteen- ja taaksepäin, kun uudelleen aikataulutettavaa tilausta etsitään.|  
|**Muuta määrä**|Kun määrä muuttuu toimitustilauksiin seurattavassa kysynnässä, järjestelmää luo toimenpideviestin **Muuta määrä**. Se merkitsee, että asiaankuuluvaa tarjontaa täytyy muuttaa suhteessa kysynnässä tapahtuneeseen muutokseen. Jos uutta kysyntää ilmenee, [!INCLUDE[prod_short](includes/prod_short.md)] etsii uusintatilausvälin lähimmän varaamattoman tuotantotilauksen ja luo kyseistä tilausta koskevan, muutokseen kehottavan toimenpideviestin.|  
|**Aikataul. uud.**|Kun tarjonta- tai kysyntätilauksessa tapahtuva päivämäärämuutos aiheuttaa epätasapainon tilausverkossa, järjestelmä antaa toimenpideviestin **Aikatauluta uud**. Jos kysynnän ja tarjonnan suhde on 1:1, järjestelmä antaa toimitustilauksen siirtämistä koskevan toimenpideviestin. Jos toimitustilaus kattaa usean myyntitilauksen kysynnän, toimitustilaus aikataulutetaan uudelleen ensimmäisen kysynnän päivämäärän mukaiseksi.|  
|**Aikataul. uud. & Muuta määrä**|Jos sekä päivämääriä että määriä on muutettu tilauksessa, suunnitelmia täytyy muuttaa molemmat osatekijät huomioon ottaen. Toimenpiteitä ehdotetaan yhteisessä toimenpideviestissä **Aikatauluta uud. ja Muuta määrä**, jotta tilausverkko saadaan takaisin tasapainoon.|  
|**Peruuta**|Jos sellainen kysyntä poistetaan, johon on vastattu tilauskohtaisesti, järjestelmä antaa asianmukaisten toimitustilausten peruuttamiseen kehottavan toimenpideviestin. Jos suhde ei ole tilauskohtainen, järjestelmä luo muutokseen kehottavan toimenpideviestin kysynnän vähentämiseksi. Jos muut tekijät, kuten varastonmuutokset, aiheuttavat sen, että tuotantotilausta ei tarvita, kun käyttäjä luo toimenpideviestejä, [!INCLUDE[prod_short](includes/prod_short.md)] ehdottaa työkirjassa toimenpideviestiä **Peruuta**.|  

## <a name="see-also"></a>Katso myös  
[Suunnittelu](production-planning.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]