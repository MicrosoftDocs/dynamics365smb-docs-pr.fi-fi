---
title: 'Toimintaohje: erikoistilausten luominen'
description: Tietoja siitä, miten erikoistilauksen voi luoda tietylle luettelonimikkeelle, joka toimitetaan tietylle asiakkaalle.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 3f9cb0690bf21c3b4571ff65486038499af010e9
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078542"
---
# <a name="create-special-orders"></a>Erikoistilausten luominen

Erikoistilauksen voi luoda tietylle luettelonimikkeelle, joka toimitetaan tietylle asiakkaalle. Toimittajasi toimittaa nimikkeen fyysiseen varastoosi, ja sen jälkeen voit toimittaa nimikkeen asiakkaallesi joko erikseen tai yhdessä muiden, toisen tilauksen nimikkeiden kanssa.  

Erikoistilaukset ilmaisevat, että osto- ja myyntitilaus on linkitetty toisiinsa. Näin varmistetaan, että tietty luettelonimike poimitaan ja toimitetaan kyseiselle asiakkaalle.  

Ennen kuin tätä ominaisuutta voi käyttää, tilaukselle tarpeelliset asiakas-, myyjä- ja nimikekortit tulee määrittää.  

## <a name="to-create-a-special-order"></a>Erikoistilausten luominen

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaus** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. Luo nimikkeelle  myyntitilaus ja täytä se. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
3.  Täytä myyntirivi **Rivit**-pikavälilehdessä. Valitse **Ostamisen koodi** -kentässä ostokoodi, jonka **Erikoistilaus**-kenttä on valittuna.

    Luo seuraavaksi ostotilaus hankintalistasta.  
4. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hankintalista** ja valitse sitten liittyvä linkki.  
5. Valitse ensin **Erikoistilaus**-toiminto ja sitten **Hae myyntitilaukset** -toiminto.  
6.  Näytä **Hae myyntitilaukset** -sivulla tulokset, joissa **Asiakirjan nro.** on myyntitilauksen numero. Valitse **OK**-painike. Ohjelma luo nimikkeelle hankintalistan rivin.  
7.  Valitse hankintalistarivin  **Toimenpideviesti**-kentässä **Uusi**.  
8.  Valitse **Hankintalista**-sivulla **Toteuta toimenpideviesti** -toiminto. **Toteuta toim.pideviesti - hank** -sivu avautuu. Valitse **OK**-painike.  

    Näyttöön tulee ikkuna, jossa ilmoitetaan, että ostotilaukset on luotu. Valitse **OK**-painike.  

Suunnittelujärjestelmä säilyttää myyntitilaukselle erikoistilauksena luodun ostotilauksen, koska se tasapainottaa kysyntää ja tarjontaa. Ostotilaus (tarjonta) pysyy linkitettynä myyntitilaukseen (kysyntään), vaikka ostotilauksella voisi toimittaa toisen aiemman kysynnän. Lisätietoja on kohdassa [Rakennetiedot: Uusintatilauskäytännöt](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Et voi käyttää erikoistilauksen toimintoja, jos nimike on jo varattu. Tämän varmista erikoistilauksina myydyille nimikkeille, että **Varaa**-kenttää nimikkeen kortissa ei ole määritetty arvoon **Aina**.  

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Luettelonimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md)  
[Myynti](sales-manage-sales.md)  
[Suoratoimitusten tekeminen](sales-how-drop-shipment.md)   
[Rakennetiedot: uusintatilauskäytännöt](design-details-reservation-order-tracking-and-action-messaging.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]