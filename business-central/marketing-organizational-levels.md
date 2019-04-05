---
title: Kontaktihenkilöiden organisaatiotasojen määrittäminen| Microsoft Docs
description: Voit määrittää organisaatiotason, ja kun se on määritetty kontaktille, voit ilmaista sen avulla, mikä on kontaktin asema yrityksessä (esimerkiksi ylin johto).
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: be0bde09790c68730167709e1e82562a9a39c4e6
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "795715"
---
# <a name="set-up-organizational-levels-for-contact-persons"></a>Kontaktihenkilöiden organisaatiotasojen määrittäminen
Voit käyttää kontakteissa organisaatiotasoja (esimerkiksi ylin johto) kun haluat määrittää, missä asemassa he ovat yrityksessä. Voit käyttää näitä tietoja kontaktien tietojen syöttämisessä.

Kontaktien organisaatiotasojen käyttäminen on kaksivaiheinen prosessi. Ensin määritetään organisaatiotason koodi. Tämä vaihe suoritetaan vain kerran jokaiselle organisaatiotasolle. Kun organisaation koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.

## <a name="to-define-an-organizational-level-code"></a>Organisaatiotason koodin määrittäminen
Organisaatontason koodi määrittää organisaatiotason tyypin tai luokan. Se voi olla esimerkiksi TOIMITUSJOHTAJA tai TALOUSJOHTAJA. Organisaatiotason koodeja voi olla useita. Voit määrittää organisaatiotason **Organisaatiotasot**-sivun avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Organisaation tasot** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>Organisaatiotasojen määrittäminen kontaktihenkilölle
Organisaatiotasoja voi liittää vain kontaktihenkilöihin, ei kontaktiyrityksiin. Jokaiseen kontaktiin voi liittää vain yhden organisatorisen tason.

1. Avaa kontakti.
2. Valitse **Organisaatiotasot**-kentässä koodi, jonka haluat liittää.

Kun olet liittänyt kontakteihisi organisaatiotasoja, voit käyttää näitä tietoja luodessasi segmenttejä.

Kun olet liittänyt vastuualueita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktien luominen](marketing-create-contact-companies.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
