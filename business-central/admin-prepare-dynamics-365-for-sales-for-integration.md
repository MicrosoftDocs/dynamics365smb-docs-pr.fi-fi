---
title: Dynamics 365 Sales -integrointi
description: Tietoja Dynamics 365 Business Centralin valmistelusta Dynamics 365 Sales -integrointia varten.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 12/15/2023
ms.author: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="integrating-with-dynamics-365-sales"></a>Dynamics 365 Sales -integrointi

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Myyjää pidetään usein liiketoiminnan eniten ulospäin suuntautuneena tehtävänä. Myyjien voisi kuitenkin olla hyödyllistä tarkastella liiketoimintaa myös sisäisesti, jotta he tiedostaisivat, mitä taustalla tapahtuu. Myyjät saavat merkityksellisiä tietoja, kun [!INCLUDE[prod_short](includes/prod_short.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] integroidaan. Integroinnin avulla käyttäjät näkevät, mitä tietoja [!INCLUDE[prod_short](includes/prod_short.md)] sisältää, kun käytössä on [!INCLUDE[crm_md](includes/crm_md.md)]. Myyntitarjousta valmistellessa voi esimerkiksi olla hyödyllistä tietää, riittääkö varasto tilauksen täyttämiseen. Lisätietoja on kohdassa [Dynamics 365 Salesin käyttäminen Business Centralissa](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Tässä ohjeaiheessa kerrotaan [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen online-versioiden integroinnista [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun avulla. Lisätietoja paikallisesta määrityksestä on kohdassa [Paikallisen Dynamics 365 Salesin integroinnin valmistelu](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrate-through-dataverse"></a>Integrointi Dataversen avulla

[!INCLUDE[prod_short](includes/prod_short.md)] voidaan integroida myös [!INCLUDE[prod_short](includes/cds_long_md.md)] -ratkaisun kanssa, joten tietojen yhdistäminen ja synkronoiminen Dynamics 365 -sovellusten kanssa on helppoa. Voit esimerkiksi muodostaa yhteyden sovellukseen [!INCLUDE[crm_md](includes/crm_md.md)] tai jopa itse luotuihin sovelluksiin. Jos integrointi tehdään ensimmäistä kertaa, käytössä on oltava [!INCLUDE[prod_short](includes/cds_long_md.md)]. Lisätietoja on kohdassa [Integroiminen Dataverse -palvelun kanssa](admin-common-data-service.md).

Jos [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[prod_short](includes/prod_short.md)] on jo integroitu, voit jatkaa tietojen synkronointia asetuksen avulla. Jos kuitenkin päivität [!INCLUDE[crm_md](includes/crm_md.md)] -integroinnin tai otat sen pois käytöstä, voit ottaa sen käyttöön uudelleen [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun avulla. Lisätietoja on kohdassa [Integroinnin päivittäminen Dynamics 365 Salesin avulla](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Jos uudelleenyhdistämisessä käytetään [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelua, käyttöön otetaan synkronoinnin oletusasetukset ja käytössä olevat määritykset korvataan. Esimerkiksi taulukon oletusyhdistämismääritykset otetaan käyttöön.

## <a name="integration-settings-that-are-specific-to-a--integration"></a>Sovelluksen [!INCLUDE[crm_md](includes/crm_md.md)] integrointia varten tarkoitetut integrointiasetukset

Integrointi sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] kanssa tapahtuu käyttämällä palvelua [!INCLUDE[prod_short](includes/cds_long_md.md)]. Useat vakioasetukset ja -taulukot määritetään. Vakioasetusten lisäksi [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksella on sovelluskohtaisia asetuksia. Seuraavissa osissa esitellään nämä asetukset.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Salesin käyttäjätilien käyttöoikeudet ja käyttöoikeusroolit

Kun integrointiratkaisua asennetaan, integroinnin käyttäjätilin käyttöoikeudet määritetään. Jos näitä käyttöoikeuksia on muutettu, käyttöoikeudet on ehkä palautettava alkuperäisiksi. Voit tehdä tämän asentamalla integrointiratkaisun uudelleen **Ota integraatioratkaisu uudelleen käyttöön** -kohdan avulla **Dynamics 365 -yhteyden asetukset** -sivulla. Seuraavat käyttöoikeus roolit on otettu käyttöön:

* Dynamics 365 Business Central -sovelluksen integroinnin järjestelmänvalvoja
* Dynamics 365 Business Central -sovelluksen integroinnin käyttäjä
* Dynamics 365 Business Central -sovelluksen tuotteen saatavuuden käyttäjä

> [!NOTE]
> Voidaksesi käyttää **Avaa Business Centralissa** -toimintoa Salesissa, sinulla on oltava seuraavat oikeudet seuraaville taulukoille:
>
> * Sinulla täytyy olla Luku-oikeudet Dynamics 365 Business Central -yhteystaulukkoon (nav_connection).
> * Sinulla tulee olla luku-, kirjoitus- ja poisto-oikeudet Dynamics 365 Business Centralin oletusyhteystaulukkoon (nav_defaultconnection).

### <a name="connection-settings-in-the-setup-guide"></a>Yhteysasetukset asennusoppaassa

Asetusten ohjattu määritysopas auttaa määrittämään yhteyden nopeasti ja määrittämään lisäominaisuudet, kuten tietueiden välisen yhdistämisen.

1. Valitse ensin **Asennus ja laajennukset** ja valitse sitten **Asetusten ohjattu määritys**.
2. Käynnistä asetusten ohjattu määritysopas valitsemalla **Dynamics 365 Sales -yhteyden määritys**.
3. Täytä tarvittavat kentät.
4. Vaihtoehtoisesti on lisäasetuksia, jotka voivat parantaa tietoturvaa ja mahdollistaa lisäominaisuuksien käyttämisen. Lisäasetuksia käsitellään seuraavassa taulukossa.  

| Kenttä | Kuvaus |
|--|--|
| **Tuo Dynamics 365 Sales -ratkaisu** | Asenna ja määritä integrointiratkaisu [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
|**Synkronoi nimikkeen saatavuus automaattisesti**|Määrittää, että nimikkeen saatavuuden työjono on ajoitettava. Työjono suoritetaan 30 minuutin välein, ja se päivittää yhdistettyjen nimikkeiden saatavuuden.|
| **Ota käyttöön vanha myyntitilauksen integrointi** | Kun myyntitilauksia luodaan [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa ja tilauksia täytetään [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa, tämä asetus integroi prosessin [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa. Lisätietoja on kohdassa [Myyntitilauksen käsittelyn integroinnin käyttöönotto](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).<br><br>**Huomautus:** Et voi käyttää tätä vaihtoehtoa, jos käytössä on **Myyntitilausten kaksisuuntainen synkronointi** -vaihtoehto. Nämä kaksi asetusta ovat toisensa poissulkevia. Lisätietoja tästä vaihtoehdosta on kohdassa [Myyntitilausten yksi- ja kaksisuuntainen synkronointi](#single-and-bi-directional-synchronization-of-sales-orders). |
|**Ota käyttöön Dynamics 365 Sales -yhteys** | Ota [!INCLUDE[crm_md](includes/crm_md.md)] -yhteys käyttöön. |
| **Dynamics 365 SDK -versio** | Tällä on merkitystä vain, jos integrointi tehdään [!INCLUDE[crm_md](includes/crm_md.md)]in paikalliseen versioon. [!INCLUDE[prod_short](includes/prod_short.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] voidaan yhdistää tällä Dynamics 365 SDK -versiolla (joka tunnetaan myös nimellä Xrm). Version on oltava yhteensopiva sen SDK-version kanssa, jota [!INCLUDE[crm_md](includes/crm_md.md)] käyttää. Lisäksi sen on oltava sama tai uudempi kuin versio, jota [!INCLUDE[crm_md](includes/crm_md.md)] käyttää. |
|**Myyntitilausten kaksisuuntainen synkronointi**|Synkronoi myyntitilaukset molempiin suuntiin. Lisätietoja tästä vaihtoehdosta on kohdassa [Myyntitilausten yksi- ja kaksisuuntainen synkronointi](#single-and-bi-directional-synchronization-of-sales-orders).<br><br>**Huomautus:** Et voi käyttää tätä vaihtoehtoa, jos käytössä on **Ota käyttöön vanha myyntitilauksen integrointi** -vaihtoehto. Nämä kaksi asetusta ovat toisensa poissulkevia.|

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Microsoft Dynamics 365 -yhteyden määrityssivun yhteysasetukset

Anna seuraavat tiedot yhteyden muodostamiseen [!INCLUDE[crm_md](includes/crm_md.md)]ista [!INCLUDE[prod_short](includes/prod_short.md)]iin.

| Kenttä | Kuvaus |
|--|--|
|**Dynamics 365 Sales -ohjelman URL-osoite**|[!INCLUDE[crm_md](includes/crm_md.md)] -ilmentymän URL-osoite. Tämän asetuksen avulla käyttäjät voivat avata sovelluksessa [!INCLUDE[prod_short](includes/prod_short.md)] tietueita, jotka vastaavat sovelluksen [!INCLUDE[crm_md](includes/crm_md.md)] tietueita. Tietue voi olla esimerkiksi tili tai tuote. [!INCLUDE[prod_short](includes/prod_short.md)]in tietueet avautuvat [!INCLUDE[prod_short](includes/prod_short.md)]issa.|
|**Synkronoi nimikkeen saatavuus automaattisesti**|Määrittää, että nimikkeen saatavuuden työjono on ajoitettava. Työjono suoritetaan 30 minuutin välein, ja se päivittää yhdistettyjen nimikkeiden saatavuuden.|
|**Dynamics 365 SDK -versio**|Jos integroit sovelluksen [!INCLUDE[crm_md](includes/crm_md.md)] paikallisen version, muodosta yhteys sovellusten [!INCLUDE[prod_short](includes/prod_short.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] välillä tämän Dynamics 365 SDK -version avulla (joka tunnetaan myös nimellä Xrm). Valitsemasi version on oltava yhteensopiva [!INCLUDE[crm_md](includes/crm_md.md)]in käyttämän SDK-version kanssa. Tämä versio on sama tai uudempi kuin [!INCLUDE[crm_md](includes/crm_md.md)]in käyttämä versio.|

Syötä yllä olevien asetusten lisäksi seuraavat asetukset [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukselle.

| Kenttä | Kuvaus |
|--|--|
| **Myyntitilauksen integrointi on käytössä** | Antaa käyttäjille mahdollisuuden lähettää myyntitilauksia ja aktivoituja tarjouksia [!INCLUDE[crm_md](includes/crm_md.md)]issa sekä tarkastella ja käsitellä niitä sitten [!INCLUDE[prod_short](includes/prod_short.md)]issa. Tämä asetus integroi prosessin sovelluksessa [!INCLUDE[crm_md](includes/crm_md.md)]. Lisätietoja on kohdassa [Myyntitilauksen käsittelyn integroinnin käyttöönotto](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Myyntitilausten automaattinen luominen** | Luo myyntitilaus [!INCLUDE[prod_short](includes/prod_short.md)]issa, kun käyttäjä luo ja lähettää sellaisen [!INCLUDE[crm_md](includes/crm_md.md)]issa. |
| **Käsittele myyntitarjoukset automaattisesti** | Käsittele myyntitarjous [!INCLUDE[prod_short](includes/prod_short.md)]issa, kun käyttäjä luo ja aktivoi sellaisen [!INCLUDE[crm_md](includes/crm_md.md)]issa. Lisätietoja on kohdassa [Myyntitarjoustietojen käsittely](/dynamics365/business-central/marketing-integrate-dynamicscrm?tabs=new-experience#handling-sales-quotes-data). |
|**Myyntitilausten kaksisuuntainen synkronointi**|Synkronoi myyntitilaukset molempiin suuntiin. Lisätietoja tästä vaihtoehdosta on kohdassa [Myyntitilausten yksi- ja kaksisuuntainen synkronointi](#single-and-bi-directional-synchronization-of-sales-orders).|
<!--
### <a name="user-account-settings"></a>User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->
### <a name="single-and-bi-directional-synchronization-of-sales-orders"></a>Myyntitilausten yksi- ja kaksisuuntainen synkronointi

Kun integrointi määritetään asetusoppaassa tai Microsoft Dynamics 365 -yhteysasetukset -sivulla, käytettävissä on vaihtoehtoja, jotka ohjaavat myyntitilausten synkronoinnin suuntaa sekä sitä, miten ne lähetetään.

**Myyntitilausten kaksisuuntainen synkronointi** -vaihtoehdon avulla voit synkronoida myyntitilaukset Salesista [!INCLUDE [prod_short](includes/prod_short.md)] -sovellukseen ja päin vastoin. Jos asiakas esimerkiksi muuttaa mieltään tuotteesta tai määrästä, jonka tilaamisessa on ollut käytössä [!INCLUDE[crm_md](includes/crm_md.md)], voit arkistoida myyntiasiakirjan ja luoda uuden sovelluksessa [!INCLUDE[prod_short](includes/prod_short.md)]. Sama pätee muutoksiin [!INCLUDE[prod_short](includes/prod_short.md)]issa. Esimerkiksi silloin, kun hinnat, verosummat tai oletetut toimituspäivämäärät muuttuvat, muutokset synkronoidaan [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukseen. Kaksisuuntainen synkronointi auttaa pitämään myyjät ajan tasalla uusimmista muutoksista ja myyntitilausten tilasta.

Kaksisuuntaisessa synkronoinnissa myyntitilaukset ovat käytettävissä synkronointia varten, kun niiden tilaksi Salesissa on muutettu **Lähetetty**. Kun tämä tila määritetään, tilauksen rivien tietoja ei enää voi muuttaa. Kun synkronoit tilauksen, tilaus siirretään [!INCLUDE [prod_short](includes/prod_short.md)] -sovellukseen tilassa **Vapautettu**. Virheen sattuessa tilauksen tilaksi voidaan palauttaa **Avoin** ([!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksessa) tai **Aktiivinen** (Salesissa). Tämän jälkeen rivejä voi lisätä tai poistaa virheen korjaamiseksi, ja tilaus lähetetään uudelleen.

> [!TIP]
> Kun **Myyntitilausten kaksisuuntainen synkronointi** -vaihtoehto otetaan käyttöön, [!INCLUDE [prod_short](includes/prod_short.md)] luo tietueen **Myyntitilausarkistot** -sivulla tilauksen tietojen kirjaamisen tai muuttamisen yhteydessä. Arkistoituja versioita voidaan käyttää esimerkiksi tilauksen historian tutkimisessa.

**Ota käyttöön vanha myyntitilauksen integrointi** -vaihtoehto synkronoi vain Salesista [!INCLUDE [prod_short](includes/prod_short.md)]iin. Tässä vaihtoehdossa voit käyttää **Lähetä**-toimintoa Salesissa, kun tilaukset määritetään käytettäviksi synkronointia varten. Kun näin tehdään, tilauksen tietoja ei enää voi muuttaa. Kun synkronoit tilauksen, tilaus siirretään [!INCLUDE [prod_short](includes/prod_short.md)] -sovellukseen tilassa **Vapautettu**.

Jos haluat käyttää tätä vaihtoehtoa, anna [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen järjestelmänvalvojan käyttäjätilin tunnistetiedot. Lisätietoja on kohdassa [Myyntitilauksen tietojen käsitteleminen](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!NOTE]
> **Myyntitilausten kaksisuuntainen synkronointi**- ja **Ota käyttöön vanha myyntitilauksen integrointi** -vaihtoehdot ovat toistensa poissulkevia. Molempia vaihtoehtoja ei voi käyttää samanaikaisesti.

Molemmissa vaihtoehdoissa [!INCLUDE [prod_short](includes/prod_short.md)] näyttää kaikki myyntitilaukset **Lähetetty**-tilassa **Tilaukset – Microsoft Dynamics 365 Sales** -sivulla.

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Synkronoinnin Myynti-entiteetin yhdistämismääritys

[!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen entiteetit, kuten tilaukset, yhdistetään [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa samantyyppisiin taulukoihin, kuten myyntitilauksiin. [!INCLUDE[crm_md](includes/crm_md.md)]in tietoja käytetään määrittämällä linkkejä [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in taulukoiden välille. Tätä sanotaan yhdistämiseksi.

Seuraavassa taulukossa on luettelo [!INCLUDE[prod_short](includes/prod_short.md)]in tarjoamista tavallisista yhdistämismäärityksistä [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]:n taulukoiden välillä.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synkronoinnin suunta | Oletussuodatin |
|--|--|--|--|
| Mittayksikkö | Yksikköryhmä | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Nimike | Tuote | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-sovelluksen kontaktin suodatin: **Tuotteen tyyppi** on **Myyntivarasto** |
| Resurssi | Tuote | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-sovelluksen kontaktin suodatin: **Tuotteen tyyppi** on **Palvelut** |
| Nimikkeen mittayksikkö | CRM-mittayksikkö |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
| Resurssin mittayksikkö | CRM-mittayksikkö |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]||
| Yksikköryhmä | CRM Uomschedule | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ||
| Asiakkaan hintaryhmä | Hinnasto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Myyntihinta | Tuotehinnasto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | Sovelluksen [!INCLUDE[prod_short](includes/prod_short.md)] kontaktisuodatin: **Myyntikoodi** ei ole tyhjä, **Myyntityyppi** on **Asiakkaan hintaluokka** |
| Mahdollisuus | Mahdollisuus | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Myyntilaskun otsikko | Lasku | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Myyntilaskurivi | Laskutustuote | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Myyntitilauksen otsikko | Myyntitilaus | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] <br><br> Voit synkronoida molempiin suuntiin ottamalla **Myyntitilausten kaksisuuntaisen synkronoinnin** -vaihtopainikkeen käyttöön **Dynamics 365 -yhteyden asetus** -sivulla.| [!INCLUDE[prod_short](includes/prod_short.md)] Myynnin Ylätunnuksen suodatin: **Dokumenttityyppi** on Järjestys, **Tila** on Vapautettu. |
| Myyntitilauksen huomautukset | Myyntitilauksen huomautukset | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

> [!NOTE]
> Nimikkeen mittayksikköjen, resurssin mittayksikköjen ja yksikköryhmätaulukoiden yhdistämismääritykset ovat käytettävissä vain, jos järjestelmänvalvojasi on ottanut käyttöön **Yksikköryhmän yhdistämismääritys** -valinnan **Microsoft Dynamics 365 -yhteysasetukset** -sivulla. Lue lisää kohdasta [Nimikkeiden ja resurssien synkronointi eri mittayksiköitä käyttävien tuotteiden kanssa](admin-prepare-dynamics-365-for-sales-for-integration.md#synchronize-items-and-resources-with-products-with-different-units-of-measure).

## <a name="synchronize-items-and-resources-with-products-with-different-units-of-measure"></a>Nimikkeiden ja resurssien synkronointi eri mittayksiköitä käyttävien tuotteiden kanssa

Yritykset usein tuottavat tai ostavat tiettyä mittayksikköä käyttäviä nimikkeitä ja myyvät niitä sitten käyttämällä toista mittayksikköä. Jos haluat synkronoida useita mittayksiköitä käyttävät kohteet, sinun on otettava käyttöön **Yksikköryhmän yhdistämismääritys** -kytkin **Microsoft Dynamics 365 -yhteyden määritys** -sivulla. 

Kun otat käyttöön ominaisuuden päivityksen, luodaan uusi Yksikköryhmä-taulukko ja se määritetään kullekin nimikkeelle ja resurssille [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa. Taulukoiden avulla voit yhdistää Yksikköryhmä-, Nimikkeen mittayksikkö- ja Resurssin mittayksikkö -taulukot voidaan [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen Dynamics 365 Salesin yksikköryhmään. Seuraavassa kuvassa näkyvät yhdistämismääritykset.

:::image type="content" source="media/unit group 1.png" alt-text="Yksikköryhmien taulukoiden yhdistämismääritykset":::

Kullekin yksikköryhmälle voidaan luoda useita mittayksiköitä, ja nämä ryhmät voidaan määrittää tuotteisiin [!INCLUDE[crm_md](includes/crm_md.md)]issa. Tämän jälkeen tuotteet voidaan synkronoida nimikkeiden ja resurssien kanssa [!INCLUDE[prod_short](includes/prod_short.md)]issa. Nimikkeen mittayksiköt ja resurssiin mittayksiköt voidaan yhdistää manuaalisesti yksikköryhmään. Jos nimikkeen tai resurssin yksikköryhmää ei näin toimittaessa ole yhdistetty [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen yksikköryhmään esimerkiksi siksi, että yksikköryhmää ei ole, [!INCLUDE[prod_short](includes/prod_short.md)] luo yksikköryhmän automaattisesti [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa.

### <a name="map-items-and-resources-to-products"></a>Nimikkeiden ja resurssien yhdistäminen tuotteisiin

Kun otat **Yksikköryhmän yhdistämismääritys** -kytkimen käyttöön **Microsoft Dynamics 365 -yhteyden asetukset** -sivulla, tapahtuu seuraavaa:

* Nimikkeille ja resursseille luodaan uudet yhdistämismääritykset.
* Aiemmin luodut yhdistämismääritykset poistetaan. <!--which mappings?-->
* Tietojen päivitys luo yksikköryhmät nimikkeille ja resursseille.

Näiden uusien yhdistämismääritysten käyttämäinen edellyttää, että yksikköryhmät, nimikkeen mittayksikkö ja resurssin mittayksikkö synkronoidaan. Lisäksi nimikkeet ja resurssit on synkronoitava uudelleen. 

> [!NOTE]
> [!INCLUDE[crm_md](includes/crm_md.md)] ei salli tuotteen yksikköryhmän muuttamista. Niinpä tuotteet on poistettava käytöstä sekä nimikkeiden ja resurssien yhdistäminen purettava, jonka jälkeen synkronointi tehdään luomalla uudet tuotteet [!INCLUDE[crm_md](includes/crm_md.md)]issa. 

Yksikköryhmien yhdistäminen aloitetaan seuraavasti:

1. Varmista, että [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen tuotteita ei ole yhdistetty [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen nimikkeisiin tai resursseihin. Jos ne on yhdistetty, siirry **Nimikkeet** ja/tai **Resurssit**-sivulle ja valitse yhdistetyt tietueet suodatinvaihtoehtojen avulla. Valitse sitten **Dynamics 365 Sales** -toiminto ja valitse sitten **Poista pari**. Tämä toiminto aikatauluttaa taustatyön poistamaan tietueiden yhdistämisen. Suoritettavan työn tila voidaan tarkistaa käyttämällä **Synkronointiloki**-toimintoa. Lisätietoja on kohdassa [Yhdistäminen ja synkronointi](admin-how-to-couple-and-synchronize-records-manually.md). 
2. Koska uudet tuotteet luodaan [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa siten, että niissä on uudet yksikköryhmät, nimien kaksoiskappaleet voidaan estää jollakin seuraavista vaiheista:
    
  * Anna tuotteille uusi nimi ja poista ne sitten käytöstä [!INCLUDE[crm_md](includes/crm_md.md)]issa. Lisätietoja on kohdassa [Tuotteiden poistaminen käytöstä (myyntikeskus)](/dynamics365/sales-enterprise/retire-product). Tuotteita voi joukkomuokata Microsoft Excelissa kirjautumalla Power Appsiin, valitsemalla ympäristön, siirtymällä **Tuotteet**-taulukkoon ja sitten valitsemalla **Tiedot**-taulukon. Poista kaikki käytetyt suodattimet. Valitse **Tiedot**-ryhmässä **Muokkaa tietoja Excelissä** -toiminto. Lisää yhdistettyihin tuotteisiin etu- tai jälkiliite ja poista ne käytöstä.
    * Poista tuotteet käytöstä ja poista ne. 

3. Synkronoi **Yksikköryhmät**, **Mittayksiköt**, **Nimikkeet** ja **Resurssit** seuraavasti:
    1. Avaa [!INCLUDE[prod_short](includes/prod_short.md)]issa **Dynamics 365 Sales -yhteysasetukset** -sivu.
    2. Avaa **Dataversen täyden synkronoinnin tarkistus** -sivu **Suorita täysi synkronointi** -toiminnolla.
    3. Valitse **NIMIKKEEN MITTAYKSIKKÖ**-, **RESURSSIN MITTAYKSIKKÖ**- JA **YKSIKKÖRYHMÄ**-yhdistämismäärityksiin **Suosittele täyttä synkronointia** -toiminto.
    4. Valitse **Synkronoi kaikki** -toiminto.

    > [!NOTE]
    > Toiminto tee täyden synkronoinnin kaikille yhdistämismäärityksille, joissa ei ole vielä täysin synkronoitu. Kyseisten yhdistämismääritysten synkronointi voidaan estää poistamalla yhdistämismääritykset sivulta. Ne poistetaan tässä tapauksessa vain nykyisestä täydestä synkronoinnista; yhdistämismäärityksiä ei siis poisteta kokonaan.
    
5. Valitse ensin **NIMIKE-TUOTE**-yhdistämismääritys ja sitten **Käynnistä uudelleen** -toiminto. Uudelleenkäynnistäminen luo uusia tuotteita nimikkeistä [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa ja määrittää nimikekohtaisen uuden yksikköryhmän.
6. Valitse ensin **RESURSSI-TUOTE**-yhdistämismääritys ja sitten **Käynnistä uudelleen** -toiminto. Uudelleenkäynnistäminen luo uusia tuotteita resursseista [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa ja määrittää resurssikohtaisen uuden yksikköryhmän.

### <a name="synchronization-rules"></a>Synkronointisäännöt

Seuraavassa taulukossa ovat säännöt, jotka ohjaavat [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen välistä synkronointia. Nämä säännöt ovat myös Dataversessa määritettyjä sääntöjä, jotka otetaan käyttöön. Lisätietoja on kohdassa [Vakioentiteetin yhdistämismääritys](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Integroinnin käyttäjätilin tekemiä muutoksia ei synkronoida. Tämän vuoksi on suositeltavaa, että tietoja ei muuteta kyseistä tiliä käytettäessä. Lisätietoja on kohdassa [Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).

|Sivupöytä|Sääntö|
|-----|----|
|Mittayksiköt|Mittayksiköt synkronoidaan yksikköryhmien kanssa [!INCLUDE[crm_md](includes/crm_md.md)]issa. Yksikköryhmälle voi määrittää vain yhden mittayksikön.|
|Nimikkeet|Kun nimikkeitä synkronisoidaan [!INCLUDE[crm_md](includes/crm_md.md)] tuotteiden kanssa [!INCLUDE[prod_short](includes/prod_short.md)] luo automaattisesti hintalistan [!INCLUDE[crm_md](includes/crm_md.md)]ssä. Voit välttää synkronointivirheet, jos et muokkaa tätä hinnastoa manuaalisesti.|
|Resurssit|Resurssit synkronoidaan niiden [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteiden kanssa, joiden tyyppi on Palvelu.|
|Asiakashintaryhmät|Asiakkaan hintaryhmät synkronoidaan myyntihinnastojen kanssa.|
|Myyntihinnat|Myyntihintojen myyntityyppi on Asiakkaan hintaryhmä. Niiden määritetty myyntikoodi synkronoidaan [!INCLUDE[crm_md](includes/crm_md.md)]in hinnaston rivien kanssa.|
|Mahdollisuudet|Mahdollisuudet synkronoidaan [!INCLUDE[crm_md](includes/crm_md.md)]in mahdollisuuksien kanssa. Myyjän koodin arvo määrittää yhdistetyn taulukon omistajan [!INCLUDE[crm_md](includes/crm_md.md)]issa.|
|Kirjatut myyntilaskut|Kirjatut myyntilaskut synkronoidaan myyntilaskujen kanssa. Ennen laskun synkronointia kannattaa synkronoida kaikki muut taulukot, jotka voivat vaikuttaa laskuun. Niitä voivat olla esimerkiksi myyjien taulukot ja hinnastot. Laskun otsikossa oleva myyjän koodin arvo määrittää yhdistetyn taulukon omistajan Sales-sovelluksessa.|
|Myyntitilaukset|Kun myyntitilausten integrointi on käytössä, [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen myyntitilaukset, jotka on luotu [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen lähetetyistä myyntitilauksista, synkronoidaan [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen myyntitilausten kanssa niiden vapauttamisen yhteydessä. Ennen tilausten synkronoimista on suositeltavaa synkronoida kaikki tilaukseen liittyvät taulukot, esimerkiksi myyjät ja hinnastot. Tilauksen otsikossa oleva Myyjän koodi -kenttä määrittää yhdistetyn taulukon omistajan [!INCLUDE[crm_md](includes/crm_md.md)]:ssä.|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Myynnin integroinnin synkronointityöt

Työt suoritetaan seuraavassa järjestyksessä, jotta taulukoiden välille ei muodostu yhdistämisen riippuvuussuhteita. Dataversessa on lisää projekteja. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](./admin-job-queues-schedule-tasks.md).

1. MITTAYKSIKKÖ – Dynamics 365 Salesin synkronointityö  
2. RESURSSI-TUOTE – Dynamics 365 Salesin synkronointityö  
3. NIMIKE-TUOTE – Dynamics 365 Salesin synkronointityö  
4. ASIAKHNTRHM-HINTA - Dynamics 365 Salesin synkronointityö.
5. MYYNTIHNT-TUOTEHINTA - Dynamics 365 Salesin synkronointityö.
6. KIRJMNTILASKU-LASK – Dynamics 365 Salesin synkronointityö.

### <a name="default-synchronization-job-queue-entries"></a>Oletusarvoiset synkronoinnin työjonotapahtumat

Seuraavassa taulukossa kuvaillaan [!INCLUDE[crm_md](includes/crm_md.md)]:n synkronoinnin oletustyöt.  

|Työjonotapahtuma|Kuvaus|Suunta|Integrointitaulukon yhdistämismääritys|Synkronoinnin oletustiheys (min)|Passivisuuden oletusaika (min)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|MITTAYKSIKKÖ – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in yksikköryhmät ja [!INCLUDE[prod_short](includes/prod_short.md)]in mittayksiköt.|[!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|MITTAYKSIKKÖ|30|720<br> (12 tuntia)|
|RESURSSI-TUOTE – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteet ja [!INCLUDE[prod_short](includes/prod_short.md)]in resurssit.|[!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|RESURSSI-TUOTE|30|720<br> (12 tuntia)|
|NIMIKE-TUOTE – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteet ja [!INCLUDE[prod_short](includes/prod_short.md)]in nimikkeet.|[!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|NIMIKE-TUOTE|30|1440<br> (24 tuntia)|
|ASIAKHNTRHM-HINTA – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in myyntihinnaston ja [!INCLUDE[prod_short](includes/prod_short.md)]in asiakashintaryhmät.| |ASIAKASHINTARYHMÄT-MYYNTIHINNASTOT|30|1440<br> (24 tuntia)|
|MYYNTIHNT-TUOTEHINTA – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotehinnat ja [!INCLUDE[prod_short](includes/prod_short.md)]in myyntihinnat.||TUOTEHINTA-MYYNTIHINTA|30|1440<br> (24 tuntia)|
|KIRJMNTILASKU-LASK – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in laskut ja [!INCLUDE[prod_short](includes/prod_short.md)]in kirjatut myyntilaskut.|[!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|LASKUT-KIRJATUT MYYNTILASKUT|30|1440<br> (24 tuntia)|
|Asiakastilastot – Dynamics 365 Salesin synkronointityö|Päivittää [!INCLUDE[crm_md](includes/crm_md.md)]in tilit uusilla [!INCLUDE[prod_short](includes/prod_short.md)]in asiakastiedoilla. Nämä tiedot näkyvät [!INCLUDE[crm_md](includes/crm_md.md)]issa niiden tilien **Business Central -tilin tilastot** -pikanäkymälomakkeessa, jotka on yhdistetty [!INCLUDE[prod_short](includes/prod_short.md)]in asiakkaisiin.<br /><br /> Nämä tiedot voidaan päivittää myös manuaalisesti kustakin asiakastietueesta. Lisätietoja on kohdassa [Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Huomautus:** Tällä työjonotapahtumalla on merkitystä vain, jos [!INCLUDE[prod_short](includes/prod_short.md)] -integrointiratkaisu on asennettu [!INCLUDE[crm_md](includes/crm_md.md)]iin. |Ei sovellu|Ei sovellu|30|Ei sovellu| 

## <a name="connect-to-on-premises-versions-of-business-central-2019-release-wave-1-and-microsoft-dynamics-nav-2018"></a>Yhteyden muodostaminen Business Central 2019:n 1. julkaisuaallon ja Microsoft Dynamics NAV 2018:n paikallisiin versioihin

Microsoft Power Platform -tiimi on [ilmoittanut](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse), että Office 365 -todennustyyppi vanhentuu. Jos käytössä on [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen paikallinen versio, joka on vanhempi kuin Business Central 2019:n julkaisuaalto 1, sinun on muodostettava yhteys [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukseen online-tilassa OAuth-todennustyypin avulla. Tässä osassa kerrotaan, miten seuraavat tuoteversiot yhdistetään:

* Business Central 2019:n julkaisuaalto 1
* Microsoft Dynamics NAV 2018

### <a name="prerequisites"></a>Vaatimukset

* Sinulla täytyy olla Microsoft Azure -tilaus. Kokeilutili toimii sovelluksen rekisteröinnissä.
* [!INCLUDE[crm_md](includes/crm_md.md)] on määritetty käyttämään jotakin seuraavista todennustyypeistä:

   * Office365 (vanha)

     > [!IMPORTANT]
     > Huhtikuusta 2022 alkaen Office365 (vanha) -versiota ei enää tueta. Lisätietoja on kohdassa [Power Appsiin, Power Automateen ja asiakasvuorovaikutussovelluksiin tulevia tärkeitä muutoksia (vanhentumisia)](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   * OAuth

### <a name="connect-business-central-2019-release-wave-1-and-dynamics-nav-2018"></a>Business Central 2019:n julkaisuaallon 1 ja Dynamics NAV 2018:n yhdistäminen

1. Tuo Microsoft Dynamics 365 Business Central -integrointiratkaisu [!INCLUDE[crm_md](includes/crm_md.md)] -ympäristöösi. Integrointiratkaisu on käytettävissä CrmCustomization-kansiossa [!INCLUDE[prod_short](includes/prod_short.md)]- tai Dynamics NAV -DVD-asennuslevyllä. Tuo tuoteversiostasi riippuen jokin seuraavista ratkaisuista:

   * [!INCLUDE[prod_short](includes/prod_short.md)]: kansio, joka sisältää DynamicsNAVIntegrationSolution_v9 and DynamicsNAVIntegrationSolution_v91. -ratkaisut. Tuotava ratkaisu riippuu siitä, mihin [!INCLUDE[crm_md](includes/crm_md.md)] -versioon olet muodostamassa yhteyttä. [!INCLUDE[crm_md](includes/crm_md.md)] online edellyttää DynamicsNAVIntegrationSolution_v91-integrointiratkaisun.
   * Dynamics NAV 2018: asenna DynamicsNAVIntegrationSolution-ratkaisu.

2. Luo [!INCLUDE[crm_md](includes/crm_md.md)] -ympäristöösi ei-vuorovaikutteinen integrointikäyttäjä ja määritä käyttäjälle seuraavat käyttöoikeusroolit. Lisätietoja on kohdassa [Ei-vuorovaikutteisen käyttäjätilin luominen](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central -sovelluksen integroinnin järjestelmänvalvoja
   * Dynamics 365 Business Central -sovelluksen integroinnin käyttäjä

   > [!Important]
   > Käyttäjällä ei saa olla järjestelmänvalvojan käyttöoikeusroolia. Et voi myöskään käyttää järjestelmänvalvojan tiliä integrointikäyttäjänä.

3. Azure-portaali: luo sovellusrekisteröinti [!INCLUDE[prod_short](includes/prod_short.md)]ille. Lisätietoja on kohdassa [Sovelluksen rekisteröiminen Microsoft Entra ID:ssä](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > Suosittelemme, että rekisteröit sovelluksen samaan vuokraajaan Dataverse-ympäristösi kanssa, jotta sinun ei tarvitse antaa sovellukselle suostumusta käyttää ympäristöä. Jos rekisteröit sovelluksen toisessa ympäristössä, sinun on kirjauduttava sisään Dataverse-ympäristösi Microsoft Entra ID -järjestelmänvalvojan tilille ja annettava suostumus.
   >
   > Lisäksi rekisteröimälläsi sovelluksella ei saa olla salaisuutta. Sovelluksen yhdistäminen salaisuuden kanssa Dataverseen on käytettävissä vain Business Central 2020:n julkaisuaallossa 1 ja sitä uudemmissa.
  
4. Tee tuoteversiostasi riippuen jokin seuraavista vaiheista:

    * Etsi [!INCLUDE[prod_short](includes/prod_short.md)]issa **Microsoft Dynamics 365 -yhteysasetukset** ja valitse sitten liittyvä linkki. 
    * Etsi Dynamics NAV 2018:ssa **Microsoft Dynamics 365 for Sales -yhteysasetukset** ja valitse sitten liittyvä linkki.

5. Valitse **Todennustyyppi**-kentässä OAuth-vaihtoehto. 
6. Valitse CRM SDK -versio, joka vastaa vaiheessa 1 tuotua ratkaisuversiota.

   > [!NOTE]
   > Tämä vaihe on merkityksellinen vain [!INCLUDE[prod_short](includes/prod_short.md)]ille

7. Syötä [!INCLUDE[crm_md](includes/crm_md.md)] -ympäristösi URL-osoite ja syötä sitten integrointikäyttäjän käyttäjänimi ja salasana. 

   * Käytä [!INCLUDE[prod_short](includes/prod_short.md)]issa **Palvelimen osoite** -kenttää.
   * Käytä Dynamics NAV 2018:ssa **Dynamics 365 Sales URL** -kenttää.

8. Kirjoita **Yhteysmerkkijono**-kenttään sovellusrekisteröinnin tunnus. Tässä kentässä on kaksi tunnusmerkkijonoa, joissa on määritettävä sovelluksen tunnus.

   |Tunnus           |Kuvaus  |
   |----------------|-------------|
   |**AppId**       |Määritä tähän sovellustunnus.      |
   |**RedirectUri** |Aseta tähän sovellustunnus, mutta lisää etuliite **app://**.         |

    **Esimerkki** seuraavassa esimerkissä näkyy yhteysmerkkijono.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Ota yhteys käyttöön.

> [!Note]
> Jos haluat määrittää yhteyden [!INCLUDE[crm_md](includes/crm_md.md)] -ilmentymään tietyllä todennustyypillä, täytä **Todennustyypin tiedot** -pikavälilehden kentät. Lisätietoja on kohdassa [Microsoft Dataverse -verkkopalvelujen käyttö todennuksessa](/powerapps/developer/data-platform/authentication). Tätä vaihetta tarvita yhdistettäessä [!INCLUDE[prod_short](includes/prod_short.md)]in online-versiota.

## <a name="see-also"></a>Katso myös

[[!INCLUDE[crm_md](includes/crm_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Yhteyden määrittäminen [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Business Centralin ja [!INCLUDE[crm_md](includes/crm_md.md)]in synkronointi](admin-synchronizing-business-central-and-sales.md)  
[Paikallisen Dynamics 365 Salesin integroinnin valmistelu](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
