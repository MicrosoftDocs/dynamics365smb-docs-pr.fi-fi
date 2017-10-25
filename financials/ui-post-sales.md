---
title: Myyntiasiakirjojen kirjaaminen | Microsoft Docs
description: "Tutustu erilaisiin myyntiasiakirjojen kirjauksessa käytettäviin kirjaustoimintoihin."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 106102d07761673461bc28bbf6452ed05f926112
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="posting-sales"></a>Myynnin kirjaaminen
Kun valitset myyntiasiakirjan **Kirjausryhmä**-painikkeen, voit valita seuraavista kirjaustoiminnoista:

* **Kirjaa**
* **Testiraportti**
* **Kirjaa ja lähetä**
* **Kirjaa ja tulosta**
* **Kirjaa ja lähetä sähköpostitse**
* **Kirjaa erä**
* **Esikatsele kirjausta**

Kun olet täyttänyt kaikki rivit ja syöttänyt kaikki tiedot myyntitilaukseen, voit kirjata sen eli luoda vastaanoton ja laskun. Tämä luo toimituksen ja laskun.

Kun myyntitilaus on kirjattu, asiakkaan tili, pääkirjanpito ja nimiketapahtumat päivitetään.

Jokaiselle myyntitilaukselle luodaan myyntitapahtuma **KP-tapahtuma**-taulukossa. Myös **Toimittajatapahtuma**-taulukon asiakkaan tilille luodaan tapahtuma. Lisäksi luodaan pääkirjanpidon tapahtuma asianmukaiselle myyntisaamistilille. Lisäksi tilauksen kirjauksen tuloksena saattaa olla ALV-tapahtuman ja KP-tapahtuman luonti alennussummalle. Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -ikkunan **Alennuksen kirjaus** -kentän sisällön perusteella.

Jokaiselle myyntitilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos myyntiriveillä on nimikenumeroita) tai pääkirjanpidon tapahtuma **KP-tapahtuma**-taulukkoon (jos myyntiriveillä on pääkirjanpitotili). Tämän lisäksi myyntitilaukset tallennetaan aina **Lähtevän toimituksen otsikko**- ja **Myyntilaskun otsikko** -taulukoihin.

> [!IMPORTANT]  
>   Kun kirjaat tilauksen, voit luoda sekä toimituksen että laskun. Tämä voidaan tehdä samaan aikaan tai erikseen. Voit luoda myös osittaisen toimituksen tai osittaisen laskun täyttämällä **Toimitettava määrä**- ja **Laskutettava määrä** -kentät yksittäisillä myyntitilausriveillä ennen kirjausta. Huomaa, että laskua ei voi luoda jollekin, jota ei ole toimitettu. Tämä tarkoittaa sitä, että ennen laskutusta on täytynyt tallentaa toimitus, tai täytyy valita yhtäaikainen toimitus ja laskutus.

Kun kirjaus on päättynyt, kirjatut myyntirivit poistuvat tilauksesta. Viesti kertoo, milloin kirjaus on valmis. Tämän jälkeen voit nähdä kirjatut tapahtumat kirjattuja tapahtumia sisältävissä ikkunoissa, kuten **Asiakastapahtumat**-, **KP-tapahtumat**-, **Nimiketapahtumat**-, **Kirjatut myyntitoimitukset**- ja**Kirjatut myyntilaskut** -ikkunassa.

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Toimintaohje: Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)


