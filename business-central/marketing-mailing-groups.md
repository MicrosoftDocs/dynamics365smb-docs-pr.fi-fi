---
title: "Kontaktien postitusryhmien määrittäminen| Microsoft Docs"
description: "Voit ilmaista postitusryhmien avulla ryhmät, joiden avulla määritetään samat tiedot saavat kontaktiryhmät esimerkiksi markkinointi- tai mainoskampanjaa varten."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7f40b94cef953b22684ddcc744de0cfbdb8e0f20
ms.contentlocale: fi-fi
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a>Kontaktien postitusryhmien määrittäminen
Postitusryhmien avulla voi määrittää niiden kontaktien ryhmät, joiden haluat vastaanottavan samat tiedot. Voit määrittää esimerkiksi kontaktien postitusryhmän, jolle haluat lähettää ilmoituksen toimiston siirtämisestä, tai toisen ryhmän, jolle haluat lähettää lomalahjoja.

Kontaktien postitusryhmien käyttäminen on kaksivaiheinen prosessi. Ensin määritetään postitusryhmän koodi. Tämä vaihe suoritetaan vain kerran jokaiselle postitusryhmälle. Kun postitusryhmän koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.

## <a name="to-define-mailing-group-codes"></a>Postitusryhmän koodien määrittäminen
Postitusryhmän koodi määrittää ryhmän tyypin tai luokan. Se voi olla SIIRTO toimiston siirrolle tai LAHJA lomalahjalle. Toimialaryhmän koodeja voi olla useita. Voit määrittää toimialaryhmät **Postitusryhmät**-sivun avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Postitusryhmät** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="AssignMailGroupContact"></a> Postitusryhmien määrittäminen kontaktiin
1. Avaa kontakti.
2. Valitse **Postitusryhmät**-toiminto. Näyttöön tulee **Kontaktin postitusryhmät** -sivu.
3. Valitse **Postitusryhmien koodi** -kentässä postitusryhmä, jonka haluat liittää.

Toista nämä vaiheet ja liitä niin monta postitusryhmää kuin haluat. Voit liittää samaan tapaan postitusryhmiä myös kontaktiluetteloista.

Kontaktiin liitettyjen postitusryhmien lukumäärä näytetään **Kontakti**-sivun **Segmentointi**-osan **Postitusryhmien lkm** -kentässä.

Kun olet liittänyt postitusryhmät kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on ohjeaiheessa [Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[Kontaktihenkilöiden luominen](marketing-create-contact-persons.md)  
[Business Central -sovelluksen käyttäminen](ui-work-product.md)

