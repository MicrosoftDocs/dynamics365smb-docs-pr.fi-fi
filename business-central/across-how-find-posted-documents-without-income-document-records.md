---
title: Liitteettömien asiakirjojen etsiminen| Microsoft Docs
Description: Voit etsiä kirjanpitotapahtumia kirjatuille myynti- ja ostoasiakirjoille, joilla ei ole saapuvia sähköisiä asiakirjoja, kuten tuotuja laskuja.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0b31d225083d566967b3c9cb7facee564c3d3466
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188538"
---
# <a name="find-posted-documents-without-incoming-document-records"></a>Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita
**Tilikartta**- ja **Pääkirjanpidon tapahtumat** -sivujen hakutoiminnon avulla voit etsiä pääkirjanpidon tapahtumia kirjatuille osto- ja myyntiasiakirjoille, joilla ei ole saapuvia asiakirjatietueita. Tämän jälkeen voit keskitetysti muodostaa yhteyden olemassa oleviin tietueisiin tai luoda uusia tietueita ja niihin liittyviä asiakirjatiedostoja.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tilikartta** ja valitse sitten liittyvä linkki.
2. Valitse pääkirjanpidon tapahtumien KP-tilin rivi, kun haluat tarkastella kyseisen rivin kirjattuja osto- ja myyntiasiakirjoja, joilla ei ole saapuvia asiakirjatietueita. Valitse sitten **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -toiminto.
3. Vaihtoehtoisesti voit valita **Tapahtumakirjaukset**-toiminnon.
4. Valitse **Pääkirjanpidon tapahtumat** -sivulla **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -toiminto.

Avautuvalla **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -sivulla näkyvät kirjatut osto- ja myyntiasiakirjat, joilla ei ole saapuvia asiakirjatietueita. Sivun tiedot koskevat määrittämäsi KP-tilin pääkirjanpidon tapahtumia. Sivulla näkyy enintään 1 000 riviä. Oletusarvon mukaan **Pvm-suodatus**-kentässä on suodatin, joka rajoittaa rivit tapahtumiin, joiden kirjauspäivämäärät ulottuvat tilikauden alusta käsittelypäivämäärään.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Löydettyjen asiakirjojen yhdistäminen olemassa oleviin saapuviin asiakirjatietueisiin
1. Valitse **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -sivulla rivi kirjatulle asiakirjalle, jonka haluat yhdistää olemassa olevaan saapuvaan asiakirjatietueeseen. Valitse sitten **Valitse saapuva asiakirja** -toiminto.
2. Valitse **Saapuvat asiakirjat** -sivulla saapuva asiakirjatietue, jonka haluat yhdistää löydettyyn kirjattuun asiakirjaan ja valitse sitten **OK**-painike.
3. Valittu saapuva asiakirjatietue on nyt yhdistetty **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -sivulla kirjattuun asiakirjaan, kuten **Saapuvat asiakirjatiedostot** -tietoruudusta voidaan nähdä.

Jos **Saapuvat asiakirjat** -sivulla ei ole asiaankuuluvaa saapuvaa asiakirjatietuetta, voit luoda sen. Lisätietoja on kohdassa [Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md).

## <a name="see-also"></a>Katso myös
[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
