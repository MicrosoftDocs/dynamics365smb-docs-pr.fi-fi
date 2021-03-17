---
title: Vuositilinpäätöstapahtuman kirjaaminen
description: Tässä ohjeaiheessa kerrotaan, miten Sulje tuloslaskelma -eräajossa määritetty päiväkirja avataan. Sen jälkeen käsitellään vuositilinpäätöstapahtuman tarkastelua ja kirjaamista.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 02/23/2021
ms.author: edupont
ms.openlocfilehash: 728a3edc1ef2200d4f28130cad6653d6b26a5b3b
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493351"
---
# <a name="post-the-year-end-closing-entry"></a>Vuositilinpäätöstapahtuman kirjaaminen

Kun olet luonut vuositilinpäätöstapahtuman tai -tapahtumat **Sulje tuloslaskelma** -eräajolla, sinun on avattava eräajossa määrittämäsi päiväkirja sekä tarkistettava ja kirjattava tapahtumat.  

> [!TIP]
> Organisaation työprosesseista riippuen voit päättää, suljetaanko vai eikö suljeta kirjanpitojaksoja ja tilikausia [!INCLUDE [prod_short](includes/prod_short.md)]issa. Seuraavassa oletetaan, että tilikausi on suljettu *Kirjanpitojaksot*-valinnalla ja että tilikauden lopun tapahtuma on luotu **Sulje tuloslaskelma** -eräajon avulla, ja olet nyt valmis kirjaamaan tilikauden päättämistapahtuman yhdessä vastapääomatilitapahtumien kanssa. Organisaatio voi valita, että se toimii eri tavalla, kuten kirjata vuoden lopun sulkemistapahtuman tilikauden päättämisen osana.

## <a name="to-post-the-year-end-closing-entry"></a>Kirjaa vuositilinpäätöstapahtuma

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.
2. Valitse **Yleinen päiväkirja** -sivulla **Erän nimi** kentässä erä, joka sisältää tilinpäätöstapahtumat.
3. Tarkista tapahtumat.
4. Kirjaa päiväkirja valitsemalla **Kirjaa**-toiminto.

> [!NOTE]  
> Jos havaitaan virhe, näyttöön tulee virhesanoma. Jos kirjaus onnistuu, järjestelmä poistaa kirjatut tapahtumat päiväkirjasta. Kirjaamisen jälkeen kullekin tuloslaskelmatilille kirjataan tapahtuma, jolloin tilin saldoksi tulee nolla ja vuoden tulos siirretään taseeseen.

## <a name="see-also"></a>Katso myös

[Kirjanpitojakson päättäminen](year-close-account-periods.md)  
[Kirjojen sulkeminen](year-close-books.md)  
[Sulje tuloslaskelma](year-close-income-statement.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]