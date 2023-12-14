---
title: Määritä sähköpostin lokiinkirjaus
description: 'Lisätietoja siitä, miten myyjien ja asiakkaiden sähköpostivuorovaikutukset voidaan muuttaa todellisiksi myyntimahdollisuuksiksi.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dcenic
ms.topic: how-to
ms.date: 09/18/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.search.form: '1680, 1811, 5076'
---
# Myyjien ja yhteyshenkilöiden välisten sähköpostiviestien seuraaminen

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Saat enemmän hyötyä myyjien ja asiakkaiden välisestä viestinnästä, jos muunnat sähköpostiviestit toiminnallisiksi mahdollisuuksiksi. [!INCLUDE[prod_short](includes/prod_short.md)] -sovellusta voi käyttää yhdessä Exchange Onlinen kanssa. Näin voit seurata saapuvia ja lähteviä viestejä. Voit tarkastella ja analysoida kunkin viestin sisältöä **Vuorovaikutuslokin tapahtumat** -sivulla.

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] online, [!INCLUDE[prod_short](includes/prod_short.md)] ja Exchange Online täytyy olla samassa vuokralaisessa.

## Määritä sähköpostin lokiinkirjaus

### Yleisten kansioiden ja sääntöjen määrittäminen sähköpostin lokiinkirjaukselle Exchange Onlinessa

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Seuraavaksi [!INCLUDE[prod_short](includes/prod_short.md)] yhdistetään Exchange Onlineen.

### Jaetun postilaatikon määrittäminen sähköpostin lokiinkirjausta varten kohteessa Exchange Online

> [!NOTE]
> Nämä vaiheet edellyttävät järjestelmänvalvojan oikeuksia kohteelle Exchange Online.

