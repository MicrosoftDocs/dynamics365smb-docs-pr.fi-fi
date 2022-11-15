---
title: Tietojen vaihtaminen
description: Siirrä sähköisiä yritysasiakirjoja, esimerkiksi pankkitiedostoja, Business Centralin ja ulkopuolisten osapuolten välillä.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: exchange data, external files, electronic documents, AMC Banking, OCT, SEPA
ms.date: 06/10/2021
ms.author: edupont
ms.openlocfilehash: bb5886d46e780a32f0d0e58d0f62c58cacdc91a7
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744732"
---
# <a name="exchanging-data"></a>Tietojen vaihtaminen
[!INCLUDE[prod_short](includes/prod_short.md)] -järjestelmä on määritetty vaihtamaan tietoja ulkoisten tiedostojen tai virtojen kanssa, jotka on liitetty yleisiin liiketoimintatehtäviin, kuten sähköisten asiakirjojen lähettämiseen ja vastaanottamiseen sekä pankkitiedostojen tuontiin ja vientiin.  

Ennen kuin voit lähettää ja vastaanottaa sähköisiä asiakirjoja tai tuoda ja viedä pankkitiedostoja, sinun on määritettävä tiedonsiirtokehys datatiedostojen tai virtojen käsittelemistä varten. Lisäksi sinun on määritettävä liittyvät alueet, kuten asiakkaat, joille lähetät sähköiset laskut, ja AMC Banking 365 Fundamentals -laajennuksen, jos jaat pankkitiedostojen muuntamisen ulkoiselle palvelutarjoajalle. Lisätietoja on kohdassa [Tiedonsiirron määrittäminen](across-set-up-data-exchange.md).  

 Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Muunna myyntiasiakirjojen tietueet [!INCLUDE[prod_short](includes/prod_short.md)]:ssa vakiomuotoon, jotka voi lähettää asiakkaalle sähköisessä muodossa tuotavaksi asiakkaan omaan järjestelmään.|[Sähköisten asiakirjojen lähettäminen](sales-how-to-send-electronic-documents.md)|  
|Lähetä PDF tai kuvatiedostot OCR-palvelun tuottajalle. Saat ne takaisin sähköisinä asiakirjoina, jotka voidaan muuntaa [!INCLUDE[prod_short](includes/prod_short.md)]:n asiakirjatietueiksi.|[PDF- ja kuvatiedostojen muuntaminen sähköisiksi asiakirjoiksi OCR-palvelun avulla](across-how-use-ocr-pdf-images-files.md)|  
|Vastaanota sähköiset, joko asiakirjat OCR-palvelusta tai document exchange-palvelusta, standardoidussa muodossa, jonka voit muuntaa asiakirjan tietueiksi [!INCLUDE[prod_short](includes/prod_short.md)]:ssa.|[Sähköisten asiakirjojen vastaanottaminen ja muuntaminen](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Valmistele tiliotetiedoston tuonti **Maksujen täsmäytyskirjauskansio** -sivulle saatujen maksujen täsmäyttämisen ensimmäisenä vaiheena tai **Pankkitilin täsmäytys** -sivulle pankkitilien täsmäyttämisen ensimmäisenä vaiheena.|[Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md)|  
|Vie maksut **Maksupäiväkirja**-sivulta pankkitiedostoon, jonka lataat verkkopankkitilille käsiteltäväksi.|[Maksujen vienti pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)|
|Suorita sähköiset maksut EU:n SEPA-tilisiirtostandardin mukaisesti.|[Maksujen suorittaminen AMC Banking 365 Fundamentals -laajennuksen tai SEPA-tilisiirron avulla](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Ohjaa pankkiasi siirtämään maksusummat asiakkaan pankkitileiltä yrityksesi pankkitilille SEPA-suoraveloitusasetustesi mukaisesti.|[SEPA-suoraveloitusperintätapahtumien luominen ja vieminen pankkitiedostoon](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)|  
|Käytä vaihtokurssin päivityspalvelun palveluntarjoajaa päivittämään **Valuutat**-sivu.|[Valuutan vaihtokurssien päivittäminen](finance-how-update-currencies.md)|  
|Tarkastele, mitkä tiedostoelementit on yhdistetty [!INCLUDE[prod_short](includes/prod_short.md)] -järjestelmän kenttiin kun tuot SEPA CAMT -tiliotetiedostoja.|[Kenttien vastaavuuksien määrittäminen tuotaessa SEPA-CAMT-tiedostoja](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Vie tiedot [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa Intrastat-raportointia varten.|[Intrastat-raportoinnin määrittäminen](finance-how-setup-report-intrastat.md)|
|Tarkastele, mitkä tiedostoelementit on yhdistetty [!INCLUDE[prod_short](includes/prod_short.md)]in kenttiin, kun viet maksutiedostoja käyttämällä AMC Banking 365 Fundamentals -laajennusta.|[Kenttien yhdistäminen, kun maksutiedostoja viedään AMC Banking 365 Fundamentals -laajennuksen avulla](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Katso myös  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)  
[Myynnin laskutus](sales-how-invoice-sales.md)   
[Ostojen kirjaus](purchasing-how-record-purchases.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
