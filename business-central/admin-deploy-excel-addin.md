---
title: Business Central -apuohjelman hankkiminen Exceliin
description: Tutustu siihen, miten voit hankkia käyttäjille Business Central -apuohjelman Exceliin.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource
ms.date: 10/07/2021
ms.author: jswymer
ms.openlocfilehash: beb7a01986d12458e0615918608b44a6d90c269c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518413"
---
# <a name="get-the-business-central-add-in-for-excel"></a>Business Central -apuohjelman hankkiminen Exceliin

[!INCLUDE[prod_short](includes/prod_short.md)] sisältää Excelin apuohjelman, jonka avulla käyttäjät voivat valita **Muokkaa Excelissä** -toiminnon tietyillä sivuilla tietojen avaamiseksi Excel-työkirjassa. Tämä toiminto ei ole sama kuin **Avaa Excelissä** -toiminto, koska sen avulla käyttäjät voivat tehdä muutoksia Excelissä ja julkaista muutokset sitten takaisin kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]

## <a name="overview"></a>Yleiskuvaus

### <a name="about-the-add-in"></a>Tietoja apuohjelmasta

Apuohjelma on nimeltään **Microsoft Dynamics Office-apuohjelma**, ja sen voi asentaa [Office-kaupasta (AppSourcesta)](https://appsource.microsoft.com/). Kun apuohjelma on asennettu, **Muokkaa Excelissä** -toiminto on käytettävissä useimmissa luettelo- ja luettelo-osa-sivuissa **Jaa**-kuvakkeesta ![Jaa sivu toisessa sovelluksessa.](media/share-icon.png). Lisätietoja apuohjelman käyttämisestä on kohdassa [Tarkasteleminen ja muokkaaminen Excelissä Business Centralista](across-work-with-excel.md).

> [!NOTE]
> Apuohjelma toimii vain Windowsissa, ei Mac-käyttöjärjestelmässä.

### <a name="about-deployment-as-an-admin"></a>Tietoja käyttöönotosta ylläpitäjänä

[!INCLUDE[prod_short](includes/prod_short.md)] onlinen avulla apuohjelman voi saada käyttäjille muutamalla eri tavalla. Yksi valinta on *yksittäinen hankinta*, jossa käyttäjät voivat asentaa apuohjelman itse. Tällä asetuksella käyttäjillä on oltava oikeus ladata tiedostoja Office-kaupasta. Toinen tapa on määrittää *keskitetty käyttöönotto* Microsoft 365 -hallintakeskuksessa, jolloin lisäosa otetaan automaattisesti käyttöön koko organisaatiolle, ryhmille tai tietyille käyttäjille. Keskitetty käyttöönotto tarjoaa tavan saada apuohjelma käyttöön käyttäjille, jos organisaatiosi ei myönnä käyttäjille Office-kaupan käyttöoikeutta.

Loppukäyttäjän osalta asennuskokemus poikkeaa kahdessa käyttöönottoskenaariossa:

- Kun yksittäisessä hankkimisessa käyttäjä ensimmäisen kerran valitsee **Muokkaa Excelissä** -toiminnon, **Uusi Office-apuohjelma** -ruutu avautuu Excelissä. Jos käyttäjä haluaa asentaa apuohjelman, käyttäjä valitsee **Luota tähän apuohjelmaan**, joka puolestaan asentaa apuohjelman suoraan Office-kaupasta. Käyttäjät kirjautuvat sitten sisään [!INCLUDE[prod_short](includes/prod_short.md)]iin käyttäjänimen ja salasanan avulla.

- Kun keskitetyssä käyttöönotossa käyttäjät valitsevat ensimmäisen kerran **Muokkaa Excelissä** -toiminnon, apuohjelma asennetaan automaattisesti keskitetystä käyttöönotosta, ei Office-kaupasta. Käyttäjän tarvitsee vain kirjautua sisään kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]

Molempien käyttöönotto vaihtoehtojen yhteydessä apuohjelma määritetään automaattisesti muodostamaan yhteys kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]. Kolmas käyttöönottovaihtoehto on apuohjelman manuaalinen asennus suoraan Excelistä. Tässä vaihtoehdossa käyttäjän on määritettävä apuohjelman muodostamaan yhteys kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="switching-from-individual-acquisition-to-centralized-deployment-or-the-other-way-around"></a><a name="switch"></a>Siirtyminen yksittäisestä hankinnasta keskitettyyn käyttöönottoon tai toisin päin

