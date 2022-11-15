---
title: Käytön määrittäminen Microsoft 365 -käyttöoikeuksien avulla
description: Opas siitä, miten järjestelmänvalvojat voivat määrittää käyttöoikeudet Business Centralin Microsoft 365 -käyttöoikeuksilla.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: f509c0a8bf5e9320eb0f2712863984221b7138b9
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744982"
---
# <a name="set-up-access-with-microsoft-365-licenses"></a>Käytön määrittäminen Microsoft 365 -käyttöoikeuksien avulla 

Järjestelmänvalvojien täytyy suorittaa monia aktiviteetteja, ennen kuin käyttäjät voivat käyttää Business Centralia Microsoft 365 -käyttöoikeuksilla. Alla olevat vaiheet ovat vähimmäisasetukset, joilla on tarkoitus aloittaa.  

## <a name="deploy-the-business-central-app-for-teams"></a>Ota käyttöön Business Central-sovellus Teamsille 

Jotta Business Central -lisenssin haltijat voivat jakaa tietoja Teamsissa ja Microsoft 365 -käyttöoikeuden haltijat voivat käyttää näitä tietoja, kummallakin on oltava asennettuna Business Central -sovellus Teamsille. Vaikka käyttäjät voivat asentaa sovelluksen itse, järjestelmänvalvojat suosittelevat, että järjestelmänvalvojat käyttävät keskitettyä käyttöönottoa. Keskitetyn käyttöönoton avulla voit vierittää sovelluksen laajemmalle yleisölle koko organisaatiossa ja minimoida yksittäisen käyttäjän toimet. 

