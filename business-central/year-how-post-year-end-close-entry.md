---
title: Vuositilinpäätöstapahtuman tarkasteleminen ja kirjaaminen | Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten Sulje tuloslaskelma -eräajossa määritetty päiväkirja avataan. Sen jälkeen käsitellään vuositilinpäätöstapahtuman tarkastelua ja kirjaamista.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 878079fd02a2d54ae6b878fa54c7006dee779c15
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249673"
---
# <a name="post-the-year-end-closing-entry"></a>Vuositilinpäätöstapahtuman kirjaaminen
Kun olet luonut vuositilinpäätöstapahtuman tai -tapahtumat **Sulje tuloslaskelma** -eräajolla, sinun on avattava eräajossa määrittämäsi päiväkirja sekä tarkistettava ja kirjattava tapahtumat.

## <a name="to-post-the-year-end-closing-entry"></a>Kirjaa vuositilinpäätöstapahtuma
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Yleinen päiväkirja** ja valitse sitten liittyvä linkki.
2. Valitse **Yleinen päiväkirja** -sivulla **Erän nimi** kentässä erä, joka sisältää tilinpäätöstapahtumat.
3. Tarkista tapahtumat.
4. Kirjaa päiväkirja valitsemalla **Kirjaa**-toiminto.

> [!NOTE]  
>   Jos havaitaan virhe, näyttöön tulee virhesanoma. Jos kirjaus onnistuu, järjestelmä poistaa kirjatut tapahtumat päiväkirjasta. Kirjaamisen jälkeen kullekin tuloslaskelmatilille kirjataan tapahtuma, jolloin tilin saldoksi tulee nolla ja vuoden tulos siirretään taseeseen.

## <a name="see-also"></a>Katso myös
[Kirjanpitojakson päättäminen](year-close-account-periods.md)  
[Kirjojen sulkeminen](year-close-books.md)  
[Sulje tuloslaskelma](year-close-income-statement.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
