---
title: Tavaroiden tai palvelujen nimikekorttien luominen| Microsoft Docs
description: Nimikekortit luodaan tunteina myytäville palveluille ja varastosta myytäville fyysisille tuotteille, kuten kokoonpanonimikkeille, valmiille tavaroille, komponenteille tai raaka-aineille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: badba79d8097db74ca843f37ded1b76ada5c3739
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377696"
---
# <a name="register-new-items"></a>Uusien nimikkeiden rekisteröiminen

Nimikkeet ovat muiden tuotteiden ohella liiketoimintasi perusta; ne ovat siis tavaroita ja palveluja, joilla käyt kauppaa. Jokainen nimike on rekisteröitävä nimikekorttina.

Nimikekortti sisältää tiedot, jotka tarvitaan nimikkeiden ostamista, tallentamista, myymistä ja toimittamista varten.

Nimikkeen kortin tyyppi voi olla **Varasto**, **Huolto** tai **Muu kuin huolto**. Se määrittää, onko nimike fyysisen varasto yksikkö, työn aikayksikkö vai fyysinen yksikkö, jota ei seurata varastossa. Lisätietoja on kohdassa [Tietoja nimiketyypeistä](inventory-about-item-types.md).

Nimike voi olla tuoterakenteessa päänimike, jonka alla on alinimikkeitä. [!INCLUDE[prod_short](includes/prod_short.md)]in tuoterakenne voi olla joko kokoonpanon tuoterakenne tai tuotannon tuoterakenne sen mukaan, miten sitä käytetään. Lisätietoja on kohdassa [Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md).

Jos ostat saman nimikkeen useammalta kuin yhdeltä toimittajalta, voit yhdistää kyseiset toimittajat nimikkeen korttiin. Toimittajat näkyvät sitten **Nimikkeen toimittajaluettelo** -sivulla, jossa voit valita kätevästi vaihtoehtoisen toimittajan.

