---
title: 'Kokonaisvaltaisen suunnittelun, tuotanto-ohjelman tai tarvelaskennan suorittaminen'
description: 'Suunnittelujärjestelmä voi laskea tuotanto-ohjelman tai tarvelaskennan pyydettäessä, tai se voi laskea molemmat samanaikaisesti.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: '99000852, 99000860'
ms.date: 01/24/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Kokonaisvaltaisen suunnittelun, tuotanto-ohjelman tai tarvelaskennan suorittaminen

Suunnittelutyökirjan suorittaminen ja tarvelaskennan suorittaminen tarkoittaa tuotanto-ohjelman ja materiaalitarpeen laskemista. Laskenta perustuu todelliseen ja ennustettuun kysyntään. Suunnittelujärjestelmä voi laskea tuotanto-ohjelman tai tarvelaskennan pyydettäessä, tai se voi laskea molemmat samanaikaisesti.  

- Tuotanto-ohjelma tarkoittaa todelliseen tarpeeseen ja kysyntäennusteeseen perustuvaa tuotanto-ohjelman laskentaa. Tuotanto-ohjelman laskenta tehdään lopullisille nimikkeille, joilla on ennuste ja/tai myyntitilauksen rivi. Näitä nimikkeitä kutsutaan tuotanto-ohjelmanimikkeiksi, ja ne tunnistetaan dynaamisesti laskennan alkaessa.  
- MRP tarkoittaa komponenttien todelliseen tarpeeseen ja komponenttitason kysyntäennusteeseen perustuvaa materiaalitarpeen laskentaa. Tarvelaskenta tehdään vain nimikkeille, jotka eivät ole tuotanto-ohjelmanimikkeitä. Tuotanto-ohjelman yleistavoitteena on tuottaa aikavaiheistetut, viralliset nimikekohtaiset suunnitelmat, jotta oikeaa tuotetta voidaan toimittaa oikea nimike ja oikea määrä oikeaan aikaan ja oikeassa paikassa.  

Tuotanto-ohjelmassa ja tarvelaskennassa käytetään samoja suunnittelualgoritmeja. Algoritmit liittyvät nettouttamiseen, aiempien täydennystilausten uudelleenkäyttöön ja toimenpideviesteihin. Suunnittelujärjestelmä selvittää, mitä nyt tai vastaisuudessa tarvitaan (kysyntä) sekä mitä on käsivarastossa ja mitä tulossa (tarjonta). Kun nettoutat nämä määrät, [!INCLUDE[prod_short](includes/prod_short.md)] näyttää toimenpideviestejä. Toimenpideviestit ovat ehdotuksia, jotka kehottavat luomaan uuden tilauksen, muuttamaan tilausta (määrää tai päivämäärää) tai peruuttamaan tilauksen. Tilauksella tarkoitetaan ostotilauksia, kokoonpanotilauksia, tuotantotilauksia ja siirtotilauksia.

Voit seurata **Tilauksen seuranta** -sivulta suunnittelun luomia linkkejä kysynnän ja tarjonnan välille. Lisätietoja on kohdassa [Kysynnän ja tarjonnan välisten suhteiden seuranta](production-how-track-demand-supply.md).

Suunnitelmasta saadaan asianmukaisia tuloksia sen mukaan, kuinka nimikkeen kortit, tuotannon tuoterakenteet ja reititykset on määritetty.  

## Suunnitelman luomismenetelmät  

- **Laske uudelleensuunnittelu:** Käsittele tai uudista materiaalisuunnitelma. Prosessin aluksi kaikki ladatut suunnitellut toimitustilaukset poistetaan. Tietokannan kaikki nimikkeet suunnitellaan uudelleen.  
- **Laske nettomuutossuunnitelma**: Käsittele nettomuutossuunnitelma. Kun nimikkeitä käsitellään nettomuutossuunnitelmassa kahden tyyppisistä muutoksista:  
   - **Kysynnän/tarjonnan muutokset:** Tällaisia muutoksia ovat myyntitilausten, kysyntäennusteiden, tuotantotilausten, kokoonpanotilausten ja ostotilausten määrien muutokset. Myös suunnittelematon varastotason muutos katsotaan määrän muutokseksi.  
   - **Suunnitteluparametrien muutokset**: Tällaisia muutoksia ovat varmuusvaraston, uusintatilauspisteen, reitityksen ja tuoterakenteen muutokset sekä aikavälin ja toimitusajan laskennan muutokset.  
- **Hae toimenpideviestit**: Toimii lyhyen aikavälin suunnittelutyökaluna lähettämällä toimintaviestejä varoittamaan käyttäjää muutoksista, jotka on tehty sen jälkeen, kun viimeksi laskit regeneratiivisen tai nettomuutossuunnitelman.  

