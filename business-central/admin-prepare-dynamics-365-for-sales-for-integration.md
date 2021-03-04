---
title: Dynamics 365 Sales -integrointi| Microsoft Docs
description: Tietoja Dynamics 365 Business Centralin valmistelusta Dynamics 365 Sales -integrointia varten.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 692c3d10ba8bc72b3993d4f05cc9dcaee7dabc8c
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035679"
---
# <a name="integrating-with-dynamics-365-sales"></a>Dynamics 365 Sales -integrointi
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Myyjää pidetään usein liiketoiminnan eniten ulospäin suuntautuneena tehtävänä. Myyjien voisi kuitenkin olla hyödyllistä tarkastella liiketoimintaa myös sisäisesti, jotta he tiedostaisivat, mitä taustalla tapahtuu. [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in integroinnin ansiosta myyjät saavat merkityksellisiä tietoja, joiden avulla he voivat tarkastella [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja [!INCLUDE[crm_md](includes/crm_md.md)]ia käyttäessään. Myyntitarjousta valmistellessa voi esimerkiksi olla hyödyllistä tietää, riittääkö varasto tilauksen täyttämiseen. Lisätietoja on kohdassa [Dynamics 365 Salesin käyttäminen Business Centralissa](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Tässä ohjeaiheessa kerrotaan [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen online-versioiden integroinnista [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun avulla. Lisätietoja paikallisesta määrityksestä on kohdassa [Paikallisen Dynamics 365 Salesin integroinnin valmistelu](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-dataverse"></a>Integroiminen Dataverse -palvelun avulla
[!INCLUDE[prod_short](includes/prod_short.md)] voidaan integroida myös [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun kanssa. Tämän vuoksi tietoja on helppo yhdistää ja synkronoida muiden Dynamics 365 -sovellusten, kuten [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen, tai jopa itse luotujen sovellusten kanssa. Jos integrointi tehdään ensimmäistä kertaa, on suositeltavaa tehdä se [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun kanssa. Lisätietoja on kohdassa [Integroiminen Dataverse -palvelun kanssa](admin-common-data-service.md).

Jos integrointi [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[prod_short](includes/prod_short.md)] -ratkaisun välillä on jo tehty, voit jatkaa tietojen synkronointia asetuksen avulla. Jos kuitenkin päivität [!INCLUDE[crm_md](includes/crm_md.md)] -integroinnin tai otat sen pois käytöstä, voit ottaa sen käyttöön uudelleen [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun avulla. Lisätietoja on kohdassa [Integroinnin päivittäminen Dynamics 365 Salesin avulla](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Jos uudelleenyhdistämisessä käytetään [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelua, käyttöön otetaan synkronoinnin oletusasetukset ja käytössä olevat määritykset korvataan. Esimerkiksi taulukon oletusyhdistämismääritykset otetaan käyttöön.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Integrointiasetukset, jotka ovat [!INCLUDE[crm_md](includes/crm_md.md)] -integrointikohtaisia
Integrointi [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen kanssa tapahtuu [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun kautta. Integrointi määrittää useita vakioasetuksia ja -taulukoita. Vakioasetusten lisäksi [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksella on sovelluskohtaisia asetuksia. Seuraavissa osissa esitellään ne.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Salesin käyttäjätilien käyttöoikeudet ja ja käyttöoikeusroolit
Kun integrointiratkaisua asennetaan, integroinnin käyttäjätilin käyttöoikeudet määritetään. Jos näitä käyttöoikeuksia on muutettu, käyttöoikeudet on ehkä palautettava alkuperäisiksi. Voit tehdä tämän asentamalla integrointiratkaisun uudelleen **Ota integraatioratkaisu uudelleen käyttöön** -kohdan avulla **Dynamics 365 -yhteyden asetukset** -sivulla. Seuraavat käyttöoikeus roolit on otettu käyttöön:

* Dynamics 365 Business Central -sovelluksen integroinnin järjestelmänvalvoja
* Dynamics 365 Business Central -sovelluksen integroinnin käyttäjä
* Dynamics 365 Business Central -sovelluksen tuotteen saatavuuden käyttäjä

### <a name="connection-settings-in-the-setup-guide"></a>Yhteysasetukset asennusoppaassa

Asetusten ohjattu määritysopas auttaa määrittämään yhteyden nopeasti ja määrittämään lisäominaisuudet, kuten tietueiden välisen yhdistämisen.

1. Valitse ensin **Asennus ja laajennukset** ja valitse sitten **Asetusten ohjattu määritys**.
2. Käynnistä asetusten ohjattu määritysopas valitsemalla **Dynamics 365 Sales -yhteyden määritys**.
3. Täytä tarvittavat kentät.
4. Vaihtoehtoisesti voit käyttää lisäasetuksia, jotka parantavat suojausta ja ottavat käyttöön lisäominaisuuksia, kuten myyntitilauksen käsittely ja varastotasojen tarkasteleminen. Lisäasetuksia käsitellään seuraavassa taulukossa.  

| Kenttä | Kuvaus |
|--|--|
| **Tuo Dynamics 365 Sales -ratkaisu** | Ottamalla tämän asteuksen käyttöön voit asentaa ja määrittää integrointiratkaisun [!INCLUDE[crm_md](includes/crm_md.md)]issa. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
| **Julkaise Nimikkeen saatavuus -verkkopalvelu** | Antaa [!INCLUDE[crm_md](includes/crm_md.md)]ia käyttäville henkilöille mahdollisuuden tarkastella nimikkeiden (tuotteiden) varastosaatavuutta [!INCLUDE[prod_short](includes/prod_short.md)]issa. Tämä varten tarvitaan [!INCLUDE[prod_short](includes/prod_short.md)] -käyttäjätili, jolla on verkkopalvelun käyttöoikeusavain. Avaimen määrittäminen on kaksivaiheinen prosessi. Valitse [!INCLUDE[prod_short](includes/prod_short.md)]in käyttäjätilillä **Muuta verkkopalvelun käyttöoikeusavainta** -toiminto. Määritä sitten asetusten ohjatussa Dynamics 365 Sales -yhteyden määrityksessä Dynamics 365 Business Centralin OData-verkkopalvelun URL-osoite ja anna palvelun käyttöön tarvittavat [!INCLUDE[prod_short](includes/prod_short.md)]in käyttäjän tunnistetiedot. Lisätietoja on kohdassa [OData-verkkopalvelut](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **Business Centralin OData-verkkopalvelun URL-osoite** | Jos otat käyttöön nimikkeen saatavuuden tarkastelemisen verkkopalvelun, OData-verkkopalvelun URL-osoite määritetään. |
| **Business Centralin OData-verkkopalvelun käyttäjätunnus** | Sen [!INCLUDE[prod_short](includes/prod_short.md)]in käyttäjätilin nimi, jolla [!INCLUDE[crm_md](includes/crm_md.md)] noutaa tietoja nimikkeen saatavuudesta [!INCLUDE[prod_short](includes/prod_short.md)]issa OData-verkkopalvelun kautta. |
| **Business Centralin OData-verkkopalvelun käyttöoikeusavain** | Sen käyttäjätilin käyttöoikeusavain, jolla [!INCLUDE[crm_md](includes/crm_md.md)] hakee tietoja nimikkeen saatavuudesta [!INCLUDE[prod_short](includes/prod_short.md)]ista OData-verkkopalvelun kautta. Avain on määritetty käyttäjälle, joka on valittu **Business Centralin OData-verkkopalvelun käyttäjätunnus** -kentässä. Voit hakea avaimen valitsemalla ensin käyttäjänimen vieressä **Hae arvo** -painikkeen ja sitten käyttäjän. Valitse seuraavaksi **Hallitse** ja lopuksi **Muokkaa**. Valitse käyttäjän kortissa ensin **Toiminnot**, **Tarkistus** ja sitten **Muuta verkkopalvelun käyttöoikeusavainta**. |
| **Ota käyttöön myyntitilauksen integrointi** | Kun myyntitilauksia luodaan [!INCLUDE[crm_md](includes/crm_md.md)]:ssä ja tilauksia täytetään [!INCLUDE[prod_short](includes/prod_short.md)]:ssä, [!INCLUDE[crm_md](includes/crm_md.md)] integroi prosessin. Lisätietoja on kohdassa [Myyntitilauksen käsittelyn integroinnin käyttöönotto](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Tätä varten on annettava järjestelmänvalvojan käyttäjätilin tunnistetiedot [!INCLUDE[crm_md](includes/crm_md.md)]issa. Lisätietoja on kohdassa [Myyntitilauksen tietojen käsitteleminen](marketing-integrate-dynamicscrm.md#handling-sales-order-data) |
| **Ota CDS-yhteys käyttöön** | Ota [!INCLUDE[prod_short](includes/cds_long_md.md)] -yhteys käyttöön. |
| **Dynamics 365 SDK -versio** | Tällä on merkitystä vain, jos integrointi tehdään [!INCLUDE[crm_md](includes/crm_md.md)]in paikalliseen versioon. Voit yhdistää tällä Dynamics 365 SDK -versiolla (joka tunnetaan myös nimellä Xrm) [!INCLUDE[prod_short](includes/prod_short.md)]in [!INCLUDE[crm_md](includes/crm_md.md)]iin. Version on oltava yhteensopiva sen SDK-version kanssa, jota [!INCLUDE[crm_md](includes/crm_md.md)] käyttää. Lisäksi sen on oltava sama tai uudempi kuin versio, jota [!INCLUDE[crm_md](includes/crm_md.md)] käyttää. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Microsoft Dynamics 365 -yhteyden määrityssivun yhteysasetukset

Anna seuraavat tiedot yhteyden muodostamiseen [!INCLUDE[crm_md](includes/crm_md.md)]ista [!INCLUDE[prod_short](includes/prod_short.md)]iin.

| Kenttä | Kuvaus |
|--|--|
| **Dynamics 365 Sales -ohjelman URL-osoite** | [!INCLUDE[crm_md](includes/crm_md.md)] -ilmentymän URL-osoite. Näin käyttäjät voivat avata vastaavat tietueet [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen tietueista, kuten tilistä tai tuotteesta. [!INCLUDE[prod_short](includes/prod_short.md)]in tietueet avautuvat [!INCLUDE[prod_short](includes/prod_short.md)]issa. |
|**Dynamics 365 Sales -ohjelman URL-osoite**|[!INCLUDE[crm_md](includes/crm_md.md)] -ilmentymän URL-osoite. Näin käyttäjät voivat avata vastaavat tietueet [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen tietueista, kuten tilistä tai tuotteesta. [!INCLUDE[prod_short](includes/prod_short.md)]in tietueet avautuvat [!INCLUDE[prod_short](includes/prod_short.md)]issa.|
|**Nimikkeen saatavuus -verkkopalvelu käytössä**|Antaa [!INCLUDE[crm_md](includes/crm_md.md)]ia käyttäville henkilöille mahdollisuuden tarkastella nimikkeiden (tuotteiden) varastosaatavuutta [!INCLUDE[prod_short](includes/prod_short.md)]issa. Jos otat tämän vaihtoehdon käyttöön, sinun on annettava myös [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjänimi ja käyttöoikeusavain, mikäli haluat tehdä nimikkeiden (tuotteiden) saatavuuskyselyn OData-verkkopalvelun avulla. Lisätietoja on kohdassa [OData-verkkopalvelut](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**Dynamics 365 Business Centralin OData-verkkopalvelun URL-osoite**|Jos otat Nimikkeen saatavuus -verkkopalvelun käyttöön, saat OData-verkkopalvelun URL-osoitteen. Määritä tämän kentän arvoksi käytettävän [!INCLUDE[prod_short](includes/prod_short.md)] -esiintymän URL-osoite.<br /><br /> Voit palauttaa kenttään [!INCLUDE[prod_short](includes/prod_short.md)]in oletusarvoisen URL-osoitteen valitsemalla **Palauta verkkoasiakasohjelman URL-osoite** -toiminnon.<br /><br /> Tällä kentällä on merkitystä vain, jos [!INCLUDE[prod_short](includes/prod_short.md)] -integrointiratkaisu on asennettu [!INCLUDE[crm_md](includes/crm_md.md)]issa.|
|**Dynamics 365 Business Centralin OData-verkkopalvelun käyttäjätunnus**|Sen käyttäjätilin nimi, jolla [!INCLUDE[crm_md](includes/crm_md.md)] hakee tietoja nimikkeen saatavuudesta [!INCLUDE[prod_short](includes/prod_short.md)]issa OData-verkkopalvelun kautta.|
|**Dynamics 365 Business Centralin OData-verkkopalvelun käyttöoikeusavain**|Sen käyttäjätilin käyttöoikeusavain, jolla [!INCLUDE[crm_md](includes/crm_md.md)] hakee tietoja nimikkeen saatavuudesta [!INCLUDE[prod_short](includes/prod_short.md)]ista OData-verkkopalvelun kautta. Avain on määritetty käyttäjälle, joka on valittu **Dynamics 365 Business Centralin OData-verkkopalvelun käyttäjätunnus** -kentässä. Voit hakea avaimen valitsemalla ensin käyttäjänimen vieressä **Hae arvo** -painikkeen ja sitten käyttäjän. Valitse seuraavaksi **Hallitse** ja lopuksi **Muokkaa**. Valitse käyttäjän kortissa ensin **Toiminnot**, **Tarkistus** ja sitten **Muuta verkkopalvelun käyttöoikeusavainta**.|
|**Dynamics 365 SDK -versio**|Jos integroit [!INCLUDE[crm_md](includes/crm_md.md)]in paikallisen version, muodosta yhteys [!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin tämän Dynamics 365 SDK -version avulla (joka tunnetaan myös nimellä Xrm). Valitsemasi version on oltava yhteensopiva [!INCLUDE[crm_md](includes/crm_md.md)]in käyttämän SDK-version kanssa. Tämä versio on sama tai uudempi kuin [!INCLUDE[crm_md](includes/crm_md.md)]in käyttämä versio.|-->

Syötä yllä olevien asetusten lisäksi seuraavat asetukset [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukselle.

| Kenttä | Kuvaus |
|--|--|
| **Myyntitilauksen integrointi on käytössä** | Antaa käyttäjille mahdollisuuden lähettää myyntitilauksia ja aktivoituja tarjouksia [!INCLUDE[crm_md](includes/crm_md.md)]issa sekä tarkastella ja käsitellä niitä sitten [!INCLUDE[prod_short](includes/prod_short.md)]issa. Tämä integroi prosessin [!INCLUDE[crm_md](includes/crm_md.md)]:ssä. Lisätietoja on kohdassa [Myyntitilauksen käsittelyn integroinnin käyttöönotto](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Myyntitilausten automaattinen luominen** | Luo myyntitilaus [!INCLUDE[prod_short](includes/prod_short.md)]issa, kun käyttäjä luo ja lähettää sellaisen [!INCLUDE[crm_md](includes/crm_md.md)]issa. |
| **Käsittele myyntitarjoukset automaattisesti** | Käsittele myyntitarjous [!INCLUDE[prod_short](includes/prod_short.md)]issa, kun käyttäjä luo ja aktivoi sellaisen [!INCLUDE[crm_md](includes/crm_md.md)]issa. |

<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Synkronoinnin Myynti-entiteetin yhdistämismääritys

[!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen entiteetit, kuten tilaukset, yhdistetään [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksessa samantyyppisiin taulukoihin, kuten myyntitilauksiin. [!INCLUDE[crm_md](includes/crm_md.md)]in tietoja käytetään määrittämällä linkkejä [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in taulukoiden välille. Tätä sanotaan yhdistämiseksi.

Seuraavassa taulukossa on luettelo [!INCLUDE[prod_short](includes/prod_short.md)]in tarjoamista tavallisista yhdistämismäärityksistä [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]:n taulukoiden välillä.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synkronoinnin suunta | Oletussuodatin |
|--|--|--|--|
| Mittayksikkö | Yksikköryhmä | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Nimike | Tuote | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-sovelluksen kontaktin suodatin: **Tuotteen tyyppi** on **Myyntivarasto** |
| Resurssi | Tuote | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-sovelluksen kontaktin suodatin: **Tuotteen tyyppi** on **Palvelut** |
| Asiakkaan hintaryhmä | Hinnasto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Myyntihinta | Tuotehinnasto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] kontaktisuodatin: **Myyntikoodi** ei ole tyhjä, **Myyntityyppi** on **Asiakkaan hintaluokka** |
| Mahdollisuus | Mahdollisuus | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Myyntilaskun otsikko | Lasku | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Myyntilaskurivi | Laskutustuote | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Myyntitilauksen otsikko | Myyntitilaus | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] Myynnin Ylätunnuksen suodatin: **Dokumenttityyppi** on Järjestys, **Tila** on Vapautettu. |
| Myyntitilauksen huomautukset | Myyntitilauksen huomautukset | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

### <a name="synchronization-rules"></a>Synkronointisäännöt

Seuraavassa taulukossa ovat säännöt, jotka ohjaavat [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen välistä synkronointia. Nämä ovat myös Dataverse -palvelussa määritettyjä sääntöjä, jotka otetaan käyttöön. Lisätietoja on kohdassa [Vakioentiteetin yhdistämismääritys](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Integroinnin käyttäjätilin tekemiä muutoksia ei synkronoida. Tämän vuoksi on suositeltavaa, että tietoja ei muuteta kyseistä tiliä käytettäessä. Lisätietoja on kohdassa [Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).

|Sivupöytä|Sääntö|
|-----|----|
|Mittayksiköt|Mittayksiköt synkronoidaan yksikköryhmien kanssa [!INCLUDE[crm_md](includes/crm_md.md)]issa. Yksikköryhmälle voi määrittää vain yhden mittayksikön.|
|Nimikkeet|Kun nimikkeitä synkronisoidaan [!INCLUDE[crm_md](includes/crm_md.md)] tuotteiden kanssa [!INCLUDE[prod_short](includes/prod_short.md)] luo automaattisesti hintalistan [!INCLUDE[crm_md](includes/crm_md.md)]ssä. Synkronointivirheitä välttämiseksi Älä muokkaa tämän hinnaston manuaalisesti.|
|Resurssit|Resurssit synkronoidaan niiden [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteiden kanssa, joiden tyyppi on Palvelu.|
|Asiakashintaryhmät|Asiakkaan hintaryhmät synkronoidaan myyntihinnastojen kanssa.|
|Myyntihinnat|Myyntihintojen myyntityyppi on Asiakkaan hintaryhmä. Niiden määritetty myyntikoodi synkronoidaan [!INCLUDE[crm_md](includes/crm_md.md)]in hinnaston rivien kanssa.|
|Mahdollisuudet|Mahdollisuudet synkronoidaan [!INCLUDE[crm_md](includes/crm_md.md)]in mahdollisuuksien kanssa. Myyjän koodin arvo määrittää yhdistetyn taulukon omistajan [!INCLUDE[crm_md](includes/crm_md.md)]issa.|
|Kirjatut myyntilaskut|Kirjatut myyntilaskut synkronoidaan myyntilaskujen kanssa. Ennen laskun synkronointia kannattaa synkronoida kaikki muut taulukot, jotka voivat vaikuttaa laskuun. Niitä voivat olla esimerkiksi myyjät ja hinnastot. Laskun otsikossa oleva myyjän koodin arvo määrittää yhdistetyn taulukon omistajan Sales-sovelluksessa.|
|Myyntitilaukset|Kun myyntitilausten integrointi on käytössä, [!INCLUDE[prod_short](includes/prod_short.md)]:n myyntitilaukset, jotka on luotu lähetetyistä myyntitilauksista [!INCLUDE[crm_md](includes/crm_md.md)]:ssä, synkronoidaan myyntitilausten kanssa INCLUDE SALES -kohdassa vapautuksen yhteydessä. Ennen tilausten synkronoimista on suositeltavaa synkronoida kaikki tilaukseen liittyvät taulukot, esimerkiksi myyjät ja hinnastot. Tilauksen otsikossa oleva Myyjän koodi -kenttä määrittää yhdistetyn taulukon omistajan [!INCLUDE[crm_md](includes/crm_md.md)]:ssä.|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Myynnin integroinnin synkronointityöt

Työt suoritetaan seuraavassa järjestyksessä, jotta taulukoiden välille ei muodostu yhdistämisen riippuvuussuhteita. Dataverse -palvelussa on lisätöitä. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](/dynamics365/business-central/admin-job-queues-schedule-tasks).

1. MITTAYKSIKKÖ – Dynamics 365 Salesin synkronointityö  
2. RESURSSI-TUOTE – Dynamics 365 Salesin synkronointityö  
3. NIMIKE-TUOTE – Dynamics 365 Salesin synkronointityö  
4. ASIAKHNTRHM-HINTA - Dynamics 365 Salesin synkronointityö.
5. MYYNTIHNT-TUOTEHINTA - Dynamics 365 Salesin synkronointityö.
6. KIRJMNTILASKU-LASK – Dynamics 365 Salesin synkronointityö.

### <a name="default-synchronization-job-queue-entries"></a>Oletusarvoiset synkronoinnin työjonotapahtumat

Seuraavassa taulukossa kuvaillaan Salesin synkronoinnin oletustyöt.  

|Työjonotapahtuma|Kuvaus|Suunta|Integrointitaulukon yhdistämismääritys|Synkronoinnin oletustiheys (min)|Passivisuuden oletusaika (min)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|MITTAYKSIKKÖ – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in yksikköryhmät ja [!INCLUDE[prod_short](includes/prod_short.md)]in mittayksiköt.|[!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|MITTAYKSIKKÖ|30|720<br> (12 tuntia)|
|RESURSSI-TUOTE – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteet ja [!INCLUDE[prod_short](includes/prod_short.md)]in resurssit.|[!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|RESURSSI-TUOTE|30|720<br> (12 tuntia)|
|NIMIKE-TUOTE – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteet ja [!INCLUDE[prod_short](includes/prod_short.md)]in nimikkeet.|[!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|NIMIKE-TUOTE|30|1440<br> (24 tuntia)|
|ASIAKHNTRHM-HINTA – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in myyntihinnaston ja [!INCLUDE[prod_short](includes/prod_short.md)]in asiakashintaryhmät.| |ASIAKASHINTARYHMÄT-MYYNTIHINNASTOT|30|1440<br> (24 tuntia)|
|MYYNTIHNT-TUOTEHINTA – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotehinnat ja [!INCLUDE[prod_short](includes/prod_short.md)]in myyntihinnat.||TUOTEHINTA-MYYNTIHINTA|30|1440<br> (24 tuntia)|
|KIRJMNTILASKU-LASK – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in laskut ja [!INCLUDE[prod_short](includes/prod_short.md)]in kirjatut myyntilaskut.|[!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|LASKUT-KIRJATUT MYYNTILASKUT|30|1440<br> (24 tuntia)|
|Asiakastilastot – Dynamics 365 Salesin synkronointityö|Päivittää [!INCLUDE[crm_md](includes/crm_md.md)]in tilit uusilla [!INCLUDE[prod_short](includes/prod_short.md)]in asiakastiedoilla. Nämä tiedot näkyvät [!INCLUDE[crm_md](includes/crm_md.md)]issa niiden tilien **Business Central -tilin tilastot** -pikanäkymälomakkeessa, jotka on yhdistetty [!INCLUDE[prod_short](includes/prod_short.md)]in asiakkaisiin.<br /><br /> Nämä tiedot voidaan päivittää myös manuaalisesti kustakin asiakastietueesta. Lisätietoja on kohdassa [Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Huomautus:** Tällä työjonotapahtumalla on merkitystä vain, jos [!INCLUDE[prod_short](includes/prod_short.md)] -integrointiratkaisu on asennettu [!INCLUDE[crm_md](includes/crm_md.md)]iin. |Ei sovellu|Ei sovellu|30|Ei sovellu| 

## <a name="connecting-business-central-on-premises-versions-earlier-than-version-16"></a>Versiota 16 aikaisempien Business Central On-Premises -versioiden yhdistäminen
Microsoft Power Platform -tiimi on [ilmoittanut](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse), että se poistaa käytöstä Office365-todennus tyypin. Jos käytät [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versioita, jotka ovat vanhempia kuin 16, sinun on käytettävä OAuth-todennustyyppiä yhteyden muodostamiseen [!INCLUDE[crm_md](includes/crm_md.md)] onlineen. Tässä osassa kerrotaan, miten yhteys muodostetaan.

### <a name="requirements"></a>Tarpeet
Sinulla täytyy olla Microsoft Azure -tilaus. Kokeilutili toimii sovelluksen rekisteröinnissä.

### <a name="to-connect-a-version-of-business-central-earlier-than-version-16"></a>Versiota 16 aikaisempien Business Central -versioiden yhdistäminen
1. Tuo Microsoft Dynamics 365 Business Central -integrointiratkaisu [!INCLUDE[crm_md](includes/crm_md.md)] -ympäristöösi. Integrointiratkaisu on käytettävissä Business Centralin DVD-asennuslevyn CrmCustomization-kansiossa. Ratkaisusta on monta versiota, kuten DynamicsNAVIntegrationSolution_v8, DynamicsNAVIntegrationSolution_v9 tai DynamicsNAVIntegrationSolution_v91. Tuotava ratkaisu riippuu siitä, mihin [!INCLUDE[crm_md](includes/crm_md.md)] -versioon olet muodostamassa yhteyttä. [!INCLUDE[crm_md](includes/crm_md.md)] online edellyttää DynamicsNAVIntegrationSolution_v91-integrointiratkaisun.
2. Luo [!INCLUDE[crm_md](includes/crm_md.md)] -ympäristöösi ei-vuorovaikutteinen integrointikäyttäjä ja määritä käyttäjälle seuraavat käyttöoikeusroolit. Lisätietoja on kohdassa [Ei-vuorovaikutteisen käyttäjätilin luominen](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central -sovelluksen integroinnin järjestelmänvalvoja
   * Dynamics 365 Business Central -sovelluksen integroinnin käyttäjä

   > [!Important]
   > Käyttäjällä ei saa olla järjestelmänvalvojan käyttöoikeusroolia. Et voi myöskään käyttää järjestelmänvalvojan tiliä integrointikäyttäjänä.

3.  Luo [!INCLUDE[prod_short](includes/prod_short.md)]in sovellusrekisteröinti Azure-portaalissa. Ohjeita on kohdassa [Sovelluksen rekisteröinti Azure Active Directoryssä](/business-central/dev-itpro/administration/register-app-azure?branch=live#register-an-application-in-azure-active-directory). [!INCLUDE[crm_md](includes/crm_md.md)] -yhteyden muodostamiseen liittyvät asetukset ovat delegoituja oikeuksia. Seuraavassa taulukossa on luettelo ja kuvaukset oikeuksista.

   |Ohjelmistorajapinta / käyttöoikeuden nimi |Tyyppi  |Kuvaus  |
   |---------|---------|---------|
   |Financials.ReadWrite.All     |Delegoitu|Pakollinen kohteelle: [!INCLUDE[prod_short](includes/prod_short.md)].    |
   |user_impersonation     |Delegoitu|Pakollinen kohteelle: [!INCLUDE[crm_md](includes/crm_md.md)].|
   
4. Etsi [!INCLUDE[prod_short](includes/prod_short.md)]issa **Microsoft Dynamics 365 -yhteysasetukset** ja valitse sitten liittyvä linkki. 
5. Valitse **Microsoft Dynamics 365 -yhteysasetukset** -sivun **Todennustyyppi**-kentässä OAuth-asetus. 
6. Valitse CRM SDK -versio, joka vastaa vaiheessa 1 tuotua ratkaisuversiota.
7. Kirjoita **Palvelimen osoite** -kenttään [!INCLUDE[crm_md](includes/crm_md.md)] -ympäristösi URL-osoite ja kirjoita sitten integrointikäyttäjän käyttäjänimi ja salasana.
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
> Jos haluat määrittää yhteyden [!INCLUDE[crm_md](includes/crm_md.md)] -ilmentymään tietyllä todennustyypillä, täytä **Todennustyypin tiedot** -pikavälilehden kentät. Lisätietoja on kohdassa [Yhteyden muodostaminen Dynamics 365:een XRM-työkalujen yhteysmerkkijonojen avulla](https://go.microsoft.com/fwlink/?linkid=843055). Tätä vaihetta tarvita yhdistettäessä [!INCLUDE[prod_short](includes/prod_short.md)]in online-versiota.

## <a name="see-also"></a>Katso myös

[[!INCLUDE[crm_md](includes/crm_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Yhteyden määrittäminen [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Business Centralin ja [!INCLUDE[crm_md](includes/crm_md.md)]in synkronointi](admin-synchronizing-business-central-and-sales.md)  
[Paikallisen Dynamics 365 Salesin integroinnin valmistelu](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]