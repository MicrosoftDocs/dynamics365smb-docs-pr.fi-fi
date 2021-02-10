---
title: Todellinen vs. Budjetti -analyysi| Microsoft-asiakirjat
description: Kuvaa, miten todellisia summia analysoidaan budjetoituihin summiin nähden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0a2a8ba7de175ae717dae42da44b719a9c920a15
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752253"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Todellisten summien analysointi budjetoituihin summiin nähden
Yrityksesi tietojen keräämisen, analysoinnin ja jakamisen osana tarkastelet todellisia summia ja vertaat niitä kaikkien tilien sekä useiden ajanjaksojen budjetoituihin summiin.

Budjetoitujen summia analysointia varten on ensin luotava KP-budjetteja. Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).

## <a name="to-view-a-gl-budget"></a>KP-budjetin tarkastelu
Budjetissa, jossa on dimensioita, voi suodattaa tapahtumia ja siten tarkastella tiettyjä budjetteja.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Pääkirjanpidon budjetit** ja valitse sitten liittyvä linkki.
2. Avaa **KP-budjetit** -sivulla talousarvio, jota haluat tarkastella.  
3. Täyttämällä sivun yläosan kentät määrität, mitä näytetään. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Jos olet valinnut **Jakso**-vaihtoehdon joko **Näytä riveinä**- tai **Näytä sarakkeina** -kentässä, täytä **Näyttöperuste**-kenttä. Jos et ole valinnut **Jakso**-vaihtoehtoa **Näytä riveinä**- tai **Näytä sarakkeina** -kentässä, määritä asianmukainen jakso **Pvm-suodatus**-kentässä.  

> [!NOTE]  
>   Vain ne KP-budjetin tapahtumat, joissa on **Suodattimet**-pikavälilehdessä määrittämäsi suodatinkoodit, sisällytetään laskentaan. Budjettitapahtumia, joissa on eri suodatinkoodit tai joissa ei ole suodatinkoodeja ollenkaan, ei sisällytetä. Niin kauan kuin suodatin on näkyvissä sivulla, budjetissa näkyvät vain ne budjettitapahtumat, joissa on nämä suodattimen koodit.  

> [!TIP]  
>   Jos budjettia on tarpeen muokata, voit muokata budjetin tapahtumia. Valitse summa, niin saat näkyviin sen perusteena olevat KP-budjetin tapahtumat.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Todellisten ja budjetoitujen summien tarkastelu kaikkien tilien osalta  
Pääkirjanpidon budjettien tarkastelu ja niiden vertaaminen todellisiin lukuihin useilla [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman osa-alueilla.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
2. Valitse **Tilikartta**-sivulla **KP-saldo/-budjetti**-toiminto.
3. Täyttämällä sivun yläosan kentät määrität, mitä näytetään.  
4. Valitse kenttä nähdäksesi määrityksen, josta näkyvä summa muodostuu.  

> [!NOTE]  
>   Suodattimia, jotka määritit sivun otsikossa, käytetään sekä KP-tapahtumissa että budjettitapahtumissa.

Vasemmanpuoleisimmisssa sarakkeissa on tilikartta. Oikealla olevista viidestä sarakkeesta neljässä ensimmäisessä on kunkin tilin todelliset ja budjetoidut debet- ja kreditsummat. Viidennessä sarakkeessa on todellisen ja budjetoidun summan välinen suhde KP-tilillä.  

> [!TIP]  
>   Käyttämällä **Näyttöperuste**-kenttää **KP-saldo/budjetti**-sivulla voit valita jakson pituuden. **Näyttömuoto**-kentän avulla voit valita tavan, jolla summat lasketaan (**Nettomuutos** tai **Saldo pvm:ttäin**). Valitse **Edellinen jakso** tai **Seuraava jakso** -toiminto ja muuta jaksoa.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Useiden jaksojen todellisten ja budjetoitujen summien tarkastelu  
Sen sijaan että tarkastelisit todellisia ja budjetoituja summia kaikkien tilien osalta yhdeltä kaudelta, voit tarkastella useita yhden tilin kausia.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
2. Valitse **Tilikartta**-sivulla haluamasi KP-tili ja valitse sitten **KP-tilin saldo/budjetti** -toiminto.  
3. Täyttämällä sivun yläosan kentät määrität, mitä näytetään.   
4. Valitse kenttä nähdäksesi näkyvän summan määrityksen.  

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)  
[KP-raporttimallien käyttäminen](bi-how-work-account-schedule.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
