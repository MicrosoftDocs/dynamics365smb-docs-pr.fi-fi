---
title: Common Data Service -sovelluksen käyttäminen
description: Johdanto Common Data Service -sovellukseen ja sen osiin.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: bb21647b4cd07d4d4e2d37ae597551d9ca50d210
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196851"
---
# <a name="integrating-with-common-data-service"></a>Integrointi Common Data Servicein kanssa
Yrityssovelluksissa käytetään usein tietoja useista lähteistä. [!INCLUDE[d365fin](includes/cds_long_md.md)] yhdistää tiedot yhdeksi loogiseksi joukoksi, jonka avulla on helppo muodostaa yhteys Dynamics 365 -sovelluksiin, kuten [!INCLUDE[crm_md](includes/crm_md.md)] -sovellukseen, tai omaan [!INCLUDE[d365fin](includes/cds_long_md.md)] -ratkaisun avulla luotuun sovellukseen [!INCLUDE[d365fin_md](includes/d365fin_md.md)]:ssä. Lisätietoja [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksesta on kohdassa [Mikä on Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

Seuraavat ohjeet käsittelevät [!INCLUDE[d365fin](includes/cds_long_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in integrointia.

> [!Note]  
> Näiden tehtävien suorittaminen vaatii **Järjestelmänvalvoja** käyttöoikeusroolin [!INCLUDE[d365fin](includes/cds_long_md.md)]ssa ja [!INCLUDE[d365fin](includes/d365fin_md.md)]ssa  

1. Määritä Microsoft 365:n hallintakeskuksessa käyttäjätili, jolla muodostetaan yhteys [!INCLUDE[d365fin](includes/cds_long_md.md)]iin ja synkronoidaan tietoja sen kanssa. Lisätietoja on kohdassa [Common Data Service -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).

2. Määritä [!INCLUDE[d365fin](includes/cds_long_md.md)]in käyttöoikeudet niille [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjille, jotka käyttävät integroituja sovelluksia.

3. Määritä [!INCLUDE[d365fin](includes/cds_long_md.md)] -yhteys. Lisätietoja on kohdassa [Yhteyden muodostaminen Common Data Service -sovellukseen](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Synkronoi tiedot sovellusten välillä. Lisätietoja on kohdassa [Business Centralin ja Common Data Servicein synkronointi](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-d365fin"></a>[!INCLUDE[d365fin](includes/cds_long_md.md)]in käytön aloittaminen
Jos haluat aloittaa [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksen käyttämisen, tarvitset Microsoft Power Apps -tilin. Jos sinulla ei vielä ole Power Apps -tiliä, saat ilmaisen tilin käymällä osoitteessa [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) ja valitsemalla **Aloita ilmaiseksi** -linkin. Lisätietoja [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksen aloittamisesta on [Integrointi Common Data Service -sovelluksen avulla](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) -moduulissa Microsoft Learnissa.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Kaksisuuntainen tai yksisuuntainen tietojen synkronointi
Liiketoiminnan tarpeista riippuen voit määrittää integroinnin synkronoimaan tiedot joko Dynamics 365 -liiketoimintasovelluksesta toiseen tai molempiin suuntiin reaaliaikaisesti [!INCLUDE[d365fin](includes/cds_long_md.md)]:n avulla. Jos integroit esimerkiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]:n [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen avulla [!INCLUDE[d365fin](includes/cds_long_md.md)]:n kautta, myyjä voi luoda myyntitilauksen [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa. Tilaus synkronoidaan [!INCLUDE[d365fin](includes/d365fin_md.md)]:een. Vastaavasti [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksessa myyjä voi tarkastella [!INCLUDE[d365fin](includes/d365fin_md.md)]:n tietoja tilauksen nimikkeen saatavuudesta. 

## <a name="standard-and-custom-entities"></a>Vakioentiteetit ja mukautetut entiteetit
[!INCLUDE[d365fin](includes/cds_long_md.md)] tallentaa tiedot turvallisesti entiteettijoukkoihin. Ne ovat samanlaisia joukkoja kuin taulukon tallentamat tiedot tietokannassa. [!INCLUDE[d365fin](includes/cds_long_md.md)] sisältää tavalliset skenaariot kattavien vakioentiteettien perusjoukon. Voit luoda myös organisaatiokohtaisia mukautettuja entiteettejä. [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssä voit tarkastella vakioentiteettejä ja mukautettuja entiteettejä, jotka synkronoidaan Integrointitaulukon yhdistämismääritykset -sivulla.

## <a name="about-the-base-cds-integration-solution"></a>Tietoja CDS-perusintegraatioratkaisusta
Perusintegraatioratkaisu on integroinnin avainosa. Ratkaisu lisää vaaditut roolit ja käyttöoikeustasot integroinnin käyttäjätileille ja luo entiteetit, jotka tarvitaan [!INCLUDE[d365fin](includes/d365fin_md.md)] -yrityksen yhdistämisessä liiketoimintayksikköön [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa. 

Oletusarvoisesti **[!INCLUDE[d365fin](includes/cds_long_md.md)] -yhteyden määrityksen** asetusten ohjattu määritysopas tuo ratkaisun. Tämän vuoksi asennusopas käyttää määrittämääsi järjestelmänvalvojan käyttäjätiliä. Tämän tilin on oltava hyväksytty [!INCLUDE[d365fin](includes/cds_long_md.md)]:n käyttäjä, jolla on seuraavat käyttöoikeusroolit:

* järjestelmänvalvoja  
* ratkaisun mukauttaja.  

Lisätietoja on kohdissa [[!INCLUDE[d365fin](includes/cds_long_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md) ja [Käyttäjien luominen Microsoft Dynamics 365 (online) -sovelluksessa ja käyttöoikeusroolien määrittäminen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles.md). 

Järjestelmänvalvojan tiliä käytetään vain kerran asennuksen aikana kokoonpanon muutosten takia, jotka CDS-perusratkaisu tekee [!INCLUDE[d365fin](includes/cds_long_md.md)]:ssä. Kun ratkaisu on tuotu, tiliä ei enää tarvita. Integrointi jatkaa integrointia varten luodun käyttäjätilin käyttämistä.

[!INCLUDE[d365fin](includes/cds_long_md.md)]:n mukauttamisen lisäksi ratkaisu luo integrointia varten myös seuraavat roolit [!INCLUDE[d365fin](includes/cds_long_md.md)]:ssä:

* **Integroinnin järjestelmänvalvoja** – Antaa käyttäjille mahdollisuuden [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[d365fin](includes/cds_long_md.md)]in välisen yhteyden hallintaan. Yleensä tämä määritetään synkronoinnin käyttäjätilille.  
* **Integroinnin käyttäjä** – Antaa käyttäjille mahdollisuuden käyttää synkronoituja tietoja. Yleensä tämä määritetään synkronoinnin käyttäjätilille ja sellaisille muille käyttäjille, joiden on tarkasteltava tai käytettävä synkronoituja tietoja.

Lisätietoja kustakin roolista, kuten käyttöoikeuksista ja käyttöoikeustasoista, on kohdassa [[!INCLUDE[d365fin](includes/cds_long_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).

Yhteyden muodostamisen aikana luodaan integrointitaulukon yhdistämismääritykset, joita tarvitaan tietojen synkronoimiseen. Common Data Servicen entiteetit yhdistetään taulukoihin ja taulukkokenttiin Business Centralissa integrointitaulukoiden kautta. Lisätietoja on kohdassa [Synkronoinnin vakioentiteettien yhdistämismääritys](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## <a name="see-also"></a>Katso myös
[Tietojen omistusmallit](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



