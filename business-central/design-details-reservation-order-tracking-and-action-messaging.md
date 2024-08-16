---
title: 'Suunnittelun yksityiskohdat - varaus, tilauksen seuranta ja toimenpideviestit | Microsoft-asiakirjat'
description: 'Varausjärjestelmä on kattava, ja se sisältää Tilauksen seuranta- ja Toimenpideviestintä-toimintojen toisiinsa liittyvät ja rinnakkaiset toiminnot.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 08/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys

Kattava varausjärjestelmä sisältää Tilausten seurannan ja toimenpideviestinnän toisiinsa liittyvät ja rinnakkaiset toiminnot.  

Varausjärjestelmän ytimessä on kysyntätapahtuman ja vastaavan tarjontatapahtuman linkittäminen joko varauksen tai tilauksen seurannan kautta. Varaus on käyttäjän luoma linkki ja tilauksen seurantatietue on järjestelmän luoma linkki. Varausjärjestelmään syötetty nimikemäärä on joko varattu tai tilausseurannassa, mutta ei molempia samaan aikaan. Se, miten järjestelmät käsittelevät nimikettä, riippuu siitä, miten nimike on määritetty.  

Varausjärjestelmä toimii yhteistyössä suunnittelujärjestelmän kanssa luomalla toimintaviestejä suunnitteluriveille suunnitteluajojen aikana. Toimenpideviestiä voidaan pitää lisäkkeenä seurantatietueelle. Toimenpideviestit tarjoavat kätevän työkalun tehokkaaseen tarjonnan suunnitteluun riippumatta siitä luodaanko ne dynaamisesti tilauksen seurannassa vai suunnitteluajon aikana.  

> [!NOTE]  
> Suunnittelujärjestelmä ei ota huomioon varattuja määriä. Hakemistolinkkiä, joka on tehty tuotannon ja kysynnän välille, ei voi vaihtaa suunnittelun aikana.  

 Varausjärjestelmä muotoilee myös rakenteellisen perustan nimikkeenseurantajärjestelmälle. Lisätietoja [on kohdassa Suunnittelun yksityiskohdat: Nimikkeen seuranta](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->
<!--
> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]
-->

## Varaus  

 Varaus on sitova linkki, joka yhdistää tietyn kysynnän ja tietyn tarjonnan toisiinsa. Tämä linkki vaikuttaa suoraan tuleviin varastotapahtumiin ja varmistaa nimiketapahtumien oikean kohdistuksen kustannustarkoituksia varten. Varaus ohittaa nimikkeen oletusarvoisen arvostusmenetelmän. Lisätietoja [on kohdassa Suunnittelun yksityiskohdat: Nimikkeen seuranta](design-details-item-tracking.md).  

 Varaus-sivulle **pääsee** kaikilta kysyntä- ja tarjontatyyppien tilausriveiltä. Tällä sivulla käyttäjä voi määrittää, mihin kysyntään tai tarjontaan tapahtuma luo varauslinkin. Varaus koostuu tietueparista, jotka jakavat saman kirjausnumeron. Yhdessä tietueessa on negatiivinen etumerkki ja se osoittaa kysyntään. Toisessa tietueessa on positiivinen merkki ja se osoittaa tarjontaan. Nämä tietueet tallennetaan Varaustapahtuma-taulukkoon *·*, jossa on tila-arvo *Varaus*. Käyttäjä voi tarkastella kaikkia varauksia **Varaustapahtumat**-sivulla.  

### Kompensoiminen varauksissa  

 Varaukset tehdään käytettävissä olevien nimikemäärien mukaisesti. Nimikkeen saatavuus lasketaan seuraavasti:  

 `available quantity = inventory + scheduled receipts - gross requirements`

 Seuraavassa taulukossa kuvataan tiedot tilausverkoston kohteista, jotka ovat osa käytettävyyslaskelmaa.  