Jokaisen suunnitellun menetelmän kanssa, [!INCLUDE[prod_short](includes/prod_short.md)] luo työkirjatapahtumat olettaen, että kapasiteetti on ääretön. Tuotantosolun ja kuormitusryhmän kapasiteettia ei huomioida laadittaessa aikatauluja.  

> [!IMPORTANT]  
> Laske uudelleensuunnittelu on yleisin prosessi. Suunnitelman laskentaa ja toimenpideviestin toteuttamista voidaan kuitenkin käyttää Laske nettomuutossuunnitelma -toiminnon suorittamiseen.  
>
> Voit suorittaa Hae toimenpideviestit -suunnitelman uudelleensuunnittelu- ja nettomuutossuunnittelusuoritusten välillä. Näin saadaan välitön käsitys aikataulumuutosten vaikutuksista. Sen ei kuitenkaan ole tarkoitus korvata kaikkia uudelleensuunnittelu- tai nettomuutossuunnitteluprosesseja.  

## Suunnittelutyökirjan laskeminen
  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Suunnittelutyökirjat** ja valitse sitten vastaava linkki.  
2. Avaa **Laske suunnitelma** -sivu valitsemalla **Laske uudelleensuunnittelu** -toiminto.  
3. Täytä **Vaihtoehdot**-pikavälilehden kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Tuotanto-ohjelma**|Laske päätuotantoaikataulu. Tässä ajossa otetaan huomioon nimikkeet, joilla on avoimia myyntitilauksia tai kysyntäennusteita. <br/>Jos tällaisille nimikkeille on olemassa myös muita vaatimuksia, kuten varmuusvarasto, uusintatilauspiste tai avoimet tuotantokomponenttirivit, nämä vaatimukset sisällytetään tuotanto-ohjelman laskentaan, jotta suunnittelujärjestelmä käsittelee koko varastoprofiilin.  |  
    |**Tarvelaskenta**|Materiaalitarpeen suunnittelun laskeminen. Tässä ajossa otetaan huomioon nimikkeet, joilla on riippuvuusedellytyksiä. Yleensä tuotanto-ohjelma ja tarvelaskenta suoritetaan samanaikaisesti. Tuotanto-ohjelman ja tarvelaskennan samanaikainen suorittaminen edellyttää, että **Yhdistetty tuot-ohj/tarvelask.** -kenttä on valittuna **Tuotannon asetukset** -sivun **Suunnittelu**-pikavälilehdessä.|  
    |**Aloituspvm**|Varaston saatavuuden arviointi. Jos nimikkeen käsivarastomäärä alittaa uusintatilauspisteen, järjestelmä aikatauluttaa täydennystilauksen ennakkotilauksena tämän päivämäärän perusteella. Jos nimikkeen määrä alittaa varmuusvaraston määrän (aloituspäivänä), järjestelmä aikatauluttaa takautuvasti täydennystilauksen, jonka eräpäivä on sunnittelun aloituspäivämäärä.|  
    |**Lopetuspvm**|Suunnitteluhorisontin päättymispäivämäärä. Kysyntää ja tarjontaa ei lasketa tätä päivämäärää edemmäs. Jos nimikkeen uusintatilausväli ulottuu lopetuspäivämäärän jälkeiselle ajalle, kyseisen nimikkeen suunnitteluhorisontin voimassaoloaika on Tilauspvm- ja Uusintatilausväli-arvojen summa.<br/><br/> Suunnitteluhorisontti tarkoittaa aikaa, jonka suunnitelma kattaa. Jos horisontti on liian lyhyt, pitkän toimitusajan nimikkeiden tilaukset myöhästyvät. Jos horisontti on liian pitkä, sellaisia tietoja tarkistetaan ja käsitellään liian kauan, jotka todennäköisesti ehtivät muuttua, ennen kuin niitä tarvitaan. Voit määrittää tuotantoa varten toisen ja ostoja varten toisen, pidemmän suunnitteluhorisontin, vaikka tämä ei olekaan välttämätöntä. Ostojen ja tuotannon suunnitteluhorisontit täytyy määrittää siten, että ne kattavat komponenttien kokonaistoimitusajan.|  
    |**Pysäytä ja näytä ensimmäinen virhe**|Valitse tämä vaihtoehto, jos haluat suunnitteluajon keskeytyvän heti, kun siinä ilmenee virhe. Avautuvassa sanomassa on tietoja virheestä. Virhetilanteessa vain ennen virheen ilmenemistä tehdyt onnistuneet suunnittelurivit esitetään suunnittelutyökirjassa. Jos et valitse kenttää, **Laske suunnitelma** -eräajo jatkuu valmistumiseen saakka. Virheet eivät keskeytä eräajoa. Jos virheitä ilmenee, ohjelma tuo eräajon jälkeen näkyviin sanoman, jossa ilmoitetaan virheiden vaikutusalueeseen kuuluvien nimikkeiden määrä. Jos virheitä ilmenee, ohjelma tuo eräajon jälkeen näkyviin sanoman, jossa ilmoitetaan virheiden vaikutusalueeseen kuuluvien nimikkeiden määrä. Näkyviin tulee sitten **Suunnittelun virheloki** -sivu, jossa on lisätietoja virheestä ja linkit virheen vaikutusalueeseen kuuluvien nimikkeiden kortteihin.|  
    |**Käytä ennustetta**|Valitse ennuste, jonka haluat ohjelman sisällyttävän kysyntään suunnittelueräajon yhteydessä. Oletusennuste määritetään **Tuotannon asetukset** -sivun **Suunnittelu**-pikavälilehdessä.|  
    |**Sulje ennuste pois ennen**|Määritä, mikä osa ennusteesta otetaan mukaan suunnitteluajoon, antamalla päivämäärä, jota aiempaa ennustettua kysyntää ei oteta huomioon.|  
    |**Noudata suunnitteluparametreja poikkeusvaroituksille**|Tämä kenttä on oletusarvoisesti piilotettuna.<br/><br/> Tarjontaa suunnitteluriveillä, joilla on varoituksia, ei yleensä muokata suunnitteluparametrien mukaan. Suunnittelujärjestelmä ehdottaa sen sijaan vain toimitusmäärää, joka kattaa kysyntämäärän täsmällisesti. Voit kuitenkin määrittää suunnitteluriveille tiettyjä suunnitteluparametreja, joihin liittyy tiettyjä varoituksia.<br/><br/>|  

