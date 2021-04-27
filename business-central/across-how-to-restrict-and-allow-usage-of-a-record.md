---
title: Tietueen käytön rajoittaminen ja salliminen | Microsoft Docs
description: Jos haluat rajoittaa tietueen käyttöä tietyissä aktiviteeteissa, esimerkiksi ennen kuin tietue on hyväksytty, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbb22a00e878e8c4d75cb5fcdbcc27a28d9d22a4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783989"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Tietueen käytön rajoittaminen ja salliminen
Jos haluat rajoittaa tietueen käyttöä tietyissä aktiviteeteissa, esimerkiksi ennen kuin tietue on hyväksytty, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä. Yksi työnkulku vastaus rajoittaa tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan. Toinen työnkulku vastaus sallii tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan. Yleisessä [!INCLUDE[prod_short](includes/prod_short.md)] -versiossa on kaksi vastausta tähän tarkoitukseen: **Rajoita tietueen käyttöä** ja **Salli tietueen käyttö**.

> [!NOTE]  
>  Yleinen [!INCLUDE[prod_short](includes/prod_short.md)] -versio tarjoaa tuen tietueen rajoittamiselle kirjaamisen, viennin maksuna ja tulostamisen sekkinä osalta. Muita rajoituksia saadaan, jos Microsoft-kumppani mukauttaa sovelluksen koodin.  

> [!NOTE]  
>  Työnkulun toiminnallisuus rajoittaa ja sallia tietueita käytettäväksi työnkulun toimintoihin ei liity toiminnallisuuteen estää nimike, asiakas ja toimittajatietueiden kirjaaminen.

Seuraavassa kuvataan, miten rajoittaa ostotilausten kirjaamisen ennen kuin ne on hyväksytty. Uusi työnkulku perustuu Ostolaskun hyväksymistyönkulku -työnkulkumalliin.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Voit seuraavasti luoda työnkulun vaiheen, joka rajoittaa hyväksymättömiä ostotilausten kirjaus  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvake, syötä **Työnkulut** ja valitse sitten liittyvä linkki.  
2. Luo **Työnkulut**-sivulla uusi työnkulku nimeltä Ostotilauksen hyväksymistyönkulku. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).  
3. Valitse **Kopioi työnkulun mallista** -toiminto.  
4. Valita **Lähdetyönkulun koodi** -kenttä ja sitten **Työnkulkumallit**-sivulla valitse Ostolaskun hyväksymistyönkulku -työnkulkumalli.  

     Huomaa, että kaksi ensimmäistä työnkulun vaiheet ovat rajoittaminen ja sitten salliminen ostolaskujen käyttö. Siirry muuttamaan uuden työnkulun ensimmäisen vaiheen tapahtumaehtoa niin, että se koskee ostotilauksia.  
5. Valitse **Työnkulun vaiheet** -pikavälilehdessä **Tapahtuman ehdot** -kenttä ja valitse sitten **Asiakirjan tyyppi** -suodattimeksi **Tilaus**.  
6. Siirry muokkaamaan, poistamaan tai lisäämään muita työnkulun vaiheita sovittaaksesi liiketoiminnan prosessi, joka alkaa rajoittamalla hyväksymättömien ostotilausten kirjaaminen.  

## <a name="see-also"></a>Katso myös  
[Työnkulkujen luominen](across-how-to-create-workflows.md)   
[Työnkulku](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]