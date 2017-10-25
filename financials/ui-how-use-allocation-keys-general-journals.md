---
title: "Toimintaohje: Kohdistustunnusten käyttäminen yleisissä päiväkirjoissa | Microsoft Docs"
description: "Lisätietoja kohdistusavaimen käytöstä kirjauskansioissa."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bbacf9b5634d51478dd4d54ac4b587ea9bfaaf99
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-use-allocation-keys-in-general-journals"></a>Kohdistustunnusten käyttäminen yleisissä päiväkirjoissa
Voit kohdistaa yleisen päiväkirjan tapahtuman useille eri tileille päiväkirjan kirjaamisen yhteydessä. Kohdistus voidaan tehdä määrän, prosentin tai summan mukaan.

## <a name="to-set-up-allocation-keys"></a>Kohdistustunnusten määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Toistuva yleinen päiväkirja** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Erän nimi** -kenttä, kun haluat avata **Yleisen päiväkirjan erät** -ikkunan.
3. Voit muokata luettelon olemassa olevan erän kohdistuksia tai luoda uuden erän ja kohdistukset.
   * Luo uusi erä valitsemalla **Uusi**-toiminto ja siirtymällä seuraavaan vaiheeseen.
   * Voit muuttaa olemassa olevan päiväkirjan kohdistuksia valitsemalla päiväkirjan ja siirtymällä vaiheeseen 7.    
4. Syötä **Nimi**-kenttään erän nimi, esimerkiksi SIIVOUS. Syötä **Kuvaus**-kenttään kuvaus, esimerkiksi Siivouskulujen päiväkirja.
5. Kun olet valmis, sulje ikkuna. Esiin tulee uusi tyhjä toistuva kirjaus.
6. Täytä rivin kentät.
7. Valitse **Kohdistukset**-toiminto.
8. Lisää rivi jokaista kohdistusta varten. Sinun täytyy täyttää jokin seuraavista kentistä: **Kohdistus- %**, **Kohdistettava määrä** tai **Summa**. Sinun tulee myös täyttää **Tilinro**-kenttä ja, mikäli kohdistat tapahtuman globaaleille dimensioille, globaali dimensio -kentät.
9. Jos syötät riville prosentin, ohjelma laskee **Summa**-kentän arvon automaattisesti. Näillä summilla on vastakkainen merkki kuin kokonaissummalla toistuvan kirjauksen **Summa**-kentässä.
10. Kun olet syöttänyt kohdistusrivit, valitse **OK** palataksesi takaisin **Toistuva yleinen päiväkirja** -ikkunaan. **Kohdistettu summa (USD)** -kenttä on täytetty ja vastaa **Summa** -kenttää.
11. Kirjaa päiväkirja.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Aiemmin määritetyn kohdistusavaimen muuttaminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Toistuva yleinen päiväkirja** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Toistuva yleinen päiväkirja** -ikkunassa päiväkirja, jossa kohdistus on.
3. Valitse ensin kohdistuksen rivi ja sitten **Kohdistukset**-toiminto.
4. Vaihda soveltuvat kentät ja valitse sitten **OK**-painike.

## <a name="see-also"></a>Katso myös
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[Asiakirjojen ja päiväkirjojen kirjaaminen](ui-post-documents-journals.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

