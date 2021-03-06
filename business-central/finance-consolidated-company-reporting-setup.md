---
title: Määritä yrityksen konsolidointi
description: Tietoja siitä, miten voit määrittää, miten eri yritysten tiedot Business Centralissa raportoidaan konsolidointiyritykseen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: e18566a05a9580c53329d95f52a6e197807e30b3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786246"
---
# <a name="set-up-company-consolidation"></a>Määritä yrityksen konsolidointi

Ennen kuin voit konsolidoida kahden tai useamman erillisen yrityksen (tytäryritysten) pääkirjanpidon tapahtumat konsolidoituun yritykseen, sinun täytyy valmistella tilikartat ja konsolidointiyritys.  

Yritysten monimutkaisuus määrittää, kumpaa tapaa käytetään konsolidoinnin määrittämiseen:

* Jos et tarvitse lisäasetuksia, kuten vain osittain omistamasi yrityksen sisällyttämistä, voit määrittää konsolidoinnin nopeasti käyttämällä ohjattua **Yrityksen konsolidointi** -määritystä. Opas auttaa suorittamaan perusvaiheet.
* Jos tarvitset lisäasetuksia, voit määrittää konsolidoidun yrityksen ja liiketoimintayksiköt itse.
  * Määritä, mitkä kunkin liiketoimintayksikön pääkirjanpidon tilit sisällytetään konsolidointiin, sekä konsolidoinnin muuntomenetelmän määrittäminen kullekin tilille.
  * Määritä liiketoimintayksikön kortti kullekin konsolidointiin sisällytettävälle yritykselle konsolidoidussa yrityksessä. Liiketoimintayksikön kortin tietoihin kuuluvat esimerkiksi liiketoimintayksikön tilikauden päivämäärät, kunkin konsolidointiin sisällytettävän tilin prosenttiosuus, joka tulee sisällyttää konsolidointiin.

## <a name="simple-consolidation-setup"></a>Yksinkertaiset konsolidoinnin asetukset

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Jos kyse on suoraviivaisesta konsolidoinnista, koska esimerkiksi omistat kokonaan konsolidoitavat liiketoimintayksiköt, ohjattu **Yrityksen konsolidointi** -määritys auttaa seuraavissa vaiheissa:

* Valitse, luodaanko uusi konsolidoitu yritys vai konsolidoidaanko tiedot yritykseen, joka on jo luotu konsolidointia varten. Yrityksessä ei saa olla tapahtumia.
* Esikatsele tulokset. [!INCLUDE[prod_short](includes/prod_short.md)] varmistaa, että päätiedot ja tapahtumat voidaan siirtää konsolidoituun yritykseen.

Käytä asetusten ohjattua määritystä seuraavasti:

1. Valitse **kirjanpitäjän** roolikeskuksessa **Asetusten ohjattu määritys** -toiminto.
2. Valitse **Määritä konsolidoinnin raportointi** ja tee vaiheet asetusten ohjatun määrityksen mukaisesti.

## <a name="advanced-consolidation-setup"></a>Konsolidoinnin lisäasetukset

Jos konsolidoinnissa on käytettävä lisäasetuksia, voit määrittää konsolidoinnin manuaalisesti. Sinulla voi esimerkiksi olla yrityksiä, jotka omistat vain osittain, tai et ehkä halua sisällyttää tiettyjä yrityksiä konsolidointiin.  

### <a name="set-up-the-consolidated-company"></a>Määritä konsolidoitu yritys

Ensin tulee määrittää konsolidoitu yritys. Konsolidoitu yritys määritetään samalla tavalla kuin muutkin yritykset. Lisätietoja on ohjeaiheessa [Valmistautuminen liiketoimintaan](ui-get-ready-business.md).  

Seuraavassa luettelossa havainnollistetaan konsolidoidun yrityksen keskeiset piirteet.

