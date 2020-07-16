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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 481e8bbdb13863055c4dc532cb2c214228b8a8ba
ms.sourcegitcommit: 0b5f8f68b1c9526288bfcce1a3bdc988d2910040
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454294"
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

## <a name="costing-methods-for-types-of-items"></a>Nimiketyyppien arvostusmenetelmät
Kun kirjaat varastotapahtumia varaston määrien muutokset kirjataan nimiketapahtumiin ja varaston arvon muutokset arvotapahtumiin. 

Varastonimikkeiden kustannus kirjataan **Arvotapahtumat**-sivun **Kustannussumma (todellinen)** -kenttään, ja kun se täsmäytetään pääkirjanpitoon, kustannus näytetään **KP:oon kirjattu kustannus** -kentässä. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Varaston arvostus](design-details-inventory-costing.md).

Muiden kuin varastonimikkeiden ja huoltonimikkeiden kustannus kirjataan **Arvotapahtumat**-sivun **Kustannussumma (ei-var.)** -kenttään. Muissa kuin varastonimikkeissä ja huoltonimikkeissä kustannus määritetään myynti-, kokoonpano- ja tuotantoasiakirjoissa ja -päiväkirjoissa. Oletuskustannus voidaan määrittää **Yksikkökustannus**-kentässä **Nimikkeen kortti**- ja **Varastointiyksikkö**-sivuilla. Näiden nimiketyyppien kustannuksia ei täsmäytetä pääkirjanpitoon. 

## <a name="catalog-and-service-items"></a>Luettelo- ja huoltonimikkeet
Nimikkeet, joita tarjoat asiakkaille, mutta joita et halua ylläpitää järjestelmässäsi ennen kuin niitä myydään, voidaan määrittää luettelonimikkeiksi. Luettelonimikkeitä ei tule sekoittaa tavallisiin nimikkeisiin, joiden tyyppi on Muu kuin varasto. Lisätietoja on kohdassa [Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).

Asiakkaiden nimikkeitä, joita huolletaan (esimerkiksi tulostin), sanotaan huoltonimikkeiksi. Huoltonimikkeet eivät ole samanlaisia kuin tavalliset nimikkeet tai luettelonimikkeet. Huollon komponentit voivat kuitenkin olla tavallisia nimikkeitä. Lisätietoja on kohdassa [Huoltonimikkeiden ja huoltonimikkeiden komponenttien määrittäminen](service-how-setup-service-items.md).

## <a name="see-also"></a>Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varaston määrittäminen](inventory-setup-inventory.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
