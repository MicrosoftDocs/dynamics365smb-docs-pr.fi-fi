---
title: Rakennetiedot – Nimikeseurannan rakenne | Microsoft Docs
description: Tässä aiheessa käsitellään Business Central -sovelluksen nimikeseurannan rakennetta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87c85de9f501e093679512b709841d0027fe17bf
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751328"
---
# <a name="design-details-item-tracking-design"></a>Rakennetiedot: nimikkeen seurannan rakenne
[!INCLUDE[prod_short](includes/prod_short.md)] 2.60:n ensimmäisessä nimikeseurantaversiossa sarja- tai eränumerot tallennettiin suoraan nimiketapahtumiin. Tämä rakenne tarjosi täydet saatavuustiedot ja yksinkertaisen aiempien tapahtumien seurannan, mutta siitä puuttui joustavuus ja toiminnallisuus.  

[!INCLUDE[prod_short](includes/prod_short.md)] 3.00:sta alkaen nimikkeen seurantatoiminto oli erillisessä objektirakenteessa, jossa oli monimutkaisia linkkejä kirjattuihin asiakirjoihin ja nimiketapahtumiin. Tämä rakenne oli joustava ja siinä oli paljon toimintoja, mutta nimikkeiden seurantatapahtumat eivät olleet kokonaan mukana saatavuuden laskennoissa.  

[!INCLUDE[prod_short](includes/prod_short.md)] 3.60:sta alkaen nimikeseurantatoiminto on liitetty varausjärjestelmään, joka käsittelee varauksen, tilausseurannan ja toiminnan viestit. Katso lisätiedot kohdasta Rakennetiedot: tarjonnan suunnittelu kohta Rakennetiedot: varaus, tilauksen seuranta ja toimenpiteiden viestitys.  

Tämä viimeisin rakenne sisältää järjestelmän kaikkien saatavuuslaskelmien nimikkeen seurantatapahtumat yhteensä. Näitä ovat esimerkiksi suunnittelu, valmistus ja varastointi. Vanha konsepti sarja- ja eränumeroiden viemisestä nimikkeen pääkirjan kirjauksiin on palautettu, jotta varmistetaan historiatietojen yksinkertainen käyttö nimikkeenseurantatarkoituksessa. [!INCLUDE[prod_short](includes/prod_short.md)] 3.60:n nimikeseurannan parannuksiin liittyen varausjärjestelmä laajennettiin tilausverkon ulkopuolisiin objekteihin, kuten kirjauskansioihin, laskuihin ja hyvityslaskuihin.  

Varausjärjestelmä käsittelee sarja- ja eränumeroiden lisäksi pysyviä nimikemääritteitä samalla, kun järjestelmä käsittelee tarjonnan ja kysynnän välisiä katkonaisia linkkejä tilauksen seurantatapahtumien ja varaustapahtumien muodossa. Toinen sarja- tai eränumeroiden erilaisuus verrattuna tavanomaisiin varaustietoihin on se, että ne voidaan kirjata osittain tai kokonaan. Tämän vuoksi **Varaustapahtuma**-taulukko (T337) toimii nyt liittyvän taulukon eli **Seurannan määrittely** -taulukon (T336) kanssa. Se hallitsee ja näyttää aktiivisten ja kirjattujen nimikkeen seurantamäärien summat. Lisätietoja on kohdassa [Rakennetiedot: aktiivisen nimikkeen seurantatapahtumat verrattuna historiallisen nimikkeen seurantatapahtumiin](design-details-active-versus-historic-item-tracking-entries.md).  

Seuraavassa kaaviossa on yleiskuva [!INCLUDE[prod_short](includes/prod_short.md)]in nimikkeen seurantatoiminnon rakenteesta.  

![Esimerkki nimikkeen seurannan prosessista](media/design_details_item_tracking_design.png "Esimerkki nimikkeen seurannan prosessista")  

Päätiliöintiobjekti on suunniteltu uudelleen käsittelemään ainutlaatuista asiakirjarivin aliluokitusta sarja- tai eränumeroiden muodossa. Erityiset suhdetaulukot on lisätty luomaan yhdeltä monelle -suhteita tiliöityjen asiakirjojen välillä ja niiden jaettujen nimikkeiden lokikirjaukset sekä arvojen lokikirjaukset on lisätty.  

Codeunit 22 **Nimikepäiväkirja – kirjausrivi** jakaa kirjauksen asiakirjarivillä määritettyjen nimikkeen seurantanumeroiden perusteella. Jokainen rivin yksilöllinen seurantanumero luo kullekin nimikkeelle oman nimiketapahtuman. Tämä tarkoittaa sitä, että kirjatusta asiakirjarivistä määritettyihin nimiketapahtumiin muodostettu linkki on nyt yhden suhde moneen. Seuraavat nimikeseurannan suhdetaulukot käsittelevät tätä suhdetta.  

|Kenttä|Kuvaus|  
|---------------|---------------------------------------|  
|**Nimiketapahtuman suhde** (T6507)|Liittää lähetetyt tai vastaanotetut rivit nimikkeen pääkirjan kirjauksiin|  
|**Arvotapahtuman viittaus** (T6508)|Liittää laskutetut rivit arvokirjauksiin|  

Lisätietoja on kohdassa [Rakennetiedot: Nimikeseurannan kirjausrakenne](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: Nimikkeen seuranta](design-details-item-tracking.md)
