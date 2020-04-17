---
title: Yhteyden muodostaminen Dynamics 365 Salesiin | Microsoft Docs
description: Voit integroida muita sovelluksia Business Centralin avulla Common Data Servicen kautta.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3375db0208d1a0275011f0efbfce4a13102c522e
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196637"
---
# <a name="connect-to-common-data-service"></a>Yhteyden muodostaminen Common Data Serviceen
Tässä ohjeaiheessa kuvataan, kuinka [!INCLUDE[d365fin](includes/d365fin_md.md)] ja [!INCLUDE[d365fin](includes/cds_long_md.md)] välille määritetään yhteys. Yleensä yritykset luovat yhteyden integroidakseen ja synkronoidakseen tietoja toisen Dynamics 365 -liiketoimintasovelluksen kanssa. Sovellus voi olla esimerkiksi [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Ennen aloittamista
Ennen yhteyden luomista tarvitaan seuraavat tiedot:  

* Sen [!INCLUDE[d365fin](includes/cds_long_md.md)] -ympäristön URL-osoite, johon haluat muodostaa yhteyden. Jos käytät **CDS-yhteyden määrityksen** asetusten ohjattua määritysopasta yhteyden luomiseen, ympäristöt löydetään. Sinun on kuitenkin annettava myös vuokraajan toisen ympäristön URL-osoite.  
* Vain integroinnissa käytettävän käyttäjätilin käyttäjänimi ja salasana. Tätä tiliä kutsutaan integroinnin käyttäjän tiliksi. 
* Sen tilin käyttäjätili ja salasana, jolla on järjestelmänvalvojan oikeudet [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa.  

> [!Note]
> Seuraavat vaiheet koskevat [!INCLUDE[d365fin](includes/d365fin_md.md)]in online-versiota.

## <a name="set-up-a-connection-to-d365fin"></a>Yhteyden määrittäminen [!INCLUDE[d365fin](includes/cds_long_md.md)]iin  
Jos todennustyyppi on jokin muu kuin Office 365 -todennus, voit määrittää [!INCLUDE[d365fin](includes/cds_long_md.md)] -yhteyden **CDS-yhteyden määritys** -sivulla. Office 365 -todennuksessa on suositeltavaa käyttää **CDS-yhteyden määrityksen** asetusten ohjattua määritysopasta. Opas auttaa määrittämään yhteyden nopeasti sekä määrittämään lisäominaisuudet, kuten tietueiden välisen yhdistämisen.  

### <a name="to-use-the-cds-connection-setup-assisted-setup-guide"></a>CDS-yhteyden määrityksen asetusten ohjatun määritysoppaan käyttäminen 
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys** ja valitse sitten liittyvä linkki.
2. Valitse **Määritä CDS-perusintegraation yhteys**, jos haluat käynnistää asetusten ohjatun määritysoppaan.
3. Täytä tarvittavat kentät.

> [!Note]
> **CDS-yhteyden määrityksen** asetusten ohjattu määritysopas liittää yleensä **integroinnin järjestelmänvalvojan** ja **integroinnin käyttäjän** käyttöoikeusroolit integroinnissa käytettävälle käyttäjätilille ja määrittää tilin käyttöoikeustilaksi **ei-vuorovaikutteinen**.

### <a name="to-create-or-maintain-the-connection-manually"></a>Yhteyden luominen tai ylläpitäminen manuaalisesti
Seuraavassa kerrotaan, miten yhteys määritetään manuaalisesti **CDS-yhteyden määritys** -sivulla. Tällä sivulla hallitaan myös integroinnin asetuksia.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **CDS-yhteyden määritys** ja valitse liittyvä linkki.
2. Anna seuraavat tiedot yhteyden muodostamiseen [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[d365fin](includes/cds_long_md.md)]iin.

|Kenttä|Kuvaus|
|-----|-----|
|**Ympäristön URL-osoite**|Jos [!INCLUDE[d365fin](includes/cds_long_md.md)]:ssä on omia ympäristöjä, ne löytyvät ohjatun määrityksen suorittamisen yhteydessä. Jos haluat muodostaa yhteyden toiseen ympäristöön eri vuokraajassa, voit syöttää ympäristön järjestelmänvalvojan tunnistetiedot. Ympäristö löytyy niiden avulla. |
|**Käyttäjänimi** ja **Salasana**|Integrointiin varatun käyttäjätilin tunnistetiedot. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/cds_long_md.md)] -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).|
|**Käytössä**|Aloita integroinnin käyttäminen. Jos et ota yhteyttä käyttöön nyt, yhteysasetukset tallennetaan. Käyttäjät eivät kuitenkaan voi käyttää [!INCLUDE[d365fin](includes/cds_long_md.md)]in tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Voit palata tälle sivulle myöhemmin ottamaan yhteyden käyttöön.  |

3. Valitse **Omistusmalli**-kentässä, haluatko [!INCLUDE[d365fin](includes/cds_long_md.md)]:n tiimientiteetin vai jonkin tietyn käyttäjän omistavan uudet tietueet. Jos valitset **Henkilö**-kohdan, sinun täytyy määrittää jokainen käyttäjä. Jos valitset **Tiimi**-kohdan oletusliiketoimintayksikkö BCI_Yritys näkyy **Yhdistetty liiketoimintayksikkö** -kentässä.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Jos haluat testata yhteysasetukset, valitse **Yhteys** ja valitse sitten **Testaa yhteys**.  

    > [!NOTE]  
    >  Jos tietojen salaus ei ole käytössä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, sinulta kysytään, haluatko ottaa sen käyttöön. Ota tietojen salaus käyttöön valitsemalla **Kyllä** ja määritä tarvittavat tiedot. Valitse muussa tapauksessa **Ei**. Voit ottaa tietojen salauksen käyttöön myöhemmin. Lisätietoja on kehittäjän ja IT-ammattilaisen ohjeen kohdassa [Tietojen salaus Dynamics 365 Business Centralissa](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data.md).  

5. Jos [!INCLUDE[d365fin](includes/cds_long_md.md)]in synkronointia ei ole määritetty, sinulta kysytään, haluatko käyttää oletussynkronointiasetuksia. Valitse **Kyllä** tai **Ei** sen mukaan, haluatko pitää [!INCLUDE[d365fin](includes/cds_long_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueet kohdistettuina.

> [!Note]
> Yhteyden muodostaminen [!INCLUDE[d365fin](includes/cds_long_md.md)]:een **CDS-yhteyden määritys** -sivun avulla voi edellyttää Integroinnin järjestelmänvalvoja- ja Integroinnin käyttäjä -käyttöoikeusroolien määrittämistä integroinnissa Dynamics 365 Salesissa. Lisätietoja on kohdassa [Käyttöoikeusroolin määrittäminen käyttäjälle](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user.md).

### <a name="to-disconnect-from-d365fin"></a>[!INCLUDE[d365fin](includes/cds_long_md.md)] -yhteyden katkaiseminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **CDS-yhteyden määritys** ja valitse liittyvä linkki.
2. Poista käytöstä **CDS-yhteyden määritys** -sivulla **Käytössä**-valitsin.  

## <a name="see-also"></a>Katso myös  
[Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md)  
