---
title: Sarakemääritykset Financial Reportingissa
description: 'Kuvaa, miten sarakemääritykset taloushallinnon raportointityössä'
author: kennieNP
ms.author: kepontop
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# <a name="column-definitions-in-financial-reporting"></a>Sarakemääritykset Financial Reportingissa

Määritä sarakemääritysten avulla, mitkä sarakkeet sisällytetään raporttiin. Suunniteltava raporttiasettelu voi esimerkiksi nettomuutosta ja saldoa samalta jaksolta kuluvana ja edellisenä vuonna. Sarakemäärityksessä saa olla enintään 15 saraketta. Useat sarakkeet ovat käteviä esimerkiksi silloin, kun näytetään 12 kuukauden budjetit, joissa on summan näyttävä sarake.

## <a name="create-or-edit-a-column-definition"></a>Sarakemäärityksen luominen tai muokkaaminen

Luo tai muokkaa sarakemääritys seuraavien ohjeiden mukaisesti.

> [!NOTE]
> Talousraporttien tulostetussa, esikatsellussa tai tallennetussa versioissa voi olla esillä enintään viisi saraketta. Sitä vastoin jos talousraportti on tarkoitettu vain **Talousraportti**-sivulla analysoitavaksi, voit luoda haluamasi määrän sarakkeita.

1. Valitse **Talousraportit**-sivulla liittyvä talousraportti ja valitse sitten **Muokkaa sarakemääritystä** -toiminto.
1. Luo **Sarakemääritys**-sivulla jokaiselle sarakkeelle rivi, jonka perusteella taloustiedot näytetään talousraportissa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Valitse **OK**.
1. Avaa **Talousraportti**-sivu ajoittain ja varmista, että uusi sarakemääritys toimii odotetusti.

## <a name="built-in-column-definitions"></a>Valmiit sarakemääritykset

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää esimerkkisarakemäärityksiä, joiden avulla voit nopeasti aloittaa tarpeitasi vastaavien talousraporttien määrittämisen.

<!-- update this when we release the new templates in 24.1
| Column definition code | Description | How to use this column definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 |
-->

## <a name="example-create-a-column-definition-to-calculate-percentages"></a>Esimerkki: Prosenttiosuuden laskevan sarakemäärityksen luominen

Talousraporttiin halutaan sisällyttää ehkä sarake, joka laskee kokonaissumman prosenttiosuuksia. Jos sinulla esimerkiksi on myynnin dimensioittain eritteleviä rivejä, voit lisätä sarakkeen, joka ilmoittaa kunkin rivin prosenttiosuuden kokonaissummasta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 2.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Talousraportit** ja valitse sitten vastaava linkki.
1. Valitse talousraportti **talousraportit**-sivulta.  
1. Määritä talousraportin rivi laskemaan kokonaissumma, johon prosenttiosuudet perustuvat. Tämä tehdään valitsemalla **Muokkaa talousraporttia** -toiminto.  
1. Lisää rivi heti ensimmäisen sellaisen rivin yläpuolelle, jonka prosenttiosuus halutaan näyttää.  
1. Täytä tarvittaessa rivin muut kentät seuraavasti: 
    1. Valitse **Summaustyyppi**-kentässä **Määritä prosentin perusta**. 
    1. Anna **Yhteensä**-kentässä kaava, jonka laskemaan kokonaissummaan prosenttiarvo perustuu. Jos esimerkiksi rivi 11 sisältää kokonaismyynnin, syötä **11**.  
1. Valitse **Muokkaa sarakemääritystä** -toiminto, kun haluat määrittää sarakkeen.  
1. Täytä tarvittaessa rivin muut kentät seuraavasti. 
    1. Valitse **Saraketyyppi**-kentässä **Kaava**. 
    1. Anna **Kaava**-kenttään sen summan kaava, jolle haluat laskea prosentin, ja sen perään prosenttimerkki (%). Joten jos esimerkiksi sarake N sisältää nettomuutoksen, syötä **N %**.  
1. Toista vaiheet 4-7 kullekin riviryhmälle, jonka haluat jakaa prosenttiluvun mukaan.

## <a name="comparing-accounting-periods-using-period-formulas"></a>Kirjanpitojaksojen vertaaminen käyttäen jakson kaavoja

Talousraporttisi voi verrata eri kirjanpitojaksojen tuloksia, kuten viime kuun tuloksia edellisen vuoden saman kuukauden tuloksiin. Voit tehdä sen avaamalla **sarakemääritys**-sivun ja mukauttamalla sen lisäämällä **Vertailujakson kaava** -kentän sarakkeeksi. Lue lisää kohdasta [Työtilan mukauttaminen](ui-personalization-user.md). Tämän jälkeen kenttä voidaan määrittää jakson kaavaksi.  

Kirjanpitojakson ei tarvitse vastata kalenteria. Jokaisessa tilikaudessa on kuitenkin oltava sama määrä kirjanpitojaksoja, vaikka jaksot voivatkin olla eripituisia.  

