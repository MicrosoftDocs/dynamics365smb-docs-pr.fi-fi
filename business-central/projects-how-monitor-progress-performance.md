---
title: Projektin edistymisen ja suorituskyvyn valvonta
description: Tietoja keskeneräisen työn (KET) luomisesta ja KESKENeräisen työn laskemisesta projektien taloudellisen arvon arvioimiseksi keskeneräisen työn aikana.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 07/31/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---

# Projektin edistymisen ja suorituskyvyn valvonta

Keskeneräinen työ (KET) on ominaisuus, jonka avulla voidaan arvioida keskeneräisten projektien taloudellinen arvo kirjanpidossa.

Projektin edetessä materiaaleja ja resursseja kulutetaan, ja aiheutuneet kulut on kirjattava projektiin. Monissa tapauksissa projektille saatetaan kirjata kuluja ennen laskuttamista. Jos projektista on kirjattu kuitenkin vain kulut, rahoituslaskelma on epätarkka. Projektin todellista arvoa voidaan seurata laskemalla KET ja kirjaamalla se pääkirjanpitoon. Lisätietoja on kohdassa [Tietoja KET-menetelmistä](projects-understanding-wip.md).

Voit laskea KET:n seuraavien arvojen perusteella:

* Kustannusarvo
* Myyntiarvo
* Tuloutettavat kustannukset
* Valmistumisen prosenttiosuus
* Valmis sopimus

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## Projektin KET-menetelmän luominen

Projektiin luodaan organisaation tarpeita vastaava KET-menetelmä, joka määritetään oletukseksi.  

> [!NOTE]
> Kun olet käyttänyt uutta menetelmääsi KET-tapahtumien luomiseen, et voi muokata tai poistaa sitä.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, kirjoita **Projektin KET-menetelmät** ja valitse linkit.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sulje sivu.   
4. Jos haluat tehdä tästä uudesta menetelmästä oletusmenetelmän, valitse ![Kerro-ominaisuuden avaava hehkulamppu.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Projektin asetukset** ja valitse sitten liittyvä linkki.  
5. Valitse **Oletus KET-menetelmä** -kentässä menetelmä luettelosta.

## Projektin KET-menetelmän määrittäminen

Uutta projektia luotaessa on määritettävä, mihin projektin KET-menetelmää käytetään. Joissakin tapauksissa käytettävä projektin KET-menetelmä on jo määritetty oletukseksi.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Projektien luominen](projects-how-create-jobs.md).  
3.  **Valitse Projektin kortti**  sivun **Kirjaus-pikavälilehden**  **KET-menetelmä-kentässä** keT-menetelmä luettelosta. Vaikka oletusmenetelmä olisi määritetty, voit valita tarvittaessa toisen vaihtoehdon.  

### KET-menetelmän määrittäminen projektitehtävälle

Projektitehtävälle voidaan määrittää KET-menetelmä, jättää tietyt projektitehtävät pois KET-laskutoimituksista tai ryhmitellä yhdessä laskettavat tehtävät. 

Jos kunkin projektitehtävän KET halutaan laskea erikseen, KET-kirjaus mahdollistaa yksittäisille tehtäville määritetyt dimensiot.

**KET - Yhteensä** määrittää projektitehtävät, jotka halutaan ryhmittää yhteen keskeneräisiä töitä ja tuloutusta laskettaessa. Kaikissa tehtäväryhmissä on oltava yksi tehtävä, joka täyttää kaksi ehtoa:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* **KET - Yhteensä** -kentän arvo on *Yhteensä*. (Jos yhdenkään projektitehtävän **KET - Yhteensä** -kentän arvo ei ole *Yhteensä*, *Yhteensä*-kentän arvo määritetään automaattisesti viimeisellä projektitehtävärivillä, kun KET lasketaan ensimmäisen kerran).

* Sisältää **Projektitehtävän nro** -arvon, joka on projektitehtävien ryhmän tai alueen viimeinen numero.

Seuraavassa taulukossa kuvaillaan kolme asetusta:

| Kenttä | Kuvaus |
|--|--|
| **\<blank\>** | Jätä tyhjäksi, jos projektitehtävä on osa tehtäväryhmää. |
| **Yhteensä** | Määrittää tehtävien alueen tai ryhmän, joka sisällytetään KET:n ja tunnistuksen laskutoimiin. Ryhmään sisältyvät projektitehtävät, joiden **Projektitehtävätyyppi** on **Kirjaus**, sisällytetään KET yhteensä -summaan, ellei tehtävän **KET - Yhteensä** -kentän arvoksi ole määritetty **Pois suljettu**. |
| **Pois suljettu** | Koskee vain tehtäviä, joiden **Projektitehtävän tyyppi** on **Kirjaus**, jolloin niitä ei sisällytetä mukaan KET:n ja tuloutuksen laskentaan. |

Seuraavassa esimerkissä projektitehtävät on jaettu kahteen KET-kokonaisarvon ryhmään havainnollistamaan **KET - Yhteensä** -kentän toimintaa:

