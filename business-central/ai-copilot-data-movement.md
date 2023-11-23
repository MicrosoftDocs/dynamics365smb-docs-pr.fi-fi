---
title: Copilot-tietojen siirtäminen maantieteellisten alueiden välillä
description: 'Tutustu siihen, miten Dynamics 365 Business Centralin Copilot-toiminnoissa käytetty data liikkuu eri maantieteellisillä alueilla, joilla Azure OpenAI Service ei ole oletusarvoisesti saatavilla.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection: get-started
ms.date: 11/09/2023
ms.custom: bap-template
---

# Copilot-tietojen siirtäminen maantieteellisten alueiden välillä 

Copilot on käytettävissä kaikilla tuetuilla [Business Centralin maantieteellisillä alueilla](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Copilot kuitenkin käyttää Microsoft Azure OpenAI Serviceä, joka on tällä hetkellä käytettävissä Business Centralissa vain joillakin maantieteellisillä alueilla, tällä hetkellä Yhdysvalloissa ja Sveitsissä. Tämä tarkoittaa, että jos ympäristösi sijaitsee muualla, Copilotin ja luovien tekoälyominaisuuksien tiedot on siirrettävä maantieteellisen alueesi ulkopuolelle ja niitä voidaan käsitellä ja tallentaa vaatimustenmukaisuusrajojesi ulkopuolelle. Tiedot sisältävät tekoälyn kehotukset ja liiketoimintatiedot, joita Copilot käyttää tai luo. Siinä tapauksessa sinun täytyy valita, että sallit tiedonsiirron Azure OpenAI Servicen jollakin muulla maantieteellisellä alueella. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Jos ympäristösi sijaitsee samalla maantieteellisellä alueella kuin Azure OpenAI Service, se muodostaa yhteyden automaattisesti Azure OpenAI Serviceen, vaihtoehtoja ei ole. Euroopassa Business Central ottaa automaattisesti käyttöön tiedonsiirron, mutta järjestelmänvalvojat voivat halutessaan kieltäytyä siitä milloin tahansa.

> [!NOTE]
> Yksittäiset Copilotin ja luonnin tekoälyominaisuudet eivät välttämättä ole käytettävissä kaikilla Business Centralin maantieteellisen sijainnin alueilla. Kysy julkaisijalta lisätietoja kunkin ominaisuuden saatavuudesta.
> 
> Muiden kuin Microsoftin julkaisijoiden Copilot- ja luovat tekoälyominaisuudet, kuten mukautuksista tai asentamistasi AppSource-sovelluksista peräisin olevat, määrittelevät kukin omat Azure OpenAI Service -alueet. Kysy laajennuksen julkaisijalta lisätietoja siitä, mitä alueellista Azure-palvelua laajennuksessa käytetään. 

### Azure OpenAI Servicen maantieteelliset alueet

Seuraavassa taulukossa näkyy Copilotin käyttämä Azure OpenAI Servicen paikkatieto, joka perustuu Business Central -ympäristön maantieteelliseen sijaintiin. Nämä tiedot ovat tärkeitä, kun päätetään, valitaanko tiedonsiirto maantieteellisillä alueilla. Voit tunnistaa ympäristösi maantieteellisen sijainnin Business Central -hallintakeskuksessa, jossa sitä kutsutaan *Azure-alueeksi* (lisätietoja on kohdassa [Hallintakeskuksen ympäristöjen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Business Central -ympäristön maantieteellinen sijainti (Azure-alue)| Azure OpenAI Servicen maantieteellinen alue|
| - | - |
|Aasia (Itäinen, kaakkois-) |Yhdysvallat|
|Australia (Kaakkois-)| Yhdysvallat |
|Brasilia (eteläinen) |Yhdysvallat|
|Kanada (keskinen, itäinen)|Yhdysvallat|
|Eurooppa (Läntinen, pohjoinen)| Sveitsi |
|Ranska (keskinen, eteläinen)|Sveitsi |
|Saksa (Pohjoinen, keskinen läntinen)|Sveitsi |
|Intia (Keskinen, eteläinen)|Yhdysvallat|
|Japani (itäinen, läntinen)|Yhdysvallat|
|Korea (Keskinen, eteläinen)|Yhdysvallat|
|Norja (Itäinen, läntinen)|Sveitsi |
|Etelä-Afrikka (Pohjoinen, läntinen)|Yhdysvallat|
|Sveitsi (Pohjoinen, läntinen) |Sveitsi|
|Yhdistyneet arabiemiirikunnat (Pohjoinen, läntinen)|Yhdysvallat|
|Yhdistynyt kuningaskunta (Eteläinen, läntinen)|Yhdysvallat|
|Yhdysvallat (Keskinen, itäinen, pohjoinen keskinen, eteläinen keskinen, läntinen) |Yhdysvallat|
<!--
| Business Central environment geography | Azure OpenAI Service geography|
| - | - |
|Asia Pacific|United States|
|Australia| United States |
|Brazil |United States|
|Canada|United States|
|Europe| Switzerland |
|France|Switzerland |
|Germany|Switzerland |
|France|Switzerland |
|India|United States|
|Japan|United States|
|Korea|United States|
|Norway|Switzerland |
|Singapore|United States|
|South Africa|United States|
|Switzerland |Switzerland|
|United Arab Emirates|United States|
|United Kingdom|United States|
|United States|United States|-->

> [!NOTE]
> Sen jälkeen, kun Azure OpenAI Service voidaan ottaa käyttöön Business Centralin maantieteellisellä alueellasi, ympäristösi siirtyy automaattisesti käyttämään Azure OpenAI Serviceä ja valinta ei ole pakollista tai edes mahdollista.  
<!--

BC geos base on https://dynamics.microsoft.com/en-us/availability-reports/georeport/
case "AUSTRALIAEAST":
            case "AUSTRALIASOUTHEAST":
                return new CapiRegion("au", 2);
            case "BRAZILSOUTH":
                return new CapiRegion("br", 2);
            case "CANADACENTRAL":
            case "CANADAEAST":
                return new CapiRegion("ca", 2);
            case "CENTRALINDIA":
            case "SOUTHINDIA":
                return new CapiRegion("in", 1);
            case "EASTASIA":
                return new CapiRegion("as", 2);
            case "EASTUS":
            case "EASTUS2":
            case "SOUTHCENTRALUS":
            case "CENTRALUS":
            case "NORTHCENTRALUS":
            case "WESTUS":
            case "US":
                return new CapiRegion("us", 9, HasGpt4InGeo: true, HasTurboInGeo: true);
            case "FRANCECENTRAL":
            case "FRANCESOUTH":
                return new CapiRegion("fr", 1);
            case "GERMANYNORTH":
            case "GERMANYWESTCENTRAL":
                return new CapiRegion("de", 1);
            case "JAPANEAST":
            case "JAPANWEST":
                return new CapiRegion("jp", 1);
            case "KOREACENTRAL":
            case "KOREASOUTH":
                return new CapiRegion("kr", 1);
            case "NORWAYEAST":
            case "NORWAYWEST":
                return new CapiRegion("no", 1);
            case "SOUTHAFRICANORTH":
            case "SOUTHWESTAFRICA":
                return new CapiRegion("za", 1);
            case "SOUTHEASTASIA":
                return new CapiRegion("sg", 1);
            case "SWITZERLANDNORTH":
            case "SWITZERLANDWEST":
                return new CapiRegion("ch", 1, HasTurboInGeo: true);
            case "UKSOUTH":
            case "UKWEST":
                return new CapiRegion("uk", 2);
            case "NORTHEUROPE":
            case "WESTEUROPE":
                return new CapiRegion("eu", 10);
            case "UAENORTH":
            case "UAECENTRAL":
                return new CapiRegion("ae", 1);

-->

## Seuraavat vaiheet

Voit sallia tietojen siirron maantieteellisillä alueilla [Copilot ja tekoälyominaisuudet](https://businesscentral.dynamics.com/?page=7775) -sivulta. Lisätietoja on kohdassa [Tietojen siirtämisen salliminen maantieteellisillä alueilla](enable-ai.md#allow-data-movement-across-geographies).
