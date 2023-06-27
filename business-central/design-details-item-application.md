---
title: Rakennetiedot – Nimikkeen kohdistus | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään varaston määrän ja arvon tallentamista varastotapahtuman kirjauksen yhteydessä.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, items, ledger entries, posting, inventory'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-application" />Rakennetiedot: Nimikkeen kohdistus

Kun kirjaat varastotapahtuman, määrän kirjaus tallennetaan nimiketapahtumiin ja arvon kirjaus arvotapahtumiin. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Varaston kirjaus](design-details-inventory-posting.md).  

Lisäksi suoritetaan nimikkeen kohdistus kustannuksen vastaanottajan linkittämiseksi sen kustannuksen lähteeseen kustannuksen siirron suorittamiseksi arvostusmenetelmän mukaisesti. Lisätietoja on kohdassa [Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md).  

[!INCLUDE[prod_short](includes/prod_short.md)] suorittaa kahdenlaisia nimikkeen kohdistuksia.  

|Sovelluksen tyyppi|Description|  
|----------------------|---------------------------------------|  
|Määrän kohdistus|Luotu kaikille varastotapahtumille|  
|Kustannusten kohdistus|Luotu saapuville tapahtumille yhdessä määräkohdistuksen kanssa käyttäjän toimien seurauksena erityisissä prosesseissa.|  

Nimikkeen kohdistukset voidaan tehdä seuraavilla tavoilla.  

|Tapa|Description|Sovelluksen tyyppi|  
|------------|---------------------------------------|----------------------|  
|Automaattinen|Tapahtuu yleisenä kustannuksen siirtona arvostusmenetelmän mukaan|Määrän kohdistus|  
|Kiinteä|Käyttäjän tekemät, kun:<br /><br /> -   Palautusten käsittely<br />-   Korjausten kirjaaminen<br />-   Määrän kirjausten peruuttaminen<br />-   Suoratoimitusten luonti **Huomautus:** Kiinteä kohdistus voidaan tehdä joko manuaalisesti antamalla kirjausnumero **Kohdistus nimiketapahtumasta** -kentässä tai käyttämällä toimintoa, kuten **Hae peruutettavat kirjatut asiakirjarivit**.|Määrän kohdistus<br /><br /> Kustannusten kohdistus **Huomautus**: Kustannusten kohdistus tapahtuu vain niissä saapuvissa tapahtumissa, joissa kiinteä kohdistus luodaan täyttämällä **Kohdistus nimiketapahtumasta** -kenttä. Katso seuraava taulukko.|  

Varastotapahtuman suunta määrittää, tehdäänkö määrän vai kustannusten muutokset ja tehdäänkö nimikkeen muutos automaattisesti vai kiinteästi yhdessä tiettyjen prosessien kanssa.  

Seuraavissa taulukoissa, perustuen keskeisiin sovelluskenttiin varastonsiirtoriveillä, esitetään kuinka kustannukset nousevat siirtosuunnan mukaan. Se ilmaisee myös milloin ja miksi nimikkeen kohdistuksen tyyppi on määrä tai kustannus.  

|-|Kohdista nimikkeen merkintäkenttään|Kohdistus nimikkeen merkintäkentästä|  
|-|--------------------------------|----------------------------------|  
|Lähtevän tapahtuman sovellus|Lähtevä kirjaus vetää kustannukset avoimesta tulevasta kirjauksesta.<br /><br /> **Määrän kohdistus**|Ei tueta|  
|Saapuvan tapahtuman sovellus|Tuleva kirjaus työntää kustannukset avoimeen lähtevään kirjaukseen.<br /><br /> Tuleva kirjaus ei ole kustannuslähde.<br /><br /> **Määrän kohdistus**|Tuleva kirjaus vetää kustannukset lähtevästä kirjauksesta. **Huomautus:** Saapuvaa tapahtumaa käsitellään myyntipalautuksena, kun teet tämän kiinteän kohdistuksen. Tämän vuoksi käytetty lähtevä tapahtuma jää avoimeksi. <br /><br /> Tuleva kirjaus EI OLE kustannuslähde.<br /><br /> **Kustannusten kohdistus**|  

