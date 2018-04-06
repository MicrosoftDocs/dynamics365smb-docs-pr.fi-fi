---
title: "Kohdistuksen lähteen ja kohteiden määrittäminen | Microsoft Docs"
description: "Jokainen kohdistus koostuu kohdistuslähteestä ja yhdestä tai useammasta kohdistustavoitteesta. Kohdistuksen lähde määrittää, mitkä kustannukset kohdistetaan. Kohdistuskohteet määrittävät, mihin kustannukset kohdistetaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d4dcf5f95d5fc44d4b8fb72b55d905c876989a56
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-allocation-source-and-targets"></a>Kohdistuksen lähteen ja sen tavoitteiden määrittäminen.
Jokainen kohdistus koostuu kohdistuslähteestä ja sekä vähintään yhdestä kohdistuskohteesta. Kohdistuksen lähde määrittää, mitkä kustannukset kohdistetaan. Kohdistuskohteet määrittävät, mihin kustannukset kohdistetaan.  

## <a name="to-set-up-cost-allocations"></a>Määritä kustannusten kohdistamiset  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kustannusten kohdistaminen** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Kustannusten kohdistaminen** -ikkunassa **Muokkaa** -toiminto.  
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

