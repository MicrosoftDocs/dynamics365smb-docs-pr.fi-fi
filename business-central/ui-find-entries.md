---
title: Tapahtumien etsiminen | Microsoft Docs
description: Tässä artikkelissa kuvataan, miten asiakirjoihin ja tapahtumiin liittyvät
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5f8ddd7176e69c9d1eb3b8d8ff98c93695d50993
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771159"
---
# <a name="finding-related-entries-for-posted-documents"></a>Liittyvien tapahtumien etsiminen kirjatuista asiakirjoista 

Tässä artikkelissa opit etsimään toisiinsa liittyviä asiakirjoja ja tapahtumia yhteisten tietojen perusteella.

- Asiakirjan numero tai kirjauspäivämäärä
- Työyhteyshenkilön tyyppi, numero tai ulkoisen asiakirjan numero
- Nimikkeen sarjanumero tai eränumero

Tämä ominaisuus on hyödyllinen etsittäessä tietyistä tapahtumista syntyneitä tapahtumia. Kun etsit asiakirjan numeroiden perusteella, voit myös tulostaa yhteenvedon Asiakirjatapahtumat-raportista.

## <a name="get-started"></a>Aloitus

Etsi tapahtumat -toiminto on helposti saatavilla useimmilla sivuilla, joilla näkyvät kirjatut asiakirjat tai kirjattujen asiakirjojen tapahtumat – sekä luettelot että kortit. Joten ensimmäinen askel on avata yksi näistä sivuista. Valitse sitten **Etsi tapahtumat** -toiminto tai paina Alt+G-näppäimiä.

**Etsi tapahtumat** -sivu sisältää kaikki asiaan liittyvät asiakirjat ja tapahtumat asiakirjan nro-kentän ja kirjauspäivämäärän perusteella. Sivu jakautuu kolmeen osaan:

- Yläosassa näkyy kentät ja toiminnot, joita käytetään hakujen suodattamiseen.
- Keskimmäisessä osassa näkyvät hakuun perustuvat asiakirjat.
- Alemmassa osassa on tietoja hakuohjelman löytämästä lähdeasiakirjasta.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Hae tapahtumia

Voit hakea tapahtumia joko asiakirjan, työyhteyshenkilön tai nimikeviittauksen tietojen perusteella. Voit muuttaa hakua valitsemalla **Toiminnot**, **Etsi** ja jonkin seuraavista toiminnoista:

|Toiminto|Kuvaus|
|------|-----------|
|Hae asiakirjan mukaan|Tarkastele tapahtumia tietyn asiakirjanumeron tai kirjauspäivämäärän perusteella.|
|Liiketoiminnan kontakti |Tarkastele tapahtumia tietyn kontaktityypin, kontaktinumeron, tai ulkoisen asiakirjanumeron perusteella. Voit syöttää asiakirjaan liittyviä, toimittajalta tai asiakkaalta tulleita tietoja. Käytä saatavilla olevia kenttiä, kun haluat hakea toimittajan asiakirjoja - käyttäen niitä numeroita, jotka toimittaja on asiakirjoille antanut.|
|Nimikeviittaus|Näytä tapahtumia sarjanumeron tai eränumeron perusteella. Voit syöttää sarja- tai eränumeron tai suodattaa sarja- tai eränumeroilla, joita haluat hakea. Tämä toiminto on hyödyllinen, kun haluat nähdä, missä jonkin tietyn nimikkeen seurantanumeroa käytettiin, miltä toimittajalta se saapui tai mille asiakkaalle se myytiin.|

Kun olet tehnyt valinnan, syötä asianmukaiset hakutiedot yläreunan kenttiin. Käytä ohjeen työkaluvihjeitä. Kun olet valmis, aloita haku valitsemalla **Etsi**. Jos muutat suodattimia, sinun täytyy valita **Etsi** uudelleen.

> [!TIP]
> Pari esimerkkiä **Hae tapahtumia** -toiminnon käyttämisestä on kohdassa [Jäljitä nimike-seuratut nimikkeet](inventory-how-to-trace-item-tracked-items.md) ja [vaihekuvaus: sarja-eränumeroiden jäljittäminen](walkthrough-tracing-serial-lot-numbers.md).

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös

[Business Centralin käyttäminen](ui-work-product.md)  
[Sivutoiminnon lisääminen roolikeskukseen](ui-bookmarks.md)  
[Nimikeseurannan nimikkeiden jäljittäminen](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]