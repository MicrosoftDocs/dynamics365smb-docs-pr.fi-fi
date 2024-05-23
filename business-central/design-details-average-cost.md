---
title: Rakennetiedot - Keskimääräinen kustannus
description: Nimikkeen keskimääräinen kustannus lasketaan jaksoittaisen painotetun keskiarvon avulla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '8645,'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="design-details-average-cost"></a>Rakennetiedot: Keskimääräinen kustannus

Nimikkeen keskimääräinen kustannus lasketaan jaksoittaisen painotetun keskiarvon avulla. Keskiarvo perustuu [!INCLUDE[prod_short](includes/prod_short.md)]-ohjelmassa määrittämääsi keskimääräisen kustannuksen jaksoon.  

Arvostuspäivämäärä määritetään automaattisesti.  

## <a name="setting-up-average-cost-calculation"></a>Määritetään keskimääräiskustannuslaskelma

Seuraavassa taulukossa kuvataan kaksi kenttää **Varastonhallinnan asetukset** -sivulla, jotka täytyy täyttää, jotta keskimääräiskustannuslaskelma on mahdollinen.  

|Kenttä|Kuvaus|  
|---------------------------------|---------------------------------------|  
|**Keskimääräisen kustannuksen jakso**|Määrittää miltä aikakaudelta keskimääräiskustannukset lasketaan. Käytettävissä ovat seuraavat vaihtoehdot:<br /><br /> - **Päivä**<br />- **Viikko**<br />- **Kuukausi**<br />- **Kirjanpitojakso**<br /><br /> Varaston vähennykset, jotka kirjataan keskihintajaksolla, saavat kyseiselle jaksolle lasketun keskihinnan.|  
|**Keskim. kust. laskentatyyppi**|Määrittää, kuinka keskimääräinen kustannus lasketaan. Käytettävissä ovat seuraavat vaihtoehdot:<br /><br /> - **Vaihtoehto**<br />- **Nimike, variantti ja sijainti**<br /> Kun tämä vaihtoehto on valittuna, keskimääräinen kustannus lasketaan jokaiselle nimikkeelle, sijainnille ja nimikkeen variantille. Nimikkeen keskimääräinen kustannus riippuu siitä, missä se on varastoitu ja minkä variantin, kuten esimerkiksi värin, valitset.|  

> [!NOTE]  
> Voit käyttää tilikaudella vain yhtä keskimääräistä kustannuksen jaksoa ja yhtä keskimääräisten kustannusten laskentatyyppiä.  
>
> **Kirjanpitojaksot**-sivulla näkyy mikä keskimääräiskustannuskausi ja mikä keskimääräiskustannuslaskutyyppi on voimassa kullakin kaudella, liittyen kuhunkin kirjanpitokauteen.  

## <a name="calculating-average-cost"></a>Keskimääräisen kustannuksen laskeminen

 Kun kirjaat tapahtuman nimikkeelle, joka käyttää keskimääräistä kustannusmenetelmää, ohjelma luo merkinnän **Keskim. kust. muutoksen tulopaikka** -taulukossa. Tämä sisältää tapahtuman nimikenumeron, varianttikoodin ja sijaintikoodin. Tapahtuma sisältää myös **Arvostuspvm** -kentän, joka määrittää keskimääräisen kustannuksen jakson viimeisen päivämäärän, jona tapahtuma kirjattiin.  

> [!NOTE]  
> Tätä kenttää ei tule sekoittaa **Arvotapahtuma**-taulukon **Arvostuspvm**-kenttään, jossa näkyy päivämäärä arvon tullessa voimaan. Sitä käytetään arvotapahtuman keskimääräisten kustannuksen jakson määrittämisessä.  

 Siirron keskimääräiskustannukset on laskettu, kun nimikkeen kustannus on määritetty. Katso lisätietoja kohdasta [Rakennetiedot: kustannuksen muutos](design-details-cost-adjustment.md). Kustannuksen muutos käyttää **Keskim. kust. muutoksen tulopaikka** -taulukon tapahtumia tunnistamaan, mille nimikkeille (tai nimikkeille, sijainneille ja varianteille) keskimääräiset kustannukset lasketaan. Kustannusten muuttaminen käyttää seuraavia asioita määrittämään keskimääräisen kustannuksen jokaisen sellaisen tapahtuman kohdalla, jonka kustannusta ei ole muutettu:  