1. Tilikartan määrittäminen

    Lisätietoja on kohdassa [Tilikartan määrittäminen tai muuttaminen](finance-setup-chart-accounts.md).  

    Tilikartat voivat olla identtisiä liiketoimintayksikön ja konsolidoidun yrityksen välillä, tai konsolidoidulla yrityksellä voi olla eri tilikartta. Jos liiketoimintayksikön tilikartta poikkeaa konsolidoidun yrityksen tilikartasta, sinun täytyy määrittää liiketoimintayksikön tilit -kohdan linkitys. Lisätietoja on [Pääkirjanpitotilin valmisteleminen konsolidointia varten](#glacc) -osassa.

2. Lisää liiketoimintayksiköt

    Kun haluat yhdistää useamman yrityksen finanssitietoja konsolidoidussa yrityksessä, sinun täytyy syöttää tietoja tytäryrityksistä yritykseen tulevina liiketoimintayksikköinä ja siitä, mitä lukuja näistä yrityksistä otetaan mukaan.

    Lisä tietoja on [Liiketoimintayksiköiden lisääminen](#busunit) -osassa.
3. Liiketoimintayksiköiden kondolidoinnin yhteydessä voit määrittää vaihtokurssit, mikäli tilinpäätökset ovat ulkomaisena valuuttana.

    Ohjelman käyttämät kolme vaihtokurssia ovat **Keskikurssi (manuaalinen)**, **Loppukurssi** ja **Viimeinen loppukurssi**. Lisätietoja on [konsolidointien vaihtokurssien määrittäminen](#exchrates) -osassa.
4. Voit konsolidoida dimensiotietoja samoin kuin KP-tilejäkin.

    Lisätietoja on kohdassa [Sisällytä tai jätä pois dimensiot](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Lisää liiketoimintayksiköt

Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]issa konsolidoitavien liiketoimintayksiköiden luettelon, tarkistaa laskentatiedot ennen konsolidointia, tuoda tiedostoja ja luoda konsolidointiraportteja.  

1. Kirjaudu konsolidoituun yritykseen.
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoimintayksiköt** ja valitse sitten liittyvä linkki.  
3. Valitse **Uusi** ja täytä sitten tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Kun täytät **Aloituspvm**- ja **Lopetuspvm** -kentät, varmista, että noudata kenttiä, varmista, että noudatat liiketoimintayksikön eikä emoyrityksen tilikausien GAAP-sääntöjä.
4. Toista vaihe 3 jokaisen uuden liiketoimintayksikön osalta.

Jos liiketoimintayksikkösi käyttää ulkomaan valuuttaa, sinun on määritettävä konsolidoinnissa käytettävä valuuttakurssi. Sinun täytyy myös syöttää konsolidointitiedot liiketoimintayksikön KP-tileistä. Nämä prosessit käsitellään seuraavissa osissa.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Valmistele kirjanpitotilit konsolidointia varten

Konsolidoitavan yrityksen tilikartan on määritettävä konsolidoinnissa käytettävät tilit. Kunkin yrityksen kullekin KP-tilille on määritettävä konsolidoidun yrityksen KP-tili, jolle saldo siirretään konsolidoitaessa. Tämä linkitys mahdollistaa sellaisten yritysten konsolidoinnin, joilla on eri tilikartat.

Jos liiketoimintayksikön tilikartta poikkeaa konsolidoidun yrityksen tilikartasta, kirjanpitotilit on valmisteltava konsolidointia varten. Voit määrittää tilit, joihin debet- ja kreditsummat kirjataan, ja menetelmän, jolla valuutat muunnetaan konsolidoidussa yrityksessä. Tästä on hyötyä esimerkiksi silloin, jos raportti suoritetaan usein.

1. Valitse jokaisen liiketoimintayksikön [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
2. Avaa tilin kortti ja täytä **Konsolidointi**-pikavälilehden kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Määritä valuutan vaihtokurssit konsolidoiduissa yrityksissä

Jos liiketoimintayksikön käyttämä valuutta ei ole sama kuin konsolidoidun yrityksen käyttämä valuutta, kullekin tilille on määritettävä vaihtokurssimenetelmä ennen konsolidointia. Kunkin tilin **Konsolid. muuntomenetelmä** -kentän sisältö määrittää vaihtokurssin. Määritä konsolidoidussa yhtiössä kunkin liiketoimintayksikön **Valuutan vaihtok.taulu** -kentässä, käytetäänkö konsolidoinnissa liiketoimintayksikön vai konsolidoidun yrityksen vaihtokursseja. Jos käytät konsolidoidun yrityksen vaihtokursseja, voit muuttaa liiketoimintayksikön vaihtokursseja. Jos liiketoimintayksikön kortin **Valuutan vaihtok.taulu** -kentässä on arvo **Paikallinen**, voit muuttaa vaihtokurssia liiketoimintayksikön kortista. Vaihtokurssit kopioidaan **Valuutan vaihtokurssi** -taulukosta, mutta voit muuttaa niitä ennen konsolidointia.

Seuraavassa taulukossa käsitellään tileillä käytettäviä vaihtokurssimenetelmiä.

|Vaihtokurssi | Tyypillinen käyttö |
|---|---|
|Keskikurssi (manuaalinen) | Konsolidoitavan jakson keskikurssi lasketaan manuaalisesti. Laske keskikurssi joko aritmeettisena keskiarvona tai parhaana arvioina ja määritä kunkin liiketoimintayksikön tulos. Käytetään tuloslaskelmatileillä.|
|Loppukurssi | Käytetään tasetileillä.|
|Viimeinen loppukurssi | Valuuttamarkkinoiden kurssi päivämääränä, jona tasetta tai tuloslaskelmaa valmistellaan. Käyttäjä antaa tämän kurssin kullekin liiketoimintayksikölle. Käytetään tasetileillä.|
|Historiallinen kurssi | Vaihtokurssi tapahtuman suoritusajankohtana.|
|Yhdistelmäkurssi | Kuluvan jakson summat muunnetaan keskikurssin mukaan ja lisätään aiemmin kirjattuun saldoon konsolidoidussa yrityksessä. Tätä tapaa käytetään tavallisesti edellisten tilikausien voittojen tileissä, koska ne sisältävät eri jaksojen summia ja ovat siksi eri vaihtokurssien mukaan muunnettujen summien yhdistelmiä.|
|Pääomakurssi | Tämä kurssi muistuttaa **yhdistelmäkurssia**. Erot kirjataan erillisille kirjanpitotileille.|

Liiketoimintayksiköiden vaihtokurssit määritetään seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liiketoimintayksiköt** ja valitse sitten liittyvä linkki.  
2. Valitse ensin **Liiketoimintayksiköiden luettelo** -sivulla liiketoimintayksikkö ja sitten **Keskikurssi (manuaalinen)** -toiminto.  
3. **Muuta vaihtokurssi** -sivun **Suhteellinen vaihtokurssi** -kentän sisältö on kopioitu **Valuutan vaihtokurssi** -taulukosta. Sisältöön voi kuitenkin tehdä muutoksia. Sulje sivu.  
4. Valitse **Loppukurssi**-toiminto.  
5. Anna vaihtokurssi **Suhteellinen vaihtokurssisumma** -kentässä

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Dimensioiden sisällyttäminen tai jättäminen pois

Voit konsolidoida dimensiotietoja samoin kuin KP-tilejäkin.

* Määrittele asianomaisissa dimensioissa **Konsolidointikoodi** -kenttä tai jätä se tyhjäksi
  * Jos haluat sulkea dimension pois konsolidoinnista, jätä **Dimension konsolidointikoodi** -kenttä tyhjäksi äläkä valitse dimensioita konsolidointifunktioiden tai -raporttien **Kopioi dimensiot** -kentissä.
  * Jos haluat sisällyttää dimensiotiedot konsolidointiin, jätä **Konsolidointikoodi**-kenttä tyhjäksi. Konsolidointi kuitenkin onnistuu vain, jos liiketoimintayksikön dimensiotiedot ovat täsmälleen samat kuin konsolidoidulla yrityksellä.
  * Konsolidoi dimension arvokoodi liiketoimintayksikössä eri dimension arvokoodilla konsolidoidussa yrityksessä täyttämällä asiaankuuluvien dimensioiden **Konsolidointikoodi**-kenttä.  
* Lisää asiaankuuluvat dimensiot asianmukaisiin kirjanpitotileihin

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Jätä yritys konsolidoinnin ulkopuolelle

Jos et halua sisällyttää liiketoimintayksikköä konsolidointiin, voit jättää sen pois. Se onnistuu siirtymällä liiketoimintayksikön korttiin ja poistamalla **Konsolidoi**-valintaruudun valinta.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Sisällytä osittain omistettu yritys konsolidointiin

Jos omistat osan yrityksestä, voit sisällyttää kustakin tapahtumasta sen prosenttiosuuden, joka vastaa omistamaasi osuutta yrityksestä. Jos esimerkiksi omistat yrityksestä 70 prosenttia, konsolidointiin sisältyy lasku 70 dollaria 100 dollarin laskusta. Voit määrittää omistusosuuden yrityksestä siirtymällä liiketoimintayksikön korttiin ja antamalla prosenttiosuuden **Konsolidointi-%** -kentässä.  

## <a name="see-also"></a>Katso myös

[Usean yrityksen kirjanpitotietojen konsolidoiminen](finance-consolidated-company-reporting.md)  
[Konsernitapahtumien hallinta](intercompany-manage.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Liiketoimintatietojen vienti Exceliin](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]