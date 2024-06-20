---
title: Kestävyystapahtumien tallentaminen
description: Tietoja kasvihuonekaasupäästöjen (GHG) kirjauksesta.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Kestävyystapahtumien tallentaminen

Tällä hetkellä ainoa tapa kirjata kasvihuonekaasu (GHG) -päästöjä kestävyyskirjauksiin on käyttää kestävyyspäiväkirjoja.

## Vastuullisuuspäiväkirjat

Vastuullisuuspäiväkirjat on suunniteltu seuraamaan ja tallentamaan kestävyyteen liittyviä toimia käyttäen samaa käyttökokemusta kuin muissakin Business Centralin päiväkirjoissa. Käyttäjät, joilla on tarvittavat tiedot, voivat syöttää päästöjä päiväkirjaan manuaalisesti. Vaihtoehtoisesti, jos heiltä puuttuu nämä tiedot, he voivat käyttää sisäisiä kaavoja laskeakseen päästöjä tarkasti tiettyjen tunnettujen parametrien perusteella, jotka vastaavat eri tyyppisiä lähteitä ja tilejä.

Päiväkirjaan lisäämäsi tiedot ovat väliaikaisia, ja niitä voi muuttaa niiden ollessa siinä päiväkirjassa. Kun kirjaat päiväkirjan, tiedot siirretään Kestävyyskirjanpitotapahtumiin yksittäisiin kestävyystileihin, missä niitä ei voi muuttaa. Voit kuitenkin kirjata peruuttavia tai korjaavia tapahtumia.

### Päiväkirjan mallien ja erien käyttäminen

Oletusarvoisesti on olemassa kaksi kestävyyspäiväkirjan mallia: vakiomalli ja toistuva malli.

Voit määrittää kullekin päiväkirjan mallille oman henkilökohtaisen päiväkirjan päiväkirjan eränä. Tämä edellyttää, että valitset **Erät**-toiminnon **Kestävyyspäiväkirjan mallit** -sivulla ja luot sitten uuden **kestävyyspäiväkirjan erän** uudelle sivulle. Voit esimerkiksi määrittää oman päiväkirjan erän kullekin päästöjen vaikutusalueelle käyttämällä **Päästöjen laajuus** -vaihtoehtoa, jossa valitset kolmesta olemassa olevasta vaikutusalueesta. Voit lisätä tai muuttaa jokaiselle erälle **lähdekoodi** ja **syykoodi**-arvot.

> [!TIP]
> Jos rivejä on useita, virheiden riskiä voi vähentää, kun jokaiselle päästötyypille on yksi päiväkirjan erä. Vaihtoehtoisesti voit käyttää yleistä erää kaikille päästötyypeille.

### Arvioi kestävyyspäiväkirjat

**Kestävyyden asetuksissa** -sivulla voit ottaa käyttöön taustatarkistuksen, joka auttaa estämään lähetysviiveitä. Jos kestävyyspäiväkirjaa käsitellessäsi tapahtuu virheitä, validointi ilmoittaa sinulle ja estää sinua kirjaamasta päiväkirjaa.

