---
title: "Yleisten suunnitteluasetusten parhaat käytännöt | Microsoft Docs"
description: "**Suunnittelu**-pikavälilehdellä **Tuotannon asetukset** -ikkunassa on useita kenttiä, jotka määrittävät yleiset säännöt tarjonnan suunnitteluun."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f1a4e3a30d4d665a83ab599ad19dfd3760d744b2
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

