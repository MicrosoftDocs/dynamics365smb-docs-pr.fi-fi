---
title: OneDriven ja Business Centralin integroinnin hallinta
description: Tutustu asioihin, joita voit tehdä Business Centralin ja OneDrive for Businessin välisen integroinnin hallintaan.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 05/12/2021
ms.author: bholtorf
ms.openlocfilehash: cceb05c1ad19a95494c188cd2482b45962535c94
ms.sourcegitcommit: 99c705d160451c05b226350ff94b52fb0c3ae7a0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606408"
---
# <a name="managing-onedrive-integration-with-business-central"></a>OneDriven ja Business Centralin integroinnin hallinta 
Tässä artikkelissa on yleiskuvaus siitä, mitä voit tehdä järjestelmänvalvojana, kun haluat hallita OneDrive for Businessin ja [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman integrointia. [!INCLUDE[prod_short](includes/prod_short.md)] online -asiakkaat hyötyvät automaattisesta integroinnista, eikä näiden toimintojen käyttöön tarvitse määrittää lisäasetuksia. 

## <a name="minimum-requirements"></a>Vähimmäisvaatimukset

* Jokaisella käyttäjällä on oltava [!INCLUDE[prod_short](includes/prod_short.md)]in ja OneDriven käyttöoikeus osana Microsoft 365 -palvelupakettia.
* OneDrive on määritettävä kullekin käyttäjälle.

## <a name="governance"></a>Hallinto
SharePoint-hallintakeskus tarjoaa laajat hallintamahdollisuudet käytännöille, jotka ohjaavat OneDriven käyttöä koko organisaatiossa. Yleiset järjestelmänvalvojat tai käyttäjät, joilla on SharePoint-järjestelmänvalvojan rooli, voivat määrittää käytäntöjä, jotka määrittävät, ketkä voivat käyttää OneDrivea, missä tiedot ovat, sisällön elinkaaren ja paljon muuta. Seuraavissa linkeissä on tietoja usein käytetyistä ominaisuuksista ja asetuksista, jotka voivat tehostaa integrointia [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa. 

* [Jakamisasetusten hallinta](/sharepoint/turn-external-sharing-on-or-off)
* [Tietoesteiden käyttäminen SharePointin kanssa](/sharepoint/information-barriers)
* [Lisätietoja tietojen menetyksen estämisestä](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Oletustallennustilan määrittäminen OneDrive-käyttäjille](/onedrive/set-default-storage-space)
* [Lisää ja poista järjestelmänvalvojia käyttäjän OneDrivessa](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Poista OneDrive-luominen käytöstä joillekin käyttäjille](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [OneDriven ja SharePoint Onlinen monialueominaisuudet](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Jotkin ominaisuudet voivat olla käytettävissä vain tietyissä suunnitelmissa.

## <a name="managing-privacy"></a>Yksityisyyden hallinta
Järjestelmänvalvojat ja käyttäjät voivat hallita OneDriveen tallennettuja sisältöjä, ja nämä tiedot omistaa vain oma organisaatiosi. Lisätietoja on ohjeaiheessa [Miten SharePoint ja OneDrive turvaavat tietosi pilvipalvelussa](/sharepoint/safeguarding-your-data). Voit myös käydä [Microsoftin tietosuojatiedoissa](https://privacy.microsoft.com/en-us/privacystatement), jossa selitetään Microsoftin käsittelemät tiedot, miten Microsoft käsittelee niitä ja mihin käyttötarkoituksiin.

## <a name="restoring-onedrive-and-prod_short"></a>OneDriven ja [!INCLUDE[prod_short](includes/prod_short.md)]in palauttaminen
Osana katastrofitilanteen palauttamisen harjoitusta järjestelmänvalvojat voivat joutua palauttamaan [!INCLUDE[prod_short](includes/prod_short.md)] -ympäristö aiempaan varmuuskopioon ja synkronoimaan OneDrive-tallennustila samaan ajankohtaan. OneDrive-ohjelmassa on erilaisia työkaluja tähän, kuten käyttäjän OneDriven palauttaminen aiempaan hetkeen, yksittäisen tiedoston aiemman version palauttaminen tai poistettujen tiedostojen palauttaminen. Lisätietoja on seuraavissa artikkeleissa:

* Lisätietoja [!INCLUDE[prod_short](includes/prod_short.md)]ille on kohdassa [Ympäristön palauttaminen hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Lisätietoja OneDrivelle on kohdassa [OneDriven palauttaminen](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="configuring-business-central-on-premises"></a>Business Central on-premises -version määrittäminen

Järjestelmänvalvojan täytyy määrittää yhteys [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -asennuksen ja OneDriven välillä. Toisin kuin [!INCLUDE[prod_short](includes/prod_short.md)] onlinessa, yhteys ei ole automaattinen. Jos yhteyttä ei ole määritetty, käyttäjät eivät voi käyttää OneDriven ominaisuuksia. 

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises voidaan yhdistää vain OneDriveen, jota isännöi Microsoft pilvipalvelussa. Yhteyden muodostamista [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -asennuksesta SharePoint-palvelimen Omat sivustot -säilöön ei tueta.

> [!IMPORTANT]
> Määrittämällä tämän ominaisuuden voit ottaa käyttöön myös vanhat ominaisuudet, jotka lähettävät tiedostoja OneDriveen.  
>
>* Avaa Excelissä -toiminto kopioi Excel-tiedoston automaattisesti OneDriveen ja avaa sen sitten Excel Onlinessa. 
>* Jos viet raportin tiedostoon, ohjelma kopioi tiedoston automaattisesti OneDriveen ja avaa sen sitten Excel Onlinessa, Word Onlinessa tai OneDrivessa. 
>* Myös muut toiminnot voivat avautua automaattisesti OneDrivessa.

### <a name="to-prepare-prod_short-on-premises-for-connecting-to-onedrive"></a>[!INCLUDE[prod_short](includes/prod_short.md)] on-premises -version OneDrive-yhteyden valmistelu

<!-- 
1. For the best experience Configure Azure Active Directory (AD) authentication.

   For more information, see [Authenticating Business Central Users with Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory)-->

Lisää rekisteröity sovellus Business Centralille Microsoft 365 -suunnitelman Azure AD -vuokraajassa. Muiden Business Centralissa käytettävien Azure-palvelujen tavoin OneDrive edellyttää, että sovellus rekisteröidään Azure Active Directoryssa (Azure AD). Sovelluksen rekisteröinti tuottaa Business Centralin ja SharePointin välisiä todennus- ja valtuutuspalveluita, jota OneDrive käyttää.

Määritä rekisteröidylle sovellukselle seuraavat delegoidut käyttöoikeudet SharePoint API -liittymään:

- AllSites.Write
- MyFiles.Write
- User.Read.All 

Tämä tehdään Azure-portaalissa. Kopioi rekisteröidyn sovelluksen käyttämä sovelluksen (asiakkaan) tunnus ja asiakkaan salaisuus. Tarvitset näitä tietoja seuraavassa tehtävässä.

Lisätietoja sovelluksen rekisteröimisestä ja käyttöoikeuksien määrittämisestä on kehittäjän ja IT-ammattilaisen ohjeen kohdassa [Sovelluksen rekisteröiminen Azure Active Directoryssa](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

> [!TIP]
> Jos olet jo rekisteröinyt sovelluksen osana jonkin muun Microsoft-tuotteen (kuten Power BI) integrointia, voit käyttää kyseistä sovelluksen rekisteröintiä uudelleen. Tässä tapauksessa sinun täytyy vain määrittää SharePoint-käyttöoikeudet.

### <a name="to-set-up-the-connection-in-prod_short-on-premises"></a>Yhteyden määrittäminen [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -asennuksessa

<!--
> [!NOTE]
> This requires the following types of authentication credentials:
>
> * Windows
> * NavUserPassword
> * Azure Active Directory
-->
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Microsoft SharePoint -yhteyden määritys** ja valitse sitten vastaava linkki.
2. Syötä **Kuvaus**-kenttään yhteyden kuvaus, kuten **OneDrive**.
3. Syötä **Kansio**-kenttään **Business Central**.
4. Kirjoita **Sijainti**-kenttään oman OneDriven URL-osoite.

    OneDriven URL-osoite on yleensä seuraavassa muodossa:`https://<tenant name>-my.sharepoint.com`. Lisätietoja on OneDrive-dokumentaation ohjeaiheessa [Oman organisaation käyttäjien OneDriven URL-osoitteet](/onedrive/list-onedrive-urls).
5. Syötä **asiakastunnus**-kenttään sovelluksen rekisteröinnin asiakastunnus.
6. Syötä **Asiakkaan salaisuus** -kenttään sovelluksen rekisteröinnin salaisuus. 
   <!-- 
   For information about how to find the URLs, see the following:
   * [How to find your SharePoint server URL]
   * [How to find your OneDrive URL]-->

> [!IMPORTANT]
> SharePoint-yhteyden määritys -sivulla määritetään monia vanhoja ominaisuuksia. **Yleiset**-osa määrittää yhteyden OneDriveen, ja **Jaetut asiakirjat** -osa ohjaa tiedostot sen sijaan uudelleen SharePointiin. Tämä vanha SharePoint-ominaisuus vanhenee lähitulevaisuudessa. Microsoft suosittelee, että et määritä **Jaetut asiakirjat** -osiota.

## <a name="see-also"></a>Katso myös
[Business Centralin ja OneDrive for Businessin integrointi](across-onedrive-overview.md)  
[Business Central-tiedostojen avaaminen OneDrivessa](across-share-onedrive.md)  
[OneDrive – usein kysytyt kysymykset](admin-onedrive-faq.md)

