---
title: Rakennetiedot – uudelleenarvostus
description: 'Voit uudelleenarvostaa varaston sen arvostuksen perustan perusteella, joka vastaa varaston arvoa parhaiten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-revaluation" />Rakennetiedot: uudelleenarvostus
Voit uudelleenarvostaa varaston sen arvostuksen perustan perusteella, joka vastaa varaston arvoa parhaiten. Voit myös päivätä uudelleenarvostuksen vanhemmaksi, jolloin myytyjen tuotteiden kustannukset päivitetään oikein nimikkeille, jotka on jo myyty. Vakio-arvostusmenetelmää käyttävät nimikkeet, joita ei ole laskutettu kokonaan, voidaan myös arvostaa uudelleen.  

[!INCLUDE[prod_short](includes/prod_short.md)] tukee seuraavaa uudelleenarvostukseen liittyvää joustavuutta:  

-   Uudelleenarvioitava määrä voidaan laskea mille päivälle tahansa, myös menneessä ajassa.  
-   Vakioarvostusmenetelmää käyttävien nimikkeiden osalta oletetut kustannustapahtumat on sisällytetty uudelleenarvostukseen.  
-   Järjestelmä havaitsee uudelleenarvostuksen aiheuttamia varaston arvon vähennyksiä.  

## <a name="calculating-the-revaluable-quantity" />Lasketaan uudelleenarvotettavaa määrää
 Uudelleenarvostettava määrä on jäljellä oleva määrä varastossa, joka on käytettävissä uudelleenarvostukseen annetulla päivämäärällä. Se lasketaan kokonaissummana kokonaan laskutetuista nimiketapahtumista, joiden kirjauspäivämäärä on sama tai aiempi kuin uudelleenarvostuksen kirjauspäivämäärä.  

> [!NOTE]  
>  Vakio-arvostusmenetelmää käyttäviä nimikkeitä käsitellään eri tavalla, kun lasketaan uudelleenarvotettavaa määrää nimike-, sijainti- ja varianttikohtaisesti. Nimikkeen pääkirjan kirjausten määriä ja arvoja ei ole täysin laskutettu ja ne on sisällytetty uudelleenarvostettavaan määrään.  

Kun uudelleenarvostus on kirjattu, voit kirjata varaston lisäyksen tai vähennyksen kirjauspäivämäärällä, joka on ennen uudelleenarvostuksen kirjauspäivämäärää. Uudelleenarvostus ei kuitenkaan vaikuta tähän määrään. Varaston täsmäytyksessä otetaan huomioon vain alkuperäinen uudelleenarvostettu määrä.  

Koska uudelleenarvostus voidaan tehdä minä tahansa päivänä, sinun on määritettävä yleinen käytäntö, jonka mukaan nimikkeen voidaan katsoa olevan osa varastoa taloushallinnon näkökulmasta. Esimerkiksi, kun nimike on varastossa, ja kun kohde on keskeneräinen työ (KET).  

### <a name="example" />Esimerkki
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

## <a name="expected-cost-in-revaluation" />Oletettu kustannus uudelleenarvostuksessa
Uudelleenarvostettava määrä lasketaan määrän summana kokonaan laskutetuille nimikkeen pääkirjan kirjauksille, joiden tiliöintipäivä on yhtä suuri tai aiempi kuin uudelleenarvostuspäivä. Tämä tarkoittaa sitä, että kun osa nimikkeistä on vastaanotettu/toimitettu, mutta ei laskutettu, niiden varastoarvoa voi laskea. Vakio-arvostusmenetelmää käyttävät nimikkeet eivät ole tässä suhteessa rajoitettuja.  

