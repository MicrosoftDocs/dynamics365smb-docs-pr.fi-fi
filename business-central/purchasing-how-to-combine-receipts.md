---
title: Vastaanottojen yhdistäminen yhteen laskuun
description: Jos haluat laskuttaa useita ostovastaanottoja kerralla, voit käyttää Vastaanottojen yhdistämistoimintoa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 136, 145, 146, 9308
ms.date: 08/03/2022
ms.author: edupont
ms.openlocfilehash: 10543531b6ffc7d7543ae768a2410379e75b6c80
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227389"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Vastaanottojen yhdistäminen yhteen laskuun

Jos haluat laskuttaa useita ostokuitteja kerralla, voit valita useita vastaanottorivejä ostoslaskussa.  

Yhdistetyn vastaanoton voi luoda vasta, kun vähintään kaksi saman toimittajan ostokuittia on kirjattu samalla valuutalla. Toisin sanoen vähintään kaksi ostotilausta täytyy olla täytetty ja kirjattu vastaanotetuiksi (mutta ei laskutetuiksi).  

Kun ostovastaanotot yhdistetään laskuun ja kirjataan, askutetuille riveille luodaan kirjattu ostolasku. Alkuperäisen puiteostotilauksen ja/tai ostotilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän mukaan. Tätä alkuperäistä ostoasiakirjaa ei kuitenkaan ole poistettu, vaikka se on kokonaan vastaanotettu ja laskutettu. Sen vuoksi ostoasiakirja on poistettava.  

> [!NOTE]
> Tulokseksi saatavaa ostolaskua ei voi myöhemmin korjata eikä peruuttaa. Jos tällä tavalla luotua ostolaskua halutaan muokata, sitä varten on käytettävä ostohyvityslaskua. Lisätietoja on kohdassa [Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts"></a>Vastaanottojen yhdistäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).  
3. Valitse **Rivit**-pikavälilehdessä **Hae vast.oton rivit** -toiminto.  
4. Valitse useat vastaanoton rivit, jotka haluat sisällyttää laskuun:  

    Jos valitsit väärän vastaanoton rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa rivit ostolaskusta ja suorittaa **Hae vast.oton rivit** -toiminnon uudelleen.  
5. Kirjaa lasku valitsemalla **Kirjaa**-toiminto.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Poista avoin ostotilaus yhdistetyn vastaanoton kirjauksen jälkeen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista laskutetut ostotilaukset** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Valitse **OK**-painike.  

Voit myös poistaa manuaalisesti yksittäiset tilaukset.

Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puiteostotilauksissa.

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/processing-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Osto](purchasing-manage-purchasing.md)  
[Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]