> [!IMPORTANT]  
> Myynnin tuottoa EI pidetä kustannuksen lähteenä, kiinteä on kohdistettu.  
>
> Myyntikirjaus pysyy avoimena, kunnes todellinen lähde tiliöidään.  

Nimiketapahtuma tallentaa seuraavat tiedot.  

|Kenttä|Description|  
|---------------------------------|---------------------------------------|  
|**Nimiketapahtuman nro**|Sen tapahtuman nimiketapahtuman numero, jolle tämä kohdistustapahtuma on tehty.|  
|**Saapuvan nimiketapahtuman nro**|Sen varastoarvon nousun nimiketapahtuman numero, johon tapahtuma tulee linkittää, jos sovellettavissa.|  
|**Lähtevän nimiketapahtuman nro**|Sen varastoarvon laskun nimiketapahtuman numero, johon tapahtuma tulee linkittää, jos sovellettavissa.|  
|**Määrä**|Kohdistettu määrä.|  
|**Kirjauspvm**|Tapahtuman kirjauspäivämäärä.|  

## <a name="inventory-increase" />Varastoarvon nousu
Kun kirjaat varaston arvon nousun, tämän jälkeen tallennetaan yksinkertainen nimikkeen kohdistustapahtuma ilman kohdistusta lähtevään tapahtumaan.  

### <a name="example" />Esimerkki
Seuraavassa taulukossa esitetään nimikkeen käyttökirjaus, joka luodaan, kun tiliöit 10 yksikön ostokuitit.  

|Kirjauspäivämäärä|Saapuvan nimiketapahtuman nro|Lähtevän nimiketapahtuman nro|Määrä|Nimiketapahtuman nro|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  

## <a name="inventory-decrease" />Varastoarvon lasku
Kun kirjaat varaston arvon laskun, luotava nimikkeen kohdistustapahtuma linkittää varaston arvon laskun varaston arvon nousuun. Tämä linkki luodaan käyttämällä ohjeena nimikkeen arvostusmenetelmää. FIFO-, vakio- ja keskimääräinen-arvostusmenetelmää käyttävien nimikkeiden osalta linkitys perustuu ensimmäinen käsitellään ensin -periaatteeseen. Varaston vähennystä käytetään varaston kasvuun aikaisimman tiliöintipäivämäärän mukaisesti. LIFO-arvostusmenetelmää käyttävien nimikkeiden osalta linkitys perustuu viimeisin käsitellään ensin -periaatteeseen. Varaston vähennys kohdistetaan varaston arvon nousuun viimeisimmän tiliöintipäivämäärän mukaisesti.  

**Nimiketapahtuma**-taulukon **Jäljellä oleva määrä** -kenttä näyttää määrän, jota ei ole vielä kohdistettu. Jos jäljellä oleva määrä on suurempi kuin 0, **Avoin** -valintaruutu valitaan.  

### <a name="example-1" />Esimerkki
Seuraava esimerkki näyttää nimikkeen kohdistustapahtuman, joka luodaan edellisessä esimerkissä vastaanotettujen 5 nimikkeen myyntitoimituksen kirjauksesta. Ensimmäinen nimikkeen käyttökirjaus on ostokuitti. Toinen käyttökirjaus on myyntitoimitus.  

Seuraavissa taulukoissa esitetään kaksi nimikkeen sovelluskirjausta, jotka aiheutuvat varaston kasvusta ja varaston vähennyksistä, tässä järjestyksessä.  

|Kirjauspäivämäärä|Saapuvan nimiketapahtuman nro|Lähtevän nimiketapahtuman nro|Määrä|Nimiketapahtuman nro|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
|01-03-20|1|2|-5|2|  

## <a name="fixed-application" />Kiinteä kohdistus
Teet kiinteän kohdistuksen, kun kohdistat varaston arvon nousun kustannukset tiettyyn varaston arvon laskuun tai päinvastoin. Kiinteä kohdistus vaikuttaa jäljellä oleviin kirjausten määriin, mutta se myös kumoaa alkuperäisen kirjauksen tarkat kustannukset, jota käytät.  

