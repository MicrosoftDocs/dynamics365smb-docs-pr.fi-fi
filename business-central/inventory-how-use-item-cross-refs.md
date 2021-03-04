---
title: Nimikkeen viittausten käyttäminen
description: Määritä viittaukset niiden kuvauksien välille, joita sinä ja toimittajasi käytätte nimikkeelle, jotta voit lisätä toimittajan nimikekuvauksen ostoasiakirjoihin.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 7d670f6553a1bd70dcc3d97f90436f36c6627c56
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013790"
---
# <a name="use-item-cross-references"></a>Nimikkeen viittausten käyttäminen
Jos määrität viittauksen käyttämäsi nimikkeen nimikekuvauksen ja kyseisen nimikkeen toimittajan käyttämän kuvauksen välille, toimittajan nimikekuvaus lisätään automaattiesti toimittajan ostoasiakirjoihin, kun annat arvon **Viitenro** -kentässä. Myyntiasiakirjojen asiakkaan nimikenumeroissa käytetään samoja toimintoja.

Seuraavaksi käsitellään nimikkeen viittausten käyttämistä ostojen puolella. Ostojen puolen vaiheet ovat vastaavanlaiset.

> [!NOTE]
> Yhä yleisempää on, että tuotetunnisteet, kuten GTIN- tai GUID-tunnukset, sisältävät vähintään 30 merkkiä, mikä on enemmän kuin nykyinen ominaisuus, jota kohteen ristiviittaukset pystyvät käsittelemään. Jos tarvitset viittauksia, joissa on enemmän kuin 30 merkkiä, järjestelmänvalvoja voi ottaa käyttöön **Kirjoita pidempiä viitteitä** -ominaisuuden [Ominaisuuksien hallinta](https://businesscentral.dynamics.com/?page=2610) -sivulla (linkki edellyttää, että sinulla on [!INCLUDE[prod_short](includes/prod_short.md)] -vuokraaja). Viittausten käyttö ei muutu, mutta sivujen ja painikkeiden kaltaisten asioiden nimet muuttuvat. Esimerkiksi **Nimikkeen ristiviittaustapahtumat** -sivulta tulee **Nimikkeen viitetapahtumat** -sivu.

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
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]