---
title: "Toimintaohje: Nimikkeen määritteiden käsitteleminen| Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten nimikkeen määritteet määritetään ja määritetään nimikkeisiin ja nimikeluokkiin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 04/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 82fee2e5b1ae3e87e607cd930973a8be32045e71
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-item-attributes"></a>Toimintaohje: Nimikkeen määritteiden käsitteleminen
Kun asiakkaat tekevät kyselyjä nimikkeestä kirjeenvaihdon tai integroidun verkkokaupan avulla, he voivat tehdä kyselyjä ominaisuuksien, kuten korkeuden ja vuosimallin, perusteella. Voit auttaa asiakasta määrittämällä nimikkeisiin erilaisia nimikkeen määritteen arvoja, joita voidaan käyttää nimikkeiden haussa.

Voit myös määrittää nimikkeen määritteitä nimikeluokkiin, jotka kohdistetaan nimikeluokkia käyttäviin nimikkeisiin. Lisätietoja on ohjeaiheessa [Toimintaohje: Nimikkeen luokitteleminen](inventory-how-categorize-items.md).

## <a name="to-create-item-attributes"></a>Nimikkeen määritteiden luominen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeen määritteet** ja valitse sitten liittyvä linkki.
2. Valitse **Nimikkeen määritteet** -ikkunassa **Uusi**-toiminto.
3. Täytä **Nimikkeen määrite** -ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Huomautus**: Jos valitset **Asetus**-kohdan **Tyyppi**-kentässä, voit valita **Nimikkeen määritteen arvot** -toiminnon ja luoda nimikkeen määritteelle arvot. Lisätietoja on "Arvojen luominen nimikkeen määritteille, joiden tyyppi on Asetus" -osassa.  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Arvojen luominen nimikkeen määritteille, joiden tyyppi on Asetus
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeen määritteet** ja valitse sitten liittyvä linkki.
2. Valitse **Nimikkeen määritteet** -ikkunassa nimikkeen määrite, jonka tyyppi on **Asetus** ja jolle haluat määrittää arvot. Valitse sitten **Nimikkeen määritteen arvot** -toiminto.
3. Täytä **Nimikkeen määritteen arvot** -ikkunassa tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Nimikkeen määritteiden määrittäminen nimikkeille
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Valitse **Nimikkeet**-ikkunassa nimike, jolle haluat määrittää nimikkeen määritteet. Valitse sitten **Määritteet**-toiminto.
3. Valitse **Nimikkeen määritteiden arvot** -ikkunassa **Uusi**-toiminto.
4. Valitse **Määrite**-kentässä valintapainike ja valitse aiemmin määritetty nimikkeen määrite. Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikkeen määritteen "Nimikkeen määritteiden luominen" -osassa esitetyllä tavalla.
5. Anna **Arvo**-kentässä nimikkeen määritteen arvo, kuten 2010, kun kyseessä on **Mallivuosi**-määrite.
6. Valitse **Asetus**-tyyppisille nimikkeen määritteille **Arvo**-kentän valintapainike. Valitse sitten nimikkeen määritteen arvo. Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikkeen määritteen arvon "Arvojen luominen nimikkeen määritteille, joiden tyyppi on Asetus" -osassa esitetyllä tavalla.
7. Toista vaiheet 4–6 kaikille niille nimikkeen määritteille, jotka haluat määrittää nimikkeeseen.

## <a name="to-assign-item-attributes-to-item-categories"></a>Nimikkeen määritteiden määrittäminen nimikeluokille
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikekategoriat** ja valitse sitten liittyvä linkki.
2. Valitse **Nimikeluokat**-ikkunassa nimikeluokka, jolle haluat määrittää nimikkeen määritteet. Valitse sitten **Muokkaa**-toiminto.
3. Valitse **Nimikeluokkakortti**-ikkunan **Määritteet**-pikavälilehdessä **Uusi**-toiminto.
4. Valitse **Määrite**-kentässä valintapainike ja valitse aiemmin määritetty nimikkeen määrite. Vaihtoehtoisesti voit valita **Uusi**-toiminnon ja luoda ensin uuden nimikkeen määritteen "Nimikkeen määritteen luominen" -osassa esitetyllä tavalla.
5. Valitse **Oletusarvo**-kentässä valintapainike ja valitse nimikkeen määritteen arvo.
6. Toista vaiheet 4 ja 5 kaikille niille nimikkeen määritteille, jotka haluat määrittää nimikeluokkaan.

**Huomautus**: Päänimikeluokkien nimikkeen määritteet periytyvät alinimikeluokille. Tämä osoitetaan **Peritty kohteesta** -kentässä **Määritteet**-pikavälilehdessä. Lisätietoja on kohdassa [Toimintaohje: Nimikkeiden luokitteleminen](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Suodattaminen nimikkeen määritteiden mukaan
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Valitse **Nimikkeet**-ikkunassa **Suodata määritteiden mukaan** -toiminto.
3. Valitse **Suodata nimikkeet määritteen mukaan** -ikkunassa **Määrite**-kentän valintapainike. Valitse sitten nimikkeen määrite.
4. Valitse **Arvo**-kentässä ensin valintapainike ja sitten määritteen arvo, jonka mukaan nimikkeet suodatetaan.

    **Huomautus**: Voit valita arvot vain suoraan niille nimikkeen määritteille, joilla on kiinteät arvot (esimerkiksi väri). Jos nimikkeen määritteillä on muuttuvat arvot (kuten leveys), nimikkeen määritteen arvo on määritettävä valitsemalla ensin ehto. Katso vaihe 5.
5. Valitse muuttuvan nimikkeen määritteen **Arvo**-kentässä valintapainike.
6. Valitse **Määritä suodatusarvo** -ikkunassa **Ehto**-kentässä alanuolipainike ja valitse sitten ehto.
7. Syötä **Arvo**-kenttään määritteen arvo, jonka mukaan nimikkeet suodatetaan.

    **Esimerkki**: Voit suodattaa nimikkeet, joiden materiaalin kuvaus alkaa sanalla "sininen", täyttämällä kentät seuraavasti: **Määrite**-kenttä: Materiaalin kuvaus, **Ehto**-kenttä: Alkaa, **Arvo**-kenttä: sininen.
8. Valitse **OK**-painike.   

**Nimikkeet**-ikkunan nimikkeet suodatetaan määritettyjen nimikkeen määritteen arvojen mukaan.

## <a name="see-also"></a>Katso myös
[Toimintaohje: Nimikkeiden luokitteleminen](inventory-how-categorize-items.md)    
[Toimintaohje: Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