Voit tehdä kiinteän kohdistuksen asiakirjarivien **Kohdista nimiketapahtumaan**- tai **Kohdistus nimiketapahtumasta** -kentän avulla, kun haluat määrittää nimiketapahtuman, johon haluat kohdistaa tapahtumarivin tai josta haluat sen kohdistettavan. Voit esimerkiksi tehdä kiinteän kohdistuksen, kun haluat luoda kustannuksen kohdistuksen, joka määrittää, että myynnin tuoton tulisi koskea tiettyä myyntitoimitusta myyntitilauksen kustannuksen peruuttamiseksi. Tässä tapauksessa [!INCLUDE[prod_short](includes/prod_short.md)] ohittaa arvostusmenetelmän ja käyttää myyntipalautukselle varaston arvon vähennystä tai kasvatusta määrittämääsi nimiketapahtumaan. Kiinteän sovelluksen teon hyöty on se, että alkuperäisen siirron kustannus siirretään uuteen tapahtumaan.  

### <a name="example--fixed-application-in-purchase-return" />Esimerkki – kiinteä kohdistus ostopalautuksessa
Seuraava esimerkki, jossa kuvataan sellaisen nimikkeen vaikutus ostopalautuksen kiinteään sovellukseen, joka käyttää FIFO-kustannuslaskentamenetelmää, perustuu seuraavaan skenaarioon:  

1. Tapahtumassa 1 käyttäjä kirjaa oston hintaan 10,00 (PVA).  
2. Tapahtumassa 2 käyttäjä kirjaa oston hintaan 20,00 (PVA).  
3. Tapahtumassa 3 käyttäjä kirjaa ostopalautuksen. Käyttäjä tekee toiselle ostolle kiinteän kohdistuksen antamalla nimiketapahtuman numeron ostopalautustilauksen rivin **Kohdista nimiketapahtumaan** -kenttään.  

Seuraavassa taulukossa käsitellään skenaariosta aiheutuvat nimiketapahtumat.  

|**Kirjauspvm**|**Nimiketapahtuman tyyppi**|**Määrä**|**Kustannussumma (todellinen)**|**Nimiketapahtuman nro**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|01-04-20|Osto|10|10.00|1|  
|01-05-20|Osto|10|20.00|2|  
|01-06-20|Osto (palautus)|-10|-20.00|3|  

Koska kiinteä kohdistus tehdään ostopalautuksesta toiselle ostotapahtumalle, nimikkeet palautetaan oikealla kustannuksella. Jos käyttäjä ei olisi suorittanut kiinteää kohdistusta, palautetun nimikkeen virheellinen arvo olisi ollut 10,00 PVA , koska tuottoa olisi sovellettu ensimmäiseen ostotapahtumaan FIFO-periaatteen mukaisesti.  

Seuraavassa taulukossa esitetään nimikkeen käyttökirjaus, joka johtuu kiinteästä sovelluksesta.  

|Kirjauspäivämäärä|Saapuvan nimiketapahtuman nro|Lähtevän nimiketapahtuman nro|Määrä|Nimiketapahtuman nro|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-06-20|2|3|10|3|  

Tämän jälkeen toisen oston kustannus 20,00 PVA siirtyy ostopalautukselle oikein.  

### <a name="example--fixed-application-with-average-cost" />Esimerkki – kiinteä kohdistus keskimääräisen kustannuksen kanssa
Seuraava esimerkki, jossa kuvataan kiinteän sovelluksen vaikutusta, perustuu seuraavaan skenaarioon nimikkeestä, joka käyttää keskimääräisen kustannuslaskelman menetelmää:  

1. Tapahtumissa numero 1 ja 2 käyttäjä kirjaa kaksi ostolaskua. Toisessa laskussa on väärä välitön kustannusyksikkö LCY 1000.00.  
2. Tapahtumassa numero 3 käyttäjä kirjaa ostohyvityslaskun, joka on kohdistettu kiinteästi ostotapahtumaan väärällä välittömällä yksikkökustannuksella. **Kustannussumma todellinen** -kentän kahden kiinteän käytetyn arvokirjauksen summaksi tulee 0,00  
3. Tapahtumassa numero 4 käyttäjä kirjaa toisen ostolaskun oikealla välittömällä yksikkökustannuksella 100,00 PVA  
4. Tapahtumassa 5 käyttäjä kirjaa myyntipalautuksen.  
5. Varastomäärä on 0 ja varaston arvo on myös 0.00.  

