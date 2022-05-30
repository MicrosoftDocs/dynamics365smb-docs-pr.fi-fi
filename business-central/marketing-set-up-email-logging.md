---
title: Määritä sähköpostin lokiinkirjaus
description: Lisätietoja siitä, miten myyjien ja asiakkaiden sähköpostivuorovaikutukset voidaan muuttaa todellisiksi myyntimahdollisuuksiksi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 03/22/2022
ms.search.form: 1680, 1811, 5076
ms.author: bholtorf
ms.openlocfilehash: e14e3b353cd06d348de36c23caa4bcfb1981a6e5
ms.sourcegitcommit: 2fa712d0aabe4287ebd4454c28d142d6baf045a0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/09/2022
ms.locfileid: "8729935"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Myyjien ja yhteyshenkilöiden välisten sähköpostiviestien seuraaminen
Saat enemmän hyötyä myyjien ja asiakkaiden välisestä viestinnästä, jos muunnat sähköpostiviestit toiminnallisiksi mahdollisuuksiksi. [!INCLUDE[prod_short](includes/prod_short.md)] -sovellusta voi käyttää yhdessä Exchange Onlinen kanssa. Näin voit seurata saapuvia ja lähteviä viestejä. Voit tarkastella ja analysoida kunkin viestin sisältöä **Vuorovaikutuslokin tapahtumat** -sivulla.

> [!NOTE]
> Vuoden 2022 julkaisuaallossa 1 olemme yksinkertaistaneet sähköpostin lokiinkirjauksen käyttöönottoprosesseja joustavuuden ja suojauksen lisäämiseksi. Jos olet uusi asiakas, joka käyttää kyseistä versiota, käytät uutta käyttökokemusta. Jos olet jo asiakas, uuden käyttökokemuksen käyttö riippuu siitä, onko järjestelmänvalvoja ottanut käyttöön **Sähköpostin lokiinkirjaus Microsoft Graph API:n avulla** -ominaisuuden päivityksen **Ominaisuuksien hallinta** -sivulla. Lisätietoja on kohdassa [Tulevien ominaisuuksien ottaminen käyttöön etuajassa](/dynamics365/business-central/dev-itpro/administration/feature-management).

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] onlinen kohdalla uusi kokemus edellyttää, että [!INCLUDE[prod_short](includes/prod_short.md)] ja Exchange Online ovat samalla vuokraajalla.

## <a name="to-set-up-email-logging"></a>Määritä sähköpostin lokiinkirjaus
Nämä vaiheet vaihtelevat sen mukaan, onko järjestelmänvalvoja ottanut käyttöön **Sähköpostin lokiinkirjaus Microsoft Graph API:n avulla** -ominaisuuspäivityksen. Jos ominaisuuspäivitystä ei ole otettu käyttöön, noudata **Nykyinen kokemus** -välilehdessä olevia ohjeita.

## <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience)

### <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Yleisten kansioiden ja sääntöjen määrittäminen sähköpostin lokiinkirjausta Exchange Onlinessa

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Seuraavaksi [!INCLUDE[prod_short](includes/prod_short.md)] yhdistetään Exchange Onlineen.

## <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience)
### <a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online"></a>Jaetun postilaatikon määrittäminen sähköpostin lokiinkirjausta varten kohteessa Exchange Online

> [!NOTE]
> Nämä vaiheet edellyttävät järjestelmänvalvojan oikeuksia kohteelle Exchange Online.

