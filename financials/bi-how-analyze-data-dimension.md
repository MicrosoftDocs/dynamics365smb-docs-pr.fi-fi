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
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ec3210e019da3369971d3aef6a4e38f4dcf1f530
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
#  <a name="analyze-data-by-dimensions"></a>Analysoi tiedot mittojen mukaan
Talousanalyysissä dimensio on tieto, jonka voi lisätä tapahtumaan eräänlaiseksi merkiksi. Tämän tiedon avulla voi yhdistää ryhmiksi tapahtumia, joilla on samoja ominaisuuksia, kuten asiakkaita, alueita, tuotteita tai myyjiä, sekä noutaa nämä ryhmät helposti analysoitavaksi. Dimensioita voi käyttää päiväkirjojen tapahtumissa, asiakirjoissa ja budjeteissa. Dimensiotermi kuvaa, miten analysointi tapahtuu. Esimerkiksi kaksidimensioinen analyysi voisi olla myynti per alue. Käyttämällä tapahtumaa luodessasi useita dimensiota voit luoda monimutkaisia analyysejä, kuten myynti per myyntikampanja per asiakasryhmä per alue. Lisätietoja on kohdassa [Dimensioiden käyttäminen](finance-dimensions.md).

Analysoimalla tietoja dimensioittain saat liiketoiminnasta selkeän kuvan ja voit arvioida esimerkiksi, miten hyvin yritys toimii, missä se menestyy ja missä ei, sekä minne pitäisi kohdentaa enemmän resursseja.

> [!TIP]
> Tapahtumatietoja voi analysoida nopeasti dimensioiden mukaan suodattamalla tilikarttojen loppusummat ja kaikkien **Tapahtumat**-ikkunoiden tapahtumat dimensioittain. Hae **Määritä dimension suodatus** -toiminto.

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
[Dimensioiden käyttäminen](finance-dimensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

