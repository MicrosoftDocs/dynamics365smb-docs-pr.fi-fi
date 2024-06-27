---
title: Käyttäjien luominen käyttöoikeuksien mukaan
description: 'Kuvaa, miten käyttäjät lisätään käyttöoikeuksiin perustuviin Business Central online- tai paikallisiin toimipaikkoihin.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173'
ms.date: 05/03/2024
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Käyttäjien luominen käyttöoikeuksien mukaan

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Tässä artikkelissa kuvataan, miten järjestelmänvalvojat luovat käyttäjiä ja määrittävät, ketkä voivat kirjautua sisään kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]. Tämä artikkeli kuvaa sitä, miten määritetään käyttöoikeuksia eri käyttäjille tuotteen käyttöoikeuksien mukaan.

Kun luot käyttäjiä [!INCLUDE[prod_short](includes/prod_short.md)] -järjestelmässä, myönnät heille käyttöoikeuksia käyttöoikeuksien joukkojen avulla. Voit myös järjestää käyttäjiä käyttäjäryhmiin. Käyttäjäryhmien avulla on helppo hallita useiden käyttäjien käyttöoikeuksia ja muita asetuksia samanaikaisesti. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md).  

Lisätietoja erilaisista käyttöoikeustyypeistä ja [!INCLUDE[prod_short](includes/prod_short.md)]in käyttöoikeuksista on [ladattavassa Dynamics 365:n käyttöoikeusoppaassa](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Käyttäjien ja käyttöoikeuksien hallintaprosessi vaihtelee sen mukaan, onko [!INCLUDE[prod_short](includes/prod_short.md)] käytössä online-tilassa vai paikallisesti. [!INCLUDE [prod_short](includes/prod_short.md)] online -käyttöön on lisättävä käyttäjiä Microsoft 365:stä. Paikallisissa käyttöönotoissa voit luoda, muokata ja poistaa käyttäjiä suoraan.  

## Käyttäjien ja lisenssien hallinta online-vuokraajissa

[!INCLUDE[prod_short](includes/prod_short.md)] -järjestelmän käyttäjätilit täytyy luoda ensin Microsoft 365 -hallintakeskuksessa. Nämä käyttäjätilit eivät koske vain [!INCLUDE [prod_short](includes/prod_short.md)]ia. Jos tilaat muita suunnitelmia, niillä voidaan kirjautua muihin sovelluksiin, kuten Power BI. Lisätietoja käyttäjien luomisesta Microsoft 365 -hallintakeskuksessa on kohdassa [Käyttäjien lisääminen Microsoft-hallintakeskuksessa](/microsoft-365/admin/add-users/add-users).

[!INCLUDE[prod_short](includes/prod_short.md)] online -tilauksesi määrittää sallittujen [!INCLUDE[prod_short](includes/prod_short.md)] -käyttöoikeuksien määrän. Käyttäjät lisätään vuokraajaan Microsoft Partner Centerissä, tavallisesti sen tekee Microsoft-kumppani. Lisätietoja on kohdassa [Business Central Onlinen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Kohdistat käyttöoikeudet käyttäjille sen mukaan, mitä töitä kukin käyttäjä tekee [!INCLUDE[prod_short](includes/prod_short.md)] -järjestelmässä. Käyttöoikeuksia voi määrittää monella tavalla:

- Yrityksen Microsoft 365 -järjestelmänvalvoja voi tehdä sen [Microsoft 365 -hallintakeskuksessa](https://admin.microsoft.com). Lisätietoja on kohdassa [Käyttäjien lisääminen yksittäin tai joukkona Microsoft 365:een](/microsoft-365/admin/add-users/add-users).  
- Microsoft-kumppanit voivat määrittää lisenssejä Microsoft 365 Admin Centerissä tai Microsoft Partner Centerissä. Lisätietoja on Microsoft Partner Center -ohjeen kohdassa [Asiakastunnusten käyttäjien hallintatehtävät](/partner-center/assign-licenses-to-users).

Lisätietoja on Hallinnan ohjeen kohdassa [Business Central Onlinen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Kun käyttäjätilit on luotu Microsoft 365 -hallintakeskuksessa, ne voidaan tuoda [!INCLUDE [prod_short](includes/prod_short.md)]iin kahdella seuraavalla tavalla:

- Käyttäjätili tuodaan automaattisesti, kun käyttäjä kirjautuu [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan ensimmäisen kerran.

   > [!NOTE]
   > Et voi poistaa käyttäjää sen jälkeen, kun tämä kirjautuu sisään [!INCLUDE [prod_short](includes/prod_short.md)] Onlineen.

- Järjestelmänvalvoja voi tuoda käyttäjiä valitsemalla  **Päivitä käyttäjät Microsoft 365:stä** -toiminnon **Käyttäjät* -sivulta.

Molemmilla lähestymistavoilla on omat etunsa, ja niitä voi käyttää samanaikaisesti. Molemmat lähestymistavat sallivat järjestelmänvalvojien määrittää [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman ennakoivasti kohdistaakseen alustavat käyttöoikeudet, käyttäjäryhmät ja käyttäjäprofiilit. Järjestelmänvalvojat voivat hallita käyttöoikeuksia, käyttäjäryhmiä ja profiileja tarkemmin **Päivitä käyttäjät Microsoft 365:stä** -toiminnon avulla. Se on ihanteellinen lähestymistapa, kun olet määrittämässä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman ensimmäistä kertaa, ennen kuin käyttäjät kirjautuvat sisään tai lisättäessä uutta käyttäjäryhmää.

> [!NOTE]
> Kun olet lisännyt käyttäjiä Microsoft 365 -hallintakeskukseen, suosittelemme, että päivität käyttäjätiedot [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa niin pian kuin mahdollista. Käyttäjätietojen pitäminen ajan tasalla on helppoa ja auttaa varmistamaan, että käyttäjät voivat aina kirjautua sisään. Lisätietoja on kohdassa [Käyttäjien lisääminen tai käyttäjätietojen ja käyttöoikeuksien delegoinnin päivittäminen Business Centralissa](#adduser).<br>
>
> Käyttäjätietojen päivitys on erityisen tärkeää, jos olet mukauttanut käyttöoikeuksien joukkoja. Jos uusi käyttäjä yrittää kirjautua sisään [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen ennen hänen lisäämistään, hän ei välttämättä voi tehdä niin. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttöoikeuksien perusteella](#licensespermissions).
>
> Käyttäjät, jotka kohtaavat tämän ongelman, eivät kuitenkaan itse asiassa ole estettyjä. He voivat joko käyttää **Siirry takaisin kotisivulle** -toimintoa tai yksinkertaisesti kirjautua uudelleen ongelman ratkaisemiseksi.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Lisätietoja hallintasisällössä: [Valtuutettu järjestelmänvalvojan käyttöoikeus Business Central Onlineen](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="licensespermissions"></a>Käyttöoikeuksien määrittäminen oikeuksien perusteella

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Järjestelmänvalvojat voivat määrittää käyttöoikeuksien joukkoja ja käyttäjäryhmiä kullekin käyttöoikeudelle.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Esimerkiksi yleisesti käytetty *Dynamics 365 Business Central Team Member* -käyttöoikeus sisältää oletusarvoisesti seuraavat käyttöoikeuksien joukot:

- D365-LUKU
- D365-RYHMÄN JÄSEN
- MUOKKAA EXCELISSÄ - TARKASTELU
- VIE RAPORTTI EXCEL
- PAIKALLINEN

Muut käyttöoikeuksien joukot lisätään automaattisesti käyttöoikeuteen kohdistettujen käyttäjäryhmien perusteella. Kun luot uutta käyttäjää tämän käyttöoikeuden perusteella, [!INCLUDE[prod_short](includes/prod_short.md)] kohdistaa käyttäjäryhmistä ja käyttöoikeudesta saadut käyttöoikeuksien joukot. Käyttäjälle kohdistetaan samat alustavat käyttöoikeudet, jos käyttäjätili luotiin automaattisesti [!INCLUDE[prod_short](includes/prod_short.md)] -järjestelmässä tai jos järjestelmänvalvoja käytti **Päivitä käyttäjät Microsoft 365:stä** -toimintoa **Käyttäjät**-sivulla.

Jos tämä oletusarvoinen kokoonpano ei sovi tietylle ympäristölle, järjestelmänvalvoja voi muuttaa sitä. Mukautetut käyttöoikeudet vaikuttavat kuitenkin vain uusiin käyttäjiin, joille kyseinen käyttöoikeus on määritetty. Käyttöoikeus ei vaikuta olemassa olevien käyttäjien käyttöoikeuksiin, joille käyttöoikeus on määritetty.  

1. Kirjaudu sisään [!INCLUDE[prod_short](includes/prod_short.md)]iin järjestelmänvalvojatilillä.  
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöoikeuden määritys** ja valitse sitten vastaava linkki.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. Valitse mukautettava käyttöoikeus **Käyttöoikeuden määritys** -sivulta ja valitse sitten **Määritä**-toiminto.  
4. Valitse **Mukauta oikeuksia** -kenttä, kun haluat ottaa mukauttamisen käyttöön, ja tee muutokset.  

    Tässä esimerkissä järjestelmänvalvoja haluaa poistaa muokkaamisoikeuden Excelissä, joten hän poistaa *Excelin vientitoiminto* -käyttäjäryhmän tiimin jäsenen käyttöoikeudesta. Tämän jälkeen uudet käyttäjät, joille on määritetty ryhmän jäsen -käyttöoikeus, eivät voi viedä tietoja Exceliin. Jos organisaatio muuttaa mielensä tästä aiheesta, he voivat vain palata **Käyttöoikeuden määritys** -sivulle ja poistaa kyseisen käyttöoikeustyypin räätälöinnin.  

> [!IMPORTANT]
> Tämä käyttöoikeuksien mukauttaminen koskee vain uusia käyttäjiä, joille kohdistat asiaankuuluvan käyttöoikeuden. Nykyisiä käyttäjiä ei päivitetä. Suosittelemme käyttöoikeuksien mukauttamista, ennen kuin käyttäjien käyttöoikeuksien aletaan määrittää Microsoft 365 -hallintakeskuksessa.

### <a name="adduser"></a>Käyttäjien lisääminen tai käyttäjätietojen ja käyttöoikeuksien delegoinnin päivittäminen Business Centralissa

Kun olet lisännyt käyttäjiä tai muuttanut käyttäjätietoja Microsoft 365 -hallintakeskuksessa, voit tuoda käyttäjätiedot nopeasti [!INCLUDE[prod_short](includes/prod_short.md)]iin. Tuontiin kuuluvat käyttöoikeusmääritykset.  

> [!TIP]
> Jos käyttäjätiedot on päivitettävä ja käyttäjiä on runsaasti, luettelo voidaan tarkentaa suodatinruudun avulla. Suodatusperusteena voidaan käyttää perustietoja, kuten käyttäjänimeä, tai määrittämällä teknisiä suodattimia, kuten käyttäjän suojaustunnuksen.

1. Kirjaudu sisään [!INCLUDE[prod_short](includes/prod_short.md)]iin järjestelmänvalvojatilillä.
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.  
3. Valitse **Päivitä käyttäjät Microsoft 365:stä**.

> [!IMPORTANT]  
> Käyttäjien synkronoinnin suorittaminen Microsoft 365:stä **Päivitä käyttäjät Microsoft 365:stä** -opasta käyttämällä edellyttää SUPER- käyttöoikeuksien joukkoa.

> [!NOTE]
> **Päivitä käyttäjät Microsoft 365:stä** -opas ei päivitä käyttäjiä, joille ei ole määritetty lisenssiä, kuten henkilöä, joka on Yleinen järjestelmänvalvoja ja Dynamics 365 -järjestelmänvalvoja. Nämä käyttäjät päivittävät seuraavan kerran, kun he kirjautuvat ympäristöön.

Seuraava vaihe uusille käyttäjille on käyttäjäryhmien ja käyttöoikeuksien kohdistaminen. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md). Jos päivität käyttäjän ja päivitys sisältää käyttöoikeuden muutoksen, [!INCLUDE [prod_short](includes/prod_short.md)] määrittää käyttäjät asianmukaiseen käyttäjäryhmään ja päivittää niiden käyttöoikeuksien joukot. Lisätietoja on kohdassa [Käyttäjien käyttöoikeuksien hallinta käyttäjäryhmien kautta](ui-define-granular-permissions.md).  

> [!NOTE]
> Vuoden 2024 1. julkaisuaallossa, Premium-lisenssin käyttäjä voi kirjautua sisään yritykseen, jossa **Käyttökokemus**-kentän arvo on **Yritystiedot**-sivulla **Olennainen**. Premium-käyttäjä ei voi kuitenkaan käyttää mitään Premium-käyttöoikeuden ominaisuuksia. Tämä ei toimi vastakkaiseen tilanteeseen. Käyttäjät, joilla on Olennainen-lisenssi, eivät voi kirjautua sisään yritykseen, jonka **Käyttäjäkokemus**-asetuksena on **Premium** **Yrityksen tiedot** -sivulla. Lisätietoja käyttöoikeuksista on [Business Centralin](https://dynamics.microsoft.com/business-central/overview/) sivustolla.

Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän [!INCLUDE[prod_short](includes/prod_short.md)]iin, jolloin he saavat käyttöönsä kirjanpitotietosi. Lisätietoja on kohdassa [Ulkoisen kirjanpitäjän kutsuminen Business Centraliin](finance-accounting.md#inviteaccountant).

Lisätietoja käyttäjätietojen synkronoimisesta Microsoft 365:n kanssa on [Synkronoiminen Microsoft 365:n kanssa](#m365) -osiossa.

> [!NOTE]
> Jos käytä ulkoista kirjanpitäjää kirjojen ja talousraportoinnin hallinnassa, voit kutsua kirjanpitäjän [!INCLUDE[prod_short](includes/prod_short.md)]iin, jolloin he saavat käyttöönsä kirjanpitotietosi. Lisätietoja on kohdassa [Ulkoisen kirjanpitäjän kutsuminen Business Centraliin](finance-accounting.md#inviteaccountant).

### Järjestelmän käyttöoikeuden poistaminen käyttäjältä

Voit poistaa käyttäjän [!INCLUDE[prod_short](includes/prod_short.md)] online -käyttöoikeuden. Kaikki viittaukset käyttäjään säilyvät. Käyttäjä ei kuitenkaan voi kirjautua sisään ja käyttäjän aktiiviset istunnot pysäytetään.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Avaa soveltuvan käyttäjän **Käyttäjäkortti**-sivu ja valitse sitten **Tila**-kentässä **Ei käytössä**.
3. Voit antaa käyttöoikeuden uudelleen käyttäjälle määrittämällä **Tila**-kentän arvoksi **Käytössä**.

Voit myös poistaa käyttöoikeuden käyttäjältä Microsoft 365 -hallintakeskuksessa. Käyttäjä ei pysty kirjautumaan sisään. Lisätietoja on kohdassa [Käyttöoikeuksien poistaminen käyttäjiltä](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="m365"></a>Synkronointi Microsoft 365:n kanssa

Kun määrität käyttöoikeuden [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa Microsoft 365 -käyttäjälle, käyttäjän voi luoda kahdella eri tavalla [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa.  

- Järjestelmänvalvoja voi lisätä käyttäjän valitsemalla **Päivitä käyttäjät Microsoft 365:stä** -toiminnon **Käyttäjät**-sivulta [Käyttäjän lisääminen tai käyttäjätietojen päivittäminen Business Centralissa](#adduser) -osiossa kuvatulla tavalla.
- Käyttöoikeustiedot päivitetään automaattisesti, kun käyttäjä kirjautuu sisään ensimmäisen kerran.

Molemmissa tapauksissa useita asetuksia otetaan käyttöön automaattisesti. Ne asetukset on luetteloitu seuraavan taulukon toisessa ja kolmannessa sarakkeessa.

Jos muutat käyttäjätietoja Microsoft 365:ssä, voit päivittää [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen vastaamaan muutosta. Käytä jotain **Käyttäjät**-sivun toimintoa päivitettävästä kohdasta riippuen. Toiminnot kuvataan seuraavan taulukon kahdessa viimeisessä sarakkeessa.

|Mitä tapahtuu, kun:|Ensimmäinen käyttäjä, ensimmäinen sisäänkirjautuminen|Päivitä käyttäjät Microsoft 365:stä|Palauttaa käyttäjän oletuskäyttäjäryhmät|
|-|-|-|-|
|Laajuus:|Nykyinen käyttäjä|Useita valittuja käyttäjiä|Yksittäinen valittu käyttäjä (paitsi nykyinen)|
|Luo uusi käyttäjä ja määritä SUPER-käyttöoikeusjoukko.<br /><br /><!--Platform-->|**X**|**X** | | 
|Päivitä käyttäjä Microsoft 365 -tietojen perusteella: tila, koko nimi, yhteyshenkilön sähköpostiosoite, todennuksen sähköpostiosoite.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Synkronoi käyttäjän palvelupaketit (lisenssit) ja käyttöoikeudet sekä määritetyt roolit Microsoft 365:ssä.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Lisää käyttäjä käyttäjäryhmiin nykyisen käyttäjän palvelupakettien mukaan. Poista SUPER-käyttöoikeusjoukko kaikilta muilta käyttäjiltä paitsi ensimmäiseltä sisäänkirjautuvalta käyttäjältä ja [järjestelmänvalvojilta](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Vähintään yksi SUPER-käyttäjä on määritettävä.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Poistaa määritetyt käyttäjäryhmät ja käyttöoikeudet manuaalisesti.|

Käyttäjät voivat käyttää [!INCLUDE[prod_short](includes/prod_short.md)] -tietoja Teamsissa käyttämällä vain Microsoft 365 -käyttöoikeuttaan. Kun käyttöoikeus on otettu käyttöön ympäristössä, **Päivitä käyttäjät Microsoft 365:stä** -toiminnolla suoritettu synkronointi ohittaa käyttäjät, joilla on vain Microsoft 365 -käyttöoikeus. Jos haluat sisällyttää nämä käyttäjät synkronointiin, sinun täyty ensin päivittää ympäristön asetukset ja kohdistaa suojausryhmä, joka sisältää [!INCLUDE[prod_short](includes/prod_short.md)] -käyttöoikeuden omistavat käyttäjät sekä käyttäjät, joilla on vain Microsoft 365 -käyttöoikeus.

Lisätietoja ympäristöjen käytön suojaamisesta suojausryhmillä on kohdassa [Käyttöoikeuksien hallinta Microsoft Entra -ryhmien avulla](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Katso yleiskatsaus [!INCLUDE[prod_short](includes/prod_short.md)]in käyttämisestä Teamsissa Microsoft 365 -käyttöoikeudella kohdasta [admin-access-with-m365-license](admin-access-with-m365-license.md).

## Käyttäjien ja lisenssien hallinta on-premises-käyttöönotoissa

Paikallisten käyttöönottojen käyttöoikeuksien määrä on määritetty käyttöoikeustiedostossa (.bclicense tai .flf). Kun järjestelmänvalvoja tai Microsoft-kumppani lataa käyttöoikeustiedoston, järjestelmänvalvoja voi määrittää, mitkä käyttäjät voivat kirjautua [!INCLUDE[prod_short](includes/prod_short.md)]:een.

Järjestelmänvalvoja luo, muokkaa ja poistaa käyttäjiä paikallisesti käyttöönotoissa suoraan **Käyttäjät**-sivulta.

### Käyttäjän muokkaaminen tai poistaminen paikallisesta käyttöoikeudesta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttäjät** ja valitse sitten vastaava linkki.
2. Valitse muokattava käyttäjä ja valitse sitten **Muokkaa**-toiminto.
3. Muuta tietoja tarvittaessa **Käyttäjän kortti** -sivulla.  
4. Poista käyttäjä valitsemalla ensin poistettava käyttäjä ja sitten **Poista**-toiminto.

> [!NOTE]
> Järjestelmänvalvoja voi määrittää paikallisissa käyttöönotoissa, miten käyttäjän tunnistetiedot todennetaan [!INCLUDE[server](includes/server.md)] -ilmentymässä. Kun luot käyttäjän, anna käyttämäsi tunnistetietotyyppi.
>
> Lisätietoja on [Todennus- ja käyttäjätietotyypit](/dynamics365/business-central/dev-itpro/administration/users-credential-types) -kohdassa [!INCLUDE[prod_short](includes/prod_short.md)]:n hallintaohjeessa.

## Käyttäjän tilan analysointi käyttöoikeustyypin mukaan

**Tietojen analysointi** -toiminnon avulla voit analysoida tietoja [Käyttäjät](https://businesscentral.dynamics.com/?page=9800)-sivulla. Sinun ei tarvitse suorittaa raporttia tai avata toista sovellusta, kuten Exceliä. Ominaisuus tarjoaa vuorovaikutteisen ja monipuolisen tavan laskea, tiivistää ja tarkastella tietoja. Sen sijaan, että raportteja suoritetaan vaihtoehdoilla ja suodattimilla, voit lisätä useita välilehtiä, jotka edustavat erilaisia tehtäviä tai näkymiä tiedoista. Esimerkkejä ovat "Käyttäjät tilan mukaan", "Käyttäjät käyttöoikeuden mukaan", tai mikä tahansa muu näkymä, jonka voit kuvitella. Lisätietoja **Tietojen analysointi** -ominaisuuden käytöstä on kohdassa [analyysitilassa olevien luettelo- ja kyselytietojen analysointi](analysis-mode.md).

### Käyttäjäanalyysiskenaariot

Seuraavissa osissa on esimerkkejä skenaarioista, joissa käyttäjäluettelon analysoiminen voi helpottaa muutosten seurantaa ja käyttäjiesi tilaa.

| Alue | Vastaanottaja... | Avaa tämä sivu analyysitilassa | Näiden kenttien käyttäminen |
| ---- | ----- | ------------------------------- |------------------- |
| [Käyttäjät tilan mukaan](#example-users-by-status) | Käyttäjien luettelon katsominen niiden tilan perusteella (käytössä tai poissa käytöstä). | [Käyttäjät](https://businesscentral.dynamics.com/?page=9800) | **Tila**, **Käyttäjänimi**, **Koko nimi**, **Valtuutussähköposti** ja **Käyttöoikeustyyppi**. |
| [Käyttäjät käyttöoikeustyypin mukaan](#example-users-by-license-type) | Käyttäjien luettelon katsominen niiden käyttöoikeustyypin perusteella. | [Käyttäjät](https://businesscentral.dynamics.com/?page=9800) | **Käyttöoikeustyyppi**, **Tila**, **Käyttäjänimi**, **Koko nimi** ja **Valtuutussähköposti**. |

### Esimerkki: Käyttäjät tilan mukaan

Voit analysoida käyttäjiä tilan mukaan noudattamalla seuraavia vaiheita:

1. Avaa [Käyttäjät](https://businesscentral.dynamics.com/?page=9800) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: -kuvake ja ota analyysitila käyttöön.
1. Poista kaikki sarakkeet **Sarakkeet**-valikosta (valitse **Haku**-kentän vieressä oleva ruutu oikealla).
1. Vedä **Tila** (käyttäjä käytössä/ei käytössä) ja **Käyttöoikeuden tyyppi**- kentät **Riviryhmät**-alueeseen.
1. Valitse kentät **Käyttäjänimi**, **Koko nimi** ja **Valtuutussähköposti**.
1. Nimeä analyysivälilehden nimeksi uudelleen **Käyttäjät tilan mukaan** tai tuotteiksi, jotka kuvaavat analyysiä.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source=" media/data-analysis-users.png" alt-text="Esimerkki tietoanalyysin tekemisestä Muutoslokin tapahtumat -sivulla (Kuka muutti mitä tietoja milloin) -sivulla." lightbox="media/data-analysis-users.png":::

### Esimerkki: Käyttäjät käyttöoikeustyypin mukaan

Voit analysoida käyttäjiä käyttöoikeustyypin mukaan noudattamalla seuraavia vaiheita:

1. Avaa [Käyttäjät](https://businesscentral.dynamics.com/?page=9800) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: -kuvake ja ota analyysitila käyttöön.
1. Poista kaikki sarakkeet **Sarakkeet**-valikosta (valitse **Haku**-kentän vieressä oleva ruutu oikealla).
1. Vedä **Käyttöoikeustyyppi**- ja **Tila**- (käyttäjä käytössä/ei käytössä) -kentät **Riviryhmät**-alueeseen.
1. Valitse **Käyttäjänimi**-, **Koko nimi**- ja **Valtuutussähköposti**-kentät.
1. Nimeä analyysivälilehden nimeksi uudelleen **Käyttäjät käyttöoikeuden mukaan** tai tuotteiksi, jotka kuvaavat analyysiä.

## Katso myös

[Käyttöoikeuksien delegoiminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
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