Seuraavassa taulukossa esitetään skenaarion tulos nimikkeen arvokirjauksissa.  

Seuraavassa taulukossa on esitetty skenaarion tulokset nimikkeen arvotapahtumista, sen jälkeen, kun kirjaus on valmis ja kustannusten muuttaminen on suoritettu.

|Kirjauspäivämäärä|Nimiketapahtuman tyyppi|Arvostettu määrä|Kustannussumma (Tod.)|Kohdista nimiketapahtumaan|Arvostettu keskim. kust.|Nimiketapahtuman nro|Tapahtumanro|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Osto|1|200.00||Ei|1|1|  
|01-01-20|Osto|1|1000.00||Ei|2|2|  
|01-01-20|Osto|-1|-1000|2|Ei|3|3|  
|01-01-20|Osto|1|100,00||Ei|4|4|  
|01-01-20|Myynti|-2|-300.00||Kyllä|5|5|  

Jos käyttäjä ei olisi tehnyt kiinteää kohdistusta ostohyvityslaskun ja ostojen välillä virheellisellä suoralla yksikkökustannuksella (vaihe 2 edellisessä skenaariossa), kustannus olisi muutettu eri tavalla.  

Seuraavassa taulukossa käsitellään nimikkeen arvotapahtumien tulos, jos vaihe 2 edellisessä skenaariossa suoritetaan ilman kiinteää kohdistusta.  

|Kirjauspäivämäärä|Nimiketapahtuman tyyppi|Arvostettu määrä|Kustannussumma (todellinen)|Kohdista nimiketapahtumaan|Arvostettu keskim. kust.|Nimiketapahtuman nro|Tapahtumanro|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Osto|1|200.00||Ei|1|1|  
|01-01-20|Osto|1|1000.00||Ei|2|2|  
|01-01-20|Osto|-1|433,33||Kyllä|3|3|  
|01-01-20|Osto|1|100,00||Ei|4|4|  
|01-01-20|Myynti|-2|866,67||Kyllä|5|5|  

Tapahtumassa numero 3, **Kustannussumma todellinen** -kentän arvo arvostetaan keskiarvon mukaan, minkä vuoksi siinä on virheellinen kirjaus 1000,00. Näin ollen siitä tulee -433,33, joka on liioiteltu kustannussumma. Laskelma: 1300 / 3 = .-433,33.  

Tapahtumassa numero 5 myös tämän tapahtuman **Kustannussumma todellinen** -kentän arvo on epätarkka samasta syystä.  

> [!NOTE]  
>  Jos luot Keskimäärä-arvostusmenetelmää käyttävälle varaston arvon laskulle kiinteän kohdistuksen, tällöin lasku ei vastaanota nimikkeen keskimääräistä kustannusta tavalliseen tapaan, vaan se vastaanottaa määrittämäsi varaston arvon nousun kustannukset. Tämä varaston arvon lasku ei tämän jälkeen enää ole osa keskimääräisten kustannusten laskenta.  

### <a name="example--fixed-application-in-sales-return" />Esimerkki – kiinteä kohdistus myyntipalautuksessa
Kiinteät kohdistukset ovat myös erittäin hyvä keino kustannuksen täsmälliseen peruuttamiseen, kuten myynnin palautusten kanssa.  

Seuraava esimerkki, jossa kuvataan, kuinka kiinteä sovellus varmistaa täsmällisen kustannusten muutoksen, perustuu seuraavaan skenaarioon:  

1.  Käyttäjä kirjaa ostolaskun.  
2.  Käyttäjä kirjaa myyntilaskun.  
3.  Käyttäjä kirjaa myyntitapahtumaa koskevan palautetun nimikkeen myyntihyvityslaskun, jolloin kustannuksen palautetaan oikein.  
4.  Rahtikulu, joka liittyy aiemmin kirjattuun ostotilaukseen, saapuu. Käyttäjä kirjaa sen nimikekuluksi.  

