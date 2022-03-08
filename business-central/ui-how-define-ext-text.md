---
title: Laajennettujen kuvausten määrittäminen ylimääräisiä rivejä lisäämällä
description: Voit laajentaa nimikkeen, KP-tilin ja muiden tietojen kuvauksena käytettävää vakiotekstiä lisäämällä ylimääräisiä rivejä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/08/2020
ms.author: edupont
ms.openlocfilehash: cf0418f4182e9d66da88af9262dd807a34dd3572
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782316"
---
# <a name="add-extended-text"></a>Lisätekstin lisääminen

Nimikkeiden, varastointiyksiköiden, pääkirjanpitotilien ja resurssien kuvausta voi laajentaa lisäämällä lisärivejä lisätekstinä. Lisärivien käytölle voi määrittää myös ehdot.  

Seuraavassa osassa käsitellään lisätekstin lisäämistä nimikkeen kuvaukseen. Samat ohjeet koskevat myös varastointiyksiköitä, kirjanpitotilejä ja resursseja.  

## <a name="to-define-extended-text-for-an-description"></a>Kuvauksen lisätekstin määrittäminen

1. Avaa sen nimikkeen kortti, johon lisäteksti lisätään, ja valitse **Lisäteksti**-toiminto.
2. Täytä **Koodi**- ja **Kuvaus**-kentät.
3. Valitse **Uusi**.
4. Täytä **Kielikoodi**-kenttä tai valitse **Kaikki kielikoodit** -valintaruutu, jos käytät kielikoodeja.
5. Anna arvot **Aloituspvm**- ja/tai **Lopetuspvm**-kenttään, jos haluat rajoittaa lisätekstin käyttöpäiviä.
6. Kirjoita lisäteksti **Teksti**-kenttään.
7. Valitse asianmukaiset valintaruudut niitä asiakirjatyyppejä varten, joihin haluat lisätekstin tulostuvan.
8. Sulje sivu.

Tämän lisätekstin voi lisätä nyt asiakirjoihin. Seuraavaksi käsitellään tapaa, jolla lisäteksti lisätään myyntilaukseen, mutta lisäteksti määritetään samalla tavalla myös mihin tahansa muuhun asiakirjaan.  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>Laajennetun nimiketekstin lisääminen myyntitilausriville

1. Avaa sen nimikkeen myyntitilaus ja myyntirivi, jolle on määritetty laajennettu teksti. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
2. Valitse kyseinen rivi ja valitse sitten **Syötä lisätekstit** -toiminto.

## <a name="see-also"></a>Katso myös

[Varaston määrittäminen](inventory-setup-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
