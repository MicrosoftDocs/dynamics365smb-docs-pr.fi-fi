---
title: Huoltotilastot | Microsoft Docs
description: Saat nopean yleiskuvan koko huoltoasiakirjojen, kuten tilausten, tarjousten, laskujen tai hyvityslaskujen sisällöstä, tietyn huoltorivin tiedoista ja huoltonimikkeistä.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 95bed832d95647ea538324544c302054328cae66
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877157"
---
# <a name="viewing-service-statistics"></a>Huoltotilastojen tarkasteleminen
Voit käyttää tilastoja huoltoasiakirjojen analysoimisessa ja selvittää, miten hyvin hallitse huoltoprosesseja. Voit analysoida huoltosopimuksia, tarjouksia, tilauksia, laskuja ja hyvityslaskuja valitsemalla **Tilastot**-toiminnon. Voit käyttää huoltonimikkeissä ja -sopimuksissa myös **huoltonimikkeen Trendscape-näkymää** tai **sopimuksen Trendscape-näkymää**. Voit tarkastella näissä näkymissä tietyn huoltonimikkeen huoltotapahtumia.   

## <a name="viewing-statistics-for-service-orders"></a>Huoltotilauksen tilastojen tarkasteleminen
Huoltotilauksen tilastoista saa yleiskatsauksen koko huoltotilauksen sisällöstä, tietyn huoltorivin erittelyn sekä laskutukseen, toimitukseen, kulutukseen ja asiakkaan saldoon liittyviä tietoja.  

Ohjelma näyttää huoltotilauksen tilastotiedot kyseessä olevan tilauksen **Huoltotilauksen tilastot** -sivulla. Voit avata asianmukaisen tilastosivun huoltotilauksen kautta. Valitse **Huoltotilaukset**-sivulla **Tilastot**. Tämän sivun pikavälilehdissä on erilaisia tietoja, kuten määrä, summa, ALV, kustannus, tuotto ja asiakkaan luottoraja. Sivulla mainitut summat ovat huoltotilauksen valuuttana, ellei toisin ilmoiteta.  

### <a name="view-totals-for-a-service-order"></a>Huoltotilauksen kokonaissummien tarkasteleminen  
Voit tarkastella huoltorivien kokonaissummaa joko ALV:n kanssa tai ilman sitä, ALV-osuutta sekä huoltorivien kustannuksia ja tuottoa. Sivulla on nimikekohtaisia tietoja, kuten paino, tilavuus ja pakettien määrä.  

### <a name="view-shipping-information"></a>Toimitustietojen tarkasteleminen  
Voit tarkastella tietoja toimitettavista nimikkeistä, resursseista tai kustannuksista. Ohjelma kokoaa tiedot kunkin tilauksen huoltorivin **Toimitettava määrä** -kentän arvojen perusteella.  

### <a name="view-order-details"></a>Tilaustietojen tarkasteleminen  
Voit tarkastella tietoja nimikkeistä, resurssitunneista sekä laskutettavista ja kulutettavista kustannuksista. Näitä tietoja käsitellään seuraavassa taulukossa.  

|Sarake | Kuvaus|  
|------------|---------------------------------------|  
|**Laskutus**|Tämä sarake sisältää summat, jotka kirjataan huoltotilaukseen Laskutettu-tilassa.|  
|**Kulutus**|Näyttää nimikkeiden määrän ja kustannuksen, tai kulutetuksi kirjattavat resurssit.|  
|**Yhteensä**|Tässä sarakkeessa ohjelma näyttää huoltotilauksen ne kokonaissummat, jotka saadaan lisättäessä laskutussummat kulutussummiin.|  

### <a name="analyze-service-order-lines"></a>Huoltotilausrivien analysointi  
Voit analysoida tiedot huoltotilaukseen sisältyvien huoltorivityypin mukaan. Näin ollen seuraavien kohtien summat esitetään erikseen:  

* Nimikkeet  
* Resurssit  
* Kustannukset ja pääkirjanpitotilit  

### <a name="view-customer-information"></a>Asiakastietojen tarkasteleminen  
Voit tarkastella asiakkaan tilin saldoa sekä sen asiakkaan saamaa suurinta mahdollista luottoa, jolle huoltoasiakirja luotiin.

## <a name="viewing-service-item-statistics"></a>Huoltonimikkeen tilastojen tarkasteleminen
Voit tarkastella **Huoltonimikkeen tilastot** -sivulla päivitettyjä tietoja huoltonimikkeestä seuraavien huoltotapahtumatyyppien mukaisesti:  

* Resurssit  
* Nimikkeet  
* Huoltokustannus  
* Huoltosopimukset  
* Yhteensä  

Jokaisen tapahtumatyypin osalta näkyvät laskutettu summa, käyttö (summa), kustannussumma, määrä, laskutettu määrä ja kulutettu määrä, tuottosumma ja tuottoprosentti. Tuottoprosentti lasketaan seuraavalla kaavalla:  

* (Laskutettu summa - Käyttö (Hinta)) x 100 / Laskutettu summa  

## <a name="using-trendscapes"></a>Trendscape-näkymien käyttäminen
Huoltonimikkeiden ja -sopimusten **Huoltonimikkeen Trendscape-näkymä**- ja **Huoltosopimuksen Trendscape-näkymä** -sivuilla on vieritettävä yhteenveto huoltonimikkeessä tai -sopimuksessa määritetyn ajanjakson huoltotapahtumille. Voit tarkastella Trendscape-näkymän avaamalla huoltonimikkeen tai -sopimuksen ja valitsemalla ensin **Tilastot**-toiminnon ja sitten **Trendscape**.

