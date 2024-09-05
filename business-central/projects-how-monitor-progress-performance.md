---
title: Projektin edistymisen ja suorituskyvyn valvonta
description: Tietoja keskeneräisen työn (KET) luomisesta ja KESKENeräisen työn laskemisesta projektien taloudellisen arvon arvioimiseksi keskeneräisen työn aikana.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/19/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---

# <a name="monitor-project-progress-and-performance"></a>Projektin edistymisen ja suorituskyvyn valvonta

Keskeneräinen työ (KET) on ominaisuus, jonka avulla voidaan arvioida keskeneräisten projektien taloudellinen arvo kirjanpidossa.

Projektin edetessä materiaaleja ja resursseja kulutetaan, ja aiheutuneet kulut on kirjattava projektiin. Monissa tapauksissa projektille saatetaan kirjata kuluja ennen laskuttamista. Mutta jos kirjaat vain kuluja, rahoituslaskelmasi on epätarkka. Projektin todellista arvoa voidaan seurata laskemalla KET ja kirjaamalla se pääkirjanpitoon. Seuraavat KET-menetelmät ovat käytettävissä ruudussa:

* Kustannusarvo
* Myyntiarvo
* Tuloutettavat kustannukset
* Valmistumisen prosenttiosuus
* Valmis sopimus

Voit myös luoda keT-menetelmän, joka vastaa organisaatiosi tarpeita ja määrittää sen oletusarvoksi.  

Lisätietoja on kohdassa [Tietoja KET-menetelmistä](projects-understanding-wip.md).

Jos haluat tarkastella tulosta jollakin toisella menetelmällä, muuta menetelmää ja laske KET uudelleen. KESKENERÄisen työn laskentakertaa ei ole rajoitettu. Arvoa ei kirjata automaattisesti pääkirjanpitoon. Kun olet laskenut KET:n haluamallasi tavalla, voit kirjata sen pääkirjanpitoon.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, kirjoita **Projektin KET-menetelmät** ja valitse linkit.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Sulje sivu.   
4. Jos haluat tehdä tästä uudesta menetelmästä oletusmenetelmän, valitse ![Kerro-ominaisuuden avaava hehkulamppu.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Projektin asetukset** ja valitse sitten liittyvä linkki.  
5. Valitse **Oletus KET-menetelmä** -kentässä menetelmä luettelosta.

## <a name="define-a-wip-method-for-a-project"></a>Projektin KET-menetelmän määrittäminen

Uutta projektia luotaessa on määritettävä, mihin projektin KET-menetelmää käytetään. Joissakin tapauksissa käytettävä projektin KET-menetelmä on jo määritetty oletukseksi.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Projektien luominen](projects-how-create-jobs.md).  
3.  **Valitse Projektin kortti**  sivun **Kirjaus-pikavälilehden**  **KET-menetelmä-kentässä** keT-menetelmä luettelosta. Jos oletustapa on määritetty, voit tarvittaessa valita toisen vaihtoehdon.  

### <a name="define-a-wip-method-for-a-project-task"></a>KET-menetelmän määrittäminen projektitehtävälle

Voit määrittää projektitehtävälle KET-menetelmän, jättää projektitehtävät pois KET-laskennasta tai ryhmiteltää laskettavat tehtävät.

Jos kunkin projektitehtävän KET halutaan laskea erikseen, KET-kirjaus mahdollistaa yksittäisille tehtäville määritetyt dimensiot.

**KET - Yhteensä** määrittää projektitehtävät, jotka halutaan ryhmittää yhteen keskeneräisiä töitä ja tuloutusta laskettaessa. Kaikissa tehtäväryhmissä on oltava yksi tehtävä, joka täyttää kaksi ehtoa:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* **KET - Yhteensä** -tyypiksi **on määritetty Yhteensä**. Jos projektitehtäviä, joiden **KET-kokonaissummaksi ei ole määritetty Yhteensä**, Yhteensä määritetään automaattisesti viimeiselle projektitehtäväriville, kun KET lasketaan ensimmäistä kertaa.
* Projektitehtävänro-kentän **·**  numero-kenttä on projektitehtävien ryhmän tai alueen viimeinen.

Vaihtoehdot on kuvattu seuraavassa taulukossa:

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

* Ohjelma *laskee tälle projektitehtäväryhmälle erikseen KET-summat 1 000*  *:sta 1299*:ään. Huomaa kuitenkin, että kaksi tehtävää, 1010 ja 1110, jätetään pois KET-laskennasta, koska niiden projektitehtävän tyyppi on **Kirjaus**.
* Ohjelma *laskee tälle projektitehtäväryhmälle erikseen 1300-1399*  *keskeneräisen* työn.

## <a name="calculate-wip"></a>Laske KET

