---
title: "Rakennetiedot – suunnittelun kohdistustaulukko | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, mitä tapahtuu, kun muutat nimikkeen suunnittelua."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e7591196c3335f7640d37151054b22dd687b36e8
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-planning-assignment-table"></a>Rakennetiedot: suunnittelun kohdistustaulukko
Kaikki nimikkeet tulee suunnitella, mutta nimikkeelle ei ole syytä laskea suunnitelmaa ellei kysyntä- tai tarjontakuvio ole muuttunut edellisen suunnitelman laskemisen jälkeen.  
  
Jos käyttäjä on kirjoittanut uuden myyntitilauksen tai muuttanut olemassa olevaa, suunnitelman uudelleen laskeminen on tarpeellista. Muita syitä ovat muutos ennusteeseen tai haluttu varmuusvaraston määrä. Tuoterakenteen muuttaminen komponentin lisäyksellä tai poistolla ilmaisisi todennäköisesti muutosta, mutta vain komponenttinimikkeelle.  
  
Useiden sijaintien kohdalla, määritys tapahtuu nimikkeen tasolla sijaintiyhdistelmää kohti. Jos esimerkiksi myyntitilaus on luotu vain yhdessä sijainnissa, ohjelma määrittää suunnittelulle tässä tietyssä sijainnissa olevan nimikkeen.  
  
Syy valita nimikkeitä suunnittelua varten on järjestelmän toimintaseikka. Jos nimikkeen kysyntä–tarjonta-mallissa ei ole tapahtunut muutosta, suunnittelujärjestelmä ei ehdota toimenpiteitä. Ilman suunnittelun tehtävää järjestelmän on suoritettava laskennat kaikille nimikkeille suunnitelmaa ja järjestelmän resurssit kuluttavaa tilannetta määritettäessä.  
  
**Suunnittelun tehtävä**-taulukko valvoo kysynnän ja toimituksen tapahtumia ja määrittää sopivat nimikkeet suunnittelua varten. Seuraavia tapahtumia tarkkaillaan:  
  
* Uusi myyntitilaus, ennuste, komponentti, ostotilaus, tuotantotilaus, kokoonpanotilaus tai siirtotilaus.  
* Nimikkeen, määrän, sijainnin, variantin tai päivämäärän muutos myyntitilauksessa, ennusteessa, komponentissa, ostotilauksessa, tuotantotilauksessa, kokoonpanotilauksessa tai siirtotilauksessa.  
* Myyntitilauksen, ennusteen, komponentin, ostotilauksen, tuotantotilauksen, kokoonpanotilauksen tai siirtotilauksen peruutus.  
* Muiden kuin suunniteltujen nimikkeiden kulutus.  
* Muiden kuin suunniteltujen nimikkeiden tuotos.  
* Varaston suunnittelemattomat muutokset.  
  
Näiden suorien tarjonta-kysyntä-siirtojen osalta tilausten seuranta- ja toimenpiteiden viestitysjärjestelmä ylläpitää Suunnittelun tehtävä -taulukkoa ja ilmoittaa suunnittelun syyn toimenpideviestinä.  
  
Seuraavat muutokset päätiedoissa voivat myös aiheuttaa suunnittelun epätasapainon:  
  
* Tilan muutos hyväksytyksi tuotannon tuoterakenteen otsikossa (kaikille tätä otsikkoa käyttäville nimikkeille).  
* Poistettu rivi (alinimike).  
* Tilan muutos hyväksytyksi reitityksen otsikossa (kaikille tätä reititystä käyttäville nimikkeille).  
* Muutokset seuraavissa nimikkeen kortin kentissä.  
* Varmuusvaraston määrä tai varmistuksen läpimenoaika  
* Toimitusajan laskenta.  
* Uusintatilauspiste.  
* Tuotannon tuoterakenteen nro (ja kaikki vanhan tuoterakenteen viitteen alikohteet).  
* Reititysnro  
* Uusintatilauskäytäntö.  
  
Näissä tapauksissa uusi suunnittelun määrityksen hallinta -toiminto ylläpitää taulukkoa ja määrittää suunnittelun syyksi nettomuutoksen.  
  
Seuraavat muutokset eivät aiheuta suunnittelutehtävää:  
  
* Kalenterit  
* Muut suunnitteluparametrit nimikkeen kortilla:  
  
Tuotanto-ohjelman ja tarvelaskennan laskentaa koskevat seuraavat rajoitukset:  
  
* Tuotanto-ohjelma: suunnittelujärjestelmä tarkistaa, että nimikkeellä on tuotantoennuste tai myyntitilaus. Jos ei ole, nimike ei kuulu suunnitelmaan.  
* Tarvelaskenta: jos suunnittelujärjestelmä havaitsee, että tuotanto-ohjelman suunnittelurivi tai tuotanto-ohjelman toimitustilaus täydentää nimikettä, nimike jätetään pois suunnittelusta. Kaikki kysyntä asiaankuuluvista osista on kuitenkin mukana.  
  
## <a name="see-also"></a>Katso myös  
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
[Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)   
[Rakennetiedot: siirrot suunnittelussa](design-details-transfers-in-planning.md)   
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)  

