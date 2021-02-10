---
title: Yhteyden muodostaminen Microsoft Dataverseiin | Microsoft Docs
description: Voit integroida muita sovelluksia Business Centralin avulla Microsoft Dataversen kautta.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/20/2020
ms.author: bholtorf
ms.openlocfilehash: e0713de255aabc599fbc80cf29f1bfa618a29003
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753915"
---
# <a name="connect-to-microsoft-dataverse"></a>Yhteyden muodostaminen Microsoft Dataverseen
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka [!INCLUDE[prod_short](includes/prod_short.md)] ja [!INCLUDE[cds_long_md](includes/cds_long_md.md)] välille määritetään yhteys. Yleensä yritykset luovat yhteyden integroidakseen ja synkronoidakseen tietoja toisen Dynamics 365 -liiketoimintasovelluksen kanssa. Sovellus voi olla esimerkiksi [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Ennen aloittamista

Ennen yhteyden luomista tarvitaan seuraavat tiedot:  

* Sen [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -ympäristön URL-osoite, johon haluat muodostaa yhteyden. Jos käytät **Common Data Service -yhteyden määrityksen** asetusten ohjattua määritysopasta yhteyden luomiseen, ympäristöt löydetään. Sinun on kuitenkin annettava myös vuokraajan toisen ympäristön URL-osoite.  
* Sen tilin käyttäjätili ja salasana, jolla on järjestelmänvalvojan oikeudet [!INCLUDE[prod_short](includes/prod_short.md)]- ja [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -sovelluksessa.  
* Jos käytössäsi on [!INCLUDE[prod_short](includes/prod_short.md)]vuoden 2020 1. julkaisuaallon on-premises-versio 16.5, lue [Joitakin tunnettuja ongelmia](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services) -artikkeli. Sinun on toteutettava kuvattu kiertotapa, ennen kuin voit luoda yhteyden [!INCLUDE[cds_long_md](includes/cds_long_md.md)]en.

> [!Note]
> Seuraavat vaiheet koskevat [!INCLUDE[prod_short](includes/prod_short.md)] online -versiota.
> Jos käytössä [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versiota eikä Azure Active Directory -tiliä käytetä muodostamaan yhteyttä [!INCLUDE [cds_long_md](includes/cds_long_md.md)]en, integrointia varten on määritettävä käyttäjätilin käyttäjänimi ja salasana. Tätä tiliä kutsutaan integroinnin käyttäjän tiliksi. Azure Active Directory -tiliä käytettäessä integroinnin käyttäjän tiliä ei tarvita eikä sitä näytetä. Integroinnin käyttäjä määritetään automaattisesti, eikä sitä varten tarvita käyttöoikeutta.

## <a name="set-up-a-connection-to-cds_long_md"></a>Yhteyden määrittäminen [!INCLUDE[cds_long_md](includes/cds_long_md.md)]iin

Jos todennustyyppi on jokin muu kuin Microsoft 365 -todennus, voit määrittää [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -yhteyden **Common Data Service -yhteyden määritys** -sivulla. Microsoft 365 -todennuksessa on suositeltavaa käyttää **Common Data Service -yhteyden määrityksen** asetusten ohjattua määritysopasta. Opas auttaa määrittämään nopeasti yhteyden ja lisäominaisuudet, kuten omistajamallin ja ensimmäisen synkronoinnin.  

> [!IMPORTANT]
> [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -yhteyttä määritettäessä järjestelmänvalvojaa pyydetään antamaan seuraavat käyttöoikeudet rekisteröidylle Azuren [!INCLUDE[prod_short](includes/prod_short.md)] Integration to [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -sovellukselle:
>
> * **[!INCLUDE[cds_long_md](includes/cds_long_md.md)]n käyttö sinuna** -käyttöoikeus tarvitaan, jotta [!INCLUDE[prod_short](includes/prod_short.md)] voi luoda järjestelmänvalvojan puolesta automaattisesti [!INCLUDE[prod_short](includes/prod_short.md)] Integration -sovelluksen käyttäjän, jolla ei ole käyttö- eikä vuorovaikutusoikeutta, määrittää käyttöoikeusroolit kyseiselle käyttäjälle ja ottaa käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]in perustason CDS -integrointiratkaisun [!INCLUDE[cds_long_md](includes/cds_long_md.md)]en. Tätä käyttöoikeutta käytetään vain kerran määritettäessä yhteyttä [!INCLUDE[cds_long_md](includes/cds_long_md.md)]en.  
> * **Täydet Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)] -käyttöoikeudet** tarvitaan, jotta automaattisesti luotu [!INCLUDE[prod_short](includes/prod_short.md)] Integration -sovelluksen käyttäjä voi käyttää synkronoitavia [!INCLUDE[prod_short](includes/prod_short.md)]in tietoja.  
> * **Kirjautuminen ja profiilin lukeminen** -käyttöoikeus tarvitaan varmistamaan, että kirjautuvalle käyttäjälle on määritetty järjestelmänvalvojan käyttöoikeusrooli [!INCLUDE[cds_long_md](includes/cds_long_md.md)]ssa.  
>
> Antamalla suostumuksen organisaation puolesta järjestelmänvalvoja antaa [!INCLUDE[prod_short](includes/prod_short.md)] Integration to [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -nimiselle Azure-sovelluksen oikeuden synkronoida tietoja käyttämällä automaattisesti luodun [!INCLUDE[prod_short](includes/prod_short.md)] Integration -sovelluksen käyttäjän tunnistetietoja.

### <a name="to-use-the-common-data-service-connection-setup-assisted-setup-guide"></a>Common Data Service -yhteyden määrityksen asetusten ohjatun määritysoppaan käyttäminen
Common Data Service -yhteyden asetusopas helpottaa sovellusten yhdistämistä, ja se voi auttaa sinua myös suorittamaan ensimmäisen synkronoinnin. Jos päätät käynnistää ensimmäisen synkronoinnin, [!INCLUDE[prod_short](includes/prod_short.md)] tarkistaa molempien sovellusten tiedot ja antaa suosituksia ensimmäisen synkronoinnin toteutusta varten. Seuraavassa taulukossa kuvaillaan näitä suosituksia.

|Suositus  |Kuvaus  |
|---------|---------|
|**Täysi synkronointi**|Tietoja on vain [!INCLUDE[prod_short](includes/prod_short.md)] -järjestelmässä tai vain [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -järjestelmässä. Suositus on synkronoida toiseen palveluun kaikki tiedot palvelusta, jossa tiedot ovat.|
|**Ei synkronointia**|Molemmissa sovelluksissa on tietoja, ja täyden synkronoinnin suorittaminen loisi tietojen kaksoiskappaleita. Suositus on yhdistää tietueet.|
|**Riippuvuus ei täyty**|Molemmissa sovelluksissa on tietoja, mutta riviä tai taulukkoa ei voi synkronoida, koska se riippuu rivistä tai taulukosta, jossa on Ei synkronointia -suositus. Jos esimerkiksi asiakkaita ei voi synkronoida, asiakastiedoista riippuvien kontaktien tietoja ei voi myöskään synkronoida.|

> [!IMPORTANT]
> Yleensä täysi synkronointi on käytössä vain, kun sovellukset integroidaan ensimmäistä kertaa ja vain yksi sovellus sisältää tietoja. Täydellisestä synkronoinnista voi olla hyötyä demoympäristössä, koska se luo ja yhdistää tietueet automaattisesti kummassakin sovelluksessa, minkä ansiosta synkronoitujen tietojen käsittelemisen aloittaminen nopeutuu. Suorita täysi synkronointi kuitenkin vain, jos haluat taulukon yhdistämismäärityksille yhden rivin [!INCLUDE[prod_short](includes/prod_short.md)]issa kutakin [!INCLUDE[cds_long_md](includes/cds_long_md.md)]n riviä kohden. Muussa tapauksessa tuloksena voi olla tietueiden kaksoiskappaleita.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys** ja valitse sitten liittyvä linkki.
2. Käynnistä asetusten ohjattu määritys valitsemalla **Dataverse -yhteyden määritys**.
3. Täytä tarvittavat kentät.

> [!NOTE]
> Jos sinua ei pyydetä käyttämään kirjautumiseen järjestelmänvalvojan tiliä, syynä on luultavasti estetyt ponnahdusikkunat. Kirjautumista varten on sallittava ponnahdusikkunat osoitteesta `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Yhteyden luominen tai ylläpitäminen manuaalisesti

Seuraavassa kerrotaan, miten yhteys määritetään manuaalisesti **Common Data Service -yhteyden määritys** -sivulla. Tällä sivulla hallitaan myös integroinnin asetuksia.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Common Data Service -yhteyden määritys** ja valitse sitten liittyvä linkki.
2. Anna seuraavat tiedot yhteyden muodostamiseen [!INCLUDE[prod_short](includes/prod_short.md)]ista [!INCLUDE[cds_long_md](includes/cds_long_md.md)]iin.

    |Kenttä|Kuvaus|
    |-----|-----|
    |**Ympäristön URL-osoite**|Jos [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:ssä on omia ympäristöjä, ne löytyvät ohjatun määrityksen suorittamisen yhteydessä. Jos haluat muodostaa yhteyden toiseen ympäristöön eri vuokraajassa, voit syöttää ympäristön järjestelmänvalvojan tunnistetiedot. Ympäristö löytyy niiden avulla. |
    |**Käytössä**|Aloita integroinnin käyttäminen. Jos et ota yhteyttä käyttöön nyt, yhteysasetukset tallennetaan. Käyttäjät eivät kuitenkaan voi käyttää [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in tietoja [!INCLUDE[prod_short](includes/prod_short.md)]ista. Voit palata tälle sivulle myöhemmin ottamaan yhteyden käyttöön.  |

3. Valitse **Omistusmalli**-kentässä, haluatko [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:n tiimitaulukon vai jonkin tietyn käyttäjän omistavan uudet tietueet. Jos valitset **Henkilö**-kohdan, sinun täytyy määrittää jokainen käyttäjä. Jos valitset **Tiimi**-kohdan oletusliiketoimintayksikkö näkyy **Yhdistetty liiketoimintayksikkö** -kentässä.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

   <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field-->|

4. Jos haluat testata yhteysasetukset, valitse **Yhteys** ja valitse sitten **Testaa yhteys**.  

    > [!NOTE]  
    > Jos tietojen salaus ei ole käytössä [!INCLUDE[prod_short](includes/prod_short.md)]issa, sinulta kysytään, haluatko ottaa sen käyttöön. Ota tietojen salaus käyttöön valitsemalla **Kyllä** ja määritä tarvittavat tiedot. Valitse muussa tapauksessa **Ei**. Voit ottaa tietojen salauksen käyttöön myöhemmin. Lisätietoja on kehittäjän ja järjestelmänvalvojan ohjeen kohdassa [Tietojen salaus Dynamics 365 Business Centralissa](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data).  

5. Jos [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in synkronointia ei ole määritetty, sinulta kysytään, haluatko käyttää oletussynkronointiasetuksia. Valitse **Kyllä** tai **Ei** sen mukaan, haluatko pitää [!INCLUDE[cds_long_md](includes/cds_long_md.md)]in ja [!INCLUDE[prod_short](includes/prod_short.md)]in tietueet kohdistettuina.
<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="connecting-on-premises-versions"></a>Paikallisten versioiden yhdistäminen

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises -version yhdistäminen [!INCLUDE[cds_long_md](includes/cds_long_md.md)]en edellyttää, että **Common Data Service -yhteyden määritys** -sivulla määritetään joitakin tietoja.

Jos haluat muodostaa yhteyden käyttämällä Azure Active Directory (Azure AD) -tiliä, sovellus on rekisteröitävä Azure AD:ssä, minkä lisäksi on asennettava sovelluksen tunnus, avainsäilön salaisuus ja käytettävä uudelleenohjauksen URL-osoite. Uudelleenohjauksen URL-osoite täytetään valmiiksi, ja sen pitäisi toimia useimmissa asennuksissa. Asennus on määritettävä käyttämään HTTPS-yhteyttä. Lisätietoja on kohdassa [SSL:n määrittäminen suojaamaan Business Centralin verkkoasiakasohjelman yhteyttä](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Jos palvelimelle määritetään jokin muu aloitussivu, URL-osoitteen voi vaihtaa. Asiakasohjelman salaisuus tallennetaan tietokantaan salattuna merkkijonona.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>Sovelluksen rekisteröiminen Azure AD:ssä muodostamaan yhteys Business Centralista Dataverseen

Seuraavissa vaiheissa oletetaan, käyttäjätietojen ja käyttöoikeuksien hallintaan käytetään Azure AD:tä. Lisätietoja sovelluksen rekisteröimisestä Azure AD:ssä on kohdassa [Pika-aloitus: sovelluksen rekisteröinti Microsoftin idtable-ympäristössä](/azure/active-directory/develop/quickstart-register-app). Jos Azure AD ei ole käytössä, lisätietoja on kohdassa [Jonkin muun Idtable- ja käyttöoikeuspalvelun käyttäminen](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-idtable-and-access-management-service).  

1. Valitse Azure-portaalin **Hallinta**-kohdan siirtymisruudussa **Todennus**.  
2. Lisää **Uudelleenohjauksen URL-osoite** -kohdassa [!INCLUDE[prod_short](includes/prod_short.md)]in **Common Data Service -yhteyden määritys** -sivulla ehdotettu uudelleenohjauksen URL-osoite.
3. Valitse **Hallinta**-kohdassa **API-käyttöoikeudet**.
4. Valitse **Määritetyt käyttöoikeudet** -kohdassa **Lisää käyttöoikeus** ja lisää sitten delegoidut käyttöoikeudet **Microsoftin API:t** -välilehdessä seuraavasti:
    * Business Central: lisää **Financials.ReadWrite.All**-käyttöoikeudet.
    * Dynamics CRM: lisää **user_impersonation**-käyttöoikeudet.  

    > [!NOTE]
    > Dynamics CRM -API:n nimi voi muuttua.

5. Valitse **Hallinta**-kohdassa **Varmenteet ja salaiset avaimet** ja lue sitten sovellukselle uusi salaisuus. Salaista avainta joko käytetään [!INCLUDE[prod_short](includes/prod_short.md)]in **Common Data Service -yhteyden määritys** -sivun **Asiakasohjelman salainen avain** -kentässä tai se tallennetaan suojattuun tallennustilaan, josta se annetaan tapahtumaan tilaajassa aiemmin tässä aiheessa kuvatulla tavalla.
6. Valitse **Yleiskuvaus** ja etsi sitten **Sovelluksen (asiakasohjelman) tunnus** -arvo. Tämä on sovelluksen asiakasohjelman tunnus. Se on joko annettava **Common Data Service -yhteyden määritys** -sivun **Asiakasohjelman tunnus** -kentässä tai tallennettava suojattuun tallennustilaan tapahtuman tilaajassa annettavaksi.
7. Anna [!INCLUDE[prod_short](includes/prod_short.md)]in **Common Data Service -yhteyden määritys** -sivun **Ympäristön URL-osoite** -kentässä [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -ympäristön URL-osoite.
8. [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -yhteys otetaan käyttöön **Käytössä**-valitsimella.
9. Käytä kirjautumiseen Azure Active Directoryn järjestelmänvalvojan tiliä. (Tämä tili tarvitsee voimassaolevan [!INCLUDE[cds_long_md](includes/cds_long_md.md)]n käyttöoikeuden, ja sen on oltava [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -ympäristön järjestelmänvalvoja.) Kirjautumisen jälkeen sinua pyydetään antamaan rekisteröidylle sovellukselle lupa kirjautua [!INCLUDE[cds_long_md](includes/cds_long_md.md)]en organisaation puolesta. Määrityksen valmistumisen edellyttää tämän luvan antamista.

   > [!NOTE]
   > Jos sinua ei pyydetä käyttämään kirjautumiseen järjestelmänvalvojan tiliä, syynä on luultavasti estetyt ponnahdusikkunat. Kirjautumista varten on sallittava ponnahdusikkunat osoitteesta `https://login.microsoftonline.com`.

#### <a name="using-another-idtable-and-access-management-service"></a>Jonkin muun Idtable- ja käyttöoikeuspalvelun käyttäminen

Jos Azure Active Directorya ei käytetä käyttäjätietojen ja käyttöoikeuksien hallintaa, apua on pyydettävä kehittäjältä. Jos haluat tallentaa sovelluksen tunnuksen ja salaisen avaimen eri sijaintiin, Asiakasohjelman tunnus- ja Asiakasohjelman salainen avain -kentät voidaan jättää tyhjäksi. Tunnuksen ja salaisen avaimen sijainnista noutoa varten on siinä tapauksessa kirjoitettava laajennus. Salainen avain voidaan antaa suorituspalvelussa tilaamalla OnGetCDSConnectionClientId- ja OnGetCDSConnectionClientSecret-tapahtumat codeunitissa 7201 CDS Integration Impl.

### <a name="to-disconnect-from-cds_long_md"></a>[!INCLUDE[cds_long_md](includes/cds_long_md.md)] -yhteyden katkaiseminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Common Data Service -yhteyden määritys** ja valitse sitten liittyvä linkki.
2. Poista käytöstä **Common Data Service -yhteyden määritys** -sivulla **Käytössä**-valitsin.  

## <a name="see-also"></a>Katso myös

[Synkronoinnin tilan näyttäminen](admin-how-to-view-synchronization-status.md)  
