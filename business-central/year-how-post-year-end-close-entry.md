---
title: Vuositilinpäätöstapahtuman kirjaaminen
description: Tässä ohjeaiheessa kerrotaan, miten Sulje tuloslaskelma -eräajossa määritetty päiväkirja avataan. Sen jälkeen käsitellään vuositilinpäätöstapahtuman tarkastelua ja kirjaamista.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 6dfba7323eeaad538cf45525d11212a6e5d7438e
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438525"
---
# <a name="posting-the-year-end-closing-entry"></a>Vuositilinpäätöstapahtuman kirjaaminen

Kun olet luonut vuositilinpäätöstapahtuman tai -tapahtumat **Sulje tuloslaskelma** -eräajolla, sinun on avattava eräajossa määrittämäsi päiväkirja sekä tarkistettava ja kirjattava tapahtumat.  

> [!TIP]
> Organisaation työprosesseista riippuen voit päättää, suljetaanko vai eikö suljeta kirjanpitojaksoja ja tilikausia [!INCLUDE [prod_short](includes/prod_short.md)]issa. Seuraavassa oletetaan, että tilikausi on suljettu *Kirjanpitojaksot*-valinnalla ja että tilikauden lopun tapahtuma on luotu **Sulje tuloslaskelma** -eräajon avulla, ja olet nyt valmis kirjaamaan tilikauden päättämistapahtuman yhdessä vastapääomatilitapahtumien kanssa. Organisaatio voi valita, että se toimii eri tavalla, kuten kirjata vuoden lopun sulkemistapahtuman tilikauden päättämisen osana.

## <a name="to-post-the-year-end-closing-entry"></a>Kirjaa vuositilinpäätöstapahtuma

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleinen päiväkirja** ja valitse sitten vastaava linkki.
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