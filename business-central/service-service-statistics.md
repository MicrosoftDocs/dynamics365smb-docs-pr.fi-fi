---
title: Huoltotilastot | Microsoft Docs
description: "Saat nopean yleiskuvan koko huoltoasiakirjojen, kuten tilausten, tarjousten, laskujen tai hyvityslaskujen sisällöstä, tietyn huoltorivin tiedoista ja huoltonimikkeistä."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 73d0044308d619f92e0379cc7b678301c72ce31c
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---

# <a name="viewing-service-statistics"></a>Huoltotilastojen tarkasteleminen
Financials sisältää tiettyjä tilastoja, joilla voit analysoida huoltoasiakirjoja ja selvittää, miten hyvin hallitse huoltoprosesseja. Voit analysoida huoltosopimuksia, tarjouksia, tilauksia, laskuja ja hyvityslaskuja valitsemalla **Tilastot**-toiminnon. Voit käyttää huoltonimikkeissä ja -sopimuksissa myös **huoltonimikkeen Trendscape-näkymää** tai **sopimuksen Trendscape-näkymää**. Voit tarkastella näissä näkymissä tietyn huoltonimikkeen huoltotapahtumia.   

## <a name="viewing-statistics-for-service-orders"></a>Huoltotilauksen tilastojen tarkasteleminen
Huoltotilauksen tilastoista saa yleiskatsauksen koko huoltotilauksen sisällöstä, tietyn huoltorivin erittelyn sekä laskutukseen, toimitukseen, kulutukseen ja asiakkaan saldoon liittyviä tietoja.  

Ohjelma näyttää huoltotilauksen tilastotiedot kyseessä olevan tilauksen **Huoltotilauksen tilastot** -ikkunassa. Voit avata asianmukaisen tilastoikkunan huoltotilauksen kautta. Valitse **Huoltotilaukset**-ikkunassa **Tilastot**. Tämän ikkunan pikavälilehdissä on erilaisia tietoja, kuten määrä, summa, ALV, kustannus, tuotto ja asiakkaan luottoraja. Ikkunassa mainitut summat ovat huoltotilauksen valuuttana, ellei toisin ilmoiteta.  

### <a name="view-totals-for-a-service-order"></a>Huoltotilauksen kokonaissummien tarkasteleminen  
Voit tarkastella huoltorivien kokonaissummaa joko ALV:n kanssa tai ilman sitä, ALV-osuutta sekä huoltorivien kustannuksia ja tuottoa. Ikkunassa on nimikekohtaisia tietoja, kuten paino, tilavuus ja pakettien määrä.  

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
Voit tarkastella **Huoltonimikkeen tilastot** -ikkunassa päivitettyjä tietoja huoltonimikkeestä seuraavien huoltotapahtumatyyppien mukaisesti:  

* Resurssit  
* Nimikkeet  
* Huoltokustannus  
* Huoltosopimukset  
* Yhteensä  

Jokaisen tapahtumatyypin osalta näkyvät laskutettu summa, käyttö (summa), kustannussumma, määrä, laskutettu määrä ja kulutettu määrä, tuottosumma ja tuottoprosentti. Tuottoprosentti lasketaan seuraavalla kaavalla:  

* (Laskutettu summa - Käyttö (Hinta)) x 100 / Laskutettu summa  

## <a name="using-trendscapes"></a>Trendscape-näkymien käyttäminen
Huoltonimikkeiden ja -sopimusten **Huoltonimikkeen Trendscape-näkymä**- ja **Huoltosopimuksen Trendscape-näkymä** -ikkunoissa on vieritettävä yhteenveto huoltonimikkeessä tai -sopimuksessa määritetyn ajanjakson huoltotapahtumille. Voit tarkastella Trendscape-näkymän avaamalla huoltonimikkeen tai -sopimuksen ja valitsemalla ensin **Tilastot**-toiminnon ja sitten **Trendscape**.

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

1. Valitse ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, kirjoita näytettävän sivun nimi ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä suodatusehdot, joita haluat käyttää. Valitse esimerkiksi **Sop. voitto/tappio (syyt)** -ikkunassa **Syykoodin suodatus** -kohdan arvo.  
3. Valitse **Näytä matriisi** -toiminto.

## <a name="viewing-statistics-for-posted-service-documents"></a>Kirjattujen huoltoasiakirjojen tilastojen tarkasteleminen
Huoltotilastojen avulla saat tilaston yleiskuvauksen kirjattujen huoltoasiakirjojen, kuten kirjatun toimituksen, laskun ja hyvityslaskun, sisällöstä.  

Ohjelma tulostaa tilastotiedot näyttöön vastaavan kirjatun huoltoasiakirjan Tilastot-ikkunassa. Voit avata asianmukaiset tilastoikkunat kirjattujen huoltotoimitusten, kirjatun huoltolaskun tai kirjatun huoltohyvityslaskun kautta. Valitse jokaiselle asiakirjatyypille **Koti**-välilehden **Prosessi**-ryhmän **Tilastot**-kohta. Valitse esimerkiksi **Kirjatut huoltolaskut** -ikkunan **Koti**-välilehden **Prosessi**-ryhmän **Tilastot**-vaihtoehto.  

### <a name="posted-service-shipment-statistics"></a>Kirjatun huoltotoimituksen tilastot  
**Huoltotoimituksen tilastot** -ikkunassa on kirjatun huoltotoimituksen yleiskuvaus. Tietoja on esimerkiksi toimituksen fyysisestä sisällöstä, kuten toimitettujen nimikkeiden, resurssituntien tai kustannusten määrästä sekä toimitettujen nimikkeiden painosta ja tilavuudesta.  

### <a name="posted-service-invoice-statistics"></a>Kirjatun huoltolaskun tilastot  
Ohjelma näyttää kirjatun huoltolaskun tilaston yleiskuvauksen **Huoltolaskun tilastot** -ikkunassa. Voit tarkastella kirjatun huoltolaskun kokonaissummia. Tiedot sisältävät laskutetuiksi kirjattujen huoltorivien kokonaissumman (ALV:n kanssa ja ilman ALV:a), ALV:n osan sekä kirjatun laskun kustannuksen ja tuoton. Ikkunassa on myös seuraavat tiedot:  

* Huoltolaskuriveillä olevat nimikkeet, kuten paino, tilavuus ja pakettien määrä.  
* Asiakkaan tilin saldo ja suurin mahdollinen luotto, joka voidaan myöntää asiakkaalle.  

### <a name="posted-service-credit-memo-statistics"></a>Kirjattujen huollon hyvityslaskujen tilastot  
Voit hakea kirjatun huollon hyvityslaskun rivien tilaston yleiskuvausta **Huollon hyvityslaskun tilastot** -ikkunan avulla. Yhteenvetoon voi sisältyä esimerkiksi

* kirjatun hyvityslaskun kokonaissummat, jotka näkyvät määränä, summana, ALV:nä, kustannuksena ja tuottona tietoja kirjatun hyvityslaskun huoltorivien nimikkeistä, kuten pakettien paino, tilavuus ja määrä  
* yleisiä tietoja asiakkaasta, kuten asiakkaan luottoraja ja tilin saldo.  

## <a name="see-also"></a>Katso myös  
[Huoltotilausten luominen](service-how-to-create-service-orders.md)   
[Huoltonimikkeiden luominen](service-how-to-create-service-items.md)   
[Huollon suunnittelu](service-plan-service.md)  

