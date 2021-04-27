---
title: Yhdistäminen ja synkronointi | Microsoft Docs
description: Kun integrointitaulukon yhdistämismääritys synkronoidaan, yhdistettyjen Business Central- ja Dynamics 365 Sales -taulukoiden kaikkien tietueiden tiedot voidaan synkronoida.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 53b12b6ab7e53a20bb1b8fcc659b2f1454e85321
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779930"
---
# <a name="coupling-and-synchronizing"></a>Yhdistäminen ja synkronointi
Tässä ohjeaiheessa kerrotaan, miten yksi tietue tai useita tietueita yhdistetään [!INCLUDE[prod_short](includes/prod_short.md)]:ssä Dataverse- tai [!INCLUDE[crm_md](includes/crm_md.md)]-tietueisiin. Tietueiden yhdistämisen ansiosta voit tarkastella Dataversein tietoja [!INCLUDE[prod_short](includes/prod_short.md)]ista ja päin vastoin. Yhdistäminen mahdollistaa myös tietojen synkronoinnin tietueiden välillä. Voit yhdistää aiemmin luotuja tietueita tai luoda ja yhdistää uusia tietueita.

> [!Note]
> Tietojen yhdistäminen ja synkronointi on käytettävissä vain, jos järjestelmänvalvoja on muodostanut yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]:n ja Dataversen tai [!INCLUDE[crm_md](includes/crm_md.md)]:n välille. Asian voi tarkistaa nopeasti avaamalla **Asiakas**-kortin ja etsimällä **Määritä yhdistäminen** -toiminnon. Jos toiminto on käytettävissä, sovellukset on yhdistetty.   

## <a name="video-example"></a>Esimerkkivideo

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Tietueen yhdistäminen  
1.  Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa sen tietueen kortti, jonka haluat yhdistää. Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.  

    Voit myös avata luettelosivun ja valita tietueen, jonka haluat yhdistää.  

2.  Valitse **Määritä yhdistäminen** -toiminto.  
3.  Täytä kentät ja valitse **OK**.  

## <a name="to-synchronize-a-single-record"></a>Yhden tietueen synkronointi  
1.  Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa sen tietueen kortti, jonka haluat yhdistää. Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.  
2.  Valitse **Synkronoi nyt** -toiminto.  
3.  Jos tietue voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Yhden tietueen synkronointi [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta  
1.  Avaa [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksessa sen tietueen lomake, jonka haluat yhdistää. Se voi olla esimerkiksi tilikortin tai yhteyshenkilökortin lomake.  
2.  Valitse **[!INCLUDE[prod_short](includes/prod_short.md)]** -toiminto valintanauhasta. Tietue avataan ja yhdistetään automaattisesti.

> [!Note]
> Voit synkronoida yhden tietueen [!INCLUDE[crm_md](includes/crm_md.md)]-sovelluksesta automaattisesti vain, kun **Synkronoi vain yhdistetyt tietueet** on poistettu käytöstä ja synkronoinnin suunnaksi on määritetty Kaksisuuntainen tai Integrointitaulukosta tietueen **Integrointitaulukon yhdistämismääritys** -sivulla. Lisätietoja on kohdassa [Taulukoiden ja kenttien yhdistäminen synkronointia varten](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-synchronize-multiple-records"></a>Useiden tietueiden synkronointi  
1.  Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa tietueen luettelosivu, kuten asiakkaiden tai yhteyshenkilöiden luettelosivu.  
2.  Valitse ensin synkronoitavat tietueet ja sitten **Synkronoi nyt** -toiminto.  
3.  Jos tietueet voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.  

## <a name="uncoupling-records"></a>Tietueiden yhdistämisen poistaminen
Voit irrottaa yhden tai useamman tietueen luettelosivuilta tai **Yhdistettyjen tietojen synkronointivirheet** -sivulta valitsemalla yhden tai useamman rivin ja valitsemalla **Poista yhdistäminen**. Voit myös poistaa kaikki yhden tai useamman taulukon yhdistämismäärityksen yhdistämiset **Integrointitaulukon yhdistämismääritykset** -sivulla.

## <a name="see-also"></a>Katso myös  
[Dynamics 365 Salesin käyttäminen Business Centralissa](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]