---
title: 'Toimintaohje: Tuloslaskelman sulkeminen | Microsoft Docs'
description: "Tämä artikkeli sisältää tietoja tuloslaskelman sulkemisesta."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: dde7b93c6a3dcf78173494f1c6fa09a38207e676
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="close-income-statement"></a>Sulje tuloslaskelma
Kun tilikausi on ohi, sinun täytyy päättää tilikauteen sisältyvät kirjanpitojaksot. Voit tehdä sen ajamalla **Sulje tuloslaskelma** -eräajon. Tämä ajo siirtää vuoden tuloksen tilille taseeseen ja sulkee tuloslaskelmatilit. Voit tehdä tämän luomalla rivejä päiväkirjaan, jonka sitten voit kirjata.

## <a name="to-run-the-close-income-statement-batch-job"></a>Sulje tuloslaskelma -eräajon ajaminen
1. Sulje tilikausi. Tilikausi täytyy sulkea ennen eräajon suorittamista. Lisätietoja on kohdassa [Toimintaohje: Kirjanpitojakson päättäminen](year-close-account-periods.md).
2. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Sulje tuloslaskelma** ja valitse sitten liittyvä linkki.
3. Suorita eräajo valitsemalla **OK**.

## <a name="about-the-close-income-statement-batch-job"></a>Tietoja Sulje tuloslaskelma -eräajosta
Eräajo käsittelee kaikki Tuloslaskelma-tyyppiset kirjanpitotilit ja luo niiden saldojen vastatapahtumat. Jokainen tapahtuma on tilikauden kaikkien pääkirjanpidon tilin tapahtumien summa. Nämä uudet tapahtumat sijoitetaan päiväkirjaan, missä sinun täytyy määrittää vastatili ja jakamattoman voiton tili taseeseen ennen kirjausta. Kun päiväkirja on kirjattu, jokaiselle tuloslaskelmatilille kirjataan tapahtuma, jotta tilin saldoksi tulee nolla, ja samalla vuoden tulos siirretään taseeseen.

Sinun täytyy itse kirjata päiväkirja. Eräajo ei kirjaa niitä automaattisesti, ellei käytetä lisäraportointivaluuttaa. Lisäraportointivaluuttaa käytettäessä eräajo kirjaa tapahtumat suoraan pääkirjanpitoon.

Niillä riveillä, jotka eräajo syöttää päiväkirjan riveille, on aina tilikauden päättämispäivämäärä. Tilikauden päättämispäivä on kuvitteellinen päivä tilikauden viimeisen päivän ja seuraavan tilikauden ensimmäisen päivän välissä. Tilikauden päättämispäivän kirjauksesta on se hyöty, että oikeat saldot säilyvät tilikauden tavallisissa päivämäärissä.

**Sulje tuloslaskelma** -eräajoa voi käyttää monta kertaa. Jos suoritat eräajon uudelleen, voit kirjata edelliselle tilikaudelle vielä tuloslaskelmatilien päättämisen jälkeenkin.

## <a name="see-also"></a>Katso myös
[Kirjojen sulkeminen](year-close-books.md)  
[Toimintaohje: Vuositilinpäätöstapahtuman kirjaaminen](year-how-post-year-end-close-entry.md)  
[Toimintaohje: Uuden tilikauden avaaminen](finance-how-open-new-fiscal-year.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

