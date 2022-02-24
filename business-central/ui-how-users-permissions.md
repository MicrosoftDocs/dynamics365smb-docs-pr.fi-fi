---
title: Käyttöoikeuksien määrittäminen tai muokkaaminen | Microsoft Docs
description: Lisätietoja Office 365 -käyttäjien lisäämisestä Business Central -sovellukseen sekä käyttöoikeuksien ja suojausasetusten määrittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 01/06/2020
ms.author: sgroespe
ms.openlocfilehash: e07636b6211eb57205d41d982bfbfb4bc2d5b330
ms.sourcegitcommit: 0cb8a646dcba8f6d6336ebd008587874d25f4629
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030050"
---
# <a name="create-users-according-to-licenses"></a>Luo käyttäjät käyttöoikeuksien mukaan
Seuraavassa kuvataan miten järjestelmänvalvoja voi luoda käyttäjiä ja määrittää, ketkä voivat kirjautua sisään [!INCLUDE[d365fin](includes/d365fin_md.md)]iin ja mitkä perusoikeudet eri käyttäjätyypeillä on käyttöoikeuksien mukaan.

Kun käyttäjät on luotu [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan, voit määrittää käyttöoikeuksia käyttäjille käyttöoikeusjoukkojen avulla sekä järjestää käyttäjäryhmien käyttäjiä helppoa käyttöoikeuksien hallintaa varten. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).  

