---
title: Määritteiden määrittäminen ja niiden määrittäminen nimikkeille
description: Tässä ohjeaiheessa kerrotaan, miten esimerkiksi hakusanoina käytettävät nimikkeiden määritearvot määritetään ja miten ne sitten määritetään nimikkeille ja nimikeluokille.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.search.forms: 7507, 7509, 7506, 7505, 7503, 7502, 7510, 7504, 7501, 7500, 9110, 5734, 7508
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d2c8eec702840e6046eab362a867317091a9c3aa
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059358"
---
# <a name="work-with-item-attributes"></a>Nimikkeen määritteiden käsitteleminen
Kun asiakkaat tekevät kyselyjä nimikkeestä kirjeenvaihdon tai integroidun verkkokaupan avulla, he voivat tehdä kyselyjä ominaisuuksien, kuten korkeuden ja vuosimallin, perusteella. Voit auttaa asiakasta määrittämällä nimikkeisiin erilaisia nimikkeen määritteen arvoja, joita voidaan käyttää nimikkeiden haussa.

Voit myös määrittää nimikkeen määritteitä nimikeluokkiin, jotka kohdistetaan nimikeluokkia käyttäviin nimikkeisiin. Lisätietoja on kohdassa [Nimikkeen luokitteleminen](inventory-how-categorize-items.md).

> [!Tip]  
> Jos liität nimikkeisiin kuvia, kuvan analysointilaajennus havaitsee kuvassa olevat määritteet. Lisäksi se ehdottaa määritteitä, ja voit päättää, määritetäänkö ne. Laajennusta voi käyttää heti, kun olet ottanut sen käyttöön. Lisätietoja on kohdassa [Kuvan analysointilaajennus](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>Nimikkeen määritteiden luominen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen määritteet** ja valitse sitten vastaava linkki.
2. Valitse **Nimikkeen määritteet** -sivulla **Uusi**-toiminto.
3. Täytä **Nimikkeen määrite** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Jos valitset **Tyyppi**-kentässä **Asetus**, voit valita **Nimikkeen määritteen arvot** -toiminnon ja luoda nimikkeen määritteelle arvot. Lisätietoja on kohdassa [Arvojen luominen nimikkeen määritteille, joiden tyyppi on Asetus](inventory-how-work-item-attributes.md#to-create-values-for-item-attributes-of-type-option).  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Arvojen luominen nimikkeen määritteille, joiden tyyppi on Asetus
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen määritteet** ja valitse sitten vastaava linkki.
2. Valitse **Nimikkeen määritteet** -sivulla nimikkeen määrite, jonka tyyppi on **Asetus** ja jolle haluat määrittää arvot. Valitse sitten **Nimikkeen määritteen arvot** -toiminto.
3. Täytä **Nimikkeen määritteen arvot** -sivulla tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Nimikkeen määritteiden määrittäminen nimikkeille
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Valitse **Nimikkeet**-sivulla nimike, jolle haluat määrittää nimikkeen määritteet. Valitse sitten **Määritteet**-toiminto.
3. Valitse **Nimikkeen määritteen arvot** -sivulla **Uusi**-toiminto.
4. Valitse **Määrite**-kentässä valintapainike ja valitse aiemmin määritetty nimikkeen määrite. Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikkeen määritteen kohdassa [Nimikkeen määritteiden luominen](inventory-how-work-item-attributes.md#to-create-item-attributes) esitetyllä tavalla.
5. Anna **Arvo**-kentässä nimikkeen määritteen arvo, kuten 2010, kun kyseessä on **Mallivuosi**-määrite.
6. Valitse **Asetus**-tyyppisille nimikkeen määritteille **Arvo**-kentän valintapainike. Valitse sitten nimikkeen määritteen arvo. Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikkeen määritteen arvon kohdassa [Arvojen luominen nimikkeen määritteille, joiden tyyppi on Asetus](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-items) esitetyllä tavalla.
7. Toista vaiheet 4–6 kaikille niille nimikkeen määritteille, jotka haluat määrittää nimikkeeseen.

## <a name="to-assign-item-attributes-to-item-categories"></a>Nimikkeen määritteiden määrittäminen nimikeluokille
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikeluokat** ja valitse sitten vastaava linkki.
2. Valitse **Nimikeluokat**-sivulla nimikeluokka, jolle haluat määrittää nimikkeen määritteet. Valitse sitten **Muokkaa**-toiminto.
3. Valitse **Nimikeluokkakortti**-sivun **Määritteet**-pikavälilehdessä **Uusi**-toiminto.
4. Valitse **Määrite**-kentässä valintapainike ja valitse aiemmin määritetty nimikkeen määrite. Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikkeen määritteen kohdassa [Nimikkeen määritteiden luominen](inventory-how-work-item-attributes.md#to-create-item-attributes) esitetyllä tavalla.
5. Valitse **Oletusarvo**-kentässä valintapainike ja valitse nimikkeen määritteen arvo.
6. Toista vaiheet 4 ja 5 kaikille niille nimikkeen määritteille, jotka haluat määrittää nimikeluokkaan.

> [!NOTE]  
>   Päänimikeluokkien nimikkeen määritteet periytyvät alinimikeluokille. Tämä osoitetaan **Peritty kohteesta** -kentässä **Määritteet**-pikavälilehdessä. Lisätietoja on kohdassa [Nimikkeiden luokitteleminen](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Suodattaminen nimikkeen määritteiden mukaan
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Valitse **Nimikkeet**-sivulla **Suodata määritteiden mukaan** -toiminto.
3. Valitse **Suodata nimikkeet määritteen mukaan** -sivulla **Määrite**-kentän valintapainike. Valitse sitten nimikkeen määrite.
4. Valitse **Arvo**-kentässä ensin valintapainike ja sitten määritteen arvo, jonka mukaan nimikkeet suodatetaan.

    > [!NOTE]  
    >   Voit valita arvot vain suoraan niille nimikkeen määritteille, joilla on kiinteät arvot (esimerkiksi väri). Jos nimikkeen määritteillä on muuttuvat arvot (kuten leveys), nimikkeen määritteen arvo on määritettävä valitsemalla ensin ehto. Katso vaihe 5.
5. Valitse muuttuvan nimikkeen määritteen **Arvo**-kentässä valintapainike.
6. Valitse **Määritä suodatusarvo** -sivun **Ehto**-kentässä alanuolipainike ja valitse sitten ehto.
7. Syötä **Arvo**-kenttään määritteen arvo, jonka mukaan nimikkeet suodatetaan.

    **Esimerkki**: Voit suodattaa nimikkeet, joiden materiaalin kuvaus alkaa sanalla "sininen", täyttämällä kentät seuraavasti: **Määrite**-kenttä: Materiaalin kuvaus, **Ehto**-kenttä: Alkaa, **Arvo**-kenttä: sininen.
8. Valitse **OK**-painike.   

**Nimikkeet**-sivun nimikkeet suodatetaan määritettyjen nimikkeen määritteen arvojen mukaan.

## <a name="see-also"></a>Katso myös
[Nimikkeiden luokitteleminen](inventory-how-categorize-items.md)    
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]