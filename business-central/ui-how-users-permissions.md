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
ms.date: 07/14/2020
ms.author: edupont
ms.openlocfilehash: 35819d7db3e22059738c6738d998319d0eb6691c
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577226"
---
# <a name="create-users-according-to-licenses"></a>Luo käyttäjät käyttöoikeuksien mukaan

Tässä artikkelissa kuvataan, miten järjestelmänvalvojat luovat käyttäjiä ja määrittävät, ketkä voivat kirjautua sisään [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen ja mitkä käyttöoikeudet eri käyttäjätyypeille annetaan käyttöoikeuksien mukaan.

Kun luot käyttäjiä [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa, voit määrittää käyttäjille tiettyjä käyttöoikeuksia käyttöoikeusjoukkojen avulla ja järjestää käyttäjät käyttäjäryhmiin. Käyttäjäryhmien avulla on helppo hallita usean käyttäjän käyttöoikeuksia samanaikaisesti. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).  

> [!NOTE]
> Käyttäjien ja käyttöoikeuksien hallintaprosessi vaihtelee sen mukaan, onko [!INCLUDE[d365fin](includes/d365fin_md.md)] käytössä online-tilassa vai paikallisesti. [!INCLUDE [prodshort](includes/prodshort.md)] online -käyttöön on lisättävä käyttäjiä Office 365:stä. Paikallisissa käyttöönotoissa voit luoda, muokata ja poistaa käyttäjiä suoraan.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Käyttäjien ja lisenssien hallinta online-käyttöönotoissa

[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen online-versiossa tilaus määrittää käyttäjien lukumäärän. Se lisätään vuokraajalle Microsoft Partner Centerissä. Tämän tekee tavallisesti Microsoft-kumppanisi. Lisätietoja on kohdassa [Uuden asiakkaan lisääminen](/partner-center/add-a-new-customer) sekä [Asiakastilausten luominen, keskeyttäminen ja peruuttaminen](/partner-center/create-a-new-subscription) Microsoft Partner Center -ohjeessa.

Jotta voisit määrittää ketkä voivat kirjautua sisään [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen, tuotteen käyttöoikeudet täytyy määrittää käyttäjille niiden roolien mukaan, joita he käyttävät [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa. Tämä voidaan tehdä seuraavilla tavoilla:

- Yrityksen Office 365 -järjestelmänvalvoja voi tehdä sen [Microsoft 365 -hallintakeskuksessa](https://admin.microsoft.com). Lisätietoja on kohdassa [Käyttäjien lisääminen yksittäin tai joukkona Office 365:een](https://aka.ms/CreateOffice365Users).  
- Microsoft-kumppanit voivat määrittää lisenssejä Microsoft 365 Admin Centerissä tai Microsoft Partner Centerissä. Lisätietoja on Microsoft Partner Center -ohjeen kohdassa [Asiakastunnusten käyttäjien hallintatehtävät](/partner-center/assign-licenses-to-users).

Lisätietoja on Hallinnan ohjeen kohdassa [Business Central Onlinen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Kun käyttäjille on määritetty [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttöoikeus Office 365:ssä, voit tuoda heidät  **Käyttäjät**-sivulle [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa käyttämällä **Hae uudet käyttäjät Office 365:stä** -toimintoa.

### <a name="to-add-a-user-or-update-user-information-in-business-central"></a><a name="adduser"></a>Käyttäjän lisääminen tai käyttäjätietojen päivittäminen Business Centralissa

Käytä määritettyjä tuontitoimintoja, jos haluat lisätä uusia käyttäjiä tai päivittää käyttäjän tiedot [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen Microsoft 365 -hallintakeskuksessa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.  
2. Valitse tai **Päivitä käyttäjät Office 365:stä** -toiminto.

    Jos lisäät käyttäjiä ensimmäistä kertaa Office 365:stä, valitse **Hae uusia käyttäjiä Office 365:stä** -toiminto.  
3. Noudata näyttöön tulevan oppaan ohjeita.

Office 365 -tilauksen uudet käyttäjät ja käyttäjätiedot lisätään **Käyttäjät**-sivulle [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa. Voit nyt määrittää käyttäjäryhmiä ja käyttöoikeuksia. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).  

Lisätietoja käyttäjätietojen synkronoimisesta Office 365:n kanssa on kohdassa [Synkronoiminen Office 365:n kanssa](#synchronization-with-office-365) -osiossa.

> [!NOTE]
> Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän Business Centraliin, jolloin he saavat käyttöönsä kirjanpitotietosi. Lisätietoja on kohdassa [Ulkoisen kirjanpitäjän kutsuminen Business Centraliin](finance-accounting.md#inviteaccountant)

### <a name="to-change-the-assigned-license-for-a-user"></a>Käyttäjän määritetyn käyttöoikeuden muuttaminen

Joskus käyttäjälle määritettyä käyttöoikeutta on ehkä muutettava. Jos esimerkiksi päätät käyttää huoltohallintomoduulia ja haluat päivittää kaikki tärkeät käyttöoikeudet Premiumiin. Tai jos käyttäjän vastuu on muuttunut ja sinun täytyy vaihtaa tiimin jäsenen käyttöoikeudeksi Essential.

1. Muuta käyttöoikeutta Microsoft 365 -hallintakeskuksessa. Lisätietoja on kohdassa [Käyttäjien lisääminen yksittäin tai joukkona Office 365:een](https://aka.ms/CreateOffice365Users).
2. Kirjaudu sisään [!INCLUDE[d365fin](includes/d365fin_md.md)]:een järjestelmänvalvojana.
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
4. Valitse **Käyttäjät**sivulla **Palauta käyttäjän oletusarvoiset käyttäjäryhmät**-toiminto.

Käyttäjät siirtyvät asianmukaiseen käyttäjäryhmään, ja käyttöoikeusjoukot päivittyvät. Lisätietoja on kohdassa [Käyttäjien käyttöoikeuksien hallinta käyttäjäryhmien kautta](ui-define-granular-permissions.md).

> [!NOTE]
> Kaikille käyttäjille on määritettävä sama käyttöoikeus. Se voi olla joko Essential tai Premium. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/business-central/overview/) verkkosivulla.

### <a name="to-remove-a-users-access-to-the-system"></a>Järjestelmän käyttöoikeuden poistaminen käyttäjältä

Online-käyttöönotoissa voit poistaa käyttäjän [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttöoikeuden. Kaikki viittaukset käyttäjään säilytetään, mutta käyttäjä ei voi kirjautua sisään ja aktivoida istuntoja, jos käyttäjä on pysäytetty.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Avaa asianmukaisen käyttäjän **Käyttäjäkortti**-sivu ja valitse sitten **Tila**-kentässä **Ei käytössä**.
3. Voit antaa käyttöoikeuden uudelleen käyttäjälle määrittämällä **Tila**-kentän arvoksi **Käytössä**.

Voit myös poistaa käyttöoikeuden käyttäjältä Microsoft 365 -hallintakeskuksessa. Käyttäjä ei pysty kirjautumaan sisään. Lisätietoja on kohdassa [Käyttöoikeuksien poistaminen käyttäjiltä](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-office-365"></a>Synkronointi Office 365:n kanssa

Kun määrität käyttöoikeuden [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa Office 365 -käyttäjälle, käyttäjän voi luoda kahdella eri tavalla [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa.  

- Järjestelmänvalvoja voi lisätä käyttäjän valitsemalla **Päivitä käyttäjät Office 365:stä** -toiminnon **Käyttäjät**-sivulta [Käyttäjän lisääminen tai käyttäjätietojen päivittäminen Business Centralissa](#adduser) -osiossa kuvatulla tavalla.
- Käyttöoikeustiedot päivitetään automaattisesti, kun käyttäjä kirjautuu sisään ensimmäisen kerran.

Molemmissa tapauksissa tehdään automaattisesti useita asetuksia. Ne on luetteloitu taulukon toisessa ja kolmannessa sarakkeessa.

Jos muutat käyttäjätietoja Office 365:ssä, voit päivittää [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen vastaamaan muutosta. Käytä jotain **Käyttäjät**-sivun toimintoa päivitettävästä kohdasta riippuen. Toiminnot kuvataan alla olevan taulukon kolmessa viimeisessä sarakkeessa.

|Mitä tapahtuu, kun:|Ensimmäinen käyttäjä, ensimmäinen sisäänkirjautuminen|Hae käyttäjät Office 365:stä|Päivitä käyttäjät Office 365:stä|Palauttaa käyttäjän oletuskäyttäjäryhmät|Päivitä käyttäjäryhmät|
|-|-|-|-|-|-|
|Laajuus:|Nykyinen käyttäjä|Uusia käyttäjiä Office 365:ssä|Useita valittuja käyttäjiä|Yksittäinen valittu käyttäjä (paitsi nykyinen)|Useita valittuja käyttäjiä|
|Luo uusi käyttäjä ja määritä SUPER-käyttöoikeusjoukko.<br /><br /><!--Platform-->|**X**|| | | |
|Päivitä käyttäjätietue todellisten tietojen perusteella Office 365:ssä: tila, koko nimi, yhteyshenkilön sähköpostiosoite, todennuksen sähköpostiosoite.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**| |
|Synkronoi käyttäjän palvelupaketit (lisenssit) ja käyttöoikeudet sekä määritetyt roolit Office 365:ssä.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**| |**X**|**X**|
|Lisää käyttäjä käyttäjäryhmiin nykyisen käyttäjän palvelupakettien mukaan. Poista SUPER-käyttöoikeusjoukko kaikilta muilta käyttäjiltä paitsi ensimmäiseltä sisäänkirjautuvalta käyttäjältä ja [järjestelmänvalvojilta](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Vähintään yksi SUPER-käyttäjä on määritettävä.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**| |**X**<br /><br />Poistaa määritetyt käyttäjäryhmät ja käyttöoikeudet manuaalisesti.|**X**<br /><br />Päivitä käyttäjäryhmän määritykset.|

## <a name="the-device-license"></a>Laitteen käyttöoikeus

Dynamics 365 Business Central Devicen käyttöoikeuden avulla useat käyttäjät voivat käyttää käyttöoikeuden kattamaa laitetta samanaikaisesti. Tämä voi olla esimerkiksi myyntipiste-, tuotanto- tai varastolaite. Kun olet ostanut laitekäyttöoikeuksia tietyn määrän, samanaikaisesti sisäänkirjautuvia käyttäjiä voi olla enintään Dynamics 365 Business Central Devicen käyttäjäryhmään liitettyjen käyttäjien määrä. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/business-central/overview/) verkkosivulla.

Yrityksen Office 365 -järjestelmänvalvoja tai Microsoft-kumppani voi luoda Dynamics 365 Business Central Device -käyttäjäryhmän ja lisätä laitteen käyttäjät jäseniksi [Microsoft 365 -hallintakeskukseen](https://admin.microsoft.com/) tai [Azure-portaaliin](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Laitteen käyttäjärajoitukset

Käyttäjät, joilla on laitteen käyttöoikeus, eivät voi suorittaa seuraavia tehtäviä kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]:

- Määritä työt, jotka suoritetaan työjonon ajoitettuina tehtävinä. Laitteen käyttäjät ovat samanaikaisia käyttäjiä, joten emme voi varmistaa, että mukana oleva käyttäjä on läsnä järjestelmässä, kun tehtävä suoritetaan, mikä on tarpeen.

- Laitteen käyttäjä ei voi olla ensimmäinen käyttäjä, joka sisäänkirjautuva käyttäjä. Järjestelmänvalvojan, täydet käyttöoikeudet omaavan käyttäjän tai ulkoisen kirjanpitäjän käyttäjän on kirjauduttava sisään ensimmäisenä, jotta hän voi määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in. Lisätietoja on Hallinnan ohjeen kohdassa [Business Central Onlinen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Laitekäyttäjät Dynamics 365 Business Central -ryhmän luominen

1. Siirry Microsoft 365 -hallintakeskuksen**Ryhmät**-sivulle.
2. Valitse **Lisää ryhmä** -toiminto.
3. Valitse **Valitse ryhmän tyyppi** -sivulla **Suojaus**-toiminto ja valitse sitten **Lisää**-toiminto.
4. Anna **Perustiedot**-sivulla ryhmän nimeksi **Dynamics 365 Business Central Device Users**.
  
   >[!NOTE]
   >Ryhmän nimi on annettava englanniksi täsmälleen vaiheessa 4 kerrotulla tavalla, vaikka käytössä muuten olisi toinen kieli.
5. Valitse **Sulje**-painike.

> [!NOTE]
> Voit myös luoda ryhmän, jonka tyyppi on Office 365. Lisätietoja on kohdassa [Ryhmien vertaaminen](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Jäsenien lisääminen ryhmään

1. Päivitä Microsoft 365 -hallintakeskuksessa **Ryhmät**-sivu, jotta uusi ryhmä tulee näkyviin.
2. Valitse **Dynamics 365 Business Central Device Users** -ryhmä ja valitse sitten **Näytä kaikki ja hallitse jäseniä** -toiminto.
3. Valitse **Lisää jäseniä** -toiminto.
4. Valitse käyttäjät, jotka haluat lisätä, ja valitse sitten **Tallenna**-painike.
5. Valitse **Sulje**-painike kolme kertaa.

Voit lisätä niin monta käyttäjää Dynamics 365 Business Central Device Users -ryhmään kuin tarvitset. Kuitenkin niiden laitteiden määrä, joihin käyttäjät voivat kirjautua samanaikaisesti, määritetään ostettujen laitekäyttöoikeuksien määrän mukaan.

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_md.md)]- käyttöoikeutta ei tarvitse määrittää käyttäjille, jotka ovat laitteen Dynamics 365 Business Central Device Users -ryhmän jäseniä.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Käyttäjien ja lisenssien hallinta on-premises-käyttöönotoissa

Paikallisissa käyttöönotoissa käyttöoikeustiedostossa (.flf) on määritetty useita käyttöoikeuden omaavia käyttäjiä. Kun järjestelmänvalvoja tai Microsoft-kumppani lataa käyttöoikeustiedoston, järjestelmänvalvoja voi määrittää, mitkä käyttäjät voivat kirjautua [!INCLUDE[d365fin](includes/d365fin_md.md)]:een.

Järjestelmänvalvoja luo, muokkaa ja poistaa käyttäjiä paikallisesti käyttöönotoissa suoraan **Käyttäjät**-sivulta.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Käyttäjän muokkaaminen tai poistaminen paikallisesta käyttöoikeudesta

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse muokattava käyttäjä ja valitse sitten **Muokkaa**-toiminto.
3. Muuta tietoja tarvittaessa **Käyttäjän kortti** -sivulla.  
4. Poista käyttäjä valitsemalla ensin poistettava käyttäjä ja sitten **Poista**-toiminto.

> [!NOTE]
> Järjestelmänvalvoja voi määrittää paikallisissa käyttöönotoissa, miten käyttäjän tunnistetiedot todennetaan [!INCLUDE[server](includes/server.md)] -ilmentymässä. Kun luot käyttäjän, anna käyttämäsi tunnistetietotyyppi.
>
> Lisätietoja on [Todennus- ja käyttäjätietotyypit](/dynamics365/business-central/dev-itpro/administration/users-credential-types) -kohdassa [!INCLUDE[d365fin](includes/d365fin_md.md)]:n hallintaohjeessa.

## <a name="see-also"></a>Katso myös

[Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Profiilien hallinta](admin-users-profiles-roles.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen mukauttaminen](ui-customizing-overview.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Hallinta](admin-setup-and-administration.md)  
[Käyttäjien lisääminen Office 365 for Businessiin](https://aka.ms/CreateOffice365Users)  
[Business Centralin tietoturva ja suojaus (hallinnon sisältö)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
