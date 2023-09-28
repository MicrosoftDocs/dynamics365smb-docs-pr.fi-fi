---
title: Todellisten summien analysointi budjetoituihin summiin nähden
description: 'Tässä artikkelissa kuvataan, miten voit analysoida todellisia summia budjetoituihin summiin verrattuna, jotta voit kerätä, analysoida ja jakaa yrityksesi tietoja.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '120, 121, 422'
ms.date: 09/14/2022
ms.author: bholtorf
---
# Todellisten summien analysointi budjetoituihin summiin nähden

Yrityksesi tietojen keräämisen, analysoinnin ja jakamisen osana tarkastelet todellisia summia ja vertaat niitä kaikkien tilien sekä useiden ajanjaksojen budjetoituihin summiin.

Budjetoitujen summia analysointia varten on ensin luotava pääkirjanpito (KP) -budjetteja. Lisätietoja on kohdassa [KP-budjettien luominen](finance-how-create-budgets.md).

## KP-budjetin tarkastelu

Budjetissa, jossa on dimensioita, voi suodattaa tapahtumia ja siten tarkastella tiettyjä budjetteja.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **KP-budjetit**, valitse sitten vastaava linkki.
2. Avaa **KP-budjetit** -sivulla talousarvio, jota haluat tarkastella.  
3. Täyttämällä sivun yläosan kentät määrität, mitä näytetään. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Jos olet valinnut **Jakso**-vaihtoehdon joko **Näytä riveinä**- tai **Näytä sarakkeina** -kentässä, täytä **Näyttöperuste**-kenttä. Jos et ole valinnut **Jakso**-vaihtoehtoa kummassakaan kentässä, määritä asianmukainen jakso **Pvm-suodatus**-kentässä.  

> [!NOTE]  
> Vain ne KP-budjetin tapahtumat, joissa on **Suodattimet**-pikavälilehdessä määrittämäsi suodatinkoodit, sisällytetään laskentaan. Budjettitapahtumia, joissa ei ole suodatinkoodeja tai on eri suodatinkoodit, ei sisällytetä. Niin kauan kuin suodatin on näkyvissä sivulla, budjetissa näkyvät vain tapahtumat, joissa on nämä suodattimen koodit.  

> [!TIP]  
> Muokkaa budjettia **Muokkaa budjettia** -toiminnon avulla. Valitse budjettisivulla summa, niin saat näkyviin sen perusteena olevat KP-budjetin tapahtumat.

## Todellisten ja budjetoitujen summien tarkastelu kaikkien tilien osalta

Pääkirjanpidon budjettien tarkastelu ja niiden vertaaminen todellisiin lukuihin useilla [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman osa-alueilla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta**, valitse sitten vastaava linkki.  
2. Valitse **Tilikartta**-sivulla **KP-saldo/-budjetti**-toiminto.
3. Täyttämällä **Valinnat**-pikavälilehden kentät määrität, mitä näytetään taulukossa.  
4. Viemällä osoittimen taulukon kentän päälle voit lukea lyhyen kuvauksen näytettävästä summasta.

> [!NOTE]  
> Suodattimia, jotka määritit sivun otsikossa, käytetään sekä KP- että budjettitapahtumissa.

Vasemmanpuoleisimmisssa sarakkeissa on tilikartta. Oikealla olevista viidestä sarakkeesta neljässä ensimmäisessä on kunkin tilin todelliset ja budjetoidut debet- ja kreditsummat. Viidennessä sarakkeessa on todellisen ja budjetoidun summan välinen suhde KP-tilillä.  

> [!TIP]  
> Käyttämällä **Näyttöperuste**-kenttää **KP-saldo/budjetti**-sivulla voit valita jakson pituuden. **Näyttömuoto**-kentän avulla voit valita tavan, jolla summat lasketaan, joko **Nettomuutos** tai **Saldo pvm:ttäin**. Valitse **Edellinen jakso** tai **Seuraava jakso** -toiminto ja muuta jaksoa.  

## Useiden jaksojen todellisten ja budjetoitujen summien tarkastelu  

Sen sijaan että tarkastelisit todellisia ja budjetoituja summia kaikkien tilien osalta yhdeltä kaudelta, voit tarkastella useita yhden tilin kausia.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta**, valitse sitten vastaava linkki.  
2. Valitse **Tilikartta**-sivulla haluamasi KP-tili, valitse sitten **KP-tilin saldo/budjetti** -toiminto.  
3. Täyttämällä **Valinnat**-pikavälilehden kentät määrität, mitä näytetään taulukossa.  
4. Vie osoitin taulukon kentän päälle **Rivit**-pikavälilehdellä voit lukea lyhyen kuvauksen näytettävästä summasta.  

## Katso myös

[Taloushallinnon liiketoimintatiedot](bi.md)  
[Talousraporttien käsitteleminen](bi-how-work-account-schedule.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Pääkirjanpito ja tilikartta](finance-general-ledger.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
