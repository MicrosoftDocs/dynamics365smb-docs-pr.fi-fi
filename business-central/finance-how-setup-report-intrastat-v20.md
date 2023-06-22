---
title: Intrastat-ilmoituksen määrittäminen ja raportoiminen
description: Opi määrittämään Intrastat-raportointiominaisuudet ja raportoimaan muiden EU-maissa toimivien yritysten kanssa käyty kauppa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 8451, 12202, 31077'
ms.date: 05/23/2022
ms.author: bholtorf
---
# <a name="set-up-and-report-intrastat" />Intrastat-ilmoituksen määrittäminen ja raportoiminen

Kaikkien Euroopan unionin alueen yritysten täytyy raportoida kaupastaan muiden EU-maiden/alueiden kanssa. Tavaran liikkuminen on raportoitava kotimaan/-alueen tilastoviranomaisille kuukausittain ja raportti on toimitettava veroviranomaisille. Ohjelmassa tätä kutsutaan Intrastat-raportoinniksi. **Intrastat-ilmoitus**-sivulla voi täyttää jaksottaiset Intrastat-ilmoitukset.

[!INCLUDE[intrastat-2022w2](includes/intrastat-2022w2.md)]

## <a name="required-and-optional-setups" />Pakolliset ja valinnaiset määritykset

> [!IMPORTANT]
> Asiakaskortit ja toimittajakortit sisältävät **Intrastat-kumppanin tyyppi**-kentän, jolla on samat arvovaihtoehdot kuin **Kumppanin tyyppi** -kentällä eli *"" (tyhjä)*, *Yritys* ja *Henkilö*. **Intrastat-kumppanin tyyppi** -kenttä on korvannut **Kumppanin tyyppi** -kentän Intrastat-raportoinnissa. **Kumppanin tyyppiä** käytetään SEPA:ssa SEPA-suoraveloitusmaksujärjestelmän määrittämiseen (Core tai B2B). **Intrastat-kumppanin tyyppiä** käytetään vain Intrastat-raportoinnissa. Tällä tavoin voit tarpeen mukaan määrittää eri arvot näille kahdelle kentälle.
>
> Huomaa kuitenkin, että jos **Intrastat-kumppanin tyyppi** -kenttä jätetään tyhjäksi, Intrastat-raportoinnissa käytetään **Kumppanin tyyppi** -kentän arvoa.

Sinun on määritettävä useita asetuksia, ennen kuin voit raportoida Intrastat-tiedot Intrastat-ilmoituksella.  

* **Valtiokohtaiset Asetukset**: Valtiokohtaiset Asetukset sivua käytetään intrastat-reportoinnin käyttöönottoon ja sen osetusaletusten määrittelyyn. Voit määrittää sen, tarvitkseeko sinun raportoida Intrastat lähetyksistä (toimitukset), kuiteista (saapuvat) vai molemmista, riippuen paikkalisten asetuksien rajoista. Voit myös määrittää oletusasetukset tapahtumatyypeille tavallisia ja palautusdokumentteja koskien, joita käytetään maksuliikenteen raportointiin.
* **Intrastat-ilmoitusmallit**: Käytettävät Intrastat-ilmoitusmallit ja -erät on määritettävä. Koska Intrastat-tiedot raportoidaan kuukausittain, sinun on luotava 12 samaan malliin perustuvaa Intrastat-ilmoituserää.  
* **Kauppatavarakoodit**: Tulli- ja veroviranomaiset ovat luoneet nimikkeiden ja palvelujen luokittelua varten numeeriset koodit. Nämä koodit määritetään nimikkeissä.
* **Kauppatapahtuman luonteen koodit**: Mailla ja alueilla on eri koodit Intrastat-tapahtumatyypeille, kuten tavallisille ostoille ja myynneille, palautettujen tavaroiden vaihdolle ja palauttamattomien tavaroiden vaihdolle. Määritä omaa maata tai aluetta koskevat koodit. Näitä koodeja käytetään myynti-ja ostoasiakirjojen **Ulkomaankauppa**-pikavälilehdessä sekä palautusten käsittelyssä.

    > [!NOTE]
    > Tammikuusta 2022 alkaen Intrastat edellyttää eri tapahtuman luonteen koodia yksityishenkilöille tai ALV-rekisteröitymättömille yrityksille suunnatuille ja ALV-rekisteröityneille yrityksille osoitetuille toimituksille. Tämän vaatimuksen täyttämiseksi on suositeltavaa tarkistaa tapahtumien luonteiden koodit ja/tai lisätä uusia sellaisia **Tapahtumien tyypit** -sivulle kulloisenkin maan vaatimusten mukaisesti. Lisäksi kannattaa tarkistaa ja päivittää **Intrastat-kumppanin tyyppi**-kenttä muotoon *Henkilö* asianomaisten asiakkaiden eli yksityishenkilöjen ja ALV-rekisteröimättömien yritysten **Asiakas**-sivulla. Jos et ole varma oikeasta Intrastat-kumppani- tai tapahtumatyypistä, suosittelemme, että pyydät samassa maassa tai samalla alueella asuvan asiantuntijan neuvoa.

