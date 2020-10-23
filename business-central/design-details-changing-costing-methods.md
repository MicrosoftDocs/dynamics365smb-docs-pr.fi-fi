---
title: Rakennetiedot – nimikkeiden arvostusmenetelmien muuttaminen
description: Tietoja erilaisten arvostusmenetelmien määrittämisestä nimikkeelle, jota on jo käytetty tapahtumissa.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing methods, costing, item cost
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 344aa53f965f832d8e7fb2abd3431a1853105c8c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917524"
---
# <a name="design-details-change-the-costing-method-for-items"></a>Rakennetiedot: nimikkeiden arvostusmenetelmän muuttaminen

Nimikkeen arvostusmenetelmää ei voi muuttaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa sen jälkeen, kun se on sisällytetty tapahtumaan. Niinpä sitä ei voi tehdä esimerkiksi nimikkeen ostamisen tai myymisen jälkeen. Jos nimikkeille on määritetty väärä arvostusmenetelmä, ongelmaa ei ehkä huomata ennen talousraportointia.

Tässä aiheessa käsitellään tämän tilanteen ratkaisemista. Suosituksena on korvata nimike, jossa on virheellinen arvostusmenetelmä, uudella nimikkeellä ja siirtää varasto vanhasta nimikkeestä uuteen käyttämällä kokoonpanotilausta.

> [!NOTE]
> Kokoonpanotilauksia käytettäessä kustannukset siirtyvät edelleen, vaikka kirjattavaksi jääkin avoimia ostolaskuja tai kuljetusmaksuja. Lisäksi tällä tavoin voidaan kumota muunto ja saada alkuperäisten nimikkeiden määrät tarvittaessa takaisin.

> [!TIP]
> Prosessiin kannattaa perehtyä käyttämällä muuntoprosessissa luksi yhtä nimikettä tai pientä nimikejoukkoa.

## <a name="about-costing-methods"></a>Tietoja arvostusmenetelmistä

Arvostusmenetelmät ohjaavat tavaroiden ostamiseen, varastoon vastaanottamiseen ja myyntiin liittyvää kustannuslaskentaa. Arvostusmenetelmät vaikuttavat sellaisten myytyjen tuotteiden kustannuksiin kirjattujen summien ajoitukseen, jotka vaikuttavat bruttovoittoon. Ja juuri tämä virta laskee myytyjen tuotteiden kustannukset. Bruttotuotto määritetään myytyjen tuotteiden kustannusten (MTKUST) ja tuoton perusteella seuraavasti:

*bruttotuotto* = *tuotto - MTKUST*

Kun varastonimikkeitä määritetään, niille on määritettävä arvostusmenetelmä. Menetelmä voi vaihdella yritysten ja nimikkeiden mukaan, joten oikean menetelmän valitseminen on tärkeää. [!INCLUDE[d365fin](includes/d365fin_md.md)] tukee seuraavia arvostusmenetelmiä:

* Keskiarvo
* FIFO
* LIFO
* Vakio
* Määrätty

Katso lisätietoja kohdasta [Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md).

## <a name="using-assembly-orders-to-change-costing-method-assignments"></a>Arvostusmenetelmämääritysten muuttaminen kokoonpanotilauksia käyttämällä

Tässä osassa käsitellään seuraavia nimikkeelle määritetyn arvostusmenetelmän muutoksen vaiheet:

1. Arvostuksen oletusmenetelmän määrittäminen.
2. Niiden nimikkeiden määrittäminen, joiden kustannusmenetelmä muutetaan ja nimikkeiden uudelleenumerointi.
3. Uusien nimikkeiden luonti vanhalla numerointimallilla ja päätietojen kopiointi eränä.
4. Liittyvien päätietojen manuaalinen kopiointi aiemmin luodusta nimikkeestä uuteen nimikkeeseen.
5. Alkuperäisestä nimikkeestä uuteen nimikkeeseen muunnettavan varastomäärän määrittäminen.
6. Varaston siirtäminen uuteen nimikkeeseen.
7. Kysyntään kohdistettujen varastomäärien käsitteleminen.
8. Alkuperäisen nimikkeen käytön estäminen.  

