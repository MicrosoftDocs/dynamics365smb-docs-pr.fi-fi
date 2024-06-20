---
title: Talousraporttien luomiminen taloustietojen ja tililuokkien avulla
description: 'Kuvailee, kuinka talousraporttien avulla luodaan erilaisia ​​näkymiä ja raportteja taloudellisen suorituskyvyn tietojen analysointia varten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: 'Report_25, 103, 104, 108, 195, 196, 197, 198, 488, 489, 490, 764, 765, 766'
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

KP-tililuokat yksinkertaistavat taloudellisten raporttien määritelmiä, minkä lisäksi ne myös reagoivat joustavasti tilikarttarakenteen muutoksiin. Lisätietoja on kohdassa [Tilipäätösten asettelun muuttaminen KP-tililuokkien avulla](bi-row-definitions.md#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

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

- Nimi (koodi)
- Kuvaus
- Rivimääritys
- Sarakemääritys

:::image type="content" source="media/financial-reports.png" alt-text="Näkyvissä kaikkien talousraporttien muodostaminen rivi- ja sarakemäärityksiä hyödyntämällä" lightbox="media/financial-reports.png":::

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]in esimerkkitalousraportit eivät ole sellaisenaan käyttövalmiita. KP-tilien, dimensioiden, KP-tililuokkien ja budjettien määrittämistapa määrittää, miten esimerkkirivi- ja sarakemäärityksiä sekä niitä käyttäviä talousraportteja on muutettava omia määrityksiä vastaaviksi.

Vähintään kahta talousraporttia ja sarakemääritystä voidaan verrata myös kaavojen avulla. Vertailujen avulla voidaan

- luoda mukautettuja raportteja
- luoda tarvitta määrä talousraportteja, joista kullakin on yksilöivä nimi
- määrittää useita raportin asetteluita sekä tulostaa raportit käyttäen nykyisiä lukuja.

## Oppimispolku: Talousraporttien luominen Microsoft Dynamics 365 Business Centralissa

Haluatko oppia luomaan budjetteja ja käyttämään sitten talousraportteja, ulottuvuuksia sekä rivi- ja sarakemäärityksiä yritysten tyypillisesti tarvitsemien talousraporttien luomiseen?

Aloita käyttämällä seuraavaa oppimispolkua [Talousraporttien luominen Microsoft Dynamics 365 Business Centralissa](/training/paths/create-financial-reports-dynamics-365-business-central).

## Luo uusi talousraportti

Käytät talousraportteja pääkirjanpitotilien analysointiin tai pääkirjanpidon kirjausten vertaamiseen budjettimerkintöihin. Voit esimerkiksi tarkastella KP-tapahtumien prosenttiosuuksia budjettitapahtumista.

[!INCLUDE[prod_short](includes/prod_short.md)] -vakioversion talousraportit eivät välttämättä vastaa yrityksen tarpeita. Voit nopeasti luoda omia talousraportteja kopioimalla olemassa olevan, kuten vaiheessa 3 kuvataan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.  
1. Valitse **Talousraportit**-sivulla **Uusi** uuden talousraportin nimen luomiseksi. Vaihtoehtoisesti aiemmin luodun talousraportin asetuksia voidaan käyttää uudelleen valitsemalla **Kopioi talousraportti** -toiminto.
1. Kirjoita raportin lyhyt nimi (et voi muuttaa nimeä myöhemmin) ja raportin kuvaus.
1. Valitse rivi- ja sarakemääritykset.
1. Valinnainen: valitse rivi- ja sarakemääritysten analyysinäkymät.
1. Valitse **Muokkaa talousraporttia** -toiminto, jossa haluat käyttöösi lisää talousraportin ominaisuuksia.
1. **Asetukset**-pikavälilehdessä voidaan muokata raportin kuvausta, muuttaa rivi- ja sarakemäärityksiä sekä määrittää päivämäärien näyttötapa. Päivämäärähierarkiana voi olla päivä, viikko, kuukausi, vuosineljännes ja vuosi tai kirjanpitojaksot. Lisätietoja on kohdassa [Kirjanpitojaksojen vertaaminen jakson kaavojen avulla](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas).
1. **Dimensiot**-pikavälilehdessä voidaan määrittää raportin dimensiosuodattimet.
1. Raporttia voi esikatsella **Dimensiot**-pikavälilehden alla olevalla alueella.

