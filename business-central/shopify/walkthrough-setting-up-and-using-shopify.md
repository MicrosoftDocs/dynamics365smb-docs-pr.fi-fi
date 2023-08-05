---
title: Shopify-yhdistimen määrittäminen ja käyttäminen
description: Useita integrointiskenaarioita Shopifyn ja Business Centralin välisen työnkulun esittelyyn
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# Vaihekuvaus: Shopify-yhdistimen määrittäminen ja käyttäminen

Tässä osiossa esitellään joitakin tyypillisiä skenaarioita ja käydään läpi vaiheet, joiden avulla voit testata integroidun [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmän ja Shopify-kaupan välistä työnkulkua ja kouluttaa käyttäjiä sen parissa.

## Vaatimukset 

### Shopify

Tarvitaan:

- Shopify-tili
- Shopify-verkkokauppa

Lisätietoja Shopify-kokeiluversioiden luomisesta ja suositelluista asetuksista on kohdassa [Shopify-tilin luominen ja määrittäminen](shopify-account.md).

### Business Central

Sinulla täytyy olla [!INCLUDE[prod_short](../includes/prod_short.md)] -tili. 

Voit esimerkiksi luoda esittelytilin tai aloittaa kokeiluversion. Lisätietoja on kohdissa [Dynamics 365 Business Central -esittely-ympäristöjen valmistelu](/dynamics365/business-central/dev-itpro/administration/demo-environment) ja [Rekisteröityminen kokeiluversion käyttäjäksi](../trial-signup.md). 

## Business Centralin yhdistäminen Shopify-kauppaan

Suorita [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Kirjoita **Koodi**-kenttään `DEMO1`.
4. Syötä **Shopify URL** -kenttään URL-osoite verkkokauppaan, johon haluat muodostaa yhteyden.
5. Aktivoi **Käytössä**-valitsin ja tarkista ja hyväksy ehdot ja edellytykset.

Määritä Shopify-kauppa seuraavissa vaiheissa kuvatulla tavalla:

1. Ota **Loki käytössä** -valitsin käyttöön.
2. Poista **Salli synkronointi taustalla** -valitsin käytöstä.
3. Valitse **Synkronoi nimike** -kentästä **Shopifyhin**.
4. Valitse **Synkronoi nimikekuvat** -kentästä **Shopifyhin**.
5. Ota **Synkronoi nimikemääritteet** -valitsin käyttöön.
6. Ota **Varastoa seurataan** -valitsin käyttöön.
7. Valitse **Oletusvarastokäytäntö**-kentästä **Estä**.
8. Ota **Luo tuntemattomat asiakkaat automaattisesti** -valitsin käyttöön.
9. Täytä **Asiakasmallin koodi** -kenttä asiaankuuluvalle mallilla.
10. Täytä **Toimituskulutili** ja **Tippitili** tuoton tilillä. Käytä esimerkiksi Yhdysvalloissa arvoa `40100`.
11. Ota **Luo tilaukset automaattisesti** -valitsin käyttöön.

Määritä sijaintien yhdistäminen:

1. Valitse **sijainnit** -toiminto, jolla **Shopify-myymäläsijainnit** avataan.
2. Valitse **Hae Shopify-sijainnit** -toiminto tuodaksesi kaikki Shopifyssa määritetyt sijainnit.
3. Syötä **Sijaintisuodatus**-kenttään `''|EAST|MAIN`.
4. Ota valitun Shopify-sijainnin varaston synkronointi käyttöön poistamalla **Poista käytöstä** -vaihtoehto käytöstä.

## Vaihekuvaus: Tuotteiden myynnin aloittaminen verkossa

### Skenaario

Oletetaan, että haluat kokeilla Shopifya verkkokauppana kuluttamatta liian paljon aikaa asioiden määrittämiseen, varsinkin koska ylläpidät jo nimikkeitäsi [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä oikein. Kun julkaiset Shopify-verkkokauppasi, saat heti uusia asiakkaita, jotka ovat tyytyväisiä kauppaasi ja ostokokemukseensa. Tästä syystä he päättävät jättää tippiä kassalla.

### Vaiheet

Suorita [!INCLUDE[prod_short](../includes/prod_short.md)]issa seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet**, valitse sitten vastaava linkki.
2. Valitse **Lisää nimikkeitä** -toiminto.
3. Kirjoita **Kaupan koodi** -kenttään *DEMO1*.
4. Määritä `CHAIR`-suodatin **Nimikeluokan koodi** -kenttään (Lisää suodatinkenttä tarvittaessa).
5. Valitse **OK** ja odota, kunnes nimikkeiden ja hintojen alustava synkronointi on suoritettu.
6. Valitse **Synkronoi tuotekuvat** -toiminto.
7. Valitse **Synkronoi varasto** -toiminto.

**Shopify-verkkokaupassa**
> [!Tip]  
> Avaa **Shopify-järjestelmänvalvoja** siirtymällä **Shopify-ostoskortti**-sivun **URL**-kentässä määritettyyn URL-osoitteeseen. Valitse sitten **verkkokaupan** myyntikanavan vieressä oleva silmäkuvake, joka sijaitsee **Shopify-järjestelmänvalvoja**-sivupalkissa. 

Avaa tuotekatalogi. Ilmoitus:

* Tuotteiden otsikot, kuvat ja hinnat.
* Saatavuuden ilmaisin (loppuunmyydyille ja varastosta loppuneille tuotteille).

Valitse mikä tahansa myytävä tuote, esimerkiksi `BERLIN Swivel Chair, yellow`. Huomaa, että kuvaus sisältää nimikkeen määritteet.

Valitse **Osta nyt** -painike ja siirry kassalle.

1. Syötä **Sähköposti tai matkapuhelinnumero** -kenttään `cl@contoso.com` (tai sähköpostiosoite, jonka haluat vastaanottavan tilausten ja toimitusten vahvistukset).
2. Kirjoita **Etunimi**- ja **Sukunimi**-kenttiin `Claudia Lawson`.
3. Syötä paikallinen osoite.
4. Valitse **Tallenna nämä tiedot seuraavaa kertaa varten** -valintaruutu.
5. Valitse **Jatka toimitukseen** -painike.
6. Pidä `Standard` toimitustapana ja valitse **Jatka maksu** -painike.
7. Valitse tipiksi `10%`.
8. Syötä **Luottokortti**-kenttään `1`, jos käytät *(for testing) Bogus Gateway* -vaihtoehtoa. Jos käytät *Shopify Paymentsia* testitilassa, syötä `5555 5555 5555 4444`.
9. Täytä **Kortissa oleva nimi** -kenttä.
10. Syötä **Voimassaolon päättymispäivä** -kenttään tämänhetkinen kuukausi/vuosi.
11. Syötä **Suojauskoodi**-kenttään `111`.
12. Valitse **Maksa nyt** -painike.

Suorita [!INCLUDE[prod_short](../includes/prod_short.md)]issa seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-tilaukset** ja valitse sitten vastaava linkki.
2. Valitse **Synkronoi tilaukset Shopifysta** -toiminto.
3. Valitse **OK**.

Tuotu tilaus on valmis käsiteltäväksi.

1. Valitse tuotu tilaus avataksesi **Shopify-tilaus**-ikkunan.
2. Huomaa, että uusi asiakas ja myyntitilaus luodaan.
3. Tutki **Riski**- ja **Toimituskulut**-toimintoja.
4. Valitse **Myyntitilaus**-toiminto avataksesi **Myyntitilaus**-ikkunan. Myyntitilaus on kysyntä, joka voidaan tarvittaessa kattaa kokoonpanolla, tuotannolla tai ostoksella suunnittelumoduulin avulla. Se tukee myös erilaisia varaston käsittelyprosesseja, joilla on toisistaan täysin erilliset tehtävät.
5. Valitse **Avaa uudelleen** -toiminto.
6. Syötä **Agentti**-kenttään `DHL`.
7. Syötä **Kollin seurantanro** -kenttään `123456789`.
8. Valitse ensin **Kirjaa**-toiminto, pidä **Toimitus ja lasku** -vaihtoehto ennallaan ja valitse lopuksi **OK**-painike.

Fyysiset ja taloudelliset tiedot on nyt rekisteröity [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmään. On aika ilmoittaa Shopifylle muutoksista.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Synkronoi toimitukset Shopifyhin** ja valitse sitten vastaava linkki.
2. Valitse **OK**.

Huomaa, että tilauksen tila on nyt **Shopify Adminissa** *Fulfilled*. Voit myös tarkastella toimituksen tietoja ja nähdä seurannan URL-osoitteen. Jos suoritat **Synkronoi tilaukset Shopifysta** -toiminnon uudelleen, tilaus arkistoidaan molempiin järjestelmiin.

## Vaihekuvaus: Asiakkaiden kutsuminen uuteen verkkokauppaasi

### Skenaario

Uuden verkkokauppasi onnistuneen lanseerauksen jälkeen haluat, että nykyiset asiakkaasi vierailevat siellä ja aloittavat tilausten tekemisen.

### Vaiheet

Suorita [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse **DEMO1**-kauppa, jolle haluat synkronoida asiakkaat, avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi asiakkaat** -toiminto.

Huomaa, että asiakkaat tuotiin **Shopify Adminiin**. Avaa joku asiakkaista ja huomioi, että asiakkaan etu- ja sukunimi saadaan **asiakkaan kortin** **Yhteyshenkilön nimi** -kentästä. Yrityksen nimi löytyy oletusosoitteesta, joka on linkitetty asiakkaaseen. Kutsu asiakas valitsemalla **Lähetä tilin kutsu**.

## Vaihekuvaus: Nimikkeiden hallinnan hienosäätö

### Skenaario 

Haluat varmasti tehdä nimikkeiden hallinnan prosesseista joustavampia ja helpommin hallittavia. Haluat parantaa tuotteiden kuvausta ja lisätä uusia tarkistusvaiheita ennen kuin tuotteet julkaistaan loppuasiakkaille.

### Vaiheet

Suorita [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä seuraavat vaiheet:

Valmistele tiedot.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Asiakashintaryhmä** ja valitse sitten vastaava linkki.
2. Lisää uusi hintaryhmä. Kirjoita **Koodi**-kenttään `SHOPIFY`.
3. Sulje **Asiakashintaryhmä**-ikkuna.
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse vastaava linkki.

Valitse nimike **1896-S, Athens Desk** ja suorita seuraavat vaiheet.

1. Valitse **Variantit**-toiminto ja lisää sitten kaksi varianttia: `PREMIUM, Athens Desk, Premium edition` ja `ESSENTIAL, Athens Desk, Essential edition`.
2. Valitse **Lisäteksti**-toiminto ja luo uusi lisäteksti, joka on käypä kaikille kielikoodeille. Kirjoita **Kuvaus**-kenttään `Shopify`. 
3. Lisää seuraava teksti HTML-tunnisteineen: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`.
4. Valitse **Myyntihinnat**-toiminto ja lisää seuraavassa taulukossa esitetyt uudet hinnat:

  |Rivi|**Myynnin tyyppi**|**Myyntikoodi**|Tyyppi|Postinumero|Versiokoodi<br>(lisää kenttä mukautuksen avulla)|Yksikköhinta|
  |------|------------|------------|------------|------------|------------|------------|
  |1|Asiakkaan hintaryhmä|SHOPIFY|Vaihtoehto|1896-S|ESSENTIAL|700|
  |2|Asiakkaan hintaryhmä|SHOPIFY|Nimike|1896-S|PREMIUM|1 000|

5. Valitse **Myyntialennukset**-toiminto ja lisää uusi alennus:

* **Myynnin tyyppi** *Asiakkaan alennusryhmä*
* **Myyntikoodi** *RETAIL*
* **Tyyppi** *Nimike*
* **Koodi** *1896-S*
* **Mittayksikön koodi** *PCS*
* **Rivialennus-%** *10*

6. Valitse **Nimikeviittaukset**-toiminto ja lisää seuraavat rivit:

  |Rivi|**Viittauksen tyyppi**|**Viittauksen nro**|Versiokoodi|
  |------|------------|------------|------------|
  |1|Viivakoodi|77777777|ESSENTIAL|
  |2|Viivakoodi|11111111|PREMIUM|


Valitse nimike **1920-S, ANTWERP Conference Table** ja suorita seuraavat vaiheet.

1. Valitse **Muuta varastoa** ja syötä **Uusi varasto** -kenttään `100` sijainneille *EAST* ja *WEST*. 
2. Valitse **OK**.

Säädä synkronointiasetuksia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse *DEMO1*-kauppa, jolle haluat synkronoida nimikkeet, avataksesi Shopify-ostoskortti-sivun.
3. Valitse **Asiakkaan hintaryhmä** -kentästä *SHOPIFY*.
4. Valitse **Asiakkaan alennusryhmä** -kentästä *RETAIL*.
5. Ota **Synkronoi nimikkeen lisäteksti** -kenttä käyttöön.
6. Valitse **Varastointiyksikön yhdistämismääritykset** -kentästä *Nimikenro + versiokoodi*.
7. Valitse **Luotujen tuotteiden tila** -kentästä *Luonnos*.
8. Valitse **Toiminto poistetuille tuotteille** -kentästä *Tilaksi Arkistoitu*.

Suorita synkronointi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse *DEMO1*-kauppa, jolle haluat synkronoida nimikkeet, avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Tuotteet**-toiminto avataksesi **Shopify-tuotteet**-ikkunan.
4. Valitse **Lisää nimikkeitä** -toiminto.
5. Määritä *TABLE*-suodatin **Nimikeluokan koodi** -kentälle.
6. Valitse **Synkronoi tuotekuvat** -toiminto.
7. Valitse **Synkronoi varasto** -toiminto.

Tuotteet lisätään. Huomaa, että niiden tilaksi määritetään *Luonnos*, joten nimikkeitä ei näytetä Shopify-verkkokaupassa.

1. Valitse rivi, joka sisältää nimikkeen *1920-S, ANTWERP Conference Table*. Syötä **SEO:n otsikko**-kenttään `Rectangular meeting table Antwerp, 10 seats, black`.
2. Valitse **Tila**-kentästä *Aktiivinen*.
3. Valitse rivi, joka sisältää nimikkeen *1906-S, ATHENS, Mobile Pedestal*, ja valitse sitten **Poista**-toiminto.

Huomaa, että kaikilla tuotteilla on eri tilat **Shopify Adminissa**.

* *ANTWERP Conference Table* on *aktiivinen*, koska muutimme sen tilaa **Shopify-tuote**-ikkunassa.
* *ATHENS Desk* on *luonnos*, koska määritimme kaikkien lisättyjen tuotteiden oletusarvoiseksi tilaksi *Luonnos*.
* *ATHENS Mobile Pedestal* on *arkistoitu*, koska määritimme kaupan kohdistamaan poistetut tuotteet *Arkistoitu*-tilaan.

Huomaa, että ANTWERP Conference Table -nimikkeen varasto on 100, koska määritimme järjestelmän käyttämään varastoa vain kahdesta sijainnista: MAIN ja EAST. Muissa sijainneissa (WEST) olevaa varastoa ei huomioida.

* Avaa *ANTWERP Conference Table*, huomioi **Mukautettu tyyppi**-, **Toimittaja**-, **Paino**-, **Kustannus per nimike** -kentät sekä **Hakukonelistauksen esikatselu** -osio.
* Avaa *Athens Desk*, siirry alas **Variantit**-osioon ja huomioi, miten **Varastointiyksikkö**-kenttä on täytetty.
* Valitse **Muokkaa** tarkastaaksesi viivakoodin ja hinnat.
* Muuta *Athens Desk* -nimikkeen tilaksi *Aktiivinen* ja valitse **Esikatsele**-toiminto.

Avaa tuotekatalogi **Shopify-verkkokaupassa** ja etsi *ATHENS Desk* -tuote. Huomaa, että saatavilla on eri vaihtoehtoja. Hinnat vaihtelevat eri vaihtoehdoissa. Kiinnitä huomiota alennustietoihin.

## Vaihekuvaus: Nimikkeiden tuominen Shopifysta

### Skenaario 

Sinulla on jo menestyvä verkkokauppa ja haluaisit aloittaa [!INCLUDE[prod_short](../includes/prod_short.md)]in käyttämisen liiketoiminnan hallintaohjelmistona. Haluat tuoda mahdollisimman paljon tietoja Shopifysta. 

### Vaiheet

Tämä on jatkoa [Vaihekuvaus: Tuotteiden myynnin aloittaminen verkossa](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) -osiolle. Voit myös kokeilla käyttää omia tietojasi, esimerkiksi Shopify-kauppaasi tai -eristysympäristöäsi.

Suorita [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä seuraavat vaiheet:

#### Valmistele tiedot

1. Vaihda maksuttomaan 30 päivän kokeiluversioon ilman näytetietoja. Lisätietoja on kohdassa [Omien tietojen lisääminen tyhjään kokeiluyritykseen](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat** ja valitse sitten vastaava linkki.
3. Valitse **Uusi**-toiminto.
4. Kirjoita **Koodi**-kenttään `DEMO2`.
5. Syötä **Shopify URL** -kenttään URL-osoite verkkokauppaan, johon haluat muodostaa yhteyden.
6. Aktivoi **Käytössä**-valitsin ja tarkista ja hyväksy ehdot ja edellytykset.

Määritä Shopify-kauppa seuraavissa vaiheissa kuvatulla tavalla:

7. Ota **Loki käytössä** -valitsin käyttöön.
8. Poista **Salli synkronointi taustalla** -valitsin käytöstä.
9. Valitse **Synkronoi nimike** -kentästä **Shopifysta**.
5. Ota **Luo tuntemattomat nimikkeet automaattisesti** -valitsin käyttöön.
11. Täytä **Nimikemallin koodi** -kenttä asiaankuuluvalle mallilla.
12. Valitse **Synkronoi nimikekuvat** -kentästä **Shopifysta**.
13. Valitse **Asiakkaan tuonti Shopifysta** -kentästä **Kaikki asiakkaat**.
14. Ota **Luo tuntemattomat asiakkaat automaattisesti** -valitsin käyttöön.
15. Täytä **Asiakasmallin koodi** -kenttä asiaankuuluvalle mallilla.
16. Täytä **Kuljetusmaksutili** ja **Tippitili** tuoton tilillä. Käytä esimerkiksi Yhdysvalloissa arvoa `40100`.
17. Ota **Luo tilaukset automaattisesti** -valitsin käyttöön.

#### Suorita synkronointi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse *DEMO2*-kauppa, jolle haluat synkronoida tiedot, avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi tuotteet** -toiminto.
4. Valitse **Synkronoi tuotekuvat** -toiminto.
5. Valitse **Synkronoi asiakkaat** -toiminto.

### Tulokset

* Shopify-tuotteet tuodaan. Jos haluat vahvistaa tulokset, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-tuotteet** ja valitse vastaava linkki.
* Nimikkeet ja kuvat luodaan. Jos haluat vahvistaa tulokset, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Nimike** ja valitse vastaava linkki.
* Shopify-asiakkaat tuodaan. Jos haluat vahvistaa tulokset, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-asiakkaat** ja valitse vastaava linkki.
* Asiakkaat luodaan. Jos haluat vahvistaa tulokset, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Asiakkaat** ja valitse vastaava linkki.


## Katso myös

[Shopify-yhdistimen käytön aloittaminen](get-started.md)  