### <a name="define-a-default-costing-method"></a>Arvostuksen oletusmenetelmän määrittäminen

Virheet voidaan estää jatkossa määrittämällä uusille nimikkeille oletusarvoisen arvostusmenetelmän. Aina kun joku luo uuden nimikkeen, [!INCLUDE[d365fin](includes/d365fin_md.md)] ehdottaa arvostuksen oletusmenetelmää. Oletusmenetelmä määritetään **Varastonhallinnan asetukset** -sivun **Arvostuksen oletusmenetelmä** -kentässä. 

### <a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a>Niiden nimikkeiden määrittäminen, joiden kustannusmenetelmä muutetaan ja nimikkeiden uudelleenumerointi

Uusille nimikkeille halutaan ehkä antaa sama numero kuin oli nimikkeillä, jotka ne korvaavat. Sitä varten on muutettava aiemmin luotujen nimikkeiden numerot. Jos aiemman luodun nimikkeen numero on esimerkiksi P1000, sen voi korvat numerolla X-P1000. Tämä manuaalinen muutos on tehtävä jokaiselle nimikkeelle.

### <a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a>Uusien nimikkeiden luonti vanhalla numerointimallilla ja päätietojen kopiointi eränä

Nykyistä numeromallia käyttävien uusien nimikkeiden luonti on mahdollista. **Arvostusmenetelmä**-kenttää lukuun ottamatta uusissa nimikkeissä pitäisi olla samat päätiedot kuin nykyisissä nimikkeissä. Nimikkeen päätiedot ja muiden ominaisuuksien liittyvät tiedot siirretään valitsemalla **Kopioi nimike** -toiminto **Nimikkeen kortti** -sivulla. Lisätietoja on kohdassa [Uusien nimikkeiden luominen kopioimalla aiemmin luotuja nimikkeitä](inventory-how-copy-items.md).

Uusien nimikkeiden luonnin ja päätietojen siirron jälkeen määritetään oikea arvostusmenetelmä.

### <a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a>Liittyvien päätietojen manuaalinen kopiointi alkuperäisestä nimikkeestä uuteen nimikkeeseen

Uusien nimikkeiden täysi käytettävyys edellyttää, että joitakin päätietoja kopioidaan manuaalisesti muilta alueilta seuraavassa taulukossa kuvatulla tavalla.

