---
title: OneDriven ja Business Centralin integroinnin hallinta
description: 'Tutustu asioihin, joita voit tehdä Business Centralin ja OneDrive for Businessin välisen integroinnin hallintaan.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 06/13/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="managing-onedrive-integration-with-business-central"></a>OneDriven ja Business Centralin integroinnin hallinta

Tässä artikkelissa on yleiskuvaus siitä, mitä voit tehdä järjestelmänvalvojana, kun haluat hallita OneDrive for Businessin ja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman integrointia. [!INCLUDE[prod_short](includes/prod_short.md)] online -asiakkaat hyötyvät automaattisesta integroinnista, eikä OneDriven avaamisen ja jakamisen käyttäminen ei vaadi ylimääräisiä asetuksia. **OneDrive määritys** avustetun määritysoppaan avulla käyttäjät voivat käyttää entistä useampia OneDrive-toimintoja, kuten avata Excel-tiedoston OneDrivessä&mdash;tai jopa poistaa kaikki ominaisuudet käytöstä.  

## <a name="configure-onedrive-for-integration-with-business-central"></a>Määritä OneDrive:n ja Business Centralin integrointi

Tässä osassa käsitellään tarpeita, joiden on täytyttävä OneDrivessa, jotta yritys voi määrittää integroinnin Business Centralin ja haluamasi tehtävän kanssa.

### <a name="minimum-requirements"></a>Vähimmäisvaatimukset

* Jokaisella käyttäjällä on oltava [!INCLUDE[prod_short](includes/prod_short.md)]in ja OneDriven käyttöoikeus osana Microsoft 365 -palvelupakettia.
* OneDrive on määritettävä kullekin käyttäjälle.

### <a name="managing-privacy"></a>Yksityisyyden hallinta

> [!IMPORTANT]
> Jos olet valinnut Business Centralin ja OneDriven eri maiden tai alueiden käyttöönoton, Business Centralin luomat ja OneDriveen asetetut tiedostot saattavat olla asuinpaikkarajojen ulkopuolella. Varmista, että vahvistat organisaation käytännöt ja tietojen noudattamista koskevat viranomaisvaatimukset ennen yhteyden muodostamista OneDriveen.