* **Kuljetusmuodot**: Intrastat-kuljetusmuodoilla on seitsemän yksimerkkistä koodia. **1** tarkoittaa merikuljetusta, **2** rautatiekuljetusta, **3** tiekuljetusta, **4** ilmakuljetusta, **5** postitusta, **7** kiinteää asennusta ja **9** omaa käyttövoimaa (esimerkiksi auton kuljettaminen sitä ajamalla). [!INCLUDE[prod_short](includes/prod_short.md)] ei edellytä näitä koodeja, mutta suosituksena on käyttää merkitykseltään vastaavia kuvauksia.  
* **Tapahtumamääritykset**: Voit täydentää näiden määritysten avulla tapahtumatyyppien kuvauksia.  
* **Alkuperämaa** : Käytä kaksikirjaimisia ISO-alfakoodeja sen maan osalta, jossa tuote hankittiin tai tuotettiin. Jos tuotetta on tuotettu useammassa kuin yhdessä maassa, alkuperämaa on viimeinen maa, jossa sitä käsiteltiin merkittävästi.
* **Tuontijäsenmaassa sijaitsevan kumppanin ALV-tunnistenumero** : Tämä on sen kumppanin ALV-tunnistenumero, joka sijaitsee jäsenvaltiossa, johon tuote tuotiin. ALV-tunnusta käytetään myös EU-maiden välisten vientitietojen vaihdossa jäsenvaltioiden kesken, ja sen avulla jäsenvaltiot voivat jakaa vastaanotetut tiedot oman maansa tuontiyritykselle. Raportointiyksiköiden on ilmoitettava sen yrityksen ALV-tunnus, joka on ilmoittanut unionin sisäisen tuotteiden hankinnan jäsenvaltiossa, johon tuote tuotiin.

> [!NOTE]
> Liikekumppanien ALV-tunnus voi vaihdella liiketoimintaolosuhteiden mukaan. Käytettävä tunnus eroaa esimerkiksi ketju myynnin tapauksista, joissa toimittaja myy tuotteen toiseen maahan, ja sitten kyseinen yritys esimerkiksi myy nimikkeen toiselle yritykselle samassa maassa tai kolmikantakaupassa. Jos et ole varma oikeasta ALV-tunnuksesta, suosittelemme, että pyydät samassa maassa tai samalla alueella asuvan asiantuntijan neuvoa.

Myös seuraavat voi määrittää:

* **Alueet**: Voit täydentää tämän vaihtoehdon avulla maita ja alueita koskevia tietoja.  
* **Tulo-/ lähtöpaikat**: Voit määrittää tämän vaihtoehdon avulla sijainnit, joissa lähetät nimikkeitä muihin maihin tai vastaanotat nimikkeitä muista maista. Heathrow'n lentoasema on esimerkki tulo- tai lähtöpaikasta. Tulo- tai lähtöpaikat annetaan myynti- ja ostoasiakirjoihin **Ulkomaankauppa**-pikavälilehdessä. Nämä tiedot kopioidaan myös nimiketapahtumista Intrastat-ilmoituksen luomisen yhteydessä.  

