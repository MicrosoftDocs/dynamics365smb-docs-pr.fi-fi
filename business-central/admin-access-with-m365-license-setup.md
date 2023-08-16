---
title: Käytön määrittäminen Microsoft 365 -käyttöoikeuksien avulla
description: 'Opas siitä, miten järjestelmänvalvojat voivat määrittää käyttöoikeudet Business Centralin Microsoft 365 -käyttöoikeuksilla.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: 9061
---
# Business Centralin käytön määrittäminen Teamsissa Microsoft 365 -käyttöoikeuksilla

Järjestelmänvalvojien täytyy suorittaa monia aktiviteetteja, ennen kuin käyttäjät voivat käyttää [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa Microsoft 365 -käyttöoikeuksilla. Alla olevat vaiheet ovat vähimmäisasetukset, joilla on tarkoitus aloittaa. Lisätietoja käytöstä Microsoft 365 -käyttöoikeuksilla on kohdassa [Business Centralin käyttäminen Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license.md).

## Suuntaviivoja

Käyttöoikeuksien määrittäminen Microsoft 365 -käyttöoikeuksineen sisältää seuraavat tehtävät:

||Tehtävä|Pakollinen|
|-|-|-|
|1|[Määritä, mitä Business Central -tietoja Microsoft 365 -käyttöoikeuksien haltijoilla on oikeus tarkastella](#configure-permissions)|![valintamerkki](media/check.png "tarkistus")|
|2|[Microsoft 365 -käyttöoikeuksien ottaminen käyttöön Business Central -ympäristössä](#enable-access-with-microsoft-365-licenses)|![valintamerkki](media/check.png "tarkistus")|
|3|[Määritä suojausryhmä ympäristöön](#choose-who-gets-access-by-using-security-group)|
|4|[Ota käyttöön Business Central-sovellus Teamsille käyttäjiä varten](#deploy-the-business-central-app-for-teams)|![valintamerkki](media/check.png "tarkistus")|
|5|[Testaa määritystä](#test-your-setup)||

> [!TIP]
> Viimeistä tehtävää lukuun ottamatta voit suorittaa tehtävät missä tahansa järjestyksessä. Voit tehdä tehtäviä erikseen, kuten seuraavissa osissa kuvataan tai käyttää **Pääsy Microsoft 365:n käyttöoikeuksien avulla** -asetusten ohjattua määritystä.
>
> Suorittaaksesi asetusten ohjatun määrityksen, toimi seuraavasti:
>
> 1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys** ja valitse sitten vastaava linkki.
> 2. Siirry **Asetusten ohjattu määritys** -sivulla **Tee enemmän Business Centralin avulla** -osioon ja valitse **Käyttö Microsoft 365 -käyttöoikeuksien avulla**.
> 3. Seuraa ohjeita.  

## Määritä oikeudet

[!INCLUDE [prod_short](includes/prod_short.md)] on suunniteltu suojatuksi ja minimoi riskit olemalla myöntämättä valmiita oikeuksia Microsoft 365 -käyttäjille. Järjestelmänvalvojien täytyy määrittää objektien käyttöoikeudet, jotka määrittävät, mitä taulukoita, sivuja ja raportteja voi käyttää Teamsissa vain Microsoft 365 -käyttöoikeuden avulla. Nämä käyttöoikeudet ovat aloitusoikeuksia, jotka määritetään, kun käyttäjä kirjautuu ensimmäisen kerran Microsoft 365 -käyttöoikeudellaan. 

Aloitusoikeuksien määrittäminen:

1. Etsi **Käyttöoikeuksien määritys** [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman avulla.
2. Valitse Microsoft 365 -käyttöoikeus.
3. Valitse **Microsoft 365** -käyttöoikeussivun yläosassa muokkaa-kuvake ![Muokkaakuvake](media/edit-pencil.png) ja ota sitten käyttöön **Mukauta käyttöoikeuksia**. 
4. Lisää **mukautetut käyttöoikeusjoukot** -osaan tarvittavat käyttöoikeusjoukot ja valitse, koskevatko ne yhtä yritystä vai kaikkia ympäristössä olevia yrityksiä.

Tällä kokoonpanolla käyttäjät, joilla on vain Microsoft 365 -käyttöoikeus, lisätään **Käyttäjät**-luetteloon, kun he käyttävät [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaa ensimmäistä kertaa. Lisätietoja käyttäjistä on kohdassa [Käyttäjien luominen käyttöoikeuksien mukaan](ui-how-users-permissions.md).

> [!NOTE]
> Kun Microsoft 365:n käyttäjät-luettelo synkronoidaan [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman käyttäjien kanssa, vain [!INCLUDE [prod_short](includes/prod_short.md)] -käyttöoikeuden käyttäjät lisätään [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman käyttäjät -luetteloon. Voit lisätä ympäristölle suojausryhmän hallitaksesi käyttöoikeuksia ja profiileja tarkemmin. Kun ympäristöt on suojattu suojausryhmällä ja niiden käyttö on sallittu Microsoft 365 -käyttöoikeuksilla, **Käyttäjät**-sivulla oleva **Päivitä käyttäjät Microsoft 365:stä** -toiminto sisältää myös käyttäjät, joilla Microsoft 365 -käyttöoikeus. Lisätietoja ympäristöjen suojaamisesta on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Käyttöoikeuksien hallinta Azure Active Directory -ryhmien avulla](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

> [!TIP]
> Etsitkö nopeampaa tapaa päästä alkuun tätä ominaisuutta kokeiltaessa eritysympäristössä tai arviointiyrityksessä? Määritä **D365-luku**-oikeusjoukko, joka sallii useimpien objektien käyttöoikeuden.  

Kun työskentelet useissa ympäristöissä, käyttöoikeusmääritykset täytyy ottaa käyttöön jokaisessa ympäristössä, ja ne voivat olla erilaisia kussakin ympäristössä.

Lue lisätietoja kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md) ja [Oikeusjoukkojen luominen](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## Microsoft 365 -käyttöoikeuksien käyttämisen ottaminen käyttöön

Microsoft 365 -käyttöoikeudet ovat oletusarvoisesti poissa käytöstä. Käyttöoikeus on otettava käyttöön jokaisessa ympäristössä itsenäisesti, jolloin järjestelmänvalvojat voivat hallita ja mahdollistaa vaiheittaisen käyttöönoton koko organisaatiossa. Käyttöoikeus kytketään päälle [!INCLUDE [prod_short](includes/prod_short.md)] -hallintakeskuksen avulla: 

1. Valitse oikeasta yläkulmasta **Asetukset** ![Asetukset.](media/ui-experience/settings_icon_small.png "Roolikeskuksen Asetukset-kuvake") > **Hallintakeskus**.  
2. Valitse hallintakeskus-kohdassa  **ympäristöt** ja valitse sitten ympäristö, jossa haluat muuttaa käyttöoikeuden käyttöä. 
3. Valitse **ympäristön tiedot** -sivun **Microsoft 365 -käyttöoikeuksien käyttö** -asetuksen avulla **Muokkaa**.
4. Ota valinta käyttöön **Microsoft 365 -käyttöoikeudet** -ruudussa. 
5. Valitse **Tallenna**, kun olet valmis, ja hyväksy vahvistus. Muutos astuu voimaan välittömästi.

## Suojausryhmän avulla tapahtuvan käyttöoikeuden valitseminen

Business Central -hallintakeskuksessa voi määrittää ympäristön, joka voidaan määrittää yhdelle tai useammalle suojausryhmälle käyttöä varten. Voit määrittää Azure Active Directory (Azure AD) -ryhmän ympäristöön. Määrittämällä Azure AD -ryhmän ympäristöön vain ryhmän suorat ja epäsuorat jäsenet saavat käyttää ympäristöä. Epäsuorat jäsenet ovat toisen ryhmän käyttäjiä, jotka itse ovat ympäristöön määritetyn ryhmän jäseniä. Vaikka kaikki Azure AD:n lisensoidut käyttäjät lisätään ympäristöön Microsoft 365:n synkronoinnin yhteydessä, vain ryhmän jäsenet voivat kirjautua sisään. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Käyttöoikeuksien hallinta Azure Active Directory -ryhmien avulla](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

## Ota käyttöön Business Central -sovellus Teamsille

Jotta [!INCLUDE [prod_short](includes/prod_short.md)] -lisenssin haltijat voivat jakaa tietoja Teamsissa ja Microsoft 365 -käyttöoikeuden haltijat voivat käyttää näitä tietoja, kummallakin on oltava asennettuna [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus Teamsille. Vaikka käyttäjät voivat asentaa sovelluksen itse, järjestelmänvalvojat suosittelevat, että järjestelmänvalvojat käyttävät keskitettyä käyttöönottoa. Keskitetyn käyttöönoton avulla voit vierittää sovelluksen laajemmalle yleisölle koko organisaatiossa ja minimoida yksittäisen käyttäjän toimet. 

Jos haluat tietää, miten [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus Teamsille otetaan keskitetysti käyttöön, katso [Business Central -sovelluksen asentaminen keskitetyn käyttöönoton avulla](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Jos olet käyttänyt keskitettyä käyttöönottoa aiemmin ja asentanut sovelluksen vain lisensoitujen [!INCLUDE [prod_short](includes/prod_short.md)] -käyttäjien suojausryhmään, sinun on suoritettava se uudelleen, jotta voit käyttää sitä lisäryhmissä tai koko organisaatiossa sen mukaan, miten olet konfiguroinut käyttöoikeuden.

> [!TIP]
> Etsitkö nopeampaa tapaa päästä alkuun tätä ominaisuutta kokeiltaessa? Testikäyttäjät voivat asentaa sovelluksen osoitteessa [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## Testaa asennustasi

Seuraavien vaiheiden avulla voit varmistaa, että asetukset ovat valmiit tuotantoa varten, ja varmistaa, että kaikki toimii niin kuin pitääkin.

1. Luo tai yksilöi kaksi testikäyttäjää (A ja B).

   - Testikäyttäjällä A on oltava [!INCLUDE [prod_short](includes/prod_short.md)] -lisenssi ja Microsoft 365 -lisenssi, jolla on pääsy Teamsiin.
   - Testikäyttäjällä B tulee olla vain Microsoft 365 -käyttöoikeus Teamsiin.

2. Kirjaudu [!INCLUDE [prod_short](includes/prod_short.md)] -WWW-asiakasohjelmaan testikäyttäjänä A.

   1. Avaa tietue, johon testikäyttäjä B:llä tulisi olla käyttöoikeus, kuten **nimikkeen** kortti sopivassa yrityksessä ja ympäristössä.
   2. Valitse **Jaa** ![!Jaa sivujen muihin sovelluksiin -toiminto.](media/share-icon.png) > **Jaa Teamsiin** tuodaksesi Jaa Teamsiin -ikkunan näkyviin.
   3. Lisää **Jaa kohteeseen** -kenttään vastaanottajaksi testikäyttäjä B.
   4. Odota, että linkki laajenee korttiin ja valitse Jaa.

3. Kirjaudu sisään Microsoft Teamsiin testikäyttäjänä B.

   1. Valitse keskustelu ja avaa keskustelu testikäyttäjän A kanssa.
   2. Valitse testikäyttäjän A lähettämän viestin kortissa tiedot-painike. Jos [!INCLUDE [prod_short](includes/prod_short.md)] -asiakasohjelma on näkyvissä ja vain luku-tilassa, määrittämäsi määritys onnistui.

> [!TIP]
> Tapahtuiko virhe? Katso [Microsoft 365 -käyttöoikeuksien käytön vianmääritys](admin-access-with-m365-license-troubleshooting.md).

## Katso myös

[Yleiskatsaus Business Centralin käyttämisestä Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license.md#minimum-requirements)  
[Microsoft 365 -käyttöoikeuksien käytön vianmääritys](admin-access-with-m365-license-troubleshooting.md)  
[Business Centralin ja Microsoft Teamsin integraatio](across-teams-overview.md)  
