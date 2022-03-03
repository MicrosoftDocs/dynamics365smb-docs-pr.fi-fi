---
title: Uusien arvotapahtumien luominen varastossa oleville nimikkeille| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten vähintään yhden varaston nimikkeen arvotapahtumaa nostetaan tai lasketaan kirjaamalla nimikkeen nykyinen laskettu arvo.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.search.forms: 5803,
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4abfe521684fd6e0e4d8d519248919b0628dc1fb
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8135930"
---
# <a name="revalue-inventory"></a>Varaston uudelleenarvostus
Jos haluat nostaa tai laskea nimikkeen tai tietyn nimiketapahtuman varastoarvoa, sinun tulee käyttää uudelleenarvostuspäiväkirjaa.

## <a name="to-revalue-inventory"></a>Varaston uudelleenarvostus
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Uud.arviointipvk.** ja valitse sitten vastaava linkki.
2. Valitse **Laske varaston arvo** -toiminto.
3. Täytä **Laske varaston arvo** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Valitse **OK**-painike.
5. Syötä uusi yksikkökustannus **Uudelleenarvostus pvk** -sivun kuhunkin **Yks.kust. (uudelleenarvostet.)** -kenttään. Vaihtoehtoisesti voit syöttää uuden kokonaissumman **Var. arvo (uudell.arvostettu)** -kenttään.

    Asianmukaiset kentät päivitetään automaattisesti. Huomaa että **Summa**-kentässä on varaston arvon todellinen muutos valitun nimiketapahtuman osalta. Ohjelma laskee **Varaston arvo (laskettu)** -kentän ja **Var. arvo (uudell.arvostettu)** -kentän erotuksen.
6. Kun olet saanut kaikki uudelleenarvostuspäiväkirjan rivit valmiiksi, valitse **Kirjaa**-toiminto.

Kirjaamiasi uudelleenarvostuksia vastaavat uudet arvotapahtumat on nyt luotu. Uudet arvot näkyvät vastaavissa nimikekorteissa.

## <a name="see-also"></a>Katso myös
[Rakennetiedot: uudelleenarvostus](design-details-revaluation.md)  
[Varasto](inventory-manage-inventory.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]