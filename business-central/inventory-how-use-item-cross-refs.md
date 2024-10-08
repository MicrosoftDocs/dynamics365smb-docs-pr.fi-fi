---
title: Nimikeviittausten käyttäminen
description: 'Viitteiden määrittäminen niiden kuvausten, mittayksiköiden ja varianttien välille, joita sekä sinä että toimittaja tai asiakas käyttää nimikkeessä.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 05/16/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="use-item-references"></a>Nimikeviittausten käyttäminen

Jos ostat tai myyt nimikkeitä, joissa sinä sekä toimittaja tai asiakas käyttävät erilaisia ehtoja, nimikkeiden ehtojen ja kyseisen nimikkeen asiakkaan tai toimittajan käyttämien ehtojen välille voidaan määrittää viittaus. Tällä tavoin toimittajan tai asiakkaan nimikkeen kuvaus, mittayksikkö tai varianttikoodi lisätään automaattisesti soveltuviin asiakirjoihin, kun tiedot annetaan **Nimikeviittauksen nro** -kentässä.  

## <a name="to-set-up-an-item-reference"></a>Nimikeviittauksen määrittäminen

1. Valitse :::image type="icon" source="media/ui-search/search_small.png" border="false":::-kuvake, kirjoita **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jolle haluat luoda viittauksen.
3. Valitse **Nimikeviittaukset** -toiminto.

     Jos et löydä **Nimikeviittaus-toimintoa**, voit tarkastella useita vaihtoehtoja ja etsiä sen aiheeseen liittyvä **nimike -kohdasta** > **·**.
  
4. Täytä **Nimikkeen viittaustapahtumat** -sivun uudella rivillä kenttiä tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Seuraavaksi käsitellään nimikeviittauksen määrittämistä ostotilauksessa. Vastaavat ohjeet koskevat myyntiasiakirjoja ja muita ostoasiakirjoja.  

## <a name="to-enter-a-vendors-item-description-on-a-document"></a>Toimittajan nimikekuvauksen antaminen asiakirjassa

1. Valitse :::image type="icon" source="media/ui-search/search_small.png" border="false":::-kuvake, kirjoita **Ostotilaukset** ja valitse sitten liittyvä linkki.
2. Luo ostotilaus toimittajalle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.
3. Luo ostorivi nimikkeelle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.
4. Nimikeviittauksen nro -kentässä **·** -kentässä liittyvä nimikeviittaus ja valitse sitten **OK**-painike.

Rivin **Kuvaus**-kentän tiedot on korvattu toimittajan nimikkeen kuvauksella nimikkeen viittaustapauksessa määritetyllä tavalla. Jos nimikeviittaus sisältää varianttikoodin tai mittayksikön, myös nämä arvot kopioidaan asiakirjaan.  

## <a name="scan-barcodes-with-the-business-central-mobile-app"></a>Viivakoodien skannaaminen Business Central -mobiilisovelluksen kanssa

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Seuraavassa taulukossa ovat sivut, jotka tukevat nimikeviittausten viivakoodien lukemista [!INCLUDE [prod_short](includes/prod_short.md)] -mobiilisovelluksessa.

|Sivu  |Kenttäarvo, jonka voi lukea  |
|---------|---------|
|Nimikeviittaus     | Viittauksen nro        |
|Nimikepäiväkirjan rivi     | Nimikeviittauksen nro        |
|Inventointitilausrivi     |Nimikeviittauksen nro         |
|Ostorivi     |   Nimikeviittauksen nro      |
|Myyntirivi     | Nimikeviittauksen nro        |

## <a name="see-also"></a>Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