Jos haluat tietää, miten Business Central -sovellus Teamsille otetaan keskitetysti käyttöön, katso [Business Central -sovelluksen asentaminen keskitetyn käyttöönoton avulla](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Jos olet käyttänyt keskitettyä käyttöönottoa aiemmin ja asentanut sovelluksen vain lisensoitujen Business Central -käyttäjien suojausryhmään, sinun on suoritettava se uudelleen, jotta voit käyttää sitä lisäryhmissä tai koko organisaatiossa sen mukaan, miten olet konfiguroinut käyttöoikeuden.

> [!TIP]
> Etsitkö nopeampaa tapaa päästä alkuun tätä ominaisuutta kokeiltaessa? Testikäyttäjät voivat asentaa sovelluksen osoitteesta [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="configure-permissions"></a>Oikeuksien määritys

Business Central on suunniteltu suojatuksi ja minimoi riskit olemalla myöntämättä valmiita oikeuksia Microsoft 365 -käyttäjille. Järjestelmänvalvojien täytyy määrittää objektien käyttöoikeudet, jotka määrittävät, mitä taulukoita, sivuja ja raportteja voi käyttää Teamsissa vain Microsoft 365 -käyttöoikeuden avulla. Nämä käyttöoikeudet ovat aloitusoikeuksia, jotka määritetään, kun käyttäjä kirjautuu ensimmäisen kerran Microsoft 365 -käyttöoikeudellaan. 

Aloitusoikeuksien määrittäminen:

1. Etsi **Käyttöoikeuksien määritys** Business Centralin avulla.
2. Valitse Microsoft 365 -käyttöoikeus.
3. Valitse **Microsoft 365** -käyttöoikeussivun yläosassa muokkaa-kuvake ![Muokkaakuvake](media/edit-pencil.png) ja ota sitten käyttöön **Mukauta käyttöoikeuksia**. 
4. Lisää **mukautetut käyttöoikeusjoukot** -osaan tarvittavat käyttöoikeusjoukot ja valitse, koskevatko ne yhtä yritystä vai kaikkia ympäristössä olevia yrityksiä.

> [!NOTE]
> Kun Business Centralin käyttäjät-luettelo synkronoidaan Microsoft 365 -ohjelman käyttäjien kanssa, vain Business Central -käyttöoikeuden käyttäjät lisätään Business Centralin käyttäjät -luetteloon. Käyttäjät, joilla on vain Microsoft 365 -käyttöoikeus, lisätään käyttäjät-luetteloon, kun he käyttävät Business Centralia ensimmäistä kertaa. Lue lisätietoja kohdasta [Käyttäjien luominen käyttöoikeuksien mukaan](ui-how-users-permissions.md).

> [!TIP]
> Etsitkö nopeampaa tapaa päästä alkuun tätä ominaisuutta kokeiltaessa eritysympäristössä tai arviointiyrityksessä? Määritä **D365-luku**-oikeusjoukko, joka sallii useimpien objektien käyttöoikeuden.  

Kun työskentelet useissa ympäristöissä, käyttöoikeusmääritykset täytyy ottaa käyttöön jokaisessa ympäristössä, ja ne voivat olla erilaisia kussakin ympäristössä. 

Lue lisätietoja kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md) ja [Oikeusjoukkojen luominen](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="turn-on-access-with-microsoft-365-licenses"></a>Microsoft 365 -käyttöoikeuksien käytön käyttöönotto

Microsoft 365 -käyttöoikeudet ovat oletusarvoisesti poissa käytöstä. Käyttöoikeus on otettava käyttöön jokaisessa ympäristössä itsenäisesti, jolloin järjestelmänvalvojat voivat hallita ja mahdollistaa vaiheittaisen käyttöönoton koko organisaatiossa. Käyttöoikeus kytketään päälle Business Central -hallintakeskuksen avulla: 

1. Valitse oikeasta yläkulmasta **Asetukset** ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") > **Hallintakeskus**.  
2. Valitse hallintakeskus-kohdassa  **ympäristöt** ja valitse sitten ympäristö, jossa haluat muuttaa käyttöoikeuden käyttöä. 
3. Valitse **ympäristön tiedot** -sivun **Microsoft 365 -käyttöoikeuksien käyttö** -asetuksen avulla **Muokkaa**.
4. Ota valinta käyttöön **Microsoft 365 -käyttöoikeudet** -ruudussa. 
5. Valitse **Tallenna**, kun olet valmis, ja hyväksy vahvistus. Muutos astuu voimaan välittömästi.

## <a name="test-your-setup"></a>Testaa asennustasi

Seuraavien vaiheiden avulla voit varmistaa, että asetukset ovat valmiit tuotantoa varten, ja varmistaa, että kaikki toimii niin kuin pitääkin. 

1. Luo tai yksilöi kaksi testikäyttäjää (A ja B).

   - Testikäyttäjällä A on oltava Business Central -lisenssi ja Microsoft 365 -lisenssi, jolla on pääsy Teamsiin.
   - Testikäyttäjällä B tulee olla vain Microsoft 365 -käyttöoikeus Teamsiin.

2. Kirjaudu Business Central -WWW-asiakasohjelmaan testikäyttäjänä A.

   1. Avaa tietue, johon testikäyttäjä B:llä tulisi olla käyttöoikeus, kuten **nimikkeen** kortti sopivassa yrityksessä ja ympäristössä.
   2. Valitse **Jaa** ![!Jaa sivujen muihin sovelluksiin -toiminto.](media/share-icon.png) > **Jaa Teamsiin** tuodaksesi Jaa Teamsiin -ikkunan näkyviin.
   3. Lisää **Jaa kohteeseen** -kenttään vastaanottajaksi testikäyttäjä B. 
   4. Odota, että linkki laajenee korttiin ja valitse Jaa. 

3. Kirjaudu sisään Microsoft Teamsiin testikäyttäjänä B.

   1. Valitse keskustelu ja avaa keskustelu testikäyttäjän A kanssa. 
   2. Valitse testikäyttäjän A lähettämän viestin kortissa tiedot-painike. Jos Business Central -asiakasohjelma on näkyvissä ja vain luku-tilassa, määrittämäsi määritys onnistui. 

> [!TIP]
> Tapahtuiko virhe? Katso [Microsoft 365 -käyttöoikeuksien käytön vianmääritys](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Katso myös

[Business Centralin käyttäminen Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license.md#minimum-requirements)  
[Microsoft 365 -käyttöoikeuksien käytön vianmääritys](admin-access-with-m365-license-troubleshooting.md)  
[Business Centralin ja Microsoft Teamsin integraatio](across-teams-overview.md)  