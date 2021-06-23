---
title: Tuotantotilausten luominen myyntitilauksista
description: Tuotantotilauksia voi luoda myyntitilauksista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115234"
---
# <a name="create-production-orders-from-sales-orders"></a>Tuotantotilausten luominen myyntitilauksista
Voit luoda tuotettujen nimikkeiden tuotantotilaukset suodaan myyntitilauksista.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Tuotantotilausten luominen myyntitilauksista  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitilaukset** ja valitse sitten liittyvä linkki.  
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