### <a name="to-set-up-intrastat-templates-and-batches" />Intrastat-ilmoituksen mallien ja erien määrittäminen

Intrastat-erätyöt sisältävät vain nimiketapahtumat mutta ei kirjanpitotapahtumia. Jos yrityksellä on Intrastat-raportointiin soveltuvia kirjanpitotapahtumia, ne on lisättävä manuaalisesti. Jos esimerkiksi ostat tietokoneen toisesta EU-maasta tai toiselta EU-alueelta, tietokonetta ei sijoiteta varastoon, mutta se kirjataan pääkirjanpitoon. Tällaiset tapahtumat on lisättävä manuaalisesti Intrastat-ilmoitukseen.  

Voit viedä tapahtumat tiedostoon, jonka voit lähettää Intrastat-viranomaisille. Voit myös tulostaa raportin, lisätä viranomaisten tiedot manuaalisesti lomakkeisiin ja lähettää sitten tiedot.

> [!NOTE]
> Jokaiselle kuukaudelle kannattaa määrittää Intrastat-ilmoituksen erä.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-ilmoitusmallit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Luo malli jokaiselle käyttämällesi Intrastat-lomakkeelle.  
3. Luo eriä valitsemalla **Erät**-toiminto.  
4. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Luo malli jokaiselle käyttämällesi Intrastat-lomakkeelle.

> [!NOTE]
> Anna tilastokausi **Tilastokausi**-kenttään nelinumeroisena lukuna, jossa kaksi ensimmäistä lukua merkitsevät vuotta ja kaksi seuraavaa kuukautta. Anna esimerkiksi kesäkuulle 2017 luku 1706.

### <a name="to-set-up-transport-methods" />Kuljetusmuotojen määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kuljetusmuodot** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory" />Joidenkin Intrastat-raportin kenttien määrittäminen pakolliseksi

Joissakin maissa, kuten Espanjassa ja Isossa-Britanniassa, viranomaiset vaativat Intrastat-raportteihin esimerkiksi ostojen toimitustavan tai joitakin arvoja myynnin ylittäessä tietyn raja-arvon. Voit valita **Intrastat-asetukset**-sivulla voi osoittaa, että **Intrastat-tarkistusluettelon asetukset** määrittää pakolliset kentät **Intrastat-ilmoitus**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Valtiokohtaiset asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Intrastat-tarkistusluettelon asetukset** -toiminto.
3. Valitse **Intrastat-tarkistusluettelon asetukset** -sivulla **Kentän nimi** ja valitse se Intrastat-raportin kenttä, josta tehdään pakollinen.

### <a name="czechia" />Tšekki

Erityisesti tšekkiläisten yritysten on määritettävä myös kauppatavarakoodit ja tapahtumien luonteiden koodit.  

#### <a name="to-set-up-commodity-codes" />Kauppatavarakoodien määrittäminen

Kaikilla ostettavilla ja myytävillä nimikkeillä on oltava kauppatavarakoodi.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kauppatavarakoodit** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Määritä kauppatavarakoodi laajentamalla **Nimikkeen kortti** -sivulla **Kustannukset ja kirjaus** -pikavälilehti ja antamalla koodi **Kauppatavarakoodi**-kenttään.

### <a name="italy" />Italia

Erityisesti italialaisten yritysten on määritettävä myös kauppatavarakoodit ja tapahtumien luonteiden koodit.  

#### <a name="to-set-up-transaction-nature-codes" />Kauppatapahtuman luonteen koodien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tapahtuman luonteen koodit** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Jos käytät tiettyä kauppatapahtuman luonteen koodia usein, voit määrittää sen oletusasetukseksi. Se onnistuu valitsemalla koodi **Valtiokohtaiset asetukset** -sivulla.

## <a name="to-report-intrastat" />Intrastat-raportointi

Kun olet täyttänyt Intrastat-ilmoituksen, voit suorittaa **Tarkistusluettelo-raportti**-toiminnon ja varmistaa, että kaikki ilmoituksen tiedot ovat oikein. **Intrastat-tarkistusluettelon asetukset** -sivulla määritetyt pakolliset kentät, joissa ei ole arvoja, näytetään Virheet ja varoitukset -tietoruudussa **Intrastat-kirjaus**-sivulla. Voit sitten tulostaa Intrastat-raportin lomakkeena tai luoda tiedoston, jonka voit lähettää oman maasi tai alueesi veroviranomaisille.  

