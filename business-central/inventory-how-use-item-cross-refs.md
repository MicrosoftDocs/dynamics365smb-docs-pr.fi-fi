---
title: Käytä nimikeviittauksia
description: Määritä viittaukset niiden kuvauksien välille, joita sinä ja toimittajasi käytätte nimikkeelle, jotta voit lisätä toimittajan nimikekuvauksen ostoasiakirjoihin.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4eed6fce594b0b6835020fcdddb7275489b4d160
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588599"
---
# <a name="use-item-references"></a>Käytä nimikeviittauksia
Jos määrität viittauksen käyttämäsi nimikkeen nimikekuvauksen ja kyseisen nimikkeen toimittajan käyttämän kuvauksen välille, toimittajan nimikekuvaus lisätään automaattiesti toimittajan ostoasiakirjoihin, kun annat arvon **Nimikkeen viitenro** -kentässä. Myyntiasiakirjojen asiakkaan nimikenumeroissa käytetään samoja toimintoja.

Seuraavaksi käsitellään nimikkeen viittausten käyttämistä ostojen puolella. Ostojen puolen vaiheet ovat vastaavanlaiset.

> [!NOTE]
> Kaikki yritykset eivät käytä nimikeviitteitä, joten sivujen sotkun vähentämiseksi olemme piilottaneet liittyvät kentät ja toiminnot. Jos päätät käyttää niitä, voit ottaa käyttöön **Käytä nimikeviitteitä** -valitsimen **Varastonhallinnan asetukset** -sivulla. Kun olet ottanut nimikeviitteet käyttöön, kentät ja toiminnot ovat käytettävissä nimikekortin, toimittajakortin ja asiakaskortin sivuilla sekä myynti- ja ostoasiakirjoissa.

## <a name="to-start-using-item-references"></a>Voit alkaa käyttää nimikeviitteitä seuraavasti
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten vastaava linkki.
2. Ota käyttöön **Käytä nimikeviitteitä** -valitsin.

## <a name="to-set-up-an-item-reference-to-a-vendors-item-description"></a>Nimikkeen viittauksen määrittäminen toimittajan nimikkeen kuvaukseen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Avaa sen nimikkeen kortti, jolle haluat luoda viittauksen toimittajan kyseistä nimikettä koskevaan nimikkeen kuvaukseen.
3. Valitse **Nimikeviittaukset** -toiminto.

     Jos **Nimikeviittaukset**-toimintoa ei löydy, valitse lisäasetusten näyttäminen ja etsi se sitten kohdassa **Liittyvät** > **Nimike**.
  
4. Täytä **Nimikkeen viittaustapahtumat** -sivun uudella rivillä kenttiä tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Toimittajan nimikkeen kuvauksen antaminen ostotilauksessa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.
2. Luo ostotilaus toimittajalle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.
3. Luo ostorivi nimikkeelle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.
4. Valitse **Nimikeviittauksen nro** -kentässä nimikkeen viittaus, jonka loit, ja valitse sitten **OK**-painike.

Rivin **Kuvaus**-kentän tiedot on korvattu toimittajan nimikkeen kuvauksella nimikkeen viittaustapauksessa määritetyllä tavalla.

## <a name="see-also"></a>Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]