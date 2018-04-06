---
title: "KO-vakuutuksen määrittäminen| Microsoft Docs"
description: "Voit hallita käyttöomaisuuden vakuutuksen kattavuutta, kun määrität ensin joitakin sopimusta koskevia yleisiä vakuutustietoja sekä vakuutuskortin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fd59a1aea6cb42dbeac7c6978619a5648f877b52
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-insurance"></a>Käyttöomaisuuserän määrittäminen
Voit hallita käyttöomaisuuden vakuutuksen kattavuutta, kun määrität ensin joitakin sopimusta koskevia yleisiä vakuutustietoja sekä vakuutuskortin.

## <a name="to-set-up-general-insurance-information"></a>Yleisten vakuutustietojen määrittäminen
Jotta [!INCLUDE[d365fin](includes/d365fin_md.md)]in vakuutusominaisuuksia voitaisiin käyttää, tietyt yleiset vakuutustiedot on määritettävä.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **KO-asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Vakuutustyyppien määrittäminen
Voit ryhmitellä vakuutussopimukset luokkiin, esimerkiksi vakuutukset varkauksia vastaan ja vakuutukset tulipaloa vastaan. Vakuutustyyppejä käytetään vakuutuskortissa.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Vakuutustyypit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-set-up-insurance-cards"></a>Vakuutuskorttien määrittäminen
Vakuutuskorttiin voi kerätä tietoja kustakin vakuutussopimuksesta.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Vakuutus** ja valitse sitten aiheeseen liittyvä linkki.  
2. Luo uusi vakuutuskortti valitsemalla **Vakuutus**-ikkunassa **Uusi**-toiminto.  
3. Täytä tarvittavat kentät.

## <a name="to-set-up-insurance-journal-templates"></a>Vakuutuspäiväkirjamallien määrittäminen
[!INCLUDE[d365fin](includes/d365fin_md.md)] luo automaattisesti vakuutuspäiväkirjan mallin, kun avaat **Vakuutuspäiväkirja**-ikkunan ensimmäisen kerran, mutta voit määrittää myös lisää päiväkirjamalleja. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Vakuutuspäiväkirjan mallit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä tarvittavat kentät.

## <a name="to-set-up-insurance-journal-batches"></a>Vakuutuspäiväkirjaerien määrittäminen
Vakuutuspäiväkirjan mallin alla voidaan määrittää eriä. Päiväkirjaerän arvoja käytetään oletusarvoina, jos päiväkirjarivien kenttiä ei täytetä. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Vakuutuspäiväkirjan mallit** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse vakuutuspäiväkirjamalli ja valitse sitten **Erät**-toiminto.
3. Täytä **Vakuutuspäiväkirjan erät** -ikkunassa tarvittavat kentät.

> [!NOTE]  
>   Numeroilla on päiväkirjan nimissä erityistehtävä. Jos päiväkirjamallin nimessä tai päiväkirjaerän nimessä on numero, numero suurenee automaattisesti yhdellä joka kerta, kun päiväkirja kirjataan. Esimerkiksi jos **Nimi**-kenttään syötetään HH1, päiväkirjan nimi muuttuu HH2:ksi sen jälkeen, kun päiväkirja, jonka nimi on HH1, on kirjattu.

## <a name="see-also"></a>Katso myös
[Käyttöomaisuuden määrittäminen](fa-setup.md)  
[Käyttöomaisuus](fa-manage.md)  
[Rahoitus](finance.md)  
[Tervetuloa [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]iin!](index.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

