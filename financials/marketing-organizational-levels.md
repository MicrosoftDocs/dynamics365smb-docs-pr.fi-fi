---
title: "Kontaktihenkilöiden organisaatiotasojen määrittäminen| Microsoft Docs"
description: "Voit määrittää organisaatiotason, ja kun se on määritetty kontaktille, voit ilmaista sen avulla, mikä on kontaktin asema yrityksessä (esimerkiksi ylin johto)."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d101076c8a51b1c7a79606d207f79a826c89bf29
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-organizational-levels-for-contact-persons"></a>Toimintaohje: Kontaktihenkilöiden organisaatiotasojen määrittäminen
Voit käyttää kontakteissa organisaatiotasoja (esimerkiksi ylin johto) kun haluat määrittää, missä asemassa he ovat yrityksessä. Voit käyttää näitä tietoja kontaktien tietojen syöttämisessä.

Kontaktien organisaatiotasojen käyttäminen on kaksivaiheinen prosessi. Ensin määritetään organisaatiotason koodi. Tämä vaihe suoritetaan vain kerran jokaiselle organisaatiotasolle. Kun organisaation koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.

## <a name="to-define-an-organizational-level-code"></a>Organisaatiotason koodin määrittäminen
Organisaatontason koodi määrittää organisaatiotason tyypin tai luokan. Se voi olla esimerkiksi TOIMITUSJOHTAJA tai TALOUSJOHTAJA. Organisaatiotason koodeja voi olla useita. Voit määrittää organisaatiotason **Organisaatiotasot**-ikkunan avulla.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Organisaatiotasot** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>Organisaatiotasojen määrittäminen kontaktihenkilölle
Organisaatiotasoja voi liittää vain kontaktihenkilöihin, ei kontaktiyrityksiin. Jokaiseen kontaktiin voi liittää vain yhden organisatorisen tason.

1. Avaa kontakti.
2. Valitse **Organisaatiotasot**-kentässä koodi, jonka haluat liittää.

Kun olet liittänyt kontakteihisi organisaatiotasoja, voit käyttää näitä tietoja luodessasi segmenttejä.

Kun olet liittänyt vastuualueita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Toimintaohje: Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[Kontaktihenkilöiden luominen](marketing-create-contact-persons.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

