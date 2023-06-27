---
title: Talousraporttien luomiminen taloustietojen ja tililuokkien avulla
description: 'Kuvailee, kuinka talousraporttien avulla luodaan erilaisia ​​näkymiä ja raportteja taloudellisen suorituskyvyn tietojen analysointia varten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories" />Taloushallinnon raportoinnin valmisteleminen taloustietojen ja tililuokkien avulla

Talousraporttien avulla saat tietoja tilikarttaan sisältyvistä kirjanpitotiedoista. Taloudelliset raportit analysoivat kirjanpitotilien lukuja ja vertaavat pääkirjanpidon tapahtumia budjettitapahtumiin. Tulokset näkyvät roolikeskuksen kaavioissa ja raporteissa, kuten kassavirtakaaviossa ja Tuloslaskelma- ja Tase-raporteissa.

Voit käyttää näitä kahta raporttia esimerkiksi liiketoimintajohtajan ja kirjanpitäjän roolikeskusten **Tilinpäätökset**-toiminnon avulla.  

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää taloudellisen raportin malleja, joita voi käyttää heti. Voit myös määrittää omia rivejä ja sarakkeita määrittääksesi vertailtavat luvut. Voit esimerkiksi luoda taloudellisia raportteja katteen laskemista varten osastojen tai asiakasryhmien kaltaisille dimensioille. Voit luoda niin monta mukautettua rahoituslaskelmaa kuin haluat.  

Taloudellisten raporttien määrittäminen vaatii tilikartan taloustietojen ymmärtämistä. Voit esimerkiksi tarkastella KP-tapahtumien prosenttiosuuksia budjettitapahtumista, mutta se edellyttää, että olet luonut budjetteja. Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).

## <a name="financial-reports" />Talousraportit

Taloudelliset raportit järjestävät tilikarttasi tilejä tavoilla, jotka tekevät tiedoista helpommin esitettäviä. Voit määrittää eri asetteluja määrittääksesi tiedot, jotka haluat suodattaa tilikartasta. Taloudelliset raportit tarjoavat paikan laskelmille, joita ei voi tehdä suoraan tilikartassa. Voit esimerkiksi luoda tiliryhmien välisummia ja sisällyttää ne muihin summiin. Toinen esimerkki on laskea katteita osastojen tai asiakasryhmien kaltaisille dimensioille. Lisäksi pääkirjanpidon tapahtumia ja budjettitapahtumia voi suodattaa esimerkiksi nettomuutoksen tai veloitussumman perusteella.

Voit myös verrata kahta tai useampaa taloudellista raporttia ja sarakemääritelmiä käyttämällä kaavoja, jotta voit tehdä seuraavat asiat:

* luoda mukautettuja raportteja
* Luo niin monta talousraporttia kuin tarvitset, joista jokaisella on yksilöllinen nimi.
* määrittää useita raportin asetteluita sekä tulostaa raportit käyttäen nykyisiä lukuja.

## <a name="gl-account-categories" />KP-tilin luokat

KP-tililuokkien avulla voit muuttaa rahoituslaskelmien asettelua. Kun olet esimerkiksi määrittänyt tililuokat **KP-tililuokat** -sivulla, voit valita **Luo talousraportit** -toiminnon ja päivittää talousraportin perustana olevat talousraportit. Kun seuraavan kerran suoritat toisen näistä raporteista, esimerkiksi **Tase**-raportin, uudet kokonaissummat ja korvaustapahtumat lisätään.

> [!NOTE]
> Ylimmän tason tililuokat, kuten **Velat**-solmu, ovat kiinteitä, eikä niitä voi lisätä. Voit kuitenkin poistaa ja lisätä tililuokkia alemmilla tasoilla ja muuttaa niiden rakennetta määrittääksesi, miten liittyvä talousraportti näkyy raporteissa.
>
> Sinun tulisi luoda ja jäsentää omat alemman tason KP-tililuokat alusta alkaen hierarkkisesti sen sijaan, että yrittäisit järjestää aiemmin luotuja. Voit esimerkiksi jäsentää **Velat**-solmun uudelleen niin, että siinä on uusi **Oma pääoma** -solmu, ja sen perässä ovat **Lyhytaikaiset velat**- ja **Pitkäaikaiset velat** -solmut.

