---
title: Kirjatun myyntilaskun korjaaminen tai peruuttaminen | Microsoft Docs
description: Ohjeaiheessa käsitellään, miten kirjattu myyntilasku korjataan, kumotaan tai peruutetaan ja miten myyntihyvityslasku kohdistetaan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: a74dcd8e2d0409ca7385ea8a47a78dd9a74561b6
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796070"
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen
Voit korjata tai peruuttaa maksamattoman myyntilaskun. Tästä on hyötyä, jos teet virheen tai jos asiakas pyytää muutosta.

> [!NOTE]  
>   Kun kirjattu myyntilasku on osittain tai kokonaan maksettu, et voi korjata tai peruuttaa sitä itse kirjatusta myyntilaskusta. Sen sijaan sinun on luotava manuaalisesti myyntihyvityslasku, jolla myynti mitätöidään ja asiakas hyvitetään. Sitä voi haluttaessa hallita myyntipalautustilauksella. Lisätietoja on kohdassa [Myyntipalautusten tai -peruutusten käsitteleminen](sales-how-process-sales-returns-cancellations.md).

Voit valita **Kirjattu myyntilasku** -sivulla **Korjaa** - tai **Peruuta**-toiminnon suorittaaksesi toimintoja, jotka on kuvattu seuraavassa taulukossa.

| Toiminto | Kuvaus |
| --- | --- |
| **Korjaa** |Kirjattu myyntilaskun peruutetaan. Luodaan uusi myyntilasku, jossa on samat tiedot. Voit suorittaa korjauksen ja jatkaa sitten myyntiprosessia. Uudella myyntilaskulla on eri numero kuin alkuperäisellä myyntilaskulla. Korjaavat myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku. Alkuperäisen kirjatun myyntilaskun Peruutettu- ja Maksettu-valintaruudut ovat valittuina. |
| **Peruuta** |Kirjattu myyntilaskun peruutetaan. Korjaavat myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku. Alkuperäisen kirjatun myyntilaskun Peruutettu- ja Maksettu-valintaruudut ovat valittuina. |

Kun korjaat tai peruutat kirjatun myyntilaskun, korjaavaa myyntihyvityslaskua käytetään kaikkiin pääkirjanpidon ja varastotapahtumiin, jotka luotiin, kun alkuperäinen myyntilasku kirjattiin. Tämä kumoaa kirjatun myyntilaskun kirjanpitotietueissa ja jättää korjaavan kirjatun myyntihyvityslaskun kirjausketjua varten.

## <a name="to-correct-a-posted-sales-invoice"></a>Kirjatun myyntilaskun korjaaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntilaskut** ja valitse sitten liittyvä linkki.  
2. Valitse kirjattu myyntilasku, jonka haluat korjata.

    > [!NOTE]  
    >   Jos **Peruutettu**-valintaruutu on valittuna, et voi korjata kirjattua myyntilaskua, koska se on jo korjattu tai peruutettu.
3. Valitse **Kirjattu myyntilasku** -sivulla **Korjaa**-toiminto.  
4. Luodaan samoilla tiedoilla uusi myyntilasku, johon voit tehdä korjauksen. Alkuperäisen kirjatun myyntilaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.

    Korjaava myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku.
5. Valitse **Näytä korjaava hyvityslasku** -toiminto, kun haluat tarkastella kirjattua myyntihyvityslaskua, joka mitätöi alkuperäisen kirjatun myyntilaskun.

## <a name="to-cancel-a-posted-sales-invoice"></a>Kirjatun myyntilaskun peruuttaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntilaskut** ja valitse sitten liittyvä linkki.  
2. Valitse kirjattu myyntilasku, jonka haluat peruuttaa.

    > [!NOTE]  
    >   Jos **Peruutettu**-valintaruutu on valittuna, et voi peruuttaa kirjattua myyntilaskua, koska se on jo peruutettu tai korjattu.
3. Valitse **Kirjattu myyntilasku** -sivulla **Peruuta**-toiminto.

    Korjaava myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku. Alkuperäisen kirjatun myyntilaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.
4. Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua myyntihyvityslaskua, joka mitätöi alkuperäisen kirjatun myyntilaskun.

## <a name="see-also"></a>Katso myös
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
