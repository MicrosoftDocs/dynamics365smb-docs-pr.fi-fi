---
title: Käyttäjäasetusten ja asetusten hallinta järjestelmänvalvojana
description: Käyttäjäasetusten ja asetusten hallinta Dynamics 365 Business Centralissa.
author: sorenfriisalexandersen
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.search.form: 9204
ms.date: 04/01/2021
ms.author: soalex
ms.openlocfilehash: 779dcea91d2e856bfae847f98695ceed0c0d600e
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145938"
---
# <a name="manage-user-settings-and-preferences"></a>Käyttäjäasetusten ja asetusten hallinta

Järjestelmänvalvojana voit määrittää käyttäjäasetuksia [!INCLUDE[prod_short](includes/prod_short.md)]issa samalla tavoin kuin yksittäiset käyttäjät voivat hallita omia asetuksiaan **Omat asetukset** -sivulla.  

**Käyttäjät**-luettelosta saa yleiskuvan kaikista käyttäjistä ja yksittäisen käyttäjän asetuksia voi muuttaa valitsemalla kyseisen käyttäjän **Käyttäjäasetukset**-toiminnon.

> [!TIP]
> **Käyttäjäasetukset**-luettelo näyttää kunkin käyttäjän nykyiset asetukset. Kutakin yksittäistä käyttäjää voi tarkastella tai muokata valitsemalla **Näytä**- tai **Muokkaa**-toiminnon.

**Käyttäjäasetukset-kortti**-sivu muistuttaa kunkin käyttäjän käytettävissä olevaa **Omat asetukset** -sivua, ja kyseinen sivu on tehokas työkalu, jossa järjestelmänvalvoja voi esimerkiksi määrittää oletusasetuksia ja poistaa mukautettuja sivuja.  

## <a name="types-of-user-settings"></a>Käyttäjäasetusten tyypit

*Käyttäjäasetukset* eivät ole sama asia kuin *käyttäjän määritykset*, jotka koskevat käyttäjää entiteettinä ja käyttäjän järjestelmän käyttöoikeuksia. Käyttäjäasetuksilla ei ole myöskään mitään tekemistä käyttäjän mukauttamisella, mikä tarkoittaa pinnallisia käyttöliittymän muutoksia. Käyttäjäasetuksilla määritetään kunkin käyttäjän esimääritetyt asetukset siltä osin, miten sovelluksen eri osat näkyvät käyttäjälle. Seuraavaksi käsitellään viisi käyttäjäasetus- ja määritystyyppiä, jotka yksittäinen käyttäjä voi määrittää tai jotka järjestelmänvalvoja voi määrittää keskitetysti.

- **Yritys**  

  Tämä asetus määrittää yrityksen, joka kirjaudutaan seuraavan kirjautumisen yhteydessä. Käyttäjällä voi olla useiden yritysten käyttöoikeus ja käyttäjä voi olla aktiivinen useissa yrityksissä.

- **Rooli**  

  Rooli tai profiili tarkoittaa käyttäjän tehtävää yrityksessä, kuten *myyntipäällikköä*, *kirjanpitäjää* tai *ostajaa*. Profiili määrittää sitten käyttäjän roolikeskuksen eli aloitussivun, joka avautuu käyttäjille kirjauduttaessa. Profiili ei vaikuta [!INCLUDE[prod_short](includes/prod_short.md)]in toimintojen käyttöoikeuksiin.  

- **Kieli**  

  Määrittää kielen, jolla [!INCLUDE[prod_short](includes/prod_short.md)] näyttää tekstin, kuvatekstit ja virhesanomat sovelluksessa. Jos [!INCLUDE[prod_short](includes/prod_short.md)]in käyttäjiä synkronoidaan Microsoft 365:stä, käytössä on Microsoft 365:n kieliasetukset olettaen, että käyttäjä haluaa käyttää samoja asetuksia Office-tuotteissa ja [!INCLUDE[prod_short](includes/prod_short.md)]issa. Järjestelmänvalvoja voi muuttaa oletusasetuksen, ja kukin käyttäjä tehdä Omat asetukset -sivulla valinnan käytettävissä olevista kielistä. Ne kuitenkin palautetaan Microsoft 365:n arvoon, kun synkronointi suoritetaan seuraavan kerran.

  Jos Microsoft 365:n kieliasetus vastaa [!INCLUDE[prod_short](includes/prod_short.md)]in tukemaa kieltä, kyseinen kieli valitaan käyttäjälle.  

  > [!NOTE]
  > Kielen näyttäminen oikein voi edellyttää, [!INCLUDE[prod_short](includes/prod_short.md)]in kielisovelluksen asentamista. Tämän vuoksi tarvittavat kielisovelluksen kannattaakin asentaa, ennen kuin kukaan on kirjautunut sisään ensimmäisen kerran, jotta käyttökokemus on hyvä alusta alkaen. Lisätietoja on [tuettujen kielien](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) luettelossa.  
  
