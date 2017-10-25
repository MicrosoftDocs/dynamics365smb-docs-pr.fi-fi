---
title: "Työnkulkujen luominen työnkulkumalleista | Microsoft Docs"
description: "Voit säästää aikaa uusien työnkulkujen luomisessa luomalla työnkulut työnkulkumalleista."
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
ms.openlocfilehash: dcf6f5f5b0364ebcaefdcbc43fdbd7471cb6079e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-workflows-from-workflow-templates"></a>Ohje: Työnkulkujen luominen työnkulkumalleista
Voit säästää aikaa uusien työnkulkujen luomisessa luomalla työnkulut työnkulkumalleista.  

 Työnkulkumallit ovat yleisen [!INCLUDE[d365fin](includes/d365fin_md.md)] -version työnkulkuja, joita ei voi muokata. Työnkulkumallien koodit, jotka Microsoft on lisännyt, sisältävät etuliitteen "MS-".  

 Työnkulun voi nopeasti myös tuomalla aiemmin luodun työnkulun, joka on [!INCLUDE[d365fin](includes/d365fin_md.md)]in ulkopuolisessa tiedostossa. Lisätietoja on kohdassa [Toimintaohje: Työnkulkujen vienti ja tuonti](across-how-to-export-and-import-workflows.md).  

**Työnkulku**-ikkunassa voit luoda työnkulun luetteloimalla liittyvät toimet riveillä. Jokainen vaihe koostuu työnkulun tapahtumasta, jota valvotaan tapahtuman ehtojen mukaan, ja työnkulun vastauksesta, jota valvotaan vastausvaihtoehtojen mukaan. Työnkulku määritetään täyttämällä työnkulkurivien kentät tapahtumien kiinteistä luetteloista ja vastausarvot, jotka edustavat sovelluskoodin tukemia skenaarioita. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Työnkulun luominen työnkulkumallista  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Työnkulut** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Luo työnkulku mallista** -toiminto. **Työnkulkumallit**-ikkuna avautuu.  
3.  Valitse työnkulkumalli ja sitten **OK**-painike.  

     Uuden työnkulun avautuvassa **Työnkulku**-ikkunassa on kaikki valitun mallin tiedot. **Koodi**-kentän arvoon liitetään esimerkiksi ”-01”, joka osoittaa, että kyseessä on ensimmäinen työnkulkumallista luotu työnkulku.  
4.  Jatka työnkulun luontia muokkaamalla työnkulun vaiheita tai lisäämällä uusia vaiheita. Lisätietoja on kohdassa [Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Katso myös  
 [Toimintaohje: Työnkulkujen luominen](across-how-to-create-workflows.md)   
 [Toimintaohje: työnkulkujen vienti ja tuonti](across-how-to-export-and-import-workflows.md)   
 [Toimintaohje: Arkistoitujen työnkulun osavaiheen instanssien tarkasteleminen](across-how-to-view-archived-workflow-step-instances.md)   
 [Toimintaohje: Työnkulkujen poistaminen](across-how-to-delete-workflows.md)   
 [Vaihekuvaus: Ostojen hyväksyntä -työnkulun määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Työnkulkujen määrittäminen](across-set-up-workflows.md)   
 [Työnkulkujen käyttäminen](across-use-workflows.md)   
 [Työnkulku](across-workflow.md)   

