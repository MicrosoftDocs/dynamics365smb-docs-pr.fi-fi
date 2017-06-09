---
title: 'Toimintaohje: Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen| Microsoft Docs'
description: 'Ohjeet: Korjaa tai peruuta maksamattomat myyntilaskut'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9289aeb9b44ec300646fbe6e6fdbf77e72cd7b08
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-correct-or-cancel-unpaid-sales-invoices"></a>Ohjeet: Korjaa tai peruuta maksamattomat myyntilaskut
Voit korjata tai peruuttaa maksamattoman myyntilaskun. Tästä on hyötyä, jos teet virheen tai jos asiakas pyytää muutosta.

**Huomautus**: Kun kirjattu myyntilasku on osittain tai kokonaan maksettu, et voi korjata tai peruuttaa sitä itse kirjatusta myyntilaskusta. Sen sijaan sinun on luotava manuaalisesti myyntihyvityslasku, jolla myynti mitätöidään, ja asiakas hyvitetään. Lisätietoja on kohdassa [Toimintaohje: Myyntipalautusten tai -peruutusten käsitteleminen](sales-how-process-sales-returns-cancellations.md).

Voit valita **Kirjattu myyntilasku** -ikkunassa **Korjaa** - tai **Peruuta**-toiminnon suorittaaksesi toimintoja, jotka on kuvattu seuraavassa taulukossa.

| Toiminto | Kuvaus |
| --- | --- |
| **Korjaa** |Kirjattu myyntilaskun peruutetaan. Luodaan uusi myyntilasku, jossa on samat tiedot. Voit suorittaa korjauksen ja jatkaa sitten myyntiprosessia. Uudella myyntilaskulla on eri numero kuin alkuperäisellä myyntilaskulla. Korjaavat myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku. Alkuperäisen kirjatun myyntilaskun Peruutettu- ja Maksettu-valintaruudut ovat valittuina. |
| **Peruuta** |Kirjattu myyntilaskun peruutetaan. Korjaavat myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku. Alkuperäisen kirjatun myyntilaskun Peruutettu- ja Maksettu-valintaruudut ovat valittuina. |

Kun korjaat tai peruutat kirjatun myyntilaskun, korjaavaa myyntihyvityslaskua käytetään kaikkiin pääkirjanpidon ja varastotapahtumiin, jotka luotiin, kun alkuperäinen myyntilasku kirjattiin. Tämä kumoaa kirjatun myyntilaskun kirjanpitotietueissa ja jättää korjaavan kirjatun myyntihyvityslaskun kirjausketjua varten.

## <a name="to-correct-a-posted-sales-invoice"></a>Kirjatun myyntilaskun korjaaminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Kirjatut myyntilaskut** ja valitse sitten liittyvä linkki.  
2. Valitse kirjattu myyntilasku, jonka haluat korjata.

    **Huomautus**: Jos **Peruutettu**-valintaruutu on valittuna, et voi korjata kirjattua myyntilaskua, koska se on jo korjattu tai peruutettu.
3. Valitse **Kirjattu myyntilasku** -ikkunassa **Korjaa**-toiminto.  
4. Luodaan samoilla tiedoilla uusi myyntilasku, johon voit tehdä korjauksen. Alkuperäisen kirjatun myyntilaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.

    Korjaava myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku.
5. Valitse **Näytä korjaava hyvityslasku** -toiminto, kun haluat tarkastella kirjattua myyntihyvityslaskua, joka mitätöi alkuperäisen kirjatun myyntilaskun.

## <a name="to-cancel-a-posted-sales-invoice"></a>Kirjatun myyntilaskun peruuttaminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Kirjatut myyntilaskut** ja valitse sitten liittyvä linkki.  
2. Valitse kirjattu myyntilasku, jonka haluat peruuttaa.

    **Huomautus**: Jos **Peruutettu**-valintaruutu on valittuna, et voi peruuttaa kirjattua myyntilaskua, koska se on jo peruutettu tai korjattu.
3. Valitse **Kirjattu myyntilasku** -ikkunassa **Peruuta**-toiminto.

    Korjaava myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku. Alkuperäisen kirjatun myyntilaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.
4. Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua myyntihyvityslaskua, joka mitätöi alkuperäisen kirjatun myyntilaskun.

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Toimintaohje: Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

