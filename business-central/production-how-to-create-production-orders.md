---
title: Tuotantotilauksen otsikoiden luominen | Microsoft Docs
description: Tuotantotilauksen voi luoda manuaalisesti. Ensimmäinen työvaihe on tuotantotilauksen otsikon luominen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: fc0a0dda33b7b90658ca60285abab0562c28fbbc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314118"
---
# <a name="create-production-order-headers"></a>Tuotantotilausten otsikoiden luominen
Tuotantotilauksen voi luoda manuaalisesti. Ensimmäinen työvaihe on tuotantotilauksen otsikon luominen.

Suunnittelutoiminto luo tuotantotilaukset tavallisesti automaattisesti toteuttamaan tunnetun kysynnän. Lisätietoja on kohdassa [Suunnittelu](production-planning.md).   

Seuraavassa toienpiteessä luodaan sitovasti suunniteltu tuotantotilaus. Voit luoda myös tuotantotilauksia, joilla on eri tila.  

## <a name="to-create-a-production-order-header"></a>Tuotantotilausten otsikoiden luominen  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sitovasti suun. tuotantotil.** ja valitse sitten liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Valitse **Nro**-kenttään seuraava numero sarjasta.  
4.  Valitse **Lähdetyyppi**-kentässä tuotantotilauksen lähde.

    Voit valita täällä tuotenimikeperheen tuotannon. Lisätietoja on kohdassa [Tuotantoperheiden käyttäminen](production-how-work-family.md).
5.  Valitse **Lähteen nro** -kentässä nimikenumero, tuoteperhe tai myynnin tunnistetiedot, jolle tuotantotilaus luodaan.  
6.  Täytä **Määrä**- ja **Eräpäivä**-kentät määritystesi mukaisesti.  

Kun tuotannon vaatimukset, kuten komponentit tai toiminnot, muuttuvat, voit suunnitella tuotantotilauksen nopeasti uudelleen. Lisätietoja on kohdassa [Tuotantotilausten suora uudelleensuunnittelu tai päivitys](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Katso myös  
[Tuotanto](production-manage-manufacturing.md)    
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)      
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