Seuraavassa taulukossa esitetään skenaarion vaiheiden 1-3 tulos nimikkeen arvokirjauksissa.  

|Kirjauspäivämäärä|Nimiketapahtuman tyyppi|Arvostettu määrä|Kustannussumma (todellinen)|Kohdistus nimiketapahtumasta|Nimiketapahtuman nro|Tapahtumanro|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Osto|1|1000.00||1|1|  
|02-01-20|Myynti|-1|1000.00||2|2|  
|03-01-20|Myynti (hyvityslasku)|1|1000|2|3|3|  

Seuraavassa taulukossa esitetään arvotapahtuma joka aiheutuu skenaarion vaiheesta 4, nimikekulun kirjauksesta.  

|Kirjauspäivämäärä|Nimiketapahtuman tyyppi|Arvostettu määrä|Kustannussumma (todellinen)|Kohdistus nimiketapahtumasta|Nimiketapahtuman nro|Tapahtumanro|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|04-01-20|(Nimikekulu)|1|100.00||1|4|  

Seuraavassa taulukossa esitetään täsmällisen kustannusten kumoamisen vaikutukset nimikkeen arvotapahtumiin.  

|Kirjauspäivämäärä|Nimiketapahtuman tyyppi|Arvostettu määrä|Kustannussumma (todellinen)|Kohdistus nimiketapahtumasta|Nimiketapahtuman nro|Tapahtumanro|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Osto|1|1000.00||1|1|  
|02-01-20|Myynti|-1|1100.00||2|2|  
|03-01-20|Myynti (hyvityslasku)|1|1100.00|2|3|3|  
|04-01-20|(Nimikekulu)|1|100.00||1|4|  

Kun **Muuta kustannuksia - Nimiketapahtumat** -eräajo suoritetaan, ostotapahtuman nimikeveloituksen vuoksi nousseet kustannukset välitetään myyntitapahtumalle (tapahtuma numero 2). Myyntikirjaus lähettää sitten edelleen nämä kasvaneet kustannukset myynnin kredit-kirjaukseen (kirjausnumero 3). Lopputulos on se, että kustannukset on kumottu oikein.  

> [!NOTE]  
>  Kun käsittelet palautuksia tai hyvityslaskuja ja olet määrittänyt **Todellisen kust. peruutt. pakollinen** -kentän joko **Ostojen ja ostovelkojen asetukset**- tai **Myyntien ja myyntisaamisten asetukset** -sivulla tilanteesi mukaisesti, [!INCLUDE[prod_short](includes/prod_short.md)] täyttää kohdistustapahtumakentät automaattisesti, kun käytät **Kopioi asiakirjasta** -toimintoa. Jos käytät **Hae peruutettavat kirjatut asiakirjarivit** -toimintoa, tällöin kentät täytetään aina automaattisesti.  

> [!NOTE]  
>  Jos kirjaat tapahtuman, jolla on kiinteä kohdistus ja kohdistettava nimiketapahtuma on suljettu (eli jäljellä oleva määrä on nolla), tällöin vanha kohdistus kumotaan automaattisesti ja nimiketapahtuma kohdistetaan uudelleen käyttämällä määrittämääsi kiinteää kohdistusta.  

## <a name="transfer-application" />Sovelluksen siirtäminen
Kun nimike siirretään paikasta toiseen yrityksen varastossa, näiden kahden siirtotapahtuman välille luodaan kohdistus. Siirtotapahtuman arvostaminen riippuu arvostusmenetelmästä. Keskiarvo-arvostusmenetelmää käyttävien nimikkeiden arvostus suoritetaan käyttämällä keskimääräistä kustannusta keskimääräisellä kustannusjaksolla jolla siirron arvostuspäivämäärä esiintyy. Muuta arvostusmenetelmää käyttävien nimikkeiden arvostus suoritetaan jäljittämällä takaisin alkuperäisen varaston arvon lisäyksen kustannukseen.  

