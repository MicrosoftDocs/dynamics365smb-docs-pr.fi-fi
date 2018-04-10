---
title: "Kontaktiyritysten verkkopalvelujen määrittäminen| Microsoft Docs"
description: "Voit määrittää internet- tai verkkolähteet ja määrittää ne kontaktiyritykseen. Tämä auttaa ilmaisemaan, miten haluat etsiä kontakteja koskevia tietoja."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4fb61c804d1f01326349d7733e52de48811c18e3
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a>Kontaktiyritysten verkkolähteiden määrittäminen
Voit käyttää verkkolähteitä (esimerkiksi hakukoneita ja verkkosivustoja) kontaktiyrityksissä silloin, kun haluat ilmaista, mistä aiot hakea tietoa kontakteistasi Internetissä. Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.

Kontaktien verkkolähteiden käyttäminen on kaksivaiheinen prosessi. Ensin määritetään verkkolähteen koodi. Tämä vaihe suoritetaan vain kerran jokaiselle verkkolähteelle. Kun verkkolähteen koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.

## <a name="to-define-a-web-source-code"></a>Verkkolähteen koodin määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Verkkolähteet** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Koodi**-, **Kuvaus**- ja **URL**-kentät.

    Kirjoita %1 **URL-osoite**-kenttään lisätäksesi hakusanan paikkamerkin URL-osoitekenttään. Kun avaat verkkolähteen kontaktista, %1 korvataan hakusanalla (esimerkiksi yrityksen nimellä), jonka syötit **Kontaktin verkkolähteet** -ikkunaan.

Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Verkkolähteiden määrittäminen kontaktiyritykselle
Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.

1. Avaa kontakti.
2. Valitse **Yritys**-toiminto ja valitse sitten **Verkkolähteet**-toiminto. Näyttöön tulee **Kontaktin verkkolähteet** -ikkuna.
3. Valitse **Verkkolähteen koodi** -kentässä verkkolähde, jonka haluat liittää.
4. Syötä **Hakusana**-kenttään se sana, jolla haluat ohjelman hakevan tietoa.

Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.

Voit liittää samaan tapaan verkkolähteitä myös **Kontaktiluettelo**-ikkunassa.

## <a name="see-also"></a>Katso myös
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
