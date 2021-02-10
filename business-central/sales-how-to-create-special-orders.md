---
title: Erikoistilausten luominen | Microsoft Docs
description: Erikoistilauksen voi luoda tietylle luettelonimikkeelle, joka toimitetaan tietylle asiakkaalle. Toimittajasi toimittaa nimikkeen fyysiseen varastoosi, ja sen jälkeen voit toimittaa nimikkeen asiakkaallesi joko erikseen tai yhdessä muiden, toisen tilauksen nimikkeiden kanssa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c4549492e118d1b4367e89f2b0169f43ba7f8393
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748241"
---
# <a name="create-special-orders"></a>Erikoistilausten luominen
Erikoistilauksen voi luoda tietylle luettelonimikkeelle, joka toimitetaan tietylle asiakkaalle. Toimittajasi toimittaa nimikkeen fyysiseen varastoosi, ja sen jälkeen voit toimittaa nimikkeen asiakkaallesi joko erikseen tai yhdessä muiden, toisen tilauksen nimikkeiden kanssa.  

Erikoistilaukset ilmaisevat, että osto- ja myyntitilaus on linkitetty toisiinsa. Näin varmistetaan, että tietty luettelonimike poimitaan ja toimitetaan kyseiselle asiakkaalle.  

Ennen kuin tätä ominaisuutta voi käyttää, tilaukselle tarpeelliset asiakas-, myyjä- ja nimikekortit tulee määrittää.  

## <a name="to-create-a-special-order"></a>Erikoistilausten luominen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaus** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto. Luo nimikkeelle  myyntitilaus ja täytä se. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
3.  Täytä myyntirivi **Rivit**-pikavälilehdessä. Valitse **Ostamisen koodi** -kentässä ostokoodi, jonka **Erikoistilaus**-kenttä on valittuna.

    Luo seuraavaksi ostotilaus hankintalistasta.  
4. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hankintalista** ja valitse sitten liittyvä linkki.  
5. Valitse ensin **Erikoistilaus**-toiminto ja sitten **Hae myyntitilaukset** -toiminto.  
6.  Näytä **Hae myyntitilaukset** -sivulla tulokset, joissa **Asiakirjan nro.** on myyntitilauksen numero. Valitse **OK**-painike. Ohjelma luo nimikkeelle hankintalistan rivin.  
7.  Valitse hankintalistarivin  **Toimenpideviesti**-kentässä **Uusi**.  
8.  Valitse **Hankintalista**-sivulla **Toteuta toimenpideviesti** -toiminto. **Toteuta toim.pideviesti - hank** -sivu avautuu. Valitse **OK**-painike.  

    Näyttöön tulee ikkuna, jossa ilmoitetaan, että ostotilaukset on luotu. Valitse **OK**-painike.  

Suunnittelujärjestelmä säilyttää myyntitilaukselle erikoistilauksena luodun ostotilauksen, koska se tasapainottaa kysyntää ja tarjontaa. Ostotilaus (tarjonta) pysyy linkitettynä myyntitilaukseen (kysyntään), vaikka ostotilauksella voisi toimittaa toisen aiemman kysynnän. Lisätietoja on kohdassa [Rakennetiedot: Uusintatilauskäytännöt](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Et voi käyttää erikoistilauksen toimintoja, jos nimike on jo varattu. Tämän varmista erikoistilauksina myydyille nimikkeille, että **Varaa**-kenttää nimikkeen kortissa ei ole määritetty arvoon **Aina**.  

## <a name="see-also"></a>Katso myös  
[Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md)  
[Myynti](sales-manage-sales.md)  
[Suoratoimitusten tekeminen](sales-how-drop-shipment.md)   
[Rakennetiedot: uusintatilauskäytännöt](design-details-reservation-order-tracking-and-action-messaging.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)
