---
title: Luo käyttäjät käyttöoikeuksien mukaan
description: Kuvaa, miten käyttäjät lisätään käyttöoikeuksiin perustuviin Business Central online- tai paikallisiin toimipaikkoihin.
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173
ms.date: 03/23/2022
ms.author: edupont
ms.openlocfilehash: 52d8c0fb735bb0667f2219f5ed73e914e236014a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512150"
---
# <a name="create-users-according-to-licenses"></a>Luo käyttäjät käyttöoikeuksien mukaan

Tässä artikkelissa kuvataan, miten järjestelmänvalvojat luovat käyttäjiä ja määrittävät, ketkä voivat kirjautua sisään kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]. Tämä artikkeli kattaa myös sen, miten määritetään käyttöoikeuksia eri tyyppisille käyttäjille tuotteen käyttöoikeuksien mukaan.

Kun luot käyttäjiä [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa, voit määrittää käyttäjille käyttöoikeuksia käyttöoikeusjoukkojen avulla ja järjestää käyttäjät käyttäjäryhmiin. Käyttäjäryhmien avulla on helppo hallita usean käyttäjän käyttöoikeuksia samanaikaisesti. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md).  

Lisätietoja erilaisista käyttöoikeustyypeistä ja [!INCLUDE[prod_short](includes/prod_short.md)]in käyttöoikeuksista on [ladattavassa Dynamics 365:n käyttöoikeusoppaassa](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Käyttäjien ja käyttöoikeuksien hallintaprosessi vaihtelee sen mukaan, onko [!INCLUDE[prod_short](includes/prod_short.md)] käytössä online-tilassa vai paikallisesti. [!INCLUDE [prod_short](includes/prod_short.md)] online -käyttöön on lisättävä käyttäjiä Microsoft 365:stä. Paikallisissa käyttöönotoissa voit luoda, muokata ja poistaa käyttäjiä suoraan.  

## <a name="manage-users-and-licenses-in-online-tenants"></a>Käyttäjien ja lisenssien hallinta online-vuokraajissa

[!INCLUDE[prod_short](includes/prod_short.md)]-ohjelman online-versiossa tilauksesi määrittää sallittujen käyttäjien määrän. Käyttäjät lisätään vuokraajaan Microsoft Partner Centerissä, tavallisesti sen tekee Microsoft-kumppani. Lisätietoja on kohdassa [Uuden asiakkaan lisääminen](/partner-center/add-a-new-customer) sekä [Asiakastilausten luominen, keskeyttäminen ja peruuttaminen](/partner-center/create-a-new-subscription) Microsoft Partner Center -ohjeessa.

Jotta voisit määrittää ketkä voivat kirjautua sisään [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen, tuotteen käyttöoikeudet täytyy määrittää käyttäjille työn mukaan, jota he tekevät [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa. Käyttöoikeuksia voi määrittää monella tavalla:

- Yrityksen Microsoft 365 -järjestelmänvalvoja voi tehdä sen [Microsoft 365 -hallintakeskuksessa](https://admin.microsoft.com). Lisätietoja on kohdassa [Käyttäjien lisääminen yksittäin tai joukkona Microsoft 365:een](/microsoft-365/admin/add-users/add-users).  
- Microsoft-kumppanit voivat määrittää lisenssejä Microsoft 365 Admin Centerissä tai Microsoft Partner Centerissä. Lisätietoja on Microsoft Partner Center -ohjeen kohdassa [Asiakastunnusten käyttäjien hallintatehtävät](/partner-center/assign-licenses-to-users).

Lisätietoja on Hallinnan ohjeen kohdassa [Business Central Onlinen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

> [!NOTE]
> Kun olet lisännyt käyttäjiä Microsoft 365 -hallintakeskukseen, suosittelemme, että päivität käyttäjätiedot [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa niin pian kuin mahdollista. Käyttäjätietojen pitäminen ajan tasalla on helppoa ja auttaa varmistamaan, että käyttäjät voivat aina kirjautua sisään. Lisätietoja on kohdassa [Käyttäjien lisääminen tai käyttäjätietojen ja käyttöoikeuksien delegoinnin päivittäminen Business Centralissa](#adduser).<br>
> 
> Käyttäjätietojen päivitys on erityisen tärkeää, jos olet mukauttanut käyttöoikeuksien joukkoja. Jos uusi käyttäjä yrittää kirjautua sisään [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen ennen hänen lisäämistään, hän ei välttämättä voi tehdä niin. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttöoikeuksien perusteella](#licensespermissions). 
> 
> Käyttäjät, jotka kohtaavat tämän ongelman, eivät kuitenkaan itse asiassa ole estettyjä. He voivat joko käyttää **Siirry takaisin kotisivulle** -toimintoa tai yksinkertaisesti kirjautua uudelleen ongelman ratkaisemiseksi.

### <a name="configure-permissions-based-on-licenses"></a><a name="licensespermissions"></a>Käyttöoikeuksien määrittäminen oikeuksien perusteella

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Järjestelmänvalvojat voivat määrittää käyttöoikeusjoukkoja ja käyttäjäryhmiä eri käyttöoikeustyyppien perusteella.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Esimerkiksi yleisesti käytetty käyttöoikeus, *Dynamics 365 Business Central -ryhmän jäsen*, on määritetty oletusarvon mukaan niin, että se sisältää käyttäjäryhmät *D365-ryhmän jäsenen* ja *Excel-vientitoiminto* sekä seuraavat käyttöoikeusjoukot:

- D365-LUKU
- D365-RYHMÄN JÄSEN
- MUOKKAA EXCELISSÄ - TARKASTELU
- VIE RAPORTTI EXCEL
- PAIKALLINEN

Jos tämä ei ole oikea asetus tietylle vuokraajalle, ylläpitäjä voi muuttaa kyseistä kokoonpanoa. Mukautetut käyttöoikeudet vaikuttavat kuitenkin vain uusiin käyttäjiin, joille kyseinen käyttöoikeus on määritetty. Käyttöoikeus ei vaikuta olemassa olevien käyttäjien käyttöoikeuksiin, joille käyttöoikeus on määritetty.  

1. Kirjaudu sisään [!INCLUDE[prod_short](includes/prod_short.md)]iin järjestelmänvalvojatilillä.  
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöoikeuden määritys** ja valitse sitten vastaava linkki.  

    Jos olet jo **Käyttäjät**-sivulla, voit myös käyttää **Päivitä käyttäjät Microsoft 365:stä** -opasta ja valita sitten oppaan ensimmäisellä sivulla **Määritä käyttöoikeuteen sisältyvät oikeudet** -linkki.  
3. Valitse mukautettava käyttöoikeus **Käyttöoikeuden määritys** -sivulta ja valitse sitten **Määritä**-toiminto.  
4. Valitse **Mukauta oikeuksia** -kenttä, kun haluat ottaa mukauttamisen käyttöön, ja tee tarvittavat muutokset.  

    Tässä esimerkissä järjestelmänvalvoja haluaa poistaa muokkaamisoikeuden Excelissä, joten hän poistaa *Excelin vientitoiminto* -käyttäjäryhmän tiimin jäsenen käyttöoikeudesta. Jatkossa uudet käyttäjät, joille on määritetty tiimin jäsenen käyttöoikeus, eivät voi viedä tietoja Exceliin. Jos organisaatio muuttaa mielensä tästä, he voivat vain palata **Käyttöoikeuden määritys** -sivulle ja poistaa kyseisen käyttöoikeustyypin räätälöinnin.  

> [!IMPORTANT]
> Tämä käyttöoikeuksien mukauttaminen on voimassa vain uusille käyttäjille, jotka määrittävät asianmukaisen käyttöoikeuden. Nykyisiä käyttäjiä ei päivitetä. Suosittelemme käyttöoikeuksien mukauttamista, ennen kuin käyttäjien käyttöoikeuksien aletaan määrittää Microsoft 365 -hallintakeskuksessa.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Käyttäjien lisääminen tai käyttäjätietojen ja käyttöoikeuksien delegoinnin päivittäminen Business Centralissa
Kun olet lisännyt käyttäjiä tai muuttanut käyttäjätietoja Microsoft 365 -hallintakeskuksessa, voit tuoda käyttäjätiedot nopeasti [!INCLUDE[prod_short](includes/prod_short.md)]iin. Tuontiin kuuluvat käyttöoikeusmääritykset. 

1. Kirjaudu sisään [!INCLUDE[prod_short](includes/prod_short.md)]iin järjestelmänvalvojatilillä.
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.  
3. Valitse **Päivitä käyttäjät Microsoft 365:stä**.

Kun lisäät uusia käyttäjiä, seuraava vaihe on käyttäjäryhmien ja käyttöoikeuksien määrittäminen. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md). Jos päivität käyttäjätietoja ja päivitys sisältää käyttöoikeuden muutoksen, käyttäjät liitetään asianmukaiseen käyttäjäryhmään, ja niiden käyttöoikeusjoukot päivitetään. Lisätietoja on kohdassa [Käyttäjien käyttöoikeuksien hallinta käyttäjäryhmien kautta](ui-define-granular-permissions.md).  

> [!NOTE]
> Kaikille ympäristön käyttäjille on määritettävä sama käyttöoikeus. Se voi olla joko Essential tai Premium. Lisätietoja on Microsoft Dynamics 365 Business Centralin käyttöoikeusoppaassa. Opas on ladattavissa [Business Centralin](https://dynamics.microsoft.com/business-central/overview/) verkkosivulla.

Lisätietoja käyttäjätietojen synkronoimisesta Microsoft 365:n kanssa on kohdassa [Synkronoiminen Microsoft 365:n kanssa](#m365) -osiossa.

> [!NOTE]
> Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän Business Centraliin, jolloin he saavat käyttöönsä kirjanpitotietosi. Lisätietoja on kohdassa [Ulkoisen kirjanpitäjän kutsuminen Business Centraliin](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Järjestelmän käyttöoikeuden poistaminen käyttäjältä

Online-käyttöönotoissa voit poistaa käyttäjän [!INCLUDE[prod_short](includes/prod_short.md)] -käyttöoikeuden. Kaikki viittaukset käyttäjään säilyvät. Käyttäjä ei kuitenkaan voi kirjautua sisään ja käyttäjän aktiiviset istunnot pysäytetään.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Avaa soveltuvan käyttäjän **Käyttäjäkortti**-sivu ja valitse sitten **Tila**-kentässä **Ei käytössä**.
3. Voit antaa käyttöoikeuden uudelleen käyttäjälle määrittämällä **Tila**-kentän arvoksi **Käytössä**.

Voit myös poistaa käyttöoikeuden käyttäjältä Microsoft 365 -hallintakeskuksessa. Käyttäjä ei pysty kirjautumaan sisään. Lisätietoja on kohdassa [Käyttöoikeuksien poistaminen käyttäjiltä](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synkronointi Microsoft 365:n kanssa

Kun määrität käyttöoikeuden [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa Microsoft 365 -käyttäjälle, käyttäjän voi luoda kahdella eri tavalla [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa.  

- Järjestelmänvalvoja voi lisätä käyttäjän valitsemalla **Päivitä käyttäjät Microsoft 365:stä** -toiminnon **Käyttäjät**-sivulta [Käyttäjän lisääminen tai käyttäjätietojen päivittäminen Business Centralissa](#adduser) -osiossa kuvatulla tavalla.
- Käyttöoikeustiedot päivitetään automaattisesti, kun käyttäjä kirjautuu sisään ensimmäisen kerran.

Molemmissa tapauksissa tehdään automaattisesti useita asetuksia. Ne asetukset on luetteloitu taulukon toisessa ja kolmannessa sarakkeessa.

Jos muutat käyttäjätietoja Microsoft 365:ssä, voit päivittää [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen vastaamaan muutosta. Käytä jotain **Käyttäjät**-sivun toimintoa päivitettävästä kohdasta riippuen. Toiminnot kuvataan alla olevan taulukon kolmessa viimeisessä sarakkeessa.

> [!NOTE]
> Seuraavassa taulukossa esitetyt toimet ovat tarkkoja, mutta ainoa tarvitsemasi on **Päivitä käyttäjät Microsoft 365:stä**, joka on lisätty prosessin yksinkertaistamiseksi. Muut toiminnot poistetaan [!INCLUDE[prod_short](includes/prod_short.md)]in tulevassa versiossa.

|Mitä tapahtuu, kun:|Ensimmäinen käyttäjä, ensimmäinen sisäänkirjautuminen|Hae käyttäjät Microsoft 365:stä|Päivitä käyttäjät Microsoft 365:stä|Palauttaa käyttäjän oletuskäyttäjäryhmät|Päivitä käyttäjäryhmät|Päivitä käyttäjätiedot Microsoft 365:stä|
|-|-|-|-|-|-|-|
|Laajuus:|Nykyinen käyttäjä|Uusia käyttäjiä Microsoft 365:ssä|Useita valittuja käyttäjiä|Yksittäinen valittu käyttäjä (paitsi nykyinen)|Useita valittuja käyttäjiä|Useita valittuja käyttäjiä|
|Luo uusi käyttäjä ja määritä SUPER-käyttöoikeusjoukko.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Päivitä käyttäjä Microsoft 365 -tietojen perusteella: tila, koko nimi, yhteyshenkilön sähköpostiosoite, todennuksen sähköpostiosoite.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Synkronoi käyttäjän palvelupaketit (lisenssit) ja käyttöoikeudet sekä määritetyt roolit Microsoft 365:ssä.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Lisää käyttäjä käyttäjäryhmiin nykyisen käyttäjän palvelupakettien mukaan. Poista SUPER-käyttöoikeusjoukko kaikilta muilta käyttäjiltä paitsi ensimmäiseltä sisäänkirjautuvalta käyttäjältä ja [järjestelmänvalvojilta](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Vähintään yksi SUPER-käyttäjä on määritettävä.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Poistaa määritetyt käyttäjäryhmät ja käyttöoikeudet manuaalisesti.|**X**<br /><br />Päivitä käyttäjäryhmän määritykset.| |

<!--
## The Device License
This section has been moved to [Licensing in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).
-->

## <a name="manage-users-and-licenses-in-on-premises-deployments"></a>Käyttäjien ja lisenssien hallinta on-premises-käyttöönotoissa

Paikallisissa käyttöönotoissa käyttöoikeustiedostossa (.flf) on määritetty useita käyttöoikeuden omaavia käyttäjiä. Kun järjestelmänvalvoja tai Microsoft-kumppani lataa käyttöoikeustiedoston, järjestelmänvalvoja voi määrittää, mitkä käyttäjät voivat kirjautua [!INCLUDE[prod_short](includes/prod_short.md)]:een.

Järjestelmänvalvoja luo, muokkaa ja poistaa käyttäjiä paikallisesti käyttöönotoissa suoraan **Käyttäjät**-sivulta.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Käyttäjän muokkaaminen tai poistaminen paikallisesta käyttöoikeudesta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
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
[Käyttöoikeudet Dynamics 365 Business Centralissa ](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Käyttäjien lisääminen Microsoft 365 for Businessiin](/microsoft-365/admin/add-users/add-users)  
[Business Centralin tietoturva ja suojaus (hallinnon sisältö)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Telemetriatunnuksen määrittäminen käyttäjille](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]