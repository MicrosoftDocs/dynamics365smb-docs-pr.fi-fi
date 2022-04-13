---
title: Markkinointikampanjoiden määrittäminen Business Central -sovelluksessa | Microsoft Docs
description: Ohjeaiheessa käsitellään, miten markkinointikampanjat määritetään ja toteutetaan Business Central -sovelluksessa ja miten ne auttavat tunnistamaan ja houkuttelemaan prospekteja sekä säilyttämään asiakkaita.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ab9ad6e770e1a8c1c6ebc9e20d00e9f72ebec7c6
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518963"
---
# <a name="managing-marketing-campaigns"></a>Markkinointikampanjoiden hallinta
Vahvan markkinointisuunnitelman avulla yritys voi tunnistaa, houkutella ja säilyttää asiakkaita. Markkinointisuunnitelma sisältää erilaisia kampanjoita ja muita myyntiin ja markkinointiin liittyviä vuorovaikutustapoja. Kampanjan suunnitteluvaiheessa on päätettävä kohteena olevat kontaktit, kampanjan tyyppi (kuten messut tai suoramainonta) ja myyjien tehtävät.

Jokainen kampanja koostuu eri toiminnoista tai tehtävistä. Voit yhdistää toiminnoissa useita tehtäviä, kuten kutakin vaihetta koskeva tehtävän. Toiminnon tehtävät liittyvät toisiinsa päivämääräkaavan avulla. Yksittäiset tehtävät voidaan määrittää vain myyjille. Toiminnot voidaan määrittää mahdollisuuksille, myyjille, myyjäryhmille tai kontakteille. Lisätietoja on ohjeaiheessa [Mahdollisuuden myyntisyklien ja syklin vaiheiden määrittäminen](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="defining-individual-campaigns"></a>Yksittäisten kampanjoiden määrittäminen
Ennen kampanjan luomista on määritettävä *kampanjan tilakoodit*. Näiden koodien avulla kampanjoiden hallinta on helpompaa, koska kampanjalle määritetään tila. Kun kampanja etenee, näet nopeasti, missä vaiheessa kampanja on ja mikä on seuraava vaihe. Kampanjan tilakoodit määritetään **Kampanjan tila** -sivulla.

Voit luoda jokaiselle seurattavalle kampanjalle kampanjan kortin. Näiden korttien avulla voit myös tarkastella kampanjoiden yleistietoja.
Voit poistaa kampanjatapahtumia, esimerkiksi jos tapahtumassa on kyse toiminnosta, jotka on peruutettu. Vain peruutettuja kampanjatapahtumia voi poistaa.

### <a name="selecting-the-target-audience"></a>Kohderyhmän valitseminen
Kampanjan luomisen jälkeen voit luoda kampanjassa käytettävät segmentit, jotka määrittävät kampanjan kohdeyleisön. Lisätietoja on myös kohdassa [Segmenttien hallinta](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Alennusprosenttien rekisteröiminen
Kun olet asettanut kampanjan, päättänyt mitä segmenttejä haluat kampanjan kattavan ja määrittänyt aloitus- ja loputuspäivämäärät, rekisteröit alennusprosentin, jonka asiakkaat saavat yksittäisille nimikkeille **Myyntirivialennukset**-sivulla. Voit rekisteröidä myös rivien yksittäisten nimikkeiden myyntihinnat **Myyntihinnat**-sivulla. Voit käyttää molempia sivuja kampanjan kortista.

 Kun olet asettanut myyntihinnat/rivialennukset ja kampanjakortin segmentit, sinun tulee aktivoida ne niin, että kampanjan hinnat/alennukset tulevat esille myös riveille.

> [!NOTE]  
>   Voit aktivoida myyntihinnat ja rivialennukset määrittämällä, onko kampanjan kohteena koko segmentti vai vain osa kontakteista. Jos myyntihinta/rivialennus kattaa kaikki segmentin kontaktit, lisää valintamerkki **Segmentti**-kortin **Kampanja**-pikavälilehden **Kampanjan kohde** -kenttään.

Jos myyntihintaa tai rivialennuksia ei tarjota segmentin kaikille kontakteille, voit poistaa valintamerkin kyseisten kontaktien **Kampanjan kohde** -kentästä. Jos tämä kenttä ei ole näkyvissä, voit lisätä sen näkymään. Lisätietoja on kohdassa [Työtilan mukauttaminen](ui-personalization-user.md).

## <a name="conducting-campaigns"></a>Kampanjoiden toteuttaminen
Kaikki kampanjan aikainen kontaktin tai segmentin kanssa tapahtuva yhteydenpito tallennetaan. Tällä tavoin saat käyttöösi kampanjaa sekä kustannuksia ja onnistumisprosentteja koskevia tilastotietoja ja muita tietoja.

Myyjät hoitavat kampanjoita, ja sinun onkin luotava kutakin tehtävää vastaa toiminto ja määritettävä se soveltuvalle myyjälle. Lisätietoja on ohjeaiheessa [Mahdollisuuden myyntisyklien ja syklin vaiheiden määrittäminen](marketing-how-setup-opportunity-sales-cycles-stages.md).

## <a name="see-also"></a>Katso myös
[Kontaktien hallinta](marketing-contacts.md)  
[Segmenttien hallinta](marketing-segments.md)  
[Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md)  
[Business Centralin käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]