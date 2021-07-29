---
title: Word-mallien käyttö joukkoviestinnässä | Microsoft Docs
description: Word-mallit helpottavat tietyille entiteeteille mukautettujen asiakirjojen joukkoluontia.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 84b6a9fa74cea99f8b939edcf0cd883e39eb6937
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445970"
---
# <a name="using-word-templates-for-bulk-communication"></a>Word-mallien käyttö joukkoviestinnässä
Microsoft Word -mallit helpottavat entiteettien, kuten asiakkaiden ja toimittajien, kanssa tapahtuvaa joukkoviestintää. Voit luoda esimerkiksi esitteitä, joissa kerrotaan asiakkaille myyntikampanjoista, kirjeitä, joissa toimittajille kerrotaan uudesta ostokäytännöstä, tai kutsuja, joilla houkutellaan yhteyshenkilöitä tulevaan tapahtumaan.

> [!NOTE]
> Voit käyttää Word-malleja vain laitteissa, joissa on Microsoft Word 2019 ja Windows-käyttöjärjestelmä asennettuna.

[!INCLUDE[prod_short](includes/prod_short.md)]in entiteettejä voi käyttää mallin tietolähteinä, ja asiakirjat voidaan mukauttaa kullekin entiteetille lisäämällä yhdistämiskenttiä. Yhdistämiskentät saadaan [!INCLUDE[prod_short](includes/prod_short.md)]in entiteetistä. Kun Word-mallia käytetään entiteetissä, yhdistämiskenttien tiedot lisätään asiakirjaan.

**Word-mallit**-sivulla on asetusten ohjatun määrityksen opas, jolla voi ladata DataSource.txt-tiedoston ja entiteetin Word-mallitiedoston sisältävän ZIP-tiedoston. Kun malli on määritetty ja yhdistämiskentät lisätty, mallin voi ladata takaisin samaa opasta käyttämällä. Voit käyttää vain [!INCLUDE[prod_short](includes/prod_short.md)]ista ladattuja Word-malli- ja tietolähdetiedostoja, ja nämä tiedostot on tallennettava samaan sijaintiin.

> [!NOTE]
> Kun valitset entiteetin, jolle malli luodaan, luettelossa on näkyvissä kaikki [!INCLUDE[prod_short](includes/prod_short.md)]in entiteetit. Malleja ei kuitenkaan voi luoda kaikille entiteeteille. Jos entiteetin nimessä on erikoismerkkejä, kuten **/**, **.**, **_** tai **-**, sille ei voi luoda mallia. Entiteetin nimi näkyy **Objektin otsikko** -sarakkeessa.

Kun mallia määritetään Wordissa, yhdistämiskentät voidaan lisätä **Postitukset**-välilehdessä valitsemalla **Lisää yhdistämiskenttä**.

> [!NOTE]
> Yhdistämiskenttiä ei voi käyttää, jos kentän nimessä on vähintään 40 merkkiä. Esimerkiksi Company__Information_Customs_Permit_Date-kenttää ei voi käyttää, koska siinä on 40 merkkiä. 

Kun Word-malli on valmis, asiakirjat voidaan luoda valitsemalla **Word-mallit**-sivulla **Käytä**. Voit luoda joko yhden asiakirjan, jossa on osa kullekin entiteetille, tai jakaa toiminnon luomaan uuden asiakirjan kullekin entiteetille.

## <a name="to-create-a-word-template"></a>Word-mallin luominen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Word-mallit** ja valitse sitten vastaava linkki.
2. Noudata asetusten ohjatun määritysoppaan ohjeita. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Katso myös
[Raporttien ja asiakirjojen asettelujen hallinta](ui-manage-report-layouts.md)  
