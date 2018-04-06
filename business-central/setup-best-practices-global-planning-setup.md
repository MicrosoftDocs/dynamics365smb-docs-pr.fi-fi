---
title: "Yleisten suunnitteluasetusten parhaat käytännöt | Microsoft Docs"
description: "**Suunnittelu**-pikavälilehdellä **Tuotannon asetukset** -ikkunassa on useita kenttiä, jotka määrittävät yleiset säännöt tarjonnan suunnitteluun."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5f9eda3b9bb2482a446370058c7bd4a503dde6ee
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-global-planning-setup"></a>Asetukset - parhaat käytännöt: yleiset suunnitteluasetukset
**Suunnittelu**-pikavälilehdellä **Tuotannon asetukset** -ikkunassa on useita kenttiä, jotka määrittävät yleiset säännöt tarjonnan suunnitteluun.  

 Seuraavassa taulukossa on parhaita käytäntöjä siitä, miten voit määrittää valitun yleisen suunnitteluparametrin kentät. Saat lisätietoja kentästä valitsemalla **Asetuskenttä**-sarakkeessa olevan linkin.  

|Kentän asetukset|Parhaat käytännöt|Kommentti|  
|-----------------|-------------------|-------------|  
|Käytä ennustetta sijainneissa|Valitse, jos sinulla on määrättyjen sijaintien ennusteet.||  
|Komponentit sijainnissa|Jos nimikkeitä ei ole määritetty varastointiyksikköinä, valitse fyysisen päävaraston sijaintikoodi.|Tämä pätee myös, jos käytetään vain hankintalistaa.|  
|Tyhjä ylivuototaso|Valitse **Salli oletuslaskenta**, jos siirryt Microsoft Dynamics NAV 5.0- tai sitä aikaisemmasta versiosta.|Käytä vain, jos haluat sallia kaikkien tai joidenkin kohteiden ylittää uusintatilauspisteen.|  
|Oletusvaimentimen jakso|Valitse 1D tai 5D .<br /><br /> Jos et ole aiemmin käyttänyt ohjelman [!INCLUDE[d365fin](includes/d365fin_md.md)] suunnittelutoimintoa, määritä pidempi jakso.|Kun käyttäjät tuntevat toimintosanomien eri syyt, lyhennä puskuriaikaa antaaksesi lisää muutosehdotuksia.|  
|Oletuspuskurimäärä|Määritä 5-20% nimikkeen eräkoosta.||  

## <a name="see-also"></a>Katso myös  
 [Asetukset - parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md)   
 [Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
 [Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla](set-up-complex-application-areas-using-best-practices.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

