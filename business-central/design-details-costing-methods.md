---
title: Rakennetiedot – arvostusmenetelmät
description: Tässä aiheessa käsitellään arvostusmenetelmän vaikutusta siihen, miten todelliset ja budjetoidut arvot siirretään pääomaan ja käytetään kustannuslaskennassa.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: b3bfdbc2fb163d48edb6bf22eb79efa01b63090f
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442433"
---
# <a name="design-details-costing-methods"></a>Rakennetiedot: arvostusmenetelmät

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

 ![Arvostusmenetelmät.](media/design_details_inventory_costing_7_costing_methods.png "Arvostusmenetelmät")  

 Arvostusmenetelmät eroavat siinä, miten ne arvostavat varaston vähennyksiä, ja että käyttävätkö ne todellista kustannusta vai vakiokustannusta arvostuksen perustana. Seuraavassa taulukossa selitetään eri ominaisuudet. (LIFO-menetelmä on suljettu pois, koska se on hyvin samankaltainen kuin FIFO-menetelmä.)  

|Luokka|FIFO|Keskiarvo|Vakio|Määrätty|  
|-|----------|-------------|--------------|--------------|  
|Yleiset ominaisuudet|Helppo ymmärtää|Perustuu jakson vaihtoehtoihin: **päivä**/**viikko**/**kuukausi**/**vuosineljännes**/**kirjanpitojakso**.<br /><br /> Voidaan laskea nimikekohtaisesti tai nimikkeen/sijainnin/variantin mukaan.|Helppo käyttää, mutta vaatii pätevää kunnossapitoa|Vaatii nimikeseurantaa sekä saapuvissa että lähtevissä tapahtumissa.<br /><br /> Yleensä käytetään sarjoitettuja nimikkeitä|  
|Sovellus/muutos|Sovellus seuraa **jäljellä olevaa määrää**.<br /><br /> Säätäminen välittää kustannukset määrän kohdistuksen mukaisesti.|Sovellus seuraa **jäljellä olevaa määrää**.<br /><br /> Kustannukset lasketaan ja siirretään edelleen **arvostuspäivämäärän** mukaan.|Sovellus seuraa **jäljellä olevaa määrää**.<br /><br /> Sovellus perustuu FIFO-käytäntöön.|Kaikki sovellukset ovat kiinteitä.|  
|Uudelleenarvostus|Uudelleen arvostaa vain laskutetut määrät.<br /><br /> Voidaan suorittaa nimikekohtaisesti tai tapahtumakohtaisesti.<br /><br /> Voidaan suorittaa ajassa taaksepäin.|Uudelleen arvostaa vain laskutetut määrät.<br /><br /> Voidaan suorittaa vain nimikettä kohden.<br /><br /> Voidaan suorittaa ajassa taaksepäin.|Uudelleen arvostaa laskutetut ja laskuttamattomat määrät.<br /><br /> Voidaan suorittaa nimikekohtaisesti tai tapahtumakohtaisesti.<br /><br /> Voidaan suorittaa ajassa taaksepäin.|Uudelleen arvostaa vain laskutetut määrät.<br /><br /> Voidaan suorittaa nimikekohtaisesti tai tapahtumakohtaisesti.<br /><br /> Voidaan suorittaa ajassa taaksepäin.|  
|Sekalaista|Jos asetat varaston arvon vähennyksen takautuvasti, olemassa olevia tapahtumia EI kohdisteta uudelleen oikean FIFO-kustannusvirran luomiseksi.|Jos asetat varaston arvon nousun tai vähennyksen takautuvasti, keskimääräinen kustannus lasketaan uudelleen ja kaikki liittyvät tapahtumat oikaistaan.<br /><br /> Jos vaihdat jaksoa tai laskentatyyppiä, kaikkia liittyviä tapahtumia on muutettava.|Voit päivittää ja vyöryttää vakiokustannukset säännöllisesti **Vakiotyökirja**-sivun avulla.<br /><br /> EI tueta varastoyksikkökohtaisesti.<br /><br /> Historiallisia tietueita ei ole olemassa standardikustannuksille.|Voit käyttää tietyn nimikkeen seurantaa ilman Spesifinen-arvostusmenetelmän käyttöä. Kustannukset eivät seuraa eränumeroa, vaan valitun arvostusmenetelmän kustannusten oletusta.|  

## <a name="example"></a>Esimerkki  
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
>  Tästä seuraava määrä varastossa on nolla. Näin ollen myös varastoarvon on oltava nolla arvostusmenetelmästä riippumatta.  

