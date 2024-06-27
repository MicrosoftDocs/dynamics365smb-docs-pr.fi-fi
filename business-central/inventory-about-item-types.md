---
title: Tietoja nimiketyypeistä
description: 'Lue lisää siitä, minkä tyyppisiä nimikkeitä voit hallita varastossa ja miten ne vaikuttavat. Voit muuttaa nimikkeen varastonarvostusta FIFO- tai Keskiarvo-arvostusmenetelmällä, kun nimikkeen kustannusten muutoksen syynä on jokin muu kuin tapahtuma.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-item-types"></a>Tietoja nimiketyypeistä

Voit valita **Nimikkeen kortti** -sivun **Tyyppi**-kentässä nimikkeen käyttötarkoituksen yrityksessä. Valinta määrittää myös sen, missä määrin voit hallita tavaraa varastossa. Seuraavassa taulukossa on lueteltu ja kuvattu käytettävissä olevat kolme nimiketyyppiä.

|Asetus|Tyypillinen tarkoitus|
|------|-----------|
|Varasto|Fyysiset asiat, kuten polkupyörät, puhelimet ja työpöydät, joiden osalta haluat pystyä käyttämään kaikkia varastoprosesseja. Varastotuotteet voivat sisältää myös ei-fyysisiä nimikkeitä, kuten ohjelmistolisenssejä ja tilauksia, jos tuotteilla on tunnistenumerot, kuten sarjanumerot. Voit seurata täysin tuotteiden arvoja ja saatavuutta varastossa.|
|Muu kuin varasto|Tyypillisesti muut kuin varastotuotteet ovat fyysisiä tavaroita, kuten pultteja tai kyniä, joita yritys kuluttaa, mutta joita ei haluta seurata täysin varastossa. Esimerkiksi, koska ne ovat edullisia nimikkeitä ja niitä käytetään vain sisäisesti.|
|Palvelu|Työn aikayksikkö, kuten konsultointitunti, jolla on yrityksen rajoitettu tuki.|

> [!NOTE]
> **Huolto**- ja **Muu kuin varasto** -tyypit eivät anna sinun seurata varaston määriä ja arvoja. Vain valittuja nimiketapahtuman tyyppejä ja toimintoja tuetaan. Seuraavassa taulukossa on lueteltu ominaisuudet, joita nämä kolme kohdetyyppiä tukevat.

|Nimiketyyppi|Myynti|Ostaminen|Projektin kulutus|Huollon kulutus|Kokoonpanon kulutus|Tuotanto Kulutus|Kokoonpanon tuotos|Tuotannon tuotos|Sijainnin siirto|Fyysinen inventointi|varaston uudelleenarvostus|Varaston arvostus|Nimikeseuranta|Varaus|Varastointi|Suunnitt.|Tilauksen suunnittelu|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Vaihto-omaisuus|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|
|Muu kuin varasto|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Kyllä|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Kyllä|
|Palvelu|Kyllä|Kyllä|Kyllä|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Ei|Kyllä|

## <a name="costing-methods-for-types-of-items"></a>Nimiketyyppien arvostusmenetelmät

Kun kirjaat varastotapahtumia varaston määrien muutokset kirjataan nimiketapahtumiin ja varaston arvon muutokset arvotapahtumiin.

Varastonimikkeiden kustannukset kirjataan **Kustannusmäärä (todellinen)** -kenttään sivulla **Arvon merkinnät**. Kun täsmäytät tapahtuman pääkirjanpitoon, kustannus näkyy **Kustannus kirjattu KP:toon** -kentässä. Lisätietoja varaston arvostuskustannuksista on kohdassa [Suunnittelun yksityiskohdat: Varaston arvostus](design-details-inventory-costing.md).

Muiden kuin varastonimikkeiden ja huoltonimikkeiden kustannus kirjataan **Arvotapahtumat**-sivun **Kustannussumma (ei-var.)** -kenttään. Muissa kuin varastonimikkeissä ja huoltonimikkeissä kustannus määritetään myynti-, kokoonpano- ja tuotantoasiakirjoissa ja -päiväkirjoissa. Oletuskustannus voidaan määrittää **Yksikkökustannus**-kentässä **Nimikkeen kortti**- ja **Varastointiyksikkö**-sivuilla. Näiden nimiketyyppien kustannuksia ei täsmäytetä pääkirjanpitoon.

## <a name="catalog-and-service-items"></a>Luettelo- ja huoltonimikkeet

Voit määrittää nimikkeitä, joita tarjoat asiakkaillesi, mutta et hallitse niitä ennen kuin myyt ne luettelonimikkeinä. Vaikka kataloginimikkeet ovat samanlaisia kuin tavalliset nimikkeet, joiden tyyppi on tässä suhteessa **Ei varasto**, älä sekoita näitä kahta, koska niissä on eroja. Saat lisätietoja siirtymällä kohtaan [Luettelonimikkeiden käyttäminen](inventory-how-work-nonstock-items.md).

Asiakkaan nimikkeet, joita huolletaan (esimerkiksi tulostin), sanotaan huoltonimikkeiksi. Huoltonimikkeet eivät ole samanlaisia kuin tavalliset nimikkeet tai luettelonimikkeet. Huollon komponentit voivat kuitenkin olla tavallisia nimikkeitä. Lisätietoja on kohdassa [Huoltonimikkeiden ja huoltonimikkeiden komponenttien määrittäminen](service-how-setup-service-items.md).

## <a name="see-also"></a>Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varaston määrittäminen](inventory-setup-inventory.md)  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Varasto](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