- **Alue**  

  Määrittää, miten päivämäärät ja numerot esitetään [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelmassa (esimerkiksi, käytetäänkö eurooppalaisia vai amerikkalaisia päivämäärämuotoja) tai miten desimaali ja tuhaterottimet näytetään summissa. Jos [!INCLUDE[prod_short](includes/prod_short.md)]in käyttäjiä synkronoidaan Microsoft 365:stä, käytössä on Microsoft 365:n aluekohtaiset asetukset olettaen, että käyttäjä haluaa käyttää samoja asetuksia Office-tuotteissa ja [!INCLUDE[prod_short](includes/prod_short.md)]issa. Järjestelmänvalvoja tai käyttäjä voi muuttaa näitä asetuksia manuaalisesti [!INCLUDE[prod_short](includes/prod_short.md)]issa, mutta ne palautetaan Microsoft 365:n arvoon seuraavan synkronoinnin yhteydessä.

- **Aikavyöhyke**  

  Määrittää käyttäjän aikavyöhykkeen. Tätä ei tällä hetkellä synkronoida Microsoft 365:stä, joten se on määritettävä manuaalisesti.  

- **Opastusvihjeitä**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)] Järjestelmänvalvoja voi poistaa opastusvihjeet käytöstä kaikilta käyttäjiltä esimerkiksi silloin, kun käyttöön otetaan uusia käyttäjiä, joille [!INCLUDE [prod_short](includes/prod_short.md)] on jo tuttu.  

> [!NOTE]
> Jos Microsoft 365 -käyttäjän synkronointi tapahtuu silloin, kun käyttäjät ovat kirjautuneet [!INCLUDE[prod_short](includes/prod_short.md)]iin, kyseisten käyttäjien on ladattava selain uudelleen tai kirjauduttava ensin ulos ja sitten takaisin [!INCLUDE[prod_short](includes/prod_short.md)]iin, jotta synkronointitoiminnon mahdollisesti määrittämä toinen kielijoukko on näkyvissä.

## <a name="overview-of-all-user-specific-changes"></a>Kaikkien käyttäjäkohtaisten muutosten yleiskuvaus

Järjestelmänvalvoja voi saada yleiskuvan niistä [!INCLUDE [prod_short](includes/prod_short.md)]iin tehdyistä yksittäisistä muutoksista, joita kukin käyttäjä on voinut tehdä [!INCLUDE [prod_short](includes/prod_short.md)]in eri sivuille. Kun käyttäjät tekevät muutoksia omaan [!INCLUDE [prod_short](includes/prod_short.md)] -kokemukseen, nämä muutokset näkyvät myös **Käyttäjän mukautukset** -luettelossa. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## <a name="to-review-or-delete-user-personalizations"></a>Käyttäjän mukautusten tarkasteleminen ja poistaminen

1. Valitse ![Etsi sivua tai raporttia.](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, syötä **Mukautetut sivut** ja valitse sitten vastaava linkki.
2. Näkyviin tulee luettelo käyttäjistä ja heidän mukautetuista sivuistaan. Käyttäjän mukautukset poistetaan napsauttamalla kyseistä riviä tai valitsemalla ensin **Hallinta** ja sitten **Poista**.

Mukautus poistetaan ja kyseisen sivun käyttökokemus palautuu oletustilaan.

## <a name="see-also"></a>Katso myös

[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Maa- ja aluekohtainen saatavuus ja tuetut kielet](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Kielen ja kielialueen muuttaminen](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
