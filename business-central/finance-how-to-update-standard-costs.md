---
title: Vakiokustannusten päivittäminen
description: Komponenttien vakiokustannukset on päivitettävä säännöllisesti ja uudet kustannukset on vyörytettävä päänimikkeelle.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4bada4ee28df77cc9700d5957ef8fb8b1a64535b
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8517444"
---
# <a name="update-standard-costs"></a>Vakiokustannusten päivittäminen
Komponenttien vakiokustannukset on päivitettävä säännöllisesti ja uudet kustannukset on vyörytettävä päänimikkeelle. Prosessi sisältää yleensä seuraavat neljä vaihetta:  

1.  Päivitä kustannukset osa- ja kapasiteettitasolla. Lisätietoja on kohdassa **Ehdota nimikkeen vakiokust.** -eräajo.  
2.  Yhdistä ja kokoa osa- ja kapasiteettikustannukset laskeaksesi nimikkeiden tuotannon tai kokoonpanon kokonaiskustannuksen.  
3.  Ota käyttöön edellisten eräajojen aikana syötetyt vakiokustannukset. Vakiokustannukset eivät tule voimaan, ennen kuin ne on otettu käyttöön. Käytä **Ota käyttöön vakiokustannusten muutokset** -erätyötä, joka päivittää nimikkeiden vakiokustannusten muutokset Vakiokustannustyökirja-taulukossa.  
4.  Ota muutokset käyttöön nimikkeen kortin **Yksikkökustannus**-kentän päivittämistä ja varaston uudelleenarvostuksen suorittamista varten. Lisätietoja on kohdassa [Varaston uudelleenarvostus](inventory-how-revalue-inventory.md).  

Lisätietoja on kohdassa [Tietoja vakiokustannusten laskennasta](finance-about-calculating-standard-cost.md).
  
## <a name="to-update-standard-costs"></a>Vakiokustannusten päivittäminen

1.  Suorita **Muuta kustannuksia - Nimiketapahtumat** -eräajo.  
2.  Suorita **Kirjaa varaston kust. KP:oon** -eräajo.  
3.  Avaa **Vakiokust. työkirja** ja käytä vähintään yhtä seuraavista toiminnoista:  

    1.  Suorita **Ehdota nimikkeen vakiokust.** -eräajo.  
    2.  Tarkasta tulokset ja tee tarvittavat muutokset.  
    3.  Suorita **Ehdota kapasiteetin vakiokustannusta** -eräajo.  
    4.  Tarkasta tulokset ja tee tarvittavat muutokset.
    5. Suorita **Vyörytä vakiokustannus** -eräajo.
    6.  Tarkasta tulokset ja tee tarvittavat muutokset.
    7.  Suorita **Ota käyttöön vakiokustannusten muutokset** -eräajo.  
4.  Tarkasta ja kirjaa **Uudelleenarvostus pvk** -sivu, jonka tapahtumat on täytetty tämän prosessin aiemmissa vaiheissa.  

## <a name="see-also"></a>Katso myös

 [Tietoja standardikustannuksen laskemisesta](finance-about-calculating-standard-cost.md)   
 [Varaston kustannusten hallinta](finance-manage-inventory-costs.md)   
 [Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md) [Rahoitus](finance.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]