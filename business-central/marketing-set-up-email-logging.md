---
title: Sähköpostin lokiinkirjauksen määrittäminen | Microsoft Docs
description: Lisätietoja siitä, miten myyjien ja asiakkaiden sähköpostivuorovaikutukset voidaan muuttaa todellisiksi myyntimahdollisuuksiksi.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6e2a72b1917fdf419b0f103db39b5cdf84f8b425
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437575"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Myyjien ja yhteyshenkilöiden välisten sähköpostiviestien seuraaminen

Saat enemmän hyötyä myyjien ja olemassa olevien tai potentiaalisten asiakkaiden välisestä viestinnästä, jos seuraat sähköpostiviestejä ja muunnat ne toiminnallisiksi mahdollisuuksiksi. [!INCLUDE[prod_short](includes/prod_short.md)] -sovellusta voi käyttää yhdessä Exchange Onlinen kanssa. Näin voit seurata saapuvia ja lähteviä viestejä. Voit tarkastella ja analysoida kunkin viestin sisältöä **Vuorovaikutuslokin tapahtumat** -sivulla.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Yleisten kansioiden ja sääntöjen määrittäminen sähköpostin lokiinkirjausta Exchange Onlinessa

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Seuraavaksi [!INCLUDE[prod_short](includes/prod_short.md)] yhdistetään Exchange Onlineen.

## <a name="setting-up-prod_short-to-log-email-messages"></a>Määritetään [!INCLUDE[prod_short](includes/prod_short.md)] -sovellus sähköpostiviestien kirjaamista varten

Aloita sähköpostien kirjaaminen seuraavien kahden helpon vaiheen avulla:

