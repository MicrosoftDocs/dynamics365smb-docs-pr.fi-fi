---
title: Synkronoinnin tilan näyttäminen | Microsoft Docs
description: Lisätietoja yksittäisen synkronointityö tilan näyttämisestä.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620882"
---
# <a name="view-the-status-of-a-synchronization"></a>Synkronoinnin tilan näyttäminen
Voit tarkastella sellaisten yksittäisten synkronointitöiden tilaa, jotka on suoritettu [!INCLUDE[crm_md](includes/crm_md.md)] -integrointia varten. Tämä sisältää synkronointityöt, jotka on suoritettu työjonosta, ja manuaaliset synkronointityöt, jotka on suoritettu [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueista. Tästä on hyötyä synkronointiongelmien vianmäärityksessä, koska sen avulla saat tietoja yksittäisistä virheistä.

### <a name="to-view-synchronization-issues-for-coupled-records"></a>Tarkastellaksesi synkronisaatio-ongelmia yhdistetyille tietuielle
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Yhdistettyjen tietojen synkronointivirheet** ja valitse sitten liittyvä linkki.
2. **Yhdistettyjen Tietojen Synkrnoiniti Virheet** esittää ongelmat jotka tapahtuivat yhdistetyjen tietuiden synkronoinnissa. Voit suodattaa ja lajitella tietueita ja suorittaa toimintoja kuten **Palauta** tai **Poistat Tietue** ratkaistaksesi ongelmat yksi kerrallaan.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Tietyn (manuaalisesti synkronoidun) tietueen synkronointilokin näyttäminen
1. Esimerkiksi, voit avata asiakkaan, esineen tai minkä tahansa muun tietueen joka synkronisoi tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)] ja Salesin välillä.
2. Valitse **Synkronointiloki** toimenpide tarkastellaksesi valitun tietueen synkronointilokia. Esimerkiksi tiettyä asiakasta jonka synkronoit manuaalisesti.

## <a name="see-also"></a>Katso myös  
[Dynamics 365 for Sales -integroinnin määrittäminen Business Centralissa](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 for Salesin käyttö Business Centralista](marketing-integrate-dynamicscrm.md)
