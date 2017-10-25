---
title: "Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta | Microsoft Docs"
description: "Kun otat maksupalvelut käyttöön, asiakkaiden on helpompi maksaa laskunsa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c149949b939a551a14236c84f8ba7538fcb54bbe
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-customer-payments-through-payment-services"></a>Toimintaohje: Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta
Pankkisiirron tai luottokorttien lisäksi asiakkaat voivat maksaa sinulle maksupalvelutilin, kuten Microsoft Payn, PayPalin tai WorldPayn, avulla.  

Kun olet ottanut maksupalvelun käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, palvelun linkki on käytössä sähköpostitse asiakkaille lähetettävissä myyntiasiakirjoissa. Asiakkaat voivat siirtyä linkin kautta maksupalveluun ja maksaa laskun suoraan myyntiasiakirjasta. Jos et halua lisätä linkkiä esimerkiksi silloin, kun asiakas maksaa käteisellä, voit poistaa maksupalvelun laskusta ennen kirjaamista.  

Microsoft Pay, PayPal Payments Standard- ja WorldPay Payments Standard -laajennukset on asennettu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, ja ne odottavat käyttöönottoa.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Maksupalvelun ottaminen käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupalvelut** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Maksupalvelut**-ikkunassa **Uusi**-toiminto.  
3. Valitse maksupalvelu ja sulje sitten ikkuna.  
4. Valitse **Maksupalvelut**-ikkunassa **Asetus**-toiminto.  
5. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Sulje ikkuna.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Maksupalvelun valitseminen myyntilaskussa
1. Valitse kotisivun **Myyntilaskut**-kohta.  
2. Avaa myyntilasku, jonka haluat maksaa maksupalvelun avulla.  
3. Valitse maksupalvelu **Maksupalvelu**-kentässä.  

    > [!NOTE]  
>   **Maksupalvelu**-kenttä on käytettävissä vain, jos olet ottanut maksupalvelun käyttöön.  

## <a name="see-also"></a>Katso myös  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

