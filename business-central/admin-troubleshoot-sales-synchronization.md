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
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 1c2181ee381425a168a9b6b6ce321e595a01ed8e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754990"
---
# <a name="troubleshooting-synchronization-errors"></a>Synkronointivirheiden vianmääritys
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Sovellusten [!INCLUDE[prod_short](includes/prod_short.md)] ja [!INCLUDE[prod_short](includes/cds_long_md.md)] integrointi sisältää useita vaiheita, ja joskus tapahtuu virheitä. Tässä ohjeaiheessa kerrotaan yleisimpiä virheitä ja annetaan vinkkejä niiden korjaamiseen.

Virheet johtuvat usein siitä, että käyttäjä on tehnyt jotain yhdistetyille tietueille tai integroinnin määrittämisessä on tapahtunut virhe. Jos virheet ovat tapahtuneet yhdistettyjen tietueiden vuoksi, käyttäjät voivat ratkaista ne itse. Nämä virheet johtuvat esimerkiksi siitä, että poistat tietoja yhdestä liiketoimintasovelluksesta, mutta et molemmista, ja synkronoit tämän jälkeen. Lisätietoja on kohdassa [Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Esimerkki
Tässä videossa on esimerkki siitä, miten Salesin synkronoinnissa tapahtuneet virheet voidaan korjata. Prosessi on sama kaikille integroinneille. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Integroinnin määrittämiseen liittyvät virheet vaativat yleensä järjestelmänvalvojan toimia. Voit tarkastella näitä virheitä **Integroinnin synkronointivirheet** -sivulla. Seuraavassa esitellään tyypillisiä virheitä:  
  
* Käyttäjille määritetyt käyttöoikeudet ja roolit ovat virheellisiä.  
* Järjestelmänvalvojan tili on määritetty integroinnin käyttäjäksi.  
* Integroinnin käyttäjän salasana on määritetty vaihdettavaksi, kun käyttäjä kirjautuu sisään.  
* Valuuttojen vaihtokursseja ei ole määritetty yhdessä tai kummassakaan sovelluksessa.  
  
Nämä virheet on ratkaistava manuaalisesti. Sivulla olevat toiminnot voivat kuitenkin auttaa tässä. Esimerkiksi:  

* **Lähde**- ja **Kohde**-kentät voivat sisältää linkkejä riviin, josta virhe löytyi. Tutki virhettä napsauttamalla linkkiä.  
* **Poista yli 7 päivää vanhat tapahtumat**- ja **Poista kaikki tapahtumat** -toiminnot tyhjentävät luettelon. Näitä toimintoja käytetään yleensä sen jälkeen, kun useisiin tietueisiin vaikuttavan virheen syy on selvitetty. Mieti kuitenkin tarkasti, kun teet sen. Nämä toiminnot saattavat poistaa virheitä, jotka vielä vaikuttavat toimintaan.

Joskus tietueiden aikaleimat voivat aiheuttaa ristiriitoja. "CDS-integrointitietue" -taulukossa on aikaleimat "Viimeinen synkronointi muokattu" ja "Synkronoitu viimeksi CDS muokattu" viimeiselle yhdistämiselle, joka on tehty riville molempiin suuntiin. Näitä aikaleimoja verrataan liike Business Centralin ja myyntitietueiden aikaleimoihin. Business Centralin aikaleima on Integrointitietue -taulukossa.

Voit suodattaa synkronoitavat tietueet vertaamalla rivin aikaleimoja taulukossa "Integrointitaulukon linkitys" kentissä "Synkronoi mukautettu suodattimessa" ja "Synkronoi sis. taul. Muok. Suodattimella.”.

Ristiriidan virhesanoma "Asiakastietuetta ei voida päivittää, koska sen muokkauspäivämäärä on myöhäisempi kuin tilitietueessa" tai "Tilitietuetta ei voida päivittää, koska sen muokkauspäivämäärä on myöhäisempi kuin asiakastietueessa" voi tapahtua, jos rivillä on aikaleima, joka on suurempi kuin IntegrationTableMapping."Synch. Modified On Filter", mutta se ei ole myöhäisempi kuin myynnin integroinnin tietueen aikaleima. Se tarkoittaa sitä, että lähderivi synkronoitiin manuaalisesti, ei työjonotapahtuman mukaan. 

Ristiriita johtuu siitä, että myös kohderiviä on muutettu – rivin aikaleima on uudempi kuin myynnin integroinnin tietueen aikaleima. Kohde tarkistetaan vain kaksisuuntaisissa taulukoissa. 

Nämä tietueet siirretään nyt "Ohitettu synkronointi" -sivulle, jonka voit avata Business Centralin Microsoft Dynamics yhteyden asetukset -sivulta. Siellä voit määrittää säilytettävät muutokset ja synkronoida sitten tietueet uudelleen.

## <a name="remove-couplings-between-records"></a>Liitosten poistaminen tietueiden väliltä
Kun integraatiossa on jotain vikaa ja haluat poistaa tietueiden synkronoinnin pysäyttämisen, voit tehdä sen yhden tai usean tietueen kanssa kerralla. Voit irrottaa yhden tai useamman tietueen luettelosivuilta tai **Yhdistettyjen tietojen synkronointivirheet** -sivulta valitsemalla yhden tai useamman rivin ja valitsemalla **Poista yhdistäminen**. Voit myös poistaa kaikki yhden tai useamman taulukon yhdistämismäärityksen yhdistämiset **Integrointitaulukon yhdistämismääritykset** -sivulla. 

## <a name="see-also"></a>Katso myös
[Integrointi Microsoft Dataversein kanssa](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Microsoft Dataverse -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Yhteyden määrittäminen Microsoft Dataverse -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md)  
[Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md)  
