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
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245683"
---
# <a name="view-the-status-of-a-synchronization"></a>Synkronoinnin tilan näyttäminen
Voit tarkastella sellaisten yksittäisten synkronointitöiden tilaa, jotka on suoritettu [!INCLUDE[crm_md](includes/crm_md.md)] -integrointia varten. Tämä sisältää synkronointityöt, jotka on suoritettu työjonosta, ja manuaaliset synkronointityöt, jotka on suoritettu [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueista. Tästä on hyötyä synkronointiongelmien vianmäärityksessä, koska sen avulla saat tietoja yksittäisistä virheistä.

### <a name="to-view-all-synchronization-issues"></a>Kaikkien synkronointiongelmien näyttäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Yhdistettyjen tietojen synkronointivirheet** ja valitse sitten liittyvä linkki.
2. Voit tarkastella **Yhdistettyjen tietojen synkronointivirheet** -sivulla kaikki ongelmia, joita tapahtui synkronoitaessa tietoja [!INCLUDE[crm_md](includes/crm_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in välillä, suodattaa ja lajitella sivulla olevia tietoja taulukon ja virhesanoman mukaan sekä ratkaista ongelmia yksitellen tai joukkotoiminnolla esimerkiksi **Yritä uudelleen**- tai **Poista yhdistäminen** -toiminnolla.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Tietyn (manuaalisesti synkronoidun) tietueen synkronointilokin näyttäminen
1. Avaa esimerkiksi asiakas-, nimike- tai muu tietue, joka synkronoi tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja Salesin välillä.
2. Valitse **Synkronointiloki**-toiminto, jos haluat tarkastella valitun tietueen synkronointilokia. Kyse voi olla esimerkiksi tietystä manuaalisesti synkronoidusta asiakkaasta.

## <a name="see-also"></a>Katso myös  
[Dynamics 365 for Sales -integroinnin määrittäminen Business Centralissa](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 for Salesin käyttö Business Centralista](marketing-integrate-dynamicscrm.md)
