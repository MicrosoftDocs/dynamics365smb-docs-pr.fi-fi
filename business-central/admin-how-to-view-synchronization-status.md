---
title: Synkronointitöiden tilan näyttäminen | Microsoft Docs
description: Lisätietoja tilan näyttämisestä yhdistettyjen tietueiden synkronoinnin jälkeen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 022e364b6a40fe8df1f9c4e3425030d35f729e6a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304490"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Synkronointitöiden tilan näyttäminen
Käytä **Yhdistettyjen tietojen synkronointivirheet** -sivua, kun haluat näyttää niiden synkronointitöiden tilan, jotka on suoritettu yhdistetyille tietueille [!INCLUDE[crm_md](includes/crm_md.md)] -integroinnissa. Tämä sisältää työt, jotka on suoritettu työjonosta, ja manuaaliset synkronointityöt, jotka on suoritettu [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietueista. Näiden tilan näyttäminen on hyödyllistä esimerkiksi vianmäärityksen yhteydessä, koska tällöin saat tietoja yhdistettyihin tietueisiin liittyvistä virheistä. Yleensä tällaiset virheet johtuvat käyttäjän toiminnoista. Näitä ovat esimerkiksi seuraavat:  

* Kaksi henkilö tekee muutoksia samaan tietueeseen kummassakin liiketoimintasovelluksessa.
* Joku poisti tietueen yhdestä sovelluksesta, ei molemmista.

> [!Note]
> **Yhdistettyjen tietojen synkronointivirheet** -sivulla näkyvät yhdistettyjen tietueiden töihin liittyvät tiedot. Jos ratkaiset kaikki virheet, mutta tietueita ei silti synkronoida, syy voi olla integroinnin asetuksissa. Järjestelmänvalvojan on yleensä ratkaistava tämäntyyppiset virheet.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Yhdistettyjen tietueiden synkronointivirheiden tarkasteleminen ja ratkaiseminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Yhdistettyjen tietojen synkronointivirheet** ja valitse sitten liittyvä linkki.
2. **Yhdistettyjen Tietojen Synkrnoiniti Virheet** esittää ongelmat jotka tapahtuivat yhdistetyjen tietuiden synkronoinnissa. Seuraavassa taulukossa on toimintoja, joiden avulla voit ratkaista ongelmia yksi kerrallaan.

|Toiminto|Kuvaus|
|----|----|
|**Poista yhdistäminen**|Poistaa tietueiden yhdistämisen. Tämän jälkeen niitä ei enää synkronoida keskenään. Jos haluat jatkaa tietueiden synkronointia, tietueet on yhdistettävä uudelleen.|
|**Yritä uudelleen**|Jos tietueesta löytyy virhe, sen synkronointi ohitetaan, kunnes ongelma korjataan manuaalisesti. Uudelleenyritys sisällyttää tietueen seuraavaan synkronointiin.|
|**Synkronoi**|Sovellus yrittää ratkaista ristiriidan, jossa tietuetta on muutettu kummassakin liiketoimintasovelluksessa. Voit valita kummassakin sovelluksessa käytettävän tietueen version.|
|**Palauta tietueet** ja **Poista tietueet**|Nämä ovat hyödyllisiä silloin, kun tietue on poistettu jommassakummassa sovelluksessa. Poista tietueet -vaihtoehto poistaa tietueen sovelluksesta, jossa se vielä on. Palautusvaihtoehto luo tietueen uudelleen sovellukseen, josta se poistettiin.|

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Tietyn (manuaalisesti synkronoidun) tietueen synkronointilokin näyttäminen
1. Voit esimerkiksi avata asiakkaan, nimikkeen tai minkä tahansa muun tietoja sovellusten [!INCLUDE[d365fin](includes/d365fin_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] välillä synkronoivan tietueen.
2. Valitse **Synkronointiloki** toimenpide tarkastellaksesi valitun tietueen synkronointilokia. Esimerkiksi tiettyä asiakasta jonka synkronoit manuaalisesti.

## <a name="see-also"></a>Katso myös  
[Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 Salesin käyttäminen Business Centralissa](marketing-integrate-dynamicscrm.md)
