---
title: Ostotarjouksen luominen tarjouksen pyytämistä varten | Microsoft Docs
description: Ohjeaiheessa käsitellään, miten luodaan myyntitarjous- tai tarjouspyyntöasiakirja kirjaamaan asiakkaalle tehty tarjous tuotteiden myynnistä tietyin ehdoin.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 71c31fc15027d1f2d571afe97ae79f95709c9f06
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312410"
---
# <a name="request-quotes"></a>Tarjousten pyytäminen
Ostotarjousta voidaan käyttää ostotilauksen alustavana luonnoksena, jonka jälkeen tilaus voidaan muuttaa ostolaskuksi tai -tilaukseksi.


## <a name="to-create-a-purchase-quote"></a>Uuden ostotarjouksen luominen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotarjoukset** ja valitse sitten liittyvä linkki.
2. Luo uusi asiakirja samalla tavalla kuin tekisit ostotilauksen. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Ostotarjousten muuttaminen ostotilauksiksi
Kun olet hyväksynyt toimittajan tarjouksen, voit käsitellä oston muuntamalla tarjouksen ostolaskuksi tai tilaukseksi.

1. Avaa muuntovalmis ostotarjous ja valitse sitten **Tee tilaus** -toiminto.

Ostotarjous poistetaan tietokannasta. Ostotarjouksen tietojen perusteella luodaan ostolasku tai -tilaus, jossa voit käsitellä oston. Luodun ostolaskun tai -tilauksen **Tarjouksen nro** -kenttä määrittää sen ostotarjouksen numeron, josta tilaus on muunnettu.

## <a name="see-also"></a>Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
