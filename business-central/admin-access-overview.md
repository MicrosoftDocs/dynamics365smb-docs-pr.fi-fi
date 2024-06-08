---
title: Business Centraliin pääsyn hallinta
description: Järjestelmänvalvojat käyttävät monitasoista lähestymistapaa Business Centralin ja sen ominaisuuksien käytön valvontaan.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="manage-access-to-business-central"></a>Business Centraliin pääsyn hallinta

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Tämä artikkeli antaa järjestelmänvalvojille ja sovelluskehittäjille korkean tason yleiskatsauksen siitä, miten [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman ja sen toimintojen käyttöä hallitaan. Linkkien avulla voit siirtyä muihin artikkeleihin, joissa on lisätietoja aiheista.

## <a name="layered-access"></a>Monitasoiset käyttöoikeudet

[!INCLUDE [prod_short](includes/prod_short.md)] käyttää monitasoista lähestymistapaa sovellusten suojaukseen seuraavassa kaaviossa kuvatulla tavalla. Saat lisätietoja kustakin tasosta siirtymällä [Sovelluksen suojaus Business Centralissa](/dynamics365/business-central/dev-itpro/security/security-application) -kohtaan.

:::image type="content" source="media/security-overview.png" alt-text="Monitasoinen sovellusten suojaus Business Centralissa.":::

## <a name="licenses"></a>Käyttöoikeudet

[!INCLUDE [prod_short](includes/prod_short.md)] -käyttäjille annetaan **Dynamics 365 Business Central** -käyttöoikeus, jotta he voivat tarkastella, muokata ja käsitellä liiketoimintatietojaan mistä tahansa käyttöliittymästä. Lisätietoja käyttöoikeuksista on kohdassa [Dynamics 365 Business Centralin käyttöoikeudet](/dynamics365/business-central/dev-itpro/deployment/licensing).

Kuitenkin ihmiset, jotka joskus tarvitsevat vain luku-oikeuden saadakseen tietoja [!INCLUDE [prod_short](includes/prod_short.md)] -ohjemassa voivat käyttää **Microsoft 365** -käyttöoikeutta. Lisätietoja rajattujen käyttöoikeuksien antamisesta on kohdassa [Business Centralin käyttäminen Microsoft 365 -käyttöoikeuksilla](admin-access-with-m365-license.md).

Perusteellisia tietoja erilaisista käyttöoikeustyypeistä ja [!INCLUDE[prod_short](includes/prod_short.md)]in käyttöoikeuksista on [ladattavassa Dynamics 365:n käyttöoikeusoppaassa](https://go.microsoft.com/fwlink/?LinkId=866544).

## <a name="business-central-administrator-tasks"></a>Business Centralin järjestelmänvalvojan tehtävät

Seuraavassa taulukossa on luettelo siitä, miten järjestelmänvalvojat voivat hallita [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman käyttöoikeuksia ja mitä ominaisuuksia käyttäjät käyttävät. Jotkin tehtävät auttavat myös pitämään käyttöoikeusasetukset ajan tasalla.

|Tehtävä| Lisätietoja |
|--|--|--|
|Jokaisella käyttäjällä on oltava käyttäjätili, ennen kuin he voivat kirjautua sisään [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan. Helpoin tapa määrittää käyttäjät on lisätä ne yksitellen [Microsoft 365 -hallintakeskukseen](https://go.microsoft.com/fwlink/p/?linkid=2024339). |[Käyttäjien lisääminen ja käyttöoikeuksien määrittäminen samalla kertaa](/microsoft-365/admin/add-users/add-users)|
|Hallitse kaikkien käyttäjien käyttöoikeuksia ympäristön tasolla. Luo Microsoft Entra -suojausryhmä ja määritä se ympäristöön.<br><br> Suojausryhmien avulla voit myös hallita tiettyjen käyttäjäryhmien käyttöä. | [Ympäristöjen käyttöoikeuksien hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Business Centralin käyttöoikeuden hallinta suojausryhmien avulla](ui-security-groups.md) |
|Luo käyttäjiä [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan ja määritä, ketkä voivat kirjautua sisään. | [Käyttäjien luominen käyttöoikeuksien mukaan](ui-how-users-permissions.md) |
|Yhdessä käyttäjäoikeuksien kanssa käyttöoikeudet määrittelevät objektit, joita käyttäjä voi käyttää kussakin tietokannassa tai ympäristössä. Määritä, voivatko ihmiset lukea, muokata tai syöttää tietoja tietokantaobjekteissa. |[Käyttöoikeuksien delegoiminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)|
|Jos ulkopuolinen kirjanpitäjä hallinnoi teoksiaan ja taloudellista raportointia, kutsu ne [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaasi. He pystyvät työskentelemään tiiviimmin kanssasi verotietojen parissa.|[Kirjanpitäjän käyttökokemukset [!INCLUDE[prod_long](includes/prod_long.md)]issa](finance-accounting.md)|
|Jos olet [!INCLUDE [prod_short](includes/prod_short.md)] -jälleenmyyntisopimuksen osapuoli, voit lähettää asiakkaalle sähköpostiviestin, jossa pyydät jälleenmyyjäsuhdetta. Voit sisällyttää sähköpostiviestiin delegoituja järjestelmänvalvojaoikeuksia Microsoft Entra ID:hen ja Microsoft 365:een.| [Delegoitu järjestelmänvalvojan käyttöoikeus Business Central Onlineen](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|Azure-huoltotunniste edustaa ryhmää IP-osoitteita, joista palvelun liikenne voi tulla tai joihin se voi siirtyä. Huoltotunnisteiden avulla voit määrittää palomuurit sallimaan liikenteen vain tietyistä palveluista. **Dynamics365BusinessCentral**-tunnisteen avulla voit käyttää palomuurin ja verkon suojausryhmän sääntöjä liikenteen rajoittamiseen [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan ja -ohjelmasta.| [Azure-suojauspalvelun tunnisteet](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|Käyttäessäsi Microsoft Entra -todennusta [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa, on suositeltavaa hyödyntää [Microsoft Entra ID:n monimenetelmäistä todentamista (MFA)](/azure/active-directory/authentication/concept-mfa-howitworks). MFA antaa lisäturvaa hakemuksen ja datan käyttöön.|[Dynamics 365 Business Centralin monimenetelmäinen todentaminen](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## <a name="business-central-developer-tasks"></a>Business Central -sovelluksen kehittäjätehtävät

[!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman käyttöoikeuden hallintaan on myös kehittäjän tarina. Kehittäjät ja järjestelmänvalvojat voivat esimerkiksi muodostaa ja yhdistää liiketoimintaa hyödyntäviä sovelluksia [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmaan:  

* Liiketoimintaprosessien yksinkertaistaminen
* Paranna asiakaskontakteja
* Tee parempia päätöksiä, nopeammin

Seuraavassa taulukossa on linkit tietoihin siitä, kuinka sovelluksille ja laajennuksille annetaan käyttöoikeus [!INCLUDE [prod_short](includes/prod_short.md)] -tietoihin.

| Tehtävä | Lisätietoja |
|--|--|
|Ominaisuuksien käytön määrittämisen kaksi pääkäsitettä ovat oikeudet ja käyttöoikeudet. Käyttöoikeudet antavat objektien laajan käyttöoikeuden Microsoft Entra -käyttöoikeuksien tai -roolien mukaan. Käyttöoikeuksien ja käyttöoikeusjoukkojen avulla voit hienosäätää objektien käyttöä. |[Oikeuksien ja käyttöoikeusjoukkojen yleiskuvaus](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## <a name="see-also"></a>Katso myös

[Suojaus Business Centralissa](/dynamics365/business-central/dev-itpro/security/security-and-protection)
