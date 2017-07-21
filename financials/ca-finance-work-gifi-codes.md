---
title: Kanadalaiset GIFI-koodit | Microsoft Docs
Description: "Voit määrittää Kanadassa GIFI-koodeja (General Index of Financial Information) ja liittää ne kirjaustileihin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-gifi-codes-in-canada"></a>Toimintaohje: Kanadan GIFI-koodien käyttäminen
Taloustiedot voivat sisältää kirjanpitotilejä, raportteja, tuloslaskelmia, taseita ja jakamattoman voiton tiliotteita. Taloustiedot luokitellaan koodien avulla. Viranomaiset käyttävät koodeja tietojen käsittelemiseen, sähköiseen arkistoimiseen ja verotietojen sähköiseen tarkistamiseen. Koodit auttavat myös tilastotietojen tehokkaassa käsittelyssä, koska taloustiedot ovat helpommin käytettävissä. Lisätietoja on [Kanadan CRA:n (Canada Revenue Agency) verkkosivustossa](http://www.cra-arc.gc.ca/).

Kanadan CRA käyttää tilinpäätösten kirjanpitotietojen yleisindeksikoodeja eli GIFI (General Index of Financial Information) -koodeja talous- ja verotietojen sähköisessä keräämiseen, tarkistamiseen ja käsittelyyn. GIFI-koodit kannattaa liittää vain kirjaustileihin niin, että verojen valmistelussa käytettävä ohjelmisto suorittaa summauksen.

Kun tili on liitetty GIFI-koodiin, kyseistä koodia käytetään verotoimiston raporteissa. Sama GIFI-koodi voi olla useilla tileillä, mutta tilillä voi olla vain yksi GIFI-koodi.

Saldotiedot voidaan viedä GIFI-koodin avulla, ja viety tiedosto voidaan tallentaa Exceliin. Tämä on hyödyllistä silloin, kun tietoja siirretään verojen valmistelussa käytettävään ohjelmistoon.

## <a name="to-set-up-gifi-codes"></a>GIFI-koodien määrittäminen
Dynamics NAV -ohjelmassa GIFI-koodit on määritettävä kirjanpitotileille, raporteille, taseille, tuloslaskelmille ja jakamattoman voiton tiliotteille.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **GIFI-koodit** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **GIFI-koodit**-ikkunassa **Uusi**-toiminto.
3. Määritä GIFI-koodit täyttämällä kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a>GIFI-koodien liittäminen kirjanpitotileihin
Voit raportoida taloustiedot GIFI-koodien mukaan, kun kukin GIFI-koodi on liitetty tilikartan asianmukaiseen tiliin.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse asiaankuuluva kirjanpitotili ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Kustannuslaskenta**-pikavälilehden **GIFI-koodi**-kenttään asiaankuuluva GIFI-koodi.

## <a name="to-view-account-balances-using-the-gifi-code-report"></a>Tilien saldojen tarkasteleminen GIFI-koodiraportin avulla
Voit tarkastella tilien saldoja GIFI-koodin mukaan **Tilien saldot GIFI-koodin mukaan** -raportin avulla.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Tilien saldot GIFI-koodin mukaan** ja valitse sitten aiheeseen liittyvä linkki.
2. Määritä raporttiin sisällytettävät tiedot täyttämällä kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Tulosta**- tai **Esikatsele**-painike.

## <a name="to-export-balance-information-using-gifi-codes"></a>Saldotietojen vieminen GIFI-koodien avulla
Voit viedä saldotiedot GIFI-koodien avulla ja tallentaa viedyn tiedoston Excelissä. Voit muokata tiedostoa tai tallentaa tai poistaa sen. Tiedoston avulla voit siirtää tietoja verojen valmistelussa käytettävään ohjelmistoon.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **GIFI-koodit** ja valitse sitten aiheeseen liittyvä linkki.
2. Määritä Exceliin vietävät tiedot täyttämällä kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **OK**-painike.

> [!NOTE]  
>   Excel-tiedostolla on seuraavat ominaisuudet:

* Saldo pyöristetään lähimpään prosenttilukuun, mutta solun arvona pidetään pääkirjanpidossa oleva prosenttiluku.
* Negatiiviset luvut esitetään suluissa olevina positiivisina lukuina. Luku -123 on siis (123).

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)   
[Rahoituksen määrittäminen](finance-setup-finance.md)

