---
title: Vaihekuvaus – Projektinhallinta Projektit-sovellusalueen avulla
description: 'Tässä opastuksessa esitellään töiden projektinhallintaominaisuudet, joiden avulla voit ajoittaa yrityksesi resurssien käytön ja paljon muuta.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# Vaihekuvaus: Projektinhallinta Projektit-sovellusalueen avulla

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Tässä vaihekuvauksessa esitellään töiden projektinhallintatoiminnot. Projektien avulla voit laatia yrityksen resurssien käyttöön liittyviä aikatauluja ja seurata tietyn projektin resursseihin liittyviä kustannuksia. Projekteissa kuluu esimerkiksi työntekijöiden työtunteja, koneiden käyttötunteja ja varastonimikkeitä, joita täytyy seurata projektin edetessä.  

 Tässä vaihekuvauksessa käsitellään uusien projektien määrittämistä moduulissa sekä joitakin tavanomaisia tehtäviä, joita ovat esimerkiksi kiinteän hinnoittelun käsittely, maksujen suorittaminen osamaksuina, projektien laskujen kirjaaminen sekä projektien kopioiminen.  

## Tietoja tästä vaihekuvauksesta

 Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

### Projektin määrittäminen

 Budjettirakenne määritettynä projekteille, prjektin luominen on yksinkertaista. Tässä vaihekuvauksessa käsitellään seuraavia vaiheita:  

- tehtävärivien ja suunnittelurivien määrittäminen  
- projektikohtaisten hintojen luominen nimikkeille, resursseille ja KP-tileille  
- laskuttaminen projektista.  

### Kiinteiden hintojen käsitteleminen

 Projektit-sovellusalueessa voit käsitellä paitsi kiinteitä hintoja myös sellaisia palveluiden tai tavaroiden hintoja, joista on sovittu ennalta asiakkaiden kanssa. Tässä vaihekuvauksessa voit tehdä seuraavat toimet:  

- Katso, kuinka sopimuksen ja laskun arvot määritetään  
- Salli ylimääräisen (laskuttamattoman) työn lisääminen aikatauluun.  

### Projektin kopioiminen

 Tässä esimerkkitilanteessa keskitytään siihen, kuinka koko projekti tai osa siitä kopioidaan tietojen manuaalisen lisäämistarpeen vähentämiseksi ja tarkkuuden parantamiseksi. Mukana olevia aiheita ovat Se sisältää seuraavat:  

- projektin osan kopioiminen uuteen projektiin  
- projektikohtaisten hintojen kopioiminen  
- suunnittelurivien kopioiminen.  

### Maksujen suorittaminen osamaksuina

 Kun suuri, kallis projekti kestää pitkään, asiakas tekee usein yrityksen kanssa sopimuksen maksuerien maksamiseksi. Tämä esimerkki näyttää, miten maksutapa määritellään osamaksuina, ja se kattaa seuraavat asiat:  

- osamaksun luominen projektille  
- maksujen laskuttaminen asiakkailta  
- käytön ottaminen huomioon projektissa, jossa käytetään osamaksua.  

## Roolit

 Tässä vaihekuvauksessa on seuraaviin rooleihin liittyviä tehtäviä:  

- Projektipäällikkö  
- Projektitiimin jäsen  

## Vaatimukset

 Tee seuraavat toimet ennen tämän vaihekuvauksen tehtävien suorittamista:  

- Asenna CRONUS-esittelytietokanta.
- Luo esimerkkitietoja noudattamalla seuraavan osan toimintaohjeita.  

## Taustatietoja