4. **Nimike**-pikavälilehdessä voit suodattaa ja suorittaa suunnittelutoimia nimikkeen, nimikkeen kuvauksen tai sijainnin perusteella.  
5. Valitse **OK**-painike. Eräajo suoritetaan ja suunnittelurivit lisätään suunnittelutyökirjaan.  

## Suorita toimenpideviestit
  
1. Valitse **Suunnittelutyökirja**-sivulla **Toteuta toimenpideviesti** -toiminto.  
2. Määritä **Asetukset**-pikavälilehdessä, miten toimitukset luodaan. Täytä tilikentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Tuotantotilaus**|Määritä, kuinka tuotantotilaukset luodaan. Nämä toimet voit tehdä suoraan suunnittelurivin ehdotuksista. Voit luoda sekä suunniteltuja että sitovasti suunniteltuja tuotantotilauksia.|  
    |**Kokoonpanotilaus**|Määritä, miten kokoonpanotilaukset luodaan. Nämä toimet voit tehdä suoraan suunnittelurivin ehdotuksista.|  
    |**Ostotilaus**|Määritä, miten ostotilaukset luodaan. Nämä toimet voit tehdä suoraan suunnittelurivin ehdotuksista.<br/><br/> Jos olet valinnut kopioivasi suunnitteluriviehdotukset ostotilauksia varten hankintalistaan, valitse mallin ja työkirjan nimi.|  
    |**Siirtotilaus**|Määritä, miten siirtotilaukset luodaan. Nämä toimet voit tehdä suoraan suunnittelurivin ehdotuksista.<br/><br/> Jos olet valinnut kopioivasi suunnitteluriviehdotukset siirtotilauksia varten hankintalistaan, valitse mallin ja työkirjan nimi.|  
    |**Yhdistä siirtotilaukset**|Valitse haluatko yhdistää siirtotilauksia.|  
    |**Pysäytä ja näytä ensimmäinen virhe**|Valitse tämä vaihtoehto, jos haluat, että **Toteuta toim.pidviesti - Suun.** -eräajo pysähtyy heti, kun se havaitsee virheen. Avautuvassa sanomassa on tietoja virheestä. Virhetilanteessa vain virhettä ennen käsitellyistä suunnitteluriveistä luodaan toimitustilauksia.|  

3. **Suunnittelurivi**-pikavälilehdessä voit määrittää toimenpideviestien luomista rajoittavia suodattimia.  
4. Valitse **OK**-painike.  

Eräajo poistaa työkirjan rivit toimenpideviestin suorittamisen jälkeen. Muut rivit jäävät suunnittelutyökirjaan, kunnes ne joko hyväksytään myöhemmin tai muuten poistetaan. Rivit voi poistaa myös manuaalisesti.  

## Toimenpideviestit
  
