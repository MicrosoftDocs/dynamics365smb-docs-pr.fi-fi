---
title: Käytä nimikeviittauksia
description: 'Viitteiden määrittäminen niiden kuvausten, mittayksiköiden ja varianttien välille, joita sekä sinä että toimittaja tai asiakas käyttää nimikkeessä.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/27/2021
ms.author: edupont
---
# Käytä nimikeviittauksia

Jos ostat tai myyt nimikkeitä, joissa sinä sekä toimittaja tai asiakas käyttävät erilaisia ehtoja, nimikkeiden ehtojen ja kyseisen nimikkeen asiakkaan tai toimittajan käyttämien ehtojen välille voidaan määrittää viittaus. Tällä tavoin toimittajan tai asiakkaan nimikkeen kuvaus, mittayksikkö tai varianttikoodi lisätään automaattisesti soveltuviin asiakirjoihin, kun tiedot annetaan **Nimikeviittauksen nro** -kentässä.  

> [!NOTE]
> [!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]
>
> Kaikki yritykset eivät käytä nimikeviitteitä. Sivut pidetään mahdollisimman selkeinä piilottamalla liittyvät kentät ja toiminnot oletusarvoisesti. Jos päätät käyttää niitä, valitse **Käytä nimikeviitteitä** -kenttä **Varastonhallinnan asetukset** -sivulla. Kun nimikeviitteet on otettu käyttöön, kentät ja toiminnot ovat käytettävissä nimikekortin, toimittajakortin ja asiakaskortin sivuilla sekä myynti- ja ostoasiakirjoissa.
>
> Vuoden 2021 2. julkaisuaaltoa edeltävissä versioissa järjestelmänvalvoja voi ottaa käyttöön *Kirjoita pidempiä viitteitä* -ominaisuuden [Ominaisuuksien hallinta](https://businesscentral.dynamics.com/?page=2610) -sivulla (linkki edellyttää, että sinulla on [!INCLUDE [prod_short](includes/prod_short.md)] -vuokraaja). Viittausten käyttö ei muutu, mutta sivujen ja painikkeiden kaltaisten asioiden nimet muuttuvat. Esimerkiksi **Nimikkeen ristiviittaustapahtumat** -sivulta tulee **Nimikkeen viitetapahtumat** -sivu.

## Voit alkaa käyttää nimikeviitteitä seuraavasti

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

1. Valitse :::image type="icon" source="media/ui-search/search_small.png" border="false":::-kuvake, kirjoita **Varastonhallinnan asetukset** ja valitse sitten liittyvä linkki.
2. Valitse **Käytä nimikeviittauksia** -kenttä.

## Nimikeviittauksen määrittäminen

1. Valitse :::image type="icon" source="media/ui-search/search_small.png" border="false":::-kuvake, kirjoita **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jolle haluat luoda viittauksen.
3. Valitse **Nimikeviittaukset** -toiminto.

     Jos **Nimikeviittaukset**-toimintoa ei löydy, valitse lisäasetusten näyttäminen ja etsi se sitten kohdassa **Liittyvät** > **Nimike**.
  
4. Täytä **Nimikkeen viittaustapahtumat** -sivun uudella rivillä kenttiä tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Seuraavaksi käsitellään nimikeviittauksen määrittämistä ostotilauksessa. Vastaavat ohjeet koskevat myyntiasiakirjoja ja muita ostoasiakirjoja.  

## Toimittajan nimikekuvauksen antaminen asiakirjassa

1. Valitse :::image type="icon" source="media/ui-search/search_small.png" border="false":::-kuvake, kirjoita **Ostotilaukset** ja valitse sitten liittyvä linkki.
2. Luo ostotilaus toimittajalle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.
3. Luo ostorivi nimikkeelle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.
4. Valitse **Nimikeviittauksen nro** -kentässä liittyvä nimikeviittaus ja valitse sitten **OK**-painike.

Rivin **Kuvaus**-kentän tiedot on korvattu toimittajan nimikkeen kuvauksella nimikkeen viittaustapauksessa määritetyllä tavalla. Jos nimikeviittaus sisältää varianttikoodin tai mittayksikön, myös nämä arvot kopioidaan asiakirjaan.  

## Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]