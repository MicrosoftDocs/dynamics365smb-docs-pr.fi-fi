---
title: Perustöiden vaihekuvaus
description: Tässä artikkelissa käsitellään useita projektinhallinnan ydinprosesseja.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-of-basic-jobs"></a>Perustöiden vaihekuvaus

Tässä vaihekuvauksessa kuvataan useita ydinprosesseja:

- Työtehtävien lisääminen töihin
- Työn aika- ja materiaalikustannusten kirjaaminen
- Työn laskuttaminen

## <a name="adding-a-job-task-to-a-job"></a>Työtehtävän lisääminen työhön

### <a name="scenario"></a>Skenaario

Projektipäällikkö Simon haluaa tallentaa ajan, joka kuluu asiakkaan kouluttamiseen espressokeitintuotteen käyttöön erilliseksi tehtäväksi kaupallisen koneen asennustyössä paikan päällä.

### <a name="steps"></a>Vaiheet

1. Työtehtävän luominen  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
    2. Valitse työ *J00010*.
    3. Valitse **Tehtävät**-alueessa **Uusi rivi** -toiminto.  Syötä seuraavat arvot:
 
    |Työtehtävänro|Kuvaus|Projektitehtävätyyppi|
    |------------|-----------|-------------|  
    |220|Asiakaskoulutus|Kirjaus|

2. Sisennä projektitehtävät
   1. Etsi Tehtävät-alueen **Sisennä projektitehtävät** -toiminto
   2. Vahvista, että haluat sisentää tehtäviä valitsemalla **Kyllä**.

### <a name="results"></a>Tulokset

 - Nyt aika ja kulut voidaan tallentaa uuteen projektitehtävään

## <a name="record-time-and-material-expenses-to-a-job"></a>Työn aika- ja materiaalikustannusten kirjaaminen

### <a name="scenario-1"></a>Skenaario

Koneen asentavan teknikon Edginin on kirjattava työhön asennuksen aikana käytetyt aika ja materiaalit laskutusta varten.  Hän on jo lisännyt matkat ja materiaalit, ja nyt on lisättävä aika, joka käytetään koneen käytön opettamiseen henkilöstölle.

### <a name="steps-1"></a>Vaiheet

1. Projektipäiväkirjan lisärivien luominen

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
    2. Valitse erä *CONTOSO*.  Resurssi- ja Nimike-tyyppisistä riveistä näkyy useita rivejä, jotka kuvastavat käytettyä aikaa (teknikko ja ajoneuvo) sekä käytettyjä materiaaleja (kone ja tarvikkeet).
    3. Luo uusi rivi. Syötä seuraavat arvot:
 
    |Työnro|Työtehtävänro|Tyyppi|Nro|Kuvaus|Määrä|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Resurssi|EDGIN|Asiakaskoulutus|1|

2. Ajan ja kustannuksen kirjaaminen
   1. Valitse **Kirjaa**-toiminto
   2. Vahvista, että haluat kirjata rivit valitsemalla **Kyllä**.

### <a name="results-1"></a>Tulokset

 - *Käyttö*-tyyppiset projektitapahtumat ja resurssitapahtumat luodaan
 - Nimiketapahtumat luodaan, jotta varastoa voitaisiin muuttaa negatiivisesti
 - Projektikortin Tehtävät-alueen kustannukset ja hinnat vastaavat laskutettavaa uutta saldoa
 - Projektikortin projektin tietojen tietoruudussa näkyvät hintojen kokonaissummat

## <a name="creating-a-sales-invoice-for-a-job"></a>Projektin myyntilaskun luominen

### <a name="scenario-2"></a>Skenaario
Simonin on luotava ja kirjattava asiakkaalle lähetettävä lasku, jossa on projektin aika ja kustannukset.

### <a name="steps-2"></a>Vaiheet
1. Luo myyntilasku

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
    2. Valitse Projektit-luettelosta **Luo projektin myyntilasku** -toiminto.
    3. Määritä **projektinro** -suodattimen arvoksi *J00010*.
    4. Luo myyntilasku valitsemalla **OK**.  Saat vahvistuksen siitä, kuinka monta laskua on luotu

2. Ajan ja kustannuslaskun kirjaaminen
   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.  
   2. Valitse viimeinen lasku, jos haluat avata sen tarkasteltavaksi.
   3. Valitse **Kirjaa**-toiminto.

### <a name="results-2"></a>Tulokset

 - *Myynti*-tyyppiset projektitapahtumat ja resurssitapahtumat luodaan
 - Projektikortin Tehtävät-alueen kustannukset ja hinnat vastaavat laskutettavaa uutta saldoa
 - Projektikortin projektin tietojen tietoruudussa näkyvät hintojen kokonaissummat Laskutetut hinnat -osassa
