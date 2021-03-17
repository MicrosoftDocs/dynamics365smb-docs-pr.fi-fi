---
title: Myyntiasiakirjojen kirjaaminen | Microsoft Docs
description: Lisätietoja myyntiasiakirjojen kirjaamisessa käytetyistä kirjaustoiminnoista ja kirjattujen asiakirjojen päivittämisestä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: e0d1bd7770eb3bb44a2e9b3203ffa158a246cfa9
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392047"
---
# <a name="posting-sales"></a>Myynnin kirjaaminen

Kun valitset myyntiasiakirjan **Kirjaus**-valikon, voit valita seuraavista kirjaustoiminnoista:

* **Kirjaa**
* **Kirjaus ja uusi**
* **Kirjaa ja lähetä**
* **Esikatsele kirjausta**
* **Kirjaa erä**
* **Testiraportti**

> [HUOMAUTUS!] Myyntitilausten osalta voit tarkastella myös ennakkomaksutoimintoihin liittyviä asetuksia. Lisätietoja on kohdassa [Ennakkomaksujen laskuttaminen](finance-invoice-prepayments.md). 

Kun olet täyttänyt kaikki rivit ja syöttänyt kaikki tiedot myyntitilaukseen, voit kirjata sen eli luoda vastaanoton ja laskun. Tämä luo toimituksen ja laskun.

Kun myyntitilaus on kirjattu, asiakkaan tili, pääkirjanpito ja nimiketapahtumat päivitetään.

Jokaiselle myyntitilaukselle luodaan myyntitapahtuma **KP-tapahtuma**-taulukossa. Myös **Toimittajatapahtuma**-taulukon asiakkaan tilille luodaan tapahtuma. Lisäksi luodaan pääkirjanpidon tapahtuma asianmukaiselle myyntisaamistilille. Lisäksi tilauksen kirjauksen tuloksena saattaa olla ALV-tapahtuman ja KP-tapahtuman luonti alennussummalle. Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -sivun **Alennuksen kirjaus** -kentän sisällön perusteella.

Jokaiselle myyntitilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos myyntiriveillä on nimikenumeroita) tai pääkirjanpidon tapahtuma **KP-tapahtuma**-taulukkoon (jos myyntiriveillä on pääkirjanpitotili). Tämän lisäksi myyntitilaukset tallennetaan aina **Lähtevän toimituksen otsikko**- ja **Myyntilaskun otsikko** -taulukoihin.

> [!IMPORTANT]  
> Kun kirjaat tilauksen, voit luoda sekä toimituksen että laskun. Tämä voidaan tehdä samaan aikaan tai erikseen. Voit luoda myös osittaisen toimituksen tai osittaisen laskun täyttämällä **Toimitettava määrä**- ja **Laskutettava määrä** -kentät yksittäisillä myyntitilausriveillä ennen kirjausta. Huomaa, että laskua ei voi luoda jollekin, jota ei ole toimitettu. Tämä tarkoittaa sitä, että ennen laskutusta on täytynyt tallentaa toimitus, tai täytyy valita yhtäaikainen toimitus ja laskutus.

Voit kirjata tai kirjata ja lähettää. Jos valitset kirjaamisen ja lähettämisen, ohjelma luo PDF-tiedoston, jonka voit lähettää. **Kirjaa erä** -toiminnolla voit kirjata useita tilauksia samanaikaisesti. Lisätietoja on kohdassa [Useiden asiakirjojen kirjaaminen samanaikaisesti](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Kirjaustapahtuminen katselu

Kun kirjaus on päättynyt, kirjatut myyntirivit poistuvat tilauksesta. Viesti kertoo, milloin kirjaus on valmis. Tämän jälkeen voit nähdä kirjatut tapahtumat kirjattuja tapahtumia sisältävillä sivuilla, kuten **Asiakastapahtumat**-, **KP-tapahtumat**-, **Nimiketapahtumat**-, **Kirjatut myyntitoimitukset**- ja **Kirjatut myyntilaskut** -sivuilla.  

Useimmissa tapauksissa voit avata tapahtumat kortista tai asiakirjasta, johon ne vaikuttavat. Valitse esimerkiksi **Asiakaskortti**-sivulla **Tapahtumat**-toiminto.

## <a name="editing-ledger-entries"></a>Kirjaustapahtuminen muokkaus

Voit muokata arvoja kirjattujen ostoasiakirjojen tietyissä kentissä, kuten **Paketin seurantanumerossa** -kentässä. Lisätietoja on kohdassa [Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md). Jos sinulla on enemmän kriittisiä kenttiä, jotka vaikuttavat jäljitysketjuun, sinun täytyy peruuttaa tai kumota kirjaus. Lisätietoja on kohdassa [Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Myynti](sales-manage-sales.md)  
[Useiden asiakirjojen kirjaaminen samanaikaisesti](ui-batch-posting.md)  
[Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]