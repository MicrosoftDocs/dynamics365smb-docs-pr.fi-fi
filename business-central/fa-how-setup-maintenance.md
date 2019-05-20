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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ba01ccb88349a1f1943655949a36e2a21f3ae2de
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244491"
---
# <a name="set-up-fixed-asset-maintenance"></a>Käyttöomaisuuden huollon määrittäminen
Kun haluat hallita käyttöomaisuuden kunnossapitoa, määritä ensin joitakin yleisiä kunnossapitotietoja, kunnossapitokustannusten kirjaustili ja työtyyppien, kuten rutiinihuollon tai korjauksen, kunnossapitokoodit.

## <a name="to-set-up-general-maintenance-information"></a>Yleisten kunnossapitotietojen määrittäminen
Jos kunnossapidolle määritetään kentät, kunnossapitokuluja voi kirjata käyttöomaisuuden päiväkirjasta.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Käyttöomaisuus** ja valitse sitten liittyvä linkki.
2. Valitse käyttöomaisuus, jolle määrität vakuutuksen kattavuuden, ja valitse sitten **Muokkaa**-toiminto.
3. Täytä **Kunnossapito**-pikavälilehdessä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Kunnossapitokoodien määrittäminen
Kun kunnossapitokustannuksia kirjataan (yleisestä päiväkirjasta), **Kunnossapitokoodi**-kenttään tallennetaan suoritetun kunnossapidon tyyppi, kuten rutiinihuolto tai korjaus.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kunnossapito** ja valitse sitten liittyvä linkki.
2. Määritä **Kunnossapito**-sivulla erityyppisten kunnossapitotöiden koodit.

## <a name="to-set-up-maintenance-expense-accounts"></a>Kunnossapitokustannusten tilien määrittäminen
Voit kirjata kunnossapitokustannuksia, kun annat ensin tilinumeron **KO-kirjausryhmät**-sivulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **KO:n kirjausryhmät** ja valitse sitten liittyvä linkki.
2. Täytä **Kunnossapitokustannusten tili** -kenttä kunkin kirjausryhmän osalta.

> [!NOTE]  
>   Voit kohdistaa kunnossapitokustannukset osastoille ja/tai projekteille määrittämällä kohdistusavaimet. Lisätietoja on kohdassa [Käyttöomaisuuden yleisten ominaisuuksien määrittäminen](fa-how-setup-general.md).

## <a name="see-also"></a>Katso myös
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Rahoitus](finance.md)  
[Käytön aloittaminen](product-get-started.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
