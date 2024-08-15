---
title: Maksujen suorittaminen AMC-pankkitoiminnolla (US) tai SEPA-hyvityksen siirrolla (EU)
description: Käsittele maksut toimittajille viemällä tiedosto (EFT) yhdessä maksutietojen kanssa päiväkirjan riveiltä.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 07/17/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Maksujen suorittaminen AMC pankki 365 peruslaajennuksella tai SEPA-hyvityksen siirrolla

 **Maksupäiväkirjat-sivulla** voit käsitellä toimittajille suoritettavia maksuja viemällä tiedoston sekä maksutiedot päiväkirjan riveiltä. Voit sitten ladata tiedoston verkkopankkiin, jossa liittyvät rahansiirrot käsitellään. [!INCLUDE[prod_short](includes/prod_short.md)] tukee SEPA-hyvityksen siirto -muotoa, mutta omassa maassasi/alueellasi saattaa olla muita elektronisten maksujen muotoja.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]in yleisessä versiossa asetetaan ja yhdistetään yleiset palvelut pankkitietojen muuntamiseen mihin tahansa pankkisi vaatimaan muotoon. Pohjois-Amerikan versioissa samaa palvelua voi käyttää maksutiedostojen lähettämiseen sähköisenä rahansiirtona (EFT), esimerkkinä usein käytetty ACH-verkko (Automated Clearing House), joskin prosessi on hieman erilainen. Lisätietoja on kohdan [Maksujen vienti pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file) vaiheessa 6.  

 Kun haluat ottaa SEPA-hyvityksen siirrot käyttöön, määritä ensin pankkitili, toimittaja ja yleinen päiväkirja, johon maksupäiväkirja perustuu. Tämän jälkeen toimittajille suoritettavia maksuja valmistellaan täyttämällä **automaattisesti Maksupäiväkirjat-sivulle** erämaksut määritetyillä kirjauspäivämäärillä.  

> [!NOTE]  
> Kun olet varmistanut, että pankki on käsitellyt maksut onnistuneesti, voit jatkaa maksupäiväkirjan rivien kirjaamista.  

## AMC Banking 365 Fundamentals -laajennuksen määrittäminen

Voit aktivoida AMC Banking 365 Fundamentals -laajennuksen, jolla voi muuntaa minkä tahansa pankin tiliotteen tuotavaan muotoon, tai voit muuttaa viedyt maksutiedostot pankin edellyttämään muotoon. Lisätietoja on kohdassa [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md).

## SEPA-hyvityksen siirron määrittäminen

 **Maksupäiväkirjat-sivulta** voit viedä maksuja tiedostoon, joka on tarkoitus ladata sähköiseen pankkiin liittyvien rahansiirtojen käsittelyä varten. [!INCLUDE[prod_short](includes/prod_short.md)] tukee SEPA-hyvityksen siirto -muotoa, mutta omassa maassasi/alueellasi saattaa olla muita elektronisten maksujen muotoja.  

Tietojen vaihdon kehystä käyttämällä voit ottaa käyttöön sellaisten pankin tiedostomuotojen viennin, joita ei tueta ruudusta [!INCLUDE[prod_short](includes/prod_short.md)]. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

Ennen kuin voit käsitellä maksun sähköisesti viemällä maksutiedostot SEPA-hyvityksen siirto -muodossa, sinun on suoritettava seuraavat asetukset:  

* Määritä kyseinen pankkitilin käsittelemään SEPA-hyvityksen siirtomuoto  
* Määritä toimittajan kortit, jotta voit käsitellä maksut viemällä tiedostot SEPA-hyvityksen siirtomuotoon  
* Määritä liittyvä yleisen päiväkirjan erä, joka ottaa maksuviennin **käyttöön Maksupäiväkirjat-sivulta** .  
* Yhdistä vähintään yhden maksutyypin tiedonsiirtomääritys liittyvään maksutapaan  

