---
title: Myyntitilausten synkronoiminen ja täyttäminen
description: Määritä ja suorita myyntitilauksen tuonti ja käsittely Shopifysta.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: bef02c5fcbc2b6174e8a3f746a97f0e11564dcf6
ms.sourcegitcommit: 902da19b0ab7a3fbc051cd69ab2802f30d0f378f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2022
ms.locfileid: "9213687"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Myyntitilausten synkronoiminen ja täyttäminen

Tässä artikkelissa kuvataan tarvittavat asetukset ja vaiheet, jotka täytyy suorittaa myyntitilausten synkronoimiseksi ja täyttämiseksi Shopifylla [!INCLUDE[prod_short](../includes/prod_short.md)]issa.

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Tilausten tuonnin määrittäminen Shopify-ostoskortissa

Tavallinen Shopify-tilaus voi sisältää välisumman lisäksi muita kustannuksia, kuten kuljetusmaksuja tai tippejä, jos ne ovat käytössä. Nämä summat kirjataan suoraan KP-tilille, jota haluat käyttää tietyille tapahtumatyypeille:

- **Toimituskulutili**
- **Myytyjen lahjakorttien tili**: lisätietoja on kohdassa [Lahjakortti](synchronize-orders.md#gift-cards)
- **Tippitili**  

Ota käyttöön **Automaattiset tilaukset**, joiden avulla voit luoda myyntiasiakirjoja automaattisesti [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, kun Shopify-tilaus on tuotu.
[!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelman myyntiasiakirjassa on linkki Shopify-tilaukseen. Jos valitset **Shopify--tilausnro asiakirjarivillä** -kentän, tämä tieto toistetaan myyntiriveillä, joiden tyyppi on *Kommentti*.

**Veroalueen lähde** -kentässä voit määrittää prioriteetin, jonka mukaan veroaluekoodi tai liiketoiminnan ALV-kirjausryhmä valitaan osoitteen perusteella. Tämä vaihe koskee sekä myyntiveroa että arvonlisäveroa käyttäviä maita. Lisätietoja on kohdassa [Verohuomautukset](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Toimitustavan yhdistäminen

**Toimitustavan koodi** Shopifysta tuoduille myyntiasiakirjoille, voidaan täyttää automaattisesti. **Toimitusehdon yhdistämismääritys** täytyy määrittää.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälät** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat määrittää kartoituksen avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Lähetystavan kartoitus** -toiminto. Tämä luo automaattisesti tietueet toimitustavoille, jotka on määritetty **Shopify-hallintaportaalisi** [**Toimitus**](https://www.shopify.com/admin/settings/payments)-asetuksissa.
4. **Nimi**-kentässä voit nähdä toimitus tavan nimen Shopifysta.
5. **Syötä toimitusehdon koodi** ja vastaava toimitustapa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

> [!NOTE]  
> Jos myyntitilaukseen liittyy useita toimituskuluja, vain yksi valitaan toimitustavaksi ja liitetään myyntiasiakirjaan.

### <a name="payment-method-mapping"></a>Maksutavan yhdistäminen

Täyttääksesi **Maksutapakoodin** myyntiasiakirjoille, jotka on automaattisesti tuotu Shopifysta, sinun tulee määrittää **Maksutavan yhdistämismääritys**.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat määrittää kartoituksen avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Maksutavan yhdistämismääritys** -toiminto.
4. Syötä Shopifyn maksutavan nimi kenttiin **Yhdyskäytävä** ja **Luottokorttiyhtiö**. Tietueet luodaan automaattisesti, kun tuot Shopify-tilauksia.
5. **Syötä maksuehdon koodi** ja vastaava maksutapa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.
6. Määritä **prioriteetti** tapauksissa, joissa asiakas käyttää useaa maksutapaa. Korkeimman prioriteetin maksutapa valitaan myyntiasiakirjassa. Jos molemmilla maksutavoilla on sama prioriteetti, käytetään maksutapaa, jossa on korkein summa.

> [!NOTE]  
> Jos vastaavan maksutavan **Vastatilin tyyppi**- ja **Vastatilin nro** -kentät on täytetty [!INCLUDE[prod_short](../includes/prod_short.md)]issa, järjestelmä luo laskun kirjaamisen yhteydessä *Maksu*-tyyppisen vastatapahtuman ja lisää sen *Lasku*-tyyppiin asiakkaan kirjanpitotapahtumassa.

### <a name="location-mapping"></a>Sijainnin kartta

Täyttääksesi **sijaintikoodin** myyntiasiakirjoille, jotka on automaattisesti tuotu Shopifysta, sinun tulee määrittää **Shopify-myymälöiden sijainnit**.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat määrittää sijaintien kartoituksen avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Sijainnit** -toiminto, jolla **Shopify-myymäläsijainnit** avataan.
4. Valitse **Hae Shopify-sijainnit** -toiminto, jos haluat tuoda kaikki Shopifyssa määritetyt sijainnit. Voit etsiä niitä [**Sijainnit**](https://www.shopify.com/admin/settings/locations)-asetuksista **Shopify-hallinta** -paneelista. Huomaa, että *Oletus*-arvona olevaa sijaintia käytetään tuotaessa täyttymättömiä Shopify-tilauksia.
5. Syötä **oletussijaintikoodi** ja vastaava sijainti [!INCLUDE[prod_short](../includes/prod_short.md)]issa.

> [!NOTE]  
> Sinun täytyy määrittää sijaintien kartoitus, jos **Sijainti pakollinen** -valitsin on päällä **Varastonhallinnan asetukset** -kortissa, sillä muutoin et voi luoda myyntiasiakirjoja.

## <a name="run-the-order-synchronization"></a>Suorita tilausten synkronointi

Seuraavassa kuvataan, miten myyntitilaukset tuodaan ja päivitetään.

> [!NOTE]  
> Arkistoituja tilauksia Shopify ei voi tuoda. Poista **Arkistoi tilaus automaattisesti** -valinta käytöstä **Shopify-hallintapaneelin** **Kassa**-asetusten **Tilauksen käsitteleminen** -osiosta varmistaaksesi, että kaikki tilaukset tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)]iin. Jos sinun täytyy tuoda arkistoituja tilauksia, käytä **Shopify-hallintapaneelin** [Tilaukset](https://www.shopify.com/admin/orders)-sivun **Palauta tilauksia arkistosta** -toimintoa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat tuoda tilauksia avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Tilaukset**-toiminto.
4. Valitse **Synkronoi tilaukset Shopifysta** -toiminto.
5. Määritä tilausten suodattimet tarpeen mukaan. Voit esimerkiksi tuoda kokonaan maksetut tilaukset tai ne, joiden riskitaso on alhainen.
6. Valitse **OK**-painike.

Vaihtoehtoisesti voit etsiä **synkronoituja tilauksia Shopifysta** -erätyötä.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoittaminen](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Tuotujen tilausten tarkistaminen

Kun tuonti on valmis, voit tutkia Shopify-tilausta ja löytää kaikkia siihen liittyvät tiedot, kuten maksutapahtumat, toimituskulut, riskitason tai täydennykset, jos tilaus oli jo täytetty Shopifyssa. Voit myös tarkastella mitä tahansa asiakkaalle lähetettyä tilausvahvistusta valitsemalla **Shopify-tilasivu**-toiminnon.

> [!NOTE]  
> Voit siirtyä **Shopify-tilaukset**-ikkunaan suoraan, jolloin näet tilaukset, joissa on *avoin* tila kaikista kaupoista. Jos haluat tarkastella valmiita tilauksia, sinun täytyy avata **Shopify-tilaukset**-sivu tietystä **Shopify-ostoskortti**-ikkunasta.

## <a name="create-sales-documents-in-business-central"></a>Luo myyntiasiakirjoja Business Centralissa

Jos **Tilausten automaattinen luominen**-vaihto on otettu käyttöön **Shopify-ostoskortissa**, [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelma yrittää luoda myyntiasiakirjan, kun tilaus tuodaan. Jos sinulla esiintyy ongelmia, kuten jos asiakas tai tuote puuttuu, sinun täytyy korjata ongelmat ja luoda myyntitilaus uudelleen.

### <a name="to-create-sales-documents"></a>Myyntiasiakirjojen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida tilaukset avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Tilaukset**-toiminto.
4. Valitse tilaus, jolle haluat luoda myyntiasiakirjan ja valitse **Luo myyntiasiakirjat** -toiminto.
5. Valitse **Kyllä**.

Jos Shopify-tilaus edellyttää täyttämistä, **myyntitilaus** luodaan. Täytettyjen Shopify-tilausten, kuten vain lahjakortin sisältävien tilausten tai jo Shopifyssa käsiteltyjen tilausten, osalta luodaan **Myyntilasku**.

Myyntiasiakirja luodaan nyt, ja sitä voidaan hallita [!INCLUDE[prod_short](../includes/prod_short.md)]in vakiotoimintojen avulla.

### <a name="manage-missing-customers"></a>Puuttuvien asiakkaiden hallinta

Jos asetuksesi estävät asiakkaan luomisen automaattisesti ja sopivaa asiakasta ei löydy, sinun täytyy kohdistaa asiakas Shopify-tilaukseen manuaalisesti. Voit tehdä tämän muutamalla eri tavalla:

- Voit määrittää **Myyntiasiakasnron** suoraan **Shopify-tilaukset**-sivulta valitsemalla asiakkaan olemassa olevien asiakkaiden luettelosta.
- Voit valita asiakasmallin koodin ja luoda ja kohdistaa asiakkaan sitten **Shopify-tilaukset**-sivun **Luo uusi asiakas** -toiminnolla.
- Voit yhdistää aiemmin luodun **Shopify-asiakkaan** asiakkaaseen **Shopify-asiakas**-ikkunassa ja valita sitten **Shopify-tilaukset** -sivulla **Etsi yhdistämismääritys** -toiminto.

### <a name="tax-remarks"></a>Verohuomautukset

Tuotu Shopify-tilaus sisältää verotiedot, mutta verot lasketaan uudelleen, kun luot myyntiasiakirjan, joten on tärkeää, että ALV-/veroasetukset on määritetty oikein [!INCLUDE[prod_short](../includes/prod_short.md)]issa.

- Tuotteiden useat ALV-/veroprosentit. Esimerkiksi jotkin tuoteluokat ovat oikeutettuja alennettuihin veroprosentteihin. Nimikkeiden täytyy olla [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä ja niitä on yhdistettävä Shopify-tuotteisiin. Muussa tapauksessa puuttuvien nimikkeiden automaattisessa luonnissa käytetään tuotteen ALV-kirjausryhmää.

- Osoiteriippuvainen veroaste. Käytä **Veroalueen prioriteetti** -kenttää yhdessä **Asiakasmallit**-taulukon kanssa korvataksesi standardilogiikan, joka täyttää myyntiasiakirjan **Veroalueen koodi** -kentän. **Veroalueen prioriteetti** -kenttä määrittää prioriteetin, jota käytetään maan/alueen ja osavaltion/provinssin tietojen määrittämiseen. Tämän jälkeen Shopify-asiakasmallien vastaava tietue löytyy ja **Veroalueen koodi**-, **Verovelvollinen**- ja **Liiketoiminnan ALV-kirjausryhmä** -kenttiä käytetään, kun myyntiasiakirja luodaan.

- Hinta sisältäen veron. Luodun myyntiasiakirjan **Hinnat sisältävät veron**- / **Hinnat sisältävät ALV:n** -kenttä ei riipu asiakkaasta, vaan **Shopify-kauppa-kortti**-sivun **Asiakasmalli**-kentästä tai Asiakasmalli maata kohti -kentästä.

### <a name="impact-of-order-editing"></a>Tilausten muokkaamisen vaikutus

Shopifyssa:

|Muokkaa|Vaikutus|
|------|-----------|
|Muuta täyttämissijaintia | Alkuperäinen sijainti synkronoidaan [!INCLUDE[prod_short](../includes/prod_short.md)]iin. |
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

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Synkronoi toimitukset Shopifyhin** ja valitse sitten vastaava linkki.
2. Määritä toimitusten suodattimet tarpeen mukaan. Voit esimerkiksi päivittää tiettynä päivämääränä kirjatun toimituksen.
3. Valitse **OK**-painike.

Tilaus Shopifyssa merkitään täytetyksi. Asiakas saa automaattisesti toimitusilmoituksen sähköpostilla tai tekstiviestillä. Jos toimitukselle on määritetty kuljetusliike ja seurantakoodi, sähköposti sisältää seurantatiedot.

> [!NOTE]  
> Muista suorittaa **Synkronoi tilaukset Shopifysta** -toiminto päivittääksesi tilauksen jakelun tilan [!INCLUDE[prod_short](../includes/prod_short.md)]issa. Yhdistintoiminto arkistoi myös täysin maksetut ja täytetyt tilaukset sekä Shopifyssa että [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa edellyttäen, että ehdot täyttyvät.

### <a name="shipping-agents-and-tracking-url"></a>Kuljetusliikkeet ja seuranta-URL-osoite

Jos **Kirjattu myyntitoimitus** -asiakirja sisältää **Kuljetusliikkeen koodi**- ja/tai **Kollin seurantanro** -kentän, nämä tiedot lähetetään Shopify'hin ja asiakkaalle toimituksen vahvistussähköpostissa.

Seurantayritys-kenttä täytetään seuraavassa järjestyksessä (suurimmasta pienimpään) kuljetusliikkeen tietueen perusteella:

- **Shopify-seurantayritys**
- **Nimi**
- **Koodi**

Jos kuljetusliikkeen tietueen **Paketin seurannan URL-osoite** -kenttä on täytetty, toimitusvahvistus sisältää myös seuranta-URL-osoitteen.

## <a name="gift-cards"></a>Lahjakortit

Voit myydä Shopify-kaupassa lahjakortteja, joita voidaan käyttää oikeiden tuotteiden maksamiseen.

Kun on kyse lahjakorteista, on tärkeää syöttää **myydyn lahjakortin tili** -kenttään arvo **Shopify-ostoskortti**-ikkunassa. Myyty lahjakortti synkronoidaan yhdessä rivintilausten kanssa. Kohdistettu lahjakortti tuodaan myös tilauksen mukana, mutta nyt tapahtumana. Huomaa, että lahjakortti ei vähennä laskun summaa.

Jos haluat tarkastella myönnettyjä ja käytettyjä lahjakortteja, valitse ![Kerro-ominaisuuden avaava Hehkulamppu.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Lahjakortit** ja valitse sitten vastaava linkki.

## <a name="transactions-and-payouts"></a>Tapahtumat ja maksut

Kun asiakas suorittaa kassaprosessin loppuun verkkokaupassa, maksujen tiedot tallennetaan **tapahtumana**. Tilaukseen voi liittyä useita tapahtumia, esimerkiksi kun asiakas maksaa osan tilauksestaan lahjakortilla ja loput luottokortilla tai PayPalilla. 

Jos maksupalvelun tarjoajasi on Shopify Payment, näet tietoja asiakkailta saaduista maksuista maksupalvelun tarjoajan mukaan sekä Shopifysta pankkitilillesi lähetetyt maksut. 

### <a name="transactions"></a>Tapahtumat

Shopifyssa tapahtuvat maksutapahtumat synkronoidaan tilausten kanssa ja näytetään *Shopify-tilaukset*-sivulla.

Tarkastellaksesi kaikkia tapahtumia, valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tapahtumat** ja valitse vastaava linkki.

Jos olet määrittänyt maksutapojen kartoituksen, luodulle myyntiasiakirjalle kohdistetaan maksutavan koodi. Lisätietoja on kohdassa [Maksutavan yhdistäminen](#payment-method-mapping).

### <a name="payouts"></a>Maksut

Jos kauppasi käyttää Shopify Payment -palvelua, saat maksut *Shopify-maksuina*, kun asiakas maksaa käyttämällä Shopify Payments -palvelua ja nopeutettua kassaprosessia.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida maksuja avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Synkronoi maksut** -toiminto.

Tarkastellaksesi kaikkia maksuja, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksut** ja valitse vastaava linkki.

**Maksut** on tarkoitettu vain tiedonannoksi eivätkä ne vaikuta pääkirjanpitoon tai pankkikirjanpitoon, mutta ne voivat olla hyödyllisiä, kun tarkastat tiliotettasi.

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
