---
title: Microsoft Dataverse -integroinnissa käytettävien käyttäjätilien määrittäminen | Microsoft Docs
description: 'Tietoja niiden käyttäjätilien määrittämisestä, joilla sovellukset vaihtavat tietoja ja joiden avulla käytetään ja synkronoidaan sovellusten tietoja.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="setting-up-user-accounts-for-integrating-with-microsoft-dataverse-via-data-sync"></a>Microsoft Dataverse -integroinnissa käytettävien käyttäjätilien määrittäminen tietojen synkronoinnin avulla

Tässä artikkelissa on yleiskatsaus [!INCLUDE[prod_short](includes/cds_long_md.md)]in ja [!INCLUDE[prod_short](includes/prod_short.md)]in integroinnissa tarvittavien käyttäjätilien määrittämisestä.

## <a name="set-up-the-administrator-user-account"></a>Järjestelmänvalvojan käyttäjätilin määrittäminen

Jos haluat määrittää yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]- ja [!INCLUDE[prod_short](includes/cds_long_md.md)]-kohteiden välille, sinun on kirjauduttava sisään kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)] käyttäjätilillä, joka on määritetty [!INCLUDE[prod_short](includes/prod_short.md)] Essential- tai [!INCLUDE[prod_short](includes/prod_short.md)] Premium-käyttöoikeuteen. Käytämme tätä tiliä kerran asentaaksemme ja määrittääksemme joitakin tarvittavia komponentteja.

> [!IMPORTANT]
> Asennuksen aikana sinua pyydetään antamaan tunnistetiedot [!INCLUDE[prod_short](includes/cds_long_md.md)] -ympäristölle. Anna sellaisen tilin tunnistetiedot, jolla on käyttöoikeuden alainen käyttäjä ja jolle on määritetty **järjestelmänvalvojan** käyttöoikeus [!INCLUDE[prod_short](includes/cds_long_md.md)]-ympäristössä ja yleisen järjestelmänvalvojan suojausrooli ympäristössä, johon se kuuluu. Tämä tili ei tarvitse käyttöoikeutta [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan, koska sitä käytetään vain tehtävien määrittämiseen [!INCLUDE[prod_short](includes/cds_long_md.md)] -ympäristössä.
>
> Kun yhteyden määritys on tehty, voit poistaa [!INCLUDE[prod_short](includes/cds_long_md.md)] -käyttäjän. Integrointi jatkaa integrointia varten automaattisesti luodun käyttäjätilin käyttämistä.

## <a name="permissions-and-security-roles-for-user-accounts-in-"></a>[!INCLUDE[prod_short](includes/cds_long_md.md)] -sovelluksen käyttäjätilien käyttöoikeudet ja ja käyttöoikeusroolit

Perusintegraatioratkaisu luo seuraavat roolit [!INCLUDE[cds_long](includes/cds_long_md.md)] -ohjelmassa integrointia varten:

* **Integroinnin järjestelmänvalvoja**: Antaa käyttäjille mahdollisuuden [!INCLUDE[prod_short](includes/prod_short.md)]in ja [!INCLUDE[cds_long](includes/cds_long_md.md)]in välisen yhteyden hallintaan. Yleensä se määritetään vain automaattisesti luodulle synkronoinnin käyttäjätilille.
* **Integroinnin käyttäjä**: Antaa käyttäjille mahdollisuuden käyttää synkronoituja tietoja. Yleensä se määritään automaattisesti luodulle synkronoinnin käyttäjätilille ja sellaisille muille käyttäjille, joiden on tarkasteltava tai käytettävä synkronoituja tietoja.

> [!NOTE]
>
> **Integroinnin hallinta**- ja **Integrointikäyttäjä**-rooleja saa käyttää vain sovelluksen käyttäjä, joka suorittaa integroinnin. Sovelluksen käyttäjä ei tarvitse määritettyä [!INCLUDE[prod_short](includes/prod_short.md)]- tai [!INCLUDE[cds_long](includes/cds_long_md.md)]-lisenssiä.

Kun perusintegrointiratkaisua asennetaan, se määrittää integroinnin käyttäjätilin käyttöoikeudet. Jos näitä käyttöoikeuksia on muutettu manuaalisesti, ne voidaan palauttaa alkuperäisiksi. Valitse **Ota integraatioratkaisu uudelleen käyttöön** **Dataverse-yhteysmääritys**-sivulla asentaaksesi perusintegraatioratkaisun uudelleen. Tämä vaihe ottaa Business Centralin integroinnin käyttöoikeusroolin käyttöön.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### <a name="minimum-permissions-for-the-administrator"></a>Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### <a name="customization"></a>Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### <a name="custom-entities"></a>Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### <a name="minimum-permissions-for-automatically-created--integration-application-user"></a>Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### <a name="core-records"></a>Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### <a name="sales"></a>Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### <a name="service"></a>Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### <a name="business-management"></a>Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### <a name="customization-1"></a>Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### <a name="custom-entities-1"></a>Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### <a name="product-availability-user"></a>Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### <a name="custom-entities-2"></a>Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## <a name="see-also"></a>Katso myös

[Integrointi Microsoft Dataversein kanssa](admin-common-data-service.md)  
[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
