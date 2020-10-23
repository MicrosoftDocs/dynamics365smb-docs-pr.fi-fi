---
title: Nimikkeiden viittausten käyttäminen | Microsoft Docs
description: Määritä viittaukset niiden kuvauksien välille, joita sinä ja toimittajasi käytätte nimikkeelle, jotta voit lisätä toimittajan nimikekuvauksen ostoasiakirjoihin.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 056897c799dd12755432637690446a0797c9f18c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919436"
---
# <a name="use-item-cross-references"></a>Nimikkeen viittausten käyttäminen
Jos määrität viittauksen käyttämäsi nimikkeen nimikekuvauksen ja kyseisen nimikkeen toimittajan käyttämän kuvauksen välille, toimittajan nimikekuvaus lisätään automaattiesti toimittajan ostoasiakirjoihin, kun annat arvon **Viitenro** -kentässä. Myyntiasiakirjojen asiakkaan nimikenumeroissa käytetään samoja toimintoja.

Seuraavaksi käsitellään nimikkeen viittausten käyttämistä ostojen puolella. Ostojen puolen vaiheet ovat vastaavanlaiset.

> [!NOTE]
> Yhä yleisempää on, että tuotetunnisteet, kuten GTIN- tai GUID-tunnukset, sisältävät vähintään 30 merkkiä, mikä on enemmän kuin nykyinen ominaisuus, jota kohteen ristiviittaukset pystyvät käsittelemään. Jos tarvitset viittauksia, joissa on enemmän kuin 30 merkkiä, järjestelmänvalvoja voi ottaa käyttöön **Kirjoita pidempiä viitteitä** -ominaisuuden [Ominaisuuksien hallinta](https://businesscentral.dynamics.com/?page=xzy) -sivulla (linkki edellyttää, että sinulla on [!INCLUDE[d365fin](includes/d365fin_md.md)] -vuokraaja). Viittausten käyttö ei muutu, mutta sivujen ja painikkeiden kaltaisten asioiden nimet muuttuvat. Esimerkiksi **Nimikkeen ristiviittaustapahtumat** -sivulta tulee **Nimikkeen viitetapahtumat** -sivu.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Nimikkeen viittauksen määrittäminen toimittajan nimikkeen kuvaukseen.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jolle haluat luoda viittauksen toimittajan kyseistä nimikettä koskevaan nimikkeen kuvaukseen.
3. Valitse **Ristiviittaukset**-toiminto.

     Jos **Ristiviittaukset**-toimintoa ei löydy, valitse lisäasetusten näyttäminen ja etsi se sitten kohdassa **Liittyvät** > **Nimike**.
  
4. Täytä **Nimikkeen viittaustapahtumat** -sivun uudella rivillä kenttiä tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Toimittajan nimikkeen kuvauksen antaminen ostotilauksessa

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.
2. Luo ostotilaus toimittajalle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.
3. Luo ostorivi nimikkeelle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.
4. Valitse **Viittauksen tyypin nro** -kentässä nimikkeen viittaus, jonka loit, ja valitse sitten **OK**-painike.

Rivin **Kuvaus**-kentän tiedot on korvattu toimittajan nimikkeen kuvauksella nimikkeen viittaustapauksessa määritetyllä tavalla.

## <a name="see-also"></a>Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
