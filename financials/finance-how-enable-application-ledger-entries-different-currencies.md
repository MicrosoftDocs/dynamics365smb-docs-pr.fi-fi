---
title: "Toimintaohje: Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa| Microsoft Docs"
description: "Lisätietoja tapahtumien käytöstä eri valuutoilla."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 4f904d1600d56a83238581915726a7b7fd6cca38
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a>Toimintaohje: Tapahtumakirjausten kohdistamisen ottaminen käyttöön eri valuutoissa
Jos ostat toimittajalta yhdessä valuutassa ja maksat maksun toisessa valuutassa, maksu voidaan kohdistaa ostoon.

Ja jos asiakkaalle myydään yhdessä valuutassa ja maksu vastaanotetaan toisessa valuutassa, maksu voidaan kohdistaa myyntilaskuun.

Seuraavassa kuvataan, miten tämä määritetään toimittajatapahtumille **Ostojen ja ostovelkojen asetukset** -ikkunassa. Asetukset tehdään samoin kuin asiakastapahtumille **Myyntien ja myyntisaamisten asetukset** -ikkunassa.

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Toimittajatapahtumien kohdistamisen ottaminen käyttöön eri valuutoissa
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Ostojen ja ostovelkojen asetukset** ja valitse sitten liittyvä linkki.
2. Valitse **Valuuttojen välinen kohdistus** -kentässä jokin seuraavista vaihtoehdoista.

| Asetus | Kuvaus |
| --- | --- |
| Ei yhtään |Valuuttojen välistä kohdistusta ei sallita. |
| EMU |EMU-valuuttojen välinen kohdistus sallitaan. |
| Kaikki |Kaikkien valuuttojen välinen kohdistus sallitaan. |

## <a name="see-also"></a>Katso myös
[Ostovelkojen hallinta](payables-manage-payables.md)  
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