|Alue  |Kopioitava sisältö  |Kopiointiohjeet  |
|---------|---------|---------|
|Varasto     |Varastointiyksiköt (SKU:t)         |Tarkista, onko alkuperäiselle nimikkeelle määritetty varastointiyksikkö. Jos jokaiseen SKU-korttiin on lisätty suunnitteluparametrit, SKU on luotava manuaalisesti uudelle nimikkeelle. Jos parametreja ei ole määritetty, tiedot voidaan luoda käyttämällä **Nimikkeen kortti** -sivun **Luo varastointiyksikkö** -erätyötä.        |
|     |Nimikekorvaukset         |Tarkista, onko alkuperäiselle nimikkeelle määritetty nimikekorvauksia. Jos niitä on, siirrä tiedot uuteen nimikkeeseen. Korvaavia nimikkeitä voi tarkastella **Nimikkeen kortti** -sivun **Korvaukset**-toiminnolla.         |
|     |Analyysiraportit         |Tarkista nimikkeen, myynnin ja oston analyysiraportit. Jos raportti viittaa alkuperäisiin nimikkeisiin, sen osalta voidaan joko luoda uusi analyysiraportti, jossa on viittaus uuteen nimikkeeseen (ja alkuperäinen analyysiraportti säilytetään historiatietona) tai raportti oikaistaan viittaamaan uuteen nimikkeeseen.         |
|     |Vakiopäiväkirjat         |Tarkista, viittaavatko vakiopäiväkirjat alkuperäiseen nimikkeeseen ja siirrä kyseiset tiedot tarvittaessa uuteen nimikkeeseen. Nämä tiedot ovat vakiopäiväkirjoissa, jotka ovat saatavana nimikepäiväkirjassa.          |
|Myynti     |Myynnin ennakkomaksuprosentti         | Tarkista, onko alkuperäiselle nimikkeelle määritetty myynnin ennakkomaksuprosentteja, ja siirrä kyseiset tiedot uuteen nimikkeeseen. Ennakkomaksuprosentteja voi tarkastella valitsemalla **Nimikkeen kortti** -sivulla ensin **Myynti** ja sitten **Ennakkomaksuprosentit**.        |
|Osto     |Oston ennakkomaksuprosentti         |Tarkista, onko alkuperäiselle nimikkeelle määritetty oston ennakkomaksuprosentteja, ja siirrä kyseiset tiedot uuteen nimikkeeseen. Ennakkomaksuprosentteja voi tarkastella valitsemalla **Nimikkeen kortti** -sivulla ensin **Ostot** ja sitten **Ennakkomaksuprosentit**.                 |
|F. varastointi     |Varastopaikan sisältö         |Tarkista alkuperäiselle nimikkeelle määritetty varastopaikan sisältö. Jos sarakkeet, kuten Vähimmäismäärä, Enimmäismäärä, Oletus ja Erityinen on annettu erikseen, uuden nimikkeen varastopaikan sisältö on luotava manuaalisesti. Jos niitä ei ole, mitään toimenpiteitä ei tarvita. [!INCLUDE[d365fin](includes/d365fin_md.md)] säilyttää tietueet, fyysisen varastoinnin asiakirjoja ja päiväkirjoja rekisteröidään.|
|Projekti     |Projektihinnat         |Tarkista, onko alkuperäiselle nimikkeelle määritetty projektihintoja, ja siirrä kyseiset tiedot uuteen nimikkeeseen. Nämä tiedot ovat saatavana **Projektikortti**-sivulla **tietoruudun** **Projektin tiedot - Hintojen määrä** -kohdassa.         |
|Palvelu     |Palveluresurssin taito         |Tarkista, onko alkuperäiselle nimikkeelle määritetty palveluresurssin taitoja, ja siirrä kyseiset tiedot uuteen nimikkeeseen. Resurssin taitoja voi tarkastella **Nimikkeen kortti** -sivun **Resurssin taidot** -toiminnolla.          |
|     |Huoltonimikkeen komponentit         |Tarkista, onko alkuperäiselle huoltonimikkeelle määritetty komponentteja, ja siirrä kyseiset tiedot uuteen nimikkeeseen. Huoltonimikekomponentteja voi tarkastella avaamalla **Nimikkeen kortti** -sivulla **Huoltonimike**-toiminnolla luettelon liittyvistä huoltonimikkeistä ja valitsemalla sitten **Komponentit**-toiminnon.          |
|Tuotanto     |Tuotantotuoterakent.         |Tarkista, sisältääkö jokin tuotannon tuoterakenne alkuperäisen nimikkeen, ja korvaa se uudella nimikkeellä. Alkuperäinen nimike korvataan valitsemalla **Tuotannon tuoterakenteet** -sivulla **Vaihda tuotannon tuoterakenteen nimike** -toiminto.         |
|Kokoonpano     |Kokoonpanon tuoterakenteet         |Tarkista, sisältääkö jokin kokoonpanon tuoterakenne alkuperäisen nimikkeen, ja korvaa se manuaalisesti uudella nimikkeellä.         |

> [!IMPORTANT]
> Jos uutena arvostusmenetelmänä on Vakio, arvo annetaan **Nimikkeen kortti** -sivun **Vakiokustannus**-kentässä. Kustannusjakauma voidaan sitten määrittää **Vakiokustannustyökirja**-sivulla. Lisätietoja on kohdassa [Vakiokustannusten päivittäminen](finance-how-to-update-standard-costs.md).

### <a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a>Alkuperäisestä nimikkeestä uuteen nimikkeeseen muunnettavan varastomäärän määrittäminen

> [!NOTE]
> Tässä vaiheessa ei oteta huomioon määriä, jotka sisältyvät toimittamattomiin tilauksiin. Lisätietoja on kohdassa [Kysyntään kohdistettujen varastomäärien käsitteleminen](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand). 

