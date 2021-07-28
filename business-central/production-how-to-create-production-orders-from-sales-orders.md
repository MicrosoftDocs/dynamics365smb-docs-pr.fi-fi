---
title: Tuotantotilausten luominen myyntitilauksista
description: Tietoja eri tavoista, joiden avulla voit luoda tuotettujen nimikkeiden tuotantotilaukset suodaan myyntitilauksista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: a432b8f00a24771578716a1b51678904d2e29ec5
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438625"
---
# <a name="create-production-orders-from-sales-orders"></a>Tuotantotilausten luominen myyntitilauksista
Voit luoda tuotettujen nimikkeiden tuotantotilaukset suodaan myyntitilauksista.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Tuotantotilausten luominen myyntitilauksista  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.  
2.  Valitse myyntitilaus, jolle haluat luoda tuotantotilauksen.  
3.  Valitse **Suunnittelu**-toiminto. **Myyntitilaus suunnittelu** -sivulla voi tarkastella myyntitilausnimikkeen saatavuutta.  
4.  Valitse **Luo tuotantotilaus** -toiminto.  
5.  Valitse tila ja tilaustyyppi.  
6.  Valitse **Kyllä** -painike luodaksesi yhden tai useamman tuotantotilauksen niiden rivien osalta, joilla on **Tuotantotilaus** **Täydennysjärjestelmä**-kentässään.


> [!NOTE]  
> Luodun tuotantotilauksen kysyntärivit, joilla on **Tuotantotilaus** niiden **Täydennysjärjestelmä** -kentässä, edustavat perustana olevia tuotantotilauksia.. Kun olet luonut nämä tuotantotilaukset, muista tunnistaa kaikki niihin kohdistuvat täyttämättömät komponenttivaatimukset käyttämällä **Tilauksen suunnittelu** -sivua tai **Uudelleensuunnittele**-toimintoa luoduista tilauksista. 

## <a name="order-type"></a>Tilaustyyppi  
Voit valita kahdesta eri tavasta luoda tuotantotilaukset seuraavassa taulukossa kuvatulla tavalla.

|Asetus|Kuvaus|
|------|-----------|
|Nimiketilaus|Yksi tuotantotilaus luodaan kutakin tarvittavaa tuotantotilausta varten. Sitä edustaa rivi **Myyntitilauksen suunnittelu** -ikkunassa.|
|Projektitilaus|Yksi tuotantotilaus luodaan kaikkia tarvittavia tuotantotilauksia varten. Niitä edustavat rivit **Myyntitilauksen suunnittelu** -ikkunassa. |

Kun käytät projektitilauksia, tuotantotilauksen **Lähdetyyppi**-kentässä on **Myynnin tunnistetiedot** ja tilauksessa on useita rivejä, yksi jokaista tuotettavaa myyntirivinimikettä kohden.  


## <a name="see-also"></a>Katso myös  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
[Asetukset - parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
