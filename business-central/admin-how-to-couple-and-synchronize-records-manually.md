---
title: Tietueiden yhdistäminen ja synkronoiminen manuaalisesti| Microsoft Docs
description: Kun integrointitaulukon yhdistämismääritys synkronoidaan, yhdistetyn Business Central- ja Dynamics 365 for Sales -objektin taulukon kaikkien tietueiden tiedot voidaan synkronoida.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 6d1248ac77208e382c5594af57335df6ff824630
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726765"
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
[Dynamics 365 for Salesin käyttö Business Centralista](marketing-integrate-dynamicscrm.md)
