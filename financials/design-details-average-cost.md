---
title: "Rakennetiedot – Keskimääräinen kustannus | Microsoft Docs"
description: "Nimikkeen keskimääräiskustannukset on laskettu kausittain painotetulla keskiarvolla Dynamics 365:ssä määritetyn keskimääräiskustannusten kauden perusteella."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4ced0ece340de08598fecff157d59aa708e4e17c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-average-cost"></a>Rakennetiedot: keskimääräinen kustannus
Nimikkeen keskimääräiskustannukset on laskettu kausittain painotetulla keskiarvolla perustuen keskimääräiskustannusten kauteen, joka on määritetty [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa.  

 Arvostuspäivämäärä määritetään automaattisesti.  

## <a name="setting-up-average-cost-calculation"></a>Määritetään keskimääräiskustannuslaskelma  
 Seuraavassa taulukossa kuvataan kaksi kenttää **Varastonhallinnan asetukset** -ikkunassa, jotka täytyy täyttää, jotta keskimääräiskustannuslaskelma on mahdollinen.  

|Kenttä|Description|  
|---------------------------------|---------------------------------------|  
|**Keskimääräisen kustannuksen jakso**|Määrittää miltä aikakaudelta keskimääräiskustannukset lasketaan. Käytettävissä ovat seuraavat vaihtoehdot:<br /><br /> -   **Päivä**<br />-   **Viikko**<br />-   **Kuukausi**<br />-   **Kirjanpitojakso**<br /><br /> Kaikki keskimääräisellä kustannuksen jaksolla kirjatut varaston arvon laskut saavat tälle jaksolle lasketun keskimääräisen kustannuksen.|  
|**Keskim. kust. laskentatyyppi**|Määrittää, kuinka keskimääräinen kustannus lasketaan. Käytettävissä ovat seuraavat vaihtoehdot:<br /><br /> -   **Vaihtoehto**<br />-   **Nimike, variantti ja sijainti**<br />     Kun tämä vaihtoehto on valittuna, keskimääräinen kustannus lasketaan jokaiselle nimikkeelle, sijainnille ja nimikkeen variantille. Tämä tarkoittaa sitä, että nimikkeen keskimääräinen kustannus riippuu siitä, missä se on varastoitu ja minkä nimikkeen variantin, kuten esimerkiksi värin, olet valinnut.|  

> [!NOTE]  
>  Voit käyttää tilikaudella vain yhtä keskimääräistä kustannuksen jaksoa ja yhtä keskimääräisten kustannusten laskentatyyppiä.  
>   
>  **Kirjanpitojaksot**-ikkunassa näkyy mikä keskimääräiskustannuskausi ja mikä keskimääräiskustannuslaskutyyppi on voimassa kullakin kaudella, liittyen kuhunkin kirjanpitokauteen.  

## <a name="calculating-average-cost"></a>Keskimääräisen kustannuksen laskeminen  
 Kun kirjaat tapahtuman nimikkeelle, joka käyttää keskimääräistä kustannusmenetelmää, ohjelma luo merkinnän **Keskim. kust. muutoksen tulopaikka** -taulukossa. Tämä sisältää tapahtuman nimikenumeron, varianttikoodin ja sijaintikoodin. Tapahtuma sisältää myös **Arvostuspvm** -kentän, joka määrittää keskimääräisen kustannuksen jakson viimeisen päivämäärän, jona tapahtuma kirjattiin.  

> [!NOTE]  
>  Tätä kenttää ei tule sekoittaa **Arvotapahtuma**-taulukon **Arvostuspvm**-kenttään, jossa näkyy päivämäärä arvon tullessa voimaan. Sitä käytetään arvotapahtuman keskimääräisten kustannuksen jakson määrittämisessä.  

 Siirron keskimääräiskustannukset on laskettu, kun nimikkeen kustannus on määritetty. Katso lisätietoja kohdasta [Rakennetiedot: kustannuksen muutos](design-details-cost-adjustment.md). Kustannuksen muutos käyttää **Keskim. kust. muutoksen tulopaikka** -taulukon tapahtumia tunnistamaan, mille nimikkeille (tai nimikkeille, sijainneille ja varianteille) keskimääräiset kustannukset lasketaan. Kustannusten muuttaminen käyttää seuraavia asioita määrittämään keskimääräisen kustannuksen jokaisen sellaisen tapahtuman kohdalla, jonka kustannusta ei ole muutettu:  

-   Määrittää nimikkeen kustannuksen keskimääräisen kustannuksen jakson alussa.  
-   Lisää keskimääräisen kustannuksen jakson aikana kirjattujen saapuvien kustannusten summan. Näitä ovat ostot, myyntipalautukset, positiiviset muutokset, ja tuotannon ja kokoonpanon tuotokset.  
-   Vähentää keskimääräisen kustannuksen jakson aikana kiinteästi kohdistettujen minkä tahansa lähtevien transaktioiden kustannusten summan. Näitä ovat tavallisesti ostopalautukset ja negatiiviset tuotokset.  
-   Jakaa varaston kokonaismäärällä keskimääräisen kustannusjakson loppuun, lukuun ottamatta arvostettavia varaston vähennyksiä.  

 Laskettu keskimääräinen kustannus kohdistetaan tämän jälkeen varaston vähennyksiin nimikkeelle (tai nimikkeelle, sijainnille ja variantille) joiden kirjauspäivämäärät ovat keskimääräisellä kustannusjaksolla. Jos on olemassa varaston arvon nousuja, jotka kohdistettiin kiinteästi varaston arvon laskuihin keskimääräisellä kustannusjaksolla, tällöin laskettu keskimääräinen kustannus siirretään kasvusta vähennykseen.  

### <a name="example-average-cost-period--day"></a>Esimerkki: keskimääräisen kustannusjakso = päivä  
 Seuraavassa esimerkissä kuvataan yhden päivän keskimääräiskustannusjaksoon perustuvan keskimääräiskustannusten laskennan vaikutus. **Varastonhallinnan asetukset** -ikkunan **Keskim. kust. laskentatyyppi** -kentän arvoksi on asetettu **Nimike**.  

 Seuraavassa taulukossa esitetään nimikkeen pääkirjan kirjaukset esimerkkinä olevalle keskimääräiskustannusnimikkeelle, NIMIKE1, ennen kuin **Muuta kustannuksia - Nimiketapahtumat** -eräajo on ajettu.  

|**Kirjauspvm**|**Nimiketapahtuman tyyppi**|**Määrä**|**Kustannussumma (todellinen)**|**Tapahtumanro**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Osto|1|20.00|1|  
|01-01-20|Osto|1|40.00|2|  
|01-01-20|Myynti|-1|-20.00|3|  
|02-01-20|Myynti|-1|-40.00|4|  
|02-02-20|Osto|1|100,00|5|  
|02-03-20|Myynti|-1|-100.00|6|  

> [!NOTE]  
>  Koska kustannuksia ei ole vielä muutettu, varaston **Kustannussumma (todellinen)** -kentän arvot vähenevät vastaten varaston kasvua, johon ne on kohdistettu.  

 Seuraavassa taulukossa esitetään kirjaukset **Keskim. kust. muutoksen tulopaikka** -taulukossa, jotka koskevat arvokirjauksia, jotka johtuvat nimikkeen pääkirjan kirjauksista edellisessä taulukossa.  

|**Nimikkeen nro**|**Varianttikoodi**|**Sijaintikoodi**|**Arvostuspvm**|**Kustannusta on muutettu**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|NIMIKE1||SININEN|01-01-20|Ei|  
|NIMIKE1||SININEN|02-01-20|Ei|  
|NIMIKE1||SININEN|02-02-20|Ei|  
|NIMIKE1||SININEN|02-03-20|Ei|  

 Seuraavassa taulukossa esitetään nimikkeen pääkirjan kirjaukset, kun **Muuta kustannuksia - Nimiketapahtumat** -eräajo on ajettu. Päiväkohtainen, keskimääräinen kustannus lasketaan ja kohdistetaan varastoarvon laskuihin.  

|**Kirjauspvm**|**Nimiketapahtuman tyyppi**|**Määrä**|**Kustannussumma (todellinen)**|**Tapahtumanro**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Osto|1|20.00|1|  
|01-01-20|Osto|1|40.00|2|  
|01-01-20|Myynti|-1|-30.00|3|  
|02-01-20|Myynti|-1|-30.00|4|  
|02-02-20|Osto|1|100,00|5|  
|02-03-20|Myynti|-1|-100.00|6|  

### <a name="example-average-cost-period--month"></a>Esimerkki: keskimääräinen kustannusjakso = kuukausi  
 Seuraavassa esimerkissä kuvataan kuukauden keskimääräiskustannusjaksoon perustuvan keskimääräiskustannusten laskennan vaikutus. **Varastonhallinnan asetukset** -ikkunan **Keskim. kust. laskentatyyppi** -kentän arvoksi on asetettu **Nimike**.  

 Jos keskimääräinen kustannusjakso on yksi kuukausi, tällöin jokaiselle nimikenumeron, varianttikoodin, sijaintikoodin ja arvostuspäivämäärän yhdistelmälle luodaan vain yksi tapahtuma.  

 Seuraavassa taulukossa esitetään nimikkeen pääkirjan kirjaukset esimerkkinä olevalle keskimääräiskustannusnimikkeelle, NIMIKE1, ennen kuin **Muuta kustannuksia - Nimiketapahtumat** -eräajo on ajettu.  

|**Kirjauspvm**|**Nimiketapahtuman tyyppi**|**Määrä**|**Kustannussumma (todellinen)**|**Tapahtumanro**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Osto|1|20.00|1|  
|01-01-20|Osto|1|40.00|2|  
|01-01-20|Myynti|-1|-20.00|3|  
|02-01-20|Myynti|-1|-40.00|4|  
|02-02-20|Osto|1|100,00|5|  
|02-03-20|Myynti|-1|-100.00|6|  

> [!NOTE]  
>  Koska kustannuksia ei ole vielä muutettu, varaston **Kustannussumma (todellinen)** -kentän arvot vähenevät vastaten varaston kasvua, johon ne on kohdistettu.  

 Seuraavassa taulukossa esitetään kirjaukset **Keskim. kust. muutoksen tulopaikka** -taulukossa, jotka koskevat arvokirjauksia, jotka johtuvat nimikkeen pääkirjan kirjauksista edellisessä taulukossa.  

|**Nimikkeen nro**|**Varianttikoodi**|**Sijaintikoodi**|**Arvostuspvm**|**Kustannusta on muutettu**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|NIMIKE1||SININEN|01-31-20|Ei|  
|NIMIKE1||SININEN|02-28-20|Ei|  

> [!NOTE]  
>  Arvostuspäivämääräksi määritetään keskimääräisten kustannusten jakson viimeinen päivä, joka on tässä tapauksessa kuukauden viimeinen päivä.  

 Seuraavassa taulukossa esitetään nimikkeen pääkirjan kirjaukset, kun **Muuta kustannuksia - Nimiketapahtumat** -eräajo on ajettu. Kuukausikohtainen, keskimääräinen kustannus lasketaan ja kohdistetaan varastoarvon laskuihin.  

|**Kirjauspvm**|**Nimiketapahtuman tyyppi**|**Määrä**|**Kustannussumma (todellinen)**|**Tapahtumanro**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Osto|1|20.00|1|  
|01-01-20|Osto|1|40.00|2|  
|01-01-20|Myynti|-1|-30.00|3|  
|02-01-20|Myynti|-1|-65.00|4|  
|02-02-20|Osto|1|100,00|5|  
|02-03-20|Myynti|-1|-65.00|6|  

 Kirjausnumeron 3 keskimääräiskustannus on laskettu keskimääräiskustannuksen kaudelle tammikuussa ja kirjausten 4 ja 6 keskimääräiskustannus on laskettu keskimääräiskustannusten kaudelle helmikuussa.  

 Saat helmikuun keskimääräisen kustannuksen, kun kappaleen keskimääräinen kustannus varastossa (100,00) lisätään jakson alun keskimääräiseen kustannukseen (30,00). Näiden kahden summa (130,00) jaetaan varaston kokonaismäärällä (2). Tuloksena saadaan nimikkeen keskimääräinen kustannus helmikuussa (65,00). Keskimääräinen kustannus määritetään varaston vähennyksille tilikaudella (tapahtumat 4 ja 6).  

## <a name="setting-the-valuation-date"></a>Arvostuspäivämäärän asetus  
 **Arvostuspvm**-kenttää **Arvotapahtuma**-taulukossa käytetään määrittelemään mihin keskimääräiskustannuskauteen varastonvähennyskirjaus kuuluu. Tämä koskee myös KET-varastoa.  

 Seuraavassa taulukossa esitetään kriteeri, jota käytetään arviointipäivämäärän määritykseen.  

|Esimerkkitilanne|Kirjauspäivämäärä|Arvostettu määrä|Uudelleenarvostus|Arvostuspvm|  
|--------------|-------------------------------------|-----------------------------------------|-----------------|-----------------------------------------|  
|1||Positiivinen|Ei|Nimiketapahtuman päivämäärään kirjaaminen|  
|2|Myöhempi kuin viimeisin käytettyjen arvotapahtumien arvostuspäivämäärä|Negatiivinen|Ei|Nimiketapahtuman päivämäärään kirjaaminen|  
|3|Aiempi kuin viimeisin käytettyjen arvotapahtumien arvostuspäivämäärä|Positiivinen|Ei|Viimeisin käytettyjen arvotapahtumien arvostuspäivämäärä|  
|4||Negatiivinen|Kyllä|Uudelleenarvostuksen arvotapahtuman päivämäärän kirjaaminen|  

### <a name="example"></a>Esimerkki  
 Seuraavassa arvokirjaustaulukossa kuvataan eri skenaariot.  

|Esimerkkitilanne|Kirjauspäivämäärä|Nimiketapahtuman tyyppi|Arvostuspvm|Arvostettu määrä|Kustannussumma (todellinen)|Nimiketapahtuman nro|Tapahtumanro|  
|--------------|-------------------------------------|-----------------------------------------------|-----------------------------------------|-----------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|1|01-01-20|Osto|01-01-20|2|20.00|1|1|  
|2|01-15-20|(Nimikekulu)|01-01-20|2|8,00|1|2|  
|3|02-01-20|Myynti|02-01-20|-1|-14.00|2|3|  
|4|03-01-20|(Uudelleenarvostus)|03-01-20|1|-.4.00|1|4|  
|5|02-01-20|Myynti|03-01-20|-1|-10.00|3|5|  

> [!NOTE]  
>  Edellisen taulukon tapahtumassa 5 käyttäjä on kirjoittanut myyntitilauksen kirjauspäivämäärällä (1.2.2000), joka tapahtuu ennen viimeisintä kohdistettujen arvotapahtumien (1.3.2000) arvostuspäivämäärää. Jos kyseistä päivää (1.2.2020) vastaavaa **Kustannussumma (todellinen)** -kentän arvoa on käytetty tässä tapahtumassa, arvo on 14,00. Tällöin saadaan aikaan tilanne, jossa varaston määrä on nolla, mutta varaston arvo on -4,00.  
>   
>  Tämä määrän ja arvon ristiriita vältetään, kun arvostuspäivämääräksi määritetään sama kuin kohdistettujen arvotapahtumien edellinen arvostuspäivämäärä (1.3.2020). **Kustannussumma (todellinen)** -kentän arvoksi tulee 10,00 (uudelleenarvostuksen jälkeen). Tämä tarkoittaa sitä, että varaston määrä on nolla ja myös varaston arvo on nolla.  

> [!CAUTION]  
>  Koska **Varaston arvostus**-raportti perustuu kirjauspäivämäärään, raportti kuvaa mitä tahansa määrän ja arvon ristiriidan vastaavissa skenaarioissa kuin yläpuolella olevassa esimerkissä. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Varaston arvostus](design-details-inventory-valuation.md).  

 Jos varastomäärä on pienempi kuin nolla varaston arvon vähennyksen kirjauksen jälkeen, arvostuspäivämäärä asetetaan ensin varaston arvon vähennyksen kirjauspäivämääräksi. Tämä päivämäärä saattaa muuttua myöhemmin aiemmin tässä luvussa kuvatun säännön mukaan, kun varastoarvon nousu kohdistetaan.  