Nimikkeet, joita tarjoat asiakkaille, mutta joita et halua ylläpitää järjestelmässäsi ennen kuin niitä myydään, voidaan määrittää luettelonimikkeiksi. Luettelonimikkeitä ei tule sekoittaa tavallisiin nimikkeisiin, joiden tyyppi on **Muu kuin varasto** Lisätietoja on kohdassa [Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Jos eri nimiketyypeillä on nimikemalleja, sivu avautuu, kun luot uuden nimikekortin, jossa voit valita sopivan mallin. Jos vain yksi nimikemalli on olemassa, uudet nimikekortit käyttävät aina kyseistä mallia.

Seuraavaksi selitetään, miten nimikekortti luodaan alusta lähtien. Voit luoda uusia nimikekortteja myös kopioimalla aiemmin luotuja kortteja. Lisätietoja on kohdassa [Uusien nimikkeiden luominen kopioimalla aiemmin luotuja nimikkeitä](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>Uuden nimikekortin luominen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
2. Valitse **Nimikkeet** -sivulla **Uusi**-toiminto.

    Jos vain yksi nimikemalli on olemassa, uusi nimikekortti avautuu. Kortissa on kenttiä, jotka on täytetty mallin tiedoilla.
3. Valitse **Valitse malli uudelle nimikkeelle** -sivulla malli, jota haluat käyttää uudessa nimikekortissa.
4. Valitse **OK**-painike. Uuden nimikekortti avautuu. Osa kortin kentistä on täytetty mallin tiedoilla.
5. Voit täyttää nimikekortin kenttiä tai muuttaa niitä tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Määritä **Arvostusmenetelmä** -kentässä tapa, jolla nimikkeen yksikkökustannukset lasketaan tekemällä oletuksia fyysisestä tavaravirrasta yrityksen läpi. Käytössä on viisi arvostusmenetelmää nimikkeen tyypin mukaan. Katso lisätietoja kohdasta [Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md).
>
> Jos valitset **Keskiarvo**, nimikkeen yksikkökustannus lasketaan kussakin vaiheessa keskimääräisenä yksikkökustannuksena oston jälkeen. Varastonarvostus olettaa, että kaikki varastot myydään samanaikaisesti. Voit valita tällä asetuksella **Keskimääräisten kustannusten laskennan yleiskuvaus** -sivun **Yksikkökustannus**-kentän, jolla voit tarkastella tapahtumahistoriaa, josta keskimääräinen kustannus lasketaan.

Voit tarkastella tai muokata erityiset hinnat tai alennukset, jotka haluat myöntää nimikkeelle, tai toimittajasi myöntää sinulle, jos tietyt ehdot, kuten asiakas, vähimmäistilausmäärä tai päättymispäivämäärä, täyttyvät. Tämä tehdään valitsemalla **Määritä erikoishinnat**- tai **Määritä erikoisalennukset** -toiminto. Jokainen rivi, esimerkiksi **Myyntihinnat**-sivulla, edustaa erikoishintaa. Jokainen sarake vastaa ehtoa, jonka täytyy olla voimassa, jotta asiakkaalle voidaan myöntää erikoishinta, joka syötetään **Myyntihinnat**-sivun **Yksikköhinta**-kenttään. Lisätietoja on kohdassa [myyntihinnan, alennuksen ja maksusopimusten kirjaaminen](sales-how-record-sales-price-discount-payment-agreements.md) tai [erityisten ostohintojen ja alennusten kirjaaminen](purchasing-how-record-purchase-price-discount-payment-agreements.md).

Nimike on nyt rekisteröity ja nimikekortti on valmis käytettäväksi osto- ja myyntiasiakirjoissa.

Jos haluat käyttää tätä nimikekorttia mallina, kun luot uusia nimikkeen kortteja, tallenna se mallina. Lisätietoja on seuraavassa osassa.  

### <a name="to-save-the-item-card-as-a-template"></a>Nimikekortin tallentaminen mallina

1. Valitse **Nimikekortti**-sivulla **Tallenna mallina** -toiminto. **Nimikemalli**-sivu avautuu ja näyttää nimikekortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-sivu avautuu ja esittää kaikki dimensiokoodit, jotka on määritetty nimikkeelle.
4. Muokkaa tai syötä dimensiokoodit, joita käytetään mallin avulla luotuihin uusiin nimikkeen kortteihin.
5. Kun olet määrittänyt uuden nimikemallin, valitse **OK**-painike.

Nimikemalli lisätään nimikemallien luetteloon niin, että sen avulla voit luoda uusia nimikekortteja.

### <a name="items-used-in-production-orders"></a>Tuotantotilauksissa käytetyt nimikkeet

Jos halutaan rekisteröidä myöhemmin tuotantotilauksessa käytettäviä nimikkeitä, täydennysjärjestelmä määritetään *tuotantotilauksena* **Täydennys**-pikavälilehdessä. Lisätietoja on kohdassa [Tietoja tuotantotilauksista](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Useiden toimittajien määrittäminen nimikkeille

Jos ostat saman nimikkeen useammalta kuin yhdeltä toimittajalta, sinun tulee syöttää tietoja kustakin nimikkeen toimittajasta, esimerkiksi hinnat, toimitusaika ja alennukset.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
2. Valitse ensin käsiteltävä nimike ja sitten **Muokkaa**-toiminto.  
3. Valitse **Toimittajat**-toiminto.  
4. Valitse **Toimittajan nro** -kenttä, ja valitse toimittaja, jonka haluat määrittää nimikkeelle.  
5. Voit täyttää myös jäljellä olevat rivit.  
6. Toista vaiheet 2–5 kullekin toimittajalle, jolta haluat ostaa nimikkeitä.

Toimittajat näkyvät nyt nimikkeen kortissa avattavassa **Nimikkeen toimittajaluettelo** -sivulla, jossa voit valita kätevästi vaihtoehtoisen toimittajan.

## <a name="categories-attributes-and-variants"></a>Luokat, määritteet ja variantit

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="deleting-item-cards"></a>Nimikekorttien poistaminen

Jos olet kirjannut nimikkeelle tapahtuman, et voi poistaa korttia, koska nimiketapahtumia voi tarvita varaston arvostamiseen tai valvontaan. Voit poistaa nimiketapahtumia tapahtumakirjauksilta ottamalla yhteyttä Microsoft-kumppaniin koodin avulla.  

## <a name="manage-inventory-in-warehouses"></a>Hallitse varastoa fyysisessä varastossa

Kun rekisteröit uuden nimikkeen, näyttöön tulee varastoinnin hallintaan liittyviä kenttiä, erityisesti **Fyysinen varasto** -pikavälilehdessä. Jos organisaatiossasi ei käytetä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman varastonhallinnan ominaisuuksia, voit ohittaa kyseiset kentät.  

Jos organisaatiosi myöhemmin määrittää varastonhallinnan, sinun täytyy useimmiten palata takaisin kuhunkin aiemmin luotuun nimikkeeseen ja varmistaa, että tiedot ovat oikein eri kentissä, jotta fyysisen varastoinnin prosessit voidaan suorittaa odotetulla tavalla. Nämä tiedot voivat sisältää esimerkiksi **Fyysisen varaston luokkakoodi**- tai **Hyllytysmallin koodi** -kenttiä. Katso lisätietoja kohdasta [Rakennetiedot: Fyysisen varastoinnin asetukset](design-details-warehouse-setup.md).  

## <a name="see-also"></a>Katso myös

[Varasto](inventory-manage-inventory.md)  
[Mittayksikön määrittäminen](inventory-how-setup-units-of-measure.md)  
[Tavaranimikkeet](finance-how-setup-report-intrastat.md#tariff-numbers)  
[Varaston kustannusten täsmäyttäminen pääkirjanpitoon](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Numerosarjojen luominen](ui-create-number-series.md)  
[Kirjausryhmien määrittäminen](finance-posting-groups.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]