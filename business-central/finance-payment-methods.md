---
title: Maksutapojen määrittäminen
description: Voit määrittää myynti- ja ostolaskuille maksutavan, kuten sekin, pankkisiirron, käteisen tai PayPal-maksun.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 1e836b43392cd915a77c5ee85d5a322753dcd5df
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773953"
---
# <a name="set-up-payment-methods"></a>Maksutapojen määrittäminen

Maksutavat määrittävät, miten asiakkaiden halutaan ensisijaisesti maksavan ja miten haluat maksaa toimittajille. Maksutapa voi olla asiakas- tai toimittajakohtainen, Tyypillisiä maksutapoja ovat esimerkiksi **pankki**, **käteinen**, **sekki** tai **tili**.

Kun maksutapa määritetään asiakkaille ja toimittajille, heille luotavissa myynti- ja ostoasiakirjoissa käytetään aina samaa maksutapaa. Voit tarvittaessa muuttaa maksutapaa myynti- tai ostoasiakirjassa. Voit tehdä näin esimerkiksi tilanteessa, jossa haluat maksaa tietyn ostolaskun käteisenä sekin sijaan. Tämä muutos ei vaikuta toimittajalle määritettyyn oletusmaksutapaan.

Myynti- ja ostoasiakirjoissa käytetään samaa maksutapaa. Jos maksutavaksi on määritetty _käteinen_, sitä käytetään sekä maksuja maksettaessa että niitä vastaanotettaessa. [!INCLUDE[prod_short](includes/prod_short.md)] tietää, että odotat myyntilaskua luodessasi vastaanottavasi maksun ja päin vastoin ostolaskuja luotaessa.

Palautusten hyvityslaskut ovat kuitenkin poikkeuksia, sillä rahavirrat kulkevat vastakkaisiin suuntiin eli sinulta asiakkaalle ja toimittajalta sinulle. Tämän vuoksi hyvityslaskuille ei määritetä oletusmaksutapaa. Tämän voi kuitenkin kiertää, jos olet määrittänyt asiakkaalle tai toimittajalle maksuehdot. Vaikka **Laske maksualen. hyvityslask.** -kenttää ei ole tarkoitettu tähän tarkoitukseen, tämän valintaruudun valitseminen **Maksuehdot**-sivulla lisää oletusmaksutavan hyvityslaskua luotaessa. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a>Maksutapojen määrittäminen

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää muutamia yritysten usein käyttämiä maksutapoja. Voit kuitenkin lisätä niitä tarvittavan määrän.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Maksutavat** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Vaihtoehtoisesti voit lisätä maksuehdot maksutapaan. Lisätietoja on ohjeaiheessa [Maksuehtojen määrittäminen](finance-payment-terms.md).  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Maksutavan määrittely asiakkaalle tai toimittajalle

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** tai **Toimittaja** ja valitse sitten liittyvä linkki.
2. Valitse **Maksutavan koodi** -kentässä menetelmä, jota käytetään oletusarvoisesti asiakkaalle tai toimittajalle.

## <a name="see-also"></a>Katso myös

[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)  
[Maksuehtojen määrittäminen](finance-payment-terms.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]