Varaston määrien luettelo luodaan käyttämällä inventointipäiväkirjaa. Fyysisen varaston sijaintiasetusten käytetään seuraavista jompaakumpaa:

* Inventointipäiväkirjat
* F.var. inventointipvk:t

Kumpikin päiväkirja voi laskea nimikkeen varastomäärän, mukaan lukien sijainnin, variantin, varastopaikan ja varastosijainnin. Lisätietoja on kohdassa [Varaston laskeminen, muuttaminen ja uudelleenluokitus päiväkirjojen avulla](inventory-how-count-adjust-reclassify.md).

### <a name="transfer-the-inventory-to-the-new-item"></a>Varaston siirtäminen uuteen nimikkeeseen

Kustannus ja varastomäärä voidaan siirtää alkuperäisestä nimikkeestä uuteen nimikkeeseen luomalla ja kirjaamalla kokoonpanotilauksia. Kokoonpanotilaukset voivat muuntaa nimikkeen toiseksi nimikkeeksi kustannukset säilyttäen. Näin voidaan varmistaa, että varastotilin ja myytyjen tuotteiden kustannusten nettosummat eivät muutu (paitsi silloin kun uusi arvostusmenetelmä on Vakio, jolloin tapauksen kustannukset voidaan jakaa vaihtelutileille). Lisätietoja on kohdassa [Kokoonpanon hallinta](assembly-assemble-items.md).

Kokoonpanotilauksia luotaessa käytetään Kun luot kokoonpano tilauksia, käytetään inventointipäiväkirjan tai f.var. inventointipvk:n tietoja. Seuraavassa taulukossa käsitellään raporttien kokoonpanotilauksen otsikkoon ja riveille annettavia tietoja.

#### <a name="header"></a>Otsikko

|Kenttä  |Annettava arvo  |
|---------|---------|
|Nimikkeen nro     |Uuden nimikkeen numero.         |
|määrä     |Inventointipäiväkirjan määrä.<br> **HUOMAUTUS:** inventointipäiväkirjojen laskevat määrät eivät sisällä toimittamattomien tilausten määriä.          |
|Varianttikoodi     |Sama kuin inventointipäiväkirjassa.          |
|Sijaintikoodi      |Sama kuin inventointipäiväkirjassa.         |
|Mittayksikön koodi     |Sama kuin inventointipäiväkirjassa.         |
|Varastopaikan koodi     |Sama kuin inventointipäiväkirjassa.         |

#### <a name="lines"></a>Rivit

|Kenttä  |Annettava arvo  |
|---------|---------|
|Tyyppi     |Nimike         |
|Ei.     |Alkuperäisen nimikkeen numero.         |
|Määrä per     |1         |
|Varianttikoodi     |Sama kuin inventointipäiväkirjassa.         |
|Sijaintikoodi      |Sama kuin inventointipäiväkirjassa.         |
|Mittayksikön koodi     |Sama kuin inventointipäiväkirjassa.         |

> [!NOTE]
> Kokoonpanotilaus voi käsitellä kerrallaan vain yhden nimikkeen SKU:n. Kokoonpanotilaus on luotava jokaiselle SKU-yhdistelmälle, jolla on varastossa määrä.

> [!NOTE]
> Fyysisen varaston sijaintia varten on ehkä luotava poimintoja, ennen kuin kokoonpanotilaus voidaan kirjata. Siihen voi perehtyä tutustumalla poiminnan määritykseen **Sijaintikortti**-sivulla. Lisätietoja on kohdassa [Nimikkeiden ja sijaintien määrittäminen ohjattua hyllytystä ja poimintaa varten](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md).

### <a name="handle-inventory-quantities-that-are-allocated-to-demand"></a>Kysyntään kohdistettujen varastomäärien käsitteleminen

Alkuperäisen nimikkeen varastomääräksi tulisi parhaassa tapauksessa nolla sen jälkeen, kun varastomäärät on siirretty. Järjestelmässä voi kuitenkin olla avoimia tilauksia, työkirjoja ja päiväkirjoja (katso seuraava taulukko), joissa tarvitaan alkuperäistä nimikettä. Myös varauksilla ja nimikeseurannalla voi olla tietty määrä varattuna.

