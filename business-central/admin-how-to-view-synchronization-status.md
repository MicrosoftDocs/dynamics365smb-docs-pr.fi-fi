---
title: Synkronointitöiden tilan näyttäminen (sisältää videon)
description: Käytä Yhdistettyjen tietojen synkronointivirheet -sivua, kun haluat näyttää niiden synkronointitöiden tilan, jotka on suoritettu yhdistetyille tietueille integroinneissa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.search.form: 6250
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: c98cadba0a9bdf21a89a6c50dd61d805f0547685
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521252"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Synkronointitöiden tilan näyttäminen


Käytä **Yhdistettyjen tietojen synkronointivirheet** -sivua, kun haluat näyttää niiden synkronointitöiden tilan, jotka on suoritettu yhdistetyille tietueille Dataverse- tai [!INCLUDE[crm_md](includes/crm_md.md)] -integroinneissa. Tämä sisältää työt, jotka on suoritettu työjonosta, ja manuaaliset synkronointityöt, jotka on suoritettu [!INCLUDE[prod_short](includes/prod_short.md)] -tietueista. Näiden tilan näyttäminen on hyödyllistä esimerkiksi vianmäärityksen yhteydessä, koska tällöin saat tietoja yhdistettyihin tietueisiin liittyvistä virheistä. Yleensä tällaiset virheet johtuvat käyttäjän toiminnoista. Näitä ovat esimerkiksi seuraavat:  

* Kaksi henkilö tekee muutoksia samaan tietoon kummassakin liiketoimintasovelluksessa.
* Joku poisti tiedon yhdestä sovelluksesta, ei molemmista.

> [!Note]
> **Yhdistettyjen tietojen synkronointivirheet** -sivulla näkyvät yhdistettyjen tietueiden töihin liittyvät tiedot. Jos ratkaiset kaikki virheet, mutta tietueita ei silti synkronoida, syy voi olla integroinnin asetuksissa. Järjestelmänvalvojan on yleensä ratkaistava tämäntyyppiset virheet.   

## <a name="example"></a>Esimerkki
Tässä videossa on esimerkki siitä, miten tuotteen [!INCLUDE[prod_short](includes/cds_long_md.md)] synkronoinnissa tapahtuneet virheet voidaan korjata. Prosessi on sama kaikille integroinneille. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]


## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Yhdistettyjen tietueiden synkronointivirheiden tarkasteleminen ja ratkaiseminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yhdistettyjen tietojen synkronointivirheet** ja valitse sitten aiheeseen liittyvä linkki.
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

## <a name="remove-couplings-between-records"></a>Liitosten poistaminen tietueiden väliltä
Kun integraatiossa on jotain vikaa ja haluat poistaa tietueiden synkronoinnin pysäyttämisen, voit tehdä sen yhden tai usean tietueen kanssa kerralla. Voit irrottaa yhden tai useamman tietueen luettelosivuilta tai **Yhdistettyjen tietojen synkronointivirheet** -sivulta valitsemalla yhden tai useamman rivin ja valitsemalla **Poista yhdistäminen**. Voit myös poistaa kaikki yhden tai useamman taulukon yhdistämismäärityksen yhdistämiset **Integrointitaulukon yhdistämismääritykset** -sivulla. 

Jos entiteetti, jolla on yksisuuntainen yhdistämismääritys, on poistettu tuotteesta [!INCLUDE[prod_short](includes/prod_short.md)], rikottu yhdistämismääritys on poistettava manuaalisesti. Voit tehdä tämän **Yhdistettyjen tietojen synkronointivirheet** -sivulla valitsemalla **Etsi poistettavaksi** -toiminnon ja poistamalla yhdistämismääritykset.

## <a name="see-also"></a>Katso myös  
[Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 Salesin käyttäminen Business Centralista](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]