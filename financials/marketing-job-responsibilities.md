---
title: "Kontaktien vastuualueiden määrittäminen | Microsoft Docs"
description: "Tässä artikkelissa kerrotaan kontaktien vastuualueista Financialsissa"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 610ae314502e60b959f0e2ff705a48b936d79d68
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-job-responsibilities-for-contact-persons"></a>Kontaktihenkilöiden vastuualueiden määrittäminen
Voit lisätä kontaktihenkilöiden vastuualueiden tietoja, kun haluat osoittaa, mistä kontaktihenkilö vastaa yrityksessä (esimerkiksi IT, hallinto tai tuotanto). Voit käyttää näitä tietoja kontaktien tietojen syöttämisessä.

Kontaktien vastuualueiden käyttäminen on kaksivaiheinen prosessi. Ensin määritetään vastuualueen koodi. Tämä vaihe suoritetaan vain kerran jokaiselle vastuualueelle. Kun vastuualueen koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.

## <a name="tp-define-a-job-responsibility-code"></a>vastuualueen koodin määrittäminen
Vastuualueen koodi määrittää työn tyypin tai luokan. Se voi olla esimerkiksi MARKKINOINTI tai OSTO. Vastuualueen koodeja voi olla useita. Voit määrittää vastuualueen **Vastuualueet**-ikkunassa.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Vastuualueet** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a>vastuualueiden määrittäminen kontaktihenkilöihin
Et voi liittää vastuualueita kontaktiyrityksiin.

1. Avaa yhteyshenkilö.
2. Valitse **Henkilö**-toiminto ja valitse sitten **Vastuualueet**-toiminto. Näyttöön tulee **Kontaktin tehtäväalueet** -ikkuna.
3. Valitse **Vastuualueen koodi** -kentässä vastuualue, jonka haluat liittää.

Toista nämä vaiheet ja luo niin monta vastuualuetta kuin haluat. Voit liittää samaan tapaan vastuualueita myös kontaktiluettelosta.

Kontaktille liittämiesi vastuualueiden lukumäärä näkyy **Yhteyshenkilö**-ikkunan **Segmentointi**-osan **Vastuualueiden lkm** -kentässä.

Kun olet liittänyt vastuualueita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Toimintaohje: Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktihenkilöiden luominen](marketing-create-contact-persons.md)  
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[Financialsin käyttäminen](ui-work-product.md)
