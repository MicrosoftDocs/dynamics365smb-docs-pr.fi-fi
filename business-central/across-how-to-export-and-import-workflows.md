---
title: Työnkulkujen vienti ja tuonti | Microsoft Docs
description: Voit siirtää työnkulkuja muihin Business Central -tietokantoihin. esimerkiksi luotaessa uusia työnkuluja voidaan aikaa säästääksesi viedä ja tuoda työnkulkuja.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1a52d4b4bff0f96023b6206e6cb8cad3d9e59276
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129927"
---
# <a name="export-and-import-workflows"></a>Työnkulkujen vienti ja tuonti

Voit siirtää työnkulkuja muihin [!INCLUDE[prod_short](includes/prod_short.md)] tietokantoihin. esimerkiksi luotaessa uusia työnkuluja voidaan aikaa säästääksesi viedä ja tuoda työnkulkuja.  

Toinen tapa luoda nopeasti työnkulut on työnkulkujen luominen työnkulkumalleista. Lisätietoja on kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).  

Voit luoda **Työnkulku**-sivulla työnkulun mainitsemalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Työnkulun vieminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut** ja valitse sitten vastaava linkki.  
2. Valitse ensin työnkulku ja sitten **Vie tiedostoon** -toiminto.  

## <a name="to-import-a-workflow"></a>Työnkulun tuominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut** ja valitse sitten vastaava linkki.  
2. Valitse **Tuo tiedostosta** -toiminto.  
3. Valitse **Tuo**-sivulla **Valitse**-painike, valitse XML-tiedosto, joka sisältää työnkulun, ja valitse sitten **Avaa**-painike.  

> [!CAUTION]  
> Jos työnkulun koodi on jo tietokannassa, työnkulun osavaiheita korvataan tuodun työnkulun vaiheilla.  

## <a name="see-also"></a>Katso myös

[Työnkulkujen luominen](across-how-to-create-workflows.md)  
[Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md)  
[Arkistoitujen työnkulun osavaiheen ilmentymien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)  
[Työnkulkujen poistaminen](across-how-to-delete-workflows.md)  
[Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Työnkulkujen määrittäminen](across-set-up-workflows.md)  
[Käytä työnkulkuja](across-use-workflows.md)  
[Työnkulku](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]