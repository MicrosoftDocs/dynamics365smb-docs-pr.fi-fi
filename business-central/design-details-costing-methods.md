---
title: Rakennetiedot – Arvostusmenetelmät
description: 'Tässä aiheessa käsitellään arvostusmenetelmän vaikutusta siihen, miten todelliset ja budjetoidut arvot siirretään pääomaan ja käytetään kustannuslaskennassa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 05/12/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Rakennetiedot: arvostusmenetelmät

Arvostusmenetelmä määrittää, siirretäänkö todellinen tai budjetoitu arvo pääomaan ja käytetäänkö sitä kustannuslaskennassa. Kirjauspäivämäärän ja järjestyksen kanssa arvostusmenetelmä vaikuttaa myös siihen, miten kustannusvirta tallennetaan.

> [!NOTE]
> Et voi muuttaa tuotteen arvostusmenetelmää jos tuotteelle on olemassa nimikekirjaus Lisätietoja on kohdassa [Suunnittelun yksityiskohdat: muuta nimikkeiden arvostusmenetelmää](design-details-changing-costing-methods.md).

Seuraavia menetelmiä tuetaan kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]:  

| Arvostusmenetelmä | Kuvaus | Käyttäminen |
|--|--|--|
| FIFO | Nimikkeen yksikkökustannus on FIFO-säännön perusteella valitun nimikkeen vastaanoton todellinen arvo.<br /><br /> Varastonarvostuksessa oletetaan, että ensin varastoon sijoitetut nimikkeet myydään ensin. | Liiketoimintaympäristöissä, joissa tuotteen kustannus on vakaa.<br /><br /> (Kun hinnat nousevat, taseessa näkyy suurempi arvo. Tämä tarkoittaa, että verovelat kasvavat, mutta luottoluokitus ja rahanlainauskyky paranevat.)<br /><br /> Nimikkeille, joilla on rajoitettu varastointiaika, koska vanhimmat tavarat täytyy myydä ennen kuin niiden viimeinen myyntipäivä ohitetaan. |
| LIFO | Nimikkeen yksikkökustannus on LIFO-säännön perusteella valitun nimikkeen vastaanoton todellinen arvo.<br /><br /> Varastonarvostuksessa oletetaan, että viimeiseksi varastoon sijoitetut nimikkeet myydään ensin. | Ei sallittu monissa maissa/monilla alueilla, koska sitä voidaan käyttää voiton alas painamiseen.<br /><br /> (Kun hinnat nousevat, tuloslaskelman arvo pienenee. Tämä tarkoittaa, että verovelat vähenevät, mutta rahanlainauskyky heikkenee.) |
| Keskiarvo | Nimikkeen yksikkökustannus lasketaan kussakin vaiheessa keskimääräisenä yksikkökustannuksena oston jälkeen.<br /><br /> Varastonarvostus olettaa, että kaikki vaihto-omaisuus myydään samanaikaisesti. | Liiketoimintaympäristöissä, joissa tuotteen kustannus on epävakaa.<br /><br /> Käytä, kun vaihto-omaisuus on pinottu tai sekoitettu yhteen, eikä niitä voida erottaa, kuten kemikaalit. |
| Määrätty | Nimikkeen yksikkökustannus on tarkka kustannus, jolloin tietty yksikkö vastaanotettiin. | Tuotannon tai kaupan helposti tunnistettavissa nimikkeissä, joilla on suhteellisen korkeat yksikkökustannukset.<br /><br /> Nimikkeille, jotka ovat säätelyn alaisia.<br /><br /> Nimikkeille, joilla on sarjanumero. |
| Vakio | Nimikkeen yksikkökustannus määritetty etukäteen arvion perusteella.<br /><br /> Kun todelliset kustannukset realisoituvat myöhemmin, vakiokustannus täytyy mukauttaa todellisiin kustannuksiin varianssin arvojen kautta. | Missä kustannusten valvonta on erittäin tärkeää.<br /><br /> Toistuvassa valmistuksessa arvostaaksesi suoria materiaali- ja resurssikustannuksia sekä valmistuksen yleiskustannuksia.<br /><br /> Jos standardien ylläpitämiseksi on olemassa kurinalaisuutta ja henkilöstöä. |

