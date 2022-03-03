---
title: OneDrive for Business - usein kysytyt kysymykset
description: Hanki vastauksia joihinkin tyypillisiin kysymyksiin, jotka liittyvät OneDrive for Businessin ja Business Centralin käyttöön.
author: bholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, integration, share, browser
ms.date: 05/19/2021
ms.author: bholtorf
ms.openlocfilehash: f54e8b6290e9dd653180b3ea05246255b84dc2ae
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144048"
---
# <a name="onedrive-for-business-faq"></a>OneDrive for Business - usein kysytyt kysymykset

[!INCLUDE [online_only](includes/online_only.md)]

Tässä artikkelissa vastataan joihinkin kysymyksiin, joita sinulla voi olla, kun käytössä on OneDrive ja [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="does-this-work-with-all-prod_short-clients"></a>Toimiiko tämä kaikkien [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelmien kanssa?

Kyllä. Voit avata tiedostoja OneDrivessa [!INCLUDE[prod_short](includes/prod_short.md)] -mobiilisovelluksista, kun tarkastelet kortin tietoja Microsoft Teamsissa tai myös Outlook-apuohjelmasta.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a>Onko OneDrive sama kuin SharePoint tiedostojen tallentamiseen?

Microsoft 365 -tilauksen osana organisaatiosi tarjoaa sinulle OneDriven, tiedostojen tallennuksen pilvipalveluun. OneDrive on yksityinen oletusarvon mukaan, ja siellä voit järjestellä sisältöä ja valita mitkä tiedostot ja kansiot jaetaan ja kenelle ne jaetaan. SharePoint puolestaan tarjoaa pilvipalvelussa tiedostosäilön, joka jaetaan muiden organisaation käyttäjien kanssa.  

## <a name="does-prod_short-support-consumer-onedrive"></a>Tukeeko [!INCLUDE[prod_short](includes/prod_short.md)] OneDriven kuluttajaversiota?

Ei. Tämä integrointi on tarkoitettu ainoastaan OneDrive for Businessille, ja se tukee vain työtiliäsi. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>Tuetaanko kaikkia OneDrive for Business -suunnitelmia?

[!INCLUDE[prod_short](includes/prod_short.md)] ei tue OneDrive for Businessin erillisiä suunnitelmia. OneDrive on ostettava osana Microsoft 365:n Business- tai Enterprise-suunnitelmaa. Lisätietoja on ohjeaiheessa [OneDrive -pilvivarastoinnin hinnoittelun ja suunnitelmien vertailu](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>Missä voin nähdä OneDrive-palvelun kunnon?

Järjestelmänvalvojat voivat käyttää palvelun kunnon koontinäyttöä osana Microsoft 365 -hallintakeskusta. Koontinäyttö sisältää OneDrive-palvelun käytettävyyden. 
 
## <a name="is-onedrive-integration-available-to-prod_short-on-premises"></a>Onko OneDrive-integrointi saatavilla [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versioon?

Kyllä, mutta toisin kuin [!INCLUDE[prod_short](includes/prod_short.md)] online, se vaatii lisäasetuksia. Lisätietoja on kohdassa [Business Central on-premises -version määritys](admin-onedrive-integration.md#configuring-business-central-on-premises).  

## <a name="does-prod_short-on-premises-connect-with-sharepoint-server"></a>Onko [!INCLUDE[prod_short](includes/prod_short.md)] on-premises yhteydessä SharePoint Serveriin?

Ei. Tätä käyttöönottoyhdistelmää ei tueta, vaikka SharePoint Server olisi sallinut Omat sivustot.  

## <a name="does-prod_short-online-connect-with-sharepoint-server"></a>Onko [!INCLUDE[prod_short](includes/prod_short.md)] online yhteydessä SharePoint Serveriin?

Ei. Tätä käyttöönottoyhdistelmää ei tueta, vaikka SharePoint Server olisi sallinut Omat sivustot.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>Miten tämä toimii organisaatiossa, jossa on useampia ympäristöjä?

Integrointi olettaa, että yritysten nimet ovat yksilöllisiä eri [!INCLUDE[prod_short](includes/prod_short.md)] -ympäristöissä. Kun yrityksen nimet ovat yksilöiviä koko organisaatiossa, tiedoston avaaminen OneDrivessa kopioi tiedoston kansioon, joka on nimetty valitun yrityksen mukaan. Jos yritysten nimet eivät ole yksilöllisiä eri ympäristöissä, tiedostot saatetaan sijoittaa samanlaisten yritysten nimien mukaan samaan kansioon.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>Olemme muuttaneet yrityksen nimeä. Mitä aiemmille tiedostoilleni tapahtuu?

[!INCLUDE[prod_short](includes/prod_short.md)] ei siirrä aiemmin OneDrivessa avattuja tiedostoja uuteen kansioon automaattisesti. Kun olet nimennyt yrityksen uudelleen, Avaa OneDrivessa -toiminto kopioi tiedostot kansioon, jossa on yrityksen uusi nimi.   

## <a name="when-attaching-files-to-prod_short-how-do-i-pick-a-file-from-onedrive"></a>Kun liität tiedostoja [!INCLUDE[prod_short](includes/prod_short.md)]iin, miten valitsen tiedoston OneDrivesta? 
[!INCLUDE[prod_short](includes/prod_short.md)] ei tarjoa pilvitiedostojen valitsinta. Tiedosto on ladattava OneDrivesta laitteeseen ja sitten ladattava [!INCLUDE[prod_short](includes/prod_short.md)]iin. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Haluan avata tiedostoja SharePointissa sen sijaan. Miten tämä tehdään?

[!INCLUDE[prod_short](includes/prod_short.md)] ei tarjoa ominaisuuksia, joiden avulla tiedostoja voidaan kopioida SharePointiin ja avata niitä SharePoint -kirjastosta. Ota yhteyttä Microsoft-kumppaniin, jos haluat tietoja vaihtoehdoista tai hae sovelluksia AppSourcesta.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>Miten OneDrive-integrointi kytketään pois päältä?

[!INCLUDE[prod_short](includes/prod_short.md)] online ei tarjoa tapaa ottaa OneDrive-integrointi käyttöön tai poistaa sitä käytöstä.  

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>Pitäisikö minun käyttää SharePoint-yhteyden määritys -sivua yhteyden muodostamiseen SharePointiin?

Tämä on vanha ominaisuus, jossa kaikkien käyttäjien kaikki [!INCLUDE[prod_short](includes/prod_short.md)]-tiedostot lähetetään yhteen SharePoint-kansioon. Microsoft suosittelee, että et määritä SharePoint-yhteyden määritys -sivulla Jaetut asiakirjat -pikavälilehteä, koska pyrimme poistamaan tämän ominaisuuden käytöstä.  

## <a name="which-version-of-prod_short-supports-onedrive"></a>Mikä [!INCLUDE[prod_short](includes/prod_short.md)]-versio tukee OneDrivea?

Integrointi OneDriven kanssa tuli saataville vuoden 2021 2. julkaisuaallossa.  

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>Jatkaako Microsoft OneDrive-integraation parantamista?

Microsoft saa jatkuvasti palautetta monipuoliselta käyttäjäyhteisöltä ja ottaa parhaat ehdotukset huomioon. Saat lisätietoja integraatioiden uusista ominaisuuksista Microsoft 365 -sovelluksille [Dynamics 365:n julkaisusuunnitelmasta](/dynamics365-release-plan/2021wave1).  

Jos haluat osallistua OneDrive-integraation parantamiseen, tai sinulla on idea, joka parantaisi tiedostojen jakamista ja yhteiskäyttöä [!INCLUDE[prod_short](includes/prod_short.md)]issa, lisää idea tai äänestä olemassa olevia ideoita osoitteessa [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="troubleshooting"></a>Vianetsintä

Tässä osassa on tietoja OneDriven [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa käytössä mahdollisesti olevien ongelmien tunnistamisesta ja korjaamisesta.  

### <a name="i-have-to-sign-in-each-time-i-open-a-file"></a>Minun täytyy kirjautua sisään joka kerta kun avaan tiedoston

Pahoittelut. Tämä on tunnettu ongelma, ja työskentelemme sen ratkaisemiseksi. Odotamme tarjoavamme sujuvamman kokemuksen tulevassa päivityksessä.  

### <a name="business-central-cant-find-my-onedrive"></a>Business Central ei löydä OneDrivea

Kun tämä näyttöön tulee sanoma "Ei voitu määrittää OneDrive for Businessin sijaintia, ota yhteyttä kumppaniisi", tarkista, onko käyttäjä käyttänyt  OneDrivea vähintään kerran. Jos näin ei ole, pyydä henkilöä menemään osoitteeseen portal.office.com/onedrive. Tämä voi kestää jonkin aikaa. Jos viesti näkyy yhä 24 tunnin kuluttua, ota yhteyttä tukeen.  
 

## <a name="see-also"></a>Katso myös
[Business Centralin ja OneDriven integraatio](across-onedrive-overview.md)  
[OneDriven ja Business Centralin integroinnin hallinta](admin-onedrive-integration.md)  
[Business Central-tiedostojen avaaminen OneDrivessa](across-share-onedrive.md)  
