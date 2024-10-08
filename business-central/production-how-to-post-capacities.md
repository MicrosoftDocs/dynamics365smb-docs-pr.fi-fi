---
title: Kapasiteettien kirjaaminen
description: 'Kirjaa kuluneet kapasiteetit, joita ei ole määritetty tuotantotilaukseen kapasiteettipäiväkirjassa, ja tarkastele kirjattuja kapasiteetteja kapasiteettitapahtumien sivulla.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '5832, 99000802, 99000820'
ms.date: 03/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="post-capacities"></a>Kapasiteettien kirjaaminen

Kapasiteettipäiväkirjaan kirjataan kulutetut kapasiteetit, joita ei ole määritelty tuotantotilaukselle. Esimerkiksi ylläpitotyö tulee määritellä kapasiteetille, muttei tuotantotilaukselle.  

## <a name="to-post-capacities"></a>Kapasiteettien kirjaaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kapasiteettipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Täytä **Kirjauspvm**- ja **Asiakirjan nro** -kentät.  
3. Syötä **Tyyppi**-kenttään kapasiteetin tyyppi (**Kuormitusryhmä** tai **Tuotantosolu**), jota olet kirjaamassa.  
4. Valitse **Nro**-kenttään kuormitusryhmän tai tuotantosolun numero.  
5. Syötä asianmukaiset tiedot muihin kenttiin, esimerkiksi **Aloitusaika**-, **Lopetusaika**-, **Määrä**- ja **Hukkatavara**-kenttiin.  
6. Kirjaa kapasiteetit valitsemalla **Kirjaa**-toiminto.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-view-work-center-ledger-entries"></a>Tuotantosolutapahtumien näyttäminen

Voit tarkastella **Tuotantosolukortti**- ja **Kuormitusryhmän kortti** -sivuilla valmiiden tuotantotilausten tuloksena kirjattuja kapasiteetteja.    
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotantosolut** ja valitse sitten vastaava linkki.  
2. Avaa käsiteltävä **Tuotantosolukortti** luettelossa ja valitse sitten **Kapasiteettitapahtumat**-toiminto.  

    **Kapasiteettitapahtumat**-sivulla näkyvät tuotantosolun kirjatut tapahtumat siinä järjestyksessä kuin ne on kirjattu.   

## <a name="see-also"></a>Katso myös

[Tuotanto](production-manage-manufacturing.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
