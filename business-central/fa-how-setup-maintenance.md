---
title: KO-kunnossapidon määrittäminen| Microsoft Docs
description: Käyttöomaisuuden korjauksia ja huoltoa hallitaan yleensä määrittämällä kunnossapidon perustiedot, työn tyyppikoodit ja kustannusten kirjaustili.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 60080b0a8982420ff2f3a6654d496395733bc425
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749216"
---
# <a name="set-up-fixed-asset-maintenance"></a>Käyttöomaisuuden huollon määrittäminen
Kun haluat hallita käyttöomaisuuden kunnossapitoa, määritä ensin joitakin yleisiä kunnossapitotietoja, kunnossapitokustannusten kirjaustili ja työtyyppien, kuten rutiinihuollon tai korjauksen, kunnossapitokoodit.

## <a name="to-set-up-general-maintenance-information"></a>Yleisten kunnossapitotietojen määrittäminen
Jos kunnossapidolle määritetään kentät, kunnossapitokuluja voi kirjata käyttöomaisuuden päiväkirjasta.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse käyttöomaisuus, jolle määrität vakuutuksen kattavuuden, ja valitse sitten **Muokkaa**-toiminto.
3. Täytä **Kunnossapito**-pikavälilehdessä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Kunnossapitokoodien määrittäminen
Kun kunnossapitokustannuksia kirjataan (yleisestä päiväkirjasta), **Kunnossapitokoodi**-kenttään tallennetaan suoritetun kunnossapidon tyyppi, kuten rutiinihuolto tai korjaus.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ylläpito** ja valitse sitten liittyvä linkki.
2. Määritä **Kunnossapito**-sivulla erityyppisten kunnossapitotöiden koodit.

## <a name="to-set-up-maintenance-expense-accounts"></a>Kunnossapitokustannusten tilien määrittäminen
Voit kirjata kunnossapitokustannuksia, kun annat ensin tilinumeron **KO-kirjausryhmät**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KO:n kirjausryhmät** ja valitse sitten liittyvä linkki.
2. Täytä **Kunnossapitokustannusten tili** -kenttä kunkin kirjausryhmän osalta.

> [!NOTE]  
>   Voit kohdistaa kunnossapitokustannukset osastoille ja/tai projekteille määrittämällä kohdistusavaimet. Lisätietoja on kohdassa [Käyttöomaisuuden yleisten ominaisuuksien määrittäminen](fa-how-setup-general.md).

## <a name="see-also"></a>Katso myös
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Rahoitus](finance.md)  
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)
