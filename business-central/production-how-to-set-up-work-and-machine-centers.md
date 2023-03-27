---
title: Tuotantosolujen ja kuormituskeskusten määrittäminen
description: Tuotantosolukorttiin kootaan tuotantoresurssin kiinteät arvot ja vaatimukset. Nämä tiedot ohjaavat tuotantosolussa tapahtuvan tuotannon tuotosta.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 04/01/2021
ms.author: edupont
---
# Tuotantosolujen ja kuormituskeskusten määrittäminen

Sovelluksessa erotetaan kolme eri kapasiteettityyppiä. Tyypit on järjestelty hierarkkisesti. Jokaiseen tasoon kuuluu alatasoja.  

Ylin taso on tuotantosoluryhmä. Tuotantosolut on määritelty tuotantosoluryhmiin. Jokainen tuotantosolu voi kuulua vain yhteen tuotantosoluryhmään.

Jokaiselle tuotantosolulle voi määritellä useita kuormitusryhmiä. Yksi kuormitusryhmä voi kuulua vain yhteen tuotantosoluun.  

Tuotantosolun suunniteltu kapasiteetti koostuu vastaavien kuormitusryhmien saatavuudesta ja tuotantosolun suunnitellusta lisäsaatavuudesta. Tuotantosoluryhmän suunniteltu saatavuus on siten kaikkien vastaavien kuormitusryhmien ja tuotantosolujen saatavuuksien summa.  

Saatavuus tallennetaan kalenteritapahtumiin.  

> [!IMPORTANT]
> Tuotantokalenteri on määritettävä ennen tuotantosolujen tai kuormitusryhmien määrittämistä. Lisätietoja on kohdassa [Tuotantokalenterien luominen](production-how-to-create-work-center-calendars.md).

## Tuotantosolun määrittäminen

Seuraavaksi käsitellään ennen kaikkea tuotantosolun määrittämiseen. Kuormitusryhmän kalenterin määrittämisen vaiheet ovat vastaavanlaiset **Reitityksen asetukset** -pikavälilehteä lukuun ottamatta.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotantosolut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse tarvittaessa **Tuotantosoluryhmä**-kentässä ylätason resurssiryhmä, johon tuotantosolu kuuluu. Valitse avattavassa luettelossa **Uusi**-toiminto.  
5. Valitse **Vaihtoehtoinen tuotantosolu** -kentässä tuotantosolu, jota käytetään, jos tämä tuotantosolu ei ole käytettävissä tai jos kysyntä ylittää kapasiteetin. Vaihtoehtoinen tuotanto-solu on tarkoitettu vain tiedoksi, eikä se sisälly suunnitteluprosesseihin automaattisesti.
6. Valitse **Estetty** -kenttä, jos haluat estää tuotantosolun käyttämisen käsittelyssä. Siinä tapauksessa tuotosta ei voi kirjata tuotantosolussa tuotetulle nimikkeelle. Lisätietoja on kohdassa [Tuotannon tuotoksen kirjaaminen](production-how-to-post-output-quantity.md).
7. Anna **Välitön yksikkökustannus** -kenttään yhden yksikön tuottamiskustannus tässä tuotantosolussa muita kustannuselementtejä huomioon ottamatta. Tätä kustannusta kutsutaan usein myös *välittömäksi työkustannukseksi*.  
8. Syötä **Välillinen kustannus-%** -kenttään yleiset tuotantosolun käytöstä syntyvät toimintakustannukset prosenttiosuutena välittömästä yksikkökustannuksesta. Tämä prosentti lisätään välittömiin kustannuksiin yksikkökustannusta laskettaessa.  
9. Syötä **Yleiskustannus (arvo)** -kenttään tuotantosolun kaikki muut kuin toiminnasta syntyvät kustannukset, esimerkiksi kunnossapitokulut, absoluuttisena arvona.  

    **Yksikkökustannus**-kenttään lasketaan seuraavasti yhden mittayksikön tuottamisen yksikkökustannus tässä tuotantosolussa kaikki kustannuselementit huomioon ottaen:  

    Yksikkökustannus = välitön yksikkökustannus + (välitön yksikkökustannus x välillinen kustannus-%) + yleiskustannus (arvo).  

