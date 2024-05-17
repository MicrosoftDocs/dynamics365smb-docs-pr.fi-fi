---
title: Kestävyystapahtumien tallentaminen
description: Tietoja kasvihuonekaasupäästöjen (GHG) kirjauksesta.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Kestävyystapahtumien tallentaminen  

Tällä hetkellä ainoa tapa kirjata GHG-päästöjä **kestävyyskirjauksiin** on käyttää **kestävyyspäiväkirjoja**.   

## Vastuullisuuspäiväkirja  

**Vastuullisuuspäiväkirjat** on suunniteltu seuraamaan ja tallentamaan kestävyyteen liittyviä toimia käyttäen samaa käyttökokemusta kuin muissakin Business Centralin päiväkirjoissa. Päiväkirjassa käyttäjillä on mahdollisuus syöttää päästöjä manuaalisesti, jos heillä on tarvittavat tiedot. Vaihtoehtoisesti, jos heiltä puuttuu nämä tiedot, he voivat käyttää sisäisiä kaavoja laskeakseen päästöjä tarkasti tiettyjen tunnettujen parametrien perusteella, jotka vastaavat eri tyyppisiä lähteitä ja tilejä. 

Päiväkirjaan lisäämäsi tiedot ovat väliaikaisia, ja niitä voidaan muuttaa niiden ollessa päiväkirjassa. Kun kirjaat päiväkirjan, tiedot siirretään **Kestävyyskirjanpitotapahtumiin** yksittäisiin **kestävyystileihin**, missä niitä ei voi muuttaa. Voit kuitenkin kirjata peruuttavia tai korjaavia tapahtumia.  

### Päiväkirjan mallien ja erien käyttäminen 

Ohjelmassa on oletusarvoisesti kaksi **kestävyyspäiväkirjan mallia**, vakiomalli ja toistuva malli. Voit määrittää kullekin päiväkirjan mallille oman henkilökohtaisen päiväkirjan päiväkirjan eränä. Tämä edellyttää, että valitset **Erät**-toiminnon **Kestävyyspäiväkirjan mallit** -sivulla ja luot uuden **kestävyyspäiväkirjan erän** uudelle sivulle. Voit esimerkiksi määrittää oman päiväkirjan erän kullekin päästöjen vaikutusalueelle käyttämällä **Päästöjen laajuus** -vaihtoehtoa, jossa voit valita kolmesta olemassa olevasta vaikutusalueesta. Voit myös lisätä tai muuttaa **lähdekoodia** ja **syykoodia** kunkin erän osalta. 

>[!TIP]
>Kullekin päästötyypille voi olla yksi päiväkirjan erä, jos rivejä on monta, koska se voi vähentää virheiden mahdollisuutta, mutta voit myös käyttää yleistä erää kaikentyyppisille päästöille.   

### Kestävyyspäiväkirjojen arviointi 

Voit ottaa taustatarkistuksen käyttöön **Kestävyyden asetuksissa**, mikä auttaa estämään viiveet kirjauksessa. Merkki ilmoittaa sinulle, kun käsittelemäsi **Kestävyyspäiväkirjassa** on virhe ja se estää sinua kirjaamasta päiväkirjaa.  

Kun oikeellisuustarkistus otetaan käyttöön, **päiväkirjan tarkistuksen** -tietoruudussa näkyvät tämän rivin ja koko erän seurantakohteet. Vahvistus tehdään silloin, kun lataat päiväkirjan erän ja kun valitset toisen päiväkirjarivin. Tietoruudun **Virheet yhteensä** -ruudussa näkyy [!INCLUDE [prod_short](includes/prod_short.md)]in löytämien virheiden kokonaismäärä, ja valitsemalla se voidaan avata virheiden yleiskatsaus. 

### Kestävyystapahtumien päiväkirjojen käyttäminen 

Voit aloittaa **kestävyyspäiväkirjojen** käytön noudattamalla seuraavia vaiheita:   

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyyspäiväkirjat** ja valitse sitten vastaava linkki. 
2. Voit syöttää niin monta riviä **Kestävyyspäiväkirja**-sivulle kuin aiot kirjata samalla erällä.  
3. **Asiakirjatyyppinä** voit säilyttää tyhjän vaihtoehdon tai käyttää **laskua** tai **hyvityslaskua**.  
4. **Tilinro**-kentässä voit valita vain **Kestävyystilit**, joilla on valittu **Suora kirjaus** -kenttä, **Kirjaus** **Kirjanpitotyypiksi** ja ei-suljettu tili. Tilit täytyy myös määrittää luokan ja alaryhmän avulla.  

>[!NOTE]
>Jos käytät erää, jossa päästöalue on määritetty, **Kestävyystilin** **Päästöjen laajuus** on oltava yhtä suuri kuin käytetyn erän **Päästöjen laajuus**.  

