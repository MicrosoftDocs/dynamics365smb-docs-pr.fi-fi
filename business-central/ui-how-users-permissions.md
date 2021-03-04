---
title: Luo käyttäjät käyttöoikeuksien mukaan | Microsoft Docs
description: Kuvaa, miten käyttäjät lisätään käyttöoikeuksiin perustuviin Business Central online- tai paikallisiin toimipaikkoihin.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 217b658e6a4c54996d3f0e9cfa7470f02908b380
ms.sourcegitcommit: 5d5451ee618f122c926e3189290f3765052f7077
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/11/2021
ms.locfileid: "4846338"
---
# <a name="create-users-according-to-licenses"></a>Luo käyttäjät käyttöoikeuksien mukaan

Tässä artikkelissa kuvataan, miten järjestelmänvalvojat luovat käyttäjiä ja määrittävät, ketkä voivat kirjautua sisään [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen ja mitkä käyttöoikeudet eri käyttäjätyypeille annetaan käyttöoikeuksien mukaan.

Kun luot käyttäjiä [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa, voit määrittää käyttäjille tiettyjä käyttöoikeuksia käyttöoikeusjoukkojen avulla ja järjestää käyttäjät käyttäjäryhmiin. Käyttäjäryhmien avulla on helppo hallita usean käyttäjän käyttöoikeuksia samanaikaisesti. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md). 

Lisätietoja erilaisista käyttöoikeustyypeistä ja lisensoinnin toiminnasta on [!INCLUDE[prod_short](includes/prod_short.md)]Dynamics 365:n käyttöoikeusoppaassa, jonka voi ladata osoitteesta [https://go.microsoft.com/fwlink/?LinkId=866544](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Käyttäjien ja käyttöoikeuksien hallintaprosessi vaihtelee sen mukaan, onko [!INCLUDE[prod_short](includes/prod_short.md)] käytössä online-tilassa vai paikallisesti. [!INCLUDE [prod_short](includes/prod_short.md)] online -käyttöön on lisättävä käyttäjiä Microsoft 365:stä. Paikallisissa käyttöönotoissa voit luoda, muokata ja poistaa käyttäjiä suoraan.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Käyttäjien ja lisenssien hallinta online-käyttöönotoissa

[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen online-versiossa tilaus määrittää käyttäjien lukumäärän. Se lisätään vuokraajalle Microsoft Partner Centerissä. Tämän tekee tavallisesti Microsoft-kumppanisi. Lisätietoja on kohdassa [Uuden asiakkaan lisääminen](/partner-center/add-a-new-customer) sekä [Asiakastilausten luominen, keskeyttäminen ja peruuttaminen](/partner-center/create-a-new-subscription) Microsoft Partner Center -ohjeessa.

Jotta voisit määrittää ketkä voivat kirjautua sisään [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen, tuotteen käyttöoikeudet täytyy määrittää käyttäjille niiden roolien mukaan, joita he käyttävät [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa. Tämä voidaan tehdä seuraavilla tavoilla:

- Yrityksen Microsoft 365 -järjestelmänvalvoja voi tehdä sen [Microsoft 365 -hallintakeskuksessa](https://admin.microsoft.com). Lisätietoja on kohdassa [Käyttäjien lisääminen yksittäin tai joukkona Microsoft 365:een](https://aka.ms/CreateOffice365Users).  
- Microsoft-kumppanit voivat määrittää lisenssejä Microsoft 365 Admin Centerissä tai Microsoft Partner Centerissä. Lisätietoja on Microsoft Partner Center -ohjeen kohdassa [Asiakastunnusten käyttäjien hallintatehtävät](/partner-center/assign-licenses-to-users).

Lisätietoja on Hallinnan ohjeen kohdassa [Business Central Onlinen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Käyttäjien lisääminen tai käyttäjätietojen ja käyttöoikeuksien delegoinnin päivittäminen Business Centralissa
Kun olet lisännyt käyttäjiä tai muuttanut käyttäjätietoja Microsoft 365 -hallintakeskuksessa, voit tuoda käyttäjätiedot nopeasti [!INCLUDE[prod_short](includes/prod_short.md)]iin. Näihin kuuluvat käyttöoikeusmääritykset. 

1. Kirjaudu sisään [!INCLUDE[prod_short](includes/prod_short.md)]iin järjestelmänvalvojatilillä.
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.  
3. Valitse **Päivitä käyttäjät Office 365:stä**.

Jos lisäät uusia käyttäjiä, seuraava vaihe on käyttäjäryhmien ja käyttöoikeuksien määrittäminen. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md). Jos päivität käyttäjätietoja ja päivitys sisältää käyttöoikeuden muutoksen, käyttäjät liitetään asianmukaiseen käyttäjäryhmään, ja niiden käyttöoikeusjoukot päivitetään. Lisätietoja on kohdassa [Käyttäjien käyttöoikeuksien hallinta käyttäjäryhmien kautta](ui-define-granular-permissions.md).  

> [!NOTE]
> Kaikille käyttäjille on määritettävä sama käyttöoikeus. Se voi olla joko Essential tai Premium. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/business-central/overview/) verkkosivulla.

Lisätietoja käyttäjätietojen synkronoimisesta Microsoft 365:n kanssa on kohdassa [Synkronoiminen Microsoft 365:n kanssa](#m365) -osiossa.

> [!NOTE]
> Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän Business Centraliin, jolloin he saavat käyttöönsä kirjanpitotietosi. Lisätietoja on kohdassa [Ulkoisen kirjanpitäjän kutsuminen Business Centraliin](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Järjestelmän käyttöoikeuden poistaminen käyttäjältä

Online-käyttöönotoissa voit poistaa käyttäjän [!INCLUDE[prod_short](includes/prod_short.md)] -käyttöoikeuden. Kaikki viittaukset käyttäjään säilytetään, mutta käyttäjä ei voi kirjautua sisään ja aktivoida istuntoja, jos käyttäjä on pysäytetty.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Avaa asianmukaisen käyttäjän **Käyttäjäkortti**-sivu ja valitse sitten **Tila**-kentässä **Ei käytössä**.
3. Voit antaa käyttöoikeuden uudelleen käyttäjälle määrittämällä **Tila**-kentän arvoksi **Käytössä**.

Voit myös poistaa käyttöoikeuden käyttäjältä Microsoft 365 -hallintakeskuksessa. Käyttäjä ei pysty kirjautumaan sisään. Lisätietoja on kohdassa [Käyttöoikeuksien poistaminen käyttäjiltä](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synkronointi Microsoft 365:n kanssa

Kun määrität käyttöoikeuden [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa Microsoft 365 -käyttäjälle, käyttäjän voi luoda kahdella eri tavalla [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa.  

- Järjestelmänvalvoja voi lisätä käyttäjän valitsemalla **Päivitä käyttäjät Office 365:stä** -toiminnon **Käyttäjät**-sivulta [Käyttäjän lisääminen tai käyttäjätietojen päivittäminen Business Centralissa](#adduser) -osiossa kuvatulla tavalla.
- Käyttöoikeustiedot päivitetään automaattisesti, kun käyttäjä kirjautuu sisään ensimmäisen kerran.

Molemmissa tapauksissa tehdään automaattisesti useita asetuksia. Ne on luetteloitu taulukon toisessa ja kolmannessa sarakkeessa.

Jos muutat käyttäjätietoja Microsoft 365:ssä, voit päivittää [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen vastaamaan muutosta. Käytä jotain **Käyttäjät**-sivun toimintoa päivitettävästä kohdasta riippuen. Toiminnot kuvataan alla olevan taulukon kolmessa viimeisessä sarakkeessa.

> [!NOTE]
> Seuraavassa taulukossa esitetyt toimet ovat tarkkoja, mutta ainoa tarvitsemasi on **Päivitä käyttäjät Office 365:stä**, joka on lisätty prosessin yksinkertaistamiseksi. Muut toiminnot poistetaan [!INCLUDE[prod_short](includes/prod_short.md)]in tulevassa versiossa.

|Mitä tapahtuu, kun:|Ensimmäinen käyttäjä, ensimmäinen sisäänkirjautuminen|Hae käyttäjät Microsoft 365:stä|Päivitä käyttäjät Microsoft 365:stä|Palauttaa käyttäjän oletuskäyttäjäryhmät|Päivitä käyttäjäryhmät|Päivitä käyttäjätiedot Microsoft 365:stä|
|-|-|-|-|-|-|-|
|Laajuus:|Nykyinen käyttäjä|Uudet käyttäjät Microsoft 365:ssä|Useita valittuja käyttäjiä|Yksittäinen valittu käyttäjä (paitsi nykyinen)|Useita valittuja käyttäjiä|Useita valittuja käyttäjiä|
|Luo uusi käyttäjä ja määritä SUPER-käyttöoikeusjoukko.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Päivitä käyttäjä Microsoft 365 -tietojen perusteella: tila, koko nimi, yhteyshenkilön sähköpostiosoite, todennuksen sähköpostiosoite.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Synkronoi käyttäjän palvelupaketit (lisenssit) ja käyttöoikeudet sekä määritetyt roolit Microsoft 365:ssä.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Lisää käyttäjä käyttäjäryhmiin nykyisen käyttäjän palvelupakettien mukaan. Poista SUPER-käyttöoikeusjoukko kaikilta muilta käyttäjiltä paitsi ensimmäiseltä sisäänkirjautuvalta käyttäjältä ja [järjestelmänvalvojilta](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Vähintään yksi SUPER-käyttäjä on määritettävä.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Poistaa määritetyt käyttäjäryhmät ja käyttöoikeudet manuaalisesti.|**X**<br /><br />Päivitä käyttäjäryhmän määritykset.| |

## <a name="the-device-license"></a>Laitteen käyttöoikeus

Dynamics 365 Business Central Devicen käyttöoikeuden avulla useat käyttäjät voivat käyttää käyttöoikeuden kattamaa laitetta samanaikaisesti. Tämä voi olla esimerkiksi myyntipiste-, tuotanto- tai varastolaite. Kun olet ostanut laitekäyttöoikeuksia tietyn määrän, samanaikaisesti sisäänkirjautuvia käyttäjiä voi olla enintään Dynamics 365 Business Central Devicen käyttäjäryhmään liitettyjen käyttäjien määrä. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/business-central/overview/) verkkosivulla.

Yrityksen Microsoft 365 -järjestelmänvalvoja tai Microsoft-kumppani voi luoda Dynamics 365 Business Central Device -käyttäjäryhmän ja lisätä laitteen käyttäjät jäseniksi [Microsoft 365 -hallintakeskukseen](https://admin.microsoft.com/) tai [Azure-portaaliin](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Laitteen käyttäjärajoitukset

Käyttäjät, joilla on laitteen käyttöoikeus, eivät voi suorittaa seuraavia tehtäviä kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]:

- Määritä työt, jotka suoritetaan työjonon ajoitettuina tehtävinä. Laitteen käyttäjät ovat samanaikaisia käyttäjiä, joten emme voi varmistaa, että mukana oleva käyttäjä on läsnä järjestelmässä, kun tehtävä suoritetaan, mikä on tarpeen.

- Laitteen käyttäjä ei voi olla ensimmäinen käyttäjä, joka sisäänkirjautuva käyttäjä. Järjestelmänvalvojan, täydet käyttöoikeudet omaavan käyttäjän tai ulkoisen kirjanpitäjän käyttäjän on kirjauduttava sisään ensimmäisenä, jotta hän voi määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in. Lisätietoja on Hallinnan ohjeen kohdassa [Business Central Onlinen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Laitekäyttäjät Dynamics 365 Business Central -ryhmän luominen

1. Siirry Microsoft 365 -hallintakeskuksen **Ryhmät**-sivulle.
2. Valitse **Lisää ryhmä** -toiminto.
3. Valitse **Valitse ryhmän tyyppi** -sivulla **Suojaus**-toiminto ja valitse sitten **Lisää**-toiminto.
4. Anna **Perustiedot**-sivulla ryhmän nimeksi **Dynamics 365 Business Central Device Users**.
  
   >[!NOTE]
   >Ryhmän nimi on annettava englanniksi täsmälleen vaiheessa 4 kerrotulla tavalla, vaikka käytössä muuten olisi toinen kieli.
5. Valitse **Sulje**-painike.

> [!NOTE]
> Voit myös luoda ryhmän, jonka tyyppi on Microsoft 365. Lisätietoja on kohdassa [Ryhmien vertaaminen](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Jäsenien lisääminen ryhmään

1. Päivitä Microsoft 365 -hallintakeskuksessa **Ryhmät**-sivu, jotta uusi ryhmä tulee näkyviin.
2. Valitse **Dynamics 365 Business Central Device Users** -ryhmä ja valitse sitten **Näytä kaikki ja hallitse jäseniä** -toiminto.
3. Valitse **Lisää jäseniä** -toiminto.
4. Valitse käyttäjät, jotka haluat lisätä, ja valitse sitten **Tallenna**-painike.
5. Valitse **Sulje**-painike kolme kertaa.

Voit lisätä niin monta käyttäjää Dynamics 365 Business Central Device Users -ryhmään kuin tarvitset. Kuitenkin niiden laitteiden määrä, joihin käyttäjät voivat kirjautua samanaikaisesti, määritetään ostettujen laitekäyttöoikeuksien määrän mukaan.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]- käyttöoikeutta ei tarvitse määrittää käyttäjille, jotka ovat laitteen Dynamics 365 Business Central Device Users -ryhmän jäseniä.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Käyttäjien ja lisenssien hallinta on-premises-käyttöönotoissa

Paikallisissa käyttöönotoissa käyttöoikeustiedostossa (.flf) on määritetty useita käyttöoikeuden omaavia käyttäjiä. Kun järjestelmänvalvoja tai Microsoft-kumppani lataa käyttöoikeustiedoston, järjestelmänvalvoja voi määrittää, mitkä käyttäjät voivat kirjautua [!INCLUDE[prod_short](includes/prod_short.md)]:een.

Järjestelmänvalvoja luo, muokkaa ja poistaa käyttäjiä paikallisesti käyttöönotoissa suoraan **Käyttäjät**-sivulta.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Käyttäjän muokkaaminen tai poistaminen paikallisesta käyttöoikeudesta

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse muokattava käyttäjä ja valitse sitten **Muokkaa**-toiminto.
3. Muuta tietoja tarvittaessa **Käyttäjän kortti** -sivulla.  
4. Poista käyttäjä valitsemalla ensin poistettava käyttäjä ja sitten **Poista**-toiminto.

> [!NOTE]
> Järjestelmänvalvoja voi määrittää paikallisissa käyttöönotoissa, miten käyttäjän tunnistetiedot todennetaan [!INCLUDE[server](includes/server.md)] -ilmentymässä. Kun luot käyttäjän, anna käyttämäsi tunnistetietotyyppi.
>
> Lisätietoja on [Todennus- ja käyttäjätietotyypit](/dynamics365/business-central/dev-itpro/administration/users-credential-types) -kohdassa [!INCLUDE[prod_short](includes/prod_short.md)]:n hallintaohjeessa.

## <a name="see-also"></a>Katso myös

[Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Profiilien hallinta](admin-users-profiles-roles.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen mukauttaminen](ui-customizing-overview.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Hallinta](admin-setup-and-administration.md)  
[Lisää käyttäjiä Microsoft 365 yrityksille](https://aka.ms/CreateOffice365Users)  
[Business Centralin tietoturva ja suojaus (hallinnon sisältö)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  


[!INCLUDE[footer-include](includes/footer-banner.md)]