Järjestelmänvalvojat ja käyttäjät voivat hallita OneDriveen tallennettuja sisältöjä, ja nämä tiedot omistaa vain oma organisaatiosi. Lisätietoja on ohjeaiheessa [Miten SharePoint ja OneDrive turvaavat tietosi pilvipalvelussa](/sharepoint/safeguarding-your-data). Voit myös käydä [Microsoftin tietosuojatiedoissa](https://privacy.microsoft.com/en-us/privacystatement), jossa selitetään Microsoftin käsittelemät tiedot, miten Microsoft käsittelee niitä ja mihin käyttötarkoituksiin.

Ottamalla tämän palveluyhteyden käyttöön hyväksyt, että

(a) tietoja voidaan jakaa tästä Dynamics 365 Business Central -tuotteesta palveluntarjoajalle, joka käyttää tietoja tuotteen käyttöehtojen ja tietosuojakäytännön mukaisesti, (b) palveluntarjoajan yhteensopivuustasot voivat olla eri kuin Dynamics 365 Business Central -tuotteessa ja että (c) Microsoft voi jakaa yhteystietosi tälle palveluntarjoajalle tarvittaessa, jotta se voi käyttää palvelua ja ratkaista palveluun liittyviä ongelmia.

## <a name="configure-business-central"></a>Määritä Business Central

Business Central online -yhteydessä Business Centralin ja OneDriven välinen yhteys on määritetty automaattisesti, ja OneDrive-ominaisuudet ovat helposti käyttäjien saatavilla oletusarvoisesti. Jos haluat poistaa käytöstä jotkin tai kaikki ominaisuudet, voit käyttää Business Central -asiakassovelluksen **OneDrive-määrityksen** asetusten ohjattua määritysopasta.

Paikallisen Business Centralin määrittäminen on erilainen, sillä Business Centralin ja OneDriven välistä yhteyttä ei ole määritetty sinulle. Sinun tulee tehdä se manuaalisesti. Lisätietoja on kohdassa [OneDrive-integraation ja paikallisen Business Central -version välinen määritys](admin-onedrive-integration-onpremises.md).

### <a name="about-multiple-environments"></a>Tietoja useista ympäristöistä

OneDrive-integrointi on määritetty ympäristöä kohden eli asetuksia käytetään kaikissa kyseisen ympäristön yrityksissä. Jos organisaatiossasi on enemmän kuin yksi ympäristö, sinun on määritettävä kunkin OneDrive-integrointi.

### <a name="prerequisites"></a>Vaatimukset

- Vähintään epäsuora-, Muokkaa- ja Poista (IMD)-käyttöoikeus taulukossa **Asiakirja huoltoskenaariolle**

### <a name="configure-onedrive-using-onedrive-setup"></a>OneDriven määritys käyttämällä OneDrive-asetuksia

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **OneDrive -määritys** ja valitse sitten vastaava linkki. 
2. Kun suoritat asetusten ohjatun määrityksen ensimmäisen kerran, näet **Oma tietosuoja**. Lue sivun tiedot, ja jos hyväksyt käyttöehdot, jatka valitsemalla **Hyväksy**.
3. **Määritä OneDrive-tiedoston käsittely** -sivulla voit valita seuraavista vaihtoehdoista:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Valitse **Seuraava**>**Valmis**.

### <a name="switching-to-new-onedrive-integration-after-upgrade"></a>Siirtyminen uuteen OneDrive-integrointiin päivityksen jälkeen

**OneDrive-määrityksen** asetusten ohjattu määritys otettiin käyttöön vuoden 2022 julkaisuaallossa 2, versiossa 21.0. Aiemmin OneDrive-integrointi käytti **SharePoint-yhteyden asetuksia**, jotka on vanhentunut ja poistetaan vuoden 2023 julkaisuaalto 2:ssa, versiossa 23.0. Kun olet päivittänyt versioon 21, OneDrive toimii edelleen kuten ennenkin. Suosittelemme kuitenkin, että siirryt uuteen OneDrive-integrointiin. Tämän vaihdon tekeminen nyt helpottaa sitä, kun **SharePoint-yhteyden asetukset** poistetaan lopullisesti. Lisäksi sen avulla voit käyttää **OneDrive-määrityksen** asetusten ohjattu määritysopasta käyttäjien käytettävissä olevien OneDrive-ominaisuuksien hallintaan. **OneDrive-määrityksen** asetusten ohjattu määritys tekee siirtymisen vanhasta SharePoint-määrityksestä helpoksi ja saumattomaksi.

Voit vaihtaa yksinkertaisesti avaamalla ja suorittamalla **OneDrive-määrityksen** asetusten ohjatun määrityksen suoraan tai avaamalla **SharePoint-yhteysmääritys**-sivun ja valitsemalla sivun yläreunassa olevasta ilmoituksesta **Siirry uusiin OneDrive-asetuksiin**. Noudata edellisessä osassa kuvattuja asennusohjeita.

## <a name="restoring-onedrive-and-"></a>OneDriven ja [!INCLUDE[prod_short](includes/prod_short.md)]in palauttaminen

Osana katastrofitilanteen palauttamisen harjoitusta järjestelmänvalvojat voivat joutua palauttamaan [!INCLUDE[prod_short](includes/prod_short.md)] online -ympäristö aiempaan varmuuskopioon ja synkronoimaan OneDrive-tallennustila samaan ajankohtaan. OneDrive-ohjelmassa on erilaisia palautustyökaluja tähän, kuten käyttäjän OneDriven palauttaminen aiempaan hetkeen, yksittäisen tiedoston aiemman version palauttaminen tai poistettujen tiedostojen palauttaminen. Lisätietoja on seuraavissa artikkeleissa:

* Lisätietoja [!INCLUDE[prod_short](includes/prod_short.md)]ille on kohdassa [Ympäristön palauttaminen hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Lisätietoja OneDrivelle on kohdassa [OneDriven palauttaminen](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="governance"></a>Hallinto

SharePoint-hallintakeskus tarjoaa laajat hallintamahdollisuudet käytännöille, jotka ohjaavat OneDriven käyttöä koko organisaatiossa. Käyttäjät, joilla on vähintään järjestelmänvalvojan [SharePoint](/entra/identity/role-based-access-control/permissions-reference#sharepoint-administrator) rooli, voivat määrittää, kuka voi käyttää OneDrive, missä tiedot sijaitsevat, mikä on sisällön elinkaari ja paljon muuta. Seuraavissa linkeissä on tietoja usein käytetyistä ominaisuuksista ja asetuksista, jotka voivat tehostaa integrointia [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa. 

* [Jakamisasetusten hallinta](/sharepoint/turn-external-sharing-on-or-off)
* [Tietoesteiden käyttäminen SharePointin kanssa](/sharepoint/information-barriers)
* [Lisätietoja tietojen menetyksen estämisestä](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Oletustallennustilan määrittäminen OneDrive-käyttäjille](/onedrive/set-default-storage-space)
* [Lisää ja poista järjestelmänvalvojia käyttäjän OneDrivessa](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Poista OneDrive-luominen käytöstä joillekin käyttäjille](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [OneDriven ja SharePoint Onlinen monialueominaisuudet](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Jotkin ominaisuudet voivat olla käytettävissä vain tietyissä suunnitelmissa.

## <a name="see-also"></a>Katso myös

[Business Centralin ja OneDrive for Businessin integrointi](across-onedrive-overview.md)  
[Business Central-tiedostojen avaaminen OneDrivessa](across-share-onedrive.md)  
[OneDrive – usein kysytyt kysymykset](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
