---
title: Projektin edistymisen ja suorituskyvyn valvonta
description: 'Tässä artikkelissa kerrotaan, miten keskeneräisen työn (KET) menetelmä luodaan ja miten KET lasketaan, kun projektien taloudellinen arvo arvioidaan projektin ollessa kesken.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
---
# <a name="monitor-job-progress-and-performance"></a>Projektin edistymisen ja suorituskyvyn valvonta

Keskeneräinen työ (KET) on ominaisuus, jonka avulla voit arvioida keskeneräisten projektien taloudellisen arvon kirjanpidossa.

Projektin edetessä kulutetaan materiaaleja ja resursseja, ja aiheutuneet kulut täytyy kirjata projektiin. Monissa tapauksissa saatat kirjata projektille kuluja ennen laskuttamista. Jos projektista on kirjattu kuitenkin vain kulut, rahoituslaskelma on epätarkka. Jos haluat seurata projektin todellista arvoa, laske KET ja kirjaa se pääkirjanpitoon. Lisätietoja on kohdassa [Tietoja KET-menetelmistä](projects-understanding-wip.md).

Voit laskea KET:n seuraavien arvojen perusteella:

* Kustannusarvo
* Myyntiarvo
* Tuloutettavat kustannukset
* Valmistumisen prosenttiosuus
* Valmis sopimus

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## <a name="create-a-job-wip-method"></a>Projektin KET-menetelmän luominen

Luo projektin KET-menetelmä organisaatiosi tarpeiden mukaan ja valitse se oletukseksi.  

> [!NOTE]
> Kun olet käyttänyt uutta menetelmääsi KET-tapahtumien luomiseen, et voi muokata tai poistaa sitä.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Projektin KET-menetelmät** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sulje sivu.   
4. Jos haluat tehdä tästä uudesta menetelmästä oletusmenetelmän, valitse ![Kerro-ominaisuuden avaava hehkulamppu.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Projektienhallinnan asetukset** ja valitse sitten vastaava linkki.  
5. Valitse **Oletus KET-menetelmä** -kentässä menetelmä luettelosta.

## <a name="define-a-wip-method-for-a-job"></a>KET-menetelmän määrittäminen projektille

Kun luot uuden projektin, sinun täytyy määrittää sille KET-menetelmä. Joissakin tapauksissa käyttämäsi projektin KET-menetelmä on jo määritetty oletukseksi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Projektit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Projektien luominen](projects-how-create-jobs.md).  
3. Valitse **Projektikortti**-sivun **KET-menetelmä**-kentässä KET-menetelmä luettelosta. Vaikka oletusmenetelmä olisi määritetty, voit valita tarvittaessa toisen vaihtoehdon.  

### <a name="define-a-wip-method-for-a-job-task"></a>KET-menetelmän määrittäminen projektitehtävälle

Voit määrittää projektitehtävälle KET-menetelmän, jättää tietyt projektitehtävät pois KET-laskutoimista tai ryhmittää tehtävät, jotka haluat laskea yhdessä. 

Jos haluat laskea KET:n erikseen jokaiselle projektitehtävälle, KET-kirjaus tarjoaa yksittäisille tehtäville määritettyjä dimensioita.

**KET - Yhteensä** määrittää projektitehtävät, jotka haluat ryhmittää yhteen, kun keskeneräisiä töitä ja tuloutusta lasketaan. Kaikissa tehtäväryhmissä on oltava yksi tehtävä, joka täyttää kaksi ehtoa:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* **KET - Yhteensä** -kentän arvo on *Yhteensä*. (Jos yhdenkään projektitehtävän **KET - Yhteensä** -kentän arvo ei ole *Yhteensä*, *Yhteensä*-kentän arvo määritetään automaattisesti viimeisellä projektitehtävärivillä, kun KET lasketaan ensimmäisen kerran).

* Sisältää **Projektitehtävän nro** -arvon, joka on projektitehtävien ryhmän tai alueen lopullinen numero.

Seuraavassa taulukossa kuvaillaan kolme asetusta:

| Kenttä | Kuvaus |
|--|--|
| **\<blank\>** | Jätä tyhjäksi, jos projektitehtävä ei sisälly tehtävien ryhmään. |
| **Yhteensä** | Määrittää tehtävien alueen tai ryhmän, joka sisällytetään KET:n ja tunnistuksen laskutoimiin. Ryhmään sisältyvät projektitehtävät, joiden **Projektitehtävätyyppi** on **Kirjaus**, sisällytetään KET yhteensä -summaan, ellei tehtävän **KET - Yhteensä** -kentän arvoksi ole määritetty **Pois suljettu**. |
| **Pois suljettu** | Koskee vain tehtäviä, joiden **Projektitehtävätyyppi** on **Kirjaus**, jolloin niitä ei sisällytetä mukaan KET:n ja tuloutuksen laskentaan. |

