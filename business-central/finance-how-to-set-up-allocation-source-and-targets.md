---
title: Kohdistuksen lähteen ja kohteiden määrittäminen | Microsoft Docs
description: Jokainen kohdistus koostuu kohdistuslähteestä ja yhdestä tai useammasta kohdistustavoitteesta. Kohdistuksen lähde määrittää, mitkä kustannukset kohdistetaan. Kohdistuskohteet määrittävät, mihin kustannukset kohdistetaan.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 2e8040816ed5089188f06f76b2cd8f027ba83766
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243570"
---
# <a name="set-up-allocation-source-and-targets"></a>Kohdistuksen lähteen ja sen tavoitteiden määrittäminen.
Jokainen kohdistus koostuu kohdistuslähteestä ja sekä vähintään yhdestä kohdistuskohteesta. Kohdistuksen lähde määrittää, mitkä kustannukset kohdistetaan. Kohdistuskohteet määrittävät, mihin kustannukset kohdistetaan.  

## <a name="to-set-up-cost-allocations"></a>Määritä kustannusten kohdistamiset  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kustannusten kohdistaminen** ja valitse sitten liittyvä linkki.  
2.  Valitse **Kustannusten kohdistaminen** -sivulla **Muokkaa**-toiminto.  
3.  Kirjoita tunnus kohdistuslähteelle **Tunnus**-kentässä.  
4.  Määritä taso numerona väliltä 1-99 **Taso**-kentässä Kohdistuksen kirjauksen tulee noudattaa tasojen järjestystä.  
5.  Syötä kustannustyyppi, joka määrittää mitkä kustannukset kohdistetaan **Kustannustyypin väli** -kentässä. Jos kustannustyypin kaikki kustannukset on kohdistettu, alueväliä ei ole määritetty.  
6.  Määritä kustannuspaikka ja kustannukset, jotka kohdistetaan **Kustannuspaikan koodi** -kentässä.  
7.  Määritä kustannusobjekti ja kustannukset, jotka kohdistetaan **Kustannusobjektin koodi** -kentässä. Tämä kenttä pysyy useimmiten tyhjänä, koska kustannuskohteet kohdistetaan harvoin toisiin kustannuskohteisiin.  
8.  Syötä kustannustyyppi **Luotto kustannustyyppiin** -kenttään. Kohdistetut kustannukset hyvitetään lähdekustannustyypille. Hyvityskirjaus kirjataan tässä annettuun kustannustyyppiin.  
9. Määritä **Rivit**-pikavälilehdessä kohdistuksen kohteet. Valitse **Kohdekustannustyyppi** -kentässä ensimmäisellä rivillä kustannustyyppi. Se määrittää, mille kustannustyypille kohdistaminen veloitetaan.  
10. Anna ensimmäisellä rivillä ensimmäinen kohdistuskohde **Kohdekustannuspaikka** -kenttää tai **Kohdekustannuskohde** -kenttään. Nämä kaksi kenttää määrittävät, mistä kustannuspaikasta tai kustannuskohteesta kohdistaminen veloitetaan. Voit täyttää vaon yhden näistä kentistä, mutta et molempia.  
11. Toista samat vaiheet toisella rivillä määrittääksesi lisäkohdistustavoitteet.  
12. Kun olet määrittänyt kohdistuksen kohteet ja lähteet, laske kokonaisjakauma-arvot valitsemalla **Laske kohdistusavain** -toiminto.  

> [!NOTE]  
>  Deaktivoi kohdistamisen määritys valitsemalla **Estetty** -valintaruutu.  

## <a name="see-also"></a>Katso myös  
[Kustannuslaskenta](finance-manage-cost-accounting.md)  
 [Suodattimien määrittäminen dynaamisen kohdistuksen perusteille.](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Esimerkkiskenaario: Kohdistamissuhteeseen perustuvan staattisen kohdistamisen määrittäminen](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)   
 [Esimerkkiskenaario: Määrittämällä myytyihin nimikkeisiin perustuvat dynaamiset kohdistamiset](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Kustannusten määrittäminen ja kohdistaminen](finance-define-and-allocate-costs.md)   
 [Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
