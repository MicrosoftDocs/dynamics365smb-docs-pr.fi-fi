---
title: 'Toimintaohje: Palkkatapahtumien tuominen| Microsoft Docs'
description: "Artikkelissa kerrotaan, miten palkanmaksut ja liittyvät tapahtumat tuodaan palkkojen toimittajalta pääkirjanpitoon."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 03/24/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8d7ee87a80b4de2bc90086c188e5a53291c52683
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-import-payroll-transactions"></a>Toimintaohje: palkkatapahtumien tuominen
Jotta palkanmaksut ja liittyvät tapahtumat voidaan käsitellä, palkanlaskennan tarjoajan tekemät rahoitustapahtumat on tuotava ja kirjattava pääkirjanpitoon. Voit tehdä tämän tuomalla ensin palkanlaskennan tarjoajalta saadun csv-tiedoston **Yleinen päiväkirja** -ikkunaan. Linkitä sitten ulkoiset tilit palkanlaskentatiedostoon soveltuvissa KP-tileissä. Kirjaa lopuksi palkkatapahtumat tilin yhdistämisen perusteella.

**Huomautus**: Palkanlaskennan tuonnin laajennus on oltava asennettuna ja käytössä, jotta tätä toimintoa voi käyttää. Ceridian Payroll- ja Quickbooks Payroll -tiedostojen tuontilaajennuksen on asennettu valmiiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]iin. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennuksilla](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Palkanlaskentatiedoston tuominen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Yleiset päiväkirjat** ja valitse sitten liittyvä linkki.
2. Valitse kyseessä olevan yleisen päiväkirjan erän **Tuo palkkatapahtumat** -toiminto. Avustettu määritysopas aukeaa.
3. Noudata **Tuo palkkatapahtumat** -ikkunan ohjeita.

    **Vihje**: Ulkoisen palkanlaskennan tietueiden yhdistämisvaiheessa tekemäsi yhdistykset KP-tileihin säilytetään, kun samat tietueet tuodaan takaisin. Tämä toiminto säästää aikaa täyttämällä **Tilinumero** -kentän yleiseen päiväkirjaan aina, kun tuot toistuvia palkkatapahtumia.   

    Kun napsautat ohjatun määritystoiminnon **OK**-painiketta, ohjelma täyttää **yleinen päiväkirja** -ikkunan palkanlaskennan tiedoston tapahtumilla sekä asiaankuuluvat tilit **KP-tili** -kenttiin opastetussa toiminnossa tekemiesi yhdistysten mukaisesti.
4. Muokkaa tai kirjaa päiväkirjarivit samalla tavalla kuin muille pääkirjanpidon tapahtumille. Lisätietoja on kohdassa [Toimintaohje: Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).   

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in mukauttaminen laajennuksilla](ui-extensions.md)  
[Toimintaohje: Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  