||Kenttä T27-nimikkeessä|Lähdetaulukko|Taulukkosuodatin|Lähdekenttä|  
|-|------------------|------------------|------------------|------------------|  
|**Varasto**|Vaihto-omaisuus|Nimiketapahtuma|Ei saatavilla|määrä.|  
|**Aikataulutetut vastaanotot**|Sitsuun. til. vast.ot. (määrä)|Tuot.til. rivi|=Sitovasti suunniteltu|Jäljellä oleva määrä (perus)|  
|**Aikataulutetut vastaanotot**|Vapaut. til. vast.ot. (määrä)|Tuot.til. rivi|=Vapautettu|Jäljellä oleva määrä (perus)|  
|**Aikataulutetut vastaanotot**|Määrä kokoonpanotilauksessa|Kokoonpanon otsikko|=Järjestys|Jäljellä oleva määrä (perus)|  
|**Aikataulutetut vastaanotot**|Määrä ostotilauksessa|Ostorivi|=Järjestys|Avoin määrä (perus)|  
|**Aikataulutetut vastaanotot**|Siirtotil. vast.otto (määrä)|Siirtorivi|Ei saatavilla|Avoin määrä|  
|**Bruttotarpeet**|Määrä myyntitilauksessa|Myyntirivi|=Järjestys|Avoin määrä (perus)|  
|**Bruttotarpeet**|Aikataulut. tarve(määrä)|Tuotantotilauksen komponentti|<>Simuloitu|Jäljellä oleva määrä (perus)|  
|**Bruttotarpeet**|Määrä kokoonpanokomponentissa|Kokoonpanolinja|=Järjestys|Jäljellä oleva määrä (perus)|  
|**Bruttotarpeet**|Siirtotil. toimitus (määrä)|Siirtorivi|Ei saatavilla|Avoin määrä|  

 Lisätietoja on kohdassa [Suunnittelun yksityiskohdat: Saatavuus fyysisessä varastoinnissa](design-details-availability-in-the-warehouse.md).  

### Manuaalinen varaus  

Kun käyttäjä luo varauksen tarkoituksenmukaisesti, hän saa näiden nimikkeiden täydet omistusoikeudet ja on nimikkeistä vastuussa. Tämä tarkoittaa sitä, että käyttäjän on myös muutettava tai peruutettava varaus manuaalisesti. Tällaiset manuaaliset muutokset voivat aiheuttaa kyseisten varausten automaattisen muokkauksen.  

Seuraavassa taulukossa näkyy, milloin ja mitä muutoksia voi tapahtua:  

|Käyttäjän toimenpide|Järjestelmän reaktio|  
|-----------------|---------------------|  
|Varatun määrän pienentäminen|Liittyvät lukumäärät päivitetään.|  
|Päivämääräkenttien muuttaminen|Liittyvät päivämääräkentät päivitetään.<br /><br /> **Huomautus:** Jos kysynnän eräpäivä muutetaan toimituspäivämäärää tai tarjonnan eräpäivää edeltäväksi, varaus peruuntuu.|  
|Tilauksen poistaminen|Varaus on peruttu.|  
|Sijainnin, varastopaikan, variantin, sarjanumeron tai eränumeron muuttaminen|Varaus on peruttu.|  

> [!NOTE]  
> Late Binding -toiminto voi myös vaihtaa varaukset ilman, että tiedottaa tästä käyttäjää, järjestämällä uudelleen yleiset sarja- tai eränumeroiden varaukset. Lisätietoja [on kohdassa Suunnittelun yksityiskohdat: Nimikeseuranta ja Varaukset](design-details-item-tracking-and-reservations.md).  

### Automaattiset varaukset  

Nimikkeen kortti voidaan määrittää varaamaan nimikkeitä automaattisesti kysynnän perusteella, esimerkiksi myyntitilausten perusteella. Tässä tapauksessa varaus suoritetaan varastolle, ostotilauksille, kokoonpanotilauksille ja tuotantotilauksille. Varoitus annetaan, jos tarjonta ei riitä.  

Lisäksi useat suunnittelutoiminnot varaavat nimikkeitä automaattisesti, jotta tiettyyn tarjontaan linkitetty kysyntä säilyy. Tällaisten suunnittelulinkkien **tilauksen seurantatapahtumissa** on Varaustapahtuma-taulukon Varauksen tila **-** kentässä *Varaus* . Automaattiset varaukset luodaan seuraavissa tilanteissa:  