Kun vierität luetteloa, summat lasketaan paikallisena valuuttana määritetyn aikavälin mukaisesti. Ohjelma laskee kaikki summat huoltotapahtumista (tapahtumista, jotka ohjelma luo silloin, kun kirjaat huoltotilauksia tai huoltolaskuja).

Voit suodattaa luetteloa määrittämällä sisällytettävät huoltonimikkeet.  

> [!Tip]  
>  Jos olet asettanut aikaväliksi  **Päivä** ja sinun täytyy vierittää pitkä ajanjakso eteenpäin, kannattaa vaihtaa aikaväli isommaksi, esimerkiksi  **Vuosineljännekseksi**. Kun olet löytänyt haluamasi ajanjakson, voit vaihtaa takaisin alkuperäiseen aikaväliin, jotta voisit katsoa tietoja yksityiskohtaisemmin.   

## <a name="viewing-gains-and-losses-on-contracts"></a>Sopimusten voittojen ja tappioiden tarkasteleminen  
Sopimuksen voitto- tai tappiotapahtumia luodaan, kun sopimustarjous muunnetaan huoltosopimukseksi, sopimusrivejä lisätään huoltosopimuksiin tai poistetaan niistä tai sopimus peruutetaan. Voit tarkastella sopimuksen voittoja tai tappioita seuraavilla sivuilla.  

|Sivu | Kuvaus|  
|----------------|---------------------------------------|  
|**Sop.voitto/tappio (sopimukset)**|Sopimusten voiton/tappion tarkastelu huoltosopimuksittain |  
|**Sop. voitto/tappio (ryhmät)**|Sopimusten voiton/tappion tarkastelu sopimusryhmittäin|  
|**Sop.voitto-/tappio (asiakkaat)**|Voittojen/tappioiden tarkastelu asiakkaittain|  
|**Sop. voitto/tappio (syyt)**|Sopimusten voiton/tappion tarkastelu syykoodeittain|  
|**Sop. voitto/tappio (vast.paik)**|Sopimusten voiton/tappion tarkastelu vastuupaikoittain|  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä näytettävän sivun nimi ja valitse sitten liittyvä linkki.  
2. Täytä suodatusehdot, joita haluat käyttää. Valitse esimerkiksi **Sop. voitto/tappio (syyt)** -sivulla **Syykoodin suodatus** -kohdan arvo.  
3. Valitse **Näytä matriisi** -toiminto.

## <a name="viewing-statistics-for-posted-service-documents"></a>Kirjattujen huoltoasiakirjojen tilastojen tarkasteleminen
Huoltotilastojen avulla saat tilaston yleiskuvauksen kirjattujen huoltoasiakirjojen, kuten kirjatun toimituksen, laskun ja hyvityslaskun, sisällöstä.  

Ohjelma tulostaa tilastotiedot näyttöön vastaavan kirjatun huoltoasiakirjan tilastosivulla. Voit avata asianmukaiset tilastosivut kirjattujen huoltotoimitusten, kirjatun huoltolaskun tai kirjatun huoltohyvityslaskun kautta. Valitse kullekin näistä asiakirjatyypeistä **Tilasto**-toiminto. Valitse esimerkiksi **Kirjatut huoltolaskut** -sivulta **Tilasto**-toiminto.  

### <a name="posted-service-shipment-statistics"></a>Kirjatun huoltotoimituksen tilastot  
**Huoltotoimituksen tilastot** -sivulla on kirjatun huoltotoimituksen yleiskuvaus. Tietoja on esimerkiksi toimituksen fyysisestä sisällöstä, kuten toimitettujen nimikkeiden, resurssituntien tai kustannusten määrästä sekä toimitettujen nimikkeiden painosta ja tilavuudesta.  

### <a name="posted-service-invoice-statistics"></a>Kirjatun huoltolaskun tilastot  
Ohjelma näyttää kirjatun huoltolaskun tilaston yleiskuvauksen **Huoltolaskun tilastot** -sivulla. Voit tarkastella kirjatun huoltolaskun kokonaissummia. Tiedot sisältävät laskutetuiksi kirjattujen huoltorivien kokonaissumman (ALV:n kanssa ja ilman ALV:a), ALV:n osan sekä kirjatun laskun kustannuksen ja tuoton. Sivulla on myös seuraavat tiedot:  

* Huoltolaskuriveillä olevat nimikkeet, kuten paino, tilavuus ja pakettien määrä.  
* Asiakkaan tilin saldo ja suurin mahdollinen luotto, joka voidaan myöntää asiakkaalle.  

### <a name="posted-service-credit-memo-statistics"></a>Kirjattujen huollon hyvityslaskujen tilastot  
Voit hakea kirjatun huollon hyvityslaskun rivien tilaston yleiskuvausta **Huollon hyvityslaskun tilastot** -sivun avulla. Yhteenvetoon voi sisältyä esimerkiksi

* kirjatun hyvityslaskun kokonaissummat, jotka näkyvät määränä, summana, ALV:nä, kustannuksena ja tuottona tietoja kirjatun hyvityslaskun huoltorivien nimikkeistä, kuten pakettien paino, tilavuus ja määrä  
* yleisiä tietoja asiakkaasta, kuten asiakkaan luottoraja ja tilin saldo.  

## <a name="see-also"></a>Katso myös  
[Huoltotilausten luominen](service-how-to-create-service-orders.md)   
[Huoltonimikkeiden luominen](service-how-to-create-service-items.md)   
[Huollon suunnittelu](service-plan-service.md)  
