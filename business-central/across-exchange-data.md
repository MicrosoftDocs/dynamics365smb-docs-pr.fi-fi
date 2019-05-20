---
title: Tietojen vaihtaminen | Microsoft Docs
description: Tietoja voidaan vaihtaa Business Central -sovelluksen ja ulkoisten tiedostojen tai sellaisten virtojen kanssa, jotka on liitetty yleisiin liiketoimintatehtäviin, kuten sähköisten asiakirjojen lähettämiseen ja vastaanottamiseen sekä pankkitiedostojen tuontiin ja vientiin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: edb3ef5d977994588feb4331cf8f15e6f1b32438
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240836"
---
# <a name="exchanging-data"></a>Tietojen vaihtaminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] -järjestelmä on määritetty vaihtamaan tietoja ulkoisten tiedostojen tai virtojen kanssa, jotka on liitetty yleisiin liiketoimintatehtäviin, kuten sähköisten asiakirjojen lähettämiseen ja vastaanottamiseen sekä pankkitiedostojen tuontiin ja vientiin.  

Ennen kuin voit lähettää ja vastaanottaa sähköisiä asiakirjoja tai tuoda ja viedä pankkitiedostoja, sinun on määritettävä tiedonsiirtokehys datatiedostojen tai virtojen käsittelemistä varten. Liittyvät alueet pitää määritellä. Näihin kuuluvat esimerkiksi niiden asiakkaiden perustiedot, joille lähetät sähköisiä laskuja, tai pankkitietojen muuntopalvelun, jos käytät ulkoista palveluntarjoajaa pankkitiedostojen muuntamiseen. Lisätietoja on kohdassa [Tiedonsiirron määrittäminen](across-set-up-data-exchange.md).  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Muunna myyntiasiakirjojen tietueet [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa vakiomuotoon, jotka voi lähettää asiakkaalle sähköisessä muodossa tuotavaksi asiakkaan omaan järjestelmään.|[Sähköisten asiakirjojen lähettäminen](sales-how-to-send-electronic-documents.md)|  
|Lähetä PDF tai kuvatiedostot OCR-palvelun tuottajalle. Saat ne takaisin sähköisinä asiakirjoina, jotka voidaan muuntaa [!INCLUDE[d365fin](includes/d365fin_md.md)]:n asiakirjatietueiksi.|[PDF- ja kuvatiedostojen muuntaminen sähköisiksi asiakirjoiksi OCR-palvelun avulla](across-how-use-ocr-pdf-images-files.md)|  
|Vastaanota sähköiset, joko asiakirjat OCR-palvelusta tai document exchange-palvelusta, standardoidussa muodossa, jonka voit muuntaa asiakirjan tietueiksi [!INCLUDE[d365fin](includes/d365fin_md.md)]:ssa.|[Sähköisten asiakirjojen vastaanottaminen ja muuntaminen](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Valmistele tiliotetiedoston tuonti **Maksujen täsmäytyskirjauskansio** -sivulle saatujen maksujen täsmäyttämisen ensimmäisenä vaiheena tai **Pankkitilin täsmäytys** -sivulle pankkitilien täsmäyttämisen ensimmäisenä vaiheena.|[Envestnet Yodlee Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md)|  
|Vie maksut **Maksupäiväkirja**-sivulta pankkitiedostoon, jonka lataat verkkopankkitilille käsiteltäväksi.|[Maksujen vienti pankkitiedostoon](payables-how-export-payments-bank-file.md)|
|Suorita sähköiset maksut EU:n SEPA-tilisiirtostandardin mukaisesti.|[Maksujen suorittaminen pankkitietojen muunnospalvelulla tai SEPA-tilisiirrolla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Ohjaa pankkiasi siirtämään maksusummat asiakkaan pankkitileiltä yrityksesi pankkitilille SEPA-suoraveloitusasetustesi mukaisesti.|[SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Käytä vaihtokurssin päivityspalvelun palveluntarjoajaa päivittämään **Valuutat**-sivu.|[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)|  
|Tarkastele, mitkä tiedostoelementit on yhdistetty [!INCLUDE[d365fin](includes/d365fin_md.md)] -järjestelmän kenttiin kun tuot SEPA CAMT -tiliotetiedostoja.|[Kenttien vastaavuuksien määrittäminen tuotaessa SEPA-CAMT-tiedostoja](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Tarkastele, mitkä tiedostoelementit on yhdistetty [!INCLUDE[d365fin](includes/d365fin_md.md)] -järjestelmän kenttiin kun viet maksutiedostoja pankkipäivämäärän muuntopalvelu-ominaisuuteen.|[Kenttien vastaavuuksien määrittäminen vietäessä maksutiedostot käyttämällä pankkitietojen muuntopalvelua](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Katso myös  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Myynnin laskutus](sales-how-invoice-sales.md)   
[Ostojen kirjaus](purchasing-how-record-purchases.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
