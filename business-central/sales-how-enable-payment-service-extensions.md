---
title: Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta
description: Kun otat asiakkaiden maksuille maksupalvelut käyttöön, asiakkaiden on helpompi maksaa laskunsa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.search.forms: 1060, 1061, 1062
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 7dad5bcdc5f3c98364bffc81787639e1f3ff11d2
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9074405"
---
# <a name="enable-customer-payments-through-payment-services"></a>Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta

Pankkisiirron tai luottokorttien lisäksi asiakkaat voivat maksaa sinulle maksupalvelutilin, kuten PayPalin tai WorldPayn, avulla.  

Kun olet ottanut maksupalvelun käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]issa, palvelun linkki on käytössä sähköpostitse asiakkaille lähetettävissä myyntiasiakirjoissa. Asiakkaat voivat siirtyä linkin kautta maksupalveluun ja maksaa laskun suoraan myyntiasiakirjasta. Jos et halua lisätä linkkiä esimerkiksi silloin, kun asiakas maksaa käteisellä, voit poistaa maksupalvelun laskusta ennen kirjaamista.  

PayPal Payments Standard- ja WorldPay Payments Standard -laajennukset ovat asennettuina [!INCLUDE[prod_short](includes/prod_short.md)]iin, ja ne ovat valiina otettaviksi käyttöön.  

## <a name="to-enable-a-payment-service-in-prod_short"></a>Maksupalvelun ottaminen käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]issa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupalvelut** ja valitse sitten vastaava linkki.  
2. Valitse **Maksupalvelut**-sivulla **Uusi**-toiminto.  
3. Valitse maksupalvelu ja sulje sitten sivu.  
4. Valitse **Maksupalvelut**-sivulla **Määritys**-toiminto.  
5. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Sulje sivu.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Maksupalvelun valitseminen myyntilaskussa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.  
2. Avaa myyntilasku, jonka haluat maksaa maksupalvelun avulla.  
3. Valitse maksupalvelu **Maksupalvelu**-kentässä.  

    > [!NOTE]  
    > **Maksupalvelu**-kenttä on käytettävissä vain, jos olet ottanut maksupalvelun käyttöön.  

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]