> [!NOTE]
> Käyttäjien ja lisenssien hallinnan prosessi vaihtelee sen mukaan, onko ratkaisu käytössä onlinessa vai paikallisesti. Online-käyttöönotoissa voit esimerkiksi poistaa ja ottaa käyttöön käyttäjän, joka on lisätty [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan. Paikallisissa käyttöönotoissa voit luoda, muokata ja poistaa käyttäjiä.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Käyttäjien ja lisenssien hallinta online-käyttöönotoissa
[!INCLUDE[d365fin](includes/d365fin_md.md)] -online-tilauksen määrittää käyttäjien lukumäärä, ja se lisätään vuokraajalle Microsoft Partner Centerissä, ja sen tekee tavallisesti Microsoft-kumppanisi. Lisätietoja on kohdassa [Uuden asiakkaan lisääminen](https://docs.microsoft.com/partner-center/add-a-new-customer) sekä [Asiakastilausten luominen, keskeyttäminen ja peruuttaminen](https://docs.microsoft.com/partner-center/create-a-new-subscription) Microsoft Partner Center -ohjeessa.

Jotta voisit määrittää ketkä voivat kirjautua sisään [!INCLUDE[d365fin](includes/d365fin_md.md)]:iin, tuotteen käyttöoikeudet täytyy määrittää käyttäjille niiden roolien mukaan, jotka he tekevät [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa. Tämä voidaan tehdä seuraavilla tavoilla:
- Yrityksen Office 365 -järjestelmänvalvoja voi tehdä sen [Microsoft 365 -hallintakeskuksessa](https://admin.microsoft.com). Lisätietoja on kohdassa [Käyttäjien lisääminen yksittäin tai joukkona Office 365:een](https://aka.ms/CreateOffice365Users).  
- Microsoft-kumppanit voivat määrittää lisenssejä Microsoft 365 Admin Centerissä tai Microsoft Partner Centerissä. Lisätietoja on Microsoft Partner Center -ohjeen kohdassa [Asiakastunnusten käyttäjien hallintatehtävät](https://docs.microsoft.com/partner-center/assign-licenses-to-users).

Lisätietoja on Kehittäjä- ja ITpro-ohjeen kohdassa [Business Central Onlinen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Kun käyttäjät, joilla on [!INCLUDE[d365fin](includes/d365fin_md.md)] -lisenssi on luotu Office 365:ssa, heidät voidaan tuoda **Käyttäjät**-sivulle [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa käyttämällä **Hae uudet käyttäjät Office 365:stä** -toimintoa.

### <a name="to-add-a-user-in-business-central"></a>Käyttäjän lisääminen Business Central -sovellukseen
Voit lisätä käyttäjiä Microsoft 365 admin Centeristä [!INCLUDE[d365fin](includes/d365fin_md.md)]online-käyttöön käyttämällä erityistä tuontitoimintoa.  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse **Hae uudet käyttäjät Office 365:stä** -toiminto.

Kaikki uudet Office 365 -tilaukseen luodut käyttäjät lisätään **Käyttäjät**-sivulla. Käyttäjille määritetään käyttöoikeusjoukot sen mukaan, mikä lisenssi on määritetty käyttäjälle Office 365:ssä. Voit määrittää tämän jälkeen käyttäjien tarkemmat käyttöoikeudet ja järjestää käyttäjät käyttäjäryhmiin käyttöoikeuksien hallinnan helpottamiseksi. Lisätietoja on kohdassa [Käyttöoikeuksien joukkojen määrittäminen käyttäjille](ui-define-granular-permissions.md#to-assign-permission-sets-to-users).

> [!NOTE]
> Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän Business Centraliin, jolloin he saavat käyttöönsä kirjanpitotietosi. Lisätietoja on kohdassa [Ulkoisen kirjanpitäjän kutsuminen Business Centraliin](finance-accounting.md#inviteaccountant)

### <a name="to-remove-a-users-access-to-the-system"></a>Järjestelmän käyttöoikeuden poistaminen käyttäjältä
Online-käyttöönotoissa voit poistaa käyttäjältä järjestelmän käyttöoikeuden määrittämällä **Tila**-kentän arvoksi **Ei käytössä**. Kaikki viittaukset käyttäjään säilyvät, mutta käyttäjä ei voi enää kirjautua järjestelmään ja käyttäjän aktiiviset istunnot lopetetaan.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Avaa asianmukaisen käyttäjän **Käyttäjäkortti**-sivu ja valitse sitten **Tila**-kentässä **Ei käytössä**.
3. Voit antaa käyttöoikeuden uudelleen käyttäjälle määrittämällä **Tila**-kentän arvoksi **Käytössä**.

Käyttäjän poistamisen lisäksi voit poistaa käyttäjän käyttöoikeuden Microsoft 365 -hallintakeskuksessa. Käyttäjä ei pysty kirjautumaan sisään. Lisätietoja on ohjeaiheessa [Käyttöoikeuksien poistaminen käyttäjiltä](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Käyttäjän määritetyn käyttöoikeuden muuttaminen
Joskus käyttäjälle määritettyä käyttöoikeutta on ehkä muutettava. Jos esimerkiksi päätät käyttää huoltohallintomoduulia ja haluat päivittää kaikki tärkeät käyttöoikeudet Premiumiin. Tai jos käyttäjän vastuu on muuttunut ja sinun täytyy vaihtaa tiimin jäsenen käyttöoikeus olennaiseen.

1. Muuta käyttöoikeutta Microsoft 365 -hallintakeskuksessa. Lisätietoja on kohdassa [Käyttäjien lisääminen yksittäin tai joukkona Office 365:een](https://aka.ms/CreateOffice365Users).
2. Kirjaudu sisään [!INCLUDE[d365fin](includes/d365fin_md.md)]:een järjestelmänvalvojana.
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
4. Valitse **Käyttäjät** sivulla **Palauta käyttäjän oletusarvoiset käyttäjäryhmät**-toiminto.

Käyttäjät siirtyvät asianmukaiseen käyttäjäryhmään, ja käyttöoikeusjoukot päivittyvät. Lisätietoja on kohdassa [Käyttäjien käyttöoikeuksien hallinta käyttäjäryhmien kautta](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Kaikille ratkaisun tavallisille käyttäjille on määritettävä sama käyttöoikeus, olennainen tai Premium.
> Tietoja käyttöoikeuksista on kohdassa [Microsoft Dynamics 365 Business Centralin käyttöoikeusopas](https://aka.ms/BusinessCentralLicensing).

### <a name="synchronization-with-office-365"></a>Synkronointi Office 365:n kanssa
Kun käyttöoikeus on määritetty käyttäjälle Office 365:ssä, voit luoda käyttäjän [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmassa kahdella tavalla. Järjestelmä tekee sen automaattisesti, kun käyttäjä kirjautuu ensimmäisen kerran, tai järjestelmänvalvoja voi lisätä käyttäjän valitsemalla **Käyttäjät**-sivun **Hae käyttäjät Office 365:stä**.

Molemmissa tapauksissa tehdään automaattisesti useita lisäasetuksia. Ne on luetteloitu taulukon toisessa ja kolmannessa sarakkeessa.

Jos muutat Office 365 -käyttäjää jälkeenpäin ja sinun täytyy synkronoida muutokset [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan, voit käyttää eri toimintoja **Käyttäjät**-sivulla sen mukaan, mitä tarkalleen haluat synkronoida. Ne on luetteloitu taulukon kolmessa viimeisessä sarakkeessa.

|Mitä tapahtuu, kun:|Ensimmäinen sisäänkirjautuminen|Hae käyttäjät Office 365:stä|Päivitä käyttäjät Office 365:stä|Palauttaa käyttäjän oletuskäyttäjäryhmät|Päivitä käyttäjäryhmät|
|-|-|-|-|-|-|
|Laajuus:|Nykyinen käyttäjä|Uusia käyttäjiä Office 365:ssä|Useita valittuja käyttäjiä|Yksittäinen valittu käyttäjä (paitsi nykyinen)|Useita valittuja käyttäjiä|
|Luo uusi käyttäjä ja määritä SUPER-käyttöoikeusjoukko.<br /><br />Ympäristö|**X**|**X**| | | |
|Päivitä käyttäjätietue todellisten tietojen perusteella Office 365:ssä: tila, koko nimi, yhteyshenkilön sähköpostiosoite, todennuksen sähköpostiosoite.<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph|**X**|**X**|**X**|**X**| |
|Synkronoi käyttäjän palvelupaketit (lisenssit) ja käyttöoikeudet sekä määritetyt roolit Office 365:ssä.<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans|**X**|**X**| |**X**|**X**|
|Lisää käyttäjä käyttäjäryhmiin nykyisen käyttäjän palvelupakettien mukaan. Peruuta SUPER-käyttöoikeusjoukko (Vähintään yksi SUPER-käyttäjä tarvitaan. Älä peruuta tätä oikeutta [järjestelmänvalvojilta](/dynamics365/business-central/dev-itpro/administration/tenant-administration).)<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups|**X**|**X**| |**X**<br /><br />Korvaa: Poista käyttäjä muista ryhmistä. Poista manuaalisesti määritetyt käyttöoikeus joukot.|**X**<br /><br />Lisäävä: Säilytä nykyinen jäsenyys käyttäjäryhmässä ja määritetyt käyttöoikeusjoukot ennallaan. Lisää käyttäjä ryhmiin vain tarvittaessa.|

## <a name="the-device-license"></a>Laitteen käyttöoikeus
Dynamics 365 Business Central laitteen käyttöoikeuden avulla useat käyttäjät voivat käyttää myyntipisteen laitetta, kauppatilan laitetta tai varaston laitetta, jolla on laitteen käyttöoikeus. Lisätietoja on kohdassa [Microsoft Dynamics 365 Business Centralin käyttöoikeusopas](https://aka.ms/BusinessCentralLicensing).

Laitteen käyttöoikeus on toteutettu samanaikaisten käyttäjien mallina. Kun olet ostanut x määrän laitelisenssejä, enintään x käyttäjää erityisestä ryhmästä nimeltä Dynamics 365 Business Central -laitekäyttäjät voi kirjautua samanaikaisesti.

Yrityksesi Office 365 -järjestelmänvalvojan tai Microsoft-kumppanin on luotava erityinen laiteryhmä ja lisättävä laitteen käyttäjät kyseisen ryhmän jäseniksi. He voivat tehdä tämän [Microsoft 365 -hallintakeskuksessa](https://admin.microsoft.com/) tai [Azure-portaalissa](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Laitteen käyttäjärajoitukset
Käyttäjät, joilla on laitteen käyttöoikeus, eivät voi suorittaa seuraavia tehtäviä kohteessa [!INCLUDE[d365fin](includes/d365fin_md.md)]:

-   Määritä työt, jotka suoritetaan työjonon ajoitettuina tehtävinä. Laitteen käyttäjät ovat samanaikaisia käyttäjiä, joten emme voi varmistaa, että mukana oleva käyttäjä on läsnä järjestelmässä, kun tehtävä suoritetaan, mikä on tarpeen.

-   Laitteen käyttäjä ei voi olla ensimmäinen käyttäjä, joka kirjautuu sisään. Järjestelmänvalvojan, täyden käyttäjän tai ulkoisen kirjanpitäjän käyttäjän on kirjauduttava sisään ensimmäisenä, jotta hän voi määrittää [!INCLUDE[d365fin](includes/d365fin_md.md)]in. Lisätietoja on kohdassa [Ylläpitäjät](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Laitekäyttäjät Dynamics 365 Business Central -ryhmän luominen
1.  Siirry Microsoft 365 -hallintakeskuksen **Ryhmät**-sivulle.
2.  Valitse **Lisää ryhmä** -toiminto.
3.  Valitse **Valitse ryhmän tyyppi** -sivulla **Suojaus**-toiminto ja valitse sitten **Lisää**-toiminto.
4.  Kirjoita **Perustiedot**-sivulla ryhmän nimeksi *Dynamics 365 Business Central Device Users*.

    > [!Note]
    > Ryhmän nimen on oltava kirjoitettu täsmälleen kuten yllä, myös ei-englanninkielisissä määrityksissä.
5. Valitse **Sulje**-painike.

> [!NOTE]
> Voit myös luoda ryhmän, jonka tyyppi on Office 365. Lisätietoja on kohdassa [Ryhmien vertaaminen](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>Jäsenien lisääminen ryhmään
1.  Päivitä Microsoft 365 -hallintakeskuksessa **Ryhmät**-sivu, jotta uusi ryhmä tulee näkyviin.
2.  Valitse **Dynamics 365 Business Central Device Users** -ryhmä ja valitse sitten **Näytä kaikki ja hallitse jäseniä** -toiminto.
3.  Valitse **Lisää jäseniä** -toiminto.
4.  Valitse käyttäjät, jotka haluat lisätä, ja valitse sitten **Tallenna**-painike.
5.  Valitse **Sulje**-painike kolme kertaa.

Voit lisätä niin monta käyttäjää Dynamics 365 Business Central Device Users -ryhmään kuin tarvitset. Niiden laitteiden määrä, joihin käyttäjät voivat kirjautua samanaikaisesti, määritetään ostettujen laitekäyttöoikeuksien määrän mukaan.

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_md.md)]- käyttöoikeutta ei tarvitse määrittää käyttäjille, jotka ovat laitteen Dynamics 365 Business Central Device Users -ryhmän jäseniä.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Käyttäjien ja lisenssien hallinta on-premises-käyttöönotoissa
Paikallisissa käyttöönotoissa käyttöoikeustiedostossa (.flf) on määritetty useita lisensoituja käyttäjiä. Kun järjestelmänvalvoja tai Microsoft-kumppani lataa käyttöoikeustiedoston, järjestelmänvalvoja voi määrittää, mitkä käyttäjät voivat kirjautua [!INCLUDE[d365fin](includes/d365fin_md.md)]:een.

Järjestelmänvalvoja luo, muokkaa ja poistaa käyttäjiä paikallisesti käyttöönotoissa suoraan **Käyttäjät**-sivulta.

### <a name="to-edit-or-delete-a-user-on-premises"></a>Käyttäjän muokkaaminen tai poistaminen paikallisesti
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse muokattava käyttäjä ja valitse sitten **Muokkaa**-toiminto.
3. Muuta tietoja tarvittaessa **Käyttäjän kortti** -sivulla.    
4. Poista käyttäjä valitsemalla ensin poistettava käyttäjä ja sitten **poista**-toiminto.

> [!NOTE]
> Järjestelmänvalvoja voi valita käyttäjille [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen paikallisten käyttöönottojen eri tunnistetietojen mekanismeista. Kun olet luonut käyttäjän, annat eri tietoja riippuen tunnistetiedoista, joita käytät tietyssä [!INCLUDE[server](includes/server.md)] -ilmentymässä.<br /><br />
> Lisätietoja on [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen kehittäjän ja ITPro-sisällön järjestelmänvalvojan osan [Todennus ja tunnistetietotyypit](/dynamics365/business-central/dev-itpro/administration/users-credential-types) -kohdassa.

## <a name="see-also"></a>Katso myös
[Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Profiilien hallinta](admin-users-profiles-roles.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen mukauttaminen](ui-customizing-overview.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Hallinta](admin-setup-and-administration.md)  
[Käyttäjien lisääminen Office 365 for Businessiin](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Centralin käyttöoikeusopas](https://aka.ms/BusinessCentralLicensing)  
[Turvallisuus ja suojaus Business Centralissa](/dynamics365/business-central/dev-itpro/security/security-and-protection) kohdassa Kehittäjä- ja IT-Pro -ohje
