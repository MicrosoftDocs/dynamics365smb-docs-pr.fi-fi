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
ms.date: 11/07/2019
ms.author: sgroespe
ms.openlocfilehash: c64a14ed66668f8c3cbe09e8db3430a7dc25db5c
ms.sourcegitcommit: 2a6d629cf290645606356b714a77ef2872bdec64
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/07/2019
ms.locfileid: "2774817"
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

Kun käyttäjät, joilla on [!INCLUDE[d365fin](includes/d365fin_md.md)] -lisenssi on luotu Office 365:ssa, heidät voidaan tuoda **Käyttäjät**-sivulle [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa käyttämällä **Hae käyttäjät Office 365:stä** -toimintoa.

### <a name="to-add-a-user-in-business-central"></a>Käyttäjän lisääminen Business Central -sovellukseen
Voit lisätä käyttäjiä Microsoft 365 admin Centeristä [!INCLUDE[d365fin](includes/d365fin_md.md)]online-käyttöön käyttämällä erityistä tuontitoimintoa.  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Valitse **Hae käyttäjät Office 365:stä** -toiminto.

Kaikki uudet Office 365 -tilaukseen luodut käyttäjät lisätään **Käyttäjät**-sivulla. Käyttäjille määritetään käyttöoikeusjoukot sen mukaan, mikä lisenssi on määritetty käyttäjälle Office 365:ssä. Voit määrittää tämän jälkeen käyttäjien tarkemmat käyttöoikeudet ja järjestää käyttäjät käyttäjäryhmiin käyttöoikeuksien hallinnan helpottamiseksi. Lisätietoja on kohdassa [Käyttöoikeuksien joukkojen määrittäminen käyttäjille](ui-define-granular-permissions.md#to-assign-permission-sets-to-users).

### <a name="to-remove-a-users-access-to-the-system"></a>Järjestelmän käyttöoikeuden poistaminen käyttäjältä
Online-käyttöönotoissa voit poistaa käyttäjältä järjestelmän käyttöoikeuden määrittämällä **Tila**-kentän arvoksi **Ei käytössä**. Kaikki viittaukset käyttäjään säilyvät, mutta käyttäjä ei voi enää kirjautua järjestelmään ja käyttäjän aktiiviset istunnot lopetetaan.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
2. Avaa asianmukaisen käyttäjän **Käyttäjäkortti**-sivu ja valitse sitten **Tila**-kentässä **Ei käytössä**.
3. Voit antaa käyttöoikeuden uudelleen käyttäjälle määrittämällä **Tila**-kentän arvoksi **Käytössä**.

Käyttäjän poistamisen lisäksi voit poistaa käyttäjän käyttöoikeuden Office 365 -hallintakeskuksessa. Käyttäjä ei pysty kirjautumaan sisään. Lisätietoja on ohjeaiheessa [Käyttöoikeuksien poistaminen käyttäjiltä](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Käyttäjän määritetyn käyttöoikeuden muuttaminen
Joskus käyttäjälle määritettyä käyttöoikeutta on ehkä muutettava. Jos esimerkiksi päätät käyttää huoltohallintomoduulia ja haluat päivittää kaikki tärkeät käyttöoikeudet Premiumiin. Tai jos käyttäjän vastuu on muuttunut ja sinun täytyy vaihtaa tiimin jäsenen käyttöoikeus olennaiseen.

1. Muuta käyttöoikeutta Office 365 -hallintakeskuksessa. Lisätietoja on kohdassa [Käyttäjien lisääminen yksittäin tai joukkona Office 365:een](https://aka.ms/CreateOffice365Users).
2. Kirjaudu sisään [!INCLUDE[d365fin](includes/d365fin_md.md)]:een järjestelmänvalvojana.
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten liittyvä linkki.
4. Vaihtoehtoisesti voit valita **Käyttäjät**-sivulla **Päivitä kaikki käyttäjäryhmät** -toiminnon.
Käyttäjät siirtyvät asianmukaiseen käyttäjäryhmään, ja käyttöoikeusjoukot päivittyvät. Lisätietoja on kohdassa [Käyttäjien käyttöoikeuksien hallinta käyttäjäryhmien kautta](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Kaikille ratkaisun tavallisille käyttäjille on määritettävä sama käyttöoikeus, olennainen tai Premium.
> Tietoja käyttöoikeuksista on kohdassa [Microsoft Dynamics 365 Business Centralin käyttöoikeusopas](https://aka.ms/BusinessCentralLicensing).

## <a name="managing-users-and-licenses-in-online-deployments"></a>Käyttäjien ja lisenssien hallinta online-käyttöönotoissa
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
