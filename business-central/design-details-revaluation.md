---
title: Rakennetiedot – uudelleenarvostus
description: 'Voit uudelleenarvostaa varaston sen arvostuksen perustan perusteella, joka vastaa varaston arvoa parhaiten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 07/07/2023
ms.custom: bap-template
---

# Rakennetiedot: uudelleenarvostus

Voit uudelleenarvostaa varaston sen arvostuksen perustan perusteella, joka vastaa varaston arvoa parhaiten. Voit myös päivittää uudelleenarvostuksen taaksepäin päivittääksesi jo myymiesi tuotteiden myytyjen tavaroiden kustannukset (COGS). Vakio-arvostusmenetelmää käyttävät nimikkeet, joita ei ole laskutettu kokonaan, voidaan myös arvostaa uudelleen.  

[!INCLUDE[prod_short](includes/prod_short.md)] tukee seuraavaa uudelleenarvostukseen liittyvää joustavuutta:  

- Uudelleenarvioitava määrä voidaan laskea mille päivälle tahansa, myös menneessä ajassa.  
- Vakioarvostusmenetelmää käyttävien nimikkeiden osalta oletetut kustannustapahtumat on sisällytetty uudelleenarvostukseen.  
- Järjestelmä havaitsee uudelleenarvostuksen aiheuttamia varaston arvon vähennyksiä.  

## Lasketaan uudelleenarvotettavaa määrää

Uudelleenarvostettava määrä on tiettynä päivänä käytettävissä oleva jäljellä oleva varasto. Määrä on uudelleenarvostuspäivänä tai sitä ennen kirjaamasi kokonaan laskutettujen nimiketapahtumien kokonaismäärä.  

> [!NOTE]  
>  Vakio-arvostusmenetelmää käyttäviä nimikkeitä käsitellään eri tavalla, kun lasketaan uudelleenarvotettavaa määrää nimike-, sijainti- ja varianttikohtaisesti. Nimikkeen pääkirjan kirjausten määriä ja arvoja ei ole täysin laskutettu ja ne on sisällytetty uudelleenarvostettavaan määrään.  

Kun uudelleenarvostus on kirjattu, voit kirjata varaston lisäyksen tai vähennyksen kirjauspäivämäärällä, joka on ennen uudelleenarvostuksen kirjauspäivämäärää. Uudelleenarvostus ei kuitenkaan vaikuta tähän määrään. Varaston täsmäytyksessä otetaan huomioon vain alkuperäinen uudelleenarvostettu määrä.  

Koska voit arvostaa uudelleen milloin tahansa, sinulla on oltava käytännöt, kun pidät tuotetta osana varastoa. Esimerkiksi, kun nimike on varastossa, ja kun kohde on keskeneräinen työ (KET).  

### Esimerkki  

Seuraavassa esimerkissä kuvataan milloin WIP-nimikkeiden siirroista tulee osa varastoa. Esimerkki perustuu ketjun ja 150 linkin tuotantoon.  

![KET-varasto ja uudelleenarvostus.](media/design_details_inventory_costing_10_revaluation_wip.png "KET-varasto ja uudelleenarvostus")  

**1Q**: käyttäjä kirjaa ostetut linkit vastaanotetuksi. Seuraavassa taulukossa kuvataan aiheutuva nimikkeen pääkirjan kirjaus.  

|Kirjauspvm|Nimike|Tapahtuman tyyppi|määrä.|Tapahtumanro|  
|------------------|----------|----------------|--------------|---------------|  
|01-01-20|LINKKI|Osto|150|1|  

> [!NOTE]  
>  Nyt vakio-arvostusmenetelmää käyttävä nimike on käytettävissä uudelleenarvostukseen.  

**1V**: käyttäjä kirjaa ostetut linkit laskutetuksi ja linkeistä tulee taloushallinnon näkökulmasta osa varastoa. Seuraavassa taulukossa on tuloksena saatavat arvotapahtumat.  

|Kirjauspvm|Tapahtuman tyyppi|Arvostuspvm|Kustannussumma (Tod.)|Nimiketapahtuman nro|Tapahtumanro|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Välitön kustannus|01-01-20|150.00|1|1|  

 **2Q + 2V**: käyttäjä kirjaa ostetut linkit kulutetuiksi rautaketjun tuotannolle. Taloudellisesta näkökulmasta linkeistä tulee osa KET-varastoa.  Seuraavassa taulukossa kuvataan aiheutuva nimikkeen pääkirjan kirjaus.  

|Kirjauspvm|Nimike|Tapahtuman tyyppi|määrä.|Tapahtumanro|  
|------------------|----------|----------------|--------------|---------------|  
|02-01-20|LINKKI|Kulutus|-150|1|  

Seuraavassa taulukossa kuvataan aiheutuva arvokirjaus.  