1. Muodosta yhteys [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen Exchange Onlinen avulla Microsoft 365 -tilauksessa. Exchange Online käsittelee sähköpostiviestisi. Tämä on helppo tehdä asetusten ohjatun määrityksen oppaan avulla. Tarvitset vain järjestelmänvalvojan tunnistetiedot Microsoft 365:n järjestelmänvalvojan tiliä varten. Aloita oppaan käyttäminen siirtymällä **Asetusten ohjattu määritys** -kohtaan ja valitsemalla **Määritä sähköpostin lokiinkirjaus**.  

2. Varmista, että [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen on määritetty oikeat sähköpostiosoitteet myyjille ja yhteyshenkilöille sen mukaan, ovatko he potentiaalisia vai olemassa olevia asiakkaita. Tee tämä avaamalla kunkin asiakkaan tai myyjän **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortti ja tarkistamalla **Sähköposti**-kenttä.

> [!Tip]
> Kun olet tehnyt nämä oppaan vaiheet, voit tarkistaa yhteyden tilan. Siirry **Kontaktienhallinnan asetukset** -kohtaan, valitse **Prosessi** ja valitse sitten **Toiminnot**. Valitse lopuksi **Tarkista sähköpostin lokiinkirjauksen asetukset**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Sähköpostiviestien tarkasteleminen vuorovaikutuslokissa
[!INCLUDE[prod_short](includes/prod_short.md)] luo **Vuorovaikutusloki**-sivulle tapahtuman aina, kun myyjä ja yhteyshenkilö lähettävät sähköpostiviestejä. Voit tarkastella vuorovaikutuslokia avaamalla **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortin ja valitsemalla sitten **Historia**- ja **Vuorovaikutuslokin tapahtumat** -kohdat. Lokin tapahtumille voi tehdä esimerkiksi seuraavia toimintoja:

- Voit tarkastella sähköpostiviestin sisältöä valitsemalla **Näytä liitteet** -toiminnon.
- Voit muuttaa sähköpostiviestinnän myyntimahdollisuudeksi. Jos tapahtuma näyttää lupaavalta, voit muuttaa sen mahdollisuudeksi, jonka jälkeen siitä voi kehittyä myyntiä. Valitse ensin tapahtuma ja valitse sitten **Luo mahdollisuus**-toiminto. Lisätietoja on kohdassa [Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>On-Premises-versioiden yhdistäminen Microsoft Exchangeen
Voit muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -ratkaisusta paikalliseen Exchange on-premisesiin tai Exchange Onlineen sähköpostin lokiinkirjaamiseksi. Molemmissa Exchange-versioissa yhteyden asetukset ovat käytettävissä **Kontaktienhallinnan asetukset** -sivulla. Exchange Onlinessa voit käyttää myös avustettua asennusopasta. 

### <a name="connecting-to-exchange-on-premises"></a>Yhdistäminen Exchange On-premisesiin
Jos haluat yhdistää [!INCLUDE[prod_short](includes/prod_short.md)] on-premisesin Exchange on-premisesiin, voit käyttää **Kontaktienhallinnan asetukset** -sivulla **Perus**-vaihtoehtoa **todennustyyppinä** ja kirjoittaa sitten Exchange on-premisesin käyttäjätilin tunnistetiedot. Aloita sitten sähköpostin lokiinkirjaaminen valitsemalla **Käytössä**-valitsin. 

### <a name="connecting-to-exchange-online"></a>Yhdistäminen Exchange Onlineen
Jos haluat muodostaa yhteyden Exchange Onlineen, sinun on käytettävä **OAuth2**-arvoa **todennustyyppinä**. Sovellus on myös rekisteröitävä Azure Active Directoryssä, minkä lisäksi on asennettava sovelluksen tunnus, avainsäilön salaisuus ja käytettävä uudelleenohjauksen URL-osoite. Uudelleenohjauksen URL-osoite täytetään valmiiksi, ja sen pitäisi toimia useimmissa asennuksissa. Lisätietoja on kohdassa [Sovelluksen rekisteröiminen Azure AD:ssä yhteyden muodostamiseksi Business Centralista Exchange Onlineen](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Asennus on määritettävä käyttämään HTTPS-yhteyttä. Lisätietoja on kohdassa [SSL:n määrittäminen suojaamaan Business Centralin verkkoasiakasohjelman yhteyttä](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Jos palvelimelle määritetään jokin muu aloitussivu, URL-osoitteen voi vaihtaa. Asiakasohjelman salaisuus tallennetaan tietokantaan salattuna merkkijonona.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Sovelluksen rekisteröiminen Azure AD:ssä muodostamaan yhteys Business Centralista Exchange Onlineen
Seuraavissa vaiheissa oletetaan, käyttäjätietojen ja käyttöoikeuksien hallintaan käytetään Azure Active Directory:tä. Lisätietoja on kohdassa [Pika-aloitus: sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristössä](/azure/active-directory/develop/quickstart-register-app). Jos Azure Active Directory ei ole käytössä, lisätietoja on kohdassa [Jonkin muun käyttäjätieto- ja käyttöoikeuspalvelun käyttäminen](marketing-set-up-email-logging.md#using-another-identity-and-access-management-service). 

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
8. Valitse **Yleiskuvaus** ja etsi sitten **Sovelluksen (asiakasohjelman) tunnus** -arvo. Tämä on sovelluksen asiakasohjelman tunnus. Se on joko annettava **Kontaktienhallinnan asetukset** -sivun **Asiakasohjelman tunnus** -kentässä tai tallennettava suojattuun tallennustilaan tapahtuman tilaajassa annettavaksi.
9. Määritä [!INCLUDE[prod_short](includes/prod_short.md)]issa sähköpostin lokiinkirjaus **Kontaktienhallinnan asetukset** -sivulla tai käytä **Sähköpostin lokiinkirjauksen asetusten ohjattu määritys** -asennusopasta prosessin apuna.
    * Anna sen käyttäjän sähköpostitili, jonka puolesta aikataulutettu projekti muodostaa Exchange Online -yhteyden ja käsittelee sähköpostiviestit. Käyttäjällä on oltava voimassa oleva Exchange Online -käyttöoikeus.
    * Anna Exchange Onlinen URL-osoite. Yleensä tämä on toimialue, jonka olet määrittänyt käyttäjän sähköpostiosoitteessa.
    * Anna **Jonon kansiopolku** ja **Tallennuskansion polku**.
10. Aloita sitten sähköpostin lokiinkirjaaminen valitsemalla **Käytössä**-valitsin.
11. Käytä kirjautumiseen Azure Active Directoryn järjestelmänvalvojan tiliä. (Tämä tili tarvitsee voimassaolevan Exchangen käyttöoikeuden, ja sen on oltava Exchange Onlinen järjestelmänvalvoja.) Kirjautumisen jälkeen sinua pyydetään antamaan rekisteröidylle sovellukselle lupa kirjautua Exchange Onlineen organisaation puolesta. Määrityksen valmistumisen edellyttää tämän luvan antamista.

   > [!NOTE]
   > Jos sinua ei pyydetä käyttämään kirjautumiseen järjestelmänvalvojan tiliä, syynä on luultavasti estetyt ponnahdusikkunat. Kirjautumista varten on sallittava ponnahdusikkunat osoitteesta https://login.microsoftonline.com.

### <a name="using-another-identity-and-access-management-service"></a>Jonkin muun käyttäjätieto- ja käyttöoikeuspalvelun käyttäminen
Jos Azure Active Directorya ei käytetä käyttäjätietojen ja käyttöoikeuksien hallintaa, apua on pyydettävä kehittäjältä. Jos haluat tallentaa sovelluksen tunnuksen ja salaisen avaimen eri sijaintiin, Asiakasohjelman tunnus- ja Asiakasohjelman salainen avain -kentät voidaan jättää tyhjäksi. Tunnuksen ja salaisen avaimen sijainnista noutoa varten on siinä tapauksessa kirjoitettava laajennus. Salainen avain voidaan antaa suorituspalvelussa tilaamalla OnGetEmailLoggingClientId- ja OnGetEmailLoggingClientSecret-tapahtumat codeunitissa 1641 "Setup Email Logging".

### <a name="to-stop-logging-email"></a>Sähköpostin lokiinkirjaamisen lopettaminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kontaktienhallinnan asetukset** ja valitse sitten vastaava linkki.
2. Poista **Käytössä**-valitsin käytöstä.

## <a name="see-also"></a>Katso myös
[Kontaktienhallinta](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]