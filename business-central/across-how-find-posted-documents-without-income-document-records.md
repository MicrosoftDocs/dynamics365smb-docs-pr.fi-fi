---
title: 'Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjoja'
description: 'Voit etsiä kirjanpitotapahtumia kirjatuille myynti- ja ostoasiakirjoille, joilla ei ole saapuvia sähköisiä asiakirjoja, kuten tuotuja laskuja.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="find-posted-documents-without-incoming-document-records"></a><a name="find-posted-documents-without-incoming-document-records"></a><a name="find-posted-documents-without-incoming-document-records"></a>Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita

**Tilikartta**- ja **Pääkirjanpidon tapahtumat** -sivujen hakutoiminnon avulla voit etsiä pääkirjanpidon tapahtumia kirjatuille osto- ja myyntiasiakirjoille, joilla ei ole saapuvia asiakirjatietueita. Tämän jälkeen voit keskitetysti muodostaa yhteyden olemassa oleviin tietueisiin tai luoda uusia tietueita ja niihin liittyviä asiakirjatiedostoja.

## <a name="to-find-posted-documents-without-incoming-document-records"></a><a name="to-find-posted-documents-without-incoming-document-records"></a><a name="to-find-posted-documents-without-incoming-document-records"></a>Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.
2. Valitse pääkirjanpidon tapahtumien KP-tilin rivi, kun haluat tarkastella kyseisen rivin kirjattuja osto- ja myyntiasiakirjoja, joilla ei ole saapuvia asiakirjatietueita. Valitse sitten **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -toiminto.
3. Vaihtoehtoisesti voit valita **Tapahtumakirjaukset**-toiminnon.
4. Valitse **Pääkirjanpidon tapahtumat** -sivulla **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -toiminto.

Avautuvalla **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -sivulla näkyvät kirjatut osto- ja myyntiasiakirjat, joilla ei ole saapuvia asiakirjatietueita. Sivun tiedot koskevat määrittämäsi KP-tilin pääkirjanpidon tapahtumia. Sivulla näkyy enintään 1 000 riviä. Oletusarvon mukaan **Pvm-suodatus**-kentässä on suodatin, joka rajoittaa rivit tapahtumiin, joiden kirjauspäivämäärät ulottuvat tilikauden alusta käsittelypäivämäärään.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><a name="to-connect-found-documents-to-existing-incoming-document-records"></a><a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Löydettyjen asiakirjojen yhdistäminen olemassa oleviin saapuviin asiakirjatietueisiin

1. Valitse **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -sivulla rivi kirjatulle asiakirjalle, jonka haluat yhdistää olemassa olevaan saapuvaan asiakirjatietueeseen. Valitse sitten **Valitse saapuva asiakirja** -toiminto.
2. Valitse **Saapuvat asiakirjat** -sivulla saapuva asiakirjatietue, jonka haluat yhdistää löydettyyn kirjattuun asiakirjaan ja valitse sitten **OK**-painike.
3. Valittu saapuva asiakirjatietue on nyt yhdistetty **Kirjatut asiakirjat ilman saapuvaa asiakirjaa** -sivulla kirjattuun asiakirjaan, kuten **Saapuvat asiakirjatiedostot** -tietoruudusta voidaan nähdä.

Jos **Saapuvat asiakirjat** -sivulla ei ole asiaankuuluvaa saapuvaa asiakirjatietuetta, voit luoda sen. Lisätietoja on kohdassa [Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Saapuvien asiakirjatietueiden luonti](across-how-create-income-document-records.md)
[Käytä OCR:ää PDF-ja kuvatiedostojen muuntamiseksi sähköisiksi asiakirjoiksi](across-how-use-ocr-pdf-images-files.md)
[Saapuvien asiakirjatietueiden luominen suoraan asiakirjoista ja tapahtumista](across-how-connect-disconnect-income-document-records.md)
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
