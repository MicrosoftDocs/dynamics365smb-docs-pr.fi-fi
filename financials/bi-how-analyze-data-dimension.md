---
title: Analysoi tietoja dimensioiden mukaan | Microsoft Docs
description: "Tässä osassa kuvataan eri liiketoiminnan tietojen analysointi dimensioiden mukaan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/13/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 463dcad5d918e9655cd92991403d00a76aca7d69
ms.contentlocale: fi-fi
ms.lasthandoff: 07/07/2017


---
#  <a name="how-to-analyze-data-by-dimensions"></a>Analysoi tiedot dimensioiden mukaan
Talousanalyysissä dimensio on tieto, jonka voi lisätä tapahtumaan eräänlaiseksi merkiksi. Tämän tiedon avulla voi yhdistää ryhmiksi tapahtumia, joilla on samoja ominaisuuksia, kuten asiakkaita, alueita, tuotteita tai myyjiä, sekä noutaa nämä ryhmät helposti analysoitavaksi. Dimensioita voi käyttää päiväkirjojen tapahtumissa, asiakirjoissa ja budjeteissa. Dimensiotermi kuvaa, miten analysointi tapahtuu. Esimerkiksi kaksidimensioinen analyysi voisi olla myynti per alue. Käyttämällä tapahtumaa luodessasi useita dimensiota voit luoda monimutkaisia analyysejä, kuten myynti per myyntikampanja per asiakasryhmä per alue. Lisätietoja on kohdassa [Dimensioiden käyttäminen](finance-dimensions.md).

Analysoimalla tietoja dimensioittain saat liiketoiminnasta selkeän kuvan ja voit arvioida esimerkiksi, miten hyvin yritys toimii, missä se menestyy ja missä ei, sekä minne pitäisi kohdentaa enemmän resursseja.

> [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu **Ohjelmistopaketti**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-set-up-an-analysis-view"></a>Analyysinäkymän luominen  
Analyysissa dimensioittain näkyy valittu dimensioyhdistelmä. Voit tallentaa ja hakea jokaisen määrittelemäsi analyysin. Analyysin määrityksen tiedot tallentuvat **analyysinäkymän** korttiin, jotta tulevien analyysien laatiminen olisi yksinkertaisempaa.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Analyysinäkymät** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Analyysinäkymän luettelo** -ikkunassa **Uusi**-toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Jos haluat lisätä muita dimensiokoodeja neljän **Dimensiot**-pikavälilehden koodin lisäksi, valitse **Suodatin**-toiminto, täytä kentät ja valitse **OK**.  
5. Voit päivittää näkymän valitsemalla **Päivitä**-toiminnon.

## <a name="to-analyze-by-dimensions"></a>Analyysi dimensioiden mukaan
Voit tarkastella pääkirjanpidon summia **Varastoanalyysi dimensioittain** -matriisissa aiemmin määrittämiesi analyysinäkymien avulla. Täytä **Analyysi dimensioittain** -ikkuna, kun haluat määrittää matriisissa näkyvät tiedot. Voit katsella matriisia valitsemalla **Näytä matriisi** -toiminnon.  

- Vasemmanpuoleisimmisssa sarakkeissa oleva tieto perustuu otsikon **Näytä riveinä** -kentässä tekemääsi valintaan.  
- Oikeanpuoleisissa sarakkeissa oleva tieto perustuu otsikon **Näytä sarakkeina** -kentässä tekemääsi valintaan.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Analyysi dimensioittain** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse haluamasi analyysinäkymä ja valitse sitten **Muokkaa analyysinäkymää** -toiminto.
3. Täyttämällä **Analyysi dimensioittain** -ikkunan yläosan kentät määrität, mitä näytetään.
4. 5. Voit näyttää matriisi-ikkunassa näkyvän summan määrityksen napsauttamalla summaa.  

> [!IMPORTANT]  
>   **Analyysinäkymä**-kortin Pvmtiivistys-kentässä määritettyä jaksoa lyhyempää jakson pituutta ei voi valita. **Seuraava joukko**- ja **Edellinen joukko** -komennot eivät ole käytettävissä, jos olet valinnut **Jakso**-vaihtoehdon **Näytä riveinä**- tai **Näytä sarakkeina** -kentässä.  

> [!NOTE]  
>   **Dimensiot - Yksityiskohdat** -raportti sisältää yksityiskohtaisen luokittelun, josta näkyy, miten dimensioita on käytetty valitun jakson tapahtumissa. **Dimensiot - Yhteensä** -raporttia voidaan käyttää yhteissummien tarkastelemiseen.  

> [!TIP]  
>   Näkymää voidaan mukauttaa myös muuttamalla **Näytä riveinä** -kentän ja **Näytä sarakkeina** -kentän sisältöä. Voit peruuttaa näkymäasetukset **Muuta rivit ja sar. käänt.** -toiminnolla.

## <a name="to-update-an-analysis-view"></a>Analyysinäkymän päivittämien  
Summat, jotka näkyvät **Analyysi dimensioittain** -ikkunassa, kuvaavat yrityksen tilaa viimeisimmän päivityksen aikaan. Jos haluat nähdä nykyisen tilanteen, sinun on päivitettävä analyysinäkymä suorittamalla päivitystoiminto.

Seuraavan menettelyn avulla voit päivittää analyysinäkymän **Analyysi dimensioittain** -ikkunassa. Vaiheet ovat samanlaiset **Analyysinäkymän kortti** ja **Analyysinäkymän luettelo** -ikkunoissa.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Analyysi dimensioittain** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Analyysi dimensioittain** -ikkunassa **Analyysinäkymän koodi** -kenttä.  
3. Valitse asianomaisen analyysinäkymän rivi.  
4. Valitse **Päivitä**-toiminto.  

> [!TIP]  
>   Jos valitset **Päivitä kirjattaessa** -valintaruudun analyysinäkymän kortilla, näkymä päivitetään automaattisesti liittyvää tapahtumaa kirjattaessa.

> [!NOTE]  
>   Kun haluat päivittää joitakin tai kaikkia analyysinäkymiä samanaikaisesti, sinun täytyy käyttää **Päivitä analyysinäkymät** -eräajoa.  

## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