### <a name="example--average-costing-method" />Esimerkki – keskiarvo-arvostusmenetelmä
Seuraava esimerkki, joka kuvaa sitä, kuinka eri siirtokirjauksia käytetään, perustuu seuraavaan skenaarion nimikkeestä, joka käyttää keskimääräisen kustannuslaskelman menetelmää ja keskimääräistä päivän kustannusjaksoa.  

1. Käyttäjä ostaa nimikkeen hintaan 10,00 (PVA).  
2. Käyttäjä ostaa nimikkeen uudelleen hintaan 20,00 (PVA).  
3. Käyttäjä siirtää nimikkeen ITÄ-sijainnista LÄNSI-sijaintiin.  

Seuraavassa taulukossa esitetään siirron vaikutus nimikkeen arvokirjauksiin.  

|Kirjauspäivämäärä|Nimiketapahtuman tyyppi|Sijaintikoodi |Arvostettu määrä|Kustannussumma (Tod.)|Tapahtumanro|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Osto|ITÄ|1|10,00|1|  
|01-01-20|Osto|ITÄ|1|20,00|2|  
|02-01-20|Siirto|ITÄ|-1|15,00|3|  
|02-01-20|Siirto|LÄNSI|1|15,00|4|  

### <a name="example--standard-costing-method" />Esimerkki – Arvostusmenetelmä Vakio
Seuraava esimerkki, joka kuvaa sitä, kuinka eri siirtokirjauksia käytetään, perustuu seuraavaan skenaarion nimikkeestä, joka käyttää kustannuslaskelman perusmenetelmää ja keskimääräistä päivän kustannusjaksoa.  

1. Käyttäjä ostaa nimikkeen normaaliin hintaan 10,00 (PVA).  
2. Käyttäjä siirtää nimikkeen ITÄ-sijainnista LÄNSI-sijaintiin vakiohinnalla 12,00 (PVA).  

Seuraavassa taulukossa esitetään siirron vaikutus nimikkeen arvokirjauksiin.  

|Kirjauspäivämäärä|Nimiketapahtuman tyyppi|Sijaintikoodi |Arvostettu määrä|Kustannussumma (Tod.)|Tapahtumanro|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Osto|ITÄ|1|10,00|1|  
|02-01-20|Siirto|ITÄ|-1|10,00|2|  
|02-01-20|Siirto|LÄNSI|1|10,00|3|  

Koska alkuperäisen varaston kasvun arvo on LCY 10.00, siirto arvioidaan kustannuksen mukaan, ei LCY 12.00.  

## <a name="reapplication" />Uudelleenkohdistus
Nimikkeen yksikkökustannuksen laskentatavan mukaan nimikkeen virheellinen kohdistus voi johtaa vääristyneeseen keskimääräiseen kustannukseen ja vääristyneeseen yksikkökustannukseen. Seuraavat skenaariot voivat aiheuttaa vääriä nimikesovelluksia, mikä vaatii sen, että mitätöit nimikesovellukset ja käytät uudelleen nimikkeen pääkirjan kirjaukset:  

* Unohdit tehdä kiinteän kohdistuksen.  
* Teit virheellisen kiinteän kohdistuksen.  
* Haluat ohittaa kirjauksen yhteydessä automaattisesti nimikkeen arvostusmenetelmän perusteella luodun kohdistuksen.  
* Palauta nimike, jolle on jo manuaalisesti kohdistettu myynti, ilman **Hae peruutettavat kirjatut asiakirjarivit** -toiminnon käyttämistä. Kohdistus on tämän vuoksi peruutettava.  

[!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa ominaisuuden nimikkeen kohdistusten analysointiin ja korjaamiseen. Tämä työ tehdään **Kohdistustyökirja**-sivulla.  

## <a name="see-also" />Katso myös
[Rakennetiedot: Nimikkeen kohdistuksen tunnettu ongelma](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[Rakennetiedot: Varaston arvostus](design-details-inventory-costing.md)  
[Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md)  
[Rakennetiedot: Keskimääräinen kustannus](design-details-average-cost.md)   
[Rakennetiedot: Kustannuksen muutos](design-details-cost-adjustment.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Rahoitus](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
