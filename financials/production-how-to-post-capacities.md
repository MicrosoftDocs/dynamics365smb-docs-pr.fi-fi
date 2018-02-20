---
title: Kapasiteettien kirjaaminen | Microsoft Docs
description: "Kapasiteettipäiväkirjaan kirjataan kulutetut kapasiteetit, joita ei ole määritelty tuotantotilaukselle. Esimerkiksi ylläpitotyö tulee määritellä kapasiteetille, muttei tuotantotilaukselle."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a30e62bf2bf62c547398d733fcfe80b0204805cf
ms.contentlocale: fi-fi
ms.lasthandoff: 01/30/2018

---
# <a name="post-capacities"></a>Kapasiteettien kirjaaminen
Kapasiteettipäiväkirjaan kirjataan kulutetut kapasiteetit, joita ei ole määritelty tuotantotilaukselle. Esimerkiksi ylläpitotyö on määritettävä määritellä kapasiteetille mutta ei tuotantotilaukselle.  

## <a name="to-post-capacities"></a>Kapasiteettien kirjaaminen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kapasiteettipäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Täytä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.  
3.  Syötä **Tyyppi**-kenttään kapasiteetin tyyppi (**Kuormitusryhmä** tai **Tuotantosolu**), jota olet kirjaamassa.  
4.  Valitse **Nro**-kenttään kuormitusryhmän tai tuotantosolun numero.  
5.  Syötä asianmukaiset tiedot muihin kenttiin, esimerkiksi **Aloitusaika**-, **Lopetusaika**-, **Määrä**- ja **Hukkatavara**-kenttiin.  
6.  Kirjaa kapasiteetit valitsemalla **Kirjaa**-toiminto.  

## <a name="to-view-work-center-ledger-entries"></a>Tuotantosolutapahtumien näyttäminen  
Voit tarkastella **Tuotantosolukortti**- ja **Kuormitusryhmän kortti** -ikkunoissa valmiiden tuotantotilausten tuloksena kirjattuja kapasiteetteja.    
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotantosolut** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa käsiteltävä **Tuotantosolukortti** luettelossa ja valitse sitten **Kapasiteettitapahtumat**-toiminto.  

**Kapasiteettitapahtumat**-ikkunassa näkyvät tuotantosolun kirjatut tapahtumat siinä järjestyksessä kuin ne on kirjattu.   

## <a name="see-also"></a>Katso myös  
[Tuotanto](production-manage-manufacturing.md)    
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)      
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

