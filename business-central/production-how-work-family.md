---
title: Tuotannon nimikeperheiden käyttäminen | Microsoft Docs
description: Päätehtävä peruskalenterin räätälöimisessä yrityksellesi tai yhdelle sen liiketoimintakumppaneista on syöttää kaikki työskentely- ja ei-työskentelypäivätilan muutokset.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f33ac3e581325eb714af67ee7040157a61e59fc7
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758865"
---
# <a name="work-with-production-families"></a>Tuotantoperheiden käsitteleminen
Tuoteperhe on ryhmä yksittäisiä nimikkeitä, joiden suhde perustuu niiden tuotantoprosessien samankaltaisuuteen. Tuoteperheitä muodostamalla joitain nimikkeitä voidaan tuottaa kaksi kertaa tai useammin yhdessä tuotannossa, joka optimoi materiaalinkulutusta.

Anna **Tuoteperhe**-sivun **Määrä**-kentässä määrä, joka tuotetaan, kun koko tuoteperhe on tuotettu kerran.

## <a name="example"></a>Esimerkki
Lävistysprosessissa saman nimikkeen neljä kappaletta voidaan tuottaa yhdestä lomakkeesta ja toisen, eri nimikkeen, 10 kappaletta yhtä aikaa. Lävistyskone lävistää kaikki 14 kappaletta saman työvaiheen aikana.

Tuoteperheiden muodostamisella vähennetään hukkatavaran määrää, koska se, mikä olisi tavallisesti hylättyä tavaraa isojen kappaleiden tuotannossa, käytetäänkin pienempien nimikkeiden tuottamisessa.

## <a name="to-set-up-a-production-family"></a>Tuotantoperheen määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Perheet** ja valitse sitten liittyvä linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a>Tuotanto tuoteperheen perusteella
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Sitovasti suunn. tuotantotil.** ja valitse sitten liittyvä linkki.
2. Luo uusi tuotantotilaus. Lisätietoja on kohdassa [Tuotantotilausten luominen](production-how-to-create-production-orders.md).
3. Valitse **Lähdetyyppi**-kentässä **Tuoteperhe**.  
4. Valitse **Lähdenro** -kentässä käsiteltävä tuotantoperhe.

## <a name="see-also"></a>Katso myös
[Tuotannon tuoterakenteiden luominen](production-how-to-create-production-boms.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Suunnittelu](production-planning.md)   
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]