- Määrittää nimikkeen kustannuksen keskimääräisen kustannuksen jakson alussa.  
- Lisää keskimääräisen kustannuksen jakson aikana kirjattujen saapuvien kustannusten summan. Näitä ovat ostot, myyntipalautukset, positiiviset muutokset, ja tuotannon ja kokoonpanon tuotokset.  
- Vähentää keskimääräisen kustannuksen jakson aikana kiinteästi kohdistettujen minkä tahansa lähtevien transaktioiden kustannusten summan. Näitä ovat tavallisesti ostopalautukset ja negatiiviset tuotokset.  
- Jakaa varaston kokonaismäärällä, joka on olemassa keskimääräisen kustannuksen jakson lopussa. Jättää arvon määrityksen kohteena olevat varaston arvon laskut pois.  

 Laskettu keskimääräinen kustannus kohdistetaan tämän jälkeen varaston vähennyksiin nimikkeelle (tai nimikkeelle, sijainnille ja variantille) joiden kirjauspäivämäärät ovat keskimääräisellä kustannusjaksolla. Jos varastojen lisäyksiä sovelletaan kiinteästi varastojen vähennyksiin keskikustannusjakson aikana, [!INCLUDE [prod_short](includes/prod_short.md)] siirtää laskettuja keskikustannuksia lisäyksestä vähennykseen.  

### <a name="example-average-cost-period--day"></a>Esimerkki: keskimääräisen kustannusjakso = päivä

Seuraavassa esimerkissä kuvataan yhden päivän keskimääräiskustannusjaksoon perustuvan keskimääräiskustannusten laskennan vaikutus. **Varastonhallinnan asetukset** -sivun **Keskim. kust. laskentatyyppi** -kentän arvoksi on asetettu **Nimike**.  

Seuraavassa taulukossa esitetään nimikkeen pääkirjan kirjaukset esimerkkinä olevalle keskimääräiskustannusnimikkeelle, NIMIKE1, ennen kuin suoritat **Muuta kustannuksia - Nimiketapahtumat** -eräajon.  

| **Kirjauspvm** | **Nimiketapahtuman tyyppi** | **Määrä** | **Kustannussumma (todellinen)** | **Tapahtumanro** |
|--|--|--|--|--|
| 01-01-23 |   Ostot | 1 | 20.00 | 1 |
| 01-01-23 |   Ostot | 1 | 40.00 | 2 |
| 01-01-23 |   Myynti | -1 | -20.00 | 3 |
| 02-01-23 |   Myynti | -1 | -40.00 | 4 |
| 02-02-23 |   Ostot | 1 | 100.00 | 5 |
| 02-03-23 |   Myynti | -1 | -100.00 | 6 |

> [!NOTE]  
> Koska kustannuksia ei ole vielä muutettu, varaston **Kustannussumma (todellinen)** -kentän arvot vähenevät vastaten varaston kasvua, johon ne on kohdistettu.  

 Seuraavassa taulukossa esitetään kirjaukset **Keskim. kust. muutoksen tulopaikka** -taulukossa, jotka koskevat arvokirjauksia, jotka johtuvat nimikkeen pääkirjan kirjauksista edellisessä taulukossa.  

| **Nimikkeen nro** | **Varianttikoodi** | **Sijaintikoodi** | **Arvostuspvm** | **Kustannusta on muutettu** |
|--|--|--|--|--|
| NIMIKE1 |  | SININEN | 01-01-23 |   Ei |
| NIMIKE1 |  | SININEN | 02-01-23 |   Ei |
| NIMIKE1 |  | SININEN | 02-02-23 |   Ei |
| NIMIKE1 |  | SININEN | 02-03-23 |   Ei |

 Seuraavassa taulukossa esitetään nimikkeen pääkirjan kirjaukset, kun suoritat **Muuta kustannuksia - Nimiketapahtumat** -eräajon. Päiväkohtainen, keskimääräinen kustannus lasketaan ja kohdistetaan varastoarvon laskuihin.  

| **Kirjauspvm** | **Nimiketapahtuman tyyppi** | **Määrä** | **Kustannussumma (todellinen)** | **Tapahtumanro** |
|--|--|--|--|--|--|
| 01-01-23 |   Ostot | 1 | 20.00 | 1 |
| 01-01-23 |   Ostot | 1 | 40.00 | 2 |
| 01-01-23 |   Myynti | -1 | -30.00 | 3 |
| 02-01-23 |   Myynti | -1 | -30.00 | 4 |
| 02-02-23 |   Ostot | 1 | 100.00 | 5 |
| 02-03-23 |   Myynti | -1 | -100.00 | 6 |