### <a name="effect-of-costing-methods-on-valuing-inventory-increases"></a>Arvostusmenetelmien vaikutus arvostetussa varastossa kasvaa  
 **FIFO**/**LIFO**/**Keskimääräinen**/**Spesifinen**  

 Niiden nimikkeiden kohdalla, jotka käyttävät todelliseen kustannukseen pohjautuvaa arvostusmenetelmää (**FIFO**, **LIFO**, **Keskimääräinen** tai **Spesifinen**), varaston arvon nousut arvostetaan nimikkeen hankintamenon mukaan.  

 Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan kaikissa kustannuslaskelmamenetelmissä, paitsi **Perus**-menetelmässä.  

|Kirjauspvm|määrä.|Kustannussumma (Tod.)|Tapahtumanro|  
|------------------|--------------|----------------------------|---------------|  
|01-01-20|1|10,00|1|  
|01-01-20|1|20,00|2|  
|01-01-20|1|30,00|3|  

 **Vakio**  

 **Vakio** arvostusmenetelmää käyttävien nimikkeiden kohdalla varastoarvon nousut arvostetaan nimikkeen nykyisellä vakiokustannuksella.  

 Seuraavassa taulukossa esitetään, kuinka varaston kasvua arvotetaan **Perus**-kustannuslaskelmamenetelmässä.  

|Kirjauspvm|määrä.|Kustannussumma (Tod.)|Tapahtumanro|  
|------------------|--------------|----------------------------|---------------|  
|01-01-20|1|15,00|1|  
|01-01-20|1|15,00|2|  
|01-01-20|1|15,00|3|  

### <a name="effect-of-costing-methods-on-valuing-inventory-decreases"></a>Arvostusmenetelmien vaikutus arvostetussa varastossa laskee  
 **FIFO**  

 **FIFO**-arvostusmenetelmää käyttävien nimikkeiden osalta ensimmäisinä ostetut nimikkeet myydään aina ensin (tapahtumanumerot 3, 2 ja 1 tässä esimerkissä). Vastaavasti, varaston arvon laskut arvostetaan ottamalla varaston ensimmäisen arvonnousun arvo.  

 Myytyjen tuotteiden kustannukset lasketaan käyttämällä ensimmäisen varastohankinnan arvoa.  

 Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan **FIFO**- kustannuslaskelmamenetelmässä.  

|Kirjauspvm|määrä.|Kustannussumma (Tod.)|Tapahtumanro|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-10.00|4|  
|03-01-20|-1|-20.00|5|  
|04-01-20|-1|-30.00|6|  

 **LIFO**  

 **LIFO**-arvostusmenetelmää käyttävien nimikkeiden osalta viimeksi ostetut nimikkeet myydään aina ensin (tapahtumanumerot 3, 2 ja 1 tässä esimerkissä). Vastaavasti, varaston arvon laskut arvostetaan ottamalla varaston viimeisen arvonnousun arvo.  

 Myytyjen tuotteiden kustannukset lasketaan käyttämällä viimeisimmän varastohankinnan arvoa.  

 Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan **LIFO**- kustannuslaskelmamenetelmässä.  

|Kirjauspvm|määrä.|Kustannussumma (Tod.)|Tapahtumanro|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-30.00|4|  
|03-01-20|-1|-20.00|5|  
|04-01-20|-1|-10.00|6|  

 **Keskiarvo**  

 Niiden nimikkeiden kohdalla, jotka käyttävät **Keskimääräinen** arvostusmenetelmää, varastoarvon vähennykset määritetään laskemalla painotettu keskiarvo jäljellä olevasta varastosta viimeisenä keskimääräisen kustannusjakson päivänä jona varastoarvon vähennys kirjattiin. Katso lisätietoja kohdasta [Rakennetiedot: Keskimääräinen kustannus](design-details-average-cost.md).  

 Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan **Keskimääräisessä** kustannuslaskelmamenetelmässä.  

|Kirjauspvm|määrä.|Kustannussumma (Tod.)|Tapahtumanro|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-20.00|4|  
|03-01-20|-1|-20.00|5|  
|04-01-20|-1|-20.00|6|  

 **Vakio**  

 **Vakio**-arvostusmenetelmää käyttävien nimikkeiden osalta varaston arvon vähennykset arvostetaan vastaavasti kuin **FIFO**- arvostusmenetelmässä, mutta arvostus perustuu vakiokustannukseen, eikä todelliseen kustannukseen.  

 Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan **Perus**-kustannuslaskelmamenetelmässä.  

|Kirjauspvm|määrä.|Kustannussumma (Tod.)|Tapahtumanro|  
|------------------|--------------|----------------------------|---------------|  
|02-01-20|-1|-15.00|4|  
|03-01-20|-1|-15.00|5|  
|04-01-20|-1|-15.00|6|  

 **Määrätty**  

 Arvostusmenetelmät luovat oletuksen siitä, kuinka kustannusvirtaukset varastosta nousevat varaston vähentyessä. Jos kustannusvirrasta on kuitenkin olemassa tarkempia tietoja, voit ohittaa tämän oletuksen luomalla tapahtumien välille kiinteän kohdistuksen. Kiinteä kohdistus luo linkin varaston arvon vähennyksen ja tietyn varaston lisäyksen välille ja ohjaa kustannusvirran vastaavasti.  

 **Spesifinen**-arvostusmenetelmää käyttävien nimikkeiden osalta varaston arvon vähennykset arvostetaan varaston arvon nousun mukaan, johon se on linkitetty kiinteällä kohdistuksella.  

 Seuraavassa taulukossa esitetään, kuinka varaston vähennyksiä arvotetaan **Erityisessä** kustannuslaskelmamenetelmässä.  

|Kirjauspvm|määrä.|Kustannussumma (Tod.)|Kohdistetaan tapahtumaan|Tapahtumanro|  
|------------------|--------------|----------------------------|-----------------------|---------------|  
|02-01-20|-1|-20.00|**2**|4|  
|03-01-20|-1|-10.00|**1**|5|  
|04-01-20|-1|-30.00|**3**|6|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
 [Rakennetiedot: varianssi](design-details-variance.md)   
 [Rakennetiedot: keskimääräinen kustannus](design-details-average-cost.md)   
 [Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  
 [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
 [Rahoitus](finance.md)  
 [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]