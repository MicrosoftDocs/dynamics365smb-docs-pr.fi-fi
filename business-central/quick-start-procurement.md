---
title: Hankinnan pika-aloitus (sisältää videon)
description: Opettele täyttämään ensimmäiset kriittiset kentät, jotka koskevat toimittajia Business Centralissa, jotta voit aloittaa tuotteiden ja palveluiden ostamisen.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: 26, 27, 50, 56
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 58476145830438b85e70c03958b2bf997640e2c7
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953107"
---
# <a name="procurement-quick-start"></a>Hankinnan pika-aloitus

Jotta voisit ostaa tuotteita ja palveluita, sinun täytyy ensin määrittää toimittajat. Kun tämä on tehty, voit aloittaa ostotilausten rekisteröimisen ja laskujen vastaanottamisen.  

## <a name="set-up-vendors"></a>Toimittajien määrittäminen

Seuraavassa videossa kerrotaan, miten voit määrittää toimittajan [!INCLUDE[prod_short](includes/prod_short.md)]issa.

<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

### <a name="set-up-a-new-vendor"></a>Uuden toimittajan määrittäminen

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

Lisätietoja ja muita asioita, joita voit tehdä toimittajien rekisteröimiseksi, on ohjeaiheessa [Uusien toimittajien rekisteröinti](purchasing-how-register-new-vendors.md).  

## <a name="create-new-purchase-orders"></a>Luo uusia ostotilauksia

Kun ostat jotain toimittajalta sinulla on kaksi vaihtoehtoa. Ensimmäinen ja yksinkertaisin on vain ostolaskun luominen. Ostotilauksia on kuitenkin käytettävä, jos ostoprosessi vaatii tilausmäärän osittaisten vastaanottojen tallentamisen esimerkiksi silloin, kun koko määrä ei ole kerralla toimittajan käytettävissä.

Seuraavassa videossa kerrotaan, miten voit luoda ostotilauksen [!INCLUDE[prod_short](includes/prod_short.md)]issa.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### <a name="to-create-a-purchase-order"></a>Ostotilauksen luominen  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  

2. Luo uusi ostotilaus valitsemalla **Ostotilaukset**-sivulla **Uusi**-toiminto.

3. Syötä **Toimittajan nimi**-kenttään nykyisen toimittajan nimi.

    Muut **Ostolaskun otsikko** -kohdan kentät täytetään nyt valitun toimittajan vakiotiedoilla.  

4. Täytä tarvittaessa jäljellä olevat kentät **Ostotilaus**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Voit nyt täyttää ostotilausrivit nimikkeillä tai resursseilla, joita olet ostanut toimittajalta.

5. Syötä **Rivit**-pikavälilehden **Nimikenro**-kenttään varastonimikkeen tai palvelun numero.

6. Syötä **Määrä**-kenttään ostettavien nimikkeiden lukumäärä.

    **Rivisumma**-kenttä päivitetään näyttämään arvoa, joka saadaan kertomalla **Välitön yksikkökustannus** -kentän arvo **Määrä**-kentän arvolla.

7. Syötä **Tilauksen alennussumma** -kenttään summa, joka vähennetään tilauksen alaosan **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

8. Kun vastaanotat ostettuja nimikkeitä tai palveluita, valitse **Kirjaa**.

Lisätietoja ja muita asioita, joita voit tehdä ostotilauksen luonnin yhteydessä, on kohdassa [Osto](purchasing-manage-purchasing.md).  

## <a name="create-a-purchase-invoice"></a>Luo ostolasku  

Voit luoda ostolaskun ostojen kustannusten tallentamiseksi ja ostoreskontran seuraamiseksi. Ostolaskun luominen on samanlaista kuin ostotilauksen luominen.

### <a name="how-to-create-and-post-a-purchase-invoice"></a>Ostolaskun luominen ja kirjaaminen  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.  
2. Luo uusi ostolasku valitsemalla **Ostolasku**-sivulla **Uusi**-toiminto.
3. Syötä **Toimittaja**-kenttään nykyisen toimittajan nimi.

    Muut **Ostolasku**-sivun kentät täytetään nyt valitun toimittajan vakiotiedoilla.

4. Täytä tarvittaessa jäljellä olevat kentät **Ostolasku**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Voit nyt täyttää ostolaskurivit nimikkeillä tai resursseilla, joita olet ostanut toimittajalta.

5. Syötä **Rivit**-pikavälilehden **Nimikenro**-kenttään varastonimikkeen tai palvelun numero.
6. Syötä **Määrä**-kenttään ostettavien nimikkeiden lukumäärä.

    **Rivisumma**-kenttä päivitetään näyttämään arvoa, joka saadaan kertomalla **Välitön yksikkökustannus** -kentän arvo **Määrä**-kentän arvolla.

7. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään laskun alaosan **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

8. Kun vastaanotat ostettuja nimikkeitä tai palveluita, valitse **Kirjaa**.

Osto vaikuttaa nyt varastoon, resurssitapahtumiin ja taloustietueisiin, ja myyjän maksu on aktivoitu. Ostolasku poistetaan ostolaskujen luettelosta ja korvataan uudella asiakirjalla kirjattujen ostolaskujen luettelosta.  

Lisätietoja ja muita asioita, joita voit tehdä ostolaskun luonnin yhteydessä, on kohdassa [Ostojen rekisteröiminen ostolaskuilla](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Katso myös

[Business Centralin pika-aloitus](quick-start-business-central.md)  
[Oston yleiskuvaus](Purchasing-manage-purchasing.md)  
[Ostojen kirjaaminen ostolaskujen avulla](purchasing-how-record-purchases.md)  