Valmistele jaettu postilaatikko Exchange-hallintakeskuksessa. Vaihtoehtoisesti voit myös käyttää Exchange Online PowerShelliä. Lisätietoja on ohjeaiheessa [Jaetun postilaatikon luominen](/microsoft-365/admin/email/create-a-shared-mailbox) tai [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Jos käytät Exchange Management PowerShelliä, muutokset tulevat näkyviin Exchangen hallintakeskuksessa viiveen jälkeen. Viive voi olla useita tunteja.

### Käyttäjätilin lisääminen jaetun postilaatikon jäsenille

Sähköpostin lokiinkirjauksessa käytettävä tili on Exchange Online-tili. Aikataulutettu projekti muodostaa yhteyden jaettuun postilaatikkoon ja käsittelee sähköpostiviestit tilin avulla. Tätä tiliä ei tulisi liittää tiettyyn henkilöön. Lisää sähköpostitili jaetun postilaatikon jäsenille. Lisätietoja on ohjeaiheessa [Jaetun postilaatikon delegoimisen muokkaus EAC-määrityksen avulla](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### Salli muiden käyttäjien nähdä lokiin kirjatut sähköpostit

Voit antaa toisen käyttäjän avata Exchangessa sähköpostiviestin, joka liittyy vuorovaikutuslokitapahtumaan kohteesta [!INCLUDE[prod_short](includes/prod_short.md)]. Jos haluat tehdä niin, anna käyttäjälle jaetun postilaatikon ``Read``-käyttöoikeus **Arkisto**-kansioon. Lisätietoja on kohdassa [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

### Sähköpostin työnkulkusääntöjen luominen

Sähköpostin työnkulkusäännöt etsivät viesteistä tiettyjä ehtoja ja toteuttavat niitä koskevia toimia. Kahden postityönkulkusäännön luonti seuraavan taulukon tietojen perusteella. Lisätietoja on kohdassa [Postityönkulkusääntöjen hallinta Exchange Onlinessa](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) ja [Postityönkulkusäännön toiminnot Exchange Onlinessa](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Tarkoitus  |Name  |Käytä tätä sääntöä, jos...  |Tee seuraavat toiminnot...  |
|---------|---------|---------|---------|
|Saapuvan sähköpostin sääntö     |Lokin sähköposti lähetetty tälle organisaatiolle|Lähettäjä sijaitsee organisaation ulkopuolella ja vastaanottaja sijaitsee organisaation sisäpuolella|Piilokopion lähettäminen jaetulle postilaatikolle määritetylle sähköpostitilille.|
|Lähtevän sähköpostin sääntö     |Lokin sähköposti lähetetty tästä organisaatiosta|Lähettäjä sijaitsee organisaation sisäpuolella ja vastaanottaja sijaitsee organisaation ulkopuolella.|Piilokopion lähettäminen jaetulle postilaatikolle määritetylle sähköpostitilille.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] käsittelee vain jaetun postilaatikon Saapuneet-kansion viestit. Jos sääntö siirtää viestit Saapuneet-kansiosta toiseen kansioon, viestejä ei käsitellä. Lisäksi roskapostikansion viestit ohitetaan.

## Määritä [!INCLUDE[prod_short](includes/prod_short.md)] -sovellus sähköpostiviestien kirjaamista varten

Aloita sähköpostien kirjaaminen seuraavien kahden helpon vaiheen avulla:

1. Muodosta yhteys [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen Exchange Onlinen avulla Microsoft 365 -tilauksessa. Exchange Online käsittelee sähköpostiviestisi. Tämä on helppo tehdä asetusten ohjatun määrityksen oppaan avulla. Tarvitset vain järjestelmänvalvojan tunnistetiedot Microsoft 365:n järjestelmänvalvojan tiliä varten. Aloita oppaan käyttäminen siirtymällä **Asetusten ohjattu määritys** -sivulle ja valitsemalla **Määritä sähköpostin lokiinkirjaus** -oppaan.  

2. Varmista, että myyntihenkilöiden ja yhteyshenkilöidesi sähköpostiosoitteet kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] ovat voimassa. Tee tämä avaamalla kunkin asiakkaan tai myyjän **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortti ja tarkistamalla **Sähköposti**-kenttä.

    > [!Tip]
    > Kun olet tehnyt nämä oppaan vaiheet, voit tarkistaa yhteyden tilan. Etsi **Sähköpostin lokiinkirjaus**, valitse **Toiminnot** ja valitse sitten **Tarkista asetukset**.

## Sähköpostiviestien tarkasteleminen vuorovaikutuslokissa

[!INCLUDE[prod_short](includes/prod_short.md)] luo **Vuorovaikutusloki**-sivulle tapahtuman aina, kun myyjä ja yhteyshenkilö lähettävät sähköpostiviestejä. Voit tarkastella vuorovaikutuslokia avaamalla **Yhteyshenkilö**-kortin, valitsemalla sitten **Liittyvä** ja valitsemalla sitten **Historia**- ja **Vuorovaikutuslokin tapahtumat**. Lokin tapahtumille voi tehdä esimerkiksi seuraavia toimintoja:

* Voit tarkastella sähköpostiviestin sisältöä valitsemalla **Prosessi** ja sitten **Näytä liitteet** -toiminnon.
* Voit muuttaa sähköpostiviestinnän myyntimahdollisuudeksi. Jos tapahtuma näyttää lupaavalta, voit muuttaa sen mahdollisuudeksi, jonka jälkeen siitä voi kehittyä myyntiä. Jos haluat muuttaa sähköpostiviestinnän myyntimahdollisuudeksi, valitse tapahtuma, sitten **Käsittely** ja sitten **Luo mahdollisuus**. Lisätietoja on kohdassa [Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md).

## Exchange Onlinen postilaatikon ja kansion rajat

Exchange Onlinessa on postilaatikon ja kansion rajoituksia, kuten kansioiden kokojen rajoitukset ja viestien lukumäärä. Lisätietoja on kohdassa [Exchange Online -rajoitukset](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) ja [Yleisten kansioiden rajoitukset Exchange Serverissa](/Exchange/collaboration/public-folders/limits?view=exchserver-2019&preserve-view=true).

[!INCLUDE[prod_short](includes/prod_short.md)] tallentaa lokiin kirjatut sähköpostiviestit kansioon Exchange Onlinessa. [!INCLUDE[prod_short](includes/prod_short.md)] tallentaa myös linkin jokaiseen lokiin kirjattuun viestiin. Linkit avaavat lokiin kirjatut viestit Exchange Onlinessa vuorovaikutuslokin tapahtumat-, kontaktikortti- ja myyjäkorttisivuista [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa. Jos kirjattu viesti siirretään toiseen kansioon, linkki katkeaa. Viesti saatetaan siirtää esimerkiksi manuaalisesti tai Exchange Online voi automaattisesti aloittaa automaattisen jakamisen, kun tallennusraja saavutetaan.

Seuraavien vaiheiden avulla voit välttää Exchange Online -ohjelman viestien linkkien katkeamisen.

1. Älä siirrä aiemmin luotuja viestejä toiseen kansioon sen jälkeen, kun olet muuttanut sähköpostin kirjaamisasetusten asetuksia. Säilytetään olemassa olevia viestejä, jos ne säilyttävät linkit. Linkit uuden kansion viesteihin ovat voimassa.
2. Postilaatikon ja kansion rajoitusten välttäminen. Jos olet saavuttamassa rajoituksen, tee seuraavat toimet:
    1. Määritä uusi jaettu postilaatikko Exchange Onlineen.
    2. Päivitä sähköpostityökulun säännöt Exchange Onlineen.
    3. Päivitä sähköpostin kirjaamisasetukset Business Centralissa sen mukaisesti

## Yhdistä on-premises-versiot Microsoft Exchangeen

Voit muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -ratkaisusta paikalliseen Exchange on-premisesiin tai Exchange Onlineen sähköpostin lokiinkirjaamiseksi. Molemmissa Exchange-versioissa yhteyden asetukset ovat käytettävissä **Kontaktienhallinnan asetukset** -sivulla. Exchange Onlinessa voit käyttää myös avustettua asennusopasta.

<!-- [!IMPORTANT]
> The new experience doesn't support a connection to Exchange on-premises. If you must use Exchange on-premises, do not enable the feature update for the new experience.

## Connect to Exchange on-premises
<!--
## [Current Experience](#tab/current-experience)
To connect [!INCLUDE[prod_short](includes/prod_short.md)] on-premises to Exchange on-premises, on the **Marketing Setup** page, you can use **Basic** as the **Authentication Type**, and then enter credentials for the user account for Exchange on-premises. Then turn on the **Enabled** toggle to start logging email.

## [New Experience](#tab/new-experience)
The new experience does not support connections to Exchange on-premises.
-->
## Yhdistä tuotteeseen Exchange Online

Jotta voisit muodostaa yhteyden kohteeseen Exchange Online, sinun täytyy rekisteröidä sovellus Microsoft Entra ID:ssä. Anna sovelluksen tunnus, avainsäilön salaisuus ja uudelleenohjauksen URL-osoite rekisteröintiä varten. Uudelleenohjauksen URL-osoite määritetään valmiiksi, ja sen pitäisi toimia useimmissa asennuksissa. Lisätietoja on kohdassa [Sovelluksen rekisteröiminen Microsoft Entra ID:ssä yhteyden muodostamiseksi Business Centralista Exchange Onlineen](#to-register-an-application-in-microsoft-entra-id-for-connecting-from-business-central-to-exchange-online). 

Sinun on myös käytettävä **OAuth2**-arvoa **todennustyyppinä**. Sinun täytyy myös rekisteröidä sovellus Microsoft Entra ID:ssä. Anna sovelluksen tunnus, avainsäilön salaisuus ja uudelleenohjauksen URL-osoite rekisteröintiä varten. Uudelleenohjauksen URL-osoite täytetään valmiiksi, ja sen pitäisi toimia useimmissa asennuksissa. Lisätietoja on kohdassa Sovelluksen rekisteröiminen Microsoft Entra ID:ssä yhteyden muodostamiseksi Business Centralista Exchange Onlineen.

Asennus on määritettävä käyttämään HTTPS-yhteyttä. Lisätietoja on kohdassa [SSL:n määrittäminen suojaamaan Business Centralin verkkoasiakasohjelman yhteyttä](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Jos palvelimelle määritetään jokin muu aloitussivu, URL-osoitteen voi vaihtaa. Asiakasohjelman salaisuus tallennetaan tietokantaan salattuna merkkijonona.

### Sovelluksen rekisteröiminen Microsoft Entra ID:ssä muodostamaan yhteys Business Centralista Exchange Onlineen

Seuraavissa vaiheissa oletetaan, käyttäjätietojen ja käyttöoikeuksien hallintaan käytetään Microsoft Entra ID:tä. Lisätietoja on kohdassa [Pika-aloitus: sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristössä](/azure/active-directory/develop/quickstart-register-app). 

1. Valitse Azure-portaalin **Hallinta**-kohdassa **Todennus**.
2. Lisää **Uudelleenohjauksen URL-osoite** -kohdassa [!INCLUDE[prod_short](includes/prod_short.md)]in **Sähköpostin lokiinkirjaus** -sivulla ehdotettu uudelleenohjauksen URL-osoite. Jos Sähköpostin lokiinkirjaus -sivun uudelleenohjauksen URL-kenttä on tyhjä, etsi ehdotettu uudelleenohjauksen URL-osoite **Asetusten ohjattu määritys** -sivulta. Voit avata sivun valitsemalla **Sähköpostin lokiinkirjaus** -sivulla **Toiminnot** ja valitsemalla sitten **Asetusten ohjattu määritys**.

    > [!NOTE]
    > Jos et määritä uudelleenohjauksen URL-osoitetta, voit tehdä sen myöhemmin valitsemalla **Lisää ympäristö** ja valitsemalla sitten **Verkko**, jos haluat lisätä verkkosovelluksen ja uudelleenohjauksen URL-osoitteen.

3. Valitse **Hallinta**-kohdassa **API-oikeudet** ja sitten **Microsoft Graph** ja valitse sitten **Delegoidut käyttöoikeudet**.
4. Etsi ja valitse **Sähköposti** hakuruudun avulla ja lisää sitten **Mail.ReadWrite.Shared**-oikeudet. 
5. Valitse **Hallinta**-kohdassa **Varmenteet ja salaiset avaimet** ja lue sitten sovellukselle uusi salaisuus. Voit käyttää salaisuutta joko **Asiakkaan salaisuus** -kentässä **Sähköpostin lokiinkirjaus** -kentässä kohteessa [!INCLUDE[prod_short](includes/prod_short.md)].
6. Valitse **Yleiskuvaus** ja etsi sitten **Sovelluksen (asiakasohjelman) tunnus** -arvo. Tämä on sovelluksen asiakasohjelman tunnus. Sinun täytyy syöttää se joko **Asiakastunnus** -kenttään **Sähköpostin lokiinkirjaus** -sivulla.
7. Määritä [!INCLUDE[prod_short](includes/prod_short.md)]issa sähköpostin lokiinkirjaus **Sähköpostin lokiinkirjaus** -sivulla tai käytä **Asetusten ohjattu määritys** -asennusopasta apuna.

### Jonkin muun käyttäjätieto- ja käyttöoikeuspalvelun käyttäminen

Jos Microsoft Entra ID:tä ei käytetä käyttäjätietojen ja käyttöoikeuksien hallintaa, apua on pyydettävä kehittäjältä. Jos haluat tallentaa sovelluksen tunnuksen ja salaisen avaimen eri sijaintiin, Asiakasohjelman tunnus- ja Asiakasohjelman salainen avain -kentät voidaan jättää tyhjäksi. Tunnuksen ja salaisen avaimen sijainnista noutoa varten on siinä tapauksessa kirjoitettava laajennus. Salainen avain voidaan antaa suorituspalvelussa tilaamalla OnGetEmailLoggingClientId- ja OnGetEmailLoggingClientSecret-tapahtumat codeunitissa 1641 "Setup Email Logging".

## Sähköpostin lokiinkirjaamisen aloittaminen

1. Aloita sähköpostin lokiinkirjaaminen **Sähköpostin lokiinkirjaus** -sivulla ottamalla käyttöön **Käytössä**-valitsin.
2. Kirjaudu sisään Exchange Online-tilillä, jonka avulla aikataulutettu projekti muodostaa yhteyden jaettuun postilaatikkoon ja käsittelee sähköpostiviestit tilin avulla.

    > [!NOTE]
    > Jos sinua ei pyydetä käyttämään kirjautumiseen Exchange Online-tiliä, syynä on luultavasti selaimen estetyt ponnahdusikkunat. Kirjautumista varten on sallittava ponnahdusikkunat osoitteesta https://login.microsoftonline.com.

## Sähköpostin lokiinkirjaamisen lopettaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköpostin lokiinkirjaus** ja valitse sitten vastaava linkki.
2. Poista **Käytössä**-valitsin käytöstä.

## Sähköpostin lokiinkirjauksessa käytetyn käyttäjätilin vaihtaminen

### [!INCLUDE[prod_short](includes/prod_short.md)] Online

1. Kirjaudu sisään kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)] tilillä, jonka avulla aikataulutettu projekti muodostaa yhteyden jaettuun postilaatikkoon ja käsittelee sähköpostiviestit tilin avulla. Tällä tilillä täytyy olla sekä [!INCLUDE[prod_short](includes/prod_short.md)]- että Exchange Online-oikeudet.
2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköpostin lokiinkirjaus** ja valitse sitten vastaava linkki. 
3. Valitse **Aiheeseen liittyvät** ja sitten **Työjonotapahtuma**.
4. Käynnistä **Sähköpostin lokiinkirjaus** -työ uudelleen.

### [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköpostin lokiinkirjaus** ja valitse sitten vastaava linkki.
2. Valitse **Toiminnot** ja sitten **Uudista tunnus**.
3. Kirjaudu sisään Exchange Online-tilillä, jonka avulla aikataulutettu projekti muodostaa yhteyden jaettuun postilaatikkoon ja käsittelee sähköpostiviestit tilin avulla.

## Katso myös
[Kontaktienhallinta](marketing-relationship-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]