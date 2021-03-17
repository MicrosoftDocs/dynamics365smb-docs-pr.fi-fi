---
title: Vastaanottojen yhdistäminen | Microsoft Docs
description: Jos haluat laskuttaa useita ostovastaanottoja kerralla, voit käyttää Vastaanottojen yhdistämistoimintoa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 991c244d9e9233067903cfe21fbabcb732293490
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387697"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Vastaanottojen yhdistäminen yhteen laskuun

Jos haluat laskuttaa useita ostovastaanottoja kerralla, voit käyttää **Vastaanottojen yhdistämistoimintoa**.  

Yhdistetyn vastaanoton voi luoda vasta, kun vähintään kaksi saman toimittajan ostokuittia on kirjattu samalla valuutalla. Toisin sanoen vähintään kaksi ostotilausta täytyy olla täytetty ja kirjattu vastaanotetuiksi (mutta ei laskutetuiksi).  

Kun ostovastaanotot yhdistetään laskuun ja kirjataan, askutetuille riveille luodaan kirjattu ostolasku. Alkuperäisen puiteostotilauksen ja/tai ostotilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän mukaan. Tätä alkuperäistä ostoasiakirjaa ei kuitenkaan ole poistettu, vaikka se on kokonaan vastaanotettu ja laskutettu. Sen vuoksi ostoasiakirja on poistettava.  

> [!NOTE]
> Tulokseksi saatavaa ostolaskua ei voi myöhemmin korjata eikä peruuttaa. Jos tällä tavalla luotua ostolaskua halutaan muokata, sitä varten on käytettävä ostohyvityslaskua. Lisätietoja on kohdassa [Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts"></a>Vastaanottojen yhdistäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Ostolaskut** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).  
3. Valitse **Rivit**-pikavälilehdessä **Hae vast.oton rivit** -toiminto.  
4. Valitse useat vastaanoton rivit, jotka haluat sisällyttää laskuun:  

    Jos valitsit väärän vastaanoton rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa rivit ostolaskusta ja suorittaa **Hae vast.oton rivit** -toiminnon uudelleen.  
5. Kirjaa lasku valitsemalla **Kirjaa**-toiminto.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Poista avoin ostotilaus yhdistetyn vastaanoton kirjauksen jälkeen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poista laskutettuja ostotilauksia** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Valitse **OK**-painike.  

Voit myös poistaa manuaalisesti yksittäiset tilaukset.

Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puiteostotilauksissa.

## <a name="see-also"></a>Katso myös

[Osto](purchasing-manage-purchasing.md)  
[Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]