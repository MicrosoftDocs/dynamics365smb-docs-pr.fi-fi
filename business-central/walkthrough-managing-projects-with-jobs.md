---
title: Vaihekuvaus - Projektinhallinta Projektien avulla
description: 'Tässä opastuksessa esitellään töiden projektinhallintaominaisuudet, joiden avulla voit ajoittaa yrityksesi resurssien käytön.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 05/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="walkthrough-managing-projects"></a>Vaihekuvaus: Projektinhallinta

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Tässä vaihekuvauksessa esitellään projektinhallinnan toimintoja. Projektien avulla voidaan laatia yrityksen resurssien käyttöön liittyviä aikatauluja ja seurata tietyn projektin resursseihin liittyviä kustannuksia. Projekteissa kuluu esimerkiksi työntekijöiden työtunteja, koneiden käyttötunteja ja varastonimikkeitä, joita täytyy seurata projektin edetessä.  

Tässä vaihekuvauksessa käsitellään uuden projektin määrittämistoimia ja siihen liittyviä tehtäviä:

- Kiinteiden hintojen käsitteleminen
- Maksujen suorittaminen osamaksuina
- Projektien laskujen kirjaaminen
- Kopioi projektit

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta

 Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

### <a name="setting-up-a-project"></a>Projektin määrittäminen

Kun budjettirakenne on määritetty projekteille, projektin luominen on yksinkertaista. Tässä vaihekuvauksessa käsitellään seuraavia vaiheita:  

- Projektin tehtävärivien ja suunnittelurivien määrittäminen  
- Projektikohtaisten hintojen luominen nimikkeille, resursseille ja KP-tileille  
- Projektin laskuttaminen asiakkailta.  

### <a name="handling-fixed-prices"></a>Kiinteiden hintojen käsitteleminen

 Kiinteiden hintojen lisäksi käsitellään myös sellaisia palveluiden tai tavaroiden hintoja, joista on sovittu ennalta asiakkaiden kanssa. Tässä ohjeessa on tietoja seuraavista toiminnoista:  

- Katso, kuinka sopimuksen ja laskun arvot määritetään  
- Salli ylimääräisen (laskuttamattoman) työn lisääminen aikatauluun.  

### <a name="copying-a-project"></a>Projektien kopioiminen

 Tässä vaihekuvauksessa keskitytään koko projektin tai sen osa kopioimiseen, mikä vähentää tietojen manuaalisen syöttämisen tarvetta ja parantaa tarkkuutta.

- projektin osan kopioiminen uuteen projektiin  
- Projektikohtaisten hintojen kopioiminen  
- Projektin suunnittelurivien kopioiminen.  

### <a name="making-payment-by-installment"></a>Maksujen suorittaminen osamaksuina

 Kun suuri, kallis projekti kestää pitkään, asiakas tekee usein yrityksen kanssa sopimuksen maksuerien maksamiseksi. Tämä esimerkki näyttää, miten maksutapa määritellään osamaksuina, ja se kattaa seuraavat asiat:  

- Osamaksun luominen projektille.  
- Maksujen laskuttaminen asiakkailta.  
- Projektin käyttötilille projektissa, joka on määritetty osamaksuille.  

## <a name="roles"></a>Roolit

 Tässä vaihekuvauksessa on seuraaviin rooleihin liittyviä tehtäviä:  

- Projektipäällikkö  
- Projektitiimin jäsen  

## <a name="prerequisites"></a>Vaatimukset

 Ennen tämän vaihekuvauksen tehtävien suorittamista, sinun tulee:  

- Asenna CRONUS-esittelytietokanta.
- Luo esimerkkitietoja noudattamalla seuraavan osan toimintaohjeita.  

## <a name="story"></a>Taustatietoja

