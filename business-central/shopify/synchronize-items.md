---
title: Synkronoi nimikkeet ja varasto
description: Määritä ja suorita nimikkeiden synkronoinnit Shopifyn ja Business Centralin välillä
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ad69d58a84926041df1125809f748b9129cc64e2
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808957"
---
# <a name="synchronize-items-and-inventory"></a>Synkronoi nimikkeet ja varasto

**Nimikkeet** [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa vastaavat *tuotteita* Shopifyssa, kuten fyysisiä tavaroita, digitaalisia latauksia, palveluja ja lahjakortteja, joita myyt. On kaksi pääasiallista syytä synkronoida nimikkeet:

1. Ensisijaisesti tiedon hallinta suoritetaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, ja kaikki tai osa tiedoista on vietävä Shopifyhin ja tehtävä ne näkyviksi. Voit viedä nimikkeen nimen, kuvauksen, kuvan, hinnat, saatavuuden, variantit, toimittajan tiedot ja viivakoodin. Kun nimikkeet on tuotu, ne voivat tulla heti näkyviin, tai vastuuhenkilö voi tarkistaa ja parantaa niitä ensin.
2. Kun tilaus Shopifysta tuodaan, nimikkeen tiedot ovat olennaisia asiakirjan käsittelemisessä [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

Nämä kaksi skenaariota ovat aina käytössä.

Kolmas skenaario on tietojen hallinta Shopify mutta kyseisten nimikkeiden tuonti joukkona [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Tämä skenaario voi olla hyödyllinen tiedonsiirtotapahtumissa, kun aiemmin luotu verkkokauppa halutaan yhdistää uuteen [!INCLUDE[prod_short](../includes/prod_short.md)] -ympäristöön.

## <a name="to-define-item-synchronizations"></a>Nimikkeiden synkronointivaltuuksien määrittäminen

1. Valitse haku ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kauppa**. Avaa myymälä, jolle haluat määrittää nimikkeen synkronoinnin.
2. Valitse haluamasi vaihtoehdot **synkronointikohde**-kentästä. <br>Seuraavassa taulukossa kuvaillaan eri vaihtoehtojen erot.

|Asetus|Kuvaus|
|------|-----------|
|**Tyhjä**| Tuotteet tuodaan yhdessä tilausten tuonnin kanssa. Tuotteet viedään Shopifyhin, jos käyttäjä suorittaa **Lisää nimike** -toiminnon **Shopify-tuotteet** -sivulla. Tämä prosessi on oletustoiminta. |
|**Shopifyhin**| Valitse tämä vaihtoehto, jos aiot päivittää nimikkeet manuaalisesti **Lisää nimike** -toiminnon käynnistämän synkronoinnin jälkeen **Synkronoi tuote** -toiminnolla tai toistuvien päivitysten työjonon kautta. Muista ottaa käyttöön **voi päivittää Shopify-tuotetta** -kenttä. Jos se ei ole käytössä, se on sama kuin **tyhjä**-asetus. Lisätietoja on kohdassa [Nimikkeiden vienti Shopifyhin](synchronize-items.md#export-items-to-shopify)|
|**Lähettäjä Shopify**| Valitse tämä vaihtoehto, jos aiot tuoda tuotteita Shopifysta joukkona; joko manuaalisesti käyttämällä **Synkronoi tuote** -toimintoa tai työjonon kautta toistuvia päivityksiä varten. Jos asetusta ei ole valittu, se on yhtä kuin **tyhjä**-valinta. Lisätietoja nimikkeiden tuonnista: [kohteiden tuonti Shopifysta](synchronize-items.md#import-items-from-shopify)|

## <a name="import-items-from-shopify"></a>Tuo nimikkeitä Shopifysta

Joko tuot nimikkeitä Shopifysta joukkona tai yhdessä tilausten tuonnin kanssa, nämä nimikkeet lisätään ensin **Shopify-tuote**- ja **Shopify-variantti**-taulukoihin. Seuraavien asetusten avulla voit hallita prosessia:

|Kenttä|Kuvaus|
|------|-----------|
|**Luo tuntemattomat nimikkeet automaattisesti**|Kun Shopify-tuotteet ja-variantit tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan, [!INCLUDE[prod_short](../includes/prod_short.md)] -funktio yrittää aina etsiä vastaavaa tietuetta ensin nimikeluettelosta. **Varastointiyksikön yhdistäminen** vaikuttaa siihen, miten kohdistus suoritetaan, ja luo uuden nimikkeen ja/tai nimikevariantin. Ota tämä valinta käyttöön, jos haluat luoda uuden nimikkeen tai kun vastaavaa tietuetta ei ole olemassa. Uusi nimike luodaan tuotujen tietojen ja **Nimikemallikoodin** avulla. Jos tämä valinta ei ole käytössä, sinun on luotava nimike manuaalisesti ja käytettävä **Yhdistä tuote** -toimintoa **Shopify tuotteet** -sivulla.|
|**Nimikemallin koodi**|Käytetään yhdessä **Tuntemattomien nimikkeiden luominen automaattisesti** -toiminnon kanssa. <br> Valitse malli, jota käytetään automaattisesti luoduille nimikkeille.|
|**Varastointiyksikön yhdistämismääritykset**|Valitse nimikkeen/variantti määrityksen ja luonnin aikana Shopifysta tuotujen **varastointiyksikön** arvojen käyttötarkoitus. Lisätietoja on kohdassa [Miten Shopify-tuotteessa määritellyt varastointiyksikkö ja viivakoodi vaikuttavat kartoitukseen ja tuotteiden ja muunnelmien luomiseen](synchronize-items.md#how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|**Varastointiyksikön kenttäerotin**|Käytetään yhdessä **Varastointiyksikön yhdistämismääritykset** kanssa, joka on asetettu arvoon **Tuotenro + Varianttikoodi** -vaihtoehto.<br> Määritä erotin, jota käytetään SKU-luettelon jakamista varten. <br>Jos esimerkiksi luot Shopifyssa muunnelman varastointiyksiköllä '1000/001', kirjoita '/' **Varastointiyksikön erotin** -kenttään saadaksesi tuotenumeron [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa muodossa "1000" ja nimikkeen muunnelman koodi "001".
|**Version etuliite**|Käytetään yhdessä **Varastointiyksikön yhdistämismäärityksen** kanssa , jonka arvona on **Varianttikoodi** tai **Nimikenro + varianttikoodi** -vaihtoehtoja varmistusstrategiaksi silloin, kun Shopifysta lähtevä varastointiyksikkö on tyhjä.<br>Jos haluat luoda nimikevariantin [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa automaattisesti, sinun täytyy syöttää arvo **koodiin**. Oletusarvon mukaan käytetään Shopifysta tuodussa varastointiyksikkökentässä määritettyä arvoa. Jos varastointiyksikkö on kuitenkin tyhjä, se luo koodin alkaen määritetystä variantti-etuliitteestä ja "001"-numerosta.|
|**Shopify voi päivittää nimikkeen**| Valitse tämä vaihtoehdoista, jos haluat päivittää nimikkeet ja/tai variantit automaattisesti.|

### <a name="how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central"></a>Miten Shopifyssa määritetyt varastointiyksiköt ja viivakoodit vaikuttavat nimikkeiden ja varianttien kartoittamiseen ja luomiseen Business Centralissa

Kun tuotteet tuodaan Shopifysta **Shopify-tuotteet**- ja **Shopify-variantit**-taulukoihin, [!INCLUDE[prod_short](../includes/prod_short.md)] yrittää löytää aiemmin luotuja tietueita. Seuraavassa taulukossa kuvaillaan eri vaihtoehtojen erot **Varastointiyksikön yhdistämismääritykset** -kentässä.

|Asetus|Vaikutus yhdistämiseen|Vaikutus luomiseen|
|------|-----------------|------------------|
|**Tyhjä**|Varastointiyksikkö-kenttää ei käytetä nimikkeen yhdistämisrutiinissa.|Ei vaikutusta nimikkeen luomiseen. <br>Estää varianttien luonnin. On hyödyllistä, kun myyntitilauksessa käytetään vain päänimikettä. Variantti voidaan silti linkittää manuaalisesti **Shopify-tuote**-ikkunasta.|
|**Nimikkeen nro**|Valitse, jos varastointiyksikkö-kentässä on nimikkeen nro.|Ei vaikutusta nimikkeen luomiseen ilman variantteja. Jos nimikkeellä on variantteja, jokainen variantti luodaan erillisenä nimikkeenä.<br> Jos esimerkiksi Shopifylla on tuote, jossa on kaksi versiota ja niiden varastointiyksiköt ovat '1000' ja '2000', [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa järjestelmä luo kaksi nimikettä numeroilla ' 1000' ja '2000'.|
|**Varianttikoodi**|Varastointiyksikkö-kenttää ei käytetä nimikkeen yhdistämisrutiinissa.|Ei vaikutusta nimikkeen luomiseen. Kun nimikevariantti luodaan, koodina käytetään varastointiyksikkökentän arvoa. Jos varastointiyksikkö on tyhjä, luodaan **varianttietuliite**-kentän avulla koodi.|
|**Nimikenro + versiokoodi**| Valitse, jos varastointiyksikkö-kentässä on nimikkeen nro. ja nimikkeen varianttikoodi, joka on erotettu **varastointiyksikkö-kenttäerotin** -kentässä määritetyllä arvolla.|Kun nimike luodaan, käytetään varastointiyksikkö-kentän arvon ensimmäistä osaa **nro**-arvona. Jos varastointiyksikkö on tyhjä, nimikkeen nro luodaan käyttämällä numerosarjoja, jotka on määritetty **Nimikemallikoodissa** tai **Nimikenumeroissa** **Varaston määritys** -ikkunassa.<br>Kun nimike luodaan, varianttifunktio käyttää varastointiyksikkö-kentän arvon toista osaa muodossa **Koodi**. Jos varastointiyksikkö on tyhjä, luodaan **varianttietuliite**-kentän avulla koodi.|
|**Toimittajan nimikenro**| Valitse, sisältääkö varastointiyksikkö-kenttä toimittajan nimikkeen numeron. Tässä tapauksessa **Nimiketoimittajanroa** ei käytetä **Nimikekortti**-ikkunassa, vaan **Toimittajan nimikenumeroa** **Nimiketoimittajaluettelosta**. Jos löydetyssä *nimiketoimittajaluettelo*-tietueessa on varianttikoodi, tätä varianttikoodia käytetään Shopify-variantin yhdistämiseen.|Jos vastaava toimittaja on [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä, varastointiyksikköarvoa käytetään **Toimittajan nimikenro** -tyyppinä **nimikekortissa** ja **Nimike viitteenä** -toimittajatyyppinä. <br>Estää varianttien luonnin. Se on hyödyllinen silloin, kun haluat käyttää päänimikettä vain myyntitilauksessa. Voit silti yhdistää variantin manuaalisesti **Shopify-tuote**-ikkunasta.|
|**Viivakoodi**| Valitse, jos varastointiyksikkö-kentässä on viivakoodi. Haku suoritetaan **Nimikeviittausten** osalta, jotka ovat tyyppiä toimittaja. Jos löydetyssä nimikeviitetietueessa on varianttikoodi, tätä varianttikoodia käytetään Shopify-variantin yhdistämiseen.|Ei vaikutusta nimikkeen luomiseen. <br>Estää varianttien luonnin. Se voi olla hyödyllistä, jos myyntitilauksessa käytetään vain päänimikettä. Variantti voidaan silti linkittää manuaalisesti **Shopify-tuote**-ikkunasta.|

Seuraava taulukko luonnostelee **Viivakoodi**-kentän vaikutuksen.

|Vaikutus yhdistämiseen|Vaikutus luomiseen|
|-----------------|------------------|
|Haku suoritetaan Shopifyn viivakoodi-kentässä määritellylle arvolle **Nimikeviitteistä**, jonka tyyppi on viivakoodi. Jos löydetyssä nimikeviitetietueessa on varianttikoodi, tätä varianttikoodia käytetään Shopify-variantin yhdistämiseen.|Viivakoodi tallennetaan nimikkeen ja nimikevariantin **nimikeviitteenä**.|

> [!NOTE]  
> Voit käynnistää valittujen tuotteiden/varianttien tai kaikkien tuotujen yhdistämättömien tuotteiden yhdistämisen valitsemalla **Etsi tuotteen yhdistäminen** (valituille) tai **Etsi yhdistämisiä** (kaikille).

## <a name="export-items-to-shopify"></a>Vie nimikkeet Shopifyhin

Valitse elementit nimikeluettelosta, joka viedään Shopifyhin. Käytä **Lisää nimike**-toimintoa **Shopify-tuotteet**-ikkunassa lisätäksesi nimikkeitä Shopify-tuoteluetteloon.

Seuraavien asetusten avulla voit hallita nimikkeiden vientiprosessia:

|Kenttä|Kuvaus|
|------|-----------|
|**Asiakkaan hintaryhmä**|Määritä nimikkeen hinta Shopifyssa. Tämän asiakkaan hintaryhmän myyntihinta on otettu. Jos ryhmää ei ole syötetty, käytetään nimikekortin hintaa.|
|**Asiakkaan alennusryhmä**|Määritä alennus, jota käytetään nimikkeen hinnan laskennassa Shopifyssa. Alennetut hinnat tallennetaan **hinta**-kenttään, ja koko hinta tallentuu **Vertaa hintaan** -kenttään.|
|**Synkronoi nimikkeen lisäteksti**|Valitsemalla tämän voit synkronoida nimikkeen lisätekstin. Koska se lisätään *kuvaukseen*, se voi sisältää HTML-koodia. |
|**Synkronoi nimikemääritteet**|Valitse tämä, jos haluat synkronoida nimikemääritteet. Määritteet muotoillaan taulukkona ja sisällytetään *kuvaus*-kenttään Shopifyssa.|
|**Kielikoodi**|Jos tämä valitaan, käännettyjä versioita käytetään otsikossa, määritteissä ja lisätekstissä.|
|**Varastointiyksikön yhdistämismääritykset**|Valitse, miten haluat täyttää varastointiyksikkökentän Shopifyssa. Tuettuja vaihtoehtoja ovat:<br> - **Nimikenro** käyttää nimikenroa sekä tuotteille että varianteille.<br> - **Nimikenro + varianttikoodi**, jolla varastointiyksikkö luodaan yhdistämällä kahden kentän arvot toisiinsa. Nimikkeille, joilla ei ole variantteja, käytetään arvona vain nimikenroa.<br>- **Nimikkeen toimittajanro** käyttää *nimikekortissa* määritettyä nimiketoimittajan numeroa sekä tuotteille että varianteille.<br> - **Viivakoodi** - käyttää viivakoodityypin **nimikeviittausta**. Tässä vaihtoehdossa noudatetaan variantteja. |
|**Varastointiyksikön kenttäerotin**|Määritä nimikkeen erotin **Nimikenro + varianttikoodi** -vaihtoehto.|
|**Varastoa seurataan**|Valitse, miten järjestelmä täyttää Shopifyn vietävien tuotteiden **seuraa varastoa** -kentän. Voit päivittää niiden tuotteiden saatavuustiedot [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmasta Shopifyssa oleville tuotteille, joiden seuranta on otettu käyttöön. Lisätietoja on myös kohdassa [Varasto](synchronize-items.md#sync-inventory-to-shopify).|
|**Oletusvarastokäytäntö**|Valitse *kiellä*, jos haluat estää Shopify-puolen negatiivisen varaston. |
|**Voi päivittää Shopify-tuotteita**|Määritä, voiko [!INCLUDE[prod_short](../includes/prod_short.md)] myös luoda nimikkeitä tai päivittää nimikkeitä. Valitse tämä vaihtoehto, jos aiot päivittää nimikkeet manuaalisesti **Lisää nimike** -toiminnon käynnistämän synkronoinnin jälkeen **Synkronoi tuote** -toiminnolla tai toistuvien päivitysten työjonon kautta. Muista valita **Shopifyhin** **Nimikkeen synkronointi** -kentässä.|

### <a name="fields-mapping-overview"></a>Kenttien yhdistämisen yleiskatsaus

|Shopify|Lähde vietäessä kohteesta [!INCLUDE[prod_short](../includes/prod_short.md)]|Kohde tuotaessa kohteeseen [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Tila|**Shopify-ostoskortissa** **luotujen tuotteiden tilan** mukaan. Lisätietoja on kohdassa [Ad-hoc-tuotteiden Shopify-päivitykset](synchronize-items.md#ad-hock-updates-of-shopify-products).|Ei käytetty.|
|Otsikko|**Kuvaus**. Jos kielikoodi on määritetty ja vastaava nimikekäännös on olemassa, käytetään nimikkeen käännöstä kuvauksen sijaan.|**Kuvaus**|
|Kuvaus|Yhdistää lisätekstit ja määritteet, jos vastaava vaihto Shopify-ostoskortissa on käytössä. Säilyttää kielikoodit.|Ei käytetty.|
|Hakukoneoptimointisivun otsikko|Korjaa arvo: tyhjä, katso [Shopify-tuotteiden Ad-hoc-päivitykset](synchronize-items.md#ad-hock-updates-of-shopify-products). |Ei käytetty.|
|Hakukoneoptimoinnin metakuvaus|Korjaa arvo: tyhjä, katso [Shopify-tuotteiden Ad-hoc-päivitykset](synchronize-items.md#ad-hock-updates-of-shopify-products). |Ei käytetty.|
|Media|**Kuva**, lisätietoja on kohdassa [Synkronoi nimikekuvat](synchronize-items.md#sync-item-images)|**Kuva**|
|Hinta|Loppuasiakkaan hinnan laskenta sisältää nimikkeen hintaryhmän, nimikkeen alennusryhmän, valuuttakoodin ja asiakasmallinkoodin. |Ei käytetty.|
|Vertailuhinta|Hinnan laskenta ilman alennusta sisältää nimikkeen hintaryhmän, nimikkeen alennusryhmän, valuuttakoodin ja asiakasmallinkoodin. |Ei käytetty.|
|Kustannus per nimike|**Yksikkökustannus**|**Yksikkökustannus**|
|Varastointiyksikkö|Katso **Varastointiyksikön yhdistämismääritykset** kohdassa [vie nimikkeitä Shopifyhin](synchronize-items.md#export-items-to-shopify)| Katso [Miten Shopify-tuotteessa määritellyt varastointiyksikkö ja viivakoodi vaikuttavat kartoitukseen ja tuotteiden ja muunnelmien luomiseen](synchronize-items.md#how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|Viivakoodi|Viivakoodityypin **nimikeviitteet**|Viivakoodityypin **nimikeviitteet**|
|Seurattava määrä|**Shopify-ostoskortin** **Seuratun varaston** mukaan. Lisätietoja on myös kohdassa [Varasto](synchronize-items.md#sync-inventory-to-shopify).|Ei käytetty.|
|Jatka myyntiä, kun varasto on loppunut|**Shopify-ostoskortin** **Oletusvarastokäytännön** mukaan. Ei tuotu.|Ei käytetty.|
|Tyyppi|**Nimikekategoriakoodin** **kuvaus**. Jos tyyppiä ei ole määritetty Shopifyssa, se lisätään mukautettuna tyyppinä.|**Nimikeluokan koodi**. Linkitys kuvauksen mukaan.|
|Toimittaja|Toimittajan **nimi** **Toimittajan nro**-kohteesta |**Toimittajan nro** Linkitys nimen mukaan.|
|Paino|**Bruttopaino**.|Ei käytetty.|
|Verotettava|Vakioarvo: käytössä.|Ei käytetty.|
|Verokoodit|**Veroryhmän koodi**. Koskee vain myyntiveroja. Lisätietoja on ohjeaiheessa [Verot](synchronize-orders.md#tax-remarks). |Ei käytetty.|

### <a name="tags"></a>Tunnisteet

Poista tuodut tunnisteen **Tunnisteet**-tietoruudusta **Shopify-tuote**-sivulla. Muokkaa tunnisteita valitsemalla **Tunnisteet**-toiminto **Shopify-tuote**-sivulla.
Jos **Shopifyhin** on valittuna **Synkronoi nimike** -kentässä, määritetyt tunnisteet viedään Shopifyhin seuraavan synkronoinnin yhteydessä.

## <a name="run-item-synchronization"></a>Suorita nimikkeiden synkronointi

Kohteiden synkronointi kokonaan tai osittain voidaan suorittaa monella eri tavalla.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Nimikkeiden alkusynkronointi Business Centralista Shopifyhin

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet** ja valitse sitten vastaava linkki.
2. Valitse **Lisää nimikkeitä** -toiminto.
3. Syötä koodi **Ostoskoodi**-kenttään. Jos avaat **Shopify-tuote**-ikkunan **ostoskortti**-ikkunasta, ostoskoodi täytetään automaattisesti.
4. Määritä nimikkeiden suodattimet tarpeen mukaan. Voit suodattaa esimerkiksi nimikenumeron tai nimikekategorian koodin mukaan.
5. Valitse **OK**.

Tuloksena syntyvät nimikkeet luodaan automaattisesti Shopifyssa hintoihin, mutta kuvat ja varastotasot eivät sisälly. Toiminto voi kestää jonkin aikaa, jos useita nimikkeitä on lisätty.

### <a name="sync-products-from-shopify-to-business-central"></a>Synkronoi tuotteita Shopifysta Business Centraliin

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida nimikkeet avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi tuotteet** -toiminto.

Vaihtoehtoisesti voit käyttää **Synkronoi tuotteet** - toimintoa **Shopify-tuotteet**-ikkunassa tai hae **Synkronoi tuotteet** -eräajoa.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoitus](background.md#to-schedule-recurring-tasks).

### <a name="ad-hock-updates-of-shopify-products"></a>Shopify-tuotteiden Ad-Hoc-päivitykset

Kun tietueet on päivitettävä **Shopify-tuote**-taulukossa, seuraavat muutokset synkronoidaan Shopifyn kanssa.

Päivitys:

* **Tila** - voit valita aktiivisen, arkistoidun tai luonnoksen.
* **SEO:n otsikko**
* **SEO:n kuvaus**

Poisto:

**Toimenpide poistetuille tuotteille** **Shopify-ostoskortti** -kohdan arvon perusteella tuote päivitetään Shopifyssa, kun tietue poistetaan **Shopify-tuotteet**-sivulta.

* **Tyhjä** - mitään ei tapahdu. Tarvittaessa käyttäjän täytyy suorittaa tarvittavat toimet Shopify-järjestelmänvalvojasta.
* **Tila luonnokseksi** - Shopifyn tuotteen tilaksi on asetettu *Luonnos*.
* **Tilaksi arkistoitu** - tuote on arkistoitu Shopifyssa.

## <a name="sync-item-images"></a>Synkronoi nimikekuvat

Kuvien synkronointi voidaan määrittää synkronoiduille nimikkeille. Voit valita seuraavista vaihtoehdoista:

* **Tyhjä** - kuvan synkronointi on poistettu käytöstä.
* **Shopifyhin** - kuvia nimikkeistä viedään Shopifyhin
* **Shopifysta** - kuvat Shopifysta tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan

Kuvan synkronointi voidaan alustaa kahdella tavalla.

### <a name="sync-product-images-from-the-shopify-shop-window"></a>Synkronoi tuotekuvat Shopify-myymäläikkunasta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida kuvat avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi tuotekuvat** -toiminto.

### <a name="sync-product-images-from-the-shopify-products-window"></a>Synkronoi tuotekuvat Shopify-tuoteikkunasta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet** ja valitse sitten vastaava linkki.
2. Valitse **Synkronoi tuotekuvat** -toiminto.

### <a name="image-synchronization-remarks"></a>Kuvien synkronoinnin huomautukset

* Kun viet kuvia [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmasta Shopifyhin, uudet kuvat lisätään Shopifyhin ja vanhat kuvat säilyvät ennallaan. Jos kuva päivitetään [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan, sinun täytyy poistaa vanhoja kuvia Shopify-ylläpitäjänä.
* Kuvat, joita viedään Shopifyhin ja jotka eivät vastaa Shopifyn määrittämiä vaatimuksia, tuodaan. Lisätietoja on kohdassa [Tuotemediatyypit osoitteessa help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## <a name="sync-prices-with-shopify"></a>Synkronoi hintoja Shopifyn kanssa

Synkronoitujen nimikkeiden hinnat voidaan viedä alla kuvatulla tavalla.

### <a name="sync-prices-from-the-shopify-products-window"></a>Synkronoi hinnat Shopify-tuoteikkunasta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet** ja valitse sitten vastaava linkki.
2. Valitse **Synkronoi tuotteet Shopifyhin** -toiminto.

### <a name="price-calculation-remarks"></a>Hintalaskennan huomautukset

* Hinnan laskennassa on tärkeää, että **oletusasiakasmalli** -kentässä on arvo. [!INCLUDE[prod_short](../includes/prod_short.md)] käyttää **VAT-yritysryhmä**-kenttää laskiessaan ALV:n sisältävän hinnan. Haluat ehkä luoda asiakashintaryhmän, jossa valitset **ALV:n sisältävä hinta** -kentän ja määrität asianmukaisen arvon **Liiketoim. ALV-kirjryh. (Hinta)** -kentässä.
* Syötä **Valuuttakoodi**, jos verkkokauppa käyttää eri valuuttaa kuin paikallinen valuutta. Määritetyllä valuutalla on oltava määritettynä vaihtokurssit. Jos verkkokauppa käyttää samaa valuuttaa kuin [!INCLUDE[prod_short](../includes/prod_short.md)], jätä kenttä tyhjäksi.
* Hinnan määrittämisessä [!INCLUDE[prod_short](../includes/prod_short.md)] käyttää "alin hinta" -logiikkaa. Se tarkoittaa sitä, että jos nimikekortissa määritetty yksikköhinta on pienempi kuin hintaryhmässä määritetty, ohjelma käyttää nimikekortin yksikköä.

## <a name="sync-inventory-to-shopify"></a>Synkronoi varasto Shopifyhin

Varaston synkronointi voidaan määrittää jo synkronoiduille nimikkeille. On täytettävä kaksi ehtoa:

1. Shopifyssa olevalle tuotteelle otettava käyttöön varastoseuranta. Jos nimikkeitä viedään Shopifyhin, harkitse **Seuratun varaston** vaihto-ohjelman käyttöönottoa **Shopify-ostos**-kortissa. Lisätietoja on kohdassa [Nimikkeiden vienti Shopifyhin](synchronize-items.md#export-items-to-shopify).
2. **Shopify-sijaintien** synkronoinnin on oltava käytössä.

### <a name="to-enable-inventory-sync"></a>Varaston synkronoinnin ottaminen käyttöön

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida varaston avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **sijainnit** -toiminto, jolla **Shopify-myymäläsijainnit** avataan.
4. Valitse **Hae Shopify-sijainnit** -toiminto, jos haluat tuoda kaikki Shopifyssa määritetyt sijainnit. Voit etsiä niitä [**Sijainnit**](https://www.shopify.com/admin/settings/locations)-asetuksista **Shopify-järjestelmänvalvojastasi**.
5. Lisää **sijaintisuodatus** -kenttään sijainteja, jos haluat sisällyttää varaston vain tietyistä sijainneista. Voit esimerkiksi syöttää *ITÄ|LÄNSI*, joten varasto vain näistä kahdesta sijainnista on myynnissä verkkokaupan kautta.
6. Ota käyttöön valittujen Shopify-sijaintien varaston synkronointi poistamalla **Poista käytöstä** -vaihtoehto.

Voit alustaa varaston synkronoinnin kahdella tavalla.

### <a name="sync-inventory-from-the-shopify-shop-window"></a>Synkronoi varasto Shopify-myymäläikkunasta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida varaston avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi varasto** -toiminto.

### <a name="sync-inventory-from-the-shopify-products-window"></a>Synkronoi varasto Shopify-tuoteikkunasta

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Shopify-tuotteet** ja valitse sitten vastaava linkki.
2. Valitse **Synkronoi varasto** -toiminto.

### <a name="inventory-remarks"></a>Varaston huomautukset

* Yhdistin laskee **Arvioidun käytettävissä olevan saldon** ja vie sen Shopifyhin.
* Voit tarkistaa Shopifysta saadut varastotiedot **Shopify-varaston tietoruutu** -sivulta. Tässä tietoruudussa on yleiskuvaus Shopify-varastosta ja viimeisestä lasketusta varastosta [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa. Sijaintia kohti on tietue.
* Jos Shopifyn varastotiedot poikkeavat [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelman **Arvioidusta käytettävissä olevasta saldosta**, varastotiedot päivitetään Shopifyssa.

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
