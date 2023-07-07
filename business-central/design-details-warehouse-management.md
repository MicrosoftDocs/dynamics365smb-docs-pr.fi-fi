---
title: Fyysisen varaston aktiviteetit
description: Vastaanottojen ja toimitusten lisäksi Business Central tukee sisäisiä varastotoimintoja.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/05/2022
ms.custom: bap-template
---

# <a name="warehouse-management-overview"></a>Varastohallinnan yleiskuvaus

Fyysiseen varastoon tavaroita sisään ja ulos siirtäville yrityksille seuraavat kaksi asiaa ovat tärkeitä:

* Varastomääristä ja nimikkeen paikasta varastossa oltava yleiskuva.
* Nimikkeitä voidaan vastaanottaa, poimia ja toimittaa nopeasti ja tarkasti.

[!INCLUDE[prod_short](includes/prod_short.md)]in varastotoimintoiin on lisätty seuraavat varastonhallinnan ominaisuudet, joiden avulla edellä mainitut seikat ovat mahdollisia yrityksille:

* Varastopaikat
* Fyysisen varaston toimitukset
* Varaston poiminnat
* Siirtotyökirja

Liiketoimintaan sopivia varastointiprosesseja voidaan räätälöidä toteuttamalla näitä ominaisuuksia erilaisina yhdistelmiä. Yrityksen kasvaessa ja prosessien muuttuessa myös monimutkaisuus lisääntyy, mikä kannattaa ottaa huomioon jo alkuvaiheessa.

## <a name="overview-of-different-configuration-options"></a>Erilaisten määritysvaihtoehtojen yleiskatsaus

Fyysisen varaston ominaisuuksia voidaan määrittää eri tavoin. On tärkeää, valita vaihtoehdot, jotka parantavat prosesseja yleiskustannuksia lisäämättä. Seuraavassa taulukossa on yleiskuva määrityksistä, joita käytetään yleisesti fyysisten tavaroiden käsittelyssä.

|Monimutkaisuustaso|Kuvaus|Asetukset|Varastopaikan koodi|Esimerkki saapuvasta virrasta|Esimerkki lähtevästä virrasta|Esimerkki sisäisestä virrasta|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ei määritettyä fyysisen varaston toimintaa.|Kirjaaminen tilauksista ja päiväkirjoista.||Valinnainen. Hallitaan **Varastopaikka on pakollinen** -vaihtopainikkeella.|Ostotilaus|Myyntitilaus| Tuotantotilaus -> kulutuspäiväkirja|  
|Perus|Useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus|**Vaadi vastaanotto**<br>**Vaadi toimitus**|Valinnainen. Hallitaan Varastopaikka on pakollinen -vaihtopainikkeella|Ostotilaukset -> fyysisen varastoinnin vastaanotto|Myyntitilaus -> Fyysisen varaston toimitus|Sama kuin edellä.|
|Perus|Tilauksittain.|Vaadi hyllytys tai vaadi poiminta </br><br/> **Huomautus**: vaikka asetusten nimenä on **Vaadi poiminta** ja **Vaadi hyllytys**, vastaanottoja ja toimituksia voidaan silti kirjata suoraan lähdeasiakirjoista sijainneissa, joissa nämä valintaruudut on valittu.|Valinnainen. Hallitaan **Varastopaikka on pakollinen** -vaihtopainikkeella.|Ostotilaukset -> varaston hyllytys|Myyntitilaus -> varaston poiminta|Tuotantotilaus -> Varaston poiminta|
|Lisäasetukset|Useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus<br /><br />Useiden lähdeasiakirjojen konsolidoidut poiminta- ja hyllytystoiminnot.|Vaadi vastaanotto + vaadi hyllytys,</br> Vaadi toimitus + vaadi poiminta|Valinnainen. Hallitaan Varastopaikka on pakollinen -vaihtopainikkeella|Ostotilaukset -> fyysisen varastoinnin vastaanotto -> fyysisen varastoinnin hyllytys|Myyntitilaukset -> fyysisen varastoinnin toimitukset -> poimintatyökirja -> fyysisen varastoinnin poiminnat| Tuotantotilaus -> poimintatyökirja -> fyysisen varastoinnin poiminnat -> kulutuspäiväkirja|
|Lisäasetukset|Sama kuin edellä + ohjatut poiminta- ja hyllytystoiminnot|Ohjattu poiminta ja hyllytys (kyseiset vaihtopainikkeet otetaan käyttöön automaattisesti)|Pakollinen|Sama kuin edellä.|Sama kuin edellä.| Tuotantotilaus -> poimintatyökirja -> fyysisen varastoinnin poiminnat -> kulutuspäiväkirja|

