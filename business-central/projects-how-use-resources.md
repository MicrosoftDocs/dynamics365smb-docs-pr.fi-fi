---
title: Resurssin käytön ja hintojen kirjaaminen ja muuttaminen| Microsoft Docs
description: Tässä ohjeaiheessa kerrotaan, miten voit kirjata projektiin liitetyn resurssin käytön tai kulutuksen sekä seurata ja hallinta kustannuksia, hintoja ja työtyyppejä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c753e38566971c044da3337f0f35f1609bd489c8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748866"
---
# <a name="use-resources-for-jobs"></a>Resurssien käyttäminen projekteissa
Kirjaa resurssien käyttö projektipäiväkirjaan, kun haluat seurata kustannuksia ja hintoja sekä projekteihin linkitettyjä työtyyppejä. Lisätietoja on kohdassa [Projektien käytön kirjaaminen](projects-how-record-job-usage.md).

> [!NOTE]
> Voit ostaa myös ulkoisia resursseja, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).

Voit kirjata resurssin käytön myös resurssipäiväkirjaan. Resurssipäiväkirjassa kirjatuilla tapahtumilla ei ole vaikutusta pääkirjanpitoon.

## <a name="to-assign-resources-to-jobs"></a>Resurssien määrittäminen projekteihin:
Voit määrittää resursseja projekteihin luomalla projektiin suunnittelurivejä. Lisätietoja on kohdassa [Projektien luominen](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Projektin resurssin käytön kirjaaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Projektipäiväkirjat** ja valitse sitten liittyvä linkki.
2. Avaa kyseessä oleva projektipäiväkirjan erä ja täytä vaaditut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Kun päiväkirja on valmis, valitse **Kirjaa**-toiminto.

## <a name="to-adjust-resource-prices"></a>Resurssihintojen muuttaminen
Jos haluat muuttaa useiden resurssien kustannuksia tai hintoja, voit käyttää eräajoa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muuta resurssin kustannuksia tai hintoja** ja valitse sitten liittyvä linkki.
2. Täytä rivin tarvittavat kentät ja valitse **OK**-painike.

> [!NOTE]  
>   Tämä eräajo ei luo vaihtoehtoisia kustannuksia tai hintoja resursseille tai muuta niitä. Se muuttaa vain sen **Muuta kenttää** -kentässä olevan resurssin kortin kentän sisältöä, joka on valittu eräajoon. Muutokset tulevat resurssien osalta voimaan heti, joten tarkista muutoskertoimet ennen eräajon suorittamista.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Resurssihintojen muutosehdotusten saaminen olemassa olevien vaihtoehtoisten hintojen perusteella
Jos olet jo määrittänyt vaihtoehtoisia resurssihintoja joillekin resursseille, voit määrittää useita vaihtoehtoisia resurssihintoja eräajon avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssin hinnan muutokset** ja valitse sitten liittyvä linkki.
2. Valitse **Ehdota res.hintamuut. (hinta)** -toiminto ja täytä tarvittavat kentät.
3. Valitse **OK**-painike.  
4. Kun eräajo on päättynyt, eräajon tulokset näkyvät **Resurssin hinnan muutokset** -sivulla.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Resurssihintojen muutosehdotusten saaminen vakiohintojen perusteella
Jos haluat määrittää useita vaihtoehtoisia resurssihintoja resurssikorttien vakiohintojen perusteella, voit käyttää eräajoa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssin hinnan muutokset** ja valitse sitten liittyvä linkki.
2. Valitse **Ehdota res.hintamuut. (res.)** -toiminto ja täytä tarvittavat kentät.  
3. Valitse **OK**-painike.  
4. Kun eräajo on päättynyt, voit katsoa eräajon tulokset avaamalla **Resurssin hinnan muutokset** -sivun.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Resurssihintojen muutosehdotusten saaminen vakiohintojen perusteella
Jos olet jo määrittänyt vaihtoehtoisia resurssihintoja joillekin resursseille, voit määrittää useita vaihtoehtoisia resurssihintoja eräajon avulla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ehdota res.hintamuut. (hinta)** ja valitse sitten liittyvä linkki.  
2. Täytä tarvittavat kentät.
3. Valitse **OK**-painike.  
4. Kun eräajo on päättynyt, voit katsoa eräajon tulokset avaamalla **Resurssin hinnan muutokset** -sivun.

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)     
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]