10. Määritä **Yksikkökustannuslaskenta**-kentässä, käytetäänkö yllä olevan laskennan perustana käytettyä aikaa ( **Aika**) vai tuotettujen yksiköiden määrää ( **Yksiköt**).  
11. Lisää **Spesifinen yksikkökustannus** -kenttään valintamerkki, jos haluat määrittää tuotantosolun yksikkökustannuksen sitä käyttävällä reititysrivillä. Tämä saattaa olla järkevää sellaisten operaatioiden kohdalla, joiden kapasiteettikustannukset eroavat huomattavasti tuotantosolun normaaleista kustannuksista.  
12. Valitse **Materiaalinottotapa**-kentässä, lasketaanko ja kirjataanko tämän tuotantosolun tuotoksen kirjaus manuaalisesti vai automaattisesti jommallakummalla seuraavista menetelmistä:

    |Asetus|Kuvaus|
    |------|-----------|
    |**Manuaalinen**| Käytetty aika, tuotos ja hävikki kirjataan manuaalisesti tuotospäiväkirjaan tai tuotantopäiväkirjaan.|
    |**Eteenpäin**|Tuotos kirjataan automaattisesti, kun tuotantotilaus vapautetaan.|
    |**Taaksepäin**|Tuotos kirjataan automaattisesti, kun tuotantotilaus on valmis.|

    > [!NOTE]
    > Tässä valittua materiaalinottotapaa voidaan muuttaa yksittäisten toimintojen kohdalla vaihtamalla asetus reititysriveillä.

13. Anna **Mittayksikön koodi** -kenttään ajan yksikkö, jota käytetään tämän tuotantosolun kustannuslaskennassa ja kapasiteettisuunnittelussa.
    Jotta kulutusta voitaisiin jatkuvasti tarkkailla, ensin tulee määrittää mittaustapa. Syötettävät yksiköt ovat perusyksiköitä. Esimerkiksi käsittelyaikaa mitataan tunneissa ja minuuteissa.

    > [!NOTE]  
    > Jos valitset yksiköksi Päivää, muista, että yksi päivä tarkoittaa 24:ää tuntia, ei 8:aa tuntia (työpäivää).

14. Määritä **Kapasiteetti**-kentässä, onko tuotantosolussa samanaikaisesti useita työntekijöitä tai koneita. Jos käyttämääsi [!INCLUDE[prod_short](includes/prod_short.md)] -järjestelmään ei ole asennettu Kuormitusryhmä-toimintoa, kentän arvon on oltava **1**.  
15. Anna **Tehokkuus**-kenttään tuotantosolun todellinen tuotos prosenttiosuutena oletetusta vakiotuotoksesta. Jos annat arvoksi **100**, tämä tarkoittaa, että tuotantosolun todellinen tuotos on sama kuin vakiotuotos.  
16. Valitse **Yhdistetty kalenteriin** -valintaruutu, jos käytät myös kuormitusryhmiä. Tämä varmistaa, että kalenteritapahtumat vyörytetään kuormitusryhmän kalentereista.  
17. Valitse **Tuotantokalenterin koodi** -kentässä tuotantokalenteri. Lisätietoja on kohdassa [Tuotantokalenterien luominen](production-how-to-create-work-center-calendars.md).  
18. Määritä **Jonotusaika**-kenttään aika, jonka täytyy kulua, ennen kuin tuotantosolulle määritetty työ voidaan aloittaa. 

> [!NOTE]
> Jonotusaikojen avulla voit määrittää puskurin sille, kuinka kauan komponentin saapumisesta kuormitusryhmälle tai tuotantosolulle kuluu toiminnon varsinaiseen aloittamiseen. Esimerkiksi osa toimitetaan kuormitusryhmälle klo 10:00, mutta se kestää tunnin, ennen kuin se asennetaan koneeseen, jolloin toiminto ei ala ennen klo 11:00. Jotta voisit ottaa huomioon kyseisen tunnin, jonotusaika on tunti. Kun lasketaan yhteen kuormitusryhmän tai tuotantosolun kortin **Jonotusaika**-kentän arvo sekä nimikkeen reititysrivin **Asetusaika**-, **Ajoaika**-, **Odotusaika**- ja **Siirtoaika**-kenttien arvot, saadaan nimikkeen tuotannon toimitusaika. Tämä auttaa tarjoamaan tarkkoja kokonaistuotantoaikoja.  