|Projektitehtävän nro|Kuvaus|Projektitehtävän tyyppi|**KET - Yhteensä** -kenttä|  
|------------------|----------------------|----------------------|----------------------|  
|1 000|Valmistelu|Alku-Yhteensä|\<blank\>|
|1010|.    Siivous|Kirjaus|**Pois suljettu**|
|1099|Valmistelu yhteensä|Loppu-Yhteensä|\<blank\>|
|1100|Maton asentaminen|Alku-Yhteensä|\<blank\>|
|1110|.    Lattian liimaaminen|Kirjaus|**Pois suljettu**|
|1120|.    Maton levittäminen|Kirjaus|\<blank\>|
|1199|Maton asentaminen yhteensä|Loppu-Yhteensä|\<blank\>|
|1200|Viimeistele|Alku-Yhteensä|\<blank\>|
|1210|.    Maton imurointi|Kirjaus|\<blank\>|
|1299|Viimeistely yhteensä|Loppu-Yhteensä|**Yhteensä**|
|1300|Virheen korjaus|Alku-Yhteensä|\<blank\>|
|1310|.    Virheen korjaus|Kirjaus|\<blank\>|
|1399|Virheen korjaus yhteensä|Loppu-Yhteensä|**Yhteensä**|

Huomaat:

* *1000* - *1299*: Tämän projektitehtäväryhmän KET lasketaan erikseen. On kuitenkin huomattava, että tehtäviä 1010 ja 1110 ei sisällytetä KET-laskutoimituksiin, koska niiden projektitehtävän tyyppi on **Kirjaus**.

* *1300* - *1399*: Tämän projektitehtäväryhmän KET lasketaan erikseen.

## Laske KET

Voit määrittää tasetileille kirjattavan KET-summan kauden lopussa suoritettavaa raportointia varten. Se tehdään **Laske projektin KET** -eräajon avulla.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Laske projektin KET** ja valitse sitten liittyvä linkki.  
2. Valitse **Laske KET** -toiminto.
3. Täytä **Laske projektin KET** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike.  

> [!NOTE]  
> Eräajo laskee KET:n muttei kirjaa sitä pääkirjanpitoon. Se kirjataan suorittamalla **Kirjaa KET kirjanpitoon** -eräajo, kun KET on laskettu. Katso lisätietoja seuraavasta toimenpiteestä.

## Kirjaa KET

Kun olet laskenut KET:n, voit kirjata sen tasetileille kauden lopussa suoritettavaa raportointia varten. Se tehdään **Kirjaa projektin KET kirjanpitoon** -eräajon avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjaa projektin KET kirjanpitoon** ja valitse sitten vastaava linkki.  
2. Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.  
3. Valitse **OK**-painike.

## Projektin valmistumistapahtumien laskeminen ja kirjaaminen

Kun kaikki projektin toimenpiteet, kuten käytön kirjaus ja laskutus, ovat valmiita valmiiksi, projekti on päivitettävä tilaan **Valmis**. Tämän jälkeen mahdollinen kirjanpitoon kirjattu KET peruuntuu.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse avoin projekti ja valitse sitten **Muokkaa**-toiminto.
3. Valitse Kirjaus-pikavälilehden **·**  **Tila-kentästä**  **Valmis**.
4. Laske ja kirjaa KET ohjattujen vaiheiden avulla tai tee se manuaalisesti vaiheiden 5 ja 6 mukaisesti.  
5. Valitse **Laske KET** -toiminto.
6. Täytä **Laske projektin KET** -sivulla tarvittavat kentät.  

     Eräajon **luomien projektin KET-tapahtumien Projekti valmis -** valintaruutu on valittuna. Valintaruudussa näkyy, että kyseessä ovat valmistumistapahtumat.  
7. Valitse **Kirjaa projektin KET kirjanpitoon** -toiminto.
8. Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.  

     Eräprojektin luomien PROJEKTIN KET-kirjanpitotapahtumien Project Complete - **valintaruutu on** valittuna. Valintaruudussa näkyvät valmistumistapahtumat.

## Projektitapahtumien tarkasteleminen

Kaikki projekteihin liittyvät tapahtumat on tallennettu projektirekistereihin ja numeroitu järjestyksessä numerosta 1 alkaen. Projektirekisteristä saadaan yleiskuva kaikista projektitapahtumista.    

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Projektirekisterit** ja valitse sitten vastaava linkki.
2. Valitse sopiva rekisteri ja valitse sitten **Projektikirjaukset**-toiminto.

**Projektitapahtumat**-sivulla voi tarkastella mihin tahansa projektiin liittyviä tapahtumia.  

## Katso myös

[Vaihekuvaus - Projektin keskeneräisen työn laskeminen](walkthrough-calculating-work-in-process-for-a-job.md)    
[Projektien hallinta](projects-manage-projects.md)    
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)    
[Rahoitus](finance.md)    
[Osto](purchasing-manage-purchasing.md)    
[Myynti](sales-manage-sales.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
