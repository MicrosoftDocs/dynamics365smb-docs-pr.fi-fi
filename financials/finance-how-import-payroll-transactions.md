---
title: Palkkatapahtumien tuominen| Microsoft Docs
description: "Voit hallita palkkoja tuomalla ja kirjaamalla taloustapahtumia palkka-aineiston toimittajalta pääkirjanpitoon palkanlaskennan laajennusta, kuten Ceridian tai Quickbooks."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d53dfb26a3fea663e68a3b558579a59184e9de26
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-import-payroll-transactions"></a>Toimintaohje: palkkatapahtumien tuominen
Jotta palkanmaksut ja liittyvät tapahtumat voidaan käsitellä, palkanlaskennan tarjoajan tekemät rahoitustapahtumat on tuotava ja kirjattava pääkirjanpitoon. Voit tehdä tämän tuomalla ensin palkanlaskennan tarjoajalta saadun csv-tiedoston **Yleinen päiväkirja** -ikkunaan. Linkitä sitten ulkoiset tilit palkanlaskentatiedostoon soveltuvissa KP-tileissä. Kirjaa lopuksi palkkatapahtumat tilin yhdistämisen perusteella.

> [!NOTE]  
>   Palkanlaskennan tuonnin laajennus on oltava asennettuna ja käytössä, jotta tätä toimintoa voi käyttää. Ceridian Payroll- ja Quickbooks Payroll -tiedostojen tuontilaajennuksen on asennettu valmiiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Palkanlaskentatiedoston tuominen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse kyseessä olevan yleisen päiväkirjan erän **Tuo palkkatapahtumat** -toiminto. Avustettu määritysopas aukeaa.
3. Noudata **Tuo palkkatapahtumat** -ikkunan ohjeita.

    > [!TIP]  
>   Ulkoisen palkanlaskennan tietueiden yhdistämisvaiheessa tekemäsi yhdistykset KP-tileihin säilytetään, kun samat tietueet tuodaan takaisin. Tämä toiminto säästää aikaa täyttämällä **Tilinumero** -kentän yleiseen päiväkirjaan aina, kun tuot toistuvia palkkatapahtumia.   

    Kun napsautat ohjatun määritystoiminnon **OK**-painiketta, ohjelma täyttää **yleinen päiväkirja** -ikkunan palkanlaskennan tiedoston tapahtumilla sekä asiaankuuluvat tilit **KP-tili** -kenttiin opastetussa toiminnossa tekemiesi yhdistysten mukaisesti.
4. Muokkaa tai kirjaa päiväkirjarivit samalla tavalla kuin muille pääkirjanpidon tapahtumille. Lisätietoja on kohdassa [Toimintaohje: Tapahtumien kirjaaminen suoraan pääkirjanpitoon](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  