## Huomioitavaa kapasiteetista

Tuotantosolulle ja kuormitusryhmälle määritetty kapasiteetti ja tehokkuus eivät vaikuta vain käytettävissä olevaan kapasiteettiin. Ne vaikuttavat myös tuotannon kokonaisaikaan, joka koostuu määritys- ja suoritusajasta. Ne puolestaan määritetään reititysrivillä.  

Kun tietty reititysrivi kohdistetaan tuotantosolulle tai kuormitusryhmälle, järjestelmä laskee, kuinka paljon kapasiteettia tarvitaan ja kuinka kauan toiminnon valmistuminen kestää.  

### Ajoaika

Järjestelmä laskee ajoajan kohdistamalla täsmälleen sen ajan, joka on määritetty reititysrivin **Ajoaika**-kentässä. Tehokkuus ja kapasiteetti eivät kumpikaan vaikuta kohdistettuun aikaan. Jos ajoajaksi on esimerkiksi määritetty 2 tuntia, kohdistettu aika on 2 tuntia riippumatta siitä, mitä arvoja tuotantosolun tehokkuus- ja kapasiteettikentissä on.  

> [!NOTE]
> Laskelmissa käytettävä kapasiteetti määritetään tuotantosolussa tai kuormitusryhmässä määritetyn kapasiteetin ja reititysriville määritetyn samanaikaisen kapasiteetin välisenä vähimmäisarvona. Jos tuotantosolun kapasiteetti on 100 mutta reititysrivin samanaikainen kapasiteetti on 2, silloin laskelmissa käytettävä arvon on *2*.

Toiminnon *kestossa* sen sijaan otetaan huomioon sekä tehokkuus että kapasiteetti. Kesto lasketaan seuraavasti: *ajoaika/tehokkuus/kapasiteetti*. Seuraavassa taulukossa on esimerkkejä samaa ajoaikaa käyttävän keston laskemisesta. Kestoksi on määritetty reititysrivillä 2 tuntia:

- Jos tehokkuus on 80 %, tarvitaan 2,5 tuntia kahden tunnin sijaan.  
- Jos tehokkuus on 200 %, työ voidaan suorittaa tunnissa. Toisin sanoen kaivaminen sujuu kaksi kertaa nopeammin, jos kaivinkone on kaksi kertaa suurempi.  

    Sama tulos saavutetaan, jos käytössä on kaksi pientä kaivinkonetta eikä yksi iso kaivinkone. Silloin käytössä on kapasiteettina *2* ja tehokkuutena *100 %*.  

Osittaisessa kapasiteetissa on tiettyjä hankaluuksia, ja sitä käsitellään myöhemmin. 

### Määritysaika

Määritykseen kohdistettu aika määräytyy kapasiteetin mukaan, ja se lasketaan kaavalla *Määritysaika * kapasiteetti*. Jos kapasiteetiksi on esimerkiksi määritetty *2*, kohdistettu määritysaika kaksinkertaistuu, koska toimintoa varten on määritettävä kaksi konetta.  

Määritysajan *kesto* määräytyy tehokkuuden mukaan, ja se lasketaan kaavalla *Määritysaika / tehokkuus*. 

- Jos tehokkuus on 80 %, määrittämiseen tarvitaan 2,5 tuntia kahden tunnin sijaan.  
- Jos tehokkuus on 200 %, määritys voidaan tehdä tunnissa reititysrivillä määritetyn 2 tunnin sijaan.  

Osittaisen kapasiteetin hahmottaminen ei ole yksinkertaista, ja sitä vain käytetään vain tietyissä erikoistilanteissa.

### Tuotantosolu käsittelee samanaikaisesti useita tilauksia

Käytetään esimerkkejä ruiskumaalauspistettä. Siinä kunkin käsitellyn erän määritys- ja ajoaika on sama. Kussakin erässä voi olla useita yksittäisiä tilauksia, jotka maalataan samanaikaisesti.  

Tässä tapauksessa tilauksiin kohdistettavaa aikaa ja kustannusta hallitaan määritysajan ja samanaikaisen kapasiteetin avulla. Ajoajan käyttämistä reititysriveillä ei suositella.  

