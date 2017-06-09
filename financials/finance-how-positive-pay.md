---
title: 'Toimintaohje: Positive Pay -tiedostojen vieminen| Microsoft Docs'
description: "Tässä artikkelissa kerrotaan, miten voit varmistaa toimittaja- ja maksutiedot sisältävän Positive Pay -tiedoston viennin avulla, että pankki vahvistaa vain tarkistetut sekit ja summat, viemällä ."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 03/24/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ee93f8eb889ae1d635bca22ff133e1523fd1b825
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-export-a-positive-pay-file"></a>Toimintaohje: Positive Pay -tiedoston vieminen
Kun viet toimittajan tiedot, sekin numeron ja maksun summan sisältävän Positive Pay -tiedoston, jonka sitten lähetät viitetiedoiksi pankkiin maksuja käsitellessäsi, voit varmistaa, että pankki vahvistaa vain tarkistetut sekit ja summat.

[!INCLUDE[d365fin](includes/d365fin_md.md)] on määritetty tukemaan Bank of American ja City Bankin Positive Pay -tiedostoja.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Positive Pay -pankkitilin määrittäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Avaa sen pankin kortti, jossa haluat käyttää Positive Pay -toimintoa.
3. Kirjoita **Positive Pay -vientikoodi** -kenttään POSPAYBANK.
4. Sulje ikkuna.

## <a name="to-export-a-positive-pay-file"></a>Positive Pay -tiedoston vienti
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse pankkitili, johon haluat viedä Positive Pay -tiedoston.
3. Valitse **Positive Pay, vienti** -toiminto.

    **Positive Pay, vienti** -ikkuna avautuu ja näkyvissä on maksut, jotka on tehty pankkitilille edellisen latauspäivän jälkeen (**Edellinen latauspvm**- ja **Edellinen latausaika** -kentät).
4. Määrittää**Latauksen katkaisupvm** -kenttää päivämäärä, jota edeltäviä maksuja ei sisällytetä vientitiedostoon.
5. Valitse **Vie**-toiminto.
6. Valitse **Vie tiedosto** -ikkunassa **Tallenna**-painike ja tallenna tiedosto sopivaan paikkaan.
7. Lataa tiedosto sähköisen pankin sivustoon.
8. Kirjoita muistiin tai kopioi vahvistusnumero, joka näkyy, kun tiedoston lataus on onnistunut.

Vietyjen Positive Pay -tietueiden näyttäminen

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse pankkitili, jonka Positive Pay -vientitietueet haluat näyttää.
3. Valitse **Positive Pay -tapahtumat** -toiminto.

    Kaikki pankkitilin Positive Pay -vientitietueet näkyvät **Positive Pay -tapahtumat** -ikkunassa.
4. Anna kunkin vientitietueen **Vahvistusnumero**-kenttään numero, jonka sait, kun tiedoston lataus pankkiin onnistui.
5. Voit tarkastella liittyviä maksurivejä valitsemalla **Positive Pay -tapahtuman tiedot** -toiminnon.

Positive Pay -tiedostojen uudelleenvienti

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Pankkitilit** ja valitse sitten liittyvä linkki.
2. Valitse pankkitili, johon haluat viedä Positive Pay -tiedostot uudelleen.
3. Valitse **Positive Pay -tapahtumat** -toiminto.
4. Valitse uudelleenvietävä Positive Pay -vientitiedoston rivi.
5. Valitse **Positive Pay -tapahtumat** -ikkunassa **Vie Positive Pay -maksu uudelleen tiedostoon** -toiminto.

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Toimintaohje: Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

