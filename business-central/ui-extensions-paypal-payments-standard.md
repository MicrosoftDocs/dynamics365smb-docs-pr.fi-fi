---
title: PayPal Payments Standard -laajennuksen käyttäminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten laajennusten avulla asiakkaille voidaan antaa mahdollisuus suorittaa PayPal-maksuja.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f715108b17d355084fee7983e106cd33dd476906
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249765"
---
# <a name="the-paypal-payments-standard-extension"></a>PayPal Payments Standard -laajennus
Asiakkaat vaativat jatkuvasti yhä korkeatasoisempaa asiakaspalvelua sekä tuotteen laadun että toimitus- ja maksuvaihtoehtojen osalta. Voit parantaa asiakaspalvelun tasoa PayPal Payments Standard -palvelun avulla.

Pankkisiirron tai luottokorttien lisäksi asiakkaille voi tarjota mahdollisuuden maksaa PayPal-tilin avulla. Kun lähetät myyntilaskun tai -tilauksen sähköpostitse, sähköpostin perustekstissä ja liitetyssä PDF-tiedostossa on PayPal-linkki. Kun asiakas valitsee PayPal-linkin, näyttöön avautuu asiakkaan PayPal-tilin palvelusivu, joka sisältää myyntiä koskevat maksutiedot. Tämän jälkeen asiakas voi maksaa laskun kuten minkä tahansa PayPal-maksun.

PayPal Payments Standard -palvelusta on apua seuraavissa asioissa:

* asiakkaan maksut saapuvat nopeammin pankkitilillesi
* asiakkailla on useita vaihtoehtoja maksaa laskut.
* PayPal on luotettava maksupalvelu. Asiakkaat käyttävät PayPalia mieluummin kuin syöttävät luottokorttitietonsa verkkosivulle.
* PayPalin avulla maksuja voi käsitellä useilla eri tavoilla. Niitä ovat luottokorttikäsittely, PayPal-tilit ja muut lähteet.
* PayPal-linkki voidaan lisätä automaattisesti myyntiasiakirjoihin. Myös käyttäjä voi lisätä linkin.
* PayPal Payments Standard -palvelu ei sisällä kuukausi- tai aloitusmaksuja.
* Koska palvelu on laajennus, voit ottaa PayPal Payment Standard -palvelun helposti käyttöön silloin, kun yritys tarvitsee sitä.  

Lisätietoja on kohdassa [Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md).

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
