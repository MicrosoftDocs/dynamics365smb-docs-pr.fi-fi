---
title: Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen | Microsoft Docs
description: Tietoja niiden käyttäjätilien määrittämisestä, joilla sovellukset vaihtavat tietoja ja joiden avulla käytetään ja synkronoidaan sovellusten tietoja.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: a876df301476cb6b4af335e8ee957de26865cbaa
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307826"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-sales"></a>Dynamics 365 Sales -integroinnissa käytettävien käyttäjätilien määrittäminen
Tässä artikkelissa on yleiskatsaus [!INCLUDE[crm_md](includes/crm_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in integroinnissa tarvittavien käyttäjätilien määrittämisestä.  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-administrator-user-account-in-sales"></a>Järjestelmänvalvojan käyttäjätilin määrittäminen Salesissa
[!INCLUDE[d365fin](includes/d365fin_md.md)]in järjestelmänvalvojan käyttäjätili on lisättävä ensin käyttäjänä [!INCLUDE[crm_md](includes/crm_md.md)]iin ja siirrettävä käyttäjä sitten [!INCLUDE[crm_md](includes/crm_md.md)]in järjestelmänvalvojaksi. Järjestelmänvalvojan käyttäjätilillä on oltava [!INCLUDE[crm_md](includes/crm_md.md)]issa myös järjestelmän mukauttajan rooli ja ainakin yksi ei-hallinnollinen käyttäjärooli, kuten myyntipäällikkö.

## <a name="setting-up-the-user-account-for-the-integration"></a>Käyttäjätilin määrittäminen integrointia varten
Office 365 -tilauksessa on luotava erillinen käyttäjätili, jota sekä [!INCLUDE[d365fin](includes/d365fin_md.md)] että [!INCLUDE[crm_md](includes/crm_md.md)] voi käyttää tietojen synkronoimiseen. Käyttäjätilin tulee voida kirjautua [!INCLUDE[crm_md](includes/crm_md.md)]iin, mikä tarkoittaa sitä, että tällä käyttäjällä tulee olla [!INCLUDE[crm_md](includes/crm_md.md)] lisenssi ja vähintään yksi käyttäjäoikeusrooli määritettynä [!INCLUDE[crm_md](includes/crm_md.md)]ssa, kuten [tässä kuvataan](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). Lisätietoja käyttäjien luomisesta [!INCLUDE[crm_md](includes/crm_md.md)]issa on kohdassa [Tietoturvan, käyttäjien ja tiimien hallinta](http://go.microsoft.com/fwlink/?LinkID=616518). Kun yhteys on määritetty, [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää käyttäjätilin käyttöoikeusroolit, joita se tarvitsee [!INCLUDE[d365fin](includes/d365fin_md.md)]ssa ja tämän tilin voi määrittää [epäinteraktiiviseen käyttötilaan](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) [!INCLUDE[crm_md](includes/crm_md.md)]ssä.

![Asetusten ohjattu määritys osoittaa paikan, johon synkronoinnin käyttäjätiedot annetaan](media/sync-user-setup.png "Visualisointina asetusten ohjattu määrityssivu osoittaa paikan, johon synkronoinnin käyttäjätiedot annetaan")

> [!IMPORTANT]  
> Älä käytä [!INCLUDE[crm_md](includes/crm_md.md)]in järjestelmänvalvojan tiliä synkronointiin, sillä se katkaisee synkronoinnin.
> Jotta synkronointi ei olisi jatkuvaa, integroinnin käyttäjätilin tietoihin tekemiä muutoksia ei myöskään synkronoida. <!--What changes would this account make?--> Kun yhteys on muodostettu, on suositeltavaa määrittää integroinnin käyttäjätilin käyttöoikeus [!INCLUDE[crm_md](includes/crm_md.md)]issa ei-vuorovaikutteiseen tilaan. Lisätietoja on kohdassa [Ei-vuorovaikutteisen käyttäjätilin luominen](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-sales-people"></a>Myyjien tilien määrittäminen
[!INCLUDE[crm_md](includes/crm_md.md)]issa on luotava käyttäjätilit [!INCLUDE[d365fin](includes/d365fin_md.md)]in myyjille. Tämän helpottamiseksi Microsoft 365:n hallintakeskuksessa on Excel-malli, jota voit käyttää. Valitse **Aktiiviset käyttäjät** -sivulla ensin **Lisää** ja sitten **Tuo useita käyttäjiä**. Valitse **Lataa vain otsikot sisältävä CSV-tiedosto** ja anna myyjien tiedot. Jos haluat nähdä esimerkin, valitse **Lataa otsikot sisältävä CSV-tiedosto ja esimerkkikäyttäjätiedot**. Kun olet antanut käyttäjien tiedot, tuontiprosessin seuraava vaihe on määrittää käyttäjien käyttöoikeudet Dynamics 365 Customer Engagement -palvelupakettiin.  

Kun olet tuonut käyttäjät ja määrittänyt heille Dynamics 365 Customer Engagementin käyttöoikeudet, sinun on määritettävä käyttäjille **myyjän** rooli [!INCLUDE[crm_md](includes/crm_md.md)]issa.

![Myyjien yhdistäminen käyttäjiin Dynamics 365 Salesissa](media/couple-salespeople.png "Visualisointina myyjien yhdistäminen käyttäjiin Dynamics 365 Salesissa")

## <a name="minimum-permissions-for-user-accounts-in-includecrm_mdincludescrm_mdmd"></a>Sovelluksen [!INCLUDE[crm_md](includes/crm_md.md)] käyttäjätilien vähimmäiskäyttöoikeusvaatimukset
Kun integrointiratkaisua asennetaan, integroinnin käyttäjätilin käyttöoikeudet määritetään sovelluksessa [!INCLUDE[crm_md](includes/crm_md.md)]. Jos näitä käyttöoikeuksia on muutettu, käyttöoikeudet on ehkä palautettava alkuperäisiksi. Tämä tehdään asentamalla integrointiratkaisu uudelleen tai määrittämällä käyttöoikeudet uudelleen manuaalisesti. Seuraavassa taulukossa ovat sovelluksen [!INCLUDE[crm_md](includes/crm_md.md)] käyttäjätilien vähimmäiskäyttöoikeudet.

### <a name="integration-administrator"></a>Integroinnin järjestelmänvalvoja
Seuraavan taulukon välilehdissä ovat kunkin käyttöoikeusroolin vähimmäiskäyttöoikeudet, jotka järjestelmänvalvojakäyttäjältä vaaditaan.

##### <a name="customization"></a>Mukauttaminen
|Käyttöoikeusrooli|Käyttöoikeustaso|Dynamics NAV 2018 ja aiemmat versiot|Business Central <br> Lokakuu 2018|Business Central <br> Huhtikuu 2019|
|----|----|-----|----|----|
|Malliin perustuva sovellus|Yleinen|||Lue|
|Laajennuksen kokoonpano|Yleinen|Lue|Lue|Lue|
|Laajennuksen tyyppi|Yleinen|Lue|Lue|Lue|
|Suhde|Yleinen|||Lue|
|SDK-viesti|Yleinen|Lue|Lue|Lue|
|SDK-viestin käsittelyvaihe|Yleinen|Lue|Lue|Lue|
|SDK-viestin käsittelyvaiheen kuva|Yleinen|Lue|Lue|Lue|
|Lähtöjärjestelmä|Yleinen|||Kirjoita|

##### <a name="custom-entities"></a>Mukautetut entiteetit
|Käyttöoikeusrooli|Käyttöoikeustaso|Dynamics NAV 2018 ja aiemmat versiot|Business Central <br> Lokakuu 2018|Business Central <br> Huhtikuu 2019|
|----|----|-----|----|----|
|Business Central -tilin tilastot|Yleinen|Lue|Lue|Lue|
|Business Central -yhteys|Yleinen|Luo, Lue, Kirjoita, Poista|Luo, Lue, Kirjoita, Poista|Luo, Lue, Kirjoita, Poista|
|Kirjaa määritys|Yleinen|||Kirjoita|

#### <a name="integration-user"></a>Integroinnin käyttäjä
Seuraavan taulukon välilehdissä ovat kunkin käyttöoikeusroolin vähimmäiskäyttöoikeudet, jotka integroinnin käyttäjältä vaaditaan.

##### <a name="core-records"></a>Tärkeimmät tietueet
|Käyttöoikeusrooli|Käyttöoikeustaso|Dynamics NAV 2018 ja aiemmat versiot|Business Central <br> Lokakuu 2018|Business Central <br> Huhtikuu 2019|
|----|----|-----|----|----|
|Tili|Yleinen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen, Määritä|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen, Määritä|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen, Määritä|
|Toimintokortti|Yleinen||Lue|Lue|
|Yhteys|Yleinen|Lue|Lue|Lue|
|Kontakti|Yleinen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|
|Huomautus|Yleinen|||Luo, Lue, Kirjoita, Poista, Liitä, Määritä|
|Mahdollisuus|Yleinen||Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|
|Kirjaus|Yleinen|||Luo, Lue, Liitä kohteeseen|
|Käyttäjän entiteetin käyttöliittymä|Käyttäjä|Luo, Lue, Kirjoita|Luo, Lue, Kirjoita|Luo, Lue, Kirjoita|

##### <a name="sales"></a>Myynti
|Käyttöoikeusrooli|Käyttöoikeustaso|Dynamics NAV 2018 ja aiemmat versiot|Business Central <br> Lokakuu 2018|Business Central <br> Huhtikuu 2019|
|----|----|-----|----|----|
|Lasku|Yleinen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|
|Tilaus|Yleinen|Lue, Kirjoita, Liitä kohteeseen|Lue, Kirjoita, Liitä kohteeseen|Lue, Kirjoita, Liitä, Liitä kohteeseen, Määritä|
|Tuote|Yleinen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|
|Ominaisuus|Yleinen|Lue|Lue|Lue|
|Ominaisuuden liitos|Yleinen|Lue|Lue|Lue|
|Ominaisuuden asetuksen määritetty nimike|Yleinen|Lue|Lue|Lue|
|Tarjous|Yleinen|Lue|Lue|Lue|

##### <a name="service"></a>Palvelu
|Käyttöoikeusrooli|Käyttöoikeustaso|Dynamics NAV 2018 ja aiemmat versiot|Business Central <br> Lokakuu 2018|Business Central <br> Huhtikuu 2019|
|----|----|-----|----|----|
|Palvelupyyntö|Yleinen|Lue|Lue|Lue|

##### <a name="business-management"></a>Liiketoiminnan hallinta
|Käyttöoikeusrooli|Käyttöoikeustaso|Dynamics NAV 2018 ja aiemmat versiot|Business Central <br> Lokakuu 2018|Business Central <br> Huhtikuu 2019|
|----|----|-----|----|----|
|Valuutta|Yleinen|Luo, Lue, Kirjoita|Luo, Lue, Kirjoita|Luo, Lue, Kirjoita|
|Organisaatio|Yleinen|Lue, Kirjoita|Lue, Kirjoita|Lue, Kirjoita|
|Käyttöoikeusrooli|Yleinen|||Lue|
|Käyttäjä|Yleinen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä, Liitä kohteeseen|
|Käyttäjän asetukset|Yleinen|Luo, Lue, Kirjoita, Poista, Liitä kohteeseen|Luo, Lue, Kirjoita, Poista, Liitä kohteeseen|Luo, Lue, Kirjoita, Poista, Liitä kohteeseen|
|Toimi toisen käyttäjän puolesta|Yleinen|Kyllä|Kyllä|Kyllä|

##### <a name="customization"></a>Mukauttaminen
|Käyttöoikeusrooli|Käyttöoikeustaso|Dynamics NAV 2018 ja aiemmat versiot|Business Central <br> Lokakuu 2018|Business Central <br> Huhtikuu 2019|
|----|----|-----|----|----|
|Kenttä|Yleinen||Lue|Lue|
|Laajennuksen kokoonpano|Yleinen|Lue|Lue|Lue|
|Laajennuksen tyyppi|Yleinen|Lue|Lue|Lue|
|SDK-viesti|Yleinen|Lue|Lue|Lue|
|SDK-viestin käsittelyvaihe|Yleinen|Lue|Lue|Lue|
|Verkkoresurssi|Yleinen|Lue|Lue|Lue|

##### <a name="custom-entities"></a>Mukautetut entiteetit
|Käyttöoikeusrooli|Käyttöoikeustaso|Dynamics NAV 2018 ja aiemmat versiot|Business Central <br> Lokakuu 2018|Business Central <br> Huhtikuu 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central -tilin tilastot|Yleinen|Luo, Lue, Kirjoita, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä kohteeseen|
|Dynamics 365 Business Central -yhteys|Yleinen|Lue|Lue|Lue|

### <a name="product-availability-user"></a>Tuotteen saatavuuden käyttäjä
Voit antaa myyjille mahdollisuuden tarkastella myynnissä olevien nimikkeiden varastotasoja, kun myönnät heille seuraavassa taulukossa mainitut käyttöoikeudet.

##### <a name="custom-entities"></a>Mukautetut entiteetit
|Käyttöoikeusrooli|Käyttöoikeustaso|Dynamics NAV 2018 ja aiemmat versiot|Business Central <br> Lokakuu 2018|Business Central <br> Huhtikuu 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central -tilin tilastot|Yleinen|Luo, Lue, Kirjoita, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä kohteeseen|Luo, Lue, Kirjoita, Liitä kohteeseen|
|Dynamics 365 Business Central -yhteys|Yleinen|Lue|Lue|Lue|

## <a name="see-also"></a>Katso myös  
[Dynamics 365 Sales -integrointi](admin-prepare-dynamics-365-for-sales-for-integration.md)  
