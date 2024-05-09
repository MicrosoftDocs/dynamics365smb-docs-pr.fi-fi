---
title: Sähköisten asiakirjojen käyttäminen ostoprosessissa
description: Lisätietoja ostolaskuihin ja tilauksiin liittyvien sähköisten asiakirjojen toimintojen käyttämisestä.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, receive, purchase, matching, mapping, Copilot'
ms.search.form: '50, 51, 138, 6103, 6133, 6121, 6167, 9307, 9308'
ms.date: 04/03/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Sähköisten asiakirjojen käyttäminen ostoprosessissa

Voit käyttää määritettyjä sähköisiä asiakirjoja ostoasiakirjojen yhteydessä.

Tällä hetkellä voit käyttää seuraavia ostoasiakirjoja sähköisten asiakirjojen toimintojen kanssa:  

- Ostolaskut
- Ostotilaukset (versiosta 24.0)
- Ostohyvityslaskut
- Yleiset päiväkirjat

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] -versiosta 24.0 on mahdollista liittää **ostotilaukset** vastaanotettuihin **E-asiakirjoihin**.  

## Sähköiset asiakirjat ostoissa

Dynamics 365 Business Centralin ostojen sähköisten asiakirjojen vastaanotto voidaan tehdä eräajona tai manuaalisesti.  

### Miten määrittää toimittajia työskentelemään eri ostoasiakirjojen kanssa  

Määritä toimittajat käyttämään saapuvia elektronisia laskuja oikein noudattamalla seuraavia ohjeita: 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten vastaava linkki. 
2. Valitse toimittaja, jonka haluat määrittää.   
3. Etsi **Vastaanotto**-pikavälilehdessä **Vastaanota e-asiakirja vastaanottajalle** -kenttä määrittääksesi oletusostoasiakirjan, joka luodaan vastaanotettavasta E-asiakirjasta. 

> [!NOTE]
> **Vastaanota e-asiakirjaan kohteeseen** -kentässä käyttäjät voivat joko valita **ostolaskun** tai **ostotilauksen** sen perusteella, mitä he ovat halunneet luoda vastaanotetusta e-laskusta. Tämä valinta ei vaikuta korjaavien asiakirjojen luomiseen. Molemmissa skenaarioissa järjestelmä luo **hyvityslaskun**.  

