---
title: Integroinnin päivittäminen Dynamics 365 Salesissa
description: Tämä aihe opastaa siirtämään Dynamics 365 Business Centralin ja Dynamics 365 Salesin välisen integroinnin uusimpaan versioon.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Integroinnin päivittäminen Dynamics 365 Salesissa
[!INCLUDE[prod_short](includes/prod_short.md)] voidaan integroida [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun kanssa. Tämän vuoksi tietoja on helppo yhdistää ja synkronoida muiden Dynamics 365 -sovellusten, kuten [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen, tai jopa itse luotujen sovellusten kanssa. Jos integrointi tehdään ensimmäistä kertaa, on suositeltavaa tehdä se [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelun kanssa. Lisätietoja on kohdassa [Integroiminen Dataverse -palvelun kanssa](admin-common-data-service.md).

Jos integrointi [!INCLUDE[crm_md](includes/crm_md.md)]- ja [!INCLUDE[prod_short](includes/prod_short.md)] -ratkaisun välillä on jo tehty, voit jatkaa tietojen synkronointia asetuksen avulla. Jos päivität [!INCLUDE[prod_short](includes/prod_short.md)]:n tai poistat [!INCLUDE[crm_md](includes/crm_md.md)]-integroinnin käytöstä, voit ottaa sen uudelleen käyttöön muodostamalla yhteyden [!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksen avulla. 

> [!NOTE]
> Jos uudelleenyhdistämisessä käytetään [!INCLUDE[prod_short](includes/cds_long_md.md)] -palvelua, käyttöön otetaan synkronoinnin oletusasetukset ja käytössä olevat määritykset korvataan. Esimerkiksi taulukon oletusyhdistämismääritykset otetaan käyttöön.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Yhteyden päivittäminen niin, että se käyttää Dataverse -sovellusta
1. Avaa **Microsoft Dynamics 365 -yhteyden määritys** -sivu ja poista sitten **Käytössä**-valitsin käytöstä. Katkaise sitten yhteys [!INCLUDE[crm_md](includes/crm_md.md)]iin sulkemalla sivu.
2. Avaa **Dataverse-yhteyden asetukset** -sivu ja valitse sitten **Omistajuusmalli** -kentässä **Henkilö**. Valitse sitten **Käytössä**-valitsin ottaaksesi [!INCLUDE[prod_short](includes/cds_long_md.md)] -yhteyden käyttöön.
  
   > [!NOTE]
   > Kun olet ottanut yhteyden käyttöön, Business Centralin integrointiratkaisu otetaan käyttöön Dataversessa.
4. Valitse **Microsoft Dynamics 365 -yhteyden asetukset** -sivulla **Ota integraatioratkaisu uudelleen käyttöön** asentaaksesi Business Central -integraatioratkaisun uudelleen.
5. Ota käyttöön **Käytössä**-valitsin muodostaaksesi uudelleen yhteyden [!INCLUDE[crm_md](includes/crm_md.md)]iin.
  
   > [!NOTE]
   > Kun olet ottanut yhteyden käyttöön, Business Centralin integrointiratkaisu otetaan käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]ssa. Tämä mahdollistaa integroinnin [!INCLUDE[crm_md](includes/crm_md.md)]-kohtaisten taulukoiden kanssa. Näitä ovat esimerkiksi myyntitilaukset, tarjoukset ja laskut.
6. Valitse **Sales-yhteyden määritys** -sivulla **Käytä oletussynkronoinnin määritystä**, jos haluat käynnistää integrointitaulukon yhdistämismääritykset [!INCLUDE[crm_md](includes/crm_md.md)]-sovellusta varten.

   > [!IMPORTANT]
   > **Käytä oletussynkronoinnin määritystä** -toiminto kohdistaa integroinnin taulukon oletusyhdistämismääritykset. Kaikki mukautetut yhdistämismääritykset korvataan. Jos haluat säilyttää mukautetut yhdistämismääritykset, suosittelemme, että viet ne Exceliin tai pyydät lisätietoja Microsoftin kumppanilta muista tavoista säilyttää mukautetut yhdistämismääritykset.    

## <a name="see-also"></a>Katso myös
[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrointi Microsoft Dataversein kanssa](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
