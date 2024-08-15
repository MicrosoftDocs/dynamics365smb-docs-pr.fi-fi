---
title: Tuotevarianttien hallinta
description: 'Lisätietoja siitä, miten voit tallentaa tuotteita, jotka ovat lähes identtisiä, mutta joilla on väri-, koko- tai materiaalieroja nimikevarianteissa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---

# Tuotevarianttien hallinta

Nimikevariantit ovat hyvä tapa hallita tuoteluetteloa. Tämä on hyödyllistä esimerkiksi silloin, jos on olemassa suuri määrä lähes samanlaisia nimikkeitä, joissa vain värit poikkeavat toisistaan. Jokainen variantti voidaan määrittää erilliseksi nimikkeeksi. Voit myös päättää määrittää yhden nimikkeen ja määrittää useita värejä nimikkeen varianteiksi.  

> [!TIP]
> Käytännöllinen esittely varianttien käyttämisestä tuotannossa on Contoso Coffeen esittelytietojen kohdassa [Vaihekuvaus: Variantit](contoso-coffee/manufacturing/variants.md).  

## Varianttien lisääminen nimikkeeseen

Nimikkeelle on helppo määrittää variantteja.  

### Varianttien lisääminen

1. Avaa [**Nimikeluettelo**-sivu](https://businesscentral.dynamics.com/?page=31) ja avaa sitten haluamasi nimike.  
2. Valitse **Nimike kortti-ikkunassa** Aiheeseen liittyvä **toiminto, valitse**  **nimike ja valitse variantit-toiminto** **.**   
3.  **Luetteloi Variantit-sivulla** variantit.  

Kun sitten luot myyntiasiakirjan ja lisäät nimikkeen, voit määrittää nimikkeen variantin Varianttikoodi-kenttään **·** . Sama pätee myös ostoasiakirjoihin.  

## Nimikkeen saat. varianteittain

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## Vaadi varianttien käyttöä

Vuoden 2022 2. julkaisuaallosta lähtien järjestelmänvalvojat ovat voineet vaatia käyttäjiä määrittämään variantin asiakirjoissa ja kirjauskansioissa nimikkeille, joilla on variantteja. Voit aktivoida ominaisuuden siirtymällä **Varaston asetukset** -sivulla ja valitsemalla **Versio pakollinen, jos on** -kenttä. Voit ohittaa tämän yleisen asetuksen tiettyjen nimikkeiden osalta.  

Nimikekorteissa **Variantti pakollinen jos on olemassa** -kentässä on seuraavat vaihtoehdot:

|Kentän arvo |Kuvaus|
|---------|----|
|Oletus (Ei)| **Varaston asetukset** -kohdan asetukset koskevat nimikettä.|
|Ei| Käyttäjien ei tarvitse määrittää tälle nimikkeelle varianttia.|
|Kyllä| Jos nimikkeellä on useita variantteja, käyttäjien täytyy määrittää asianmukainen variantti. Jos niitä ei ole, ne estetään kirjaamalla tapahtuma.|

> [!NOTE]
> Nämä asetukset eivät vaikuta sellaisiin nimikkeisiin, joilla ei ole variantteja.

Jos ominaisuus on otettu käyttöön, käyttäjät eivät voi kirjata tapahtumaa, jos varianttia ei ole määritetty.

## Luokat, määritteet ja variantit

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)    
[Yleisen varaston tietojen määrittäminen](inventory-how-setup-general.md)    
[Vaihekuvaus: Variantit](contoso-coffee/manufacturing/variants.md)    
