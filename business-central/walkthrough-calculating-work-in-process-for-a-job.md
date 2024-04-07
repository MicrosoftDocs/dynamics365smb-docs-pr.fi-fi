---
title: Vaihekuvaus - Projektin keskeneräisen työn laskeminen
description: 'Projekteissa kuluu esimerkiksi työntekijöiden työtunteja, koneiden käyttötunteja ja varastonimikkeitä, joita täytyy seurata projektin edetessä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Vaihekuvaus: Projektin keskeneräisen työn laskeminen

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Projektien avulla voit laatia yrityksen resurssien käyttöön liittyviä aikatauluja ja seurata tietyn projektin resurssien käyttöön liittyviä kustannuksia. Projekteissa kuluu esimerkiksi työntekijöiden työtunteja, koneiden käyttötunteja ja varastonimikkeitä, joita täytyy seurata projektin edetessä. Jos projekti on pitkäkestoinen, kustannukset täytyy ehkä siirtää taseeseen KET (Keskeneräinen työ) -tilille, kun projekti on vielä kesken. Kustannukset ja myynnit voi myöhemmin tulouttaa tuloslaskelmatilille, kun tämä on ajankohtaista.  

## Tietoja tästä vaihekuvauksesta

 Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

-   keskeneräisen työn (KET) laskeminen  
-   keskeneräisen työn laskemistavan valitseminen  
-   projektin osan sulkeminen pois keskeneräisestä työstä  
-   KET:n kirjaaminen pääkirjanpitoon  
-   KET-kirjauksen peruuttaminen.  

 Prosessin jokainen vaihe laskee arvon ja siirtää projektitapahtumia pääkirjanpitoon. Laskeminen ja kirjaus ovat erillisiä vaiheita, jotta käyttäjälle jää mahdollisuus käydä tiedot läpi ja tehdä muutoksia ennen kirjaamista pääkirjanpitoon. Laskennan eräajojen jälkeen ja ennen kirjauksen eräajojen suorittamista kannattaakin varmistaa, että kaikki tiedot ovat oikein.  

## Roolit

 Tämän vaihekuvauksen esimerkkejä havainnollistetaan erään projektitiimin jäsenen kautta. Hänen nimensä on Marianne.  

## Vaatimukset

 Asenna [!INCLUDE[prod_short](includes/prod_short.md)] tietokoneeseen ennen tämän vaihekuvauksen tehtävien suorittamista.  

## Taustatietoja

 Tämä vaihekuvaus keskittyy suunnittelu- ja konsulttiyritykseen CRONUS Finland Oy, joka suunnittelee ja varustaa uusia infrastruktuureja, kuten konferenssisaleja ja toimistoja huonekaluineen, tarvikkeineen ja varastoineen. Suurin osa CRONUS -töistä on projektisuuntautuneita, ja projektitiimin jäsen Marianne käyttää töitä yleiskatsauksen luomiseen jokaisesta meneillään olevasta työstä, jonka CRONUS on aloittanut, ja myös valmistuneista töitä. Jotkut työt voivat olla pitkiä ja kestää kuukausia. Marianne voi käyttää KET-tiliä tallentaakseen keskeneräisen työn ja seuratakseen kustannuksia projektin aikana.  

## Keskeneräisen työn laskeminen

 CRONUS on aloittanut pitkän projektin, joka on nyt laajennettu raportointikausien yli. Marianne, projektiryhmän jäsen, laskee keskeneräiset työt (KET) varmistaakseen, että yhtiön tilinpäätös on tarkka.  

 Näiden toimien aikana Marianne valitsee tietyn joukon tehtäviä, jotka sisällytetään KET-laskentaan. **Projektitehtävärivit**-sivulla Marianne voi määrittää nämä rivit **KET - Yhteensä** -sarakkeeseen.  

 Seuraavassa taulukossa kuvaillaan nämä kolme asetusta.  

|Kenttä|Description|  
|-------------------------------------|---------------------------------------|  
|**\<blank\>**|Jätä tyhjäksi, jos projektitehtävä on osa tehtäväryhmää.|  
|**Yhteensä**|Määrittää alueen tai tehtäväryhmän, jotka kuuluvat KET:n ja tunnistuksen laskentaan. Ryhmässä mikä tahansa projektitehtävä, jonka **Projektitehtävätyyppi** on **Kirjaus**, sisällytetään KET yhteensä -summaan, ellei sen **KET yhteensä** -kentäksi ole määritetty **Pois suljettu**.|  
|**Pois suljettu**|Koskee vain tehtävää, jonka **Projektitehtävätyyppi** on **Kirjaus**. Tehtävää ei oteta lukuun, kun KET ja tuloutus lasketaan.|  

 Seuraavassa vaihekuvauksessa Marianne käyttää KET: n laskennassa yrityksensä vakiomenetelmää, eli kustannusarvomenetelmää. Marianne määrittää, mikä projektin osa sisältyy KET-laskentaan määrittämällä KET:in yhteensä-arvoja eri projektitehtäväriveille.  