> [!NOTE]
> Jos käyttäjä valitsee **Ostotilaus**-vaihtoehdon **Vastaanota e-asiakirjalle** -kentässä, järjestelmä yrittää päivittää yhtä olemassa olevista ostotilauksista, mutta jos vastaanotetun **e-asiakirjan** sisältämän toimittajan ostotilausta ei ole olemassa, [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelma luo uuden **ostotilauksen** käyttäen samaa lähestymistapaa kuin tällä sivulla myöhemmin selitettyjen uusien **ostolaskujen** luominen.  

4. Valitse yksi vaihtoehdoista, joita haluat käyttää valitulle toimittajalle. 
5. Sulje sivu.   

### Ostolaskujen käyttäminen  

#### Eräajon suorittaminen  

> [!NOTE]
> Tämä eräajo on tarkoitettu saapuvien laskujen automaattista keräilyä varten. Toiminnon käyttäminen on mahdollista vain, jos se on otettu käyttöön maassa tai alueella.  

Aina, kun **työjono** valitaan suoritettavaksi ja ulkoisella palvelulla on toimittajan lähettämiä saapuvia laskuja, järjestelmä kerää ja tuo kyseiset laskut. Voit suorittaa prosessin loppuun alla olevien ohjeiden avulla. 

1. Kun eräajo on suoritettu loppuun, juuri tuodut laskut ja niiden perustiedot näkyvät **Sähköiset asiakirjat** -sivulla. 
2. Voit tarkastella lisätietoja avaamalla tietyn sähköisen asiakirjan.   
3. Jos e-asiakirjassa ei ollut virheitä tai ongelmia, **Tietue**-kenttä kartoittaa ostolaskun tositteen numeron, jos tämä on määritetty **Toimittajakortti**-sivulla (jonka järjestelmä loi automaattisesti). Avaa asiakirja valitsemalla linkki.
 
> [!NOTE]
> Järjestelmän luoma asiakirja ei ole kirjattu asiakirja. 

1. Voit siirtyä suoraan ostoasiakirjaan valitsemalla **Tietue**-kentän. Kun olet avannut **Ostolasku**-sivun, tarkista asiakirja. Jos kaikki on nyt oikein, voit kirjata asiakirjan.  
1. Kun kirjaat ostoasiakirjan, **Sähköinen asiakirja** -sivun**Tietue**-kentän arvo päivitetään **Lasku**-arvosta **Ostotilaus**-arvoksi, ja kirjatun ostoasiakirjan numero on saatavilla. Voit valita numeron, jos haluat avata kirjatun ostolaskun. 

Lokien tiedot ovat samat kuin sähköisten asiakirjojen myyntiprosessissa.  

Koska myyntiprosessin virheet liittyvät useimmiten palvelun saatavuuteen, saapuva asiakirja voi sisältää useita syitä. Virheen yleisin syy on se, että järjestelmä ei tunnista toimittajalta saadun sähköisen asiakirjan rivejä. Sen vuoksi ostolaskuun ei voida syöttää rivejä. 

Seuraavassa kerrotaan kaksi yleisintä virhettä:  

- Jos haluat käyttää suoraan pääkirjanpidon (KP) tilille kirjatun toimittajalaskun tiettyä riviä, **Tekstin linkitys** -arvo on määritettävä oikein. Jos haluat ohittaa tämän virheen ja käyttää KP-tilejä, valitse **Linkitä teksti tiliin** ja luo **Tekstin linkitys** -arvolle ja käytettävälle **Debet-tilin numero** -arvolle tietty yhdistämismääritys. 
- Jos haluat seurata varastoa ja käyttää toimittajalaskun rivejä asiakirjarivien nimikkeiden täyttämisessä, määritä oikein **Nimikeviittauksen nro** -arvo. Voit ohittaa tämän virheen linkittämällä ulkoisen nimikkeen nimikenumeroihin nimikkeen viiteluettelon avulla. Saat lisätietoja kohdasta [Nimikkeen viittausten käyttäminen](inventory-how-use-item-cross-refs.md). 

Virheiden ja varoitusten korjaamisen jälkeen voit manuaalisesti määrittää, milloin järjestelmän tulee luoda ostolasku asetusten perusteella, valitsemalla **Luo tiedosto**.   

#### Laskujen tuominen manuaalisesti  

Voit tuoda manuaalisesti ulkoisia sähköisiä asiakirjoja alla olevien ohjeiden mukaan:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköinen asiakirjapalvelu** ja valitse sitten vastaava linkki. 
2. Valitse **Sähköinen asiakirjapalvelu** -sivulla aktiivinen palvelu.   
3. Valitse **Vastaanotto** ja lataa toimittajalta saatu sähköisen asiakirjan tiedosto. 
4. Jos virhesanoma näkyy jälleen, avaa sähköinen asiakirja ja korjaa virheet. 
5. Kun virheet on korjattu, valitse **Tuo manuaalisesti** -ryhmässä **Luo asiakirja**.  
6. Kun asiakirja on luotu [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasssa, eräajon käyttäminen ei muuta tapaa, jolla näet sen. 

### Ostotilausten sähköiset asiakirjat  

#### Linkitä ostotilaukset vastaanotettuihin sähköisiin asiakirjoihin

Jos **toimittajasi** on määrittänyt **Vastaanota e-asiakirjalle** -kentän käyttämään **ostotilauksia**, niin kun sähköinen asiakirja on luotu [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa (manuaalisesti tai ulkoisesta päätepisteestä), [!INCLUDE[prod_short](includes/prod_short.md)] se tekee seuraavaa:  

1. Jos kyseisen toimittajan **ostotilaus** on olemassa ja jos vastaanoton **E-asiakirja**-tiedostossa on ostotilauksen numero, [!INCLUDE[prod_short](includes/prod_short.md)] linkittää tämän **E-asiakirjan** automaattisesti mainittuun **ostotilaukseen**, ja tämän **e-asiakirjan** **asiakirjan tila** on **Käynnissä**, ja **Huollon tila** -alasivun **E-asiakirjan tila** on **Tilaus linkitetty**. Linkki näkyy kyseisen **E-asiakirjan** **Asiakirja**-kentässä. Jos sinun täytyy muuttaa linkitetty **ostotilaus** automaattisesti, voit tehdä sen käyttämällä **Päivitä ostotilauslinkki** -toimintoa ja valita manuaalisesti yhden toimittajan olemassa olevista ostotilauksista. Voit tehdä sen vain, ennen kuin vastaat **E-asiakirjan** ja **ostotilauksen** välisiä rivejä.  
2. Jos kyseisen toimittajan **ostotilaus** on olemassa, mutta **E-asiakirja**-tiedostossa ei ole ostotilausnumeroa, [!INCLUDE[prod_short](includes/prod_short.md)] tarjoaa mahdollisuuden valita yksi olemassa olevista ostotilauksista silloin, kun ja jos latasit tämän asiakirjan manuaalisesti, avaamalla **Ostotilaukset**-luettelon tilauksilla vain toimittajalle, jonka sait **E-asiakirjan**, jossa sinun täytyy valita **ostotilaus** ja valita **OK**. Jos et valinnut oikeaa **ostotilausta** tai sait **E-asiakirjan** automaattisesti ulkoisesta päätepisteestä **työjonon** avulla , uutta **e-asiakirjaa** ei linkitetä minkään ostoasiakirjan kanssa, ja **asiakirjan tilaksi** tulee **Virhe** ja **Huollon tila** -alasivun **e-asiakirjan tilaksi** **tuodun asiakirjan käsittelyvirhe**. Kun haluat lopettaa linkittämisen **ostotilaukseen**, valitse **Päivitä ostotilauslinkki** -toiminto ja valitse yksi tämän toimittajan ostotilauksista. 
3. Jos kyseisen toimittajan **ostotilausta** ei ole olemassa uuden **E-asiakirjan** luonnin hetkellä, [!INCLUDE[prod_short](includes/prod_short.md)] luo uuden **ostotilauksen** käyttäen samaa luontimallia kuin uusissa **ostolaskuissa** jo on. Tämän **sähköisen asiakirjan** **asiakirjan tila** on **käsitellään**, ja **Palvelun tila** -alisivun **sähköisen asiakirjan tila** on **Tuotu asiakirja luotu**. Linkki näkyy kyseisen **E-asiakirjan** **Asiakirja**-kentässä.   

#### Vastaanotetun e-asiakirjan rivien täsmäytys ostotilauksen kanssa  

Voit liittää vastaanotetut sähköiset asiakirjat ostotilausten riveihin kahdesta eri paikasta, **E-asiakirja**-sivulta tai **Ostotilaus**-sivulta. Helpoin tapa paikallistaa jo linkitetyt **ostotilaukset** on käyttää **Linkitetyt ostotilaukset** -ruutua osana **E-asiakirjan toimenpiteitä**. Kaikki ei-linkitetyt asiakirjat löytyvät **odottavat ostojen e-laskut** -ruudusta, jossa on luettelo tarkasteltavissa olevista **E-asiakirjoista**.  

> [!NOTE]
> Näitä kahta ruutua koskevat **e-asiakirjatoiminnot** ovat seuraavissa **Roolikeskuksissa**: Liiketoimintapäällikön arviointi, Liiketoimintapäällikkö, Kirjanpitäjä, Varastopäällikkö ja Toimitus ja vastaanotto.  

> [!NOTE]
> Jos ALV-prosentti eroaa saapuvan tositteen ja yrityksen ALV-prosentin välillä, vastaavia tositteita ei voi käyttää usean maan ympäristössä.  

##### Ostotilauksen rivien kohdistus  

Voit täsmätä **Ostotilaukset**-luettelon tai jonkin avatun **ostotilauksen** rivejä. Voit aloittaa tämän käyttämällä seuraavia vaiheita:  

1. Valitse Roolikeskuksen **Linkitetyt ostotilaukset** -ruutu, jos niitä on. 
2. Koska kohdistukselle on kaksi vaihtoehtoa, valitse niistä toinen: 

    1. Jos haluat täsmätä **Ostotilaukset**-luettelon rivien kanssa, valitse täsmäättävä **Ostotilaus**-rivi ja valitse **Liitä e-asiakirjarivit** -toiminto.  
    2. Jos haluat avata **ostotilauksen** ensin, avaa asiakirja ja valitse **liitä E-asiakirjan rivit** -toiminto. 

3. Koska molemmilla vaihtoehdoilla on sama prosessi, avaat **Ostotilausten täsmäytys** -sivun seuraavalla sisällöllä: 

    1. Otsikosta löydät seuraavat tiedot, joiden avulla voit linkittää rivit helpommin: 

    |Kentän nimi |Kuvaus |
    |--------|-----------------|
    |Toimittajan nimi |Määrittää sähköisen asiakirjan toimittajan nimen. |
    |Sähköisen asiakirjan nro |Määrittää linkitetyn sähköisen asiakirjan numeron. |
    |Sähköisen asiakirjan päivämäärä |Määrittää linkitetyn sähköisen asiakirjan päivämäärän.  |
    |Sähköisen asiakirjan summa |Määrittää linkitetyn sähköisen asiakirjan kokonaissumman, joka sisältää ALV:n. |

    2. Riveiltä löydät rivit, jotka on tuotu **E-asiakirja**-tiedostosta vasemmalla ja rivit olemassa olevasta **ostotilauksesta** oikealla puolella.  
    3. Molemmilla puolilla riveillä on nimikenumerot ja kuvaukset sekä **Välitön yksikkökustannus** ja **Rivialennus-%**.  
    4. **Tuodut rivit** -puolella voit myös etsiä **Määrä**-kentän e-laskun kokonaismääränä ja **Täsmäytetty määrä** -kentän määrittämällä määrän, joka on jo täsmännyt ostotilausriveihin. 
    5. **Ostotilausrivit**-puolella on myös **Saatavilla oleva määrä** määränä, joka voidaan täsmätä tälle riville (vastaanotettu, mutta ei laskutettu määrä) ja **Laskutettava määrä** määrittäen määrän, joka on jo täsmäytetty tälle riville. 
    6. Kun haluat kohdistaa rivit vastaamaan toisiaan, valitse ne molemmilla puolilla olevat rivit, jotka haluat liittää riveihin, ja valitse **Täsmäytä manuaalisesti** -toiminto. Täsmäävät rivit merkitään vihreällä värillä. 
    7. On mahdollista täsmäyttää yksi yhteen, mutta on myös mahdollista täsmäyttää useita yhteen tai yksi useisiin valitsemalla useampi rivi yhdeltä tai toiselta puolelta ennen kuin valitset **Täsmäytä manuaalisesti** -toiminnon. 
    8. Voit myös valita **Täsmäytä automaattisesti** -toiminnon vastaamaan automaattisesti kaikkia rivejä, joilla on sama **tyyppi**, **numero**, **yksikköhinta**, **alennus** ja **mittayksikkö**. 
    9. Jos teet virheen, voit valita **Poista täsmäytys** -toiminnon poistaaksesi vastaavat rivit ostotilauksen puolelta tai valita **Nollaa täsmäytys** nollataksesi kaiken täsmäävän. 
    10. Jos **e-asiakirjassa** on useita rivejä, voit saman prosessin aikana valita **Näytä odottavat rivit** -toiminnon ja poistaa kaikki sähköisen asiakirjan rivit, jos ne on jo täysin täsmäytetty. Jos haluat nähdä kaikki rivit, voit aina valita **Näytä kaikki rivit** -toiminnon. 

4. Kun olet lopettanut vastaavuuden, sinun täytyy valita **Kohdista ostotilaukseen** -toiminto.   
5. Kun kohdistat vastaavuuden **ostotilaukseen**, [!INCLUDE[prod_short](includes/prod_short.md)] päivittää seuraavat kentät:

    1. **Toimittajan laskunro** asiakirjan otsikon **asiakirjapvm** päivitetään vastaanottamiesi ja linkittämiesi sähköisten asiakirjojen arvoilla. 
    2. Rivien **Laskutettava määrä** päivitetään **Ostotilausten täsmäytys** -sivun **Laskutettava määrä** -sarakkeen arvoilla sen perusteella, mitä olet tehnyt. 
    3. Nyt voit kirjata asiakirjan valitsemalla **Kirjaa**-toiminnon.  
    4. Kun olet kirjannut asiakirjan, **E-asiakirja**-sivun **Asiakirja**-kenttä muuttaa arvon ja liittyy **Kirjattuun ostolaskuun**. 
    5. Sulje sivu.  

> [!IMPORTANT]
> Oletusarvon mukaan voit verrata vain rivejä, joilla on sama kokonaissumma molemmissa asiakirjoissa. Tämä tarkoittaa sitä, että **välittömän yksikkökustannuksen** ja kohdistetun **rivialennus-%:n** täytyy olla sama, koska yhdessä asiakirjassa voi olla summa ilman alennusta ja toisessa alennuksella.  

Jos haluat lisätä toleranssia ja sallia eron **E-laskun** ja **Ostotilauksen** rivien välillä, noudata seuraavia vaiheita:   

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostojen ja maksettavien määritys** ja valitse sitten vastaava linkki.  
2. Haluat sallia toleranssin **E-asiakirjan vastaavuuden ero-%** -kentässä, joka määrittää suurimman sallitun kustannuseroprosentin, kun saapuvaa **E-asiakirjan** riviä täsmäytetään **ostotilaus**-rivin kanssa. 
3. Nämä asetukset koskevat kaikkia vastaavia rivejä, mutta harkitsevat jälleen kokonaissumman toleranssia, kuten **välitön yksikkökustannus** yhdessä kohdistetun **rivialennus-%:n** kanssa.  
4. Sulje sivu.   

##### E-asiakirjan rivien täsmäytys  

Voit täsmäyttää rivejä **E-asiakirja** -sivulla. Voit aloittaa tämän käyttämällä seuraavia vaiheita:  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköiset asiakirjat** ja valitse sitten vastaava linkki. 
2. Valitse täsmäytettävät **E-asiakirjat**.   
3. Avaa **Ostotilauksen täsmäytys** -sivu valitsemalla **Täsmäytä ostotilaus** -toiminto.  
4. Toista samat työvaiheet, joita käytit aloittaessasi ostotilauksien täsmäytyksen.

### Sähköisen asiakirjan kohdistusavustaja  

> [!NOTE]
> Tällä hetkellä **Sähköisen asiakirjan kohdistusavustaja** on Valmis tuotantoon -esiversiotilassa, ja se on saatavilla maailmanlaajuisesti, paitsi Kanadassa. Mutta se toimii vain englanniksi. 

> [!NOTE]
> Copilot on tekoälyyn perustuva avustaja, joka auttaa organisaatiossa työskenteleviä ihmisiä olemaan luovia ja automatisoimaan yksitoikkoisia tehtäviä. **Sähköisen asiakirjan kohdistusavustajan** avulla käyttäjät voivat helposti liittää vastaanotetut sähköiset laskunsa olemassa oleviin ostotilausriveihin käyttämällä LLM-mallia, jonka avulla kahden eri asiakirjan väliset rivit täsmäävät. 

#### Avustajan aktivoiminen  

Jos et aktivoinut **Sähköisen asiakirjan kohdistusavustaja** -toimintoa, se on tehtävä manuaalisesti. Ota **Sähköisen asiakirjan kohdistusavustaja** käyttöön noudattamalla seuraavia vaiheita: 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Avustaja- ja tekoälyominaisuudet** ja valitse sitten liittyvä linkki. 
2. Valitse ominaisuuksien luettelossa **Sähköisen asiakirjan kohdistusavustaja** ja muuta tilaksi **Aktiivinen**.  

Kun avustaja on aktivoitu, sitä voidaan alkaa käyttää.

#### Käytä sähköisen asiakirjan kohdistusavustajaa 

Jos avustaja on aktivoitu, olemassa olevat toiminnot **Yhdistä e-asiakirjan rivit** ostotilauksiin ja **Täsmäytä ostotilaus** **E-asiakirja** -sivulla saavat eri kuvakkeita, jotka symboloivat tekoälyominaisuutta. Voit suorittaa nämä toiminnot (täysin samalla tavalla kuin aiemmissa esimerkeissä ostotilausten luettelosta), yhdestä **ostotilauksista** tai **E-asiakirjasta**. Kaikki suoritusvaiheet ovat samat, mutta kun suoritat tämän toiminnon, tulokset poikkeavat toisistaan, ja sinun on noudatettava seuraavia vaiheita:  

1. Valitse linkitetyille asiakirjoille **Liitä e-asiakirjarivit**- tai **Täsmäytä ostotilaus** -toiminto.  
2. Voit huomata, että **E-asiakirjan täsmäytystilausrivit, joissa on avustaja** toimivat ja taustalla on **Ostotilauksen täsmäytys** -sivu. Tämä tarkoittaa, että sama prosessi tapahtuu, mutta **avustajan** automaattisella tuella, joka suorittaa täsmäytysprosessin sinun sijastasi. 
3. Muutaman sekunnin kuluttua **E-asiakirjan vastaavuustilausrivit avustajan kanssa** ehdottaa rivejä, joiden vastaavuuksien lisätiedot ovat: 

    1. Voit etsiä seuraavat tiedot kehotteen otsikosta: 

    |Kentän nimi |Kuvaus |
    |--------|-----------------|
    |Kohdistettu automaattisesti | Määrittää automaattisesti ehdotettujen kohdistusten määrän. Tämä perustuu merkkijonovertailuun, ja jos kuvaus on vähintään 80 %:n päällekkäinen, järjestelmä vastaa näitä kuvauksia automaattisesti käyttämättä GPT-ominaisuuksia. |
    |Copilotin kohdistamat | Määrittää avustajan ehdottamien osumien määrän käyttäen sekä merkkijonoa että semanttista vertailua. |
    |Sähköisen asiakirjan nro | Määrittää linkitetyn sähköisen asiakirjan numeron. |
    |Laskun summa yhteensä ilman ALV:tä | Määrittää laskun kokonaissumman ilman arvonlisäveroa. |
    |Kohdistettu summa yhteensä ALV:n kanssa | Määrittää kohdistetun summan ilman ALV:tä. |
    
    2. Jos kaikki rivit täsmäävät, oikeassa yläkulmassa näkyy vihreä teksti: **Kaikki rivit (100 %) vastaavat toisiaan. Tarkista vastaavuusehdotukset**.  
    3. Voit etsiä seuraavat tiedot **Täsmäytetyt ehdotukset** -riveiltä:  

    |Kentän nimi |Kuvaus |
    |--------|-----------------|
    |Sähköisen asiakirjan rivinro | Määrittää E-asiakirjan rivinumeron (joka tulee alkuperäisestä e-asiakirjatiedostosta). |
    |Sähköisen asiakirjan rivin kuvaus | Määrittää E-asiakirjan rivikuvauksen (joka tulee alkuperäisestä e-asiakirjatiedostosta). |
    |Kohdistettu määrä | Määrittää määrän, joka kohdistetaan ostotilausriviin. |
    |Ehdotus | Määrittää tekoälyn ehdottaman toimen, ja nämä ehdotetut toimenpiteet liittyvät ostotilausrivien vastaavuuksien täsmäytykseen. |

    4. Kaikki täysin ehdotetut ja toisiaan vastaavat rivit on merkitty vihreällä värillä. Jos on olemassa ongelma eli eri hinta, mutta sallitulla hintavälillä tämä rivi merkitään keltaiseksi, ja jos kuvauskenttien välillä on samankaltaisuutta, mutta hintaero on suurempi kuin sallittu, tämä rivi merkitään punaiseksi. 
    5. Jos et ole tyytyväinen joihinkin ehdotuksiin, voit poistaa ne **Poista rivi** -toiminnolla.  
    6. Jos haluat nähdä ehdotuksen täsmäytykset, voit avata **E-asiakirjan vastaavuustiedot** -sivun valitsemalla linkin **Ehdotus**-sarakkeesta. 
    7. **E-asiakirjan vastaavuuksien tiedot** -sivulla voit vertailla **E-asiakirjan** ja **ostotilauksen** tietoja varmistaaksesi ehdotetun vastaavuuden ennen sen vahvistamista. 
    8. Sulje sivu tarkistuksen jälkeen.   

4. Jos et ole tyytyväinen useimpiin ehdotuksiin tai et halua käyttää **Täsmäytä e-asiakirjan tilausrivit avustajan avulla** -ominaisuutta, valitse **Hylkää se**, ja voit jatkaa manuaalista sovittamista edellä selitetyllä tavalla.  
5. Jos haluat säilyttää ehdotukset, valitse **Säilytä se** -painike, niin järjestelmä tallentaa kaikki **Avustajan** tekemät ehdotukset.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] sulkee avustajan kehotteen ja **Ostotilausten täsmäytys** -sivun rivit merkitään vihreiksi, koska ne on jo täsmäytetty.  
7. Tästä hetkestä lähtien voit jatkaa työskentelyä manuaalisen täsmäytyksen tekemisessä, mikä tarkoittaa, että voit poistaa osumat, manuaaliset täsmäytykset, nollata täsmäytyksen tai jos et halua tehdä muutoksia, valitse **Käytä ostotilaukseen** -toiminto ja jatka työskentelyä **Ostotilauksen** kanssa. 

> [!NOTE]
> Jos haluat valita **Ostotilausten täsmäytys** -sivun uudelleen **Täsmäytä avustajan avulla** -toiminnon, ohjelma kysyy kuitenkin, haluatko korvata olemassa olevat vastaavuudet, koska kaikki rivit on jo täsmäytetty.  

> [!NOTE]
> Hinnan/kustannuksen analysointi, ja saatavilla oleva määrätarkistus on osa esikäsittelytoimintoa.   

## Sähköisten asiakirjojen tilojen yleiskatsaus

Jos haluat aiempaa paremman yleiskatsauksen yrityksen kaikista sähköisistä asiakirjoista, voit valita **Kirjanpitäjä**-roolikeskuksen, jossa sähköisten asiakirjojen tilat ovat. Siellä voit etsiä sähköistä asiakirjaa koskevat aktiviteetit, joilla on seuraavat tilat:

- **Saapuvat asiakirjat:**

    - Käsitelty
    - Työn alla
    - Virhe


## Katso myös

[Toimintaohje: Sähköisten asiakirjojen määrittäminen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa](finance-how-setup-edocuments.md)    
[Ohjeita sähköisten asiakirjojen käyttämiseen myyntiprosessissa](finance-how-use-edocuments.md)   
[Sähköisten asiakirjojen laajentaminen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Taloushallinto](finance.md)    
[Myynnin laskutus](sales-how-invoice-sales.md)    
[Ostojen kirjaaminen ostolaskujen ja tilausten avulla](purchasing-how-record-purchases.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

