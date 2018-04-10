---
title: "Kontaktien liikesuhteen koodien määrittäminen| Microsoft Docs"
description: "Voit käyttää Business Central -sovelluksen liikesuhteita markkinoinnissa. Niiden avulla voit ilmaista, minkälainen liikesuhde sinulla on prospektien ja asiakkaiden kanssa. Kyse voi olla esimerkiksi pankista tai palvelun toimittajasta."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f879d933822e061913975c1dbac2bf883ad9bbc1
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Liikesuhteiden määrittäminen kontaktiyrityksissä
Voit käyttää liikesuhteita, kun haluat osoittaa eri kontaktien, kuten prospektin, pankin, konsultin tai palvelun toimittajan, kanssa olevan liikesuhteen.

Kontaktien liikesuhteiden käyttäminen on kaksivaiheinen prosessi. Ensin määritetään liikesuhteen koodi. Tämä vaihe suoritetaan vain kerran jokaiselle liikesuhteelle. Kun liikesuhteen koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.

> [!NOTE]  
>   Jos aiot synkronisoida kontaktisi ohjelman muissa osissa olevien toimittajien, asiakkaiden tai pankkitilien kanssa, haluat ehkä määrittää niille liikesuhteen.

## <a name="to-define-a-business-relation-code"></a>Liikesuhteen koodin määrittäminen
Liikesuhteen koodi määrittää liikesuhteen luokan tai tyypin. Se voi olla esimerkiksi PANKKI tai LAKI. Liikesuhteen koodeja voi olla useita. Määritä liikesuhde **Liikesuhteet**-ikkunassa.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Liikesuhteet** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="AssignBusRelContact"></a> Liikesuhteiden määrittäminen kontaktille
Liikesuhteita ei voi liittää kontaktihenkilöön, vaan ainoastaan yrityksiin.

1. Avaa kontakti.
2. Valitse **Yritys**-toiminto ja sitten **Liikesuhteet**-toiminto.

    **Kontaktin liikesuhteet** -ikkuna avautuu.
3. Valitse **Liikesuhteen koodi** -kentässä liikesuhde, jonka haluat määrittää.

Toista nämä vaiheet ja luo niin monta liikesuhdetta kuin haluat. Voit myös liittää liikesuhteita kontaktiluettelosta saman menettelytavan avulla.

Kontaktille liitettyjen liikesuhteiden lukumäärä näkyy **Kontakti**-ikkunan **Segmentointi**-osan **Liikesuhteiden lkm** -kentässä.

Kun olet liittänyt liikesuhteita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on ohjeaiheessa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