### Keskeneräisen työn laskeminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2.  Valitse **Projektit**-luettelossa ensin **Karjaa**-projekti ja sitten **Muokkaa**-toiminto. Työkortti avataan muokkaustilassa.  

     Keskeneräinen työ voidaan laskea kustannusarvon, myyntiarvon, myynnin kulujen, valmistumisen prosenttiosuuden ja valmiin sopimuksen perusteella. Tässä esimerkissä CRONUS käyttää kustannusarvomenetelmää.  

3.  Napsauta**Kirjaus**-pikavälilehdessä **KET-menetelmä**-kentässä ja valitse **Kustannusarvo**.  
4.  Valitse **Projektitehtävärivit** ja määritä seuraavat arvot **KET - Yhteensä** -kentässä.  

     Arvot kuvaillaan seuraavassa taulukossa.  

    |Projektitehtävänumero|KET-summa -kenttä|  
    |------------------|----------------------|  
    |1130|Pois suljettu|  
    |1190|Yhteensä|  
    |1210|Pois suljettu|  
    |1310|Pois suljettu|  

5.  Valitse ensin **KET**-toiminto ja sitten **Laske KET**-toiminto.  
6.  **Laske projektin KET** -sivulla voi valita projektin, jonka keskeneräinen työ on tarkoitus laskea. Varmista **Projekti**-pikavälilehdessä, että **Karjaa** on valittuna **Nro** -kentässä.  
7.  Anna **Kirjauspvm**-kentässä päivämäärä, joka käsittelypäivämäärän jälkeen.
8.  Anna **Asiakirjan nro** -kenttään **1**. Tämä luo asiakirjan, johon voit viitata myöhemmin jäljitettävyyttä varten.  
9. Suorita eräajo valisemalla **OK**. Näyttöön tulee sanoma. Jatka valitsemalla **OK**-painike. Sulje **Projektitehtävärivit**-sivu.  

    > [!NOTE]  
    >  Sanoma on, että KET-laskentaan liittyy varoituksia. Tarkastele varoitukset uudelleen seuraavassa toimenpiteessä.  

10. Vieritä **Projekti**-kortissa **Keskeneräiset työt ja tuloutus** -pikavälilehteen, jossa on tietoja lasketuista arvoista. Näet myös **KET-kirjauksen päivämäärän** ja arvot, jotka on kirjattu pääkirjanpitoon, jos sellainen on.  

 Huomaa, että **Tuloutettu kustannussumma** -arvona on 215.60 **Kirjattava**-sarakkeessa. Tämä kuvastaa työtehtävien 1110 - 1130 muodostaman ryhmän kahden nimikkeen kokonaiskustannuksia. Kolmas nimike on **Pois suljettu**, eikä se siksi sisälly KET-laskentaan.  

### Tarkastele KET-varoituksia  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektin KET-ohjaamo** ja valitse sitten vastaava linkki.  
2.  Valitse ensin **Karjaa**-projekti ja sitten **Näytä varoitukset** -toiminto.  
3.  Tarkastele **Projektin KET-varoitukset** -sivulla työhön liittyvää varoitusta.  

 Tämän kirjanpitojakson jälkeen Mariannen täytyy laskea keskeneräinen työ uudelleen, jotta tähän mennessä valmistunut työ voidaan laskea mukaan.  

### Keskeneräisen työn uudelleenlaskeminen  

1.  Avaa KET-laskenta valitsemalla **Projekti**-kortissa **KET-tapahtumat**-toiminto.  

     Tällä sivulla näkyvät **Projektin KET-tapahtumat**, jotka projektille on viimeksi laskettu, vaikka keskeneräistä työtä ei vielä ole kirjattu pääkirjanpitoon.  

2.  Voit seurata menetelmän ohjeita, joissa kerrotaan, kuinka voit laskea KET: n laskeaksesi KET:n uudelleen. **KET-tapahtumat**-sivulle luodaan uusi tapahtuma aina, kun keskeneräinen työ lasketaan.  
3.  Sulje sivu.  

> [!NOTE]  
>  Vain keskeneräinen työ ja tuloutus lasketaan. Sitä ei kirjata pääkirjanpitoon. Nämä toimet edellyttävät, että suoritat **Kirjaa KET kirjanpitoon** -eräajon, kun olet laskenut keskeneräisen työn ja tuloutuksen.

## Keskeneräisen työn kirjaaminen pääkirjanpitoon

 Kun Marianne on laskenut tämän projektin keskeneräisen työn, hän voi kirjata sen pääkirjanpitoon.  

### KET-arvon kirjaaminen pääkirjanpitoon  

1.  Valitse **Projektit**-luettelosta rivi, jossa on **Karjaa**-projekti.  
2.  Valitse ensin **KET**-toiminto ja sitten **Kirjaa KET kirjanpitoon** -toiminto.  
3.  Valitse **Kirjaa projektin KET kirjanpitoon** -sivun **Projekti**-pikavälilehden **Nro**-kentästä **Karjaa**. -kentässä.  
4.  Lisää **Vaihtoehdot**-pikavälilehden **Peruutusasiakirjan numero** -kenttään **1**.  
5.  Kirjaa KET pääkirjanpitoon valitsemalla **OK**.  
6.  Sulje vahvistussivu valitsemalla **OK**.  

     Kun kirjaus on valmis, voit tarkastella tietoja **KET KP-tapahtumat** -sivulla.  

