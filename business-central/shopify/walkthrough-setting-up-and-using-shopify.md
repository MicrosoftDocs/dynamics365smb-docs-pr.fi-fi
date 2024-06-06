---
title: Shopify-yhdistimen määrittäminen ja käyttäminen
description: Useita integrointiskenaarioita Shopifyn ja Business Centralin välisen työnkulun esittelyyn
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# Vaihekuvaus: Shopify-yhdistimen määrittäminen ja käyttäminen

Tässä osiossa esitellään joitakin tyypillisiä skenaarioita ja käydään läpi vaiheet, joiden avulla voit testata integroidun [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmän ja Shopify-kaupan välistä työnkulkua ja kouluttaa käyttäjiä sen parissa.

## Vaatimukset 

### Shopify

Tarvitaan:

- Shopify-tili
- Shopify-verkkokauppa

Lisätietoja Shopify-kokeiluversioiden luomisesta ja suositelluista asetuksista on kohdassa [Luo ja määritä Shopify-tili](shopify-account.md).

### Business Central

Sinulla täytyy olla [!INCLUDE[prod_short](../includes/prod_short.md)] -tili. 

Voit esimerkiksi luoda esittelytilin tai aloittaa kokeiluversion. Lisätietoja on kohdissa [Dynamics 365 Business Central -esittely-ympäristöjen valmistelu](/dynamics365/business-central/dev-itpro/administration/demo-environment) ja [Rekisteröityminen kokeiluversion käyttäjäksi](../trial-signup.md). 

## Business Centralin yhdistäminen Shopify-kauppaan

Toimi [!INCLUDE[prod_short](../includes/prod_short.md)]issa seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Kirjoita **Koodi**-kenttään `DEMO1`.
4. Syötä **Shopify URL** -kenttään URL-osoite verkkokauppaan, johon haluat muodostaa yhteyden.
5. Aktivoi **Käytössä**-valitsin ja tarkista ja hyväksy sitten ehdot ja edellytykset.

Seuraa näitä ohjeita määrittääksesi Shopify-kaupan:

1. Poista **Salli synkronointi taustalla** -valitsin käytöstä.
2. Valitse *Synkronoi nimike* -kentästä **Shopifyhin**.
3. Valitse *Synkronoi nimikekuvat* -kentästä **Shopifyhin**.
4. Ota **Synkronoi nimikemääritteet** -valitsin käyttöön.
5. Ota **Varastoa seurataan** -valitsin käyttöön.
6. Valitse *Oletusvarastokäytäntö*-kentästä **Estä**.
7. Ota **Luo tuntemattomat asiakkaat automaattisesti** -valitsin käyttöön.
8. Täytä **Asiakas-/yritysmallin koodi** -kenttä asiaankuuluvalle mallilla.
9. Täytä **Toimituskulutili** ja **Tippitili** tuoton tilillä. Käytä esimerkiksi Yhdysvalloissa arvoa `40210`.
10. Ota **Luo tilaukset automaattisesti** -valitsin käyttöön.
11. Ota **myyntitilausten automaattisten vapautusten** vaihto pois käytöstä.

Määritä sijaintien yhdistäminen:

1. Valitse **sijainnit** -toiminto, jolla **Shopify-myymäläsijainnit** avataan.
2. Valitse **Hae Shopify-sijainnit** -toiminto tuodaksesi kaikki Shopifyssa määritetyt sijainnit. Valitse tapahtuma, jonka **on ensisijainen** -valinta on valittu.
3. Syötä **Sijaintisuodatus**-kenttään `''|EAST|MAIN`.
4. Valitse *Arvioitu käytettävissä oleva saldo tänään* **Varastolaskenta**-kentästä ottaaksesi varastosynkronoinnin käyttöön valitussa Shopify-sijainnissa.

## Vaihekuvaus: Tuotteiden myynnin aloittaminen verkossa

### Skenaario

Oletetaan, että haluat kokeilla Shopifya verkkokauppana kuluttamatta liian paljon aikaa määritykseen, varsinkin koska ylläpidät jo nimikkeitäsi [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä oikein. Kun julkaiset Shopify-verkkokauppasi, saat heti uusia asiakkaita, jotka ovat tyytyväisiä kauppaasi ja ostokokemukseensa. Tästä syystä he päättävät jättää tippiä kassalla.

### Vaiheet

Seuraa näitä ohjeita [!INCLUDE[prod_short](../includes/prod_short.md)]-ohjelmassa:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet** ja valitse vastaava linkki.
2. Valitse **Lisää nimikkeet**.
3. Kirjoita **Kaupan koodi** -kenttään `DEMO1`.
4. Määritä `CHAIR`-suodatin **Nimikeluokan koodi** -kentälle.
5. Ota **Synkronoi tuotekuvat** -valitsin käyttöön.
6. Ota **Synkronoi varasto** -valitsin käyttöön.
7. Valitse **OK** ja odota, kunnes nimikkeiden, hintojen, kuvien ja varaston alustava synkronointi on suoritettu.

**Shopify-verkkokaupassa**:
> [!Tip]  
> Avaa **Shopify-järjestelmänvalvoja** siirtymällä **Shopify-ostoskortti**-sivun **URL**-kentässä määritettyyn URL-osoitteeseen. Valitse **verkkokaupan** myyntikanavan vieressä oleva silmäkuvake, joka sijaitsee **Shopify-järjestelmänvalvoja**-sivupalkissa. 

Avaa tuotekatalogi. Ilmoitus:

* Tuotteiden otsikot, kuvat ja hinnat.
* Saatavuuden ilmaisin (loppuunmyydyille ja varastosta loppuneille tuotteille).

Valitse mikä tahansa myytävä tuote, esimerkiksi `BERLIN Swivel Chair, yellow`. Huomaa, että kuvaus sisältää nimikkeen määritteet.

Valitse **Osta nyt** ja siirry kassalle.

1. Syötä **Sähköposti tai matkapuhelinnumero** -kenttään `cl@contoso.com` (tai sähköpostiosoite, jonka haluat vastaanottavan tilausten ja toimitusten vahvistukset).
2. Kirjoita **Etunimi**- ja **Sukunimi**-kenttiin `Claudia Lawson`.
3. Syötä paikallinen osoite.
4. Valitse **Tallenna nämä tiedot seuraavaa kertaa varten** -valintaruutu.
6. Säilytä toimitustapana *vakio*.
8. Syötä **Luottokortin numero** -kenttään `1`, jos käytät *(for testing) Bogus Gateway* -vaihtoehtoa. Jos käytät *Shopify Paymentsia* testitilassa, syötä `5555 5555 5555 4444`.
9. Täytä **Kortissa oleva nimi** -kenttä.
10. Syötä **Voimassaolon päättymispäivä** -kenttään tämänhetkinen kuukausi/vuosi.
11. Syötä **Suojauskoodi**-kenttään `111`.
7. Valinnainen: Valitse tipiksi `10%`.
8. 12. Valitse **Maksa nyt**.

Suorita [!INCLUDE[prod_short](../includes/prod_short.md)]issa seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tilaukset** ja valitse sitten vastaava linkki.
2. Valitse **Synkronoi tilaukset Shopifysta** -toiminto.
3. Valitse **OK**.

Tuotu tilaus on valmis käsiteltäväksi.

1. Valitse tuotu tilaus avataksesi **Shopify-tilaus**-ikkunan.
2. Huomaa, että uusi asiakas ja myyntitilaukset luodaan.
3. Tutki **Riski**- ja **Toimituskulut**-toimintoja.
4. Valitse **Myyntitilaus** avataksesi **Myyntitilaus**-ikkunan. Myyntitilaus on kysyntä, joka voidaan tarvittaessa kattaa kokoonpanolla, tuotannolla tai ostoksella suunnittelumoduulin avulla. Se tukee myös erilaisia varaston käsittelyprosesseja, joilla on toisistaan täysin erilliset tehtävät.
6. Syötä **Agentti**-kenttään `DHL`. Avaa tilaus tarvittaessa uudelleen valitsemalla **Avaa uudelleen** -toiminto.
7. Syötä **Kollin seurantanro** -kenttään `123456789`.
8. Valitse ensin **Kirjaa**, pidä **Toimitus ja lasku** -vaihtoehto ennallaan ja valitse **OK**.

Fyysiset ja taloudelliset tiedot on nyt rekisteröity [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmään. On aika ilmoittaa Shopifylle muutoksista.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Synkronoi toimitukset Shopifyhin** ja valitse sitten vastaava linkki.
2. Valitse **OK**.

Huomaa, että tilauksen tila on nyt **Shopify Adminissa** *Fulfilled*. Voit myös tarkastella toimituksen tietoja ja nähdä seurannan URL-osoitteen. Jos suoritat **Synkronoi tilaukset Shopifysta** -toiminnon uudelleen, tilaus arkistoidaan molempiin järjestelmiin.

## Vaihekuvaus: Asiakkaiden lisääminen uuteen verkkokauppaasi

### Skenaario

Uuden verkkokauppasi onnistuneen lanseerauksen jälkeen haluat, että nykyiset asiakkaasi vierailevat siellä ja aloittavat tilausten tekemisen. Shopify-suunnitelmasta ja prosessista riippuen voit kokeilla B2B- ja DTC-virtoja.

### DTC-vaiheet

Toimi [!INCLUDE[prod_short](../includes/prod_short.md)]issa seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-asiakkaat** ja valitse vastaava linkki.
2. Valitse **Lisää asiakkaita**.
3. Kirjoita **Kaupan koodi** -kenttään `DEMO1`.
4. Määritä kohteen **Nro** suodattimeksi `20000` -kentässä.
5. Valitse **OK** ja odota, kunnes asiakkaiden alustava synkronointi on suoritettu.

Huomaa, että asiakas tuotiin **Shopify Adminiin**. Avaa asiakkaat ja huomioi, että asiakkaan etu- ja sukunimi saadaan **asiakkaan kortin** **Yhteyshenkilön nimi** -kentästä. Yrityksen nimi löytyy oletusosoitteesta, joka on linkitetty asiakkaaseen. Jos käytät *Klassisia asiakastilejä*, voit valita **Lähetä asiakaskutsu** kutsuaksesi asiakkaan. *Uudet asiakastilit* eivät vaadi salasanaa, jotta asiakkaat voivat kirjautua sisään, vaan Shopify sallii asiakkaiden kirjautua sisään käyttämällä kertakäyttöistä 6-numeroista vahvistuskoodia, joka lähetetään sähköpostitse. 

### B2B-vaiheet

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Toimi [!INCLUDE[prod_short](../includes/prod_short.md)]issa seuraavasti:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-yritykset** ja valitse vastaava linkki.
2. Valitse **Lisää yritys**.
3. Kirjoita **Kaupan koodi** -kenttään `DEMO1`.
4. Määritä kohteen **Nro** suodattimeksi `30000` -kentässä.
5. Valitse **OK** ja odota, kunnes asiakkaiden alustava synkronointi on suoritettu.

Huomaa **Shopify-järjestelmänvalvojassa**, että sekä yritys että asiakas on tuotu. Avaa asiakkaat ja huomaa Yritys-tietoruutu, jossa on linkki Yritykseen, sijaintiin ja määritettyihin käyttöoikeuksiin. Kutsu asiakas valitsemalla **[...]** **Yritys-tietoruudussa ja valitsemalla sitten **Lähetä B2B-käyttösähköposti**.

## Vaihekuvaus: Nimikkeiden hallinnan hienosäätö

### Skenaario 

Haluat varmasti tehdä nimikkeiden hallinnan prosesseista joustavampia ja helpommin hallittavia. Haluat parantaa tuotteiden kuvausta ja lisätä uusia tarkistusvaiheita ennen kuin tuotteet julkaistaan kaikille asiakkaille.

### Vaiheet

Toimi [!INCLUDE[prod_short](../includes/prod_short.md)]issa seuraavasti:

Valmistele tiedot.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Asiakashintaryhmä** ja valitse sitten vastaava linkki.
2. Lisää uusi hintaryhmä. Kirjoita **Koodi**-kenttään `SHOPIFY`.
3. Sulje **Asiakashintaryhmä**-ikkuna.
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse vastaava linkki.
5. Valitse nimike *1896-S, Athens Desk* ja seuraa sitten näitä vaiheita.

6. Valitse **Variantit**-toiminto ja lisää sitten kaksi varianttia: `PREMIUM, Athens Desk, Premium edition` ja `ESSENTIAL, Athens Desk, Essential edition`.
7. Valitse **Markkinointiteksti**-toiminto ja käytä **Luo luonnos Copilotin avulla** -toimintoa, kun haluat luovaa ja kiinnostavaa tekstiä. Jos markkinointitekstiehdotus ei ole käytössä, syötä vain: '**Yksinkertainen tyylikäs muotoilu** sulautuu mihin tahansa kokoonpanoon. *Saatavilla kahtena versiona.* 
8. Valitse **Myyntihinnat**-toiminto ja lisää seuraavassa taulukossa esitetyt uudet hinnat:

   |Rivi|Myynnin tyyppi|Myyntikoodi|Tyyppi|Postinumero|Versiokoodi<br>(lisää kenttä mukautuksen avulla)|Yksikköhinta|
   |------|------------|------------|------------|----------------|------------|------------|
   |1|Asiakkaan hintaryhmä|SHOPIFY|Vaihtoehto|1896-S|ESSENTIAL|700|
   |2|Asiakkaan hintaryhmä|SHOPIFY|Vaihtoehto|1896-S|PREMIUM|1 000|

9. Valitse **Myyntialennukset**-toiminto ja lisää uusi alennus:

   * **Myynnin tyyppi** *Asiakkaan alennusryhmä*
   * **Myyntikoodi** *RETAIL*
   * **Tyyppi** *Nimike*
   * **Koodi** *1896-S*
   * **Mittayksikön koodi** *PCS*
   * **Rivialennus-%** *10*

10. Valitse **Nimikeviittaukset**-toiminto ja lisää seuraavat rivit:

   |Rivi|Viittauksen tyyppi|Viittauksen nro|Versiokoodi|
   |------|------------|------------|------------|
   |1|Viivakoodi|77777777|ESSENTIAL|
   |2|Viivakoodi|11111111|PREMIUM|

11. Valitse nimike *1920-S, ANTWERP Conference Table* ja seuraa sitten näitä vaiheita:
12. Valitse **Muuta varastoa** ja syötä **Uusi varasto** -kenttään `100` sijainneille *EAST* ja *WEST*. 
13. Valitse **OK**.

Säädä synkronointiasetuksia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse `DEMO1`-kauppa, jolle haluat synkronoida nimikkeet, avataksesi **Shopify-ostoskortti**-sivun.
3. Ota **Synkronoi markkinointiteksti** -kenttä käyttöön.
4. Valitse **Varastointiyksikön yhdistämismääritykset** -kentästä *Nimikenro + versiokoodi*.
5. Valitse *Oletusvarastokäytäntö*-kentästä **Jatka**.
6. Valitse **Luotujen tuotteiden tila** -kentästä *Luonnos*.
7. Valitse **Toiminto poistetuille tuotteille** -kentästä *Tilaksi Arkistoitu*.
8. Valitse **Asiakkaan hintaryhmä** -kentästä *SHOPIFY*.
9. Valitse **Asiakkaan alennusryhmä** -kentästä *RETAIL*.
 
Suorita synkronointi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse `DEMO1`-kauppa, jolle haluat synkronoida nimikkeet, avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Tuotteet** avataksesi **Shopify-tuotteet**-ikkunan.
4. Valitse **Lisää nimikkeitä** -toiminto.
5. Määritä *TABLE|DESK*-suodatin **Nimikeluokan koodi** -kentälle.
6. Ota **Synkronoi tuotekuvat** -valitsin käyttöön.
7. Ota **Synkronoi varasto** -valitsin käyttöön.
8. Valitse **OK** ja odota, kunnes nimikkeiden, hintojen, kuvien ja varaston alustava synkronointi on suoritettu.

Tuotteet lisätään. Huomaa, että niiden tilaksi määritetään *Luonnos*, joten nimikkeitä ei näytetä Shopify-verkkokaupassa.

1. Valitse rivi, joka sisältää nimikkeen *1920-S, ANTWERP Conference Table*. Syötä **SEO:n otsikko**-kenttään `Rectangular meeting table Antwerp, 10 seats, black`.
2. Valitse **Tila**-kentästä *Aktiivinen*.
3. Valitse rivi, joka sisältää nimikkeen *1906-S, ATHENS, Mobile Pedestal*, ja valitse sitten **Poista**.

Huomaa, että kaikilla tuotteilla on eri tilat **Shopify Adminissa**.

* *ANTWERP Conference Table* on *aktiivinen*, koska muutimme sen tilaa **Shopify-tuote**-ikkunassa.
* *ATHENS Desk* on *luonnos*, koska määritimme kaikkien lisättyjen tuotteiden oletusarvoiseksi tilaksi *Luonnos*.
* *ATHENS Mobile Pedestal* on *arkistoitu*, koska määritimme kaupan kohdistamaan poistetut tuotteet *Arkistoitu*-tilaan.

Huomaa, että ANTWERP Conference Table -nimikkeen varasto on 100, koska määritimme järjestelmän käyttämään varastoa vain kahdesta sijainnista: MAIN ja EAST. Toisessa sijainnissa (WEST) olevaa varastoa ei huomioida.

* Avaa *ANTWERP Conference Table*, huomioi **Mukautettu tyyppi**-, **Toimittaja**-, **Paino**- ja **Kustannus per nimike** -kentät sekä **Hakukonelistauksen esikatselu** -osio.
* Avaa *Athens Desk*, siirry alas **Variantit**-osioon ja huomioi, miten **Varastointiyksikkö**-kenttä on täytetty.
* Valitse **Muokkaa** tarkastaaksesi viivakoodin ja hinnat.
* Muuta *Athens Desk* -nimikkeen tilaksi *Aktiivinen* ja valitse **Esikatsele**.

Avaa tuotekatalogi **Shopify-verkkokaupassa** ja etsi *ATHENS Desk* -tuote. Huomaa, että saatavilla on eri vaihtoehtoja. Hinnat vaihtelevat eri vaihtoehdoissa. Kiinnitä huomiota alennustietoihin.

### B2B:n lisävaiheet

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Voit määrittää yhdistimen luomaan ja liittämään katalogin vietyjä yrityksiä varten automaattisesti. Alla olevat vaiheet ovat hyödyllisiä, jos haluat tarkemman hallinnan siitä, mitä B2B-asiakkaille on saatavilla.

Luo ja liitä katalogi **Shopify-järjestelmänvalvojassa**.

1. Valitse **Shopify-järjestelmänvalvojan** sivupalkissa **Tuotteet** ja sitten **Luettelot**.
2. Luo luettelo tiettyjä tuotteita varten. Syötä otsikko "B2B". 
3. Valitse **Hallitse** ja sitten **Tuotteiden ja hinnoittelun hallinta**.
4. Valitse *Poissuljettu* suodatin, etsi *ATHERN-työpöytä* ja valitse **Sisällytä luetteloon**.
5. Valitse **Shopify-järjestelmänvalvojan** sivupalkissa **Asiakkaat** ja sitten **Yritykset**.
6. Valitse *Kuvataidekoulu* ja valitse **[...]** ja lisää sitten **Lisää luettelot** ja aiemmin luotu *B2B*-luettelo.

Toimi [!INCLUDE[prod_short](../includes/prod_short.md)]issa seuraavasti:

Valmistele tiedot.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse vastaava linkki.

2. Valitse nimike **1896-S, Athens Desk** ja seuraa sitten näitä vaiheita.

3. Valitse **Myyntialennukset**-toiminto ja lisää uusi alennus:

   * **Myynnin tyyppi** *Asiakkaan alennusryhmä*
   * **Myyntikoodi** *LARGE ACC*
   * **Tyyppi** *Nimike*
   * **Koodi** *1896-S*
   * **Mittayksikön koodi** *PCS*
   * **Rivialennus-%** *25*

4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-luettelot** ja valitse vastaava linkki.
5. Valitse **Hae luettelot**.
6. Kirjoita **Kaupan koodi** -kenttään `DEMO1`.
7. Valitse *B2B*-luettelo -niminen tapahtuma, jonka hinnat haluat synkronoida.
8. Ota käyttöön **synkronointihinnat**-valinta.
9. Valitse **Asiakkaan hintaryhmä** -kentästä *SHOPIFY*.
10. Valitse **Asiakkaan alennusryhmä** -kentästä *LARGE ACC*.
11. Valitse **Synkronoi hinnat** ja odota, kunnes hintojen synkronointi on suoritettu.

Tutki *B2B*-luettelon hintoja **Shopify-järjestelmänvalvojassa**.

Avaa tuotekatalogi **Shopify-verkkokaupassa** ja etsi *ATHENS Desk* -tuote. Huomaa, että hinnat ovat alennustietoja.

## Vaihekuvaus: Yksittäisen ostajan ja yrityksen edustajan tilauksen synkronointi
Tämä on jatkoa [Vaihekuvaus: Tuotteiden myynnin aloittaminen verkossa](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) -osiolle. Voit myös kokeilla käyttää omia tietojasi, esimerkiksi Shopify-kauppaasi tai -eristysympäristöäsi.

Yksittäinen ostaja

1. **Shopify-verkkokaupassa**. Valitse **Asiakas**-kuvake. Syötä sähköpostiosoite, johon sinulla on käyttöoikeus.
2. Kirjaudu sisään käyttämällä kuusinumeroista vahvistuskoodia, joka lähetettiin syöttämääsi sähköpostiin.
3. Tutustu tuotekatalogiin ja tarkastele kaikkia tuotteita, joilla on vähittäishintoja.
4. Valitse Olennainen variantti ja valitse **Osta se nyt** ja jatka kassalle.
5. Täytä **Etunimi**- ja **Sukunimi**-kentät.
6. Syötä paikallinen osoite.
7. Säilytä toimitustapana *vakio*.
8. Syötä **Luottokortin numero** -kenttään `1`, jos käytät *(for testing) Bogus Gateway* -vaihtoehtoa. Jos käytät *Shopify Paymentsia* testitilassa, syötä `5555 5555 5555 4444`.
9. Syötä **Voimassaolon päättymispäivä** -kenttään tämänhetkinen kuukausi/vuosi.
10. Syötä **Suojauskoodi**-kenttään `111`.
11. Täytä **Kortissa oleva nimi** -kenttä.
12. Valitse **Maksa nyt**.
 
Yrityksen edustaja

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. **Shopify-järjestelmänvalvojassa**.
2. Valitse **Shopify-järjestelmänvalvojan** sivupalkissa **Asiakkaat** ja sitten **Yritykset**.
3. Avaa *Kuvataidekoulun* tapahtuma.
4. Valitse **[...]** **Kuvataidekoulun** tietoruudusta, **muokkaa maksuehtoja** ja valitse *Erääntyvä täydennys*.
5. Valitse **[...]** **Asiakas**-tietoruudussa ja sitten **Lisää asiakas** ja lisää se sähköpostilla, jota käytit aiemmin kauppaan kirjautumiseen.
6. **Shopify-verkkokaupassa**. Valitse **Asiakas**-kuvake. Syötä sähköpostiosoite, johon sinulla on käyttöoikeus.
7. Kirjaudu sisään käyttämällä kuusinumeroista vahvistuskoodia, joka lähetettiin syöttämääsi sähköpostiin.
8. Tutustu tuotekatalogiin, niin näet vain ne *B2B*-luetteloon lisätyt tuotteet, joilla on erityishintoja vähittäiskaupassa.
9. Valitse Olennainen variantti ja valitse **Osta se nyt** ja jatka kassalle.
10. Huomaa, että tili, Toimitusasiakas, maksutapa on täytetty.
11. Täytä viitatun **Ostotilausnumeron** tietoihin `PO-12345`.
12. Valitse **Lähetä tilaus**.
 
Suorita [!INCLUDE[prod_short](../includes/prod_short.md)]issa seuraavat vaiheet:

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tilaukset** ja valitse sitten vastaava linkki.
2. Valitse **Synkronoi tilaukset Shopifysta** -toiminto.
3. Valitse **OK**.

Tuotu tilaus on valmis käsiteltäväksi.

1. Valitse tuotu tilaus avataksesi **Shopify-tilaus**-ikkunan.
2. Huomaa, että vaikka molemmat tilaukset on lähettänyt sama henkilö, ne on linkitetty kahteen eri asiakkaaseen. 
3. Yrityksen puolesta lähetetyssä tilauksessa näkyy arvo **Ostotilausnumero**-kentässä, joka siirretään myös luodun myyntiasiakirjan **Ulkoisen asiakirjan nro** -kenttään.
4. Koska määritimme B2B-yrityksen käsittelemään maksuja Shopifyn ulkopuolella, **Taloudellinen tila** on *Odottaa*. Kun olet vastaanottanut maksun, valitse **Merkitse maksetuksi** -toiminto. Taloudellinen tila päivitetään Shopifyssa. 

## Vaihekuvaus: Nimikkeiden, asiakkaiden, yritysten tuominen Shopifysta

### Skenaario 

Sinulla on jo menestyvä verkkokauppa ja haluaisit aloittaa [!INCLUDE[prod_short](../includes/prod_short.md)]in käyttämisen liiketoiminnan hallintaohjelmistona. Haluat tuoda mahdollisimman paljon tietoja Shopifysta. 

### Vaiheet

Tämä on jatkoa toiminnoille [Vaihekuvaus: Tuotteiden myynnin aloittaminen verkossa](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) ja [Vaihekuvaus: Lisää asiakkaasi uuteen verkkokauppaasi](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). Voit myös kokeilla käyttää omia tietojasi, esimerkiksi Shopify-kauppaasi tai -eristysympäristöäsi.

Noudata seuraavia vaiheita [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

#### Valmistele tiedot

1. Vaihda maksuttomaan 30 päivän kokeiluversioon ilman näytetietoja. Lisätietoja on kohdassa [Omien tietojen lisääminen tyhjään kokeiluyritykseen](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat** ja valitse sitten vastaava linkki.
3. Valitse **Uusi**.
4. Kirjoita **Koodi**-kenttään `DEMO2`.
5. Syötä **Shopify URL** -kenttään URL-osoite verkkokauppaan, johon haluat muodostaa yhteyden.
6. Aktivoi **Käytössä**-valitsin ja tarkista ja hyväksy sitten ehdot ja edellytykset.

Määritä Shopify-kauppa seuraavassa kuvatulla tavalla:

1. Poista **Salli synkronointi taustalla** -valitsin käytöstä.
2. Valitse *Synkronoi nimike* -kentästä **Shopifysta**.
3. Ota **Luo tuntemattomat nimikkeet automaattisesti** -valitsin käyttöön.
4. Täytä **Nimikemallin koodi** -kenttä asiaankuuluvalle mallilla.
5. Valitse *Synkronoi nimikekuvat* -kentästä **Shopifysta**.
6. Valitse **Varastointiyksikön yhdistämismääritykset** -kentästä *Nimikenro + versiokoodi*.
7. Valitse *Asiakkaan tuonti Shopifysta* -kentästä **Kaikki asiakkaat**.
8. Ota **Luo tuntematon asiakas automaattisesti** -valitsin käyttöön.
9. Täytä **Asiakas-/yritysmallin koodi** -kenttä asiaankuuluvalle mallilla.
10. Valitse *Yrityksen tuonti Shopifysta* -kentästä **Kaikki asiakkaat**.
11. Ota **Luo tuntemattomat yritykset automaattisesti** -valitsin käyttöön.

#### Suorita synkronointi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse *DEMO2*-kauppa, jolle haluat synkronoida tiedot, avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi tuotteet**.
4. Valitse **Synkronoi tuotekuvat**.
5. Valitse **Synkronoi asiakkaat**.
6. Valitse **Synkronoi yritykset**

### Tulokset

* Shopify-tuotteet tuodaan. Jos haluat vahvistaa tulokset, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet** ja valitse vastaava linkki.
* Nimikkeet ja kuvat luodaan. Jos haluat vahvistaa tulokset, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimike** ja valitse vastaava linkki.
* Shopify-asiakkaat tuodaan. Jos haluat vahvistaa tulokset, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-asiakkaat** ja valitse vastaava linkki.
* Shopify-yritykset tuodaan. Jos haluat vahvistaa tulokset, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-yritykset** ja valitse vastaava linkki.
* Asiakkaat luodaan. Jos haluat vahvistaa tulokset, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Asiakkaat** ja valitse vastaava linkki.


## Katso myös

[Shopify-yhdistimen käytön aloittaminen](get-started.md)  