Valmistele jaettu postilaatikko Exchange-hallintakeskuksessa. Vaihtoehtoisesti voit myös käyttää Exchange Online PowerShelliä. Lisätietoja on ohjeaiheessa [Jaetun postilaatikon luominen](/microsoft-365/admin/email/create-a-shared-mailbox) tai [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Jos käytät Exchange Management PowerShelliä, muutokset tulevat näkyviin Exchangen hallintakeskuksessa viiveen jälkeen. Viive voi olla useita tunteja.

### <a name="add-a-user-account-for-members-of-the-shared-mailbox"></a>Käyttäjätilin lisääminen jaetun postilaatikon jäsenille
Sähköpostin lokiinkirjauksessa käytettävä tili on Exchange Online-tili. Aikataulutettu projekti muodostaa yhteyden jaettuun postilaatikkoon ja käsittelee sähköpostiviestit tilin avulla. Tätä tiliä ei tulisi liittää tiettyyn henkilöön. Lisää sähköpostitili jaetun postilaatikon jäsenille. Lisätietoja on ohjeaiheessa [Jaetun postilaatikon delegoimisen muokkaus EAC-määrityksen avulla](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### <a name="allow-other-users-to-see-logged-emails"></a>Salli muiden käyttäjien nähdä lokiin kirjatut sähköpostit
Voit antaa toisen käyttäjän avata Exchangessa sähköpostiviestin, joka liittyy vuorovaikutuslokitapahtumaan kohteesta [!INCLUDE[prod_short](includes/prod_short.md)]. Jos haluat tehdä niin, anna käyttäjälle jaetun postilaatikon ``Read``-käyttöoikeus **Arkisto**-kansioon. Lisätietoja on kohdassa [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### <a name="create-mail-flow-rules"></a>Sähköpostin työnkulkusääntöjen luominen
Sähköpostin työnkulkusäännöt etsivät viesteistä tiettyjä ehtoja ja toteuttavat niitä koskevia toimia. Kahden postityönkulkusäännön luonti seuraavan taulukon tietojen perusteella. Lisätietoja on kohdassa [Postityönkulkusääntöjen hallinta Exchange Onlinessa](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) ja [Postityönkulkusäännön toiminnot Exchange Onlinessa](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Tarkoitus  |Name  |Käytä tätä sääntöä, jos...  |Tee seuraavat toiminnot...  |
|---------|---------|---------|---------|
|Saapuvan sähköpostin sääntö     |Lokin sähköposti lähetetty tälle organisaatiolle|Lähettäjä sijaitsee organisaation ulkopuolella ja vastaanottaja sijaitsee organisaation sisäpuolella|Piilokopion lähettäminen jaetulle postilaatikolle määritetylle sähköpostitilille.|
|Lähtevän sähköpostin sääntö     |Lokin sähköposti lähetetty tästä organisaatiosta|Lähettäjä sijaitsee organisaation sisäpuolella ja vastaanottaja sijaitsee organisaation ulkopuolella.|Piilokopion lähettäminen jaetulle postilaatikolle määritetylle sähköpostitilille.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] käsittelee vain jaetun postilaatikon Saapuneet-kansion viestit. Jos sääntö siirtää viestit Saapuneet-kansiosta toiseen kansioon, viestejä ei käsitellä. Lisäksi roskapostikansion viestit ohitetaan. 

---

## <a name="set-up-prod_short-to-log-email-messages"></a>Määritä [!INCLUDE[prod_short](includes/prod_short.md)] -sovellus sähköpostiviestien kirjaamista varten
Nämä vaiheet ovat samat sekä nykyisille että uusille kokemuksille.

Aloita sähköpostien kirjaaminen seuraavien kahden helpon vaiheen avulla:

1. Muodosta yhteys [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen Exchange Onlinen avulla Microsoft 365 -tilauksessa. Exchange Online käsittelee sähköpostiviestisi. Tämä on helppo tehdä asetusten ohjatun määrityksen oppaan avulla. Tarvitset vain järjestelmänvalvojan tunnistetiedot Microsoft 365:n järjestelmänvalvojan tiliä varten. Aloita oppaan käyttäminen siirtymällä **Asetusten ohjattu määritys** -sivulle ja valitsemalla **Määritä sähköpostin lokiinkirjaus** -oppaan.  

2. Varmista, että myyntihenkilöiden ja yhteyshenkilöidesi sähköpostiosoitteet kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] ovat voimassa. Tee tämä avaamalla kunkin asiakkaan tai myyjän **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortti ja tarkistamalla **Sähköposti**-kenttä.

> [!Tip]
> Kun olet tehnyt nämä oppaan vaiheet, voit tarkistaa yhteyden tilan. Valitse jompikumpi seuraavista vaiheista sen mukaan, onko käytössä nykyinen vai uusi kokemus: 
>
> * **Nykyinen kokemus**: Etsi **Kontaktienhallinnan asetukset**, valitse **Käytä** ja sitten **Toiminnot**. Valitse lopuksi **Tarkista sähköpostin lokiinkirjauksen asetukset**.
> * **Uusi kokemus**: Etsi **Sähköpostin lokiinkirjaus**, valitse **Toiminnot** ja valitse sitten **Tarkista asetukset**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Sähköpostiviestien tarkasteleminen vuorovaikutuslokissa

[!INCLUDE[prod_short](includes/prod_short.md)] luo **Vuorovaikutusloki**-sivulle tapahtuman aina, kun myyjä ja yhteyshenkilö lähettävät sähköpostiviestejä. Voit tarkastella vuorovaikutuslokia avaamalla **Yhteyshenkilö**-kortin, valitsemalla sitten **Liittyvä** ja valitsemalla sitten **Historia**- ja **Vuorovaikutuslokin tapahtumat**. Lokin tapahtumille voi tehdä esimerkiksi seuraavia toimintoja:

- Voit tarkastella sähköpostiviestin sisältöä valitsemalla **Prosessi** ja sitten **Näytä liitteet** -toiminnon.
- Voit muuttaa sähköpostiviestinnän myyntimahdollisuudeksi. Jos tapahtuma näyttää lupaavalta, voit muuttaa sen mahdollisuudeksi, jonka jälkeen siitä voi kehittyä myyntiä. Jos haluat muuttaa sähköpostiviestinnän myyntimahdollisuudeksi, valitse tapahtuma, sitten **Käsittely** ja sitten **Luo mahdollisuus**. Lisätietoja on kohdassa [Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md).

## <a name="mailbox-and-folder-limits-in-exchange-online"></a>Exchange Onlinen postilaatikon ja kansion rajat
Exchange Onlinessa on postilaatikon ja kansion rajoituksia, kuten kansioiden kokojen rajoitukset ja viestien lukumäärä. Lisätietoja on kohdassa [Exchange Online -rajoitukset](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) ja [Yleisten kansioiden rajoitukset Exchange Serverissa](/Exchange/collaboration/public-folders/limits?view=exchserver-2019).

[!INCLUDE[prod_short](includes/prod_short.md)] tallentaa lokiin kirjatut sähköpostiviestit kansioon Exchange Onlinessa. [!INCLUDE[prod_short](includes/prod_short.md)] tallentaa myös linkin jokaiseen lokiin kirjattuun viestiin. Linkit avaavat lokiin kirjatut viestit Exchange Onlinessa vuorovaikutuslokin tapahtumat-, kontaktikortti- ja myyjäkorttisivuista [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Jos kirjattu viesti siirretään toiseen kansioon, linkki katkeaa. Viesti saatetaan siirtää esimerkiksi manuaalisesti tai Exchange Online voi automaattisesti aloittaa automaattisen jakamisen, kun tallennusraja saavutetaan.

Seuraavien vaiheiden avulla voit välttää Exchange Online -ohjelman viestien linkkien katkeamisen.

1. Älä siirrä aiemmin luotuja viestejä toiseen kansioon sen jälkeen, kun olet muuttanut sähköpostin kirjaamisasetusten asetuksia. Säilytetään olemassa olevia viestejä, jos ne säilyttävät linkit. Linkit uuden kansion viesteihin ovat voimassa.
2. Postilaatikon ja kansion rajoitusten välttäminen. Jos olet saavuttamassa rajoituksen, tee seuraavat toimet:
    1. Määritä uusi jaettu postilaatikko (uusi käyttökokemus) tai uusi jaettu kansio (tämänhetkinen käyttökokemus) Exchange Online -ohjelmaan.
    2. Päivitä sähköpostityökulun säännöt Exchange Onlineen.
    3. Päivitä sähköpostin kirjaamisasetukset Business Centralissa sen mukaisesti

## <a name="connect-on-premises-versions-to-microsoft-exchange"></a>Yhdistä on-premises-versiot Microsoft Exchangeen

Voit muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -ratkaisusta paikalliseen Exchange on-premisesiin tai Exchange Onlineen sähköpostin lokiinkirjaamiseksi. Molemmissa Exchange-versioissa yhteyden asetukset ovat käytettävissä **Kontaktienhallinnan asetukset** -sivulla. Exchange Onlinessa voit käyttää myös avustettua asennusopasta.

> [!IMPORTANT]
> Uusi kokemus ei tue yhteyttä paikalliseen Exchangeen. Jos sinun täytyy käyttää paikallista Exchangea, älä ota ominaisuuden päivitystä käyttöön uutta kokemusta varten.

## <a name="connect-to-exchange-on-premises"></a>Yhdistä Exchange On-Premisesiin
## <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience)
Jos haluat yhdistää [!INCLUDE[prod_short](includes/prod_short.md)] on-premisesin Exchange on-premisesiin, voit käyttää **Kontaktienhallinnan asetukset** -sivulla **Perus**-vaihtoehtoa **todennustyyppinä** ja kirjoittaa sitten Exchange on-premisesin käyttäjätilin tunnistetiedot. Aloita sitten sähköpostin lokiinkirjaaminen valitsemalla **Käytössä**-valitsin.

## <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience)
Uusi kokemus ei tue yhteyksiä paikalliseen Exchangeen.

---

## <a name="connect-to-exchange-online"></a>Yhdistä tuotteeseen Exchange Online
Jotta voisit muodostaa yhteyden kohteeseen Exchange Online, sinun täytyy rekisteröidä sovellus kohteessa Azure Active Directory. Anna sovelluksen tunnus, avainsäilön salaisuus ja uudelleenohjauksen URL-osoite rekisteröintiä varten. Uudelleenohjauksen URL-osoite määritetään valmiiksi, ja sen pitäisi toimia useimmissa asennuksissa. Lisätietoja on kohdassa [Sovelluksen rekisteröiminen Azure AD:ssä yhteyden muodostamiseksi Business Centralista Exchange Onlineen](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Sinun on myös käytettävä **OAuth2**-arvoa **todennustyyppinä**. Sinun täytyy myös rekisteröidä sovellus kohteessa Azure Active Directory. Anna sovelluksen tunnus, avainsäilön salaisuus ja uudelleenohjauksen URL-osoite rekisteröintiä varten. Uudelleenohjauksen URL-osoite täytetään valmiiksi, ja sen pitäisi toimia useimmissa asennuksissa. Lisätietoja on kohdassa Sovelluksen rekisteröiminen Azure AD:ssä yhteyden muodostamiseksi Business Centralista Exchange Onlineen.

Asennus on määritettävä käyttämään HTTPS-yhteyttä. Lisätietoja on kohdassa [SSL:n määrittäminen suojaamaan Business Centralin verkkoasiakasohjelman yhteyttä](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Jos palvelimelle määritetään jokin muu aloitussivu, URL-osoitteen voi vaihtaa. Asiakasohjelman salaisuus tallennetaan tietokantaan salattuna merkkijonona.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Sovelluksen rekisteröiminen Azure AD:ssä muodostamaan yhteys Business Centralista Exchange Onlineen
Seuraavissa vaiheissa oletetaan, käyttäjätietojen ja käyttöoikeuksien hallintaan käytetään Azure Active Directory:tä. Lisätietoja on kohdassa [Pika-aloitus: sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristössä](/azure/active-directory/develop/quickstart-register-app). 

## <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience) 
Seuraavissa vaiheissa oletetaan, käyttäjätietojen ja käyttöoikeuksien hallintaan käytetään Azure Active Directory:tä. Lisätietoja on kohdassa [Pika-aloitus: sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristössä](/azure/active-directory/develop/quickstart-register-app). Jos Azure Active Directory ei ole käytössä, lisätietoja on kohdassa [Jonkin muun käyttäjätieto- ja käyttöoikeuspalvelun käyttäminen](marketing-set-up-email-logging.md#use-another-identity-and-access-management-service). 

1. Valitse Azure-portaalin **Hallinta**-kohdassa **Todennus**.
2. Lisää **Uudelleenohjauksen URL-osoite** -kohdassa [!INCLUDE[prod_short](includes/prod_short.md)]in **Kontaktienhallinnan asetukset** -sivulla ehdotettu uudelleenohjauksen URL-osoite. Jos Kontaktienhallinnan asetukset -sivun uudelleenohjauksen URL-osoite on tyhjä, etsi ehdotettu uudelleenohjauksen URL-osoite **Sähköpostin lokiinkirjauksen asetusten ohjattu määritys** -sivulta.

    > [!NOTE]
    > Jos et määritä uudelleenohjauksen URL-osoitetta, voit tehdä sen myöhemmin valitsemalla **Lisää ympäristö** ja valitsemalla sitten **Verkko**, jos haluat lisätä verkkosovelluksen ja uudelleenohjauksen URL-osoitteen. 

3. Valitse **Hallinta**-kohdassa **Kokoonpanotiedot**.
4. Etsi kokoonpanotiedoista **requiredResourceAccess**-ominaisuus luetteloluettelosta ja lisää tarvittavat käyttöoikeudet lisäämällä seuraava koodi hakasulkeisiin ([]). Lisätietoja on kohdassa [Sovelluksen rekisteröiminen](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Valitse **Tallenna**.
6. Valitse **Hallinta**-kohdassa **API-käyttöoikeudet** ja vahvista sitten, että luettelossa ovat seuraavat käyttöoikeudet:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. Valitse **Hallinta**-kohdassa **Varmenteet ja salaiset avaimet** ja lue sitten sovellukselle uusi salaisuus. Salaisuutta käytetään joko [!INCLUDE[prod_short](includes/prod_short.md)]in **Kontaktienhallinnan asetukset** -sivun **Asiakasohjelman salainen avain** -kentässä tai tallennettava suojattuun tallennustilaan tapahtuman tilaajassa annettavaksi.
8. Valitse **Yleiskuvaus** ja etsi sitten **Sovelluksen (asiakasohjelman) tunnus** -arvo. **Sovelluksen (asiakkaan) tunnus** -arvo on sovelluksen asiakastunnus. Asiakastunnus on joko annettava **Kontaktienhallinnan asetukset** -sivun **Asiakasohjelman tunnus** -kentässä tai tallennettava suojattuun tallennustilaan tapahtuman tilaajassa annettavaksi.
9. Määritä [!INCLUDE[prod_short](includes/prod_short.md)]issa sähköpostin lokiinkirjaus **Kontaktienhallinnan asetukset** -sivulla tai käytä **Sähköpostin lokiinkirjauksen asetusten ohjattu määritys** -asennusopasta prosessin apuna.
    * Anna sen käyttäjän sähköpostitili, jonka puolesta aikataulutettu projekti muodostaa Exchange Online -yhteyden ja käsittelee sähköpostiviestit. Käyttäjällä on oltava voimassa oleva Exchange Online -käyttöoikeus.
    * Anna Exchange Onlinen URL-osoite. Yleensä tämä URL on toimialue, jonka olet määrittänyt käyttäjän sähköpostiosoitteessa.
    * Anna **Jonon kansiopolku** ja **Tallennuskansion polku**.
10. Aloita sitten sähköpostin lokiinkirjaaminen valitsemalla **Käytössä**-valitsin.
11. Käytä kirjautumiseen Azure Active Directoryn järjestelmänvalvojan tiliä. (Tämä tili tarvitsee voimassaolevan Exchangen käyttöoikeuden, ja sen on oltava Exchange Onlinen järjestelmänvalvoja.) Kirjautumisen jälkeen sinun on annettava rekisteröidylle sovellukselle lupa kirjautua Exchange Onlineen organisaation puolesta. Määrityksen valmistumisen edellyttää tämän luvan antamista.

   > [!NOTE]
   > Jos sinua ei pyydetä käyttämään kirjautumiseen järjestelmänvalvojan tiliä, syynä on luultavasti estetyt ponnahdusikkunat. Kirjautumista varten on sallittava ponnahdusikkunat osoitteesta https://login.microsoftonline.com.

## <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience)
1. Valitse Azure-portaalin **Hallinta**-kohdassa **Todennus**.
2. Lisää **Uudelleenohjauksen URL-osoite** -kohdassa [!INCLUDE[prod_short](includes/prod_short.md)]in **Sähköpostin lokiinkirjaus** -sivulla ehdotettu uudelleenohjauksen URL-osoite. Jos Sähköpostin lokiinkirjaus -sivun uudelleenohjauksen URL-kenttä on tyhjä, etsi ehdotettu uudelleenohjauksen URL-osoite **Asetusten ohjattu määritys** -sivulta. Voit avata sivun valitsemalla **Sähköpostin lokiinkirjaus** -sivulla **Toiminnot** ja valitsemalla sitten **Asetusten ohjattu määritys**.

    > [!NOTE]
    > Jos et määritä uudelleenohjauksen URL-osoitetta, voit tehdä sen myöhemmin valitsemalla **Lisää ympäristö** ja valitsemalla sitten **Verkko**, jos haluat lisätä verkkosovelluksen ja uudelleenohjauksen URL-osoitteen.

3. Valitse **Hallinta**-kohdassa **API-oikeudet** ja sitten **Microsoft Graph** ja valitse sitten **Delegoidut käyttöoikeudet**.
4. Etsi ja valitse **Sähköposti** hakuruudun avulla ja lisää sitten **Mail.ReadWrite.Shared**-oikeudet. 
5. Valitse **Hallinta**-kohdassa **Varmenteet ja salaiset avaimet** ja lue sitten sovellukselle uusi salaisuus. Voit käyttää salaisuutta joko **Asiakkaan salaisuus** -kentässä **Sähköpostin lokiinkirjaus** -kentässä kohteessa [!INCLUDE[prod_short](includes/prod_short.md)].
6. Valitse **Yleiskuvaus** ja etsi sitten **Sovelluksen (asiakasohjelman) tunnus** -arvo. Tämä on sovelluksen asiakasohjelman tunnus. Sinun täytyy syöttää se joko **Asiakastunnus** -kenttään **Sähköpostin lokiinkirjaus** -sivulla.
7. Määritä [!INCLUDE[prod_short](includes/prod_short.md)]issa sähköpostin lokiinkirjaus **Sähköpostin lokiinkirjaus** -sivulla tai käytä **Asetusten ohjattu määritys** -asennusopasta apuna.

### <a name="use-another-identity-and-access-management-service"></a>Jonkin muun käyttäjätieto- ja käyttöoikeuspalvelun käyttäminen
Jos Azure Active Directorya ei käytetä käyttäjätietojen ja käyttöoikeuksien hallintaa, apua on pyydettävä kehittäjältä. Jos haluat tallentaa sovelluksen tunnuksen ja salaisen avaimen eri sijaintiin, Asiakasohjelman tunnus- ja Asiakasohjelman salainen avain -kentät voidaan jättää tyhjäksi. Tunnuksen ja salaisen avaimen sijainnista noutoa varten on siinä tapauksessa kirjoitettava laajennus. Salainen avain voidaan antaa suorituspalvelussa tilaamalla OnGetEmailLoggingClientId- ja OnGetEmailLoggingClientSecret-tapahtumat codeunitissa 1641 "Setup Email Logging".

---

## <a name="to-start-logging-email"></a>Sähköpostin lokiinkirjaamisen aloittaminen
1. Aloita sähköpostin lokiinkirjaaminen **Sähköpostin lokiinkirjaus** -sivulla ottamalla käyttöön **Käytössä**-valitsin.
2. Kirjaudu sisään Exchange Online-tilillä, jonka avulla aikataulutettu projekti muodostaa yhteyden jaettuun postilaatikkoon ja käsittelee sähköpostiviestit tilin avulla.

    > [!NOTE]
    > Jos sinua ei pyydetä käyttämään kirjautumiseen Exchange Online-tiliä, syynä on luultavasti selaimen estetyt ponnahdusikkunat. Kirjautumista varten on sallittava ponnahdusikkunat osoitteesta https://login.microsoftonline.com.

## <a name="to-stop-logging-email"></a>Sähköpostin lokiinkirjaamisen lopettaminen
## <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience)
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktienhallinnan asetukset** ja valitse sitten vastaava linkki.
1. Poista **Käytössä**-valitsin käytöstä.

## <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience)
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköpostin lokiinkirjaus** ja valitse sitten vastaava linkki.
2. Poista **Käytössä**-valitsin käytöstä.

---

## <a name="to-change-the-user-account-used-for-email-logging"></a>Sähköpostin lokiinkirjauksessa käytetyn käyttäjätilin vaihtaminen
Jos käytät uutta kokemusta, voit vaihtaa sähköpostin lokiinkirjauksessa käytettävää käyttäjätiliä. Nykyinen kokemus ei tue tätä.

## <a name="current-experience"></a>[Nykyinen kokemus](#tab/current-experience) 
Poista käytöstä nykyiset määritykset, vaihda käyttäjä **Sähköpostin lokiinkirjaus** -sivulla ja ota sähköpostin lokiinkirjaus uudelleen käyttöön. Voit myös suorittaa asetusten ohjatun määrityksen uudelleen.

## <a name="new-experience"></a>[Uusi kokemus](#tab/new-experience)
### <a name="prod_short-online"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Online
1. Kirjaudu sisään kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)] tilillä, jonka avulla aikataulutettu projekti muodostaa yhteyden jaettuun postilaatikkoon ja käsittelee sähköpostiviestit tilin avulla. Tällä tilillä täytyy olla sekä [!INCLUDE[prod_short](includes/prod_short.md)]- että Exchange Online-oikeudet.
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköpostin lokiinkirjaus** ja valitse sitten vastaava linkki. 
3. Valitse **Aiheeseen liittyvät** ja sitten **Työjonotapahtuma**.
4. Käynnistä **Sähköpostin lokiinkirjaus** -työ uudelleen.

### <a name="prod_short-on-premises"></a>[!INCLUDE[prod_short](includes/prod_short.md)] On-Premises
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköpostin lokiinkirjaus** ja valitse sitten vastaava linkki. 
2. Valitse **Toiminnot** ja sitten **Uudista tunnus**.
3. Kirjaudu sisään Exchange Online-tilillä, jonka avulla aikataulutettu projekti muodostaa yhteyden jaettuun postilaatikkoon ja käsittelee sähköpostiviestit tilin avulla.



## <a name="see-also"></a>Katso myös
[Kontaktienhallinta](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]