Seuraavassa kuvassa esitetään, kuinka kustannukset virtaavat varaston läpi kussakin kustannuslaskelmamenetelmässä.  

![Arvostusmenetelmät visualisoituna.](media/design_details_inventory_costing_7_costing_methods.png "Arvostusmenetelmät visualisoituna")  

Arvostusmenetelmät eroavat siinä, miten ne arvostavat varaston vähennyksiä, ja että käyttävätkö ne todellista kustannusta vai vakiokustannusta arvostuksen perustana. Seuraavassa taulukossa selitetään eri ominaisuudet. (LIFO-menetelmä on suljettu pois, koska se on hyvin samankaltainen kuin FIFO-menetelmä.)  
<!--Old  table
|Category|FIFO|Average|Standard|Specific|  
|-|----------|-------------|--------------|--------------|  
|General characteristic|Easy to understand|Based on period options: **Day**/**Week**/**Month**/**Quarter**/**Accounting Period**.<br /><br /> Can be calculated per item or per item/location/variant.|Easy to use, but requires qualified maintenance.|Requires item tracking on both inbound and outbound transaction.<br /><br /> Typically used for serialized items.|  
|Application/Adjustment|Application keeps track of **the remaining quantity**.<br /><br /> Adjustment forwards costs according to quantity application.|Application keeps track of the **remaining quantity**.<br /><br /> Costs are calculated and forwarded per the **valuation date**.|Application keeps track of the **remaining quantity**.<br /><br /> Application is based on FIFO.|All applications are fixed.|  
|Revaluation|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item only.<br /><br /> Can be done backward in time.|Revalues invoiced and un-invoiced quantities.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|  
|Miscellaneous|If you back-date an inventory decrease, then existing entries are NOT reapplied to provide a correct FIFO cost flow.|If you back-date an inventory increase or decrease, then the average cost is recalculated, and all affected entries are adjusted.<br /><br /> If you change the period or calculation type, then all affected entries must be adjusted.|Use the **Standard Worksheet** page to periodically update and roll up standard costs.<br /><br /> Is NOT supported per SKU.<br /><br /> No historic records exist for standard costs.|You can use specific item tracking without using the Specific costing method. Then the cost will NOT follow the lot number, but the cost assumption of the selected costing method.|  
-->
<!--Table flipped for slightly better readability -->

||Yleiset ominaisuudet|Sovellus/muutos |Uudelleenarvostus|Sekalaista |
|-|---------|---------|---------|---------|
|**FIFO**     |Helppo ymmärtää|Sovellus seuraa **jäljellä olevaa määrää**.<br /><br /> Säätäminen välittää kustannukset määrän kohdistuksen mukaisesti. |Uudelleen arvostaa vain laskutetut määrät.<br /><br /> Voidaan suorittaa nimikekohtaisesti tai tapahtumakohtaisesti.<br /><br /> Voidaan suorittaa ajassa taaksepäin.|Jos asetat varaston arvon vähennyksen takautuvasti, olemassa olevia tapahtumia EI kohdisteta uudelleen oikean FIFO-kustannusvirran luomiseksi.|
|**Keskiarvo**     |Perustuu jakson vaihtoehtoihin: **päivä**/**viikko**/**kuukausi**/**vuosineljännes**/**kirjanpitojakso**.<br /><br /> Voidaan laskea nimikekohtaisesti tai nimikkeen/sijainnin/variantin mukaan.|Sovellus seuraa **jäljellä olevaa määrää**.<br /><br /> Kustannukset lasketaan ja siirretään edelleen **arvostuspäivämäärän** mukaan. |Uudelleen arvostaa vain laskutetut määrät.<br /><br /> Voidaan suorittaa vain nimikettä kohden.<br /><br /> Voidaan suorittaa ajassa taaksepäin. |Jos asetat varaston arvon nousun tai vähennyksen takautuvasti, keskimääräinen kustannus lasketaan uudelleen ja kaikki liittyvät tapahtumat oikaistaan.<br /><br /> Jos vaihdat jaksoa tai laskentatyyppiä, kaikkia liittyviä tapahtumia on muutettava.|
|**Vakio**     |Helppo käyttää, mutta vaatii pätevää kunnossapitoa|Sovellus seuraa **jäljellä olevaa määrää**.<br /><br /> Sovellus perustuu FIFO-käytäntöön.|Uudelleen arvostaa laskutetut ja laskuttamattomat määrät.<br /><br /> Voidaan suorittaa nimikekohtaisesti tai tapahtumakohtaisesti.<br /><br /> Voidaan suorittaa ajassa taaksepäin.|Voit päivittää ja vyöryttää vakiokustannukset säännöllisesti **Vakiotyökirja**-sivun avulla.<br /><br /> EI tueta varastoyksikkökohtaisesti.<br /><br /> Historiallisia tietueita ei ole olemassa standardikustannuksille.|
|**Yksilöity**     |Vaatii nimikeseurantaa sekä saapuvissa että lähtevissä tapahtumissa.<br /><br /> Yleensä käytetään sarjoitettuja nimikkeitä|Kaikki sovellukset ovat kiinteitä.|Uudelleen arvostaa vain laskutetut määrät.<br /><br /> Voidaan suorittaa nimikekohtaisesti tai tapahtumakohtaisesti.<br /><br /> Voidaan suorittaa ajassa taaksepäin.|Voit käyttää tietyn nimikkeen seurantaa ilman Spesifinen-arvostusmenetelmän käyttöä. Kustannukset eivät seuraa eränumeroa, vaan valitun arvostusmenetelmän kustannusten oletusta.|

