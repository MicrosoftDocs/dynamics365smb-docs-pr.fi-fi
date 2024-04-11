---
title: Talousraporttien luomiminen taloustietojen ja tililuokkien avulla
description: 'Kuvailee, kuinka talousraporttien avulla luodaan erilaisia ​​näkymiä ja raportteja taloudellisen suorituskyvyn tietojen analysointia varten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---
# Talousraportoinnin valmisteleminen taloustietojen ja tililuokkien avulla

**Talousraportit**-ominaisuus antaa merkityksellisiä tietoja tilikartassa näkyvistä taloudellisesta tiedoista. Talousraportit voidaan määrittää analysoimaan kirjanpitotilien lukuja ja vertaamaan pääkirjanpidon tapahtumia budjettitapahtumiin. Tulokset näkyvät roolikeskuksen kaavioissa ja raporteissa, kuten kassavirtakaaviossa sekä Tuloslaskelma- ja Tase-raporteissa. Voit käyttää näitä kahta raporttia esimerkiksi liiketoimintajohtajan ja kirjanpitäjän aloitussivujen **Tilinpäätökset**-toiminnon avulla.  

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää talousraporttinäytteitä, joita voi käyttää heti malleina. Lisäksi voidaan määrittää omia raportteja vertailulukujen määrittämistä varten. Voit esimerkiksi luoda taloudellisia raportteja katteen laskemista varten osastojen tai asiakasryhmien kaltaisille dimensioille. Luotavien talousraporttien määrää ei ole rajoitettu, eikä niiden luontiin tarvita kehittäjän apua.  

## Talousraportoinnin edellytykset

Taloudellisten raporttien määrittäminen edellyttää tilikartan rakenteen ymmärtämistä. Taloudellisten raporttien suunnittelussa on todennäköisimmin otettava huomioon kolme keskeistä käsitettä:

- KP-kirjaustilien yhdistäminen KP-tililuokkiin.
- Dimensioiden käytön suunnitteleminen.
- KP-budjettien määrittäminen.

KP-tililuokat yksinkertaistavat taloudellisten raporttien määritelmiä, minkä lisäksi ne myös reagoivat joustavasti tilikarttarakenteen muutoksiin. Lisätietoja on kohdassa [Tilipäätösten asettelun muuttaminen KP-tililuokkien avulla](#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

Dimensioiden määrittäminen mahdollistaa taloushallinnon tietojen jaottelun organisaation kannalta sopivalla tavalla. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md). 

Jos kirjanpitotapahtumia halutaan tarkastella budjettitapahtumien prosenttiosuuksina, sitä varten on luotava KP-budjetteja. Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).

## Talousraportit

Taloudelliset raportit järjestävät tilikarttasi tilejä tavoilla, jotka tekevät tiedoista helpommin esitettäviä. Voit määrittää eri asetteluja määrittääksesi tiedot, jotka haluat suodattaa tilikartasta. Taloudelliset raportit mahdollistavat myös laskelmat, joita ei voi tehdä suoraan tilikartassa. Voit esimerkiksi luoda tiliryhmien välisummia ja sisällyttää ne muihin summiin. Toinen esimerkki on laskea katteita osastojen tai asiakasryhmien kaltaisille dimensioille. Lisäksi pääkirjanpidon tapahtumia ja budjettitapahtumia voi suodattaa esimerkiksi nettomuutoksen tai veloitussumman perusteella.

> [!NOTE] 
> Ajattele matemaattisesti tilinpäätösraporttia, joka on määritelty kahdella asialla:
>
> - Rivimääritysten vektori, joka määrittää, mitä tulee laskea.
> - Sarakemääritysten vektori, joka määrittää laskennan tiedot.
>
> Rahoitusraportti on sitten näiden kahden vektorin ulkotuote, jossa kukin solun arvo lasketaan sarakkeen datamääritykseen käytettävän rivin kaavan mukaan.

:::image type="content" source="media/financial-report-definition.svg" alt-text="Näkyvissä talousraportin muodostaminen rivi- ja sarakemäärityksiä hyödyntämällä" lightbox="media/financial-report-definition.svg":::

**Talousraportit**-sivulla nähdään, miten kaikissa talousraporteissa käytetään seuraavat määritteet sisältävää mallia:

