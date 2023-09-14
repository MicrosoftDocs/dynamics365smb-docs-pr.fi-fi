---
title: Rakennetiedot – nimikkeen seurannan rakenne
description: 'Tässä aiheessa käsitellään Business Centralin nimikkeen seurannan taustalla olevaa rakennetta, kun se kehittyy tuoteversioiden kautta.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item, tracking, tracing'
ms.date: 06/08/2021
ms.author: bholtorf
---
# Rakennetiedot: nimikkeen seurannan rakenne

[!INCLUDE[prod_short](includes/prod_short.md)]in nimikeseuranta alkoi versiossa [!INCLUDE [navnow_md](includes/navnow_md.md)]. Nimikeseurantatoiminto on erillinen objektirakenne, jossa on tarkkoja linkkejä kirjattuihin asiakirjoihin ja nimiketapahtumiin. Se on myös integroitu varausjärjestelmään, joka käsittelee varaukset, tilausten seurannan ja toiminnon viestinnän. Lisätietoja on tarjonnan suunnittelun rakennetietojen kohdassa [Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys](design-details-reservation-order-tracking-and-action-messaging.md).  

Tämä rakenne sisältää järjestelmän kaikkien saatavuuslaskelmien nimikkeen seurantatapahtumat yhteensä. Näitä ovat esimerkiksi suunnittelu, valmistus ja varastointi. Sarja- ja eränumeroita käytetään nimiketapahtumiin varmistamaan historiatietojen yksinkertainen käyttö nimikkeenseurantatarkoituksessa. Vuoden 2021 1. julkaisuaallossa [!INCLUDE [prod_short](includes/prod_short.md)]in nimikeseuranta sisältää pakettinumerot.  

Varausjärjestelmä käsittelee sarja-, erä- ja pakettinumeroiden lisäksi pysyviä nimikemääritteitä samalla, kun järjestelmä käsittelee tarjonnan ja kysynnän välisiä katkonaisia linkkejä tilauksen seurantatapahtumien ja varaustapahtumien muodossa. Toinen sarja- tai eränumeroiden erilaisuus verrattuna tavanomaisiin varaustietoihin on se, että ne voidaan kirjata osittain tai kokonaan. Tämän vuoksi **Varaustapahtuma**-taulukko (T337) toimii nyt liittyvän taulukon eli **Seurannan määrittely** -taulukon (T336) kanssa. Se hallitsee ja näyttää aktiivisten ja kirjattujen nimikkeen seurantamäärien summat. Lisätietoja on kohdassa [Rakennetiedot: aktiivisen nimikkeen seurantatapahtumat verrattuna historiallisen nimikkeen seurantatapahtumiin](design-details-active-versus-historic-item-tracking-entries.md).  

Seuraavassa kaaviossa on yleiskuva [!INCLUDE[prod_short](includes/prod_short.md)]in nimikkeen seurantatoiminnon rakenteesta.  

![Esimerkki nimikeseurannan työnkulusta.](media/design_details_item_tracking_design.png "Esimerkki nimikkeen seurannan prosessista")  

Päätiliöintiobjekti on suunniteltu uudelleen käsittelemään ainutlaatuista asiakirjarivin aliluokitusta sarja- tai eränumeroiden muodossa. Erityiset suhdetaulukot on lisätty luomaan yhdeltä monelle -suhteita tiliöityjen asiakirjojen välillä ja niiden jaettujen nimikkeiden lokikirjaukset sekä arvojen lokikirjaukset on lisätty.  

Codeunit 22 **Nimikepäiväkirja – kirjausrivi** jakaa kirjauksen asiakirjarivillä määritettyjen nimikkeen seurantanumeroiden perusteella. Jokainen rivin yksilöllinen seurantanumero luo kullekin nimikkeelle oman nimiketapahtuman. Tämä tarkoittaa sitä, että kirjatusta asiakirjarivistä määritettyihin nimiketapahtumiin muodostettu linkki on nyt yhden suhde moneen. Seuraavat nimikeseurannan suhdetaulukot käsittelevät tätä suhdetta.  

|Kenttä|Kuvaus|  
|---------------|---------------------------------------|  
|**Nimiketapahtuman suhde** (T6507)|Liittää lähetetyt tai vastaanotetut rivit nimikkeen pääkirjan kirjauksiin|  
|**Arvotapahtuman viittaus** (T6508)|Liittää laskutetut rivit arvokirjauksiin|  

Lisätietoja on kohdassa [Rakennetiedot: Nimikeseurannan kirjausrakenne](design-details-item-tracking-posting-structure.md).  

## Katso myös

[Rakennetiedot: Nimikkeen seuranta](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