> [!TIP]
> Kun talousraportti on luotu, se voidaan esikatsella ja tarkistaa **Talousraportti**-sivulla. Avaa sivu valitsemalla **Näytä talousraportti** -toiminto.  

> [!NOTE]
> Kun talousraportti avataan Näytä- tai Muokkaus-tilassa, suodatinruutu on käytettävissä. Raportin tietojen suodattimia ei määritetä suodatinruudussa. Kyseiset suodattimet voivat aiheuttaa virheitä, tai ne eivät suodata tietoja. Raportin suodattimet määritetään sen sijaan **Asetukset**- ja **Dimensiot**-pikavälilehtien kenttien avulla.

### Rivimäärityksen luominen tai muokkaaminen

Talousraporttien rivimääritykset mahdollistavat laskelmat, joita ei voi tehdä suoraan tilikartassa. Voit esimerkiksi luoda tiliryhmien välisummia ja sisällyttää ne muihin summiin. Lisäksi voidaan laskea välivaiheet, joita ei näytetä lopullisessa raportissa.

Lisätietoja on kohdassa [Rivimääritykset talousraporteissa](bi-row-definitions.md).

### Sarakemäärityksen luominen tai muokkaaminen

Määritä sarakemääritysten avulla, mitkä sarakkeet sisällytetään raporttiin. Suunniteltava raporttiasettelu voi esimerkiksi nettomuutosta ja saldoa samalta jaksolta kuluvana ja edellisenä vuonna. Sarakemäärityksessä saa olla enintään 15 saraketta. Useat sarakkeet ovat käteviä esimerkiksi silloin, kun näytetään 12 kuukauden budjetit, joissa on summan näyttävä sarake.

Lisätietoja on kohdassa [Sarakemääritykset talousraporteissa](bi-column-definitions.md).

## Dimensioiden käyttäminen talousraporteissa

Talousanalyysissä dimensio on tieto, jonka lisäät tapahtumaan eräänlaiseksi merkiksi. Tämän tiedon avulla voi yhdistää ryhmiksi tapahtumia, joilla on samoja ominaisuuksia, kuten asiakkaita, alueita, tuotteita tai myyjiä, sekä noutaa nämä ryhmät helposti analysoitavaksi. Dimensioita voidaan käyttää päiväkirjojen tapahtumissa, asiakirjoissa ja budjeteissa.

Kukin dimensio kuvaa sitä, mihin analysointi keskittyy. Joten esimerkiksi kaksidimensioinen analyysi voisi olla myynti per alue. Useamman kuin kahden dimension käyttäminen tapahtumaa luotaessa mahdollistaa monisyisen analysoinnin. Esimerkki monimutkaisesta analyysista on perehtyä alue-, asiakasryhmä- ja myyntikampanjakohtaiseen myyntiin. Näin saadaan entistä enemmän merkityksellisiä tietoja liiketoiminnasta. Tällaisia tietoja ovat esimerkiksi se, miten hyvin yritys toimii, missä se menestyy ja missä ei sekä minne pitäisi kohdentaa enemmän resursseja. Nämä merkitykselliset tiedot auttavat tekemään tietopohjaisia liiketoimintapäätöksiä. Saat lisätietoja siirtymällä kohtaan [Dimensioiden käyttäminen](finance-dimensions.md).

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

## Talousraporttien integroiminen Exceliin

