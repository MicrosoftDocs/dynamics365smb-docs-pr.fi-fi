---
title: "Työnkulkujen vienti ja tuonti | Microsoft Docs"
description: "Voit siirtää työnkulkuja muihin [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietokantoihin. Esimerkiksi uusia työnkuluja luotaessa työnkulkujen vienti ja tuonti säästää aikaa."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8126d3850103819e885d9d131ca3074f1b7cfda1
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-export-and-import-workflows"></a>Toimintaohje: työnkulkujen vienti ja tuonti
Voit siirtää työnkulkuja muihin [!INCLUDE[d365fin](includes/d365fin_md.md)] tietokantoihin. esimerkiksi luotaessa uusia työnkuluja voidaan aikaa säästääksesi viedä ja tuoda työnkulkuja.  

 Toinen tapa luoda nopeasti työnkulut on työnkulkujen luominen työnkulkumalleista. Lisätietoja on kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).  

 **Työnkulku**-ikkunassa voit luoda työnkulun luetteloimalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Työnkulun vieminen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Työnkulut** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ensin työnkulku ja sitten **Vie tiedostoon** -toiminto.  
3.  Valitse **Vie tiedosto** -ikkunassa **Tallenna**.  
4.  Valitse tiedostosijainti **Vie**-ikkunassa ja valitse sitten **Tallenna**-painike.  

## <a name="to-import-a-workflow"></a>Työnkulun tuominen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Työnkulut** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Tuo tiedostosta** -toiminto.  
3.  Valitse **Tuo** ikkunassa XML-tiedosto, joka sisältää työnkulun, ja valitse sitten **Avaa**.  

> [!CAUTION]  
>  Jos työnkulun koodi on jo tietokannassa, työnkulun osavaiheita korvataan tuodun työnkulun vaiheilla.  

## <a name="see-also"></a>Katso myös  
 [Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md)   
 [Ohje: Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md)   
 [Toimintaohje: Arkistoitujen työnkulun osavaiheen instanssien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)   
 [Toimintaohje: Työnkulkujen poistaminen](across-how-to-delete-workflows.md)   
 [Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Työnkulkujen määrittäminen](across-set-up-workflows.md)   
 [Työnkulkujen käyttäminen](across-use-workflows.md)   
 [Työnkulku](across-workflow.md)   

