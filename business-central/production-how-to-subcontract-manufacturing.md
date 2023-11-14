---
title: Tuotanto alihankintana
description: 'Tässä aiheessa on laaja yleiskuva Business Centralin alihankinnan laajennetusta toiminnosta, mukaan lukien tuotantosolu ja reititys.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 99000886
ms.date: 06/22/2021
ms.author: bholtorf
---
# Tuotanto alihankintana

Valittujen toimintojen siirtäminen alihankintoina toimittajalle on yleistä monissa tuotantoyrityksissä. Alihankinta voi olla joko harvinaista tai keskeinen osa kaikkia tuotantoprosesseja.

[!INCLUDE[prod_short](includes/prod_short.md)]issa on useita työkaluja alihankintatöiden hallintaan:  

- Tuotantosolut, joihin on määritetty alihankkija: Tämän ominaisuuden avulla voit määrittää alihankkijaan liittyvän tuotantosolun. Sitä kutsutaan alihankkijan tuotantosoluksi. Voit määrittää alihankkijan tuotantosolun reititysoperaatioon, jolloin voit käsitellä alihankkijalla teetettävän toimen. Operaation kustannukset voi myös määrittää reitityksen tai tuotantosolun tasolla.  
- Yksikkö- tai aikaperustaiset työsolukustannukset: Tämän ominaisuuden avulla voit määrittää, perustuvatko tuotantosoluun liittyvät kustannukset tuotantoaikaan vai kiinteään yksikköperustaiseen korvaukseen. Vaikka alihankkijat laskuttavatkin palveluistaan usein yksikköperustaisen kiinteän maksun, sovellus osaa käsitellä molemmat vaihtoehdot (sekä tuotantoaikaan perustuvan että yksikköperustaisen kiinteän korvauksen).  
- Alihankintatyökirja: Tämä ominaisuuden avulla voit etsiä tuotantotilaukset, joissa on valmista alihankkijalle lähetettävää materiaalia, sekä luoda alihankintatöiden ostotilaukset automaattisesti tuotantotilauksen reitityksistä. Sovellus kirjaa tämän jälkeen ostotilausten kulut automaattisesti tuotantotilaukseen ostotilauksen kirjaamisen yhteydessä. Vain sellaisia tuotantotilauksia voi avata ja käyttää alihankintatyökirjasta, joiden tila on Vapautettu.  

## Alihankinnan tuotantosolut  
Alihankinnan tuotantosolut määritetään samalla tavalla kuin tavallisetkin tuotantosolut, mutta mukana on tarkentavia tietoja. Ne määritetään reitityksiin samalla tavalla kuin muutkin tuotantosolut.  

### Alihankinnan tuotantosolukentät  
**Alihankkijan nro** -kenttä määrittää tuotantosolun alihankinnan tuotantosoluksi. Tähän kenttään voit lisätä sen alihankkijan numeron, joka toimittaa tuotantosolun. Tätä kenttää voidaan käyttää niiden tuotantosolujen hallinnointiin, jotka eivät ole yrityksen sisäisiä, mutta jotka suorittavat sopimuskäsittelyä.  

Jos alihankkijalle maksetaan eri prosesseista eri hinta, lisää valintamerkki **Spesifinen yksikkökustannus** -kenttään. Tällöin voit määrittää kustannuksen kuhunkin reititysriviin, ja aikaa säästyy, kun tietoja ei tarvitse määrittää erikseen jokaisen ostotilaukseen. Käsittelyssä käytetään reititysrivin kustannusta, ei tuotantokeskuksen kustannuskenttien kustannusta. Kun **Spesifinen yksikkökustannus** otetaan käyttöön, järjestelmä voi laskea alihankkijan kustannukset reititysoperaation mukaan.  

Jos kaikista yksittäisen alihankkijan töistä maksetaan sama hinta, jätä **Spesifinen yksikkökustannus** -kenttä tyhjäksi. Kustannukset määritetään täyttämällä **Välitön yksikkökustannus**-, **Välillinen kustannus-%**- ja **Yksikkökustannus (arvo)** -kenttien tiedot.  

### Alihankinnan tuotantokeskuksia käyttävät reititykset  
Alihankinnan tuotantokeskuksia voi käytätä reititysten operaatioissa samalla tavalla kuin tavallisia tuotantokeskuksiakin.  

Voit määrittää reitityksen, joka käyttää ulkoista tuotantokeskusta, normaaliksi toimintavaiheeksi. Halutessasi voit myös muokata tietyn tuotantotilauksen reititystä ja ottaa mukaan ulkoisen operaation. Tästä voi olla hyötyä hätätilanteissa, jos palvelin ei esimerkiksi toimi kunnolla tai kysyntäpiikkien aikana, jolloin yhtiön sisäisiä töitä täytyy teettää alihankkijoilla.  

