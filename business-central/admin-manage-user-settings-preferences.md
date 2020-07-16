---
title: Käyttäjäasetusten ja asetusten hallinta Dynamics 365 Business Centralissa
description: Käyttäjäasetusten ja asetusten hallinta Dynamics 365 Business Centralissa.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 06/17/2020
ms.author: soalex
ms.openlocfilehash: 633a0872a878843f26d627dcd76e69d1c851ef8a
ms.sourcegitcommit: 3945f16d6d9c9853651e6291ce1465a44fd71fc8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2020
ms.locfileid: "3460418"
---
# <a name="manage-user-settings-and-preferences"></a>Käyttäjäasetusten ja asetusten hallinta

Järjestelmänvalvojana voit hallita käyttäjäasetuksia [!INCLUDE[d365fin](includes/d365fin_md.md)]issa samalla tavoin kuin yksittäiset käyttäjät voivat hallita omia asetuksiaan **Omat asetukset** -sivulla.  

## <a name="types-of-user-settings"></a>Käyttäjäasetusten tyypit

*Käyttäjäasetukset* eivät ole sama asia kuin *käyttäjän määritykset*, jotka koskevat käyttäjää entiteettinä ja käyttäjän järjestelmän käyttöoikeuksia. Käyttäjäasetuksilla ei ole myöskään mitään tekemistä käyttäjän mukauttamisella, mikä tarkoittaa pinnallisia käyttöliittymän muutoksia. Käyttäjäasetuksilla määritetään käyttäjän mieltymysten mukaan, miten sovelluksen eri osat näkyvät käyttäjälle. Seuraavaksi käsitellään viisi käyttäjäasetus- ja määritystyyppiä, jotka yksittäinen käyttäjä voi määrittää tai jotka järjestelmänvalvoja voi määrittää keskitetysti.

- **Yritys**  

  Tämä asetus määrittää yrityksen, joka kirjaudutaan seuraavan kirjautumisen yhteydessä. Käyttäjällä voi olla useiden yritysten käyttöoikeus ja käyttäjä voi olla aktiivinen useissa yrityksissä.

- **Profiili (roolit)**  

  Profiili tarkoittaa käyttäjän tehtävää yrityksessä, kuten *myyntipäällikköä*, *kirjanpitäjää* tai *ostajaa*. Profiili määrittää sitten käyttäjän roolikeskuksen eli aloitussivun, joka avautuu käyttäjille kirjauduttaessa. Profiili ei vaikuta [!INCLUDE[d365fin](includes/d365fin_md.md)]in toimintojen käyttöoikeuksiin.  

- **Kielialueen tunnus (aluekohtaiset asetukset)**  

  Määrittää, miten päivämäärät ja numerot esitetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -asiakasohjelmassa (esimerkiksi, käytetäänkö eurooppalaisia vai amerikkalaisia päivämäärämuotoja) tai miten desimaali ja tuhaterottimet näytetään summissa. Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjiä synkronoidaan Office 365:stä, käytössä on Office 365:n aluekohtaiset asetukset olettaen, että käyttäjä haluaa käyttää samoja asetuksia Office-tuotteissa ja [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Järjestelmänvalvoja tai käyttäjä voi muuttaa näitä asetuksia manuaalisesti [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, mutta ne palautetaan Office 365:n arvoon seuraavan synkronoinnin yhteydessä.

- **Kieli**  

  Määrittää kielen, jolla [!INCLUDE[d365fin](includes/d365fin_md.md)] näyttää tekstin, kuvatekstit ja virhesanomat sovelluksessa. Jos [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjiä synkronoidaan Office 365:stä, käytössä on Office 365:n kieliasetukset olettaen, että käyttäjä haluaa käyttää samoja asetuksia Office-tuotteissa ja [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Järjestelmänvalvoja tai käyttäjä voi muuttaa näitä asetuksia manuaalisesti [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, mutta ne palautetaan Office 365:n arvoon seuraavan synkronoinnin yhteydessä.

  Jos Office 365:n kieliasetus vastaa [!INCLUDE[d365fin](includes/d365fin_md.md)]in tukemaa kieltä, kyseinen kieli valitaan käyttäjälle.  

  > [!NOTE]
  > Kielen näyttäminen oikein voi edellyttää, [!INCLUDE[d365fin](includes/d365fin_md.md)]in kielisovelluksen asentamista. Tämän vuoksi tarvittavat kielisovelluksen kannattaakin asentaa, ennen kuin kukaan on kirjautunut sisään ensimmäisen kerran, jotta käyttökokemus on hyvä alusta alkaen. Lisätietoja on [tuettujen kielien](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) luettelossa.  
  
- **Aikavyöhyke**  

  Määrittää käyttäjän aikavyöhykkeen. Tätä ei tällä hetkellä synkronoida Office 365:stä, joten se on määritettävä manuaalisesti.  

> [!NOTE]
> Jos Office 365 -käyttäjän synkronointi tapahtuu silloin, kun käyttäjät ovat kirjautuneet [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, kyseisten käyttäjien on ladattava selain uudelleen tai kirjauduttava ensin ulos ja sitten takaisin [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, jotta synkronointitoiminnon mahdollisesti määrittämä toinen kielijoukko on näkyvissä.

## <a name="overview-of-all-user-settings"></a>Kaikkien käyttäjäasetusten yleiskuvaus

Järjestelmänvalvojilla on mahdollisuus määrittää tai muuttaa näitä käyttäjien asetuksia kussakin yrityksessä. Se tehdään **Käyttäjän mukautukset** -sivulla. Tällä sivulla olevat tietueet ilmaisevat käyttäjien edellä olevia asetuksia koskevat valinnat. Tietueita on yksi kullakin käyttäjällä. Kun käyttäjät tekevät muutoksia asetuksiin **Omat asetukset** -sivulla, nämä muutokset ilmenevät myös **Käyttäjän mukautukset** -luettelossa. Järjestelmänvalvojat voivat myös määrittää nämä asetukset käyttäjille ennen käyttäjien ensimmäistä kirjautumista, jolloin käyttäjien ei tarvitse tehdä sitä itse, mikä puolestaan parantaa käyttäjien *aloituskokemusta*.

> [!NOTE]
> Käyttäjien mukautuksilla ei ole mitään tekemistä käyttäjien *omien* pinnallisten käyttökokemusmuutosten kanssa.

## <a name="to-review-or-make-changes-to-user-settings"></a>Käyttäjäasetusten tarkasteleminen tai muuttaminen

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Käyttäjän mukautukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Näkyviin tulee luettelo käyttäjistä ja heidän asetuksistaan. Käyttäjän asetuksia voi muokata valitsemalla **Käyttäjän tunnus** tai valitsemalla ensin **Hallinta** ja sitten **Muokkaa**.
3. Näkyviin tulee tietyn käyttäjän asetusten **Käyttäjän mukautus** -kortti, johon voi tehdä tarvittavat muutokset.  

## <a name="see-also"></a>Katso myös

[Käytön aloittaminen](product-get-started.md)  
[Maa- ja aluekohtainen saatavuus ja tuetut kielet](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Kielen ja kielialueen muuttaminen](about-locale-language.md)  
