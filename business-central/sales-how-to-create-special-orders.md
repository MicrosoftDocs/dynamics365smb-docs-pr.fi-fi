---
title: Erikoistilausten luominen | Microsoft Docs
description: "Erikoistilauksen voi luoda tietylle ei-varastoitavalle nimikkeelle, joka toimitetaan tietylle asiakkaalle. Toimittajasi toimittaa nimikkeen fyysiseen varastoosi, ja sen jälkeen voit toimittaa nimikkeen asiakkaallesi joko erikseen tai yhdessä muiden, toisen tilauksen nimikkeiden kanssa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 84b7a66734b3da5bdbc474bc43e463481c7f6ba5
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-special-orders"></a>Erikoistilausten luominen
Erikoistilauksen voi luoda tietylle ei-varastoitavalle nimikkeelle, joka toimitetaan tietylle asiakkaalle. Toimittajasi toimittaa nimikkeen fyysiseen varastoosi, ja sen jälkeen voit toimittaa nimikkeen asiakkaallesi joko erikseen tai yhdessä muiden, toisen tilauksen nimikkeiden kanssa.  

Erikoistilaukset ilmaisevat, että osto- ja myyntitilaus on linkitetty toisiinsa. Näin varmistetaan, että tietty ei-varastoistava nimike poimitaan ja toimitetaan kyseiselle asiakkaalle.  

Ennen kuin tätä ominaisuutta voi käyttää, tilaukselle tarpeelliset asiakas-, myyjä- ja nimikekortit tulee määrittää.  

## <a name="to-create-a-special-order"></a>Erikoistilausten luominen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntitilaus** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto. Luo nimikkeelle  myyntitilaus ja täytä se. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).
3.  Täytä myyntirivi **Rivit**-pikavälilehdessä. Valitse **Ostamisen koodi** -kentässä ostokoodi, jonka **Erikoistilaus**-kenttä on valittuna.

    Luo seuraavaksi ostotilaus hankintalistasta.  
4. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Hankintalista** ja valitse sitten aiheeseen liittyvä linkki.  
5. Valitse ensin **Erikoistilaus**-toiminto ja sitten **Hae myyntitilaukset** -toiminto.  
6.  Näytä **Hae myyntitilaukset** -ikkunassa tulokset, joissa **Asiakirjan nro.** on myyntitilauksen numero. Valitse **OK**-painike. Ohjelma luo nimikkeelle hankintalistan rivin.  
7.  Valitse hankintalistarivin  **Toimenpideviesti**-kentässä **Uusi**.  
8.  Valitse **Hankintalista**-ikkunassa **Toteuta toimenpideviesti** -toiminto. **Toteuta toim.pideviesti - hank** -ikkuna avautuu. Valitse **OK**-painike.  

    Näyttöön tulee ikkuna, jossa ilmoitetaan, että ostotilaukset on luotu. Valitse **OK**-painike.  

Suunnittelujärjestelmä säilyttää myyntitilaukselle erikoistilauksena luodun ostotilauksen, koska se tasapainottaa kysyntää ja tarjontaa. Ostotilaus (tarjonta) pysyy linkitettynä myyntitilaukseen (kysyntään), vaikka ostotilauksella voisi toimittaa toisen aiemman kysynnän. Lisätietoja on kohdassa [Rakennetiedot: Uusintatilauskäytännöt](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Et voi käyttää erikoistilauksen toimintoja, jos nimike on jo varattu. Tämän varmista erikoistilauksina myydyille nimikkeille, että **Varaa**-kenttää nimikkeen kortissa ei ole määritetty arvoon **Aina**.  

## <a name="see-also"></a>Katso myös  
[Ei-varastoitavien nimikkeiden käsitteleminen](inventory-how-work-nonstock-items.md)  
[Myynti](sales-manage-sales.md)  
[Suoratoimitusten tekeminen](sales-how-drop-shipment.md)   
[Rakennetiedot: uusintatilauskäytännöt](design-details-reservation-order-tracking-and-action-messaging.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
