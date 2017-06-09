---
title: "Kontaktihenkilöiden organisaatiotasojen määrittäminen | Microsoft Docs"
description: "Tässä artikkelissa kerrotaan Financialsin kontaktien organisaatiotasoista"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bde26a2d5fcb7ec10dcd70fdd30c74893bcb34d5
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-organizational-levels-for-contact-persons"></a>Kontaktihenkilöiden organisaatiotasojen määrittäminen
Voit käyttää kontakteissa organisaatiotasoja (esimerkiksi ylin johto) kun haluat määrittää, missä asemassa he ovat yrityksessä. Voit käyttää näitä tietoja kontaktien tietojen syöttämisessä.

Kontaktien organisaatiotasojen käyttäminen on kaksivaiheinen prosessi. Ensin määritetään organisaatiotason koodi. Tämä vaihe suoritetaan vain kerran jokaiselle organisaatiotasolle. Kun organisaation koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.

## <a name="to-define-an-organizational-level-code"></a>organisaatiotason koodin määrittäminen
Organisaatontason koodi määrittää organisaatiotason tyypin tai luokan. Se voi olla esimerkiksi TOIMITUSJOHTAJA tai TALOUSJOHTAJA. Organisaatiotason koodeja voi olla useita. Voit määrittää organisaatiotason **Organisaatiotasot**-ikkunan avulla.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Organisaation tasot** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>organisaatiotasojen liittäminen kontaktihenkilölle
Organisaatiotasoja voi liittää vain kontaktihenkilöihin, ei kontaktiyrityksiin. Jokaiseen kontaktiin voi liittää vain yhden organisatorisen tason.

1. Avaa kontakti.
2. Valitse **Organisaatiotasot**-kentässä koodi, jonka haluat liittää.

Kun olet liittänyt kontakteihisi organisaatiotasoja, voit käyttää näitä tietoja luodessasi segmenttejä.

Kun olet liittänyt vastuualueita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Toimintaohje: Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[Kontaktihenkilöiden luominen](marketing-create-contact-persons.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

