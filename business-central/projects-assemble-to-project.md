---
title: Kokoonpano projektiin
description: Tietoja projektin kokoonpanosta tilausta varten käytöstä.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Kokoonpano projektiin

Kokoonpano projektiin auttaa parantaa varastonhallintaa kokoamalla tilausta varten vasta tarvittaessa.

Kun projektin suunnittelurivillä valitaan kokoonpano tilausta varten -nimike, [!INCLUDE [prod_short](includes/prod_short.md)] luo kokoonpanotilauksen. Kokoonpanotilaus perustuu projektin suunnitteluriviin, ja sen rivit perustuvat nimikkeen kokoonpanon tuoterakenteeseen. Lisätietoja kokoonpanon tuoterakenteesta on kohdassa [Kokoonpanon tuoterakenteiden käsitteleminen](assembly-how-work-assembly-boms.md). Kokoonpanon tuoterakenteen komponenttien määrä kerrotaan tilauksen määrällä. **Kokoonpano tilausta varten -rivit** -sivulla on tietoja linkitetyissä kokoonpanotilauksen riveistä. Tiedot voivat auttaa mukauttamaan kokoonpanon nimikettä. Myynnin tavoin linkitettyjä kokoonpanotilauksia ei voi kirjata suoraan. Lisätietoja kokoonpanotilauksista on kohdassa [Varastonimikkeiden myyminen kokoonpano tilausta varten -työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

Kokoonpanotilaukset varataan projekteille ja [!INCLUDE [prod_short](includes/prod_short.md)] synkronoi nimikeseurannan projektin suunnittelurivien ja kokoonpanotilauksen välillä.

## Varastonhallinnan integrointi

Kokoonpano projektiin integroituu varastonhallinnan ominaisuuksiin, mikä helpottaa kokoonpanoa ja toimitusta. Prosessi auttaa myös varmistamaan, että työnkulku projektin kokoonpanosta toimitukseen tapahtuu sujuvasti sisäisissä varastoprosesseissa. Lisätietoja projektien sisäisistä varastotyönkuluista on kohdassa [Tuotanto-, kokoonpano- ja projektityönkulut](design-details-internal-warehouse-flows.md#flows-to-and-from-assembly-in-a-basic-warehouse-configuration).

Seuraavassa taulukossa käsitellään varastomäärityksiä, joita kokoonpano tilauksia varten tukee.

|Määritys  |Kuvaus  |
|---------|---------|
|**Ei fyysisen varaston käsittelyä**|Täyden tai osittaisen käytön kirjaaminen projektipäiväkirjaan. Kokoonpanotilauksen komponenttien tuotos ja kulutus kirjataan automaattisesti.         |
|**Varaston poiminta**|Täyden tai osittaisen käytön kirjaaminen varaston poiminnan avulla. Kokoonpanotilauksen komponenttien tuotos ja kulutus kirjataan automaattisesti.          |
|**F.varastoinnin poiminta**|Komponenttien fyysisen varaston poimintojen luominen ja rekisteröiminen sekä käytön kirjaaminen projektipäiväkirjaan. [!INCLUDE [prod_short](includes/prod_short.md)] tarkistaa, poimittiinko kulutetut kokoonpanon komponentit. Kokoonpanotilauksen komponenttien tuotos ja kulutus kirjataan automaattisesti.         |

## Tunnetut rajoitukset

Tässä osassa käsitellään tunnettuja kokoonpano projektiin -rajoituksia.

* **Kokoonpantava määrä tilausta varten** -kenttä ei ole käytettävissä suljetuissa projekteissa.
* Fyysisen varaston poimintaskenaarioissa **Kokoonpantava määrä tilausta varten** voi olla joko nolla tai sama kuin määrä. Kokoonpanoa tilausta varten ja kokoonpanoa varastoon ei voi yhdistää projektin suunnittelurivillä. Niille on luotava erilliset projektin suunnittelurivit.
* Kokoonpano tilausta varten ei vaikuta projektin laskutettaviin osiin. Kokoonpano sisällytetään myyntilaskuihin, sen komponentteja ei. Laskutettavien rivien **Kokoonpantava määrä tilausta varten** -kenttää ei voi muokata.
* Tällä ei ole vaikutusta tilauksen suunnitteluun eikä suunnittelutyökirjaan, koska projektia käytetään suunnitteluun. Suunnittelumoduuli pitää kokoonpanoa kysyntänä.
* **Kokoonpantava määrä tilausta varten** -kenttään ei voi syöttää negatiivista arvoa.
* Kokoonpanoa ei voi kumota.

## Katso myös

[Projektien hallinta](projects-manage-projects.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Projektien luominen](projects-how-create-jobs.md)
