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
ms.date: 07/23/2020
ms.author: bholtorf
ms.openlocfilehash: 7132a32a37844078b696af5e8d19bf951460a2e2
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617652"
---
# <a name="integrating-with-dynamics-365-sales"></a>Dynamics 365 Sales -integrointi

Myyjää pidetään usein liiketoiminnan eniten ulospäin suuntautuneena tehtävänä. Myyjien voisi kuitenkin olla hyödyllistä tarkastella liiketoimintaa myös sisäisesti, jotta he tiedostaisivat, mitä taustalla tapahtuu. [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in integroinnin ansiosta myyjät saavat merkityksellisiä tietoja, joiden avulla he voivat tarkastella [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja [!INCLUDE[crm_md](includes/crm_md.md)]ia käyttäessään. Myyntitarjousta valmistellessa voi esimerkiksi olla hyödyllistä tietää, riittääkö varasto tilauksen täyttämiseen. Lisätietoja on kohdassa [Dynamics 365 Salesin käyttäminen Business Centralissa](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Tässä ohjeaiheessa kerrotaan [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen online-versioiden integroinnista [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelun avulla. Lisätietoja paikallisesta määrityksestä on kohdassa [Paikallisen Dynamics 365 Salesin integroinnin valmistelu](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-common-data-service"></a>Integroiminen Common Data Service -palvelun avulla
[!INCLUDE[d365fin](includes/d365fin_md.md)] voidaan integroida myös [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelun kanssa. Tämän vuoksi tietoja on helppo yhdistää ja synkronoida muiden Dynamics 365 -sovellusten, kuten [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen, tai jopa itse luotujen sovellusten kanssa. Jos integrointi tehdään ensimmäistä kertaa, on suositeltavaa tehdä se [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelun kanssa. Lisätietoja on kohdassa [Integroiminen Common Data Service -palvelun kanssa](admin-common-data-service.md).

Jos integrointi [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ratkaisun välillä on jo tehty, voit jatkaa tietojen synkronointia asetuksen avulla. Jos kuitenkin päivität [!INCLUDE[crm_md](includes/crm_md.md)] -integroinnin tai otat sen pois käytöstä, voit ottaa sen käyttöön uudelleen [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelun avulla. Lisätietoja on kohdassa [Integroinnin päivittäminen Dynamics 365 Salesin avulla](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Jos uudelleenyhdistämisessä käytetään [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelua, käyttöön otetaan synkronoinnin oletusasetukset ja käytössä olevat määritykset korvataan. Esimerkiksi taulukon oletusyhdistämismääritykset otetaan käyttöön.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Integrointiasetukset, jotka ovat [!INCLUDE[crm_md](includes/crm_md.md)] -integrointikohtaisia
Integrointi [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen kanssa tapahtuu [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelun kautta. Integrointi määrittää useita vakioasetuksia ja -entiteettejä. Vakioasetusten lisäksi [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksella on sovelluskohtaisia asetuksia. Seuraavissa osissa esitellään ne.

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
| **Julkaise Nimikkeen saatavuus -verkkopalvelu** | Antaa [!INCLUDE[crm_md](includes/crm_md.md)]ia käyttäville henkilöille mahdollisuuden tarkastella nimikkeiden (tuotteiden) varastosaatavuutta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Tämä varten tarvitaan [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjätili, jolla on verkkopalvelun käyttöoikeusavain. Avaimen määrittäminen on kaksivaiheinen prosessi. Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätilillä **Muuta verkkopalvelun käyttöoikeusavainta** -toiminto. Määritä sitten asetusten ohjatussa Dynamics 365 Sales -yhteyden määrityksessä Dynamics 365 Business Centralin OData-verkkopalvelun URL-osoite ja anna palvelun käyttöön tarvittavat [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjän tunnistetiedot. Lisätietoja on kohdassa [OData-verkkopalvelut](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **Business Centralin OData-verkkopalvelun URL-osoite** | Jos otat käyttöön nimikkeen saatavuuden tarkastelemisen verkkopalvelun, OData-verkkopalvelun URL-osoite määritetään. |
| **Business Centralin OData-verkkopalvelun käyttäjätunnus** | Sen [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätilin nimi, jolla [!INCLUDE[crm_md](includes/crm_md.md)] noutaa tietoja nimikkeen saatavuudesta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa OData-verkkopalvelun kautta. |
| **Business Centralin OData-verkkopalvelun käyttöoikeusavain** | Sen käyttäjätilin käyttöoikeusavain, jolla [!INCLUDE[crm_md](includes/crm_md.md)] hakee tietoja nimikkeen saatavuudesta [!INCLUDE[d365fin](includes/d365fin_md.md)]ista OData-verkkopalvelun kautta. Avain on määritetty käyttäjälle, joka on valittu **Business Centralin OData-verkkopalvelun käyttäjätunnus** -kentässä. Voit hakea avaimen valitsemalla ensin käyttäjänimen vieressä **Hae arvo** -painikkeen ja sitten käyttäjän. Valitse seuraavaksi **Hallitse** ja lopuksi **Muokkaa**. Valitse käyttäjän kortissa ensin **Toiminnot**, **Tarkistus** ja sitten **Muuta verkkopalvelun käyttöoikeusavainta**. |
| **Ota käyttöön myyntitilauksen integrointi** | Kun myyntitilauksia luodaan [!INCLUDE[crm_md](includes/crm_md.md)]:ssä ja tilauksia täytetään [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä, [!INCLUDE[crm_md](includes/crm_md.md)] integroi prosessin. Lisätietoja on kohdassa [Myyntitilauksen käsittelyn integroinnin käyttöönotto](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Tätä varten on annettava järjestelmänvalvojan käyttäjätilin tunnistetiedot [!INCLUDE[crm_md](includes/crm_md.md)]issa. Lisätietoja on kohdassa [Myyntitilauksen tietojen käsitteleminen](marketing-integrate-dynamicscrm.md#handling-sales-order-data) |
| **Ota CDS-yhteys käyttöön** | Ota [!INCLUDE[d365fin](includes/cds_long_md.md)] -yhteys käyttöön. |
| **Dynamics 365 SDK -versio** | Tällä on merkitystä vain, jos integrointi tehdään [!INCLUDE[crm_md](includes/crm_md.md)]in paikalliseen versioon. Voit yhdistää tällä Dynamics 365 SDK -versiolla (joka tunnetaan myös nimellä Xrm) [!INCLUDE[d365fin](includes/d365fin_md.md)]in [!INCLUDE[crm_md](includes/crm_md.md)]iin. Version on oltava yhteensopiva sen SDK-version kanssa, jota [!INCLUDE[crm_md](includes/crm_md.md)] käyttää. Lisäksi sen on oltava sama tai uudempi kuin versio, jota [!INCLUDE[crm_md](includes/crm_md.md)] käyttää. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Microsoft Dynamics 365 -yhteyden määrityssivun yhteysasetukset

Anna seuraavat tiedot yhteyden muodostamiseen [!INCLUDE[crm_md](includes/crm_md.md)]ista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.

| Kenttä | Kuvaus |
|--|--|
| **Dynamics 365 Sales -ohjelman URL-osoite** | [!INCLUDE[crm_md](includes/crm_md.md)] -ilmentymän URL-osoite. Näin käyttäjät voivat avata vastaavat tietueet [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen tietueista, kuten tilistä tai tuotteesta. [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueet avautuvat [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. |
|**Dynamics 365 Sales -ohjelman URL-osoite**|[!INCLUDE[crm_md](includes/crm_md.md)] -ilmentymän URL-osoite. Näin käyttäjät voivat avata vastaavat tietueet [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen tietueista, kuten tilistä tai tuotteesta. [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueet avautuvat [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.|
|**Nimikkeen saatavuus -verkkopalvelu käytössä**|Antaa [!INCLUDE[crm_md](includes/crm_md.md)]ia käyttäville henkilöille mahdollisuuden tarkastella nimikkeiden (tuotteiden) varastosaatavuutta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Jos otat tämän vaihtoehdon käyttöön, sinun on annettava myös [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjänimi ja käyttöoikeusavain, mikäli haluat tehdä nimikkeiden (tuotteiden) saatavuuskyselyn OData-verkkopalvelun avulla. Lisätietoja on kohdassa [OData-verkkopalvelut](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**Dynamics 365 Business Centralin OData-verkkopalvelun URL-osoite**|Jos otat Nimikkeen saatavuus -verkkopalvelun käyttöön, saat OData-verkkopalvelun URL-osoitteen. Määritä tämän kentän arvoksi käytettävän [!INCLUDE[d365fin](includes/d365fin_md.md)] -esiintymän URL-osoite.<br /><br /> Voit palauttaa kenttään [!INCLUDE[d365fin](includes/d365fin_md.md)]in oletusarvoisen URL-osoitteen valitsemalla **Palauta verkkoasiakasohjelman URL-osoite** -toiminnon.<br /><br /> Tällä kentällä on merkitystä vain, jos [!INCLUDE[d365fin](includes/d365fin_md.md)] -integrointiratkaisu on asennettu [!INCLUDE[crm_md](includes/crm_md.md)]issa.|
|**Dynamics 365 Business Centralin OData-verkkopalvelun käyttäjätunnus**|Sen käyttäjätilin nimi, jolla [!INCLUDE[crm_md](includes/crm_md.md)] hakee tietoja nimikkeen saatavuudesta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa OData-verkkopalvelun kautta.|
|**Dynamics 365 Business Centralin OData-verkkopalvelun käyttöoikeusavain**|Sen käyttäjätilin käyttöoikeusavain, jolla [!INCLUDE[crm_md](includes/crm_md.md)] hakee tietoja nimikkeen saatavuudesta [!INCLUDE[d365fin](includes/d365fin_md.md)]ista OData-verkkopalvelun kautta. Avain on määritetty käyttäjälle, joka on valittu **Dynamics 365 Business Centralin OData-verkkopalvelun käyttäjätunnus** -kentässä. Voit hakea avaimen valitsemalla ensin käyttäjänimen vieressä **Hae arvo** -painikkeen ja sitten käyttäjän. Valitse seuraavaksi **Hallitse** ja lopuksi **Muokkaa**. Valitse käyttäjän kortissa ensin **Toiminnot**, **Tarkistus** ja sitten **Muuta verkkopalvelun käyttöoikeusavainta**.|
|**Dynamics 365 SDK -versio**|Jos integroit [!INCLUDE[crm_md](includes/crm_md.md)]in paikallisen version, muodosta yhteys [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin tämän Dynamics 365 SDK -version avulla (joka tunnetaan myös nimellä Xrm). Valitsemasi version on oltava yhteensopiva [!INCLUDE[crm_md](includes/crm_md.md)]in käyttämän SDK-version kanssa. Tämä versio on sama tai uudempi kuin [!INCLUDE[crm_md](includes/crm_md.md)]in käyttämä versio.|-->

Syötä yllä olevien asetusten lisäksi seuraavat asetukset [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukselle.

| Kenttä | Kuvaus |
|--|--|
| **Myyntitilauksen integrointi on käytössä** | Antaa käyttäjille mahdollisuuden lähettää myyntitilauksia ja aktivoituja tarjouksia [!INCLUDE[crm_md](includes/crm_md.md)]issa sekä tarkastella ja käsitellä niitä sitten [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Tämä integroi prosessin [!INCLUDE[crm_md](includes/crm_md.md)]:ssä. Lisätietoja on kohdassa [Myyntitilauksen käsittelyn integroinnin käyttöönotto](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Myyntitilausten automaattinen luominen** | Luo myyntitilaus [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, kun käyttäjä luo ja lähettää sellaisen [!INCLUDE[crm_md](includes/crm_md.md)]issa. |
| **Käsittele myyntitarjoukset automaattisesti** | Käsittele myyntitarjous [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, kun käyttäjä luo ja aktivoi sellaisen [!INCLUDE[crm_md](includes/crm_md.md)]issa. |

<!--
### User Account Settings
Integrate with Business Central through Common Data Service requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Synkronoinnin Myynti-entiteetin yhdistämismääritys

[!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen entiteetit, kuten tilaukset, yhdistetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa samantyyppisiin entiteetteihin, kuten myyntitilauksiin. [!INCLUDE[crm_md](includes/crm_md.md)]in tietoja käytetään määrittämällä linkkejä [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in välille. Tätä sanotaan yhdistämiseksi.

Seuraavassa taulukossa on luettelo tavallisista [!INCLUDE[d365fin](includes/d365fin_md.md)]in yhdistämismäärityksistä [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)] välillä.

| [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synkronoinnin suunta | Oletussuodatin |
|--|--|--|--|
| Mittayksikkö | Yksikköryhmä | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Nimike | Tuote | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Sales-sovelluksen kontaktin suodatin: **Tuotteen tyyppi** on **Myyntivarasto** |
| Resurssi | Tuote | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Sales-sovelluksen kontaktin suodatin: **Tuotteen tyyppi** on **Palvelut** |
| Asiakkaan hintaryhmä | Hinnasto | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Myyntihinta | Tuotehinnasto | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] kontaktisuodatin: **Myyntikoodi** ei ole tyhjä, **Myyntityyppi** on **Asiakkaan hintaluokka** |
| Mahdollisuus | Mahdollisuus | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |
| Myyntilaskun otsikko | Lasku | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Myyntilaskurivi | Laskutustuote | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Myyntitilauksen otsikko | Myyntitilaus | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] Myynnin Ylätunnuksen suodatin: **Dokumenttityyppi** on Järjestys, **Tila** on Vapautettu. |
| Myyntitilauksen huomautukset | Myyntitilauksen huomautukset | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |

### <a name="synchronization-rules"></a>Synkronointisäännöt

Seuraavassa taulukossa ovat säännöt, jotka ohjaavat [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen välistä synkronointia. Nämä ovat myös Common Data Service -palvelussa määritettyjä sääntöjä, jotka otetaan käyttöön. Lisätietoja on kohdassa [Vakioentiteetin yhdistämismääritys](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-entity-mapping-for-synchronization).

> [!NOTE]  
> Integroinnin käyttäjätilin tekemiä muutoksia ei synkronoida. Tämän vuoksi on suositeltavaa, että tietoja ei muuteta kyseistä tiliä käytettäessä. Lisätietoja on kohdassa [Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).

|Sivupöytä|Sääntö|
|-----|----|
|Mittayksiköt|Mittayksiköt synkronoidaan yksikköryhmien kanssa [!INCLUDE[crm_md](includes/crm_md.md)]issa. Yksikköryhmälle voi määrittää vain yhden mittayksikön.|
|Nimikkeet|Kun nimikkeitä synkronisoidaan [!INCLUDE[crm_md](includes/crm_md.md)] tuotteiden kanssa [!INCLUDE[d365fin](includes/d365fin_md.md)] luo automaattisesti hintalistan [!INCLUDE[crm_md](includes/crm_md.md)]ssä. Synkronointivirheitä välttämiseksi Älä muokkaa tämän hinnaston manuaalisesti.|
|Resurssit|Resurssit synkronoidaan niiden [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteiden kanssa, joiden tyyppi on Palvelu.|
|Asiakashintaryhmät|Asiakkaan hintaryhmät synkronoidaan myyntihinnastojen kanssa.|
|Myyntihinnat|Myyntihintojen myyntityyppi on Asiakkaan hintaryhmä. Niiden määritetty myyntikoodi synkronoidaan [!INCLUDE[crm_md](includes/crm_md.md)]in hinnaston rivien kanssa.|
|Mahdollisuudet|Mahdollisuudet synkronoidaan [!INCLUDE[crm_md](includes/crm_md.md)]in mahdollisuuksien kanssa. Myyjän koodin arvo määrittää yhdistetyn entiteetin omistajan [!INCLUDE[crm_md](includes/crm_md.md)]issa.|
|Kirjatut myyntilaskut|Kirjatut myyntilaskut synkronoidaan myyntilaskujen kanssa. Ennen laskun synkronointia kannattaa synkronoida kaikki muut entiteetit, jotka voivat vaikuttaa laskuun. Niitä voivat olla esimerkiksi myyjät ja hinnastot. Laskun otsikossa oleva myyjän koodin arvo määrittää yhdistetyn entiteetin omistajan Sales-sovelluksessa.|
|Myyntitilaukset|Kun myyntitilausten integrointi on käytössä, [!INCLUDE[d365fin](includes/d365fin_md.md)]:n myyntitilaukset, jotka on luotu lähetetyistä myyntitilauksista [!INCLUDE[crm_md](includes/crm_md.md)]:ssä, synkronoidaan myyntitilausten kanssa INCLUDE SALES -kohdassa vapautuksen yhteydessä. Ennen tilausten synkronoimista on suositeltavaa synkronoida kaikki tilaukseen liittyvät entiteetit, esimerkiksi myyjät ja hinnastot. Tilauksen otsikossa oleva Myyjän koodi -kenttä määrittää yhdistetyn entiteetin omistajan [!INCLUDE[crm_md](includes/crm_md.md)]:ssä.|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Myynnin integroinnin synkronointityöt

Työt suoritetaan seuraavassa järjestyksessä, jotta objektien välille ei muodostu yhdistämisen riippuvuussuhteita. Common Data Service -palvelussa on lisätöitä. Lisätietoja on kohdassa [Tehtävien aikatauluttaminen työjonojen avulla](/dynamics365/business-central/admin-job-queues-schedule-tasks).

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
|MITTAYKSIKKÖ – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in yksikköryhmät ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in mittayksiköt.|[!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|MITTAYKSIKKÖ|30|720<br> (12 tuntia)|
|RESURSSI-TUOTE – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteet ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in resurssit.|[!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|RESURSSI-TUOTE|30|720<br> (12 tuntia)|
|NIMIKE-TUOTE – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotteet ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in nimikkeet.|[!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|NIMIKE-TUOTE|30|1440<br> (24 tuntia)|
|ASIAKHNTRHM-HINTA – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in myyntihinnaston ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakashintaryhmät.| |ASIAKASHINTARYHMÄT-MYYNTIHINNASTOT|30|1440<br> (24 tuntia)|
|MYYNTIHNT-TUOTEHINTA – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in tuotehinnat ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyntihinnat.||TUOTEHINTA-MYYNTIHINTA|30|1440<br> (24 tuntia)|
|KIRJMNTILASKU-LASK – Dynamics 365 Salesin synkronointityö|Synkronoi [!INCLUDE[crm_md](includes/crm_md.md)]in laskut ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in kirjatut myyntilaskut.|[!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin|LASKUT-KIRJATUT MYYNTILASKUT|30|1440<br> (24 tuntia)|
|Asiakastilastot – Dynamics 365 Salesin synkronointityö|Päivittää [!INCLUDE[crm_md](includes/crm_md.md)]in tilit uusilla [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakastiedoilla. Nämä tiedot näkyvät [!INCLUDE[crm_md](includes/crm_md.md)]issa niiden tilien **Business Central -tilin tilastot** -pikanäkymälomakkeessa, jotka on yhdistetty [!INCLUDE[d365fin](includes/d365fin_md.md)]in asiakkaisiin.<br /><br /> Nämä tiedot voidaan päivittää myös manuaalisesti kustakin asiakastietueesta. Lisätietoja on kohdassa [Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Huomautus:** Tällä työjonotapahtumalla on merkitystä vain, jos [!INCLUDE[d365fin](includes/d365fin_md.md)] -integrointiratkaisu on asennettu [!INCLUDE[crm_md](includes/crm_md.md)]iin. |Ei sovellu|Ei sovellu|30|Ei sovellu| 

### <a name="note-for-on-premises-versions"></a>Huomautus paikallisia versioita varten

> [!Note]
> Jos yhdistät [!INCLUDE[d365fin](includes/d365fin_md.md)]in paikallisen version [!INCLUDE[crm_md](includes/crm_md.md)] ja haluat määrittää yhteyden [!INCLUDE[crm_md](includes/crm_md.md)] -ilmentymään tietyllä todennustyypillä, täytä **Todennustyypin tiedot** -pikavälilehden kentät. Lisätietoja on kohdassa [Yhteyden muodostaminen Dynamics 365:een XRM-työkalujen yhteysmerkkijonojen avulla](https://go.microsoft.com/fwlink/?linkid=843055). Tätä vaihetta tarvita yhdistettäessä [!INCLUDE[d365fin](includes/d365fin_md.md)]in online-versiota.

## <a name="see-also"></a>Katso myös

[[!INCLUDE[crm_md](includes/crm_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Yhteyden määrittäminen [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Business Centralin ja [!INCLUDE[crm_md](includes/crm_md.md)]in synkronointi](admin-synchronizing-business-central-and-sales.md)  
[Paikallisen Dynamics 365 Salesin integroinnin valmistelu](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