Tämä vaihekuvaus keskittyy CRONUS-nimiseen suunnittelu- ja konsulttifirmaan, joka suunnittelee ja sovittaa uusia infrastruktuureja, kuten konferenssihalleja ja toimistoja huonekaluineen, tarvikkeineen ja varastointiyksikköineen. Sen useimmat työt projektisuuntautuneita. Thomas, CRONUSin projektipäällikkö, saa käynnissä olevien CRONUSin käynnistämien projektien ansiosta yleiskäsityksen jokaisesta meneillään olevasta ja valmiista projektista. Thomas järjestää tavallisesti kaupat asiakkaiden kanssa ja lisää projektin ydintiedot, joita olivat tehtävä- ja suunnittelurivit sekä hinnat, [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Thomas toteaa, että tietojen luominen, ylläpitäminen ja tarkistaminen on suoraviivaista. Thomas pitää myös tavasta, jolla [!INCLUDE[prod_short](includes/prod_short.md)] mahdollistaa töiden kopioinnin ja maksamisen osamaksuina.

 Projektitiimin jäsen Marianne, joka työskentelee Thomasin alaisena, on projektin päivittäinen vastuuhenkilö. Marianne lisää paitsi omat työt myös teknikoiden kussakin tehtävässä suorittamat työt, mukaan lukien työssä käytetyt nimikkeet ja työstä kertyneet kustannukset.  

## Esimerkkitietojen valmisteleminen

 Valmistaudu tähän vaihekuvaukseen lisäämällä Tricia uutena resurssina.  

### Esimerkkitietojen valmisteleminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten vastaava linkki.  
2.  Luo uusi resurssin kortti valitsemalla **Uusi**-toiminto.  
3.  Anna **Yleiset**-pikavälilehdessä seuraavat tiedot:  

    - **Nro:**: **Marianne**  
    - **Nimi**: **Marianne**  
    - **Tyyppi**: **Henkilö**  

4.  Valitse **Perusmittayksikkö** -kenttä ja avaa sitten **Resurssin mittayksikkö** -sivu valitsemalla **Uusi**. Valitse **Tyyppi**-kentässä **Tunti**.  
5.  Lisää seuraavat tiedot **Laskutus**-pikavälilehteen:  

    - **Välitön yksikkökustannus**: **5**  
    - **Välillinen kustannus**: **4**  
    - **Yksikkökustannus**: **10**  
    - **Yleinen tuotteen kirjausryhmä**: **Palvelut**  
    - **Tuotteen ALV-kirjausryhmä**: **ALV 25**  

6. Sulje sivu.

Seuraavassa toimenpiteessä luot projektipäiväkirjan erän Mariannea varten, jotta hän voi kirjata käyttönsä.  

### Luo uusi päiväkirjan erä.  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2.  Valitse **Projektipäiväkirja**-sivulla **Erän nimi**-kenttä. **Projektipäiväkirjan erät** -sivu avautuu.  
3.  Valitse **Uusi**-toiminto, jos haluat luoda uuden rivin, jolla ovat seuraavat tiedot:  

    - **Nimi**: **Marianne**  
    - **Kuvaus**: **Marianne**  
    - **Nrosarja**: **PPVK-YLEIN**.  

4.  Tallenna muutokset valitsemalla **OK**-painike.

## Projektin määrittäminen

 Tässä skenaariossa CRONUS on voittanut sopimuksen Progressive Home Furnishings -yrityksen kanssa, jonka kanssa on päästy sopimukseen neuvottelusalin ja ruokasalin suunnittelemisesta. Asiakkaan tilat ovat Yhdysvalloissa, ja projektissa tarvitaan erityistä ohjelmistoa. Projektipäällikkö pääsee asiakkaan sopimukseen ja sopimuksen keston kattava projekti luodaan.  

### Projektin määrittäminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2.  Luo uusi kortti valitsemalla **Uusi**-toiminto.  
3.  Anna **Yleiset**-pikavälilehdessä seuraavat tiedot:  

    - **Kuvaus**: **Konsultointi neuvottelusalin sisustuksesta**  
    - **Laskutusasiakkaan nro**: **01445544**  

4.  Lisää seuraavat tiedot **Kirjaus**-pikavälilehteen:  

    - **Tila**: **Suunnittelu**  
    - **Projektin kirjausryhmä**: **As. määr.**  
    - **KET-menetelmä**: **Kustannusarvo**  

5.  Kirjoita kuluvan päivän päivämäärä **Kesto**-pikavälilehden **Aloituspvm**- ja **Lopetuspvm**-kenttiin. Nämä päivämäärät helpottavat valuuttamuunnosten tekemistä, kun projekti laskutetaan.  
6.  Vahvista **Ulkomaankauppa**-pikavälilehdessä, että valuuttakoodi on **USD**. Jos valitset **Laskun valuutan koodi** -kentässä USD, projekti laskutetaan Yhdysvaltain dollareina ja suunnitellaan vain CRONUSin paikallisen valuutan mukaan.  

 Voit mukauttaa asiakkaiden hinnoittelun työkohtaiseksi sopimuksissa, jotka olet määrittänyt. Seuraavassa toimenpiteessä projektipäällikkö määrittää kustannukset Mariannen ajasta, määrittää tarvittavan ohjelmiston hinnan ja lisää matkakustannukset, jotka asiakas on suostunut maksamaan.  

### Mukauta hinnoittelu  

1.  Valitse projektikortissa **Resurssi**-toiminto.  
2.  Lisää seuraavat tiedot **Projektiresurssien hinnat** -sivulle:  

    - **Koodi**: **Marianne**  
    - **Yksikköhinta**: **20**  

3.  Sulje sivu.  
4.  Valitse **Nimike**-toiminto.  
5.  Lisää seuraavat tiedot ja mukautettu hinta **Projektinimikkeiden hinnat** -sivulle:  

    1.  **Nimikkeen nro**: **80201 (Grafiikkaohjelma)**  
    2.  **Yksikköhinta**: **200**  

6.  Sulje sivu.  
7.  Valitse **KP-tili**-toiminto.  
8.  Anna **Projektin kirjanpitotilin hinnat** -sivulla seuraavat tiedot ja matkan kustannus, jonka asiakas on luvannut maksaa, plus 25 %:  

    1.  **KP-tili**: **8430 (Matka)**  
    2.  **Yksikkökustannustekijä**: **1,25**.  

9. Sulje sivu.  

 Projektin määrittämisen viimeisiä askeleita ovat projektin tehtävien sekä jokaisen tehtävän suunnittelurivien lisääminen. Nämä suunnittelurivit määrittävät, mitä asiakkaalta laskutetaan.  

### Työtehtävien lisääminen  

1.  Valitse uuden projektin **Projekti**-kortissa **Projektitehtävärivit**-toiminto.  
2.  Seuraavassa taulukossa kuvaillaan tiedot, jotka tulisi syöttää kenttiin.  

    |Projektitehtävän nro|Description|Projektitehtävätyyppi|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Konsulttiapua salin sisustukseen|Alkusumma|  
    |1010|Konsultointitapaaminen asiakkaan kanssa|Kirjaus|  
    |1020|Kehittäminen|Kirjaus|  
    |1090|Konsultointi yhteensä|Loppusumma|  

3.  Osoittaaksesi, että jotkin tehtävät ovat muiden tehtävien alaluokkia, valitse **Sisennä projektitehtävät** -toiminto.  

 Suunnittelurivi voi olla jokin seuraavista tyypeistä:  

- **Budjetti**: Lisätty aikatauluun, mutta ei laskutettu.  
- **Laskutettava**: Laskutettu mutta ei lisätty aikatauluun.  
- **Sekä budjetti että laskutettava**: laskutettu ja lisätty aikatauluun.  

 Tässä vaihekuvauksessa projektipäällikön käytössä on **Sekä budjetti että laskutettava**. Hän luo tehtävälle 1010 kolme suunnitteluriviä ja tehtävälle 1020 kaksi suunnitteluriviä.  

### Luo suunnittelurivit  

1. Valitse ensin rivi 1010 ja sitten **Projektin suunnittelurivit** -toiminto.  

2. Luo suunnittelurivit, joissa on seuraavat tiedot:  

    | Rivi | Rivityyppi | Suunnittelupäivämäärä  | Tyyppi        | Ei.   | määrä | Yksikköhinta |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Sekä budjetti että laskutettava | (kuluvan päivän päivämäärä) | Resurssi | Marianne | 40        |     |
    | 2    | Sekä budjetti että laskutettava | (kuluvan päivän päivämäärä) | Resurssi | Teemu | 40        |     |
    | 3    | Sekä budjetti että laskutettava | (kuluvan päivän päivämäärä) | KP-tili | 8430 (Matka) | 2 | 400    |

     Sulje sivu. Summat on päivitetty **Projektitehtävärivit**-sivulla.  
3. Valitse ensin rivi 1020 ja sitten **Projektin suunnittelurivit** -toiminto. Lisää seuraavat tiedot:  

    | Rivi | Rivityyppi | Suunnittelupäivämäärä  | Tyyppi        | Ei.   | määrä | Yksikköhinta |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Sekä budjetti että laskutettava | (kuluvan päivän päivämäärä) | Resurssi | Marianne | 80        |     |
    | 2    | Sekä budjetti että laskutettava | (kuluvan päivän päivämäärä) | Nimike | 80201 (Grafiikkaohjelma) | 1 |     |

4. Sulje sivu. Summat on päivitetty **Projektitehtävärivit**-sivulla.  

## Jäljellä olevan käytön laskeminen

 Marianne, projektiryhmän jäsen, on tehnyt työtä projektissa jonkin aikaa ja haluaa rekisteröidä omat tuntinsa ja käytön projektissa. Työmäärä ja käyttö eivät ole ylittäneet asiakkaan kanssa sovittua määrää. Marianne laskee **Laske jäljellä oleva käyttö** -eräajon avulla projektin jäljellä olevan käytön projektipäiväkirjaan. Erätyö laskee kullekin tehtävälle nimikkeiden, resurssien ja kirjanpitokustannusten suunnitellun käytön ja projektitapahtumiin kirjatun todellisen käytön välisen eron. Jäljellä oleva käyttö tulee näkyviin projektipäiväkirjaan, josta sen voi kirjata.  

### Jäljellä olevan käytön laskeminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2.  Avaa **Projektipäiväkirjan erät** -luettelo napsauttamalla **Projektipäiväkirja**-sivun **Erän nimi** -kentässä. Valitse **Tricia**-projektipäiväkirjan erä.  
3.  Valitse **Laske jäljellä oleva käyttö** -toiminto.  
4.  Valitse **Laske projektin jäljellä oleva käyttö** -sivun **Projektitehtävä**-pikavälilehdessä **Projektinro**-kenttä ja valitse sitten asianmukainen projektin numero, tyypillisesti projekti J00010.  
5.  Kirjoita **Vaihtoehdot**-pikavälilehden **Asiakirjan nro** -kenttään **J00001**. Tämä helpottaa kirjauksen myöhempää jäljittämistä.  
6.  Määritä kirjauspäivämääräksi kuluva päivä.  
7.  Valitse **OK**-painike. Kaikki Thomasin projektipäiväkirjaan luomista suunnitteluriveistä johdetut ehdotetut rivit tuodaan.  
8.  Valitse vahvistussivulla **OK**-painike. Luodut rivit lisätään projektipäiväkirjaan.  
9. Varmista, että kaikki asiakirjan numerot ovat J00001. Valitse sitten **Kirjaa**-toiminto. Vahvista kirjaus valitsemalla **Kyllä**.  

Rivit kirjataan.  

## Projektin myyntilaskun luominen ja kirjaaminen

 Seuraavaksi Marianne voi luoda uuden laskun koko projektia tai projektin osaa varten. Marianne voi myös liittää laskun saman asiakkaan toiseen, samaa projektia koskevaan laskuun. Tällöin Marianne laskuttaa koko projektista, koska projekti on nyt valmis.  

### Projektin myyntilaskun luominen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2.  Valitse ensin aiemmin luotu projekti ja sitten **Luo projektin myyntilasku** -toiminto.  
3.  Tyhjennä **Projektitehtävä**-pikavälilehden **Projektitehtävänro**-kentässä kaikki suodattimet, jotta työ voidaan laskuttaa. Valitse **Projektinro**-kentässä asianmukainen projekti.  
4.  Anna **Vaihtoehdot**-pikavälilehdessä kirjauspäivämäärä ja määritä, haluatko luoda yhden laskun tehtävää kohti vai yhden laskun kaikille tehtäville.  
5.  Luo lasku valitsemalla **OK**-painike ja valitse sitten **OK**-painike vahvistussivulla.  

 Kun Marianne on luonut laskun, hän voi käyttää sitä esimerkiksi **Myyntitilausten käsittelijän** roolikeskuksessa. 

### Uuden myyntilaskun kirjaaminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.  
2.  Avaa sen asiakkaan lasku, jonka asiakkaan numero on 01445544. Suunnitteluriveiltä lisätyt tiedot tulevat näkyviin.  
3.  Valitse **Kirjaa**-toiminto. Vahvista kirjaus valitsemalla **Kyllä**.  

### Kirjatun laskun tarkasteleminen  

1.  Avaa projekti ja valitse sitten **Projektin suunnittelurivit** -toiminto.  
2.  Valitse ensin jokin laskutettu suunnittelurivi ja sitten **Myyntilasku/hyvityslasku**-toiminto.
3. Valitse **Projektin laskut** -sivulla **Avaa myyntilasku/hyvityslasku** -toiminto.  

 Mariannella on kysyttävää tähän projektiin liittyvistä hinnoista, kustannuksista ja tuotoista, joten hän arvioi näitä tietoja **Tilastot**-sivulla.  

### Tilastot-sivun avaaminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2.  Valitse **Tilastot**-toiminto. Voit tarkastella yksityiskohtaisia tietoja projektihinnoista, kustannuksista ja paikallisista ja ulkomaisista valuuttojen voitoista.  
3.  Valitse **Sulje**-painike **Projektin tilastot** -sivun sulkemiseksi.  

## Kiinteiden hintojen käsitteleminen

 CRONUS kanssa on tehty sopimus kokoushuoneiden määrittämiseksi. Projektipäällikkö Thomas tarvitsee hyvän yleiskäsityksen projektin edellyttämistä tehtävistä sekä kuhunkin tehtävään liittyvistä budjetoiduista ja kertyneistä kustannuksista. Tarkoitus on myös selvittää projektin sopimuksenmukainen kokonaishinta sekä tähän mennessä laskutettu summa. Asiakkaan kanssa on päästy sopimukseen projektin kiinteästä hinnoittelusta.  

### Kiinteän hinnoittelun hallinta projekteissa  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse ensin **Espoo**-projektinumero ja sitten **Projektitehtävärivit**- toiminto.  
3. Valitse rivi 1120 ja valitse **Budjetti (kokonaiskustannus)** -kentässä hiiren kakkospainikkeella **Siirtyminen**.  

     Projektin suunnitteluluetteloa tarkasteltaessa päädytään siihen, että myös Mariannea tarvitaan 30 tunniksi projektin tässä vaiheessa. Asiakkaan kanssa sovitaan kiinteästä hinnasta.  

4. Valitse **Projektitehtävärivit**-sivulla ensin rivi 1120 ja sitten **Projektin suunnittelurivit** -toiminto. Luo suunnittelurivi, jossa on seuraavat tiedot:  

    | Rivi | Rivityyppi | Tyyppi        | Ei.   | määrä |
    |------|-----------|-------------|-------|----------|
    | 1    | Sekä budjetti että laskutettava  | Resurssi | Marianne | 30 |

     Sulje sivu.  
5. Kaksoisnapsauta **Budjetti (kokonaiskustannus)** -kenttää hiiren kakkospainikkeella ja valitse uudelleen **Siirtyminen** **Projektitehtävärivit**-sivulla. Tarkastele muutoksia aikatauluun. Kuten huomaat, aikatauluun on lisätty 30 tuntia.  
6. Sulje sivut.  

Kun Marianne on lisätty aikatauluun tämän tehtävärivin osalta, hän työskentelee projektissa 25 tuntia. Nämä tunnit voidaan lisätä projektipäiväkirjaan.  

### Tuntien lisääminen projektipäiväkirjaan  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Lisää seuraavat tiedot uudelle riville:  

    - **Rivityyppi**: **(tyhjä)**  
    - **Kirjauspvm**: **(kuluva päivämäärä)**.  
    - **Asiakirjan nro**:**J00002**  
    - **Projektinro**: **Espoo**  
    - **Projektitehtävänro**: **1120**  
    - **Tyyppi**: **Resurssi**  
    - **Nro:**: **Marianne**  
    - **Määrä**: **25**  

3. Valitse **Kirjaa**-toiminto.  

     Muutamaa päivää myöhemmin Marianne työskentelee vielä 10 tuntia, ja on nyt työskennellyt 35 tuntia. Koska asiakkaan kanssa on sovittu vain 30 tunnista, tunneista vain viisi laskutetaan asiakkaalta. Marianne lisää manuaalisesti aikatauluun viisi lisätuntia, jotka hän on työskennellyt.  

4. Valitse **Projektipäiväkirja**-sivulla **Laske jäljellä oleva käyttö**-toiminto.  
5. Lisää seuraavat tiedot **Laske projektin jäljellä oleva käyttö** -sivun **Vaihtoehdot**-pikavälilehteen:  

    - **Asiakirjan nro**:**J00003**  
    - **Kirjauspvm**: **(kuluva päivämäärä)**.  

6. Lisää seuraavat tiedot **Projektitehtävä**-pikavälilehteen:  

    - **Projektinro**: **Espoo**  
    - **Projektitehtävänro**: **1120**  

7. Suorita laskenta valitsemalla **OK**.

    Mariannen työpäivässä on jäljellä viisi tuntia. **Rivityyppi**-kenttä on tyhjä sen merkiksi, että vain käyttö pysyy kirjattuna, koska työ on jo ajoitettu.  

8. Luo **Projektipäiväkirjan erät** -ikkunassa uusi rivi, jolla on seuraavat tiedot: Varmista, että projektinumerot ovat järjestyksessä seuraavina niistä, joita olet jo käyttänyt:  

    - **Rivityyppi**: **Budjetti**  
    - **Projektinro**: **Espoo**  
    - **Projektitehtävänro**: **1120**  
    - **Tyyppi**: **Resurssi**  
    - **Nro:**: **Marianne**  
    - **Määrä**: **5**  

     Kun käytät **Budjetti**-rivityyppiä, ohjelma päivittää ajoitetut kustannukset ja hinnat päivittämättä asiakkaalta laskutettavia sopimuskustannuksia ja -hintoja.  

9. Valitse **Kirjaa**-toiminto. Sulje sivu valitsemalla **OK**-painike.  
10. Avaa **Projektit** -luettelo.  
11. Valitse ensin ESPOO-projekti ja sitten **Projektitehtävärivit**-osassa rivi 1120. Napsauta sitten summaa hiiren kakkospainikkeella **Budjetti (kokonaiskustannus)** -kentässä. Tarkastele tietoja valitsemalla **Siirtyminen**.  

     Muutokset lisätään automaattisesti projektitehtävänumeron 1120 riville. Marianne on lisännyt viisi lisätuntia aikataulun ajoitetun työn kokonaiskustannukseen.  

12. Sulje sivu valitsemalla **Sulje**-painike.  
13. Napsauta summaa **Sopimus (kokonaiskustannus)** -kentässä hiiren kakkospainikkeella ja tarkastele tietoja valitsemalla **Siirtyminen**.  

Kun sopimuksen kokonaishintaa tarkastellaan taulukossa, vain alkuperäiset, sopimuksenmukaiset 30 tuntia ovat mukana, koska tästä on asiakkaan kanssa sovittu.  

## Projektien kopioiminen

Thomas on päässyt Tinayhtymä Oy -asiakkaan kanssa sopimukseen kymmenen neuvotteluhuoneen sisustamisesta. Sopimus muistuttaa aiempaa työtä. Tämän vuoksi aikaisemman työn kopiointi säästää aikaa.  

Valitse kopioitavat projekti- ja tehtävärivit **Kopioi projekti** -sivulla. Voit myös valita lähdeprojektin tapahtumien kopioinnin, joka luo suunnittelurivit perustuen todelliseen käyttöön, tai voit kopioida lähdeprojektin suunnittelurivit, mikä kopioi alkuperäiset suunnittelurivit uuteen työhön. Voit sitten valita suunnittelurivin tai nimiketapahtuman rivityypin, jonka haluat sisällyttää, valitsemalla vain sen, millä on merkitystä tälle uudelle työlle. Lopuksi voit valita kopioitavan projektin ja määrittää, kopioidaanko hinnat ja määrät myös.  

### Projektin kopioiminen  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Luo uusi projekti valitsemalla **Uusi**-toiminto. Anna seuraavat tiedot:  

    - **Kuvaus**: **10 kokoushuoneen sisustaminen**  
    - **Laskutusasiakkaan nro**: **20000**  

3. Valitse **Kopioi projektitehtävät kohteesta** -toiminto.  
4. Anna seuraavat tiedot **Kopioi projektitehtävät** -sivulla:  

    - **Projektinro**: **Espoo**  
    - **Ensimmäisen projektitehtävän numero**: **1000**  
    - **Lähde**: **Projektin suunnittelurivit**  
    - **Sisällytä suunnittelurivin tyyppi**: **Budjetti + laskutettava**  
    - **Viimeisen projektitehtävän numero**: **Espoo 10 kokoushuoneen sisustaminen**.  
    - Valitse **Kopioi dimensiot**- ja **Kopioi määrä** -kentät.  

5. Kopioi työ valitsemalla **OK** ja sulje sitten vahvistussivu valitsemalla **OK**.  

Kahden työn hintoja, työn tehtävärivejä ja töiden suunnittelurivejä vertaamalla näet, että tiedot on kopioitu oikein.  

## Maksujen suorittaminen osamaksuina

CRONUS on juuri ottanut hoitaakseen suuren projektin, joka kestää kokonaisen vuoden. Koska siihen täytyy kohdistaa huomattava määrä resursseja, asiakkaalta halutaan ennakkomaksu, maksu projektin puolivälissä ja lopullinen maksu projektin valmistuessa.  

### Uuden tilin luominen  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
2. Luo uusi kortti valitsemalla **Tilikartta**-sivulla **Uusi**.  
3. Lisää seuraavat tiedot uuteen **KP-tilin korttiin**:  

    - **Nro**: **40255**  
    - **Nimi**: **Projektin maksu**.  

4. Täytä **Kirjaus**-pikavälilehdessä **Yleinen tuotteen kirjausryhmä** -kenttä, valitse **Palvelut**. Sulje sivu.  
5. Valitse **Tilikartta**-sivulla ensin **Projektin nro 40255 maksu** ja sitten **Sisennä tilikartta** -toiminto. Vahvista valitsemalla **Kyllä**.  

Seuraavissa ohjeissa neuvotaan, miten luot uuden projektin, asetat hinnoittelun ja määrittelet osamaksuvaihtoehdon. Projektitehtäväriveillä voit luoda tiettyjä rivejä, jotka on tarkoitettu yksinomaan osamaksuja varten. Kaikki projektin valmistuneet työt, jotka on lisätty aikatauluun, lisätään käyttöriveille. Jokaisen suunnittelurivin maksutehtävärivin rivityyppi on **Laskutettava**. Se tarkoittaa, että asiakasta tullaan laskuttamaan. Syötä uusi rivi ennakkomaksulle. Käytön tehtäväriveillä voit lisätä tässä projektissa käytettyjen, aikataulua pidentävien nimikkeiden ja resurssien tietoja. Tällaisia nimikkeitä ja resursseja ovat esimerkiksi projektissa käytetyt työntekijätunnit ja nimikkeet.  

### Osamaksujen käyttäminen  

1. Luo uusi projekti.  
2. Täytä seuraavat tiedot **projekti**-korttiin:  

    - **Kuvaus**: **Vastaanottoalueen uusiminen**  
    - **Laskutusasiakkaan nro**: **30000**  
    - **Projektin kirjausryhmä**: **As. määr.**  
    - **KET-menetelmä**: **Kustannusarvo**  

3. Valitse projektikortissa **Hinnat**-toiminto ja valitse sitten **Resurssi**-toiminto. Lisää seuraavat tiedot:  

    - **Koodi**: **Marianne**  
    - **Yksikköhinta**: **10**  

     Sulje sivu.  

4. Lisää **Projekti**-kortin **Tehtävät**-osassa projektitehtävän rivin seuraavassa taulukossa kuvatulla tavalla:  

    | Rivi | Projektitehtävän nro | Kuvaus          | Projektitehtävätyyppi |
    |------|--------------|----------------------|---------------|
    | 1    | 1000         | Maksu - ennakkomaksu | Kirjaus       |
    | 2    | 2000         | Käyttö                | Kirjaus       |
    | 3    | 3000         | Maksu - välimaksu     | Kirjaus       |
    | 4    | 4000         | Maksu - loppumaksu | Kirjaus       |

5. Valitse ensin tehtävä 1000 ja sitten **Projektin suunnittelurivit** -toiminto.  

6. Luo suunnittelurivi, jossa on seuraavat tiedot:  

    | Rivi | Rivityyppi | Suunnittelupäivämäärä  | Tyyppi        | Ei.   | määrä | Yksikköhinta |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Laskutettava  | (kuluvan päivän päivämäärä) | KP-tili | 40255 | 1        | 5000       |

     Sulje sivu.  

7. Valitse ensin tehtävä 2000 ja sitten **Projektin suunnittelurivit** -toiminto.  

8. Luo suunnittelurivi, jossa on seuraavat tiedot:

    | Rivi | Rivityyppi | Suunnittelupäivämäärä  | Tyyppi     | Ei.    | määrä |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Budjetti    | (kuluvan päivän päivämäärä) | Resurssi | Marianne | 120      |
    | 2    | Budjetti    | (kuluvan päivän päivämäärä) | Nimike     | 70104  | 10       |

     Sulje sivu. Suunnitellut summat näkyvät päivitettyinä **Projektitehtävärivit**-sivulla.  

9. Valitse ensin tehtävä 32000 ja sitten **Projektin suunnittelurivit** -toiminto.  

10. Luo suunnittelurivi, jossa on seuraavat tiedot:

    | Rivi | Rivityyppi | Suunnittelupäivämäärä   | Tyyppi        | Ei.   | määrä | Yksikköhinta |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Laskutettava  | (tuleva päivämäärä) | KP-tili | 40255 | 1        | 5000       |

     Sulje sivu.  

11. Luo vastaava suunnittelurivi työtehtävälle 4000.  

 Kun tehtävä- ja suunnittelurivit on nyt lisätty, Thomas luo laskun ensimmäistä maksua varten. Nämä toimet tehdään projektitehtävän riveiltä, jotta laskussa on varmasti vain ensimmäisen maksun rivit. Voit avata myyntitilauksen suunnitteluriveiltä tai tehtäväriveiltä.  

### Luo lasku  

1.  Valitse **Projektitehtävärivit**-sivulla ensin rivi 1000 ja sitten **Luo myyntilasku** -toiminto.  
2.  Määritä **Luo myyntilasku** -sivulla kuluva päivämäärä kirjauspäivämääräksi, määritä **Tehtäväkohtainen** ja valitse **OK**, jos haluat luoda oletustiedot sisältävän laskun. Sulje vahvistussivu valitsemalla **OK**.  
3.  Valitse **Myyntilasku/hyvityslasku**-toiminto. Myyntilaskussa näkyy, että vain ennakkomaksu on mukana laskussa. Voit nyt lähettää tämän asiakkaalle sopimuksen mukaisesti.  

## Seuraavat vaiheet

 Tämä vaihekuvaus on ohjannut sinut läpi tiettyjen perusvaiheiden töiden [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman parissa. Olet oppinut kuinka luodaan uusi työ, kuinka työ kopioidaan ja kuinka maksuja käsitellään. Olet myös nähnyt esityksen siitä, miten voit luoda laskuja ja seurata tunteja.  

## Katso myös

 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
 [Projektinhallinnan määrittäminen](projects-setup-projects.md)  
 [Resurssien käyttäminen](projects-how-use-resources.md)  
 [Etenemisen ja tehokkuuden valvonta](projects-how-monitor-progress-performance.md)  
 [Projektien laskuttaminen](projects-how-invoice-jobs.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
