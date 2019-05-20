---
title: Yrityksen mukautettujen määrityspakettien luominen | Microsoft Docs
description: Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa. Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0f87e3708802898d1b86dfaae31b37cdee37ff74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244628"
---
# <a name="create-custom-company-configuration-packages"></a>Yrityksen mukautettujen määrityspakettien luominen
Liiketoimintasi kasvaessa tulet todennäköisesti käyttämään yritystyyppejä, joita käytät useimpien asikkaittesi kanssa. Ottamalla huomioon yrityksen kokoonpanopaketit, jotka ovat käytettävissä uudelleen, voit tehostaa toteutusprosessia.  

Yleensä määrityspaketti luodaan toiminta-aluetta kohti. Voit esimerkiksi luoda paketin tuotantotoiminnolle. Niiden avulla voit ottaa käyttöön ja määrittää yrityksen uusia alueita silloin, kun niitä tarvitaan  

Toinen vaihtoehto olisi luoda paketti, joka sisältää taulukot, jotka määrittävät asetukset, esim. seuraavasti:  

-   Käyttöomaisuuden asetukset  
-   Pääkirjanpidon asetukset  
-   Varastonhallinnan asetukset  
-   Tuotannon asetukset  
-   Ostojen ja ostovelkojen asetukset  
-   Kontaktienhallinnan asetukset  
-   Huollon asetukset  
-   Myyntien ja saamisten asetukset  
-   Fyys. varastoinnin asetukset  
-   Yleiset kirjausasetukset  
-   ALV-kirjausten asetukset  
-   Varastokirjauksien asetukset  

Jos haluat nähdä asetustaulukoiden täydellisen luettelon, valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Manuaalinen määritys** ja valitse sitten liittyvä linkki.  

## <a name="to-create-a-custom-company-configuration-package"></a>Yrityksen mukautetun määrityspaketin luominen  
1.  Luo uusi yritys. Lisätietoja on kohdassa [Uusien yritysten luominen Business Centralissa](about-new-company.md).  
3.  Määritä uuden yrityksen asetukset tarvitsemallasi tavalla. Täydennä kaikki pakolliset asetustaulukot.  
4.  Avaa uusi yritys.
5. Avaa **Määritystyökirja**-sivu.  
6.  Lisää työkirjaan taulukot, jotka haluat siirtää toiselle yhtiölle. Määritä työkirjan rivit pakettiin.  
7.  Luo uusi kysely usein käytettyjen asetusten taulukoille.  
8.  Luominen määritysmallit, jotta on helpompi luoda perustiedot, kuten asiakkaat ja nimikkeet.  
9.  Vie paketti .rapidstart-tiedostona.  

## <a name="see-also"></a>Katso myös  
[Yrityksen määrittäminen RapidStart Servicesin avulla](admin-set-up-a-company-with-rapidstart.md)  
[Hallinta](admin-setup-and-administration.md)
