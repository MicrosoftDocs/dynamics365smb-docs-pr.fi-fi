---
title: "Määritä, mitkä saapuvat asiakirjat näytetään| Microsoft Docs"
description: "Voit muuttaa saapuvien asiakirjojen, kuten sähköisten laskujen oletusnäkymää parantaaksesi käsiteltyjen ja käsittelemättömien tietojen yleisnäkymää."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4256c563edc79ebfbe1bbe9337cf1e8a7e9d9991
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-many-incoming-document-records"></a>Toimintaohje: Useiden saapuvien asiakirjatietueiden hallinta
Kun luot tai käsittelet saapuvia asiakirjatietueita, **Saapuvat asiakirjat** -ikkunan sisältämien rivien määrä voi kasvaa niin paljon, että yleiskuvauksen tarkasteleminen ei enää ole mahdollista. Tämän vuoksi voit määrittää saapuvien asiakirjatietueiden tilaksi Käsitelty, kun haluat poistaa ne oletusnäkymästä. Kun valitset **Näytä kaikki** -toiminnon, näkyvillä ovat sekä käsitellyt että käsittelemättömät tietueet.

> [!NOTE]  
>   Et voi muokata tietoja, liittää tiedostoja tai suorittaa prosesseja niille saapuville asiakirjatietueille, joiden tilaksi on määritetty Käsitelty. Niiden tilaksi on ensin määritettävä Käsittelemätön.

**Käsitelty**-valintaruutu valitaan automaattisesti niille saapuville asiakirjatietueille, jotka on käsitelty. Valintaruudun voi valita tai valinnan voi poistaa myös manuaalisesti. Liiketoimintaprosessista riippuen saapuva asiakirjatietue voidaan käsitellä silloin, kun sille luodaan liittyvä asiakirja, tai tiedoston liittämisen yhteydessä.

> [!NOTE]  
>   Kun avaat **Saapuvat asiakirjat** -ikkunan, jonka Roolikeskuksessa on **Omat saapuvat asiakirjat** -toiminto, oletusarvoisesti näytetään vain käsittelemättömät saapuvat asiakirjatietueet. Sitä kutsutaan tässä ohjeaiheessa "oletusnäkymäksi".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Saapuvien asiakirjatietueiden poistaminen oletusnäkymästä
1. Valitse **Saapuvat asiakirjat** -ikkunassa saapuvista asiakirjatietueista vähintään yksi oletusnäkymästä poistettava rivi.
2. Valitse **Määritä tilaksi Käsitelty** -toiminto.

    Saapuvat asiakirjatietueet poistetaan oletusnäkymästä ja rivien **Käsitelty**-valintaruutu valitaan.

> [!NOTE]  
>   Voit tehdä tämän toiminnon yksittäiselle tietueelle **Saapuvan asiakirjan kortti** -ikkunassa.

## <a name="to-view-all-incoming-document-records"></a>Saapuvien asiakirjatietueiden tarkasteleminen
1. Valitse **Saapuvat asiakirjat** -ikkunassa **Näytä kaikki** -toiminto.

Näkyvissä ovat kaikki saapuvat asiakirjatietueet, eli myös ne, joiden **Käsitelty**-valintaruutua ei ole valittu.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Saapuvien asiakirjatietueiden lisääminen oletusnäkymään
1. Valitse **Saapuvat asiakirjat** -ikkunassa **Näytä kaikki** -toiminto.
2. Valitse saapuvista asiakirjatietueista vähintään yksi rivi, jonka haluat näkyvän oletusnäkymässä.
3. Valitse **Määritä tilaksi Käsittelemätön** -toiminto.  

> [!NOTE]  
>   Voit tehdä tämän toiminnon yksittäiselle tietueelle **Saapuvan asiakirjan kortti** -ikkunassa.

## <a name="see-also"></a>Katso myös
[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