7.  Valitse **Projektit**-luettelossa ensin **Karjaa**-projekti ja sitten **KET-kirjanpitotapahtumat**-toiminto.  

     Projektin **KET-kirjanpitotapahtumat** -sivulla näkyy, että keskeneräinen työ on kirjattu pääkirjanpitoon.  

8.  Sulje sivu.  
9. Avaa **Karjaa**-kohteen **Projekti-** kortti.  
10. Huomaa, että **Keskeneräiset työt ja tuloutus** -pikavalintalehden **Kirjattu**-sarakkeen **Tuloutettu kustannusten kirjanpitosumma** -kenttä on nyt täytetty, mikä ilmaisee, että kyseinen KET on kirjattu pääkirjanpitoon onnistuneesti.  
11. Sulje kortti valitsemalla **OK**-painike.  

## KET-kirjauksen peruuttaminen

 Marianne määrittää, että projektitehtävät, jotka jätettiin ulkopuolelle laskettaessa KET, olisi pitänyt laskea mukaan KET:iin. Kaikeksi onneksi Marianne kuitenkin voi peruuttaa väärät kirjaukset tekemättä uusia KET-kirjauksia.  

### KET-kirjauksen peruuttaminen  

1.  Valitse **Projektit**-luettelosta **Karjaa**-projekti.  
2.  Valitse ensin **KET**-toiminto ja sitten **Kirjaa KET kirjanpitoon** -toiminto.  
3.  Valitse **Kirjaa projekti KET kirjanpitoon** -sivun **Projekti**-pikavälilehden **Nro**-kentästä **Karjaa**. -kentässä.  
4.  Lisää **Vaihtoehdot**-pikavälilehden **Peruutusasiakirjan numero** -kenttään **1**.  
5.  Valitse **Peruutuksen kirjauspäivämäärä** -kentässä alkuperäinen kirjauspäivämäärä. Sen tulee olla sama päivämäärä, jota on käytetty, kun KET on laskettu ensimmäistä kertaa.  
6.  Valitse **Vain peruutus** -valintaruutu. Tällöin aiemmin kirjattu keskeneräinen työ peruutetaan, mutta uutta keskeneräistä työtä ei kirjata pääkirjanpitoon.  
7.  Valitse **OK**-painike eräajon suorittamiseksi ja valitse sitten **OK**-painike sulkeaksesi vahvistussivun.  
8.  Avaa **Karjaa**-kohteen **projektikortti**.  
9. Varmista **Keskeneräiset työt ja tuloutus** -pikavälilehdessä, ettei kirjattuja KET-tapahtumia ole.  
10. Sulje tämä sivu.  
11. Valitse **Projektit**-luettelossa ensin **Karjaa**-projekti, sitten **KET**-toiminto ja lopuksi **KET-kirjanpitotapahtumat**-toiminto. KET-tapahtumissa on valittuna **Peruutettu**-valintaruutu.  
12. Sulje tämä sivu.  
13. Voit siirtyä takaisin projektin **Projektitehtävärivit**-kohtaan, liittää mukaan projektin osat, jotka olisivat kuuluneet keskeneräiseen työhön, tehdä laskutoimitukset uudelleen ja kirjata uuden arvon pääkirjanpitoon.  

    > [!NOTE]  
    >  Oletetaan, että Tricia on laskenut ja kirjannut keskeneräisen työn, jossa on virheellisiä päivämääriä. Marianne voi peruuttaa virheellisen kirjauksen, korjata päivämääriä ja tehdä uuden kirjauksen pääkirjanpitoon käyttämällä aiemmin kerrottua menetelmää.  

## Seuraavat vaiheet

 Tämä vaihekuvaus on ohjannut sinut keskeneräisen työn laskemisen vaiheiden läpi kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]. Jos projektit ovat suuria, kustannukset kannattaa ehkä siirtää KET-tilille ajoittain siksi aikaa, että projekti valmistuu. Tässä vaihekuvauksessa osoitettiin, milloin ja miksi tehtävärivejä täytyy jättää pois laskennasta sekä milloin uudelleenlaskeminen on tarpeen. Se myös näyttää, milloiin uudellenlaskenta on suoritettava. Ja lopuksi, näissä vaiheittaisissa ohjeissa kerrotaan, miten kirjaat KET:n pääkirjanpitoon. Mukana on myös esimerkki siitä, miten voit kääntää KET-kirjauksen pääkirjanpitoon.  

## Katso myös

 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
 [Vaihekuvaus: Projektinhallinta Projektit-sovellusalueen avulla](walkthrough-managing-projects-with-jobs.md)  
 [Tietoja KET-menetelmistä](projects-understanding-wip.md)  
 [Etenemisen ja tehokkuuden valvonta](projects-how-monitor-progress-performance.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
