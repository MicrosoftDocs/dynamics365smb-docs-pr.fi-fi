---
title: Tilikauden päättämistapahtuman kirjaaminen
description: 'Tässä ohjeaiheessa kerrotaan, miten Sulje tuloslaskelma -eräajossa määritetty päiväkirja avataan. Sen jälkeen käsitellään vuositilinpäätöstapahtuman tarkastelua ja kirjaamista.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: 100
ms.date: 08/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="post-the-year-end-closing-entry"></a>Tilikauden päättämistapahtuman kirjaaminen

Kun olet luonut vuositilinpäätöstapahtuman tai -tapahtumat **Sulje tuloslaskelma** -eräajolla, sinun on avattava eräajossa määrittämäsi päiväkirja sekä tarkistettava ja kirjattava tapahtumat.  

> [!TIP]
> Organisaation työprosesseista riippuen voit päättää, suljetaanko vai eikö suljeta kirjanpitojaksoja ja tilikausia [!INCLUDE [prod_short](includes/prod_short.md)]issa. Seuraavassa oletetaan, että tilikausi on suljettu *Kirjanpitojaksot*-valinnalla ja että tilikauden lopun tapahtuma on luotu **Sulje tuloslaskelma** -eräajon avulla, ja olet nyt valmis kirjaamaan tilikauden päättämistapahtuman yhdessä vastapääomatilitapahtumien kanssa. Organisaatio voi valita, että se toimii eri tavalla, kuten kirjata vuoden lopun sulkemistapahtuman tilikauden päättämisen osana.

## <a name="to-post-the-year-end-closing-entry"></a>Kirjaa vuositilinpäätöstapahtuma

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleiset päiväkirjat** ja valitse sitten vastaava linkki.
2. Valitse Yleiset **päiväkirjat** -sivun **Erän nimi** -kentässä erä, joka sisältää tilinpäätöstapahtumat.
3. Tarkista tapahtumat.
4. Kirjaa päiväkirja valitsemalla **Kirjaa**-toiminto.

> [!NOTE]  
> Jos havaitaan virhe, näyttöön tulee virhesanoma. Jos kirjaus onnistuu, järjestelmä poistaa kirjatut tapahtumat päiväkirjasta. Kirjaamisen jälkeen kullekin tuloslaskelmatilille kirjataan tapahtuma, jolloin tilin saldoksi tulee nolla ja vuoden tulos siirretään taseeseen.

## <a name="see-also"></a>Katso myös

[Kirjanpitojaksojen sulkeminen](year-close-account-periods.md)    
[Kirjojen sulkeminen](year-close-books.md)    
[Tuloslaskelman sulkeminen](year-close-income-statement.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
