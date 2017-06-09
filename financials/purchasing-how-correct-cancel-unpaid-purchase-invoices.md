---
title: 'Toimintaohje: Maksamattomien ostolaskujen korjaaminen tai peruuttaminen| Microsoft Docs'
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
ms.openlocfilehash: fba080da79d3a9d3f816c8ddc0a02c877211bcb4
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a>Ohjeet: Korjaa tai peruuta maksamattomat myyntilaskut
Voit korjata tai peruuttaa maksamattoman ostolaskun. Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai muuttaa ostoa tilausprosessin alkuvaiheessa.

Jos olet jo maksanut kirjatun ostolaskun tuotteet, et voi korjata tai peruuttaa sitä itse kirjatusta ostolaskusta. Sen sijaan sinun on luotava ostohyvityslasku manuaalisesti oston peruuttamiseksi. Lisätietoja on kohdassa [Toimintaohje: Ostopalautusten tai -peruutusten käsitteleminen](purchasing-how-process-purchase-returns-cancellations.md).

Valitse **Kirjattu ostolasku** -ikkunassa **Korjaa**- tai **Peruuta**-painike. Kun korjaat tai peruutat kirjatun ostolaskun, korjaavaa ostohyvityslaskua käytetään kaikkiin pääkirjanpidon ja varastotapahtumiin, jotka luotiin, kun alkuperäinen ostolasku kirjattiin. Tämä kumoaa kirjatun ostolaskun kirjanpitotietueissa ja jättää korjaavan kirjatun ostohyvityslaskun kirjausketjua varten. Alla kerrotaan, miten **Korjaa**- ja **Peruuta**-painikkeita käytetään.

## <a name="to-correct-a-posted-purchase-invoice"></a>Kirjatun ostolaskun korjaamiseksi
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Kirjatut ostolaskut** ja valitse sitten liittyvä linkki.  
2. Valitse kirjattu ostolasku, jonka haluat korjata.  

    **Huomautus**: Jos **Peruutettu**-valintaruutu on valittuna, et voi korjata kirjattua ostolaskua, koska se on jo korjattu tai peruutettu.
3. Valitse **Kirjattu ostolasku** -ikkunassa **Korjaa**.

    Luodaan samoilla tiedoilla uusi ostolasku, johon voit tehdä korjauksen. Lisätietoja on kohdassa [Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md). Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.

    Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku.
4. Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Kirjatun ostolaskun peruuttamiseksi
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Kirjatut ostolaskut** ja valitse sitten liittyvä linkki.  
2. Valitse kirjattu ostolasku, jonka haluat peruuttaa.

    **Huomautus**: Jos **Peruutettu**-valintaruutu on valittuna, et voi peruuttaa kirjattua ostolaskua, koska se on jo peruutettu tai korjattu.
3. Valitse **Kirjattu ostolasku** -ikkunassa **Peruuta**.

    Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku. Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.
4. Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Toimintaohje: Ostojen kirjaus](purchasing-how-record-purchases.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

