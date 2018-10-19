---
title: Tuloslaskelmatilien sulkeminen | Microsoft Docs
description: "Vuositilinpäätöksessä on suoritettava Sulje tuloslaskelma -etätyö, jolla suljetaan tilikauden muodostavat kirjanpitojaksot."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 20bc194772d1aa0a8caadf0605911d0a214a9ab2
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="close-income-statement-accounts"></a>Tuloslaskelmatilien sulkeminen
Kun tilikausi on ohi, sinun täytyy päättää tilikauteen sisältyvät kirjanpitojaksot. Voit tehdä sen ajamalla **Sulje tuloslaskelma** -eräajon. Tämä ajo siirtää vuoden tuloksen tilille taseeseen ja sulkee tuloslaskelmatilit. Voit tehdä tämän luomalla rivejä päiväkirjaan, jonka sitten voit kirjata.

## <a name="to-run-the-close-income-statement-batch-job"></a>Sulje tuloslaskelma -eräajon ajaminen
1. Sulje tilikausi. Tilikausi täytyy sulkea ennen eräajon suorittamista. Lisätietoja on kohdassa [Kirjanpitojakson päättäminen](year-close-account-periods.md).
2. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sulje tuloslaskelma** ja valitse sitten liittyvä linkki.
3. Suorita eräajo valitsemalla **OK**.

## <a name="about-the-close-income-statement-batch-job"></a>Tietoja Sulje tuloslaskelma -eräajosta
Eräajo käsittelee kaikki Tuloslaskelma-tyyppiset kirjanpitotilit ja luo niiden saldojen vastatapahtumat. Jokainen tapahtuma on tilikauden kaikkien pääkirjanpidon tilin tapahtumien summa. Nämä uudet tapahtumat sijoitetaan päiväkirjaan, missä sinun täytyy määrittää vastatili ja jakamattoman voiton tili taseeseen ennen kirjausta. Kun päiväkirja on kirjattu, jokaiselle tuloslaskelmatilille kirjataan tapahtuma, jotta tilin saldoksi tulee nolla, ja samalla vuoden tulos siirretään taseeseen.

Sinun täytyy itse kirjata päiväkirja. Eräajo ei kirjaa niitä automaattisesti, ellei käytetä lisäraportointivaluuttaa. Lisäraportointivaluuttaa käytettäessä eräajo kirjaa tapahtumat suoraan pääkirjanpitoon.

Niillä riveillä, jotka eräajo syöttää päiväkirjan riveille, on aina tilikauden päättämispäivämäärä. Tilikauden päättämispäivä on kuvitteellinen päivä tilikauden viimeisen päivän ja seuraavan tilikauden ensimmäisen päivän välissä. Tilikauden päättämispäivän kirjauksesta on se hyöty, että oikeat saldot säilyvät tilikauden tavallisissa päivämäärissä.

**Sulje tuloslaskelma** -eräajoa voi käyttää monta kertaa. Jos suoritat eräajon uudelleen, voit kirjata edelliselle tilikaudelle vielä tuloslaskelmatilien päättämisen jälkeenkin.

## <a name="see-also"></a>Katso myös
[Kirjojen sulkeminen](year-close-books.md)  
[Vuositilinpäätöstapahtuman kirjaaminen](year-how-post-year-end-close-entry.md)  
[Uuden tilikauden avaaminen](finance-how-open-new-fiscal-year.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

