---
title: 'Rakennetiedot – varaus, tilauksen seuranta ja toimenpiteiden viestintä | Microsoft Docs'
description: Varausjärjestelmä on kokonaisvaltainen ja se sisältää Tilausten seurannan ja toimintaviestinnän keskenään yhteydessä olevat ja rinnakkaiset ominaisuudet.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-reservation-order-tracking-and-action-messaging" />Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys
Varausjärjestelmä on kokonaisvaltainen ja se sisältää Tilausten seurannan ja toimintaviestinnän keskenään yhteydessä olevat ja rinnakkaiset ominaisuudet.  

 Varausjärjestelmän ydin on kysyntätapahtuman ja vastaavan toimitustapahtuman linkittäminen varauksen tai tilauksen seurannan kautta. Varaus on käyttäjän luoma linkki ja tilauksen seurantatietue on järjestelmän luoma linkki. Varausjärjestelmään kirjoitettava nimikemäärä on joko varattu tai tilauksen seuranta mutta se ei voi olla molempia samanaikaisesti. Järjestelmien nimikkeiden käsittely riippuu siitä miten nimike määritetään.  

 Varausjärjestelmä toimii yhteistyössä suunnittelujärjestelmän kanssa luomalla toimintaviestejä suunnitteluriveille suunnitteluajojen aikana. Toimenpideviestiä voidaan pitää lisäkkeenä seurantatietueelle. Toimenpideviestit tarjoavat kätevän työkalun tehokkaaseen tarjonnan suunnitteluun riippumatta siitä luodaanko ne dynaamisesti tilauksen seurannassa vai suunnitteluajon aikana.  