### <a name="example-average-cost-period--month"></a>Esimerkki: keskimääräinen kustannusjakso = kuukausi

 Tässä esimerkissä kuvataan kuukauden keskimääräiskustannusjaksoon perustuvan keskimääräiskustannusten laskennan vaikutus. **Varastonhallinnan asetukset** -sivun **Keskim. kust. laskentatyyppi** -kentän arvoksi on asetettu **Nimike**.  

 Jos keskimääräinen kustannusjakso on yksi kuukausi, [!INCLUDE [prod_short](includes/prod_short.md)] luo yhden tapahtuman jokaiselle nimikenumeron, varianttikoodin, sijaintikoodin ja arvostuspäivämäärän yhdistelmälle.  

 Seuraavassa taulukossa esitetään nimikkeen pääkirjan kirjaukset esimerkkinä olevalle keskimääräiskustannusnimikkeelle, NIMIKE1, ennen kuin suoritat **Muuta kustannuksia - Nimiketapahtumat** -eräajon.  

| **Kirjauspvm** | **Nimiketapahtuman tyyppi** | **Määrä** | **Kustannussumma (todellinen)** | **Tapahtumanro** |
|--|--|--|--|--|
| 01-01-23 |   Ostot | 1 | 20.00 | 1 |
| 01-01-23 |   Ostot | 1 | 40.00 | 2 |
| 01-01-23 |   Myynti | -1 | -20.00 | 3 |
| 02-01-23 |   Myynti | -1 | -40.00 | 4 |
| 02-02-23 |   Ostot | 1 | 100.00 | 5 |
| 02-03-23 |   Myynti | -1 | -100.00 | 6 |

> [!NOTE]  
> Koska kustannuksia ei ole vielä muutettu, varaston **Kustannussumma (todellinen)** -kentän arvot vähenevät vastaten varaston kasvua, johon ne on kohdistettu.  

Seuraavassa taulukossa esitetään kirjaukset **Keskim. kust. muutoksen tulopaikka** -taulukossa, jotka koskevat arvokirjauksia, jotka johtuvat nimikkeen pääkirjan kirjauksista edellisessä taulukossa.  

| **Nimikkeen nro** | **Varianttikoodi** | **Sijaintikoodi** | **Arvostuspvm** | **Kustannusta on muutettu** |
|--|--|--|--|--|
| NIMIKE1 |  | SININEN | 01-31-23 |   Ei |
| NIMIKE1 |  | SININEN | 02-28-23 |   Ei |

> [!NOTE]  
> Arvostuspäivämääräksi määritetään keskimääräisten kustannusten jakson viimeinen päivä, joka on tässä tapauksessa kuukauden viimeinen päivä.  

Seuraavassa taulukossa esitetään nimikkeen pääkirjan kirjaukset, kun suoritat **Muuta kustannuksia - Nimiketapahtumat** -eräajon. Kuukausikohtainen, keskimääräinen kustannus lasketaan ja kohdistetaan varastoarvon laskuihin.  

|**Kirjauspvm** | **Nimiketapahtuman tyyppi** | **Määrä** | **Kustannussumma (todellinen)** | **Tapahtumanro** |
|--|--|--|--|--|
| 01-01-23 | Ostot | 1 | 20.00 | 1 |
| 01-01-23 | Ostot | 1 | 40.00 | 2 |
| 01-01-23 | Myynti | -1 | -30.00 | 3 |
| 02-01-23 | Myynti | -1 | -65.00 | 4 |
| 02-02-23 | Ostot | 1 | 100.00 | 5 |
| 02-03-23 | Myynti | -1 | -65.00 | 6 |

Tapahtumanumeron 3 keskimääräinen kustannus lasketaan tammikuun keskimääräisen kustannusjakson mukaan. Tapahtumanumeroiden 4 ja 6 keskimääräinen kustannus lasketaan helmikuun keskimääräisen kustannusjakson mukaan.  

Helmikuun keskimääräisten kustannusten saamiseksi [!INCLUDE [prod_short](includes/prod_short.md)] lisää varastoon saadun tuotteen keskimääräiset kustannukset (100,00) jakson alun keskimääräisiin kustannuksiin (30,00). Summa (130,00) jaetaan sitten varaston kokonaismäärällä (2). Tämä laskelma antaa nimikkeen keskimääräisen kustannuksen helmikuun aikana (65,00). Keskimääräinen kustannus määritetään varaston vähennyksille tilikaudella (tapahtumat 4 ja 6).  

