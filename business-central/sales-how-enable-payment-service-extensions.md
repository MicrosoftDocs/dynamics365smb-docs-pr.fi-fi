---
title: Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta | Microsoft Docs
description: Kun otat maksupalvelut käyttöön, asiakkaiden on helpompi maksaa laskunsa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7bd02b7d802faa3b0766d6689eaa223ba3e3573a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316450"
---
# <a name="enable-customer-payments-through-payment-services"></a>Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta
Pankkisiirron tai luottokorttien lisäksi asiakkaat voivat maksaa sinulle maksupalvelutilin, kuten Microsoft Payn, PayPalin tai WorldPayn, avulla.  

Kun olet ottanut maksupalvelun käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, palvelun linkki on käytössä sähköpostitse asiakkaille lähetettävissä myyntiasiakirjoissa. Asiakkaat voivat siirtyä linkin kautta maksupalveluun ja maksaa laskun suoraan myyntiasiakirjasta. Jos et halua lisätä linkkiä esimerkiksi silloin, kun asiakas maksaa käteisellä, voit poistaa maksupalvelun laskusta ennen kirjaamista.  

Microsoft Pay, PayPal Payments Standard- ja WorldPay Payments Standard -laajennukset on asennettu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, ja ne odottavat käyttöönottoa.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365fin_mdmd"></a>Maksupalvelun ottaminen käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksupalvelut** ja valitse sitten liittyvä linkki.  
2. Valitse **Maksupalvelut**-sivulla **Uusi**-toiminto.  
3. Valitse maksupalvelu ja sulje sitten sivu.  
4. Valitse **Maksupalvelut**-sivulla **Määritys**-toiminto.  
5. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Sulje sivu.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Maksupalvelun valitseminen myyntilaskussa
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.  
2. Avaa myyntilasku, jonka haluat maksaa maksupalvelun avulla.  
3. Valitse maksupalvelu **Maksupalvelu**-kentässä.  

    > [!NOTE]  
    > **Maksupalvelu**-kenttä on käytettävissä vain, jos olet ottanut maksupalvelun käyttöön.  

## <a name="see-also"></a>Katso myös  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
