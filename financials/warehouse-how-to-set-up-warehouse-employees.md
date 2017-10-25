---
title: "Varastotyöntekijöiden määrittäminen | Microsoft Docs"
description: "Jokainen varastotoimintoja tekevä käyttäjä on määritettävä varastotyöntekijäksi ja liitettävä yhteen oletussijaintiin ja mahdollisesti muihin sijainteihin, jotka eivät ole oletussijainteja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6fb0aa48352bc35c2e9ee399a3d0b17032a5ed7e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-warehouse-employees"></a>Varastotyöntekijöiden määrittäminen
Jokainen varastotoimintoja tekevä käyttäjä on määritettävä varastotyöntekijäksi sekä liitettävä yhteen oletussijaintiin ja mahdollisesti muihin sijainteihin, jotka eivät ole oletussijainteja. Nämä käyttäjäasetukset suodattavat kaikki tietokannan varastotoiminnot työntekijän sijainnissa niin, että työntekijä voi suorittaa varastotoimintoja vain oletussijainnissa. Käyttäjä voidaan liittää myös muihin kuin oletussijanteihin, joissa käyttäjä voi katsella toimintorivejä mutta ei suorittaa toimintoja.

## <a name="to-set-up-warehouse-employees"></a>Varastotyöntekijöiden määrittäminen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Varaston työntekijät** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Käyttäjätunnus**-kenttä ja valitse sitten käyttäjä, joka lisätään varaston työntekijäksi. Valitse **OK**-painike.  
6.  Syötä **Sijaintikoodi**-kenttään käyttäjän työskentelypaikan sijainnin koodi.  
7.  Valitse **Oletusarvo**-valintaruutu, kun haluat määrittää tämän sijainnin ainoaksi sijainniksi, jossa käyttäjä voi tehdä varastotoimintoja.  
8.  Liitä sijainteihin muita työntekijöitä tai liitä aiemmin luoduille varastotyöntekijöille muita kuin oletussijainteja toistamalla nämä vaiheet.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

