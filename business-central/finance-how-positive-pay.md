---
title: Positive Pay -tiedostojen vieminen| Microsoft Docs
description: Voit varmistaa toimittaja- ja maksutiedot sisältävän Positive Pay -tiedoston viennin avulla, että pankki vahvistaa vain tarkistetut sekit ja summat.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: be71a8edc556708f88d00b088f49b52e2fd5ee45
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778916"
---
# <a name="export-a-positive-pay-file"></a>Positive Pay -tiedoston vienti
Kun viet toimittajan tiedot, sekin numeron ja maksun summan sisältävän Positive Pay -tiedoston, jonka sitten lähetät viitetiedoiksi pankkiin maksuja käsitellessäsi, voit varmistaa, että pankki vahvistaa vain tarkistetut sekit ja summat.

[!INCLUDE[d365fin](includes/d365fin_md.md)] on määritetty tukemaan Bank of American ja City Bankin Positive Pay -tiedostoja.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Positive Pay -pankkitilin määrittäminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilit** ja valitse sitten liittyvä linkki.
2. Avaa sen pankin kortti, jossa haluat käyttää Positive Pay -toimintoa.
3. Kirjoita **Positive Pay -vientikoodi** -kenttään POSPAYBANK.
4. Sulje sivu.

## <a name="to-export-a-positive-pay-file"></a>Positive Pay -tiedoston vienti
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilit** ja valitse sitten liittyvä linkki.
2. Valitse pankkitili, johon haluat viedä Positive Pay -tiedoston.
3. Valitse **Positive Pay, vienti** -toiminto.

    **Positive Pay, vienti** -sivu avautuu ja näkyvissä on maksut, jotka on tehty pankkitilille edellisen latauspäivän jälkeen (**Edellinen latauspvm**- ja **Edellinen latausaika** -kentät).
4. Määrittää**Latauksen katkaisupvm** -kenttää päivämäärä, jota edeltäviä maksuja ei sisällytetä vientitiedostoon.
5. Valitse **Vie**-toiminto.
6. Valitse **Vie tiedosto** -sivulla **Tallenna**-painike ja tallenna tiedosto sopivaan paikkaan.
7. Lataa tiedosto sähköisen pankin sivustoon.
8. Kirjoita muistiin tai kopioi vahvistusnumero, joka näkyy, kun tiedoston lataus on onnistunut.

Vietyjen Positive Pay -tietueiden näyttäminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilit** ja valitse sitten liittyvä linkki.
2. Valitse pankkitili, jonka Positive Pay -vientitietueet haluat näyttää.
3. Valitse **Positive Pay -tapahtumat** -toiminto.

    Kaikki pankkitilin Positive Pay -vientitietueet näkyvät **Positive Pay -tapahtumat** -sivulla.
4. Anna kunkin vientitietueen **Vahvistusnumero**-kenttään numero, jonka sait, kun tiedoston lataus pankkiin onnistui.
5. Voit tarkastella liittyviä maksurivejä valitsemalla **Positive Pay -tapahtuman tiedot** -toiminnon.

Positive Pay -tiedostojen uudelleenvienti

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilit** ja valitse sitten liittyvä linkki.
2. Valitse pankkitili, johon haluat viedä Positive Pay -tiedostot uudelleen.
3. Valitse **Positive Pay -tapahtumat** -toiminto.
4. Valitse uudelleenvietävä Positive Pay -vientitiedoston rivi.
5. Valitse **Positive Pay -tapahtumat** -sivulla **Vie Positive Pay -maksu uudelleen tiedostoon** -toiminto.

## <a name="see-also"></a>Katso myös
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
