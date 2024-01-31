---
title: Business Central -sovelluksen sähköpostin määrittäminen (sisältää videon)
description: 'Tässä artikkelissa kuvataan, miten sähköpostitilit yhdistetään Business Centraliin, jotta voit lähettää lähteviä viestejä avaamatta toista sovellusta.'
author: brentholtorf
ms.author: bholtorf
ms.topic: get-started
ms.search.keywords: 'SMTP, email, Office 365, connector'
ms.search.form: '1805, 9813, 9814, 1262, 1263'
ms.date: 10/06/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Määritä sähköposti

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Ihmiset yrityksissä lähettävät päivittäin sähköpostitse tietoja ja asiakirjoja, kuten myynti- ja ostotilauksia ja laskuja. Järjestelmänvalvojat yhdistää yhden tai useamman sähköpostitilin [!INCLUDE[prod_short](includes/prod_short.md)] -sovellukseen, joten voit lähettää asiakirjoja avaamatta sähköpostisovellusta. Voit kirjoittaa jokaisen viestin yksitellen perusmuotoilutyökaluilla, kuten fontilla, tyyleillä, väreillä ja niin edelleen, ja lisätä liitteitä, joiden koko on enintään 100 Mt. Raporttiasettelujen avulla järjestelmänvalvojat voivat sisällyttää asiakirjoista vain tärkeimmät tiedot. Lisätietoja on kohdassa [Asiakirjojen lähettäminen sähköpostilla](ui-how-send-documents-email.md).

