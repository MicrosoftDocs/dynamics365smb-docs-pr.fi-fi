---
title: Ennakkomaksujen korjaaminen
description: Voit tehdä korjauksen tilaukseen sen jälkeen, kun olet kirjannut tilauksesta ennakkomaksulaskun, ja lisätä tilaukseen uusia rivejä ennakkomaksun julkaisun jälkeen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 44, 48, 42, 50, 52, 9305, 9307
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 45bc013c983e4c58d2c4b54dfa074c2170165652
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529674"
---
# <a name="correct-prepayments"></a>Ennakkomaksujen korjaaminen

Joskus sinun on korjattava tilausta ennakkomaksulaskun kirjaamisen jälkeen. Voit lisätä tilaukseen uusia rivejä ennakkomaksun lähettämisen jälkeen ja voit kirjata uuden ennakkomaksulaskun, mutta et voi poistaa riviä tilauksesta sen jälkeen, kun rivin ennakkomaksu on laskutettu.  

> [!TIP]
> Jos myyntilaskun ennakkomaksulasku on kirjattu ja sitä sitten korjataan tai se peruutetaan, myös ennakkomaksu on korjattava tai peruutettava.

## <a name="to-correct-a-prepayment"></a>Ennakkomaksujen korjaaminen

Seuraavaksi kerrotaan, miten kaikki myyntitilauksen laskutetut ennakkomaksut peruutetaan luomalla ennakkomaksun hyvityslasku.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2. Avaa asianomainen myyntitilaus.
3. Valitse ensin **Ennakkomaksu**-toiminto, sitten **Kirjaa ennakkomaksun hyvityslasku**- tai **Kirjaa ja tulosta ennakkomaksun hyvityslasku** -toiminto.  
4. Siirry **Myyntihyvityslasku**-sivulle korjaamaan kyseiset tapahtumat samalla tavoin kuin muissakin myyntihyvityslaskussa. Lisätietoja on kohdassa [Myyntipalautusten tai -peruutusten käsitteleminen](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > **Rivisumma**-kentän summaa voi vähentää kasvattamalla ensin rivin ennakkomaksuprosenttia, jotta **Ennakkomaksun rivisumma** -kentän arvo ei ole pienempi kuin **Laskutettu ennakkomaksun summa** -kentän arvo.

5. Tee ennakkomaksu myyntihyvityslaskun uusille riveille valitsemalla **Ennakkomaksu**-toiminto ja valitsemalla sitten **Kirjaa ennakkomaksulasku**- tai **Kirjaa ja tulosta ennakkomaksulasku** -toiminto.  
6. Voit luoda ylimääräisen ennakkomaksulaskun nostamalla vähintään yhden rivin ennakkomaksua ja kirjaamalla ennakkomaksulaskun. Uusi lasku luodaan ennakkomaksun laskutettujen summien ja uusien ennakkomaksun summien välisen eron vuoksi.  

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Ennakkomaksujen laskuttaminen](finance-invoice-prepayments.md)  
[Vaihekuvaus: Myynnin ennakkomaksujen määrittäminen ja laskuttaminen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Rahoitus](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
