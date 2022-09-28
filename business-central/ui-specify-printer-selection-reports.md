---
title: Tulostimien määrittäminen
description: Tietoja raporttien ja asiakirjojen käytettävissä olevien tulostimien määrittämisestä sekä Business Centralin erilaisista tulostusominaisuuksista.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.search.form: 2650, 2750, 2752, 2753, 2754, 8900,
ms.date: 06/24/2021
ms.author: jswymer
ms.openlocfilehash: 8915015f015642a85439fbdd5511271b06a8358f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531294"
---
# <a name="set-up-printers"></a>Tulostimien määrittäminen

Asiakirjojen ja raporttien tulostaminen [!INCLUDE[prod_short](includes/prod_short.md)]ista on tärkeä tehtävä yrityskäyttäjille. Käyttäjät haluavat yleensä lähettää tulostustyöt suoraan yhteen organisaation tulostimista riippumatta siitä, mitä [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelmaa tai -sovellusta he käyttävät. Koska [!INCLUDE[prod_short](includes/prod_short.md)] online on pilvipalvelu, se ei voi olla suoraan yhteydessä käyttäjien laitteisiin yhdistettyihin tulostimiin. Se voidaan kuitenkin yhdistää pilvipohjaisiin tulostimiin.

[!INCLUDE[prod_short](includes/prod_short.md)]issa on seuraavat tulostamista tukevat ominaisuudet:

|Ominaisuus|Kuvaus|Verkkoasiakasohjelma| Mobiilisovellus|Teamsin käyttöön sopiva sovellus|
|-------|-----------|----------|-----------|--------------|
|Yleistulostus|Yleistulostus on Microsoftin pilvipalveluna saatava tulostimen hallintaratkaisu. Tällä ominaisuudessa tulostimet voidaan määrittää yleistulostuksessa, jonka jälkeen rekisteröidään käyttöä varten [!INCLUDE[prod_short](includes/prod_short.md)]issa. Ominaisuuden käyttöä varten tarvitaan yleistulostustilaus ja **Yleistulostuksen integrointi** -laajennus.|![toimii verkossa.](media/check.png)|![toimii verkossa.](media/check.png)|![toimii verkossa](media/check.png)|
|Sähköpostitulostus|Tällä ominaisuudella voidaan määrittää sähköpostitulostukseen sopivia tulostimia. [!INCLUDE[prod_short](includes/prod_short.md)] lähettää sitten tulostustyöt tulostimeen käyttämällä tulostimen sähköpostiosoitetta. Ominaisuuden käyttöä varten tarvitaan tulostin, jossa sähköpostitulostus on otettu käyttöön, ja **Lähetä sähköpostitulostimeen** -laajennus.|![toimii verkossa.](media/check.png)|![toimii verkossa](media/check.png)|![toimii verkossa](media/check.png)|
|Selaimesta tulostaminen|Käyttäjän selaimen tulostustoiminto käsittelee tulostustyöt. Jos pilvitulostinta ei ole asennettu ja määritetty tai jos asennettu tulostin ei toimi kunnolla, tulostuksessa käytetään selaimen tulostusasetusten oletustulostinta. Raportin pyyntösivun **Tulostin**-kentässä on teksti *(Käsitellään selaimessa)*.|![toimii verkossa](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] tukee myös mukautettuja tulostinlaajennuksia, joilla saadaan käyttöön vielä lisää tulostusominaisuuksia. Niinpä jos asennettuna on mukautettuja tulostinlaajennuksia, sovelluksessa voi olla sellaisia tulostusominaisuuksia, joita ei käsitellä tässä artikkelissa. 

## <a name="set-up-universal-print"></a>Yleistulostuksen määrittäminen

Yleistulostus on tilauspohjainen Microsoft 365 -palvelu, joka suoritetaan kokonaisuudessaan Microsoft Azuressa. Yleistulostusportaalin kautta käytettävissä on keskitetty tulostimen hallinta. [!INCLUDE[prod_short](includes/prod_short.md)] tuo yleistulostuksessa määritetyt tulostimet asiakasohjelmakäyttäjien käyttöön **Yleistulostuksen integrointi** -laajennuksen avulla.

![Yleistulostus-asetus.](media/Universal-Print-arch.png)

Täydellinen määritys edellyttää, että työskentelet sekä Microsoft Azuressa [Azure-portaalia](https://portal.azure.com) käyttäen että [!INCLUDE[prod_short](includes/prod_short.md)]ssa.

### <a name="supported-printers"></a>Tuetut tulostimet

[!INCLUDE[prod_short](includes/prod_short.md)] tukee samoja tulostimia kuin yleistulostus, ja nämä tulostimet voivat olla joko yhteensopivia yleistulostuksen kanssa tai sitten ne eivät ole sitä. Yhteensopimattomat tulostimet eivät voi olla suoraan yhteydessä yleistulostukseen, joten niissä tarvitaan ylimääräinen yleistulostuksen toimittama yhdistinohjelmisto. Joitakin vanhoja tulostimia ei ehkä tueta. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Vaatimukset

**[!INCLUDE[prod_short](includes/prod_short.md)]**

- [!INCLUDE[prod_short](includes/prod_short.md)]in vuoden 2021 1. julkaisuaalto tai uudempi
- Asennettu **Yleistulostuksen integrointi** -laajennus

    Tämä laajennus julkaistaan ja asennetaan oletusarvoisesti [!INCLUDE[prod_short](includes/prod_short.md)]in verkkoversion ja paikallisen ympäristön osana.  Sen asennuksen voi tarkistaa **Laajennuksen hallinta** -sivulla. Lisätietoja on kohdassa [Laajennusten asentaminen Business Centraliin ja asennusten poistaminen](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] paikallisessa ympäristössä:
  - Azure Active Directory (AD)- tai NavUserPassword-todennus on määritetty
  - Business Central -sovellus on rekisteröity Azure AD -vuokraajaan ja [!INCLUDE[prod_short](includes/prod_short.md)]iin

      Muiden [!INCLUDE[prod_short](includes/prod_short.md)]issa käytettävien Azure-palvelujen tavoin yleistulostus edellyttää, että sovellus rekisteröidään [!INCLUDE[prod_short](includes/prod_short.md)]iin Azure Active Directoryssa (Azure AD). Sovelluksen rekisteröinti tuottaa [!INCLUDE[prod_short](includes/prod_short.md)]in ja yleistulostuksen välisiä todennus- ja valtuutuspalveluita.

      Käyttöönotossa voi olla jo käytössä muiden Azure-palvelujen, kuten Power BI:n, sovelluksen rekisteröinti. Siinä tapauksessa aiemmin luotua sovelluksen rekisteröintiä käytetään myös yleistulostuksessa sen sijaan, että lisättäisiin uusi rekisteröinti. Tässä tapauksessa sovelluksen rekisteröinti on vain muokattava sisältämään Microsoft Graph -ohjelmointirajapinnan soveltuvat tulostusoikeudet.

      Lisätietoja soveltuvien oikeuksien määrittämisestä rekisteröidyssä sovelluksessa on kohdassa [Sovelluksen rekisteröinti Azure Active Directoryssa](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**Yleistulostus**

- Yleistulostuksen tilaus tai käyttöoikeus organisaation osalta.

    Lisätietoja on kohdassa [Yleistulostuksen käyttöoikeus](/universal-print/fundamentals/universal-print-license).

- Azuressa oltava **Tulostimen hallinta**- ja **Yleinen järjestelmänvalvoja** -roolit.

    Yleistulostuksen hallintaa varten tilillä on oltava **Tulostuksen hallinta**- ja **Yleinen järjestelmänvalvoja** -roolit Azure AD:ssa. Näitä rooleja tarvitaan vain yleistulostuksen hallintaan. Käyttäjät eivät tarvitse näitä rooleja tulostimien käyttämiseen [!INCLUDE[prod_short](includes/prod_short.md)]issa.

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Yleistulostuksen määrittäminen ja tulostimien lisääminen Microsoft Azuressa

Ennen kuin yleistulostuksen tulostimia voi hallita Business Centralissa, yleistulostus on otettava käyttöön Azuressa ja siihen on määritettävä käytettävät tulostimet.

Lisätietoja määrittämisestä on yleistulostuksen ohjeiden kohdassa [Aloitus: yleistulostuksen määrittäminen](/universal-print/fundamentals/universal-print-getting-started). Seuraavassa on yhteenveto suoritettavista vaiheista. Suurin osa näistä vaiheista tehdään Azure-portaalissa.

1. Määritä yleistulostuksen käyttöoikeudet itsellesi ja muille käyttäjille.

    Käyttöoikeuden määrittäminen määräytyy sen mukaan, integroidaanko paikallinen Business Central vai verkkoversio.

    - Jos kyseessä on [!INCLUDE[prod_short](includes/prod_short.md)] Online, käyttöoikeudet määritetään Microsoft 365 -hallintakeskuksessa.

      Lisätietoja on kohdassa [Microsoft-hallintakeskuksen ohje – Käyttöoikeuksien määrittäminen käyttäjille](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Jos kyse on paikallisesta [!INCLUDE[prod_short](includes/prod_short.md)]ista, käyttöoikeudet määritetään Azure-vuokraajassa Azure-portaalia käyttämällä.

      Lisätietoja on kohdassa [Azure Directory – käyttöoikeuksien määrittäminen tai poistaminen Azure Active Directory -portaalissa](/azure/active-directory/fundamentals/license-users-groups).

2. Asenna yleistulostuksen yhdistin niiden tulostimien rekisteröintiä varten, jotka eivät voi olla suoraan yhteydessä yleistulostukseen.

    Useimmat markkinoilla olevat tulostimet eivät voi olla suoraan yhteydessä yleistulostukseen. Kyseisiä tulostimia varten on asennettava yleistulostuksen yhdistin. Lisätietoja on kohdassa [Yleistulostuksen yhdistimen asentaminen](/universal-print/fundamentals/universal-print-connector-installation).

3. Rekisteröi tulostimet yleistulostukseen.

    Kun tulostin on rekisteröity, yleistulostus havaitsee sen.

    - Jos tulostin voi olla yhteydessä suoraan yleistulostukseen, noudata tulostimen valmistajan antamia ohjeita.

    - Rekisteröi muut tulostimet käyttämällä yleistulostuksen yhdistintä. 

      Lisätietoja on kohdassa [Tulostimen rekisteröinti](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Tulostimen ominaisuuksien muuttaminen (valinnainen)

    Kun tulostin on rekisteröity, tulostimen ominaisuuksia, kuten oletusasetuksia, voi tarkastella ja muuttaa.

    Lisätietoja on kohdassa [Tulostimen asetusten hallinta yleistulostusportaalin avulla](/universal-print/portal/configure-printer-settings).

5. Jaa tulostimet.

    Jokainen tulostin, jota halutaan käyttää [!INCLUDE[prod_short](includes/prod_short.md)]issa, on jaettava yleistulostuksessa. avulla.

    <!--For more information, see [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

    Lisätietoja on kohdassa [Tulostimen jakaminen](/universal-print/portal/share-printers).

6. Anna jaettujen tulostimien käyttöoikeudet käyttäjille.

    <!--For more information, see [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

    Lisätietoja on kohdassa [Tulostimen käyttöoikeudet](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Ota asiakirjan muuntaminen käyttöön.

    Yleistulostus hahmontaa tulostuksen sisällön XPS-muodossa. Osa markkinoilla olevista vanhoista tulostimista ei tue XPS-sisällön hahmontamista vaan usein tuetaan vain PDF-muotoa. Tulostaminen tällaisiin tulostimiin epäonnistuu, ellei yleistulostusta ole määritetty muuntamaan asiakirjat tulostimen tukemaan muotoon.

    Lisätietoja on kohdassa [Asiakirjan muuntamisen yleiskatsaus](/universal-print/portal/document-conversion).

Olet nyt valmis lisäämään tulostimia [!INCLUDE[prod_short](includes/prod_short.md)]iin, määrittämään raporttien oletustulostimet ja tulostamaan.  

### <a name="add-universal-printer-printers-to-business-central"></a>Yleistulostuksen tulostimien lisääminen Business Centralin

Kun tulostimet on määritetty ja jaettu yleistulostuksessa, niitä voi käyttää Business Centralissa. Yleistulostuksen tulostimia voi lisätä kahdella tavalla. Tulostimet voidaan lisätä kaikki kerralla tai yksi kerrallaan.

Jos tulostimet lisätään yksitellen, sama yleistulostuksen tulostin voidaan määrittää Business Centralissa useita kertoja. Sen jälkeen kussakin lisätyssä tulostimessa voidaan muuttaa tulostusasetuksia, kuten paperilokeroa, kokoa ja suuntaa. Tällä tavoin tulostimet voidaan määrittää erilaisille raporteille ja asiakirjoille, joilla on erityiset tulostusvaatimukset.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostimien hallinta** ja valitse sitten vastaava linkki.
2. Valitse ensin **Yleistulostus** ja sitten jokin seuraavista vaihtoehdoista:

    - **Lisää kaikki yleistulostuksen tulostimet** -vaihtoehdolla voi lisätä kaikki tulostimet, joita ei ole vielä lisätty. Tätä vaihtoehtoa voi käyttää, vaikka tulostimia olisi jo lisätty. 

    - **Lisää yleistulostuksen tulostin** -vaihtoehdolla voi lisätä tietyn tulostimen.  
3. Noudata näytön ohjeita.

    - Jos valitsit **Lisää kaikki yleistulostuksen tulostimet**, **Lisää yleistulostuksen tulostimet** -määritys käynnistyy. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Jos valitsit **Lisää yleistulostuksen tulostin**, **Yleistulostuksen asetukset** -sivu avautuu. Täytä **Nimi**-kenttä ja valitse yleistulostuksen tulostin valitsemalla **...** **Yleistulostuksen tulostusresurssi** -kentän vieressä. Täytä jäljellä olevat kentät tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Nämä toiminnot vahvistavat Azure AD -asetukset (paikallisessa versiossa), tarkistavat, että käytössä on yleistuloksen käyttöoikeus, ja lopulta lisäävät tulostimet.

    > [!NOTE]
    > Jos yhteys muodostetaan ensimmäisen kerran paikallisessa versiossa yleistulostukseen, AZURE ACTIVE DIRECTORY -PALVELUN KÄYTTÖOIKEUDET -sivu avautuu, sinua pyydetään antamaan suostumus Azure-palveluihin. Suostumus tarvitsee antaa vain kerran.

Kun tulostin on lisätty, sen asetuksia voi tarkastella ja muuttaa **Tulostimen hallinta** -kohdassa. Valitse ensin tulostin ja sitten **Muokkaa tulostimen asetuksia**. 

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

## You don't have access to the printer

- You have not been assigned a Up license
- You have not been given access to the printer in UP.
- (On-prem) The app registration has been broken
-->
## <a name="set-up-email-print"></a>Sähköpostitulostuksen määrittäminen

### <a name="prerequisites"></a>Vaatimukset

- [!INCLUDE[prod_short](includes/prod_short.md)]in vuoden 2020 1. julkaisuaalto tai uudempi
- **Lähetä sähköpostitulostimeen** -laajennus on asennettu

    Tämä laajennus asennetaan oletusarvoisesti. Lisätietoja laajennuksien asentamisesta on kohdassa 
- Sähköpostitoiminnot on määritetty.

   Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

### <a name="add-an-email-printer"></a>Sähköpostitulostimen lisääminen

**Tulostimen hallinta** -sivulla on näkyvissä tällä hetkellä määritetyt tulostimet. Sivulta pääsee myös kunkin tulostimen **Asetukset**-sivulle, jossa voi muokata nykyisiä määrityksiä ja määrittää uuden tulostimen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostimien hallinta** ja valitse sitten vastaava linkki.
2. Valitse ensin **Sähköpostitulostus** ja sitten **Lisää sähköpostitulostin**.
3. Täytä tarvittavat kentät **Sähköpostitulostimen asetukset** -sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Tulostimelle on valittava manuaalisesti sopiva paperikoko, koska paikallista tulostinta tai käyttäjän asetuksia ei voi tallentaa.
    >
    > Huomaa, että sähköpostitulostinlaajennuksen oletusasetuksena on **A4**-paperikoko, joka ei ole oikea koko esimerkiksi Pohjois-Amerikassa.

### <a name="privacy-notice"></a>Tietosuojatiedot

Jos käytät sähköpostitulostinlaajennusta, kaikki tai jotkin tulostustyöt lähetetään tulostimelle määritettyyn sähköpostiosoitteeseen. Yksilöllinen sähköpostitunnus kannattaa yhdistää tulostinlaitteeseen käyttämällä vain virallisia laitevalmistajan tarjoamia palveluita. Valmistaja voi olla esimerkiksi HP ePrint, KonicaMinolta EveryonePrint tai Epson Email Print.

Noudata varovaisuutta tietoturva-asioissa. Varmista esimerkiksi, että sähköpostitulostusratkaisun käyttöoikeudet, tietosuoja-asetukset ja tietojen säilyttämistä koskevat käytännöt on määritetty oikein. Vastuullasi on antaa oikea, varmistettu ja toimiva sähköpostiosoite. Lisätietoja on kohdassa [Microsoftin tietosuojatiedot](https://privacy.microsoft.com/privacystatement).


## <a name="set-up-default-printers"></a><a name="default"></a>Oletustulostimien määrittäminen

Tulostustöissä oletusarvoisesti käytettävät tulostimet voidaan määrittää muutamalla eri tavalla. Oletustulostin on kätevä, jos käytössä on raportteja, joissa on käytettävä eri tulostinta sen vuoksi, miten ne on sijoitettu yrityksessä tai mitä tulostusominaisuuksia niissä on.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Tulostimen määrittäminen kaikkien tulostustöiden oletustulostimeksi

Tulostimen voi määrittää kaikkien tulostustöiden oletustulostimeksi **Tulostimen hallinta** -sivulla. Tulostimen voi määrittää oletustulostimeksi joko itselle tai kaikille käyttäjille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostimien hallinta** ja valitse sitten vastaava linkki.

    > [!TIP]
    > **Tulostimen hallinta** -sivun voi avata myös valitsemalla **Tulostimen hallinta** **Tulostimen valinnat** -sivulla.  
2. Valitse tulostin luettelossa **Tulostimen hallinta**-sivulla. Valitse sitten **Hallinta** ja lopuksi **Määritä oletustulostimeksi** tai **Määritä kaikkien käyttäjien oletustulostimeksi**.

> [!NOTE]
> Kun oletustulostin määritetään **Tulostimen hallinta** -sivulla, **Tulostimen valinnat** -sivulle lisätään merkintä.

### <a name="set-a-default-printer-for-specific-reports"></a>Oletustulostimen määrittäminen tietyille raporteille

**Tulostimen valinnat** -sivulla voidaan määrittää tulostin, jota raportti oletusarvoisesti käyttää. Oletustulostimet määritetään käyttäjätilin perusteella. Oletustulostin voidaan määrittää vain itselle, toiselle käyttäjälle tai kaikille käyttäjille.

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)]in paikallisessa versiossa **Tulostimen valinnat** -sivua voidaan käyttää vain tulostinlaajennusten, kuten sähköpostitulostuksen tai yleistulostuksen tulostimien, määrittämissä pilvitulostimissa. Sitä ei voi käyttää paikallisissa tulostimissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tulostimien valinta** ja valitse sitten vastaava linkki. Sen sijaan voit valita **Tulostimen hallinta** -sivulla tulostimen ja valita sitten **Tulostimen valinnat**-toiminnon.
2. Valitse **Uusi**-toiminto, jos haluat lisätä tulostinvalinnan tiettyä raporttia varten.
3. Täytä tarvittavat kentät.

Määritetty raportti on nyt määritetty tulostamaan halutulle tulostimelle oletusarvoisesti.

> [!NOTE]
> Kun kyseinen raportti tulostetaan, voit valita toisen tulostimen käyttämällä pyyntösivun **Tulosta**-kenttää.

> [!NOTE]
> Jos et määritä raporttia tietylle tulostimelle **Tulostinvalinnat**-sivulla, se tulostetaan yrityksen oletustulostimeen **Tulostimen hallinta** -sivun määritysten mukaisesti.

Sinä tai järjestelmänvalvoja voitte käyttää myös **Tulostinvalinnat**-sivua käyttäjien ja raporttien muiden tulostusvaihtoehtojen määrittämisessä. Seuraava taulukko sisältää niiden arvojen yhdistelmät, joiden avulla määritetään raportin eri tulostusasetukset.

|Tehtävä                                                 |Määritä seuraavat arvot                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Tulosta raportti tiettyyn tulostimeen kaikille käyttäjille |Määritä arvot **Raportin tunnus**- ja **Tulostimen nimi** -kenttiin ja jätä **Käyttäjän tunnus** -kenttä tyhjäksi.|
|Tulosta kaikki raportit tiettyyn tulostimeen tietylle käyttäjälle|Määritä arvot **Käyttäjän tunnus**- ja **Tulostimen nimi** -kenttiin ja jätä **Raportin tunnus** -kenttä tyhjäksi. Tämä merkintä toimii samoin kuin **Määritä oletustulostimeksi** -toiminto **Tulostuksen hallinta** -sivulla.|
|Kaikki raporttien oletustulostimen määrittäminen kaikille käyttäjille|Määritä arvo **Tulostimen nimi** -kenttään ja jätä **Käyttäjän tunnus**- ja **Raportin tunnus** -kentät tyhjiksi. Tämä merkintä toimii samoin kuin **Määritä oletustulostimeksi kaikille käyttäjille** -toiminto **Tulostuksen hallinta** -sivulla.|
|Tulosta tietty raportti käyttäjän oletustulostimeen|Määritä arvo **Raportin tunnus** -kenttään ja jätä **Tulostimen nimi**- ja **Käyttäjän tunnus** -kentät tyhjiksi.|
|Tulosta tietty raportti tiettyyn tulostimeen tietylle käyttäjälle|Määritä arvot kaikkiin kolmeen kenttään.|

> [!NOTE]
> Yksityiskohtaiset tulostinvalinnat ohittavat yleisemmät tulostinvalinnat. Esimerkiksi tulostinvalinta, jossa on arvot **Käyttäjän tunnus**-, **Raportin tunnus**- ja **Tulostimen nimi** -kentissä, ohittaa tulostinvalinnan, jossa **Käyttäjän tunnus**- tai **Raportin tunnus** -kentät ovat tyhjät.

### <a name="choosing-the-printer-when-running-a-report"></a>Tulostimen valitseminen raporttia suoritettaessa

Sen sijaan, että käytät oletustulostinta raporttia suoritettaessa, voit ohittaa tämän asetuksen pyyntösivulla. Valitse vain avattavasta **Tulostin**-valikosta, mitä tulostinta haluat käyttää tässä raportin ilmentymässä.

### <a name="sizing-print-jobs"></a>Tulostustöiden mitoitus

Pilvitulostus on suunniteltu kohtuullisen kokoisia asiakirjoja varten. Useimmissa pilvipalveluissa, kuten PrintNode- ja HP ePrint -palveluissa, on enintään 10 megatavua työtä kohti. Jos haluat tulostaa suurempia raportteja, ne täytyy ehkä jakaa useisiin tulosteisiin.

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/change-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

[Raportin tulostaminen](ui-work-report.md#PrintReport)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eräajojen ajaminen](ui-how-run-batch-jobs.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
