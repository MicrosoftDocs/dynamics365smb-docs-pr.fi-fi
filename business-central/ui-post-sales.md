---
title: Myyntiasiakirjojen kirjaaminen | Microsoft Docs
description: Lisätietoja myyntiasiakirjojen kirjaamisessa käytetyistä kirjaustoiminnoista ja kirjattujen asiakirjojen päivittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/27/2019
ms.author: sgroespe
ms.openlocfilehash: a2eb27a541033b755b9ab9d4ea9156bf7de9cab4
ms.sourcegitcommit: f46793abdb3efd8384c10eb7992e076383251f2c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/27/2019
ms.locfileid: "1921428"
---
# <a name="posting-sales"></a>Myynnin kirjaaminen
Kun valitset myyntiasiakirjan **Kirjaus**-valikon, voit valita seuraavista kirjaustoiminnoista:

* **Kirjaa**
* **Kirjaus ja uusi**
* **Kirjaa ja lähetä**
* **Esikatsele kirjausta**
* **Laskuluonnos**
* **Proformalasku**
* **Testiraportti**

Kun olet täyttänyt kaikki rivit ja syöttänyt kaikki tiedot myyntitilaukseen, voit kirjata sen eli luoda vastaanoton ja laskun. Tämä luo toimituksen ja laskun.

Kun myyntitilaus on kirjattu, asiakkaan tili, pääkirjanpito ja nimiketapahtumat päivitetään.

Jokaiselle myyntitilaukselle luodaan myyntitapahtuma **KP-tapahtuma**-taulukossa. Myös **Toimittajatapahtuma**-taulukon asiakkaan tilille luodaan tapahtuma. Lisäksi luodaan pääkirjanpidon tapahtuma asianmukaiselle myyntisaamistilille. Lisäksi tilauksen kirjauksen tuloksena saattaa olla ALV-tapahtuman ja KP-tapahtuman luonti alennussummalle. Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -sivun **Alennuksen kirjaus** -kentän sisällön perusteella.

Jokaiselle myyntitilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos myyntiriveillä on nimikenumeroita) tai pääkirjanpidon tapahtuma **KP-tapahtuma**-taulukkoon (jos myyntiriveillä on pääkirjanpitotili). Tämän lisäksi myyntitilaukset tallennetaan aina **Lähtevän toimituksen otsikko**- ja **Myyntilaskun otsikko** -taulukoihin.

> [!IMPORTANT]  
>   Kun kirjaat tilauksen, voit luoda sekä toimituksen että laskun. Tämä voidaan tehdä samaan aikaan tai erikseen. Voit luoda myös osittaisen toimituksen tai osittaisen laskun täyttämällä **Toimitettava määrä**- ja **Laskutettava määrä** -kentät yksittäisillä myyntitilausriveillä ennen kirjausta. Huomaa, että laskua ei voi luoda jollekin, jota ei ole toimitettu. Tämä tarkoittaa sitä, että ennen laskutusta on täytynyt tallentaa toimitus, tai täytyy valita yhtäaikainen toimitus ja laskutus.

Kun kirjaus on päättynyt, kirjatut myyntirivit poistuvat tilauksesta. Viesti kertoo, milloin kirjaus on valmis. Tämän jälkeen voit nähdä kirjatut tapahtumat kirjattuja tapahtumia sisältävillä sivuilla, kuten **Asiakastapahtumat**-, **KP-tapahtumat**-, **Nimiketapahtumat**-, **Kirjatut myyntitoimitukset**- ja**Kirjatut myyntilaskut** -sivuilla.  

Voit muokata arvoja kirjattujen myyntiasiakirjojen tietyissä kentissä, kuten **Paketin seurantanumero** -kentässä. Lisätietoja on kohdassa [Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md).

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md)  
[Kerro, mitä haluat tehdä -toiminnon käyttäminen toimintojen ja tietojen etsimisessä](ui-search.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
