---
title: Toistuvat vakio-ostorivit
description: Voit määrittää usein käytettäviä ostorivejä. Voit sitten lisätä ne ostoasiakirjoihin ja täyttää tällä tavoin vakiotiedot nopeasti.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, purchase, replenishment'
ms.search.form: 177
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Toistuvien ostorivien luominen

Jos sinun on usein luotava samankaltaisia tietoja sisältäviä ostorivejä, voit määrittää vakiorivejä ja lisätä ne sitten toistuviin ostoasiakirjoihin, kuten toistuviin täydennystilauksiin.

## Toistuvien ostorivien määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toistuvat ostorivit** ja valitse sitten vastaava linkki.
2. Valitse **Toistuvat ostorivit** -sivulla **Uusi**-toiminto.
3. Täytä **Yleiset**-pikavälilehdessä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kirjoita **Rivit**-pikavälilehden kenttiin esitiedot, jotka vastaavat vakiorivejä, joita odotat käyttäväsi toistuvina riveinä ostoasiakirjoissa.

> [!NOTE]
> Toistuvilla ostoriveillä ei voi määrittää hintoja, koska esimerkiksi hinnat ja alennukset lasketaan varsinaisissa ostoasiakirjoissa toistuvien ostorivien lisäämisen jälkeen.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## Toistuvien ostorivien määrittäminen toimittajalle

Määritä toimittajalle vähintään yksi toistuva ostorivi, jotta näitä rivejä voidaan liittää kyseisen toimittajan ostoasiakirjoihin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Toimittajat** ja valitse sitten vastaava linkki.
2. Avaa soveltuvan toimittajan kortti.
3. Valitse **Toistuvat ostorivit** -toiminto.
4. Valitse **Toistuvat ostorivit** -sivulla niiden toistuvien ostorivien koodit, joita haluat lisätä toimittajan ostoasiakirjoihin.
5. Täytä muut kentät ja määritä, milloin, miten ja missä toistuvia ostorivejä käytetään.
6. Voit valita neljässä kentässä, miten rivejä lisätään kuhunkin asiakirjatyyppiin valitsemalla jonkin seuraavista asetuksista:

|Asetus|Kuvaus|
|------|-----------|
|**Manuaalinen**|Toimittajalla olevat toistuvat ostorivit on valittava ja lisättävä manuaalisesti.|
|**Automaattinen**|Jos toimittajalla on useita toistuvia ostorivejä, saat ilmoituksen siitä, mistä lisättävä rivi voidaan valita. Jos toistuvia ostorivejä on vain yksi, se lisätään automaattisesti.<br /><br />Tämä toimii vain, jos uusi asiakirja luotiin asiakirjaluettelosta esimerkiksi valitsemalla **Uusi**-toiminto **Ostotilaukset**-sivulla. Se ei toimi, jos asiakirja luotiin esimerkiksi toimittajakortista.|
|**Kysy aina**|Ilmoitus avautuu ja kaikki aiemmin luodut toistuvat ostorivit näytetään. Voit sitten valita niistä yhden.

## Lisää toistuvia ostorivejä ostolaskulle

Jos toimittajalla on toistuvia ostorivejä, voit lisätä tai antaa lisätä niitä automaattisesti kaikenlaisiin ostoasiaakirjoihin, kuten ostolaskuihin. Jos olet aktivoinut **Kysy aina** -asetukset määrittäessäsi toistuvia ostorivejä toimittajille, saat ilmoituksen, jos toistuvia ostorivejä on.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.
2. Avaa ostolasku, johon haluat lisätä vähintään yhden vakio-ostorivin.
3. Valitse **Nouda toistuvat ostorivit** -toiminto.
4. Valitse **Toistuvat ostorivit** -sivun **Koodi**-kentässä hakupainike ja valitse sitten vakio-ostorivijoukko.
5. Lisää vakio-ostorivit laskuun valitsemalla **OK**. Voit sitten käyttää näitä rivejä sellaisenaan tai muokata rivien tietoja.

## Katso myös

[Osto](purchasing-manage-purchasing.md)  
[Oston määrittäminen](purchasing-setup-purchasing.md)  
[Luo toistuvia myyntejä](sales-how-work-standard-lines.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]