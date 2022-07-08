---
title: Luettelonimikkeiden luominen ja hallinta
description: Tietoja siitä, miten myydään nimikkeitä, joita ei pidä nimikeluettelossa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.search.forms: 5725, 5726, 5732
ms.date: 06/20/2022
ms.author: bholtorf
ms.openlocfilehash: c12eb256d4e7f1e211e28dacf4c403406dba3d85
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077005"
---
# <a name="work-with-catalog-items"></a>Luettelonimikkeiden käsitteleminen

Luettelonimikkeet ovat nimikkeitä, joita et hallitse [!INCLUDE[prod_short](includes/prod_short.md)]issa ennen kuin myyt ne. Kun lisäät luettelonimikkeen myyntitilauksen tai -tarjouksen riviin käyttämällä **Valitse luettelonimike** -toimintoa, luettelonimike muunnetaan tavalliseksi nimikkeeksi.

> [!NOTE]  
> Luettelonimikettä ei voi valita **Myyntilasku**-sivulla.

Luettelonimikkeellä on yleensä sen toimittavan toimittajan nimikenumero. Ennen kuin voit muuntaa luettelonimikkeen tavalliseksi nimikkeeksi, sinun täytyy määrittää, miten toimittajan nimikenumerot muunnetaan nimikenumerointisi mukaisiksi. Lisätietoja: [Määritä, miten luettelonimikenumerot muunnetaan omaksi numeroinniksi](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering)  

> [!IMPORTANT]
> Luettelonimikkeitä ei tule sekoittaa muihin kuin varastonimikkeisiin, jotka ovat tavallisia nimikkeitä, joiden tyyppi on **Muu kuin varasto**. Niitä ei oteta mukaan saatavuus- ja arvostuslaskelmiin esimerkiksi sen vuoksi, että niitä käytetään vain sisäisesti ja niiden arvo on vähäinen. Lisätietoja on kohdassa [Tietoja nimiketyypeistä](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a>Luettelonimikkeen luominen

Luettelonimikkeiden korteissa on paljon vähemmän tietoja kuin normaalien nimikkeiden korteissa, koska niitä käytetään tarjouksissa ja tehtäessä muita tilauksia. Tämän vuoksi ne on muunnettava normaaleiden nimikkeiden korteiksi, ennen kuin niille voidaan kirjata myyntitapahtumat.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luettelonimikkeet** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Määritä, miten luettelonimikenumerot muunnetaan omaksi numeroinniksi

Ennen kuin voit muuntaa luettelonimikkeen tavalliseksi nimikkeeksi, sinun täytyy määrittää, miten toimittajan nimikenumerot muunnetaan nimikenumerointisi mukaisiksi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luettelonimikkeen asetukset** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät.

## <a name="convert-a-catalog-item-to-a-normal-item"></a>Muunna luettelonimike normaaliksi nimikkeeksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luettelonimikkeet** ja valitse sitten vastaava linkki.
2. Avaa sen luettelonimikkeen kortti, jonka haluat muuntaa normaaliksi nimikkeeksi.
3. Valitse **Luettelonimikkeen kortti**-sivulla **Luo nimike** -toiminto.

Luodaan uusi nimikekortti, johon on täytetty luettelonimikkeen tiedot, ja asiaankuuluva nimikemalli. Tämän jälkeen voit täyttää uuden nimikekortin kentät tai muokata niitä tarvittaessa. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Luettelonimikkeen myyminen ja muuntaminen normaaliksi nimikkeeksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto. Täytä **Yleinen**-pikavälilehden kentät samalla tavalla kuin myyntitilauksen kentät. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
3. Valitse uuden tilausrivin **Tyyppi**-kentässä **Nimike**, mutta jätä **Nro**-kenttä tyhjäksi.
4. Valitse ensin **Rivi**-toiminto ja sitten **Valitse luettelonimikkeet** -toiminto.

    Luettelonimike muunnetaan normaaliksi nimikkeeksi. Luodaan uusi nimikekortti, johon on täytetty luettelonimikkeen tiedot, ja asiaankuuluva nimikemalli.
5. Valitse **Luettelonimikkeet**-sivulla luettelonimike, jonka haluat myydä, ja valitse sitten **OK**-painike.
6. Kun myyntitilaus on valmis, valitse **Kirjaa**-toiminto.

Tämän jälkeen voit täyttää uuden nimikekortin kentät tai muokata niitä tarvittaessa. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

> [!NOTE]  
> Nimikkeen viittaus on automaattisesti nimike, jonka numero on toimittajan nimikenumeron ja uuden nimikenumeron välissä. Lisätietoja on kohdassa [Nimikkeen viittausten käyttäminen](inventory-how-use-item-cross-refs.md).

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Erikoistilausten luominen](sales-how-to-create-special-orders.md)  
[Varasto](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