> [!NOTE]
> Business Central tukee sekä SEPA-muotoista CT-kipua.001.001.03 että TT-kipua.001.001.09. Voit valita minkä tahansa muodon Pankkitilin **kortti**  sivulla.  
> [!TIP]
> Tämä artikkeli koskee yleistä [!INCLUDE [prod_short](includes/prod_short.md)] -versiota. Omassa maassa tai omalla alueella eri sivuille on voitu lisätä muita pakollisia kenttiä. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### Pankkitilin määrittäminen SEPA-hyvityksen siirtoa varten

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilit** ja valitse sitten vastaava linkki.  
2. Avaa sen pankkitilin kortti, jolta viet maksutiedostot SEPA-hyvityksen siirto -muodossa.  
3. Valitse Tilinhaltija-pikavälilehden **·**  **Maksun vientimuoto** -kentässä sePA-muoto, jota haluat käyttää.  
4. Valitse **Yleiset**-pikavälilehden **Hyvityksen siirtoviestinrot** -kentässä numerosarja, josta numerot määritetään SEPA-tilisiirtotapahtumiin.  
5. Varmista, että **IBAN**-kenttä on täytetty.  

    > [!NOTE]  
    > **Valuuttakoodi**-kentän asetuksena on oltava **EUR**, koska SEPA-hyvityksen siirrot voidaan tehdä vain euroina.  

### Toimittajan kortin määrittäminen SEPA-hyvityksen siirtoa varten

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten vastaava linkki.  
2. Avaa sen toimittajan kortti, josta maksat sähköisesti viemällä maksutiedostot SEPA-hyvitys siirtomuodossa.  
3. Valitse **Maksut-pikavälilehden**  **Maksutavan koodi** -kentässä **PANKKI**.  
4.  **Valitse Ensisijainen pankkitili -** kentässä pankki, johon rahat siirretään, kun verkkopankkisi käsittelee ne.  

    Jos toimittajalle ei ole vielä määritetty pankkitietoja, se voidaan tehdä nyt. Lisätietoja on kohdassa [Toimittajan pankkitilien määrittäminen pankkitiedostojen vientiä varten](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). **Ensisijainen pankkitili** -kentän arvo kopioidaan **Maksupäiväkirja**-sivun **Vastaanottajan pankkitili** -kenttään.  

### Maksupäiväkirjan määrittäminen maksutiedostojen vientiä varten

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse **Erän nimi** -kentässä avattavan\- luettelon painike.  
3. Valitse **Yleisen päiväkirjan erät** -sivulla **Muokkaa luetteloa** -toiminto.  
4. Valitse maksupäiväkirjan rivillä, jota aiot käyttää maksujen viemiseen, **Salli maksuvienti -** valintaruutu.  

### Vähintään yhden maksutyypin tiedonsiirtomäärityksen yhdistäminen liittyvään maksutapaan

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksutavat** ja valitse sitten vastaava linkki.  
2. Valitse **Maksutavat**-sivulla ensin maksutapa, jolla maksut viedään, ja sitten **Maksun vientirivin määritys** -kenttä.  
3. Valitse **Maksun vientirivin määritykset** -sivulla koodi, jonka määritit **Rivimääritykset**-pikavälilehden **Koodi**-kentässä ohjeaiheen [Tiedonsiirtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md) Tiedoston rivien ja sarakkeiden muotoilun kuvaaminen -kohdan vaiheessa 4.  

## Maksupäiväkirjan valmistelu

Täytä maksupäiväkirja toimittajiin kohdistuvilla erääntyvillä maksuriveillä ja vaihtoehdolla lisätä kirjauspäivämäärät perustuen liittyvien ostoasiakirjojen eräpäivään. Lisätietoja on kohdassa [Ostovelkojen hallinta](payables-manage-payables.md).

## Maksujen vienti pankkitiedostoon

Kun olet valmis suorittamaan maksuja toimittajille tai työntekijöillesi karttoja, voit viedä tiedoston, jossa on maksutiedot Maksupäiväkirjat-sivun **riveillä** . Voit sitten ladata tiedoston pankkiin kyseisten rahansiirtojen käsittelyä varten.

AMC Banking 365 Fundamentals -laajennus on saatavana [!INCLUDE[prod_short](includes/prod_short.md)]in yleisessä versiossa. Pohjoisamerikkalaisessa versioissa maksutiedostot voidaan lähettää samalla laajennuksella sähköisenä rahansiirtona, joskin prosessi on hieman erilainen. Lisätietoja on kohdan [Maksujen vienti pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file) vaiheessa 6.

