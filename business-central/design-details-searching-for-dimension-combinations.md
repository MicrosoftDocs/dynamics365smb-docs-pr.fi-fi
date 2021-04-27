---
title: Rakennetiedot – Dimensioyhdistelmien etsiminen | Microsoft Docs
description: Kun suljet sivun dimensioyhdistelmän muokkaamisen jälkeen, Business Central arvioi, onko muokattu dimensiojoukko olemassa. Jos yhdistelmää ei ole olemassa, järjestelmän luo uuden ja palauttaa dimensioyhdistelmän tunnuksen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: db971af61719bfa84566c78cc91b4c805c14ab9b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783845"
---
# <a name="design-details-searching-for-dimension-combinations"></a>Rakennetiedot: dimensioyhdistelmien etsiminen
Kun suljet sivun dimensioyhdistelmän muokkaamisen jälkeen, [!INCLUDE[prod_short](includes/prod_short.md)] arvioi, onko muokattu dimensiojoukko olemassa. Jos yhdistelmää ei ole olemassa, järjestelmän luo uuden ja palauttaa dimensioyhdistelmän tunnuksen.  

## <a name="building-search-tree"></a>Rakennetaan hakupuuta  
 Taulukkoa 481 **Dimensionasetuksen puusolmu** käytetään, kun [!INCLUDE[prod_short](includes/prod_short.md)] arvioi onko dimensiosarja jo olemassa taulukossa 480 **Dimensionasetuskirjaus**. Arviointi suoritetaan kulkemalla hakupuu läpi rekursiivisesti aloittaen ylätason numerosta 0. Ylätason 0 edustaa dimensiosarjaa, jossa ei ole dimensiosarjan kirjauksia. Tämän dimensiosarjan jälkeläiset edustavat dimensiosarjoja, joilla on vain yksi dimensiosarjan kirjaus. Näiden dimensiosarjojen jälkeläiset edustavat dimensiosarjoja, joilla on kaksi jälkeläistä jne.  

### <a name="example-1"></a>Esimerkki 1  
 Seuraava kaavio esittelee hakupuun ja kuusi dimensiosarjaa. Kaaviossa näkyy vain erottava dimensioyhdistelmä.  

 ![Esimerkki dimension puurakenteesta](media/nav2013_dimension_tree.png "Esimerkki dimension puurakenteesta")  

 Seuraavassa taulukossa kuvataan koko dimensiosarjan kirjausten luettelo, joka muodostaa kunkin dimensiosarjan.  

|Dimensioyhdistelmät|Dimensioyhdistelmän tapahtumat|  
|--------------------|---------------------------|  
|Aseta 0|Ei mitään|  
|Aseta 1|AREA 30|  
|Aseta 2|AREA 30, DEPT ADM|  
|Aseta 3|AREA 30, DEPT PROD|  
|Aseta 4|AREA 30, DEPT ADM, PROJ VW|  
|Aseta 5|AREA 40|  
|Aseta 6|AREA 40, PROJ VW|  

### <a name="example-2"></a>Esimerkki 2  
 Tämä esimerkki osoittaa, miten [!INCLUDE[prod_short](includes/prod_short.md)] arvioi, onko dimensioyhdistelmän tapahtumat AREA 40 ja DEPT PROD sisältävä dimensioyhdistelmä olemassa.  

 [!INCLUDE[prod_short](includes/prod_short.md)] varmistaa ensin päivittämällä **Dimensioyhdistelmän puusolmu** -taulukon, että hakupuu näyttää samalta kuin seuraavassa kaaviossa. Dimensioyhdistelmästä 7 tulee dimensioyhdistelmän 5 alitaso.  

 ![Esimerkki dimension puurakenteesta NAV 2013 -sovelluksessa](media/nav2013_dimension_tree_example2.png "Esimerkki dimension puurakenteesta NAV 2013 -sovelluksessa")  

### <a name="finding-dimension-set-id"></a>Dimensioyhdistelmän tunnuksen etsiminen  
 Käsitteellisellä tasolla hakupuun **Päätunnus**, **Dimensio** ja **Dimensioarvo** yhdistetään ja niitä käytetään perusavaimena, koska [!INCLUDE[prod_short](includes/prod_short.md)] kulkee puussa samassa järjestyksessä kuin dimensiotapahtumat. GET-toimintoa (tietue) käytetään etsimään dimensiosarjan tunnusta. Seuraava koodiesimerkki osoittaa, kuinka löydetään dimensiosarjan tunnus, kun dimensioarvoja on kolme.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

Jotta [!INCLUDE[prod_short](includes/prod_short.md)] voisi kuitenkin edelleen nimetä sekä dimension että dimensioarvon uudelleen, taulukkoa 349, **Dimensioarvo**, laajennetaan **Dimensioarvon tunnus** -kokonaislukukentällä. Tämä taulukko muuntaa kenttäparin **Dimensio** ja **Dimension arvo** kokonaislukuarvoksi. Kun nimeät dimension ja dimension arvon, kokonaislukuarvoa ei muuteta.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a>Katso myös

 [GET-funktio (tietue)](/dynamics-nav/GET-Function--Record-)    
 [Rakennetiedot: Dimensioyhdistelmätapahtumat](design-details-dimension-set-entries.md)   
 [Dimensioyhdistelmätapahtumien yleiskuva](design-details-dimension-set-entries-overview.md)   
 [Rakennetiedot: taulukkorakenne](design-details-table-structure.md)   
 


[!INCLUDE[footer-include](includes/footer-banner.md)]
