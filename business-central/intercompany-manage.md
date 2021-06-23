---
title: Konsernitapahtumien hallinta
description: Voit yksinkertaistaa konsernitoiminnoilla samaan organisaatioon kuuluvien yritysten välisiä liiketoimintaprosesseja ja tapahtumia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/02/2021
ms.author: edupont
ms.openlocfilehash: 0a69507b32f8782fe876458adb590529bfd64b20
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184422"
---
# <a name="managing-intercompany-transactions"></a>Konsernitapahtumien hallinta

Organisaatio saattaa koostua useasta yrityksestä, mutta siinä ei välttämättä ole samaa määrää laskenta- ja hallintotyöryhmiä. Konsernitoimintojen ansiosta liiketoiminta tytäryhtiöiden ja sisäisten kumppaniorganisaatioiden on samanlaista kuin ulkoisten toimittajien ja asiakkaiden kanssa toimiminen. Konsernin tapahtumien tiedot lisätään asianmukaisiin asiakirjoihin vain kerran. Voit käyttää itsellesi tuttua toimintoa, esimerkiksi myyntisaamisten ja ostovelkojen hallintaa. Tilikartan ja dimensioiden linkitystoiminto auttaa varmistamaan, että tiedot näkyvät oikeissa paikoissa.  

Konsernitoimintoihin liittyy neljä merkittävää etua:  

- Ajansäästö ja yksinkertaistetut tapahtumat lisäävät tuottavuutta.  
- Tietojen kertakirjaus ja järjestelmänlaajuiset automaattiset päivitykset pienentävät virhepotentiaalia.  
- Kirjausketju on täydellinen, ja liiketoiminnoilla sekä tapahtumahistorioilla on täysi näkyvyys.  
- Tapahtumat sisar- ja tytäryhtiöiden kanssa ovat tehokkaita ja kannattavia.  

Kaikki tapahtuma-asiakirjat ovat täysin hallinnassasi. Voit esimerkiksi hylätä sinulle lähetetyn asiakirjan ja tällä tavalla peruuttaa virheelliset päiväkirjakirjaukset sekä kumota virheelliset vastaanotot tai toimitukset. Tehdessäsi ostoja kumppani- tai tytäryritykseltä voit päivittää ostotilausta niin kauan kuin myyjäyritys ei ole lähettänyt tavaroita.  

Kun lisäät tapahtuman, yksittäisten tilijoukkojen tilejä ei tarvitse määrittää, vaan kumppaniyrityksen tunnus riittää. Konsernitoiminto luo yleisen päiväkirjan rivejä, jotka täsmäävät molempien tapahtumaan osallistuneiden yritysten tilit. Myyntisaamisissa ja ostoveloissa asiakkaille ja toimittajille voi määrittää konsernikumppanin koodin. Sen jälkeen aina, kun luodaan näiden yritysten kanssa suoritettuihin tapahtumiin liittyviä tilauksia tai laskuja, vastaavat asiakirjat luodaan myös kumppaniyritykseen, jolloin tilit täsmäytyvät oikein.  

Kun olet määrittänyt liiketoimintakumppanit asiakkaiksi ja toimittajiksi järjestelmässä sekä luonut heille konsernikumppanin koodit, on mahdollista vaihtaa konsernin osto- ja myyntiasiakirjoja, kuten nimikkeitä ja nimikekuluja. [!INCLUDE [prod_short](includes/prod_short.md)] tukee konsernin tapahtumia eri tietokantojen välillä, esimerkiksi eri maissa ja eri alueilla, sekä eri valuuttoja, erilaisia tilikarttoja, eri dimensioita ja erilaisia nimikenumerointeja.  

> [!NOTE]
> Kaikkia tietotyyppejä ei voi vaihtaa yritysten välillä tällä tavalla. Ostolaskuja ei lähetetä liiketoimintakumppaneille konsernitapahtumaprosessien avulla. Konsernitapahtumaprosessien avulla lähetetyt myyntilaskut luodaan kuitenkin ostolaskuina vastaanottavassa yrityksessä.

Kirjanpitotietojen konsolidoiminen voi olla erityisen tärkeää konsernin sisäisissä prosesseissa. Lisätietoja on kohdassa [Usean yrityksen kirjanpitotietojen konsolidoiminen](finance-consolidated-company-reporting.md).

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä kuvaaviin artikkeleihin.

|Tehtävä |Katso|
|---|---|
|Luo konsernitoimittajat ja -asiakkaat konsernikumppaneina ja määritä konsernin tilikartta.|[Konsernin tietojen määrittäminen](intercompany-how-setup.md)|
|Voit kirjata konsernin asiakirjojen tai päiväkirjojen avulla tapahtumia yhdessä konsernikumppanien kanssa.|[Konserniasiakirjojen ja -päiväkirjojen käyttäminen](intercompany-how-work-documents-journals.md)|
|Järjestää ja käsitellä konsernikumppanien kanssa vaihdettavat saapuvat ja lähtevät tapahtumat.|[Konsernin Saapuneet- ja Lähtevät-kansion hallinta](intercompany-how-manage-intercompany-inbox.md)|
|Konserniyritysten välisten kirjausten avulla voit jakaa kustannuksia kumppaniyritysten kesken.|[Kustannusten kohdistaminen konsernikumppaneille](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Katso myös

[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]