* Nimi (koodi)
* Kuvaus
* Rivimääritys
* Sarakemääritys

:::image type="content" source="media/financial-reports.png" alt-text="Näkyvissä kaikkien talousraporttien muodostaminen rivi- ja sarakemäärityksiä hyödyntämällä" lightbox="media/financial-reports.png":::

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]in esimerkkitalousraportit eivät ole sellaisenaan käyttövalmiita. KP-tilien, dimensioiden, KP-tililuokkien ja budjettien määrittämistapa määrittää, miten esimerkkirivi- ja sarakemäärityksiä sekä niitä käyttäviä talousraportteja on muutettava omia määrityksiä vastaaviksi.

Vähintään kahta talousraporttia ja sarakemääritystä voidaan verrata myös kaavojen avulla. Vertailujen avulla voidaan

* luoda mukautettuja raportteja
* luoda tarvitta määrä talousraportteja, joista kullakin on yksilöivä nimi
* määrittää useita raportin asetteluita sekä tulostaa raportit käyttäen nykyisiä lukuja.

## Oppimispolku: Talousraporttien luominen Microsoft Dynamics 365 Business Centralissa

Budjettien luomisesta sekä liiketoiminnassa yleensä tarvittavien raporttien luonnissa käytetyistä talousraporteista, dimensioista sekä rivi- ja sarakemäärityksistä on saatavana lisätietoja.

Oppisen voi aloittaa käyttämällä oppimispolkua [Talousraporttien luominen Microsoft Dynamics 365 Business Centralissa](/training/paths/create-financial-reports-dynamics-365-business-central)

## Luo uusi talousraportti

Käytät talousraportteja pääkirjanpitotilien analysointiin tai pääkirjanpidon kirjausten vertaamiseen budjettimerkintöihin. Voit esimerkiksi tarkastella KP-tapahtumien prosenttiosuuksia budjettitapahtumista.

