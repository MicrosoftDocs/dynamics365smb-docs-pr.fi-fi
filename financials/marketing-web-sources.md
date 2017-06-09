---
title: "Kontaktiyritysten verkkopalvelujen määrittäminen | Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten kontaktien verkkolähteitä käytetään Financialsissa"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8a452619aeeee907cf61fd5d1a8fce409ad2e42d
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-web-sources-for-contact-companies"></a>Kontaktiyritysten verkkolähteiden määrittäminen
Voit käyttää verkkolähteitä (esimerkiksi hakukoneita ja verkkosivustoja) kontaktiyrityksissä silloin, kun haluat ilmaista, mistä aiot hakea tietoa kontakteistasi Internetissä. Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.

Kontaktien verkkolähteiden käyttäminen on kaksivaiheinen prosessi. Ensin määritetään verkkolähteen koodi. Tämä vaihe suoritetaan vain kerran jokaiselle verkkolähteelle. Kun verkkolähteen koodi on määritetty, voit aloittaa koodin liittämisen kontaktihenkilöille.

## <a name="to-define-a-web-source-code"></a>verkkolähteen koodin määrittäminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Verkkolähteet** ja valitse sitten liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä **Koodi**-, **Kuvaus**- ja **URL**-kentät.

    Kirjoita %1 **URL-osoite**-kenttään lisätäksesi hakusanan paikkamerkin URL-osoitekenttään. Kun avaat verkkolähteen kontaktista, %1 korvataan hakusanalla (esimerkiksi yrityksen nimellä), jonka syötit **Kontaktin verkkolähteet** -ikkunaan.

Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.

## <a name="to-assign-web-sources-to-a-contact-company"></a>verkkolähteiden määrittäminen kontaktiyritykselle
Kun liität verkkolähteitä, määritä, mitä hakukonetta ja hakusanaa sovellus käyttää hakiessaan pyydettyjä tietoja.

1. Avaa kontakti.
2. Valitse **Yritys**-toiminto ja valitse sitten **Verkkolähteet**-toiminto. Näyttöön tulee **Kontaktin verkkolähteet** -ikkuna.
3. Valitse **Verkkolähteen koodi** -kentässä verkkolähde, jonka haluat liittää.
4. Syötä **Hakusana**-kenttään se sana, jolla haluat ohjelman hakevan tietoa.

Toista nämä vaiheet ja luo niin monta verkkolähdettä kuin haluat.

Voit liittää samaan tapaan verkkolähteitä myös **Kontaktiluettelo**-ikkunassa.

## <a name="see-also"></a>Katso myös
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

