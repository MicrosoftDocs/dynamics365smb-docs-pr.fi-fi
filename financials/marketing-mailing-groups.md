---
title: "Kontaktien postitusryhmien määrittäminen| Microsoft Docs"
description: "Voit ilmaista postitusryhmien avulla ryhmät, joiden avulla määritetään samat tiedot saavat kontaktiryhmät esimerkiksi markkinointi- tai mainoskampanjaa varten."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bc1c89b87426b72ce4f9522cb7f0dc31c77acad1
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-mailing-groups-for-contacts"></a>Toimintaohje: Kontaktien postitusryhmien määrittäminen
Postitusryhmien avulla voi määrittää niiden kontaktien ryhmät, joiden haluat vastaanottavan samat tiedot. Voit määrittää esimerkiksi kontaktien postitusryhmän, jolle haluat lähettää ilmoituksen toimiston siirtämisestä, tai toisen ryhmän, jolle haluat lähettää lomalahjoja.

Kontaktien postitusryhmien käyttäminen on kaksivaiheinen prosessi. Ensin määritetään postitusryhmän koodi. Tämä vaihe suoritetaan vain kerran jokaiselle postitusryhmälle. Kun postitusryhmän koodi on määritetty, voit aloittaa koodin liittämisen kontaktiyrityksille.

## <a name="to-define-mailing-group-codes"></a>Postitusryhmän koodien määrittäminen
Postitusryhmän koodi määrittää ryhmän tyypin tai luokan. Se voi olla SIIRTO toimiston siirrolle tai LAHJA lomalahjalle. Toimialaryhmän koodeja voi olla useita. Voit määrittää toimialaryhmät **Postitusryhmät**-ikkunan avulla.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Postitusryhmät** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto. Täytä sitten koodi ja kuvaus. Koodi voi olla enintään 11 merkkiä pitkä. Se voi sisältää numeroita ja kirjaimia.

## <a name="AssignMailGroupContact"></a> Postitusryhmien määrittäminen kontaktiin
1. Avaa kontakti.
2. Valitse **Postitusryhmät**-toiminto. Näyttöön tulee **Kontaktin postitusryhmät** -ikkuna.
3. Valitse **Postitusryhmien koodi** -kentässä postitusryhmä, jonka haluat liittää.

Toista nämä vaiheet ja liitä niin monta postitusryhmää kuin haluat. Voit liittää samaan tapaan postitusryhmiä myös kontaktiluetteloista.

Kontaktiin liitettyjen postitusryhmien lukumäärä näytetään **Kontakti**-ikkunan **Segmentointi**-osan **Postitusryhmien lkm** -kentässä.

Kun olet liittänyt postitusryhmät kontakteihisi, voit käyttää näitä tietoja valitessasi kontakteja segmentteihisi. Lisätietoja on kohdassa [Toimintaohje: Kontaktien lisääminen segmentteihin](marketing-add-contact-segment.md).

## <a name="see-also"></a>Katso myös
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[Kontaktihenkilöiden luominen](marketing-create-contact-persons.md)  
[Financialsin käyttäminen](ui-work-product.md)

