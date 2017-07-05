---
title: "Toimintaohje: Uusien nimikkeiden rekisteröinti| Microsoft Docs"
description: "Voit luoda kortteja uusille, varastosta esimerkiksi kappaleittain myytäville fyysisille tuotteille, tai tunteina myytäville palveluille."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 582e006291e51e19d80304d24ae055ce6ac8d698
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-register-new-items"></a>Toimintaohje: Uusien nimikkeiden rekisteröiminen
Nimikkeet ovat muiden tuotteiden eli tavaroiden tai palveluiden, joilla käyt kauppaa, ohessa liiketoimintasi perusta. Jokainen nimike on rekisteröitävä nimikekorttina.

Nimikekortti sisältää tiedot, jotka tarvitaan nimikkeiden ostamista, tallentamista, myymistä ja toimittamista varten.

Nimikekortin tyyppi voi olla **Varasto** tai **Palvelu**, jolloin voidaan määritellä, onko nimike fyysinen yksikkö vai työaikayksikkö. Lukuun ottamatta kenttiä, jotka liittyvät nimikkeen fyysisiin osa-alueisiin, kaikki nimikkeen kortin kentät toimivat samalla tavalla varastonimikkeille ja palveluille. Lisätietoja nimikkeen myymisestä on kohdassa [Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md) ja [Toimintaohje: Myynnin laskuttaminen](sales-how-invoice-sales.md).

Nimike voi olla tuoterakenteessa päänimike, jonka alla on alinimikkeitä. [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tuoterakennetta kutsutaan kokoonpanon tuoterakenteeksi. Kokoonpanon tuoterakenteen avulla jäsennetään päänimikkeet, joita myydään päänimikkeen osista koostuvina paketteina tai jotka kootaan tilausta tai varastointia varten. Lisätietoja on kohdassa [Toimintaohje: Tuoterakenteiden käyttäminen](inventory-how-work-BOMs.md).

**Huomautus**: Jos eri nimikkeen on olemassa asiakasmalleja, ikkuna tulee näkyviin, kun luot uuden nimikkeen kortin, jossa voit valita haluamasi mallin. Jos vain yksi nimikemalli on olemassa, uudet nimikekortit käyttävät aina kyseistä mallia.

## <a name="to-create-a-new-item-card"></a>Uuden nimikekortin luominen
1. Valitse kotisivun **Nimikkeet**-toiminto, kun haluat avata olemassa olevien nimikkeiden luettelon.  
2. Valitse **Nimikkeet**-ikkunassa **Uusi**-toiminto.

    Jos vain yksi nimikemalli on olemassa, uusi nimikekortti avautuu. Kortissa on kenttiä, jotka on täytetty mallin tiedoilla.
3. Valitse **Valitse malli uudelle nimikkeelle** -ikkunassa malli, jota haluat käyttää uudessa nimikekortissa.
4. Valitse **OK**-painike. Uuden nimikekortti avautuu. Osa kortin kentistä on täytetty mallin tiedoilla.
5. Voit täyttää nimikekortin kenttiä tai muuttaa niitä tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Hinta ja kirjaus**-pikavälilehti sisältää erityiset hinnat tai alennukset, jotka haluat myöntää nimikkeelle, jos tietyt ehdot, kuten asiakas, vähimmäistilausmäärä tai päättymispäivämäärä, täyttyvät. Kukin rivi edustaa erityistä hinnan alennusta tai rivialennusta. Kukin sarake vastaa ehtoa, joka takaa **Yksikköhinta**-kenttään kirjoitetun erikoishinnan tai **Rivialennus-%**-kenttään kirjoitetun rivialennuksen. Lisätietoja on kohdassa [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

Nimike on nyt rekisteröity ja nimikekortti on valmis käytettäväksi osto- ja myyntiasiakirjoissa.

Jos haluat käyttää tätä nimikekorttia mallina, kun luot uusia nimikkeen kortteja, tallenna se mallina. Lisätietoja on seuraavassa osassa.

## <a name="to-save-the-item-card-as-a-template"></a>Nimikekortin tallentaminen mallina
1. Valitse **Nimikekortti**-ikkunassa **Tallenna mallina** -toiminto. **Nimikemalli**-ikkuna avautuu ja näyttää nimikekortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-ikkuna avautuu ja esittää kaikki dimensiokoodit, jotka on määritetty nimikkeelle.
4. Muokkaa tai syötä dimensiokoodit, joita käytetään mallin avulla luotuihin uusiin nimikkeen kortteihin.
5. Kun olet määrittänyt uuden nimikemallin, valitse **OK**-painike.

Nimikemalli lisätään nimikemallien luetteloon niin, että sen avulla voit luoda uusia nimikekortteja.

## <a name="see-also"></a>Katso myös
  [Varasto](inventory-manage-inventory.md)  
  [Osto](purchasing-manage-purchasing.md)  
  [Myynti](sales-manage-sales.md)  
  [[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]in käyttäminen](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]