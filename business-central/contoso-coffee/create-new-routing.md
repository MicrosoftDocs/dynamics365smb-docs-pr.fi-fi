---
title: Uuden reitityksen luominen
description: Vaihekuvauksessa on tietoja siitä, miten uuden reitityksen tiedot syötetään manuaalisesti Business Centralissa.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: deb1ef6ab18cbd6562ae18cc17495fe3e5021db1
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525067"
---
# <a name="walkthrough-create-a-new-routing"></a>Vaihekuvaus: Luo uusi reititys

Tässä artikkelissa on tietoja Contoso Coffee -esittelytietojen käytöstä uuden tuotantoreitityksen manuaaliseen määrittämiseen [!INCLUDE [prod_short](../includes/prod_short.md)]issa.  

## <a name="scenario"></a>Esimerkkitilanne

Contoso Coffeen prosessisuunnittelija Oscar päättää luoda uuden reitityksen nimellä *Uusi polku*. Koska reititys on erilainen kuin mikä tahansa muu reititys Contoso Coffeessa, hänen täytyy syöttää kaikki reitityksen tiedot manuaalisesti.  

## <a name="steps"></a>Vaiheet

1. Luo reitityksen otsikko.  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **reititykset** ja valitse sitten vastaava linkki.  

    2. Valitse **Uusi**-toiminto ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä  |Arvo  |
        |---------|---------|
        |**Ei.** |1099|
        |**Kuvaus** |Uusi polku|
2. Luo reititysrivit.

    1. Lisää **Rivit** -pikavälilehdessä uusi rivi ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä  |Arvo  |
        |---------|---------|
        |**Operaation nro** |10|
        |**Tyyppi** |Tuotantosolu|
        |**Ei.** |100|
        |**Asetusaika** |20|
        |**Ajoaika** |15|

    2. Lisää uusi rivi ja täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

        |Kenttä  |Arvo  |
        |---------|---------|
        |**Operaation nro** |20|
        |**Tyyppi** |Tuotantosolu|
        |**Ei.** |200|
        |**Asetusaika** |30|
        |**Ajoaika** |5|
3. Hyväksy reititys.

    1. Valitse **Tila**-kentässä *Varmennettu*.  

Uusi reititys on nyt määritetty.  

## <a name="see-also"></a>Katso myös

[Johdatus Contoson kahvidemotietoihin](contoso-coffee-intro.md)  
