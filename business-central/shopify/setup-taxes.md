---
title: Määritä Shopify-yhteyden verot
description: 'Määrittää, miten Shopifyn ja Business Centralin verot määritetään.'
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# Määritä Shopify-yhteyden verot

Tässä artikkelissa selvitetään, miten eri asetukset Shopifyssa vaikuttavat kaupan hintoihin ja veroihin, jotka näkyvät asiakkaalle. Otamme myös tarkastella, miten määrittää [!INCLUDE[prod_short](../includes/prod_short.md)] tukemaan Shopifyn asetuksia. Tätä artikkelia ei ole tarkoitettu kattavaksi verotusoppaaksi. Saat lisätietoja paikalliselta veroviranomaiselta tai veroasiantuntijalta.  

Artikkelissa oletetaan, että olet velvollinen maksamaan veroja myydessäsi tavaroita paikallisesti tai kansainvälisesti.

## Jos myyt kotimaassa

Kun olet määrittänyt oman Shopifyn keräämään veroja kotimaassa tai -alueella, voit päättää, miten haluat näyttää hinnat kaupassa.
Voit hallita tätä ottamalla käyttöön tai poistamalla käytöstä **Kaikki hinnat sisältävät verot** -valinnan **Shopify-järjestelmänvalvojan** [**verot ja tullit**](https://www.shopify.com/admin/settings/taxes) -asetuksissa.

On tavallista, että tämä vaihtoehto otetaan käyttöön esimerkiksi Australiassa, Itävallassa, Belgiassa, Tšekissä, Tanskassa, Suomessa, Ranskassa, Saksassa, Islannissa, Italiassa, Alankomaissa, Uudessa-Seelannissa, Norjassa, Espanjassa, Ruotsissa, Sveitsissä ja Yhdistyneessä kuningaskunnassa. Tämänkaltaisten markkinoiden hinta *100 EUR* on määritelty tuotekortissa sisältämään arvonlisäveron (ALV) ja tämä sama hinta näkyy asiakkaalle kaupassa ja kassalla.  

Yhdysvalloissa ja Kanadassa asiakkaat odottavat näkevänsä tuotehinnat ilman veroja, jotka lisätään kassalla. **Kaikki hinnat sisältävät ALV:n** -kenttää ei siis yleensä valita. Tässä tapauksessa tuotekortissa määritetty hinta *$100* vastaa hintaa ilman veroa. Kassalla hinnan päälle lisätään verot, jotka vastaavat maksettavaa loppusummaa.

Jos haluat tukea skenaariota, jossa **Kaikki hinnat sisältävät veron** on valittuna [!INCLUDE[prod_short](../includes/prod_short.md)] -puolella, täytä **asiakasmallin koodi** -kenttä **Shopify-ostoskortti**-sivulla, jotta voit käyttää mallia seuraavilla määritetyillä kentillä:  

1. **Yleinen liiketoiminnan kirjausryhmä**, käytetään kotimaan asiakkaille.  
2. **ALV-liiketoiminnan kirjausryhmä**, käytetään kotimaan asiakkaille.  
3. **Hinnat sisältävät ALV:n** -arvo on *Kyllä*.  

Määritä nimikehinnat nyt **nimikekortti**- tai **myyntihintaluettelo**-kentässä joko veroineen tai ilman niitä. Kun tuot hintoja Shopify -järjestelmään, järjestelmä laskee hinnan niin, että se sisältää kotimaiset verot, ja näyttää sitten kyseisen hinnan Shopifyn tuotekortissa.

> [!NOTE]
> Jos olet määrittänyt Shopify-yhdistimen luomaan asiakkaat automaattisesti, sinun täytyy ehkä lisää kenttiä malliin, esimerkiksi **asiakkaan kirjausryhmä**. Jos olet käyttänyt tuotujen tilausten oletusasiakasta, varmista, että asiakkaaseen on täytetty samat kentät. Sinun tulee silti täyttää yllä esitetyn mukaisesti **Asiakkaan mallikoodi**, koska **Hinnat sisältävät veron**/**Hinnat sisältävät ALV:n** -kenttä ei riipu asiakkaasta, vaan Shopify-kauppakortin maakohtaisen asiakasmalli-kentän **Asiakasmallista**.

## Jos myyt ulkomailla

Tässä osassa tutkitaan sellaisten skenaarioiden asetuksia, joissa sinulta kerätään veroja, kun myyt toiseen maahan, kuten muihin EU-maihin.

Tällä hetkellä **Shopify-yhdistin**-laajennus tukee vain yhden hinnan vientiä. Shopify käyttää automaattisesti paikallisia veroja, valuuttoja ja pyöristystä. **Kaikkiin hintoihin sisältyy vero** -vaihtoehto, joka johtaa seuraavissa alikohdissa kuvattuihin toimintoihin.

### *Kaikki hinnat sisältävät ALV:n* on valittu

|-|Kotimaan myynti|Ulkomaa, jossa keräät veroja|Ulkomaa, jossa et kerää veroja|
|------------------------|--------|--------|--------|
|Hinta näkyy kaupassa|1200|1200|1200|
|Veroprosentti|20|25|0|
|Hinta kassalla|1200|1200|1200|

Hinta asiakkaalle säilyy ennallaan, riippumatta heidän sijainnistaan, mutta marginaali muuttuu eri maiden verokantojen vuoksi.

### *Kaikki hinnat sisältävät ALV:n* ei ole valittu

|-|Kotimaan myynti|Ulkomaa, jossa keräät veroja|Ulkomaa, jossa et kerää veroja|
|------------------------|--------|--------|--------|
|Hinta näkyy kaupassa|1 000|1 000|1 000|
|Veroprosentti|20|25|0|
|Hinta kassalla|1200|1250|1 000|

Shopify lisää paikalliset verot tuotekortissa määritetyn hinnan päälle sen perusteella, mihin tavarat toimitetaan.

## Dynaaminen verot sisältävä hinnoittelu

Koska eri mailla on erilaiset vaatimukset riippuen siitä, onko verot sisällytetty näkyvään hintaan vai ei, voit siirtyä [dynaamiseen verolliseen hinnoitteluun](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) Shopifyssa. Tämä automatisoi veronsisällyttämistoiminnon.

Valitse **Sisällytä tai jätä pois verot asiakkaan maan mukaan** **Muut markkinat - Asetukset** -osassa [**Markkinat**](https://www.shopify.com/admin/settings/markets)-asetuksissa **Shopify-järjestelmänhallinnassa**.  

> [!NOTE]
> Tämä asetus ei vaikuta hintojen näyttämiseen kotimaan markkinoilla, joita ohjaa **Kaikki hinnat sisältävät veron** -vaihtoehto.

### *Kaikki hinnat sisältävät ALV:n* on valittu

|-|Kotimaan myynti|Ulkomaa, jossa vero sisältyy hintaan|Ulkomaa, jossa vero ei sisälly hintaan|
|------------------------|--------|--------|--------|
|Hinta näkyy kaupassa|1200|1250|1 000|
|Veroprosentti|20|25|10|
|Hinta kassalla|1200|1250|1100|

Kunkin asiakkaan hinta muuttuu heidän sijaintinsa mukaan.

### *Kaikki hinnat sisältävät ALV:n* ei ole valittu

|-|Kotimaan myynti|Ulkomaa, jossa vero sisältyy hintaan|Ulkomaa, jossa vero ei sisälly hintaan|
|------------------------|--------|--------|--------|
|Hinta näkyy kaupassa|1 000|1250|1 000|
|Veroprosentti|20|25|10|
|Hinta kassalla|1200|1250|1100|

> [!NOTE]
> **Kaikki hinnat sisältävät veron** -vaihtoehto ei muuta tapaa, jolla hinnat näytetään kansainvälisille asiakkaille.

## Jos myyt EU-asiakkaille

Eri EU-mailla on erilaiset paikalliset verokannat. Jos kuitenkin olet EU:n alueella ja myyt muihin EU-maihin, voit käyttää joissakin tapauksissa paikallista verokantaa.  

Valitse [**verot ja velvollisuudet**](https://www.shopify.com/admin/settings/taxes) -kohdan **Euroopan unioni** -osiosta **kerää ALV** -ruutu **Shopify-järjestelmänhallinnassa**.

|Kerää ALV|ALV-prosentti|
|-|-|
|Mikroyritysten vapauttaminen|Kotimaan veroprosentin käyttäminen kaikessa myynnissä EU:ssa|
|Keskitetty palvelupiste tai maakohtainen rekisteröinti|Käytä asiakkaan maan ALV-prosenttia|


### ALV-joukon nouto yhden luukun rekisteröinnistä

Seuraavassa esimerkissä **Kaikki hinnat sisältävät veron** -vaihtoehto on käytössä. Tuotekortissa olevan hinnan arvo on *1200*.
        
|-|Kotimaan myynti|Ulkomaa|
|------------------------|--------|--------|
|Hinta näkyy kaupassa|1200|1250|
|Veroprosentti|20|25|
|Hinta kassalla|1200|1250|       
        
### ALV:n kerääminen mikroyritysten vapautuksesta

Seuraavassa esimerkissä **Kaikki hinnat sisältävät veron** -vaihtoehto on käytössä. Tuotekortissa olevan hinnan arvo on *1200*.
        
|-|Kotimaan myynti|Ulkomaan veroprosentti on 25 prosenttia.|
|------------------------|--------|--------|
|Hinta näkyy kaupassa|1200|1200|
|Veroprosentti|20|20|
|Hinta kassalla|1200|1200|           
    
Shopify ei ota huomioon ulkomaan veroprosenttia lopullista hintaa laskettaessa ja käyttää kotimaan veroprosenttia.

## Kansainvälisille asiakkaille myytyjen Shopify-tilausten tuominen

Jos keräät veroja useista maista, sinun on todennäköisesti määritettävä maakohtaiset asetukset kohdassa [!INCLUDE[prod_short](../includes/prod_short.md)]. Tämä on pakollista, koska kun myyntiasiakirja luodaan [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmässä, järjestelmä laskee verot Shopify-ohjelman tuomien tietojen uudelleenkäytön sijaan.

Maa-/aluekohtaiset asetukset valitaan **Shopify-asiakasmalli**-ikkunassa. Siellä voit määrittää **oletusasiakasnron** tai **Asiakasmallinron**. Varmista kummassakin tapauksessa, että valittuun asiakkaaseen tai malliin on määritetty seuraavat kentät:

1. **Yleinen liiketoiminnan kirjausryhmä** (käytetään ulkomaan asiakkaille).
2. **ALV-liiketoiminnan kirjausryhmä** (käytetään ulkomaan asiakkaille).
3. **Hinnat sisältävät ALV:n** (yhdenmukaistettu asetus Shopify-puolella):
* Valitse *Kyllä*, jos **kaikki hinnat sisältävät ALV:n** -asetus on käytössä ja jos **Sisällytä tai sulje pois vero asiakkaan maan perusteella** on poistettu käytöstä.
* Valitse *Ei*, jos **kaikki hinnat sisältävät ALV:n** -asetus on poissa käytöstä ja jos **Sisällytä tai sulje pois vero asiakkaan maan perusteella** on poistettu käytöstä.
* Valitse *Kyllä*, jos **sisällytä tai poissulje verot asiakkaan maan perusteella** on käytössä ja maa tai alue on luetteloitu kohdassa [verot sisällyttävät maat](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Valitse *Ei*, jos **sisällytä tai poissulje verot asiakkaan maan perusteella** on käytössä ja maa/alue ei ole luetteloitu kohdassa [verot sisällyttävät maat](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

[!Note]
> **Hinnat sisältävät ALV:n** -kentän asetus tulee mallista, ei tietyltä asiakkaalta. Siksi on tärkeää, että asiakasmalli on määritetty.

## Muut verohuomautukset

Kun tuotu Shopify-tilaus sisältää tietoja veroista, verot lasketaan uudelleen, kun luot myyntiasiakirjan. Tämä uudelleenlaskenta tarkoittaa, että on tärkeää, että ALV-/veroasetukset ovat [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa oikein.

- Tuotteiden useat vero- tai ALV-prosentit. Esimerkiksi jotkin tuoteluokat ovat kelvollisia alennettuihin veroprosentteihin. Voit käyttää [veron ohitus](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) -toimintoa Shopifyssa. Kun nimikkeet tuodaan ja luodaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, ne käyttävät veroasetuksia, jotka on täytetty Shopify-kaupan nimikemallin koodikohdassa. Ennen tilausten tuomista tällaisille nimikkeille sinun täytyy päivittää tuotteen ALV-kirjausryhmä.  

- Osoiteriippuvainen veroaste. Käytä **veroalueprioriteetti**-kenttää yhdessä **asiakasmallit**-taulukon kanssa, kun haluat korvata vakiologiikan, joka täyttää myyntiasiakirjan **veroaluekoodin**. **Veroalueen prioriteetti** -kentässä määritetään prioriteetti, josta toiminnon tulisi ottaa tietoja maasta tai alueesta ja osavaltiosta tai maakunnasta. Tämän jälkeen Shopify-asiakasmallien vastaava tietue tunnistetaan ja **Veroalueen koodi**-, **Verovelvollinen**- ja **Liiketoiminnan ALV-kirjausryhmä** -kenttiä käytetään, kun myyntiasiakirja luodaan.  

## Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
