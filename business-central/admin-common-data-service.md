---
title: Microsoft Dataverse -sovelluksen käyttäminen
description: Johdatus siihen, miten Microsoft Dataversen ja sen komponentit voi integroida ja miten niitä voi käyttää yhteyden muodostamiseksi muihin Dynamics 365 -sovelluksiin.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.date: 06/14/2021
ms.openlocfilehash: 95b1146f2f664ad73966162e24c3e0ad0c34e310
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141435"
---
# <a name="integrating-with-microsoft-dataverse"></a>Integrointi Microsoft Dataversein kanssa


Yrityssovelluksissa käytetään usein tietoja useista lähteistä. [!INCLUDE[prod_short](includes/cds_long_md.md)] yhdistää tiedot yhdeksi loogiseksi joukoksi, jonka avulla on helppo muodostaa yhteys Dynamics 365 -sovelluksiin, kuten [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukseen, tai omaan [!INCLUDE[prod_short](includes/cds_long_md.md)] -ratkaisun avulla luotuun sovellukseen [!INCLUDE[prod_short_md](includes/prod_short.md)]:ssä. Lisätietoja [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksesta on kohdassa [Mikä on Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)

Seuraavat ohjeet käsittelevät [!INCLUDE[prod_short](includes/cds_long_md.md)]in ja [!INCLUDE[prod_short](includes/prod_short.md)]in integrointia.

> [!Note]  
> Näiden tehtävien suorittaminen vaatii **Järjestelmänvalvoja** käyttöoikeusroolin [!INCLUDE[prod_short](includes/cds_long_md.md)]ssa ja [!INCLUDE[prod_short](includes/prod_short.md)]ssa  

1. Määritä [!INCLUDE[prod_short](includes/cds_long_md.md)]in käyttöoikeudet niille [!INCLUDE[prod_short](includes/prod_short.md)]in käyttäjille, jotka käyttävät integroituja sovelluksia.

2. Määritä [!INCLUDE[prod_short](includes/cds_long_md.md)] -yhteys. Lisätietoja on kohdassa [Yhteyden muodostaminen Dataverse -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkronoi tiedot sovellusten välillä. Lisätietoja on kohdassa [Business Centralin ja Dataversein synkronointi](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-prod_short"></a>[!INCLUDE[prod_short](includes/cds_long_md.md)]in käytön aloittaminen
Jos haluat aloittaa [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksen käyttämisen, tarvitset Microsoft Power Apps -tilin. Jos sinulla ei vielä ole Power Apps -tiliä, saat ilmaisen tilin käymällä osoitteessa [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) ja valitsemalla **Aloita ilmaiseksi** -linkin. Lisätietoja [!INCLUDE[prod_short](includes/cds_long_md.md)]n käytön aloittamisesta on [Dataversen käytön aloittaminen](/learn/modules/get-started-with-powerapps-common-data-service/) -moduulissa Microsoft Learnissa.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Kaksisuuntainen tai yksisuuntainen tietojen synkronointi
Liiketoiminnan tarpeista riippuen voit määrittää integroinnin synkronoimaan tiedot joko Dynamics 365 -liiketoimintasovelluksesta toiseen tai molempiin suuntiin reaaliaikaisesti [!INCLUDE[prod_short](includes/cds_long_md.md)]:n avulla. Jos integroit esimerkiksi [!INCLUDE[prod_short](includes/prod_short.md)]:n [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen avulla [!INCLUDE[prod_short](includes/cds_long_md.md)]:n kautta, myyjä voi luoda myyntitilauksen [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa. Tilaus synkronoidaan [!INCLUDE[prod_short](includes/prod_short.md)]:een. Vastaavasti [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa myyjä voi tarkastella [!INCLUDE[prod_short](includes/prod_short.md)]:n tietoja tilauksen nimikkeen saatavuudesta. 

## <a name="standard-and-custom-entities"></a>Vakioentiteetit ja mukautetut entiteetit
[!INCLUDE[prod_short](includes/cds_long_md.md)] tallentaa tiedot turvallisesti taulukkojoukkoihin. Ne ovat samanlaisia joukkoja kuin taulukon tallentamat tiedot tietokannassa. [!INCLUDE[prod_short](includes/cds_long_md.md)] sisältää tavalliset skenaariot kattavien vakiotaulukoiden perusjoukon. Voit luoda myös organisaatiokohtaisia mukautettuja taulukoita. [!INCLUDE[prod_short](includes/prod_short.md)]:ssä voit tarkastella vakiotaulukoita ja mukautettuja taulukoita, jotka synkronoidaan Integrointitaulukon yhdistämismääritykset -sivulla.

## <a name="about-the-business-central-base-integration-solution"></a>Tietoja Business Central -perusintegrointiratkaisusta

Perusintegraatioratkaisu on integroinnin avainosa. Ratkaisu lisää vaaditut roolit ja käyttöoikeustasot integroinnin käyttäjätileille ja luo taulukot, jotka tarvitaan [!INCLUDE[prod_short](includes/prod_short.md)] -yrityksen yhdistämisessä liiketoimintayksikköön [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksessa. 

Oletusarvoisesti **[!INCLUDE[prod_short](includes/cds_long_md.md)] -yhteyden määrityksen** asetusten ohjattu määritysopas tuo ratkaisun. Tämän vuoksi asennusopas käyttää määrittämääsi järjestelmänvalvojan käyttäjätiliä. Tämän tilin on oltava [!INCLUDE[prod_short](includes/cds_long_md.md)]n hyväksytty käyttäjä, jolla on seuraava käyttöoikeusrooli:

* järjestelmänvalvoja  

Lisätietoja on kohdissa [[!INCLUDE[prod_short](includes/cds_long_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md) ja [Käyttäjien luominen Microsoft Dynamics 365 (online) -sovelluksessa ja käyttöoikeusroolien määrittäminen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Järjestelmänvalvojan tiliä käytetään vain kerran asennuksen aikana kokoonpanon muutosten takia, jotka perusintegrointiratkaisu tekee [!INCLUDE[prod_short](includes/cds_long_md.md)]ssa. Kun ratkaisu on tuotu, tiliä ei enää tarvita. Integrointi jatkaa integrointia varten automaattisesti luodun käyttäjätilin käyttämistä.

[!INCLUDE[prod_short](includes/cds_long_md.md)]:n mukauttamisen lisäksi ratkaisu luo integrointia varten myös seuraavat roolit [!INCLUDE[prod_short](includes/cds_long_md.md)]:ssä:

* **Integroinnin järjestelmänvalvoja** – Antaa käyttäjille mahdollisuuden [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[prod_short](includes/cds_long_md.md)]in välisen yhteyden hallintaan. Yleensä se määritetään vain automaattisesti luodulle synkronoinnin käyttäjätilille.  
* **Integroinnin käyttäjä** – Antaa käyttäjille mahdollisuuden käyttää synkronoituja tietoja. Yleensä se määritään automaattisesti luodulle synkronoinnin käyttäjätilille ja sellaisille muille käyttäjille, joiden on tarkasteltava tai käytettävä synkronoituja tietoja.

Lisätietoja kustakin roolista, kuten käyttöoikeuksista ja käyttöoikeustasoista, on kohdassa [[!INCLUDE[prod_short](includes/cds_long_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).

Yhteyden muodostamisen aikana luodaan integrointitaulukon yhdistämismääritykset, joita tarvitaan tietojen synkronoimiseen. [!INCLUDE[prod_short](includes/cds_long_md.md)]n entiteetit yhdistetään taulukoihin ja taulukkokenttiin Business Centralissa integrointitaulukoiden kautta. Lisätietoja on kohdassa [Synkronoinnin vakioentiteettien yhdistämismääritys](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="see-also"></a>Katso myös
[Tietojen omistusmallit](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->





[!INCLUDE[footer-include](includes/footer-banner.md)]