Kullekin yksittäiselle tilaukselle kohdistettu määritysaika on samanaikaisesti suoritettavien tilausmäärien käänteisessä järjestyksessä. Lisäesimerkkejä määritysajan laskemisesta, kun ajaksi on reititysrivillä määritetty kaksi tuntia:

- Jos tilauksia on kaksi, reititysrivin samanaikaiseksi kapasiteetiksi on määritettä 0,5.

    Tällä tavoin kullekin kohdistetaan tunnin kapasiteetti, mutta kunkin tilauksen kestoksi jää kaksi tuntia.
- Jos tilauksia on kaksi ja niiden määränä on yksi ja neljä, ensimmäisen tilauksen samanaikainen kapasiteetti reititysrivillä on 0,2 ja toisen tilauksen 0,8.  

    Näin ollen ensimmäisen tilauksen kohdistettu kapasiteetti on 24 minuuttia ja toisen tilauksen 96 minuuttia. Kummankin tilauksen kestona on edelleen kaksi tuntia.  

Kummasakin tapauksessa kaikkien tilausten kohdistettu aika on yhteensä kaksi tuntia.


### Tehokas resurssi voi varata vain osan työpäivästä tuottavaan työhön

> [!NOTE]
> Tämä ei ole suositeltava skenaario. Sen sijaan kannattaa käyttää tehokkuutta. 

Yksi tuotantosoluista ilmaisee kokeneen työntekijän, joka tehokkuus tehtävissä on 100 %. Tämä työntekijä voi kuitenkin käyttää vain 50 % työajastaan tehtävien tekemiseen, koska muu aika kuluu hallintotehtäviin. Vaikka tämä työntekijä pystyy suorittamaan kahden tunnin tehtävän täsmälleen kahdessa tunnissa, keskimäärin on odotettava toiset kaksi tuntia, kun kyseinen henkilö suorittaa muita tehtäviä.  

Kohdistettu ajoaika on kaksi tuntia ja kesto on neljä tuntia.  

Määritysaikaa ei kannata käyttää tällaisissa skenaarioissa, sillä järjestelmä kohdistaa 50 % ajasta. Jos määritysajaksi on määritetty *2*, kohdistettu määritysaika on yksi tunti ja kesto on kaksi tuntia.

### Yhdistetty kalenteriin

Kun **Yhdistetty kalenteriin** -kenttä on valittu, tuotantosolulla ei ole omaa kapasiteettia. Sen sijaan sen kapasiteetti on yhtä suuri kuin kaikkien tuotantosoluun määritettyjen kuormitusryhmien kapasiteettien summa.  

> [!NOTE]
>  Kuormitusryhmän tehokkuus muunnetaan tuotantosolun kapasiteetiksi.

Jos käytössä on esimerkiksi kaksi kuormitusryhmää, joiden tehokkuus on 80 ja 70, kalenteriin yhdistetyn tapahtuman tehokkuus on 100, kapasiteetti 1,5 ja kokonaiskapasiteetti 12 tuntia (kahdeksan tunnin vuoro * kapasiteetti 1,5). 

> [!NOTE]
>  **Kalenteriin yhdistetty** -kenttää käytetään, kun reititykset jäsennetään aikatauluttamaan tuotantotoiminnot kuormitusryhmä- eikä tuotantosolutasolla. Kun kalenteriin yhdistäminen tehdään, **Tuotantosolun kuormitus** -sivusta ja -raporteista tulee kaikkien tuotantosoluun määritettyjen kuormitusryhmien kootun kuormituksen yleiskuvaus.

### Esimerkki - Tuotantosoluun liitetyt erilaiset kuormitusryhmät

On tärkeää suunnitella, mitkä kapasiteetit muodostavat kokonaiskapasiteetin silloin, kun määritellään kuormitusryhmiä ja tuotantosoluja.

Jos eri kuormitusryhmiä (esimerkiksi 210 Pakkausosasto 1, 310 Maalaushuone) on määritelty yhdelle tuotantosolulle, kuormitusryhmien yksittäisten kapasiteettien huomioon ottaminen on tärkeää, koska yhden kuormitusryhmän epäonnistuminen voi keskeyttää koko prosessin. Kuormitusryhmät voi syöttää niiden kapasiteetin mukaisesti, mutta niitä ei voi sisällyttää suunnitteluun. Jos **Yhdistetty kalenteriin** -kenttä deaktivoidaan, suunnitteluun määritellään vain tuotantosolun kapasiteetti, muttei kuormitusryhmän kapasiteettia.