### <a name="to-fill-in-intrastat-journals" />Intrastat-ilmoitusten täyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-ilmoitus** ja valitse sitten vastaava linkki.  
2. Valitse **Intrastat-ilmoitus**-sivulla **Erän nimi** -kentässä käsiteltävä kirjauskansion erä ja valitse sitten **OK**.  
3. Valitse **Ehdota rivejä** -toiminto. **Aloituspvm**- ja **Lopetuspvm**-kentissä on valmiina päivämäärät, jotka määriteltiin tilastokaudelle päiväkirjan erässä.  
4. Voit syöttää **Epäsuorien kustann. pros.osuus** -kenttään prosentin (kattamaan kuljetus- ja vakuutuskustannuksia). Jos syötät prosentin, päiväkirjan **Tilastoarvo**-kentän sisältö on suhteellisesti korkeampi.  
5. Käynnistä eräajo valitsemalla **OK**.  

Eräajo hakee kaikki tämän tilastokauden nimiketapahtumat ja lisää ne riveiksi Intrastat-ilmoitukseen. Voit muokata rivejä tarvittaessa.  

> [!IMPORTANT]  
> Eräajo hakee vain ne tapahtumat, joilla on sellainen maa- tai aluekoodi, joille Intrastat-koodi annettiin **Maat/alueet**-sivulla. Siksi on tärkeää, että syötät Intrastat-koodit sellaisille maa-/aluekoodeille, joilla tulet tekemään eräajoja. Eräajo määrittää **Kumppanin ALV-tunnus** -kentän arvoksi *QV999999999999* yksityishenkilöillä ja ALV-rekisteröimättömillä yrityksillä (asiakkailla, joiden **Intrastat-kumppanin tyyppi**-kentän arvo on *Henkilö*) ja käyttää kirjatun nimiketapahtumamerkinnän tai työtapahtumamerkinnän **Tapahtuman tyyppi** -kentän arvoa.

