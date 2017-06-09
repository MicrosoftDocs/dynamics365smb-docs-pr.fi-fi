---
title: "Toimintaohje: Pankkivarojen siirtäminen| Microsoft Docs"
description: "Toimintaohje: Pankkivarojen siirtäminen"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 03/32/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e2e3642d08428367fac1dd5845013e14627fe6ed
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-transfer-bank-funds"></a>Toimintaohje: Pankkivarojen siirtäminen
Joskus on siirrettävä varoja yhdeltä pankkitililtä toiselle. Se tehdään kirjaamalla tapahtuma yleiseen päiväkirjaan. Tehtävä vaihtelee sen mukaan, käytetäänkö pankkitileillä samaa vai eri valuuttaa.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Siirtojen kirjaaminen pankkitileillä, jotka käyttävät samaa valuuttakoodia
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.
2. Täytä päiväkirjan rivillä **Kirjauspvm**- ja **Asiakirjan nro** -kenttä. -kentät.
3. Valitse **Tilityyppi**-kentässä **Pankkitili**.
4. Valitse **Tilinumero**-kenttään pankkitili, josta haluat siirtää varat.
5. Syötä siirrettävä summa **Summa**-kenttään.
6. Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.
7. Valitse **Vastatilin nro** -kentässä pankkitili, jolle haluat siirtää varat.
8. Kirjaa päiväkirja.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Siirtojen kirjaaminen pankkitileillä, joilla on eri valuuttakoodit
Voit siirtää varoja eri valuuttoja käyttävien pankkitilien välillä kirjaamalla kaksi yleisen päiväkirjan riviä.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.
2. Luo kaksi päiväkirjan riviä ja täytä **Kirjauspvm**- ja **Asiakirjan nro.** -kenttä. -kentät.
3. Valitse **Tyyppi**-kentän ensimmäisellä rivillä **Pankkitili**.
4. Valitse **Tilinumero**-kenttään pankkitili, josta haluat siirtää varat.
5. Syötä **Summa**-kenttään summa pankkitilin valuuttana. Anna kredit-summat miinusmerkkisinä. Anna debet-summat ilman miinusmerkkiä.
6. Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.
7. Valitse **Vastatilin nro** -kentässä pankkitili, jolle haluat siirtää varat.
8. Valitse **Tyyppi**-kentän toisella rivillä **Pankkitili**.
9. Valitse **Tilinumero**-kenttään pankkitili, jolle haluat siirtää varat.
10. Syötä **Summa**-kenttään summa pankkitilin valuuttana. Anna kredit-summat miinusmerkkisinä. Anna debet-summat ilman miinusmerkkiä.
11. Valitse **Vastatilin tyyppi** -kentässä **Pankkitili**.  
12. Valitse **Vastatilin nro** -kentässä pankkitili, josta haluat siirtää varat.

    **Huomautus**: Jos päiväkirjassa käytetyt vaihtokurssit eroavat **Valuutan vaihtokurssit** -ikkunan kursseista, syötä kolmas rivi vaihtokurssivoittoa tai -tappiota varten. Valitse **KP-tili**-kentässä**Pankkitili**. Syötä **Tilinro**-kenttään valuuttakurssivoittojen ja -tappioiden KP-tilin numero. -kentässä. Syötä valuuttakurssivoitto tai -tappio **Summa**-kenttään. Syötä summa miinusmerkin kanssa, jos kyseessä on kredit, ja ilman miinusmerkkiä, jos kyseessä on debet.
13. Kirjaa päiväkirja.

## <a name="see-also"></a>Katso myös
[Pankkitilien hallinta](bank-manage-bank-accounts.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

