---
title: Myyntitilausten synkronoiminen ja täyttäminen
description: Määritä ja suorita myyntitilauksen tuonti ja käsittely Shopifysta.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 4e8d640f6de61d642037a55fdfeb09e32f197a96
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809011"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Myyntitilausten synkronoiminen ja täyttäminen

Tässä artikkelissa kuvataan tarvittavat asetukset ja vaiheet, jotka tulee suorittaa myyntitilausten synkronoimiseksi ja toteuttamiseksi.

## <a name="set-import-of-orders-on-the-shopify-shop-card"></a>Tilausten tuonnin määrittäminen Shopify-ostoskortissa

Tavallisella Shopify-tilauksella voi olla ylimääräisiä summia, kuten kuljetusmaksuja tai, jos käytössä, tippejä. Nämä summat kirjataan suoraan KP-tileille. Valitse KP-tili, jota käytetään tietyissä tapahtumissa:

- **Toimituskulutili**
- **Myyty lahjakortti -tili**, lisätietoja on kohdassa [Lahjakortti](synchronize-orders.md#gift-cards).
- **Tippitili**  

Ota käyttöön **Automaattiset tilaukset**, joiden avulla voit luoda myyntiasiakirjoja automaattisesti [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, kun Shopify-tilaus on tuotu.
[!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelman myyntiasiakirjassa on linkki Shopify-tilaukseen. Jos valitset **Shopify-tilausnumeron asiakirjassa asiak. rivi** -kentän, tämä tieto toistetaan myyntiriveillä, joiden tyyppi on *Kommentti*.

**Veroaluelähde**-kentässä voit määrittää, miten veroaluekoodi- tai liiketoiminnan ALV-kirjausryhmä valitaan osoitteen perusteella. Tämä vaihe on merkityksellinen maissa, joissa on myyntivero, mutta sitä voi käyttää ALV-maissa. Lisätietoja on kohdassa [Verotukselliset huomautukset](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Toimitustavan yhdistäminen

**Toimitustavan koodi** Shopifysta tuoduille myyntiasiakirjoille, voidaan täyttää automaattisesti. **Toimitusehdon yhdistämismääritys** täytyy määrittää.

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat määrittää yhdistämisen avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Lähetystavan kartoitus** -toiminto. [**Toimitus**](https://www.shopify.com/admin/settings/payments)-asetuksissa **Shopify-järjestelmänvalvojassa** määritettyjen toimitustapojen tietueet luodaan automaattisesti.
4. **Nimi**-kentässä voit nähdä toimitus tavan nimen Shopifysta.
5. **Syötä toimitusehdon koodi** ja vastaava toimitustapa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

> [!NOTE]  
> Jos myyntitilaukseen liittyy useita toimituskuluja; vain yksi valitaan toimitustavaksi ja liitetään myyntiasiakirjaan.

### <a name="payment-method-mapping"></a>Maksutavan yhdistäminen

Täyttääksesi **Maksutapakoodin** myyntiasiakirjoille, jotka on automaattisesti tuotu Shopifysta, sinun tulee määrittää **Maksutavan yhdistämismääritys**.

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat määrittää yhdistämisen avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Maksutavan yhdistämismääritys** -toiminto.
4. Syötä Shopifyn maksutavan nimi kenttiin **Yhdyskäytävä** ja **Luottokorttiyhtiö**. Tietueet luodaan automaattisesti, kun tuot Shopify-tilauksia.
5. **Syötä maksuehdon koodi** ja vastaava maksutapa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.
6. Määritä **prioriteetti** tapauksissa, joissa asiakas käyttää useaa maksutapaa. Korkeimman prioriteetin maksutapa valitaan myyntiasiakirjassa. Jos molemmilla maksutavoilla on sama prioriteetti, käytetään maksutapaa, jossa on korkein summa.

## <a name="run-order-synchronization"></a>Suorita tilausten synkronointi

Seuraavassa kuvataan, miten myyntitilaukset tuodaan ja päivitetään.

> [!NOTE]  
> Arkistoituja tilauksia Shopify ei voi tuoda. Poista käytöstä **Arkistoi tilaus automaattisesti** **Kassa**-asetusten **Tilauksen käsittely** -osiossa **Shopify-järjestelmänvalvojassasi** varmistuaksesi, että kaikki tilaukset tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Jos sinun on tuotava arkistoituja tilauksia, käytä Shopify-järjestelmänvalvojan [Tilaukset](https://www.shopify.com/admin/orders)-sivun **Poista tilaus arkistosta** -toimintoa.

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat tuoda tilaukset avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Tilaukset**-toiminto.
4. Valitse **Synkronoi tilaukset Shopifysta** -toiminto.
5. Määritä tilausten suodattimet tarpeen mukaan. Voit esimerkiksi tuoda kokonaan maksetut tilaukset tai ne, joiden riskitaso on alhainen.
6. Valitse **OK**-painike.

Vaihtoehtoisesti voit etsiä **synkronoituja tilauksia Shopifysta** -erätyötä.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoitus](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Tuotujen tilausten tarkistaminen

Kun tuonti on valmis, voit tutkia Shopify-tilausta ja löytää kaikki siihen liittyvät tiedot. Voit esimerkiksi etsiä maksutapahtumat, toimituskulut, riskitason tai täyttämiset, jos tilaus on jo täytetty Shopifyssa. Voit myös tarkastella mitä tahansa asiakkaalle lähetettyä tilausvahvistusta valitsemalla **Shopify-tilasivu**-toiminnon.

> [!NOTE]  
> Voit siirtyä **Shopify-tilaukset**-ikkunaan suoraan, jolloin näet tilaukset, joissa on *avoin* tila kaikista kaupoista. Jos haluat tarkastella valmiita tilauksia, sinun täytyy avata **Shopify-tilaukset**-sivu tietystä **Shopify-ostoskortti**-ikkunasta.

## <a name="create-sales-documents-in-business-central"></a>Luo myyntiasiakirjoja Business Centralissa

Jos **Tilausten automaattinen luominen**-vaihto on otettu käyttöön **Shopify-ostoskortissa**, [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelma yrittää luoda myyntiasiakirjan, kun tilaus tuodaan. Jos prosessissa esiintyy ongelmia, kuten jos asiakas tai tuote puuttuu, sinun on korjattava ongelma. Tämän jälkeen voit yrittää luoda myyntitilauksen uudelleen.

### <a name="to-create-sales-documents"></a>Myyntiasiakirjojen luominen

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida tilaukset avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Tilaukset**-toiminto.
4. Valitse tilaus, jolle haluat luoda myyntiasiakirjan ja valitse **Luo myyntiasiakirjat** -toiminto.
5. Valitse **Kyllä**.

Jos Shopify-tilaus edellyttää täyttämistä, **Myyntitilaus** luodaan. Täysin täytettyjen Shopify-tilausten, kuten vain lahjakortin sisältävien tilausten tai jo Shopifyssa käsiteltyjen tilausten, osalta luodaan **Myyntilasku**.

Myyntiasiakirja luodaan nyt, ja sitä voidaan hallita [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelman vakiotoimintojen avulla.

### <a name="manage-missing-customers"></a>Puuttuvien asiakkaiden hallinta

Jos asetukset estävät asiakkaan luomisen automaattisesti ja oikeaa olemassa olevaa asiakasta ei löydy, voit määrittää Shopify-tilauksen manuaalisesti asiakkaalle. Vaihtoehtoja on muutamia:

- Voit määrittää **Myyntiasiakasnron** suoraan **Shopify-tilaukseen** valitsemalla asiakkaan olemassa olevien asiakkaiden luettelosta.
- Voit valita asiakasmallin koodin, luoda ja määrittää asiakkaan **Luo uusi asiakas** -toiminnolla **Shopify-tilaus** -kohdassa.
- Voit yhdistää aiemmin luodun **Shopify-asiakkaan** asiakkaaseen **Shopify-asiakas**-ikkunassa ja valita sitten **Shopify-tilauksessa** **Etsi yhdistämismääritys** -toiminto.

### <a name="tax-remarks"></a>Verohuomautukset

Kun tuotu Shopify-tilaus sisältää tietoja veroista, verot lasketaan uudelleen, kun luot myyntiasiakirjan. Uudelleenlaskennan vuoksi on tärkeää, että ALV-/veroasetukset ovat [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa oikein.

- Useat tuotevero-/ALV-prosentit. Esimerkiksi jotkin tuoteluokat ovat oikeutettuja alennettuihin veroprosentteihin. Nimikkeiden täytyy olla [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä ja niitä on yhdistettävä Shopify-tuotteisiin. Muussa tapauksessa käytetään automaattista puuttuvien nimikkeiden luontia, tuotteen ALV-kirjausryhmä otetaan käyttöön.

- Osoiteriippuvainen veroaste. Käytä **veroalueprioriteetti**-kenttää yhdessä **asiakasmallit**-taulukon kanssa, kun haluat korvata vakiologiikan, joka täyttää myyntiasiakirjan **veroaluekoodin**. **Veroalueen prioriteetti** -kentässä määritetään prioriteetti, josta toiminnon tulisi ottaa tietoja maasta/alueesta ja tilasta. Tämän jälkeen Shopify-asiakasmallien vastaavat tietueet löytyvät ja **veroaluekoodi**, **Verovelvollinen** ja **liiketoiminnan ALV-kirjausryhmä** ovat käytössä, kun myyntiasiakirja luodaan.

## <a name="synchronize-shipments-to-shopify"></a>Synkronoi toimitukset Shopifyhin

Kun Shopify-tilauksesta luotu myyntitilaus toimitetaan, voit synkronoida toimitukset Shopifyhin.

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Synkronoi toimitukset Shopifyhin** ja valitse sitten vastaava linkki.
2. Määritä toimitusten suodattimet tarpeen mukaan. Voit esimerkiksi päivittää tiettynä päivämääränä kirjatun toimituksen.
3. Valitse **OK**-painike.

Tilaus Shopifyssa merkitään täytetyksi. Asiakas saa automaattisesti toimitusilmoituksen sähköpostilla tai tekstiviestillä. Jos kuljetusliike ja seurantakoodi on määritetty toimitukseen, seurantatiedot sisältyvät sähköpostiin.

> [!NOTE]  
> Muista käyttää **Synkronoi tilauksia Shopifysta** -ohjelmaa, jos haluat päivittää tilauksen toimitustilan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Yhdistintoiminto arkistoi myös täysin maksetut ja täytetyt tilaukset sekä Shopifyssa että [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa edellyttäen, että ehdot täyttyvät.

### <a name="shipping-agents-and-tracking-url"></a>Kuljetusliikkeet ja seuranta-URL-osoite

Jos **Lähetetty myyntitoimitus** -asiakirja sisältää **kuljetusliikkeen koodin** ja/tai **Paketin seurantanumeron**, nämä tiedot lähetetään Shopifyhin ja toimitusvahvistus sähköpostissa loppuasiakkaalle.

Seurantayritys täytetään kuljetusliikkeen tietueeseen seuraavien prioriteettien perusteella (suurimmasta pienimpään):

- **Shopify-seurantayritys**
- **Nimi**
- **Koodi**

Jos kuljetusliikkeen tietueeseen on täytetty **paketin seurannan URL-osoite** -kenttä, toimitusvahvistus sisältää myös seuranta-URL-osoitteen.

## <a name="gift-cards"></a>Lahjakortit

Shopify-myymälässä voit myydä lahjakortteja, joita voidaan myöhemmin käyttää oikeiden tuotteiden maksamiseen.

Kun on kyse lahjakorteista, on tärkeää syöttää **myydyn lahjakortin tili** -kenttään arvo **Shopify-ostoskortti**-ikkunassa. Myyty lahjakortti synkronoidaan yhdessä rivintilausten kanssa. Kohdistettu lahjakortti tuodaan myös tilauksen mukana, mutta nyt tapahtumana. Huomaa, että lahjakortti ei vähennä laskun summaa.

Jos haluat tarkastella myönnettyjä ja käytettyjä lahjakortteja, valitse ![Kerro-ominaisuuden avaava Hehkulamppu.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Lahjakortit** ja valitse sitten vastaava linkki.

## <a name="transactions"></a>Tapahtumat

Shopifyssa tapahtuneet maksutapahtumat synkronoidaan tilausten kanssa ja niitä voi tarkastella *Shopify-tilauksesta*.

Tarkastellaksesi kaikkia tapahtumia, valitse hae ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tapahtumat** ja valitse vastaava linkki.

## <a name="payouts"></a>Maksut

Jos myymäläsi Shopify payments on käytössä, saat maksuja *Shopify-maksujen* avulla, kun asiakas maksaa Shopify paymentsin ja nopeutetun kassalle siirtymisten avulla.

1. Siirry hakuun ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida maksut avataksesi **Shopify-ostoskortti**-sivun.
3. Valitse **Synkronoi maksut** -toiminto.

Tarkastellaksesi kaikkia maksuja, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksut** ja valitse vastaava linkki.

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
