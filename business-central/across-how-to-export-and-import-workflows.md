---
title: Työnkulkujen vienti ja tuonti | Microsoft Docs
description: Voit siirtää työnkulkuja muihin Business Central -tietokantoihin. esimerkiksi luotaessa uusia työnkuluja voidaan aikaa säästääksesi viedä ja tuoda työnkulkuja.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2d309940d177491ce24f49884f388a5c233147fa
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188274"
---
# <a name="export-and-import-workflows"></a>Työnkulkujen vienti ja tuonti
Voit siirtää työnkulkuja muihin [!INCLUDE[d365fin](includes/d365fin_md.md)] tietokantoihin. esimerkiksi luotaessa uusia työnkuluja voidaan aikaa säästääksesi viedä ja tuoda työnkulkuja.  

 Toinen tapa luoda nopeasti työnkulut on työnkulkujen luominen työnkulkumalleista. Lisätietoja on kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).  

 Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Työnkulun vieminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.  
2.  Valitse ensin työnkulku ja sitten **Vie tiedostoon** -toiminto.  
3.  Valitse **Vie tiedosto** -sivulla **Tallenna**.  
4.  Valitse tiedostosijainti **Vie**-sivulla ja valitse sitten **Tallenna**-painike.  

## <a name="to-import-a-workflow"></a>Työnkulun tuominen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.  
2.  Valitse **Tuo tiedostosta** -toiminto.  
3.  Valitse **Tuo**-sivulla XML-tiedosto, joka sisältää työnkulun, ja valitse sitten **Avaa**.  

> [!CAUTION]  
>  Jos työnkulun koodi on jo tietokannassa, työnkulun osavaiheita korvataan tuodun työnkulun vaiheilla.  

## <a name="see-also"></a>Katso myös  
 [Työnkulkujen luominen](across-how-to-create-workflows.md)   
 [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md)   
 [Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)   
 [Työnkulkujen poistaminen](across-how-to-delete-workflows.md)   
 [Vaihekuvaus: Ostojen hyväksyntätyönkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Työnkulkujen määrittäminen](across-set-up-workflows.md)   
 [Työnkulkujen käyttäminen](across-use-workflows.md)   
 [Työnkulku](across-workflow.md)   
