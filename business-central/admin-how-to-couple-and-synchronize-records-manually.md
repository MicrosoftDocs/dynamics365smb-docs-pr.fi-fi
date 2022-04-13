---
title: Yhdistäminen ja synkronointi (sisältää videon)
description: Kun integrointitaulukon yhdistämismääritys synkronoidaan, yhdistettyjen Business Central- ja Dynamics 365 Sales -taulukoiden kaikkien tietueiden tiedot voidaan synkronoida.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.search.form: 6250
ms.date: 10/01/2021
ms.author: bholtorf
ms.openlocfilehash: 2bc46e165018d29684b116f7aac3745c9d533c42
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8517600"
---
# <a name="coupling-and-synchronizing-records-between-dataverse-and-business-central"></a>Tietueiden yhdistäminen ja synkronoiminen Dataversen ja Business Centralin välillä

Tässä ohjeaiheessa kerrotaan, miten yksi tietue tai useita tietueita yhdistetään [!INCLUDE[prod_short](includes/prod_short.md)]:ssä Dataverse- tai [!INCLUDE[crm_md](includes/crm_md.md)]-tietueisiin. Tietueiden yhdistämisen ansiosta voit tarkastella Dataversein tietoja [!INCLUDE[prod_short](includes/prod_short.md)]ista ja päin vastoin. Yhdistäminen mahdollistaa myös tietojen synkronoinnin tietueiden välillä. Voit yhdistää aiemmin luotuja tietueita tai luoda ja yhdistää uusia tietueita.

> [!Note]
> Tietojen yhdistäminen ja synkronointi on käytettävissä vain, jos järjestelmänvalvoja on muodostanut yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]:n ja Dataversen tai [!INCLUDE[crm_md](includes/crm_md.md)]:n välille. Asian voi tarkistaa nopeasti avaamalla **Asiakas**-kortin ja etsimällä **Määritä yhdistäminen** -toiminnon. Jos toiminto on käytettävissä, sovellukset on yhdistetty.   

## <a name="video-example"></a>Esimerkkivideo
Tässä videossa näytetään tietojen kytkentä ja synkronointi osana [!INCLUDE[crm_md](includes/crm_md.md)] -ohjelman integrointia.

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

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>Voit yhdistää monta tietuetta vastaavuuspohjaisen yhdistämisen avulla.

Voit määrittää entiteetin (esimerkiksi asiakkaan tai kontaktin) synkronoitavat tiedot yhdistämällä tietueet vastaavuuksien perusteella. Voit tarkentaa vastaavuuksia määrittämällä haun kirjainkoon merkitseväksi ja määrittämällä kullekin vastaavuudelle prioriteetin. Jos vastaavuutta ei löydy, voit myös määrittää, että haluat luoda entiteetin Dataversessa. Lisätietoja on kohdassa [Vastaavuuspohjaisen yhdistämisen mukauttaminen](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

1. Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa tietueen luettelosivu, kuten asiakkaiden tai yhteyshenkilöiden luettelosivu.
2. Valitse **Vastaavuuspohjainen yhdistäminen** -toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>Useiden tietueiden synkronointi  
1.  Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa tietueen luettelosivu, kuten asiakkaiden tai yhteyshenkilöiden luettelosivu.  
2.  Valitse ensin synkronoitavat tietueet ja sitten **Synkronoi nyt** -toiminto.  
3.  Jos tietueet voidaan synkronoida yhteen suuntaan, valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.  

## <a name="uncoupling-records"></a>Tietueiden yhdistämisen poistaminen
Voit irrottaa yhden tai useamman tietueen luettelosivuilta tai **Yhdistettyjen tietojen synkronointivirheet** -sivulta valitsemalla yhden tai useamman rivin ja valitsemalla **Poista yhdistäminen**. Voit myös poistaa kaikki yhden tai useamman taulukon yhdistämismäärityksen yhdistämiset **Integrointitaulukon yhdistämismääritykset** -sivulla.

## <a name="see-also"></a>Katso myös  
[Dynamics 365 Salesin käyttäminen Business Centralista](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]