Seuraavassa esimerkissä projektitehtävät on jaettu kahteen KET-kokonaisarvon ryhmään **KET - Yhteensä** -kentän toiminnan havainnollistamiseksi:

|Projektitehtävän nro|Kuvaus|Projektitehtävätyyppi|**KET - Yhteensä** -kenttä|  
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

* *1000*–*1299*: Tämän projektitehtäväryhmän KET lasketaan erikseen. Huomaa kuitenkin, että tehtäviä 1010 ja 1110 ei sisällytetä KET-laskutoimiin, koska niiden projektitehtävätyyppi on **Kirjaus**.

* *1300*–*1399*: Tämän projektitehtäväryhmän KET lasketaan erikseen.

## <a name="calculate-wip"></a>Laske KET

Voit määrittää tasetileille kirjattavan KET-summan kauden lopussa suoritettavaa raportointia varten. Käytä tähän tarkoitukseen **Laske projektin KET** -erätyötä.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Laske projektin KET** ja valitse sitten vastaava linkki.  
2. Valitse **Laske KET** -toiminto.
3. Täytä **Laske projektin KET** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike.  

> [!NOTE]  
>   Erätyö laskee KET:n, mutta ei kirjaa sitä pääkirjanpitoon. Jos haluat kirjata sen, suorita **Kirjaa KET kirjanpitoon** -eräajo, kun olet laskenut KET:n. Katso lisätietoja seuraavasta toimenpiteestä.

## <a name="post-wip"></a>Kirjaa KET

Kun olet laskenut KET:n, voit kirjata sen tasetileille kauden lopussa suoritettavaa raportointia varten. Tähän käytetään **Kirjaa projektin KET kirjanpitoon** -erätyötä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Kirjaa projektin KET kirjanpitoon** ja valitse sitten vastaava linkki.  
2. Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.  
3. Valitse **OK**-painike.

## <a name="calculate-and-post-job-completion-entries"></a>Projektin valmistumistapahtumien laskeminen ja kirjaaminen

Kun olet suorittanut kaikki projektin toimenpiteet, kuten käytön kirjauksen ja laskutuksen, projektin **Tila**-arvoksi täytyy päivittää **Valmis**. Tämän jälkeen mahdollinen kirjanpitoon kirjattu KET peruuntuu.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse avoin projekti ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Tila**-kentässä **Valmis**.
4. Laske ja kirjaa KET ohjattujen vaiheiden avulla. Voit tehdä sen myös manuaalisesti vaiheiden 5 ja 6 mukaisesti.  
5. Valitse **Laske KET** -toiminto.
6. Täytä **Laske projektin KET** -sivulla tarvittavat kentät.  

     Erätyön luomien projektin KET-tapahtumien vieressä on nyt valintamerkki **Projekti valmis** -kentässä. Valintamerkki osoittaa, että kyseessä ovat valmistumistapahtumat.  
7. Valitse **Kirjaa projektin KET kirjanpitoon** -toiminto.
8. Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.  

     Erätyön luomien projektin pääkirjanpidon KET-tapahtumien vieressä on nyt valintamerkki **Projekti valmis** -kentässä. Valintamerkki osoittaa, että kyseessä ovat valmistumistapahtumat.

## <a name="view-job-ledger-entries"></a>Projektin kirjanpitotapahtumien tarkasteleminen

Kaikki projektiin liittyvät tapahtumat on tallennettu projektirekistereihin ja numeroitu järjestyksessä numerosta 1 alkaen. Projektirekisterissä voi saada yleiskuvan kaikista projektitapahtumista.    

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Projektirekisterit** ja valitse sitten vastaava linkki.
2. Valitse asianmukainen rekisteri ja valitse sitten **Projektikirjaukset**-toiminto.

**Projektitapahtumat**-sivulla voi tarkastella mihin tahansa projektiin liittyviä tapahtumia.  

## <a name="see-also"></a>Katso myös

[Vaihekuvaus – Projektin keskeneräisen työn laskeminen](walkthrough-calculating-work-in-process-for-a-job.md)
[Projektien hallinta](projects-manage-projects.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