> [!NOTE]  
>  Toisen tyyppinen oletettu kustannus, joka voidaan arvostaa uudelleen on tiettyjen sääntöjen puitteissa KET-varasto. Lisätietoja on kohdassa [KET-varaston uudelleenarvostus](design-details-revaluation.md#wip-inventory-revaluation).  

Kun vakio-arvostusmenetelmää käyttävien nimikkeiden uudelleenarvostusmäärä lasketaan, myös nimiketapahtumat, joita ei ole laskutettu kokonaan, sisällytetään laskentaan. Nämä tapahtumat arvostetaan uudelleen uudelleenarvostuksen kirjaamisen yhteydessä. Kun laskutat uudelleenarvostetun tapahtuman, luodaan seuraavat arvotapahtumat:  

-   Tavallinen laskun arvotapahtuma tapahtumatyypillä **Välitön kustannus**. Tässä kirjauksessa kustannussumma on suora kustannus lähtöriviltä.  
-   Arvotapahtuman, jonka tapahtumatyyppi on **Varianssi**. Tämä tapahtuma tallentaa laskutettujen kustannusten ja uudelleenarvostettujen vakiokustannusten välisen eron.  
-   Arvotapahtuman, jonka tapahtumatyyppi on **Uudelleenarvostus**. Tämä tapahtuma tallentaa oletetun kustannuksen uudelleenarvostuksen peruutuksen.  

### <a name="example-1" />Esimerkki
Seuraava esimerkki, joka perustuu edellisen esimerkin ketjun valmistukseen, kuvaa, kuinka kolme kirjaustyyppiä luodaan. Se perustuu seuraavaan skenaarioon:  

1.  Käyttäjä kirjaa ostetut lenkit vastaanotetuiksi yksikköhintaan 2,00 (PVA).  
2.  Käyttäjä kirjaa tämän jälkeen lenkkien uudelleenarvostukseksi uuden yksikkökustannuksen, joka on 3,00 (PVA). Tällöin vakiokustannukseksi tulee 3,00 (PVA).  
3.  Käyttäjä kirjaa lenkkien alkuperäisen oston laskujen perusteella. Ne ovat seuraavat:  

    1.  Laskun arvotapahtuma tapahtumatyypillä **Välitön kustannus**.  
    2.  Arvotapahtuma, jonka tapahtumatyyppi on **Uudelleenarvostus** oletetun kustannuksen uudelleenarvostuksen palautuksen kirjaamiseksi.  
    3.  Arvotapahtuma, jonka tapahtumatyyppi on varianssi, kirjaa laskutetun kustannuksen ja uudelleenarvostetun vakiokustannuksen välisen eron.  
Seuraavassa taulukossa on tuloksena saatavat arvotapahtumat.  

|Vaihe|Kirjauspvm|Tapahtuman tyyppi|Arvostuspvm|Kustannussumma (oletettu)|Kustannussumma (Tod.)|Nimiketapahtuman nro|Tapahtumanro|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|Välitön kustannus|01-15-20|300.00|0,00|1|1|  
|2.|01-20-20|Uudelleenarvostus|01-20-20|150.00|0,00|1|2|  
|3.a.|01-15-20|Välitön kustannus|01-15-20|-300.00|0,00|1|3|  
|3.b.|01-15-20|Uudelleenarvostus|01-20-20|-150.00|0,00|1|4|  
|3.c.|01-15-20|Vaihtelu.|01-15-20|0.00|450,00|1|5|  

## <a name="determining-whether-an-inventory-decrease-is-affected-by-revaluation" />Määritetään vaikuttaako uudelleenarvostus varaston vähennykseen
Uudelleenarvostuksen tai tiliöinnin päivämäärää käytetään määrittämään onko uudelleenarvostus vaikuttanut varaston vähenemiseen.  

Seuraavassa taulukossa esitetään kriteeri, jota käytetään nimikkeelle, joka ei käytä keskimääräistä kustannuslaskelmamenetelmää.  

|Esimerkkitilanne|Tapahtumanro|Ajoitus|Uudelleenarvostuksen vaikuttama|  
|--------------|---------------|------------|-----------------------------|  
|A|Aiempi kuin uudelleenarvostustapahtuman numero|Aiempi kuin uudelleenarvostuksen kirjauspäivämäärä|Ei|  
|B|Aiempi kuin uudelleenarvostustapahtuman nro.|Vastaava kuin uudelleenarvostuksen kirjauspäivämäärä|Ei|  
|N|Aiempi kuin uudelleenarvostustapahtuman nro.|Myöhempi kuin uudelleenarvostuksen kirjauspäivämäärä|Kyllä|  
|P|Myöhempi kuin uudelleenarvostustapahtuman nro|Aiempi kuin uudelleenarvostuksen kirjauspäivämäärä|Kyllä|  
|I|Myöhempi kuin uudelleenarvostustapahtuman nro|Vastaava kuin uudelleenarvostuksen kirjauspäivämäärä|Kyllä|  
|N|Myöhempi kuin uudelleenarvostustapahtuman nro|Myöhempi kuin uudelleenarvostuksen kirjauspäivämäärä|Kyllä|  

### <a name="example-2" />Esimerkki
Seuraava esimerkki, jossa kuvataan sellaisen nimikkeen uudelleenarvostus, joka käyttää FIFO-kustannuslaskentamenetelmää, perustuu seuraavaan skenaarioon:  

1.  1.1.2000 käyttäjä kirjaa 6 yksikön oston.  
2.  1.2.2000 käyttäjä kirjaa 1 yksikön myynnin.  
3.  Käyttäjä kirjaa yhden yksikön myynnin kohteessa 03-01-20.  
4.  Käyttäjä kirjaa yhden yksikön myynnin kohteessa 04-01-20.  
5.  1.3.2000 käyttäjä laskee varastoarvon nimikkeelle ja kirjaa nimikkeen kustannuksen uudelleenarvostuksen arvosta 10,00 PVA arvoon 8,00 PVA.  
6.  1.2.2000 käyttäjä kirjaa 1 yksikön myynnin.  
7.  Käyttäjä kirjaa yhden yksikön myynnin kohteessa 03-01-20.  
8.  Käyttäjä kirjaa yhden yksikön myynnin kohteessa 04-01-20.  
9. Käyttäjät suorittavat **Muuta kustannuksia - Nimiketapahtumat** -eräajon.  

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
||04-01-20|Myynti|04-01-20|-1|2,00|7|12|  

## <a name="wip-inventory-revaluation" />KET-varaston uudelleenarvostus
WIP-varaston uudelleenarvostus käsittää uudelleenarvostettuja osia, jotka rekisteröidään osana WIP-varastoa uudelleenarvostusajankohtana.  

Tämä huomioon ottaen on tärkeää muodostaa käytännöt sille, milloin nimikettä pidetään osana KET-varastoa taloudellisesta näkökulmasta. [!INCLUDE[prod_short](includes/prod_short.md)]issa on seuraavat käytännöt:  

-   Ostetusta komponentista tulee osa raaka-ainevarastoa siitä hetkestä lähtien, kun osto kirjataan laskutetuksi.  
-   Ostetusta/osakokoonpanon komponentista tulee osa KET-varastoa siitä hetkestä lähtien, kun sen kulutus kirjataan yhdessä tuotantotilauksen kanssa.  
-   Ostettu/osakokoonpanon komponentti säilyy osana KET-varastoa siihen asti, kun tuotantotilaus (valmistettu nimike) laskutetaan.  

Kulutuksen arvotapahtuman arvostuspäivämäärä määritetään samojen sääntöjen perusteella kuin muun kuin KET-varaston säännöt. Katso lisätietoja: [Määritetään vaikuttaako uudelleenarvostus varaston vähennykseen](design-details-revaluation.md#determining-whether-an-inventory-decrease-is-affected-by-revaluation).  

KET-varasto voidaan uudelleenarvioida niin kauan kuin uudelleenarvostuksen päivämäärä ei ole myöhempi kuin Kulutus-tyyppiä olevien vastaavien nimiketapahtumien kirjauspäivämäärä ja vastaavaa tuotantotilausta ei ole vielä laskutettu.  

> [!CAUTION]  
>  **Varaston arvostus - WIP** -raportti osoittaa tiliöityjen tuotantotilauskirjausten arvon ja voi siksi olla hieman sekava WIP-nimikkeiden suhteen, jotka on uudelleenarvostettu.  

## <a name="see-also" />Katso myös
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
 [Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md)   
 [Rakennetiedot: Varaston arvostus](design-details-inventory-valuation.md) [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
 [Rahoitus](finance.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