## <a name="setting-the-valuation-date"></a>Arvostuspäivämäärän asetus

 **Arvostuspvm**-kenttä **Arvotapahtuma**-taulukko määrittelee mihin keskimääräiskustannuskauteen varastonvähennyskirjaus kuuluu. Tämä asetus koskee myös KET-varastoa.  

 Seuraavassa taulukossa esitetään kriteeri, jota käytetään arviointipäivämäärän määritykseen.  

| Esimerkkitilanne | Kirjauspäivämäärä | Arvostettu määrä | Uudelleenarvostus | Arvostuspvm |
|--|--|--|--|--|
| 1 |  | Positiivinen | Ei | Nimiketapahtuman päivämäärään kirjaaminen |
| 2 | Myöhempi kuin viimeisin käytettyjen arvotapahtumien arvostuspäivämäärä | Negatiivinen | Ei | Nimiketapahtuman päivämäärään kirjaaminen |
| 3 | Aiempi kuin viimeisin käytettyjen arvotapahtumien arvostuspäivämäärä | Positiivinen | Ei | Viimeisin käytettyjen arvotapahtumien arvostuspäivämäärä |
| 4 |  | Negatiivinen | Kyllä | Uudelleenarvostuksen arvotapahtuman päivämäärän kirjaaminen |

### <a name="example"></a>Esimerkki

Seuraavassa arvokirjaustaulukossa kuvataan eri skenaariot.  

| Esimerkkitilanne | Kirjauspäivämäärä | Nimiketapahtuman tyyppi | Arvostuspvm | Arvostettu määrä | Kustannussumma (todellinen) | Nimiketapahtuman nro | Tapahtumanro |
|--|--|--|--|--|--|--|--|
| 1 | 01-01-20 | Osto | 01-01-20 | 2 | 20.00 | 1 | 1 |
| 2 | 01-15-20 | (Nimikekulu) | 01-01-20 | 2 | 8,00 | 1 | 2 |
| 3 | 02-01-20 | Myynti | 02-01-20 | -1 | -14.00 | 2 | 3 |
| 4 | 03-01-20 | (Uudelleenarvostus) | 03-01-20 | 1 | -.4.00 | 1 | 4 |
| 5 | 02-01-20 | Myynti | 03-01-20 | -1 | -10.00 | 3 | 5 |

> [!NOTE]  
> Edellisen taulukon tapahtumassa 5 käyttäjä on kirjoittanut myyntitilauksen kirjauspäivämäärällä (1.2.2000), joka tapahtuu ennen viimeisintä kohdistettujen arvotapahtumien (1.3.2000) arvostuspäivämäärää. Jos kyseistä päivää (1.2.2020) vastaavaa **Kustannussumma (todellinen)** -kentän arvoa on käytetty tässä tapahtumassa, arvo on 14,00. Tällöin saadaan aikaan tilanne, jossa varaston määrä on nolla, mutta varaston arvo on -4,00.  
>
> Tämä määrän ja arvon ristiriita vältetään, kun arvostuspäivämääräksi määritetään sama kuin kohdistettujen arvotapahtumien edellinen arvostuspäivämäärä (1.3.2020). **Kustannussumma (todellinen)** -kentän arvoksi tulee 10,00 (uudelleenarvostuksen jälkeen). Tämä tarkoittaa sitä, että varaston määrä on nolla ja myös varaston arvo on nolla.  

> [!CAUTION]  
> Koska **Varaston arvostus**-raportti perustuu kirjauspäivämäärään, raportti kuvaa mitä tahansa määrän ja arvon ristiriidan vastaavissa skenaarioissa kuin yläpuolella olevassa esimerkissä. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Varaston arvostus](design-details-inventory-valuation.md).  

Jos varastomäärä on pienempi kuin nolla varaston arvon vähennyksen kirjauksen jälkeen, arvostuspäivämäärä asetetaan ensin varaston arvon vähennyksen kirjauspäivämääräksi. Voit muuttaa tätä päivämäärää, jolloin varastokorotusta sovelletaan, tämän jakson aiemmassa huomautuksessa kuvattujen sääntöjen mukaisesti.  

