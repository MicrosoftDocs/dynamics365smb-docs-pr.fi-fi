---
title: Toistuvien myyntien ja ostojen vakiorivien määrittäminen | Microsoft Docs
description: Voit määrittää usein käytettäviä myynti- ja ostorivejä. Voit sitten lisätä ne myynti- ja ostoasiakirjoihin ja täyttää tällä tavoin vakiotiedot nopeasti.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 35395ad71dbc0717410ed5a910f5bcd0170b1d8c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "936786"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Toistuvien myynti- ja ostorivien luominen
Jos sinun on usein luotava samankaltaisia tietoja sisältäviä myynti- ja ostorivejä, voit määrittää vakiorivejä ja lisätä ne sitten toistuviin myynti- ja ostoasiakirjoihin, kuten toistuviin täydennystilauksiin.  

Seuraavissa menettelyissä käsitellään myyntilaskun vakiomyyntirivien käyttämistä. Niitä käytetään samalla tavoin kaikissa muissa myyntiasiakirjoissa ja kaikissa ostoasiakirjoissa.  

## <a name="to-set-up-standard-sales-lines"></a>Vakiomyyntirivien määrittäminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vakiomyyntirivit** ja valitse sitten liittyvä linkki.  
2. Valitse **Vakiomyyntirivit**-sivulla **Uusi**-toiminto.  
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Kirjoita **Rivit**-pikavälilehden kenttiin esitiedot, jotka sopivat toistuvina riveinä myyntiasiakirjoissa käytettäviksi vakioriveiksi.  

> [!NOTE]
> Vakiomyyntiriveillä ei voi määrittää hintoja, koska esimerkiksi hinnat ja alennukset lasketaan varsinaisissa myyntiasiakirjoissa vakiomyyntirivien lisäämisen jälkeen.

## <a name="to-assign-standard-sales-lines-to-a-customers"></a>Vakiomyyntikoodien määrittäminen asiakkaille
Määritä asiakkaalle vähintään yksi vakiomyyntirivi, jotta näitä rivejä voidaan liittää kyseisen asiakkaan myyntiasiakirjoihin.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Asiakkaat** ja valitse sitten liittyvä linkki.
2. Avaa soveltuvan asiakkaan kortti.
3. Valitse **Toistuvat myyntirivit** -toiminto.
4. Valitse **Toistuvat myyntirivit** -sivulla niiden toistuvien myyntirivien koodit, joita haluat lisätä asiakkaan myyntiasiakirjoihin.
5. Täytä muut kentät ja määritä, milloin, miten ja missä toistuvia myyntirivejä käytetään. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Toistuvien myyntirivien lisääminen myyntilaskuun
Jos asiakkaalla on toistuvia myyntirivejä, voit lisätä niitä kaikenlaisiin myyntiasiakirjoihin, kuten myyntilaskuun. Jos olet aktivoinut kyseisen ilmoituksen, saat ilmoituksen, jos toistuvia myyntirivejä on.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Laskut** ja valitse sitten liittyvä linkki.
2. Avaa myyntilasku, johon haluat lisätä vähintään yhden vakiomyyntirivin.
3. Valitse **Nouda toistuvat myyntirivit** -toiminto.
4. Valitse **Toistuvat myyntirivit** -sivun **Koodi**-kentässä hakupainike ja valitse sitten vakiomyyntirivijoukko.

    > [!NOTE]
    > Jos haluat käyttää toistuvien myyntirivien joukkoa yhdessä **Luo toistuvia myyntilaskuja** -erätyön avulla, myös **Voimassaolon alkamispäivämäärä**- ja **Voimassaolon päättymispäivämäärä** -kentät on täytettävä **Toistuvat myyntirivit** -sivulla. Lisätietoja on kohdassa [Useiden myyntilaskujen luonti vakiomyyntikoodien perusteella](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-standard-sales-lines).

5. Lisää vakiomyyntirivit laskuun valitsemalla **OK**. Voit sitten käyttää näitä rivejä sellaisenaan tai muokata rivien tietoja.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Useiden myyntilaskujen luonti vakiomyyntirivien perusteella
Voit luoda **Luo toistuvia myyntilaskuja** -eräajolla myyntilaskuja asiakkaille määritettyjen vakiomyyntirivien mukaan siten, että niiden kirjauspäivämäärät ovat vakiomyyntiriveille määritetyllä voimassaolon päivämäärävälillä.

> [!NOTE]
> Voit määrittää **Toistuvat myyntirivit** -sivulla myös suoraveloitusmaksutavan ja suoraveloitusvaltakirjan. Laskut, jotka luodaan **Luo toistuvia myyntilaskuja** -eräajolla, sisältävät tietoja, jotka vaaditaan maksun perimiseen SEPA-suoraveloituksen sisältävistä myyntilaskuista. Lisätietoja on ohjeaiheessa [Maksujen kerääminen SEPA-suoraveloitusperintänä](finance-collect-payments-with-sepa-direct-debit.md).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo toistuvia myyntilaskuja** ja valitse sitten liittyvä linkki.
2. Täytä **Luo toistuvia myyntilaskuja** -sivulla tarvittavat kentät.
3. Anna **Koodi**-suodatinkentässä sille asiakkaalle määritetty vakiomyyntirivien koodi, jolle haluat luoda myyntilaskuja.
4. Valitse **OK**-painike.

Myyntilaskut luodaan asiakkaille, joilla on määrätty asiakkaan vakiomyyntikoodi ja jotkut määritetyt suoraveloitustiedot kirjaamista varten määrättynä päivämääränä.

## <a name="see-also"></a>Katso myös  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
