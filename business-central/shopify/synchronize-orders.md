---
title: Myyntitilausten synkronoiminen ja täyttäminen
description: Määritä ja suorita myyntitilauksen tuonti ja käsittely Shopifysta.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 70c401e072e742e508b8f623ae3242d8e647ccb6
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802928"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Myyntitilausten synkronoiminen ja täyttäminen

Tässä artikkelissa kuvataan tarvittavat asetukset ja vaiheet, jotka täytyy suorittaa myyntitilausten synkronoimiseksi ja täyttämiseksi Shopifylla [!INCLUDE[prod_short](../includes/prod_short.md)]issa.

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Tilausten tuonnin määrittäminen Shopify-ostoskortissa

Syötä **Valuuttakoodi**, jos verkkokauppa käyttää eri valuuttaa kuin paikallinen valuutta (PVA). Määritetyllä valuutalla on oltava määritettynä vaihtokurssit. Jos verkkokauppa käyttää samaa valuuttaa kuin [!INCLUDE[prod_short](../includes/prod_short.md)], jätä kenttä tyhjäksi. 

Voit nähdä kaupan valuutan [Kaupan tiedot](https://www.shopify.com/admin/settings/general) -asetuksissa Shopify Adminissa. Shopify voidaan määrittää hyväksymään eri valuuttoja, mutta [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmään tuodut tilaukset käyttävät kaupan valuuttaa.

Tavallinen Shopify-tilaus voi sisältää välisumman lisäksi muita kustannuksia, kuten kuljetusmaksuja tai tippejä, jos ne ovat käytössä. Nämä summat kirjataan suoraan KP-tilille, jota haluat käyttää tietyille tapahtumatyypeille:

* **Toimituskulutili**
* **Myytyjen lahjakorttien tili**: lisätietoja on kohdassa [Lahjakortti](synchronize-orders.md#gift-cards)
* **Tippitili**  

Ota käyttöön **Automaattiset tilaukset**, joiden avulla voit luoda myyntiasiakirjoja automaattisesti [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, kun Shopify-tilaus on tuotu.

[!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelman myyntiasiakirjassa on linkki Shopify-tilaukseen. Jos valitset **Shopify--tilausnro asiakirjarivillä** -kentän, tämä tieto toistetaan myyntiriveillä, joiden tyyppi on *Kommentti*.

**Veroalueen lähde** -kentässä voit määrittää prioriteetin, jonka mukaan veroaluekoodi tai liiketoiminnan ALV-kirjausryhmä valitaan osoitteen perusteella. Tuotu Shopify-tilaus sisältää verotiedot, mutta verot lasketaan uudelleen, kun luot myyntiasiakirjan, joten on tärkeää, että ALV-/veroasetukset on määritetty oikein [!INCLUDE[prod_short](../includes/prod_short.md)]issa. Lisätietoja veroista on ohjeaiheessa [Shopify-yhteyden verojen määrittäminen](setup-taxes.md).

### <a name="shipment-method-mapping"></a>Toimitustavan yhdistäminen

**Toimitustavan koodi** Shopifysta tuoduille myyntiasiakirjoille, voidaan täyttää automaattisesti. **Toimitusehdon yhdistämismääritys** täytyy määrittää.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat määrittää kartoituksen avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Lähetystavan kartoitus** -toiminto. Tämä luo automaattisesti tietueet toimitustavoille, jotka on määritetty **Shopify-hallintaportaalisi** [**Toimitus**](https://www.shopify.com/admin/settings/payments)-asetuksissa.
4. **Nimi**-kentässä voit nähdä toimitus tavan nimen Shopifysta.
5. **Syötä toimitusehdon koodi** ja vastaava toimitustapa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

> [!NOTE]  
> Jos myyntitilaukseen liittyy useita toimituskuluja, vain yksi valitaan toimitustavaksi ja liitetään myyntiasiakirjaan.

### <a name="location-mapping"></a>Sijainnin kartta

Sijaintikartoitus tarvitaan kolmea tarkoitusta varten:

* Jos haluat synkronoida varaston, katso lisätietoja kohdasta [Synkronoi varasto Shopifyhin](synchronize-items.md#sync-inventory-to-shopify)
* Voit täyttää Shopifysta tuotujen myyntiasiakirjojen **sijaintikoodin**. Tämä on tärkeää, jos **Sijainti pakollinen** -valitsin on otettu käyttöön **Varaston asetukset** -kortissa, muuten myyntiasiakirjoja ei voi luoda.
* Shopify-tilauksen päivittäminen toimitustiedoilla **kirjattu myyntitoimitus** -sivun perusteella.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat määrittää sijaintien kartoituksen avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Sijainnit** -toiminto, jolla **Shopify-myymäläsijainnit** avataan.
4. Valitse **Hae Shopify-sijainnit** -toiminto, jos haluat tuoda kaikki Shopifyssa määritetyt sijainnit. Voit etsiä niitä [**Sijainnit**](https://www.shopify.com/admin/settings/locations)-asetuksista **Shopify-hallinta** -paneelista. Huomaa, että *Oletus*-arvona olevaa sijaintia käytetään tuotaessa täyttymättömiä Shopify-tilauksia.
5. Syötä **oletussijaintikoodi** ja vastaava sijainti [!INCLUDE[prod_short](../includes/prod_short.md)]issa.

## <a name="run-the-order-synchronization"></a>Suorita tilausten synkronointi

Seuraavassa kuvataan, miten myyntitilaukset tuodaan ja päivitetään.

> [!NOTE]  
> Arkistoituja tilauksia Shopify ei voi tuoda. Poista **Arkistoi tilaus automaattisesti** -valinta käytöstä **Shopify-hallintapaneelin** **Kassa**-asetusten **Tilauksen käsitteleminen** -osiosta varmistaaksesi, että kaikki tilaukset tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)]iin. Jos sinun täytyy tuoda arkistoituja tilauksia, käytä **Shopify-hallintapaneelin** [Tilaukset](https://www.shopify.com/admin/orders)-sivun **Palauta tilauksia arkistosta** -toimintoa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat tuoda tilauksia avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Tilaukset**-toiminto.
4. Valitse **Synkronoi tilaukset Shopifysta** -toiminto.
5. Määritä tilausten suodattimet tarpeen mukaan. Voit esimerkiksi tuoda kokonaan maksetut tilaukset tai ne, joiden riskitaso on alhainen.
6. Valitse **OK**-painike.

Vaihtoehtoisesti voit etsiä **synkronoituja tilauksia Shopifysta** -erätyötä.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoittaminen](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Tuotujen tilausten tarkistaminen

Kun tuonti on valmis, voit tutkia Shopify-tilausta ja löytää kaikkia siihen liittyvät tiedot, kuten maksutapahtumat, toimituskulut, riskitason, muut määritteet ja tunnisteet tai täydennykset, jos tilaus oli jo täytetty Shopifyssa. Voit myös tarkastella mitä tahansa asiakkaalle lähetettyä tilausvahvistusta valitsemalla **Shopify-tilasivu**-toiminnon.

> [!NOTE]  
> Voit siirtyä **Shopify-tilaukset**-ikkunaan suoraan, jolloin näet tilaukset, joissa on *avoin* tila kaikista kaupoista. Jos haluat tarkastella valmiita tilauksia, sinun täytyy avata **Shopify-tilaukset**-sivu tietystä **Shopify-ostoskortti**-ikkunasta.

## <a name="create-sales-documents-in-business-central"></a>Luo myyntiasiakirjoja Business Centralissa

Jos **Tilausten automaattinen luominen**-vaihto on otettu käyttöön **Shopify-ostoskortissa**, [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelma yrittää luoda myyntiasiakirjan, kun tilaus tuodaan. Jos sinulla esiintyy ongelmia, kuten jos asiakas tai tuote puuttuu, sinun täytyy korjata ongelmat ja luoda myyntitilaus uudelleen.

### <a name="to-create-sales-documents"></a>Myyntiasiakirjojen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida tilaukset avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Tilaukset**-toiminto.
4. Valitse tilaus, jolle haluat luoda myyntiasiakirjan ja valitse **Luo myyntiasiakirjat** -toiminto.
5. Valitse **Kyllä**.

Jos Shopify-tilaus edellyttää täyttämistä, **myyntitilaus** luodaan. Täytettyjen Shopify-tilausten, kuten vain lahjakortin sisältävien tilausten tai jo Shopifyssa käsiteltyjen tilausten, osalta luodaan **Myyntilasku**.

Myyntiasiakirja luodaan nyt, ja sitä voidaan hallita [!INCLUDE[prod_short](../includes/prod_short.md)]in vakiotoimintojen avulla.

### <a name="manage-missing-customers"></a>Puuttuvien asiakkaiden hallinta

Jos asetuksesi estävät asiakkaan luomisen automaattisesti ja sopivaa asiakasta ei löydy, sinun täytyy kohdistaa asiakas Shopify-tilaukseen manuaalisesti. Voit tehdä tämän muutamalla eri tavalla:

* Voit määrittää **Myyntiasiakasnron** ja **Laskutusasiakkaan nron** suoraan **Shopify-tilaukset**-sivulta valitsemalla asiakkaan olemassa olevien asiakkaiden luettelosta.
* Voit valita asiakasmallin koodin ja luoda ja kohdistaa asiakkaan sitten **Shopify-tilaukset**-sivun **Luo uusi asiakas** -toiminnolla.
* Voit yhdistää aiemmin luodun **Shopify-asiakkaan** asiakkaaseen **Shopify-asiakas**-ikkunassa ja valita sitten **Shopify-tilaukset** -sivulla **Etsi yhdistämismääritys** -toiminto.

### <a name="how-the-connector-chooses-which-customer-to-use"></a>Miten yhdistin valitsee käytettävän asiakkaan

*Tuo tilaus Shopifysta* -toiminto yrittää valita asiakkaat seuraavassa järjestyksessä:

1. Jos **Oletusasiakasnro** -kenttä määritetään vastaavan maan **Shopify-asiakasmallissa**, vastaavalle maalle, silloin **oletusasiakasnroa** käytetään, riippumatta **asiakkaan tuonti Shopifysta** ja **Asiakkaan yhdistämismäärityksen tyyppi** -kentistä. Lisätietoja kohdassa [Asiakasmalli maata kohti](synchronize-customers.md#customer-template-per-country).
2. Jos **Asiakkaan tuonti Shopifysta** on määritetty arvoon *Ei mitään* ja **Oletusasiakasnro** on määritetty **Shopify-ostoskortti**-sivulla, sitten **Oletusasiakasnro** käytetään.

Seuraavat vaiheet määräytyvät **asiakkaan yhdistämismäärityksen tyypin** mukaan.

* Jos se on **Ota aina oletusasiakas**, silloin yhdistin käyttää asiakasta, joka on määritetty kohdassa **oletusasiakasnro** -kentässä **Shopify-ostoskortti**-sivulla.
* Jos se on **Sähköpostilla/puhelimella**-yhdistin yrittää löytää nykyisen asiakkaan ensin tunnuksella, sitten sähköpostitse, ja sitten puhelinnumeron avulla. Jos asiakasta ei löydy - yhdistin luo uuden asiakkaan.
* Jos se on **Laskutustiedoilla**, yhdistin yrittää löytää olemassa olevan asiakkaan ensin tunnuksella ja sitten laskutusosoitteen tiedoilla. Jos asiakasta ei löydy - yhdistin luo uuden asiakkaan.

> [!NOTE]  
> Yhdistin käyttää laskutusosoitteen tietoja ja luo laskutusasiakkaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Tilausasiakas on sama kuin laskutusasiakas.

### <a name="impact-of-order-editing"></a>Tilausten muokkaamisen vaikutus

Shopifyssa:

|Muokkaa|Vaikutus|
|------|-----------|
|Muuta täyttämissijaintia | Alkuperäinen sijainti synkronoidaan [!INCLUDE[prod_short](../includes/prod_short.md)]iin. |
|Täyttämissijainnin ja täyttämisen rekisteröinti Shopifyssa| Jos tilaus oli jo tuotu, rivejä ei päivitetä. Muussa tapauksessa tuotu tilaus käyttää täyttämissijaintia. |
|Muokkaa tilausta ja muuta määrää| Tilausotsikko ja lisätaulukot päivittyvät [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, rivit eivät. |
|Muokkaa tilausta ja lisää uusi nimike | Tilausotsikko päivittyy, rivit eivät. |

[!INCLUDE[prod_short](../includes/prod_short.md)]issa:

|Muokkaa|Vaikutus|
|------|-----------|
|Muuta sijainti toiseen sijaintiin, joka on kartoitettu Shopify-sijainteihin. Kirjaa toimitus. | Kun toteutus on synkronoitu, sijainti päivittyy Shopifyssa. |
|Muuta sijainti toiseen sijaintiin, jota ei ole kartoitettu Shopify-sijainteihin. Kirjaa toimitus. | Täydennystä ei synkronoida Shopifyn kanssa. |
|Vähennä määrää. Kirjaa toimitus. | Shopify-tilaus merkitään osittain täytetyksi. |
|Lisää uusi nimike. Kirjaa toimitus. | Shopify-tilaus merkitään täytetyksi. Rivejä ei päivitetä. |

## <a name="synchronize-shipments-to-shopify"></a>Synkronoi toimitukset Shopifyhin

Kun Shopify-tilauksesta luotu myyntitilaus toimitetaan, voit synkronoida toimitukset Shopifyn kanssa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Synkronoi toimitukset Shopifyhin**, valitse sitten vastaava linkki.
2. Määritä toimitusten suodattimet tarpeen mukaan. Voit esimerkiksi päivittää tiettynä päivämääränä kirjatun toimituksen.
3. Valitse **OK**-painike.

Tilaus Shopifyssa merkitään täytetyksi. Asiakas saa automaattisesti toimitusilmoituksen sähköpostilla tai tekstiviestillä. Jos toimitukselle on määritetty kuljetusliike ja seurantakoodi, sähköposti sisältää seurantatiedot.

Vaihtoehtoisesti voit käyttää **Synkronoi toimitukset** -toimintoa Shopifyn myyntitilauksissa tai Shopifyn myyntisivuilla.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoittaminen](background.md#to-schedule-recurring-tasks).

>[Tärkeää] Kirjatulla toimitusrivillä olevalla sijainnilla, myös tyhjällä sijainnilla, täytyy olla vastaava Shopify-sijainti. Muussa tapauksessa tätä riviä ei lähetetä takaisin Shopifyhin. Lisätietoja on kohdassa [Sijainnin yhdistämismääritys](synchronize-orders.md#location-mapping).

Muista suorittaa **Synkronoi tilaukset Shopifysta** -toiminto päivittääksesi tilauksen jakelun tilan [!INCLUDE[prod_short](../includes/prod_short.md)]issa. Yhdistintoiminto arkistoi myös täysin maksetut ja täytetyt tilaukset sekä Shopifyssa että [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa edellyttäen, että ehdot täyttyvät.

### <a name="shipping-agents-and-tracking-url"></a>Kuljetusliikkeet ja seuranta-URL-osoite

Jos **Kirjattu myyntitoimitus** -asiakirja sisältää **Kuljetusliikkeen koodi**- ja/tai **Kollin seurantanro** -kentän, nämä tiedot lähetetään Shopify'hin ja asiakkaalle toimituksen vahvistussähköpostissa.

Seurantayritys-kenttä täytetään seuraavassa järjestyksessä (suurimmasta pienimpään) kuljetusliikkeen tietueen perusteella:

* **Shopify-seurantayritys**
* **Nimi**
* **Koodi**

Jos kuljetusliikkeen tietueen **Paketin seurannan URL-osoite** -kenttä on täytetty, toimitusvahvistus sisältää myös seuranta-URL-osoitteen.

## <a name="gift-cards"></a>Lahjakortit

Voit myydä Shopify-kaupassa lahjakortteja, joita voidaan käyttää oikeiden tuotteiden maksamiseen.

Kun on kyse lahjakorteista, on tärkeää syöttää **myydyn lahjakortin tili** -kenttään arvo **Shopify-ostoskortti**-ikkunassa. Myyty lahjakortti synkronoidaan yhdessä rivintilausten kanssa. Kohdistettu lahjakortti tuodaan myös tilauksen mukana, mutta nyt tapahtumana. Huomaa, että lahjakortti ei vähennä laskun summaa.

Jos haluat tarkastella myönnettyjä ja käytettyjä lahjakortteja, valitse ![Kerro-ominaisuuden avaava Hehkulamppu.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Lahjakortit**, valitse sitten vastaava linkki.

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
