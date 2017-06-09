---
title: "Toimialaryhmien määrittäminen kontaktiyrityksille | Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten toimialaryhmiä käytetään kontaktien kanssa Financialsissa"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34b81ec1e92eea67af13c7a2dfe03bdb97c8c59c
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-industry-groups-for-contact-companies"></a>Toimialaryhmien määrittäminen kontaktiyrityksille
Toimialaryhmien avulla osoitetaan, minkä tyyppiseen toimialaryhmään (esimerkiksi vähittäistavarakauppa ja autoteollisuus) kontaktit kuuluvat.

Kontaktien toimialaryhmien käyttäminen on kaksivaiheinen prosessi. Ensin määritetään toimialaryhmän koodi. Tämä vaihe suoritetaan vain kerran jokaiselle toimialaryhmälle. Kun toimialaryhmän koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.

**Huomautus:** Jos aiot synkronisoida kontaktisi ohjelman muissa osissa olevien toimittajien, asiakkaiden tai pankkitilien kanssa, haluat ehkä määrittää niille liikesuhteen.

## <a name="to-define-an-industry-group-code"></a>Toimialaryhmän koodin määrittäminen
Toimialaryhmän koodi määrittää ryhmän tyypin tai luokan, joka voi olla esimerkiksi mainonnalle MAINOS tai televisiolle ja radiolle TIED.VÄL. Toimialaryhmän koodeja voi olla useita. Voit määrittää toimialaryhmät **Toimialaryhmät**-ikkunan avulla.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Toimialaryhmät** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="AssignIndustryGroupContact"></a> Toimialaryhmien määrittäminen kontaktille
Toimialaryhmiä ei voi liittää kontaktihenkilöön, vaan ainoastaan yrityksiin.

1. Avaa kontakti.
2. Valitse **Yritys**-toiminto ja sitten **Toimialaryhmät**-toiminto. Näyttöön tulee **Kontaktin toimialaryhmät** -ikkuna.
3. Valitse **Toimialaryhmien koodi** -kentässä toimialaryhmät, jotka haluat liittää.

Toista nämä vaiheet ja luo niin monta toimialaryhmää kuin haluat. Voit luoda samaan tapaan toimialaryhmiä kontaktiluettelosta.

Kontaktille määritettyjen toimialaryhmien lukumäärä näkyy **Kontakti**-ikkunan **Segmentointi**-osan **Toimialaryhmien lkm** -kentässä.

Kun olet liittänyt toimialaryhmiä kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Toimintaohje: Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

