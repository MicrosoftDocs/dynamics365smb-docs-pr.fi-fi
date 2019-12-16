---
title: Dynamics 365 Sales -integrointi| Microsoft Docs
description: Tietoja Dynamics 365 Business Centralin valmistelusta Dynamics 365 Sales -integrointia varten.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 09edf4a84720085d0accb008b0ae29f47fa38f60
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808767"
---
# <a name="integrating-with-dynamics-365-sales"></a>Dynamics 365 Sales -integrointi
Myyjää pidetään usein liiketoiminnan eniten ulospäin suuntautuneena tehtävänä. Myyjien voisi kuitenkin olla hyödyllistä tarkastella liiketoimintaa myös sisäisesti, jotta he tiedostaisivat, mitä taustalla tapahtuu. [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in integroinnin ansiosta myyjät saavat merkityksellisiä tietoja, joiden avulla he voivat tarkastella [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja [!INCLUDE[crm_md](includes/crm_md.md)]ia käyttäessään. Myyntitarjousta valmistellessa voi esimerkiksi olla hyödyllistä tietää, riittääkö varasto tilauksen täyttämiseen. Lisätietoja on kohdassa [Dynamics 365 Salesin käyttäminen Business Centralissa](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Seuraavat ohjeet käsittelevät sovellusten [!INCLUDE[crm_md](includes/crm_md.md)] ja [!INCLUDE[d365fin](includes/d365fin_md.md)]verkkoversioiden integrointiprosessia. Lisätietoja paikallisesta määrityksestä on kohdassa [Paikallisen Dynamics 365 Salesin integroinnin valmistelu](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## <a name="overview-of-the-integration-process"></a>Integrointiprosessin yleiskatsaus
Seuraavat ohjeet käsittelevät [!INCLUDE[crm_md](includes/crm_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in integrointia.

> [!Note]  
> Näiden tehtävien suorittaminen vaatii **Järjestelmänvalvoja** käyttöoikeusroolin [!INCLUDE[crm_md](includes/crm_md.md)]ssa ja [!INCLUDE[d365fin](includes/d365fin_md.md)]ssa  

1. Määritä Microsoft 365:n hallintakeskuksessa käyttäjätili, jolla muodostetaan yhteys [!INCLUDE[crm_md](includes/crm_md.md)]iin ja synkronoidaan tietoja sen kanssa. Lisätietoja on kohdassa [Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).

2. Määritä [!INCLUDE[crm_md](includes/crm_md.md)]in käyttöoikeudet niille [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjille, jotka käyttävät integroituja sovelluksia.

3. Määritä [!INCLUDE[crm_md](includes/crm_md.md)] -yhteys. Lisätietoja on kohdassa [Dynamics 365 for Sales -yhteyden määrittäminen](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Valinnainen: [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in tietueiden yhdistäminen. Lisätietoja on kohdassa [Tietueiden yhdistäminen ja synkronoiminen manuaalisesti](admin-how-to-couple-and-synchronize-records-manually.md).

5. Synkronoi tiedot sovellusten välillä. Lisätietoja on kohdassa [Business Centralin ja Dynamics 365 Salesin synkronointi](admin-synchronizing-business-central-and-sales.md).  

## <a name="about-the-business-central-integration-solution"></a>Tietoja Business Central -integrointiratkaisusta
Ratkaisun avulla käyttäjät näkevän [!INCLUDE[d365fin](includes/d365fin_md.md)]in tiedot käyttäessään [!INCLUDE[crm_md](includes/crm_md.md)]ia. Tällä tavoin saadaan merkityksellisiä tietoja esimerkiksi asiakastilastoista sekä antaa käyttäjille mahdollisuuden yhdistää [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja [!INCLUDE[crm_md](includes/crm_md.md)]ista ja tarkistaa tuotteiden saatavuuden [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.

Asetusten ohjattu **Dynamics 365 Sales -yhteyden määritys** -opas tuo [!INCLUDE[d365fin](includes/d365fin_md.md)] -integrointiratkaisun. Tämän vuoksi asennusopas käyttää järjestelmänvalvojan käyttäjätiliä. Tämän tilin on lisäksi oltava hyväksytty [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjä, jolla on seuraavat käyttöoikeusroolit:

* järjestelmänvalvoja  
* ratkaisun mukauttaja.  

Lisätietoja on kohdissa [Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md), [Käyttäjien luominen Microsoft Dynamics 365 (online) -sovelluksessa ja käyttöoikeusroolien määrittäminen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) sekä [Käyttäjien ja ryhmien käyttöoikeuksien määrittäminen](ui-define-granular-permissions.md).  

Tätä tiliä käytetään vain kerran asennuksen aikana. Kun ratkaisu on tuotu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, tiliä ei enää tarvita. Integrointi jatkaa integrointia varten luodun käyttäjätilin käyttämistä.

[!INCLUDE[crm_md](includes/crm_md.md)]in mukauttamisen lisäksi [!INCLUDE[d365fin](includes/d365fin_md.md)] -integrointiratkaisu luo integrointia varten myös seuraavat roolit [!INCLUDE[crm_md](includes/crm_md.md)]issa:

* **Integroinnin järjestelmänvalvoja** – Antaa käyttäjille mahdollisuuden [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in välisen yhteyden hallintaan. Yleensä määritetään synkronoinnin käyttäjätilille.  
* **Integroinnin käyttäjä** – Antaa käyttäjille mahdollisuuden käyttää synkronoituja tietoja. Yleensä määritetään synkronoinnin käyttäjätilille ja sellaisille muille käyttäjille, joiden on tarkasteltava tai käytettävä synkronoituja tietoja.
* **Tuotteen saatavuuden käyttäjä** – antaa käyttäjille mahdollisuuden kysellä tuotteen saatavuutta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa [!INCLUDE[crm_md](includes/crm_md.md)]ista.

Lisätietoja kustakin roolista, kuten käyttöoikeuksista ja käyttöoikeustasoista, on kohdassa [Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).

[!INCLUDE[d365fin](includes/d365fin_md.md)] pyytää asennusoppaan lopuksi yhdistämään myyjät [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjiin. [!INCLUDE[crm_md](includes/crm_md.md)]in tietueille on yleensä määritetty omistaja (käyttäjä), ja synkronointi epäonnistuu, jos [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjää ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjää ei ole yhdistetty. Tämän voi tehdä myös myöhemmin käyttämällä **Yhdistä myyjät** -toimintoa **Microsoft Dynamics 365 -yhteyden määritys** -sivulla.

## <a name="see-also"></a>Katso myös  
[Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 Sales -yhteyden määrittäminen](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Business Centralin ja Dynamics 365 Salesin synkronointi](admin-synchronizing-business-central-and-sales.md)  
[Paikallisen Dynamics 365 Salesin integroinnin valmistelu](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
