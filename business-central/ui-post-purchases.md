---
title: Ostoasiakirjojen kirjaaminen | Microsoft Docs
description: Lisätietoja ostoasiakirjojen kirjaamisessa käytetyistä kirjaustoiminnoista ja kirjattujen asiakirjojen päivittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 01/17/2020
ms.author: sgroespe
ms.openlocfilehash: 2565133adfab4fb5f6febeeccb69c4f3d6f59e71
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991878"
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

Jokaiselle ostotilaukselle luodaan ostotapahtuma **KP-tapahtuma**-taulukkoon. Myös toimittajan tilille **Toimittajatapahtuma**-taulukkoon luodaan tapahtuma ja lisäksi luodaan KP-tapahtuma asianmukaiselle ostovelkatilille. Lisäksi tilauksen kirjauksen tuloksena saattaa olla ALV-tapahtuman ja KP-tapahtuman luonti alennussummalle. Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -sivun **Alennuksen kirjaus** -kentän sisällön perusteella.

Kullekin ostotilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos ostorivit sisältävät nimikenumeroita) tai KP-tapahtuma **KP-tapahtuma**-taulukkoon (jos ostorivit sisältävät KP-tilin). Lisäksi ostotilaukset tallennetaan aina **Tavaran vastaanoton otsikko**- ja **Ostolaskun otsikko** -taulukoihin.

Ennen kirjausta voit tulostaa testiraportin, jossa on kaikki tiedot ostotilauksesta ja joka osoittaa mahdolliset virheet. Kun haluat tulostaa raportin, valitse **Kirjaus** ja valitse sitten **Testiraportti**.

> [!IMPORTANT]  
>   Kun kirjaat tilauksen, voit luoda sekä vastaanoton että laskun. Nämä voidaan luoda joko yhtäaikaa tai erikseen. Voit luoda osittaisen vastaanoton ja osittaisen laskutuksen täyttämällä **Vastaanotettava määrä** ja **Laskutettava määrä** -kentät yksittäisillä ostotilausriveillä ennen kirjausta. Huomaa, et voi luoda laskua jos sellaista ei ole vastaanotettu. Siispä ennen laskuttamista on täytynyt tallentaa vastaanotto, tai sinun täytyy valita samanaikainen vastaanotto ja laskutus.

Voit kirjata tai kirjata ja tulostaa. Jos valitset kirjaamisen ja tulostamisen, raportti tulostetaan tilauksen kirjaamisen yhteydessä. **Kirjaa erä** -toiminnolla voit kirjata useita tilauksia samanaikaisesti. Lisätietoja on kohdassa [Useiden asiakirjojen kirjaaminen samanaikaisesti](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Kirjaustapahtuminen katselu
Kun kirjaus on päättynyt, kirjatut ostorivit poistuvat tilauksesta. Viesti kertoo, milloin kirjaus on valmis. Tämän jälkeen voit nähdä kirjatut tapahtumat useissa kirjattuja tapahtumia sisältävissä sivuilla, kuten **Toimittajatapahtumat**-, **KP -tapahtumat**-, **Nimiketapahtumat**-, **Ostovastaanotot**- ja **Kirjatut ostolaskut** -sivuilla.

Useimmissa tapauksissa voit avata tapahtumat kortista tai asiakirjasta, johon ne vaikuttavat. Valitse esimerkiksi **Toimittajakortti**-sivulla **Tapahtumat**-toiminto.

## <a name="editing-ledger-entries"></a>Kirjaustapahtuminen muokkaus
Voit muokata arvoja kirjattujen ostoasiakirjojen tietyissä kentissä, kuten **Maksuviite**-kentässä. Lisätietoja on kohdassa [Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md). Jos sinulla on enemmän kriittisiä kenttiä, jotka vaikuttavat jäljitysketjuun, sinun täytyy peruuttaa tai kumota kirjaus. Lisätietoja on kohdassa [Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md). 

## <a name="see-related-training-at-microsoft-learnlearnmodulesreceive-invoice-dynamics-d365-business-centralindex"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Katso myös
[Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md)  
[Useiden asiakirjojen kirjaaminen samanaikaisesti](ui-batch-posting.md)  
[Osto](purchasing-manage-purchasing.md)  
[Asiakirjojen ja päiväkirjojen kirjaaminen](ui-post-documents-journals.md)  
[Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
