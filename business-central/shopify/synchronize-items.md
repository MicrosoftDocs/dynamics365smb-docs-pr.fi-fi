---
title: Synkronoi nimikkeet ja varasto
description: Määritä ja suorita nimikkeiden synkronoinnit Shopifyn ja Business Centralin välillä
ms.date: 04/28/2024
ms.topic: article
ms.search.form: '30116, 30117, 30126, 30127,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# <a name="synchronize-items-and-inventory"></a>Synkronoi nimikkeet ja varasto

**Nimikkeet** tuotteessa [!INCLUDE[prod_short](../includes/prod_short.md)] vastaavat **tuotteita** Shopifyssa. Ne ovat fyysisiä tavaroita, digitaalisia latauksia, palveluja ja lahjakortteja, joita myyt. On kaksi pääasiallista syytä synkronoida nimikkeet:

1. Kun hallitset tietoja ensisijaisesti tuotteessa [!INCLUDE[prod_short](../includes/prod_short.md)]. Sinun täytyy viedä kaikki tiedot sieltä Shopifyhin ja tehdä niistä näkyviä. Voit viedä nimikkeen nimen, kuvauksen, kuvan, hinnat, saatavuuden, variantit, toimittajan tiedot ja viivakoodin. Kun ne on viety, voit tarkastella nimikkeitä tai tehdä ne näkyviksi heti.
2. Kun tilaus Shopifysta tuodaan, nimikkeen tiedot ovat olennaisia asiakirjan käsittelemisessä [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

Edeltävät kaksi skenaariota ovat aina käytössä.

Kolmas skenaario on tietojen hallinta Shopify mutta kyseisten nimikkeiden tuonti joukkona [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Tämä skenaario voi olla hyödyllinen tiedonsiirtotapahtumissa, kuten kun aiemmin luotu verkkokauppa halutaan yhdistää uuteen [!INCLUDE[prod_short](../includes/prod_short.md)] -ympäristöön.

## <a name="define-item-synchronizations"></a>Määritä nimikkeiden synkronointivaltuudet

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

## <a name="import-items-from-shopify"></a>Tuo nimikkeitä Shopifysta

Tuo ensin nimikkeitä Shopifysta joko joukkona tai yhdessä tilausten tuonnin kanssa lisätäksesi nimikkeet ensin **Shopify-tuote**- ja **Shopify-variantti**-taulukoihin. Yhdistä sitten tuotuja tuotteita ja variantteja nimikkeisiin ja variantteihin [!INCLUDE[prod_short](../includes/prod_short.md)]issa. Hallitse prosessia seuraavien asetusten avulla:

|Kenttä|Kuvaus|
|------|-----------|
|**Luo tuntemattomat nimikkeet automaattisesti**|Kun Shopify-tuotteet ja-variantit tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan, [!INCLUDE[prod_short](../includes/prod_short.md)] -funktio yrittää aina etsiä vastaavaa tietuetta ensin nimikeluettelosta. **Varastointiyksikön yhdistäminen** vaikuttaa siihen, miten kohdistus suoritetaan, ja luo uuden nimikkeen ja/tai nimikevariantin. Ota tämä valinta käyttöön, jos haluat luoda uuden nimikkeen tai kun vastaavaa tietuetta ei ole olemassa. Uusi nimike luodaan tuotujen tietojen ja **Nimikemallikoodin** avulla. Jos tämä valinta ei ole käytössä, luo nimike manuaalisesti ja käytettävä **Yhdistä tuote** -toimintoa **Shopify-tuotteet** -sivulla.|
|**Nimikemallin koodi**|Käytä tätä kenttää **Tuntemattomien nimikkeiden luominen automaattisesti** -vaihtoehdon kanssa.<br>Valitse haluamasi malli, jota käytetään automaattisesti luoduille nimikkeille.|
|**Varastointiyksikön yhdistämismääritykset**|Valitse nimikkeen/variantti määrityksen ja luonnin aikana Shopifysta tuotujen **varastointiyksikön** arvojen käyttötarkoitus. Lue lisätietoja [Shopifyn tuotteiden varastointiyksiköiden ja viivakoodien vaikutus nimikkeiden ja varianttien kartoittaminen ja luominen Business Centralissa](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central) -osasta.|
|**Varastointiyksikön kenttäerotin**|Käytä tätä yhdessä **Varastointiyksikön yhdistämismääritysten** kanssa, joka on määritetty **[Tuotenro + Varianttikoodi](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)** -vaihtoehtoon.<br>Määritä erotin, jota käytetään SKU-luettelon jakamista varten.<br>Jos siis luot Shopifyssa muunnelman varastointiyksiköllä '1000/001', kirjoita '/' **Varastointiyksikön erotin** -kenttään saadaksesi tuotenumeron [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa muodossa "1000" ja nimikkeen muunnelman koodi "001". Jos luot muunnelman SKU:lla 1000/001/111 Shopifyssa, tuotteen numero [!INCLUDE[prod_short](../includes/prod_short.md)] on "1000" ja tuoteversion koodi "001". 111-osa ohitetaan. |
|**Version etuliite**|Käytä yhdessä **Varastointiyksikön yhdistämismäärityksen** kanssa , jonka arvona on joko **Varianttikoodi** tai **Nimikenro + varianttikoodi** -vaihtoehtoja varmistusstrategiaksi silloin, kun Shopifysta lähtevä varastointiyksikkö on tyhjä.<br>Jos haluat luoda nimikevariantin [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa automaattisesti, sinun on syötettävä arvo kohtaan **Koodi**. Oletusarvon mukaan käytetään Shopifysta tuodussa varastointiyksikkökentässä määritettyä arvoa. Jos varastointiyksikkö on kuitenkin tyhjä, se luo koodin alkaen määritetystä variantti-etuliitteestä ja "001"-numerosta.|
|**Shopify voi päivittää nimikkeen**|Valitse tämä vaihtoehdoista, jos haluat päivittää nimikkeet ja/tai variantit automaattisesti.|
|**Mittayksikkö versiona**| Valitse tämä vaihtoehto, jos haluat viedä kaikki nimikkeen mittayksiköt erillisinä variantteina. Voit lisätä kentän mukauttamalla sivua. Lisätietoja on osassa [Mittayksikkö varianttina](synchronize-items.md#unit-of-measure-as-variant).|
|**Mittayksikköversiovaihtoehdon nimi**| Käytä tätä kenttää ja **Mittayksikkö versiona** -vaihtoehtoa määrittämään, missä vaihtoehdossa lisätään mittayksikön ilmaisevat variantit. Oletusarvo on *Mittayksikkö*. Käytä mukautusta lisätäksesi kentän sivulle.|

## <a name="export-items-to-shopify"></a>Vie nimikkeet Shopifyhin

On useita tapoja viedä nimikkeitä Shopifyhin:

* Käytä **Lisää nimike Shopifyhin** -toimintoa suoraan **Nimikekortti**-sivulta.
* Käytä **Lisää nimike** -toimintoa **Shopify-tuotteet** -sivulla.
* Suorita nimikkeiden synkronointi kerran tai toistuvasti automaation avulla.

Riippumatta siitä, miten viet nimikkeitä, tietyt tuotetiedot siirretään Shopify-tuoteluetteloon riippuen valitsemistasi nimikkeiden synkronointiasetuksista.

Ennen kuin yhdistin vie nimikkeen Shopifyhin, se tarkastaa, onko nimike jo olemassa. Aluksi se tarkastaa, onko olemassa tuotetta tai varianttia, jolla on viivakoodi, koska se on määritetty viivakoodityypin **Nimikeviitteet**-tapahtumassa. Jos **Varastointiyksikön yhdistämismääritys**-kenttä on täytettynä, yhdistin tarkastaa, onko olemassa tuotetta tai varianttia, jolla varastointiyksikkö on täytettynä. Lisätietoja: [Shopifyn tuotteiden varastointiyksiköiden ja viivakoodien vaikutus nimikkeiden ja varianttien kartoittaminen ja luominen Business Centralissa](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).

> [!IMPORTANT]
> Tuote lisätään vain **verkkokaupan** myyntikanavaan. Tuotteet täytyy julkaista muihin myyntikanaviin, kuten Shopify-myyntipisteeseen Shopifysta.

Voit hallita nimikkeiden vientiprosessia seuraavien asetusten avulla:

|Kenttä|Kuvaus|
|------|-----------|
|**Synkronoi nimikkeen lisäteksti**|Valitsemalla tämän kentän voit synkronoida nimikkeen lisätekstin. Koska se lisätään **kuvaus**-kenttään, se voi sisältää HTML-koodia. |
|**Synkronoi nimikemääritteet**|Valitse tämä kenttä, jos haluat synkronoida nimikemääritteet. Määritteet muotoillaan taulukkona ja sisällytetään **kuvaus**-kenttään Shopifyssa.|
|**Synkronoi nimikkeen markkinointiteksti**|Valitse tämä kenttä, jos haluat synkronoida nimikkeen markkinointitekstin. Vaikka markkinointiteksti on eräänlainen kuvaus, se on eri kuin nimikkeen **Kuvaus**-kenttä. **Kuvaus**-kenttää käytetään tyypillisesti suppeana näyttönimenä, jotta tuote voidaan määrittää nopeasti. Toisaalta markkinointiteksti on rikas ja kuvaava teksti. Sen tarkoituksena on lisätä markkinointi- ja mainosmateriaalia. Tämä teksti voidaan sitten julkaista nimikkeen mukana Shopifyssa. Markkinointitekstin voi luoda kahdella tavalla. Käytä Copilotia, joka ehdottaa tekoälypohjaista tekstiä sinulle, tai aloita tyhjästä.|
|**Kielikoodi**|Käännettyjä versioita käytetään otsikossa, määritteissä ja lisätekstissä, jos tämä kenttä valitaan.|
|**Varastointiyksikön yhdistämismääritykset**|Valitse, miten haluat täyttää varastointiyksikkökentän Shopifyssa. Tuettuja vaihtoehtoja ovat:<br> - **Nimikenro** käyttää nimikenumeroa sekä tuotteille että varianteille.<br> - **Nimikenro + varianttikoodi**, jolla varastointiyksikkö luodaan yhdistämällä kahden kentän arvot toisiinsa. Nimikkeille, joilla ei ole variantteja, käytetään arvona vain nimikenumeroa.<br>- **Nimikkeen toimittajanro** käyttää **nimikekortissa** määritettyä nimiketoimittajan numeroa sekä tuotteille että varianteille.<br> - **Viivakoodi** käyttää viivakoodityypin **nimikeviittausta**. Tässä vaihtoehdossa noudatetaan variantteja.<br>Jos **Voi päivittää Shopify -tuotteita** on käytössä, **Varastointiyksikön yhdistämismääritykset** -kentän muutokset lisätään Shopifyihin kaikkien **Shopify-tuotteet**-sivulla lueteltujen tuotteiden ja varianttien seuraavan synkronoinnin jälkeen valitule kaupalle.|
|**Varastointiyksikön kenttäerotin**|Määritä nimikkeen erotin **Nimikenro + varianttikoodi** -vaihtoehto.|
|**Varastoa seurataan**| Valitse, miten järjestelmä täyttää Shopifyn vietävien tuotteiden **seuraa varastoa** -kentän. Voit päivittää niiden tuotteiden saatavuustiedot [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmasta Shopifyssa oleville tuotteille, joiden seuranta on otettu käyttöön. Katso lisätietoja [Varasto](synchronize-items.md#sync-inventory-to-shopify)-osasta.|
|**Oletusvarastokäytäntö**|Valitse *kiellä*, jos haluat estää Shopify-puolen negatiivisen varaston. <br>Jos **Voi päivittää Shopify -tuotteita** on käytössä, **Oletusvarastokäytäntö**-kentän muutokset lisätään Shopifyihin kaikkien **Shopify-tuotteet**-sivulla lueteltujen tuotteiden ja varianttien seuraavan synkronoinnin jälkeen valitule kaupalle.|
|**Voi päivittää Shopify-tuotteita**|Määritä tämä kenttä, jos [!INCLUDE[prod_short](../includes/prod_short.md)] voi luoda vain nimikkeitä tai jos voi myös päivittää nimikkeitä. Valitse tämä vaihtoehto, jos aiot päivittää nimikkeet manuaalisesti **Lisää nimike** -toiminnon käynnistämän synkronoinnin jälkeen **Synkronoi tuote** -toiminnolla tai toistuvien päivitysten työjonon kautta. Muista valita **Shopifyhin** **Nimikkeen synkronointi** -kentässä.<br>**Voi päivittää Shopify-tuotteita** -toiminnolla ei ole vaikutusta hintojen, kuvien tai varastotasojen synkronointiin, jotka riippumattomat valvojat ovat määrittäneet.<br>Jos **Voi päivittää Shopify-tuotteita** on käytössä, seuraavat Shopify-puolen kentät päivitetään tuote- ja tarvittaessa varianttitasolla: **SKU**, **viivakoodi**, **paino**. Tuotteen **nimike**, **tuotetyyppi**, **toimittaja** ja **kuvaus** päivittyvät myös, jos viedyt arvot eivät ole tyhjiä. Kuvauksen osalta tämä tarkoittaa, että sinun on otettava käyttöön jokin **Synkronoi nimikkeen laajennettu teksti**, **Synkronoi nimikkeen markkinointiteksti** ja **Synkronoi nimikemääritteet** -vaihtoehdoista, ja määritteillä, laajennuksilla tai markkinointitekstillä on oltava arvot. Jos tuote käyttää variantteja, ohjelma lisää tai poistaa variantin tarpeen mukaan. <br>Jos tuote on määritetty Shopifyssa käyttämään varianttimatriisia, joka yhdistää kaksi tai useampia vaihtoehtoja, Shopify Connector ei voi luoda varianttia kyseiselle tuotteelle. Asetusmatriisia ei voi määrittää [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, joten liitin käyttää **Varianttikoodia** ainoana vaihtoehtona. Shopify odottaa kuitenkin useita vaihtoehtoja ja kieltäytyy luomasta varianttia, jos toisen ja muiden vaihtoehtojen tietoja puuttuu. |
|**Mittayksikkö versiona**| Valitse tämä vaihtoehto, jotkin vaihtoehdot halutaan viedä tuotuina mittayksiköinä eikä variantteina. Mukauta sivu lisätäksesi kentän. Lisätietoja on osassa [Mittayksikkö varianttina](synchronize-items.md#unit-of-measure-as-variant).|
|**Mittayksikköversiovaihtoehdon nimi**| Käytä tätä kenttää ja **Mittayksikkö versiona** -vaihtoehtoa määrittämään, mikä vaihtoehto sisältää mittayksikön ilmaisevat variantit. Oletusarvo on *Mittayksikkö*. Mukauta sivu lisätäksesi kentän.|

> [!NOTE]
> Jos vietäviä nimikkeitä ja variantteja on runsaasti, jotkin niistä on voitu estää. Estettyjä nimikkeitä ja variantteja ei voi sisällyttää hintalaskelmiin, joten niitä ei viedä. Yhdistin ohittaa kyseiset nimikkeet ja variantit, joten niitä ei tarvitse suodattaa **Lisää nimike Shopifyhin** -pyyntösivulla.

## <a name="advanced-details"></a>Lisätietoja

### <a name="effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central"></a>Shopify-tuotteiden SKU:iden ja viivakoodien vaikutus tuotteiden ja varianttien kartoittamiseen ja luomiseen Business Centralissa

Kun tuotteet tuodaan Shopifysta **Shopify-tuotteet**- ja **Shopify-variantit**-taulukoihin, [!INCLUDE[prod_short](../includes/prod_short.md)] yrittää löytää aiemmin luotuja tietueita.

Seuraavassa taulukossa kuvaillaan eri vaihtoehtojen väliset erot **Varastointiyksikön yhdistämismääritykset** -kentässä.

|Asetus|Vaikutus yhdistämiseen|Vaikutus luomiseen|
|------|-----------------|------------------|
|**Tyhjä**|Varastointiyksikkö-kenttää ei käytetä nimikkeen yhdistämisrutiinissa.|Ei vaikutusta nimikkeen luomiseen.<br>Tämä asetus estää varianttien luomisen. Myyntitilauksessa käytetään vain päänimikettä. Variantti voidaan silti linkittää manuaalisesti **Shopify-tuote**-sivulta.|
|**Nimikkeen nro**|Valitse, jos varastointiyksikkö-kentässä on nimikkeen numero.|Ei vaikutusta nimikkeen luomiseen ilman variantteja. Jos nimikkeellä on variantteja, jokainen variantti luodaan erillisenä nimikkeenä.<br>Jos Shopifylla on tuote, jossa on kaksi versiota ja niiden varastointiyksiköt ovat 1000 ja 2000, [!INCLUDE[prod_short](../includes/prod_short.md)] luo kaksi nimikettä, joilla on numerot 1000 ja 2000.|
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

### <a name="fields-mapping-overview"></a>Kenttien yhdistämisen yleiskatsaus

|Shopify|Lähde vietäessä kohteesta [!INCLUDE[prod_short](../includes/prod_short.md)]|Kohde tuotaessa kohteeseen [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Tila|**Shopify-ostoskortissa** **luotujen tuotteiden tila** -kentän mukaan. Lisätietoja on [Shopify-tuotteiden Ad-hoc-päivitykset](synchronize-items.md#ad-hoc-updates-of-shopify-products) -osassa.|Ei käytetty.|
|Otsikko | **Kuvaus**. Jos kielikoodi on määritetty ja vastaava nimikekäännös on olemassa, käytetään nimikkeen käännöstä kuvauksen sijaan.|**Kuvaus**|
|Variantin otsikko | **Varianttikoodi**.<br>Syy **Koodi**-arvon käyttöön **Kuvaus**-arvon sijaan on, että Shopify edellyttää kullekin tuotteelle yksilöllisiä varianttien otsikkoja. Tuotteessa [!INCLUDE[prod_short](../includes/prod_short.md)] **Koodi** on yksilöllinen, mutta **Kuvaus** ei. Kuvaukset, jotka eivät ole yksilöllisiä, johtavat ongelmiin tuotteen viennin aikana.|Variantin **kuvaus**|
|Kuvaus|Yhdistää lisätekstit, markkinointitekstit ja määritteet, jos otat käyttöön vastaavat vaihdot Shopify-ostoskortissa käyttöön. Säilyttää kielikoodit.|Ei käytetty.|
|Hakukoneoptimointisivun otsikko|Vakioarvo: tyhjä. Lisätietoja on [Shopify-tuotteiden Ad-hoc-päivitykset](synchronize-items.md#ad-hoc-updates-of-shopify-products) -osassa.|Ei käytetty.|
|Hakukoneoptimoinnin metakuvaus|Vakioarvo: tyhjä. Lisätietoja on [Shopify-tuotteiden Ad-hoc-päivitykset](synchronize-items.md#ad-hoc-updates-of-shopify-products) -osassa.|Ei käytetty.|
|Media|**Kuva**. Lisätietoja on [Synkronoi nimikekuvat](synchronize-items.md#sync-item-images) -osassa|**Kuva**|
|Hinta|Loppuasiakkaan hinnan laskenta sisältää nimikkeen yksikköhinnan, asiakkaan hintaryhmän, asiakkaan alennusryhmän ja valuuttakoodin. Lisätietoja on [Synkronoi hinnat](synchronize-items.md#sync-prices-with-shopify) -osassa|**Yksikköhinta**. Hinta tuodaan vain uusille nimikkeille, mutta sitä ei päivitetä myöhemmissä synkronoinneissa.|
|Vertailuhinta|Hinnan laskeminen ilman alennusta. Jos arvo on pienempi tai yhtä suuri kuin **Hinta**, liitin lähettää 0 (tyhjäarvo) todellisen arvon sijaan.|Ei käytetty.|
|Kustannus per nimike|**Yksikkökustannus**|**Yksikkökustannus**. Yksikkökustannus tuodaan vain uusille nimikkeille, eikä sitä päivitetä myöhemmissä synkronoinneissa.|
|Varastointiyksikkö|Lisätietoja varastointiyksiköistä on [Vie nimikkeitä Shopifyhin](synchronize-items.md#export-items-to-shopify) **SKU-määritys**-kohdassa.|Lue lisää varastointiyksiköistä [Shopifyn tuotteiden varastointiyksiköiden ja viivakoodien vaikutus nimikkeiden ja varianttien kartoittaminen ja luominen Business Centralissa](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central) -osasta.|
|Viivakoodi|Viivakoodityypin **nimikeviitteet**.|Viivakoodityypin **nimikeviitteet**.|
|Varasto varastoidaan kohteessa| Riippuu Shopify-kaupan sijainneista. Jos **Tuotteen oletussijainti** -kenttä on otettu käyttöön **Business Centralin täyttämispalveluissa**, varasto varastoidaan ja lähetetään **Business Centralin täyttämispalveluista**. Muutoin käytetään Shopifyn ensisijaista sijaintia tai useaa sijaintia. Lisätietoja on [Kaksi tapaa hallita täyttämisiä](synchronize-items.md#two-approaches-to-manage-fulfillments) -osassa.| Ei käytetty.|
|Seurattava määrä|**Shopify-ostoskortti**-sivun **Seurattu varasto** -kentän mukaan. Katso lisätietoja [Varasto](synchronize-items.md#sync-inventory-to-shopify)-osasta. Käytetään vain, kun tuote viedään ensimmäisen kerran.|Ei käytetty.|
|Jatka myyntiä, kun varasto on loppunut|**Shopify-ostoskortin** **Oletusvarastokäytännön** mukaan.|Ei käytetty.|
|Tyyppi|**Nimikekategoriakoodin** **kuvaus**. Jos tyyppiä ei ole määritetty Shopifyssa, se lisätään mukautettuna tyyppinä.|**Nimikeluokan koodi**. Linkitys kuvauksen mukaan.|
|Toimittaja|Toimittajan **nimi** **Toimittajan nro**-kohteesta|**Toimittajan nro** Linkitys nimen mukaan.|
|Paino|**Bruttopaino**.|Ei käytetty.|
|Verotettava|Vakioarvo: käytössä.|Ei käytetty.|
|Verokoodit|**Veroryhmän koodi**. Koskee vain myyntiveroja. Lisätietoja kohdassa [Verojen määrittäminen](setup-taxes.md).|Ei käytetty.|

### <a name="tags"></a>Tunnisteet

Poista tuodut tunnisteen **Tunnisteet**-tietoruudusta **Shopify-tuote**-sivulla. Muokkaa tunnisteita valitsemalla **Tunnisteet**-toiminto samalla sivulla.

Jos **Shopifyhin** on valittuna **Synkronoi nimike** -kentässä, määritetyt tunnisteet viedään Shopifyhin seuraavan synkronoinnin yhteydessä.

### <a name="unit-of-measure-as-variant"></a>Mittayksikkö varianttina

Shopify ei tue useita mittayksiköitä. Jos sama tuote halutaan myydä esimerkiksi kappaletavarana ja pakkauksena sekä käyttää eri hintoja tai alennuksia, mittayksikkö on luotava tuotevarianttina.
Shopify-yhdistin voidaan määrittää viemään mittayksikkö varianttina tai tuomaan variantit mittayksikköinä.

Tämä ominaisuus otetaan käyttöön **Shopify-ostoskortin** **Mittayksikkö versiona**- ja **Versiovaihtoehdon nimi** -kentissä. Kentät on oletusarvoisesti piilotettu, joten ne on lisättävä sivulle mukauttamalla.

**Mittayksikköä varianttina koskevia huomautuksia**

* Varianttimatriisia, kuten väriä ja mittayksikköä, käytettäessä ja tuotteita tuotaessa kohteeseen [!INCLUDE[prod_short](../includes/prod_short.md)] *Nimikenro + varianttikoodi* on määritettävä **Varastointiyksikön yhdistämismääritykset** -kentässä. Lisäksi on varmistettava, että Shopifyn **Varastointiyksikkö**-kentässä on sama arvo kaikille mittayksiköille ja sekä nimikenumero että varianttikoodi.
* Saatavuus lasketaan [!INCLUDE[prod_short](../includes/prod_short.md)]issa nimike- tai nimikevarianttikohtaisesti eikä mittayksikön mukaan. Tällä tavoin sama saatavuus määritetään kullekin mittayksikköä ilmaisevalla variantille (**Määrä mittayksikköä kohti** -arvon osalta). Tämä voi johtaa tilanteisiin, joissa Shopifyssa oleva määrä ei ole tarkka. Esimerkki: Nimike myydään kappaletavarana ja 6 tuotteen pakkauksena. Varasto [!INCLUDE[prod_short](../includes/prod_short.md)]issa on 6 kpl. Nimike viedään Shopifyhyn tuotteena, jolla on kaksi varianttia. Varaston synkronoinnin jälkeen Shopifyn varastomäärä on 6, kun varianttina on kappaletavara, ja 1, kun varianttina on pakkaus. Ostaja voi tutkia vain myymälää ja havaitsee, että tuotteen molemmat vaihtoehdot ovat saatavana. Ostaja päättää tilata 1 pakkauksen. Seuraava ostaja näkee, että pakkaus ei ole saatavana, mutta kappaletavaraa on jäljellä 6. Tämä korjautuu seuraavan varaston synkronoinnin jälkeen.
* Et voi lisätä Mittayksikkö-vaihtoehtoa olemassa oleviin tuotteisiin, joilla on variantteja (kulloinenkin tulos määräytyy muun asetuksen, kuten **Varastonimikkeen yhdistämismääritys**, perusteella).

### <a name="url-and-preview-url"></a>URL- ja esiversion URL-osoite

Shopifyhin lisätyllä tai Shopifysta tuodulla nimikkeellä voi olla **URL**- tai **Esiversion URL**-osoite täytettynä. **URL-osoite**-kenttä on tyhjä, jos tuotetta ei julkaistu verkkokaupassa esimerkiksi siksi, että sen tila on luonnos. **URL-osoite** on tyhjä, jos kauppa on suojattu salasanalla esimerkiksi siksi, että se on kehityskauppa. Useimmissa tapauksissa voit tarkistaa **Esiversion URL-osoitteen** avulla, miltä tuote näyttää julkaisun jälkeen.

## <a name="run-item-synchronization"></a>Suorita nimikkeiden synkronointi

Kohteiden synkronointi kokonaan tai osittain voidaan suorittaa monella eri tavalla.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Nimikkeiden alkusynkronointi Business Centralista Shopifyhin

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet**, valitse sitten vastaava linkki.
2. Valitse **Lisää nimikkeitä** -toiminto.
3. Syötä koodi **Ostoskoodi**-kenttään. Jos avaat **Shopify-tuote**-ikkunan **ostoskortti**-sivulla, ostoskoodi täytetään automaattisesti.
4. Jos olet määrittänyt näköistiedoston ja varaston synkronoinnin, voit sisällyttää ne samaan prosessiin. Niiden sisällyttäminen samaan prosessiin on kätevää esittelyskenaarioissa tai kun käsitellään pienempiä tietomääriä.
5. Määritä nimikkeiden suodattimet tarpeen mukaan. Voit suodattaa esimerkiksi nimikenumeron tai nimikekategorian koodin mukaan.
6. Valitse **OK**.

Tuloksena syntyvät nimikkeet hintoineen luodaan Shopifyssa automaattisesti. Tekemiesi valintojen mukaan ne voivat sisältää kuvia ja varastomääriä. Toiminto voi kestää jonkin aikaa, jos useita nimikkeitä on lisätty.

Vaihtoehtoisesti voit synkronoida yhden kohteen valitsemalla **Lisää Shopifyhyn**-toiminnon **Tuotekortti**-sivulla.  

> [!NOTE]  
> Kohteiden alkuperäinen synkronointi kohteesta [!INCLUDE[prod_short](../includes/prod_short.md)] Shopifyhyn ei ota huomioon **Synkronoi kohde** - ja **Voi päivittää Shopify-tuotteita** -asetusta. 

### <a name="sync-products-from-shopify-to-business-central"></a>Synkronoi tuotteita Shopifysta Business Centraliin

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida nimikkeet avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi tuotteet** -toiminto.

Vaihtoehtoisesti voit käyttää **Synkronoi tuotteet** - toimintoa **Shopify-tuotteet**-sivulla tai hae **Synkronoi tuotteet** -eräajoa.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoittaminen](background.md#to-schedule-recurring-tasks).

### <a name="ad-hoc-updates-of-shopify-products"></a>Shopify-tuotteiden Ad-Hoc-päivitykset

Kun tietueet on päivitettävä **Shopify-tuote**-taulukossa, seuraavat muutokset synkronoidaan Shopifyn kanssa.

Päivitys:

* **Tila** - voit valita aktiivisen, arkistoidun tai luonnoksen.
* **SEO:n otsikko**
* **SEO:n kuvaus**

Poisto:

**Toimenpide poistetuille tuotteille** **Shopify-ostoskortti** -sivun arvon perusteella tuote päivitetään Shopifyssa, kun tietue poistetaan **Shopify-tuotteet**-sivulta.

* **Tyhjä**: mitään ei tapahdu. Tarvittaessa sinun täytyy suorittaa tarvittavat toimet **Shopify-järjestelmänvalvojasta**.
* **Tila luonnokseksi**: Shopifyn tuotteen tilaksi on asetettu *Luonnos*.
* **Tilaksi arkistoitu**: tuote on arkistoitu Shopifyssa.

## <a name="sync-item-images"></a>Synkronoi nimikekuvat

Kuvien synkronointi voidaan määrittää synkronoiduille nimikkeille. Valitse seuraavista vaihtoehdoista:

* **Poistettu käytöstä**: Kuvan synkronointi on poistettu käytöstä.
* **Shopifyhin**: kuvia nimikkeistä viedään Shopifyhin.
* **Shopifysta**: kuvat Shopifysta tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan.

Kuvan synkronointi voidaan alustaa kahdella alla kuvatulla tavalla.

### <a name="sync-product-images-from-the-shopify-shop-page"></a>Synkronoi tuotekuvat Shopify-myymäläsivulla

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida kuvat avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi tuotekuvat** -toiminto.

### <a name="sync-product-images-from-the-shopify-products-page"></a>Synkronoi tuotekuvat Shopify-tuotesivulta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet**, valitse sitten vastaava linkki.
2. Valitse **Synkronoi tuotekuvat** -toiminto.

### <a name="image-synchronization-remarks"></a>Kuvien synkronoinnin huomautukset

* Kun viet kuvia [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmästä Shopifyhin, kuvat korvaavat aiemmin viedyt kuvat. Aiemmat kuvat eivät ole enää käytettävissä.
* Jos poistat kuvan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, Shopifyssa olevaa kuvaa ei poisteta samalla. Sinun täytyy poistaa vanhoja kuvia manuaalisesti **Shopify-järjestelmänhallinnassa**.
* Shopifyhin vietävien kuvien on täytettävä Shopifyn vaatimukset. Muussa tapauksessa et voi tuoda niitä. Lisätietoja median vaatimuksista on kohdassa [Tuotemediatyypit osoitteessa help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## <a name="sync-prices-with-shopify"></a>Synkronoi hintoja Shopifyn kanssa

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

### <a name="sync-prices-from-the-shopify-products-page"></a>Synkronoi hinnat Shopify-tuotesivulla

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet**, valitse sitten vastaava linkki.
2. Valitse **Synkronoi tuotteet Shopifyhin** -toiminto.

### <a name="price-calculation-remarks"></a>Hintalaskennan huomautukset

* Hinnan määrittämisessä [!INCLUDE[prod_short](../includes/prod_short.md)] käyttää "alin hinta" -logiikkaa. Alhaisin hintalogiikka ei kuitenkaan huomioi nimikekortissa määritettyä yksikköhintaa, jos hinta on määritelty hintaryhmässä. Tämä pätee, vaikka nimikekortin hinnan yksikkökohtainen hinta on pienempi.
* Kun haluat laskea hintoja, yhdistin luo nimikkeelle tilapäisen myyntitarjouksen, jonka määrä on 1, ja käyttää vakiohinnan laskentalogiikkaa. Vain määrään 1 sovellettavia hintoja ja alennuksia käytetään. Et voi viedä eri hintoja tai alennuksia määrän perusteella.
* Liitin lähettää hintojen päivityspyynnön Shopifyhin jos hinta kohteessa [!INCLUDE[prod_short](../includes/prod_short.md)] on muuttunut. Jos esimerkiksi synkronoit tuotteet ja hinnat ja muutit sitten hintaa Shopifyssa, valitsemalla **Synkronoi hinnat kohteeseen Shopify** -toiminnolla ei ole vaikutusta hintaan Shopifyssa, koska liittimen laskema uusi hinta on sama kuin Shopify-varianttiin tallennettu hinta edellisestä synkronoinnista. **Vertaa hintaan** päivitetään vain, jos päähinta on muuttunut.

## <a name="sync-inventory-to-shopify"></a>Synkronoi varasto Shopifyhin

Varaston synkronointi voidaan määrittää jo synkronoiduille nimikkeille. On täytettävä kaksi ehtoa:

1. Shopifyssa olevalle tuotteelle otettava käyttöön varastoseuranta. Jos nimikkeitä viedään Shopifyhin, harkitse **Seuratun varaston** vaihto-ohjelman käyttöönottoa **Shopify-ostos**-sivulla. Lue lisää [Nimikkeiden vienti Shopifyhin](synchronize-items.md#export-items-to-shopify) -osasta.
2. **Shopify-sijaintien** synkronoinnin on oltava käytössä.

### <a name="to-enable-inventory-sync"></a>Varaston synkronoinnin ottaminen käyttöön

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida varaston avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **sijainnit** -toiminto, jolla **Shopify-myymäläsijainnit** avataan.
4. Valitse **Hae Shopify-sijainnit** -toiminto, jos haluat tuoda kaikki Shopifyssa määritetyt sijainnit. Voit etsiä niitä [**Sijainnit**](https://www.shopify.com/admin/settings/locations)-asetuksista **Shopify-järjestelmänvalvojastasi**.
5. Lisää **sijaintisuodatus** -kenttään sijainteja, jos haluat sisällyttää varaston vain tietyistä sijainneista. Voit siis syöttää arvoksi *ITÄ|LÄNSI*, jolloin varasto vain näistä kahdesta sijainnista on myynnissä verkkokaupan kautta.
6. Valitse varaston laskentatapa, jota käytetään valituissa Shopify-sijainneissa.
7. Ota **Tuotteen oletussijainti** käyttöön, jos haluat, että sijaintia käytetään varastotietueiden luonnissa ja jos haluat osallistua varaston synkronointiin.

Voit alustaa varaston synkronoinnin kahdella alla kuvatulla tavalla.

### <a name="sync-inventory-from-the-shopify-shop-page"></a>Synkronoi varasto Shopify-myymäläsivulta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida varaston avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi varasto** -toiminto.

### <a name="sync-inventory-from-the-shopify-products-page"></a>Synkronoi varasto Shopify-tuotesivulta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-tuotteet** ja valitse vastaava linkki.
2. Valitse **Synkronoi varasto** -toiminto.

### <a name="inventory-remarks"></a>Varaston huomautukset

* Varaston laskentaan kaksi vakiomenetelmää: **Oletettu saatavilla oleva päivän saldo** ja **Vapaa varasto (ei varattu)**. Laajennettavuuden avulla voit lisätä vaihtoehtoja. Saat lisätietoja laajennettavuudesta siirtymällä [esimerkkeihin](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify#stock-calculation). 
* Voit tarkistaa Shopifysta saadut varastotiedot **Shopify-varaston tietoruutu** -sivulta. Tässä tietoruudussa on yleiskuvaus Shopify-varastosta ja viimeisestä lasketusta varastosta [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa. Sijaintia kohti on yksi tietue.
* Jos Shopifyn varastotiedot poikkeavat [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelman **Arvioidusta käytettävissä olevasta saldosta**, varastotiedot päivitetään Shopifyssa.
* Kun lisäät uuden sijainnin Shopifyhyn, sitä varten on lisättävä myös varastotietueita. Shopify ei tee sitä automaattisesti olemassa oleville tuotteille ja varianteille, eikä yhdistin synkronoi näiden nimikkeiden varastomääriä uudessa sijainnissa. Saat lisätietoja siirtymällä kohtaan [Varaston määrittäminen sijainteihin](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).
* Sekä **Business Centralin täyttämispalveluja** että normaalit sijainteja tuetaan, ja niitä voidaan käyttää toimitukseen ja varastoon.

#### <a name="example-of-calculation-of-projected-available-balance"></a>Esimerkki oletetun saatavilla olevan saldon laskemisesta

Nimikettä A saatavilla on 10 kappaletta ja niille on kaksi avointa myyntitilausta. Toinen on maanantaille, jossa määrä on *Yksi*, ja toinen torstaille, jossa määrä on *Kaksi*. Riippuen siitä, milloin synkronoit varaston, järjestelmä päivittää varastotason Shopifyssa käyttämällä eri määriä:

|Milloin varaston synkronointi suoritetaan|Varastotason päivittämiseen käytetty arvo|Kommentti|
|------|-----------------|-----------------|
|Tiistai|9|Varasto 10 miinus myyntitilaus asetettu lähetettäväksi maanantaina|
|Perjantai|7|Varasto 10 miinus molemmat myyntitilaukset|

#### <a name="example-of-calculation-of-free-inventory-not-reserved"></a>Esimerkki vapaan varaston (ei varattu) laskemisesta

Nimikettä A saatavilla on 10 kappaletta ja niille on kolme avointa myyntitilausta. Yksi tilaus määrällä *1* varattu nimiketapahtumasta, yksi määrällä *2* ei varattu ja yksi määrällä *3* varattu ostotilauksesta. Tämän menetelmän osalta synkronointipäivämäärällä ei ole merkitystä.

|Varastotason päivittämiseen käytetty arvo|Kommentti|
|-----------------|-----------------|
|9|Varasto 10 vähennettynä myyntitilauksella, jolla on varastoa varattuna nimiketapahtumasta. Muut myyntitilaukset ohitetaan.|

### <a name="two-approaches-to-manage-fulfillments"></a>Kaksi tapaa hallita täyttämisiä

Täyttämiseen on Shopifyssa kaksi tapaa:

* Shopifyhyn sisältyvä täyttäminen ja varaston seuranta
* Kolmannen osapuolen täyttäminen ja varaston seuranta

Kunkin Shopifyn tuotteen varasto voi olla joko Shopifyn tai 3PL-palvelun varastoima.

Jos käytössä on Shopifyn täyttäminen, Shopifyhyn voidaan määrittää useita sijainteja. Kun tilaus on luotu, Shopify valitsee sijainnin saatavuuden ja prioriteetin perusteella. Lisäksi voidaan määrittää, missä sijainnissa tiettyä tuotetta on tarkoitus seurata. Esimerkki: sijainnissa *Esittelytila* ei ole koskaan myyntiä.

Jos käytössä 3PL, 3PL-palvelu huolehtii fyysisestä käsittelystä, joten sijainteja ei tarvita. 3PL-palvelu Varastointiyksikkö-kenttä on tulossa pakolliseksi.

Kun on päätetty, missä sijainnissa nimikettä seurataan, Shopify luo tietueet **Varastomäärä**-taulukossa, johon varaston saatavuus voidaan päivittää manuaalisesti.

Yhdistin tukee kumpaakin tilaa. Se voi lähettää varastoa useisiin Shopify-sijainteihin tai toimia täyttämispalveluna.

[!INCLUDE[prod_short](../includes/prod_short.md)]in kannalta nimikettä luotaessa ja lähetettäessä se Shopifyhyn halutaan myös

* Määrittää **Tuotteen oletussijainti** -vaihtopainikkeella, käytetäänkö nimikkeen täyttämiseen Shopifyta vai 3PL-palvelua. Käytössä on aina **Business Centralin täyttämispalvelu**, mutta käytössä voi myös muita täyttämispalveluita, jos myös muita sovelluksia on asennettu. **Tuotteen oletussijainti** voidaan ottaa käyttöön vain yhdessä tietueessa, jos täyttämispalvelua halutaan käyttää. 
* määrittää **Tuotteen oletussijainti** -vaihtopainikkeella, mitä sijainteja halutaan käyttää varaston seurantaan. **Tuotteen oletussijainti** voidaan ottaa käyttöön useissa sijainneissa, joissa **On jakelupalvelu** on poistettu käytöstä. Kannattaa muistaa, että pääsijainnin varastoa seurataan aina.

#### <a name="whats-the-difference"></a>Vaihtoehtojen erot

Shopify-täyttäminen on kätevä käytettäessä Shopify-myyntipisteitä ja kun fyysisiä myymälöitä on useita. Fyysisen myymälän työntekijän halutaan olevan perillä nykyisestä varastosta. Siinä tapauksessa Shopifyhyn ja [!INCLUDE[prod_short](../includes/prod_short.md)]iin luodaan useita sijainteja ja **Tuotteen oletussijainti** aktivoidaan kaikissa näissä sijainneissa.  

Jos logistiikka käsitellään [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, jossa voi olla tarvittava määrä jakelukeskukset ilmaisevia sijainteja, sijainteja ei tarvitse luoda Shopifyssa, -yhdistin luo Business Centralin täyttämispalvelut automaattisesti ja varasto voi linkittää sijaintisuodattimien kautta useista sijainneista yhteen täyttämispalvelutietueeseen. Tämän seurauksena Shopifyssa ei ole tietoa siitä, mistä tavaroita lähetetään – sillä on vain seurantatietoja, kun taas [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa voit valita kohteen saatavuuden ja läheisyyden perusteella.

#### <a name="example-of-using-default-product-location-toggle"></a>Esimerkki Tuotteen oletussijainti -vaihtopainikkeen käyttämisestä

Seuraavat sijainnit näkyvät, kun **Hae Shopify-sijainnit** -toiminto on valittu **Shopify-sijainnit**-sivulla:

|Nimi|On jakelupalvelu|On ensisijainen|
|------|-----------------|-----------------|
|Pääasiallinen| |**Kyllä**|
|Toissijainen| | |
|Business Centralin täyttämispalvelu|**Kyllä**| |

Tuotteen oletussijainti -vaihtopainikkeen käyttöönoton vaikutuksen tarkastelu:

|Niiden sijaintien nimi, joissa Tuotteen oletussijainti on otettu käyttöön vaihtopainikkeella|Vaikutus tuotteen luontiin Shopifyssa|
|------|-----------------|
|Pääasiallinen| Varaston varastointipaikka: useita sijainteja; valitut sijainnit: pääasiallinen (ensisijainen) |
|Pääasiallinen ja toissijainen| Varaston varastointipaikka: useita sijainteja; valitut sijainnit: pääasiallinen ja toissijainen |
|Business Centralin täyttämispalvelu|Varaston varastointipaikka: Business Centralin täyttämispalvelu; valitut sijainnit: (sovellus) Business Centralin täyttämispalvelu|
|Business Centralin täyttämispalvelu ja pääasiallinen| Virhe: Shopify-vakiosijainteja ei voi käyttää täyttämispalvelusijaintien kanssa|

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
