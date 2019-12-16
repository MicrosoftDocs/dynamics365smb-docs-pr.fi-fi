---
title: Tavaroiden tai palvelujen nimikekorttien luominen| Microsoft Docs
description: Nimikekortit luodaan tunteina myytäville palveluille ja varastosta myytäville fyysisille tuotteille, kuten kokoonpanonimikkeille, valmiille tavaroille, komponenteille tai raaka-aineille.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 11/27/2019
ms.author: sgroespe
ms.openlocfilehash: 3cb9ffd6dadaeba7aab782c0bd8f45d3f4aa5387
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878339"
---
# <a name="register-new-items"></a>Uusien nimikkeiden rekisteröiminen
Nimikkeet ovat muiden tuotteiden ohella liiketoimintasi perusta; ne ovat siis tavaroita ja palveluja, joilla käyt kauppaa. Jokainen nimike on rekisteröitävä nimikekorttina.

Nimikekortti sisältää tiedot, jotka tarvitaan nimikkeiden ostamista, tallentamista, myymistä ja toimittamista varten.

Nimikkeen kortin tyyppi voi olla **Varasto**, **Huolto** tai **Muu kuin huolto**. Se määrittää, onko nimike fyysisen varasto yksikkö, työn aikayksikkö vai fyysinen yksikkö, jota ei seurata varastossa. Lisätietoja on kohdassa [Tietoja nimiketyypeistä](inventory-about-item-types.md).

Nimike voi olla tuoterakenteessa päänimike, jonka alla on alinimikkeitä. [!INCLUDE[d365fin](includes/d365fin_md.md)]in tuoterakenne voi olla joko kokoonpanon tuoterakenne tai tuotannon tuoterakenne sen mukaan, miten sitä käytetään. Lisätietoja on kohdassa [Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md).

Jos ostat saman nimikkeen useammalta kuin yhdeltä toimittajalta, voit yhdistää kyseiset toimittajat nimikkeen korttiin. Toimittajat näkyvät sitten **Nimikkeen toimittajaluettelo** -sivulla, jossa voit valita kätevästi vaihtoehtoisen toimittajan.

Nimikkeet, joita tarjoat asiakkaille, mutta joita et halua ylläpitää järjestelmässäsi ennen kuin niitä myydään, voidaan määrittää luettelonimikkeiksi. Luettelonimikkeitä ei tule sekoittaa tavallisiin nimikkeisiin, joiden tyyppi on **Muu kuin varasto** Lisätietoja on kohdassa [Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Jos eri nimiketyypeillä on nimikemalleja, sivu avautuu, kun luot uuden nimikekortin, jossa voit valita sopivan mallin. Jos vain yksi nimikemalli on olemassa, uudet nimikekortit käyttävät aina kyseistä mallia.

Seuraavaksi selitetään, miten nimikekortti luodaan alusta lähtien. Voit luoda uusia nimikekortteja myös kopioimalla aiemmin luotuja kortteja. Lisätietoja on kohdassa [Uusien nimikkeiden luominen kopioimalla aiemmin luotuja nimikkeitä](inventory-how-copy-items.md).<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx]

## <a name="to-create-a-new-item-card"></a>Uuden nimikekortin luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
2. Valitse **Nimikkeet** -sivulla **Uusi**-toiminto.

    Jos vain yksi nimikemalli on olemassa, uusi nimikekortti avautuu. Kortissa on kenttiä, jotka on täytetty mallin tiedoilla.
3. Valitse **Valitse malli uudelle nimikkeelle** -sivulla malli, jota haluat käyttää uudessa nimikekortissa.
4. Valitse **OK**-painike. Uuden nimikekortti avautuu. Osa kortin kentistä on täytetty mallin tiedoilla.
5. Voit täyttää nimikekortin kenttiä tai muuttaa niitä tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Määritä **Arvostusmenetelmä** -kentässä tapa, jolla nimikkeen yksikkökustannukset lasketaan tekemällä oletuksia fyysisestä tavaravirrasta yrityksen läpi. Käytössä on viisi arvostusmenetelmää nimikkeen tyypin mukaan. Lisätietoja on kohdassa [Rakennetiedot: Arvostusmenetelmät](design-details-costing-methods.md).
>
> Jos valitset **Keskiarvo**, nimikkeen yksikkökustannus lasketaan kussakin vaiheessa keskimääräisenä yksikkökustannuksena oston jälkeen. Varastonarvostus olettaa, että kaikki varastot myydään samanaikaisesti. Voit valita tällä asetuksella **Keskimääräisten kustannusten laskennan yleiskuvaus** -sivun **Yksikkökustannus**-kentän, jolla voit tarkastella tapahtumahistoriaa, josta keskimääräinen kustannus lasketaan.

Voit tarkastella tai muokata erityiset hinnat tai alennukset, jotka haluat myöntää nimikkeelle, jos tietyt ehdot, kuten asiakas, vähimmäistilausmäärä tai päättymispäivämäärä, täyttyvät. Tämä tehdään valitsemalla **Määritä erikoishinnat**- tai **Määritä erikoisalennukset** -toiminto. Jokainen rivi, esimerkiksi **Myyntihinnat**-sivulla, edustaa erikoishintaa. Jokainen sarake vastaa ehtoa, jonka täytyy olla voimassa, jotta asiakkaalle voidaan myöntää erikoishinta, joka syötetään **Myyntihinnat**-sivun **Yksikköhinta**-kenttään. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

Nimike on nyt rekisteröity ja nimikekortti on valmis käytettäväksi osto- ja myyntiasiakirjoissa.

Jos haluat käyttää tätä nimikekorttia mallina, kun luot uusia nimikkeen kortteja, tallenna se mallina. Lisätietoja on seuraavassa osassa.

## <a name="to-save-the-item-card-as-a-template"></a>Nimikekortin tallentaminen mallina
1. Valitse **Nimikekortti**-sivulla **Tallenna mallina** -toiminto. **Nimikemalli**-sivu avautuu ja näyttää nimikekortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-sivu avautuu ja esittää kaikki dimensiokoodit, jotka on määritetty nimikkeelle.
4. Muokkaa tai syötä dimensiokoodit, joita käytetään mallin avulla luotuihin uusiin nimikkeen kortteihin.
5. Kun olet määrittänyt uuden nimikemallin, valitse **OK**-painike.

Nimikemalli lisätään nimikemallien luetteloon niin, että sen avulla voit luoda uusia nimikekortteja.

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Useiden toimittajien määrittäminen nimikkeille  
Jos ostat saman nimikkeen useammalta kuin yhdeltä toimittajalta, sinun tulee syöttää tietoja kustakin nimikkeen toimittajasta, esimerkiksi hinnat, toimitusaika ja alennukset.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.  
2.  Valitse ensin käsiteltävä nimike ja sitten **Muokkaa**-toiminto.  
3.  Valitse **Toimittajat**-toiminto.  
4.  Valitse **Toimittajan nro** -kenttä, ja valitse toimittaja, jonka haluat määrittää nimikkeelle.  
5.  Voit täyttää myös jäljellä olevat rivit.  
6.  Toista vaiheet 2–5 kullekin toimittajalle, jolta haluat ostaa nimikkeitä.

Toimittajat näkyvät nyt nimikkeen kortissa avattavassa **Nimikkeen toimittajaluettelo** -sivulla, jossa voit valita kätevästi vaihtoehtoisen toimittajan.

## <a name="see-also"></a>Katso myös
[Numerosarjojen luominen](ui-create-number-series.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
