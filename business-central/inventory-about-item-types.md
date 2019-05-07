---
title: Tietoja nimiketyypeistä | Microsoft Docs
description: Voit muuttaa nimikkeen varastonarvostusta FIFO- tai Keskiarvo-arvostusmenetelmällä, esimerkiksi silloin, kun nimikkeen kustannusten muutoksen syynä on jokin muu kuin tapahtuma.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7e535abbc3fb61a958f63f648cca6694199acdc8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "921770"
---
# <a name="about-item-types"></a>Tietoja nimiketyypeistä
Voit valita **Nimikkeen kortti** -sivun **Tyyppi**-kentässä nimikkeen käyttötarkoituksen yrityksessä. Valinta määrittää myös sen, miten nimikettä ylläpidetään järjestelmässä. Valittavana on seuraavat kolme vaihtoehtoa:

|Asetus|Tyypillinen tarkoitus|
|------|-----------|
|Vaihto-omaisuus|Fyysinen yksikkö, kuten polkupyörä, jolla on yrityksen täysi tuki.|
|Muu kuin varasto|Fyysinen yksikkö, kuten pultti, jolla on yrityksen rajoitettu tuki esimerkiksi siksi, että nimikettä käytetään vain sisäisesti ja sen arvo on vähäinen.|
|Palvelu|Työn aikayksikkö, kuten konsultointitunti, jolla on yrityksen rajoitettu tuki.|

**Varasto**-tyyppi käsittää varaston määrän ja arvon täydellisen seurannan. Sen vuoksi kaikkia nimiketapahtuman tyyppejä tuetaan ja nimikkeitä, joiden tyyppi on Varasto, voidaan käyttää kaikissa nimikkeitä käsittelevissä toiminnoissa.

**Huolto**- ja **Muu kuin varasto** -tyypit eivät sisällä varaston määrän ja arvon seurantaa. Tämän vuoksi vain valittuja nimiketapahtuman tyyppejä ja toimintoja tuetaan.

Kolme nimiketyyppiä tukevat seuraavia toimintoja.

|Nimiketyyppi|Myynti|Ostaminen|Projektin kulutus|Huollon kulutus|Kokoonpanon kulutus|Tuotanto Kulutus|Kokoonpanon tuotos|Tuotannon tuotos|Sijainnin siirto|Fyysinen inventointi|varaston uudelleenarvostus|Varaston arvostus|Nimikeseuranta|Varaus|Varastointi|Suunnittelu|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Vaihto-omaisuus|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|
|Muu kuin varasto|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|
|Palvelu|Kyllä|Kyllä|Kyllä|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|

> [!NOTE]
> Nimikkeet, joita tarjoat asiakkaille, mutta joita et halua ylläpitää järjestelmässäsi ennen kuin niitä myydään, voidaan määrittää luettelonimikkeiksi. Luettelonimikkeitä ei tule sekoittaa tavallisiin nimikkeisiin, joiden tyyppi on Muu kuin varasto. Lisätietoja on kohdassa [Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Asiakkaiden nimikkeitä, joita huolletaan (esimerkiksi tulostin), sanotaan huoltonimikkeiksi. Huoltonimikkeet eivät ole samanlaisia kuin tavalliset nimikkeet tai luettelonimikkeet. Huollon komponentit voivat kuitenkin olla tavallisia nimikkeitä. Lisätietoja on kohdassa [Huoltonimikkeiden ja huoltonimikkeiden komponenttien määrittäminen](service-how-setup-service-items.md).

## <a name="see-also"></a>Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varaston määrittäminen](inventory-setup-inventory.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
