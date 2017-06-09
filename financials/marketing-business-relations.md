---
title: "Kontaktien liikesuhteiden määrittäminen | Microsoft Docs"
description: "Tässä artikkelissa kerrotaan kontaktien liikesuhteista Financialsissa"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f6719ac45f298d6c952427c871eaf818cb7480c3
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-business-relations-on-contact-companies"></a>Liikesuhteiden määrittäminen kontaktiyrityksissä
Voit käyttää liikesuhteita, kun haluat osoittaa eri kontaktien, kuten prospektin, pankin, konsultin tai palvelun toimittajan, kanssa olevan liikesuhteen.

Kontaktien liikesuhteiden käyttäminen on kaksivaiheinen prosessi. Ensin määritetään liikesuhteen koodi. Tämä vaihe suoritetaan vain kerran jokaiselle liikesuhteelle. Kun liikesuhteen koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.

**Huomautus**: Jos aiot synkronisoida kontaktisi ohjelman muissa osissa olevien toimittajien, asiakkaiden tai pankkitilien kanssa, haluat ehkä määrittää niille liikesuhteen.

## <a name="to-define-a-business-relation-code"></a>Liikesuhteen koodin määrittäminen
Liikesuhteen koodi määrittää liikesuhteen luokan tai tyypin. Se voi olla esimerkiksi PANKKI tai LAKI. Liikesuhteen koodeja voi olla useita. Määritä liikesuhde **Liikesuhteet**-ikkunassa.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Liikesuhteet** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="AssignBusRelContact"></a> Liikesuhteiden määrittäminen kontaktille
Liikesuhteita ei voi liittää kontaktihenkilöön, vaan ainoastaan yrityksiin.

1. Avaa kontakti.
2. Valitse **Yritys**-toiminto ja sitten **Liikesuhteet**-toiminto.

    **Kontaktin liikesuhteet** -ikkuna avautuu.
3. Valitse **Liikesuhteen koodi** -kentässä liikesuhde, jonka haluat määrittää.

Toista nämä vaiheet ja luo niin monta liikesuhdetta kuin haluat. Voit myös liittää liikesuhteita kontaktiluettelosta saman menettelytavan avulla.

Kontaktille liitettyjen liikesuhteiden lukumäärä näkyy **Kontakti**-ikkunan **Segmentointi**-osan **Liikesuhteiden lkm** -kentässä.

Kun olet liittänyt liikesuhteita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Toimintaohje: Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

