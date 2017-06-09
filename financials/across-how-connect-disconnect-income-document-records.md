---
title: "Toimintaohje: Saapuvien asiakirjatietueiden yhdistäminen ja yhdistämisen poistaminen asiakirjoista ja tapahtumista| Microsoft Docs"
description: "Toimintaohje: Saapuvien asiakirjatietueiden yhdistäminen ja yhdistämisen poistaminen asiakirjoista ja tapahtumista"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 05/12/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d29979de3643cbe542f31d3bc67ee0f47effcd4a
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-connect-and-disconnect-incoming-document-records-from-documents-and-entries"></a>Toimintaohje: Saapuvien asiakirjatietueiden yhdistäminen ja yhdistämisen poistaminen asiakirjoista ja tapahtumista
Voit tallentaa ulkoisia liiketoiminta-asiakirjoja [!INCLUDE[d365fin](includes/d365fin_md.md)]iin liittämällä asiakirjatiedostoja soveltuviin saapuviin asiakirjatietueisiin. Vaikka asiakirja (kuten ostolasku) ei olisi ollut alun pitäen saapuva asiakirjatietue, voit silti luoda ja yhdistää siihen saapuvan asiakirjatietueen myöhemmin. Voit myös liittää saapuvia asiakirjatiedostoja kirjattuihin osto- ja myyntiasiakirjoihin sekä toimittaja-, asiakas- ja pääkirjanpidon tapahtumiin käyttämällä **Saapuvat asiakirjatiedostot** -tietoruutua esimerkiksi **Kirjatut ostolaskut**- ja **Toimittajatapahtumat**-ikkunassa.

**Tilikartta**- ja **Pääkirjanpidon tapahtumat** -ikkunan hakutoiminnon avulla voit etsiä pääkirjanpidon tapahtumia kirjatuille osto- ja myyntiasiakirjoille, joilla ei ole saapuvia asiakirjatietueita. Tämän jälkeen voit keskitetysti muodostaa yhteyden olemassa oleviin tietueisiin tai luoda uusia tietueita ja niihin liittyviä asiakirjatiedostoja. Lisätietoja on kohdassa [Toimintaohje: Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita](across-how-find-posted-documents-without-income-document-records.md).

Seuraavassa kuvataan, kuinka voit liittää tiedoston olemassa olevaan ostolaskuun, jota ei ole luotu saapuvasta asiakirjatietueesta. Lisäksi kuvataan, kuinka voit liittää tiedoston toimittajatapahtumaan. Tiedoston liittäminen kirjattuihin osto- tai myyntiasiakirjoihin toimii vastaavalla tavalla.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Saapuvan asiakirjatietueen luominen ja yhdistäminen ostolaskusta
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Ostolaskut** ja valitse sitten liittyvä linkki.
2. Valitse sen ostolaskun rivi, johon haluat liittää tiedoston, ja valitse sitten **Luo saapuva asiakirja tiedostosta** -toiminto.
3. Vaihtoehtoisesti voit valita sen ostolaskun rivin, johon haluat liittää tiedoston, ja valita sitten **Liitä tiedosto**-toiminnon.
4. Valitse **Lisää tiedosto** -ikkunassa tiedosto, joka vastaa kyseistä saapuvaa asiakirjaa, ja valitse sitten **Avaa**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Saapuvan asiakirjatietueen luominen ja yhdistäminen toimittajatapahtumasta
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Toimittajatapahtumat** ja valitse sitten liittyvä linkki.
2. Valitse sen toimittajatapahtuman rivi, johon haluat liittää tiedoston, ja valitse sitten **Luo saapuva asiakirja tiedostosta** -toiminto.
3. Vaihtoehtoisesti voit valita sen toimittajatapahtuman rivin, johon haluat liittää tiedoston, ja valita sitten **Liitä tiedosto**-toiminnon.
4. Valitse **Lisää tiedosto** -ikkunassa tiedosto, joka vastaa kyseistä saapuvaa asiakirjaa, ja valitse sitten **Avaa**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Saapuvan asiakirjan tietueen ja kirjatun asiakirjan yhteyden poistaminen
Voit poistaa liitetiedostot kirjaamattomista asiakirjoista milloin tahansa poistamalla saapuvan asiakirjan tietueen. Jos asiakirja on kirjattu, liitos saapuvan asiakirjan tietueeseen on poistettava ensin.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Saapuvat asiakirjat** ja valitse sitten liittyvä linkki.
2. Valitse sen saapuvan asiakirjatietueen rivi, joka on liitetty poistettavaan kirjattuun asiakirjaan, ja valitse sitten **Poista viite tietueeseen** -toiminto.

Yhteys kirjattuun asiakirjaan poistetaan. Voit nyt liittää toisen saapuvan asiakirjatietueen kirjattuun asiakirjaan tässä ohjeaiheessa kuvatulla tavalla.

## <a name="see-also"></a>Katso myös
[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

