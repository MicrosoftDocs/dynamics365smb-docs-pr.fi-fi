---
title: Yleisten suunnitteluasetusten parhaat käytännöt | Microsoft Docs
description: Suunnittelu-pikavälilehden Tuotannon asetukset-sivulla on useita kenttiä, jotka määrittävät tarjonnan suunnittelun yleiset säännöt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f70e720cd8639038f7c06de7f6b2f338652e8e4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757765"
---
# <a name="setup-best-practices-global-planning-setup"></a>Asetukset - parhaat käytännöt: yleiset suunnitteluasetukset
**Suunnittelu**-pikavälilehden **Tuotannon asetukset**-sivulla on useita kenttiä, jotka määrittävät tarjonnan suunnittelun yleiset säännöt.  

 Seuraavassa taulukossa on parhaita käytäntöjä siitä, miten voit määrittää valitun yleisen suunnitteluparametrin kentät. Saat lisätietoja kentästä valitsemalla **Asetuskenttä**-sarakkeessa olevan linkin.  

|Kentän asetukset|Parhaat käytännöt|Kommentti|  
|-----------------|-------------------|-------------|  
|Käytä ennustetta sijainneissa|Valitse, jos sinulla on määrättyjen sijaintien ennusteet.||  
|Komponentit sijainnissa|Jos nimikkeitä ei ole määritetty varastointiyksikköinä, valitse fyysisen päävaraston sijaintikoodi.|Tämä pätee myös, jos käytetään vain hankintalistaa.|  
|Tyhjä ylivuototaso|Valitse **Salli oletuslaskenta**, jos siirryt Microsoft Dynamics NAV 5.0- tai sitä aikaisemmasta versiosta.|Käytä vain, jos haluat sallia kaikkien tai joidenkin kohteiden ylittää uusintatilauspisteen.|  
|Oletusvaimentimen jakso|Valitse 1D tai 5D .<br /><br /> Jos et ole aiemmin käyttänyt ohjelman [!INCLUDE[prod_short](includes/prod_short.md)] suunnittelutoimintoa, määritä pidempi jakso.|Kun käyttäjät tuntevat toimintosanomien eri syyt, lyhennä puskuriaikaa antaaksesi lisää muutosehdotuksia.|  
|Oletuspuskurimäärä-%|Määritä 5-20% nimikkeen eräkoosta.||  

## <a name="see-also"></a>Katso myös  
 [Asetukset - parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md)   
 [Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
 [Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla](set-up-complex-application-areas-using-best-practices.md)  
 [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]