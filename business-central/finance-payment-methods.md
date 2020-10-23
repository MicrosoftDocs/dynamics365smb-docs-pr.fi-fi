---
title: Maksutapojen määrittäminen | Microsoft Docs
description: Voit määrittää myynti- ja ostolaskuille maksutavan, kuten sekin, pankkisiirron, käteisen tai PayPal-maksun.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: cba54a66815874a3885e038283e8fe9a84b9dd09
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916848"
---
# <a name="defining-payment-methods"></a>Maksutapojen määrittäminen
Maksutavat määrittävät, miten asiakkaiden halutaan ensisijaisesti maksavan ja miten haluat maksaa toimittajille. Maksutapa voi olla asiakas- tai toimittajakohtainen, Tyypillisiä maksutapoja ovat esimerkiksi **pankki**, **käteinen**, **sekki** tai **tili**.

Kun maksutapa määritetään asiakkaille ja toimittajille, heille luotavissa myynti- ja ostoasiakirjoissa käytetään aina samaa maksutapaa. Voit tarvittaessa muuttaa maksutapaa myynti- tai ostoasiakirjassa. Voit tehdä näin esimerkiksi tilanteessa, jossa haluat maksaa tietyn ostolaskun käteisenä sekin sijaan. Tämä muutos ei vaikuta toimittajalle määritettyyn oletusmaksutapaan.

Myynti- ja ostoasiakirjoissa käytetään samaa maksutapaa. Jos maksutavaksi on määritetty _käteinen_, sitä käytetään sekä maksuja maksettaessa että niitä vastaanotettaessa. [!INCLUDE[d365fin](includes/d365fin_md.md)] tietää, että odotat myyntilaskua luodessasi vastaanottavasi maksun ja päin vastoin ostolaskuja luotaessa.

Palautusten hyvityslaskut ovat kuitenkin poikkeuksia, sillä rahavirrat kulkevat vastakkaisiin suuntiin eli sinulta asiakkaalle ja toimittajalta sinulle. Tämän vuoksi hyvityslaskuille ei määritetä oletusmaksutapaa. Tämän voi kuitenkin kiertää, jos olet määrittänyt asiakkaalle tai toimittajalle maksuehdot. Vaikka **Laske maksualen. hyvityslask.** -kenttää ei ole tarkoitettu tähän tarkoitukseen, tämän valintaruudun valitseminen **Maksuehdot**-sivulla lisää oletusmaksutavan hyvityslaskua luotaessa. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a>Maksutapojen määrittäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] sisältää muutamia yritysten usein käyttämiä maksutapoja. Voit kuitenkin lisätä niitä tarvittavan määrän.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Maksutavat** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Maksutavan määrittely asiakkaalle tai toimittajalle
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten liittyvä linkki.
2. Valitse **Maksutavan koodi** -kentässä menetelmä, jota käytetään oletusarvoisesti asiakkaalle tai toimittajalle.

## <a name="see-also"></a>Katso myös
[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