Lisätietoja on kohdassa [Reititysten luominen](production-how-to-create-routings.md).  

## Alihankintatyökirjan laskeminen ja alihankkijan ostotilausten luominen  
Kun alihankintatyökirja on laskettu, käsiteltävä asiakirja, tässä tapauksessa ostotilaus, luodaan.  

**Alihankintatyökirja** -sivu toimii kuin **Suunnittelutyökirja** laskemalla tarvittavan tarjonnan, tässä tapauksessa ostotilaukset, jotka tarkistat ja luot työkirjan perusteella käyttäen **Toteuta toimenpideviesti** -funktiota.  

> [!NOTE]  
>  Vai sellaisia tuotantotilauksia voi avata ja käyttää alihankintatyökirjasta, joiden tila on **Vapautettu**.  

### Alihankintatyökirjan laskeminen  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Alihankintatyökirja** ja valitse sitten vastaava linkki.  
2.  Voit laskea työkirjan valitsemalla **Laske alihankinnat** -toiminto.  
3.  Määritä **Laske alihankinnat** -sivulla suodattimet alihankintatoimintoja tai toiminnot suorittavia tuotantosoluja varten vain olennaisten tuotantotilausten laskemiseksi.  
4.  Valitse **OK**-painike.  

    Tarkista **Alihankintatyökirja**-sivun rivien tiedot. Tämän työkirjan tiedot ovat peräisin tuotantotilauksesta ja tuotantotilauksen reititysriveistä, ja ne tulevat näkyviin ostotilaukseen, kun kyseinen asiakirja luodaan. Voit poistaa rivin työkirjasta alkuperäisiä tietoja muuttamatta samalla tavalla kuin muistakin työkirjoista. Tiedot tulevat uudelleen näkyviin, kun seuraavan kerran suoritat **Laske alihankinnat** -toiminnon.  

### Luo alihankkijan ostotilaus  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Alihankintatyökirja** ja valitse sitten vastaava linkki.  
2.  Valitse **Toteuta toimenpideviesti** -toiminto.  
3.  Jos haluat tulostaa ostotilauksen samalla, kun se luodaan, lisää valintamerkki **Tulosta tilaukset** -kenttään.  
4.  Valitse **OK**-painike.  

Jos kaikki alihankintatoiminnot on tarkoitus lähettää samaan toimittajan sijaintiin, vain yksi ostotilaus luodaan.  

Ostotilaukseksi muuttunut työkirjarivi poistetaan työkirjasta.  Kun ostotilaus on luotu, se ei enää näy työkirjassa.  

## Alihankkijan ostotilauksen kirjaaminen  
Kun alihankkijan ostotilaukset on luotu, ne voidaan kirjata. Kun tilaus vastaanotetaan, tuotantotilaukseen kirjataan kapasiteettitapahtuma; kun tilaus laskutetaan, ostotilauksen välitön kustannus kirjataan tuotantotilaukseen.  

## Alihankkijan ostotilauksen kirjaaminen  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  
2.  Avaa ostotilaus, joka on luotu alihankintatyökirjasta.  

    Ostotilausriveillä näkyy samat tiedot kuin työkirjassa. **Tuotantotilauksen nro**-, **Tuot.til. rivinro**-, **Operaation nro**- ja **Tuotantosolun nro** -kentät on täytetty lähdetuotantotilauksen tiedoilla.  

3.  Valitse **Kirjaa**-toiminto.  

Ohjelma kirjaa tuotantotilauksen tuotospäiväkirjan rivin tapahtuman automaattisesti, kun ostotilaus vastaanotetaan. Tätä sovelletaan vain, jos alihankintasopimuksen työvaihe on tuotantotilauksen reitityksen viimeinen työvaihe.  

> [!CAUTION]  
>  Kirjataan jatkuvan tuotantotilauksen tuotos automaattisesti, kun vastaanotettuja alihankinnan nimikkeitä ehkä haluttu. Syynä tälle voi olla, että odotettu tuotoksen määrä, joka kirjataan, voi olla erilainen kuin todellinen määrä ja automaattisen tulostuksen kirjauspäivämäärä voi olla harhaanjohtava.  
>   
>  Jos haluat välttää oletetun tuotantotilauksen tuotoksen kirjaamisen alihankintasopimuksen oston vastaanoton yhteydessä, varmista, että alihankinnan toiminto ei ole viimeinen. Lisää vaihtoehtoisesti uusi viimeinen operaatio lopullisen tuotoksen määrälle.  

Ostotilauksen välitön kustannus kirjataan tuotantotilaukseen, kun ostotilaus kirjataan laskutetuksi.  

## Katso myös  
[Tuotanto](production-manage-manufacturing.md)    
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)      
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]