Jos tuotantosoluksi on kuitenkin yhdistetty identtisiä kuormitusryhmiä (kuten 210 Pakkausosasto 1 ja 220 Pakkausosasto 2), tuotantosolu kannattaa käsittää määriteltyjen kuormitusryhmien summaksi. Tämän vuoksi tuotantosolu luetteloitaisiin nollakapasiteetilla. Jos **Yhdistetty kalenteriin** -kenttä aktivoidaan, yleinen kapasiteetti määritellään tuotantosolulle.

Jos tuotantosolujen kapasiteettien ei ole tarkoitus vaikuttaa kokonaiskapasiteettiin, sen voi saavuttaa asettamalla tehokkuudeksi 0.

## Kapasiteettirajoitetun kuormitusryhmän tai tuotantosolun määrittäminen

Tässä taulukossa on mahdollista määritellä tuotantoresurssit niille alueille, joita pidät kriittisinä, ja merkitä ne hyväksymään äärellinen kuormitus oletusarvoisen äärettömän kuormituksen sijaan, jotka muut tuotantoresurssit hyväksyvät. Kapasiteettirajoitettu resurssi voi olla tuotantosolu tai kuormitusryhmä, jonka olet tunnistanut pullonkaulaksi ja jolle haluaisit määritellä rajoitetun (rajallisen) kuormituksen.

[!INCLUDE[prod_short](includes/prod_short.md)] ei tue yksityiskohtaista työnohjausta. Se suunnittelee resurssien käytön tarjoamalla karkean aikataulun, mutta se ei luo ja ylläpidä automaattisesti tarkkoja aikatauluja prioriteetteihin tai optimointisääntöihin perustuen.

Voit tehdä **Kapasiteettirajoitetut resurssit** -sivulla määritykset, jotka estävät tiettyjen resurssien ylikuormituksen ja varmistaa, että kapasiteettia ei jää kohdentamatta, jos se voisi parantaa tuotantotilauksen läpimenoaikaa. Voit lisätä **Vaimennin (% koko kapasiteetista)** -kenttään resurssien puskuriajan toiminnon jaon minimoimiseksi. Tämän avulla järjestelmä ajoittaa kuormituksen viimeiseen mahdolliseen päivään niin, että kriittinen kuormitusprosentti ylittyy hieman. Tämä voi vähentää jaettavien toimintojen määrää.

Kun suunnitellaan kapasiteettirajoitettuja resursseja, järjestelmä varmistaa, että resurssia ei ole kuormitettu enempää kuin sille määritetty kapasiteetti osoittaa (kriittinen kuormitus). Tämä tehdään määrittämällä jokaiselle toiminnolle lähin mahdollinen aika. Jos ajankohta ei ole tarpeeksi suuri koko toiminnon suorittamiseksi, toiminto jaetaan kahdeksi tai useammaksi osaksi, jotka sijoitetaan lähimpiin käytettävissä oleviin ajankohtiin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kapasiteettirajoitetut resurssit** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät.

> [!NOTE]
> Toiminnot niissä kuormitusryhmissä tai tuotantosoluissa, jotka on määritetty rajoitetuiksi resursseiksi, suunnitellaan aina sarjana. Tämä tarkoittaa, että vaikka rajoitetulla resurssilla on useita kapasiteetteja, näiden kapasiteettien suorittamia toimintoja voidaan suunnitellaan vain peräkkäin, ei rinnakkain, kuten tapahtuisi, jos tuotantosolua tai kuormitusryhmää ei olisi määritetty rajoitetuksi resurssiksi. Rajoitetun resurssin tuotantosolun tai kuormitusryhmän Kapasiteetti-kentän arvo on suurempi kuin 1.

> Jos toiminto jaetaan, asetusaika kohdistetaan vain kerran, koska oletetaan, että jotkin manuaaliset muutokset suoritetaan aikataulun optimoimiseksi.

## Katso myös

[Tuotantokalenterien luominen](production-how-to-create-work-center-calendars.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Suunnittelu](production-planning.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