Kun oikeellisuustarkistus otetaan käyttöön, **päiväkirjan tarkistuksen** -tietoruudussa näkyvät tämän rivin ja koko erän seurantakohteet. Vahvistus tehdään silloin, kun lataat päiväkirjan erän ja kun valitset toisen päiväkirjarivin. Tietoruudun **Virheet yhteensä** -ruudussa näkyy [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman havaitsemien ongelmien kokonaismäärä. Voit avata yleiskuvauksen ongelmista valitsemalla ruudun.

### Kestävyystapahtumien päiväkirjojen käyttäminen

Voit aloittaa kestävyyspäiväkirjojen käytön noudattamalla seuraavia vaiheita:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kestävyyspäiväkirjat** ja valitse sitten vastaava linkki.
2. Voit syöttää niin monta riviä **Kestävyyspäiväkirja**-sivulle kuin aiot kirjata samalla erällä.
3. Voit jättää **Asiakirjatyyppi**-kentän tyhjäksi tai valita **Lasku** tai **Hyvityslasku**.
4. **Tilinro**-kentässä voit valita vain ei-estettyjä kestävän kehityksen tilejä, joissa **Suora kirjaus** -kenttä on valittuna ja **Tilin tyyppi** -kentän arvo on **Kirjaus**. Tilit täytyy myös määrittää luokan ja alaryhmän avulla.

    > [!NOTE]
    > Jos käytät erää, jossa päästöalue on määritetty, Kestävyystilin **Päästöjen laajuus** -arvon on oltava yhtä suuri kuin käytetyn erän **Päästöjen laajuus** -arvon.

5. Summat voi kirjata manuaalisesti tai käyttää kaavoja.

    - Jos sinulla on tarkat tiedot päästöistä, haluat kirjata sen (eli sinulla on se vastaanotetussa laskussa), sinun täytyy valita **Manuaalinen syöttö** -kenttä määrittääksesi, että summat syötetään manuaalisesti. Tässä tapauksessa tietoja ei voi syöttää suoraan **Polttoaine/Sähkö**-, **Etäisyys**-, **Mukautettu summa**-, **Asennuskerroin**- ja **Aikakerroin**-kenttiin, koska niiden tila muuttuu ei-muokattavaksi. **Päästö CO2**, **Päästö CH4**- ja **Päästö N2O** -kentät ovat kuitenkin muokattavissa, ja voit syöttää tiedot suoraan niihin.
    - Jos et tunne päästöjä tarkasti ja sinun täytyy laskea se, älä valitse **Manuaalinen syöttö** -kenttää. Tässä tapauksessa **Päästö CO2**-, **Päästö CH4**- ja **Päästö N2O** -kentistä tulee ei-muokattavia. Voit kuitenkin syöttää laskentatiedot käyttämäsi laskukaavan perusteella. Lue lisätietoja käytetyistä kaavoista, jotka on määritelty **Kestävyyden tilikategoria** -kohdassa, [kestävyystilien ja -kirjausten kaaviosta](finance-sustainability-accounts-ledger.md#account-categories).

6. Valitse **Kirjaa**-toiminto kirjataksesi päiväkirjan. Kun tapahtumia kirjataan kestävyyspäiväkirjaan, tapahtumat luodaan kestävyyskirjauksiin.

Jos kaava perustuu Kestävyystilin luokka -taulukon **Laske pääkirjanpidosta** -vaihtoehtoon, sinun täytyy käyttää **Kerää summa KP-tapahtumista** -toimintoa ennen päiväkirjan kirjausta, kun haluat laskea päästöt tämän tietolähteen perusteella. Lisäksi jos olet tehnyt joitain muutoksia päästökertoimiin täytettyäsi päiväkirjan rivit, sinun täytyy valita **Laske uudelleen** -toiminto saadaksesi oikean summan päiväkirjaan.

### Toistuvat kirjaukset

Kestävyyspäiväkirja on yleinen päiväkirja, jossa on tiettyjä kenttiä sellaisten tapahtumien hallintaa varten, jotka kirjataan usein vähäisin muutoksin tai ilman muutoksia. Esimerkkeihin kuuluvat kestävyystransaktiot, kuten sähkö-, lämpö- tai muut vastaavat transaktiot. Voit käyttää toistuvia päiväkirjoja kirjataksesi kiinteitä ja muuttuvia summia.

Kun käytät toistuvaa päiväkirjaa, säännöllisesti kirjattavat merkinnät täytyy luoda vain kerran. Tiedot, kuten tilit, dimensiot ja dimensioarvot säilyvät päiväkirjassa kirjaamisen jälkeen. Joka kerta kun julkaiset viestin, voit tehdä tarvittavat muutokset.

**Toistotapa**-kenttä on tärkeä. Se määrittää, miten päiväkirjan rivin summaa käsitellään kirjauksen jälkeen. Jos esimerkiksi käytät samaa summaa joka kerta, kun lähetät rivin, voit valita **F kiinteä**, jolloin summa säilyy kirjaamisen jälkeen. Jos käytät samoja tilejä ja tekstiä rivillä, mutta summa vaihtelee joka kerta, kun lähetät, voit poistaa summan kirjaamisen jälkeen valitsemalla **V muuttuja** -vaihtoehdon.

**Toistotiheys**-kenttä on myös tärkeä, ja se on määritettävä. Se on pvm-kaava-kenttä, joka määrittää, kuinka usein tapahtuma kirjataan päiväkirjan riville. Lisätietoja on kohdassa [Päivämäärän kaavojen käyttäminen](ui-enter-date-ranges.md#use-date-formulas).

**Päättymispäivämäärä**-kenttä määrittää päivämäärän, jolloin rivi kirjataan viimeisen kerran. Riviä ei kirjata tämän päivämäärän jälkeen. **Päättymispäivämäärä**-kentän käyttämisessä on se etu, että rivi ei poistu päiväkirjasta heti. Voit syöttää myöhemmän päivämäärän, jotta voit käyttää riviä tulevaisuudessa. Jos kenttä on tyhjä, rivi kirjataan joka kerta, kunnes se poistetaan päiväkirjasta.

## Katso myös

[Taloushallinto](finance.md)  
[Vastuullisuuden hallinnan yleiskatsaus](finance-manage-sustainability.md)  
[Vastuullisuusmääritys](finance-sustainability-setup.md)  
[Kestävyystilien tilikartta ja kirjanpito](finance-sustainability-accounts-ledger.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