|Kirjauspvm|Tapahtuman tyyppi|Arvostuspvm|Kustannussumma (Tod.)|Nimiketapahtuman nro|Tapahtumanro|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|02-01-20|Välitön kustannus|02-01-20|-150.00|2|2|  

Arvostuspäivämääräksi määritetään kulutuksen kirjauspäivämäärä (1.2.2020) tavallisena varastoarvon laskuna.  

**3Q**: Käyttäjä kirjaa ketjun tuotokseksi ja päättää tuotantotilauksen. Seuraavassa taulukossa kuvataan aiheutuva nimikkeen pääkirjan kirjaus.  

|Kirjauspvm|Nimike|Tapahtuman tyyppi|Määrä|Tapahtumanro|  
|------------------|----------|----------------|--------------|---------------|  
|02-15-20|KETJU|Tuotos|1|3|  

**3V**: Käyttäjä suorittaa **Muuta kustannuksia - Nimiketapahtumat** -eräajon, joka kirjaa ketjun laskutetuksi ja osoittaa, että kaikki materiaalin kulutus on laskutettu kokonaisuudessaan. Taloudellisesta näkökulmasta linkit eivät kuulu enää osaksi KET-varastoa, kun tuotos kokonaan laskutettu ja oikaistu. Seuraavassa taulukossa on tuloksena saatavat arvotapahtumat.  

|Kirjauspvm|Tapahtuman tyyppi|Arvostuspvm|Kustannussumma (Tod.)|Nimiketapahtuman nro|Tapahtumanro|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Välitön kustannus|01-01-20|150.00|2|2|  
|02-01-20|Välitön kustannus|02-01-20|-150.00|2|2|  
|02-15-20|Välitön kustannus|02-15-20|150.00|3|3|  

## Oletettu kustannus uudelleenarvostuksessa

Uudelleenarvostettava määrä on uudelleenarvostuspäivänä tai sitä ennen kirjaamasi kokonaan laskutettujen nimikkeiden määrän summa. Kun osa nimikkeistä on vastaanotettu tai toimitettu, mutta ei laskutettu, niiden varastoarvoa voi laskea. Vakio-arvostusmenetelmää käyttävät nimikkeet eivät ole tässä suhteessa rajoitettuja.  

