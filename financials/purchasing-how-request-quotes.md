---
title: "Tarjouksen pyytäminen toimittajalta luotavan tarjouspyynnön avulla | Microsoft Docs"
description: "Ohjeaiheessa käsitellään, miten luodaan myyntitarjous- tai tarjouspyyntöasiakirja kirjaamaan asiakkaalle tehty tarjous tuotteiden myynnistä tietyin ehdoin."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: df1793d811dea11c01ff5e7d90a9f52b9e987c13
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-request-quotes"></a>Toimintaohje: Tarjousten pyytäminen
Ostotarjousta voidaan käyttää ostotilauksen alustavana luonnoksena, jonka jälkeen tilaus voidaan muuttaa ostolaskuksi tai -tilaukseksi.


## <a name="to-create-a-purchase-quote"></a>Uuden ostotarjouksen luominen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Ostotarjoukset** ja valitse sitten aiheeseen liittyvä linkki.
2. Luo uusi asiakirja samalla tavalla kuin tekisit ostotilauksen. Lisätietoja on kohdassa[Toimintaohje: Ostojen kirjaaminen](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Ostotarjousten muuttaminen ostotilauksiksi
Kun olet hyväksynyt toimittajan tarjouksen, voit käsitellä oston muuntamalla tarjouksen ostolaskuksi tai tilaukseksi.

1. Avaa muuntovalmis ostotarjous ja valitse sitten **Tee tilaus** -toiminto.

Ostotarjous poistetaan tietokannasta. Ostotarjouksen tietojen perusteella luodaan ostolasku tai -tilaus, jossa voit käsitellä oston. Luodun ostolaskun tai -tilauksen **Tarjouksen nro** -kenttä määrittää sen ostotarjouksen numeron, josta tilaus on muunnettu.

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Toimintaohje: Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

