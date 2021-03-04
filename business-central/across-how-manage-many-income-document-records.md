---
title: Määritä, mitkä saapuvat asiakirjat näytetään| Microsoft Docs
description: Voit muuttaa saapuvien asiakirjojen, kuten sähköisten laskujen oletusnäkymää parantaaksesi käsiteltyjen ja käsittelemättömien tietojen yleisnäkymää.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6ff52767bbd0a5661cad2dd80abb20885f3fca6d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754940"
---
# <a name="manage-many-incoming-document-records"></a>Useiden saapuvien asiakirjatietueiden hallinta
Kun luot tai käsittelet saapuvia asiakirjatietueita, **Saapuvat asiakirjat** -sivun sisältämien rivien määrä voi kasvaa niin paljon, että yleiskuvauksen tarkasteleminen ei enää ole mahdollista. Tämän vuoksi voit määrittää saapuvien asiakirjatietueiden tilaksi Käsitelty, kun haluat poistaa ne oletusnäkymästä. Kun valitset **Näytä kaikki** -toiminnon, näkyvillä ovat sekä käsitellyt että käsittelemättömät tietueet.

> [!NOTE]  
>   Et voi muokata tietoja, liittää tiedostoja tai suorittaa prosesseja niille saapuville asiakirjatietueille, joiden tilaksi on määritetty Käsitelty. Niiden tilaksi on ensin määritettävä Käsittelemätön.

**Käsitelty**-valintaruutu valitaan automaattisesti niille saapuville asiakirjatietueille, jotka on käsitelty. Valintaruudun voi valita tai valinnan voi poistaa myös manuaalisesti. Liiketoimintaprosessista riippuen saapuva asiakirjatietue voidaan käsitellä silloin, kun sille luodaan liittyvä asiakirja, tai tiedoston liittämisen yhteydessä.

> [!NOTE]  
>   Kun avaat **Saapuvat asiakirjat** -sivun, jonka Roolikeskuksessa on **Omat saapuvat asiakirjat** -toiminto, oletusarvoisesti näytetään vain käsittelemättömät saapuvat asiakirjatietueet. Sitä kutsutaan tässä ohjeaiheessa "oletusnäkymäksi".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Saapuvien asiakirjatietueiden poistaminen oletusnäkymästä
1. Valitse **Saapuvat asiakirjat** -sivulla saapuvista asiakirjatietueista vähintään yksi oletusnäkymästä poistettava rivi.
2. Valitse **Määritä tilaksi Käsitelty** -toiminto.

    Saapuvat asiakirjatietueet poistetaan oletusnäkymästä ja rivien **Käsitelty**-valintaruutu valitaan.

> [!NOTE]  
>   Voit tehdä tämän toiminnon yksittäiselle tietueelle **Saapuvan asiakirjan kortti** -sivulla.

## <a name="to-view-all-incoming-document-records"></a>Saapuvien asiakirjatietueiden tarkasteleminen
1. Valitse **Saapuvat asiakirjat** -sivulla **Näytä kaikki** -toiminto.

Näkyvissä ovat kaikki saapuvat asiakirjatietueet, eli myös ne, joiden **Käsitelty**-valintaruutua ei ole valittu.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Saapuvien asiakirjatietueiden lisääminen oletusnäkymään
1. Valitse **Saapuvat asiakirjat** -sivulla **Näytä kaikki** -toiminto.
2. Valitse saapuvista asiakirjatietueista vähintään yksi rivi, jonka haluat näkyvän oletusnäkymässä.
3. Valitse **Määritä tilaksi Käsittelemätön** -toiminto.  

> [!NOTE]  
>   Voit tehdä tämän toiminnon yksittäiselle tietueelle **Saapuvan asiakirjan kortti** -sivulla.

## <a name="see-also"></a>Katso myös
[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]