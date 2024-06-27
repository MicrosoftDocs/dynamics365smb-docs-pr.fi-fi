---
title: Synkronointitöiden tilan näyttäminen
description: 'Käytä Yhdistettyjen tietojen synkronointivirheet -sivua, kun haluat näyttää niiden synkronointitöiden tilan, jotka on suoritettu yhdistetyille tietueille integroinneissa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.search.form: 6250
ms.date: 06/14/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Synkronointitöiden tilan näyttäminen


Käytä **Yhdistettyjen tietojen synkronointivirheet** -sivua, kun haluat näyttää niiden synkronointitöiden tilan, jotka on suoritettu yhdistetyille tietueille Dataverse- tai [!INCLUDE[crm_md](includes/crm_md.md)] -integroinneissa. Tämä sisältää työt, jotka on suoritettu työjonosta, ja manuaaliset synkronointityöt, jotka on suoritettu [!INCLUDE[prod_short](includes/prod_short.md)] -tietueista. Näiden tilan näyttäminen on hyödyllistä esimerkiksi vianmäärityksen yhteydessä, koska tällöin saat tietoja yhdistettyihin tietueisiin liittyvistä virheistä. Yleensä tällaiset virheet johtuvat käyttäjän toiminnoista. Näitä ovat esimerkiksi seuraavat:  

* Kaksi henkilö tekee muutoksia samaan tietoon kummassakin liiketoimintasovelluksessa.
* Joku poisti tiedon yhdestä sovelluksesta, ei molemmista.

> [!Note]
> **Yhdistettyjen tietojen synkronointivirheet** -sivulla näkyvät yhdistettyjen tietueiden töihin liittyvät tiedot. Jos ratkaiset kaikki virheet, mutta tietueita ei silti synkronoida, syy voi olla integroinnin asetuksissa. Järjestelmänvalvojan on yleensä ratkaistava tämäntyyppiset virheet.   

## Esimerkki
Tässä videossa on esimerkki siitä, miten tuotteen [!INCLUDE[prod_short](includes/cds_long_md.md)] synkronoinnissa tapahtuneet virheet voidaan korjata. Prosessi on sama kaikille integroinneille. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]


## Yhdistettyjen tietueiden synkronointivirheiden tarkasteleminen ja ratkaiseminen
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

## Tietyn (manuaalisesti synkronoidun) tietueen synkronointilokin näyttäminen
1. Voit esimerkiksi avata asiakkaan, nimikkeen tai minkä tahansa muun tietoja [!INCLUDE[prod_short](includes/prod_short.md)]- ja Dataverse- tai [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksen välillä synkronoivan tietueen.
2. Valitse **Synkronointiloki** toimenpide tarkastellaksesi valitun tietueen synkronointilokia. Esimerkiksi tiettyä asiakasta jonka synkronoit manuaalisesti.

## Liitosten poistaminen tietueiden väliltä
Kun integraatiossa on jotain vikaa ja haluat poistaa tietueiden synkronoinnin pysäyttämisen, voit tehdä sen yhden tai usean tietueen kanssa kerralla. Voit irrottaa yhden tai useamman tietueen luettelosivuilta tai **Yhdistettyjen tietojen synkronointivirheet** -sivulta valitsemalla yhden tai useamman rivin ja valitsemalla **Poista yhdistäminen**. Voit myös poistaa kaikki yhden tai useamman taulukon yhdistämismäärityksen yhdistämiset **Integrointitaulukon yhdistämismääritykset** -sivulla. 

Jos entiteetti, jolla on yksisuuntainen yhdistämismääritys, on poistettu tuotteesta [!INCLUDE[prod_short](includes/prod_short.md)], rikottu yhdistämismääritys on poistettava manuaalisesti. Voit tehdä tämän **Yhdistettyjen tietojen synkronointivirheet** -sivulla valitsemalla **Etsi poistettavaksi** -toiminnon ja poistamalla yhdistämismääritykset.

## Katso myös  
[Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 Salesin käyttäminen Business Centralista](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]