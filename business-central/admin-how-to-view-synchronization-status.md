---
title: Synkronointitöiden tilan näyttäminen | Microsoft Docs
description: Lisätietoja tilan näyttämisestä yhdistettyjen tietueiden synkronoinnin jälkeen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: a54ce7805deafa5d67c3e25b89606a1a40634ad6
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378146"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Synkronointitöiden tilan näyttäminen
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Käytä **Yhdistettyjen tietojen synkronointivirheet** -sivua, kun haluat näyttää niiden synkronointitöiden tilan, jotka on suoritettu yhdistetyille tietueille Dataverse- tai [!INCLUDE[crm_md](includes/crm_md.md)] -integroinneissa. Tämä sisältää työt, jotka on suoritettu työjonosta, ja manuaaliset synkronointityöt, jotka on suoritettu [!INCLUDE[prod_short](includes/prod_short.md)] -tietueista. Näiden tilan näyttäminen on hyödyllistä esimerkiksi vianmäärityksen yhteydessä, koska tällöin saat tietoja yhdistettyihin tietueisiin liittyvistä virheistä. Yleensä tällaiset virheet johtuvat käyttäjän toiminnoista. Näitä ovat esimerkiksi seuraavat:  

* Kaksi henkilö tekee muutoksia samaan tietoon kummassakin liiketoimintasovelluksessa.
* Joku poisti tiedon yhdestä sovelluksesta, ei molemmista.

> [!Note]
> **Yhdistettyjen tietojen synkronointivirheet** -sivulla näkyvät yhdistettyjen tietueiden töihin liittyvät tiedot. Jos ratkaiset kaikki virheet, mutta tietueita ei silti synkronoida, syy voi olla integroinnin asetuksissa. Järjestelmänvalvojan on yleensä ratkaistava tämäntyyppiset virheet.   

<!--

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

-->

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Yhdistettyjen tietueiden synkronointivirheiden tarkasteleminen ja ratkaiseminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yhdistettyjen tietojen synkronointivirheet** ja valitse sitten liittyvä linkki.
2. **Yhdistettyjen Tietojen Synkrnoiniti Virheet** esittää ongelmat jotka tapahtuivat yhdistetyjen tietuiden synkronoinnissa. Seuraavassa taulukossa on toimintoja, joiden avulla voit ratkaista ongelmia yksi kerrallaan.

|Toiminto|Kuvaus|
|----|----|
|**Poista yhdistäminen**|Poistaa tietueiden yhdistämisen. Tämän jälkeen niitä ei enää synkronoida keskenään. Jos haluat käynnistää synkronoinnin uudelleen, tietueet on yhdistettävä uudelleen. |
|**Yritä uudelleen** ja **Yritä kaikki uudelleen**|Jos tietueesta löytyy virhe, sen synkronointi ohitetaan, kunnes ongelma korjataan. Yritä sisällyttää seuraava tietue seuraavaan synkronointiin ja **Yritä kaikkia uudelleen** sisältää kaikki tietueet.|
|**Synkronoi**|Sovellus yrittää ratkaista ristiriidan, jossa tietoa on muutettu kummassakin liiketoimintasovelluksessa. Voit valita käytettävän tiedon.|
|**Palauta tietueet** ja **Poista tietueet**|Nämä ovat hyödyllisiä silloin, kun tietue on poistettu jommassakummassa yrityssovelluksessa. Poista tietueet -vaihtoehto poistaa tietueen tai rivin sovelluksesta, jossa se vielä on. Palauta tietueet -vaihtoehto luo tietueen tai rivin uudelleen yrityssovellukseen, josta se poistettiin.|

> [!NOTE]
> Jotta ratkaistavana olevien ristiriitojen määrä vähenisi, voit määrittää integrointitaulukon yhdistämismääritykset, jotta nämä toiminnot ovat automaattisesti käytössä. Lisätietoja on kohdassa [Integrointitaulukoiden yhdistäminen](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Tietyn (manuaalisesti synkronoidun) tietueen synkronointilokin näyttäminen
1. Voit esimerkiksi avata asiakkaan, nimikkeen tai minkä tahansa muun tietoja [!INCLUDE[prod_short](includes/prod_short.md)]- ja Dataverse- tai [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksen välillä synkronoivan tietueen.
2. Valitse **Synkronointiloki** toimenpide tarkastellaksesi valitun tietueen synkronointilokia. Esimerkiksi tiettyä asiakasta jonka synkronoit manuaalisesti.

## <a name="see-also"></a>Katso myös  
[Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 Salesin käyttäminen Business Centralissa](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]