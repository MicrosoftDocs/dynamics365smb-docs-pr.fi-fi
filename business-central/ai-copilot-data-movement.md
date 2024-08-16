---
title: Copilot-tietojen siirtäminen maantieteellisten alueiden välillä
description: 'Tutustu siihen, miten Dynamics 365 Business Centralin Copilot-toiminnoissa käytetty data liikkuu eri maantieteellisillä alueilla, joilla Azure OpenAI Service ei ole oletusarvoisesti saatavilla.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 04/16/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
ms.search.form: 7775
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
|Australia (Kaakkois-)| Australia |Ei |
|Brasilia (eteläinen) |Yhdysvallat|Kyllä|
|Kanada (keskinen, itäinen)|Yhdysvallat|Kyllä|
|Eurooppa (Läntinen, pohjoinen)| Ruotsi tai Sveitsi |Ei\*|
|Ranska (keskinen, eteläinen)| Ruotsi tai Sveitsi |Kyllä|
|Saksa (Pohjoinen, keskinen läntinen)| Ruotsi tai Sveitsi |Kyllä|
|Intia (Keskinen, eteläinen)|Intia|Ei|
|Japani (itäinen, läntinen)|Yhdysvallat|Kyllä|
|Korea (Keskinen, eteläinen)|Yhdysvallat|Kyllä|
|Norja (Itäinen, läntinen)|Ruotsi tai Sveitsi |Kyllä|
|Etelä-Afrikka (Pohjoinen, läntinen)|Yhdysvallat|Kyllä|
|Sveitsi (Pohjoinen, läntinen) |Ruotsi tai Sveitsi |Kyllä|
|Yhdistyneet arabiemiirikunnat (Pohjoinen, läntinen)|Yhdysvallat|Kyllä|
|Yhdistynyt kuningaskunta (Eteläinen, läntinen)|Yhdistynyt kuningaskunta|Ei|
|Yhdysvallat (Keskinen, itäinen, pohjoinen keskinen, eteläinen keskinen, läntinen) |Yhdysvallat|Ei|

\* Länsi-Euroopan ja Pohjois-Euroopan Azure-alueiden ympäristöissä Business Central ottaa automaattisesti käyttöön tiedonsiirron eri maantieteellisillä alueilla, mutta järjestelmänvalvojat voivat halutessaan poistaa sen käytöstä milloin tahansa.

> [!NOTE]
> Sen jälkeen, kun Azure OpenAI Service voidaan ottaa käyttöön Business Centralin maantieteellisellä alueellasi, ympäristösi siirtyy automaattisesti käyttämään Azure OpenAI Serviceä ja valinta ei ole pakollista tai edes mahdollista.


## Seuraavat vaiheet

Voit sallia tietojen siirron (sisään tai ulos) maantieteellisillä alueilla [Copilot ja tekoälyominaisuudet](https://businesscentral.dynamics.com/?page=7775) -sivulta. Lisätietoja on kohdassa [Tietojen siirtämisen salliminen maantieteellisillä alueilla](enable-ai.md#allow-data-movement-across-geographies).