- Monitasoinen tuotantotilaus, jossa liittyvän ylä- ja alatason nimikkeiden **Tuotantotapa**-kentän arvoksi on asetettu **Tilausohjattu**. Suunnittelujärjestelmä luo varauksia pääelementti tuotantotilauksen ja sen perustana olevan tuotantotilauksen välille. Näin varmistetaan, että pääelementti käsitellään yhdessä. Tämä varauksen sitovuus ohittaa nimikkeen oletusarvoiset arvostus- ja kohdistusmenetelmät.  

- Tuotanto-, kokoonpano- tai ostotilaus, jossa liittyvän nimikkeen **Uusintatilaustapa**-kentän arvoksi on asetettu **Tilaus**. Suunnittelujärjestelmä luo varaukset kysynnän ja suunnitellun tarjonnan välillä, jolloin varmistetaan, että erityinen tarjonta on luotu. Lisätietoja on Tilaus-kohdassa [...](design-details-handling-reordering-policies.md#order).  

- Myyntitilauksesta luotu tuotantotilaus, jonka **Myyntitilaussuunnittelu**-toiminto on linkitetty myyntitilaukseen automaattisella varauksella.  

- Myyntitilausriville automaattisesti luotu kokoonpanotilaus, joka täyttää Tilaukseen koottava määrä **-** kentän määrän. Tämä automaattinen varaus linkittää myynnin kysynnän ja kokoonpanon tarjonnan niin, että myyntitilauksen käsittelijät voivat mukauttaa sitä ja luvata kokoonpanonimikkeen asiakkaalle heti. Lisäksi varaus linkittää kokoonpanon tuotoksen myyntitilausriviin toimitustoiminnon kautta, joka täyttää asiakkaan tilauksen.  

Jos kysyntää tai tarjontaa ei ole kohdistettu, suunnittelujärjestelmä määrittää automaattisesti varaustilan **Ylijäämä**. Syy voi olla kysyntä, joka aiheutuu ennustemääristä tai käyttäjän syöttämistä suunnitteluparametreista. Tämä on oikeutettu ylijäämä, jonka järjestelmä tunnistaa, eikä se aiheuta toimenpideviestejä. Ylijäämä voi olla myös aito, ylimääräinen tarjonta tai kysyntä, joka ei ole vielä seurattu. Tämä kertoo tilausverkon epätasapainosta. Epätasapainon vuoksi järjestelmä antaa toimenpideviestejä. Huomaa, että toimenpideviesti, joka ehdottaa määrän muutosta viittaa aina tyyppiin **Ylijäämä**. Lisätietoja [on tämän artikkelin Kohdassa Esimerkki: Tilauksen seuranta myynneissä, tuotannossa ja siirroissa](#example-order-tracking-in-sales-production-and-transfers) .  

Suunnitellun ajon aikana luotuja automaattisia varauksia käsitellään seuraavilla tavoilla:  

- Niitä käytetään saatavuuslaskennassa sisällytettyihin nimikemääriin, kuten manuaalisiin varauksiin. Lisätietoja on tämän artikkelin Kompensoiminen varauksissa -osassa.  

- Ne sisällytetään seuraaviin suunnitteluajoihin, ja niitä voidaan mahdollisesti muuttaa, toisin kuin manuaalisesti varatut nimikkeet.  

## Tilauksen seuranta  

Tilauksen seuranta auttaa suunnittelijaa säilyttämään kelvollisen toimitussuunnitelman esittämällä yleiskuvan kysynnän ja tarjonnan siirtymästä tilausverkossa. Tilauksenseurantatietueet palvelevat pohjana, jolle luodaan dynaamiset toimintaviestit ja suunnitteluriviehdotukset suunnitteluajojen aikana.  

> [!NOTE]  
> Tilauksenseurantajärjestelmä hyvittää käytettävissä olevan varaston, kun tilaukset on kirjattu tilausverkostoon. Tämä tarkoittaa sitä, että järjestelmä ei priorisoi mahdollisesti kiireellisempiä tilauksia niiden eräpäivän perusteella. Näin ollen näiden prioriteettien uudelleen järjestäminen on suunnittelujärjestelmän logiikan tai suunnittelijan vastuulla.  

> [!NOTE]  
> Tilauksen seurantatapaa ja Hae toimenpideviestit -toimintoa ei ole integroitu projektien kanssa. Tämä tarkoittaa sitä, että projektiin liittyvää kysyntää ei seurata automaattisesti. Koska sitä ei seurata, se voi aiheuttaa olemassa olevan täydennystilauksen ja projektitietojen seurannan käytön toiseen kysyntään, esimerkiksi myyntitilaukseen. Tällöin saattaa ilmetä tilanne, jossa käytettävissä olevan varaston tiedot eivät ole synkronoituina.  

### Tilausverkosto  

Tilauksen seurantajärjestelmä perustuu periaatteeseen, jonka mukaan tilausverkon on aina oltava tasapainossa ja varmistettava, että vastaava tarjonta offseti järjestelmän jokaiselle kysynnälle. Järjestelmä tekee tämän tunnistamalla tilausverkon kysyntä- ja tarjontatapahtumien väliset loogiset linkit.  

Tämä periaate osoittaa, että kysynnän muutos johtaa vastaavan epätasapainon syntymiseen tilausverkon tarjontapuolella. Käänteisesti, tarjonnan muutos johtaa vastaavan epätasapainon syntymiseen tilausverkon kysyntäpuolella. Todellisuudessa tilausverkossa on jatkuvassa muutostilassa, kun käyttäjät kirjoittavat, muuttavat ja poistavat tilauksia. Tilauksen seuranta käsittelee tilaukset dynaamisesti ja reagoi jokaiseen muutokseen sillä hetkellä, kun se siirtyy järjestelmään ja muuttuu osaksi tilausverkkoa. Heti kun uudet tilauksen seurantatietueet luodaan, tilausverkko on tasapainossa, mutta ainoastaan seuraavaan muutokseen asti.  

Suunnittelujärjestelmän laskentojen läpinäkyvyyttä nostaa ei-seurattujen määrien näkyminen **Ei-seuratut suunnitteluelementit** -sivulla. Arvo osoittaa tunnetun kysynnän ja ehdotetun tarjonnan välisen määrän eron. Jokainen sivun rivi viittaa ylittävän määrän syyhyn, kuten **Puitetilaus**, **Varaston turvataso**, **Kiinteä uusintatilausmäärä**, **Vähimmäistilausmäärä**, **Pyöristys** tai **Puskuriaika**.  

### Kompensoiminen tilausten seurannassa  

Toisin kuin varaukset, jotka voidaan tehdä vain käytettävissä olevien nimikkeiden määrän kohdalla, nimikkeen seuranta on mahdollista kaikkien tilausverkon yksiköiden kohdalla, jotka ovat osa suunnittelujärjestelmän nettotarpeiden laskentaa. Verkkovaatimukset lasketaan seuraavasti:  

`net requirements = gross requirements + reorder point - scheduled receipts - planned receipts - projected available balance`  

> [!NOTE]  
> Kysyntää, joka liittyy ennusteisiin tai suunnitteluparametreihin, ei seurata.  

### Esimerkki: tilauksen seuranta myynnissä, tuotannossa ja siirroissa  

Seuraavassa esimerkkitilanteessa varaustapahtuma-taulukkoon *luodaan* tilauksen seurantatapahtumat eri tilausverkkomuutosten seurauksena.  

Oletetaan, että seuraavat tiedot koskevat kahta nimikettä, joille asetetaan tilauksen seuranta.  

|Vaihtoehto|Parametri|Erittely|
|-|-|-|
|Nimike 1|Nimi|Komponentti|
||Saatavuus|100 yksikköä ITÄ-sijainnissa<br /><br />- 30 yksikköä LOTA-erää<br />- 70 yksikköä LOTB-erää|  
|Nimike 2|Nimi|Tuotettu nimike|
||Tuotannon tuoterakenne|1 määrä komponenttia kohti|  
||Kysyntä|100 yksikön myynti sijainnissa WEST|  
||Tarjonta|Vapautettu tuotantotilaus (joka on luotu 100 yksikön myynnin Myyntitilauksen suunnittelu *-toiminnolla*)|  

 **Tuotannon asetukset -** sivulla Komponentit **sijainnissa** -kentän arvoksi *määritetään ITÄ*.

Varaustapahtuma-taulukossa *on* seuraavat tilauksen seurantatapahtumat taulukon tietojen perusteella.  

<!--![First example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  -->
**Varaustapahtumat**

|Tapahtumanro|Positiivinen|Nimikenro|Sijaintikoodi|Määrä|Varauksen tila|Kuvaus|Eränro|Alkuperäinen tyyppi|Lähdetunnus|Sitovuus|  
|--------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|KOMPONENTTI|ITÄ|-70|Seuranta|Komponentti|-|5407|101004|-|
|8|Kyllä|KOMPONENTTI|ITÄ|70|Seuranta|Komponentti|ERÄB|32|-|-| 
|9|-|KOMPONENTTI|ITÄ|-30|Seuranta|Komponentti|-|5407|1001004|-| 
|9|Kyllä|KOMPONENTTI|ITÄ|30|Seuranta|Komponentti|LOTA|32|-|-| 
|10|-|TUOTETTU NIMIKE|LÄNSI|-100|Varaus|Tuotettu nimike|-|37|1001|Tilaus Tilauksesta|
|10|Kyllä|TUOTETTU NIMIKE|LÄNSI|100|Varaus|Tuotettu nimike|-|5406|101004|Tilaus Tilauksesta|


#### Tapahtumanumerot 8 ja 9  

ERÄA- ja ERÄB-komponenttitarvetta varten luodaan tilauksen seurantalinkkejä taulukon 5407 Tuotantotilauksen *komponentti* kysynnästä taulukon 32 Nimiketapahtuma *tarjontaan*. Varauksen **tila -** kentässä *on Seuranta* osoittamaan, että nämä tapahtumat ovat tarjonta ja kysyntä välisiä dynaamisia tilauksen seurantalinkkejä.  

> [!NOTE]  
> Eränro **·** -kenttä on tyhjä kysyntäriveillä, koska eränumeroita ei ole määritetty vapautetun tuotantotilauksen komponenttiriveillä.  

#### Tapahtumanumero 10  

Taulukon 37 Myyntirivit *myyntikysynnästä* luodaan tilauksen seurantalinkki tarjontaan taulukossa 5406, *Tuotantotilausrivi*. Varauksen **tila -** kentässä on *Varaus*, ja **Sitova-kentässä** on *Tilauskohtainen*. Tämä johtuu siitä, että vapautettu tuotantotilaus luotiin erityisesti myyntitilausta varten, ja se tulee säilyttää linkitettynä, toisin kuin tilauksen seurantalinkit, joiden varaustila on Seuranta, joka luodaan ja muutetaan dynaamisesti. Lisätietoja [on tämän artikkelin Automaattiset](#automatic-reservations) varaukset -osassa.  

 Tässä skenaarion vaiheessa 100 YKSIKKÖÄ ERÄA ja ERÄB siirretään WEST-sijaintiin siirtotilauksella.  

> [!NOTE]  
> Vain siirtotilauksen toimitus kirjataan tässä vaiheessa, ei vastaanottoa.  

 Varaustapahtuma-taulukossa on *nyt seuraavat tilauksen seurantatapahtumat* .  

<!-- ![Second example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  -->
**Varaustapahtumat**

|Tapahtumanro|Positiivinen|Nimikenro|Sijaintikoodi|Määrä|Varauksen tila|Kuvaus|Eränro|Alkuperäinen tyyppi|Lähdetunnus|Sitovuus|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|9|-|KOMPONENTTI|ITÄ|-30|Ylijäämä|Komponentti|-|5407|1001004|-| 
|10|-|TUOTETTU NIMIKE|LÄNSI|-100|Varaus|Tuotettu nimike|-|37|1001|Tilaus Tilauksesta|
|10|Kyllä|TUOTETTU NIMIKE|LÄNSI|100|Varaus|Tuotettu nimike|-|5406|101004|Tilaus Tilauksesta|
|12|Kyllä|KOMPONENTTI|LÄNSI|70|Ylijäämä|Komponentti|ERÄB|5741|1011|-| 
|14|Kyllä|KOMPONENTTI|LÄNSI|30|Ylijäämä|Komponentti|LOTA|5741|1011|-| 
|15|Kyllä|KOMPONENTTI|ULOS. LOKI.|70|Ylijäämä|Komponentti|ERÄB|32|-|-| 
|16|Kyllä|KOMPONENTTI|ULOS. LOKI.|30|Ylijäämä|Komponentti|LOTA|32|-|-| 

#### Tapahtumanumerot 8 ja 9  

Taulukon 5407 kysyntää kuvaavan komponentin kahden erän tilauksen seurantatapahtumat muutetaan seurannan *varaustilasta* Ylijäämäksi *·*. Syy on se, että siirtotilauksen toimitus käyttää aiemmin taulukossa 32 aiemmin linkitettyjä tarvikkeita.  

Aito ylijäämä, kuten tässä tapauksessa, kuvastaa ylimääräistä tarjontaa tai kysyntää, jota ei seurata. Se on osoitus epätasapainosta tilausverkossa, joka luo suunnittelujärjestelmän toimenpideviestin, ellei sitä ratkaista dynaamisesti.  

#### Tapahtumanumerot 12–16  

Koska komponentin kaksi erää on kirjattu siirtotilaukseen toimitetuiksi, mutta ei vastaanotetuiksi, kaikki asiaan liittyvät positiivisen tilauksen seurantatapahtumat ovat varaustyyppiä *Ylijäämä*, mikä osoittaa, että niitä ei ole kohdistettu mihinkään kysyntään. Jokaisen eränumeron osalta yksi tapahtuma liittyy taulukkoon 5741, *Siirtorivi*, ja yksi tapahtuma liittyy nimiketapahtumaan kuljetuksessa-sijainnissa, jossa nimikkeet ovat nyt olemassa.  

Tässä esimerkkitilanteessa komponenttien *siirtotilaus ITÄ-Sijainnista*  *LÄNTEEN* kirjataan vastaanotetuksi.  

Varaustapahtuma-taulukossa on *nyt seuraavat tilauksen seurantatapahtumat* .  

<!-- ![Third example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3") -->
 **Varaustapahtumat**

|Tapahtumanro|Positiivinen|Nimikenro|Sijaintikoodi|Määrä|Varauksen tila|Kuvaus|Eränro|Alkuperäinen tyyppi|Lähdetunnus|Sitovuus|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|KOMPONENTTI|ITÄ|-70|Ylijäämä|Komponentti|-|5407|101004|-| 
|9|-|KOMPONENTTI|ITÄ|-30|Ylijäämä|Komponentti|-|5407|1001004|-|
|10|-|TUOTETTU NIMIKE|LÄNSI|-100|Varaus|Tuotettu nimike|-|37|1001|Tilaus Tilauksesta|
|10|Kyllä|TUOTETTU NIMIKE|LÄNSI|100|Varaus|Tuotettu nimike|-|5406|101004|Tilaus Tilauksesta|
|17|Kyllä|KOMPONENTTI|LÄNSI|70|Ylijäämä|Komponentti|ERÄB|32|-|-| 
|18|Kyllä|KOMPONENTTI|LÄNSI|30|Ylijäämä|Komponentti|LOTA|32|-|-| 

Tilauksen seurantatapahtumat muistuttavat nyt skenaarion ensimmäistä pistettä ennen kuin siirtotilaus kirjattiin vain toimitetuksi, paitsi että komponentin tapahtumilla on nyt varaustila *Ylijäämä*. Tämä johtuu siitä, että komponenttitarve on yhä ITÄ-sijainnissa *·*, mikä kuvastaa sitä, että **tuotantotilauksen komponenttirivin Sijaintikoodi-kentässä** on *ITÄ* Komponentit **sijainnissa** -kentän määritysten mukaisesti. Kyseiselle kysynnälle aiemmin kohdistettu tarjonta siirrettiin *LÄNSI-sijaintiin*, eikä sitä voi seurata täysin, ellei tuotantotilausrivin komponenttitarvetta muuteta WEST-sijainniksi *·* .  

Tässä skenaarion vaiheessa tuotantotilauksen **komponenttirivin Sijaintikoodi-kentän** arvoksi *määritetään LÄNSI*.  **Lisäksi Nimikkeen seurantarivit** -sivulla tuotantotilauksen komponenttiriville on määritelty 30 ERÄA-yksikköä ja 70 ERÄB-yksikköä.  

Varaustapahtuma-taulukossa on *nyt seuraavat tilauksen seurantatapahtumat* .  

<!-- ![Fourth example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")   -->
 **Varaustapahtumat**

|Tapahtumanro|Positiivinen|Nimikenro|Sijaintikoodi|Määrä|Varauksen tila|Kuvaus|Eränro|Alkuperäinen tyyppi|Lähdetunnus|Sitovuus|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|10|-|TUOTETTU NIMIKE|LÄNSI|-100|Varaus|Tuotettu nimike|-|37|1001|Tilaus Tilauksesta|
|10|Kyllä|TUOTETTU NIMIKE|LÄNSI|100|Varaus|Tuotettu nimike|-|5406|101004|Tilaus Tilauksesta|
|21|-|KOMPONENTTI|LÄNSI|-70|Seuranta|Komponentti|ERÄB|5407|101004|-| 
|21|Kyllä|KOMPONENTTI|LÄNSI|70|Seuranta|Komponentti|ERÄB|32|-|-| 
|22|-|KOMPONENTTI|LÄNSI|-30|Seuranta|Komponentti|LOTA|5407|1001004|-| 
|22|Kyllä|KOMPONENTTI|LÄNSI|30|Seuranta|Komponentti|LOTA|32|-|-| 

#### Tapahtumanumerot 21 ja 22  

Koska komponenttitarve on muutettu WEST-sijainniksi *ja* tarjonta on saatavilla nimiketapahtumina WEST-sijainnissa *·*, kaikkia näiden kahden eränumeron tilauksen seurantatapahtumia seurataan nyt täysin, mikä näkyy Seurannan *varaustilana*.  

Eränro **Kentässä** on nyt taulukon 5407 tilauksen seurantatapahtuma, koska eränumerot määriteltiin tuotantotilauksen komponenttiriveille.  

## Toimenpiteiden viestitys  

Kun tilausten seurantajärjestelmä havaitsee epätasapainotilan tilausverkossa, se luo automaattisesti toimenpideviestin käyttäjälle. Toimenpideviestit ovat järjestelmän luomia käyttäjätoimintopyyntöjä, joissa määritetään epätasapainon yksityiskohdat ja ehdotukset siitä, miten tasapaino voidaan palauttaa tilausverkkoon. Ne näkyvät suunnitteluriveinä **Suunnittelutyökirjat-sivulla**, kun valitset **Hae toimenpideviestit -** toiminnon. Suunnitteluajon aikana luodaan myös suunnittelurivien toimenpideviestejä, jotka vastaavat suunnittelujärjestelmän ehdotuksia tasapainon palauttamiseksi tilausverkkoon. Molemmissa tapauksissa ehdotukset suoritetaan tilausverkossa, kun valitset **Toteuta toimenpideviesti -** toiminnon.  

Toimenpideviesti käsittelee yhden tuoterakenteen tason kerralla. Jos käyttäjä hyväksyy toimenpideviestin, siitä voi tulla lisää toimenpideviestejä seuraavalla tuoterakennetasolla.  

Seuraavassa taulukossa esitellään olemassa olevat toimintaviestit.  

|Toimenpidesanoma|Description|  
|--------------------|---------------------------------------|  
|**Muuta määrä**|Muuttaa olemassa olevan toimitustilauksen määrän kattamaan muuttunutta tai uutta kysyntää.|  
|**Aikataul. uud.**|Aikatauluttaa olemassa olevan tilauksen eräpäivän.|  
|**Aikataul. uud. & Muuta määrä**|Aikatauluttaa määräpäivän uudelleen ja muuttaa olemassa olevan tilauksen määrää.|  
|**Uusi**|Luo uuden tilauksen, jos kumpikaan aiemmista toimenpideviesteistä ei pysty täyttämään kysyntää.|  
|**Peruuta**|Peruuttaa olemassa olevan tilauksen.|  

Tilauksenseurantajärjestelmä yrittää aina ratkaista epätasapainon olemassa olevassa tilausverkostossa. Jos tämä ei ole mahdollista, se antaa toimenpideviestin uuden tilauksen luomiseksi. Seuraava on tilausten seurantajärjestelmän käyttämä prioriteetin mukaan järjestetty luettelo, jota käytetään täsmäytyksen palauttamiseen. Jos tilausverkkoon tulee lisäkysyntä, järjestelmä yrittää seurata seuraavia tarkastuksia:  

1. Tarkista tämän kysynnän ylimääräinen tarjonta olemassa olevassa seurantatietueessa.  
1. Tarkista suunnitellut ja aikataulutetut vastaanotot vastaanottopäivämääräjärjestyksessä. Viimeisin mahdollinen päivämäärä on valittu.  
1. Tarkista käytettävissä oleva varasto.  
1. Tarkista, onko toimitustilausta olemassa nykyisen tilauksen seurantatietueessa. Jos on, järjestelmä antaa muuta-tyyppisen *toimenpideviestin* tilauksen lisäämiseksi.  
1. Tarkista, että nykyisen tilauksen seurantatietueessa ei ole toimitustilausta. Jos on, järjestelmä luo uuden tilauksen luoden toimenpideviestin, jonka tyyppi *on Uusi* .  

Avaa kysyntä kulkee luettelon läpi ja siirtää käytettävissä olevaa tarjontaa jokaisessa kohdassa. Kaikki jäljellä oleva kysyntä täytetään aina tarkastuksessa 4 tai tarkastuksessa 5.  

Jos kysynnän määrä vähenee, tilausten seurantajärjestelmä yrittää ratkaista epätasapainon suorittamalla aiemmat tarkastukset käänteisessä järjestyksessä. Tämä tarkoittaa sitä, että olemassa olevia toimenpideviestejä voi muokata ja tarvittaessa ne voi poistaa. Tilauksenseurantajärjestelmä esittää aina nettotuloksen laskelmista käyttäjälle.  

## Tilauksen seuranta ja suunnittelu  

Kun suunnittelujärjestelmä toimii, se poistaa kaikki olemassa olevat tilauksen seurantatietueet ja toimenpideviestitapahtumat ja luo ne uudelleen suunnittelurivin ehdotuksina tarjonta/kysyntä-parien ja prioriteettien mukaan. Kun suunnitteluajo on päättynyt, tilausverkko on tasapainossa.  

### Suunnittelujärjestelmän vertailu tilauksen seurantaan ja toimenpideviesteihin  

 Seuraava vertailu osoittaa erot menetelmien välillä, joita suunnittelujärjestelmä käyttää luodessaan suunnittelurivin ehdotuksia ja menetelmiä, joita tilauksenseurantajärjestelmä käyttää luodakseen tilauksenseurantatietueet ja toimintaviestit.  

- Suunnittelujärjestelmä käsittelee tietyn nimikkeen koko kysyntä- ja tarjontamallin, kun taas tilauksenseuranta käsittelee tilausta, joka on aktivoinut sen.  

- Suunnittelujärjestelmä käsittelee kaikkia BOM-hierarkian tasoja, kun taas tilauksenseuranta käsittelee yhden BOM-tason kerrallaan.  

- Suunnittelujärjestelmä muodostaa linkkejä kysynnän ja tarjonnan välille etusijalle asetetun eräpäivän mukaisesti. Tilauksen seuranta muodostaa linkit kysynnän ja tarjonnan välille tilaustapahtumien järjestyksen perusteella.  

- Suunnittelujärjestelmässä otetaan huomioon suunnitteluparametrit, kun taas tilauksen seurannassa ei oteta huomioon.  

- Suunnittelujärjestelmä luo linkit käyttäjän aktivoimassa erätilassa, kun se tasapainottaa kysyntää ja tarjontaa, kun taas tilaustenseuranta luo linkit automaattisesti ja dynaamisesti, kun käyttäjä syöttää tilaukset.  

## Katso myös  

[Rakennetiedot: Suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)  
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
