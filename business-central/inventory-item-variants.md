---
title: Tuotevarianttien hallinta
description: 'Lisätietoja siitä, miten voit tallentaa tuotteita, jotka ovat lähes identtisiä, mutta joilla on väri-, koko- tai materiaalieroja nimikevarianteissa.'
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: edupont
---
# <a name="manage-product-variants"></a><a name="manage-product-variants"></a><a name="manage-product-variants"></a>Tuotevarianttien hallinta

Nimikevariantit ovat hyvä tapa hallita tuoteluetteloa. Tämä on hyödyllistä esimerkiksi silloin, jos on olemassa suuri määrä lähes samanlaisia nimikkeitä, joissa vain värit poikkeavat toisistaan. Jokainen variantti voidaan määrittää erilliseksi nimikkeeksi. Voit päättää määrittää yhden nimikkeen ja määrittää useita värejä nimikkeen varianteiksi.  

> [!TIP]
> Käytännöllinen esittely varianttien käyttämisestä tuotannossa on Contoso Coffeen esittelytietojen kohdassa [Vaihekuvaus: Variantit](contoso-coffee/manufacturing/variants.md).  

## <a name="add-variants-to-an-item"></a><a name="add-variants-to-an-item"></a><a name="add-variants-to-an-item"></a>Varianttien lisääminen nimikkeeseen

Jos organisaatio on päättänyt käyttää variantteja, nimikkeen varianttien määrittäminen on helppoa.  

### <a name="to-add-variants"></a><a name="to-add-variants"></a><a name="to-add-variants"></a>Varianttien lisääminen

1. Avaa [**Nimikeluettelo**-sivu](https://businesscentral.dynamics.com/?page=31) ja avaa sitten haluamasi nimike.  
2. Valitse **Nimike**-kortissa **Nimike**-toiminto ja valitse sitten **Variantit**-toiminto.  
3. **Nimikevariantit**-sivulla näkyy varianttiluettelo.  

Kun sitten luot myyntiasiakirjan ja lisäät nimikkeen, voit määrittää nimikkeen variantin **Varianttikoodi**-kenttään. Sama koskee ostoasiakirjoja.  

## <a name="item-availability-by-variant"></a><a name="item-availability-by-variant"></a><a name="item-availability-by-variant"></a>Nimikkeen saat. varianteittain

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a><a name="require-use-of-variants"></a><a name="require-use-of-variants"></a>Vaadi varianttien käyttöä

Vuoden 2022 2. julkaisuaallosta lähtien järjestelmänvalvojat ovat voineet vaatia käyttäjiä määrittämään variantin asiakirjoissa ja kirjauskansioissa nimikkeille, joilla on variantteja. Voit aktivoida ominaisuuden siirtymällä **Varaston asetukset** -sivulla ja valitsemalla **Versio pakollinen, jos on** -kenttä. Voit ohittaa tämän yleisen asetuksen tiettyjen nimikkeiden osalta.  

Nimikekorteissa **Variantti pakollinen jos on olemassa** -kentässä on seuraavat vaihtoehdot:

|Kentän arvo |Kuvaus|
|---------|----|
|Oletusarvo| **Varaston asetukset** -kohdan asetukset koskevat nimikettä.|
|Ei| Käyttäjien ei tarvitse määrittää tälle nimikkeelle varianttia.|
|Kyllä| Jos nimikkeellä on useita variantteja, käyttäjien täytyy määrittää asianmukainen variantti. Jos niitä ei ole, ne estetään kirjaamalla tapahtuma.|

> [!NOTE]
> Nämä asetukset eivät vaikuta sellaisiin nimikkeisiin, joilla ei ole variantteja.

Jos ominaisuus on otettu käyttöön, käyttäjät eivät voi kirjata tapahtumaa, jos varianttia ei ole määritetty.

## <a name="categories-attributes-and-variants"></a><a name="categories-attributes-and-variants"></a><a name="categories-attributes-and-variants"></a>Luokat, määritteet ja variantit

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Yleisten varastotietojen määrittäminen](inventory-how-setup-general.md)  
[Vaihekuvaus: Variantit](contoso-coffee/manufacturing/variants.md)  
