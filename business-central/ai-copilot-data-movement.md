---
title: Copilot-tietojen siirtäminen maantieteellisten alueiden välillä
description: 'Tutustu siihen, miten Dynamics 365 Business Centralin Copilot-toiminnoissa käytetty data liikkuu eri maantieteellisillä alueilla, joilla Azure OpenAI Service ei ole oletusarvoisesti saatavilla.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 11/30/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# Copilot-tietojen siirtäminen maantieteellisten alueiden välillä 

Copilot on käytettävissä kaikilla tuetuilla [Business Centralin maissa/alueilla](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Copilot kuitenkin käyttää Microsoft Azure OpenAI Serviceä, joka on tällä hetkellä käytettävissä Business Centralissa vain joillakin maantieteellisillä alueilla. Tämä tarkoittaa, että jos ympäristösi sijaitsee muualla, Copilotin ja luovien tekoälyominaisuuksien tiedot on siirrettävä maantieteellisen alueesi ulkopuolelle ja niitä voidaan käsitellä ja tallentaa vaatimustenmukaisuusrajojesi ulkopuolelle. Tiedot sisältävät tekoälyn kehotukset ja liiketoimintatiedot, joita Copilot käyttää tai luo. Siinä tapauksessa sinun täytyy valita, että sallit tiedonsiirron Azure OpenAI Servicen jollakin muulla maantieteellisellä alueella. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Jos ympäristösi sijaitsee samalla Azure-alueella kuin Azure OpenAI Service, se muodostaa yhteyden automaattisesti Azure OpenAI Serviceen, vaihtoehtoja ei ole eikä kertaluonteista määritystä vaadita.

> [!NOTE]
> Yksittäiset Copilotin ja luonnin tekoälyominaisuudet eivät välttämättä ole käytettävissä kaikissa Business Central -ympäristön maissa tai alueilla. Kysy julkaisijalta lisätietoja kunkin ominaisuuden saatavuudesta.
> 
> Muiden kuin Microsoftin julkaisijoiden Copilot- ja luovat tekoälyominaisuudet, kuten mukautuksista tai asentamistasi AppSource-sovelluksista peräisin olevat, määrittelevät kukin omat Azure OpenAI Service -alueet. Kysy laajennuksen julkaisijalta lisätietoja siitä, mitä alueellista Azure-palvelua laajennuksessa käytetään. 

### Azure OpenAI Servicen maantieteelliset alueet

Seuraavassa taulukossa näkyy Copilotin käyttämä Azure OpenAI Servicen paikkatieto, joka perustuu Business Central -ympäristön Azure-alueeseen. Nämä tiedot ovat tärkeitä, kun päätetään, valitaanko tiedonsiirto maantieteellisillä alueilla. Voit tunnistaa ympäristösi Azure-alueeseen Business Central -hallintakeskuksessa (lisätietoja on kohdassa [Hallintakeskuksen ympäristöjen hallinta](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Ympäristön Azure-alue| Azure OpenAI Servicen maantieteellinen alue|Copilotin lukituksen avaaminen edellyttää järjestelmänvalvojan toimenpiteitä| 
| - | - | - |
|Aasia (Itäinen, kaakkois-) |Yhdysvallat|Kyllä|
|Australia (Kaakkois-)| Yhdysvallat |Kyllä |
|Brasilia (eteläinen) |Yhdysvallat|Kyllä|
|Kanada (keskinen, itäinen)|Yhdysvallat|Kyllä|
|Eurooppa (Läntinen, pohjoinen)| Ruotsi tai Sveitsi |Ei\*|
|Ranska (keskinen, eteläinen)| Ruotsi tai Sveitsi |Kyllä|
|Saksa (Pohjoinen, keskinen läntinen)| Ruotsi tai Sveitsi |Kyllä|
|Intia (Keskinen, eteläinen)|Yhdysvallat|Kyllä|
|Japani (itäinen, läntinen)|Yhdysvallat|Kyllä|
|Korea (Keskinen, eteläinen)|Yhdysvallat|Kyllä|
|Norja (Itäinen, läntinen)|Ruotsi tai Sveitsi |Kyllä|
|Etelä-Afrikka (Pohjoinen, läntinen)|Yhdysvallat|Kyllä|
|Sveitsi (Pohjoinen, läntinen) |Ruotsi tai Sveitsi |Kyllä|
|Yhdistyneet arabiemiirikunnat (Pohjoinen, läntinen)|Yhdysvallat|Kyllä|
|Yhdistynyt kuningaskunta (Eteläinen, läntinen)|Yhdistynyt kuningaskunta|Kyllä|
|Yhdysvallat (Keskinen, itäinen, pohjoinen keskinen, eteläinen keskinen, läntinen) |Yhdysvallat|Ei|

\* Länsi-Euroopan ja Pohjois-Euroopan Azure-alueiden ympäristöissä Business Central ottaa automaattisesti käyttöön tiedonsiirron eri maantieteellisillä alueilla, mutta järjestelmänvalvojat voivat halutessaan poistaa sen käytöstä milloin tahansa.

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

Voit sallia tietojen siirron (sisään tai ulos) maantieteellisillä alueilla [Copilot ja tekoälyominaisuudet](https://businesscentral.dynamics.com/?page=7775) -sivulta. Lisätietoja on kohdassa [Tietojen siirtämisen salliminen maantieteellisillä alueilla](enable-ai.md#allow-data-movement-across-geographies).
