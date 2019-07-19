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
ms.date: 06/11/2019
ms.author: bholtorf
ms.openlocfilehash: bb6d0837f91240eb31abc7c02895cf2da420bf7d
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726788"
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

## <a name="see-also"></a>Katso myös
[Integrointi [!INCLUDE[crm_md](includes/crm_md.md)]in kanssa](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[[!INCLUDE[crm_md](includes/crm_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Yhteyden määrittäminen [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md)  
[Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md)  