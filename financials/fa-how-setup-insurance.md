---
title: "Toimintaohje: Käyttöomaisuuden vakuutuksen määrittäminen| Microsoft Docs"
description: "Tässä artikkelissa kerrotaan, miten järjestelmä määritetään käyttöomaisuuden vakuutusta varten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6473b74823f787e6b1eac599bb95b6d100a02c1e
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-insurance"></a>Toimintaohje: Käyttöomaisuuden vakuutuksen määrittäminen
Voit hallita käyttöomaisuuden vakuutuksen kattavuutta, kun määrität ensin joitakin sopimusta koskevia yleisiä vakuutustietoja sekä vakuutuskortin.

## <a name="to-set-up-general-insurance-information"></a>Yleisten vakuutustietojen määrittäminen
Jotta [!INCLUDE[d365fin](includes/d365fin_md.md)]in vakuutusominaisuuksia voitaisiin käyttää, tietyt yleiset vakuutustiedot on määritettävä.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **KO-asetukset** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Vakuutustyyppien määrittäminen
Voit ryhmitellä vakuutussopimukset luokkiin, esimerkiksi vakuutukset varkauksia vastaan ja vakuutukset tulipaloa vastaan. Vakuutustyyppejä käytetään vakuutuskortissa.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Vakuutuslajit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-set-up-insurance-cards"></a>Vakuutuskorttien määrittäminen
Vakuutuskorttiin voi kerätä tietoja kustakin vakuutussopimuksesta.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Vakuutus** ja valitse sitten liittyvä linkki.  
2. Luo uusi vakuutuskortti valitsemalla **Vakuutus**-ikkunassa **Uusi**-toiminto.  
3. Täytä tarvittavat kentät.

## <a name="to-set-up-insurance-journal-templates"></a>Vakuutuspäiväkirjamallien määrittäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] luo automaattisesti vakuutuspäiväkirjan mallin, kun avaat **Vakuutuspäiväkirja**-ikkunan ensimmäisen kerran, mutta voit määrittää myös lisää päiväkirjamalleja. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Vakuutuspäiväkirjan mallit** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-set-up-insurance-journal-batches"></a>Vakuutuspäiväkirjaerien määrittäminen
Vakuutuspäiväkirjan mallin alla voidaan määrittää eriä. Päiväkirjaerän arvoja käytetään oletusarvoina, jos päiväkirjarivien kenttiä ei täytetä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Vakuutuspäiväkirjan mallit** ja valitse sitten liittyvä linkki.  
2. Valitse vakuutuspäiväkirjamalli ja valitse sitten **Erät**-toiminto.
3. Täytä **Vakuutuspäiväkirjan erät** -ikkunassa tarvittavat kentät.

**Huomautus:** Numeroilla on päiväkirjan nimissä erityistehtävä. Jos päiväkirjamallin nimessä tai päiväkirjaerän nimessä on numero, numero suurenee automaattisesti yhdellä joka kerta, kun päiväkirja kirjataan. Esimerkiksi jos **Nimi**-kenttään syötetään HH1, päiväkirjan nimi muuttuu HH2:ksi sen jälkeen, kun päiväkirja, jonka nimi on HH1, on kirjattu.

## <a name="see-also"></a>Katso myös
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Rahoitus](finance.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)