Voit määrittää tasetileille kirjattavan KET-summan jakson lopun raportointia varten Laske projektin KET **-eräajon** avulla.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvaketta, syötä **Laske projektin KET** ja valitse sitten liittyvä linkki.  
2. Valitse **Laske KET** -toiminto.
3. Täytä **Laske projektin KET** -sivulla tarvittavat kentät.
4. Valitse **OK**-painike.  

> [!NOTE]  
> Eräajo laskee KET:n, mutta ei kirjaa sitä pääkirjanpitoon. Voit kirjata KET:n suorittamalla **Kirjaa KET kirjanpitoon** -eräajon keskeneräisen työn laskelman jälkeen. Katso lisätietoja seuraavasta toimenpiteestä.

### <a name="review-warnings"></a>Tarkista varoitukset

Jos KET-laskennan tuloksena ohjelma laskee KESKENERÄisen *työn varoituksella*, varoitukset kannattaa ehkä tarkistaa.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektin KET-ohjaamo** ja valitse sitten vastaava linkki.  
2. Valitse projekti, jonka varoituksia haluat tarkastella.  **KET-varoitusten** vaihto on käytössä projekteissa, joissa on KET-varoituksia.
3. Valitse **Näytä varoitus -** toiminto.

### <a name="delete-wip-entries"></a>Poista KET-tapahtumat

Jos haluat kokeilla eri KET-menetelmiä, voit määrittää *, että Projektitehtävää ei voi muuttaa, koska projektiin liittyy projektin KET-tapahtumien* virhe. Voit tarkistaa KET-menetelmän poistamalla aiemmin luodut KET-tapahtumat.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektin KET-ohjaamo** ja valitse sitten vastaava linkki.  
2. Valitse projekti, jonka KET-tapahtumat haluat poistaa.
3. Valitse **Poista KET-tapahtumat -** toiminto.

## <a name="post-wip"></a>Kirjaa KET

Kun lasket KET:iä, voit kirjata sen tasetileille jakson lopun raportointia varten.  **Kirjaa projektin KET kirjanpitoon** -eräajon käyttäminen.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -painikkeen avulla voit kirjoittaa **Kirjaa projektin KET kirjanpitoon** ja valita linkin.  
2. Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.  
3. Valitse **OK**-painike.

## <a name="calculate-and-post-project-completion-entries"></a>Projektin valmistumistapahtumien laskeminen ja kirjaaminen

Kun olet saanut kaikki projektin toimenpiteet, kuten käytön ja laskutuksen kirjauksen, valmiiksi, projektin tila on päivitettävä **Valmiiksi**. Tällöin kaikki pääkirjanpitoon kirjattu KET on peruutettava.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektit** ja valitse sitten vastaava linkki.  
2. Valitse avoin projekti ja valitse sitten **Muokkaa**-toiminto.
3. Valitse Kirjaus-pikavälilehden **·**  **Tila-kentästä**  **Valmis**.
4. Laske ja kirjaa KET ohjattujen vaiheiden avulla tai tee se manuaalisesti vaiheiden 5 ja 6 mukaisesti.  
5. Valitse **Laske KET** -toiminto.
6. Täytä **Laske projektin KET** -sivulla tarvittavat kentät.  

     Eräajon luomien projektin KET-tapahtumien Project Complete - **valintaruutu on** valittuna osoittamaan, että kyseessä ovat valmistumistapahtumat.  
7. Valitse **Kirjaa projektin KET kirjanpitoon** -toiminto.
8. Täytä **Kirjaa projektin KET kirjanpitoon** -sivulla tarvittavat kentät.  

     Eräprojektin luomien PROJEKTIN KET-kirjanpitotapahtumien Project Complete - **valintaruutu on** valittuna. Valintaruudun avulla voit osoittaa, että kyseessä ovat valmistumistapahtumat.

## <a name="view-project-ledger-entries"></a>Projektitapahtumien tarkasteleminen

Kaikki projekteihin liittyvät tapahtumat on tallennettu projektirekistereihin ja numeroitu järjestyksessä numerosta 1 alkaen. Projektirekisteristä saadaan yleiskuva kaikista projektitapahtumista.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Projektirekisterit** ja valitse sitten vastaava linkki.
2. Valitse sopiva rekisteri ja valitse sitten **Projektikirjaukset**-toiminto.

 **Projektitapahtumat-sivulla** voit tarkastella mihin tahansa projektiin liittyviä tapahtumia.  

## <a name="see-also"></a>Katso myös

[Vaihekuvaus - Projektin keskeneräisen työn laskeminen](walkthrough-calculating-work-in-process-for-a-job.md)    
[Projektien hallinta](projects-manage-projects.md)    
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)    
[Rahoitus](finance.md)    
[Osto](purchasing-manage-purchasing.md)    
[Myynti](sales-manage-sales.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
