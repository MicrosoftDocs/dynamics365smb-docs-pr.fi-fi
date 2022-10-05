---
title: Tietueen käytön rajoittaminen ja salliminen
description: Jos haluat rajoittaa tietueen käyttöä, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/08/2022
ms.author: edupont
ms.openlocfilehash: 2542dac4eba91d0d6d7dd3c773b19e1f6fd235a5
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585970"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Tietueen käytön rajoittaminen ja salliminen

Jos haluat rajoittaa tietueen käyttöä tietyissä aktiviteeteissa, esimerkiksi ennen kuin tietue on hyväksytty, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä. Yksi työnkulku vastaus rajoittaa tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan. Toinen työnkulku vastaus sallii tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan. Tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] oletusversiossa on kaksi vastausta tähän tarkoitukseen: **Lisää tietuerajoitus** ja **Poista tietuerajoitus**.

> [!NOTE]  
> Tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] oletusversio tarjoaa tuen tietueen rajoittamiselle kirjaamisen, viennin maksuna ja tulostamisen sekkinä osalta. Muita rajoituksia saadaan, jos Microsoft-kumppani mukauttaa sovelluksen koodin.  

> [!NOTE]  
> Työnkulun toiminnallisuus rajoittaa ja sallia tietueita käytettäväksi työnkulun toimintoihin ei liity toiminnallisuuteen estää nimike, asiakas ja toimittajatietueiden kirjaaminen.

Seuraavassa kuvataan, miten rajoittaa ostotilausten kirjaamisen ennen kuin ne on hyväksytty. Uusi työnkulku perustuu *Ostolaskun hyväksymistyönkulku* -malliin.  

## <a name="create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Voit seuraavasti luoda työnkulun vaiheen, joka rajoittaa hyväksymättömien ostotilausten kirjauksia

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut**, valitse sitten vastaava linkki.  
2. Valitse **Työnkulut**-sivulla **Uusi työnkulku mallista** -toiminto. Lisätietoja kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).
3. Valitse **Työnkulkumallit** sivulla *Ostolaskun hyväksymistyönkulku* -malli.  

   Huomaa, että kaksi ensimmäistä työnkulun vaihetta ovat rajoittaminen ja sitten ostolaskujen käytön salliminen. Muuta uuden työnkulun ensimmäisen vaiheen tapahtumaehtoa niin, että se koskee ostotilauksia.  
4. Valitse **Työnkulun vaiheet** -pikavälilehdessä **Ehto** -kenttä ensimmäiselle vaiheelle, valitse sitten **Asiakirjan tyyppi** -suodattimeksi **Tilaus**.  
5. Siirry muokkaamaan, poistamaan tai lisäämään muita työnkulun vaiheita kuvataksesi liiketoiminnan prosessia, joka alkaa rajoittamalla hyväksymättömien ostotilausten kirjaamista.  

## <a name="see-also"></a>Katso myös

[Hyväksymistyönkulkujen käyttäminen](across-use-workflows.md)  
[Luo hyväksymistyönkulut](across-how-to-create-workflows.md)  
[Työnkulku](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
