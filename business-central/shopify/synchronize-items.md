---
title: Synkronoi nimikkeet ja varasto
description: Määritä ja suorita nimikkeiden synkronoinnit Shopifyn ja Business Centralin välillä
ms.date: 11/17/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30116, 30117, 30126, 30127,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Synkronoi nimikkeet ja varasto

**Nimikkeet** [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa vastaavat *tuotteita* Shopifyssa ja niihin kuuluu fyysisiä tavaroita, digitaalisia latauksia, palveluja ja lahjakortteja, joita myyt. On kaksi pääasiallista syytä synkronoida nimikkeet:

1. Tietojen hallinta tapahtuu ensisijaisesti [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa. Sinun täytyy viedä kaikki tiedot sieltä Shopifyhin ja tehdä niistä näkyviä. Voit viedä nimikkeen nimen, kuvauksen, kuvan, hinnat, saatavuuden, variantit, toimittajan tiedot ja viivakoodin. Kun ne on viety, voit tarkastella nimikkeitä tai tehdä ne näkyviksi heti.
2. Kun tilaus Shopifysta tuodaan, nimikkeen tiedot ovat olennaisia asiakirjan käsittelemisessä [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

Edeltävät kaksi skenaariota ovat aina käytössä.

Kolmas skenaario on tietojen hallinta Shopify mutta kyseisten nimikkeiden tuonti joukkona [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Tämä skenaario voi olla hyödyllinen tiedonsiirtotapahtumissa, kuten kun aiemmin luotu verkkokauppa halutaan yhdistää uuteen [!INCLUDE[prod_short](../includes/prod_short.md)] -ympäristöön.

## Määritä nimikkeiden synkronointivaltuudet

1. Valitse haku ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake ja kirjoita **Shopify-kauppa**. Avaa myymälä, jolle haluat määrittää nimikkeen synkronoinnin.
2. Valitse haluamasi vaihtoehdot **synkronointikohde**-kentästä.

   Asetukset kuvaillaan seuraavassa taulukossa.

|Asetus|Kuvaus|
|------|-----------|
|**Tyhjä**| Tuotteet tuodaan yhdessä tilausten tuonnin kanssa. Tuotteet viedään Shopifyhin, jos käyttäjä suorittaa **Lisää nimike** -toiminnon **Shopify-tuotteet** -sivulla. Tämä valinta on oletusprosessi.|
|**Shopifyhin**| Valitse tämä vaihtoehto, jos aiot päivittää nimikkeet manuaalisesti **Lisää nimike** -toiminnon käynnistämän synkronoinnin jälkeen **Synkronoi tuote** -toiminnolla tai toistuvien päivitysten työjonon kautta. Muista ottaa käyttöön **voi päivittää Shopify-tuotetta** -kenttä. Jos se ei ole käytössä, se vastaa **tyhjää** (oletusprosessi)-asetusta. Lue lisää [Nimikkeiden vienti Shopifyhin](synchronize-items.md#export-items-to-shopify) -osasta.|
|**Lähettäjä Shopify**| Valitse tämä vaihtoehto, jos aiot tuoda tuotteita Shopifysta joukkona, joko manuaalisesti käyttämällä **Synkronoi tuote** -toimintoa tai työjonon kautta toistuvia päivityksiä varten. Lue lisää [Nimikkeiden tuonti Shopifysta](synchronize-items.md#import-items-from-shopify) -osasta.|

> [!NOTE]
> **Synkronointinimikkeen** muuttaminen vaihtoehdosta **Shopifysta** muotoon **Shopifyhin** ei vaikuta, ellet ota käyttöön **Voi päivittää Shopify-tuotteita** -toimintoa. 

## Tuo nimikkeitä Shopifysta

Tuo ensin nimikkeitä Shopifysta joko joukkona tai yhdessä tilausten tuonnin kanssa lisätäksesi nimikkeet ensin **Shopify-tuote**- ja **Shopify-variantti**-taulukoihin. Yhdistä sitten tuotuja tuotteita ja variantteja nimikkeisiin ja variantteihin [!INCLUDE[prod_short](../includes/prod_short.md)]issa. Hallitse prosessia seuraavien asetusten avulla:

|Kenttä|Kuvaus|
|------|-----------|
|**Luo tuntemattomat nimikkeet automaattisesti**|Kun Shopify-tuotteet ja-variantit tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan, [!INCLUDE[prod_short](../includes/prod_short.md)] -funktio yrittää aina etsiä vastaavaa tietuetta ensin nimikeluettelosta. **Varastointiyksikön yhdistäminen** vaikuttaa siihen, miten kohdistus suoritetaan, ja luo uuden nimikkeen ja/tai nimikevariantin. Ota tämä valinta käyttöön, jos haluat luoda uuden nimikkeen tai kun vastaavaa tietuetta ei ole olemassa. Uusi nimike luodaan tuotujen tietojen ja **Nimikemallikoodin** avulla. Jos tämä valinta ei ole käytössä, sinun on luotava nimike manuaalisesti ja käytettävä **Yhdistä tuote** -toimintoa **Shopify tuotteet** -sivulla.|
|**Nimikemallin koodi**|Käytä tätä kenttää **Tuntemattomien nimikkeiden luominen automaattisesti** -vaihtoehdon kanssa.<br>Valitse haluamasi malli, jota käytetään automaattisesti luoduille nimikkeille.|
|**Varastointiyksikön yhdistämismääritykset**|Valitse nimikkeen/variantti määrityksen ja luonnin aikana Shopifysta tuotujen **varastointiyksikön** arvojen käyttötarkoitus. Lue lisätietoja [Shopifyn tuotteiden varastointiyksiköiden ja viivakoodien vaikutus nimikkeiden ja varianttien kartoittaminen ja luominen Business Centralissa](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central) -osasta.|
|**Varastointiyksikön kenttäerotin**|Käytä tätä yhdessä **Varastointiyksikön yhdistämismääritysten** kanssa, joka on määritetty **[Tuotenro + Varianttikoodi](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)** -vaihtoehtoon.<br>Määritä erotin, jota käytetään SKU-luettelon jakamista varten.<br>Jos siis luot Shopifyssa muunnelman varastointiyksiköllä '1000/001', kirjoita '/' **Varastointiyksikön erotin** -kenttään saadaksesi tuotenumeron [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa muodossa "1000" ja nimikkeen muunnelman koodi "001".|
|**Version etuliite**|Käytä yhdessä **Varastointiyksikön yhdistämismäärityksen** kanssa , jonka arvona on joko **Varianttikoodi** tai **Nimikenro + varianttikoodi** -vaihtoehtoja varmistusstrategiaksi silloin, kun Shopifysta lähtevä varastointiyksikkö on tyhjä.<br>Jos haluat luoda nimikevariantin [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa automaattisesti, sinun täytyy syöttää arvo **koodiin**. Oletusarvon mukaan käytetään Shopifysta tuodussa varastointiyksikkökentässä määritettyä arvoa. Jos varastointiyksikkö on kuitenkin tyhjä, se luo koodin alkaen määritetystä variantti-etuliitteestä ja "001"-numerosta.|
|**Shopify voi päivittää nimikkeen**|Valitse tämä vaihtoehdoista, jos haluat päivittää nimikkeet ja/tai variantit automaattisesti.|

### Shopify-tuotteiden SKU:iden ja viivakoodien vaikutus tuotteiden ja varianttien kartoittamiseen ja luomiseen Business Centralissa

Kun tuotteet tuodaan Shopifysta **Shopify-tuotteet**- ja **Shopify-variantit**-taulukoihin, [!INCLUDE[prod_short](../includes/prod_short.md)] yrittää löytää aiemmin luotuja tietueita.

Seuraavassa taulukossa kuvaillaan eri vaihtoehtojen väliset erot **Varastointiyksikön yhdistämismääritykset** -kentässä.

|Asetus|Vaikutus yhdistämiseen|Vaikutus luomiseen|
|------|-----------------|------------------|
|**Tyhjä**|Varastointiyksikkö-kenttää ei käytetä nimikkeen yhdistämisrutiinissa.|Ei vaikutusta nimikkeen luomiseen.<br>Tämä asetus estää varianttien luomisen. Myyntitilauksessa käytetään vain päänimikettä. Variantti voidaan silti linkittää manuaalisesti **Shopify-tuote**-sivulta.|
|**Nimikkeen nro**|Valitse, jos varastointiyksikkö-kentässä on nimikkeen numero|Ei vaikutusta nimikkeen luomiseen ilman variantteja. Jos nimikkeellä on variantteja, jokainen variantti luodaan erillisenä nimikkeenä.<br>Jos Shopifylla on tuote, jossa on kaksi versiota ja niiden varastointiyksiköt ovat 1000 ja 2000, [!INCLUDE[prod_short](../includes/prod_short.md)] luo kaksi nimikettä, joilla on numerot 1000 ja 2000.|
|**Versiokoodi**|Varastointiyksikkö-kenttää ei käytetä nimikkeen yhdistämisrutiinissa.|Ei vaikutusta nimikkeen luomiseen. Kun nimikevariantti luodaan, koodina käytetään varastointiyksikkökentän arvoa. Jos varastointiyksikkö on tyhjä, luodaan **varianttietuliite**-kentän avulla koodi.|
|**Nimikenro + versiokoodi**|Valitse tämä vaihtoehto, jos varastointiyksikkö-kentässä on nimikkeen numero ja nimikkeen varianttikoodi, joka on erotettu **varastointiyksikkö-kenttäerotin** -kentässä määritetyllä arvolla.|Kun nimike luodaan, määritetään varastointiyksikkö-kentän arvon ensimmäiseksi osaksi **nro**-arvo. Jos varastointiyksikkökenttä on tyhjä, nimikkeen numero luodaan käyttämällä numerosarjoja, jotka on määritetty **Nimikemallikoodi**- tai **Nimikenumero**-kentässä **Varaston määritys** -sivulla.<br>Kun nimike luodaan, varianttifunktio käyttää varastointiyksikkö-kentän arvon toista osaa muodossa **Koodi**. Jos varastointiyksikkökenttä on tyhjä, luodaan **varianttietuliite**-kentän avulla koodi.|
|**Toimittajan nimikenro**|Valitse, jos varastointiyksikkö-kentässä on toimittajanimikkeen numero. Tässä tapauksessa nimikkeen **Toimittajanro**-kenttää ei käytetä **nimikkeen kortti** -sivulla. **Toimittajan nimikenro** -vaihtoehtoa käytetään **nimikkeen toimittajakatalogista**. Jos löydetyssä *nimiketoimittajaluettelo*-tietueessa on varianttikoodi, tätä koodia käytetään Shopify-variantin yhdistämiseen.|Jos vastaava toimittaja on olemassa [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä, varastointiyksikköarvoa käytetään **Toimittajan nimikenro** -arvona **Nimikkeen kortti** -sivulla sekä *toimittajan* tyypin **Nimikeviittaus**-arvona. <br>Estää varianttien luonnin. Se on hyödyllinen silloin, kun haluat käyttää päänimikettä vain myyntitilauksessa. Voit silti yhdistää variantin manuaalisesti **Shopify-tuote**-sivulla.|
|**Viivakoodi**|Valitse, jos varastointiyksikkö-kentässä on viivakoodi. Haku suoritetaan niiden **nimikeviittausten** osalta, joiden tyyppi on *viivakoodi*. Jos löydetyssä nimikeviitetietueessa on varianttikoodi, tätä varianttikoodia käytetään Shopify-variantin yhdistämiseen.|Ei vaikutusta nimikkeen luomiseen. <br>Estää varianttien luonnin. Se on hyödyllinen silloin, kun haluat käyttää päänimikettä vain myyntitilauksessa. Voit silti yhdistää variantin manuaalisesti **Shopify-tuote**-sivulla.|

Seuraava taulukko luonnostelee **Viivakoodi**-kentän vaikutuksen.

|Vaikutus yhdistämiseen|Vaikutus luomiseen|
|-----------------|------------------|
|Haku suoritetaan **Tuoteviittauksista**, jotka sisältävät Shopifyn **Viivakoodi**-kentän arvona viivakoodityypin. Jos löydetyssä nimikeviitetietueessa on varianttikoodi, tätä varianttikoodia käytetään Shopify-variantin yhdistämiseen.|Viivakoodi tallennetaan nimikkeen ja nimikevariantin **nimikeviitteenä**.|

> [!NOTE]  
> Voit käynnistää valittujen tuotteiden/varianttien tai kaikkien tuotujen yhdistämättömien tuotteiden yhdistämisen valitsemalla **Yritä etsiä tuotteen yhdistäminen** tai **Yritä etsiä yhdistämisiä**.

## Vie nimikkeet Shopifyhin

On useita tapoja viedä nimikkeitä Shopifyhin: 

- Käytä **Lisää nimike Shopifyhin** -toimintoa suoraan **Nimikekortti**-sivulta. 
- Käytä **Lisää nimike** -toimintoa **Shopify-tuotteet** -sivulla. 
- Suorita nimikkeiden synkronointi kerran tai toistuvasti automaation avulla. 

Riippumatta siitä, miten viet nimikkeitä, tietyt tuotetiedot siirretään Shopify-tuoteluetteloon riippuen valitsemistasi nimikkeiden synkronointiasetuksista.

>[!IMPORTANT]
>Tuote lisätään vain **verkkokaupan** myyntikanavaan. Tuotteet täytyy julkaista muihin myyntikanaviin, kuten Shopify-myyntipisteeseen Shopifysta.

Voit hallita nimikkeiden vientiprosessia seuraavien asetusten avulla:

|Kenttä|Kuvaus|
|------|-----------|
|**Synkronoi nimikkeen lisäteksti**|Valitsemalla tämän kentän voit synkronoida nimikkeen lisätekstin. Koska se lisätään **kuvaus**-kenttään, se voi sisältää HTML-koodia. |
|**Synkronoi nimikemääritteet**|Valitse tämä kenttä, jos haluat synkronoida nimikemääritteet. Määritteet muotoillaan taulukkona ja sisällytetään **kuvaus**-kenttään Shopifyssa.|
|**Synkronoi nimikkeen markkinointiteksti**|Valitse tämä kenttä, jos haluat synkronoida nimikkeen markkinointitekstin. Vaikka markkinointiteksti on eräänlainen kuvaus, se on eri kuin nimikkeen **kuvaus**-kenttä. **Kuvaus**-kenttää käytetään tyypillisesti suppeana näyttönimenä, jotta tuote voidaan määrittää nopeasti. Toisaalta markkinointiteksti on rikas ja kuvaava teksti. Sen tarkoituksena on lisätä markkinointi- ja mainosmateriaalia. Tämä teksti voidaan sitten julkaista nimikkeen mukana Shopifyssa. Markkinointitekstin voi luoda kahdella tavalla. Käytä Copilotia, joka ehdottaa tekoälypohjaista tekstiä sinulle, tai aloita tyhjästä.|
|**Kielikoodi**|Käännettyjä versioita käytetään otsikossa, määritteissä ja lisätekstissä, jos tämä kenttä valitaan.|
|**Varastointiyksikön yhdistämismääritykset**|Valitse, miten haluat täyttää varastointiyksikkökentän Shopifyssa. Tuettuja vaihtoehtoja ovat:<br> - **Nimikenro** käyttää nimikenroa sekä tuotteille että varianteille.<br> - **Nimikenro + varianttikoodi**, jolla varastointiyksikkö luodaan yhdistämällä kahden kentän arvot toisiinsa. Nimikkeille, joilla ei ole variantteja, käytetään arvona vain nimikenumeroa.<br>- **Nimikkeen toimittajanro** käyttää **nimikekortissa** määritettyä nimiketoimittajan numeroa sekä tuotteille että varianteille.<br> - **Viivakoodi** käyttää viivakoodityypin **nimikeviittausta**. Tässä vaihtoehdossa noudatetaan variantteja.<br>Jos **Voi päivittää Shopify -tuotteita** on käytössä, **Varastointiyksikön yhdistämismääritykset** -kentän muutokset lisätään Shopifyihin kaikkien **Shopify-tuotteet**-sivulla lueteltujen tuotteiden ja varianttien seuraavan synkronoinnin jälkeen valitule kaupalle.|
|**Varastointiyksikön kenttäerotin**|Määritä nimikkeen erotin **Nimikenro + varianttikoodi** -vaihtoehto.|
|**Varastoa seurataan**| Valitse, miten järjestelmä täyttää Shopifyn vietävien tuotteiden **seuraa varastoa** -kentän. Voit päivittää niiden tuotteiden saatavuustiedot [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmasta Shopifyssa oleville tuotteille, joiden seuranta on otettu käyttöön. Katso lisätietoja [Varasto](synchronize-items.md#sync-inventory-to-shopify)-osasta.|
|**Oletusvarastokäytäntö**|Valitse *kiellä*, jos haluat estää Shopify-puolen negatiivisen varaston. <br>Jos **Voi päivittää Shopify -tuotteita** on käytössä, **Oletusvarastokäytäntö**-kentän muutokset lisätään Shopifyihin kaikkien **Shopify-tuotteet**-sivulla lueteltujen tuotteiden ja varianttien seuraavan synkronoinnin jälkeen valitule kaupalle.|
|**Voi päivittää Shopify-tuotteita**|Määritä tämä kenttä, jos [!INCLUDE[prod_short](../includes/prod_short.md)] voi luoda vain nimikkeitä tai jos voi myös päivittää nimikkeitä. Valitse tämä vaihtoehto, jos aiot päivittää nimikkeet manuaalisesti **Lisää nimike** -toiminnon käynnistämän synkronoinnin jälkeen **Synkronoi tuote** -toiminnolla tai toistuvien päivitysten työjonon kautta. Muista valita **Shopifyhin** **Nimikkeen synkronointi** -kentässä.<br>**Voi päivittää Shopify-tuotteita** -toiminnolla ei ole vaikutusta hintojen, kuvien tai varastotasojen synkronointiin, jotka riippumattomat valvojat ovat määrittäneet.<br>Jos **Voi päivittää Shopify-tuotteita** on käytössä, seuraavat Shopify-puolen kentät päivitetään tuote- ja tarvittaessa varianttitasolla: **SKU**, **viivakoodi**, **paino**. Tuotteen **nimike**, **tuotetyyppi**, **toimittaja** ja **kuvaus** päivittyvät myös, jos viedyt arvot eivät ole tyhjiä. Kuvauksen osalta tämä tarkoittaa, että sinun on otettava käyttöön jokin **Synkronoi nimikkeen laajennettu teksti**, **Synkronoi nimikkeen markkinointiteksti**, **Synkronoi nimikemääritteet** -vaihtoehdoista, ja määritteillä, laajennuksilla tai markkinointitekstillä on oltava arvot. Jos tuote käyttää variantteja, ohjelma lisää tai poistaa variantin tarpeen mukaan. <br>Jos tuote on määritetty Shopifyssa käyttämään varianttimatriisia, joka yhdistää kaksi tai useampia vaihtoehtoja, Shopify Connector ei voi luoda varianttia kyseiselle tuotteelle. Asetusmatriisia ei voi määrittää [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, joten liitin käyttää **Varianttikoodia** ainoana vaihtoehtona. Shopify odottaa kuitenkin useita vaihtoehtoja ja kieltäytyy luomasta varianttia, jos toisen ja muiden vaihtoehtojen tietoja puuttuu. |

### Kenttien yhdistämisen yleiskatsaus

|Shopify|Lähde vietäessä kohteesta [!INCLUDE[prod_short](../includes/prod_short.md)]|Kohde tuotaessa kohteeseen [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Tila|**Shopify-ostoskortissa** **luotujen tuotteiden tila** -kentän mukaan. Lisätietoja on [Shopify-tuotteiden Ad-hoc-päivitykset](synchronize-items.md#ad-hoc-updates-of-shopify-products) -osassa.|Ei käytetty.|
|Otsikko | **Kuvaus**. Jos kielikoodi on määritetty ja vastaava nimikekäännös on olemassa, käytetään nimikkeen käännöstä kuvauksen sijaan.|**Kuvaus**|
|Variantin otsikko | **Varianttikoodi**.|Variantin **kuvaus**|
|Kuvaus|Yhdistää lisätekstit, markkinointitekstit ja määritteet, jos otat käyttöön vastaavat vaihdot Shopify-ostoskortissa käyttöön. Säilyttää kielikoodit.|Ei käytetty.|
|Hakukoneoptimointisivun otsikko|Vakioarvo: tyhjä. Lisätietoja on [Shopify-tuotteiden Ad-hoc-päivitykset](synchronize-items.md#ad-hoc-updates-of-shopify-products) -osassa.|Ei käytetty.|
|Hakukoneoptimoinnin metakuvaus|Vakioarvo: tyhjä. Lisätietoja on [Shopify-tuotteiden Ad-hoc-päivitykset](synchronize-items.md#ad-hoc-updates-of-shopify-products) -osassa.|Ei käytetty.|
|Media|**Kuva**. Lisätietoja on [Synkronoi nimikekuvat](synchronize-items.md#sync-item-images) -osassa|**Kuva**|
|Hinta|Loppuasiakkaan hinnan laskenta sisältää nimikkeen yksikköhinnan, asiakkaan hintaryhmän, asiakkaan alennusryhmän ja valuuttakoodin. Lisätietoja on [Synkronoi hinnat](synchronize-items.md#sync-prices-with-shopify) -osassa|**Yksikköhinta**. Hinta tuodaan vain uusille nimikkeille, mutta sitä ei päivitetä myöhemmissä synkronoinneissa.|
|Vertailuhinta|Hinnan laskeminen ilman alennusta.|Ei käytetty.|
|Kustannus per nimike|**Yksikkökustannus**|**Yksikkökustannus**. Yksikkökustannus tuodaan vain uusille nimikkeille, eikä sitä päivitetä myöhemmissä synkronoinneissa.|
|Varastointiyksikkö|Lisätietoja varastointiyksiköistä on [Vie nimikkeitä Shopifyhin](synchronize-items.md#export-items-to-shopify) **SKU-määritys**-kohdassa.|Lue lisää varastointiyksiköistä [Shopifyn tuotteiden varastointiyksiköiden ja viivakoodien vaikutus nimikkeiden ja varianttien kartoittaminen ja luominen Business Centralissa](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central) -osasta.|
|Viivakoodi|Viivakoodityypin **nimikeviitteet**.|Viivakoodityypin **nimikeviitteet**.|
|Varasto varastoidaan kohteessa| Riippuu Shopify-kaupan sijainneista. Jos **Business Centralin täyttämispalvelut** -kohdassa on **Oletus**-kenttä käytössä, varasto varastoidaan ja toimitetaan **Business Centralin täyttämispalvelusta**. Muussa tapauksessa käytetään ensisijaista Shopifyn sijaintia tai useita sijainteja.| Ei käytetty.|
|Seurattava määrä|**Shopify-ostoskortti**-sivun **Seurattu varasto** -kentän mukaan. Katso lisätietoja [Varasto](synchronize-items.md#sync-inventory-to-shopify)-osasta. Käytetään vain, kun tuote viedään ensimmäisen kerran.|Ei käytetty.|
|Jatka myyntiä, kun varasto on loppunut|**Shopify-ostoskortin** **Oletusvarastokäytännön** mukaan.|Ei käytetty.|
|Tyyppi|**Nimikekategoriakoodin** **kuvaus**. Jos tyyppiä ei ole määritetty Shopifyssa, se lisätään mukautettuna tyyppinä.|**Nimikeluokan koodi**. Linkitys kuvauksen mukaan.|
|Toimittaja|Toimittajan **nimi** **Toimittajan nro**-kohteesta|**Toimittajan nro** Linkitys nimen mukaan.|
|Paino|**Bruttopaino**.|Ei käytetty.|
|Verotettava|Vakioarvo: käytössä.|Ei käytetty.|
|Verokoodit|**Veroryhmän koodi**. Koskee vain myyntiveroja. Lisätietoja kohdassa [Verojen määrittäminen](setup-taxes.md).|Ei käytetty.|


### Tunnisteet

Poista tuodut tunnisteen **Tunnisteet**-tietoruudusta **Shopify-tuote**-sivulla. Muokkaa tunnisteita valitsemalla **Tunnisteet**-toiminto samalla sivulla.
Jos **Shopifyhin** on valittuna **Synkronoi nimike** -kentässä, määritetyt tunnisteet viedään Shopifyhin seuraavan synkronoinnin yhteydessä.

## Suorita nimikkeiden synkronointi

Kohteiden synkronointi kokonaan tai osittain voidaan suorittaa monella eri tavalla.

### Nimikkeiden alkusynkronointi Business Centralista Shopifyhin

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet**, valitse sitten vastaava linkki.
2. Valitse **Lisää nimikkeitä** -toiminto.
3. Syötä koodi **Ostoskoodi**-kenttään. Jos avaat **Shopify-tuote**-ikkunan **ostoskortti**-sivulla, ostoskoodi täytetään automaattisesti.
4. Jos olet määrittänyt näköistiedoston ja varaston synkronoinnin, voit sisällyttää ne samaan prosessiin. Niiden sisällyttäminen samaan prosessiin on kätevää esittelyskenaarioissa tai kun käsitellään pienempiä tietomääriä. 
5. Määritä nimikkeiden suodattimet tarpeen mukaan. Voit suodattaa esimerkiksi nimikenumeron tai nimikekategorian koodin mukaan.
6. Valitse **OK**.

Tuloksena syntyvät nimikkeet hintoineen luodaan Shopifyssa automaattisesti. Tekemiesi valintojen mukaan ne voivat sisältää kuvia ja varastomääriä. Toiminto voi kestää jonkin aikaa, jos useita nimikkeitä on lisätty.

### Synkronoi tuotteita Shopifysta Business Centraliin

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida nimikkeet avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi tuotteet** -toiminto.

Vaihtoehtoisesti voit käyttää **Synkronoi tuotteet** - toimintoa **Shopify-tuotteet**-sivulla tai hae **Synkronoi tuotteet** -eräajoa.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoittaminen](background.md#to-schedule-recurring-tasks).

### URL- ja esiversion URL-osoite

Shopifyhin lisätyllä tai Shopifysta tuodulla nimikkeellä voi olla **URL**- tai **Esiversion URL**-osoite täytettynä. **URL-osoite**-kenttä on tyhjä, jos tuotetta ei julkaistu verkkokaupassa esimerkiksi siksi, että sen tila on luonnos. **URL-osoite** on tyhjä, jos kauppa on suojattu salasanalla esimerkiksi siksi, että se on kehityskauppa. Useimmissa tapauksissa voit tarkistaa **Esiversion URL-osoitteen** avulla, miltä tuote näyttää julkaisun jälkeen.

### Shopify-tuotteiden Ad-Hoc-päivitykset

Kun tietueet on päivitettävä **Shopify-tuote**-taulukossa, seuraavat muutokset synkronoidaan Shopifyn kanssa.

Päivitys:

* **Tila** - voit valita aktiivisen, arkistoidun tai luonnoksen.
* **SEO:n otsikko**
* **SEO:n kuvaus**

Poisto:

**Toimenpide poistetuille tuotteille** **Shopify-ostoskortti** -sivun arvon perusteella tuote päivitetään Shopifyssa, kun tietue poistetaan **Shopify-tuotteet**-sivulta.

* **Tyhjä** - mitään ei tapahdu. Tarvittaessa sinun täytyy suorittaa tarvittavat toimet **Shopify-järjestelmänvalvojasta**.
* **Tila luonnokseksi** - Shopifyn tuotteen tilaksi on asetettu *Luonnos*.
* **Tilaksi arkistoitu** - tuote on arkistoitu Shopifyssa.

## Synkronoi nimikekuvat

Kuvien synkronointi voidaan määrittää synkronoiduille nimikkeille. Valitse seuraavista vaihtoehdoista:

* **Poistettu käytöstä** - Kuvan synkronointi on poistettu käytöstä.
* **Shopifyhin** - kuvia nimikkeistä viedään Shopifyhin.
* **Shopifysta** - kuvat Shopifysta tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan.

Kuvan synkronointi voidaan alustaa kahdella alla kuvatulla tavalla.

### Synkronoi tuotekuvat Shopify-myymäläsivulla

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida kuvat avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi tuotekuvat** -toiminto.

### Synkronoi tuotekuvat Shopify-tuotesivulta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet**, valitse sitten vastaava linkki.
2. Valitse **Synkronoi tuotekuvat** -toiminto.

### Kuvien synkronoinnin huomautukset

* Kun viet kuvia [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmästä Shopifyhin, kuvat korvaavat aiemmin viedyt kuvat. Aiemmat kuvat eivät ole enää käytettävissä.
* Jos poistat kuvan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, Shopifyssa olevaa kuvaa ei poisteta samalla. Sinun täytyy poistaa vanhoja kuvia manuaalisesti **Shopify-järjestelmänhallinnassa**.
* Shopifyhin vietävien kuvien on täytettävä Shopifyn vaatimukset. Muussa tapauksessa et voi tuoda niitä. Lisätietoja median vaatimuksista on kohdassa [Tuotemediatyypit osoitteessa help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## Synkronoi hintoja Shopifyn kanssa

Voit hallita hintojen vientiprosessia seuraavien asetusten avulla:

|Kenttä|Kuvaus|
|------|-----------|
|**Asiakkaan hintaryhmä**|Määritä nimikkeen hinta Shopifyssa. Tämän asiakkaan hintaryhmän myyntihinta on otettu. Jos ryhmää ei ole määritetty, käytetään nimikekortin hintaa.|
|**Asiakkaan alennusryhmä**|Määritä alennus, jota käytetään nimikkeen hinnan laskennassa Shopifyssa. Alennetut hinnat tallennetaan **hinta**-kenttään, ja koko hinta tallentuu **Vertaa hintaan** -kenttään.|
|**Salli rivialennus**|Määrittää, sallitaanko rivialennus laskettaessa hintoja Shopifylle. Tämä asetus koskee vain nimikkeen hintoja. Asiakkaan hintaryhmän hinnoilla on oma vaihtorivi.|
|**Hinnat sisältävät ALV:n**|Määrittää, sisältävätkö Shopifyn hintalaskelmat ALV:n. Lisätietoja kohdassa [Verojen määrittäminen](setup-taxes.md).|
|**Liiketoim. ALV-kirjausryhmä**|Määrittää, mitä liiketoiminnan ALV-kirjausryhmää käytetään Shopify-hintojen laskemiseen. Tämän pitäisi olla ryhmä, jota käytetään kotimaan asiakkaille. Lisätietoja kohdassa [Verojen määrittäminen](setup-taxes.md).|
|**Valuutan koodi**|Syötä Valuuttakoodi vain, jos verkkokauppa käyttää eri valuuttaa kuin paikallinen valuutta (PVA). Määritetyllä valuutalla on oltava määritettynä vaihtokurssit. Jos verkkokauppa käyttää samaa valuuttaa kuin [!INCLUDE[prod_short](../includes/prod_short.md)], jätä kenttä tyhjäksi.|

Synkronoitujen nimikkeiden hinnat voidaan viedä alla kuvatulla kahdella tavalla.

### Synkronoi hinnat Shopify-tuotesivulla

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet**, valitse sitten vastaava linkki.
2. Valitse **Synkronoi tuotteet Shopifyhin** -toiminto.

### Hintalaskennan huomautukset

* Hinnan määrittämisessä [!INCLUDE[prod_short](../includes/prod_short.md)] käyttää "alin hinta" -logiikkaa. Alhaisin hintalogiikka ei kuitenkaan huomioi nimikekortissa määritettyä yksikköhintaa, jos hinta on määritelty hintaryhmässä. Tämä pätee, vaikka nimikekortin hinnan yksikkökohtainen hinta on pienempi.
* Kun haluat laskea hintoja, yhdistin luo nimikkeelle tilapäisen myyntitarjouksen, jonka määrä on 1, ja käyttää vakiohinnan laskentalogiikkaa. Vain määrään 1 sovellettavia hintoja ja alennuksia käytetään. Et voi viedä eri hintoja tai alennuksia määrän perusteella.

## Synkronoi varasto Shopifyhin

Varaston synkronointi voidaan määrittää jo synkronoiduille nimikkeille. On täytettävä kaksi ehtoa:

1. Shopifyssa olevalle tuotteelle otettava käyttöön varastoseuranta. Jos nimikkeitä viedään Shopifyhin, harkitse **Seuratun varaston** vaihto-ohjelman käyttöönottoa **Shopify-ostos**-sivulla. Lue lisää [Nimikkeiden vienti Shopifyhin](synchronize-items.md#export-items-to-shopify) -osasta.
2. **Shopify-sijaintien** synkronoinnin on oltava käytössä.

### Varaston synkronoinnin ottaminen käyttöön

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida varaston avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **sijainnit** -toiminto, jolla **Shopify-myymäläsijainnit** avataan.
4. Valitse **Hae Shopify-sijainnit** -toiminto, jos haluat tuoda kaikki Shopifyssa määritetyt sijainnit. Voit etsiä niitä [**Sijainnit**](https://www.shopify.com/admin/settings/locations)-asetuksista **Shopify-järjestelmänvalvojastasi**.
5. Lisää **sijaintisuodatus** -kenttään sijainteja, jos haluat sisällyttää varaston vain tietyistä sijainneista. Voit siis syöttää arvoksi *ITÄ|LÄNSI*, jolloin varasto vain näistä kahdesta sijainnista on myynnissä verkkokaupan kautta.
6. Valitse varaston laskentatapa, jota käytetään valituissa Shopify-sijainneissa.
7. Ota **oletusasetus** käyttöön, jos haluat, että sijaintia käytetään varastotietueiden luonnissa ja jos haluat osallistua varaston synkronointiin. Aktivoi **oletusasetus** **Business Centralin täyttämispalveluille**, kun haluat luoda varastotietueen, joka edustaa täyttämispalvelua. Muutoin luodaan varastotietue ensisijaisesta shopify-sijainnista ja kaikista normaaleista sijainneista, joissa **Oletus** on päällä.


Voit alustaa varaston synkronoinnin kahdella alla kuvatulla tavalla.

### Synkronoi varasto Shopify-myymäläsivulta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida varaston avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi varasto** -toiminto.

### Synkronoi varasto Shopify-tuotesivulta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-tuotteet** ja valitse vastaava linkki.
2. Valitse **Synkronoi varasto** -toiminto.

### Varaston huomautukset

* Varaston vakiolaskentamenetelmä on **Oletettu saatavilla oleva päivän saldo**. Laajennettavuuden avulla voit lisätä vaihtoehtoja. Saat lisätietoja laajennettavuudesta siirtymällä [esimerkkeihin](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify#stock-calculation). 
* Voit tarkistaa Shopifysta saadut varastotiedot **Shopify-varaston tietoruutu** -sivulta. Tässä tietoruudussa on yleiskuvaus Shopify-varastosta ja viimeisestä lasketusta varastosta [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa. Sijaintia kohti on yksi tietue.
* Jos Shopifyn varastotiedot poikkeavat [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelman **Arvioidusta käytettävissä olevasta saldosta**, varastotiedot päivitetään Shopifyssa.
* Kun lisäät uuden sijainnin Shopifyhyn, sitä varten on lisättävä myös varastotietueita. Shopify ei tee sitä automaattisesti olemassa oleville tuotteille ja varianteille, eikä yhdistin synkronoi näiden nimikkeiden varastomääriä uudessa sijainnissa. Saat lisätietoja siirtymällä kohtaan [Varaston määrittäminen sijainteihin](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).
* Sekä **Business Centralin täyttämispalvelut** että normaalit sijainnit ovat tuettuja, ja niitä voidaan käyttää toimitukseen ja varastoon.

#### Esimerkki oletetun saatavilla olevan saldon laskemisesta

Nimikettä A saatavilla on 10 kappaletta ja niille on kaksi avointa myyntitilausta. Toinen on maanantaille, jossa määrä on *Yksi*, ja toinen torstaille, jossa määrä on *Kaksi*. Riippuen siitä, milloin synkronoit varaston, järjestelmä päivittää varastotason Shopifyssa käyttämällä eri määriä:

|Milloin varaston synkronointi suoritetaan|Varastotason päivittämiseen käytetty arvo|Kommentti|
|------|-----------------|-----------------|
|Tiistai|9|Varasto 10 miinus myyntitilaus asetettu lähetettäväksi maanantaina|
|Perjantai|7|Varasto 10 miinus molemmat myyntitilaukset|

## Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