## Esimerkki

Tässä osassa on esimerkkejä siitä, miten erilaiset arvostusmenetelmät vaikuttavat varaston arvoon.  

Seuraavassa taulukossa esitetään varaston kasvut ja vähennykset, joihin esimerkit perustuvat.  

|Kirjauspvm|määrä.|Tapahtumanro|  
|------------------|--------------|---------------|  
|01-01-20|1|1|  
|01-01-20|1|2|  
|01-01-20|1|3|  
|02-01-20|-1|4|  
|03-01-20|-1|5|  
|04-01-20|-1|6|  

> [!NOTE]  
> Tästä seuraava määrä varastossa on nolla. Näin ollen myös varastoarvon on oltava nolla arvostusmenetelmästä riippumatta.  

### Arvostusmenetelmien vaikutus arvostetussa varastossa kasvaa  

Niiden nimikkeiden kohdalla, jotka käyttävät todelliseen kustannukseen pohjautuvaa arvostusmenetelmää (**FIFO**, **LIFO**, **Keskimääräinen** tai **Spesifinen**), varaston arvon nousut arvostetaan nimikkeen hankintamenon mukaan.  

- **Vakio**  

    **Vakio**arvostusmenetelmää käyttävien nimikkeiden kohdalla varastoarvon nousut arvostetaan nimikkeen nykyisellä vakiokustannuksella.  

#### Vakio  

**Vakio**-arvostusmenetelmää käyttävien nimikkeiden kohdalla varastoarvon nousut arvostetaan nimikkeen nykyisellä vakiokustannuksella.  

### Arvostusmenetelmien vaikutus arvostetussa varastossa laskee

- **FIFO**  

    **FIFO**-arvostusmenetelmää käyttävien nimikkeiden osalta ensimmäisinä ostetut nimikkeet myydään aina ensin (tapahtumanumerot 3, 2 ja 1 tässä esimerkissä). Vastaavasti, varaston arvon laskut arvostetaan ottamalla varaston ensimmäisen arvonnousun arvo.  

     Myytyjen tuotteiden kustannukset lasketaan käyttämällä ensimmäisen varastohankinnan arvoa.  

     Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan **FIFO**- kustannuslaskelmamenetelmässä.  

    |Kirjauspvm|määrä.|Kustannussumma (Tod.)|Tapahtumanro|  
    |------------------|--------------|----------------------------|---------------|  
    |02-01-20|-1|-10.00|4|  
    |03-01-20|-1|-20.00|5|  
    |04-01-20|-1|-30.00|6|  

