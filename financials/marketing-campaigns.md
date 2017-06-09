---
title: "Markkinointikampanjoiden määrittäminen Financialsissa | Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten markkinointikampanjat määritetään ja toteutetaan Dynamics 365 for Financialsissa"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/08/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8f616382e28e29aab1ce7d9b45b8efb4ad374b96
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="managing-marketing-campaigns"></a>Markkinointikampanjoiden hallinta
Vahvan markkinointisuunnitelman avulla yritys voi tunnistaa, houkutella ja säilyttää asiakkaita. Markkinointisuunnitelma sisältää erilaisia kampanjoita ja muita myyntiin ja markkinointiin liittyviä vuorovaikutustapoja. Kampanjan suunnitteluvaiheessa on päätettävä kohteena olevat kontaktit, kampanjan tyyppi (kuten messut tai suoramainonta) ja myyjien tehtävät.

<!-- Each campaign consists of various activities or to-dos. Activities are large tasks that can be broken down into several smaller tasks or to-dos. To-dos are individual or team tasks that can be created within activities or individually and then be assigned to individual salespeople or groups of salespeople.-->

## <a name="defining-individual-campaigns"></a>Yksittäisten kampanjoiden määrittäminen
Ennen kampanjan luomista on määritettävä *kampanjan tilakoodit*. Näiden koodien avulla kampanjoiden hallinta on helpompaa, koska kampanjalle määritetään tila. Kun kampanja etenee, näet nopeasti, missä vaiheessa kampanja on ja mikä on seuraava vaihe. Kampanjan tilakoodit määritetään **Kampanjan tila** -ikkunassa.

Voit luoda jokaiselle seurattavalle kampanjalle *kampanjan kortin*. Näiden korttien avulla voit myös tarkastella kampanjoiden yleistietoja.
Voit poistaa kampanjatapahtumia, esimerkiksi jos tapahtumassa on kyse toiminnosta, jotka on peruutettu. Vain peruutettuja kampanjatapahtumia voi poistaa.

### <a name="selecting-the-target-audience"></a>Kohderyhmän valitseminen
Kampanjan luomisen jälkeen voit luoda kampanjassa käytettävät segmentit, jotka määrittävät kampanjan kohdeyleisön. Lisätietoja on myös kohdassa [Segmenttien hallinta](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Alennusprosenttien rekisteröiminen
Kun olet asettanut **kampanjan**, päättänyt mitä segmenttejä haluat kampanjan kattavan ja asettanut Aloitus- ja Lopetuspvm:t, rekisteröit alennus -%, jonka asiakkaat saavat yksittäisille nimikkeille Myyntirivialennukset -ikkunassa. Voit rekisteröidä myös rivien yksittäisten nimikkeiden myyntihinnat **Myyntihinnat**-ikkunassa. Voit käyttää molempia ikkunoita kampanjan kortista.

 Kun olet asettanut myyntihinnat/rivialennukset ja kampanjakortin segmentit, sinun tulee aktivoida ne niin, että kampanjan hinnat/alennukset tulevat esille myös riveille.

> [!NOTE]  
>  Voit aktivoida myyntihinnat ja rivialennukset määrittämällä, onko kampanjan kohteena koko segmentti vai vain osa kontakteista. Jos myyntihinta/rivialennus kattaa kaikki segmentin kontaktit, lisää valintamerkki **Segmentti**-kortin **Kampanja**-pikavälilehden **Kampanjan kohde** -kenttään.
Jos myyntihintaa tai rivialennuksia ei tarjota segmentin kaikille kontakteille, voit poistaa valintamerkin kyseisten kontaktien **Kampanjan kohde** -kentästä. Jos tämä kenttä ei ole näkyvissä, voit lisätä sen näkymään. Lisätietoja on kohdassa [Käyttäjän mukautus](ui-user-personalization.md).

<!-- ## Conducting campaigns
As a campaign runs, all interactions with your contacts, or segment, are recorded so that you can get statistics and other information about the costs and success rates of the campaign.

Campaigns are conducted by salespeople, and you must create activities to represent each task and assign them to the relevant salespeople.  -->

## <a name="see-also"></a>Katso myös
[Kontaktien hallinta](marketing-contacts.md)  
[Segmenttien hallinta](marketing-segments.md)  
[Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md)  
[Financialsin käyttäminen](ui-work-product.md)  