5. Vaihtoehtoja on kaksi: summat voi kirjata manuaalisesti tai käyttää kaavoja.   

    1. Jos sinulla on tarkat tiedot päästöistä, haluat kirjata sen (eli sinulla on se vastaanotetussa laskussa), sinun täytyy valita **Manuaalinen syöttö** -kenttä määrittääksesi, että summat syötetään manuaalisesti. Tässä tapauksessa tietoja ei voi täyttää **Polttoaine/Sähkö**-, **Etäisyys**-, **Mukautettu summa**-, **Asennuskerroin**- ja **Aikakerroin**-kentissä, koska niitä ei voi muokata tässä valinnassa. Mutta **Päästö CO2**, **Päästö CH4**- ja **Päästö N2O** -kentät ovat muokattavissa, ja voit täyttää tiedot suoraan siellä. 
    2. Jos et tiedä päästöjäsi tarkasti, sinun on laskettava se, etkä ole valinnut kenttää **Manuaalinen syöttö**, ja tässä tapauksessa **Päästöt CO2**, **Päästöt CH4**- ja **Päästöt N2O** -kenttiä ei voi muokata, mutta voit syöttää laskentatietosi käyttämäsi kaavan perusteella. Saat lisätietoja käytetyistä kaavoista, jotka on määritelty **Kestävyyden tilikategoria** -kohdassa, [kestävyystilien ja -kirjausten kaaviosta](finance-sustainability-accounts-ledger.md#account-categories).
    
7. Kirjaa päiväkirja valitsemalla **Kirjaa**-toiminto. Kun tapahtumia kirjataan **kestävyyspäiväkirjaan**, tapahtumat luodaan **kestävyyskirjauksiin**. 

Jos kaava perustuu **Kestävyystilin luokka** -taulukon **Laske pääkirjanpidosta** -vaihtoehtoon, sinun täytyy käyttää **Kerää summa KP-tapahtumista** -toimintoa ennen päiväkirjan kirjausta, kun haluat laskea päästöt tämän tietolähteen perusteella. Lisäksi jos olet tehnyt joitain muutoksia päästökertoimiin täytettyäsi päiväkirjan rivit, sinun täytyy valita **Laske uudelleen** -toiminto saadaksesi oikean summan päiväkirjaan.  

### Toistuvat kirjaukset 

**Kestävyyspäiväkirja** on yleinen päiväkirja, jossa on tiettyjä kenttiä sellaisten tapahtumien hallintaa varten, jotka kirjataan usein vähäisin muutoksin tai ilman muutoksia. Esimerkiksi kestävyystransaktioita, kuten sähkö-, lämpö- tai muita vastaavia transaktioita. Toistuvia päiväkirjoja käyttämällä voit kirjata kiinteitä ja muuttuvia summia. Toistuvan päiväkirjan avulla luot merkinnät, jotka kirjataan säännöllisesti vain kerran. Esimerkiksi tilit, dimensiot ja dimensioarvot säilyvät päiväkirjassa kirjaamisen jälkeen. Jos muutoksia tarvitaan, ne voidaan tehdä aina kirjauksen yhteydessä. 

**Toistotapa**-kenttä on tärkeä. Se määrittää, miten päiväkirjan rivin summaa käsitellään kirjauksen jälkeen. Jos esimerkiksi käytät samaa summaa joka kerta, kun kirjaat rivin, voit säilyttää summan, ja tässä tapauksessa kannattaa käyttää vaihtoehtona **F kiinteä**. Jos käytät rivillä samoja tilejä ja tekstiä, mutta summa vaihtelee kirjattaessa, voit valita sen vaihtoehdon, että summa poistuu riviltä kirjauksen jälkeen ja tässä tapauksessa valitset **Muuttuja V** -vaihtoehdon. 

Sinun tulee myös määrittää **Toistuvuuden tiheys** -kenttä, sillä tämä pvm-kaava-kenttä määrittää, kuinka usein tapahtuma kirjataan päiväkirjan riville, ja se tulee täyttää. Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#use-date-formulas).  

**Päättymispäivämäärä**-kenttä määrittää päivämäärän, jolloin rivi kirjataan viimeisen kerran. Riviä ei kirjata tämän päivämäärän jälkeen. **Päättymispäivämäärä**-kentän käyttämisessä on se etu, että rivi ei poistu päiväkirjasta heti. Voit syöttää myöhemmän päivämäärän, jotta voit käyttää riviä tulevaisuudessa. Jos kenttä on tyhjä, rivi kirjataan joka kerta, kunnes se poistetaan päiväkirjasta.  

## Katso myös  
[Rahoitus](finance.md)    
[Kestävän kehityksen hallinnan yleiskatsaus](finance-manage-sustainability.md)   
[Vastuullisuusmääritys](finance-sustainability-setup.md)   
[Kestävyystilien tilikartta ja kirjanpito](finance-sustainability-accounts-ledger.md)   
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
