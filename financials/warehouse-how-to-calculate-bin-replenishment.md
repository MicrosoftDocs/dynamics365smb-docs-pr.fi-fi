---
title: "Varastopaikan täydennyksen laskeminen | Microsoft Docs"
description: "Kun sijainti on määritetty käyttämään ohjattua hyllytystä ja poimintaa, hyllytysmallin sijainnin painopisteet otetaan huomioon kun vastaanottoja hyllytetään."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e667ca56aa22fafc7fe6d0a4880c419a4272db26
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="calculate-bin-replenishment"></a>Laske var.paikan täydennys
Kun sijainti on määritetty käyttämään ohjattua hyllytystä ja poimintaa, hyllytysmallin sijainnin painopisteet otetaan huomioon kun vastaanottoja hyllytetään. Prioriteetteja ovat varastopaikan sisällön pienin ja suurin määrä, joka on vahvistettu tietylle varastopaikalle, sekä varastopaikan luokittelut. Tästä seuraa, että jos nimikkeitä saapuu tasaiseen tahtiin, eniten käytetyt poimintavarastopaikat täyttyvät samalla, kun niitä tyhjennetään.  

Varasto ei kuitenkaan aina saavu tasaiseen tahtiin. Nimikkeitä ostetaan joskus suurissa määrissä, jotta yritys saisi alennuksen, tai tuotantoyksikkö voi tuottaa suuren määrän yhtä nimikettä, jotta saavutettaisiin alhainen yksikköhinta. Sitten taas nimikkeitä ei vastaanoteta fyysiselle varastolle pitkään aikaan, ja fyysisessä varastossa täytyy ajoittain siirtää nimikkeitä poimintavarastopaikkoihin irtotavaran varastointialueilta.  

Voi olla myös niin, että fyysiselle varastolle odotetaan uutta varastoa saapuvaksi lähiaikoina, ja irtotavaran varastointialue halutaan tyhjentää nimikkeistä ennen kuin uudet tavarat saapuvat.  

Jos olet määritellyt irtotavaran varastopaikoille varastopaikan tyypin, jonka toimintona on vain **Hyllytys** (varastopaikalla ei ole rastia **Poiminta**-toiminnon kohdalla), poimintavarastopaikat täytyy aina pitää täydennettyinä, koska ohjelma ei ehdota varaston hyllytystä varaston poiminnalle.  

## <a name="to-replenish-pick-bins"></a>Poiminnan varastopaikkojen täydentäminen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Siirtotyökirja** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa raportin pyyntösivu valitsemalla **Laske var.paikan täydennys** -toiminto.  
3.  Täytä eräajon pyyntöikkuna rajoittaaksesi niiden täydennysehdotusten laajuutta, jotka ohjelma laskee. Sinua voivat kiinnostaa esimerkiksi tietyt nimikkeet, alueet tai varastopaikat.  
4.  Valitse **OK**-painike. Napsauta OK ja ohjelma luo rivejä täydennyssiirtoja varten, jotka tulee suorittaa niiden sääntöjen mukaan, jotka on määritetty varastopaikoille ja varastopaikkojen sisällölle (varastopaikkojen sisältämille nimikkeille).  
5.  Jos haluat suorittaa kaikki ehdotetut täydennykset, valitse **Luo siirto** -toiminto. Työntekijät voivat nyt etsiä ohjeet **Var.siirrot**-valikkoaiheesta, suorittaa ja rekisteröidä ne.  
6.  Jos haluat suorittaa vain joitain ehdotuksista, poista vähemmän tärkeät rivit ja luo sitten siirto.  

Seuraavan kerran kun lasket varastopaikan täydennystä, ohjelma luo uudelleen poistamasi ehdotukset, jos ne ovat silloin vielä voimassa.  

> [!NOTE]  
>  Oletetaan, että nimike täyttää seuraavat ehdot:  
>   
>  -   Nimikkeellä on vanhentumispäivämäärä.  
> -   Sijaintikortin **FEFO-poiminta**-kentässä valitaan.  
> -   Käytät **Laske var.paikan täydennys**-toimintoa.  
>   
>  Tällöin **Alue koodista**- ja  **Var.paikasta**-kentät jätetään tyhjiksi, sillä nimikkeiden siirron lähtökohdan laskeva algoritmi käynnistyy vain, kun käytät **Luo siirto** -toimintoa.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[FEFO-poiminta](warehouse-picking-by-fefo.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