[!INCLUDE[prod_short](includes/prod_short.md)] -vakioversion talousraportit eivät välttämättä vastaa yrityksen tarpeita. Voit nopeasti luoda omia talousraportteja kopioimalla olemassa olevan, kuten vaiheessa 3 kuvataan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.  
1. Valitse **Talousraportit**-sivulla **Uusi** uuden talousraportin nimen luomiseksi. Vaihtoehtoisesti aiemmin luodun talousraportin asetuksia voidaan käyttää uudelleen valitsemalla **Kopioi talousraportti** -toiminto.
1. Kirjoita raportin lyhyt nimi (tätä nimeä ei voi muuttaa) ja raportin kuvaus.
1. Valitse rivi- ja sarakemääritykset.
1. Valinnainen: valitse rivi- ja sarakemääritysten analyysinäkymät.
1. Valitse **Muokkaa talousraporttia** -toiminto, jossa haluat käyttöösi lisää talousraportin ominaisuuksia.
1. **Asetukset**-pikavälilehdessä voidaan muokata raportin kuvausta, muuttaa rivi- ja sarakemäärityksiä sekä määrittää päivämäärien näyttötapa. Päivämäärähierarkiana voi olla päivä, viikko, kuukausi, vuosineljännes ja vuosi tai kirjanpitojaksot. Lisätietoja on kohdassa [Kirjanpitojaksojen vertaaminen jakson kaavojen avulla](#comparing-accounting-periods-using-period-formulas).
1. **Dimensiot**-pikavälilehdessä voidaan määrittää raportin dimensiosuodattimet.
1. Raporttia voi esikatsella **Dimensiot**-pikavälilehden alla olevalla alueella.

> [!TIP]
> Kun talousraportti on luotu, se voidaan esikatsella ja tarkistaa **Talousraportti**-sivulla. Avaa sivu valitsemalla **Näytä talousraportti** -toiminto.  

> [!NOTE]
> Kun talousraportti avataan Näytä- tai Muokkaus-tilassa, suodatinruutu on käytettävissä. Raportin tietojen suodattimia ei määritetä suodatinruudussa. Kyseiset suodattimet voivat aiheuttaa virheitä, tai ne eivät suodata tietoja. Raportin suodattimet määritetään sen sijaan **Asetukset**- ja **Dimensiot**-pikavälilehtien kenttien avulla.

### Rivimäärityksen luominen tai muokkaaminen

Talousraporttien rivimääritykset mahdollistavat laskelmat, joita ei voi tehdä suoraan tilikartassa. Voit esimerkiksi luoda tiliryhmien välisummia ja sisällyttää ne muihin summiin. Lisäksi voidaan laskea välivaiheet, joita ei näytetä lopullisessa raportissa.

1. Valitse **Talousraportit**-sivulla sopiva talousraportti ja valitse sitten **Muokkaa rivimääritystä** -toiminto.
1. Valitse toiminto **Syötä KP-tilit**, **Lisää kassavirtatilit** tai **Lisää kustannustyypit** luodaksesi rivin kullekin taloushallinnon elementille, jota haluat analysoida. Sinulla voi esimerkiksi olla yksi rivi nykyisille vastaaville ja toinen rivi käyttöomaisuudelle. Esimerkkejä on CRONUS-esittely-yrityksen talousraporteissa.

    > [!NOTE]
    > **Rivinumero**-kenttä -kenttä sisältää tunnuksen, kuten tilinumeron, 10 ensimmäistä merkkiä. Jos lisättävien elementtien alussa on samat 10 merkkiä, seurauksena on kaksoiskappaleita **Rivinumero** -kentässä. Tarvittaessa voit muokata tunnuksia manuaalisesti, kun olet lisännyt elementit. Täydelliset tunnukset näkyvät **Summausväli**-kentässä.

> [!NOTE]
> Kullekin rivimäärityksen riville määritetyt sarakkeet ilmaisevat **Talousraportti**-sivulla sarakkeita sarakkeesta 3 alkaen. Kaksi ensimmäistä saraketta, **Rivikoodi** ja **Kuvaus**, ovat kiinteitä sarakkeita.  

### Sarakemäärityksen luominen tai muokkaaminen

Määritä sarakemääritysten avulla, mitkä sarakkeet sisällytetään raporttiin. Suunniteltava raporttiasettelu voi esimerkiksi nettomuutosta ja saldoa samalta jaksolta kuluvana ja edellisenä vuonna. Sarakemäärityksessä saa olla enintään 15 saraketta. Useat sarakkeet ovat käteviä esimerkiksi silloin, kun näytetään 12 kuukauden budjetit, joissa on summan näyttävä sarake.

> [!NOTE]
> Talousraportin tulostetussa, esikatsellussa tai tallennetussa voi olla esillä enintään viisi saraketta. Sitä vastoin jos talousraportti on tarkoitettu vain **Talousraportti**-sivulla analysoitavaksi, voit luoda haluamasi määrän sarakkeita.

1. Valitse **Talousraportit**-sivulla liittyvä talousraportti ja valitse sitten **Muokkaa sarakemääritystä** -toiminto.
1. Luo **Sarakemääritys**-sivulla jokaiselle sarakkeelle rivi, jonka perusteella taloustiedot näytetään talousraportissa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Valitse **OK**.
1. Avaa **Talousraportti**-sivu ajoittain ja varmista, että uusi sarakemääritys toimii odotetusti.

### Prosenttiosuuden laskevan sarakemäärityksen luominen

Talousraporttiin halutaan sisällyttää ehkä sarake, joka laskee kokonaissumman prosenttiosuuksia. Jos sinulla esimerkiksi on myynnin dimensioittain eritteleviä rivejä, voit lisätä sarakkeen, joka ilmoittaa kunkin rivin prosenttiosuuden kokonaissummasta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Valitse talousraportti **talousraportit**-sivulta.  
1. Määritä talousraportin rivi laskemaan kokonaissumma, johon prosenttiosuudet perustuvat. Tämä tehdään valitsemalla **Muokkaa talousraporttia** -toiminto.  
1. Lisää rivi heti ensimmäisen sellaisen rivin yläpuolelle, jonka prosenttiosuus halutaan näyttää.  
1. Täytä rivin kentät seuraavasti: valitse **Summaustyyppi**-kenttään **Määritä prosentin perusta**. Anna **Yhteensä**-kentässä kaava, jonka laskemaan kokonaissummaan prosenttiarvo perustuu. Jos esimerkiksi rivi 11 sisältää kokonaismyynnin, syötä **11**.  
1. Valitse **Muokkaa sarakemääritystä** -toiminto, kun haluat määrittää sarakkeen.  
1. Täytä tarvittaessa rivin muut kentät seuraavasti. Valitse **Saraketyyppi**-kentässä **Kaava**. Anna **Kaava**-kenttään sen summan kaava, jolle haluat laskea prosentin, ja sen perään prosenttimerkki (%). Joten jos esimerkiksi sarake N sisältää nettomuutoksen, syötä **N %**.  
1. Toista vaiheet 4-7 kullekin riviryhmälle, jonka haluat jakaa prosenttiluvun mukaan.

## Tilinpäätösten asettelun muuttaminen KP-tililuokkien avulla

KP-tililuokkien avulla voit muuttaa rahoituslaskelmien asettelua. Esimerkki: Kun tililuokat on määritetty **KP-tililuokat**-sivulla, **Luo talousraportit** -toiminto voidaan valita ja talousraportit, joihin perustalousraportit pohjautuvat, voidaan päivittää. Kun jokin näistä raporteista, kuten **Tase**-raportti suoritetaan seuraavan kerran, uudet kokonaissummat ja alatapahtumat lisätään.

KP-tililuokkien etuna rivimäärityksissä pelkkiä käyttäviin KP-tileihin nähden on se, että tilakartan rakenteen muutokset eivät vaikuta talousraportteihin.

> [!NOTE]
> Ylätason tililuokat, kuten **Velat**-solmu, ovat kiinteitä, eikä niitä voi itse lisätä. Voit kuitenkin poistaa ja lisätä tililuokkia alemmilla tasoilla ja muuttaa niiden rakennetta määrittääksesi, miten liittyvä talousraportti näkyy raporteissa.
>
> Sinun tulisi luoda ja jäsentää omat alemman tason KP-tililuokat alusta alkaen hierarkkisesti sen sijaan, että yrittäisit järjestää aiemmin luotuja. Voit esimerkiksi jäsentää **Velat**-solmun uudelleen niin, että siinä on uusi **Oma pääoma** -solmu, ja sen perässä ovat **Lyhytaikaiset velat**- ja **Pitkäaikaiset velat** -solmut. Lisätietoja on kohdassa [Pääkirjanpitotilien yhdistäminen tililuokkiin](finance-general-ledger.md#account-categories).

## Dimensioiden käyttäminen talousraporteissa

Talousanalyysissä dimensio on tieto, jonka lisäät tapahtumaan eräänlaiseksi merkiksi. Tämän tiedon avulla voi yhdistää ryhmiksi tapahtumia, joilla on samoja ominaisuuksia, kuten asiakkaita, alueita, tuotteita tai myyjiä, sekä noutaa nämä ryhmät helposti analysoitavaksi. Dimensioita voidaan käyttää päiväkirjojen tapahtumissa, asiakirjoissa ja budjeteissa.

Kukin dimensio kuvaa sitä, mihin analysointi keskittyy. Joten esimerkiksi kaksidimensioinen analyysi voisi olla myynti per alue. Useamman kuin kahden dimension käyttäminen tapahtumaa luotaessa mahdollistaa monisyisen analysoinnin. Esimerkki monimutkaisesta analyysista on perehtyä alue-, asiakasryhmä- ja myyntikampanjakohtaiseen myyntiin. Näin saadaan entistä enemmän merkityksellisiä tietoja liiketoiminnasta. Tällaisia tietoja ovat esimerkiksi se, miten hyvin yritys toimii, missä se menestyy ja missä ei sekä minne pitäisi kohdentaa enemmän resursseja. Nämä merkitykselliset tiedot auttavat tekemään tietopohjaisia liiketoimintapäätöksiä. Lisätietoja on kohdassa [Dimensioiden käsitteleminen](finance-dimensions.md).

## Määritä talousraportit yleiskatsausten avulla

Talousraportin avulla voidaan luoda laskelma, joka vertaa pääkirjanpidon ja budjetin lukuja.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Valitse talousraportti **talousraportit**-sivulta.  
1. Valitse **Muokkaa rivimääritettä** -toiminto  
1. Valitse **Rivimääritys**-sivun **Nimi**-kentässä haluamasi talousraportin nimi.
1. Valitse **Syötä KP-tilit** -toiminto.  
1. Valitse ne tilit, jotka haluat sisällyttää tiliotteeseen, ja valitse **OK**.

    Tilit lisätään talousraporttiin. Halutessasi voit myös muuttaa sarakemääritystä.  
1. Valitse **Muokkaa talousraporttia** -toiminto.  
1. Määritä **Talousraportti**-sivun **Dimensiot**-pikavälilehdessä budjettisuodattimeksi haluamasi suodattimen nimi.  
1. Valitse **OK**.  

Nyt voit kopioida ja liittää budjettierittelyn laskentataulukkoon.  

## Kirjanpitojaksojen vertaaminen käyttäen jakson kaavoja

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

## Tulosta ja tallenna talousraportit

Voit tulostaa talousraportteja laitteesi tulostuspalveluiden avulla. [!INCLUDE[prod_short](includes/prod_short.md)]issa on myös mahdollisuus tallentaa raportit Excel-työkirjoina, Word-asiakirjoina sekä PDF- ja XML-tiedostoina.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Valitse **Talousraportit**-sivulla tulostettava raportti ja valitse sitten **Tulosta**-toiminto.
1. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Valitse **Tulostin**-kentässä laite, johon raportti lähetetään.
    1. **(Selaimen käsittelemä)** -vaihtoehto ilmaisee, että raportille ei ole määritetty tulostinta. Tässä tapauksessa selain käsittelee tulosteen ja näyttää vakiotulostusvaiheet. Voit valita laitteeseesi yhdistetyn paikallisen tulostimen. **(Käsitellään selaimessa)** ei ole käytettävissä [!INCLUDE[prod_short](includes/prod_short.md)] -mobiilisovelluksessa tai Teamsin sovelluksessa.
1. Valitse **Tulosta**-toiminto.

### Talousraportin ajoittaminen tai tallentaminen PDF-, Word- tai Excel-tiedostona

Taloudellinen raportti voidaan tallentaa tiedostona eri muodoissa, kuten PDF, XML, Word tai Excel. Vaihtoehtoisesti [!INCLUDE[prod_short](includes/prod_short.md)] voi luoda toistuvia talousraportteja:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Avaa **Talousraportit**-sivu, valitse **Tulosta**-toiminto.
1. Määritä raportti sen mukaisesti ja valitse sitten **Lähetä**-toiminto.
1. Valitse tiedostomuoto tai **Ajoita**-toiminto ja valitse **OK**.
1. Voit luoda ajoitetun tai toistuvan talousraportin täyttämällä kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>Toistuvissa talousraporteissa luodaan talousraportti määrittämällä **Varhaisin aloituspäivämäärä/aika** ja **Vanhentumispäivä/aika** -kenttiin ensimmäinen ja viimeinen päivämäärä. Valitse myös sen päivän päivämäärä, jolloin raportti luodaan, määrittämällä **Seuraava suorituspvm-kaava** -kenttä [Käytä pvm-kaavoja](ui-enter-date-ranges.md#use-date-formulas) -osassa selostettujen muotojen jälkeen.

## Talousraporttien määritysten tuominen tai vieminen

Talousraportti- tai rivimääritykset voidaan tuoda ja viedä RapidStart-määrityspaketteina, jotka ovat käteviä esimerkiksi tietojen jakamiseen muiden yritysten kanssa. Paketti luodaan .rapidstart-tiedostosssa, joka pakkaa paketin sisällön.

> [!NOTE]
> Talousraportti- tai rivimääritystä tuotaessa aiemmin luodut tietueet, joilla sama nimi kuin tuotavilla tietueilla, korvataan uusilla määrityksillä. On huomattava että raporttimäärityksen määrityspaketti ei korvaa mitään aiemmin luotua raporttimäärityksessä käytettävää rivi- tai sarakemääritystä.

Talousraporttimääritykset tuodaan tai viedään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Valitse talousraportti ja valitse sitten **Tuo talousraportti**- tai **Vie talousraportti** -toiminto sen mukaan, mitä haluat tehdä.

Talousraportin rivimääritykset tuodaan tai viedään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rivimääritykset** ja valitse aiheeseen liittyvä linkki.
1. Valitse ensin rivimääritys, sitten **Tuo rivimääritys**- tai **Vie rivimääritys** -toiminto sen mukaan, mitä halutaan tehdä.

## Katso myös

[Raporttien suorittaminen ja tulostaminen](ui-work-report.md)  
[Taloushallinnon liiketoimintatiedot](bi.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
