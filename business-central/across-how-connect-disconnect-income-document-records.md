---
title: Saapuvien asiakirjatietueiden luominen asiakirjoista
description: Voit tallentaa ulkoisia liiketoiminta-asiakirjoja liittämällä asiakirjatiedostoja soveltuviin saapuviin asiakirjatietueisiin.
author: jswymer
ms.topic: how-to
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 02/27/2024
ms.author: jswymer
ms.reviewer: jswymer
ms-service: dynamics-365-business-central
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Saapuvien asiakirjatietueiden luominen suoraan asiakirjoista ja tapahtumista

Voit tallentaa ulkoisia liiketoiminta-asiakirjoja [!INCLUDE[prod_short](includes/prod_short.md)]iin liittämällä asiakirjatiedostoja soveltuviin saapuviin asiakirjatietueisiin. Vaikka asiakirja (kuten ostolasku) ei olisi ollut alun pitäen saapuva asiakirjatietue, voit silti luoda ja yhdistää siihen saapuvan asiakirjatietueen myöhemmin. Voit myös liittää saapuvia asiakirjatiedostoja kirjattuihin osto- ja myyntiasiakirjoihin sekä toimittaja-, asiakas- ja pääkirjanpidon tapahtumiin käyttämällä **Saapuvat asiakirjatiedostot** -tietoruutua esimerkiksi **Kirjatut ostolaskut**- ja **Toimittajatapahtumat**-sivuilla.

**Tilikartta**- ja **Pääkirjanpidon tapahtumat** -sivujen hakutoiminnon avulla voit etsiä pääkirjanpidon tapahtumia kirjatuille osto- ja myyntiasiakirjoille, joilla ei ole saapuvia asiakirjatietueita. Tämän jälkeen voit keskitetysti muodostaa yhteyden olemassa oleviin tietueisiin tai luoda uusia tietueita ja niihin liittyviä asiakirjatiedostoja. Lisätietoja on kohdassa [Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita](across-how-find-posted-documents-without-income-document-records.md).

Seuraavassa kuvataan, kuinka voit liittää tiedoston toimittajatapahtumaan tai olemassa olevaan ostolaskuun, jota ei ole luotu saapuvasta asiakirjatietueesta. Tiedoston liittäminen kirjattuihin osto- tai myyntiasiakirjoihin toimii vastaavalla tavalla.

[!INCLUDE [incoming-doc-archived-doc](includes/incoming-doc-archived-doc.md)]

## Saapuvan asiakirjatietueen luominen ja yhdistäminen ostolaskusta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.
2. Valitse sen ostolaskun rivi, johon haluat liittää tiedoston, ja valitse sitten **Luo saapuva asiakirja tiedostosta** -toiminto.
3. Vaihtoehtoisesti voit valita sen ostolaskun rivin, johon haluat liittää tiedoston, ja valita sitten **Liitä tiedosto**-toiminnon.
4. Tee **Lisää tiedosto** -sivulla jokin seuraavista vaiheista liittääksesi tiedoston, joka vastaa kyseistä saapuvaa asiakirjaa:

   [!INCLUDE[file-upload](includes/file-upload.md)]


## Saapuvan asiakirjatietueen luominen ja yhdistäminen toimittajatapahtumasta

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajatapahtumat** ja valitse sitten vastaava linkki.
2. Valitse sen toimittajatapahtuman rivi, johon haluat liittää tiedoston, ja valitse sitten **Luo saapuva asiakirja tiedostosta** -toiminto.
3. Vaihtoehtoisesti voit valita sen toimittajatapahtuman rivin, johon haluat liittää tiedoston, ja valita sitten **Liitä tiedosto**-toiminnon.
4. Tee **Lisää tiedosto** -sivulla jokin seuraavista vaiheista liittääksesi tiedoston, joka vastaa kyseistä saapuvaa asiakirjaa:

   [!INCLUDE[file-upload](includes/file-upload.md)]


## Saapuvan asiakirjan tietueen ja kirjatun asiakirjan yhteyden poistaminen

Voit poistaa liitetiedostot kirjaamattomista asiakirjoista milloin tahansa poistamalla saapuvan asiakirjan tietueen. Jos asiakirja on kirjattu, liitos saapuvan asiakirjan tietueeseen on poistettava ensin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Saapuvat asiakirjat** ja valitse sitten vastaava linkki.
2. Valitse sen saapuvan asiakirjatietueen rivi, joka on liitetty poistettavaan kirjattuun asiakirjaan, ja valitse sitten **Poista viite tietueeseen** -toiminto.

Yhteys kirjattuun asiakirjaan poistetaan. Voit nyt liittää toisen saapuvan asiakirjatietueen kirjattuun asiakirjaan tässä artikkelissa kuvatulla tavalla.

## Katso myös

[Saapuvien asiakirjatietueiden luonti](across-how-create-income-document-records.md)
[Käytä OCR:ää PDF-ja kuvatiedostojen muuntamiseksi sähköisiksi asiakirjoiksi](across-how-use-ocr-pdf-images-files.md)
[Kirjattujen asiakirjojen etsiminen ilman saapuvien asiakirjojen tietueita](across-how-find-posted-documents-without-income-document-records.md)
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