**Esimerkki** Varastomäärä on 1 000 kpl ja 20 kpl varattu toimittamattomaan myyntitilaukseen. Tässä tapauksessa voidaan päättää säilyttää 20 kpl vanhaa nimikettä, jotta avoin tilaus voidaan täyttää.

> [!NOTE]
> Seuraavassa taulukossa on toiminnallisia alueita, jotka voivat vaikuttaa määrään, joten oikean määrän löytäminen voi olla hankalaa. Varmuuden vuoksi edellisessä esimerkissä säilytettävä määrä voikin olla 100 kpl ja jäljellä olevat 900 kpl siirretään sen sijaan. Sama lopputulos saavutetaan myös käsittelemällä asiakirjat ja päiväkirjat siten, että hallittavissa oleva määrä jää jäljelle. Vaihtoehtoisesti koko määrä voidaan siirtää uuteen tilaukseen, jonka jälkeen osa siitä siirretään takaisin alkuperäiseen nimikkeen käyttämällä kokoonpanotilausta.

Seuraavassa taulukossa käsitellään toiminnallisia alueita, joilla voi olla avoimia määriä.

|Alue  |Avoimien määrien etsiminen  |
|---------|---------|
|Myynti     |Myyntiasiakirjat, kuten tilaukset, palautustilaukset, laskut, tarjoukset, puitetilaukset ja hyvityslaskut         |
|Varasto     |Nimikepäiväkirjat, varaukset, nimikeseuranta ja vakiokustannustyökirja         |
|Osto     |Ostoasiakirjat, kuten tilaukset, palautustilaukset, laskut, tarjoukset, puitetilaukset ja hyvityslaskut         |
|Suunnittelu     |Hankintatyökirja, suunnittelutyökirja ja tilauksen suunnittelu         |
|F. varastointi     |Siirtotilaukset, varastotoimitukset, fyysisen varastoinnin päiväkirjat ja varastopoiminnat, hyllytykset ja siirrot, sisäiset poiminnat ja hyllytykset sekä varastopaikan luontityökirjat         |
|Kokoonpano     |Kokoonpanoasiakirjat, kuten tilaukset, palautustilaukset ja puitetilaukset         |
|Projektit     |Projektin suunnittelurivit ja projektipäiväkirjan rivit         |
|Palvelu     |Huoltoasiakirjat ja huoltosopimukset         |
|Tuotanto     |Tuotantotilaukset (suunniteltu, sitovasti suunniteltu ja julkaistu)         |

### <a name="block-the-original-item-from-further-use"></a>Alkuperäisen nimikkeen käytön estäminen

Kun alkuperäisen nimikkeen varasto on nolla, nimikkeen käyttö uusissa tapauksissa voidaan estää. Nimike estetään ottamalla **Nimikkeen kortti** -sivulla **Estetty**-valitsin käyttöön. Lisätietoja on kohdassa [Nimikkeiden myynnin tai oston estäminen](inventory-how-block-items.md).

## <a name="summary"></a>Yhteenveto

Tapahtumissa käytettyjen nimikkeiden arvostusmenetelmän muuttaminen on prosessi, eikä se ole [!INCLUDE[d365fin](includes/d365fin_md.md)]in vakiotoiminto. Prosessin mallina voi käyttää tässä aiheessa kuvattuja vaiheita.

Prosessi voi viedä paljon aikaa, koska siihen sisältyy useita manuaalisia vaiheita. Siihen käytettävä aika kuitenkin minimoi virheiden vaikutuksen kirjanpitoon.

Suositukset:

1. Prosessin toteutettavuuden arviointi suorittamalla koko prosessin toimet yhdessä tai muutamassa mallinimikkeessä.
2. Kokeneen kumppanin hankkiminen auttamaan prosessin aikana.

## <a name="see-also"></a>Katso myös

[Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md)  
[Yleiskuvaus](design-details-inventory-costing.md)
