---
title: Toimialaryhmien määrittäminen kontaktiyrityksille| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten toimialaryhmä määritetään ja miten sille sitten määritetään kontaktiryhmä, kuten vähittäistavarakauppa tai autoteollisuus.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 9d1f685dce54db493e830096ef5d4749f0fc221a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309026"
---
# <a name="set-up-industry-groups-for-contact-companies"></a>Kontaktiyritysten toimialaryhmien määrittäminen
Toimialaryhmien avulla osoitetaan, minkä tyyppiseen toimialaryhmään (esimerkiksi vähittäistavarakauppa ja autoteollisuus) kontaktit kuuluvat.

Kontaktien toimialaryhmien käyttäminen on kaksivaiheinen prosessi. Ensin määritetään toimialaryhmän koodi. Tämä vaihe suoritetaan vain kerran jokaiselle toimialaryhmälle. Kun toimialaryhmän koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.

> [!NOTE]  
>   Jos aiot synkronisoida kontaktisi ohjelman muissa osissa olevien toimittajien, asiakkaiden tai pankkitilien kanssa, haluat ehkä määrittää niille liikesuhteen.

## <a name="to-define-an-industry-group-code"></a>Toimialaryhmän koodin määrittäminen
Toimialaryhmän koodi määrittää ryhmän tyypin tai luokan, joka voi olla esimerkiksi mainonnalle MAINOS tai televisiolle ja radiolle TIED.VÄL. Toimialaryhmän koodeja voi olla useita. Voit määrittää toimialaryhmät **Toimialaryhmät**-sivun avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimialaryhmät** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="AssignIndustryGroupContact"></a> Toimialaryhmien määrittäminen kontaktille
Toimialaryhmiä ei voi liittää kontaktihenkilöön, vaan ainoastaan yrityksiin.

1. Avaa kontakti.
2. Valitse **Yritys**-toiminto ja sitten **Toimialaryhmät**-toiminto. Näyttöön tulee **Kontaktin toimialaryhmät** -sivu.
3. Valitse **Toimialaryhmien koodi** -kentässä toimialaryhmät, jotka haluat liittää.

Toista nämä vaiheet ja luo niin monta toimialaryhmää kuin haluat. Voit luoda samaan tapaan toimialaryhmiä kontaktiluettelosta.

Kontaktille määritettyjen toimialaryhmien lukumäärä näkyy **Kontakti**-sivun **Segmentointi**-osan **Toimialaryhmien lkm** -kentässä.

Kun olet liittänyt toimialaryhmiä kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktien luominen](marketing-create-contact-companies.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
