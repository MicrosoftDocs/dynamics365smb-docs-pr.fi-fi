---
title: Saapuvien asiakirjatietueiden luominen asiakirjoista
description: Voit tallentaa ulkoisia liiketoiminta-asiakirjoja liittämällä asiakirjatiedostoja soveltuviin saapuviin asiakirjatietueisiin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 609a57cd1d87a8a3518d6eaf7bc3fe8fc142953a
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134354"
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Saapuvien asiakirjatietueiden luominen suoraan asiakirjoista ja tapahtumista
Voit tallentaa ulkoisia liiketoiminta-asiakirjoja [!INCLUDE[prod_short](includes/prod_short.md)]iin liittämällä asiakirjatiedostoja soveltuviin saapuviin asiakirjatietueisiin. Vaikka asiakirja (kuten ostolasku) ei olisi ollut alun pitäen saapuva asiakirjatietue, voit silti luoda ja yhdistää siihen saapuvan asiakirjatietueen myöhemmin. Voit myös liittää saapuvia asiakirjatiedostoja kirjattuihin osto- ja myyntiasiakirjoihin sekä toimittaja-, asiakas- ja pääkirjanpidon tapahtumiin käyttämällä **Saapuvat asiakirjatiedostot** -tietoruutua esimerkiksi **Kirjatut ostolaskut**- ja **Toimittajatapahtumat**-sivuilla.

**Tilikartta**- ja **Pääkirjanpidon tapahtumat** -sivujen hakutoiminnon avulla voit etsiä pääkirjanpidon tapahtumia kirjatuille osto- ja myyntiasiakirjoille, joilla ei ole saapuvia asiakirjatietueita. Tämän jälkeen voit keskitetysti muodostaa yhteyden olemassa oleviin tietueisiin tai luoda uusia tietueita ja niihin liittyviä asiakirjatiedostoja. Lisätietoja on kohdassa [Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita](across-how-find-posted-documents-without-income-document-records.md).

Seuraavassa kuvataan, kuinka voit liittää tiedoston olemassa olevaan ostolaskuun, jota ei ole luotu saapuvasta asiakirjatietueesta. Lisäksi kuvataan, kuinka voit liittää tiedoston toimittajatapahtumaan. Tiedoston liittäminen kirjattuihin osto- tai myyntiasiakirjoihin toimii vastaavalla tavalla.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Saapuvan asiakirjatietueen luominen ja yhdistäminen ostolaskusta
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.
2. Valitse sen ostolaskun rivi, johon haluat liittää tiedoston, ja valitse sitten **Luo saapuva asiakirja tiedostosta** -toiminto.
3. Vaihtoehtoisesti voit valita sen ostolaskun rivin, johon haluat liittää tiedoston, ja valita sitten **Liitä tiedosto**-toiminnon.
4. Valitse **Lisää tiedosto** -sivulla tiedosto, joka vastaa kyseistä saapuvaa asiakirjaa, ja valitse sitten **Avaa**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Saapuvan asiakirjatietueen luominen ja yhdistäminen toimittajatapahtumasta
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajatapahtumat** ja valitse sitten vastaava linkki.
2. Valitse sen toimittajatapahtuman rivi, johon haluat liittää tiedoston, ja valitse sitten **Luo saapuva asiakirja tiedostosta** -toiminto.
3. Vaihtoehtoisesti voit valita sen toimittajatapahtuman rivin, johon haluat liittää tiedoston, ja valita sitten **Liitä tiedosto**-toiminnon.
4. Valitse **Lisää tiedosto** -sivulla tiedosto, joka vastaa kyseistä saapuvaa asiakirjaa, ja valitse sitten **Avaa**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Saapuvan asiakirjan tietueen ja kirjatun asiakirjan yhteyden poistaminen
Voit poistaa liitetiedostot kirjaamattomista asiakirjoista milloin tahansa poistamalla saapuvan asiakirjan tietueen. Jos asiakirja on kirjattu, liitos saapuvan asiakirjan tietueeseen on poistettava ensin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten vastaava linkki.
2. Valitse sen saapuvan asiakirjatietueen rivi, joka on liitetty poistettavaan kirjattuun asiakirjaan, ja valitse sitten **Poista viite tietueeseen** -toiminto.

Yhteys kirjattuun asiakirjaan poistetaan. Voit nyt liittää toisen saapuvan asiakirjatietueen kirjattuun asiakirjaan tässä ohjeaiheessa kuvatulla tavalla.

## <a name="see-also"></a>Katso myös
[Saapuvien asiakirjojen käsitteleminen](across-process-income-documents.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]