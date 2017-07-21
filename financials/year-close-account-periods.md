---
title: Tilikauden kirjanpitojaksojen sulkeminen | Microsoft Docs
description: Ohjeaiheessa kerrotaan, miten tilikauden muodostavat kirjanpitojaksot suljetaan.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 859801a5e9d9b900aed6af5fe672f650932b2e79
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-close-accounting-periods"></a>Kirjanpitojakson päättäminen
Kun tilikausi on ohi, sinun täytyy päättää tilikauteen sisältyvät kirjanpitojaksot.

## <a name="to-close-accounting-periods"></a>Kirjanpitojakson päättäminen
1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Kirjanpitojaksot** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Kirjanpitojaksot**-ikkunassa **Sulje vuosi** -toiminto.

    Jos avoinna on useita tilikausia, niistä valitaan automaattisesti ensimmäinen suljettavaksi. Näyttöön tulee sanoma, jossa näkyy suljettava kausi ja jossa selostetaan sulkemisen seuraukset.
3. Sulje vuosi valitsemalla **Kyllä** -painike.

Tilikausi on päätetty, ja **Suljettu**- ja **Pvm lukittu** -kentät on valittu kaikkien kauden jaksojen osalta. Nyt tilikautta ei voi avata uudestaan, eikä valintamerkkiä voi poistaa **Suljettu**- tai **Pvm lukittu** -kentistä.

> [!NOTE]  
>   Et voi sulkea tilikautta ennen kuin luot uuden. Huomaa, että kun tilikausi on suljettu, et voi muuttaa seuraavan tilikauden aloituspäivämäärää.

Vaikka tilikausi on suljettu, voit silti kirjata tilikaudelle KP-tapahtumia. Kun teet tämän, tapahtumat merkitään kirjatuiksi suljetulle tilikaudelle ja **Edellisen vuoden tapahtuma** -kenttä valitaan.

Kun tilikausi on suljettu, tuloslaskelmatilien saldo eli tilikauden tulos tulee siirtää tasetilille. Tämä toistetaan aina, kun suljetulle tilikaudelle tehdään kirjauksia.

## <a name="see-also"></a>Katso myös
[Kirjojen sulkeminen](year-close-books.md)  
[Toimintaohje: Vuositilinpäätöstapahtuman kirjaaminen](year-how-post-year-end-close-entry.md)  
[Toimintaohje: Uuden tilikauden avaaminen](finance-how-open-new-fiscal-year.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

