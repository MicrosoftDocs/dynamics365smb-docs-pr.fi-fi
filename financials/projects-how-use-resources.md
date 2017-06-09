---
title: "Toimintaohje: Projektien resurssien käyttäminen| Microsoft Docs"
description: Artikkelissa kerrotaan, miten projekteja hallitaan aikaraporttien avulla.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34d8b133a11324e1821780e3988158bb0989349b
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-resources-for-jobs"></a>Toimintaohje: Resurssien käyttäminen projekteissa
Kirjaa resurssien käyttö projektipäiväkirjaan, kun haluat seurata kustannuksia ja hintoja sekä projekteihin linkitettyjä työtyyppejä. Lisätietoja on kohdassa [Toimintaohje: Projektien käytön kirjaaminen](projects-how-record-job-usage.md).

Voit kirjata resurssin käytön myös resurssipäiväkirjaan. Resurssipäiväkirjassa kirjatuilla tapahtumilla ei ole vaikutusta pääkirjanpitoon.

**Huomautus**: Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)]-kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-assign-resources-to-jobs"></a>Resurssien määrittäminen projekteihin:
Voit määrittää resursseja projekteihin luomalla projektiin suunnittelurivejä. Lisätietoja on kohdassa [Toimintaohje: Projektien luominen](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Projektin resurssin käytön kirjaaminen
1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Projektipäiväkirjat** ja valitse sitten liittyvä linkki.
2. Avaa kyseessä oleva projektipäiväkirjan erä ja täytä vaaditut kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Kun päiväkirja on valmis, valitse **Kirjaa**-toiminto.

## <a name="to-adjust-resource-prices"></a>Resurssihintojen muuttaminen
Jos haluat muuttaa useiden resurssien kustannuksia tai hintoja, voit käyttää eräajoa.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Muuta resurssin kustannuksia tai hintoja** ja valitse sitten liittyvä linkki.
2. Täytä rivin tarvittavat kentät ja valitse **OK**-painike.

**Huomautus**: Tämä eräajo ei luo tai muuta resurssin vaihtoehtoisia kustannuksia tai hintoja. Se muuttaa vain sen **Muuta kenttää** -kentässä olevan resurssin kortin kentän sisältöä, joka on valittu eräajoon. Muutokset tulevat resurssien osalta voimaan heti, joten tarkista muutoskertoimet ennen eräajon suorittamista.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Resurssihintojen muutosehdotusten saaminen olemassa olevien vaihtoehtoisten hintojen perusteella
Jos olet jo määrittänyt vaihtoehtoisia resurssihintoja joillekin resursseille, voit määrittää useita vaihtoehtoisia resurssihintoja eräajon avulla.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Resurssin hinnan muutokset** ja valitse sitten liittyvä linkki.
2. Valitse **Ehdota res.hintamuut. (hinta)** -toiminto ja täytä tarvittavat kentät.
3. Valitse **OK**-painike.  
4. Kun eräajo on päättynyt, eräajon tulokset näkyvät **Resurssin hinnan muutokset** -ikkunassa.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Resurssihintojen muutosehdotusten saaminen vakiohintojen perusteella
Jos haluat määrittää useita vaihtoehtoisia resurssihintoja resurssikorttien vakiohintojen perusteella, voit käyttää eräajoa.  

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Resurssin hinnan muutokset** ja valitse sitten liittyvä linkki.
2. Valitse **Ehdota res.hintamuut. (res.)** -toiminto ja täytä tarvittavat kentät.  
3. Valitse **OK**-painike.  
4. Kun eräajo on päättynyt, voit katsoa eräajon tulokset avaamalla **Resurssin hinnan muutokset** -ikkunan.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Resurssihintojen muutosehdotusten saaminen vakiohintojen perusteella
Jos olet jo määrittänyt vaihtoehtoisia resurssihintoja joillekin resursseille, voit määrittää useita vaihtoehtoisia resurssihintoja eräajon avulla.

1. Syötä **Etsi**-ruudussa **Ehdota res.hintamuut. (hinta)** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät.
3. Valitse **OK**-painike.  
4. Kun eräajo on päättynyt, voit katsoa eräajon tulokset avaamalla **Resurssin hinnan muutokset** -ikkunan.

## <a name="see-also"></a>Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)         
[Myynti](sales-manage-sales.md)     
[[!INCLUDE[d365fin](includes/d365fin_md.md)]in käyttäminen](ui-work-product.md)  

