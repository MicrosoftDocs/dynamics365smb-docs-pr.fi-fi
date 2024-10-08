---
title: Perustöiden vaihekuvaus
description: Tässä artikkelissa käsitellään useita projektinhallinnan ydinprosesseja.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="walkthrough-of-basic-jobs"></a>Perustöiden vaihekuvaus

Tässä vaihekuvauksessa kuvataan useita ydinprosesseja:

- Projektitehtävien lisääminen projekteihin
- Projektin aika- ja materiaalikustannusten kirjaaminen
- Projektien laskutus

## <a name="adding-a-project-task"></a>Projektitehtävän lisääminen

### <a name="scenario"></a>Skenaario

Projektipäällikkö Simon haluaa kirjata espressokoneen käytön opettamiseen kuluneen ajan. Simon haluaa käyttää erillistä projektin tehtävää kaupallisen laitteen asentamiseen asiakkaan tiloihin.

### <a name="steps"></a>Vaiheet

1. Projektitehtävän luominen.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
    2. Valitse työ *J00010*.
    3. Valitse **Tehtävät**-alueella **Uusi rivi** -toiminto ja syötä seuraavat arvot:
 
    |Projektitehtävän nro|Kuvaus|Projektitehtävän tyyppi|
    |------------|-----------|-------------|  
    |220|Asiakaskoulutus|Kirjaus|

2. Projektitehtävien sisennys.
   1. Etsi **Sisennä projektitehtävät** -toiminto Tehtävät-alueella.
   2. Vahvista tehtävien sisennys valitsemalla **Kyllä**.

### <a name="results"></a>Tulokset

 - Nyt aika ja kulut voidaan tallentaa uuteen projektitehtävään

## <a name="record-time-and-material-expenses-to-a-project"></a>Aika- ja materiaalikustannusten kirjaaminen projektille

### <a name="scenario-1"></a>Skenaario

Koneen asentavan teknikko Edginin on kirjattava projektin asennukseen käytetty aika ja materiaalit laskutusta varten. Edgin on jo lisännyt matkat ja materiaalit, ja nyt on lisättävä aika, joka käytetään koneen käytön opettamiseen henkilöstölle.

### <a name="steps-1"></a>Vaiheet

1. Luo projektipäiväkirjaan lisää rivejä.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
    2. Valitse erä *CONTOSO*. Resurssi- ja Nimike-tyyppisistä riveistä näkyy useita rivejä, jotka kuvastavat käytettyä aikaa (teknikko ja ajoneuvo) sekä käytettyjä materiaaleja (kone ja tarvikkeet).
    3. Luo uusi rivi ja syötä seuraavat arvot:
 
    |Projektin nro|Projektitehtävän nro|Tyyppi|Nro|Kuvaus|Määrä|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Resurssi|EDGIN|Asiakaskoulutus|1|

2. Kirjaa aika ja kustannukset.
   1. Valitse **Kirjaa**-toiminto.
   2. Vahvista rivien kirjaaminen valitsemalla **Kyllä**.

### <a name="results-1"></a>Tulokset

- *Käyttö*-tyyppiset projektitapahtumat ja resurssitapahtumat luodaan.
- Nimiketapahtumat luodaan varaston negatiivista muuttamista varten.
- Projektikortin Tehtävät-alueen kustannukset ja hinnat vastaavat laskutettavaa uutta saldoa.
- Projektikortin projektin tietojen tietoruudussa näkyvät hintojen kokonaissummat.

## <a name="creating-a-sales-invoice-for-a-project"></a>Projektin myyntilaskun luominen

### <a name="scenario-2"></a>Skenaario

Simonin on luotava ja kirjattava asiakkaalle lähetettävä lasku, jossa on projektin aika ja kustannukset.

### <a name="steps-2"></a>Vaiheet

1. Luo myyntilasku.

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projekti** ja valitse sitten vastaava linkki.  
    2. Valitse projektiluettelossa **Luo projektin myyntilasku** -toiminto.
    3. Määritä **Projektin nro** -suodattimeksi *J00010*.
    4. Luo myyntilasku valitsemalla **OK**. Saat vahvistuksen siitä, kuinka monta laskua on luotu.

2. Kirjaa aika- ja kustannuslasku.

   1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.  
   2. Valitse viimeinen lasku, jos haluat avata sen tarkasteltavaksi.
   3. Valitse **Kirjaa**-toiminto.

### <a name="results-2"></a>Tulokset

- *Myynti*-tyyppiset projektitapahtumat ja resurssitapahtumat luodaan.
- Projektikortin tehtäväalueen kustannukset ja hinnat vastaavat uusia laskutettavia saldoja.
- Projektikortin projektin tietojen tietoruudussa näkyvät hintojen kokonaissummat Laskutetut hinnat -osassa.
