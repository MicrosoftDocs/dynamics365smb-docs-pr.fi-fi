---
title: Tuotannon nimikeperheiden käyttäminen | Microsoft Docs
description: Päätehtävä peruskalenterin räätälöimisessä yrityksellesi tai yhdelle sen liiketoimintakumppaneista on syöttää kaikki työskentely- ja ei-työskentelypäivätilan muutokset.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: b56ec1c5a0646c46ce5da71d35ebcff8bd01d476
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253514"
---
# <a name="work-with-production-families"></a>Tuotantoperheiden käsitteleminen
Tuoteperhe on ryhmä yksittäisiä nimikkeitä, joiden suhde perustuu niiden tuotantoprosessien samankaltaisuuteen. Tuoteperheitä muodostamalla joitain nimikkeitä voidaan tuottaa kaksi kertaa tai useammin yhdessä tuotannossa, joka optimoi materiaalinkulutusta.

Anna **Tuoteperhe**-sivun **Määrä**-kentässä määrä, joka tuotetaan, kun koko tuoteperhe on tuotettu kerran.

## <a name="example"></a>Esimerkki
Lävistysprosessissa saman nimikkeen neljä kappaletta voidaan tuottaa yhdestä lomakkeesta ja toisen, eri nimikkeen, 10 kappaletta yhtä aikaa. Lävistyskone lävistää kaikki 14 kappaletta saman työvaiheen aikana.

Tuoteperheiden muodostamisella vähennetään hukkatavaran määrää, koska se, mikä olisi tavallisesti hylättyä tavaraa isojen kappaleiden tuotannossa, käytetäänkin pienempien nimikkeiden tuottamisessa.

## <a name="to-set-up-a-production-family"></a>Tuotantoperheen määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Perheet** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a>Tuotanto tuoteperheen perusteella
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sitovasti suun. tuotantotil.** ja valitse sitten liittyvä linkki.
2. Luo uusi tuotantotilaus. Lisätietoja on kohdassa [Tuotantotilausten luominen](production-how-to-create-production-orders.md).
3. Valitse **Lähdetyyppi**-kentässä **Tuoteperhe**.  
4. Valitse **Lähdenro** -kentässä käsiteltävä tuotantoperhe.

## <a name="see-also"></a>Katso myös
[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Suunnittelu](production-planning.md)   
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
