---
title: Käyttäjän käyttöoikeustyönkulku Microsoft 365 -käyttöoikeuksille
description: Saat yleiskuvan siitä, mitä tapahtuu, kun käyttäjä käyttää Business Central -tietoja Microsoft 365 -käyttöoikeuksien avulla ensimmäisen käyttökerran yhteydessä.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: d20384149854161588df50af9e8d92af78e16fa1
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745000"
---
# <a name="user-access-flow-for-microsoft-365-licenses"></a>Käyttäjän käyttöoikeustyönkulku Microsoft 365 -käyttöoikeuksille

Tämä artikkeli kuvaa sitä, mitä tapahtuu, kun käyttäjä käyttää Business Central -tietoja Microsoft 365 -käyttöoikeuksien avulla ensimmäisen käyttökerran yhteydessä. Tämän työn ymmärtäminen mahdollistaa sen, että järjestelmänvalvojat voivat suunnitella toimintatapansa ja määrittää Business Centralin vastaamaan yrityksen tarpeita.

1. Ensin käyttäjän henkilöllisyys todennetaan 
2. Business Central varmistaa, että kaikki [vähimmäisvaatimukset](admin-access-with-m365-license.md#minimum-requirements) täyttyvät.
3. Business Central vahvistaa, että käyttäjällä ei ole suurempaa käyttöoikeutta, kuten Business Central -käyttöoikeutta tai hallinnollista roolia, kuten delegoitua järjestelmänvalvojaroolia. 
4. Business Central tarkistaa, käyttääkö käyttäjä tietoja, jotka kuuluvat ympäristöön, joka on sallinut Microsoft 365 -käyttöoikeuksien käytön. 
5. Käyttäjätietueet on valmisteltu Business Centralin Microsoft 365 -käyttöoikeuksien määrityssivulla määritetyn käyttäjäryhmän, profiilin ja käyttöoikeusjoukkojen määrittämistä varten. Teamsin käyttäjät -käyttäjäryhmä on määritetty oletusarvon mukaan, työntekijän profiili on määritetty ja vain kirjautumisoikeusjoukko on määritetty. Myös muut käyttäjäasetukset ovat voimassa, kuten lisensoitu Business Central -käyttäjä. 
6. Käytetään koko Business Central -suojausmallia, jotta voidaan määrittää, voiko käyttäjällä olla pääsy tietueeseen, sivuun, määritettyyn yritykseen ja määritettyyn ympäristöön. 

Jos kaikki vaiheet onnistuvat, käyttäjä voi nyt tarkastella tätä Business Central -tietoa Teamsissa. Business Central -palvelu varmistaa automaattisesti vain luku -oikeuden ja yksinkertaistaa käyttöliittymää. 

Käyttäjätili on nyt rekisteröity Business Centralin kautta, ja sitä voi hallita kuten mitä tahansa Business Central -käyttäjää.

> [!NOTE]
> Vaiheet voivat vaihdella niiden lisäsuojausmääritysten mukaan, jotka olet määrittänyt Microsoft 365:ssä tai Business Centralissa.

## <a name="see-also"></a>Katso myös

[Business Centralin käyttäminen Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license.md#minimum-requirements)  
[Käytön määrittäminen Microsoft 365 -käyttöoikeuksien avulla](admin-access-with-m365-license-setup.md)  