- **LIFO**  

    **LIFO**-arvostusmenetelmää käyttävien nimikkeiden osalta viimeksi ostetut nimikkeet myydään aina ensin (tapahtumanumerot 3, 2 ja 1 tässä esimerkissä). Vastaavasti, varaston arvon laskut arvostetaan ottamalla varaston viimeisen arvonnousun arvo.  

     Myytyjen tuotteiden kustannukset lasketaan käyttämällä viimeisimmän varastohankinnan arvoa.  

     Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan **LIFO**- kustannuslaskelmamenetelmässä.  

    |Kirjauspvm|määrä.|Kustannussumma (Tod.)|Tapahtumanro|  
    |------------|--------|--------------------|---------|  
    |02-01-20|-1|-30.00|4|  
    |03-01-20|-1|-20.00|5|  
    |04-01-20|-1|-10.00|6|  

- **Keskiarvo**  

    Niiden nimikkeiden kohdalla, jotka käyttävät **Keskimääräinen** arvostusmenetelmää, varastoarvon vähennykset määritetään laskemalla painotettu keskiarvo jäljellä olevasta varastosta viimeisenä keskimääräisen kustannusjakson päivänä jona varastoarvon vähennys kirjattiin. Katso lisätietoja kohdasta [Rakennetiedot: Keskimääräinen kustannus](design-details-average-cost.md).  

     Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan **Keskimääräisessä** kustannuslaskelmamenetelmässä.  

    | Kirjauspvm | määrä. | Kustannussumma (Tod.) | Tapahtumanro |
    |--|--|--|--|
    | 02-01-20 | -1 | -20.00 | 4 |
    | 03-01-20 | -1 | -20.00 | 5 |
    | 04-01-20 | -1 | -20.00 | 6 |

- **Vakio**  

    **Vakio**-arvostusmenetelmää käyttävien nimikkeiden osalta varaston arvon vähennykset arvostetaan vastaavasti kuin **FIFO**- arvostusmenetelmässä, mutta arvostus perustuu vakiokustannukseen, eikä todelliseen kustannukseen.  

    Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan **Perus**-kustannuslaskelmamenetelmässä.  

    |Kirjauspvm|määrä.|Kustannussumma (Tod.)|Tapahtumanro|  
    |------------------|--------------|----------------------------|---------------|  
    |02-01-20|-1|-15.00|4|  
    |03-01-20|-1|-15.00|5|  
    |04-01-20|-1|-15.00|6|  

- **Määrätty**  

    Arvostusmenetelmät luovat oletuksen siitä, kuinka kustannusvirtaukset varastosta nousevat varaston vähentyessä. Jos kustannusvirrasta on kuitenkin olemassa tarkempia tietoja, voit ohittaa tämän oletuksen luomalla tapahtumien välille kiinteän kohdistuksen. Kiinteä kohdistus luo linkin varaston arvon vähennyksen ja tietyn varaston lisäyksen välille ja ohjaa kustannusvirran vastaavasti.  

    **Spesifinen**-arvostusmenetelmää käyttävien nimikkeiden osalta varaston arvon vähennykset arvostetaan varaston arvon nousun mukaan, johon se on linkitetty kiinteällä kohdistuksella.  

    Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan **Erityisessä** kustannuslaskelmamenetelmässä.  

    |Kirjauspvm|määrä.|Kustannussumma (Tod.)|Kohdistetaan tapahtumaan|Tapahtumanro|
    |------------|--------|--------------------|----------------|---------|  
    |02-01-20|-1|-20.00|**2**|4|  
    |03-01-20|-1|-10.00|**1**|5|  
    |04-01-20|-1|-30.00|**3**|6|  

## Katso myös

[Rakennetiedot: Varaston kustannuslaskenta](design-details-inventory-costing.md)  
[Rakennetiedot: Varianssi](design-details-variance.md)  
[Rakennetiedot: Keskimääräinen kustannus](design-details-average-cost.md)  
[Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Termisanasto Dynamics 365:n liiketoimintaprosesseissa](/dynamics365/guidance/business-processes/glossary)  
[Tuotteen ja palvelun kustannuslaskennan yhteenvedon määrittäminen](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
