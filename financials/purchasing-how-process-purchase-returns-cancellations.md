---
title: "Palautusten tai peruutusten käsittely ostohyvityslaskujen avulla | Microsoft Docs"
description: "Tässä ohjeaiheessa kerrotaan, miten ostohyvityslasku luodaan kirjataan, kun haluat palauttaa nimikkeitä toimittajalle tai peruuttaa ostetut palvelut."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 887add30a1ec72b7de961e03161bfc34826980fc
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-process-purchase-returns-or-cancellations"></a>Toimintaohje: tavaran palautuksen tai peruutuksen käsittely
Jos haluat palauttaa nimikkeitä toimittajalle tai peruuttaa ostamiasi palveluita, voit luoda ja kirjata ostohyvityslaskun, joka määrittää pyydetyn muutoksen alkuperäisen ostolaskun suhteen. Voit lisätä oikean ostolaskun tiedot luomalla ostohyvityslaskun kirjatusta ostolaskusta tai käyttämällä kopiointitoimintoa.

> [!NOTE]  
>   Jos kirjattua ostolaskua ei ole vielä maksettu, voit käyttää kirjatussa ostolaskussa olevia **Korjaa**- tai **Peruuta**-toimintoja kääntääksesi automaattisesti mukana olevat tapahtumat. Nämä toiminnot toimivat vain maksamattomille laskuille eivätkä ne osittaisia palautuksia tai peruutuksia. Lisätietoja on kohdassa [Toimintaohje: Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Yleensä toimittajan lähettämän hyvityslaskun jälkeen luodaan ostohyvityslasku. Ostohyvityslasku toimii sisäisenä asiakirjana hyvityslaskuprosessissa kirjanpitotarkoituksessa.

Muutokset voivat liittyä alkuperäisen ostolaskun kaikkiin tuotteisiin tai vain joihinkin tuotteisiin. Näin ollen voit palauttaa osittain vastaanotetut nimikkeet tai vaatia vastaanotettujen palvelujen osittaista korvaamista. Tässä tapauksessa sinun täytyy muokata kopioituja ostolaskun tietoja.

Alkuperäisen kirjatun ostolaskun lisäksi voit kohdistaa ostohyvityslaskun muihin ostolaskuihin, kuten esimerkiksi toiseen kirjattuun ostolaskuun, koska olet palauttamassa tämän laskun kanssa toimitettuja nimikkeitä.

Hyvityslaskun kirjaaminen palauttaa myös mahdolliset kirjattuun asiakirjaan määritetyt nimikekulut, joten nimikkeen arvotapahtumat ovat samat kuin ennen nimikekulun määrittämistä.

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Ostohyvityslaskun luominen kirjatusta ostolaskusta
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kirjatut ostolaskut** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Kirjatut ostolaskut** -ikkunassa kirjattu ostolasku, jonka haluat peruuttaa, ja valitse sitten **Luo korjaava hyvityslasku** -toiminto.

    Useimpiin ostohyvityslaskun otsikon kenttiin täytetään kirjatun ostolaskun tiedot. Voit muokata kaikkia kenttiä, kuten esimerkiksi palautussopimusta vastaavia uusia tietoja.
3. Muokkaa sopimuksen mukaan rivien tietoja, kuten palautettujen nimikkeiden määrää tai hyvitettävää summaa.
4. Valitse **Kohdista tapahtumat** -toiminto.
5. Valitse **Kohdista toimittajatapaht.** -ikkunassa rivi, joka sisältää ostohyvityslaskuun kohdistettavan kirjatun ostoasiakirjan. Valitse sitten **Kohdistetaan tunnisteeseen** -toiminto. Ostohyvityslaskun numero lisätään **Kohdistetaan tunnisteeseen** -kenttään.
6. Syötä **Kohdistettava summa** -kenttään kohdistettava summa, jos se on pienempi kuin alkuperäinen summa.

    **Kohdista toimittajatapaht.** -ikkunan alaosassa näkyy kokonaissumma, joka kohdistetaan kaikkien mukaan kuuluvien tapahtumien peruuttamiseksi, kun **Saldo**-kentän arvo on nolla.
7. Valitse **OK**-painike. Kun ostohyvityslasku kirjataan, se kohdistetaan määritettyihin kirjattuihin ostoasiakirjoihin.

    Kun olet luonut tarvittavat ostohyvityslaskun rivit tai muokannut niitä ja yksi tai useita sovelluksia on määritetty, voit siirtyä kirjaamaan ostohyvityslaskun.
8. Valitse **Kirjaa**-toiminto.

Tiliöidyt ostolaskut, joita käytät hyvityslaskuun, on nyt kumottu. Jos olet jo maksanut alkuperäisen laskun, toimittajan pitäisi nyt hyvittää maksu sinulle. Jos hyvityslasku on vain osalle alkuperäisen laskun tuotetta, voit maksaa vain alkuperäisen ostolaskun jäljellä olevan summan sen sulkemiseksi.

Ostohyvityslasku poistetaan ja korvataan uudella kirjattujen ostohyvityslaskujen luettelon asiakirjalla.

## <a name="to-create-a-purchase-credit-memo-from-scratch"></a>Uuden ostohyvityslaskun luominen alusta alkaen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostohyvityslaskut** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa uusi tyhjä ostohyvityslasku valitsemalla **Uusi**-toiminto.
3. Syötä **Toimittaja**-kenttään nykyisen toimittajan nimi.
4. Valitse **Kopioi asiakirja** -toiminto.
5. Valitse **Kopioi ostoasiakirja** -ikkunan **Asiakirjan tyyppi** -kentässä **Kirjattu lasku**.
6. Valitse **Asiakirjan nro** -kenttä, jos haluat avata **Kirjatut ostolaskut** -ikkunan, ja valitse sitten peruutettavat rivit sisältävä kirjattu ostolasku.
7. Valitse **Laske rivit uudelleen** -valintaruutu, jos haluat päivittää kopioidut kirjatut ostolaskurivit nimikkeen hinta- ja yksikkökustannusten muutoksilla, jotka ovat tapahtuneet laskun kirjaamisen jälkeen.
8. Valitse **OK**-painike. Kopioidut laskurivit lisätään ostohyvityslaskuun.
9. Täytä ostohyvityslasku tämän ohjeaiheen "Ostohyvityslaskun luominen kirjatusta ostolaskusta" -osassa esitetyllä tavalla.

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Toimintaohje: Ostojen kirjaus](purchasing-how-record-purchases.md)  
[Toimintaohje: Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

