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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 947cf4314cab2ad1c326c34e797d92fa235e4096
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3789173"
---
# <a name="setup-best-practices-global-planning-setup"></a>Asetukset - parhaat käytännöt: yleiset suunnitteluasetukset
**Suunnittelu**-pikavälilehden **Tuotannon asetukset**-sivulla on useita kenttiä, jotka määrittävät tarjonnan suunnittelun yleiset säännöt.  

 Seuraavassa taulukossa on parhaita käytäntöjä siitä, miten voit määrittää valitun yleisen suunnitteluparametrin kentät. Saat lisätietoja kentästä valitsemalla **Asetuskenttä**-sarakkeessa olevan linkin.  

|Kentän asetukset|Parhaat käytännöt|Kommentti|  
|-----------------|-------------------|-------------|  
|Käytä ennustetta sijainneissa|Valitse, jos sinulla on määrättyjen sijaintien ennusteet.||  
|Komponentit sijainnissa|Jos nimikkeitä ei ole määritetty varastointiyksikköinä, valitse fyysisen päävaraston sijaintikoodi.|Tämä pätee myös, jos käytetään vain hankintalistaa.|  
|Tyhjä ylivuototaso|Valitse **Salli oletuslaskenta**, jos siirryt Microsoft Dynamics NAV 5.0- tai sitä aikaisemmasta versiosta.|Käytä vain, jos haluat sallia kaikkien tai joidenkin kohteiden ylittää uusintatilauspisteen.|  
|Oletusvaimentimen jakso|Valitse 1D tai 5D .<br /><br /> Jos et ole aiemmin käyttänyt ohjelman [!INCLUDE[d365fin](includes/d365fin_md.md)] suunnittelutoimintoa, määritä pidempi jakso.|Kun käyttäjät tuntevat toimintosanomien eri syyt, lyhennä puskuriaikaa antaaksesi lisää muutosehdotuksia.|  
|Oletuspuskurimäärä-%|Määritä 5-20% nimikkeen eräkoosta.||  

## <a name="see-also"></a>Katso myös  
 [Asetukset - parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md)   
 [Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
 [Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla](set-up-complex-application-areas-using-best-practices.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