## <a name="recalculating-average-cost"></a>Keskimääräisen kustannuksen uudelleenlaskeminen

Varaston arvon laskujen arvostus painotetun keskiarvon perusteella olisi yksinkertaista useissa tilanteissa:

- Ostot laskutetaan aina ennen myyntiä.
- Kirjauksia ei merkitä koskaan takautuviksi.
- Et koskaan tehnyt virheitä.

Todellisuus on kuitenkin toisenlainen.  

Kuten tässä artikkelissa kuvataan, arvostuspäivämäärä märitetään päivämääränä, josta arvotapahtuma sisällytetään keskimääräisen kustannuksen laskentaan. Tämän asetuksen avulla voit tehdä useita asioita nimikkeille, joiden keskimääräinen arvostusmenetelmä on:  

- Laskuta nimikkeen myynti ennen kuin laskutat sen oston.  
- Päivitä kirjaus vanhemmaksi.  
- Virheellisen kirjauksen palautus.  

> [!NOTE]  
> Toinen syy tähän joustavuuteen on kiinteä kohdistus. Lisätietoja kiinteästä kohdistuksesta on kohdassa [Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md).  

Tästä joustavuudesta johtuen sinun on ehkä laskettava keskimääräinen kustannus kirjauksen jälkeen. Jos esimerkiksi kirjaat varaston arvon kasvun tai vähenemisen arvostuspäivämääränä, se on ennen varaston arvon laskua. Keskimääräiskustannusten uudelleenlaskenta tapahtuu automaattisesti, kun ajat **Muuta kustannuksia - Nimiketapahtumat** -eräajon manuaalisesti tai automaattisesti.  

Voit muuttaa varaston arvostuspohja tilikaudella vaihtamalla **Keskimääräisen kustannuksen jakso**- ja **Keskim. kust. laskentatyyppi** -kenttien arvoja. Suosittelemme, että olet kuitenkin varovainen ja konsultoit tilintarkastajia.  

### <a name="example-of-recalculated-average-cost"></a>Esimerkki uudelleen laskettavista keskimääräisistä kustannuksista

Tässä esimerkissä näytetään, miten [!INCLUDE [prod_short](includes/prod_short.md)] laskee keskimääräisen kustannuksen uudelleen, kun kirjaat päivämääränä, joka on ennen varaston vähennystä. Esimerkki perustuu keskimääräiskustannuskauteen **Päivää**.  

Seuraavassa taulukossa esitetään arvokirjaukset, jotka ovat olemassa nimikkeellä, ennen kuin tiliöinti on esitetty.  

| Arvostuspvm | Määrä | Kustannussumma (todellinen) | Tapahtumanro |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 02-15-20 | -1 | -15.00 | 3 |
| 02-16-20 | -1 | -15.00 | 4 |

Käyttäjä kirjaa varastoarvon nousun (tapahtuma numero 5), jonka arvostuspvm (3.1.2020) on ennen varastoarvon laskua. Kun varasto täsmäytetään, keskimääräiset kustannukset on laskettava uudelleen ja arvoksi on muutettava 17,00.  

Seuraavassa taulukossa esitetään arvokirjaukset, jotka ovat olemassa nimikkeellä, kun kirjausnumero 5 on esitetty.  

| Arvostuspvm | Määrä | Kustannussumma (todellinen) | Tapahtumanro |
|--|--|--|--|
| 01-01-20 | 1 | 10.00 | 1 |
| 01-02-20 | 1 | 20.00 | 2 |
| 01-03-20 | 1 | 21.00 | 5 |
| 02-15-20 | -1 | -17.00 | 3 |
| 02-16-20 | -1 | -17.00 | 4 |

## <a name="see-also"></a>Katso myös

[Rakennetiedot: Varaston kustannuslaskenta](design-details-inventory-costing.md)  
[Rakennetiedot: Kustannuslaskennan menetelmät](design-details-costing-methods.md)  
[Rakennetiedot: Kustannusten muutos](design-details-cost-adjustment.md)  
[Rakennetiedot: Nimikkeen kohdistus](design-details-item-application.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Termisanasto Dynamics 365:n liiketoimintaprosesseissa](/dynamics365/guidance/business-processes/glossary)  
[Tuotekustannusten liiketoimintaprosessi ja se, miten se liittyy muihin Dynamics 365:n prosesseihin](/dynamics365/guidance/business-processes/design-to-retire-define-product-costing-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
