---
title: "Saapuvien asiakirjojen käsitteleminen| Microsoft Docs"
description: "Saapuvien asiakirjojen käsitteleminen"
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
ms.openlocfilehash: 93a3ba01e479ba8256f4a3628aae2b7838d8e5ad
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="processing-incoming-documents"></a>Saapuvien asiakirjojen käsitteleminen
Voit tallentaa ulkoisen asiakirjan [!INCLUDE[d365fin](includes/d365fin_md.md)]issa luomalla tai suorittamalla ensin saapuvan tiedostotietueen. Voit tehdä tämän manuaalisesti tai ottaa valokuvan ulkoisesta asiakirjasta ja luoda sitten saapuva asiakirjatietue, johon on liitetty kuvatiedosto.

Ulkoinen OCR (Optical Character Recognition) -palvelu voi luoda liikekumppaneilta vastaanotetuista PDF- tai kuvatiedostoista sähköisiä asiakirjoja, jotka voit muuntaa tiedostotietueiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]issa. Esimerkiksi kun saat PDF-muodossa laskun toimittajalta, voit lähettää sen OCR-palveluun **Saapuvat asiakirjat** -ikkunasta. Vaihtoehtoisesti voit lähettää tiedoston OCR-palveluun sähköpostitse. Sitten, kun saat sähköisen tiedoston takaisin, liittyvä saapuvan asiakirjan tietue luodaan automaattisesti. Jonkin sekunnin kuluttua saat tiedoston takaisin OCR-palvelusta sähköisenä laskuna, jonka voit muuntaa toimittajan ostolaskuksi.

| Toiminta | Katso |
| --- | --- |
| Luo saapuvat asiakirjatietueet manuaalisesti tai automaattisesti esimerkiksi ottamalla paperikuitista valokuvan. |[Toimintaohje: Saapuvien asiakirjatietueiden luominen](across-how-create-income-document-records.md) |
| Muunna PDF- ja kuvatiedostot OCR-palvelun avulla sähköisiksi asiakirjoiksi, jotka voi sitten muuntaa [!INCLUDE[d365fin](includes/d365fin_md.md)]issa esimerkiksi ostolaskuiksi. Kouluta OCR-palvelu niin, että se välttää virheitä seuraavalla kerralla, kun palvelu käsittelee samanlaisia tietoja. |[Toimintaohje: PDF- ja kuvatiedostojen muuntaminen sähköisiksi asiakirjoiksi OCR-palvelun avulla](across-how-use-ocr-pdf-images-files.md) |
| Yhdistä saapuva asiakirjatiedosto mihin tahansa kirjaamattomaan myynti- tai ostoasiakirjaan ja mihin tahansa asiakas-, toimittaja- tai pääkirjamerkintään asiakirjasta tai merkinnästä käsin tai poista saapuva asiakirjatiedosto mainituista näistä kohteista. |[Toimintaohje: Saapuvien asiakirjatietueiden yhdistäminen ja yhdistämisen poistaminen asiakirjoista ja tapahtumista](across-how-connect-disconnect-income-document-records.md) |
| **Tilikartta**- ja **Pääkirjanpidon tapahtumat** -ikkunan hakutoiminnon avulla voit etsiä pääkirjanpidon tapahtumia kirjatuille asiakirjoille, joilla ei ole saapuvia asiakirjatietueita. Tämän jälkeen voit keskitetysti muodostaa yhteyden olemassa oleviin tietueisiin tai luoda uusia tietueita ja niihin liittyviä asiakirjatiedostoja. |[Toimintaohje: Sellaisten kirjattujen asiakirjojen etsiminen, joilla ei ole saapuvia asiakirjatietueita](across-how-find-posted-documents-without-income-document-records.md) |
| Saat paremman yleiskuvan määrittämällä saapuvien asiakirjatietueiden tilaksi Käsitelty, kun haluat poistaa ne oletusnäkymästä. |[Toimintaohje: Useiden saapuvien asiakirjatietueiden hallinta](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Katso myös
[Saapuvat asiakirjat](across-income-documents.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)