> [!NOTE]  
>  Toisen tyyppinen oletettu kustannus, joka voidaan arvostaa uudelleen on tiettyjen sääntöjen puitteissa KET-varasto. Lisätietoja on kohdassa [KET-varaston uudelleenarvostus](design-details-revaluation.md#wip-inventory-revaluation).  

Kun vakio-arvostusmenetelmää käyttävien nimikkeiden uudelleenarvostusmäärä lasketaan, myös nimiketapahtumat, joita ei ole laskutettu kokonaan, sisällytetään laskentaan. Nämä tapahtumat arvostetaan uudelleen uudelleenarvostuksen kirjaamisen yhteydessä. Kun laskutat uudelleenarvostetun tapahtuman, luodaan seuraavat arvotapahtumat:  

- Tavallinen laskun arvotapahtuma tapahtumatyypillä **Välitön kustannus**. Tässä kirjauksessa kustannussumma on suora kustannus lähtöriviltä.  
- Arvotapahtuman, jonka tapahtumatyyppi on **Varianssi**. Tämä tapahtuma tallentaa laskutettujen kustannusten ja uudelleenarvostettujen vakiokustannusten välisen eron.  
- Arvotapahtuman, jonka tapahtumatyyppi on **Uudelleenarvostus**. Tämä tapahtuma tallentaa oletetun kustannuksen uudelleenarvostuksen peruutuksen.

### Esimerkki  

Seuraava esimerkki perustuu ketjun tuotantoon edellisessä esimerkissä. Tässä esimerkissä havainnollistetaan, miten kolmen tyyppisiä tapahtumia luodaan seuraavan skenaarion perusteella:  

1.  Kirjaat ostetut lenkit vastaanotetuiksi yksikköhintaan 2,00 (PVA).  
2.  Kirjaat lenkkien uudelleenarvostukseksi uuden yksikkökustannuksen, joka on 3,00 (PVA). Tällöin vakiokustannukseksi tulee 3,00 (PVA).  
3.  Kirjaat ketjun lenkkien alkuperäisen oston laskujen perusteella. Ne ovat seuraavat arvokirjaukset:  

    1.  Laskun arvotapahtuma tapahtumatyypillä **Välitön kustannus**.  
    2.  Arvotapahtuma, jonka tapahtumatyyppi on **Uudelleenarvostus** oletetun kustannuksen uudelleenarvostuksen palautuksen kirjaamiseksi.  
    3.  Arvotapahtuma, jonka tapahtumatyyppi on varianssi, kirjaa laskutetun kustannuksen ja uudelleenarvostetun vakiokustannuksen välisen eron.  

Seuraavassa taulukossa näytetään tulokset.  

|Vaihe|Kirjauspäivämäärä|Tapahtuman tyyppi|Arvostuspvm|Kustannussumma (oletettu)|Kustannussumma (Tod.)|Nimiketapahtuman nro|Tapahtumanro|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|Välitön kustannus|01-15-20|300.00|0,00|1|1|  
|2.|01-20-20|Uudelleenarvostus|01-20-20|150.00|0,00|1|2|  
|3.a.|01-15-20|Välitön kustannus|01-15-20|-300.00|0,00|1|3|  
|3.b.|01-15-20|Uudelleenarvostus|01-20-20|-150.00|0,00|1|4|  
|3.c.|01-15-20|Vaihtelu|01-15-20|0.00|450.00|1|5|  

## Selvitä, vaikuttaako uudelleenarvostus varaston vähenemiseen  

Uudelleenarvostuksen tai tiliöinnin päivämäärää käytetään määrittämään, onko uudelleenarvostus vaikuttanut varaston vähenemiseen.  

Seuraavassa taulukossa esitetään kriteeri, jota käytetään nimikkeelle, joka ei käytä keskimääräistä kustannuslaskelmamenetelmää.  

|Skenaario|Tapahtumanro|Ajoitus|Uudelleenarvostuksen vaikuttama|  
|--------------|---------------|------------|-----------------------------|  
|A|Aiempi kuin uudelleenarvostustapahtuman numero|Aiempi kuin uudelleenarvostuksen kirjauspäivämäärä|Ei|  
|B|Aiempi kuin uudelleenarvostustapahtuman nro.|Vastaava kuin uudelleenarvostuksen kirjauspäivämäärä|Ei|  
|N|Aiempi kuin uudelleenarvostustapahtuman nro.|Myöhempi kuin uudelleenarvostuksen kirjauspäivämäärä|Kyllä|  
|P|Myöhempi kuin uudelleenarvostustapahtuman nro|Aiempi kuin uudelleenarvostuksen kirjauspäivämäärä|Kyllä|  
|I|Myöhempi kuin uudelleenarvostustapahtuman nro|Vastaava kuin uudelleenarvostuksen kirjauspäivämäärä|Kyllä|  
|N|Myöhempi kuin uudelleenarvostustapahtuman nro|Myöhempi kuin uudelleenarvostuksen kirjauspäivämäärä|Kyllä|  

### Esimerkki  

Seuraava esimerkki havainnollistaa FIFO-kustannuslaskentamenetelmää käyttävän kohteen uudelleenarvostusta. Esimerkki perustuu seuraavaan skenaarioon:  

1.  1.1.20 kirjaat 6 yksikön oston.  
2.  1.2.20 kirjaat 1 yksikön myynnin.  
3.  1.3.20 kirjaat 1 yksikön myynnin.  
4.  1.4.20 kirjaat 1 yksikön myynnin.  
5.  1.3.20 lasket varastoarvon nimikkeelle ja kirjaat nimikkeen kustannuksen uudelleenarvostuksen arvosta 10,00 PVA arvoon 8,00 PVA.  
6.  1.2.20 kirjaat 1 yksikön myynnin.  
7.  1.3.20 kirjaat 1 yksikön myynnin.  
8.  1.4.20 kirjaat 1 yksikön myynnin.  
9. Suoritat **Muuta kustannuksia - Nimiketapahtumat** -eräajon.  

Seuraavassa taulukossa on tuloksena saatavat arvotapahtumat.  

|Esimerkkitilanne|Kirjauspvm|Tapahtuman tyyppi|Arvostuspvm|Arvostettu määrä|Kustannussumma (Tod.)|Nimiketapahtuman nro|Tapahtumanro|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01-01-20|Osto|01-01-20|6|60,00|1|1|  
||03-01-20|Uudelleenarvostus|03-01-20|4|-8.00|1|5|  
|A|02-01-20|Myynti|02-01-20|-1|-10.00|2|2|  
|B|03-01-20|Myynti|03-01-20|-1|-10.00|3|3|  
|N|04-01-20|Myynti|04-01-20|-1|-10.00|4|4|  
||04-01-20|Myynti|04-01-20|-1|2,00|4|9|  
|P|02-01-20|Myynti|03-01-20|-1|-10.00|5|6|  
||02-01-20|Myynti|03-01-20|-1|2,00|5|10|  
|I|03-01-20|Myynti|03-01-20|-1|-10.00|6|7|  
||03-01-20|Myynti|03-01-20|-1|2,00|6|11|  
|N|04-01-20|Myynti|04-01-20|-1|-10.00|7|8|  
||04-01-20|Myynti|04-01-20|-1|2.00|7|12|  

## KET-varaston uudelleenarvostus  

KET-varaston uudelleenarvostus tarkoittaa sitä, että uudelleenarvostetaan KET-varastona rekisteröityjä komponentteja.  

On tärkeää, että on sopimuksia, jotka ohjaavat sitä, milloin nimike on KET-varasto taloudellisesta näkökulmasta. [!INCLUDE[prod_short](includes/prod_short.md)]issa on seuraavat käytännöt:  

- Ostetusta komponentista tulee osa raaka-ainevarastoa siitä hetkestä lähtien, kun osto kirjataan laskutetuksi.  
- Ostetusta/osakokoonpanon komponentista tulee osa KET-varastoa siitä hetkestä lähtien, kun sen kulutus kirjataan yhdessä tuotantotilauksen kanssa.  
- Ostettu/osakokoonpanon komponentti säilyy osana KET-varastoa siihen asti, kun tuotantotilaus (valmistettu nimike) laskutetaan.  

Kulutuksen arvotapahtuman arvostuspäivämäärä määritetään samojen sääntöjen perusteella kuin muun kuin KET-varaston säännöt. Saat lisätietoja siirtymällä kohtaan [Selvitä, vaikuttaako uudelleenarvostus varaston vähenemiseen](#determine-whether-revaluation-affects-an-inventory-decrease).  

Voit arvostaa KET-varaston uudelleen seuraavissa olosuhteissa:

- Uudelleenarvostuspvm on ennen niiden vastaavien nimiketapahtumien kirjauspäivämääriä, joiden tyyppi on kulutus.
- Et ole laskuttanut tuotantotilausta.  

> [!CAUTION]  
> **Varaston arvostus - WIP** -raportti osoittaa tiliöityjen tuotantotilauskirjausten arvon ja voi siksi olla hieman sekava WIP-nimikkeiden suhteen, jotka on uudelleenarvostettu.  

## Uudelleen arvioi nimikkeet, joilla on keskimääräinen arvostusmenetelmä

Voit arvostaa uudelleen vain ne nimikkeet, jotka käyttävät keskimääräistä arvostusmenetelmää, jos **Laske per** -kohdan arvona on *Nimike*.

Voit tehdä uudelleenarvostuksen vain kauden lopussa, joka on valittu **Keskimääräisen kustannuksen jakso** -kentässä **Varastonhallinnan asetukset** -sivulla.

Uudelleenarvostus ei vaikuta negatiivisiin transaktioihin kuluvana kuukautena, minkä vuoksi kokonaan kohdistetut saapuvat tapahtumat eivät sisälly myöskään.

### Esimerkki

Tässä esimerkissä näkyy, mitä tapahtuu, kun varaston arvo lasketaan **Nimikkeen uudelleenarvostuspäiväkirja** -sivulla. **Varastonhallinnan asetukset** -sivulla **Nimike** valitaan **Keskim. kust. laskentatyyppi** -kentässä ja **Kuukausi** valitaan **Keskimääräisen kustannuksen jakso** -kentässä.

Seuraavassa taulukossa näkyvät nimiketapahtumat esimerkkikeskihintaerälle ITEM1.

|Kirjauspäivämäärä|Nimiketapahtuman tyyppi|Määrä|Kustannussumma (todellinen)|Tapahtumanro|
|----|----|----|----|----|
25-04-23|Ostot|5|5.00|1
26-04-23|Ostot|3|3.00|2
27-04-23|Myynti|-5|-5.00|3
28-04-23|Myynti|-1|-1.00|4
13-05-23|Ostot|2|20.00|5
17-06-23|Myynti|-6|-22.00|6

Seuraavassa taulukossa on esitetty **Laske varaston arvo** -raportin suorituksen tulos, jossa on eri kirjauspäivät

|Kirjauspäivämäärä|Määrä|Kommentti|
|---|---|-------------|
30-04-23|2|Sisältää vain jäljellä olevan määrän tapahtumasta 2. Tapahtuma 1 kohdistetaan kokonaan ennen kirjauspäivämäärää, ja tapahtuma 5 on kirjauspäivämäärän jälkeen.
31-05-23|4|Sisältää jäljellä olevat määrät tapahtumista 2 ja 13.
30-06-23|0|Ei jäljellä olevaa määrää kirjauspäivämääränä.

Seuraavien tapahtumien tulos on 0, riippumatta kirjauspäivämäärästä.

|Kirjauspäivämäärä|Nimiketapahtuman tyyppi|Määrä|Kustannussumma (todellinen)|Tapahtumanro|
|----|----|----|----|----|
13-05-23|Ostot|5|5.00|1
26-04-23|Myynti|-5|5.00|2

## Katso myös  

[Rakennetiedot: Varaston kustannuslaskenta](design-details-inventory-costing.md)   
[Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md)   
[Rakennetiedot: Varaston arvostus](design-details-inventory-valuation.md)
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Rahoitus](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
