---
title: Business Centralin sähköpostin määrittäminen
description: Tässä artikkelissa kuvataan, miten sähköpostitilit yhdistetään Business Centraliin, jotta voit lähettää lähteviä viestejä avaamatta toista sovellusta.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 1ac53955d897e8c69da5136c6326353999460625
ms.sourcegitcommit: 951d3c9d541f0b1d26712d37e253c2958dae3321
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889150"
---
# <a name="set-up-email"></a>Määritä sähköposti
Ihmiset yrityksissä lähettävät päivittäin sähköpostitse tietoja ja asiakirjoja, kuten myynti- ja ostotilauksia ja laskuja. Järjestelmänvalvojat voivat helpottaa tätä yhdistämällä yhden tai useamman sähköpostitilin [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen, joten voit lähettää asiakirjoja avaamatta sähköpostisovellusta. Voit kirjoittaa jokaisen viestin yksitellen perusmuotoilutyökaluilla, kuten fontilla, tyyleillä, väreillä ja niin edelleen, ja lisätä liitteitä, joiden koko on enintään 100 Mt. Järjestelmänvalvojat voivat myös määrittää raporttiasetteluja, jotka sisältävät vain asiakirjojen tärkeimmät tiedot. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md).

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa on sähköpostiominaisuudet vain lähteville viesteille. Vastauksia ei voi vastaanottaa, eli [!INCLUDE[prod_short](includes/prod_short.md)]issa ei ole Saapuneet-kansiosivua.

