---
title: Todellinen vs. Budjetti -analyysi| Microsoft-asiakirjat
description: "Kuvaa, miten todellisia summia analysoidaan budjetoituihin summiin nähden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 126c8da9b9ef80e954510fa8e5089906d7dd6f01
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-analyze-actual-amounts-versus-budgeted-amounts"></a>Todellisten summien analysointi budjetoituihin summiin nähden
Yrityksesi tietojen keräämisen, analysoinnin ja jakamisen osana tarkastelet todellisia summia ja vertaat niitä kaikkien tilien sekä useiden ajanjaksojen budjetoituihin summiin.

Jotta voisit analysoitava budjetoituja summia, sinun on ensin luotava budjetteja. Lisätietoja on kohdassa [Budjettien luominen](finance-how-create-budgets.md).

> [!NOTE]  
>   Tämä toiminto edellyttää, että kokemukseksi on valittu **Suite**. Lisätietoja on kohdassa [[!INCLUDE[d365fin](includes/d365fin_md.md)] -kokemuksen mukauttaminen](ui-experiences.md).

## <a name="to-view-a-budget"></a>Budjetin tarkastelu
Budjetissa, jossa on dimensioita, voi suodattaa tapahtumia ja siten tarkastella tiettyjä budjetteja.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **KP-budjetit** ja valitse sitten aiheeseen liittyvä linkki.
2. Avaa **KP-budjetit** -ikkunassa talousarvio, jota haluat tarkastella.  
3. Täyttämällä ikkunan yläosan kentät määrität, mitä näytetään. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Jos olet valinnut **Jakso**-vaihtoehdon joko **Näytä riveinä**- tai **Näytä sarakkeina** -kentässä, täytä **Näyttöperuste**-kenttä. Jos et ole valinnut **Jakso**-vaihtoehtoa **Näytä riveinä**- tai **Näytä sarakkeina** -kentässä, määritä asianmukainen jakso **Pvm-suodatus**-kentässä.  

> [!NOTE]  
>   Vain ne KP-budjetin tapahtumat, joissa on **Suodattimet**-pikavälilehdessä määrittämäsi suodatinkoodit, sisällytetään laskentaan. Budjettitapahtumia, joissa on eri suodatinkoodit tai joissa ei ole suodatinkoodeja ollenkaan, ei sisällytetä. Niin kauan kuin suodatin on näkyvissä ikkunassa, budjetissa näkyvät vain ne budjettitapahtumat, joissa on nämä suodattimen koodit.  

> [!TIP]  
>   Jos budjettia on tarpeen muokata, voit muokata budjetin tapahtumia. Valitse summa, niin saat näkyviin sen perusteena olevat KP-budjetin tapahtumat.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Todellisten ja budjetoitujen summien tarkastelu kaikkien tilien osalta  
Pääkirjanpidon budjettien tarkastelu ja niiden vertaaminen todellisiin lukuihin useilla [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman osa-alueilla.

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Tilikartta** -ikkunassa **KP-saldo/-budjetti**-toiminto.
3. Täyttämällä ikkunan yläosan kentät määrität, mitä näytetään.  
4. Valitse kenttä nähdäksesi määrityksen, josta näkyvä summa muodostuu.  

> [!NOTE]  
>   Suodattimia, jotka määritit ikkunan otsikossa, käytetään sekä KP-tapahtumissa että budjettitapahtumissa.

Vasemmanpuoleisimmisssa sarakkeissa on tilikartta. Oikealla olevista viidestä sarakkeesta neljässä ensimmäisessä on kunkin tilin todelliset ja budjetoidut debet- ja kreditsummat. Viidennessä sarakkeessa on todellisen ja budjetoidun summan välinen suhde KP-tilillä.  

> [!TIP]  
>   Käyttämällä **Näyttöperuste**-kenttää **KP-saldo/budjetti**-ikkunassa voit valita jakson pituuden. **Näyttömuoto**-kentän avulla voit valita tavan, jolla summat lasketaan (**Nettomuutos** tai **Saldo pvm:ttäin**). Valitse **Edellinen jakso** tai **Seuraava jakso** -toiminto ja muuta jaksoa.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Useiden jaksojen todellisten ja budjetoitujen summien tarkastelu  
Sen sijaan että tarkastelisit todellisia ja budjetoituja summia kaikkien tilien osalta yhdeltä kaudelta, voit tarkastella useita yhden tilin kausia.  

1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Tilikartta**-ikkunassa haluamasi KP-tili ja valitse sitten **KP-tilin saldo/budjetti** -toiminto.  
3. Täyttämällä ikkunan yläosan kentät määrität, mitä näytetään.   
4. Valitse kenttä nähdäksesi näkyvän summan määrityksen.  

## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)
[KP-raporttimallien kanssa työskenteleminen](bi-how-work-account-schedule.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  

