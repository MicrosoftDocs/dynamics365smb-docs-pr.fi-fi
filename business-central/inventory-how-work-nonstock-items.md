---
title: Luettelonimikkeiden luominen ja hallinta | Microsoft Docs
description: "Tässä artikkelissa kerrotaan, miten sellaisilla nimikkeillä käydään kauppaa, jotka ovat kuuluvat toimittajien nimikeluetteloon, mutta eivät omaan nimikeluetteloosi."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: feef36443adef82329fe47573dd05cc6941b9d87
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-catalog-items"></a>Luettelonimikkeiden käsitteleminen
Voit tarjota asiakkaille tiettyjä nimikkeitä, joita et halua ylläpitää järjestelmässäsi ennen kuin niitä myydään. Kun haluat alkaa ylläpitää tällaisia nimikkeitä järjestelmässäsi, voit muuntaa ne normaaleiden nimikkeiden korteiksi kahdella eri tavalla.

* Luo luettelonimikkeen kortille uusi nimikekortti mallin mukaan.
* Valitse luettelonimike **Nimike**-tyyppiseltä myyntitilausriviltä, jolla on tyhjä **Nro**-kenttä. Nimikekortti luodaan automaattisesti luettelonimikkeelle.

> [!NOTE]  
> Luettelonimikettä ei voi valita **Myyntilasku**-ikkunassa.<br /><br />
> Voit valita luettelonimikkeen **Myyntitarjous**-ikkunassa, mutta luettelonimikettä ei muunneta normaaliksi nimikkeeksi, jos käytössä on **Tee tilaus** -toiminto.

Luettelonimikkeellä on yleensä sen toimittavan toimittajan nimikenumero. Voit ottaa luettelonimikkeen kortin muuntamisen käyttöön normaalin nimikkeen kortille määrittämällä ensin, miten toimittajan nimikenumerointi muunnetaan omaksi nimikenumeroinniksesi.   

> [!Important]
> Luettelonimikkeitä ei tule sekoittaa muihin kuin varastonimikkeisiin, jotka ovat tavallisia nimikkeitä, joiden tyyppi on **Muu kuin varasto**. Niitä ei oteta mukaan saatavuus- ja arvostuslaskelmiin esimerkiksi sen vuoksi, että niitä käytetään vain sisäisesti ja niiden arvo on vähäinen. Lisätietoja on kohdassa [Tietoja nimiketyypeistä](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Luettelonimikkeen luominen
Luettelonimikkeiden korteissa on paljon vähemmän tietoja kuin normaalien nimikkeiden korteissa, koska niitä käytetään tarjouksissa ja tehtäessä muita tilauksia. Tämän vuoksi ne on muunnettava normaaleiden nimikkeiden korteiksi, ennen kuin niille voidaan kirjata myyntitapahtumat.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luettelonimikkeet** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Määritetään, miten luettelonimikenumerot muunnetaan omaksi numeroinniksi
Voit ottaa luettelonimikkeen kortin muuntamisen käyttöön normaalin nimikkeen kortille määrittämällä ensin, miten toimittajan nimikenumerointi muunnetaan omaksi numeromuodoksi.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luettelonimikkeen asetukset** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Luettelonimikkeen muuntaminen normaaliksi nimikkeeksi
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luettelonimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen luettelonimikkeen kortti, jonka haluat muuntaa normaaliksi nimikkeeksi.
3. Valitse **Luettelonimikkeen kortti**-ikkunassa **Luo nimike** -toiminto.

Luodaan uusi nimikekortti, johon on täytetty luettelonimikkeen tiedot, ja asiaankuuluva nimikemalli. Tämän jälkeen voit täyttää uuden nimikekortin kentät tai muokata niitä tarvittaessa. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Luettelonimikkeen myyminen ja muuntaminen normaaliksi nimikkeeksi
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä **Yleinen**-pikavälilehden kentät samalla tavalla kuin myyntitilauksen kentät. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
3. Valitse uuden tilausrivin **Tyyppi**-kentässä **Nimike**, mutta jätä **Nro**-kenttä tyhjäksi.
4. Valitse ensin **Rivi**-toiminto ja sitten **Valitse luettelonimikkeet** -toiminto.

    Luettelonimike muunnetaan normaaliksi nimikkeeksi. Luodaan uusi nimikekortti, johon on täytetty luettelonimikkeen tiedot, ja asiaankuuluva nimikemalli.
5. Valitse **Luettelonimikkeet**-ikkunassa luettelonimike, jonka haluat myydä, ja valitse sitten **OK**-painike.
6. Kun myyntitilaus on valmis, valitse **Kirjaa**-toiminto.

Tämän jälkeen voit täyttää uuden nimikekortin kentät tai muokata niitä tarvittaessa. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).

> [!NOTE]  
>   Toimittajalle luodaan automaattisesti nimikkeen viittaustietue nimikkeelle, jonka numero on toimittajan nimikenumeron ja uuden nimikenumeron välissä.

## <a name="see-also"></a>Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Erikoistilausten luominen](sales-how-to-create-special-orders.md)|  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

