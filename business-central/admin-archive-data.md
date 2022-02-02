---
title: Tietoarkisto-laajennus
description: Tietojen arkistointi luo tietueiden edullisen varmuuskopion.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 630
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 4070ff5658ad4aa976c181a3df377155080f1e3b
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012075"
---
# <a name="the-data-archive-extension"></a>Tietoarkisto-laajennus
Ajan mittaan yrityksesi kerää huomattavan määrän tietoa, ja järjestelmänvalvojana on todennäköisesti hyvä luoda tietojen arkistointistrategia. Kun tietoja on paljon, esimerkiksi raporttien luominen tai tietueiden luominen voi kestää hieman kauemmin, tai tietueet voivat jopa lukittua. Lisäksi suuret tietomäärät voivat aiheuttaa lisääntyneitä tallennuskustannuksia.

Tietoarkistolaajennus tarjoaa peruskehyksen tietojen arkistointiin ja varmuuskopiointiin päivämäärätiivistyksen osana. Kun käytät päivämäärätiivistystä, liittyvät tapahtumat konsolidoidaan yhdeksi tapahtumaksi ja alkuperäiset poistetaan. Lisätietoja on kohdassa [Tietojen pakkaaminen päivämäärätiivistyksen avulla](admin-manage-documents.md#compress-data-with-date-compression). Tietojen säilyttäminen saattaa kuitenkin olla arvokasta, joten sen sijaan voit arkistoida sen myöhempää käyttöä varten.

## <a name="start-archiving-data"></a>Tietojen arkistoinnin aloittaminen
Laajennus on esiasennettuna ja saatavilla **laajennuksen hallinnassa**, joten sinun ei tarvitse tehdä mitään päästäksesi alkuun. Laajennus on saatavilla myös Microsoft AppSourcessa. 

Tietoarkistot on luetteloitu **Tietoarkistoluettelo**-sivulla. Jokainen arkisto voi sisältää tietoja useista taulukoista, ja niihin mahtuu enintään 10 000 tietuetta. Jos taulukossa on enemmän kuin 10 000 tietuetta, seuraavalle 10 000 tietueille luodaan toinen arkisto ja niin edelleen. Jos arkistoit esimerkiksi 10 100 KP-tapahtumaa, Business Central luo yhden "KP-tapahtuma"-arkiston ensimmäiselle 10 000 tapahtumalle ja sitten toisen arkiston jäljellä oleville 100 tapahtumalle. 

Tietojen arkistoinnin jälkeen voit tutkia niitä käyttämällä Microsoft Exceliä tai CSV-tiedostona.

* Jos käytät Excel-vaihtoehtoa, työkirja sisältää yhden laskentataulukon kutakin tietoarkiston taulukkoa varten.
* Jos käytät CSV-valintaa, saat ZIP-tiedoston, jossa on yksi CSV-tiedosto kutakin tietoarkiston taulukkoa varten.

> [!TIP]
> Excel- ja CSV-vaihtoehdot helpottavat toisen sovelluksen tai palvelun käyttämistä tietojen siirtämiseen toiseen paikkaan, esimerkiksi Azure Blob -tallennustilaan tai analyysityökaluun, kuten Microsoft Power BI:hin.

Tietoarkistolaajennuksia käyttävät seuraavat erätyöt päivämäärätiivistykseen.

|Eräajot  |
|---------|
|Pvmtiivistys Nimikkeiden budjettitapahtumat |
|Tiivistä pankkitilikirjaukset |
|Tiivistä asiakastapahtumat |
|Tiivistä KO-kirjaukset |
|Tiivistä pääkirjanpito |
|Tiivistä vakuutuskirjaukset |
|Tiivistä kunn.pitokirjaukset Kirjanpito |
|Tiivistä kunn.pitokirjaukset Kirjanpito |
|Tiivistä resurssikirjaukset |
|Tiivistä ALV-tapahtumat |
|Tiivistä toimittajakirjaukset |
|Pvm-tiivistä f.var. tapahtumat Tapahtumat |
|Pvmtiivistys KP-budjetin tapahtumat |

Voit aloittaa tietojen arkistoinnin, kun suoritat yhden eräajosta, ottamalla käyttöön **Arkistoi poistetut tapahtumat** -valitsimen.

## <a name="storage-considerations"></a>Huomioitavaa tallennuksesta
Arkistoidut tiedot tallennetaan **Vuokraajan media** -taulukkoon. Tämä taulukko ei sisälly tietokannan koon laskentaan käyttöoikeusehtojen mukaisesti. Sen sijaan se lasketaan tiedostotallennustilana. On kuitenkin suositeltavaa viedä vanhat arkistot esimerkiksi CSV-tiedostoon ja poistaa vanhat arkistotietueet.

## <a name="see-also"></a>Katso myös
[Hallitse tallennustilaa poistamalla asiakirjoja tai pakkaamalla tietoja](admin-manage-documents.md)
