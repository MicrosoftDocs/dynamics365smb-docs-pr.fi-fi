---
title: Synkronointivirheiden vianmääritys | Microsoft Docs
description: Sisältää ohjeita synkronointivirheiden määrittämistä ja ratkaisemista varten.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 489e66165c5441ea63043a30dee8af314ef5d815
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991806"
---
# <a name="troubleshooting-synchronization-errors"></a>Synkronointivirheiden vianmääritys
Sovellusten [!INCLUDE[d365fin](includes/d365fin_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] integrointi sisältää useita vaiheita, ja joskus tapahtuu virheitä. Tässä ohjeaiheessa kerrotaan yleisimpiä virheitä ja annetaan vinkkejä niiden korjaamiseen.

Virheet johtuvat usein siitä, että käyttäjä on tehnyt jotain yhdistetyille tietueille tai integroinnin määrittämisessä on tapahtunut virhe. Jos virheet ovat tapahtuneet yhdistettyjen tietueiden vuoksi, käyttäjät voivat ratkaista ne itse. Nämä virheet johtuvat esimerkiksi siitä, että poistat tietueita yhdestä liiketoimintasovelluksesta, mutta et molemmista, ja synkronoit tämän jälkeen. Lisätietoja on kohdassa [Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Integroinnin määrittämiseen liittyvät virheet vaativat yleensä järjestelmänvalvojan toimia. Voit tarkastella näitä virheitä **Integroinnin synkronointivirheet** -sivulla. Seuraavassa esitellään tyypillisiä virheitä:  
  
* Käyttäjille määritetyt käyttöoikeudet ja roolit ovat virheellisiä.  
* Järjestelmänvalvojan tili on määritetty integroinnin käyttäjäksi.  
* Integroinnin käyttäjän salasana on määritetty vaihdettavaksi, kun käyttäjä kirjautuu sisään.  
* Valuuttojen vaihtokursseja ei ole määritetty yhdessä tai kummassakaan sovelluksessa.  
  
Nämä virheet on ratkaistava manuaalisesti. Sivulla olevat toiminnot voivat kuitenkin auttaa tässä. Esimerkiksi:  

* **Lähde**- ja **Kohde**-kentät voivat sisältää linkkejä tietueeseen, josta virhe löytyi. Valitse linkki, kun haluat avata tietueen ja tutkia virhettä.  
* **Poista yli 7 päivää vanhat tapahtumat**- ja **Poista kaikki tapahtumat** -toiminnot tyhjentävät luettelon. Näitä toimintoja käytetään yleensä sen jälkeen, kun useisiin tietueisiin vaikuttavan virheen syy on selvitetty. Mieti kuitenkin tarkasti, kun teet sen. Nämä toiminnot saattavat poistaa virheitä, jotka vielä vaikuttavat toimintaan.

Joskus tietueiden aikaleimat voivat aiheuttaa ristiriitoja. "CRM-integrointitietue" -taulukossa on aikaleimat "Viimeinen synkronointi muokattu" ja "Synkronoitu viimeksi CRM muokattu" viimeiselle yhdistämiselle, joka on tehty tietueelle molempiin suuntiin. Näitä aikaleimoja verrataan liike Business Centralin ja myyntitietueiden aikaleimoihin. Business Centralin aikaleima on Integrointitietue -taulukossa.

Voit suodattaa synkronoitavat tietueet vertaamalla tietueiden aikaleimoja taulukossa "Integrointitaulukon linkitys" kentissä "Synkronoi mukautettu suodattimessa" ja "Synkronoi sis. taul. Muok. Suodattimella.”.

Ristiriidan virhesanoma "Asiakastietuetta ei voida päivittää, koska sen muokkauspäivämäärä on myöhäisempi kuin tilitietueessa" tai "Tilitietuetta ei voida päivittää, koska sen muokkauspäivämäärä on myöhäisempi kuin asiakastietueessa" voi tapahtua, jos tietueella on aikaleima, joka on suurempi kuin IntegrationTableMapping."Synch. Modified On Filter", mutta se ei ole myöhäisempi kuin myynnin integroinnin tietueen aikaleima. Se tarkoittaa sitä, että lähdetietue synkronoitiin manuaalisesti, ei työjonotapahtuman mukaan. 

Ristiriita johtuu siitä, että myös kohdetietuetta on muutettu - tietueen aikaleima on uudempi kuin myynnin integroinnin tietueen aikaleima. Kohde tarkistetaan vain kaksisuuntaisissa taulukoissa. 

Nämä tietueet siirretään nyt "Ohitettu synkronointi" -sivulle, jonka voit avata Business Centralin Microsoft Dynamics yhteyden asetukset -sivulta. Siellä voit määrittää säilytettävät muutokset ja synkronoida sitten tietueet uudelleen.

## <a name="see-also"></a>Katso myös
[Integrointi [!INCLUDE[crm_md](includes/crm_md.md)]in kanssa](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[[!INCLUDE[crm_md](includes/crm_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Yhteyden määrittäminen [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md)  
[Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md)  
