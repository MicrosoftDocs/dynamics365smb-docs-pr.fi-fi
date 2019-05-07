---
title: Kustannuspaikkojen määrittäminen | Microsoft Docs
description: Kustannuspaikat ovat osastoja, jotka ovat vastuussa kustannuksista ja tuloista. Kustannuspaikkakaavio vastaa pääkirjanpidon dimensiotietoja.
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
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 48c1b9800c1e89246ba84122b4af56d75fdf6f9f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2019
ms.locfileid: "922136"
---
# <a name="set-up-cost-centers"></a>Kustannuspaikkojen määrittäminen
Kustannuspaikat ovat osastoja, jotka vastaavat tuloista ja menoista. Kustannuspaikkakaavio vastaa pääkirjanpidon dimensiotietoja. Voit määrittää kustannuspaikkakaavion seuraavilla tavoilla:  

-   Siirrä dimensioarvot pääkirjanpidosta kustannuspaikkakaavioon. Siirron jälkeen voit tehdä tarvittavat muutokset.  
-   Luo uusi kustannuspaikan kaavio, joka on riippumaton pääkirjanpidosta, tai lisää uusi kustannuspaikka nykyiseen kustannuspaikan kaavioon. Sinun on luotava kukin kustannuspaikka erikseen.  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Dimensioarvojen siirtäminen pääkirjanpidosta kustannuspaikkakaavioon  
1.  Määritä dimensio kustannuspaikan dimensioksi **Päivitä kustannuslaskennan dimensiot** -sivulla. Vain tämän dimension arvot siirretään.  
2.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Kustannuspaikkakartta** ja valitse sitten liittyvä linkki.  
3.  Valitse **Toiminnot**-välilehden **Funktiot**-ryhmässä **Nouda kustannuspaikat dimensiosta**, jolloin dimensioarvot siirretään kustannuspaikkakaavioon. Toiminto siirtää kohdassa 1 määritetyt dimensioarvot.  

    > [!NOTE]  
    >  Voit määrittää **Tasaa kustannuspaikan dimensio** -kentän määrittämään yksisuuntaisen dimensioarvojen synkronoinnin kirjanpidosta kustannuspaikkakaavioon. Et voi määrittää kaavion kustannuspaikkojen synkronointia dimensioarvoihin pääkirjanpidossa.  

Kustannuspaikkakaavio sisältää nyt kaikki pääkirjanpidossa määritetyt dimensioarvot, mukaan lukien otsikot ja välisummat.  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>Uuden kustannuspaikan luominen Kustannuspaikkakartta-sivulla  
Voit määrittää ja ylläpitää kustannuspaikkoja joko **Kustannuspaikan kortti** -kortissa tai **Kustannuspaikkakartta**-sivulla. Tässä toimenpiteessä määrität kustannuspaikat **Kustannuspaikkakartta**-sivulla.  

1. Avaa **Kustannuspaikkakartta**-sivu muokkaustilassa.  
2. Anna kustannuspaikkakoodi **Koodi**-kentässä. Kaikilla kustannuspaikoilla on oltava koodi.  
3. Syötä kustannuspaikan nimi **Nimi**-kenttään.  
4. Määritä kustannuspaikan tarkoitus valitsemalla avattava nuoli **Rivityyppi**-kentässä.  

    - **Summa**-tyyppisten kustannuspaikkojen osalta sinun täytyy täyttää **Summausväli**-kenttä. Määritä kustannuspaikkojen alueet **tai**-operaattorin avulla. Se on pystysuora viiva (**&#124;**).  
    - Jos kustannuspaikan rivityyppi on **Loppusumma**, kenttä täytetään automaattisesti, kun käytössä on sisennystoiminto.  
5.  Täytä **Lajittelujärjestys** ja **Kustannuksen alityyppi** -kentät.  
6.  Napsauta seuraavaa tyhjää riviä uuden kustannuspaikan määrittämistä varten. Toista sitten vaiheet 2-5.  
7.  Kun olet määrittänyt kaikki kustannuspaikat, valitse **Sisennä kustannuspaikat** -toiminto. Valitse **Kyllä**-painike.  

> [!IMPORTANT]  
>  Jos olet antanut määritelmiä **Loppusumma**-kustannuspaikkojen **Summausväli**-kenttiin ennen sisennyksen suorittamista, määritelmät on annettava uudelleen. Toiminto korvaa kaikki arvot **Loppusumma** -kentässä.  

## <a name="see-also"></a>Katso myös  
[Kustannuslaskenta](finance-manage-cost-accounting.md)  
[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md)   
[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md)   
[Tietoja kustannuslaskennasta](finance-about-cost-accounting.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
