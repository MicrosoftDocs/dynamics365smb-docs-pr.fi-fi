---
title: Tietueen käytön rajoittaminen ja salliminen
description: Jos haluat rajoittaa tietueen käyttöä, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7873091d64e55460986437cf255d98cd0d00b6d3
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130143"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Tietueen käytön rajoittaminen ja salliminen

Jos haluat rajoittaa tietueen käyttöä tietyissä aktiviteeteissa, esimerkiksi ennen kuin tietue on hyväksytty, voit sisällyttää kaksi työnkulun vastausta työnkulkuun, joka määrittää tietueen käyttöä. Yksi työnkulku vastaus rajoittaa tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan. Toinen työnkulku vastaus sallii tietueen käyttöä työnkulun tapahtuman ja ehtojen mukaan. Tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] oletusversiossa on kaksi vastausta tähän tarkoitukseen: **Lisää tietuerajoitus** ja **Poista tietuerajoitus**.

> [!NOTE]  
> Tuotteen [!INCLUDE[prod_short](includes/prod_short.md)] oletusversio tarjoaa tuen tietueen rajoittamiselle kirjaamisen, viennin maksuna ja tulostamisen sekkinä osalta. Muita rajoituksia saadaan, jos Microsoft-kumppani mukauttaa sovelluksen koodin.  

> [!NOTE]  
> Työnkulun toiminnallisuus rajoittaa ja sallia tietueita käytettäväksi työnkulun toimintoihin ei liity toiminnallisuuteen estää nimike, asiakas ja toimittajatietueiden kirjaaminen.

Seuraavassa kuvataan, miten rajoittaa ostotilausten kirjaamisen ennen kuin ne on hyväksytty. Uusi työnkulku perustuu Ostolaskun hyväksymistyönkulku -malliin.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Voit seuraavasti luoda työnkulun vaiheen, joka rajoittaa hyväksymättömiä ostotilausten kirjaus

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työnkulut** ja valitse sitten vastaava linkki.  
2. Valitse **Työnkulut**-sivulla **Uusi työnkulku mallista** -toiminto. Lisätietoja on kohdassa [Työnkulkujen luominen työnkulkumalleista](across-how-to-create-workflows-from-workflow-templates.md).
3. Valitse **Työnkulkumallit** sivulla *Ostolaskun hyväksymistyönkulku* -malli.  

   Huomaa, että kaksi ensimmäistä työnkulun vaiheet ovat rajoittaminen ja sitten salliminen ostolaskujen käyttö. Siirry muuttamaan uuden työnkulun ensimmäisen vaiheen tapahtumaehtoa niin, että se koskee ostotilauksia.  
4. Valitse **Työnkulun vaiheet** -pikavälilehdessä **Ehto** -kenttä ensimmäiselle vaiheelle ja valitse sitten **Asiakirjan tyyppi** -suodattimeksi **Tilaus**.  
5. Siirry muokkaamaan, poistamaan tai lisäämään muita työnkulun vaiheita sovittaaksesi liiketoiminnan prosessi, joka alkaa rajoittamalla hyväksymättömien ostotilausten kirjaaminen.  

## <a name="see-also"></a>Katso myös

[Työnkulkujen luominen](across-how-to-create-workflows.md)  
[Työnkulku](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]