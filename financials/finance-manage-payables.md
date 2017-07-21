---
title: Ostovelkojen hallinta| Microsoft Docs
description: "Yleiskatsaus tavoista, joilla Financials auttaa hallitsemaan ostovelkoja, kuten toimittajamaksuja, lainoja, velkaa ja erääntyvää saldoa."
services: project-madeira
documentationcenter: 
author: bholtorf
manager: edupont
editor: 
ms.service: dynamics365-financials
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 859647435fe3a418761f67c9067314939c734519
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a>Ostovelkojen hallinta
[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] sisältää kaiken, mitä tarvitset ostoreskontran tehokkaaseen hallintaan.  

## <a name="payments"></a>Maksut
Sen avulla on helppo priorisoida maksut, ottaa huomioon erääntymismaksut ja käsitelle aikaisin suoritettujen maksujen alennukset.

Voit kirjata maksut yleiseen päiväkirjaan ja tulostaa sitten sekit ennen maksupäiväkirjan kirjaamista.

Voit kohdistaa maksut sulkemaan laskut maksun kirjaamisen yhteydessä tai kirjaamisen jälkeen. Toimittajalle (**toimittajakortissa**) määritetty **Kohdistustapa** määrittää, kohdistetaanko maksu manuaalisesti vai automaattisesti. Voit aina kohdistaa tapahtumia manuaalisesti. Jos toimittajan kohdistustapa on **Kohdista vanhimpaan** etkä määritä asiakirjaa, johon maksu kohdistetaan, maksu kohdistetaan toimittajan vanhimpaan avoinna olevaan tapahtumaan.

## <a name="suggest-vendor-payments"></a>Ehdota toimittajamaksuja
[!INCLUDE[d365fin](includes/d365fin_md.md)] voi ehdottaa eri maksuja toimittajille, kuten maksuja, jotka erääntyvät pian, ja maksuja, joista voi saada alennuksen. Maksuehdotus voi ottaa huomioon summan, jonka määrität saatavilla olevina varoina maksuihin, ja kelpoisuuden maksualennuksiin.

## <a name="issue-checks"></a>Sekkien myöntäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)]issa sekit voi myöntää toimittajille manuaalisesti ja sähköisesti. Kumpikin tehdään **Maksupäiväkirjat**-ikkunassa, jossa voit myös mitätöidä sekkejä ja tarkastella sekkitapahtumia.

## <a name="export-payments-to-a-bank-file"></a>Maksujen vienti pankkitiedostoon
Kun olet valmis maksamaan toimittajille, voit viedä tiedoston päiväkirjan riveiltä **Maksupäiväkirja**-ikkunassa maksutietojen kanssa. Voit sitten ladata tiedoston verkkopankkiin rahansiirtojen käsittelyä varten.

Jos et halua kirjata viedyn maksun maksupäiväkirjan riviä, koska odotat esimerkiksi pankin vahvistavan tapahtuman, voit poistaa päiväkirjan rivin. Kun luot myöhemmin maksupäiväkirjan rivin, jolla maksetaan jäljellä oleva laskun summa, **Viety summa yhteensä** -kenttä näyttää, kuinka paljon maksun summasta on jo viety. Saat lisätietoja viedystä kokonaissummasta valitsemalla **Hyvityksen siirron rekisterimerkinnät** -painikkeen.

Jos odotat maksujen kirjaamista, kunnes pankki vahvistaa tapahtumien käsittelyn, voit estää avoimien asiakirjojen maksujen uudelleenviennin vahingossa kahdella tavalla:  

* Voit lajitella maksupäiväkirjan ehdotettujen maksurivien kohdalla joko **Viety maksutiedostoon**- tai **Viety summa yhteensä** -sarakkeen mukaan ja sitten poistaa maksuehdotukset avoimilta laskuilta, jotka on jo maksettu ja joita et halua maksaa.

    **Huomautus** Olet ehkä lisännyt nämä sarakkeet luetteloon. Lisätietoja on kohdassa [Käyttäjän mukautus](ui-user-personalization.md).  
* Vaihtoehtoisesti voit määrittää **Ehdota toimittajamaksuja** -eräajossa, jossa määrität maksupäiväkirjaan sisällytettävät maksut, että vietyjen maksujen päiväkirjarivejä ei lisätä valitsemalla **Ohita viedyt maksut** -valintaruudun.

## <a name="see-also"></a>Katso myös
[Maksutavat](finance-payment-methods.md)  
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

