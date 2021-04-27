---
title: Tilikauden kirjanpitojaksojen sulkeminen | Microsoft Docs
description: Ohjeaiheessa kerrotaan, miten tilikauden muodostavat kirjanpitojaksot suljetaan.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a26baaf947fdac133e3bfcd50489d680231d9971
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786680"
---
# <a name="close-accounting-periods"></a>Kirjanpitojakson päättäminen
Kun tilikausi on ohi, sinun täytyy päättää tilikauteen sisältyvät kirjanpitojaksot.

## <a name="to-close-accounting-periods"></a>Kirjanpitojakson päättäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjanpitojaksot** ja valitse sitten liittyvä linkki.
2. Valitse **Kirjanpitojaksot**-sivulla **Sulje vuosi** -toiminto.

    Jos avoinna on useita tilikausia, niistä valitaan automaattisesti ensimmäinen suljettavaksi. Näyttöön tulee sanoma, jossa näkyy suljettava kausi ja jossa selostetaan sulkemisen seuraukset.
3. Sulje vuosi valitsemalla **Kyllä** -painike.

Tilikausi on päätetty, ja **Suljettu**- ja **Pvm lukittu** -kentät on valittu kaikkien kauden jaksojen osalta. Nyt tilikautta ei voi avata uudestaan, eikä valintamerkkiä voi poistaa **Suljettu**- tai **Pvm lukittu** -kentistä.

> [!NOTE]  
>   Et voi sulkea tilikautta ennen kuin luot uuden. Huomaa, että kun tilikausi on suljettu, et voi muuttaa seuraavan tilikauden aloituspäivämäärää.

Vaikka tilikausi on suljettu, voit silti kirjata tilikaudelle KP-tapahtumia. Kun teet tämän, tapahtumat merkitään kirjatuiksi suljetulle tilikaudelle ja **Edellisen vuoden tapahtuma** -kenttä valitaan.

Kun tilikausi on suljettu, tuloslaskelmatilien saldo eli tilikauden tulos tulee siirtää tasetilille. Tämä toistetaan aina, kun suljetulle tilikaudelle tehdään kirjauksia.

## <a name="see-also"></a>Katso myös

[Kirjojen sulkeminen](year-close-books.md)  
[Vuositilinpäätöstapahtuman kirjaaminen](year-how-post-year-end-close-entry.md)  
[Kirjanpitojaksojen ja tilikausien käyttäminen](finance-accounting-periods-and-fiscal-years.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]