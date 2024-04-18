---
title: Rivimääritykset Financial Reportingissa
description: 'Kuvaa, miten rivimääritykset talousraportoinnissa toimivat.'
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

# Rivimääritykset Financial Reportingissa

Talousraporttien rivimääritykset mahdollistavat laskelmat, joita ei voi tehdä suoraan tilikartassa. Voit esimerkiksi luoda tiliryhmien välisummia ja sisällyttää ne muihin summiin. Lisäksi voidaan laskea välivaiheet, joita ei näytetä lopullisessa raportissa.

## Rivimäärityksen luominen tai muokkaaminen

Luo tai muokkaa rivimääritys seuraavien ohjeiden mukaisesti:

1. Valitse **Talousraportit**-sivulla sopiva talousraportti ja valitse sitten **Muokkaa rivimääritystä** -toiminto.
1. Valitse toiminto **Syötä KP-tilit**, **Lisää kassavirtatilit** tai **Lisää kustannustyypit** luodaksesi rivin kullekin taloushallinnon elementille, jota haluat analysoida. Sinulla voi esimerkiksi olla yksi rivi nykyisille vastaaville ja toinen rivi käyttöomaisuudelle. Esimerkkejä on CRONUS-esittely-yrityksen talousraporteissa.

    > [!NOTE]
    > **Rivinumero**-kenttä -kenttä sisältää tunnuksen, kuten tilinumeron, 10 ensimmäistä merkkiä. Jos lisättävien elementtien alussa on samat 10 merkkiä, seurauksena on kaksoiskappaleita **Rivinumero** -kentässä. Tarvittaessa voit muokata tunnuksia manuaalisesti, kun olet lisännyt elementit. Täydelliset tunnukset näkyvät **Summausväli**-kentässä.

> [!NOTE]
> Kullekin rivimäärityksen riville määritetyt sarakkeet ilmaisevat **Talousraportti**-sivulla sarakkeita sarakkeesta 3 alkaen. Kaksi ensimmäistä saraketta, **Rivikoodi** ja **Kuvaus**, ovat kiinteitä sarakkeita.  

## Valmiit rivimääritykset

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää esimerkkirivimäärityksiä, joiden avulla voit nopeasti aloittaa tarpeitasi vastaavien talousraporttien määrittämisen.

<!-- update this when we release the new templates in 24.1
| Row definition code | Description | How to use this row definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 | 
-->

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]in esimerkkitalousraportit eivät ole sellaisenaan käyttövalmiita. KP-tilien, dimensioiden, KP-tililuokkien ja budjettien määrittämistapa määrittää, miten esimerkkirivi- ja sarakemäärityksiä sekä niitä käyttäviä talousraportteja on muutettava omia määrityksiä vastaaviksi.

## Tilinpäätösten asettelun muuttaminen KP-tililuokkien avulla

KP-tililuokkien avulla voit muuttaa rahoituslaskelmien asettelua. Esimerkki: Kun tililuokat on määritetty **KP-tililuokat**-sivulla, **Luo talousraportit** -toiminto voidaan valita ja talousraportit, joihin perustalousraportit pohjautuvat, voidaan päivittää. Kun jokin näistä raporteista, kuten **Tase**-raportti suoritetaan seuraavan kerran, uudet kokonaissummat ja alatapahtumat lisätään.

KP-tililuokkien etuna rivimäärityksissä pelkkiä käyttäviin KP-tileihin nähden on se, että tilakartan rakenteen muutokset eivät vaikuta talousraportteihin.

> [!NOTE]
> Ylätason tililuokat, kuten **Velat**-solmu, ovat kiinteitä, eikä niitä voi itse lisätä. Voit kuitenkin poistaa ja lisätä tililuokkia alemmilla tasoilla ja muuttaa niiden rakennetta määrittääksesi, miten liittyvä talousraportti näkyy raporteissa.
>
> Sinun tulisi luoda ja jäsentää omat alemman tason KP-tililuokat alusta alkaen hierarkkisesti sen sijaan, että yrittäisit järjestää aiemmin luotuja. Voit esimerkiksi jäsentää **Velat**-solmun uudelleen niin, että siinä on uusi **Oma pääoma** -solmu, ja sen perässä ovat **Lyhytaikaiset velat**- ja **Pitkäaikaiset velat** -solmut. Lisätietoja on kohdassa [Pääkirjanpitotilien yhdistäminen tililuokkiin](finance-general-ledger.md#account-categories).

## Rivimääritysten käytön parhaat käytännöt

Rivimäärityksiä ei versioida. Kun muutat rivimääritystä, vanha versio korvataan, kun muutos tallentuu tietokantaan. Seuraavassa luettelossa on joitakin parhaita käytäntöjä rivimääritysten parissa työskentelemiseen:

- Jos lisäät rivimääritelmiä, valitse hyvä koodi ja täytä kuvaus-kenttään merkityksellinen teksti samalla kun tiedät, mihin rivimääritystä käytetään. Näiden tietojen avulla työkaverisi (ja tuleva itsesi) voivat työskennellä talousraportoinnin parissa ja ehkä muuttaa rivin määrittelyä.
- Ennen kuin muutat rivimääritystä, harkitse kopion ottamista varmuuskopioksi siltä varalta, että muutos ei toimi odotetulla tavalla. Voit joko kopioida määrityksen (antaa sille hyvän nimen) tai viedä sen. Lisätietoja on kohdassa [siirry rivimääritysten tuomiseen tai viemiseen](#import-or-export-financial-reporting-row-definitions).
- Jos tarvitset uuden kopion määrityksestä, jonka [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa, helppo tapa saada sellainen, on luoda uusi yritys, joka sisältää vain asetustietoja. Vie sitten määritys ja tuo se yritykseen, jossa määrityksen päivitystä tarvitaan.

## Talousraporttien rivimääritysten tuominen tai vieminen

Voit tuoda ja viedä taloudellisia rivimäärityksiä RapidStart-konfigurointipaketteina. Esimerkiksi määrityspaketit ovat hyödyllisiä silloin, kun jaat tietoja muiden yritysten kanssa. Paketti luodaan .rapidstart-tiedostosssa, joka pakkaa paketin sisällön.

> [!NOTE]
> Talousraportoinnin rivimäärityksiä tuotaessa aiemmin luodut tietueet, joilla sama nimi kuin tuotavilla tietueilla, korvataan uusilla määrityksillä. Raporttimäärityksen määrityspaketti ei korvaa mitään aiemmin luotua raporttimäärityksessä käytettävää rivi- tai sarakemääritystä.

Talousraportin rivimääritykset tuodaan tai viedään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 4.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Rivimääritykset** ja valitse aiheeseen liittyvä linkki.
1. Valitse ensin rivimääritys, sitten **Tuo rivimääritys**- tai **Vie rivimääritys** -toiminto sen mukaan, mitä halutaan tehdä.

## Katso myös

[Sarakemääritykset taloushallinnon raportoinnissa](bi-column-definitions.md)  
[Taloushallinnon raportoinnin valmisteleminen](bi-how-work-account-schedule.md)  
[Taloushallinnon liiketoimintatiedot](bi.md)  
[Taloushallinto](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
