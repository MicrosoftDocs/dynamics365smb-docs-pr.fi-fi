---
title: Pinon toiminnon visuaalisien signaalien mukauttaminen | Microsoft Docs
description: "Määritä värillinen mittari pinoruudussa mukautettuna pinon toiminnon visuaalisena signaalina."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 10/01/2018
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 366d762fbfbd2a61253b087577ef2810194e2c35
ms.contentlocale: fi-fi
ms.lasthandoff: 11/22/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a>Pinojen värillisen ilmaisimen määrittäminen
Voit määrittää pinot, jotka näkyvät roolikeskuksessa, kun haluat sisällyttää ilmaisimen, joka vaihtaa väriä pinojen arvojen mukaan.

Ilmaisin näkyy värillisenä palkkina pinon ruudun yläreunassa. Se antaa visuaalisen signaalin pinon toiminnan tilasta, joka voi ilmaista suotuisia tai epäsuotuisia olosuhteita ja kehottaa käyttäjää toimimaan. Esimerkiksi, jos pino näyttää myyntilaskujen jatkuvan, voit määrittää ilmaisimen näkymään vihreänä (hyvä), kun jatkuva myyntilaskujen määrä on alle 10, ja se muuttuu punaiseksi (epäsuotuisa) kun summa on yli 20.

**Pinon asetukset** -sivulla voi määrittää ilmaisimet kaikille pinoille, jotka ovat saatavilla yhtiön tietokannassa.

Jotta voit määrittää ilmaisimen, sinun on määritettävä korkeintaan kaksi raja-arvoa, jotka määrittävät kolme arvoaluetta (matala, keskisuuri ja korkea), joihin voit käyttää eri värejä (tai tyyliä).

## <a name="to-set-up-colored-indicators-on-cues"></a>Värillisten ilmaisinten määrittäminen pinoissa
1. Valitse **Toimenpiteet**-kohdan roolikeskuksessa **Määritä pinot**.  
   **Pinon asetukset** -sivu avautuu. Sivulla on lueteltu ilmaisimet, jotka on tällä hetkellä asetettu pinoissa.
2. Voit muokata ilmaisinta muokkaamalla kenttiä ja muokkaamalla esimerkiksi eri rajojen arvoja.  

Seuraava taulukko sisältää värit, jotka vastaavat **Matalan alueen tyyli**-, **Keskialueen tyyli**- ja **Korkean alueen tyyli** -kenttää.

| Asetus | Väri |
| --- | --- |
| **Ei mitään** |Ei väriä (sama väri kuin pinon ruutu)|
| **Suotuisa** |Vihreä |
| **Epäsuotuisa** |Punainen |
| **Epäselvä** |Keltainen |
| **Alataso** |Harmaa |

## <a name="see-also"></a>Katso myös
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