## <a name="create-a-new-financial-report" />Luo uusi talousraportti

Käytät talousraportteja pääkirjanpitotilien analysointiin tai pääkirjanpidon kirjausten vertaamiseen budjettimerkintöihin. Voit esimerkiksi tarkastella KP-tapahtumien prosenttiosuuksia budjettitapahtumista.

[!INCLUDE[prod_short](includes/prod_short.md)] -vakioversion talousraportit eivät välttämättä vastaa yrityksen tarpeita. Voit nopeasti luoda omia talousraportteja kopioimalla olemassa olevan, kuten vaiheessa 3 kuvataan.

> [!TIP]
> Kun olet luonut talousraportin, voit tarkastella ja tarkistaa juuri määriteltyä talousraporttia **Talousraportti**-sivulla. Valitse **Muokkaa talousraporttia** -toiminto avataksesi sivun.  

> [!NOTE]
> Kun talousraportti avataan Näytä- tai Muokkaus-tilassa, suodatinruutu on käytettävissä. Raportin tietojen suodattimia ei kuitenkaan pidä määrittää tässä ruudussa. Suodattimet voivat aiheuttaa virheitä tai ne eivät suodata tietoja. Käytä sen sijaan **Asetukset**- ja **Dimensiot**-pikavälilehtien suodatinkenttiä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.  
2. Valitse **Talousraportit**-sivulla **Uusi** uuden talousraportin nimen luomiseksi.
3. Vaihtoehtoisesti, jos haluat käyttää uudelleen olemassa olevan talousraportin asetuksia, valitse **Kopioi talousraportti** -toiminto.
4. Täytä tarvittavat kentät. Valitse **Sarakemääritys**-kentässä aiemmin luotu määritys, jota voit halutessasi muokata myöhemmin.

    Sarakemääritykset määrittävät niiden parametrien sarakkeet, joiden mukaan taloustiedot näytetään riveillä. Sarakemääritys voi sisältää esimerkiksi neljä saraketta, joita voidaan käyttää verrattaessa nettomuutosta ja saldoa samalta kaudelta tältä ja edelliseltä vuodelta. Lisätietoja [Muokkaa sarakkeen määritystä](bi-how-work-account-schedule.md#edit-a-column-definition) -osassa.

5. Valitse **Muokkaa rivimääritettä** -toiminto.
6. Valitse toiminto **Syötä KP-tilit**, **Lisää kassavirtatilit** tai **Lisää kustannustyypit** luodaksesi rivin kullekin taloushallinnon elementille, jota haluat analysoida. Sinulla voi esimerkiksi olla yksi rivi nykyisille vastaaville ja toinen rivi käyttöomaisuudelle. Esimerkkejä on CRONUS-esittely-yrityksen talousraporteissa.

    > [!NOTE]
    > **Rivinumero**-kenttä -kenttä sisältää tunnuksen, kuten tilinumeron, 10 ensimmäistä merkkiä. Jos lisäät elementtejä, joiden tunnukset alkavat samoilla 10 merkillä, kaksoiskappaleita esiintyy **Rivinumero** -kentässä. Tarvittaessa voit muokata tunnuksia manuaalisesti, kun olet lisännyt elementit. Täydelliset tunnukset näkyvät **Summausväli**-kentässä.

7. Voit käyttää tuloksena saatavaa talousraporttia valitsemalla **Talousraportit**-sivun **Muokkaa talousraporttia** -toiminto.
8. Valitse **Talousraportti**-sivun **Sarakemääritys**-kentässä toinen sarakemääritys. Näet nyt toisten parametrien mukaisia taloudellisia tietoja.
9. Valitse **OK**.

Olet määrittänyt seuraavan talousraportin perusteen, näytettävät taloudelliset tiedot ja aiemmin luodun sarakeasettelun, jonka mukaan tiedot näytetään rivikohtaisesti mukautettujen parametrien perusteella. Jos vaiheessa 4 valittu oletussarakemääritys ei ole tarkoituksenmukainen, toimi kohdan [Sarakemäärityksen muokkaaminen](#edit-a-column-definition) ohjeiden mukaan.

### <a name="edit-a-column-definition" />Muokkaa sarakemääritystä

Määritä sarakemääritysten avulla, mitkä sarakkeet sisällytetään raporttiin. Voit esimerkiksi suunnitella asettelun, jonka avulla voit verrata nettomuutosta ja saldoa samalta kaudelta tältä ja edelliseltä vuodelta. Sarakkeita voi olla enintään 15, mikä on hyödyllistä esimerkiksi silloin, kun näytetään 12 kuukauden budjetit, joissa on summan näyttävä sarake.

> [!NOTE]
> Talousraportin tulostetussa, esikatsellussa tai tallennetussa voi olla esillä enintään viisi saraketta. Sitä vastoin jos talousraportti on tarkoitettu vain **Talousraportti**-sivulla analysoitavaksi, voit luoda haluamasi määrän sarakkeita.

1. Valitse **Talousraportit**-sivulla liittyvä talousraportti ja valitse sitten **Muokkaa sarakemääritystä** -toiminto.
2. Luo **Sarakemääritys**-sivulla jokaiselle sarakkeelle rivi, jonka perusteella taloustiedot näytetään talousraportissa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **OK**.
4. Avaa **Talousraportti**-sivu ajoittain ja varmista, että uusi sarakemääritys toimii odotetusti.

> [!NOTE]
> Kullekin riville määritetyt sarakkeet vastaavat **Talousraportti**-sivulla saraketta 3 ja siitä eteenpäin. Kaksi ensimmäistä saraketta, **Rivikoodi** ja **Kuvaus**, ovat kiinteitä sarakkeita.  

### <a name="create-a-column-that-calculates-percentages" />Prosenttilukuja laskevan sarakkeen luominen

Joskus haluat ehkä sisällyttää talousraporttiin sarakkeen, joka laskee prosenttiluvut kokonaissummasta. Jos sinulla esimerkiksi on myynnin dimensioittain eritteleviä rivejä, voit lisätä sarakkeen, joka ilmoittaa kunkin rivin prosenttiosuuden kokonaissummasta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
2. Valitse talousraportti **talousraportit**-sivulta.  
3. Valitse **Muokkaa talousraporttia** -toiminto, jos haluat määrittää talousraportin rivin, joka laskee prosenttilukujen perustana olevan kokonaissumman.  
4. Lisää KP-raporttimalli-ikkunaan rivi välittömästi ensimmäisen sellaisen rivin yläpuolelle, jolla haluat näyttää prosenttiluvun.  
5. Täytä rivin kentät seuraavasti: valitse **Summaustyyppi**-kenttään **Määritä prosentin perusta**. Anna **Yhteensä**-kentässä kaava, jonka laskemaan kokonaissummaan prosenttiarvo perustuu. Jos esimerkiksi rivi 11 sisältää kokonaismyynnin, syötä **11**.  
6. Valitse **Muokkaa sarakemääritystä** -toiminto, kun haluat määrittää sarakkeen.  
7. Täytä rivin kentät seuraavasti: valitse **Saraketyyppi**-kenttään **Kaava**. Anna **Kaava**-kenttään sen summan kaava, jolle haluat laskea prosentin, ja sen perään prosenttimerkki (%). Joten jos esimerkiksi sarake N sisältää nettomuutoksen, syötä **N %**.  
8. Toista vaiheet 4-7 kullekin riviryhmälle, jonka haluat jakaa prosenttiluvun mukaan.

## <a name="set-up-financial-reports-with-overviews" />Määritä talousraportit yleiskatsausten avulla

Voit käyttää talousraporttia pääkirjanpidon lukuja ja pääkirjanpidon budjettilukuja vertaavan laskelman luomiseksi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
2. Valitse talousraportti **talousraportit**-sivulta.  
3. Valitse **Muokkaa rivimääritettä** -toiminto  
4. Valitse **Rivimääritys**-sivun **Nimi**-kentässä haluamasi talousraportin nimi.
5. Valitse **Syötä KP-tilit** -toiminto.  
6. Valitse ne tilit, jotka haluat sisällyttää tiliotteeseen, ja valitse **OK**.

    Tilit on nyt lisätty talousraporttiin. Halutessasi voit myös muuttaa sarakemääritystä.  
7. Valitse **Muokkaa talousraporttia** -toiminto.  
8. Määritä **Talousraportti**-sivun **Dimensiot**-pikavälilehdessä budjettisuodattimeksi haluamasi suodattimen nimi.  
9. Valitse **OK**.  

Nyt voit kopioida ja liittää budjettierittelyn laskentataulukkoon.  

## <a name="comparing-accounting-periods-using-period-formulas" />Kirjanpitojaksojen vertaaminen käyttäen jakson kaavoja

Talousraporttisi voi verrata eri kirjanpitojaksojen tuloksia, kuten viime kuun tuloksia edellisen vuoden saman kuukauden tuloksiin. Voit tehdä sen avaamalla **sarakemääritys**-sivun ja mukauttamalla sen lisäämällä **Vertailujakson kaava** -kentän sarakkeeksi. Lue lisää kohdasta [Työtilan mukauttaminen](ui-personalization-user.md). Tämän jälkeen kenttä voidaan määrittää jakson kaavaksi.  

Kirjanpitojakson ei tarvitse vastata kalenteria. Jokaisessa tilikaudessa on kuitenkin oltava sama määrä kirjanpitojaksoja, vaikka jaksot voivatkin olla eripituisia.  

[!INCLUDE[prod_short](includes/prod_short.md)] laskee jakson kaavan avulla vertailujakson keston suhteessa raportin päivämääräsuodattimen jaksoon. Vertailujakso perustuu päivämääräsuodatuksen aloituspäivämäärän jaksoon. Jaksomääritysten lyhenteet ovat seuraavat:

| Lyhenne | Kuvaus                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| J            | Jakso.                                                                                |
| VJ           | Tilikauden, puolen vuoden tai neljänneksen viimeinen jakso.                                   |
| KP           | Tilikauden, puolen vuoden tai neljänneksen nykyinen jakso. Käytä NJ:tä kaavoissa määrittääksesi kauden, joka aloittaa tai lopettaa kaavan. Esimerkiksi FY\[1..NJ\] tarkoittaa kuluvaa aikaa kuluvan tilikauden alusta lähtien.|
| TK           | Tilikausi. Esimerkiksi TK\[1..3\] tarkoittaa kuluvan tilikauden ensimmäistä neljännestä. |

Esimerkkejä kaavoista:

| Kaava         | Kuvaus                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Nykyinen jakso.                                                                                  |
| \-1J            | Edellinen jakso.                                                                                 |
| \-1TK\[1..EJ\]  | Koko edellinen tilikausi.                                                                     |
| \-1TK           | Nykyinen jakso edellisenä tilikautena.                                                          |
| \-1TK\[1..3\]   | Edellisen tilikauden ensimmäinen vuosineljännes.                                                           |
| \-1TK\[1..NJ\]  | Edellisen tilikauden alusta lähtien, edellisen tilikauden nykyiseen jaksoon asti, se mukaan lukien molemmat kaudet. |
| \-1TK\[NJ..EJ\] | Edellisen tilikauden nykyisestä jaksosta edellisen tilikauden viimeiseen jaksoon, molemmat kaudet mukaan lukien.   |

Jos haluat laskea tavallisten jaksojen mukaan, syötä kaava sen sijaan **Vertailu pvm -kaava** -kenttään. Jos esimerkiksi kentän arvoksi määritetään -1Y, [!INCLUDE [prod_short](includes/prod_short.md)] vertaa tätä vuoden takaiseen samaan kauteen.

> [!NOTE]
> Ei ole aina selvää, mitä kausia vertailet, koska voit asettaa päivämääräsuodatuksen raportille, joka sijoittuu eri päivämääräväleille kuin kirjanpitojaksot, jotka näkyvät tilikartassa. Joten jos luot talousraportin, jossa haluat verrata tätä jaksoa edellisen vuoden samaan jaksoon siten, että määrität **Vertailun päivämääräkaava** -kentän arvoksi *-1FY*. Tämän jälkeen raportti suoritetaan helmikuun 28. päivä ja määrität päivämääräsuodatukseksi tammikuun ja helmikuun. Tämän tuloksena talousraportti vertaa tämän vuoden tammikuuta ja helmikuuta edellisen vuoden tammikuuhun, joka on ainut viime vuonna valmistuneesta kirjanpitojaksosta.  

Lisätietoja on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

## <a name="print-and-save-financial-reports" />Tulosta ja tallenna talousraportit

Voit tulostaa talousraportteja laitteesi tulostuspalveluiden avulla. [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa myös mahdollisuuden tallentaa raportteja Microsoft Excel -työkirjoina, Microsoft Word -asiakirjoina, PDF- ja XML-tiedostoina.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
2. Valitse **Talousraportit**-sivulla tulostettava raportti ja valitse sitten **Tulosta**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **Tulostin**-kentässä laite, johon raportti lähetetään.
    1. **(Selaimen käsittelemä)** -vaihtoehto ilmaisee, että raportille ei ole määritetty tulostinta. Tässä tapauksessa selain käsittelee tulosteen ja näyttää vakiotulostusvaiheet. Voit valita laitteeseesi yhdistetyn paikallisen tulostimen. **(Käsitellään selaimessa)** ei ole käytössä [!INCLUDE[prod_short](includes/prod_short.md)] -mobiilisovelluksessa tai Microsoft Teamsin selaimessa.
5. Valitse **Tulosta**-toiminto.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document" />Talousraportin ajoittaminen tai tallentaminen PDF-, Word- tai Excel-tiedostona

Taloudellinen raportti voidaan tallentaa tiedostona eri muodoissa, kuten PDF, XML, Word tai Excel. Vaihtoehtoisesti [!INCLUDE[prod_short](includes/prod_short.md)] voidaan asettaa luomaan toistuvia talousraportteja:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
2. Avaa **Talousraportit**-sivu, valitse **Tulosta**-toiminto.
3. Määritä raportti sen mukaisesti ja valitse sitten **Lähetä**-toiminto.
4. Valitse tiedostomuoto tai **Ajoita**-toiminto ja valitse **OK**.
5. Voit luoda ajoitetun tai toistuvan talousraportin täyttämällä kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
   * Toistuvissa talousraporteissa luodaan talousraportti määrittämällä **Varhaisin aloituspäivämäärä/aika** ja **Vanhentumispäivä/aika** -kenttiin ensimmäinen ja viimeinen päivämäärä. Valitse myös sen päivän päivämäärä, jolloin raportti luodaan, määrittämällä **Seuraava suorituspvm-kaava** -kenttä [Käytä pvm-kaavoja](ui-enter-date-ranges.md#use-date-formulas) -osassa selostettujen muotojen jälkeen.

## <a name="importing-or-exporting-financial-reports" />Taloudellisten raporttien tuominen tai vieminen

Voit tuoda ja viedä talousraportteja RapidStart-konfigurointipaketteina, jotka ovat hyödyllisiä esimerkiksi tietojen jakamiseen muiden yritysten kanssa. Paketti luodaan .rapidstart-tiedostosssa, joka pakkaa paketin sisällön.

### <a name="import-and-export-financial-reports" />Talousraporttien tuominen ja vieminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
2. Valitse talousraportti ja valitse sitten **Tuo talousraportti**- tai **Vie talousraportti** -toiminto sen mukaan, mitä haluat tehdä.

> [!NOTE]
> Kun tuot talousraportteja, ohjelma poistaa aiemmin luodut tietueet, joiden nimet ovat samat kuin tuomasi.

## <a name="see-related-microsoft-training" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/configure-financial-reports-dynamics-365-business-central/index).

## <a name="see-also" />Katso myös

[Suorita ja tulosta raportteja](ui-work-report.md)  
[Taloudelliset liiketoimintatiedot](bi.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