## <a name="recalculating-average-cost"></a>Keskimääräisen kustannuksen uudelleenlaskeminen  
 Varaston arvon vähenemisen arvostaminen painotettuna keskiarvona olisi yksinkertaista, jos ostot laskutettaisiin aina ennen myyntien laskutusta, kirjaukset eivät olisi koskaan myöhässä etkä milloinkaan tekisi virheitä. Todellisuus on kuitenkin hieman erilainen kuin tämä ihanteellinen tilanne.  

 Kuten tämän ohjeaiheen esimerkeissä on kuvattu, arvostuspäivämäärä märitetään päivämääränä, josta arvotapahtuma sisällytetään keskimääräisen kustannuksen laskentaan. Voit tehdä nimikkeille joustavammin seuraavat toimet keskimääräisen arvostusmenetelmän avulla:  

-   Lasku nimikkeen myynnistä ennen kuin nimikkeen ostoa on laskutettu.  
-   Päivitä kirjaus vanhemmaksi.  
-   Virheellisen kirjauksen palautus.  

> [!NOTE]  
>  Toinen syy tähän joustavuuteen on kiinteä kohdistus. Lisätietoja kiinteästä kohdistuksesta on kohdassa [Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md).  

 Tästä joustavuudesta johtuen sinun on ehkä laskettava keskimääräinen kustannus uudelleen liittyvän kirjauksen jälkeen. Jos esimerkiksi kirjaat varaston arvon kasvun tai vähenemisen arvostuspäivämääränä, joka on ennen yhtä tai useampaa varaston arvon laskua. Keskimääräiskustannusten uudelleenlaskenta tapahtuu automaattisesti, kun ajat **Muuta kustannuksia - Nimiketapahtumat** -eräajon manuaalisesti tai automaattisesti.  

 On mahdollista muuttaa varaston arvostuspohja tilikaudella vaihtamalla **Keskimääräisen kustannuksen jakso**- ja **Keskim. kust. laskentatyyppi**-kenttää. Tämä tulisi kuitenkin tehdä huolellisesti ja sopimalla tilintarkastajan kanssa.  

