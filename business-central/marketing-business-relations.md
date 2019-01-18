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
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-marketing
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 33743655f682aae9e02393aa68d04dffd334357b
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Liikesuhteiden määrittäminen kontaktiyrityksissä
Voit käyttää liikesuhteita, kun haluat osoittaa eri kontaktien, kuten prospektin, pankin, konsultin tai palvelun toimittajan, kanssa olevan liikesuhteen.

Kontaktien liikesuhteiden käyttäminen on kaksivaiheinen prosessi. Ensin määritetään liikesuhteen koodi. Tämä vaihe suoritetaan vain kerran jokaiselle liikesuhteelle. Kun liikesuhteen koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.

> [!NOTE]  
>   Jos aiot synkronisoida kontaktisi ohjelman muissa osissa olevien toimittajien, asiakkaiden tai pankkitilien kanssa, haluat ehkä määrittää niille liikesuhteen.

## <a name="to-define-a-business-relation-code"></a>Liikesuhteen koodin määrittäminen
Liikesuhteen koodi määrittää liikesuhteen luokan tai tyypin. Se voi olla esimerkiksi PANKKI tai LAKI. Liikesuhteen koodeja voi olla useita. Määritä liikesuhde **Liikesuhteet**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Liikesuhteet** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="AssignBusRelContact"></a> Liikesuhteiden määrittäminen kontaktille
Liikesuhteita ei voi liittää kontaktihenkilöön, vaan ainoastaan yrityksiin.

1. Avaa kontakti.
2. Valitse **Yritys**-toiminto ja sitten **Liikesuhteet**-toiminto.

    **Kontaktin liikesuhteet** -sivu avautuu.
3. Valitse **Liikesuhteen koodi** -kentässä liikesuhde, jonka haluat määrittää.

Toista nämä vaiheet ja luo niin monta liikesuhdetta kuin haluat. Voit myös liittää liikesuhteita kontaktiluettelosta saman menettelytavan avulla.

Kontaktille liitettyjen liikesuhteiden lukumäärä näkyy **Kontakti**-sivun **Segmentointi**-osan **Liikesuhteiden lkm** -kentässä.

Kun olet liittänyt liikesuhteita kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on ohjeaiheessa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

