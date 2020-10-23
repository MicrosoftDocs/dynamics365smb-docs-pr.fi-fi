---
title: Sähköpostin lokiinkirjauksen määrittäminen | Microsoft Docs
description: Lisätietoja siitä, miten myyjien ja asiakkaiden sähköpostivuorovaikutukset voidaan muuttaa todellisiksi myyntimahdollisuuksiksi.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f02e78e0b5c7d7f6d3c22cd12e37bdaf74f4b90f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923618"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Myyjien ja yhteyshenkilöiden välisten sähköpostiviestien seuraaminen

Saat enemmän hyötyä myyjien ja olemassa olevien tai potentiaalisten asiakkaiden välisestä viestinnästä, jos seuraat sähköpostiviestejä ja muunnat ne toiminnallisiksi mahdollisuuksiksi. [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellusta voi käyttää yhdessä Exchange Onlinen kanssa. Näin voit seurata saapuvia ja lähteviä viestejä. Voit tarkastella ja analysoida kunkin viestin sisältöä **Vuorovaikutuslokin tapahtumat** -sivulla.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Yleisten kansioiden ja sääntöjen määrittäminen sähköpostin lokiinkirjausta Exchange Onlinessa

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Seuraavaksi [!INCLUDE[prodshort](includes/prodshort.md)] yhdistetään Exchange Onlineen.

## <a name="setting-up-d365fin-to-log-email-messages"></a>Määritetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellus sähköpostiviestien kirjaamista varten

Aloita sähköpostien kirjaaminen seuraavien kahden helpon vaiheen avulla:

1. Muodosta yhteys [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen Exchange Onlinen avulla Microsoft 365 -tilauksessa. Exchange Online käsittelee sähköpostiviestisi. Tämä on helppo tehdä asetusten ohjatun määrityksen oppaan avulla. Tarvitset vain järjestelmänvalvojan tunnistetiedot Microsoft 365:n järjestelmänvalvojan tiliä varten. Aloita oppaan käyttäminen siirtymällä **Asetusten ohjattu määritys** -kohtaan ja valitsemalla **Määritä sähköpostin lokiinkirjaus**.  

2. Varmista, että [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen on määritetty oikeat sähköpostiosoitteet myyjille ja yhteyshenkilöille sen mukaan, ovatko he potentiaalisia vai olemassa olevia asiakkaita. Tee tämä avaamalla kunkin asiakkaan tai myyjän **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortti ja tarkistamalla **Sähköposti**-kenttä.

> [!Tip]
> Kun olet tehnyt nämä oppaan vaiheet, voit tarkistaa yhteyden tilan. Siirry **Kontaktienhallinnan asetukset** -kohtaan, valitse **Prosessi** ja valitse sitten **Toiminnot**. Valitse lopuksi **Tarkista sähköpostin lokiinkirjauksen asetukset**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Sähköpostiviestien tarkasteleminen vuorovaikutuslokissa

[!INCLUDE[d365fin](includes/d365fin_md.md)] luo **Vuorovaikutusloki**-sivulle tapahtuman aina, kun myyjä ja yhteyshenkilö lähettävät sähköpostiviestejä. Voit tarkastella vuorovaikutuslokia avaamalla **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortin ja valitsemalla sitten **Historia**- ja **Vuorovaikutuslokin tapahtumat** -kohdat. Lokin tapahtumille voi tehdä esimerkiksi seuraavia toimintoja:

- Voit tarkastella sähköpostiviestin sisältöä valitsemalla **Näytä liitteet** -toiminnon.
- Voit muuttaa sähköpostiviestinnän myyntimahdollisuudeksi. Jos tapahtuma näyttää lupaavalta, voit muuttaa sen mahdollisuudeksi, jonka jälkeen siitä voi kehittyä myyntiä. Valitse ensin tapahtuma ja valitse sitten **Luo mahdollisuus**-toiminto. Lisätietoja on kohdassa [Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Katso myös
[Kontaktienhallinta](marketing-relationship-management.md)