### <a name="example"></a>Esimerkki  
 Seuraava esimerkki kuvaa sitä, kuinka keskimääräiskustannus lasketaan uudelleen, kun myöhäinen tiliöinti esitellään päivämääränä, joka tulee ennen yhtä tai useampaa varaston vähennystä. Esimerkki perustuu keskimääräiskustannuskauteen **Päivää**.  

 Seuraavassa taulukossa esitetään arvokirjaukset, jotka ovat olemassa nimikkeellä, ennen kuin tiliöinti on esitetty.  

|Arvostuspvm|Määrä|Kustannussumma (todellinen)|Tapahtumanro|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|01-02-20|1|20.00|2|  
|02-15-20|-1|-15.00|3|  
|02-16-20|-1|-15.00|4|  

 Käyttäjä kirjaa varastoarvon nousun (tapahtuma numero 5), jonka arvostuspvm (3.1.2020) on ennen yhden tai usean varastoarvon laskua. Kun varasto täsmäytetään, keskimääräiset kustannukset on laskettava uudelleen ja arvoksi on muutettava 17,00.  

 Seuraavassa taulukossa esitetään arvokirjaukset, jotka ovat olemassa nimikkeellä, kun kirjausnumero 5 on esitetty.  

|Arvostuspvm|Määrä|Kustannussumma (todellinen)|Tapahtumanro|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|01-02-20|1|20.00|2|  
|01-03-20|1|21.00|5|  
|02-15-20|-1|-17.00|3|  
|02-16-20|-1|-17.00|4|  

## <a name="see-also"></a>Katso myös  
 [Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)   
 [Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md)   
 [Rakennetiedot: kustannuksen muutos](design-details-cost-adjustment.md)   
 [Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  
 [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
 [Rahoitus](finance.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

