---
title: Määritä Shopify-yhteyden verot
description: 'Määrittää, miten Shopifyn ja Business Centralin verot määritetään.'
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# <a name="set-up-taxes-for-the-shopify-connection"></a>Määritä Shopify-yhteyden verot

Tässä artikkelissa selvitetään, miten eri asetukset Shopifyssa vaikuttavat kaupan hintoihin ja veroihin, jotka näkyvät asiakkaalle. Katsomme myös, miten määrittää [!INCLUDE[prod_short](../includes/prod_short.md)] tukemaan Shopifyn asetuksia. Tätä artikkelia ei ole tarkoitettu kattavaksi verotusoppaaksi. Saat lisätietoja paikalliselta veroviranomaiselta tai veroasiantuntijalta.  

Artikkelissa oletetaan, että olet velvollinen maksamaan veroja myydessäsi tavaroita paikallisesti tai kansainvälisesti.

## <a name="if-you-sell-domestically"></a>Jos myyt kotimaassa

Kun olet määrittänyt oman Shopifyn keräämään veroja kotimaassa tai -alueella, voit päättää, miten haluat näyttää hinnat kaupassa.

Voit määrittää, sisällytetäänkö verot hintoihin, ottamalla kaikki **Kaikki hinnat sisältävät ALV:n** -valinnan käyttöön tai poistamalla sen käytöstä [**Verot ja velvollisuudet**](https://www.shopify.com/admin/settings/taxes) -asetuksissa **Shopify-hallinnassa**.

Valinta on yleensä käytössä seuraavissa maissa:

* Australia
* Itävalta
* Belgia
* Tšekin tasavalta
* Tanska
* Suomi
* Ranska
* Saksa
* Islanti
* Italia
* Alankomaat
* Uusi-Seelanti
* Norja
* Espanja
* Ruotsi
* Sveitsi
* Yhdistynyt kuningaskunta. 

Tällaisilla markkinoilla tuotekortissa määritetty 100 EUR hinta sisältää jo arvonlisäveron (ALV). Hinta, sisältäen ALV:n, näkyy asiakkaalle myymälässä ja kassalla.  

USA:ssa ja Kanadassa asiakkaat eivät odota hintojen sisältävän veroa. Vero lisätään kassalla, joten **Kaikki hinnat sisältävät ALV:n** -valinta on yleensä pois päältä. Tässä tapauksessa tuotekortissa määritetty hinta $100 vastaa hintaa ilman veroa. Kassalla verot lisätään hintaan.

Jos haluat tukea skenaariota, jossa **Kaikki hinnat sisältävät ALV:n** on valittuna, kohteessa [!INCLUDE[prod_short](../includes/prod_short.md)] täytä seuraavat kentät **Shopify-ostoskortin** sivulla:  

1. Ota käyttöön **Hinnat sisältävät ALV:n**.  
2. Valitse **ALV-liiketoiminnan kirjausryhmä** -kentässä kotimaan asiakkaille käytettävä kirjausryhmä.  

Määritä nimikehinnat nyt **nimikekortti**- tai **myyntihintaluettelo**-kentässä joko veroineen tai ilman niitä. Kun tuot hintoja Shopifyhyn, [!INCLUDE [prod_short](../includes/prod_short.md)] laskee hinnan niin, että se sisältää kotimaiset verot, ja näyttää sitten kyseisen hinnan Shopifyn tuotteessa.

[!Note]
> Nämä asetukset vaikuttavat hintojen vientiin. Kun tuot tilauksia Shopifysta, **Hinnat sisältävät ALV:n** -kentän asetus **asiakasmallista** Shopify-ostoskortista tai asiakasmallista maata kohti. Vaikka käytät tuotujen tilausten oletusasiakasta, sinun täytyy täyttää **Asiakasmallin koodi**.

## <a name="if-you-sell-internationally"></a>Jos myyt ulkomailla

Tässä osassa tutkitaan sellaisten skenaarioiden asetuksia, joissa sinulta kerätään veroja, kun myyt toiseen maahan, kuten muihin EU-maihin.

Tällä hetkellä Shopify-yhdistin sallii vain yhden hinnan viemisen. Shopify käyttää automaattisesti paikallisia veroja, valuuttoja ja pyöristystä. **Kaikkiin hintoihin sisältyy vero** -vaihtoehto, joka johtaa seuraavissa alikohdissa kuvattuihin toimintoihin.

### <a name="all-prices-include-tax-is-selected"></a>Kaikki hinnat sisältävät ALV:n on valittu

|-|Kotimaan myynti|Ulkomaa, jossa keräät veroja|Ulkomaa, jossa et kerää veroja|
|------------------------|--------|--------|--------|
|Hinta näkyy kaupassa|1200|1200|1200|
|Veroprosentti|20|25|0|
|Hinta kassalla|1200|1200|1200|

Hinta asiakkaalle säilyy ennallaan, riippumatta heidän sijainnistaan, mutta marginaali muuttuu eri maiden verokantojen vuoksi.

### <a name="all-prices-include-tax-is-not-selected"></a>Kaikki hinnat sisältävät ALV:n ei ole valittu

|-|Kotimaan myynti|Ulkomaa, jossa keräät veroja|Ulkomaa, jossa et kerää veroja|
|------------------------|--------|--------|--------|
|Hinta näkyy kaupassa|1 000|1 000|1 000|
|Veroprosentti|20|25|0|
|Hinta kassalla|1200|1250|1 000|

Shopify lisää paikalliset verot tuotekortissa määritetyn hinnan päälle sen perusteella, mihin tavarat toimitetaan.

## <a name="dynamic-tax-inclusive-pricing"></a>Dynaaminen verot sisältävä hinnoittelu

Maissa on erilaiset vaatimukset, jotka koskevat verottoman hinnan sisällyttämistä. Jos haluat, että hinnat sisältävät ALV:n automaattisesti, voit ottaa [dynaamisen verot sisältävän hinnoittelun](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) käyttöön Shopifyssa.

Valitse **Sisällytä tai jätä pois verot asiakkaan maan mukaan** **Muut markkinat - Asetukset** -osassa [**Markkinat**](https://www.shopify.com/admin/settings/markets)-asetuksissa **Shopify-järjestelmänhallinnassa**.  

> [!NOTE]
> Tämä asetus ei vaikuta hintoihin kotimaan markkinoilla, joita ohjaa **Kaikki hinnat sisältävät veron** -vaihtoehto.

### <a name="all-prices-include-tax-is-selected-1"></a>Kaikki hinnat sisältävät ALV:n on valittu

|-|Kotimaan myynti|Ulkomaa, jossa vero sisältyy hintaan|Ulkomaa, jossa vero ei sisälly hintaan|
|------------------------|--------|--------|--------|
|Hinta näkyy kaupassa|1200|1250|1 000|
|Veroprosentti|20|25|10|
|Hinta kassalla|1200|1250|1100|

Kunkin asiakkaan hinta muuttuu heidän sijaintinsa mukaan.

### <a name="all-prices-include-tax-is-not-selected-1"></a>Kaikki hinnat sisältävät ALV:n ei ole valittu

|-|Kotimaan myynti|Ulkomaa, jossa vero sisältyy hintaan|Ulkomaa, jossa vero ei sisälly hintaan|
|------------------------|--------|--------|--------|
|Hinta näkyy kaupassa|1 000|1250|1 000|
|Veroprosentti|20|25|10|
|Hinta kassalla|1200|1250|1100|

> [!NOTE]
> **Kaikki hinnat sisältävät veron** -vaihtoehto ei muuta tapaa, jolla hinnat näytetään kansainvälisille asiakkaille.

## <a name="if-you-sell-to-eu-customers"></a>Jos myyt EU-asiakkaille

Eri EU-mailla on erilaiset paikalliset verokannat. Jos kuitenkin olet EU:n alueella ja myyt muihin EU-maihin, voit käyttää joissakin tapauksissa paikallista verokantaa.  

Valitse [**verot ja velvollisuudet**](https://www.shopify.com/admin/settings/taxes) -kohdan **Euroopan unioni** -osiosta **kerää ALV** -ruutu **Shopify-järjestelmänhallinnassa**.

|Kerää ALV|ALV-prosentti|
|-|-|
|Mikroyritysten vapauttaminen|Kotimaan veroprosentin käyttäminen kaikessa myynnissä EU:ssa|
|Keskitetty palvelupiste tai maakohtainen rekisteröinti|Käytä asiakkaan maan ALV-prosenttia|

### <a name="collect-vat-set-to-one-stop-shop-registration"></a>ALV-joukon nouto yhden luukun rekisteröinnistä

Seuraavassa esimerkissä **Kaikki hinnat sisältävät veron** -vaihtoehto on käytössä. Tuotekortissa olevan hinnan arvo on *1200*.

|-|Kotimaan myynti|Ulkomaa|
|------------------------|--------|--------|
|Hinta näkyy kaupassa|1200|1250|
|Veroprosentti|20|25|
|Hinta kassalla|1200|1250|

### <a name="collect-vat-set-to-micro-business-exemption"></a>ALV:n kerääminen mikroyritysten vapautuksesta

Seuraavassa esimerkissä **Kaikki hinnat sisältävät veron** -vaihtoehto on käytössä. Tuotekortissa olevan hinnan arvo on *1200*.

|-|Kotimaan myynti|Ulkomaan veroprosentti on 25 prosenttia.|
|------------------------|--------|--------|
|Hinta näkyy kaupassa|1200|1200|
|Veroprosentti|20|20|
|Hinta kassalla|1200|1200|

Shopify ei ota huomioon ulkomaan veroprosenttia lopullista hintaa laskettaessa ja käyttää kotimaan veroprosenttia.

## <a name="importing-shopify-orders-sold-to-international-customers"></a>Kansainvälisille asiakkaille myytyjen Shopify-tilausten tuominen

Jos keräät veroja useista maista, sinun on määritettävä maakohtaiset asetukset kohdassa [!INCLUDE[prod_short](../includes/prod_short.md)]. On olemassa syy, miksi tämä asetus on välttämätön. Kun myyntiasiakirja luodaan [!INCLUDE[prod_short](../includes/prod_short.md)]-ohjelmassa, [!INCLUDE [prod_short](../includes/prod_short.md)] laskee verot sen sijaan, Shopifysta tuodut verot käytetään uudelleen.

Maa-/aluekohtaiset asetukset valitaan **Shopify-asiakasmalli**-sivulla. Voit määrittää **oletusasiakasnron** tai **Asiakasmallinron**. Varmista kummassakin tapauksessa, että valittuun asiakkaaseen tai malliin on täytetty seuraavat kentät:

1. **Yleinen liiketoiminnan kirjausryhmä** (käytetään ulkomaan asiakkaille).
2. **ALV-liiketoiminnan kirjausryhmä** (käytetään ulkomaan asiakkaille).
3. **Hinnat sisältävät ALV:n** (yhdenmukaistettu asetus Shopify-puolella):

* Valitse **Kyllä**, jos **kaikki hinnat sisältävät ALV:n** -asetus on käytössä ja jos **Sisällytä tai sulje pois vero asiakkaan maan perusteella** on poistettu käytöstä.
* Valitse **Ei**, jos **kaikki hinnat sisältävät ALV:n** -asetus on poissa käytöstä ja jos **Sisällytä tai sulje pois vero asiakkaan maan perusteella** on poistettu käytöstä.
* Valitse **Kyllä**, jos **sisällytä tai poissulje verot asiakkaan maan perusteella** on käytössä ja maa tai alue on luetteloitu kohdassa [verot sisällyttävät maat](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Valitse **Ei**, jos **sisällytä tai poissulje verot asiakkaan maan/alueen perusteella** on käytössä ja maa/alue ei ole luetteloitu kohdassa [verot sisällyttävät maat/alueet](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

> [!NOTE]
> **Hinnat sisältävät ALV:n** -kentän asetus tulee mallista, ei tietyltä asiakkaalta. On tärkeää määrittää asiakasmalli.

## <a name="other-tax-remarks"></a>Muut verohuomautukset

Kun tuotu Shopify-tilaus sisältää tietoja veroista, verot lasketaan uudelleen, kun luot myyntiasiakirjan. Tämä uudelleenlaskenta tarkoittaa, että on tärkeää, että ALV-/veroasetukset ovat [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa oikein.

* Tuotteiden useat vero- tai ALV-prosentit. Esimerkiksi jotkin tuoteluokat ovat kelvollisia alennettuihin veroprosentteihin. Voit käyttää [veron ohitus](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) -toimintoa Shopifyssa. Kun nimikkeet tuodaan ja luodaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, ne käyttävät veroasetuksia, jotka on määritetty Shopify-kaupan nimikemallin koodikohdassa. Ennen tilausten tuomista tällaisille nimikkeille sinun täytyy päivittää tuotteen ALV-kirjausryhmä.  
* Osoiteriippuvainen veroaste. Käytä **veroalueprioriteetti**-kenttää yhdessä **asiakasmallit**-taulukon kanssa, kun haluat korvata vakiologiikan, joka täyttää myyntiasiakirjan **veroaluekoodin**. **Veroalueen prioriteetti** -kentässä määritetään prioriteetti, josta toiminnon tulisi ottaa tietoja maasta tai alueesta ja osavaltiosta tai maakunnasta. Tämän jälkeen Shopify-asiakasmallien vastaava tietue tunnistetaan ja **Veroalueen koodi**-, **Verovelvollinen**- ja **Liiketoiminnan ALV-kirjausryhmä** -kenttiä käytetään, kun myyntiasiakirja luodaan.  

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