> [!NOTE]
> Jos käytät paikallista [!INCLUDE[prod_short](includes/prod_short.md)]ia, ennen kuin voit määrittää sähköpostin, sinun on luotava sovellusrekisteröinti [!INCLUDE[prod_short](includes/prod_short.md)]ille Azure-portaalissa. Sovelluksen rekisteröinti mahdollistaa [!INCLUDE[prod_short](includes/prod_short.md)]in valtuuttamaan ja todentamaan sähköpostipalveluntarjoajasi kanssa. Lisätietoja on kohdassa [Business Central On-Premises -version sähköpostin määrittäminen](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa hoidamme tämän puolestasi.

## <a name="required-permissions"></a>Vaaditut käyttöoikeudet
Sähköpostin määrittäminen edellyttää, että sinulla on **SÄHKÖPOSTIN MÄÄRITYS** -oikeusjoukko. Lisätietoja on kohdassa [Määritä käyttöoikeudet käyttäjille ja ryhmille](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>Sähköpostitilien lisääminen
Sähköpostitilit lisätään laajennusten avulla, joiden avulla eri palveluntarjoajien tilit voivat muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]iin. Vakiolaajennusten avulla voit käyttää Microsoft Exchange Online-tilejä, mutta käytettävissä voi olla muita laajennuksia, jotka voivat yhdistää muiden palveluntarjoajien, kuten Gmailin, tilejä.

Kun olet lisännyt sähköpostitilin, voit määrittää ennalta määritetyt liiketoimintaskenaariot, joissa tiliä käytetään sähköpostien lähettämiseen. Voit esimerkiksi määrittää, että kaikki käyttäjät lähettävät myyntiasiakirjoja yhdestä tilistä ja ostoasiakirjoja toisesta tilistä. Lisätietoja on kohdassa [Sähköpostiskenaarioiden määrittäminen sähköpostitileille](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

Seuraavassa taulukossa kuvataan oletusarvoisesti käytettävissä olevat sähköpostilaajennukset.

|Laajennus  |Kuvaus  |Esimerkkejä siitä, milloin käytetään  |
|---------|---------|---------|
|**Microsoft 365**|Kaikki lähettävät sähköpostia jaetusta Exchange Online -postilaatikosta.|Kun kaikki viestit tulevat samalta osastolta, esimerkiksi myyntiorganisaatiosi lähettää viestejä tilistä sales@cronus.com. Tämä edellyttää, että määrität jaetun postilaatikon Microsoft 365 -hallintakeskuksessa. Lisätietoja on kohdassa [Jaetut postilaatikot](/Exchange/collaboration/shared-mailboxes/shared-mailboxes.md).|
|**Nykyinen käyttäjä**|Kaikki lähettävät sähköpostia tililtä, jolla he ovat kirjautuneet [!INCLUDE[prod_short](includes/prod_short.md)]iin.|Salli viestintä yksittäisiltä tileiltä.|
|**Muu (SMTP)**|Lähetä sähköpostit SMTP-protokollan avulla.|Salli tietoliikenne SMTP-sähköpostipalvelimen kautta. |

> [!NOTE]
> **Microsoft 365**- ja **Nykyinen käyttäjä** -laajennukset käyttävät tilejä, jotka määrität käyttäjille Microsoft 365 -hallintakeskuksessa Microsoft 365 -tilaukselle. Jotta voisit lähettää sähköpostia laajennusten avulla, käyttäjillä on oltava voimassa oleva Exchange Online -käyttöoikeus. 

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="legacy-smtp-settings-and-the-email---smtp-connector-extension"></a>Vanhat SMTP-asetukset ja Sähköposti – SMTP-yhdistin -laajennus
Jos käytät jo [!INCLUDE[prod_short](includes/prod_short.md)]ia ja olet määrittänyt sähköpostin vanhojen SMTP-asetusten avulla, voit jatkaa asetusten käyttöä yhdessä Sähköposti – SMTP-yhdistin -laajennuksen avulla. Kun päivitämme [!INCLUDE[prod_short](includes/prod_short.md)]in seuraavaan versioon, kopioimme vanhat SMTP-asetuksesi Sähköposti –SMTP-yhdistin -laajennukseen. Kun päivitys on valmis, järjestelmänvalvoja voi ottaa parannetut sähköpostiominaisuudet käyttöön ja aloitat Sähköposti – SMTP-yhdistin -laajennuksen käyttämisen. Lisätietoja on kohdassa [Tietoja ominaisuuksien hallinnasta](/dynamics365/business-central/dev-itpro/administration/feature-management#about-feature-management). SMTP-yhdistin -laajennuksen ja vanhojen asetusten välillä ei kuitenkaan ole synkronointia. Jos muutat laajennuksen SMTP-asetuksia, tee samat muutokset myös vanhoihin SMTP-asetuksiin – tai päinvastoin.

> [!NOTE]
> Jos sinulla on mukautuksia, jotka perustuvat vanhaan SMTP-sähköpostiasetukseen, on mahdollista, että jokin menee vikaan mukautusten yhteydessä, jos aloitat sähköpostilaajennusten käyttämisen. Microsoft suosittelee, että määrität ja testaat laajennuksia, ennen kuin otat käyttöön toimintovalitsimen parannetuille sähköpostiominaisuuksille.

> [!IMPORTANT]
> Jos käytössä on [!INCLUDE[prod_short](includes/prod_short.md)] online, OAuth 2.0 -todennusmenetelmän käyttö ei ole mahdollista.<br> Jos käytössä on paikallinen [!INCLUDE[prod_short](includes/prod_short.md)], OAuth 2.0 -todennusta voi käyttää mutta Azure-portaalissa on luotava sovelluksen rekisteröinti, minkä jälkeen Azure AD on yhdistettävä suorittamalla ohjattu **Määritä Azure Active Directory** -asetuksen määritysopas [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Business Centralin sovelluksen rekisteröinnin luonti Azure-portaalissa](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).

## <a name="add-email-accounts"></a>Sähköpostitilien lisääminen
Asetusten ohjattu **Määritä sähköposti** -määritys auttaa sinua pääsemään alkuun nopeasti sähköpostiviestien käytössä.

> [!NOTE]
> Sinulla on oltava oletussähköpostitili, vaikka olisit lisännyt vain yhden tilin. Oletustiliä käytetään kaikissa sähköpostiskenaarioissa, joita ei ole määritetty muulle tilille. Lisätietoja on kohdassa [Sähköpostiskenaarioiden määrittäminen sähköpostitileille](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköpostitilien määrittäminen** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Määritä skenaariot sähköpostitileille
Sähköpostiskenaariot ovat prosesseja, joihin liittyy asiakirjan (esimerkiksi myynti- tai ostotilauksen tai ilmoituksen, esimerkiksi ulkopuolisen kirjanpitäjän kutsun) lähettäminen. Tiettyjä skenaarioita varten voi käyttää tiettyjä sähköpostitilejä. Voit esimerkiksi määrittää, että kaikki käyttäjät lähettävät aina myyntiasiakirjat yhdeltä tililtä, ostoasiakirjat toiselta ja varasto- tai tuotantoasiakirjat kolmannelta tililtä. Voit määrittää, uudelleenmäärittää ja poistaa skenaarioita milloin haluat, mutta voit liittää skenaarion vain yhteen sähköpostitiliin kerrallaan. Oletussähköpostitiliä käytetään kaikissa skenaarioissa, joita ei ole määritetty muulle tilille.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents"></a>Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen myynti- ja ostoasiakirjoille
Raporttien avulla voit sisällyttää myynti- ja ostoasiakirjojen avaintietoja sähköpostien teksteihin. Tässä kuvataan , miten **Myynti–lasku**-raportti määritetään kirjatuille myyntilaskuille, mutta prosessi on samankaltainen muille raporteille.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raportin valinnat - Sales** ja valitse sitten liittyvä linkki.
2. Valitse **Raporttivalinta - Myynti** -sivun **Käyttö**-kentässä **Lasku**.
3. Valitse **Raportin tunnus** -kentän uudella rivillä esimerkiksi vakioraportti 1306.
4. Valitse **Käytä sähköpostin perustekstinä** -valintaruutu.
5. Valitse ensin **Sähköpostin perustekstin asettelun kuvaus** -kenttä ja sitten asettelu luettelosta.

    Raporttiasettelut määrittävät sähköpostin perustekstin tyylin ja sisällön, myös teksteille kuten tervehdys tai ohjeet, jotka edeltävät asiakirjan tietoja. Jos organisaatiossa on useita asetteluja, kaikki käytettävissä olevat raporttiasettelut ovat näkyvissä, jos valitset **Valitse koko luettelosta**.
6. Voit tarkastella tai muokata asettelua, johon sähköpostin teksti perustuu, valitsemalla ensin asettelun **Mukautetut raporttiasettelut** -sivulla ja sitten **Päivitä asettelua** -toiminnon.
7. Jos haluat tarjota asiakkaillesi mahdollisuuden maksaa sähköisesti, voit määrittää liittyvän maksupalvelun, kuten PayPalin. Tämän jälkeen sähköpostin tekstiin voi lisätä myös PayPal-tiedot ja -linkin. Lisätietoja on kohdassa [Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md).
8. Valitse **OK**-painike.

Kun nyt valitset esimerkiksi **Kirjattu myyntilasku** -sivulla **Lähetä**-toiminnon, sähköpostin perusteksti sisältää raportin 1306 asiakirjan tiedot, joita edeltää tyylitelty vakioteksti vaiheessa 5 valitun raporttiasettelun mukaan.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Korvaavan lähettäjän osoitteen käyttäminen lähtevissä sähköpostiviesteissä
Jos käytät vanhoja SMTP-asetuksia, voit muuttaa Microsoft Exchange -palvelimen **Lähetä –**- tai **Lähetä puolesta** -toimintoja lähtevien viestin lähettäjän osoitteen muuttamiseksi. [!INCLUDE[prod_short](includes/prod_short.md)] käyttää SMTP-tiliä Exchange-todennuksessa mutta joko korvaa lähettäjän osoitteen määrittämälläsi osoitteella tai muuttaa sitä puolesta-tiedolla.

Seuraavassa on esimerkkejä tavoista, joilla Lähetä –- tai Lähetä puolesta -toimintoja käytetään [!INCLUDE[prod_short](includes/prod_short.md)]issa:

 * Kun asiakirjoja lähetetään osto- tai myyntitilauksina toimittajille tai asiakkaille, haluat ehkä, että ne näyttävät tulevan _noreply@yourcompanyname.com_-osoitteesta.
 * Kun työnkulku lähettää hyväksyntäpyynnön sähköpostitse käyttämällä pyytäjän sähköpostiosoitetta.

> [!Note]
> Lähettäjän osoitteiden korvaamiseen voidaan käyttää vain yhtä tiliä. Et siis voi käyttää yhtä korvaavaa osoitetta ostoprosesseissa ja toista myyntiprosesseissa.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Korvaavan lähettäjän osoitteen määrittäminen kaikkiin lähteviin sähköpostiviesteihin
1. Etsi Microsoft 365 -tilin **Exchangen hallintakeskuksessa** postilaatikko, jota käytetään korvaavana osoitteena, ja kopioi sitten osoite tai kirjoita se muistiin. Jos tarvitset uuden osoitteen luo uusi käyttäjä Microsoft 365 -hallintakeskuksessa ja määritä käyttäjälle postilaatikko.
2. Valitse [!INCLUDE[prod_short](includes/prod_short.md)]:ssa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **SMTP-sähköpostin asetukset** ja valitse sitten liittyvä linkki.
3. Lisää korvaava osoite **Lähetä –** -kenttään.
4. Kopioi **Käyttäjätunnus**-kentässä oleva osoite tai kirjoita se muistiin.
5. Etsi **Exchangen hallintakeskuksessa** postilaatikko, jota käytetään korvaavana osoitteena, ja anna sitten **Käyttäjätunnus**-kentän osoite **Lähetä –** -kenttään. Lisätietoja on aiheessa [Yksittäisten postilaatikoiden käyttöoikeuksien määrittäminen EAC-määrityksen avulla](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Korvaavan osoitteen käyttäminen hyväksymistyönkuluissa
1. Valitse [!INCLUDE[prod_short](includes/prod_short.md)]:ssa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **SMTP-sähköpostin asetukset** ja valitse sitten liittyvä linkki.
2. Kopioi **Käyttäjätunnus**-kentässä oleva osoite tai kirjoita se muistiin.
3. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Hyväksynnän käyttäjäasetukset** ja valitse sitten liittyvä linkki.
4. Etsi **Exchangen hallintakeskuksessa** kunkin **Hyväksynnän käyttäjäasetukset** -sivun luettelossa olevan käyttäjän postilaatikot ja anna **Lähetä –** -kenttään osoite, joka oli **SMTP-sähköpostin asetukset** -sivun **Käyttäjätunnus**-kentässä [!INCLUDE[prod_short](includes/prod_short.md)]issa. Lisätietoja on kohdassa [Vastaanottajien käyttöoikeuksien hallinta](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. Valitse [!INCLUDE[prod_short](includes/prod_short.md)]:ssa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **SMTP-sähköpostin asetukset** ja valitse sitten liittyvä linkki.
6. Ota korvaus käyttöön ottamalla käyttöön **Salli lähettäjän korvaaminen** -valitsin.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] määrittää seuraavassa järjestyksessä, mikä osoite näytetään: <br><br> 1. **Hyväksynnän käyttäjäasetukset** -sivun **Sähköposti**-kentässä työnkulun viesteille määritetty osoite. <br> 2. **SMTP-sähköpostin asetukset** -sivun **Lähetä –** -kentässä määritetty osoite. <br> 3. **SMTP-sähköpostin asetukset** -sivun **Käyttäjätunnus**-kentässä määritetty osoite.

## <a name="set-up-document-sending-profiles"></a>Asiakirjan lähetysprofiilien määrittäminen
Voit määrittää ensisijaisen tavan lähettää myyntiasiakirjoja kullekin asiakkaalle, jotta sinun ei tarvitse valita lähetysvaihtoehtoa (esimerkiksi lähettääkö asiakirja sähköpostilla tai sähköisenä asiakirjana) aina, kun lähetät asiakirjan. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Yleisten kansioiden ja sääntöjen määrittäminen sähköpostin lokiinkirjaukselle Exchange Onlinessa
Saat enemmän hyötyä myyjien ja olemassa olevien tai potentiaalisten asiakkaiden välisestä viestinnästä, jos seuraat sähköpostiviestejä ja muunnat ne toiminnallisiksi mahdollisuuksiksi. Lisätietoja on kohdassa [Myyjien ja yhteyshenkilöiden välisten sähköpostiviestien seuraaminen](marketing-set-up-email-logging.md).  

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Seuraavaksi [!INCLUDE[prod_short](includes/prod_short.md)] yhdistetään Exchange Onlineen. Lisätietoja on kohdassa [Myyjien ja yhteyshenkilöiden välisten sähköpostiviestien seuraaminen](marketing-set-up-email-logging.md).  

## <a name="setting-up-email-for-business-central-on-premises"></a>Sähköpostin määrittäminen Business Central On-Premises -versiossa 
[!INCLUDE[prod_short](includes/prod_short.md)] on-premises voidaan integroida Microsoft Azure -järjestelmään perustuvien palveluiden kanssa. Voit esimerkiksi käyttää Cortana Intelligence -toimintoa entistä älykkäämpien kassavirtaennusteiden muodostamiseksi, Power BI:tä visualisoidaksesi liiketoimintaasi ja Exchange Onlinea lähettääksesi sähköpostia. Integrointi näihin palveluihin perustuu sovelluksen rekisteröintiin Azure Active Directoryssa. Sovelluksen rekisteröinti tarjoaa todennus- ja valtuutuspalveluita viestintää varten. Jotta voisit käyttää [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -version sähköpostitoimintoja , sinun täytyy rekisteröidä [!INCLUDE[prod_short](includes/prod_short.md)]in sovelluksena Azure-portaalissa ja yhdistää [!INCLUDE[prod_short](includes/prod_short.md)] sovellusrekisteröintiin. Seuraavissa luvuissa kerrotaan, miten tämä tehdään.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Business Centralin sovelluksen rekisteröinnin luonti Azure-portaalissa
[!INCLUDE[prod_short](includes/prod_short.md)]in Azure-portaaliin rekisteröimisen vaiheet on kuvattu kohdassa [Rekisteröi sovellus Azure Active Directoryssa](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Sähköpostiominaisuuksiin liittyvät asetukset ovat delegoituja käyttöoikeuksia, jotka myönnetään sovellusrekisteröinnille. Seuraavassa taulukossa on luettelo vähimmäisoikeuksista.

|Ohjelmistorajapinta / käyttöoikeuden nimi  |Tyyppi  |Kuvaus  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Delegoitu|Kirjaudu sisään ja lue käyttäjäprofiili.         |
|Microsoft Graph / Mail.ReadWrite |Delegoitu|Luo sähköpostiviestejä.         |
|Microsoft Graph / Mail.Send|Delegoitu|Lähetä sähköpostiviestejä.         |
|Microsoft Graph / offline_access|Delegoitu|Ylläpidä tietojen käyttöoikeuden hyväksyntää.|

Jos käytössä on vanha SMTP-määritys tai SMTP-yhdistin ja haluat käyttää OAuth-todennusta, oikeudet ovat hieman erilaiset. Seuraavassa taulukossa on oikeusluettelo.

|Ohjelmistorajapinta / käyttöoikeuden nimi  |Tyyppi  |Kuvaus  |
|---------|---------|---------|
|Microsoft Graph / offline_access|Delegoitu|Ylläpidä tietojen käyttöoikeuden hyväksyntää.|
|Microsoft Graph / openid|Delegoitu|Käyttäjien sisäänkirjautuminen.|
|Microsoft Graph / User.Read |Delegoitu|Kirjaudu sisään ja lue käyttäjäprofiili.         |
|Microsoft Graph / SMTP.Send|Delegoitu|Sähköpostien lähettäminen postilaatikosta SMTP AUTH -todennuksella.         |
|Office 365 Exchange Online / User.Read |Delegoitu|Kirjaudu sisään ja lue käyttäjäprofiili.         |

Kun luot sovelluksen rekisteröinnin, huomaa seuraavat tiedot. Sinun on yhdistettävä [!INCLUDE[prod_short](includes/prod_short.md)] sovellusrekisteröintiin.
 
* Sovelluksen (asiakkaan) tunnus 
* Uudelleenohjauksen URI-osoite (valinnainen)
* Asiakasohjelman salaisuus

Sovelluksen rekisteröimisen yleiset ohjeet: [Pika-aloitus: sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristössä](/azure/active-directory/develop/quickstart-register-app). 

> [!NOTE]
Jos vanhan SMTP-määrityksen käyttäminen sähköpostin lähettämiseen aiheuttaa ongelmia sen jälkeen, kun [!INCLUDE[prod_short](includes/prod_short.md)] yhdistettiin sovelluksen rekisteröintiin, syynä voi olla se, että SMTP AUTH ei ole otettu käyttöön vuokraajassa. Suositeltavaa onkin käyttää Microsoft 365- ja Nykyinen käyttäjä -yhdistimiä, sillä ne käyttävät Microsoft Graphin Mail-ohjelmointirajapintoja. Jos SMTP-määritystä on kuitenkin käytettävä, SMTP AUTH voidaan ottaa käyttöön. Lisätietoja on kohdassa [Todennetun asiakasohjelman SMTP-lähetyksen (SMTP AUTH) ottaminen käyttöön tai poistaminen käytöstä Exchange Onlinessa](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect-prod_short-to-your-app-registration"></a>Yhdistä [!INCLUDE[prod_short](includes/prod_short.md)] sovellusrekisteröintiisi
Kun olet rekisteröinyt sovelluksen Azure-portaalissa, voit [!INCLUDE[prod_short](includes/prod_short.md)]issa käyttää ohjattua **Sähköpostisovelluksen AAD-rekisteröinti** -määritystä yhdistääksesi [!INCLUDE[prod_short](includes/prod_short.md)]in siihen.

1. Valitse [!INCLUDE[prod_short](includes/prod_short.md)]issa ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköpostisovelluksen AAD-rekisteröinti** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Vaihtoehtoisesti, jos muodostat yhteyden ensimmäistä kertaa, voit käyttää ohjattua **Määritä sähköposti** -määritystä. Oppaassa tarvitaan tietoja, joiden avulla voit muodostaa yhteyden sovelluksen rekisteröintiin. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Azure Active Directory, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Azure AD Directory - Multitenant)** or **Accounts in any organizational directory (Any Azure AD Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Azure Active Directory, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-also"></a>Katso myös
[Exchange Onlinen jaetut postilaatikot](/exchange/collaboration-exo/shared-mailboxes)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen yrityssähköpostina Outlookissa](admin-outlook.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in hakeminen mobiililaitteeseen](install-mobile-app.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in hakeminen mobiililaitteeseen](install-mobile-app.md)
[Jäljityksen telemetrian analysointi (järjestelmänvalvojan sisältö)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