Tässä vaihekuvauksessa keskitytään CRONUSiin, joka on läpitunkeva muotoilu- ja konsultointiyritys, joka suunnittelee ja sopii uusiin infrastruktuureihin. Esim. neuvottelusalit ja toimistot, joissa on huonekaluja, asustetarvikkeita ja varastoyksiköitä. Sen useimmat työt projektisuuntautuneita. Thomas, CRONUSin projektipäällikkö, saa projektin avulla yleiskäsityksen kustakin CRONUSin käynnistämästä ja valmistuneesta tehtävästä. Thomas järjestää tavallisesti kaupat asiakkaiden kanssa ja lisää projektin ydintiedot, joita olivat tehtävä- ja suunnittelurivit sekä hinnat, [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Thomas toteaa, että tietojen luominen, ylläpitäminen ja tarkistaminen on suoraviivaista. Thomas pitää myös tavasta, jolla [!INCLUDE[prod_short](includes/prod_short.md)] mahdollistaa projektien kopioinnin ja maksamisen osamaksuina.

 Projektitiimin jäsen Marianne, joka työskentelee Thomasin alaisena, on projektin päivittäinen vastuuhenkilö. Marianne kirjoittaa teknikkojen työt jokaiseen tehtävään, kirjaa heidän käyttämänsä tavarat ja heille aiheutuneet kustannukset.  

## <a name="preparing-sample-data"></a>Esimerkkitietojen valmisteleminen

Valmistaudu tähän vaihekuvaukseen lisäämällä Mariannen resurssina.  

### <a name="to-prepare-the-sample-data"></a>Esimerkkitietojen valmisteleminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssit** ja valitse sitten vastaava linkki.  
2. Luo uusi resurssin kortti valitsemalla **Uusi**-toiminto.  
3. Anna **Yleiset**-pikavälilehdessä seuraavat tiedot:  

    - **Nro:**: **Marianne**  
    - **Nimi**: **Marianne**  
    - **Tyyppi**: **Henkilö**  

4. Valitse **Perusmittayksikkö** -kenttä ja avaa sitten **Resurssin mittayksikkö** -sivu valitsemalla **Uusi**. Valitse **Tyyppi**-kentässä **Tunti**.  
5. Lisää seuraavat tiedot **Laskutus**-pikavälilehteen:  

    - **Välitön yksikkökustannus**: **5**  
    - **Välillinen kustannus**: **4**  
    - **Yksikkökustannus**: **10**  
    - **Yleinen tuotteen kirjausryhmä**: **Palvelut**  
    - **Tuotteen ALV-kirjausryhmä**: **ALV 25**  

6. Sulje sivu.

Seuraavassa toimenpiteessä luodaan projektipäiväkirjan erä Mariannea varten, jotta hän voi kirjata käyttönsä.  

### <a name="to-create-a-project-journal-batch"></a>Projektipäiväkirjaerän luominen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse **Projektipäiväkirja**-sivulla **Erän nimi**-kenttä. **Projektipäiväkirjan erät** -sivu avautuu.  
3. Valitse **Uusi**-toiminto, jos haluat luoda uuden rivin, jolla ovat seuraavat tiedot:  

    - **Nimi**: **Marianne**  
    - **Kuvaus**: **Marianne**  
    - **Nrosarja**: **PPVK-YLEIN**.  

4. Tallenna muutokset valitsemalla **OK**-painike.

## <a name="setting-up-a-project-1"></a>Projektin määrittäminen

Tässä skenaariossa CRONUS on voittanut sopimuksen Progressive Home Furnishings -yrityksen kanssa, jonka kanssa on päästy sopimukseen neuvottelusalin ja ruokasalin suunnittelemisesta. Asiakkaan tilat ovat Yhdysvalloissa, ja projektissa tarvitaan erityistä ohjelmistoa. Projektipäällikkö solmii sopimuksen asiakkaan kanssa ja sopimuksen keston kattava projekti luodaan.  

### <a name="to-set-up-a-project"></a>Projektin määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
2. Luo uusi kortti valitsemalla **Uusi**-toiminto.  
3. Anna **Yleiset**-pikavälilehdessä seuraavat tiedot:  

    - **Kuvaus**: **Konsultointi neuvottelusalin sisustuksesta**  
    - **Laskutusasiakkaan nro**: **01445544**  

4. Lisää seuraavat tiedot **Kirjaus**-pikavälilehteen:  

    - **Tila**: **Suunnittelu**  
    - **Projektin kirjausryhmä**: **As. määr.**  
    - **KET-menetelmä**: **Kustannusarvo**  

5. Kirjoita kuluvan päivän päivämäärä **Kesto**-pikavälilehden **Aloituspvm**- ja **Lopetuspvm**-kenttiin. Nämä päivämäärät helpottavat valuuttamuunnosten tekemistä, kun projekti laskutetaan.  
6. Vahvista **Ulkomaankauppa**-pikavälilehdessä, että valuuttakoodi on **USD**. Jos **Laskun valuutan koodi** -kentässä valitaan USD, projekti laskutetaan Yhdysvaltain dollareina ja suunnitellaan vain CRONUSin paikallisen valuutan mukaan.  

 Asiakkaiden hinnoittelu voidaan mukauttaa projektikohtaiseksi määritettyjen sopimusten mukaisesti. Seuraavassa toimenpiteessä projektipäällikkö määrittää kustannukset Mariannen ajasta, määrittää tarvittavan ohjelmiston hinnan ja lisää matkakustannukset, jotka asiakas on suostunut maksamaan.  

### <a name="to-customize-pricing"></a>Mukauta hinnoittelu

1. Valitse **projektikortissa** **Resurssi**-toiminto.  
2. Lisää seuraavat tiedot **Projektiresurssien hinnat** -sivulle:  

    - **Koodi**: **Marianne**  
    - **Yksikköhinta**: **20**  

3. Sulje sivu.  
4. Valitse **Nimike**-toiminto.  
5. Lisää seuraavat tiedot ja mukautettu hinta **Projektinimikkeiden hinnat** -sivulle:  

    1. **Nimikkeen nro**: **80201 (Grafiikkaohjelma)**  
    2. **Yksikköhinta**: **200**  

6. Sulje sivu.  
7. Valitse **KP-tili**-toiminto.  
8. Anna **Projektin kirjanpitotilin hinnat** -sivulla seuraavat tiedot ja matkan kustannus, jonka asiakas on luvannut maksaa, plus 25 %:  

    1. **KP-tili**: **8430 (Matka)**  
    2. **Yksikkökustannustekijä**: **1,25**.  

9. Sulje sivu.  

 Projektin määrittämisen viimeisissä vaiheissa lisätään projektin tehtävät sekä kunkin tehtävän suunnittelurivi. Nämä suunnittelurivit määrittävät, mitä asiakkaalta laskutetaan.  

### <a name="to-add-project-tasks"></a>Projektitehtävien lisääminen

1. Valitse uuden projektin **Projekti**-kortissa **Projektitehtävärivit**-toiminto.  
2. Seuraavassa taulukossa kuvaillaan tiedot, jotka tulisi syöttää kenttiin.  

    |Projektitehtävän nro|Kuvaus|Projektitehtävän tyyppi|  
    |------------------|---------------------------------------|-------------------|  
    |1 000|Konsulttiapua salin sisustukseen|Alku-Yhteensä|  
    |1010|Konsultointitapaaminen asiakkaan kanssa|Kirjaus|  
    |1020|Kehittäminen|Kirjaus|  
    |1090|Konsultointi yhteensä|Loppusumma|  

3. **Sisennä projektitehtävät** -toiminnon valinta osoittaa, että jotkin tehtävät ovat muiden tehtävien alaluokkia.  

Suunnittelurivi voi olla jokin seuraavista tyypeistä:  

- **Budjetti**: Lisätty aikatauluun, mutta ei laskutettu.  
- **Laskutettava**: Laskutettu mutta ei lisätty aikatauluun.  
- **Sekä budjetti että laskutettava**: laskutettu ja lisätty aikatauluun.  

Tässä vaihekuvauksessa projektipäällikön käytössä on **Sekä budjetti että laskutettava**. Hän luo tehtävälle 1010 kolme suunnitteluriviä ja tehtävälle 1020 kaksi suunnitteluriviä.  

### <a name="to-create-planning-lines"></a>Luo suunnittelurivit

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

## <a name="calculating-remaining-usage"></a>Jäljellä olevan käytön laskeminen

Marianne, projektiryhmän jäsen, on tehnyt työtä projektissa jonkin aikaa ja haluaa rekisteröidä omat tuntinsa ja käytön projektissa. Työmäärä ja käyttö eivät ole ylittäneet asiakkaan kanssa sovittua määrää. Marianne laskee **Laske jäljellä oleva käyttö** -eräajon avulla projektin jäljellä olevan käytön projektipäiväkirjaan. Erätyö laskee kullekin tehtävälle nimikkeiden, resurssien ja kirjanpitokustannusten suunnitellun käytön ja projektitapahtumiin kirjatun todellisen käytön välisen eron. Jäljellä oleva käyttö tulee näkyviin projektipäiväkirjaan, josta Marianne voi kirjata sen.  

### <a name="to-calculate-remaining-usage"></a>Jäljellä olevan käytön laskeminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Avaa **Projektipäiväkirjan erät** -luettelo **Projektipäiväkirja**-sivun **Erän nimi** -kentässä. Valitse **Marianne**-projektipäiväkirjan erä.  
3. Valitse **Laske jäljellä oleva käyttö** -toiminto.  
4. Valitse **Laske projektin jäljellä oleva käyttö** -sivun **Projektitehtävä**-pikavälilehdessä **Projektin nro** -kenttä ja valitse sitten soveltuva projektin numero, tyypillisesti projekti J00010.  
5. Kirjoita **Vaihtoehdot**-pikavälilehden **Asiakirjan nro** -kenttään **J00001**. Tämä tieto helpottaa kirjauksen myöhempää jäljittämistä.  
6. Määritä kirjauspäivämääräksi kuluva päivä.  
7. Valitse **OK**-painike. Tämä toiminto luo projektipäiväkirjanrivit, jotka perustuvat Thomasin luomiin suunnitteluriveihin.  
8. Valitse vahvistussivulla **OK**-painike. Luodut rivit lisätään projektipäiväkirjaan.  
9. Varmista, että kaikki asiakirjan numerot ovat J00001. Valitse sitten **Kirjaa**-toiminto. Vahvista kirjaus valitsemalla **Kyllä**.  

Rivit kirjataan.  

## <a name="creating-and-posting-a-project-sales-invoice"></a>Projektin myyntilaskun luominen ja kirjaaminen

Seuraavaksi Marianne voi luoda uuden laskun koko projektia tai projektin osaa varten. Marianne voi myös liittää laskun saman asiakkaan toiseen, samaa projektia koskevaan laskuun. Tällöin Marianne laskuttaa koko projektista, koska projekti on nyt valmis.  

### <a name="to-create-a-project-sales-invoice"></a>Projektin myyntilaskun luominen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
2. Valitse ensin aiemmin luotu projekti ja sitten **Luo projektin myyntilasku** -toiminto.  
3. Tyhjennä **Projektitehtävä**-pikavälilehden **Projektitehtävänro**-kentässä kaikki suodattimet, jotta työ voidaan laskuttaa. Valitse **Projektin nro** -kentässä soveltuva projekti.  
4. Anna **Vaihtoehdot**-pikavälilehdessä kirjauspäivämäärä ja määritä, haluatko luoda yhden laskun tehtävää kohti vai yhden laskun kaikille tehtäville.  
5. Luo lasku valitsemalla **OK**-painike ja valitse sitten **OK**-painike vahvistussivulla.  

Kun Tricia on luonut laskun, hän voi käyttää sitä esimerkiksi **Myyntitilausten käsittelijän** roolikeskuksessa.

### <a name="to-post-a-new-sales-invoice"></a>Uuden myyntilaskun kirjaaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.  
2. Avaa sen asiakkaan lasku, jonka asiakkaan numero on 01445544. Suunnitteluriveiltä lisätyt tiedot tulevat näkyviin.  
3. Valitse **Kirjaa**-toiminto. Vahvista kirjaus valitsemalla **Kyllä**.  

### <a name="to-view-the-posted-invoice"></a>Kirjatun laskun tarkasteleminen

1. Avaa ensin projekti ja sitten **Projektin suunnittelurivit** -toiminto.  
2. Valitse ensin jokin laskutettu suunnittelurivi ja sitten **Myyntilasku/hyvityslasku**-toiminto.
3. Valitse **Projektin laskut** -sivulla **Avaa myyntilasku/hyvityslasku** -toiminto.  

Mariannella on kysyttävää tähän projektiin liittyvistä hinnoista, kustannuksista ja tuotoista, joten hän arvioi näitä tietoja **Tilastot**-sivulla.  

### <a name="to-open-the-statistics-page"></a>Tilastot-sivun avaaminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
2. Valitse **Tilastot**-toiminto. Voit tarkastella yksityiskohtaisia tietoja projektihinnoista, kustannuksista ja paikallisista ja ulkomaisista valuuttojen voitoista.  
3. Valitse **Sulje**-painike **Projektin tilastot** -sivun sulkemiseksi.  

## <a name="handling-fixed-prices-1"></a>Kiinteiden hintojen käsitteleminen

CRONUSin kanssa on tehty sopimus kokoushuoneiden määrittämiseksi. Projektipäällikkö Thomas tarvitsee hyvän yleiskäsityksen projektin edellyttämistä tehtävistä sekä kuhunkin tehtävään liittyvistä budjetoiduista ja kertyneistä kustannuksista. Tarkoitus on myös selvittää projektin sopimuksenmukainen kokonaishinta sekä tähän mennessä laskutettu summa. Asiakkaan kanssa on päästy sopimukseen projektin kiinteästä hinnoittelusta.  

### <a name="to-manage-fixed-pricing-in-projects"></a>Kiinteän hinnoittelun hallinta projekteissa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
2. Valitse ensin **Espoo**-projektinumero ja sitten **Projektitehtävärivit**- toiminto.  
3. Valitse rivi 1120 ja valitse **Budjetti (kokonaiskustannus)** -kentässä hiiren kakkospainikkeella **Siirtyminen**.  

     Projektin suunnittelurivejä tarkasteltaessa päädytään siihen, että myös Mariannea tarvitaan 30 tunniksi projektin tässä vaiheessa. Asiakkaan kanssa sovitaan kiinteästä hinnasta.  

4. Valitse **Projektitehtävärivit**-sivulla ensin rivi 1120 ja sitten **Projektin suunnittelurivit** -toiminto. Luo suunnittelurivi, jossa on seuraavat tiedot:  

    | Rivi | Rivityyppi | Tyyppi        | Ei.   | määrä |
    |------|-----------|-------------|-------|----------|
    | 1    | Sekä budjetti että laskutettava  | Resurssi | Marianne | 30 |

     Sulje sivu.  
5. Napsauta **Budjetti (kokonaiskustannus)** -kenttää hiiren kakkospainikkeella ja valitse **Siirtyminen** uudelleen **Projektitehtävärivit**-sivulla. Tarkastele muutoksia aikatauluun. Kuten huomaat, aikatauluun on lisätty 30 tuntia.  
6. Sulje sivut.  

Kun Marianne on lisätty aikatauluun tämän tehtävärivin osalta, hän työskentelee projektissa 25 tuntia. Nämä tunnit voidaan lisätä projektipäiväkirjaan.  

### <a name="to-enter-hours-in-a-project-journal"></a>Tuntien lisääminen projektipäiväkirjaan

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Lisää seuraavat tiedot uudelle riville:  

    - **Rivityyppi**: **(tyhjä)**  
    - **Kirjauspvm**: **(kuluva päivämäärä)**.  
    - **Asiakirjan nro**:**J00002**  
    - **Projektinro**: **Espoo**  
    - **Projektitehtävän nro**: **1120**  
    - **Tyyppi**: **Resurssi**  
    - **Nro:**: **Marianne**  
    - **Määrä**: **25**  

3. Valitse **Kirjaa**-toiminto.  

     Muutamaa päivää myöhemmin Marianne työskentelee vielä 10 tuntia, ja on nyt työskennellyt 35 tuntia. Koska asiakkaan kanssa on sovittu vain 30 tunnista, tunneista vain viisi laskutetaan asiakkaalta. Marianne lisää muut viisi tuntia aikatauluun manuaalisesti.  

4. Valitse **Projektipäiväkirja**-sivulla **Laske jäljellä oleva käyttö** -toiminto.  
5. Lisää seuraavat tiedot **Laske projektin jäljellä oleva käyttö** -sivun **Asetukset**-pikavälilehteen:  

    - **Asiakirjan nro**:**J00003**  
    - **Kirjauspvm**: **(kuluva päivämäärä)**  

6. Lisää seuraavat tiedot **Projektitehtävä**-pikavälilehteen:  

    - **Projektinro**: **Espoo**  
    - **Projektitehtävän nro**: **1120**  

7. Suorita laskenta valitsemalla **OK**.

    Mariannen työpäivässä on jäljellä viisi tuntia. **Rivityyppi**-kenttä on tyhjä sen merkiksi, että vain käyttö pysyy kirjattuna, koska työ on jo ajoitettu.  

8. Luo **Projektipäiväkirjan erät** -ikkunassa uusi rivi, jolla on seuraavat tiedot: Varmista, että projektinumerot ovat järjestyksessä seuraavina niistä, joita olet jo käyttänyt:  

    - **Rivityyppi**: **Budjetti**  
    - **Projektinro**: **Espoo**  
    - **Projektitehtävän nro**: **1120**  
    - **Tyyppi**: **Resurssi**  
    - **Nro:**: **Marianne**  
    - **Määrä**: **5**  

     Jos käytät **Budjetti**-rivityyppiä, ohjelma päivittää ajoitetut kustannukset ja hinnat päivittämättä asiakkaalta laskutettavia sopimuskustannuksia ja -hintoja.  

9. Valitse **Kirjaa**-toiminto. Sulje sivu valitsemalla **OK**-painike.  
10. Avaa **Projektit**-luettelo.  
11. Valitse ensin ESPOO-projekti ja sitten **Projektitehtävärivit**-osassa rivi 1120. Napsauta sitten summaa hiiren kakkospainikkeella **Budjetti (kokonaiskustannus)** -kentässä. Tarkastele tietoja valitsemalla **Siirtyminen**.  

     Muutokset lisätään automaattisesti projektitehtävänumeron 1120 riville. Marianne on lisännyt viisi lisätuntia aikataulun ajoitetun työn kokonaiskustannukseen.  

12. Sulje sivu valitsemalla **Sulje**-painike.  
13. Napsauta summaa **Sopimus (kokonaiskustannus)** -kentässä hiiren kakkospainikkeella ja tarkastele tietoja valitsemalla **Siirtyminen**.  

Kun sopimuksen kokonaishintaa tarkastellaan taulukossa, vain alkuperäiset, sopimuksenmukaiset 30 tuntia ovat mukana, koska tästä on asiakkaan kanssa sovittu.  

## <a name="copying-projects"></a>Projektien kopioiminen

Thomas on päässyt Tinayhtymä Oy -asiakkaan kanssa sopimukseen kymmenen neuvotteluhuoneen sisustamisesta. Sopimus muistuttaa aiempaa projektia. Tämän vuoksi aikaisemman projektin kopiointi säästää aikaa.  

Valitse kopioitavat projekti- ja tehtävärivit **Kopioi projekti** -sivulla.

- Kopioi lähdeprojektitapahtumat, kun haluat luoda todelliseen käyttöön perustuvia suunnittelurivejä.
- Kopioi lähdeprojektin suunnittelurivit, jotta alkuperäiset suunnittelurivit voidaan kopioida uuteen projektiin.

Voit sitten valita suunnittelurivin tai nimiketapahtuman rivityypin, jonka haluat sisällyttää, valitsemalla vain sen, millä on merkitystä tälle uudelle projektille. Lopuksi voit valita kopioitavan projektin ja määrittää, kopioidaanko hinnat ja määrät myös.  

### <a name="to-copy-a-project"></a>Projektin kopiointi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
2. Luo uusi projekti valitsemalla **Uusi**-toiminto. Lisää seuraavat tiedot:  

    - **Kuvaus**: **10 kokoushuoneen sisustaminen**  
    - **Laskutusasiakkaan nro**: **20000**  

3. Valitse **Kopioi projektitehtävät kohteesta** -toiminto.  
4. Anna seuraavat tiedot **Kopioi projektitehtävät** -sivulla:  

    - **Projektinro**: **Espoo**  
    - **Ensimmäisen projektitehtävän numero**: **1000**  
    - **Lähde**: **Projektin suunnittelurivit**  
    - **Sisällytä suunnittelurivin tyyppi**: **Budjetti + laskutettava**  
    - **Viimeisen projektitehtävän numero**: **Espoo 10 kokoushuoneen sisustaminen**  
    - Valitse **Kopioi dimensiot**- ja **Kopioi määrä** -kentät.  

5. Kopioi projekti valitsemalla **OK** ja sulje sitten vahvistussivu valitsemalla **OK**.  

Kahden työn hintoja, projektin tehtävärivejä ja projektin suunnittelurivejä vertaamalla nähdään, että tiedot on kopioitu oikein.  

## <a name="making-payments-by-installments"></a>Maksujen suorittaminen osamaksuina

CRONUS on juuri ottanut hoitaakseen suuren projektin, joka kestää kokonaisen vuoden. Koska siihen täytyy kohdistaa huomattava määrä resursseja, asiakkaalta halutaan ennakkomaksu, maksu projektin puolivälissä ja lopullinen maksu projektin valmistuessa.  

### <a name="to-set-up-a-new-account"></a>Uuden tilin luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
2. Luo uusi kortti valitsemalla **Tilikartta**-sivulla **Uusi**.  
3. Lisää seuraavat tiedot uuteen **KP-tilin korttiin**:  

    - **Nro**: **40255**  
    - **Nimi**: **Projektin maksu**  

4. Täytä **Kirjaus**-pikavälilehdessä **Yleinen tuotteen kirjausryhmä** -kenttä, valitse **Palvelut**. Sulje sivu.  
5. Valitse **Tilikartta**-sivulla ensin **Projektin nro 40255 maksu** ja sitten **Sisennä tilikartta** -toiminto. Vahvista valitsemalla **Kyllä**.  

Seuraavissa ohjeissa neuvotaan, miten luot uuden projektin, asetat hinnoittelun ja määrittelet osamaksuvaihtoehdon. Projektitehtäväriveillä voidaan luoda yksinomaan osamaksuja varten tarkoitettuja rivejä. Kaikki projektin valmistuneet työt, jotka on lisätty aikatauluun, lisätään käyttöriveille. Jokaisen suunnittelurivin maksutehtävärivin rivityyppi on **Laskutettava**. Se tarkoittaa, että asiakasta tullaan laskuttamaan. Syötä uusi rivi ennakkomaksulle. Käytön tehtäväriveillä voit lisätä tässä projektissa käytettyjen, aikataulua pidentävien nimikkeiden ja resurssien tietoja. Tällaisia nimikkeitä ja resursseja ovat esimerkiksi projektissa käytetyt työntekijätunnit ja nimikkeet.  

### <a name="to-make-a-payment-by-installment"></a>Osamaksujen käyttäminen

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

4. Lisää **Projekti**-kortin **Tehtävät**-osassa projektitehtävän rivit seuraavassa taulukossa kuvatulla tavalla:  

    | Rivi | Projektitehtävän nro | Kuvaus          | Projektitehtävän tyyppi |
    |------|--------------|----------------------|---------------|
    | 1    | 1 000         | Maksu - ennakkomaksu | Kirjaus       |
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
    | 2    | Budjetti    | (kuluvan päivän päivämäärä) | Vaihtoehto     | 70104  | 10       |

     Sulje sivu. Suunnitellut summat näkyvät päivitettyinä **Projektitehtävärivit**-sivulla.  

9. Valitse ensin tehtävä 32000 ja sitten **Projektin suunnittelurivit** -toiminto.  

10. Luo suunnittelurivi, jossa on seuraavat tiedot:

    | Rivi | Rivityyppi | Suunnittelupäivämäärä   | Tyyppi        | Ei.   | määrä | Yksikköhinta |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Laskutettava  | (tuleva päivämäärä) | KP-tili | 40255 | 1        | 5000       |

     Sulje sivu.  

11. Luo vastaava suunnittelurivi projektitehtävälle 4000.  

 Kun tehtävä- ja suunnittelurivit on nyt lisätty, Thomas luo laskun ensimmäistä maksua varten. Nämä toimet tehdään projektitehtävän riveiltä, jotta laskussa on varmasti vain ensimmäisen maksun rivit. Voit avata myyntitilauksen suunnitteluriveiltä tai tehtäväriveiltä.  

### <a name="to-create-an-invoice"></a>Luo lasku

1. Valitse **Projektitehtävärivit**-sivulla ensin rivi 1000 ja sitten **Luo myyntilasku** -toiminto.  
2. Määritä **Luo myyntilasku** -sivulla kuluva päivämäärä kirjauspäivämääräksi, määritä **Tehtäväkohtainen** ja valitse **OK**, jos haluat luoda oletustiedot sisältävän laskun. Sulje vahvistussivu valitsemalla **OK**.  
3. Valitse **Myyntilasku/hyvityslasku**-toiminto. Myyntilaskussa näkyy, että vain ennakkomaksu on mukana laskussa. Voit nyt lähettää tämän asiakkaalle sopimuksen mukaisesti.  

## <a name="summary"></a>Yhteenveto

Tämä vaihekuvaus on ohjannut sinut läpi tiettyjen perusvaiheiden projektien [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman parissa. Olet oppinut kuinka luodaan uusi projekti, kuinka projekti kopioidaan ja kuinka maksuja käsitellään. Olet myös nähnyt esityksen siitä, miten voit luoda laskuja ja seurata tunteja.  

## <a name="see-also"></a>Katso myös

 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
 [Projektinhallinnan määrittäminen](projects-setup-projects.md)  
 [Resurssien käyttäminen](projects-how-use-resources.md)  
 [Edistymisen ja suorituskyvyn valvonta](projects-how-monitor-progress-performance.md)  
 [Projektien laskutus](projects-how-invoice-jobs.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