Kun vaihdat apuohjelman yksittäisestä hankkimisesta keskitettyyn käyttöönottoon tai päinvastoin, tämä vaikuttaa Excel-tiedostoihin, jotka käyttäjät ovat luoneet ennen vaihtoa. Siirtymisen jälkeen käyttäjät voivat yhä avata **Muokkaa Excelissä** -toiminnossa aiemmin luodut tai Excel-apuohjelman määrittämällä manuaalisesti luodut Excel-laskentataulukot. He eivät kuitenkaan pysty päivittämään tiedoston tietoja Business Centralista tai lähettämään päivityksiä Business Centralin

Tämä ehto aiheutuu siitä, että jokaiseen Excel-tiedostoon liitetään apuohjelma-tunniste. Siirryttäessä keskitettyyn käyttöönottoon tai siitä pois eri tunnus määritetään, joten aiempi tunnus estetään.

## <a name="preparation-on-premises-only"></a>Valmistelu (vain on-premises)

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises edellyttää, että ympäristön on määritetty apuohjelmaa varten. Jos näin ei ole, **Muokkaa Excelissä** -toiminto ei ole käyttäjien käytettävissä. Lisätietoja on kehittäjien ja IT-ammattilaisten ohjeen kohdassa [Excel-apuohjelman määrittäminen Business Central -tietojen muokkaamiseen](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

## <a name="deploy-the-add-in-by-using-centralized-deployment"></a>Apuohjelman käyttöönottaminen keskitetyn käyttöönoton avulla

Keskitetty käyttöönotto on Microsoft 365 -hallintakeskuksen ominaisuus, jonka avulla voit asentaa apuohjelmat automaattisesti käyttäjien Office-sovelluksiin, kuten Exceliin. Keskitetyssä käyttöönotossa auttaa se, että [!INCLUDE[prod_short](includes/prod_short.md)] sisältää **Excel-apuohjelman keskitetyn käyttöönoton** avustetun asennuksen.

### <a name="before-you-begin"></a>Alkutoimet

- Lisätietoja käyttäjien lataamisen estämisestä Office-kaupasta on ohjeaiheessa [aApuohjelmien hallinta hallintakeskuksessa](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Varmista, että keskitetty käyttöönotto toimii organisaatiossasi. Lisätietoja on kohdassa [Määritä, toimiiko apuohjelmien keskitetty käyttöönotto organisaatiossasi](/microsoft-365/admin/manage/centralized-deployment-of-add-ins).
- Jos olet vaihtamassa yksittäisestä hankinnasta, katso [Siirtyminen yksittäisestä hankinnasta keskitettyyn käyttöönottoon](#switch)

> [!NOTE]
> Keskitetyn käyttöönoton ottaminen käyttöön vaikuttaa Excel-apuohjelmaa käyttäviin ominaisuuksiin, kuten **Muokkaa Excelissä** -toimintoon. Sillä ei ole vaikutusta muihin Exceliin liittyviin toimintoihin ja tai käyttöoikeuksiin, jotka on määritetty käyttäjille kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="set-up-centralized-deployment-of-the-add-in"></a>Määritä apuohjelman keskitetty käyttöönotto

Työskentelet sekä [!INCLUDE[prod_short](includes/prod_short.md)]issa että Microsoft 365 -hallintakeskuksessa.

1. Valitse [!INCLUDE[prod_short](includes/prod_short.md)]issa ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Excel-apuohjelman keskitetty käyttöönotto** ja valitse sitten liittyvä linkki.
2. Lue tiedot **Business Centralin Excel-apuohjelman määritys** -sivulta ja valitse **Seuraava**.
3. Kirjaudu [Microsoft 365 -hallintakeskukseen](https://go.microsoft.com/fwlink/?linkid=2163967) ja valitse sitten **Integroidut sovellukset**<!--**Add-ins**-->.

    Määritä apuohjelman käyttöönotto Office-kaupasta suorittamalla seuraavat vaiheet: 
    1. Avaa Office-kauppa (AppSource) valitsemalla **Hae sovelluksia**. <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
    2. Etsi **Microsoft Dynamics Office -apuohjelma** ja valitse sitten **Hae nyt**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
    3. Määritä **Lisää käyttäjiä** -sivulla käyttäjät, joille haluat ottaa apuohjelman käyttöön, ja valitse sitten **Seuraava**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
    4. Tarkista **Hyväksy käyttöoikeuspyynnöt** ja valitse sitten **Seuraava** > **Viimeistele käyttöönotto**.
    5. Odota, että apuohjelman **Käyttöönotettu**-kohdan vieressä oleva vihreä valintamerkki näkyy ja valitse sitten **Valmis**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

       Apuohjelma näkyy **Apuohjelmat**-sivulla. Lisätietoja apuohjelmien käyttöönotosta Microsoft 365 -hallintakeskuksessa on kohdassa [Apuohjelmien käyttöönotto hallintakeskuksessa](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).
4. Siirry takaisin **Excel-apuohjelman keskitetyn käyttöönoton** avustettuun määritykseen kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] ja valitse **Seuraava**.
5. Ota käyttöön **Käytä keskitettyä käyttöönottoa** ja valitse **Valmis**.

    Jos et ota tätä valitsinta käyttöön, [!INCLUDE[prod_short](includes/prod_short.md)] hakee apuohjelman suoraan Office-kaupasta.

Kun olet valmis, voit aina muuttaa käyttöönottoa Microsoft 365 -hallintakeskuksessa, kuten määrittää useampia käyttäjiä. Lisätietoja apuohjelmien käyttöönotosta hallintakeskuksessa on kohdassa [Apuohjelmien käyttöönotto hallintakeskuksessa](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).

> [!IMPORTANT]
> Jos ympäristöjä on useampia kuin yksi, sinun on suoritettava **Excel-apuohjelman keskitetty käyttöönotto** -määritys kussakin ympäristössä, jossa haluat käyttää keskitettyä käyttöönottoa. Keskitettyä käyttöönottoa ei kuitenkaan tarvitse määrittää Microsoft 365:ssä uudelleen. Ainoa asia mitä sinun tarvitsee tehdä on ottaa käyttöön **Käytä keskitettyä käyttöönottoa** -kytkin avustetussa määrityksessä. 

> [!NOTE]
> Apuohjelman automaattinen käyttöönotto käyttäjille voi kestää 24 tuntia.

## <a name="individual-acquisition-install-the-add-in-manually-for-your-own-use"></a><a name="install"></a>Yksittäinen hankinta: Asenna apuohjelma manuaalisesti omaan käyttöön

Useimmissa tapauksissa, kun avaat Excelin Business Centralista, apuohjelma asennetaan joko automaattisesti puolestasi tai sinua kehotetaan asentamaan se. Saattaa kuitenkin olla tilanteita, joissa apuohjelma on asennettava manuaalisesti.

1. Avaa Excel ja avaa sitten mikä tahansa Excel-työkirja.
2. Valitse **Lisää**-valikosta **Apuohjelmat** > **Hae apuohjelmat**
3. Siirry kohtaan **Järjestelmänvalvojan hallinnoimat** ja etsi **Microsoft Dynamics Office -apuohjelma**. Jos näet sen tässä, valitse se ja valitse sitten **Lisää**. Jos et näe sitä, siirry **kauppaan** ja etsi *Microsoft Dynamics Office -apuohjelma* ja lisää se noudattamalla näyttöön tulevia ohjeita.

Kun apuohjelma on asennettu, se näkyy paneelina Excelissä. Seuraavaksi määritetään yhteys.

### <a name="configure-the-business-central-connection"></a>Business Central -yhteyden määrittäminen

Jos käyttäjä ei voi muodostaa yhteyttä automaattisesti, voit poistaa eston pyytämällä heitä noudattamaan seuraavia vaiheita:

1. Valitse Excelissä **Microsoft Dynamics**-apuohjelmaruutu ja sitten **Lisää palvelimen tiedot**. Jos et näe sitä, valitse ![Excelin Lisää vaihtoehtoja -painike.](media/cogwheel.png) -kuvake ylhäällä avataksesi asetusikkunan. 
2. Määritä [!INCLUDE[prod_short](includes/prod_short.md)] onlinelle **palvelimen URL-osoitteeksi** `https://exceladdinprovider.smb.dynamics.com`. Määritä [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versiolle verkkoasiakkaan URL-osoite, kuten `https://myBCserver/190`.
3. Valitse **OK** ja vahvista sitten, että sovellus lataa uudelleen.
4. Kirjaudu kehotteessa Business Centralin käyttäjänimen ja salasanan avulla.
5. Valitse vaihtoehtoisesti ympäristö ja yritys, joihin haluat muodostaa yhteyden.

Apuohjelma on nyt yhdistetty kohteeseen [!INCLUDE [prod_short](includes/prod_short.md)] ja voit muokata tietoja ja julkaista muutokset kohtaan [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="prepare-devices-and-network-for-the-excel-add-in"></a>Valmistele laitteet ja verkko Excel-apuohjelmaa varten

Verkkopalveluiden, kuten välityspalvelimien tai palomuurien, on sallittava reititys kunkin sellaisen asiakaslaitteen, johon apuohjelma on asennettu, ja useiden palvelun päätepisteiden välillä. Luettelo päätepisteistä on kohdassa [Verkon valmisteleminen Excel-apuohjelmaa varten](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins).

## <a name="troubleshooting"></a>Vianetsintä

Toisinaan käyttäjät kohtaavat ongelmia Excel-apuohjelmassa. Tässä osassa on vihjeitä siitä, miten voit poistaa käyttäjien eston tietyissä tilanteissa.

|Ongelma  |Ratkaisu tai kiertotapa  |Kommentit  |
|---------|---------|---------|
|Apuohjelma ei käynnisty|Tarkista, onko apuohjelma otettu käyttöön keskitetysti. Tai tarkista, onko käyttäjän asennus estetty paikallisesti. | Järjestelmänvalvoja voi määrittää Officen niin, että käyttäjät eivät pysty hankkimaan apuohjelmia. Näissä tapauksissa järjestelmänvalvojan on otettava apuohjelma käyttöön keskitetysti. Lisätietoja on kohdassa [Apuohjelmien käyttöönotto hallintakeskuksessa](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).|
|Tietoja ei ladata Exceliin|Yhteyden testaaminen avaamalla toinen luettelo Excelissä osoitteesta [!INCLUDE [prod_short](includes/prod_short.md)]. Tai avaa työkirja Excelissä selaimessa.|Jos käyttäjä on määrittänyt yrityksen nimen, jossa on erikoismerkkejä, apuohjelma ei voi muodostaa yhteyttä. |
|Tietoja ei voi julkaista takaisin osoitteeseen [!INCLUDE [prod_short](includes/prod_short.md)].|Testaa yhteys avaamalla työkirja Excelissä selaimessa. |Joskus laajennus voi estää julkaisutyön. Jos sivua on laajennettu tai mukautettu, poista laajennukset ja yritä uudelleen.|
|Päivämäärät ovat vääriä  |Excel saattaa näyttää ajat ja päivämäärät eri muodossa kuin kohdassa [!INCLUDE [prod_short](includes/prod_short.md)]. Tämä ei tee niistä virheellisiä, eivätkä tiedot kohdassa [!INCLUDE [prod_short](includes/prod_short.md)] mene sekaisin.|         |
|Joillakin luettelosivuilla useiden rivien muokkaaminen Excelissä aiheuttaa toistuvasti virheitä. Tämä ehto voi ilmetä, jos OData-kutsut sisältävät FlowFields-kenttiä ja kenttiä toistinohjausobjektin ulkopuolella.|Valitse **Verkkopalvelut**-sivulla **Jätä pois ei-muokattavat FlowField-kentät**- ja **Jätä pois toistimen ulkopuoliset kentät** -valintaruudut julkaistulle sivulle. Jos valitset nämä valintaruudut, se jättää pois ei-muokattavat FlowField-kentät ja kentät eTag-laskennasta. |Nämä valintaruudut on oletusarvoisesti piilotettu. Voit näyttää ne **Verkkopalvelut**-sivulla käyttämällä [mukauttamista](/dynamics365/business-central/ui-personalization-user). |



<!--
## Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Rahoituslaskelmien analysointi Microsoft Excelissä](finance-analyze-excel.md)  
[Business Centralin käyttäminen](ui-work-product.md)  
[Excel-integraation parannukset vuoden 2019 2. julkaisuaallossa](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