> [!NOTE]  
>  Suunnittelujärjestelmä ei ota huomioon varattuja määriä. Hakemistolinkkiä, joka on tehty tuotannon ja kysynnän välille, ei voi vaihtaa suunnittelun aikana.  

 Varausjärjestelmä muotoilee myös rakenteellisen perustan nimikkeenseurantajärjestelmälle. Lisätietoja on kohdassa [Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="reservation" />Varaus
 Varaus on sitova linkki, joka yhdistää tietyn kysynnän ja tietyn tarjonnan toisiinsa. Tämä linkki vaikuttaa suoraan tuleviin varastotapahtumiin ja varmistaa nimiketapahtumien oikean kohdistuksen kustannustarkoituksia varten. Varaus ohittaa nimikkeen oletusarvoisen arvostusmenetelmän. Lisätietoja on kohdassa [Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md).  

 **Varaus**-sivu on käytettävissä kaikilta tilausriveiltä sekä kysyntä- että tarjontatyypeissä. Tällä sivulla käyttäjä voi määrittää mihin kysyntä- tai tarjontatapahtumaan varauslinkki luodaan. Varaus koostuu tietueparista, jotka jakavat saman kirjausnumeron. Yhdessä tietueessa on negatiivinen etumerkki ja se osoittaa kysyntään. Toisessa tietueessa on positiivinen merkki ja se osoittaa tarjontaan. Nämä tietueet on tallennettu **Varaustapahtuma** -taulukkoon, jonka tilan arvo on **varaus**. Käyttäjä voi tarkastella kaikkia varauksia **Varaustapahtumat**-sivulla.  

### <a name="offsetting-in-reservations" />Kompensoiminen varauksissa
 Varaukset tehdään käytettävissä olevien nimikemäärien mukaisesti. Nimikkeen saatavuus lasketaan seuraavasti:  

 saatavilla oleva määrä + varasto + aikataulutetut vastaanotot - bruttotarve.  

 Seuraavassa taulukossa kuvataan tiedot tilausverkoston kohteista, jotka ovat osa käytettävyyslaskelmaa.  

||Kenttä kohteessa T27|Lähdetaulukko|Taulukkosuodatin|Lähdekenttä|  
|-|------------------|------------------|------------------|------------------|  
|**Varasto**|Varasto|Nimiketapahtuma|Ei saatavilla|määrä.|  
|**Aikataulutetut vastaanotot**|Sitsuun. til. vast.ot. (määrä)|Tuot.til. rivi|=Sitovasti suunniteltu|Jäljellä oleva määrä (perus)|  
|**Aikataulutetut vastaanotot**|Vapaut. til. vast.ot. (määrä)|Tuot.til. rivi|=Vapautettu|Jäljellä oleva määrä (perus)|  
|**Aikataulutetut vastaanotot**|Määrä kokoonpanotilauksessa|Kokoonpanon otsikko|=Järjestys|Jäljellä oleva määrä (perus)|  
|**Aikataulutetut vastaanotot**|Määrä ostotilauksessa|Ostorivi|=Järjestys|Avoin määrä (perus)|  
|**Aikataulutetut vastaanotot**|Siirtotil. vast.otto (määrä)|Siirtorivi|Ei saatavilla|Avoin määrä|  
|**Bruttotarpeet**|Määrä myyntitilauksessa|Myyntirivi|=Järjestys|Avoin määrä (perus)|  
|**Bruttotarpeet**|Aikataulut. tarve(määrä)|Tuotantotilauksen komponentti|<>Simuloitu|Jäljellä oleva määrä (perus)|  
|**Bruttotarpeet**|Määrä kokoonpanokomponentissa|Kokoonpanolinja|=Järjestys|Jäljellä oleva määrä (perus)|  
|**Bruttotarpeet**|Siirtotil. toimitus (määrä)|Siirtorivi|Ei saatavilla|Avoin määrä|  

 Lisätietoja on kohdassa [Rakennetiedot: Saatavuus varastossa.](design-details-availability-in-the-warehouse.md)  

### <a name="manual-reservation" />Manuaalinen varaus
 Kun käyttäjä luo varauksen tarkoituksenmukaisesti, hän saa näiden nimikkeiden täydet omistusoikeudet ja on nimikkeistä vastuussa. Tämä tarkoittaa sitä, että käyttäjän on myös muutettava tai peruutettava varaus manuaalisesti. Tällaiset manuaaliset muutokset voivat aiheuttaa kyseisten varausten automaattisen muokkauksen.  

 Seuraavassa taulukossa kuvataan milloin ja mitkä muutokset saattavat tapahtua:  

|Käyttäjän toimenpide|Järjestelmän reaktio|  
|-----------------|---------------------|  
|Varatun määrän pienentäminen|Liittyvät lukumäärät päivitetään.|  
|Päivämääräkenttien muuttaminen|Liittyvät päivämääräkentät päivitetään.<br /><br /> **Huomautus:** Jos kysynnän eräpäivä muutetaan toimituspäivämäärää tai tarjonnan eräpäivää edeltäväksi, varaus peruuntuu.|  
|Tilauksen poistaminen|Varaus on peruttu.|  
|Sijainnin, varastopaikan, variantin, sarjanumeron tai eränumeron muuttaminen|Varaus on peruttu.|  

> [!NOTE]  
>  Late Binding -toiminto voi myös vaihtaa varaukset ilman, että tiedottaa tästä käyttäjää, järjestämällä uudelleen yleiset sarja- tai eränumeroiden varaukset. Katso lisätiedot kohdasta "Rakennetiedot: nimikkeen seuranta ja varaukset".  

### <a name="automatic-reservations" />Automaattiset varaukset
 Nimikekortti voidaan määritellä olemaan aina automaattisesti varattu kysynnästä, kuten myyntitilaukset. Tässä tapauksessa varaus suoritetaan varastolle, ostotilauksille, kokoonpanotilauksille ja tuotantotilauksille. Järjestelmä antaa varoituksen, jos tarjontaa ei ole riittävästi.  

 Lisäksi erilaiset suunnittelutoiminnot varaavat nimikkeitä automaattisesti kysynnän pitämiseksi linkitettynä tiettyyn tarjontaan. Tilauksenseurantakirjaukset tällaisille seurantalinkeille sisältävät **Varauksen** **Varauksen tila** -kentässä **Varauksen kirjaus** -taulukossa. Automaattiset varaukset luodaan seuraavissa tilanteissa:  

-   Monitasoinen tuotantotilaus, jossa liittyvän ylä- ja alatason nimikkeiden **Tuotantotapa**-kentän arvoksi on asetettu **Tilausohjattu**. Suunnittelujärjestelmä luo varaukset alkuperäisen tuotantotilauksen ja alla olevan tuotantotilausten välillä, jolloin varmistetaan, että ne suoritetaan yhdessä. Tällainen varausside kumoaa nimikkeen oletuskustannukset ja sovellusmenetelmät.  

-   Tuotanto-, kokoonpano- tai ostotilaus, jossa liittyvän nimikkeen **Uusintatilaustapa**-kentän arvoksi on asetettu **Tilaus**. Suunnittelujärjestelmä luo varaukset kysynnän ja suunnitellun tarjonnan välillä, jolloin varmistetaan, että erityinen tarjonta on luotu. Lisätietoja on kohdassa [Tilaus](design-details-handling-reordering-policies.md#order).  

-   Myyntitilauksesta luotu tuotantotilaus, jonka **Myyntitilaussuunnittelu**-toiminto on linkitetty myyntitilaukseen automaattisella varauksella.  

-   Myyntitilausriville automaattisesti luotu kokoonpanotilaus täyttää **($ T_37_900 Qty. to Assemble to Order $)** -kentän määrän. Tämä automaattinen varaus linkittää myynnin kysynnän ja kokoonpanon tarjonnan niin, että myyntitilauksen käsittelijät voivat mukauttaa sitä ja luvata kokoonpanonimikkeen asiakkaalle heti. Lisäksi varaus linkittää kokoonpanon tuotoksen myyntitilausriviin toimitustoiminnon kautta, joka täyttää asiakkaan tilauksen.  

 Määrittelemättömän tarjonnan tai kysynnän osalta suunnittelujärjestelmä määrittelee automaattisesti varauksen tilan tyypiksi **Ylijäämä**. Syy voi olla kysyntä, joka aiheutuu ennustemääristä tai käyttäjän syöttämistä suunnitteluparametreista. Tämä on järjestelmän tunnistama sallittu ylijäämä, eikä järjestelmä lähetä toimenpideviestejä. Ylijäämä voi olla myös aito, ylittää tarjonnan tai kysynnän, joka jää seuraamatta. Tämä kertoo tilausverkon epätasapainosta. Epätasapainon vuoksi järjestelmä antaa toimenpideviestejä. Huomaa, että toimenpideviesti, joka ehdottaa määrän muutosta viittaa aina tyyppiin **Ylijäämä**. Katso lisätietoja tämän ohjeaiheen "Esimerkki: tilauksen seuranta myynnissä, tuotannossa ja siirroissa" -osiosta.  

 Automaattiset varaukset, jotka luodaan suunnitteluajon aikana käsitellään seuraavilla tavoilla:  

-   Ne kohdistetaan saatavuuden laskennan osana oleviin nimikemääriin, kuten manuaalisiin varauksiin. Lisätietoja on tämän aiheen "Kompensoiminen varauksissa" -osassa.  

-   Nämä sisältyvät peräkkäisiin suunnitteluajoihin ja niitä voidaan muuttaa toisin kuin manuaalisesti varattuja nimikkeitä.  

## <a name="order-tracking" />Tilauksen seuranta
 Tilauksen seuranta auttaa suunnittelijaa säilyttämään kelvollisen toimitussuunnitelman esittämällä yleiskuvan kysynnän ja tarjonnan siirtymästä tilausverkossa. Tilauksenseurantatietueet palvelevat pohjana, jolle luodaan dynaamiset toimintaviestit ja suunnitteluriviehdotukset suunnitteluajojen aikana.  

> [!NOTE]  
>  Tilauksenseurantajärjestelmä hyvittää käytettävissä olevan varaston, kun tilaukset on kirjattu tilausverkostoon. Tämä tarkoittaa sitä, että järjestelmä ei priorisoi mahdollisesti kiireellisempiä tilauksia niiden eräpäivän perusteella. Näin ollen näiden prioriteettien uudelleen järjestäminen on suunnittelujärjestelmän logiikan tai suunnittelijan vastuulla.  

> [!NOTE]  
>  Tilauksen seuraamisen tapaa ja Hae toimenpideviestit -funktiota ei ole integroitu töiden kanssa. Tämä tarkoittaa sitä, että työhön liittyvää kysyntää ei jäljitetä automaattiseseti. Koska sitä ei seurata, se voi aiheuttaa olemassa olevan täydennystilauksen ja työtietojen seurannan käytön toiseen kysyntään, esimerkiksi myyntitilaukseen. Saatat kohdata tilanteen, jossa käytettävissä olevia varastotietoja ei ole synkronoitu.  

### <a name="the-order-network" />Tilausverkosto
 Tilauksenseurantajärjestelmä perustuu periaatteeseen, jossa tilausverkoston tulee aina olla balanssissa, ja jossa jokainen kysyntä, joka kirjataan järjestelmään, kompensoidaan vastaavalla tarjonnalla ja päinvastoin. Järjestelmä tekee tämän tunnistamalla tilausverkon kysyntä- ja tarjontatapahtumien väliset loogiset linkit.  

 Tämä periaate osoittaa, että kysynnän muutos johtaa vastaavan epätasapainon syntymiseen tilausverkon tarjontapuolella. Käänteisesti, tarjonnan muutos johtaa vastaavan epätasapainon syntymiseen tilausverkon kysyntäpuolella. Todellisuudessa tilausverkossa on jatkuvassa muutostilassa, kun käyttäjät kirjoittavat, muuttavat ja poistavat tilauksia. Tilauksen seuranta käsittelee tilaukset dynaamisesti ja reagoi jokaiseen muutokseen sillä hetkellä, kun se siirtyy järjestelmään ja muuttuu osaksi tilausverkkoa. Heti kun uudet tilauksen seurantatietueet luodaan, tilausverkko on tasapainossa, mutta ainoastaan seuraavaan muutokseen asti.  

 Suunnittelujärjestelmän laskentojen läpinäkyvyyttä nostaa ei-seurattujen määrien näkyminen **Ei-seuratut suunnitteluelementit** -sivulla. Arvo osoittaa tunnetun kysynnän ja ehdotetun tarjonnan välisen määrän eron. Jokainen sivun rivi viittaa ylittävän määrän syyhyn, kuten **Puitetilaus**, **Varaston turvataso**, **Kiinteä uusintatilausmäärä**, **Vähimmäistilausmäärä**, **Pyöristys** tai **Puskuriaika**.  

### <a name="offsetting-in-order-tracking" />Kompensoiminen tilausten seurannassa
 Toisin kuin varaukset, jotka voidaan tehdä vain käytettävissä olevien nimikkeiden määrän kohdalla, nimikkeen seuranta on mahdollista kaikkien tilausverkon yksiköiden kohdalla, jotka ovat osa suunnittelujärjestelmän nettotarpeiden laskentaa. Verkkovaatimukset lasketaan seuraavasti:  

 nettotarpeet = bruttotarpeet + uusintatilauspiste - aikataulutetut vastaanotot - suunnitellut vastaanotot - oletettu saatavilla oleva saldo  

> [!NOTE]  
>  Kysyntää, joka liittyy ennusteisiin tai suunnitteluparametreihin, ei seurata.  

### <a name="example-order-tracking-in-sales-production-and-transfers" />Esimerkki: tilauksen seuranta myynnissä, tuotannossa ja siirroissa
 Seuraavassa skenaariossa esitetään mitkä tilauksenseurantakirjaukset luodaan **Varauskirjaus**-taulukossa tuloksena useista tilausverkoston muutoksista.  

 Oletetaan, että seuraavat tiedot koskevat kahta nimikettä, joille asetetaan tilauksen seuranta.  

|Nimike 1|Name|"Komponentti"|
|-|-|-|
||Saatavuus|100 yksikköä, LÄNSI sijainti<br /><br />- 30 yksikköä LOTA-erää<br />- 70 yksikköä LOTB-erää|  
|Nimike 2|Name|"Tuotettu nimike"|
||Tuotannon tuoterakenne|1 määrä komponenttia kohti|  
||Kysyntä|100 yksikön myynti sijainnissa EAST|  
||Tarjonta|Julkaistu tuotantotilaus (luotu **Myyntitilauksen suunnittelu** -toiminnon avulla 100 yksikön myyntiä varten)|  

**Tuotannon asetukset** -sivun **Komponentit sijainnissa** -kentän arvoksi on määritetty **PUNAINEN**.

 Seuraavat tilauksenseurantakirjaukset ovat olemassa **Varauskirjaus** -taulukossa, joka perustuu taulukon tietoihin.  

 ![Ensimmäinen esimerkki: Varaustapahtumataulukon tilausten seurantatapahtumat.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  

### <a name="entry-numbers-8-and-9" />Tapahtumanumerot 8 ja 9
 Vastaavasti LOTA:n ja LOTB:n komponenttitarpeen osalta seurantalinkit luodaan taulukon 5407, **Tuotantotilauksen komponentti** kysynnästä tarjontaan taulukossa 32, **Nimiketapahtuma**. **Varauksen tila** -kenttä sisältää **Seurannan**, joka ilmaisee, että nämä kirjaukset ovat dynaamisen tilaustenseurannan linkkejä kysynnän ja tarjonnan välillä.  

> [!NOTE]  
>  **Eränro**-kenttä on tyhjä kysyntäriveillä, koska eränumeroita ei ole määritetty julkaistun tuotantotilauksen osariveillä.  

### <a name="entry-numbers-10" />Tapahtumanumerot 10
 Myynnin kysynnästä taulukossa 37, **Myyntirivi** luodaan tilausseurantalinkki tarjontaan taulukossa 5406, **Tuot. til. rivi**. **Varauksen tila** -kenttä sisältää **Varauksen** ja **Sitova**-kenttä sisältää **Tilauksesta tilaukseen**. Tämä johtuu siitä, että vapautettu tuotantotilaus luotiin erityisesti myyntitilausta varten. Sen linkitys on säilytettävä, toisin kuin tilauksen seurantalinkit, joiden varauksen tila on **Seuranta**. Nämä linkit luodaan dynaamisesti ja niitä myös muokataan dynaamisesti. Lisätietoja on tämän aiheen "Automaattiset varaukset" -osassa.  

 Tässä skenaarion vaiheessa 100 yksikköä LOTA- ja LOTB-kohteita siirretään ITÄ-sijaintiin siirtotilauksella.  

> [!NOTE]  
>  Vain siirtotilauksen toimitus kirjataan tässä vaiheessa, ei vastaanottoa.  

 Nyt **Varaustapahtuma**-taulukossa on seuraavat tilauksen seurantatapahtumat.  

 ![Toinen esimerkki: Varaustapahtumataulukon tilausten seurantatapahtumat.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  

### <a name="entry-numbers-8-and-9" />Tapahtumanumerot 8 ja 9
 Komponentin kahden erän tilauksen seurantatapahtumia, jotka kuvaavat kysyntää taulukossa 5407, muutetaan **Seuranta**-varaustilasta arvoon **Ylijäämää**. Syy on se, että siirtotilauksen lähetykseen on käytetty tarjontoja, joihin ne oli linkitetty ennen, taulukossa 32.  

 Aito ylijäämä, kuten tässä tapauksessa, kuvastaa ylimääräistä tarjontaa tai kysyntää, jota ei seurata. Se on osoitus epätasapainosta tilausverkossa, ja suunnittelujärjestelmä luo toimenpideviestin ellei sitä ratkaista dynaamisesti.  

### <a name="entry-numbers-12-to-16" />Tapahtumanumerot 12-16
 Koska komponentin kaksi lokeroa kirjataan siirtotilaukseen toimitetuiksi mutta ei vastaanotetuiksi, kaikki liittyvät positiiviset seurantatapahtumat ovat varaustyyppiä **Ylijäämä**, joka tarkoittaa, että niitä ei kohdisteta mihinkään pyyntöihin. Jokaisen eränumeron osalta yksi merkintä liittyy taulukkoon 5741, **Siirtorivi** ja yksi merkintä liittyy nimiketapahtumaan kuljetuksessa-sijainnissa, jossa nimikkeet ovat tällä hetkellä.  

 Tässä skenaarion vaiheessa LÄNSI- ja ITÄ-sijainnin komponenttien siirtotilaus kirjataan vastaanotetuksi.  

 Nyt **Varaustapahtuma**-taulukossa on seuraavat tilauksen seurantatapahtumat.  

 ![Kolmas esimerkki: Varaustapahtumataulukon tilausten seurantatapahtumat.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3")  

 Tilauksenseurantakirjaukset ovat nyt yhteneväisiä skenaarion ensimmäisen kohdan kanssa, ennen kuin siirtotilaus tiliöitiin ja lähetettiin, lukuun ottamatta sitä, että osakirjaukset ovat nyt varaustilaltaan **Surplus**. Tämä johtuu siitä, että komponentti on yhä LÄNSI-sijainnissa. Se tarkoittaa sitä, että tuotantotilauksen komponenttirivin **Sijaintikoodi**-kenttä sisältää **LÄNSI**-merkinnän **Komponentit sijainnissa** -asetuskentän asetuksissa. Tarjonta kohdistettiin tälle kysynnälle ennen ITÄ-sijaintiin siirtoa, joten sen täysi seuranta on mahdollista, ellei tuotantotilausrivin komponenttitarvetta muuteta ITÄ-sijainnissa.  

 Tässä skenaarion vaiheessa tuotantotilausrivin **Sijaintikoodi** asetetaan arvoon **ITÄ**. Lisäksi **Nimikkeen seurantarivit**-sivulla 30 yksikköä LOTA-erästä ja 70 yksikköä LOTB-erästä kohdistetaan tuotantotilausriville.  

 Nyt **Varaustapahtuma**-taulukossa on seuraavat tilauksen seurantatapahtumat.  

 ![Neljäs esimerkki: Varaustapahtumataulukon tilausten seurantatapahtumat.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")  

### <a name="entry-numbers-21-and-22" />Tapahtumanumeroita 21 ja 22
 Koska osa pitää vaihtaa sijaintiin EAST ja tarjonta on käytettävissä nimikkeen pääkirjan kirjauksina sijainnissa EAST, kaikkia tilausseurantakirjauksia, jotka kohdistuvat kahteen eränumeroon, seurataan koko ajan ja ne ilmaistaan varaustilassa **Seuranta**.  

 **Eränro**-kenttä on nyt täytetty tilauksen seurantakirjauksessa taulukossa 5407, koska eränumerot on määritetty tuotantotilauksen osariveillä.  

 Lisää **Varaustapahtuma**-taulukon tilausten seurantatapahtumien esimerkkejä on Varaustapahtumataulukko-raportissa sivustossa [Partnersource](https://go.microsoft.com/fwlink/?LinkId=258348) (edellyttää kirjautumista).

## <a name="action-messaging" />Toimenpiteiden viestitys
 Kun tilausten seurantajärjestelmä havaitsee epätasapainotilan tilausverkossa, se luo automaattisesti toimenpideviestin käyttäjälle. Toimenpideviestit ovat järjestelmän luomia kutsuja käyttäjälle, jotka määrittävät epätasapainon tiedot ja ehdotukset tasapainon palauttamisesta tilausverkkoon. Ne näkyvät suunnitteluriveinä **Suunnittelutyökirja**-sivulla, kun valitset **Hae toimenpideviestit**. Lisäksi toimenpideviestit näytetään niillä suunnitteluriveillä, jotka on luotu suunnitteluajon aikana vastaamaan suunnittelujärjestelmän ehdotuksia tasapainon palauttamiseksi tilausverkkoon. Molemmissa tapauksissa ehdotukset suoritetaan tilausverkossa, kun valitset **Toteuta toimenpideviesti**.  

 Toimenpideviesti käsittelee yhden tuoterakenteen tason kerralla. Jos käyttäjä hyväksyy toimenpideviestin, tämä voi synnyttää lisätoimenpideviestejä seuraavalla tuoterakennetasolla.  

 Seuraavassa taulukossa esitellään olemassa olevat toimintaviestit.  

|Toimenpidesanoma|Description|  
|--------------------|---------------------------------------|  
|**Muuta määrä**|Muuttaa olemassa olevan toimitustilauksen määrän kattamaan muuttunutta tai uutta kysyntää.|  
|**Aikataul. uud.**|Aikatauluttaa olemassa olevan tilauksen eräpäivän.|  
|**Aikataul. uud. & Muuta määrä**|Aikatauluttaa määräpäivän uudelleen ja muuttaa olemassa olevan tilauksen määrää.|  
|**Uusi**|Luo uuden tilauksen, jos kysyntä ei ole täytettävissä kummallakaan aiemmalla toimenpideviestillä.|  
|**Peruuta**|Peruuttaa olemassa olevan tilauksen.|  

 Tilauksenseurantajärjestelmä yrittää aina ratkaista epätasapainon olemassa olevassa tilausverkostossa. Jos tämä ei ole mahdollista, järjestelmä antaa toimenpideviestin uuden tilauksen luomisesta. Seuraava on tilausten seurantajärjestelmän käyttämä prioriteetin mukaan järjestetty luettelo, jota käytetään täsmäytyksen palauttamiseen. Jos tilausverkkoon on siirtynyt lisäkysyntää, järjestelmä pyrkii tilaamaan seuraavien tarkistusten kautta:  

1.  Tarkista tämän kysynnän ylimääräinen tarjonta olemassa olevassa seurantatietueessa.  
2.  Tarkista suunnitellut ja aikataulutetut vastaanotot vastaanottopäivämääräjärjestyksessä. Viimeisin mahdollinen päivämäärä on valittu.  
3.  Tarkista käytettävissä oleva varasto.  
4.  Tarkista, onko toimitustilausta olemassa nykyisen tilauksen seurantatietueessa. Jos näin on, järjestelmä antaa **Muuta**-toimenpideviestintilauksen kasvattamiseksi.  
5.  Tarkista, että nykyisen tilauksen seurantatietueessa ei ole toimitustilausta. Jos näin on, järjestelmä antaa **Uusi**-toimenpideviestin uuden tilauksen luomiseksi.  

 Avaa kysyntä kulkee luettelon läpi ja siirtää käytettävissä olevaa tarjontaa jokaisessa kohdassa. Kaikki jäljellä oleva kysyntä täytetään aina tarkastuksessa 4 tai tarkastuksessa 5.  

 Jos kysynnän määrä vähenee, tilausten seurantajärjestelmä yrittää ratkaista epätasapainon suorittamalla aiemmat tarkastukset käänteisessä järjestyksessä. Tämä tarkoittaa sitä, että olemassa olevia toimenpideviestejä voi muokata ja tarvittaessa ne voi poistaa. Tilauksenseurantajärjestelmä esittää aina nettotuloksen laskelmista käyttäjälle.  

## <a name="order-tracking-and-planning" />Tilauksen seuranta ja suunnittelu
 Kun suunnittelujärjestelmä toimii, se poistaa kaikki olemassa olevat tilauksen seurantatietueet ja toimenpideviestitapahtumat ja luo ne uudelleen suunnittelurivin ehdotuksina tarjonta/kysyntä-parien ja prioriteettien mukaan. Kun suunnittelu on valmis, tilausverkko on tasapainossa.  

### <a name="planning-system-versus-order-tracking-and-action-messaging" />Suunnittelujärjestelmä verrattuna tilauksen seurantaan ja toimenpideviesteihin
 Seuraava vertailu osoittaa erot menetelmien välillä, joita suunnittelujärjestelmä käyttää luodessaan suunnittelurivin ehdotuksia ja menetelmiä, joita tilauksenseurantajärjestelmä käyttää luodakseen tilauksenseurantatietueet ja toimintaviestit.  

-   Suunnittelujärjestelmä käsittelee tietyn nimikkeen koko kysyntä- ja tarjontamallin, kun taas tilauksenseuranta käsittelee tilausta, joka on aktivoinut sen.  

-   Suunnittelujärjestelmä käsittelee kaikkia BOM-hierarkian tasoja, kun taas tilauksenseuranta käsittelee yhden BOM-tason kerrallaan.  

-   Suunnittelujärjestelmä muodostaa linkkejä kysynnän ja tarjonnan välille etusijalle asetetun eräpäivän mukaisesti. Tilauksen seuranta muodostaa linkit kysynnän ja tarjonnan välille tilaustapahtumien järjestyksen perusteella.  

-   Suunnittelujärjestelmä ottaa suunnitteluparametrit huomioon, kun taas tilauksenseuranta ei ota.  

-   Suunnittelujärjestelmä luo linkit käyttäjän aktivoimassa erätilassa, kun se tasapainottaa kysyntää ja tarjontaa, kun taas tilaustenseuranta luo linkit automaattisesti ja dynaamisesti, kun käyttäjä syöttää tilaukset.  

## <a name="see-also" />Katso myös
[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
