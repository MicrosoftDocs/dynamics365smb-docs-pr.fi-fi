---
title: Huoltotilausten ja -korjausten tilan määrittäminen | Microsoft Docs
description: Sinun on määritettävä yhdeksän korjauksen tilan vaihtoehtoa, jotka ilmaisevat huoltotilauksissa olevien huoltonimikkeiden korjauksen edistymisen ja ylläpidon.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: 4c28fcfbc2cbc7493ba183812383225754fd3dfa
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389647"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Huoltotilausten ja -korjausten tilan määrittäminen

Sinun on määritettävä korjauksen tilan vaihtoehdot, jotka ilmaisevat huoltotilauksissa olevien huoltonimikkeiden korjauksen edistymisen ja ylläpidon. Sinun on määritettävä vähintään yhdeksän korjauksen tilan vaihtoehtoa, jotka ilmaisevat tilanteet tai suoritettavat toimenpiteet huoltonimikkeiden huoltamisen aikana.  

Voit määrittää huoltotilauksen tilavaihtoehtojen prioriteettitasot. Prioriteetteja on neljä: **Matala**, **Melko matala**, **Melko korkea** ja **Korkea**.  

Kun huoltotilauksessa olevan huoltonimikkeen korjauksen tilaa muutetaan, ohjelma päivittää huoltotilauksen tilan. Kunkin huoltonimikkeen korjauksen tila on linkitetty huoltotilauksen tilaan. Jos huoltonimikkeet on linkitetty kahteen tai useampaan huoltotilauksen tilan vaihtoehtoon, ohjelma valitsee huoltotilauksen tilan, jolla on korkein prioriteetti.  

Ennen kuin voit määrittää korjauksen tilan, sinun on asetettava huollon tilojen prioriteetit.

## <a name="to-set-up-service-status-priorities"></a>Huoltotilan prioriteettien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Huoltotilauksen tila** ja valitse sitten liittyvä linkki.  
2. Valitse huoltotilauksen tila, jolle haluat määrittää prioriteetin.  
3. Valitse **Prioriteetti**-kentässä kyseisen huoltotilauksen tilan prioriteetti.  

Toista työvaiheita 2 ja 3, kunnes kaikille neljälle tilan vaihtoehdolle on määritetty prioriteetti: **Odottava**, **Työn alla**, **Valmis** ja **Estossa**.  

## <a name="to-set-up-a-repair-status"></a>Korjauksen tilan määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Korjauksen tila** ja valitse sitten liittyvä linkki.
2. Luo uusi korjauksen tila.  
3. Täytä **Koodi**- ja **Kuvaus**-kentät.  
4. Valitse **Huoltotilauksen tila** -kentässä tilauksen tila, johon korjaus linkitetään. Valitsemasi huoltotilauksen tilan prioriteetti näkyy **Prioriteetti**-kentässä.  
5. Valitse korjauksen tila. Voit valita vain yhden tilan. Korjauksen tilaa ei voi linkittää useampaan kuin yhteen korjauksen tilan vaihtoehtoon.  
6. Valitse **Kirjaaminen sallittu** -kenttä, jos sallit huoltotilausten, myös huoltonimikkeiden kirjaamisen tämän korjauksen tilan yhteydessä.  
7. Valitse **Odottava-tila sallittu** -valintaruutu, jos haluat sallia, että sellaisten huoltonimikkeitä sisältävän huoltotilauksien tilaksi voidaan manuaalisesti vaihtaa **Odottava**, joiden korjaustila se on.  
8. Valitse **Työn alla -tila sallittu**-, **Valmis-tila sallittu**- ja **Estossa-tila sallittu**-valintaruudut samalla tavoin.

Toista nämä vaiheet jokaisen luotavan korjauksen tilan osalta.

## <a name="see-also"></a>Katso myös

[Huoltotilauksen tila ja korjauksen tila](service-service-order-status-and-repair-status.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]