Tilausten seurantajärjestelmä tuottaa toimenpideviestejä, kun nykyisessä tilausverkossa ei päästä tasapainoon. Viestit voidaan nähdä sellaisiin muutoksiin kehottavina ehdotuksina, jotka tasapainottavat kysynnän ja tarjonnan uudelleen.  

Toimenpideviestejä luodaan taso kerrallaan kunkin nimikkeen alatason koodin mukaan. Näin varmistetaan, että kaikki nimikkeet, joiden kysyntään tai tarjontaan on tullut tai tulee muutoksia, otetaan huomioon.  

Pieniltä, tarpeettomilta tai merkityksettömiltä toimenpideviesteiltä voidaan välttyä käyttämällä toimenpideviestien luomista rajoittavia vaimentimia. Niitä käytettäessä vain sellaiset muutokset aiheuttavat toimenpideviestin, jotka ylittävät määritetyn määrän tai määritetyn päivien määrän.  

Kun toimenpideviestit on käyty läpi ja ehdotetut muutokset on päätetty hyväksyä osittain tai kokonaan, valitse **Hyväksy toimenpideviesti** -kenttä. Päivitä seuraavaksi aikataulut sen mukaisesti.  

> [!NOTE]  
> Toimenpideviesti on ehdotus, joka kehottaa luomaan uuden tilauksen, peruuttamaan tilauksen tai muuttamaan tilauksen määrää tai päivämäärää. Tilaus voi olla ostotilaus, siirtotilaus tai tuotantotilaus.  

Ohjelma luo seuraavia toimenpideviestejä, jos kysyntä ja tarjonta menevät epätasapainoon:  

|Toimenpideviesti|Kuvaus|  
|--------------------|---------------------------------------|  
|**Uusi**|Jos olemassa olevia tilauksia koskevien toimenpideviestien **Muuta määrä**, **Aikataul. uud.** tai **Aikataul. uud. ja Muuta määrä** ehdotukset eivät riitä täyttämään kysyntää, järjestelmä luo uuteen tilaukseen kehottavan toimenpideviestin **Uusi**. Järjestelmä luo viestin **Uusi** myös, jos kyseisen nimikkeen uusintatilausvälissä ei ole toimitustilauksia. Tämä vaihtoehto määrittää saatavuusprofiilin jaksojen määrän eteen- ja taaksepäin, kun uudelleen aikataulutettavaa tilausta etsitään.|  
|**Muuta määrä**|Kun määrä muuttuu toimitustilauksiin seurattavassa kysynnässä, toimenpideviesti **Muuta määrä** luodaan. Viesti merkitsee, että asiaankuuluvaa tarjontaa täytyy muuttaa suhteessa kysynnässä tapahtuneeseen muutokseen. Jos uutta kysyntää ilmenee, [!INCLUDE[prod_short](includes/prod_short.md)] etsii uusintatilausvälin lähimmän varaamattoman tuotantotilauksen ja luo kyseistä tilausta koskevan, muutokseen kehottavan toimenpideviestin.|  
|**Aikatauluta uudelleen**|Kun tarjonta- tai kysyntätilauksen päivämäärän muutos aiheuttaa epätasapainon tilausverkostossa, toimintasanoma **Aikatauluta uudelleen** luodaan. Jos kysynnän ja tarjonnan suhde on 1:1, toimintosanoma luodaan ehdottamaan toimitustilauksen siirtämistä. Jos toimitustilaus kattaa usean myyntitilauksen kysynnän, toimitustilaus aikataulutetaan uudelleen ensimmäisen kysynnän päivämäärän mukaiseksi.|  
|**Aikataul. uud. & Muuta määrä**|Jos sekä päivämääriä että määriä muutetaan tilauksessa, suunnitelmia täytyy muuttaa molemmat osatekijät huomioon ottaen. Toimenpiteitä ehdotetaan yhteisessä toimenpideviestissä **Aikatauluta uud. ja Muuta määrä**, jotta tilausverkko saadaan takaisin tasapainoon.|  
|**Peruuta**|Jos sellainen kysyntä poistetaan, johon on vastattu tilauskohtaisesti, järjestelmä antaa asianmukaisten toimitustilausten peruuttamiseen kehottavan toimenpideviestin. Jos suhde ei ole tilauskohtainen, järjestelmä luo muutokseen kehottavan toimenpideviestin kysynnän vähentämiseksi. Jos muut tekijät, kuten varastonmuutokset, aiheuttavat sen, että tuotantotilausta ei tarvita, kun luot toimenpideviestejä, [!INCLUDE[prod_short](includes/prod_short.md)] ehdottaa työkirjassa toimenpideviestiä **Peruuta**.|  

## Katso myös  

[Suunnittelu](production-planning.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
