---
title: Tietoja nimiketyypeistä
description: 'Voit muuttaa nimikkeen varastonarvostusta FIFO- tai Keskiarvo-arvostusmenetelmällä, kun nimikkeen kustannusten muutoksen syynä on jokin muu kuin tapahtuma.'
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="about-item-types" />Tietoja nimiketyypeistä
Voit valita **Nimikkeen kortti** -sivun **Tyyppi**-kentässä nimikkeen käyttötarkoituksen yrityksessä. Valinta määrittää myös sen, missä määrin voit hallita tavaraa varastossa. Seuraavassa taulukossa on lueteltu ja kuvattu käytettävissä olevat kolme nimiketyyppiä.

|Asetus|Tyypillinen tarkoitus|
|------|-----------|
|Varasto|Fyysiset asiat, kuten polkupyörät, puhelimet ja työpöydät, joiden osalta haluat pystyä käyttämään kaikkia varastoprosesseja. Tämä voi sisältää myös muita kuin fyysisiä nimikkeitä, kuten ohjelmistolisenssit ja -tilaukset, jos nimikkeillä on tunnistenumerot, kuten sarjanumerot. Voit seurata täysin tuotteiden arvoja ja saatavuutta varastossa.|
|Muu kuin varasto|Tyypillisesti muut kuin varastotuotteet ovat fyysisiä tavaroita, kuten pultteja tai kyniä, joita yritys kuluttaa, mutta joita ei haluta seurata täysin varastossa. Esimerkiksi, koska ne ovat edullisia nimikkeitä ja niitä käytetään vain sisäisesti.|
|Palvelu|Työn aikayksikkö, kuten konsultointitunti, jolla on yrityksen rajoitettu tuki.|

> [!NOTE]
> **Huolto**- ja **Muu kuin varasto** -tyypit eivät tue varaston määrien ja arvojen seurantaa. Vain valittuja nimiketapahtuman tyyppejä ja toimintoja tuetaan.

Seuraavassa taulukossa on lueteltu ominaisuudet, joita nämä kolme kohdetyyppiä tukevat.

|Nimiketyyppi|Myynti|Ostaminen|Projektin kulutus|Huollon kulutus|Kokoonpanon kulutus|Tuotanto Kulutus|Kokoonpanon tuotos|Tuotannon tuotos|Sijainnin siirto|Fyysinen inventointi|varaston uudelleenarvostus|Varaston arvostus|Nimikeseuranta|Varaus|Varastointi|Suunnitt.|Tilauksen suunnittelu|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Vaihto-omaisuus|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|
|Muu kuin varasto|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Kyllä|
|Palvelu|Kyllä|Kyllä|Kyllä|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Kyllä|

## <a name="costing-methods-for-types-of-items" />Nimiketyyppien arvostusmenetelmät
Kun kirjaat varastotapahtumia varaston määrien muutokset kirjataan nimiketapahtumiin ja varaston arvon muutokset arvotapahtumiin. 

Varastonimikkeiden kustannus kirjataan **Arvotapahtumat**-sivun **Kustannussumma (todellinen)** -kenttään, ja kun se täsmäytetään pääkirjanpitoon, kustannus näytetään **KP:oon kirjattu kustannus** -kentässä. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Varaston arvostus](design-details-inventory-costing.md).

Muiden kuin varastonimikkeiden ja huoltonimikkeiden kustannus kirjataan **Arvotapahtumat**-sivun **Kustannussumma (ei-var.)** -kenttään. Muissa kuin varastonimikkeissä ja huoltonimikkeissä kustannus määritetään myynti-, kokoonpano- ja tuotantoasiakirjoissa ja -päiväkirjoissa. Oletuskustannus voidaan määrittää **Yksikkökustannus**-kentässä **Nimikkeen kortti**- ja **Varastointiyksikkö**-sivuilla. Näiden nimiketyyppien kustannuksia ei täsmäytetä pääkirjanpitoon. 

## <a name="catalog-and-service-items" />Luettelo- ja huoltonimikkeet
Nimikkeet, joita tarjoat asiakkaille, mutta joita et halua ylläpitää järjestelmässäsi ennen kuin niitä myydään, voidaan määrittää luettelonimikkeiksi. Luettelonimikkeitä ei tule sekoittaa tavallisiin nimikkeisiin, joiden tyyppi on Muu kuin varasto. Lisätietoja on kohdassa [Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md).

Asiakkaiden nimikkeitä, joita huolletaan (esimerkiksi tulostin), sanotaan huoltonimikkeiksi. Huoltonimikkeet eivät ole samanlaisia kuin tavalliset nimikkeet tai luettelonimikkeet. Huollon komponentit voivat kuitenkin olla tavallisia nimikkeitä. Lisätietoja on kohdassa [Huoltonimikkeiden ja huoltonimikkeiden komponenttien määrittäminen](service-how-setup-service-items.md).

## <a name="see-also" />Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varaston määrittäminen](inventory-setup-inventory.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Varasto](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
