---
title: Yhteyden muodostaminen Dynamics 365 for Salesiin | Microsoft Docs
description: Dynamics 365 for Sales -integrointi on mahdollista.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 28ce599b2067faa904f917f8fce7390202c98d7b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245755"
---
# <a name="set-up-a-connection-to-dynamics-365-for-sales"></a>Yhteyden määrittäminen Dynamics 365 for Salesiin
[!INCLUDE[crm_md](includes/crm_md.md)] -integraatiota varten on määritettävä yhteys [!INCLUDE[d365fin](includes/d365fin_md.md)]in ja [!INCLUDE[crm_md](includes/crm_md.md)]in välille. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## <a name="before-you-start"></a>Ennen aloittamista
Seuraavat tiedot kannattaa olla käsillä ennen sovellusten yhdistämistä:  

* [!INCLUDE[crm_md](includes/crm_md.md)] -sovelluksen URL-osoite. URL-osoitteen löytää nopeasti avaamalla [!INCLUDE[crm_md](includes/crm_md.md)]in, kopioimalla URL-osoitteen ja liittämällä sen sitten [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Dynamics 365 for Sales -URL-osoite** -kenttään. [!INCLUDE[d365fin](includes/d365fin_md.md)] korjaa muotoilun puolestasi.  
* Vain integroinnissa käytettävän käyttäjätilin käyttäjänimi ja salasana.  
* Sen tilin käyttäjänimi ja salasana, jolla on järjestelmänvalvojan oikeudet.  
  
> [!Note]
> Seuraavat vaiheet koskevat [!INCLUDE[d365fin](includes/d365fin_md.md)]in online-versiota.

## <a name="set-up-test-and-enable-a-connection-to-includecrmmdincludescrmmdmd"></a>[!INCLUDE[crm_md](includes/crm_md.md)] -yhteyden määrittäminen, testaaminen ja käyttöönotto  
Office 365 -todennustyyppiä lukuun ottamatta Dynamics 365 for Sales -yhteys määritetään kaikissa todennustyypeissä **Microsoft Dynamics 365 for Sales -yhteyden määritys** -sivulla. Office 365 -todennuksessa voi käyttää myös ohjattua **Dynamics 365 for Sales -yhteyden määritys** -opasta, joka sisältää tarvittavat tiedot.

### <a name="to-use-an-assisted-setup-guide"></a>Asetusten ohjatun määrityksen käyttäminen
Asetusten ohjattu **Dynamics 365 for Sales -yhteyden määritys** -opas auttaa määrittämään yhteyden. Lisäksi se määrittää, otetaanko lisäominaisuudet, kuten tietueiden välinen yhdistäminen, käyttöön. 

1. Valitse ensin **Asennus ja laajennukset** ja valitse sitten **Asetusten ohjattu määritys**.
2. Käynnistä asetusten ohjattu määritys valitsemalla **Dynamics 365 for Sales -yhteyden määritys**.
3. Täytä tarvittavat kentät.
4. Käytössä on myös valinnaisia lisäasetuksia, jotka parantavat suojausta ja ottavat käyttöön [!INCLUDE[crm_md](includes/crm_md.md)]in lisäominaisuuksia, kuten myyntitilauksen käsittelyn varastomäärien tarkastelun. Lisäasetuksia käsitellään seuraavassa taulukossa.  

|Kenttä|Kuvaus|
|-----|-----|
|**Tuo Dynamics 365 for Sales -ratkaisu**|Ottamalla tämän asteuksen käyttöön voit asentaa ja määrittää integrointiratkaisun [!INCLUDE[crm_md](includes/crm_md.md)]issa. Lisätietoja on kohdassa [Tietoja Business Central -integraatioratkaisusta](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|
|**Julkaise Nimikkeen saatavuus -verkkopalvelu**|Antaa [!INCLUDE[crm_md](includes/crm_md.md)]ia käyttäville henkilöille mahdollisuuden tarkastella nimikkeiden (tuotteiden) varastosaatavuutta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Tämä varten tarvitaan [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjätili, jolla on verkkopalvelun käyttöoikeusavain. Avaimen määrittäminen on kaksivaiheinen prosessi. Valitse [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätilillä **Muuta verkkopalvelun käyttöoikeusavainta** -toiminto. Määritä sitten asetusten ohjatussa Dynamics 365 for Sales -yhteyden määrityksessä Dynamics 365 Business Centralin OData-verkkopalvelun URL-osoite ja anna palvelun käyttöön tarvittavat [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjän tunnistetiedot. Lisätietoja on kohdassa [OData-verkkopalvelut](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**Dynamics 365 Business Centralin OData-verkkopalvelun URL-osoite**|Jos otat Nimikkeen saatavuus -verkkopalvelun käyttöön, saat OData-verkkopalvelun URL-osoitteen.|
|**Dynamics 365 Business Centralin OData-verkkopalvelun käyttäjätunnus**|Sen [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjätilin nimi, jolla [!INCLUDE[crm_md](includes/crm_md.md)] noutaa tietoja nimikkeen saatavuudesta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa OData-verkkopalvelun kautta.|
|**Dynamics 365 Business Centralin OData-verkkopalvelun käyttöoikeusavain**|Sen käyttäjätilin käyttöoikeusavain, jolla [!INCLUDE[crm_md](includes/crm_md.md)] hakee tietoja nimikkeen saatavuudesta [!INCLUDE[d365fin](includes/d365fin_md.md)]ista OData-verkkopalvelun kautta. Avain on määritetty käyttäjälle, joka on valittu **Dynamics 365 Business Centralin OData-verkkopalvelun käyttäjätunnus** -kentässä. Voit hakea avaimen valitsemalla ensin käyttäjänimen vieressä **Hae arvo** -painikkeen ja sitten käyttäjän. Valitse seuraavaksi **Hallitse** ja lopuksi **Muokkaa**. Valitse käyttäjän kortissa ensin **Toiminnot**, **Tarkistus** ja sitten **Muuta verkkopalvelun käyttöoikeusavainta**.|
|**Ota käyttöön myyntitilauksen integrointi**|Kopioi [!INCLUDE[crm_md](includes/crm_md.md)]issa luodut myyntitilaukset [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Tätä varten on annettava järjestelmänvalvojan käyttäjätilin tunnistetiedot [!INCLUDE[crm_md](includes/crm_md.md)]issa. Lisätietoja on kohdassa [Myyntitilauksen tietojen käsitteleminen](marketing-integrate-dynamicscrm.md#handling-sales-order-data)|
|**Ota käyttöön Dynamics 365 for Sales -yhteys**|Ota [!INCLUDE[crm_md](includes/crm_md.md)] -yhteys käyttöön.|
|**Dynamics 365 SDK -versio**|Tällä on merkitystä vain, jos integrointi tehdään [!INCLUDE[crm_md](includes/crm_md.md)]in paikalliseen versioon. Voit yhdistää tällä Dynamics 365 SDK -versiolla (joka tunnetaan myös nimellä Xrm) [!INCLUDE[d365fin](includes/d365fin_md.md)]in [!INCLUDE[crm_md](includes/crm_md.md)]iin. Version on oltava yhteensopiva sen SDK-version kanssa, jota [!INCLUDE[crm_md](includes/crm_md.md)] käyttää. Lisäksi sen on oltava sama tai uudempi kuin versio, jota [!INCLUDE[crm_md](includes/crm_md.md)] käyttää.|

### <a name="to-create-or-maintain-the-connection-manually"></a>Yhteyden luominen tai ylläpitäminen manuaalisesti
Seuraavaksi käsitellään **Microsoft Dynamics 365 for Sales -yhteyden määritys** -sivun kenttien täyttämistä manuaalisesti. Tällä sivulla hallitaan myös integroinnin asetuksia.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä -kuvake"), kirjoita **Microsoft Dynamics 365 -yhteyden määritys** ja valitse sitten liittyvä linkki.
2. Anna seuraavat tiedot yhteyden muodostamiseen [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin.

|Kenttä|Kuvaus|
|-----|-----|
|**Dynamics 365 for Sales -ohjelman URL-osoite**|[!INCLUDE[crm_md](includes/crm_md.md)] -ilmentymän URL-osoite. Hae URL-osoite, avaa [!INCLUDE[crm_md](includes/crm_md.md)], kopioi URL-osoite selaimen osoiteriviltä ja liitä URL-osoite sitten kenttään. [!INCLUDE[d365fin](includes/d365fin_md.md)] varmistaa, että muoto on oikein.|
|**Käyttäjänimi** ja **Salasana**|Integrointiin varatun käyttäjätilin tunnistetiedot. Lisätietoja on kohdassa [Dynamics 365 for Sales -integroinnissa käytettävien käyttäjätilien määrittäminen](admin-setting-up-integration-with-dynamics-sales.md).|
|**Käytössä**|Aloita integroinnin käyttäminen. Jos et ota yhteyttä käyttöön nyt, yhteysasetukset tallennetaan. Käyttäjät eivät kuitenkaan voi käyttää [!INCLUDE[crm_md](includes/crm_md.md)]in tietoja [!INCLUDE[d365fin](includes/d365fin_md.md)]ista. Voit palata tälle sivulle myöhemmin ottamaan yhteyden käyttöön.  |
|**Dynamics 365 SDK -versio**|Jos integroit [!INCLUDE[crm_md](includes/crm_md.md)]in paikallisen version, muodosta yhteys [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)]iin tämän Dynamics 365 SDK -version avulla (joka tunnetaan myös nimellä Xrm). Valitsemasi version on oltava yhteensopiva [!INCLUDE[crm_md](includes/crm_md.md)]in käyttämän SDK-version kanssa. Tämä versio on sama tai uudempi kuin [!INCLUDE[crm_md](includes/crm_md.md)]in käyttämä versio.|

> [!Note]
> Jos yhdistät [!INCLUDE[d365fin](includes/d365fin_md.md)]in paikallisen version [!INCLUDE[crm_md](includes/crm_md.md)] ja haluat määrittää yhteyden [!INCLUDE[crm_md](includes/crm_md.md)] -ilmentymään tietyllä todennustyypillä, täytä **Todennustyypin tiedot** -pikavälilehden kentät. Lisätietoja on kohdassa [Yhteyden muodostaminen Dynamics 365:een XRM-työkalujen yhteysmerkkijonojen avulla](https://go.microsoft.com/fwlink/?linkid=843055). Tätä vaihetta tarvita yhdistettäessä [!INCLUDE[d365fin](includes/d365fin_md.md)]in online-versiota.

3. Anna seuraavat tiedot yhteyden muodostamiseen [!INCLUDE[crm_md](includes/crm_md.md)]ista [!INCLUDE[d365fin](includes/d365fin_md.md)]iin.

|Kenttä|Kuvaus|
|-----|-----|
|**Dynamics 365 Business Central Web Client -sovelluksen URL-osoite**|[!INCLUDE[d365fin](includes/d365fin_md.md)] -ilmentymän URL-osoite. Näin [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjät voivat avata vastaavat tietueet [!INCLUDE[d365fin](includes/d365fin_md.md)]issa [!INCLUDE[crm_md](includes/crm_md.md)]in tietueista, kuten tilistä tai tietueesta. [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueet avautuvat [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Määritä tämän kentän arvoksi käytettävän [!INCLUDE[d365fin](includes/d365fin_md.md)] -esiintymän URL-osoite.<br /><br /> Voit palauttaa kenttään [!INCLUDE[d365fin](includes/d365fin_md.md)]in oletusarvoisen URL-osoitteen valitsemalla **Palauta verkkoasiakasohjelman URL-osoite** -toiminnon.<br /><br /> Tällä kentällä on merkitystä vain, jos [!INCLUDE[d365fin](includes/d365fin_md.md)] -integrointiratkaisu on asennettu [!INCLUDE[crm_md](includes/crm_md.md)]issa.|
|**Nimikkeen saatavuus -verkkopalvelu käytössä**|Antaa [!INCLUDE[crm_md](includes/crm_md.md)]ia käyttäville henkilöille mahdollisuuden tarkastella nimikkeiden (tuotteiden) varastosaatavuutta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Jos otat tämän vaihtoehdon käyttöön, sinun on annettava myös [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjänimi ja käyttöoikeusavain, mikäli haluat tehdä nimikkeiden (tuotteiden) saatavuuskyselyn OData-verkkopalvelun avulla. Lisätietoja on kohdassa [OData-verkkopalvelut](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**Dynamics 365 Business Centralin OData-verkkopalvelun URL-osoite**|Jos otat Nimikkeen saatavuus -verkkopalvelun käyttöön, saat OData-verkkopalvelun URL-osoitteen.|
|**Dynamics 365 Business Centralin OData-verkkopalvelun käyttäjätunnus**|Sen käyttäjätilin nimi, jolla [!INCLUDE[crm_md](includes/crm_md.md)] hakee tietoja nimikkeen saatavuudesta [!INCLUDE[d365fin](includes/d365fin_md.md)]issa OData-verkkopalvelun kautta.|
|**Dynamics 365 Business Centralin OData-verkkopalvelun käyttöoikeusavain**|Sen käyttäjätilin käyttöoikeusavain, jolla [!INCLUDE[crm_md](includes/crm_md.md)] hakee tietoja nimikkeen saatavuudesta [!INCLUDE[d365fin](includes/d365fin_md.md)]ista OData-verkkopalvelun kautta. Avain on määritetty käyttäjälle, joka on valittu **Dynamics 365 Business Centralin OData-verkkopalvelun käyttäjätunnus** -kentässä. Voit hakea avaimen valitsemalla ensin käyttäjänimen vieressä **Hae arvo** -painikkeen ja sitten käyttäjän. Valitse seuraavaksi **Hallitse** ja lopuksi **Muokkaa**. Valitse käyttäjän kortissa ensin **Toiminnot**, **Tarkistus** ja sitten **Muuta verkkopalvelun käyttöoikeusavainta**.|

4. Anna seuraavat [!INCLUDE[crm_md](includes/crm_md.md)]in asetukset.

|Kenttä|Kuvaus|
|-----|-----|
|**Myyntitilauksen integrointi on käytössä**|Antaa käyttäjille mahdollisuuden lähettää myyntitilauksia ja aktivoituja tarjouksia [!INCLUDE[crm_md](includes/crm_md.md)]issa sekä tarkastella ja käsitellä niitä sitten [!INCLUDE[d365fin](includes/d365fin_md.md)]issa.|
|**Myyntitilausten automaattinen luominen**|Luo myyntitilaus [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, kun käyttäjä luo ja lähettää sellaisen [!INCLUDE[crm_md](includes/crm_md.md)]issa.|
|**Käsittele myyntitarjoukset automaattisesti**|Käsittele myyntitarjous [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, kun käyttäjä luo ja aktivoi sellaisen [!INCLUDE[crm_md](includes/crm_md.md)]issa.|

5. Anna seuraavat lisäasetukset.

|Kenttä|Kuvaus|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjät on yhdistettävä Dynamics 365 for Sales -käyttäjiin**|Määritä, onko [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttäjätileillä oltava vastaavat käyttäjätilit [!INCLUDE[crm_md](includes/crm_md.md)]issa. [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjän **Office 365:n todennuksen sähköpostiosoitteen** on oltava sama kuin [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjän **ensisijainen sähköposti**.<br /><br /> Jos valitse arvoksi **Kyllä**, [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjillä, joilla ei ole vastaavaa [!INCLUDE[crm_md](includes/crm_md.md)]in käyttäjätiliä, ei ole käyttöliittymässä [!INCLUDE[d365fin](includes/d365fin_md.md)] -integrointiominaisuuksia. [!INCLUDE[crm_md](includes/crm_md.md)]in tietoja käytetään suoraan [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[crm_md](includes/crm_md.md)] -käyttäjätilin puolesta.<br /><br /> Jos valitset arvoksi **Ei**, kaikilla [!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäjillä on käyttöliittymässä [!INCLUDE[crm_md](includes/crm_md.md)] -integrointiominaisuudet. [!INCLUDE[crm_md](includes/crm_md.md)]in tietoja käytetään [!INCLUDE[crm_md](includes/crm_md.md)] -yhteyden (integroinnin) käyttäjän puolesta.|
|**Nykyinen Business Central -käyttäjä yhdistetään Dynamics 365 for Sales -käyttäjään**|Ilmaisee, yhdistetäänkö käyttäjätili [!INCLUDE[crm_md](includes/crm_md.md)]in tiliin.|

6. Voit testata yhteysasetukset valitsemalla **Testaa yhteys**.  

    > [!NOTE]  
    >  Jos tietojen salaus ei ole käytössä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, sinulta kysytään, haluatko ottaa sen käyttöön. Ota tietojen salaus käyttöön valitsemalla **Kyllä** ja määritä tarvittavat tiedot. Valitse muussa tapauksessa **Ei**. Voit ottaa tietojen salauksen käyttöön myöhemmin. Lisätietoja on kehittäjän ja IT-ammattilaisen ohjeen kohdassa [Tietojen salaus Dynamics 365 Business Centralissa](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data).  

7. Jos [!INCLUDE[crm_md](includes/crm_md.md)]in synkronointia ei ole määritetty, sinulta kysytään, haluatko käyttää oletussynkronointiasetuksia. Valitse **Kyllä** tai **Ei** sen mukaan, haluatko pitää [!INCLUDE[crm_md](includes/crm_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueet kohdistettuina. 

### <a name="to-disconnect-from-includecrmmdincludescrmmdmd"></a>[!INCLUDE[crm_md](includes/crm_md.md)] -yhteyden katkaiseminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä -kuvake"), kirjoita **Microsoft Dynamics 365 for Sales -yhteyden määritys** ja valitse sitten liittyvä linkki.
2. Poista **Microsoft Dynamics 365 for Sales -yhteyden määritys** -sivun **Käytössä**-valintaruudun valinta.  

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension? 


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [http://go.microsoft.com/fwlink/?LinkID=616519](http://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](http://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.--> 

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [How to: Set Up a Microsoft Dynamics 365 for Sales Connection]() --> 

<!-- 
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 for Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 for Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 for Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## <a name="see-also"></a>Katso myös  
[Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md)  

