---
title: Projektin ostonimikkeiden tai palvelujen ostaminen ja tarvikkeiden hallinta| Microsoft Docs
description: "Ohjeaiheessa kerrotaan, miten tarvikkeita hallitaan sekä projekteille ostetaan materiaaleja ja palveluja."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 46cae53022ba5d65a370694c9818f52a7bf45525
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-job-supplies"></a>Toimintaohje: Projektin tarvikkeiden hallinta
Projektin nimikkeiden, palveluiden ja kulujen tarvikkeiden hallinta on olennainen ja tärkeä osa kaikkia projekteja. Voit käyttää varastomääriä tai tehdä projektikohtaisia ostoja ostotilausten tai ostolaskujen avulla. Oletetaan esimerkiksi, että tietokoneen huoltoprojektia varten tarvitaan uusi levy. Tällöin luot ostolaskun uuden levyn ostamista varten ja kirjaat projektin, jossa sitä käytetään.

Jos ostoprosessi ei edellytä, että fyysinen tapahtuma kirjataan erikseen, osto voidaan käsitellä vain ostolaskussa tai **Projektin KP-päiväkirja** -ikkunassa. Lisätietoja on kohdassa [Toimintaohje: Projektien käytön kirjaaminen](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Nimikkeiden tai palveluiden ostaminen projektille
Seuraavassa kerrotaan, miten projektille ostetaan tuotteita ostolaskun avulla. Samat vaiheet toimivat myös silloin, kun käytetään ostotilausta.  

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Ostolaskut** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto ja täytä tarvittavat kentät. Lisätietoja on kohdassa [Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md).
3. Valitse **Projektinro**- ja **Projektitehtävän nro** -kentissä sen projektin tiedot, jolle haluat ostaa nimikkeitä tai huoltoja. Käytä **Valitse sarakkeita** -toiminto, jos kenttä ei ole näkyvissä. Lisätietoja on kohdassa [Käyttäjän mukautus](ui-user-personalization.md).

    **Projektin rivityyppi** -kentässä valitsemasi arvo määrittää, luodaanko suunnittelurivi nimikkeen käytön kirjaamisen yhteydessä. Jos kentän arvo on **Laskutettava**, ne projektin suunnittelurivit, jotka ovat valmiita asiakkaalta laskutettaviksi, luodaan. Lisätietoja on kohdassa [Toimintaohje: Projektien laskuttaminen](projects-how-invoice-jobs.md).
4. Valitse **Kirjaa**-toiminto.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>Projektin ostojen arvon tarkasteleminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa sopiva projektikortti.

    **Tehtävät**-pikavälilehden **Avoimet tilaukset** -kentässä näkyy projektin tehtävärivin ostoasiakirjojen varastonimikkeiden ja palveluiden avoin summa paikallisena valuuttana.  

    **Ei laskut. vast.ottojen summa** -kentässä näkyy ostoasiakirjoja vastaan toimitettujen, mutta vielä laskuttamattomien, nimikkeiden arvo.  
3. Valitse jompikumpi kentistä ja avaa **Ostorivit**-ikkuna, jossa voit tarkastella liittyvien ostoasiakirjarivien tietoja sekä tietoa siitä, mitkä nimikkeet tai palvelut on vastaanotettu.

## <a name="to-post-a-job-related-expense"></a>Projektiin liittyvän kulun kirjaaminen
Jos sisällytät satunnaisen tai kertaluontoisen projektin kulut, voit käyttää **Projektin KP-päiväkirja** -ikkunaa ja kirjata ne suoraan asianmukaiseen projektitiliin.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektin KP-päiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.  
2. Luo uusi rivi ja anna kulua koskevat tiedot, esimerkiksi **Projektinro**- ja **Projektitehtävän nro** -kenttien tiedot.  
3. Kun päiväkirja on valmis, valitse **Kirjaa**-toiminto.

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)      
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