[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa on sähköpostiominaisuudet vain lähteville viesteille. Vastauksia ei voi vastaanottaa, eli issa ei ole Saapuneet-kansiosivua.

> [!NOTE]
> Voit käyttää [!INCLUDE[prod_short](includes/prod_short.md)] onlinen sähköpostiominaisuuksia vain Exchange Onlinen kanssa. Emme tue yhdistelmäskenaarioita, kuten [!INCLUDE[prod_short](includes/prod_short.md)] onlinen yhdistämistä Exchangen paikalliseen versioon.
>
> Jos käytät paikallista [!INCLUDE[prod_short](includes/prod_short.md)]ia, ennen kuin voit määrittää sähköpostin, sinun on luotava sovellusrekisteröinti [!INCLUDE[prod_short](includes/prod_short.md)]ille Azure-portaalissa. Sovelluksen rekisteröinti mahdollistaa [!INCLUDE[prod_short](includes/prod_short.md)]in valtuuttamaan ja todentamaan sähköpostipalveluntarjoajasi kanssa. Lisätietoja on kohdassa [Sähköpostin määrittäminen Business Central On-Premises -versiossa](admin-how-setup-email.md#set-up-email-for-business-central-on-premises). [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa hoidamme tämän puolestasi.

## Tarpeet

Sähköpostitoimintojen määrittämiseen ja käyttämiseen on muutamia vaatimuksia.

* Sähköpostin määrittäminen edellyttää, että sinulla on **SÄHKÖPOSTIN MÄÄRITYS** -oikeusjoukko. Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md).
* Kaikkien sähköpostitoimintoja käyttävien käyttäjien on oltava täysin lisensoituja [!INCLUDE [prod_short](includes/prod_short.md)]. Esimerkiksi delegoidut järjestelmänvalvojat ja vieraskäyttäjät eivät voi käyttää vuokraajan sähköpostitiliä.

## Sähköpostitilien lisääminen

Sähköpostitilit lisätään laajennusten avulla, joiden avulla eri palveluntarjoajien tilit voivat muodostaa yhteyden [!INCLUDE[prod_short](includes/prod_short.md)]iin. Vakiolaajennusten avulla voit käyttää tilejä Microsoft Exchange Onlinesta. Muita laajennuksia, joiden avulla voit yhdistää muiden palveluntarjoajien, kuten Gmailin, tileihin, voivat olla käytettävissä.

Voit määrittää ennalta määritetyt liiketoimintaskenaariot, joissa sähköpostitiliä käytetään sähköpostien lähettämiseen. Voit esimerkiksi määrittää, että kaikki käyttäjät lähettävät myyntiasiakirjoja yhdestä tilistä ja ostoasiakirjoja toisesta tilistä. Lisätietoja: [Määritä skenaariot sähköpostitileille](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

Seuraavassa taulukossa kuvataan oletusarvoisesti käytettävissä olevat sähköpostilaajennukset.

|Laajennus  |Kuvaus  |Esimerkkejä siitä, milloin käytetään  |
|---------|---------|---------|
|**Microsoft 365 -yhdistin**|Kaikki lähettävät sähköpostia jaetusta Exchange Online -postilaatikosta.|Kun kaikki viestit tulevat samalta osastolta, esimerkiksi myyntiorganisaatiosi lähettää viestejä tilistä sales@cronus.com. Tämä vaihtoehto edellyttää, että määrität jaetun postilaatikon Microsoft 365 -hallintakeskuksessa. Lisätietoja on kohdassa [Jaetut postilaatikot](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Nykyinen käyttäjän yhdistin**|Kaikki lähettävät sähköpostia tililtä, jolla he ovat kirjautuneet [!INCLUDE[prod_short](includes/prod_short.md)]iin.|Salli viestintä yksittäisiltä tileiltä.|
|**SMTP-yhdistin**|Lähetä sähköpostit SMTP-protokollan avulla.|Salli tietoliikenne SMTP-sähköpostipalvelimen kautta. |

> [!NOTE]
> **Microsoft 365 -yhdistin** ja **Nykyisen käyttäjän yhdistin** -laajennukset käyttävät tilejä, jotka määrität käyttäjille Microsoft 365 -hallintakeskuksessa Microsoft 365 -tilaukselle. Jotta voisit lähettää sähköpostia laajennusten avulla, käyttäjillä on oltava voimassa oleva Exchange Online -käyttöoikeus. Lisäksi eristysympäristöissä nämä laajennukset, kuten **Outlook REST API** -laajennus edellyttävät, että **Salli HttpClient-pyynnöt** -asetus on käytössä. Jos haluat tarkistaa, onko se otettu käyttöön näille laajennuksille, siirry **Laajennuksen hallinta** -sivulle, valitse laajennus ja valitse sitten **Määritä**-asetus.

> Ulkoiset käyttäjät, kuten valtuutetut järjestelmänvalvojat ja ulkoiset kirjanpitäjät, eivät voi käyttää näitä laajennuksia sähköpostiviestien lähettämiseen [!INCLUDE[prod_short](includes/prod_short.md)] -ratkaisusta.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## Käytä SMTP

Jos haluat käyttää SMTP-protokollaa sähköpostien lähettämiseen [!INCLUDE[prod_short](includes/prod_short.md)]sta, voit käyttää SMTP-yhdistinlaajennusta. Kun määrität SMTP-protokollaa käyttävän tilin, **Lähettäjän tyyppi** on tärkeä kenttä. Jos valitset **tietyn käyttäjän**, sähköpostit lähetetään käyttäen sen tilin nimeä ja muita tietoja, jota olet määrittämässä. Jos kuitenkin valitset **nykyisen käyttäjän**, sähköpostit lähetetään kullekin käyttäjätilille määritetyltä sähköpostitililtä. Valittu käyttäjä on samankaltainen kuin Lähetä toimintona. Lisätietoja: [Korvaavan lähettäjän osoitteen käyttäminen lähtevissä sähköpostiviesteissä](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages). 

> [!IMPORTANT]
> Jos käytössä on paikallinen [!INCLUDE[prod_short](includes/prod_short.md)], OAuth 2.0 -protokollan käyttö todennukseen on mahdollista. Jotta OAuthia voitaisiin käyttää SMTP:lle, kaikkien käyttäjien on oltava samassa Microsoft Entra -vuokralaisessa. 
> 
> Sinun on luotava sovellusrekisteröinti Azure-portaalissa ja sitten suoritettava **Määritä Microsoft Entra ID** -asetusten ohjatun määrityksen opas kohteessa[!INCLUDE[prod_short](includes/prod_short.md)] muodostaaksesi yhteyden Microsoft Entra ID:hen. Lisätietoja on kohdassa [Business Centralin sovelluksen rekisteröinnin luonti Azure-portaalissa](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).
>
> Exchange Online poistaa käytöstä perustodennuksen SMTP:lle. Tämä muutos ei vaikuta tällä hetkellä SMTP AUTH -todennusta käyttäviin vuokraajiin. Suosittelemme kuitenkin, että käytät [!INCLUDE [prod_short](includes/prod_short.md)] -ratkaisun uusinta versiota ja määrität OAuth 2.0-autentikoinnin   SMTP:lle. Emme lisää varmennepohjaista todennusta [!INCLUDE [prod_short](includes/prod_short.md)] -ratkaisun aiemmille versioille, esimerkiksi versiolle 14. Jos et voi määrittää OAuth 2.0 -todennusta, sinun kannattaa tutustua kolmannen osapuolen vaihtoehtoihin, jos haluat käyttää SMTP-sähköpostia aiemmissa versioissa.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## Käytä ohjattua Määritä sähköposti -määritystä

Asetusten ohjattu **Määritä sähköposti** -määritys auttaa sinua pääsemään alkuun nopeasti sähköpostiviestien käytössä.

> [!NOTE]
> Sinulla on oltava oletussähköpostitili, vaikka olisit lisännyt vain yhden tilin. Oletustiliä käytetään kaikissa sähköpostiskenaarioissa, joita ei ole määritetty muulle tilille. Lisätietoja: [Määritä skenaariot sähköpostitileille](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Määritä sähköpostitilit** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## Sähköpostiskenaarioiden määritys sähköpostitileille

Sähköpostiskenaariot ovat prosesseja, joihin liittyy asiakirjan lähettäminen. Esimerkiksi myynti- tai ostotilaus tai ilmoitus, esimerkiksi ulkoisen kirjanpitäjän kutsu. Tietyissä skenaarioissa voi käyttää tiettyjä sähköpostitilejä. Voit esimerkiksi määrittää, että kaikki käyttäjät lähettävät aina myyntiasiakirjat yhdeltä tililtä, ostoasiakirjat toiselta ja varasto- tai tuotantoasiakirjat kolmannelta tililtä. Voit määrittää, määrittää uudelleen ja poistaa skenaarioita milloin tahansa. Skenaarion voi määrittää vain yhdelle sähköpostitilille kerrallaan. Oletusarvoista sähköpostitiliä käytetään kaikissa skenaarioissa, joita ei ole määritetty muulle tilille.

**Sähköpostiskenaarion määritys** -sivulla voit valita **Aseta oletusliitteet** -toiminnon, joka lisää sähköpostiskenaarioiden liitteet. Liitteet ovat aina käytettävissä, kun luot sähköpostiviestin skenaarioon liittyvästä asiakirjasta. Jokaisessa sähköpostitilanteessa voi olla vähintään yksi oletusliite. Oletusliitteet lisätään automaattisesti sähköpostiin sähköpostiskenaarion yhteydessä. Kun esimerkiksi lähetät myyntitilauksen sähköpostilla, ohjelma lisää myyntitilausskenaariolle määritetyn oletusliitteen. Oletusliitteet näkyvät **Liitteet**-osassa **Luo sähköposti** -sivun alaosassa. Voit lisätä sähköpostiin manuaalisesti muita kuin oletusliitteitä.

<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## Näkymäkäytäntöjen määrittäminen

Voit hallita sähköpostiviestejä, joita käyttäjä voi käyttää sähköpostin Lähtevät- ja Lähetetyt-kansion sivuilla.

Valitse **Käyttäjän sähköpostinäkymän käytännöt** -kohdassa käyttäjä ja valitse sitten jokin seuraavista vaihtoehdoista **Sähköpostinäkymän käytäntö** -kentässä:

* **Näytä omat sähköpostit** -käyttäjä voi tarkastella vain omia sähköpostiviestejä.
* **Näytä kaikki sähköpostit** - Käyttäjä voi tarkastella kaikkia sähköpostiviestejä, kuten sähköposteja, jotka muut käyttäjät lähettävät.
* **Näytä, jos käyttöoikeudet kaikkiin liittyviin tietueisiin** – Tätä näyttökäytäntöä käytetään, jos muuta käytäntöä ei ole määritetty. Käyttäjä voi tarkastella sähköpostiviestejä, joita muut käyttäjät lähettävät, jos käyttäjällä on oikeus käyttää lähetettyä tietuetta ja kaikkia siihen liittyviä tietueita. Esimerkiksi käyttäjä A lähetti asiakkaalle kirjatun myyntilaskun. Käyttäjä B näkee sähköpostiviestin, jos hänellä on pääsy sekä laskuun että asiakkaaseen.
* **Näytä, jos käyttöoikeus mihin tahansa liittyvään tietueeseen** – Käyttäjä voi tarkastella muiden käyttäjien lähettämiä sähköpostiviestejä, jos käyttäjällä on vähintään yhden lähetettyyn tietueeseen liittyvän tietueen käyttöoikeus. Esimerkiksi käyttäjä A lähetti asiakkaalle kirjatun myyntilaskun. Käyttäjä B näkee sähköpostiviestin, jos hänellä on pääsy joko laskuun tai asiakkaaseen.

> [!NOTE]
> Jos jätät **Käyttäjätunnus**-kentän tyhjäksi ja valitset **Sähköpostinäkymän käytäntö** -toiminnon, näkymäkäytäntö koskee kaikkia käyttäjiä.

## Määritä, montako viestiä tili voi lähettää minuutissa

Jotkin sähköpostipalveluntarjoajat rajoittavat sähköpostiviestien määrää, jonka sähköpostitili voi lähettää kerralla tai tietyssä ajassa tai molemmissa. *Sähköpostin rajoitukseksi* kutsuttu käytäntö auttaa palveluntarjoajia hallitsemaan liikennettä niiden palvelimilla ja estää roskapostia. Jos sähköpostitili ylittää rajoituksen, Internet-palveluntarjoaja saattaa estää viestit. Voit varmistaa, että [!INCLUDE [prod_short](includes/prod_short.md)] -ratkaisusta lähettämiesi viestien määrä vastaa palveluntarjoajan rajaa, määrittämällä kunkin sähköpostitilisi rajoituksen.

Microsoft 365 -tili- ja Nykyinen käyttäjä -tyyppien oletus raja on 30, joka vastaa Exchange Online -ohjelman asettamaa rajaa.

Rajan voi määrittää kahdella tavalla:

* Kun luot uuden tilin ohjatun Määritä sähköposti -opastuksen avulla, määritä raja **Raja minuuttia kohti** -kentässä.
* Jos kyseessä on olemassa oleva sähköpostitili, voit määrittää rajoituksen tilin **Sähköpostiraja** -kentässä.

## Uudelleenkäytettävien sähköpostitekstien ja -asettelujen määrittäminen

Raporttien avulla voit sisällyttää myynti-, osto ja huoltoasiakirjojen avaintietoja sähköpostien teksteihin. Raportin asettelujen avulla määritetään sähköpostissa olevan tekstin tyyli ja sisältö. Sisältöön voi esimerkiksi kuulua tekstejä, kuten tervehdys tai asiakirjan tietoja edeltävät ohjeet. Tässä kuvataan , miten **Myynti–lasku**-raportti määritetään kirjatuille myyntilaskuille, mutta prosessi on samankaltainen muille raporteille.

> [!NOTE]
> Jos haluat käyttää asettelua sähköpostiviestien sisällön luomiseen, sinun on käytettävä siihen Word-tiedostotyyppiä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttivalinnat - Myynti** ja valitse sitten vastaava linkki.
2. Valitse **Raporttivalinta - Myynti** -sivun **Käyttö**-kentässä **Lasku**.
3. Valitse **Raportin tunnus** -kentän uudella rivillä esimerkiksi vakioraportti 1306.
4. Valitse **Käytä sähköpostin perustekstinä** -valintaruutu.
5. Valitse ensin **Sähköpostin perustekstin asettelun kuvaus** -kenttä ja sitten asettelu luettelosta.
6. Voit tarkastella tai muokata asettelua, johon sähköpostin teksti perustuu, valitsemalla ensin asettelun **Mukautetut raporttiasettelut** -sivulla ja sitten **Vie asettelu** -toiminnon. Jos mukautat asettelua, Lataa uusi asettelu käyttämällä **Tuo asettelu** -toimintoa.
    > [!NOTE]
    > Jos haluat mukauttaa vakioraportin asettelua, kuten 1306, sinun täytyy tehdä kopio raportista. [!INCLUDE [prod_short](includes/prod_short.md)] auttaa luomaan kopion, kun tuot mukautetun asettelun vakioraporttia varten. Uuden mukautetun raportin asettelun etuliitteenä on "Kopio kohteesta".
7. Jos haluat antaa asiakkaiden käyttää maksupalvelua, kuten PayPalia, sinun on määritettävä palvelu. Jälkeenpäin PayPal-tiedot ja -linkki lisätään sähköpostin tekstiin. Lisätietoja on kohdassa [Asiakkaan maksujen ottaminen käyttöön PayPalin kautta](sales-how-enable-payment-service-extensions.md).
8. Valitse **OK**-painike.

Kun nyt valitset esimerkiksi **Kirjattu myyntilasku** -sivulla **Lähetä**-toiminnon, sähköpostin perusteksti sisältää raportin 1306 asiakirjan tiedot, joita edeltää tyylitelty vakioteksti vaiheessa 5 valitun raporttiasettelun mukaan.

## Korvaavan lähettäjän osoitteen käyttäminen lähtevissä sähköpostiviesteissä

Jos käytät SMTP-yhdistinlaajennusta, voit muuttaa Microsoft Exchange -palvelimen **Lähetä –**- tai **Lähetä puolesta** -toimintoja lähtevien viestin lähettäjän osoitteen muuttamiseksi. [!INCLUDE[prod_short](includes/prod_short.md)] käyttää SMTP-tiliä Exchange-todennuksessa mutta joko korvaa lähettäjän osoitteen määrittämälläsi osoitteella tai muuttaa sitä puolesta-tiedolla.

Kun määrität tilin ja haluat käyttää Exchangen Lähetä nimellä- tai Lähetä puolesta -ominaisuuksia, valitse **Lähettäjän tyyppi** -kentässä **Tietty käyttäjä**.

Vaihtoehtoisesti voit valita **Nykyinen käyttäjä**, jos haluat, että ihmiset voivat lähettää viestejä SMTP-yhdistimen kautta. Viesti näyttää siltä, että se on lähetetty kirjautuneen käyttäjän käyttäjäkortissa määritetyn Yhteyssähköpostiosoite-kentässä määritetyltä sähköpostitililtä. Se toimii kuitenkin samalla tavalla kuin Lähetä nimellä -toiminto ja lähetetään SMTP-yhdistimen asetuksissa määritellyltä tililtä.

Seuraavassa on esimerkkejä tavoista, joilla Lähetä –- tai Lähetä puolesta -toimintoja käytetään [!INCLUDE[prod_short](includes/prod_short.md)]issa:

* Haluat ehkä, että toimittajille ja asiakkaille lähettämäsi osto- tai myyntitilaukset näyttävät tulevan _noreply@yourcompanyname.com_-osoitteesta.
* Kun työnkulku lähettää hyväksyntäpyynnön sähköpostitse käyttämällä pyytäjän sähköpostiosoitetta.

> [!Note]
> Lähettäjän osoitteiden korvaamiseen voidaan käyttää vain yhtä tiliä. Et siis voi käyttää yhtä korvaavaa osoitetta ostoprosesseissa ja toista myyntiprosesseissa.

<!--
### To set up the substitute sender address for all outbound email messages
1. In the **Exchange admin center** for your Microsoft 365 account, find the mailbox to use as the substitute address, and then copy or make a note of the address. If you need a new address, go to your Microsoft 365 admin center to create a new user and set up their mailbox.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
3. In the **Send As** field, enter the substitute address.
4. Copy or make a note of the address in the **User ID** field.
5. In the **Exchange admin center**, find the mailbox to use as the substitute address, and then enter the address from the **User ID** field in the **Send As** field. For more information, see [Use the EAC to assign permissions to individual mailboxes](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### To use the substitute address in approval workflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Copy or make a note of the address in the **User ID** field.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval User Setup**, and then choose the related link.
4. In the **Exchange admin center**, find the mailboxes for each user listed in the **Approval User Setup** page, and in the **Send As** field enter the address from the **User ID** field of the **SMTP Email Setup** page in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Manage permissions for recipients](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
6. To enable substitution, turn on the **Allow Sender Substitution** toggle.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] will determine which address to display in the following order: <br><br> 1. The address specified in the **E-Mail** field on the **Approval User Setup** page for messages in a workflow. <br> 2. The address specified in the **Send As** field in the **SMTP Email Setup** page. <br> 3. The address specified in the **User ID** field in the **SMTP Email Setup** page. -->

## Asiakirjan lähetysprofiilien määrittäminen

Voit säästää aikaa määrittämällä ensisijaisen tavan lähettää myyntiasiakirjoja kullekin asiakkaallesi. Sinun ei tarvitse valita lähetysvaihtoehtoa, esimerkiksi lähettääkö asiakirja sähköpostilla tai sähköisenä asiakirjana aina, kun lähetät asiakirjan. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).

## Valinnainen: Sähköpostin lokiinkirjauksen määrittäminen Exchange Onlinessa

Ota enemmän irti myyjien ja nykyisten tai potentiaalisten asiakkaiden välisestä viestinnästä. Voit seurata sähköpostien vaihtoa ja muuttaa ne toiminnallisiksi mahdollisuuksiksi. Lisätietoja: [Myyjien ja yhteyshenkilöiden välisten sähköpostiviestien seuraaminen](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## Valinnainen: Valvo sähköpostin käyttöä ja tee vianetsintä sähköpostin vioista telemetrian avulla

Järjestelmänvalvojat voivat ottaa telemetriaominaisuuden käyttöön kohdassa [!INCLUDE[prod_short](includes/prod_short.md)] käyttöön ja saada tietoja järjestelmän eri ominaisuuksien käytöstä ja virheistä. Sähköpostissa kirjaamme seuraavat toiminnot:

- Sähköpostiviesti lähetettiin onnistuneesti  
- Sähköpostin lähettämisen yrittäminen epäonnistui   
- Todennus SMTP-palvelimelle onnistui/epäonnistui  
- Yhteys SMTP-palvelimelle onnistui/epäonnistui  

Voit käyttää näitä tietoja sähköpostin käytön valvontaan ja sähköpostivirheiden vian määritykseen. Lisätietoja on kohdassa [Jäljityksen telemetrian analysointi (järjestelmänvalvojan sisältö)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace).  

## Sähköpostin määrittäminen Business Central On-Premises -versiossa

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises voidaan integroida Microsoft Azure -järjestelmään perustuvien palveluiden kanssa. Voit esimerkiksi käyttää Cortana Intelligence -toimintoa entistä älykkäämpien kassavirtaennusteiden muodostamiseksi, Power BI:tä visualisoidaksesi liiketoimintaasi ja Exchange Onlinea lähettääksesi sähköpostia. Integrointi näihin palveluihin perustuu sovelluksen rekisteröintiin Microsoft Entra ID:ssä. Sovelluksen rekisteröinti tarjoaa todennus- ja valtuutuspalveluita viestintää varten. Jotta voisit käyttää [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -version sähköpostitoimintoja , sinun täytyy rekisteröidä [!INCLUDE[prod_short](includes/prod_short.md)]in sovelluksena Azure-portaalissa ja yhdistää [!INCLUDE[prod_short](includes/prod_short.md)] sovellusrekisteröintiin. Seuraavissa luvuissa kerrotaan, miten tämä tehdään.

### Business Centralin sovelluksen rekisteröinnin luonti Azure-portaalissa

Kohteen [!INCLUDE[prod_short](includes/prod_short.md)] Azure-portaaliin rekisteröimisen vaiheet on kuvattu kohdassa [Rekisteröi sovellus Microsoft Entra ID:ssä](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

> [!NOTE]
> Jotta voisit käyttää sähköpostitoimintoja, sovelluksen rekisteröinnissä on käytettävä useita vuokralaisia.

Sähköpostiominaisuuksiin liittyvät asetukset ovat delegoituja käyttöoikeuksia, jotka myönnetään sovellusrekisteröinnille. Seuraavassa taulukossa on luettelo vähimmäisoikeuksista.

|Ohjelmistorajapinta / käyttöoikeuden nimi  |Tyyppi  |Kuvaus  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Delegoitu|Kirjaudu sisään ja lue käyttäjäprofiili.         |
|Microsoft Graph / Mail.ReadWrite |Delegoitu|Luo sähköpostiviestejä.         |
|Microsoft Graph / Mail.Send|Delegoitu|Lähetä sähköpostiviestejä.         |
|Microsoft Graph / offline_access|Delegoitu|Ylläpidä tietojen käyttöoikeuden hyväksyntää.|

Jos käytössä on SMTP-yhdistin ja haluat käyttää OAuth 2.0 -todennusta, oikeudet ovat hieman erilaiset. Seuraavassa taulukossa on oikeusluettelo.

|Ohjelmistorajapinta / käyttöoikeuden nimi  |Tyyppi  |Kuvaus  |
|---------|---------|---------|
|Microsoft Graph / offline_access|Delegoitu|Ylläpidä tietojen käyttöoikeuden hyväksyntää.|
|Microsoft Graph / openid|Delegoitu|Käyttäjien sisäänkirjautuminen.|
|Microsoft Graph / User.Read |Delegoitu|Kirjaudu sisään ja lue käyttäjäprofiili.         |
|Microsoft Graph / SMTP.Send|Delegoitu|Sähköpostien lähettäminen postilaatikosta SMTP AUTH -todennuksella.         |
|Office 365 Exchange Online / User.Read |Delegoitu|Kirjaudu sisään ja lue käyttäjäprofiili.         |

Kun luot sovelluksen rekisteröinnin, huomaa seuraavat tiedot. Tarvitset niitä, kun yhdistät [!INCLUDE[prod_short](includes/prod_short.md)]in sovellusrekisteröintiin.
 
* Sovelluksen (asiakkaan) tunnus
* Uudelleenohjauksen URI-osoite (valinnainen)
* Asiakasohjelman salaisuus

Sovelluksen rekisteröimisen yleiset ohjeet: [Pika-aloitus: sovelluksen rekisteröinti Microsoftin käyttäjätietoympäristössä](/azure/active-directory/develop/quickstart-register-app).

> [!NOTE]
Jos SMTP-protokollan käyttäminen sähköpostin lähettämiseen aiheuttaa ongelmia sen jälkeen, kun [!INCLUDE[prod_short](includes/prod_short.md)] yhdistettiin sovelluksen rekisteröintiin, syynä voi olla se, että SMTP AUTH ei ole otettu käyttöön vuokraajassa. Suositeltavaa onkin käyttää Microsoft 365- ja Nykyinen käyttäjä -yhdistimiä, sillä ne käyttävät Microsoft Graphin Mail-ohjelmointirajapintoja. Jos SMTP-protokollaa on kuitenkin käytettävä, SMTP AUTH voidaan ottaa käyttöön. Lisätietoja on kohdassa [Todennetun asiakasohjelman SMTP-lähetyksen (SMTP AUTH) ottaminen käyttöön tai poistaminen käytöstä Exchange Onlinessa](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### Yhdistä [!INCLUDE[prod_short](includes/prod_short.md)] sovellusrekisteröintiisi

Kun olet rekisteröinyt sovelluksen Azure-portaalissa, voit kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] käyttää **Sähköpostisovelluksen Microsoft Entra ID:n rekisteröinti** -sivua yhdistääksesi kohteen [!INCLUDE[prod_short](includes/prod_short.md)] siihen.

1. Valitse [!INCLUDE[prod_short](includes/prod_short.md)]issa ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköpostisovelluksen Microsoft Entra ID:n rekisteröinti** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Vaihtoehtoisesti, jos muodostat yhteyden ensimmäistä kertaa, voit käyttää ohjattua **Määritä sähköposti** -määritystä. Tässä tapauksessa oppaassa on myös sähköpostisovelluksen Microsoft Entra ID:n rekisteröintisivun, jolla voit lisätä sovelluksen rekisteröintiin liittyvät tiedot. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Microsoft Entra ID, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Microsoft Entra Directory - Multitenant)** or **Accounts in any organizational directory (Any Microsoft Entra Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Microsoft Entra ID, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## Katso myös

[Exchange Onlinen jaetut postilaatikot](/exchange/collaboration-exo/shared-mailboxes)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen yrityssähköpostina Outlookissa](admin-outlook.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in hakeminen mobiililaitteeseen](install-mobile-app.md)   
[[!INCLUDE[prod_short](includes/prod_short.md)]in hakeminen mobiililaitteeseen](install-mobile-app.md)   
[Jäljityksen telemetrian analysointi (järjestelmänvalvojan sisältö)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
