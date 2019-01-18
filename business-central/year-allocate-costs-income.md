---
title: "Kustannusten ja tulojen kohdistustehtävien yleiskatsaus | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan tehtävistä, joilla voi kohdistaa yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 0c761db3f76d1fff05dd75a08a586f52386b5b88
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="allocate-costs-and-income"></a>Kohdista kustannukset ja tulot
Voit kohdistaa yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä. Kohdistamisen voi tehdä kolmella eri tavalla:

* määrä
* prosenttiosuus (%)
* Summa

Kohdistustoimintoja voi käyttää toistuvien yleisten päiväkirjojen ja käyttöomaisuuspäiväkirjojen kanssa.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Seuraavaksi kerrotaan, miten kustannusten kohdistus valmistellaan toistuvissa yleisessä päiväkirjassa määrittämällä kohdistusavaimet. Kun kohdistusavaimet on määritetty, voit suorittaa ja kirjata päiväkirjan muiden toistuvien yleisten päiväkirjojen tavoin. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).

## <a name="to-set-up-allocation-keys"></a>Kohdistusavaimien määrittäminen
Voit kohdistaa toistuvan yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä. Kohdistus voidaan tehdä määrän, prosentin tai summan mukaan.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toistuva yleinen päiväkirja** ja valitse sitten liittyvä linkki.
2. Valitse **Erän nimi** -kenttä, kun haluat avata **Yleisen päiväkirjan erät** -sivun.
3. Voit muokata luettelon olemassa olevan erän kohdistuksia tai luoda uuden erän ja kohdistukset.
   * Luo uusi erä valitsemalla **Uusi**-toiminto ja siirtymällä seuraavaan vaiheeseen.
   * Voit muuttaa olemassa olevan päiväkirjan kohdistuksia valitsemalla päiväkirjan ja siirtymällä vaiheeseen 7.    
4. Syötä **Nimi**-kenttään erän nimi, esimerkiksi SIIVOUS. Syötä **Kuvaus**-kenttään kuvaus, esimerkiksi Siivouskulujen päiväkirja.
5. Kun olet valmis, sulje sivu. Esiin tulee uusi tyhjä toistuva kirjaus.
6. Täytä rivin kentät.
7. Valitse **Kohdistukset**-toiminto.
8. Lisää rivi jokaista kohdistusta varten. Sinun täytyy täyttää jokin seuraavista kentistä: **Kohdistus- %**, **Kohdistettava määrä** tai **Summa**. Sinun tulee myös täyttää **Tilinro**-kenttä ja, mikäli kohdistat tapahtuman globaaleille dimensioille, globaali dimensio -kentät.
9. Jos syötät riville prosentin, ohjelma laskee **Summa**-kentän arvon automaattisesti. Näillä summilla on vastakkainen merkki kuin kokonaissummalla toistuvan kirjauksen **Summa**-kentässä.
10. Kun olet syöttänyt kohdistusrivit, valitse **OK** palataksesi takaisin **Toistuva yleinen päiväkirja** -sivulle. **Kohdistettu summa (USD)** -kenttä on täytetty ja vastaa **Summa** -kenttää.
11. Kirjaa päiväkirja.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Aiemmin määritetyn kohdistusavaimen muuttaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Toistuva yleinen päiväkirja** ja valitse sitten liittyvä linkki.
2. Valitse **Toistuva yleinen päiväkirja** -sivulla päiväkirja, jossa kohdistus on.
3. Valitse ensin kohdistuksen rivi ja sitten **Kohdistukset**-toiminto.
4. Vaihda soveltuvat kentät ja valitse sitten **OK**-painike.

## <a name="see-also"></a>Katso myös
[Vuosien ja jaksojen sulkeminen](year-close-years-periods.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)    
[Asiakirjojen ja päiväkirjojen kirjaaminen](ui-post-documents-journals.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

