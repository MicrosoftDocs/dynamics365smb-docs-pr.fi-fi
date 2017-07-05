---
title: "Toimintaohje: Myyntipalautusten tai -peruutusten käsitteleminen| Microsoft Docs"
description: "Toimintaohje: myynnin palautuksen tai peruutuksen käsittely"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: cf471e0c3a13a954ab7604a8b1d0f715f664722d
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-process-sales-returns-or-cancellations"></a>Toimintaohje: myynnin palautuksen tai peruutuksen käsittely
Jos asiakas haluaa palauttaa myymiäsi nimikkeitä tai saada hyvitystä myymiisi palveluihin, joista olet saanut maksun, täytyy luoda ja kirjata myyntihyvityslasku, joka määrittää pyydetyn muutoksen. Voit lisätä oikean myyntilaskun tiedot luomalla myyntihyvityslaskun kirjatusta myyntilaskusta tai käyttämällä kopiointitoimintoa.  

**Huomautus:** Jos kirjattua myyntilaskua ei ole vielä maksettu, voit peruuttaa tapahtumat käyttämällä kirjatun myyntilaskun **Korjaa**- tai **Peruuta**-toimintoa. Nämä toiminnot toimivat vain maksamattomille laskuille, eivätkä ne tue osittaisia palautuksia tai peruutuksia. Lisätietoja on kohdassa [Toimintaohje: Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen](sales-how-correct-cancel-sales-invoice.md).

Alkuperäisen kirjatun myyntilaskun lisäksi voit kohdistaa myyntihyvityslaskun muihin myyntilaskuihin, kuten esimerkiksi toiseen kirjattuun myyntilaskuun, koska asiakas on myös palauttamassa tämän laskun kanssa toimitettuja nimikkeitä.

Palautus tai hyvitys voi liittyä vain joihinkin alkuperäisen myyntilaskun nimikkeisiin tai palveluihin. Tällöin myyntihyvityslaskun riveillä olevia tietoja on muokattava. Myyntihyvityslaskun kirjaamisen yhteydessä myyntiasiakirjat, joihin muutos vaikuttaa, peruutetaan. Tämän jälkeen asiakkaalle voidaan luoda hyvitysmaksu.  

Voit lähettää kirjatun myyntihyvityslaskun asiakkaalle ja vahvistaa palautuksen tai peruutuksen ja kertoa, että liittyvä arvo korvataan, esimerkiksi silloin, kun nimikkeet palautetaan.  

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Myyntihyvityslaskun luominen kirjatusta myyntilaskusta
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Kirjatut myyntilaskut** ja valitse sitten liittyvä linkki.  
2. Valitse **Kirjatut myyntilaskut** -ikkunassa kirjattu myyntilasku, jonka haluat peruuttaa, ja valitse sitten **Luo korjaava hyvityslasku** -toiminto.

    Ostohyvityslaskun otsikossa on tietoja kirjatusta myyntilaskusta. Voit muokata sitä esimerkiksi palautussopimusta vastaavilla uusilla tiedoilla.  
3. Muokkaa sopimuksen mukaan rivien tietoja, kuten palautettujen nimikkeiden määrää tai hyvitettävää summaa.
4. Valitse **Kohdista tapahtumat** -toiminto.
5. Valitse **Kohdista asiakastapahtumat** -ikkunassa rivi, joka sisältää myyntihyvityslaskuun kohdistettavan kirjatun myyntiasiakirjan. Valitse sitten **Kohdistetaan tunnisteeseen** -toiminto.

    Myyntihyvityslaskun tunniste näkyy **Kohdistetaan tunnisteeseen** -kentässä.
6. Anna **Kohdistettava summa** -kenttään kohdistettava summa, jos se on pienempi kuin alkuperäinen summa.  

    **Kohdista asiakastapahtumat** -ikkunan alaosassa näkyy kokonaissumma, joka kohdistetaan kaikkien mukaan kuuluvien tapahtumien peruuttamiseksi, kun **Saldo**-kentän arvo on nolla.
7. Valitse **OK**-painike. Kun myyntihyvityslasku kirjataan, se kohdistetaan kirjattuihin myyntiasiakirjoihin.

    Kun olet luonut tai muokannut ostohyvityslaskun rivejä, ja vähintään yksi sovellusalue on määritetty, voit kirjata myyntihyvityslaskun.   
8. Valitse **Kirjaa ja lähetä** -toiminto.  

**Kirjaa ja lähettää vahvistuksen** -valintaikkuna avautuu, jossa näkyy suositeltu tapa lähettää asiakkaalle. Voit muuttaa lähetysmenetelmän valitsemalla **Lähetä asiakirja kohteeseen** -kentän valintapainikkeen. Lisätietoja on kohdassa [Toimintaohje: Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).  

Kirjatut myyntiasiakirjat, jotka kohdistettiin hyvityslaskuun, on nyt peruutettu, ja asiakkaalle voidaan luoda palautusmaksu. Myyntihyvityslasku poistetaan ja korvataan uudella kirjattujen myyntihyvityslaskujen luettelon asiakirjalla.

## <a name="to-create-a-sales-credit-memo-from-scratch"></a>Uuden myyntihyvityslaskun luominen alusta alkaen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Kirjatut myyntilaskut** ja valitse sitten liittyvä linkki.
2. Avaa uusi tyhjä myyntihyvityslasku valitsemalla **Uusi**-toiminto.
3. Syötä **Asiakas**-kenttään nykyisen asiakkaan nimi.
4. Valitse **Kopioi asiakirja** -toiminto.
5. Valitse **Kopioi myyntiasiakirja** -ikkunan **Asiakirjan tyyppi** -kentässä **Kirjattu lasku**.
6. Valitse **Asiakirjan nro** -kenttä, jos haluat avata **Kirjatut myyntilaskut** -ikkunan, ja valitse sitten peruutettavat rivit sisältävä kirjattu myyntilasku.
7. Valitse **Laske rivit uudelleen** -valintaruutu, jos haluat päivittää kopioidut kirjatut myyntilaskurivit nimikkeen hinta- ja yksikkökustannusten muutoksilla, jotka ovat tapahtuneet laskun kirjaamisen jälkeen.
8. Valitse **OK**-painike. Kopioidut laskurivit lisätään myyntihyvityslaskuun.
9. Täytä myyntihyvityslasku tämän ohjeaiheen "Myyntihyvityslaskun luominen kirjatusta myyntilaskusta" -osassa esitetyllä tavalla.

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Toimintaohje: Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)