Monimutkaisuus lisääntyy organisaation koon ja mukana olevien osastojen ja henkilöiden määrän mukaan. Prosessi voi olla yksinkertainen, kuten silloin kun sama henkilö luo ja kirjaa myyntiasiakirjan. Prosessi voi olla myös tätä monimutkaisempi, jolloin siinä voi olla mukana useita vaiheita ja henkilöitä. Seuraavat vaiheet ovat esimerkki monimutkaisesta prosessista:

1. Tilausten käsittelijä luo myyntitilauksen.
1. Varastopäällikkö luo poimintaohjeet.
1. Varastotyöntekijä päättää työnkulun kirjaamalla fyysisen varaston toimituksen.

Monimutkaisuuden taso vaikuttaa myös varastointitoiminnoissa käytettävien asiakirjojen tyyppiin. Esimerkiksi saapuvassa virrassa voidaan käyttää fyysisen varastoinnin vastaanoton ja hyllytyksen asiakirjoja mutta lähtevässä virrassa käytetään varaston hyllytyksen asiakirjoja.

Toinen monimutkaisuuteen vaikuttava tekijä on tapa, jolla fyysinen varasto ilmaistaan [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Fyysisen varaston mallinnus](#modeling-the-physical-warehouse).

## <a name="modeling-the-physical-warehouse"></a>Fyysisen varaston mallinnus

Varaston fyysistä todellisuutta vastaavat määritykset voidaan ilmaista eri tavoin [!INCLUDE[prod_short](includes/prod_short.md)]issa. Valinnat määrittävät, miten fyysisen varaston ominaisuuksia käytetään.

Nimikkeet voidaan sijoittaa hyllyille, sijainteihin tai varastopaikkoihin, ja kullakin vaihtoehdolla on omat hyvät ja huonot puolensa.

### <a name="locations-and-bins"></a>Sijainnit ja varastopaikat

Fyysisten tavaroiden käsittelyä varten tarvitaan ainakin yksi sijainti. Fyysisen varaston ja organisaation rakenteen mallintamiseen voi käyttää useita sijainteja tai varastopaikkoja.

Sijaintien käyttöä suositaan yleensä eri maantieteellisille alueille jaettujen toimintojen järjestämisessä. Joissakin tapauksissa halutaan kuitenkin ehkä luoda useita samassa paikassa sijaitsevia sijainteja. Sijaintien käytön hyvät puolet:

* Käyttöoikeus myönnetään **Varastotyöntekijä**- ja **Vastuupaikat**-sivuilla.
* Päivämäärän laskentaa ja suunnittelua varten määritetään kalenterit, reitit sekä saapuvien ja lähtevien käsittelyajat. Lisätietoja: [Tietoja toimintojen suunnittelusta](production-about-planning-functionality.md).
* Oletusdimensioiden määrittäminen ja erilaisten varastokirjauksien asetusten käyttäminen.
* Suunnittelun parametrien määrittäminen. Lisätietoja on kohdassa [Suunnitteluparametrit](production-about-planning-functionality.md#planning-parameters).  
* Erilaisten fyysisen varaston ominaisuuksien käyttäminen kussakin sijainnissa.

### <a name="shelves-and-bins"></a>Hyllyt ja varastopaikat

Jos nimike varastoidaan aina samassa paikassa, käytössä on **Hyllynro**-kenttä **Nimikekortti**- tai **Varastointiyksikkökortti**-sivulla. Tätä kenttä voi olla manuaalisena perusvarastointijärjestelmä ympäristöissä, joissa ei ole varastopaikkoja. Sen arvo kopioidaan nimikekortista asiakirjariveille ja raportteihin, mutta se on tarkoitettu vain tiedoksi. Arvoa käytetä fyysisen varastoinnin aktiviteeteissa eikä saatavuuslaskennassa.

Varastopaikat ilmaisevat fyysisen varastoinnin perusrakenteen, ja niitä käytetään tekemään nimikkeiden sijoitteluehdotuksia:

* Nimikkeellä vähintään yksi kiinteä varastopaikka.
* Toimintokohtaiset varastopaikat, kuten toimituksen varastopaikka tai tuotannon tuloksen varastopaikka.
* Varastopaikan kapasiteetti- ja painorajoitukset (vain ohjatussa hyllytyksessä ja poiminnassa).
* Varastopaikkaluokitus (vain ohjatussa hyllytyksessä ja poiminnassa).

## <a name="typical-warehouse-workflow"></a>Tyypillinen fyysisen varastoinnin työnkulku

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Jos kyse on tilauskohtaisesta perustyönkulusta, varaston hyllytystä voi käyttää nimikkeiden vastaanoton, myös ylittävän määrän, kirjaamiseen sijainnissa. Fyysisen varastoinnin vastaanottoa käytetään, jos vastaanotossa konsolidoidaan useita tilauksia.|[Saapuva virta](design-details-inbound-warehouse-flow.md)|
|Fyysistä varastosijainneista toimitettujen nimikkeiden kirjaaminen. Tilauskohtaisesti käytetään varaston poimintaa. Fyysisen varastoinnin toimitusta käytetään, jos toimituksessa konsolidoidaan useita tilauksia.|[Lähtevä virta](design-details-outbound-warehouse-flow.md)|
|Nimikkeiden käsitteleminen fyysisessä varastosijainnissa. Kyse voi olla esimerkiksi komponenttien siirtämisestä tuotantoon tai inventointi.|[Sisäinen virta](design-details-internal-warehouse-flows.md)|

Fyysiset varastointiprosessit määritetään liiketoiminnan tarpeiden mukaan. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).

## <a name="terminology-related-to-warehouse-management"></a>Varastoinninhallintaan liittyvät termit

### <a name="complexity-levels"></a>Monimutkaisuustasot

Monimutkaisuustasot erotetaan toisistaan termien perustaso ja laajennettu avulla. Tämä yksinkertainen erottelu kattaa useita sijaintimääritysten monimutkaisuustasoja, joista kutakin erilaiset fyysisen varastoinnin asiakirjat tukevat. Varastoinnin laajinta tasoa kutsutaan ohjatuksi hyllytykseksi ja poiminnaksi. Ohjattu hyllytys ja poiminta otetaan sijainnissa käyttöön **Sijaintikortti**-sivun **ohjattu hyllytys ja poiminta** -vaihtopainikkeella.

### <a name="warehouse-flows"></a>Fyysiset varastointivirrat

* Saapuva virta – Nimikkeiden siirtäminen fyysiseen varastosijaintiin ja niiden tuominen saataville. Esimerkki: ostot ja saapuvat siirrot.
* Lähtevä virta – nimikkeiden poimiminen ja toimittaminen asiakkaille tai muihin sijainteihin.
* Sisäinen virta – Nimikkeiden käsittely sijainnissa. Esimerkki: komponenttien siirtäminen tuotantoon tai inventointi.

### <a name="basic-documents"></a>Perusasiakirjat

Seuraavia asiakirjoja käytetään fyysisen varaston perustyönkuluissa.

* Varastohyllytys
* Varaston poiminta
* Varaston siirto
* Nimikepäiväkirja
* Nimikkeen uudelleenluokituspäiväkirja

### <a name="advanced-documents"></a>Laajennettujen toimintojen asiakirjat

Seuraavia asiakirjoja käytetään fyysisen varaston laajennetuissa työnkuluissa.

* F. varastoinnin vastaanotto
* Hyllytystyökirja
* F.varastoinnin hyllytys
* Poimintatyökirja
* F.varastoinnin poiminta
* Siirtotyökirja
* F. var. siirto
* Fyysisen varaston sisäinen poiminta
* Fyysisen varaston sisäinen hyllytys
* Var.paikan luontityökirja
* Var.p. sisällön luontityökirja
* Fyysisen varaston nimikepäiväkirja
* Fyysisen varaston nimikkeen uudelleenluokituspäiväkirja

### <a name="pages-and-settings"></a>Sivut ja asetukset

Tässä osassa käsitellään käsitteitä, joihin varastoinnin keskeiset sivut ja asetukset perustuvat.

#### <a name="bins-and-bin-content"></a>Varastopaikat ja varastopaikan sisältö

Lokero on tallennuslaite, jonka tarkoituksena on tallentaa erilliset osat. Se on [!INCLUDE[prod_short](includes/prod_short.md)]in pienin varastoyksikkö. Varastopaikkojen nimikemääriä kutsutaan *varastopaikan sisällöksi*. **Nimike**- tai **Lokerokoodi**-kentästä suoritettu haku missä tahansa fyysiseen varastoon liittyvässä asiakirjassa näyttää lokerossa olevan nimikkeen lasketun saatavuuden.  

Varastopaikan sisällön määritteenä voi olla **Kiinteä**, **Erityinen** tai **Oletus**, ja se määrittää, miten varastopaikan sisältöä voidaan käyttää. Jos varastopaikalla ei ole mitään edellisistä ominaisuuksista, sitä kutsutaan *määrittelemättömiksi* varastopaikaksi.  

Kiinteä varastopaikka sisältää varastopaikkakoodiin määritettyjä nimikkeitä: Kiinteä varastopaikkaominaisuus varmistaa, että varastonpaikan sisältö ei häviä, vaikka varastopaikka tyhjenisi. Varastopaikka valitaan uudelleen heti, kun sen sisältö täydennetään.  

Erityisvarastopaikka sisältää varastopaikan sisällön, joka voidaan poimia vain varastopaikkaa käyttävälle erityiselle resurssille. Sellainen on esimerkiksi kuormitusryhmä. Muuta ei poimittua sisältöä, kuten lähteviä määriä toimituksen kirjauksessa, voidaan kuluttaa erityisvarastopaikasta. Vain **Luo poiminta**-algoritmin huomioima varastopaikan sisältö on suojattu erityisvarastopaikassa.  

[!INCLUDE [prod_short](includes/prod_short.md)] käyttää varastopaikan **Oletus**-ominaisuutta fyysisten varastotoimintojen ehdottamiseen. Ohjattua hyllytystä ja poimintaa käyttävissä sijainneissa ei käytetä varastopaikan oletusominaisuutta. Jos varastopaikat ovat pakollisia sijainneissa, ominaisuus määrittää, mihin saapuvien virran nimikkeet sijoitetaan. Lähtevissä virroissa ominaisuus määrittää, mistä nimikkeet otetaan.  

> [!NOTE]  
> Jos lähtevät nimikkeet sijoitetaan useisiin varastopaikkoihin, nimikkeet otetaan ensin ei oletusarvoisista varastopaikoista, jolloin varastopaikan sisältö tyhjenee, ja jäljellä olevat nimikkeet otetaan sitten oletusvarastopaikasta.  

Kullakin nimikkeellä voi olla sijainnissa yksi oletusvarastopaikka.  

#### <a name="bin-type"></a>Varastopaikan tyyppi

Ohjattua hyllytystä ja poimintaa käyttävissä sijainneissa voidaan käyttää varastopaikkatyyppejä. Varastopaikkatyyppien avulla hallitaan varastopaikassa sallittuja toimintoja. Saatavana olevat varastopaikkojen tyypit:  

|Varastopaikan tyyppi|Kuvaus|  
|------------------|---------------------------------------|  
|VAST.OTTO|Nimikkeet, jotka on vastaanotettu mutta joita ei ole hyllytetty.|  
|LÄHETYS|Nimikkeet, jotka on poimittu fyysisen varastoinnin toimitusriveille mutta joita ei ole kirjattu toimitetuiksi.|  
|HYLLYTYS|Yleensä suurina mittayksiköinä varastoidut nimikkeet, joita ei haluta käyttää poimintatarkoituksiin. Näitä varastopaikkoja ei käytetä tuotantotilausten eikä toimitusten poimintaa, joten niiden käyttö voi olla rajallista. Tämä varastopaikkatyyppi on kätevä ostettaessa suuria määriä nimikkeitä. Varastopaikkojen luokituksen on oltava aina alhainen, jotta luokitukseltaan korkeammat HYLLPOIM-varastopaikat hyllytetään ensin. Tämä varastopaikkatyyppi on täydennettävä säännöllisesti, jotta niiden nimikkeet ovat saatavana HYLLPOIM- tai POIMINTA-tyyppisissä varastopaikoissa.|  
|POIMINTA|Vain poimintaan käytettävät nimikkeet. Näiden varastopaikkojen täydentämiseen voi käyttää vain varastosiirtoja, ei siis hyllytyksiä.|  
|HYLLPOIM|Nimikkeet varastopaikoissa, joille on ehdotettu sekä hyllytyksiä että poimintoja. Tämän tyyppisillä varastopaikoilla on todennäköisesti eri varastopaikan luokitteluja. Irtotavaran varastopaikoille määritetään matalampi varastopaikan luokittelu kuin tavallisiin poimintavarastopaikoille tai edelleen poimimisen alueiden varastopaikoille.|  
|QC|Tätä varastopaikkaa käytetään varastomuutoksille, jos varastopaikka määritetään sijaintikortissa **Muutosvarastopaikan koodi** -kentässä. Tämän tyyppisiä varastopaikkoja voi määrittää myös viallisille nimikkeille ja tarkastettaville nimikkeille. Nimikkeitä voi siirtää tämän tyyppiseen varastopaikkaan, jos haluat, että ne eivät ole saatavilla tavallisessa nimikevirrassa. **Huomautus:** Toisin kuin kaikki muut varastopaikkatyypit, **QC**-varastopaikkatyypin nimikkeen käsittelyn valintaruutuja ei ole oletusarvoisesti valittu. että QC-varastopaikkaan asetettu sisältö jätetään pois nimikevirroista.|  

POIMINTA-, HYLLPOIM- ja HYLLYTYS-varastopaikkatyyppejä lukuun ottamatta varastopaikan tyyppi määrittää varastopaikassa sallitun toiminnan. Esimerkiksi VASTAANOTTO-tyypin varastopaikkaa voidaan käyttää vain nimikkeiden vastaanottamiseksi tai nimikkeiden poimintaan.  

> [!NOTE]  
> Nimikkeiden siirtoon VASTAANOTTO- ja QC-varastopaikkoihin on käytettävä varastosiirtoja. Nimikkeet siirretään LÄHETYS- ja QC-varastopaikoista varastosiirtojen avulla.  

#### <a name="bin-ranking"></a>Varastopaikan luokittelu

Laajennetussa varastoinnissa nimikkeiden kerääminen voidaan automatisoida ja optimoida hyllytys- ja poimintatyökirjoissa varastopaikkojen luokittelun avulla. Nimikkeitä ehdotetaan poimittavaksi tai hyllytettäväksi varastopaikan luokittelun perusteella.

Hyllytysprosessit on optimoitu varastopaikan luokittelun mukaan ehdottamalla korkeamman luokan varastopaikkoja ennen alemman luokan varastopaikkoja. Poimintaprosessit puolestaan ehdottavat ensimmäisenä varastopaikan sisällön korkeimman luokan nimikkeitä. Varastonpaikan täydennys ehdottaa alemman luokan varastopaikkoja ennen korkean luokan varastopaikkoja.  

Varastopaikan luokittelu ja varastopaikan sisältö perustuvat perusominaisuuksiin, jotka ohjaavat fyysisen varaston varastotyöntekijöitä.  

#### <a name="bin-setup"></a>Varastopaikan asetus

Laajennetussa varastoinnissa seuraavat kapasiteettiarvot määrittämällä voidaan hallita miten ja mihin varastopaikkoihin nimikkeet varastoidaan:

* määrä
* Kokonaiskuutiotilavuus
* Paino  

Nimikkeille voidaan määrittää perusmittayksikkö. Perusmittayksikkö voi olla kappale, kuormalava, litra, gramma tai laatikko. Perusmittayksikön perusteella voidaan luoda myös suuria mittayksiköitä. Jos esimerkiksi kappale on perusmittayksikkö, kuormalava voi vastata 16 kappaletta.  

Jos nimikkeellä on useita mittayksiköitä, kunkin mittayksikön enimmäismäärä määritetään nimikekortissa. Jos nimikettä käsitellään kappaleina ja kuormalavoina, myös nimikkeen **Varastopaikan sisältö** -sivun **Enimmäismäärä**-kenttä on ilmoitettava kappaleina ja kuormalavoina. Muussa tapauksessa kyseisen varastopaikan sallittua määrää ei lasketa oikein.  

Ennen varastopaikan sisältörajoitusten määrittämistä on varmistettava, että nimikkeen mittayksikkö ja dimensiot on määritetty.  

> [!NOTE]  
> Useita mittayksiköitä voi käyttää vain ohjattua hyllytystä ja poimintaa käyttävissä sijainneissa. Kaikissa muissa määrityksissä varastopaikan sisältö voi olla vain perusmittayksikössä. Tapahtumissa, joissa mittayksikkö on suurempi kuin nimikkeen perusmittayksikkö, määrä muutetaan perusmittayksiköksi.  

#### <a name="zone"></a>Vyöhyke

Laajennetussa varastoinnissa varastopaikat voidaan ryhmitellä vyöhykkeisiin hallitsemaan sijaintien varastotoimintojen työnkulun ohjausta.  

Vyöhyke voi olla vastaanottava alue tai varastointivyöhyke, minkä lisäksi kullakin vyöhykkeellä voi olla yksi varastopaikka tai useita varastopaikkoja.  

Useimmat vyöhykkeelle määritetyt ominaisuudet määritetään vyöhykkeelle luoduille varastopaikoille.  

#### <a name="warehouse-class"></a>F. var. luokka

Laajennetussa varastoinnissa fyysisen varastoinnin luokkakoodit voidaan määrittää seuraaville entiteeteille: 

* Nimikkeet
* Varastopaikat
* Alueet

Fyysisen varastoinnin luokkien avulla hallitaan sitä, minne nimikkeet varastoidaan. Voit jakaa alueen useisiin fyysisen varastoinnin luokkiin. Nimikkeitä voidaan esimerkiksi varastoida vastaanottavan vyöhykkeen pakasteiden, vaarallisten tuotteiden tai muuhun luokkaan.

Fyysisen varastoinnin luokkia ja vastaanoton/toimituksen oletusvarastopaikkaa käytettäessä sopivat varastopaikat on valittava manuaalisesti fyysisen varastoinnin vastaanotto- ja toimitusriveillä.  

Saapuvissa virroissa luokkakoodi korostetaan vain saapuvilla riveillä, kun luokkakoodi ei vastaa vastaanoton oletusvarastopaikkaa. Jos oikeita oletusvarastopaikkoja ei määritetä, määrää ei voida vastaanottaa.  

#### <a name="location"></a>Sijainti

Sijainti on fyysinen rakenne tai paikka, jossa varastoa vastaanotetaan, varastoidaan ja toimitetaan. Sijainti voi olla fyysinen varasto, huoltoauto, esittelytila, laitos tai laitoksen alue. Varasto on usein järjestetty varastopaikkoihin ja vyöhykkeisiin.

#### <a name="first-expired-first-out"></a>FEFO (ensin vanhentunut ensimmäisenä ulos)

Jos **FEFO-poiminta**-valintaruutu valitaan **Sijaintikortti**-sivun **Varastopaikkojen periaatteet** -pikavälilehdessä, nimikeseuratut nimikkeet poimitaan sijainnissa niiden vanhenemispäivämäärän mukaan. Ensimmäisenä poimitaan nimikkeet, joissa on aikaisin erääntymispäivä.  

Kaikkien poiminta- ja siirtoasiakirjojen fyysisen varaston toiminnot on lajiteltu FEFO-menetelmän mukaan, ellei nimikkeille ole määritetty sarja- tai eränumeroa. Jos vain osalle rivin määrästä on määritetty erä- tai sarjanumerot, jäljellä oleva määrä lajitellaan FEFO:n mukaan.  

FEFO-poimintaa käytettäessä ensimmäisenä vanhenevat nimikkeet kerätään vanhenemispäivämäärien perusteella muodostettuun väliaikaisen nimikeseurantaluetteloon. Jos kahdella nimikkeellä on sama vanhentumispäivämäärä, pienemmällä erä- tai sarjanumerolla varustettu poimitaan ensin. Jos erä- tai sarjanumerot ovat samoja, ensimmäisenä rekisteröity nimike valitaan ensin. Poimimisvarastopaikkojen nimikkeiden valinnan perusehtoja, kuten varastopaikan luokittelua ja kappaletavaraa, käytetään väliaikaisessa FEFO-nimikkeenseurantaluettelossa.  

#### <a name="put-away-template"></a>Hyllytysmalli

Hyllytysmalli määrittää sarjan priorisoituja sääntöjä, joita on käytettävä hyllytyksiä luotaessa. Hyllytysmalli esimerkiksi edellyttää, että nimikkeet asetetaan varastopaikkaan, jonka varastopaikan sisällössä on sama mittayksikkö. Jos kapasiteetiltaan samanlaista varastopaikkaa ei löydy, nimike on asetettava tyhjään varastopaikkaan. Hyllytysmalli määritetään nimikkeelle ja sijainnille.  

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/get-started-warehouse-management/)

## <a name="see-also"></a>Katso myös

[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