Voit integroida talousraportin Excel-työkirjamallin kanssa, muuttaa asettelun tarpeidesi mukaan ja päivittää Excel-malliin tiedot [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta. Integrointi helpottaa esimerkiksi kuukausittaisten ja vuosittaisten taloudellisten raporttien luontia sinulle toimivassa muodossa.

### Excel-integroinnin määrittäminen rahoitusraportille (Luo Excel-malli)

Kun haluat määrittää Excel-integroinnin rahoitusraportille, luo raporttia varten Excel-malli noudattamalla näitä vaiheita.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Valitse **Talousraportit**-sivulla talousraportti ottaaksesi Excelin käyttöön ja valitse sitten **Tuo Exceliin** -toiminto.
1. Valitse **Luo uusi tiedosto** -toiminto. Tämä toiminto lataa Excel-mallin työkirjan, jossa on yksi raportin nimen mukaan nimetty työkirja.
1. Kopioi työkirja ja nimeä se uudelleen **Dataksi**.
1. Nimeä raportin työkirja uudelleen mieleiseksesi.
1. Merkitse raporttityökirjaan kaikki solut, joissa näkyy talousraportin tietoja (mukaan lukien sarake- ja riviotsikot). Etsi **Kotisivu**-valintanauhan **Numero**-valikko ja valitse muodoksi **Yleinen**.
1. Valitse alueen vasemmanpuoleisin solu, jossa on talousraportin tietoja, ja määritä viittaus vastaavaan soluun Data-työkirjassa. Laajenna kaavaa ensimmäisen rivin kaikkiin soluihin vetämällä riviä alas ja peitä sitten talousraportin kaikki rivit vetämällä riviä alas.
1. Piilota **data**-työkirja.
1. Muotoile raporttityökirja tarpeidesi mukaan.
1. Tallenna työkirja OneDriveen tai vastaavaan paikkaan, jossa tiedosto varmuuskopioidaan ja versioidaan.
1. Sulje työkirja.

### Talousraportin suorittaminen Excel-mallin avulla

Voit suorittaa talousraportin Excel-mallin avulla noudattamalla seuraavia vaiheita:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Valitse **Talousraportit**-sivulla talousraportti ottaaksesi Excelin käyttöön ja valitse sitten **Tuo Exceliin** -toiminto.
1. Valitse **Päivitä kopio olemassa olevasta asiakirjasta** -toiminto.
1. Lataa Excel-malli (sulje Excel-työkirja ennen sen lataamista).
1. Valitse **Nimi-/Arvo-haku**-sivulla Data-työkirja.
1. [!INCLUDE[prod_short](includes/prod_short.md)] suorittaa talousraportin ja yhdistää tuloksena syntyvät tiedot Excel-malliin.

## Tulosta ja tallenna talousraportit

Voit tulostaa talousraportteja laitteesi tulostuspalveluiden avulla. [!INCLUDE[prod_short](includes/prod_short.md)]issa on myös mahdollisuus tallentaa raportit Excel-työkirjoina, Word-asiakirjoina sekä PDF- ja XML-tiedostoina.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Valitse **Talousraportit**-sivulla tulostettava raportti ja valitse sitten **Tulosta**-toiminto.
1. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Valitse **Tulostin**-kentässä laite, johon raportti lähetetään.
    1. **(Selaimen käsittelemä)** -vaihtoehto ilmaisee, että raportille ei ole määritetty tulostinta. Tässä tapauksessa selain käsittelee tulosteen ja näyttää vakiotulostusvaiheet. Voit valita laitteeseesi yhdistetyn paikallisen tulostimen. **(Käsitellään selaimessa)** ei ole käytettävissä [!INCLUDE[prod_short](includes/prod_short.md)] -mobiilisovelluksessa tai Teamsin sovelluksessa.
1. Valitse **Tulosta**-toiminto.

### Talousraportin ajoittaminen tai tallentaminen PDF-, Word- tai Excel-tiedostona

Voit tallentaa taloudellisen raportin tiedostomuodoissa, kuten PDF, XML, Word tai Excel. [!INCLUDE[prod_short](includes/prod_short.md)] voi myös luoda toistuvia talousraportteja.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Avaa **Talousraportit**-sivu, valitse **Tulosta**-toiminto.
1. Määritä raportti sen mukaisesti ja valitse sitten **Lähetä**-toiminto.
1. Valitse tiedostomuoto tai **Ajoita**-toiminto ja valitse **OK**.
1. Voit luoda ajoitetun tai toistuvan talousraportin täyttämällä kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>Toistuvissa talousraporteissa luodaan talousraportti määrittämällä **Varhaisin aloituspäivämäärä/aika** ja **Vanhentumispäivä/aika** -kenttiin ensimmäinen ja viimeinen päivämäärä. Valitse myös sen päivän päivämäärä, jolloin raportti luodaan, määrittämällä **Seuraava suorituspvm-kaava** -kenttä [Käytä pvm-kaavoja](ui-enter-date-ranges.md#use-date-formulas) -osassa selostettujen muotojen jälkeen.


## Taloudellisten raporttimääritysten käytön parhaat käytännöt

Talousraportin määrityksiä ei versioita. Kun muutat raporttimääritystä, vanha versio korvataan, kun muutos tallentuu tietokantaan. Seuraavassa luettelossa on joitakin parhaita käytäntöjä talousraporttimääritysten parissa työskentelemiseen:

- Jos lisäät raporttimääritelmiä, valitse hyvä koodi ja täytä kuvaus-kenttään merkityksellinen teksti samalla kun tiedät, mihin raporttia käytetään. Näiden tietojen avulla työkaverisi (ja tuleva itsesi) voivat työskennellä raportin parissa ja ehkä muuttaa raporttimäärittelyä.
- Ennen kuin muutat raporttimääritystä, harkitse kopion ottamista varmuuskopioksi siltä varalta, että muutos ei toimi odotetulla tavalla. Voit joko kopioida määrityksen (antaa sille hyvän nimen) tai viedä sen. Lisätietoja on kohdassa [Talousraporttimääritysten tuominen tai vieminen](#import-or-export-financial-report-definitions).
- Jos tarvitset uuden kopion määrityksestä, jonka [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa, helppo tapa saada sellainen, on luoda uusi yritys, joka sisältää vain asetustietoja. Vie sitten määritys ja tuo se yritykseen, jossa määrityksen päivitystä tarvitaan.

## Tuo tai vie talousraporttien määrityksiä

Voit tuoda ja viedä taloudellisia raporttimäärityksiä RapidStart-konfigurointipaketteina. Esimerkiksi määrityspaketit ovat hyödyllisiä silloin, kun jaat tietoja muiden yritysten kanssa. Paketti luodaan .rapidstart-tiedostosssa, joka pakkaa paketin sisällön.

> [!NOTE]
> Talousraporttimääritystä tuotaessa aiemmin luodut tietueet, joilla sama nimi kuin tuotavilla tietueilla, korvataan uusilla määrityksillä. Raporttimäärityksen määrityspaketti ei korvaa mitään aiemmin luotua raporttimäärityksessä käytettävää rivi- tai sarakemääritystä.

Talousraporttimääritykset tuodaan tai viedään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Valitse talousraportti ja valitse sitten **Tuo talousraportti**- tai **Vie talousraportti** -toiminto sen mukaan, mitä haluat tehdä.

Lisätietoja talousraportin rivi- tai sarakemääritysten tuomisesta tai viemisestä on seuraavissa artikkeleissa: 

- [Talousraporttien rivimääritysten tuominen tai vieminen](bi-row-definitions.md#import-or-export-financial-reporting-row-definitions) tai
- [Talousraportoinnin sarakemääritysten tuominen tai vieminen](bi-column-definitions.md#import-or-export-financial-report-column-definitions)

## Katso myös

[Rivimääritykset taloushallinnon raportoinnissa](bi-row-definitions.md)  
[Sarakemääritykset taloushallinnon raportoinnissa](bi-column-definitions.md)  
[Raporttien suorittaminen ja tulostaminen](ui-work-report.md)  
[Taloushallinnon liiketoimintatiedot](bi.md)  
[Taloushallinto](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
