---
title: Integroinnin päivittäminen Dynamics 365 Salesissa | Microsoft Docs
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
ms.openlocfilehash: 2a5f58ac904ea05f4410ac9e1b804df1cb01c609
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410666"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Integroinnin päivittäminen Dynamics 365 Salesissa
[!INCLUDE[d365fin](includes/d365fin_md.md)] voidaan integroida [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelun kanssa. Tämän vuoksi tietoja on helppo yhdistää ja synkronoida muiden Dynamics 365 -sovellusten, kuten [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen, tai jopa itse luotujen sovellusten kanssa. Jos integrointi tehdään ensimmäistä kertaa, on suositeltavaa tehdä se [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelun kanssa. Lisätietoja on kohdassa [Integroiminen Common Data Service -palvelun kanssa](admin-common-data-service.md).

Jos integrointi [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -ratkaisun välillä on jo tehty, voit jatkaa tietojen synkronointia asetuksen avulla. Jos päivität [!INCLUDE[d365fin](includes/d365fin_md.md)]:n tai poistat [!INCLUDE[crm_md](includes/crm_md.md)]-integroinnin käytöstä, voit ottaa sen uudelleen käyttöön muodostamalla yhteyden [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksen avulla. 

> [!NOTE]
> Jos uudelleenyhdistämisessä käytetään [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelua, käyttöön otetaan synkronoinnin oletusasetukset ja käytössä olevat määritykset korvataan. Esimerkiksi taulukon oletusyhdistämismääritykset otetaan käyttöön.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Yhteyden päivittäminen niin, että se käyttää Common Data Service -sovellusta
1. Avaa **Microsoft Dynamics 365 -yhteyden määritys** -sivu, valitse **Ota käyttöön** -valitsin ja poista käytöstä olemassa oleva [!INCLUDE[crm_md](includes/crm_md.md)]-yhteys.
2. Avaa **Common Data Service -yhteyden määritys** -sivu ja valitse **Ota käyttöön** -valitsin, jos haluat ottaa yhteyden käyttöön.
  
   Kun olet ottanut CDS-yhteyden käyttöön, Business Centralin CDS-perusintegrointiratkaisu otetaan käyttöön Common Data Service -sovelluksessa.
3. Poista Microsoft Dynamics 365 Business Central -integraatioratkaisun asennus Dynamics 365 Salesista seuraavan ohjeen mukaisesti [Ratkaisun aiheen asennuksen poistaminen tai poistaminen](/powerapps/developer/common-data-service/uninstall-delete-solution) 

4. Valitse Microsoft Dynamics 365 -yhteyden määritys -sivulla Ota käyttöön -valitsin, jos haluat ottaa käyttöön [!INCLUDE[crm_md](includes/crm_md.md)]-yhteyden.
  
   Kun olet ottanut Sales-yhteyden käyttöön, Business Centralin integrointiratkaisu otetaan käyttöön Salesissa. Tämä mahdollistaa integroinnin [!INCLUDE[crm_md](includes/crm_md.md)]-kohtaisten entiteettien kanssa. Näitä ovat esimerkiksi myyntitilaukset, tarjoukset ja laskut.
5. Valitse **Ota integraatioratkaisu uudelleen käyttöön**, jos haluat asentaa ja määrittää päivitetyn Business Centralin integrointiratkaisun.
6. Valitse **Sales-yhteyden määritys** -sivulla **Käytä oletussynkronoinnin määritystä**, jos haluat käynnistää integrointitaulukon yhdistämismääritykset [!INCLUDE[crm_md](includes/crm_md.md)]-sovellusta varten.

## <a name="see-also"></a>Katso myös
[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrointi Common Data Servicein kanssa](admin-common-data-service.md)
