---
title: Tuotannon tuotos- ja suoritusaikojen eräkirjaus
description: Tuotosmäärä ilmaisee työn edistymisen valmiina määränä ja tuotantosolun tai kuormitusryhmän käytettynä kapasiteettina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787875"
---
# <a name="batch-post-output-and-run-times"></a>Tuotos- ja suoritusaikojen eräkirjaus
Tuotosmäärä ilmaisee työn edistymisen valmiina määränä ja tuotantosolun tai kuormitusryhmän käytettynä kapasiteettina.

Tuotospäiväkirjaa voi käyttää seuraaviin:
*  Varastomäärän muutos valmiiden nimikkeiden tuotannon mukaan.
*  Määrien ja hävikin rekisteröinti kussakin tuotantoreitityksen toiminnossa.
*  Tuotantosolujen ja kuormitusryhmien määrityksen ja suoritusajan rekisteröinti.

> [!NOTE]
> Jos tuotannon reititystä käytetään, varasto päivitetään vasta, kun kirjaat viimeisen toiminnon tuotosmäärän.

**Tuotantopäiväkirja**-ikkunassa voi suorittaa samat tehtävät kuin **Tuotospäivä**-ikkunassa ja samaan aikaan voi suorittaa kulutuskirjauksiin liittyviä tehtäviä. Lisätietoja on kohdassa [Yhden vapautetun tuotantotilausrivin kulutuksen ja tuotoksen rekisteröiminen](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Vähintään yhden tuotantotilausrivin tuotosmäärän ja/tai suoritusaikojen kirjaaminen
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Tuotospäiväkirja** ja valitse sitten liittyvä linkki.  
2. Täytä kentät tuotantotilauksen tiedoilla, tuotostiedoilla ja/tai suoritusajalla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    **Pura reititys** -toiminnolla voi luoda päiväkirjarivejä tuotantotilauksista.
  
4. Jos toiminto on valmis, valitse **Valmis**-kenttä.  
5. Kirjaa toiminnot valitsemalla **Kirjaa**-toiminto. 
 
Kapasiteettitapahtumat kirjataan käytetyille tuotantosoluille ja kuormitusryhmille yhdessä aikaa sekä tuotoksen ja hävikin määrää koskevien tietojen kanssa. Jos viimeinen toiminto on kirjattu, nimike lisätään varastoon. 

## <a name="see-also"></a>Katso myös  
[Hävikin kirjaaminen manuaalisesti](production-how-to-post-scrap.md)
[Tuotoksen kirjaamisen peruuttaminen](production-how-to-reverse-output-posting.md)
[Tuotanto](production-manage-manufacturing.md)    
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)      
[Varasto](inventory-manage-inventory.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
