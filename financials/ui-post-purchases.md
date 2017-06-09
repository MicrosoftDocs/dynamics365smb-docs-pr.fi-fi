---
title: Ostojen kirjaaminen | Microsoft Docs
description: "Lisätietoja ostojen kirjaamisesta."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2016
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ac79d81aba2fb86a2c4a95356e8a621e5f5813ea
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="posting-purchases"></a>Ostojen kirjaaminen
Kun valitset ostoasiakirjan **Kirjausryhmä**-painikkeen, voit valita seuraavista kirjaustoiminnoista:

* **Kirjaa**
* **Esikatsele kirjausta**
* **Kirjaa ja tulosta**
* **Testiraportti**
* **Kirjaa erä**

Kun olet täyttänyt kaikki rivit ja syöttänyt kaikki tiedot ostotilaukseen, voit kirjata sen eli luoda vastaanoton ja laskun.

Kun ostotilaus on kirjattu, toimittajan tili, pääkirjanpito ja nimiketapahtumat päivitetään.

Jokaiselle ostotilaukselle luodaan ostotapahtuma **KP-tapahtuma**-taulukkoon. Myös toimittajan tilille **Toimittajatapahtuma**-taulukkoon luodaan tapahtuma ja lisäksi luodaan KP-tapahtuma asianmukaiselle ostovelkatilille. Lisäksi tilauksen kirjauksen tuloksena saattaa olla ALV-tapahtuman ja KP-tapahtuman luonti alennussummalle. Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -taulukon **Alennuksen kirjaus** -kentän sisällön perusteella.

Kullekin ostotilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos ostorivit sisältävät nimikenumeroita) tai KP-tapahtuma **KP-tapahtuma**-taulukkoon (jos ostorivit sisältävät KP-tilin). Lisäksi ostotilaukset tallennetaan aina **Tavaran vastaanoton otsikko**- ja **Ostolaskun otsikko** -taulukoihin.

Ennen kirjausta voit tulostaa testiraportin, jossa on kaikki tiedot ostotilauksesta ja joka osoittaa mahdolliset virheet. Kun haluat tulostaa raportin, valitse **Kirjaus** ja valitse sitten **Testiraportti**.

**Tärkeää**: Kun kirjaat tilauksen, voit luoda sekä vastaanoton että laskun. Nämä voidaan luoda joko yhtäaikaa tai erikseen. Voit luoda osittaisen vastaanoton ja osittaisen laskutuksen täyttämällä **Vastaanotettava määrä** ja **Laskutettava määrä** -kentät yksittäisillä ostotilausriveillä ennen kirjausta. Huomaa, et voi luoda laskua jos sellaista ei ole vastaanotettu. Siispä ennen laskuttamista on täytynyt tallentaa vastaanotto, tai sinun täytyy valita samanaikainen vastaanotto ja laskutus.

Voit kirjata tai kirjata ja tulostaa. Jos valitset kirjaamisen ja tulostamisen, raportti tulostetaan tilauksen kirjaamisen yhteydessä. **Kirjaa erä** -toiminnolla voit kirjata useita tilauksia samanaikaisesti..

Kun kirjaus on päättynyt, kirjatut ostorivit poistuvat tilauksesta. Viesti kertoo, milloin kirjaus on valmis. Tämän jälkeen voit nähdä kirjatut tapahtumat useissa kirjattuja tapahtumia sisältävissä ikkunoissa, kuten **Toimittajatapahtumat**-, **KP -tapahtumat**-, **Nimiketapahtumat**-, **Ostovastaanotot**- ja **Kirjatut ostolaskut** -ikkunassa.

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Asiakirjojen ja päiväkirjojen kirjaaminen](ui-post-documents-journals.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)