> [!NOTE]  
> Määritä liittyvän pankkitilin sähköinen muoto ennen maksutiedostojen vientiä maksupäiväkirjasta ja ota AMC Banking 365 Fundamentals -laajennus käyttöön. Lisätietoja on kohdissa [Pankkitilin määrittäminen](bank-how-setup-bank-accounts.md) ja [AMC Banking 365 Fundamentals -laajennuksen käyttäminen](ui-extensions-amc-banking.md). Valitse myös **Salli maksun vienti** -valintaruutu **Yleisen päiväkirjan erät** -sivulla. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  

Voit tarkastella maksupäiväkirjasta vietyjä maksutiedostoja **Hyvityksen siirron rekisterit** -sivulla. Voit myös viedä sivulla maksutiedostot uudelleen, jos tekniset virheet tai tiedostomuutokset vaativat sitä. Huomaa kuitenkin, että viedyt EFT-tiedostot eivät näy tällä sivulla, eikä niitä voi viedä uudelleen.  

### Maksujen vienti pankkitiedostoon

Seuraavassa kuvataan, miten toimittajalle maksetaan sekillä. Vaiheet ovat samankaltaiset kuin hyvitettäessä asiakkaalle sekkimaksuna.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupäiväkirjat** ja valitse sitten vastaava linkki.
2. Täytä maksupäiväkirjan rivit. Lisätietoja on ohjeaiheessa [Maksujen ja hyvitysten kirjaaminen](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Jos käytät sähköistä rahansiirtoa, sinun on valittava joko **Sähköinen maksu** tai **Sähköinen maksu – IAT** **Pankkimaksun tyyppi** -kentässä. Eri tiedostojen vientipalvelut ja niiden tiedostomuodot edellyttävät erilaisia asetuksia **Pankkitilin kortti**- ja **Toimittajan pankkitilin kortti** -sivuilla. Saat ilmoituksen virheellisistä tai puuttuvista asetusarvoista, kun yrität viedä tiedoston.
    >
    > EFT-ominaisuutta voi käyttää vain pankkitileille, jotka on määritetty paikallisena valuuttana. Sitä ei voi käyttää ulkomaan valuutalle, mikä ilmaistaan **Valuutan koodi** -kentässä olevalla arvolla. (Tyhjä kentän arvo tarkoittaa paikallista valuuttaa.)

3. Kun kaikki maksupäiväkirjan rivit ovat valmiit, valitse **Vie**-toiminto.
4. Täytä **Vie sähköiset maksut** -sivun kentät tarpeen mukaan.

    Virheilmoituksia näkyy **Maksutiedoston virheet** -tietoruudussa, jossa voit myös nähdä yksityiskohtaiset tiedot virheviestistä. Kaikki virheet on ratkaistava ennen maksutiedoston vientiä.

    > [!TIP]  
    > AMC Banking 365 Fundamentals -laajennusta käytettäessä yleinen virhesanoma ilmaisee, että pankkitilin numeron pituus ei täytä pankin vaatimuksia. Voit välttää tämän virheen tai ratkaista sen poistamalla **IBAN**-kentän **Pankkitilin kortti** -sivulla ja antamalla sitten pankkitilin numeron **Pankkitilin nro** -kentässä pankin edellyttämässä muodossa.

5. Määritä **Tallenna nimellä** -sivulla paikka, johon tiedosto viedään, ja valitse sitten **Tallenna**.

    > [!NOTE]  
    > Jos käytät sähköistä rahansiirtoa, tallenna saatava toimittajan maksusuorituslomake Word-asiakirjana tai valitse sen lähettäminen suoraan toimittajalle. Maksut on nyt lisätty **Luo sähköinen rahansiirtotiedosto** -sivulle, jossa voit luoda samanaikaisesti useita maksutilauksia, mikä säästää lähetyskustannuksia. Lisätietoja on seuraavissa vaiheissa:
6. Valitse **Maksupäiväkirjat-sivulta**  **Luo EFT-tiedosto** -toiminto.

    **Luo sähköinen rahansiirtotiedosto** -sivulla kaikki sähköistä rahansiirtoa varten määritetyt maksut, jotka on viety maksupäiväkirjasta määritetylle pankkitilille mutta joita ei ole vielä muodostettu, on mainittu **Rivit**-pikavälilehdessä.
7. Vie kaikki sähköiset rahansiirtomaksut sisältävä tiedosto valitsemalla **Luo sähköinen rahansiirtotiedosto** -toiminto.
8. Määritä **Tallenna nimellä** -sivulla paikka, johon tiedosto viedään, ja valitse sitten **Tallenna**.

Pankin maksutiedosto viedään määrittämääsi sijaintiin ja voit jatkaa sen lataamista verkkopankkitilille ja suorittaa todelliset maksut. Voit sitten kirjata viedyn maksupäiväkirjan rivit.

### Vietyjen maksujen kirjaamisajankohdan suunnitteleminen

Jos et halua kirjata vietyä maksua varten maksupäiväkirjan riviä esimerkiksi siksi, että odotat vahvistusta, että pankki on käsitellyt kauppatapahtuman, voit vain poistaa päiväkirjan rivin. Kun luot myöhemmin maksupäiväkirjan rivin, jolla maksetaan jäljellä oleva laskun summa, **Viety summa yhteensä** -kenttä näyttää, kuinka paljon maksun summasta on jo viety. Lisäksi saat lisätietoja viedystä kokonaissummasta valitsemalla **Hyvityksen siirron rekisterimerkinnät** -painikkeen, joka avaa vietyjen maksutiedostojen tiedot.

Jos noudatat prosessia, jossa et kirjaa maksuja ennen kuin olet vahvistanut, että ne on käsitelty pankissa, voit hallita niitä kahdella tavalla.

* Maksupäiväkirjassa, jossa on ehdotettuja maksurivejä, voit lajitella joko **Viety maksutiedostoon** -sarakkeen tai **Viety kokonaissumma** -sarakkeen ja poistaa sitten maksuehdotukset avoimista laskuista, joiden maksut on jo suoritettu etkä halua suorittaa maksuja.
*  **Ehdota toimittajamaksuja -** sivulla, jossa määrität, mitkä maksut lisätään maksupäiväkirjaan, voit valita **Ohita viedyt maksut -** valintaruudun, jos et halua lisätä päiväkirjarivejä jo vietyihin maksuihin.

Saat lisätietoja viedyistä maksuista valitsemalla **Maksujen vientihistoria** -toiminnon.

### Maksujen vieminen uudelleen pankkitiedostoon

Voit viedä maksutiedostot uudelleen **Hyvityksen siirron rekisterit** -sivulla. Ennen kuin poistat tai kirjaat maksupäiväkirjan rivejä, voit myös viedä maksutiedoston **uudelleen Maksupäiväkirjat-sivulta** viemällä sen uudelleen. Jos poistat tai kirjaat maksupäiväkirjan rivit viennin jälkeen, voit viedä saman maksutiedoston **uudelleen Kredit-siirtorekisterit-sivulta** . Valitse rivi tilisiirtojen erälle, jonka haluat viedä uudelleen, ja käyttämällä sitten **Vie maksut uudelleen tiedostoon** -toimintoa.

> [!NOTE]  
> Viedyt sähköiset rahansiirtotiedostot eivät näy **Hyvityksen siirron rekisterit** -sivulla, eikä niitä voi viedä uudelleen.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyvityksen siirron rekisterit** ja valitse sitten vastaava linkki.
2. Valitse ensin uudelleenvietävä maksun vienti ja sitten **Vie maksut uudelleen tiedostoon** -toiminto.

## Maksujen kirjaaminen

Kirjaa maksut sen jälkeen, kun pankki on käsitellyt ne onnistuneesti. Lisätietoja on kohdassa [Maksujen suorittaminen](payables-make-payments.md).

## Katso myös

[Käytä AMC Banking 365 Fundamentals -laajennusta](ui-extensions-amc-banking.md)  
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
