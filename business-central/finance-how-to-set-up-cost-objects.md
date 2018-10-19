---
title: "Kustannuskohteiden määrittäminen | Microsoft Docs"
description: "Lisätietoja yleisen päiväkirjan dimensioita muistuttavien kustannuskohteiden määrittämisestä"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3eb90611939dce2134d9413812918c2afb82c083
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-cost-objects"></a>Kustannuskohteiden määrittäminen
Kustannuskohteet ovat yrityksen projekteja, tuotteita tai palveluja. Kustannuskohdekaavio vastaa pääkirjanpidon dimensiotietoja. Voit määrittää kustannuskohdekaavion seuraavilla tavoilla:  

* Siirrä dimensioarvot pääkirjanpidosta kustannuskohdekaavioon. Siirron jälkeen voit tehdä tarvittavat muutokset.  
* Luo uusi kustannuskohteen kaavio, joka on riippumaton pääkirjanpidosta, tai lisää uusi kustannuskohde nykyiseen kustannuskohteiden kaavioon. Sinun on luotava kukin kustannuskohde erikseen.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Siirrä dimensioarvot pääkirjanpidosta kustannuskohdekaavioon  
1.  Määritä dimensio kustannuskohteen dimensioksi **Päivitä KL-dimensiot** -ikkunassa. Vain tämän dimension arvot siirretään.  
2.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kustannuskohdekartta** ja valitse sitten liittyvä linkki.  
3.  Valitse **Nouda kustannuskohteet dimensiosta** -toiminto, jolla dimensioarvot siirretään kustannuskohdekaavioon. Toiminto siirtää kohdassa 1 määritetyt dimensioarvot.  

    > [!NOTE]  
    >  Voit määrittää **Tasaa kustannuskohteen dimensio** -kentän määrittämään yksisuuntaisen dimensioarvojen synkronoinnin kirjanpidosta kustannuskohdekarttaan. Et voi määrittää kaavion kustannuskohteiden synkronointia dimensioarvoihin pääkirjanpidossa.  

Kustannuskohdekaavio sisältää nyt kaikki pääkirjanpidossa määritetyt dimensioarvot, mukaan lukien otsikot ja välisummat.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-window"></a>Uuden kustannuskohteen luominen Kustannuskohdekartta-ikkunassa  
Voit määrittää ja ylläpitää kustannuskohteita joko **Kustannuskohteen kortti** -kortissa tai **Kustannuskohdekartta**-ikkunassa. Tässä toimenpiteessä määrität kustannuskohteet **Kustannuskohdekartta**-ikkunassa.  

1.  Avaa **Kustannuskohdekartta**-ikkuna muokkaustilassa.  
2.  Syötä kustannuskohdekoodi **Koodi**-kenttään. Kaikilla kustannuskohteilla on oltava koodi.  
3.  Syötä kustannuskohteen nimi **Nimi**-kenttään.  
4.  Valitse avattava nuoli **Rivityyppi**-kentässä määrittämään kustannuskohteen tarkoitus.  

    * Jos kustannuskohteiden rivityyppi on **Yhteensä**, anna arvo **Summan lähde/kohde** -kenttään. Käytä **tai**-operaattoria, joka on pystysuora viiva (**&#124;**) kustannuskohteiden alueiden määrittämiseen.  
    * Jos kustannuskohteiden rivityyppi on **Loppusumma**, kenttä täytetään automaattisesti, kun käytössä on sisennystoiminto.  
5.  Täytä **Lajittelujärjestys**-kentän tiedot.  
6.  Napsauta seuraavaa tyhjää riviä uuden kustannuskohteen määrittämistä varten. Toista sitten vaiheet 2-5.  
7.  Kun olet määrittänyt kaikki kustannuskohteet, valitse **Sisennä kustannuskohteet** -toiminto. Valitse **Kyllä**-painike.  

> [!IMPORTANT]  
>  Jos olet antanut määritelmiä **Loppusumma**-kustannuskohteiden **Summan lähde/kohde** -kenttiin ennen sisennyksen suorittamista, määritelmät on annettava uudelleen. Toiminto korvaa kaikki **Loppusumma**-kentän arvot.  

## <a name="see-also"></a>Katso myös  
[Kustannuslaskenta](finance-manage-cost-accounting.md)  
[Kustannuspaikkojen ja kustannuskohteiden määrittäminen tilikarttaan](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Kustannustyypin, kustannuspaikan ja kustannusobjektin saldot](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md)   
[Termit kustannuslaskennassa](finance-terminology-in-cost-accounting.md)   
[Tietoja kustannuslaskennasta](finance-about-cost-accounting.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

