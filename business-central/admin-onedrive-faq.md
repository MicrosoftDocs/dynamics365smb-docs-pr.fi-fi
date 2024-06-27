---
title: OneDrive for Business - usein kysytyt kysymykset
description: 'Hanki vastauksia joihinkin tyypillisiin kysymyksiin, jotka liittyvät OneDriveen työssä tai koulussa (tunnettiin aiemmin OneDrive for Businessina) ja Business Centralin käyttöön.'
author: brentholtorf
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'OneDrive, integration, share, browser'
ms.date: 06/13/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="onedrive-for-business-faq"></a>OneDrive for Business - usein kysytyt kysymykset

[!INCLUDE [online_only](includes/online_only.md)]

Tässä artikkelissa vastataan joihinkin kysymyksiin, joita sinulla voi olla, kun käytössä on OneDrive ja [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="does-this-work-with-all--clients"></a>Toimiiko tämä kaikkien [!INCLUDE[prod_short](includes/prod_short.md)] -asiakasohjelmien kanssa?

Kyllä. Voit avata tiedostoja OneDrivessa [!INCLUDE[prod_short](includes/prod_short.md)] -mobiilisovelluksista, kun tarkastelet kortin tietoja Microsoft Teamsissa tai myös Outlook-apuohjelmasta.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a>Onko OneDrive sama kuin SharePoint tiedostojen tallentamiseen?

Microsoft 365 -tilauksen osana organisaatiosi tarjoaa sinulle OneDriven, tiedostojen tallennuksen pilvipalveluun. OneDrive on yksityinen oletusarvon mukaan, ja siellä voit järjestellä sisältöä ja valita mitkä tiedostot ja kansiot jaetaan ja kenelle ne jaetaan. SharePoint puolestaan tarjoaa pilvipalvelussa tiedostosäilön, joka jaetaan muiden organisaation käyttäjien kanssa.  

## <a name="does--support-consumer-onedrive"></a>Tukeeko [!INCLUDE[prod_short](includes/prod_short.md)] OneDriven kuluttajaversiota?

Ei. Tämä integrointi on tarkoitettu ainoastaan OneDrive for Businessille, ja se tukee vain työtiliäsi. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>Tuetaanko kaikkia OneDrive for Business -suunnitelmia?

[!INCLUDE[prod_short](includes/prod_short.md)] ei tue OneDrive for Businessin erillisiä suunnitelmia. OneDrive on ostettava osana Microsoft 365:n Business- tai Enterprise-suunnitelmaa. Lisätietoja on ohjeaiheessa [OneDrive -pilvivarastoinnin hinnoittelun ja suunnitelmien vertailu](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>Missä voin nähdä OneDrive-palvelun kunnon?

Järjestelmänvalvojat voivat käyttää palvelun kunnon koontinäyttöä osana Microsoft 365 -hallintakeskusta. Koontinäyttö sisältää OneDrive-palvelun käytettävyyden. Siirry kohteeseen [https://admin.microsoft.com/Adminportal/Home?#/servicehealth](https://admin.microsoft.com/Adminportal/Home?#/servicehealth).

## <a name="is-onedrive-integration-available-to--on-premises"></a>Onko OneDrive-integrointi saatavilla [!INCLUDE[prod_short](includes/prod_short.md)] on-premises -versioon?

Kyllä, mutta toisin kuin [!INCLUDE[prod_short](includes/prod_short.md)] online, se vaatii lisäasetuksia. Lisätietoja on kohdassa [Business Central on-premises -version määritys](admin-onedrive-integration-onpremises.md).  

## <a name="does--on-premises-connect-with-sharepoint-server"></a>Onko [!INCLUDE[prod_short](includes/prod_short.md)] on-premises yhteydessä SharePoint Serveriin?

Nro Tätä käyttöönottoyhdistelmää ei tueta, vaikka SharePoint Server olisi sallinut Omat sivustot.  

## <a name="does--online-connect-with-sharepoint-server"></a>Onko [!INCLUDE[prod_short](includes/prod_short.md)] online yhteydessä SharePoint Serveriin?

Nro Tätä käyttöönottoyhdistelmää ei tueta, vaikka SharePoint Server olisi sallinut Omat sivustot.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>Miten tämä toimii organisaatiossa, jossa on useampia ympäristöjä?

Integrointi olettaa, että yritysten nimet ovat yksilöllisiä eri [!INCLUDE[prod_short](includes/prod_short.md)] -ympäristöissä. Kun yrityksen nimet ovat yksilöiviä koko organisaatiossa, tiedoston avaaminen OneDrivessa kopioi tiedoston kansioon, joka on nimetty valitun yrityksen mukaan. Jos yritysten nimet eivät ole yksilöllisiä eri ympäristöissä, tiedostot saatetaan sijoittaa samanlaisten yritysten nimien mukaan samaan kansioon.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>Olemme muuttaneet yrityksen nimeä. Mitä aiemmille tiedostoilleni tapahtuu?

[!INCLUDE[prod_short](includes/prod_short.md)] ei siirrä aiemmin OneDrivessa avattuja tiedostoja uuteen kansioon automaattisesti. Kun olet nimennyt yrityksen uudelleen, Avaa OneDrivessa -toiminto kopioi tiedostot kansioon, jossa on yrityksen uusi nimi.   

## <a name="when-attaching-files-to--how-do-i-pick-a-file-from-onedrive"></a>Kun liität tiedostoja [!INCLUDE[prod_short](includes/prod_short.md)]iin, miten valitsen tiedoston OneDrivesta?

[!INCLUDE[prod_short](includes/prod_short.md)] ei tarjoa pilvitiedostojen valitsinta. Tiedosto on ladattava OneDrivesta laitteeseen ja sitten ladattava [!INCLUDE[prod_short](includes/prod_short.md)]iin. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Haluan avata tiedostoja SharePointissa sen sijaan. Miten tämä tehdään?

[!INCLUDE[prod_short](includes/prod_short.md)] ei tarjoa ominaisuuksia, joiden avulla tiedostoja voidaan kopioida SharePointiin ja avata niitä SharePoint -kirjastosta. Ota yhteyttä Microsoft-kumppaniin, jos haluat tietoja vaihtoehdoista tai hae sovelluksia AppSourcesta.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>Miten OneDrive-integrointi kytketään pois päältä?

Suorita **OneDrive-määrityksen** asetusten ohjattu määritysopas ja poista **OneDrive-sovelluksen ominaisuuksien käyttö** käytöstä ja **Käytä OneDrivea järjestelmätoimintoihin** -valitsimia. 

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>Pitäisikö minun käyttää SharePoint-yhteyden määritys -sivua yhteyden muodostamiseen SharePointiin?

Tämä on vanha ominaisuus, jossa kaikkien käyttäjien kaikki [!INCLUDE[prod_short](includes/prod_short.md)]-tiedostot lähetetään yhteen SharePoint-kansioon. Suosittelemme, että et määritä jaetut asiakirjat -pikavälilehteä **SharePoint-yhteyden asetus** -sivulla, koska tämä sivu on [vanhentunut](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup) ja poistetaan vuoden 2023 julkaisuaalto 2:ssa, versiossa 23.0.  Sen sijaan kannattaa käyttää **OneDrive-määritystä**.  

## <a name="which-version-of--supports-onedrive"></a>Mikä [!INCLUDE[prod_short](includes/prod_short.md)]-versio tukee OneDrivea?

Integrointi OneDriven kanssa tuli saataville vuoden 2021 2. julkaisuaallossa.  

## <a name="which-features-are-affected-by-onedrive-integration"></a><a name="features"></a>Mihin ominaisuuksiin OneDrive-integrointi vaikuttaa?

OneDrive-integraation määrittämisen **OneDrive-määrityksen**-asetusten ohjatussa määrityksessä voit ottaa käyttöön tai poistaa käytöstä ominaisuuksia Business Central -tiedostojen käsittelyä varten OneDrivessa. Ominaisuudet on jaettu kahden vaihtoehdon välillä:

|Asetus|Kuvaus|
|------|----------|
|**Käytä sovellusominaisuuksille**|Jos otat tämän asetuksen käyttöön, **Avaa OneDrivessä**- ja **Jaa**-toiminnot ovat käytettävissä Business Centralin tiedostoissa, kuten asiakirjoihin liitetyissä tiedostoissa tai Saapuneet raportit -kansiossa. Näiden toimintojen avulla käyttäjät voivat kopioida, avata ja jakaa tiedostoja OneDrivessa. Lisätietoja on kohdassa [Business Centralin tiedostojen avaaminen ja jakaminen OneDrivessa](across-share-onedrive.md).
|**Käytä järjestelmäominaisuuksin avulla**|Tämän vaihtoehdon ottaminen käyttöön aktivoi seuraavat ominaisuudet:<ul><li> **Avaa Excelissä** ja **Muokkaa Excelissä** -toiminnot luettelosivuilla kopioivat Excel-tiedoston automaattisesti OneDriveen ja avaavat sen sitten Excel Onlinessa. Lisätietoja on kohdassa [Katsele ja muokkaa Excelissä](across-work-with-excel.md).</li><li> Raportin lähettäminen Exceliin tai Wordiin kopioi tiedoston automaattisesti OneDriveen ja avaa sen sitten Excel- tai Word Onlinessa. Lisätietoja on kohdassa [Raportin tallentaminen tiedostoon](ui-work-report.md#save-a-report-to-a-file).|

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>Jatkaako Microsoft OneDrive-integraation parantamista?

Microsoft saa jatkuvasti palautetta monipuoliselta käyttäjäyhteisöltä ja ottaa parhaat ehdotukset huomioon. Saat lisätietoja integraatioiden uusista ominaisuuksista Microsoft 365 -sovelluksille [Dynamics 365:n julkaisusuunnitelmasta](/dynamics365-release-plan/2021wave1).  

Jos haluat osallistua OneDrive-integraation parantamiseen, tai sinulla on idea, joka parantaisi tiedostojen jakamista ja yhteiskäyttöä [!INCLUDE[prod_short](includes/prod_short.md)]issa, lisää idea tai äänestä olemassa olevia ideoita osoitteessa [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="troubleshooting"></a>Vianetsintä

Tässä osassa on tietoja OneDriven [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa käytössä mahdollisesti olevien ongelmien tunnistamisesta ja korjaamisesta.  

### <a name="business-central-cant-find-my-onedrive"></a>Business Central ei löydä OneDrivea

Kun tämä näyttöön tulee sanoma "Ei voitu määrittää OneDrive for Businessin sijaintia, ota yhteyttä kumppaniisi", tarkista, onko käyttäjä käyttänyt  OneDrivea vähintään kerran. Jos näin ei ole, pyydä henkilöä menemään osoitteeseen portal.office.com/onedrive. Tämä voi kestää jonkin aikaa. Jos viesti näkyy yhä 24 tunnin kuluttua, ota yhteyttä tukeen.  
 
### <a name="im-having-problems-sharing-from-outlook"></a>Outlookin jakamisessa on ongelmia

Lue lisätietoja kohdasta [Tiedostojen jakaminen OneDriveen Outlook.comista ei onnistu](https://support.microsoft.com/en-us/office/can-t-share-onedrive-files-from-outlook-com-05d4cb21-40a2-40e3-b111-82cddb82d22f) Microsoftin tuesta.

### <a name="actions-open-in-onedrive-and-share-are-missing"></a>Avaa OneDrivessa- ja Jaa-toiminnot puuttuvat

On pari asiaa, jotka voit tarkistaa:

- Tarkista, että sovelluksen ominaisuudet OneDrivessa ovat käytössä **OneDrive-määrityksen** asetusten ohjattu määritys -oppaassa. Lisätietoja on kohdassa [OneDriven määritys käyttämällä OneDrive-asetuksia](admin-onedrive-integration.md#configure-onedrive-using-onedrive-setup).
- Tarkista, että Microsoft OneDriven tilaksi on määritetty **Hyväksyn** **tietosuojailmoitusten tila** -sivulla. Katso [Tietosuojatietojen tila](privacy-notices-status.md).

## <a name="see-also"></a>Katso myös

[Business Centralin ja OneDriven integraatio](across-onedrive-overview.md)  
[OneDriven ja Business Centralin integroinnin hallinta](admin-onedrive-integration.md)  
[Business Central-tiedostojen avaaminen OneDrivessa](across-share-onedrive.md)  
