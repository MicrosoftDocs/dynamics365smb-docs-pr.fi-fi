---
title: Käyttäjän käyttöoikeustyönkulku Microsoft 365 -käyttöoikeuksille
description: 'Saat yleiskuvan siitä, mitä tapahtuu, kun käyttäjä käyttää Business Central -tietoja Microsoft 365 -käyttöoikeuksien avulla ensimmäisen käyttökerran yhteydessä.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---
# <a name="user-access-flow-for-microsoft--licenses" />Käyttäjän käyttöoikeustyönkulku Microsoft 365 -käyttöoikeuksille

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

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

## <a name="see-also" />Katso myös

[Business Centralin käyttäminen Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license.md#minimum-requirements)  
[Käytön määrittäminen Microsoft 365 -käyttöoikeuksien avulla](admin-access-with-m365-license-setup.md)  
