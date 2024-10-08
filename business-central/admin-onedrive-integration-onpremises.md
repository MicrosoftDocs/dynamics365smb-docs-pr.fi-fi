---
title: Määritetään paikallinen Business Central OneDrive -integraatiota varten
description: 'Lue lisää siitä, miten paikallinen Business Central voidaan asentaa integroitavaksi OneDriveen työhön tai kouluun (aiemmin OneDrive for Business).'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 06/13/2024
ms.author: jswymer
ms.service: dynamics-365-op
ms.reviewer: jswymer
---
# <a name="configuring-onedrive-integration-with-business-central-on-premises"></a>Määritetään paikallinen Business Central OneDrive -integraatiota varten

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Tässä artikkelissa kerrotaan siitä, kuinka määrittää OneDrive työhön tai kouluun (aiemmin OneDrive for Business) integraatio paikalliseen Business Centraliin. Toisin kuin [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa, Business Centralin ja OneDriven välinen yhteys ei ole automaattisesti määritetty. Jos yhteyttä ei ole määritetty, käyttäjät eivät voi käyttää OneDriven ominaisuuksia.

OneDrive-integroinnin määrittämiseen tarvitaan kaksi tehtävää.

- Ensimmäiseen tehtävään kuuluu sovelluksen (sovelluksen) rekisteröinti oman Microsoft 365 -suunnitelmasi Microsoft Entra -vuokraajaan. Rekisteröityä sovellusta käytetään todennustarkoituksessa. Tämä tehtävä tehdään tavallisesti Azure-portaalissa ja Business Central -verkko-ohjelmassa.
- Toinen tehtävä sisältää yhteyden muodostamisen OneDrive URL-osoitteeseen ja Business Centralin OneDrive-toimintojen käynnistämisen. Tämä tehtävä on tehty Business Central -asiakasohjelmassa. Se tehdään eri tavalla versiosta 21 kuin versioista 19 ja 20. Versio 21 sisältää uudet **OneDrive-asetukset**, jotka korvaavat **SharePoint-yhteyksien asetukset**.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] on-premises voidaan yhdistää vain OneDriveen, jota isännöi Microsoft pilvipalvelussa. Yhteyden muodostamista [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -asennuksesta SharePoint-palvelimen Omat sivustot -säilöön ei tueta.

## <a name="register-an-app-in-microsoft-entra-id-for-onedrive-integration"></a><a name="registerapp"></a>Sovelluksen rekisteröinti Microsoft Entra ID:ssä OneDrive-integrointia varten

Tässä tehtävässä lisäät rekisteröidyn sovelluksen Business Centralille Microsoft 365 -suunnitelman Microsoft Entra -vuokraajassa. Muiden Business Centralissa käytettävien Azure-palvelujen tavoin OneDrive edellyttää rekisteröityä sovellusta Microsoft Entra ID:ssä. Rekisteröity sovellus tuottaa Business Centralin ja SharePointin välisiä todennus- ja valtuutuspalveluita, jota OneDrive käyttää.

Yksityiskohtaiset ohjeet tämän vaiheen suorittamiseen on [Sovelluksen rekisteröinti Microsoft Entra ID:ssä](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) kehittäjä- ja IT-ammattilaisen tuessa.

Kun rekisteröit sovelluksen, harkitse seuraavia seikkoja:

- Jos olet jo rekisteröinyt sovelluksen osana jonkin muun Microsoft-tuotteen (kuten Power BI) integrointia, voit käyttää kyseistä rekisteröityä sovellusta uudelleen. Tässä tapauksessa sinun täytyy vain määrittää SharePoint-käyttöoikeudet olemassa olevalle rekisteröidylle sovellukselle.

- Varmista, että määrität rekisteröidylle sovellukselle seuraavat delegoidut käyttöoikeudet SharePoint API -liittymään:

    - AllSites.FullControl
    - User.ReadWrite.All
    
    Määritä Business Centralin vuoden 2021 2. julkaisuaallossa (versio 19) sen sijaan nämä oikeudet:
    
    - AllSites.Write
    - MyFiles.Write
    - User.Read.All 

- Jos käytät Business Central -versiota 19 tai 20, kopioi rekisteröidyn sovelluksen käyttämä **Asiakastunnus** ja **Asiakkaan salaisuus**. Tarvitset näitä tietoja seuraavassa tehtävässä.

## <a name="get-your-onedrive-url"></a><a name="url"></a>Hanki OneDrive URL-osoite

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## <a name="set-up-the-onedrive-connection-in-version-21-and-later"></a>OneDrive-yhteyden määrittäminen versiossa 21 ja uudemmissa

Käytä tätä toimintoa, jos käytössäsi on Business Centralin vuoden 2022 julkaisuaalto 2 (versio 21) tai uudempi.

### <a name="prerequisites"></a>Vaatimukset

- Vähintään epäsuora-, Muokkaa- ja Poista (IMD)-käyttöoikeus taulukossa **Asiakirja huoltoskenaariolle**

### <a name="run-onedrive-setup"></a>Suorita OneDrive-määritys

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **OneDrive -määritys** ja valitse sitten vastaava linkki.
2. Kun suoritat asetusten ohjatun määrityksen ensimmäisen kerran, näet **Oma tietosuoja**. Lue sivun tiedot, ja jos hyväksyt käyttöehdot, jatka valitsemalla **Hyväksy**.
3. **Määritä tiedoston käsittely** -sivulla voit valita seuraavista vaihtoehdoista:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. Kirjoita **Määritä Business Central** -sivulla **OneDrive URL-osoite** -kenttään OneDriven URL-osoite.

   [Miten löydän OneDriveni URL-osoitteen?](#url)
5. Valitse **Testiyhteys** ja odota tuloksia.
   - Jos testi onnistuu, valitse **Valmis**, niin olet valmis aloittamaan.
   - Jos testi epäonnistuu, näyttöön tulee ongelman kuvaus. Yleensä ongelma liittyy antamaasi URL-osoitteeseen. Valitse **OK**, kun haluat palata **Määritä Business Central** -sivulle, tarkista URL-osoite ja yritä uudelleen.
   - Jos et ole vielä määrittänyt Microsoft Entra ID:n rekisteröityä sovellusta, **Määritä Microsoft Entra ID** -opas avautuu.
6. Kun se on valmis, tietosuojailmoitus OneDrive-integraatiolle hyväksytään kaikille käyttäjille. Jos haluat muuttaa sitä niin, että käyttäjien on hyväksyttävä tai hylättävä se itse, mene **Tietosuojailmoitusten tila** -sivulle ja valitse **Anna käyttäjän päättää** OneDrive-integraatiossa. Käyttäjiä pyydetään sitten hyväksymään tai hylkäämään tietosuojailmoitus, kun he käyttävät OneDrive-ominaisuuksia ensimmäisen kerran. Lisätietoja on kohdassa [Tietosuojailmoitukset](privacy-notices-status.md).

## <a name="set-up-the-connection-in--version-19-and-20"></a>[!INCLUDE[prod_short](includes/prod_short.md)]-yhteyden määrittäminen versioissa 19 ja 20

Käytä tätä toimintoa, jos käytössäsi on Business Centralin vuoden 2022 julkaisuaalto 1 (versio 20) tai vuoden 2021 julkaisuaalto 2 (versio 19).
> [!IMPORTANT]
> Määrittämällä tämän ominaisuuden voit ottaa käyttöön myös vanhat ominaisuudet, jotka lähettävät tiedostoja OneDriveen.  
>
>* Avaa Excelissä -toiminto kopioi Excel-tiedoston automaattisesti OneDriveen ja avaa sen sitten Excel Onlinessa. 
>* Jos viet raportin tiedostoon, ohjelma kopioi tiedoston automaattisesti OneDriveen ja avaa sen sitten Excel Onlinessa, Word Onlinessa tai OneDrivessa. 
>* Myös muut toiminnot voivat avautua automaattisesti OneDrivessa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Microsoft SharePoint -yhteyden määritys** ja valitse sitten vastaava linkki.
2. Syötä **Kuvaus**-kenttään yhteyden kuvaus, kuten **OneDrive**.
3. Syötä **Kansio**-kenttään **Business Central**.
4. Kirjoita **Sijainti**-kenttään oman OneDriven URL-osoite.

   [Miten löydän OneDriveni URL-osoitteen?](#url)
5. Syötä **asiakastunnus**-kenttään asiakastunnus rekisteröidystä sovelluksesta.
6. Syötä **Asiakkaan salaisuus** -kenttään rekisteröidyn sovelluksen salaisuus. 

> [!IMPORTANT]
> **SharePoint-yhteyden määritys** -sivulla määritetään monia vanhoja ominaisuuksia. **Yleiset**-osa määrittää yhteyden OneDriveen, ja **Jaetut asiakirjat** -osa ohjaa tiedostot sen sijaan uudelleen SharePointiin. **SharePoint-yhteyden asetukset** on syrjäytetty, ja ne poistetaan tulevassa versiossa. Microsoft suosittelee, että et määritä **Jaetut asiakirjat** -osiota. Lisätietoja on kohdassa [Vanhentuneet ominaisuudet perussovelluksessa](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup).

## <a name="after-upgrade-to-version-21"></a>Versioon 21 päivittämisen jälkeen

Kun päivität versioon 21 tai uudempaan, **SharePoint-yhteyden asetukset** -sivulla määritetty aiemmin luotu OneDrive-yhteys toimii edelleen. Koska **SharePoint-yhteyden asetus** -sivu poistetaan versiosta 23, Microsoft suosittelee, että siirryt uuteen OneDrive-integrointiin seuraavassa osassa kuvatulla tavalla. Tämän vaihdon tekeminen nyt helpottaa sitä, kun **SharePoint-yhteyden asetukset** poistetaan lopullisesti. Lisäksi sen avulla voit käyttää **OneDrive-määrityksen** asetusten ohjattu määritysopasta käyttäjien käytettävissä olevien OneDrive-ominaisuuksien hallintaan.

## <a name="switching-from-legacy-sharepoint-to-new-onedrive-integration"></a>Siirtyminen vanhasta SharePointista uuteen OneDrive-integraatioon

Voit siirtyä uuteen OneDrive-integrointiin suorittamalla **OneDrive-määrityksen** asetusten ohjatun määritysoppaan, jonka voit avata suoraan tai vanhalta **SharePoint-yhteyden asetus** -sivulta. **OneDrive-määritys**asetusten ohjattu määritys vie sinut läpi siirtymisen ja antaa tietoa muutoksista, joita tehdään matkan varrella.

Ennen kuin aloitat valitsimen käytön tai sen tekemisen, tutustu seuraavaan osioon ja tutustu prosessiin liittyviin näkökohtiin ja huomioihin. 

### <a name="about-switching-to-the-new-onedrive-integration"></a><a name="onedrivesetupmigration"></a>Tietoja siirtymisestä uuteen OneDrive-integraatioon

OneDrive-integroinnin lisäksi Business Central voi integroida myös muihin palveluihin, kuten Power BIhin ja Universal Print -palveluun. Integrointi näihin muihin palveluihin vaatii myös rekisteröidyn Microsoft Entra -sovelluksen todennusta varten. Näiden muiden palveluiden käyttämä Microsoft Entra -sovellus on määritetty **Määritä Microsoft Entra -tilit** asetusten ohjattuun määritykseen. Kun siirryt vanhan SharePoint-yhteyden asetuksista, uusi **OneDrive-määritys** asetusten ohjattu määritys muuttaa OneDrive-integrointia myös käyttämään **Määritä Microsoft Entra -tilien** -asetusten ohjatun määrityksen&mdash;jotta kaikki integraatiot käyttävät samaa Microsoft Entra -sovellusta.

Tämä muutos vaikuttaa siirryttäessä uuteen OneDrive-integrointiin sen mukaan, onko olemassa jo Microsoft-sovellus, joka on määritetty **Määritä Microsoft Entra -tilit** asetusten ohjatussa määrityksessä. 

> [!IMPORTANT]
> Kun siirryt uuteen OneDrive-määritykseen, et voi enää käyttää **SharePoint-yhteyden asetus** -sivua OneDrive-integroinnin määrittämiseen.

#### <a name="how-the-changes-affect-the-integration"></a>Muutosten vaikutus integrointiin

**OneDrive-määrityksen** -asetusten ohjattu määritys käyttää aina sovellusta, joka on määritetty **Määritä Microsoft Entra -tilit** asetusten ohjatussa määrityksessä, jos sellainen on olemassa. Kun suoritat **OneDrive-määrityksen** asetusten ohjatussa määrityksessä, se vertaa sovellusta, joka on määritetty **Määritä Microsoft Entra -tilisi** nykyisessä sovelluksessa, joka on määritetty **SharePoint-yhteysasetuksissa**.

> [!TIP]
> Microsoft Entra -sovellus tunnistetaan **asiakastunnuksella** **SharePoint-yhteysasetus**-sivulla ja **Määritä Microsoft Entra** -tiliesi asetusten ohjattu määritys.

- Jos **Määritä AMicrosoft Entra -tilit** -kohdassa oleva sovellus on eri kuin **SharePoint-yhteys**-asetuksissa oleva sovellus,OneDrive-integraatio muuttuu käyttämään sovellusta kohdassa **Määritä Microsoft Entra -tilit**.

   Kun **OneDrive-määritykset** tehdään valitsimen ollessa painettuna, saat seuraavanlaista sanomaa: 

  `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` edustaa sovelluksen asiakastunnusta kohdassa **Määritä Microsoft Entra -tilit**, joihin OneDrive-integrointi on siirtynyt. 

  > [!IMPORTANT]
  > Jotta uusi OneDrive-integrointi toimisi sen jälkeen, kun olet tehnyt siirtymisen, sinun on myönnettävä sovelluksen käyttöoikeus SharePoint API:lle Azure-portaalissa. Voit tehdä nämä toimet ennen uusien OneDrive-asetusten tekemistä tai sen jälkeen. Lisätietoja on kohdassa [Sovelluksen rekisteröinti Microsoft Entra ID:ssä OneDrive-integrointia varten](#registerapp).

- Jos **Määritä Microsoft Entra -tilit** -kohdassa oleva sovellus on sama kuin **SharePoint-yhteysasetuksissa** oleva sovellus, OneDrive-integraatio käyttää samaa sovellusta kuin aiemmin, lukuun ottamatta **Määritä Microsoft Entra -tilit** -asetuksissa olevia määrityksiä.

   Kun **OneDrive-määritykset** tehdään valitsimen ollessa painettuna, saat seuraavanlaista sanomaa:

    `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Jos sovellusta ei ole määritetty **Microsoft Entra -tilien määritys** -kohdassa, OneDrive-integraatio käyttää samaa sovellusta kuin ennenkin.

   **OneDrive-määrityksen** asetusten ohjattu määritys kopioi sovelluksen määritykset **Määritä Microsoft Entra -tilisi** -määritykseen, joten sitä käytetään muihin integraatioihin, jotka voidaan määrittää myöhemmin.

   Kun **OneDrive-määritykset** tehdään valitsimen ollessa painettuna, saat seuraavanlaista sanomaa:

   `The Microsoft Entra application used for authentication will be configured for all Business Central integrations`.

### <a name="run-onedrive-setup-to-switch-to-the-new-onedrive-integration"></a>Siirry uuteen OneDrive-integrointiin suorittamalla OneDrive-määritys

1. Avaa joko **OneDrive-määritys**-sivu tai **SharePoint-yhteyden määritys** -sivu.
2. Jos käytät **SharePoint-yhteyden asetus** -sivua, valitse sivun yläosassa olevassa ilmoituksessa **Siirry uuteen OneDrive-määritykseen** -kohtaan.
3. Noudata **OneDrive-asetusten** ohjatun määritysoppaan ohjeita.
4. Kun saat **Määritä tiedoston käsittely** -sivun, valitse jokin seuraavista vaihtoehdoista toimintojen käynnistämistä varten:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. **Määritä Business Central** -sivulla näkyy sama URL-osoite, jota aiemmin luotu OneDrive-integrointi käyttää. URL-osoite voidaan muuttaa tarvittaessa.
6. Valitse **Testaa yhteys** ja noudata ohjeita.

   Jos testi onnistuu, valitse **Valmis**, ja olet valmis aloittamaan. Muussa tapauksessa voit korjata ongelman käyttämällä sivun viestejä.

## <a name="see-also"></a>Katso myös
[Business Centralin ja OneDriven integraatio](across-onedrive-overview.md)  
[Business Central-tiedostojen avaaminen OneDrivessa](across-share-onedrive.md)  
[OneDriven usein kysytyt kysymykset](admin-onedrive-faq.md)

