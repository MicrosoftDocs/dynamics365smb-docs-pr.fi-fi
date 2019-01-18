---
title: Maksamattomien ostolaskujen korjaaminen tai peruuttaminen | Microsoft Docs
description: "Tässä ohjeaiheessa kerrotaan, miten kirjattua lasku korjataan, peruutetaan tai kumotaan ja miten ostohyvityslasku luodaan automaattisesti."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 275b81fa2f4170208b166645a9b8778c1e6406a5
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Maksamattomien ostolaskujen korjaaminen tai peruuttaminen
Voit korjata tai peruuttaa maksamattoman ostolaskun. Tästä on hyötyä, jos haluat korjata kirjoitusvirheen tai muuttaa ostoa tilausprosessin alkuvaiheessa.

Jos olet jo maksanut kirjatun ostolaskun tuotteet, et voi korjata tai peruuttaa sitä itse kirjatusta ostolaskusta. Sen sijaan sinun on peruutettava osto luomalla ostohyvityslasku, jota voi tarvittaessa hallinta ostopalautustilauksella. Lisätietoja on kohdassa [Ostopalautusten tai -peruutusten käsitteleminen](purchasing-how-process-purchase-returns-cancellations.md).

Valitse **Kirjattu ostolasku** -sivulla **Korjaa**- tai **Peruuta**-painike. Kun korjaat tai peruutat kirjatun ostolaskun, korjaavaa ostohyvityslaskua käytetään kaikkiin pääkirjanpidon ja varastotapahtumiin, jotka luotiin, kun alkuperäinen ostolasku kirjattiin. Tämä kumoaa kirjatun ostolaskun kirjanpitotietueissa ja jättää korjaavan kirjatun ostohyvityslaskun kirjausketjua varten. Alla kerrotaan, miten **Korjaa**- ja **Peruuta**-painikkeita käytetään.

## <a name="to-correct-a-posted-purchase-invoice"></a>Kirjatun ostolaskun korjaamiseksi
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut ostolaskut** ja valitse sitten liittyvä linkki.  
2. Valitse kirjattu ostolasku, jonka haluat korjata.  

    > [!NOTE]  
    >   Jos **Peruutettu**-valintaruutu on valittuna, et voi korjata kirjattua ostolaskua, koska se on jo korjattu tai peruutettu.
3. Valitse **Kirjattu ostolasku** -sivulla **Korjaa**.

    Luodaan samoilla tiedoilla uusi ostolasku, johon voit tehdä korjauksen. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md). Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.

    Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku.
4. Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Kirjatun ostolaskun peruuttamiseksi
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut ostolaskut** ja valitse sitten liittyvä linkki.  
2. Valitse kirjattu ostolasku, jonka haluat peruuttaa.

    > [!NOTE]  
    >   Jos **Peruutettu**-valintaruutu on valittuna, et voi peruuttaa kirjattua ostolaskua, koska se on jo peruutettu tai korjattu.
3. Valitse **Kirjattu ostolasku** -sivulla **Peruuta**.

    Ostohyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu ostolasku. Alkuperäisen kirjatun ostolaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.
4. Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua ostohyvityslaskua, joka mitätöi alkuperäisen kirjatun ostolaskun.

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Ostojen kirjaus](purchasing-how-record-purchases.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

