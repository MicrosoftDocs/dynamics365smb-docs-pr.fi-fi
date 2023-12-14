---
title: Yleistulostuksen tulostimien määrittäminen
description: Tietoja yleistulostuksen käyttämisestä Business Centralin pilvitulostuksena.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---

# Yleistulostuksen tulostimien määrittäminen

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Yleistulostus on tilauspohjainen Microsoft 365 -palvelu, joka suoritetaan kokonaisuudessaan Microsoft Azuressa. Yleistulostusportaalin kautta käytettävissä on keskitetty tulostimen hallinta. [!INCLUDE[prod_short](includes/prod_short.md)] tuo yleistulostuksessa määritetyt tulostimet asiakasohjelmakäyttäjien käyttöön **Yleistulostuksen integrointi** -laajennuksen avulla.

![Yleistulostus-asetus.](media/Universal-Print-arch.png)

Täydellinen määritys edellyttää, että työskentelet sekä Microsoft Azuressa [Azure-portaalia](https://portal.azure.com) käyttäen että [!INCLUDE[prod_short](includes/prod_short.md)]ssa. Määritys jaetaan kahteen tässä artikkelissa käsiteltävään päätehtävään:

1. Microsoft Azureissa yleistulostus määritetään ja Business Centralissa käytettävät tulostimet lisätään tulostusresurssiin. Lisätietoja on [tässä osassa](#set-up-universal-print-and-printers-in-microsoft-azure).
2. [!INCLUDE[prod_short](includes/prod_short.md)]issa tulostimet lisätään yleistulostuksen tulostusresursseista. Siirry verkkoversiossa [tähän osaan](#add-printers-in-business-central-online) tai paikallisessa versiossa [tänne](#add-printers-in-business-central-on-premises).

## Vaatimukset

- Tuetut tulostimet

  [!INCLUDE[prod_short](includes/prod_short.md)] tukee samoja tulostimia kuin yleistulostus, ja nämä tulostimet voivat olla joko yhteensopivia yleistulostuksen kanssa tai sitten ne eivät ole sitä. Yhteensopimattomat tulostimet eivät voi olla suoraan yhteydessä yleistulostukseen, joten niissä tarvitaan ylimääräinen yleistulostuksen toimittama yhdistinohjelmisto. Joitakin vanhoja tulostimia ei ehkä tueta. 

- Yleistulostus:

  - Yleistulostuksen tilaus tai käyttöoikeus organisaation osalta.

    Lisätietoja on kohdassa [Yleistulostuksen käyttöoikeus](/universal-print/fundamentals/universal-print-license).

  - Azuressa on oltava **Tulostimen järjestelmänvalvoja** (tai Tulostuksen hallinta)- ja **Yleinen järjestelmänvalvoja** -roolit.

    Yleistulostuksen hallintaa varten tilillä on oltava **Tulostimen järjestelmänvalvoja** tai (Tulostuksen hallinta)- ja **Yleinen järjestelmänvalvoja** -roolit Microsoft Entra ID:ssä. Näitä rooleja tarvitaan vain yleistulostuksen hallintaan. Niitä ei tarvita henkilöille, jotka määrittävät ja käyttävät tulostimia käytetään [!INCLUDE[prod_short](includes/prod_short.md)]issa.

- [!INCLUDE[prod_short](includes/prod_short.md)] online ja paikallinen versio:

  - [!INCLUDE[prod_short](includes/prod_short.md)]in vuoden 2021 1. julkaisuaalto tai uudempi.
  - Asennettu **Yleistulostuksen integrointi** -laajennus.

    Tämä laajennus julkaistaan ja asennetaan oletusarvoisesti [!INCLUDE[prod_short](includes/prod_short.md)]in verkkoversion ja paikallisen ympäristön osana. Sen asennuksen voi tarkistaa **Laajennuksen hallinta** -sivulla. Lisätietoja on kohdassa [Laajennusten asentaminen ja asennusten poistaminen Business Centralissa](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] vain paikallinen:
  - Microsoft Entra ID- tai NavUserPassword-todennus on määritetty.
    > [!NOTE]
    >  Yleistulostuslaajennus ei tue palveluiden välistä (S2S) todennusta. Se vaatii kirjautuneen käyttäjän lähettämään tulostustyöt Yleistulostus-palvelulle Graph API -liittymän avulla.
  - Business Central -sovellus on rekisteröity Microsoft Entra -vuokraajaan ja [!INCLUDE[prod_short](includes/prod_short.md)]iin.

    Muiden [!INCLUDE[prod_short](includes/prod_short.md)]issa käytettävien Azure-palvelujen tavoin yleistulostus edellyttää, että sovellus rekisteröidään [!INCLUDE[prod_short](includes/prod_short.md)]iin Microsoft Entra ID:ssä. Sovelluksen rekisteröinti tuottaa [!INCLUDE[prod_short](includes/prod_short.md)]in ja yleistulostuksen välisiä todennus- ja valtuutuspalveluita.

    Käyttöönotossa voi olla jo käytössä muiden Azure-palvelujen, kuten Power BI:n, sovelluksen rekisteröinti. Siinä tapauksessa aiemmin luotua sovelluksen rekisteröintiä käytetään myös yleistulostuksessa sen sijaan, että lisättäisiin uusi rekisteröinti. Tässä tapauksessa sovelluksen rekisteröinti on vain muokattava sisältämään Microsoft Graph -ohjelmointirajapinnan soveltuvat tulostusoikeudet: **PrinterShare.ReadBasic.All**, **PrintJob.Create** ja **PrintJob.ReadBasic.** 

    Lisätietoja sovelluksen rekisteröimisestä ja soveltuvien oikeuksien määrittämisestä on kohdassa [Sovelluksen rekisteröinti Microsoft Entra ID:ssä](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

## Yleistulostuksen ja tulostimien määrittäminen Microsoft Azuressa

Ennen yleistulostuksen tulostimien hallinnan aloittamista Business Centralissa yleistulostus on otettava käyttöön Azuressa ja siihen on määritettävä käytettävät tulostimet.

Lisätietoja määrittämisestä on yleistulostuksen ohjeiden kohdassa [Aloitus: yleistulostuksen määrittäminen](/universal-print/fundamentals/universal-print-getting-started). Seuraavassa on yhteenveto suoritettavista vaiheista. Suurin osa näistä vaiheista tehdään Azure-portaalissa.

1. Määritä yleistulostuksen käyttöoikeudet itsellesi ja muille käyttäjille.

    Käyttöoikeuden määrittäminen määräytyy sen mukaan, integroidaanko paikallinen Business Central vai verkkoversio.

    - Jos kyseessä on [!INCLUDE[prod_short](includes/prod_short.md)] Online, käyttöoikeudet määritetään Microsoft 365 -hallintakeskuksessa.

      Lisätietoja on kohdassa [Microsoft-hallintakeskuksen ohje – Käyttöoikeuksien määrittäminen käyttäjille](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Jos kyse on paikallisesta [!INCLUDE[prod_short](includes/prod_short.md)]ista, käyttöoikeudet määritetään vuokraajassa Azure-portaalia käyttämällä.

      Lisätietoja on kohdassa [Käyttöoikeuksien määrittäminen tai poistaminen Azure-portaalissa](/azure/active-directory/fundamentals/license-users-groups).

2. Asenna yleistulostuksen yhdistin niiden tulostimien rekisteröintiä varten, jotka eivät voi olla suoraan yhteydessä yleistulostukseen.

    Useimmat markkinoilla olevat tulostimet eivät voi olla suoraan yhteydessä yleistulostukseen, joten yleistulostuksen yhdistin on asennettava. Lisätietoja on kohdassa [Yleistulostuksen yhdistimen asentaminen](/universal-print/fundamentals/universal-print-connector-installation).

3. Rekisteröi tulostimet yleistulostukseen.

    Kun tulostin on rekisteröity, yleistulostus havaitsee sen.

    - Jos tulostin voi olla yhteydessä suoraan yleistulostukseen, noudata tulostimen valmistajan antamia ohjeita.

    - Rekisteröi muut tulostimet käyttämällä yleistulostuksen yhdistintä. 

      Lisätietoja on kohdassa [Tulostimen rekisteröiminen](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Tulostimen ominaisuuksien muuttaminen (valinnainen)

    Kun tulostin on rekisteröity, voit tarkastella ja muuttaa tulostimen ominaisuuksia, kuten oletusasetuksia.

    Lisätietoja on kohdassa [Tulostimen asetusten hallinta yleistulostusportaalin avulla](/universal-print/portal/configure-printer-settings).

5. Jaa tulostimet käyttäjien kanssa.

    Jokainen tulostin, jota halutaan käyttää [!INCLUDE[prod_short](includes/prod_short.md)]issa, on lisättä yleistulostuksen *tulostusresursseihin*. Tulostimen käyttöoikeuden tarvitseva käyttäjä on lisättävä tulostusresurssin jäseneksi. Lisätietoja on kohdassa [Tulostimen jakaminen](/universal-print/portal/share-printers).

    > [!TIP]
    > Käyttäjiä voi aina lisätä tai poistaa myöhemmin. Lisätietoja on kohdassa [Tulostimen käyttöoikeudet](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).

6. Ota asiakirjan muuntaminen käyttöön.

    Yleistulostus hahmontaa tulostuksen sisällön XPS-muodossa. Osa markkinoilla olevista vanhoista tulostimista ei tue XPS-sisällön hahmontamista vaan usein tuetaan vain PDF-muotoa. Tulostaminen tällaisiin tulostimiin epäonnistuu, ellei yleistulostusta ole määritetty muuntamaan asiakirjat tulostimen tukemaan muotoon.

    Lisätietoja on kohdassa [Asiakirjan muuntamisen yleiskatsaus](/universal-print/portal/document-conversion).

Olet nyt valmis lisäämään tulostimia [!INCLUDE[prod_short](includes/prod_short.md)]iin, määrittämään raporttien oletustulostimet ja tulostamaan.  

## Tulostimien lisääminen Business Central onlinessa

Kun tulostimet on määritetty ja jaettu yleistulostuksessa, ne voidaan lisätä käyttöä varten [!INCLUDE[prod_short](includes/prod_short.md)]iin. Yleistulostuksen tulostimia voi lisätä kahdella tavalla. Tulostimet voidaan lisätä kaikki kerralla tai yksi kerrallaan.

Jos tulostimet lisätään yksitellen, sama yleistulostuksen tulostin voidaan määrittää [!INCLUDE[prod_short](includes/prod_short.md)]issa useita kertoja. Sen jälkeen kussakin lisätyssä tulostimessa voidaan muuttaa tulostusasetuksia, kuten paperilokeroa, kokoa ja suuntaa. Tällä tavoin tulostimet voidaan määrittää erilaisille raporteille ja asiakirjoille, joilla on erityisiä tulostusvaatimuksia.

> [!NOTE]
> Onko käytössä paikallinen [!INCLUDE[prod_short](includes/prod_short.md)]? Siirry siinä tapauksessa [seuraavaan osaan](#add-printers-in-business-central-on-premises), sillä ensimmäinen määritys on hieman erilainen.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostimien hallinta** ja valitse sitten vastaava linkki.
2. Valitse ensin **Yleistulostus** ja valitse sitten jokin seuraavista vaihtoehdoista:

   - **Lisää kaikki yleistulostuksen tulostimet** -vaihtoehdon avulla voi lisätä kaikki tulostimet, joita ei ole vielä lisätty. Tätä vaihtoehtoa voi käyttää, vaikka tulostimia olisi jo lisätty.
   - **Lisää yleistulostuksen tulostin** -vaihtoehdolla voi lisätä tietyn tulostimen.  
3. Noudata näytön ohjeita.

    - Jos valitsit **Lisää kaikki yleistulostuksen tulostimet**, **Lisää yleistulostuksen tulostimet** -määritys käynnistyy. 

    - Jos valitsit **Lisää yleistulostuksen tulostin**, **Yleistulostuksen asetukset** -sivu avautuu. Täytä **Nimi**-kenttä ja valitse sen jälkeen yleistulostuksen sisältävä tulostusresurssi valitsemalla **...** **Yleistulostuksen tulostusresurssi** -kentän vieressä. Täytä jäljellä olevat kentät tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Kun tulostin on lisätty, sen asetuksia voi tarkastella ja muuttaa **Tulostimen hallinta** -sivulla. Valitse ensin tulostin ja sitten **Muokkaa tulostimen asetuksia**.

## Tulostimien lisääminen paikallisessa Business Centralissa

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Ennen kuin käyttäjä voi lisätä tai käyttää yleistulostuksen tulostimia Business Centralissa, käyttäjälle on myönnettävä yleistulostuksen käyttämien Azure-palvelujen käyttöoikeus sekä seuraavanlaisten tietojen ja toimintojen oikeudet:

- kirjautuminen ja käyttäjäprofiilin lukeminen
- tulostustyön perustietojen lukeminen
- tulostustöiden luominen.

Tämä tehdään yleensä silloin, kun käyttäjä muodostaa ensimmäisen kerran yhteyden yleistulostuksessa käytettävään Azureen rekisteröityyn sovellukseen. Business Central onlinessa tämä valtuutustyönkulku tapahtuu sujuvasti ilman käyttäjän toimia. Paikallinen Business Central toimii kuitenkin eri tavalla. Se edellyttää, että yleistulostuksen tulostimien käyttäjä käynnistää valtuutustyönkulun, mikä yleensä tarvitsee tehdä vain kerran. Se on yksinkertaisinta tehdä seuraavaksi annettavien ohjeiden avulla. Vaihtoehtoisesti voidaan muodostaa yhteys toiseen samaa Azure-rekisteröityä sovellusta, kuten Power BI:tä tai OneDrivea, käyttävään sovellukseen. Kunkin käyttäjän on yleensä toimittava näin vain kerran.

> [!NOTE]
> Järjestelmänvalvojia suositellaan suorittamaan tämä tehtävä ennen muita käyttäjiä. Tämän jälkeen käyttäjille, joiden on käytettävä yleistulostuksen tulostimia, voidaan kertoa, miten se tehdään. Jos yleistulostuksen Azure-rekisteröity sovellus edellyttää, että järjestelmänvalvoja hyväksyy ohjelmointirajapinnan oikeudet, suostumus on helpompi antaa organisaation puolesta. Järjestelmänvalvojan suostumus voidaan antaa Azure-portaalissa ja seuraavien vaiheiden suorittamisen aikana. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### Ensimmäinen yhdistäminen yleistulostukseen

Yhteys yleistulostuspalveluun muodostetaan ensimmäisen kerran seuraavien ohjeiden avulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostimien hallinta** ja valitse sitten vastaava linkki.
2. Käynnistä **Lisää Yleistulostus-tulostimet** -asetusten ohjattu määritys (ohjattu toiminto) valitsemalla **Yleistulostus** > **Lisää kaikki Yleistulostus-tulostimet**.
3. Seuraa näytön ohjeita **MICROSOFT ENTRA -PALVELUN KÄYTTÖOIKEUDET** -sivulle saakka.

    <!--The MICROSOFT ENTRA SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Microsoft Entra ID setup, checking your Universal Print license, and then adding the printers.-->

   ![Näyttää MICROSOFT ENTRA -PALVELUN KÄYTTÖOIKEUDET -sivun](media/azure-ad-services-permissions.png "Näyttää MICROSOFT ENTRA -PALVELUN KÄYTTÖOIKEUDET -sivun")

4. Valitse **Valtuuta Azure-palvelut** -linkki.

   1. Jos **Lupapyyntö on lähetetty** -sivu avautuu, lue sen tiedot huolellisesti. Hyväksy tiedot ja jatka valitsemalla **Hyväksy**. Järjestelmänvalvoja voi antaa suostumuksen kaikkien käyttäjien puolesta valitsemalla **Suostumus organisaation puolesta**.

      ![Näkyvissä Azuren lupapyyntösivu](media/azure-ad-permissions-requested.png "Azuren lupapyyntösivu")

   2. Kirjaudu pyydettäessä sisään käyttämällä nimeä ja salasanaa.

5. Valtuutuksen valmistumisen jälkeen palataan **Lisää Yleistulostus-tulostimet**  -sivulle. Viimeistele määritykset valitsemalla **Seuraava** > **Valmis**.

Kun tulostin on lisätty, sen asetuksia voi tarkastella ja muuttaa **Tulostimen hallinta** -sivulla. Valitse ensin tulostin ja sitten **Muokkaa tulostimen asetuksia**.

Ensimmäisen kirjautumisen jälkeen yleistulostuksen tulostimilla voidaan tulostaa raportteja ja muita tulostustöitä. Lisätietoja on kohdassa [Raportin tulostaminen](ui-work-report.md#PrintReport). Tulostimia voi lisätä, poistaa tai vaihtaa palaamalla **Tulostuksen hallinta** -sivulle ja valitsemalla **Yleistulostus**.

## Yleisiä ongelmia ja niiden ratkaisuja

Tässä osassa on tietoja yleisistä ongelmista, joita käyttäjillä voi olla yritettäessä määrittää tai käyttää yleistulostuksen tulostimia.

### Et voi käyttää tulostinta \<your-printer\>.

Jos käyttäjä näkee tämän sanoman, kun asiakirjaa yritetään tulostaa yleistulostuksen tulostimeen, syy voi olla jokin seuraavista:

- Käyttäjän Microsoft 365- tai Azure Active AD -tiliin ei ole määritetty yleistulostuksen käyttöoikeutta. 
- Käyttäjää ei ole määritetty tulostusresurssiin yleistulostuksessa.
- (Paikallinen) Yleistuloksessa käytetty Azure-sovellusrekisteröinti ei toimi tai sitä muutettu sen jälkeen, kun käyttäjä kirjautui edellisen kerran sisään.
- (Paikallinen) Käyttäjä ei ole vielä kirjautunut yleistulostuksen Azure-rekisteröityyn sovellukseen eikä antanut suostumustaan ensimmäistä kertaa.

## Virhe noudettaessa sinulle jaettuja tulostimia.

Jos käyttäjä näkee tämän sanoman yrittäessään lisätä yleistulostuksen tulostin **Tulostimen hallinta** -sivulta, syynä on yleensä se, että käyttäjä ei ole vielä kirjautunut yleistulostussovelluksen Azure-rekisteröityyn sovellukseen ja antanut suostumustaan ensimmäisellä kerralla. 
<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps




-->

## Seuraavat vaiheet
[Oletustulostimien määrittäminen](ui-specify-printer-selection-reports.md).

## Katso myös

[Tulostimien yleiskatsaus](admin-printer-setup-overview.md)  
[Sähköpostitulostimien määrittäminen](admin-printer-setup-email.md)
[Raportin tulostaminen](ui-work-report.md#PrintReport)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eräajojen ajaminen](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
