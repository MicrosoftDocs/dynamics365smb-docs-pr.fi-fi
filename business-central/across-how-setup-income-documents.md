---
title: Saapuvien asiakirjojen määrittäminen| Microsoft Docs
description: Voit käyttää saapuvien asiakirjojen toimintoa sähköisten asiakirjojen luomiseen, OCR-tehtävien hallintaan, laskujen tuontiin ja kuvatiedostojen muuntamiseen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f7d0741f3ead748867a52cb399967c196748c479
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305522"
---
# <a name="set-up-incoming-documents"></a>Määritä saapuvat asiakirjat
Jos luot pääkirjan rivejä saapuvista asiakirjatietueista, **Saapuvien asiakirjojen asetukset** -sivulla on määritettävä käytettävä päiväkirjan malli sekä erä.

Jos haluat, etteivät käyttäjät voi luoda laskuja tai yleisen päiväkirjan rivejä saapuvista asiakirjatietueista ennen asiakirjojen hyväksymistä, määritä hyväksyjät **Saapuvan asiakirjan hyväksyjät** -sivulla.

Jos haluat muuntaa PDF- ja kuvatiedostoja sähköisiksi asiakirjoiksi, jotka voi muuntaa esimerkiksi ostolaskuiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, määritä ensin OCR-ominaisuus ja ota palvelu käyttöön.

Kun Saapuvat asiakirjat -ominaisuus on määritetty, voit käyttää erilaisia toimintoja, joilla voit tarkistaa kulutositteita, hallita OCR-tehtäviä ja muuntaa saapuvia asiakirjatiedostoja manuaalisesti tai automaattisesti sekä siirtää niistä tietoja asiakirjoihin tai kirjanpitoriveille. Ulkoisia tiedostoja voi liittää missä tahansa prosessin vaiheessa myös kirjattuihin asiakirjoihin ja muodostuviin toimittaja-, asiakas- ja pääkirjamerkintöihin. Lisätietoja on kohdassa [Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Saapuvat asiakirjat -ominaisuuden määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvien asiakirjojen asetukset** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Saapuvien asiakirjatietueiden hyväksyjien määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvien asiakirjojen asetukset** ja valitse sitten liittyvä linkki.  
2. Valitse **Saapuvien asiakirjojen asetukset** -sivulla **Hyväksyjät**-toiminto.

    Kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)]iin rekisteröityneet käyttäjät näkyvät **Saapuvan asiakirjan hyväksyjät** -sivulla.  
3. Valitse vähintään yksi käyttäjä, joka voi hyväksyä saapuvan asiakirjan ennen liittyvän asiakirjan tai päiväkirjarivin luomista.

Kun hyväksyjät on määritetty **Saapuvien asiakirjojen hyväksyjät** -sivulla, vain kyseiset käyttäjät voivat hyväksyä saapuvan asiakirjan, jos **Saapuvien asiakirjojen asetukset** -sivun **Edellytä hyväksyntää luomista varten** -valintaruutu on valittu.

> [!NOTE]  
>   Nämä hyväksynnän asetukset eivät liity hyväksymistyönkulkuihin. Lisätietoja on kohdassa [Hyväksymistyönkulkujen käyttäminen](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>OCR-palvelun määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **OCR-palvelun asetukset** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Sisäänkirjaustiedot salataan automaattisesti.

## <a name="see-also"></a>Katso myös
[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