### <a name="to-modify-intrastat-journals-lines" />Intrastat-ilmoitusten rivien muokkaaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-ilmoitus** ja valitse sitten vastaava linkki.  
2. Valitse **Intrastat-ilmoitus**-sivulla **Erän nimi** -kentässä käsiteltävä kirjauskansion erä ja valitse sitten **OK**.  
3. Intrastat-ilmoitusten rivien suodattamiseen tietyin perustein käytetään suodatinruutua. Esimerkiksi **Kumppanin ALV-tunnus** -kentissä voi käyttää suodattimena arvoa *QV999999999999*.
4. Valitse **Jaa**-kuvake ![Jaa sivu toisessa sovelluksessa.](media/share-icon.png) ja valitse **Muokkaa Excelissä**
5. Muokkaa suodattamiasi Intrastat-ilmoituksen rivejä Excelissä. Muokkaa esimerkiksi **Tapahtuman tyyppi** -kentän arvoja.  
6. Julkaise Excelissä tehdyt muutokset takaisin kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] -versioissa, jotka eivät tue ilmoitusten osalta [**Muokkausta Excelissä**](across-work-with-excel.md#edit-in-excel), voit luoda määrityspaketteja Intrastat-ilmoitusten Exceliin viemistä ja sieltä tuomista varten. Lisätietoja on kohdassa [Paikallisten tietojen siirtäminen Business Central Online -ohjelmaan](/dynamics365/business-central/dev-itpro/administration/migrate-data) -hallintasisällössä.

### <a name="report-intrastat-on-a-form-or-a-file" />Intrastat-raportointi lomakkeella tai tiedostona

Saat Intrastat-lomakkeeseen tarvittavat tiedot tilastoja ylläpitäviltä viranomaisilta tulostamalla **Intrastat – lomake** -raportin. Ennen sitä sinun täytyy laatia Intrastat-ilmoitus ja täyttää se. Jos sinulla on sekä myyntiin että ostoihin liittyviä kauppatahtumia, sinun täytyy tehdä erillinen lomake molemmille tyypeille, ja sinun täytyy siten tulostaa raportti kahdesti.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-ilmoitukset** ja valitse sitten vastaava linkki.  
2. Valitse käsiteltävä päiväkirjan erä **Intrastat-ilmoitus**-sivun **Erän nimi** -kentässä.  
3. Jos et vielä ole tehnyt tätä, täytä ilmoitus manuaalisesti tai valitse **Ehdota rivejä** -toiminto.  
4. Valitse **Tulostaa Intrastat-ilmoituksen** -toiminnon.  
5. Lisää **Intrastat-ilmoituksen rivi** -pikavälilehdessä **Tyyppi**-suodatin ja määritä, onko kyseessä **Vastaanotto** vai **Toimitus**.  
6. Tulosta raportti valitsemalla **Lähetä kohteeseen**.  

### <a name="report-intrastat-in-a-file" />Intrastat-raportointi tiedostona

Voit nyt lähettää Intrastat-raportin tiedostona. Ennen tiedoston luomista voit tulostaa tarkastusluettelon, jossa on samat tiedo kuin mitä tiedostossa tulee olemaan.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-ilmoitus** ja valitse sitten vastaava linkki.  
2. Valitse käsiteltävä päiväkirjan erä **Intrastat-ilmoitus**-sivun **Erän nimi** -kentässä.  
3. Jos et vielä ole tehnyt tätä, täytä ilmoitus manuaalisesti tai valitsemalla **Ehdota rivejä** -toiminto.  
4. Valitse **Luo tiedosto** -toiminto.  
5. Valitse erätyösivulla **OK**-painike.  
6. Valitse **Tallenna**.  
7. Selaa sijaintiin, jonne haluat tallentaa tiedoston. Anna tiedoston nimi ja valitse sitten **Tallenna**.

> [!NOTE]
> Kun Intrastat-raportin rivillä on lisämittayksikkö, nimikkeen painoa ei näytetä, koska tätä arvoa ei edellytetä.

## <a name="reorganize-intrastat-journals" />Intrastat-ilmoitusten uudelleenjärjestely

Koska Intrastat-raportti on lähetettävä joka kuukausi ja luot uuden päiväkirjan erä kullekin raportille, sinulla tulee olemaan ajan mittaan useita päiväkirjan eriä. Kirjauskansiorivejä ei poisteta automaattisesti. Haluat ehkä järjestää päiväkirjan erien nimet uudelleen jaksoittain. Voit tehdä sen poistamalla ne päiväkirjan erät, joita et enää tarvitse. Näissä erissä olevat päiväkirjan rivit poistuvat myös.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Intrastat-ilmoitukset** ja valitse sitten vastaava linkki.  
2. Voit tarkastella asetuksia valitsemalla **Erän nimi** -kentän.  
3. Valitse ensin poistettavat päiväkirjan erät ja sitten **Poista**-painike.  

## <a name="tariff-numbers" />Tariffinumerot

Monissa maissa tulli- ja veroviranomaiset määrittävät kahdeksannumeroiset koodit eri nimikkeille. Jotta nimiketapahtumissa olisi tarvittavat tiedot, kun ohjelma tuo ne Intrastat-ilmoituksen riville, **Tavaranimikkeet**-sivulla täytyy olla syötettynä tiedot tavaranimikkeistä. Etsi niiden nimikkeiden koodit, joilla yrityksesi käy kauppaa, ja syötä ne **Tavaranimikkeet**-sivulle.

Lisää **Tavaranimikkeet**-sivulle kaikki koodit, joita käytät. Koodit täytyy syöttää nimikekortille ennen kirjauksen aloittamista. Kun olet määrittänyt koodit, syötä ne **Tavaranimike**-kenttään. kenttä nimikekortissa. Sinun täytyy myös täyttää **Nettopaino**-kenttä nimikekortilla.

## <a name="see-related-training-at-microsoft-learnlearnmodulesprocess-intrastat-dynamics--business-centralindex" />Lisätietoja aiheeseen liittyvästä koulutuksesta on [Microsoft Learnissa](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also" />Katso myös

[Taloushallinto](finance.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
