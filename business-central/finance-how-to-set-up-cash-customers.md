---
title: Käteisasiakkaiden määrittäminen | Microsoft Docs
description: Tässä ohjeaiheessa käsitellään vaiheet, joilla käteisellä maksava asiakas määritetään.
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
ms.openlocfilehash: d122eaf5e7f898f2497b3cc0848309fb36fa62c1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238824"
---
# <a name="set-up-cash-customers"></a>Käteisasiakkaiden määrittäminen
Laskua ei voi luoda ilman asiakasnumeroa. Näin on, vaikka teet käteismyynnin, eikä asiakastilille ole mitään tallennettavaa.  

## <a name="to-set-up-a-cash-customer"></a>Käteisasiakkaiden määrittäminen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asiakas** ja valitse sitten liittyvä linkki.  
2.  Luo uusi **Asiakkaan** kortti. Lisätietoja on kohdassa [Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md).
3.  Valitse **Nro**-kenttään esimerkiksi **Käteismyynti**.  
4.  Syötä **Nimi**-kenttään esimerkiksi **Käteismyynti**.  
5.  Täytä **Laskutus**-pikavälilehden **Asiakkaan kirjausryhmä**- ja **Ylein. liiketoim. kirjausryhmä** -kentät.  

 Nyt asiakas on määritetty, ja se sisältää riittävästi tietoa laskutusta varten.  

> [!NOTE]  
>  Olet voinut valita kirjausryhmän, jota on käytetty myös kotimaisiin luottomyynteihin. Jos haluat ylläpitää erillistä tietoa käteismyynneistä esimerkiksi erityisellä myynti- tai myyntisaamistilillä, voit määrittää tätä varten ylimääräisen kirjausryhmän.  
>   
>  Myyntisaamistilille täytyy syöttää numero kirjausryhmää varten, vaikka tilin saldo on aina 0 laskun kirjaamisen jälkeen.  

## <a name="see-also"></a>Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Uusien asiakkaiden rekisteröinti](sales-how-register-new-customers.md)    
[Rahoitus](finance.md)  

