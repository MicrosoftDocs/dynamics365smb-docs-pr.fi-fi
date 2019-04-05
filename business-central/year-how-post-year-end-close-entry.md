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
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: cd555cc389ff7d9e306645475ef042f7ee9bc934
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796296"
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
