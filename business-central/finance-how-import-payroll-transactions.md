---
title: Palkkatapahtumien tuominen| Microsoft Docs
description: Voit hallita palkkoja tuomalla ja kirjaamalla taloustapahtumia palkka-aineiston toimittajalta pääkirjanpitoon palkanlaskennan laajennusta, kuten Ceridian tai Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b2bd2408152cac52be5e2b22e6568600ceeb96f6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781579"
---
# <a name="import-payroll-transactions"></a>Tuo palkkatapahtumat
Jotta palkanmaksut ja liittyvät tapahtumat voidaan käsitellä, palkanlaskennan tarjoajan tekemät rahoitustapahtumat on tuotava ja kirjattava pääkirjanpitoon. Voit tehdä tämän tuomalla ensin palkanlaskennan tarjoajalta saadun csv-tiedoston **Yleinen päiväkirja** -sivulle. Linkitä sitten ulkoiset tilit palkanlaskentatiedostoon soveltuvissa KP-tileissä. Kirjaa lopuksi palkkatapahtumat tilin yhdistämisen perusteella.

> [!NOTE]  
>   Palkanlaskennan tuonnin laajennus on oltava asennettuna ja käytössä, jotta tätä toimintoa voi käyttää. Ceridian Payroll- ja Quickbooks Payroll -tiedostojen tuontilaajennuksen on asennettu valmiiksi [!INCLUDE[prod_short](includes/prod_short.md)]iin. Lisätietoja on kohdassa [[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Palkanlaskentatiedoston tuominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.
2. Valitse kyseessä olevan yleisen päiväkirjan erän **Tuo palkkatapahtumat** -toiminto. Avustettu määritysopas aukeaa.
3. Noudata **Tuo palkkatapahtumat** -sivun ohjeita.

    > [!TIP]  
    >   Ulkoisen palkanlaskennan tietueiden yhdistämisvaiheessa tekemäsi yhdistykset KP-tileihin säilytetään, kun samat tietueet tuodaan takaisin. Tämä säästää aikaa, sillä ei tarvitse täyttää manuaalisesti yleisen päiväkirjan **Tilinro**-kenttää aina, kun tuot toistuvia palkanlaskentatapahtumia.   

    Kun napsautat ohjatun määritystoiminnon **OK**-painiketta, ohjelma täyttää **Yleinen päiväkirja** -sivun palkanlaskennan tiedoston tapahtumilla sekä asiaankuuluvat tilit **KP-tili** -kenttiin opastetussa toiminnossa tekemiesi yhdistysten mukaisesti.
4. Muokkaa tai kirjaa päiväkirjarivit samalla tavalla kuin muille pääkirjanpidon tapahtumille. Lisätietoja on kohdassa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]