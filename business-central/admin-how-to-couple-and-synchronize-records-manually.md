---
title: Tietueiden yhdistäminen ja synkronoiminen manuaalisesti| Microsoft Docs
description: Kun integrointitaulukon yhdistämismääritys synkronoidaan, yhdistetyn Business Central- ja Dynamics 365 Sales -entiteetin taulukon kaikkien tietueiden tiedot voidaan synkronoida.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0c70b1ba34af32b7cf542149c8f15cb191761358
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308114"
---
# <a name="couple-and-synchronize-records-manually"></a>Tietueiden yhdistäminen ja synkronoiminen manuaalisesti
Tässä ohjeaiheessa käsitellään vähintään yhden [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueen yhdistämistä [!INCLUDE[crm_md](includes/crm_md.md)]in tietueisiin. Tietueiden yhdistämisen ansiosta voit tarkastella [!INCLUDE[crm_md](includes/crm_md.md)]in tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]ista ja päin vastoin. Yhdistäminen mahdollistaa myös tietojen synkronoinnin tietueiden välillä. Voit yhdistää aiemmin luotuja tietueita tai luoda ja yhdistää uusia tietueita.

> [!Note]
> Tietojen yhdistäminen ja synkronointi [!INCLUDE[crm_md](includes/crm_md.md)]in avulla on käytettävissä vain, jos järjestelmänvalvoja on muodostanut yhteyden [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in välille. Asian voi tarkistaa nopeasti avaamalla **Asiakas**-kortin ja etsimällä **Määritä yhdistäminen** -toiminnon. Jos toiminto on käytettävissä, sovellukset on yhdistetty.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Tietueen yhdistäminen  
1.  Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa sen tietueen kortti, jonka haluat yhdistää. Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.  

    Voit myös avata luettelosivun ja valita tietueen, jonka haluat yhdistää.  

2.  Valitse **Määritä yhdistäminen** -toiminto.  
3.  Täytä kentät ja valitse **OK**.  

## <a name="to-synchronize-a-single-record"></a>Yhden tietueen synkronointi  
1.  Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa sen tietueen kortti, jonka haluat yhdistää. Se voi olla esimerkiksi asiakkaan tai yhteyshenkilön kortti.  
2.  Valitse **Synkronoi nyt** -toiminto.  
3.  Jos tietue voidaan synkronoida joko [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin tai [!INCLUDE[crm_md](includes/crm_md.md)]ista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin , valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.  

## <a name="to-synchronize-multiple-records"></a>Useiden tietueiden synkronointi  
1.  Avaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa tietueen luettelosivu, kuten asiakkaiden tai yhteyshenkilöiden luettelosivu.  
2.  Valitse ensin synkronoitavat tietueet ja sitten **Synkronoi nyt** -toiminto.  
3.  Jos tietueet voidaan synkronoida joko [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin tai [!INCLUDE[crm_md](includes/crm_md.md)]ista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin , valitse vaihtoehto, joka määrittää suunnan tietojen päivitykselle ja valitse sitten **OK**.  

## <a name="see-also"></a>Katso myös  
[Dynamics 365 Salesin käyttäminen Business Centralissa](marketing-integrate-dynamicscrm.md)
