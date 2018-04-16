---
title: "Toistuvien myyntien ja ostojen vakiorivien määrittäminen ja käyttäminen| Microsoft Docs"
description: "Voit määrittää usein käytettäviä myynti- ja ostorivejä. Voit sitten lisätä ne myynti- ja ostoasiakirjoihin ja täyttää tällä tavoin vakiotiedot nopeasti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7c5820db4d8aa65ddeddfd5ee27f0a7e89100abf
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a>Toistuvien myynti- ja ostorivien luominen
Jos sinun on usein luotava samankaltaisia tietoja sisältäviä myynti- ja ostorivejä, voit määrittää vakiorivejä ja lisätä ne sitten toistuviin myynti- ja ostoasiakirjoihin, kuten toistuviin täydennystilauksiin.  

Seuraavassa menettelyssä käsitellään vakiomyyntirivien käyttämistä. Niitä käytetään samalla tavoin kuin vakio-ostorivejä.  

## <a name="to-set-up-standard-sales-lines"></a>Vakiomyyntirivien määrittäminen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Vakiomyyntikoodit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Vakiomyyntirivit** -ikkunassa **Uusi**-toiminto.  
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Kirjoita **Rivit**-pikavälilehden kenttiin esitiedot, jotka sopivat toistuvina riveinä myyntiasiakirjoissa käytettäviksi vakioriveiksi.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Vakiomyyntirivien lisääminen myyntilaskuun
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Vakiomyyntikoodit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa myyntilasku, johon haluat lisätä vähintään yhden vakiomyyntirivin.
3. Valitse **Nouda toistuvat myyntirivit** -toiminto.
4. Valitse **Toistuvat myyntirivit** -ikkunan **Koodi**-kentässä hakupainike ja valitse sitten vakiomyyntirivijoukko.
5. Lisää vakiomyyntirivit laskuun valitsemalla **OK**. Voit sitten käyttää näitä rivejä sellaisenaan tai muokata rivien tietoja.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Useiden myyntilaskujen luonti vakiomyyntirivien perusteella
Voit luoda **Luo toistuvia myyntilaskuja** -eräajolla myyntilaskuja asiakkaille määritettyjen vakiomyyntirivien mukaan siten, että niiden kirjauspäivämäärät ovat vakiomyyntikoodissa määritetyllä voimassaolon päivämäärävälillä.

Voit määrittää **Toistuvat myyntirivit** -ikkunassa myös suoraveloitusmaksutavan ja suoraveloitusvaltakirjan. Laskut, jotka luodaan **Luo toistuvia myyntilaskuja** -eräajolla, sisältävät tietoja, jotka vaaditaan maksun perimiseen SEPA-suoraveloituksen sisältävistä myyntilaskuista. Lisätietoja on kohdassa [SEPA-suoraveloitusmaksujen periminen](finance-collect-payments-with-sepa-direct-debit.md).

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoitta **Luo toistuvia myyntilaskuja** ja valitse sitten aiheeseen liittyvä linkki.
2. Täytä **Luo toistuvia myyntilaskuja** -ikkunassa tarvittavat kentät.
3. Anna **Koodi**-kentässä sille asiakkaalle määritetty vakiomyyntirivien koodi, jolle haluat luoda myyntilaskuja.
4. Valitse **OK**-painike.

Myyntilaskut luodaan asiakkaille, joilla on määrätty asiakkaan vakiomyyntikoodi ja jotkut määritetyt suoraveloitustiedot kirjaamista varten määrättynä päivämääränä.

## <a name="see-also"></a>Katso myös  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

