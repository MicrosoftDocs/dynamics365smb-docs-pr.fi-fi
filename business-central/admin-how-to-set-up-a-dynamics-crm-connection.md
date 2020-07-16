---
title: Yhteyden muodostaminen Common Data Serviceiin | Microsoft Docs
description: Voit integroida muita sovelluksia Business Centralin avulla Common Data Servicen kautta.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/30/2020
ms.author: bholtorf
ms.openlocfilehash: 4c57d8c79f91319675527f514b01b6ddeb83e722
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529211"
---
# <a name="connect-to-common-data-service"></a>Yhteyden muodostaminen Common Data Serviceen
Tässä ohjeaiheessa kuvataan, kuinka [!INCLUDE[d365fin](includes/d365fin_md.md)] ja [!INCLUDE[d365fin](includes/cds_long_md.md)] välille määritetään yhteys. Yleensä yritykset luovat yhteyden integroidakseen ja synkronoidakseen tietoja toisen Dynamics 365 -liiketoimintasovelluksen kanssa. Sovellus voi olla esimerkiksi [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Ennen aloittamista
Ennen yhteyden luomista tarvitaan seuraavat tiedot:  

* Sen [!INCLUDE[d365fin](includes/cds_long_md.md)] -ympäristön URL-osoite, johon haluat muodostaa yhteyden. Jos käytät **CDS-yhteyden määrityksen** asetusten ohjattua määritysopasta yhteyden luomiseen, ympäristöt löydetään. Sinun on kuitenkin annettava myös vuokraajan toisen ympäristön URL-osoite.  
* Sen tilin käyttäjätili ja salasana, jolla on järjestelmänvalvojan oikeudet [!INCLUDE[d365fin](includes/d365fin_md.md)]- ja [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa.  

> [!Note]
> Seuraavat vaiheet koskevat [!INCLUDE[d365fin](includes/d365fin_md.md)]in online-versiota.
> Jos käytössä Business Central on-premesis eikä Azure Active Directory -tiliä käytetä muodostamaan yhteyttä Common Data Serviceen, integrointia varten on määritettävä käyttäjätilin käyttäjänimi ja salasana. Tätä tiliä kutsutaan integroinnin käyttäjän tiliksi. Azure Active Directory -tiliä käytettäessä integroinnin käyttäjän tiliä ei tarvita eikä sitä näytetä. Integroinnin käyttäjä määritetään automaattisesti, eikä sitä varten tarvita käyttöoikeutta.

## <a name="set-up-a-connection-to-d365fin"></a>Yhteyden määrittäminen [!INCLUDE[d365fin](includes/cds_long_md.md)]iin  
Jos todennustyyppi on jokin muu kuin Office 365 -todennus, voit määrittää [!INCLUDE[d365fin](includes/cds_long_md.md)] -yhteyden **CDS-yhteyden määritys** -sivulla. Office 365 -todennuksessa on suositeltavaa käyttää **Common Data Service -yhteyden määrityksen** asetusten ohjattua määritysopasta. Opas auttaa määrittämään nopeasti yhteyden ja lisäominaisuudet, kuten omistajamallin ja ensimmäisen synkronoinnin.  

> [!Important]
> [!INCLUDE[d365fin](includes/cds_long_md.md)] -yhteyttä määritettäessä järjestelmänvalvojaa pyydetään antamaan seuraavat käyttöoikeudet rekisteröidylle Azuren [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration to [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovellukselle:
> * **[!INCLUDE[d365fin](includes/cds_long_md.md)]n käyttö sinuna** -käyttöoikeus tarvitaan, jotta [!INCLUDE[d365fin](includes/d365fin_md.md)] voi luoda järjestelmänvalvojan puolesta automaattisesti [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration -sovelluksen käyttäjän, jolla ei ole käyttö- eikä vuorovaikutusoikeutta, määrittää käyttöoikeusroolit kyseiselle käyttäjälle ja ottaa käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]in perustason CDS -integrointiratkaisun [!INCLUDE[d365fin](includes/cds_long_md.md)]en. Tätä käyttöoikeutta käytetään vain kerran määritettäessä yhteyttä [!INCLUDE[d365fin](includes/cds_long_md.md)]en. 
> * **Täydet Dynamics 365 [!INCLUDE[d365fin](includes/d365fin_md.md)] -käyttöoikeudet** tarvitaan, jotta automaattisesti luotu [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration -sovelluksen käyttäjä voi käyttää synkronoitavia [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietoja. 
> * **Kirjautuminen ja profiilin lukeminen** -käyttöoikeus tarvitaan varmistamaan, että kirjautuvalle käyttäjälle on määritetty järjestelmänvalvojan käyttöoikeusrooli [!INCLUDE[d365fin](includes/cds_long_md.md)]ssa. 
>
> Antamalla suostumuksen organisaation puolesta järjestelmänvalvoja antaa [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration to [!INCLUDE[d365fin](includes/cds_long_md.md)] -nimiselle Azure-sovelluksen oikeuden synkronoida tietoja käyttämällä automaattisesti luodun [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration -sovelluksen käyttäjän tunnistetietoja.

### <a name="to-use-the-set-up-common-data-service-connection-assisted-setup-guide"></a>Common Data Service -yhteyden määrityksen asetusten ohjatun määritysoppaan käyttäminen 
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys** ja valitse sitten liittyvä linkki.
2. Käynnistä asetusten ohjattu määritys valitsemalla **Common Data Service -yhteyden määritys**.
3. Täytä tarvittavat kentät.

### <a name="to-create-or-maintain-the-connection-manually"></a>Yhteyden luominen tai ylläpitäminen manuaalisesti
Seuraavassa kerrotaan, miten yhteys määritetään manuaalisesti **CDS-yhteyden määritys** -sivulla. Tällä sivulla hallitaan myös integroinnin asetuksia.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **CDS-yhteyden määritys** ja valitse liittyvä linkki.
2. Anna seuraavat tiedot yhteyden muodostamiseen [!INCLUDE[d365fin](includes/d365fin_md.md)]ista [!INCLUDE[d365fin](includes/cds_long_md.md)]iin.

|Kenttä|Kuvaus|
|-----|-----|
|**Ympäristön URL-osoite**|Jos [!INCLUDE[d365fin](includes/cds_long_md.md)]:ssä on omia ympäristöjä, ne löytyvät ohjatun määrityksen suorittamisen yhteydessä. Jos haluat muodostaa yhteyden toiseen ympäristöön eri vuokraajassa, voit syöttää ympäristön järjestelmänvalvojan tunnistetiedot. Ympäristö löytyy niiden avulla. |
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
    >  Jos tietojen salaus ei ole käytössä [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, sinulta kysytään, haluatko ottaa sen käyttöön. Ota tietojen salaus käyttöön valitsemalla **Kyllä** ja määritä tarvittavat tiedot. Valitse muussa tapauksessa **Ei**. Voit ottaa tietojen salauksen käyttöön myöhemmin. Lisätietoja on kehittäjän ja järjestelmänvalvojan ohjeen kohdassa [Tietojen salaus Dynamics 365 Business Centralissa](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data).  

5. Jos [!INCLUDE[d365fin](includes/cds_long_md.md)]in synkronointia ei ole määritetty, sinulta kysytään, haluatko käyttää oletussynkronointiasetuksia. Valitse **Kyllä** tai **Ei** sen mukaan, haluatko pitää [!INCLUDE[d365fin](includes/cds_long_md.md)]in ja [!INCLUDE[d365fin](includes/d365fin_md.md)]in tietueet kohdistettuina.

## <a name="connecting-on-premises-versions"></a>Paikallisten versioiden yhdistäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] on-premises -version yhdistäminen [!INCLUDE[d365fin](includes/cds_long_md.md)]en edellyttää, että **Common Data Service -yhteyden määritys** -sivulla määritetään joitakin tietoja.

Jos haluat muodostaa yhteyden käyttämällä Azure Active Directory (Azure AD) -tiliä, sovellus on rekisteröitävä Azure AD:ssä, minkä lisäksi on asennettava sovelluksen tunnus, avainsäilön salaisuus ja käytettävä uudelleenohjauksen URL-osoite. Uudelleenohjauksen URL-osoite täytetään valmiiksi, ja sen pitäisi toimia useimmissa asennuksissa. Asennus on määritettävä käyttämään HTTPS-yhteyttä. Lisätietoja on kohdassa [SSL:n määrittäminen suojaamaan Business Centralin verkkoasiakasohjelman yhteyttä](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Jos palvelimelle määritetään jokin muu aloitussivu, URL-osoitteen voi vaihtaa. Asiakasohjelman salaisuus tallennetaan tietokantaan salattuna merkkijonona. 

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-common-data-service"></a>Sovelluksen rekisteröiminen Azure AD:ssä muodostamaan yhteys Business Centralista Common Data Serviceen
Seuraavissa vaiheissa oletetaan, käyttäjätietojen ja käyttöoikeuksien hallintaan käytetään Azure AD:tä. Lisätietoja sovelluksen rekisteröimisestä Azure AD:ssä on kohdassa [Pika-aloitus: sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristössä](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app). Jos Azure AD ei ole käytössä, lisätietoja on kohdassa [Jonkin muun käyttäjätieto- ja käyttöoikeuspalvelun käyttäminen](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service). 

1. Valitse Azure-portaalin **Hallinta**-kohdan siirtymisruudussa **Todennus**. 
2. Lisää **Uudelleenohjauksen URL-osoite** -kohdassa [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Common Data Service -yhteyden määritys** -sivulla ehdotettu uudelleenohjauksen URL-osoite.
3. Valitse **Hallinta**-kohdassa **API-käyttöoikeudet**.
4. Valitse **Määritetyt käyttöoikeudet** -kohdassa **Lisää käyttöoikeus** ja lisää sitten delegoidut käyttöoikeudet **Microsoftin API:t** -välilehdessä seuraavasti:
    * Business Central: lisää **Financials.ReadWrite.All**-käyttöoikeudet.
    * Dynamics CRM: lisää **user_impersonation**-käyttöoikeudet. 

> [!NOTE]
> Dynamics CRM -API:n nimi voi muuttua.

5.  Valitse **Hallinta**-kohdassa **Varmenteet ja salaiset avaimet** ja lue sitten sovellukselle uusi salaisuus. Salaista avainta joko käytetään [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Common Data Service -yhteyden määritys** -sivun **Asiakasohjelman salainen avain** -kentässä tai se tallennetaan suojattuun tallennustilaan, josta se annetaan tapahtumaan tilaajassa aiemmin tässä aiheessa kuvatulla tavalla.
6. Valitse **Yleiskuvaus** ja etsi sitten **Sovelluksen (asiakasohjelman) tunnus** -arvo. Tämä on sovelluksen asiakasohjelman tunnus. Se on joko annettava **Common Data Service -yhteyden määritys** -sivun **Asiakasohjelman tunnus** -kentässä tai tallennettava suojattuun tallennustilaan tapahtuman tilaajassa annettavaksi.
7. Anna [!INCLUDE[d365fin](includes/d365fin_md.md)]in **Common Data Service -yhteyden määritys** -sivun **Ympäristön URL-osoite** -kentässä [!INCLUDE[d365fin](includes/cds_long_md.md)] -ympäristön URL-osoite.
8. [!INCLUDE[d365fin](includes/cds_long_md.md)] -yhteys otetaan käyttöön **Käytössä**-valitsimella.
9. Käytä kirjautumiseen Azure Active Directoryn järjestelmänvalvojan tiliä. (Tämä tili tarvitsee voimassaolevan [!INCLUDE[d365fin](includes/cds_long_md.md)]n käyttöoikeuden, ja sen on oltava [!INCLUDE[d365fin](includes/cds_long_md.md)] -ympäristön järjestelmänvalvoja.) Kirjautumisen jälkeen sinua pyydetään antamaan rekisteröidylle sovellukselle lupa kirjautua [!INCLUDE[d365fin](includes/cds_long_md.md)]en organisaation puolesta. Määrityksen valmistumisen edellyttää tämän luvan antamista.

   > [!NOTE]
   > Jos sinua ei pyydetä käyttämään kirjautumiseen järjestelmänvalvojan tiliä, syynä on luultavasti estetyt ponnahdusikkunat. Kirjautumista varten on sallittava ponnahdusikkunat osoitteesta https://login.microsoftonline.com.

#### <a name="using-another-identity-and-access-management-service"></a>Jonkin muun käyttäjätieto- ja käyttöoikeuspalvelun käyttäminen
Jos Azure Active Directorya ei käytetä käyttäjätietojen ja käyttöoikeuksien hallintaa, apua on pyydettävä kehittäjältä. Jos haluat tallentaa sovelluksen tunnuksen ja salaisen avaimen eri sijaintiin, Asiakasohjelman tunnus- ja Asiakasohjelman salainen avain -kentät voidaan jättää tyhjäksi. Tunnuksen ja salaisen avaimen sijainnista noutoa varten on siinä tapauksessa kirjoitettava laajennus. Salainen avain voidaan antaa suorituspalvelussa tilaamalla OnGetCDSConnectionClientId- ja OnGetCDSConnectionClientSecret-tapahtumat codeunitissa 7201 CDS Integration Impl.

### <a name="to-disconnect-from-d365fin"></a>[!INCLUDE[d365fin](includes/cds_long_md.md)] -yhteyden katkaiseminen  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **CDS-yhteyden määritys** ja valitse liittyvä linkki.
2. Poista käytöstä **CDS-yhteyden määritys** -sivulla **Käytössä**-valitsin.  

## <a name="see-also"></a>Katso myös  
[Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md)  
