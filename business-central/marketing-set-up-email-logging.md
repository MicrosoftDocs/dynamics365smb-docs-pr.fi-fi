---
title: Sähköpostin lokiinkirjauksen määrittäminen | Microsoft Docs
description: Lisätietoja siitä, miten myyjien ja asiakkaiden sähköpostivuorovaikutukset voidaan muuttaa todellisiksi myyntimahdollisuuksiksi.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 08/26/2019
ms.author: bholtorf
ms.openlocfilehash: e42618be17ff4f9bfe0d54a88e70d5a1841568c1
ms.sourcegitcommit: 8d9f08304b2f3b5504332bc626383797564ac5e3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/26/2019
ms.locfileid: "1920464"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Myyjien ja yhteyshenkilöiden välisten sähköpostiviestien seuraaminen
Saat enemmän hyötyä myyjien ja olemassa olevien tai potentiaalisten asiakkaiden välisestä viestinnästä, jos seuraat sähköpostiviestejä ja muunnat ne toiminnallisiksi mahdollisuuksiksi. [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellusta voi käyttää yhdessä Exchange Onlinen kanssa. Näin voit seurata saapuvia ja lähteviä viestejä. Voit tarkastella ja analysoida kunkin viestin sisältöä **Vuorovaikutuslokin tapahtumat** -sivulla.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a>Määritetään [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellus sähköpostiviestien kirjaamista varten
Aloita sähköpostien kirjaaminen seuraavien kahden helpon vaiheen avulla:

1. Muodosta yhteys [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen Exchange Onlinen avulla Office 365 -tilauksessa. Exchange Online käsittelee sähköpostiviestisi. Tämä on helppo tehdä asetusten ohjatun määrityksen oppaan avulla. Tarvitset vain järjestelmänvalvojan tunnistetiedot Office 365:n järjestelmänvalvojan tiliä varten. Aloita oppaan käyttäminen siirtymällä **Asetusten ohjattu määritys** -kohtaan ja valitsemalla **Määritä sähköpostin lokiinkirjaus**. 
2. Varmista, että [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovellukseen on määritetty oikeat sähköpostiosoitteet myyjille ja yhteyshenkilöille sen mukaan, ovatko he potentiaalisia vai olemassa olevia asiakkaita. Tee tämä avaamalla kunkin asiakkaan tai myyjän **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortti ja tarkistamalla **Sähköposti**-kenttä.

> [!Tip]
> Kun olet tehnyt nämä oppaan vaiheet, voit tarkistaa yhteyden tilan. Siirry **Kontaktienhallinnan asetukset** -kohtaan, valitse **Prosessi** ja valitse sitten **Toiminnot**. Valitse lopuksi **Tarkista sähköpostin lokiinkirjauksen asetukset**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Sähköpostiviestien tarkasteleminen vuorovaikutuslokissa
[!INCLUDE[d365fin](includes/d365fin_md.md)] luo **Vuorovaikutusloki**-sivulle tapahtuman aina, kun myyjä ja yhteyshenkilö lähettävät sähköpostiviestejä. Voit tarkastella vuorovaikutuslokia avaamalla **Yhteyshenkilö**- tai **Myyjä/ostaja**-kortin ja valitsemalla sitten **Siirry**-, **Historia**- ja **Vuorovaikutuslokin tapahtumat**-kohdat. Lokin tapahtumille voi tehdä esimerkiksi seuraavia toimintoja:

* Voit tarkastella sähköpostiviestin sisältöä valitsemalla **Näytä liitteet** -toiminnon.
* Voit muuttaa sähköpostiviestinnän myyntimahdollisuudeksi. Jos tapahtuma näyttää lupaavalta, voit muuttaa sen mahdollisuudeksi, jonka jälkeen siitä voi kehittyä myyntiä. Valitse ensin tapahtuma ja valitse sitten **Luo mahdollisuus**-toiminto. Lisätietoja on kohdassa [Myyntimahdollisuuksien hallinta](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Katso myös
[Kontaktienhallinta](marketing-relationship-management.md)

