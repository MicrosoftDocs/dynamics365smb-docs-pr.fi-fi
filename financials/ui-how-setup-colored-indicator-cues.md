---
title: "Toimintaohje: Pinojen värillisen mittarin määrittäminen | Microsoft Docs"
description: "Lisätietoja värillisten ilmaisimien käytöstä roolikeskuksen pinoissa."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 3c5aff53c522729a95763485eb79d13c0f051831
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-a-colored-indicator-on-cues"></a>Toimintaohje: Pinojen värillisen mittarin määrittäminen
Voit määrittää pinot, jotka näkyvät käyttäjien **kotisivulla**, kun haluat sisällyttää ilmaisimen, joka vaihtaa väriä pinojen arvojen mukaan.

Ilmaisin näkyy värillisenä palkkina pinon ruudun yläreunassa. Se antaa visuaalisen signaalin pinon toiminnan tilasta, joka voi ilmaista suotuisia tai epäsuotuisia olosuhteita ja kehottaa käyttäjää toimimaan. Esimerkiksi, jos pino näyttää myyntilaskujen jatkuvan, voit määrittää ilmaisimen näkymään vihreänä (hyvä), kun jatkuva myyntilaskujen määrä on alle 10, ja se muuttuu punaiseksi (epäsuotuisa) kun summa on yli 20.

**Pinon asetukset** -ikkunasta voit asettaa ilmaisimet kaikille pinoille, jotka ovat saatavilla yhtiön tietokannassa.

Jotta voit määrittää ilmaisimen, sinun on määritettävä korkeintaan kaksi raja-arvoa, jotka määrittävät kolme arvoaluetta (matala, keskisuuri ja korkea), joihin voit käyttää eri värejä (tai tyyliä).

## <a name="to-set-up-colored-indicators-on-cues"></a>Värillisten ilmaisinten määrittäminen pinoissa
1. Valitse **kotisivun** **Toimenpiteet**-kohdassa **Määritä pinot**.  
   **Pinon asetukset** -ikkuna aukeaa. Ikkunassa on lueteltu ilmaisimet, jotka on tällä hetkellä asetettu pinoissa.
2. Voit muokata ilmaisinta muokkaamalla kenttiä ja muokkaamalla esimerkiksi eri rajojen arvoja.  

Seuraava taulukko sisältää värit, jotka vastaavat **Matalan alueen tyyli**-, **Keskialueen tyyli**- ja **Korkean alueen tyyli** -kenttää.

| Asetus | Väri |
| --- | --- |
| **Ei yhtään** |Ei väriä (sama väri kuin pinon ruutu) |
| **Suotuisa** |Vihreä |
| **Epäsuotuisa** |Punainen |
| **Epäselvä** |Keltainen |
| **Alataso** |Harmaa |

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

