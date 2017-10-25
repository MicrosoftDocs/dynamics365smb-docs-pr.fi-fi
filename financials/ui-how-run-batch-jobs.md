---
title: "Eräajon luominen ja suorittaminen | Microsoft Docs"
description: "Voit käsitellä ja päivittämää tietoja suorittamalla eräajon esimerkiksi kausiluontoisissa kirjanpitotehtävissä tai laskutoimituksissa."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6844d5fe3efba5349eef166161c5956116bc7fc0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-run-batch-jobs"></a>Eräajojen ajaminen
Eräajo on rutiini, joka käsittelee tietoja erissä, esimerkiksi **Valuuttakurssien muutoksen** eräajo. Ohjelmassa on eräajoja, jotka suorittavat säännöllisiä kirjanpidon toimintoja, kuten tuloslaskelman sulkeminen tilikauden päättyessä. Monet eräajot suorittavat laskutoimituksia. Tällaiset eräajot voivat esimerkiksi laskea viivästyskulut, vaihtokurssien muutoksen tai yksikköhinnat.

Eräajo vastaa raporttia, mutta se päivittää tiedot suoraan saatujen tulosten perusteella sen sijaan, että tulokset tulostettaisiin.

## <a name="to-run-a-batch-job"></a>Eräajon suorittaminen
1. Voit avata kyseisten eräajojen pyyntöikkunan valitsemalla ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvakkeen, antamalla eräajon nimen ja valitsemalla aiheeseen liittyvän linkin.
2. Jos eräajolla on **Vaihtoehdot**-pikavälilehti, voit määrittää eräajon toiminnan täyttämällä kentät.
3. Ikkunassa voi olla yksi tai useita pikavälilehtiä ja suodattimia, joiden avulla voidaan rajoittaa eräajoon sisällytettyjä tietoa. Voit syöttää kriteerin ehdotetuille suodattimille tai lisätä suodattimia.
4. Aloita eräajo valitsemalla **OK**.

## <a name="see-also"></a>Katso myös
[Suodattimen ehtojen antaminen](ui-enter-criteria-filters.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