[!INCLUDE[prod_short](includes/prod_short.md)] laskee jakson kaavan avulla vertailujakson keston suhteessa raportin päivämääräsuodattimen jaksoon. Vertailujakso perustuu päivämääräsuodatuksen aloituspäivämäärän jaksoon. Seuraavassa taulukossa on lyhenteet jakson määrityksille.

| Lyhenne | Kuvaus                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| J            | Jakso.                                                                                |
| VJ           | Tilikauden, puolen vuoden tai neljänneksen viimeinen jakso.                                   |
| KP           | Tilikauden, puolen vuoden tai neljänneksen nykyinen jakso. Käytä NJ:tä kaavoissa määrittääksesi kauden, joka aloittaa tai lopettaa kaavan. Esimerkiksi FY\[1..NJ\] tarkoittaa kuluvaa aikaa kuluvan tilikauden alusta lähtien.|
| TK           | Tilikausi. Esimerkiksi TK\[1..3\] tarkoittaa kuluvan tilikauden ensimmäistä neljännestä. |

Esimerkkejä kaavoista:

| Kaava | Kuvaus |
|-----|-----|
| \<Blank\>       | Nykyinen jakso. |
| \-1J            | Edellinen jakso.            |
| \-1TK\[1..EJ\]  | Koko edellinen tilikausi.                  |
| \-1TK           | Nykyinen jakso edellisenä tilikautena.       |
| \-1TK\[1..3\]   | Edellisen tilikauden ensimmäinen vuosineljännes.        |
| \-1TK\[1..NJ\]  | Edellisen tilikauden alusta lähtien, edellisen tilikauden nykyiseen jaksoon asti, se mukaan lukien molemmat kaudet. |
| \-1TK\[NJ..EJ\] | Edellisen tilikauden nykyisestä jaksosta edellisen tilikauden viimeiseen jaksoon, molemmat kaudet mukaan lukien.   |

Laskeaksesi tavallisten jaksojen mukaan, syötä kaava sen sijaan **Vertailu pvm -kaava** -kenttään. Jos esimerkiksi kentän arvoksi määritetään -1Y, [!INCLUDE [prod_short](includes/prod_short.md)] vertaa tätä vuoden takaiseen samaan kauteen.

> [!NOTE]
> Ei ole aina selvää, mitä kausia vertailet, koska voit asettaa päivämääräsuodatuksen raportille, joka sijoittuu eri päivämääräväleille kuin kirjanpitojaksot, jotka näkyvät tilikartassa. Joten jos luot talousraportin, jossa haluat verrata tätä jaksoa edellisen vuoden samaan jaksoon siten, että määrität **Vertailun päivämääräkaava** -kentän arvoksi **-1FY**. Tämän jälkeen raportti suoritetaan **helmikuun 28. päivä** ja määrität päivämääräsuodatukseksi **tammikuun ja helmikuun**. Tämän tuloksena talousraportti vertaa tämän vuoden tammikuuta ja helmikuuta edellisen vuoden tammikuuhun, joka on ainut viime vuonna valmistuneesta kirjanpitojaksosta.  

Lisätietoja on kohdassa [Kalenterin päivämäärien ja aikojen käsitteleminen](ui-enter-date-ranges.md).

[!INCLUDE [report-best-practices-column-defs](includes/report-best-practices-column-defs.md)]

## <a name="import-or-export-financial-report-column-definitions"></a>Talousraporttien sarakemääritysten tuominen tai vieminen

Vuoden 2024 1. julkaisuaallosta (versio 24.1) alkaen voit tuoda ja viedä rahoitusraportin sarakemääritelmiä RapidStart-määrityspaketteina. Esimerkiksi määrityspaketit ovat hyödyllisiä silloin, kun jaat tietoja muiden yritysten kanssa. Paketti luodaan .rapidstart-tiedostosssa, joka pakkaa paketin sisällön.

> [!NOTE]
> Talousraportin sarakemääritystä tuotaessa aiemmin luodut tietueet, joilla sama nimi kuin tuotavilla tietueilla, korvataan uusilla määrityksillä. Raporttimäärityksen määrityspaketti ei korvaa mitään aiemmin luotua raporttimäärityksessä käytettävää rivi- tai sarakemääritystä.

Talousraportin sarakemääritykset tuodaan tai viedään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sarakemääritykset** ja valitse sitten liittyvä linkki.
1. Valitse ensin rivimääritys ja sitten **Tuo sarakemääritys**- tai **Vie sarakemääritys** -toiminto sen mukaan, mitä halutaan tehdä.

## <a name="see-also"></a>Katso myös

[Rivimääritykset taloushallinnon raportoinnissa](bi-row-definitions.md)  
[Taloushallinnon raportoinnin valmisteleminen](bi-how-work-account-schedule.md)  
[Taloushallinnon liiketoimintatiedot](bi.md)  
[Taloushallinto](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
