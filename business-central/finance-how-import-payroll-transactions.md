---
title: Palkkatapahtumien tuominen| Microsoft Docs
description: Voit hallita palkkoja tuomalla ja kirjaamalla taloustapahtumia palkka-aineiston toimittajalta pääkirjanpitoon palkanlaskennan laajennusta, kuten Ceridian tai Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2018
ms.author: SorenGP
ms.openlocfilehash: 642c35fa993b9177ec51deccaef7beb3615ab336
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795658"
---
# <a name="import-payroll-transactions"></a>Tuo palkkatapahtumat
Jotta palkanmaksut ja liittyvät tapahtumat voidaan käsitellä, palkanlaskennan tarjoajan tekemät rahoitustapahtumat on tuotava ja kirjattava pääkirjanpitoon. Voit tehdä tämän tuomalla ensin palkanlaskennan tarjoajalta saadun csv-tiedoston **Yleinen päiväkirja** -sivulle. Linkitä sitten ulkoiset tilit palkanlaskentatiedostoon soveltuvissa KP-tileissä. Kirjaa lopuksi palkkatapahtumat tilin yhdistämisen perusteella.

> [!NOTE]  
>   Palkanlaskennan tuonnin laajennus on oltava asennettuna ja käytössä, jotta tätä toimintoa voi käyttää. Ceridian Payroll- ja Quickbooks Payroll -tiedostojen tuontilaajennuksen on asennettu valmiiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Palkanlaskentatiedoston tuominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.
2. Valitse kyseessä olevan yleisen päiväkirjan erän **Tuo palkkatapahtumat** -toiminto. Avustettu määritysopas aukeaa.
3. Noudata **Tuo palkkatapahtumat** -sivun ohjeita.

    > [!TIP]  
    >   Ulkoisen palkanlaskennan tietueiden yhdistämisvaiheessa tekemäsi yhdistykset KP-tileihin säilytetään, kun samat tietueet tuodaan takaisin. Tämä säästää aikaa, sillä ei tarvitse täyttää manuaalisesti yleisen päiväkirjan **Tilinro**-kenttää aina, kun tuot toistuvia palkanlaskentatapahtumia.   

    Kun napsautat ohjatun määritystoiminnon **OK**-painiketta, ohjelma täyttää **Yleinen päiväkirja** -sivun palkanlaskennan tiedoston tapahtumilla sekä asiaankuuluvat tilit **KP-tili** -kenttiin opastetussa toiminnossa tekemiesi yhdistysten mukaisesti.
4. Muokkaa tai kirjaa päiväkirjarivit samalla tavalla kuin muille pääkirjanpidon tapahtumille. Lisätietoja on kohdassa [Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
