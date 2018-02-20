---
title: "Tilikartan kustannuspaikkojen ja kustannuskohteiden määrittäminen | Microsoft Docs"
description: "Voit siirtää kulu- ja tuottotapahtumat automaattisesti pääkirjanpidosta kustannuslaskentaan joko jokaisen pääkirjanpidon kirjauksen tai eräajon yhteydessä. Kun teet siirron, järjestelmä siirtää vain tapahtumat, jotka on jo linkitetty kustannuspaikkaan tai kustannuskohteeseen. Muodosta mielekäs siirto varmistamalla, että kustannuspaikat ja kustannuskohdeet on asianmukaisesti määritetty."
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
ms.openlocfilehash: 92ad393733c758304743ec0b63c98c1612e7240b
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Kustannuspaikkojen ja kustannuskohteiden määrittäminen tilikarttaan
Voit siirtää kulu- ja tuottotapahtumat automaattisesti pääkirjanpidosta kustannuslaskentaan joko jokaisen pääkirjanpidon kirjauksen tai eräajon yhteydessä. Kun teet siirron, [!INCLUDE[d365fin](includes/d365fin_md.md)] vain siirtää tapahtumat, jotka on jo linkitetty kustannuspaikkaan tai kustannuskohteeseen. Muodosta mielekäs siirto varmistamalla, että kustannuspaikat ja kustannuskohdeet on asianmukaisesti määritetty.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Dimension oletusarvojen määrittäminen pääkirjanpitotilejä varten  
Voit määrittää kunkin pääkirjanpidon tilin dimension oletusarvot **Oletusdimensio**-taulukossa. Seuraavassa esimerkissä näytetään, miten määritetään, että KP-tilin kirjauksia tehdessä tulee aina olla OSASTO-kustannuspaikka eikä koskaan PROJEKTI-kustannuskohde.  

|**Dimensiokoodi**|**Arvon kirjaaminen**|  
|------------------------------------------|-----------------------------------------|  
|Osaston|Koodi pakollinen|  
|Projektin|Ei koodia|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Dimensioarvojen määrittäminen yleiskustannuksille ja suorille kustannuksille  
 Voit siirtää yleiskustannukset kustannuspaikkaan ja suorat kustannukset kustannuskohteeseen. Seuraavassa taulukossa näytetään dimension asetusarvojen optimaalinen yhdistelmä.  

|Siirrä kohteeseen|Kustannuspaikan kirjaus|Kustannuskohteen kirjaus|  
|-----------------|-------------------------|-------------------------|  
|Kustannuspaikka|Koodi pakollinen|Ei koodia|  
|Kustannuskohde|Ei koodia|Koodi pakollinen|  

> [!NOTE]  
>  Varmista, että kirjanpitoon ennalta määritetty kustannuspaikka ja kustannusobjekti siirretään automaattisesti kustannuslaskentaan, valitsemalla **Tarkista KP-kirjaukset** -valintaruutu Kustannuslaskennan asetukset -ikkunassa.  

## <a name="see-also"></a>Katso myös  
[Kustannuslaskenta](finance-manage-cost-accounting.md)  
[Kustannuspaikkojen määrittäminen](finance-how-to-set-up-cost-centers.md)   
[Kustannuskohteiden määrittäminen](finance-how-to-set-up-cost-objects.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

