---
title: Tuotannon tuotos- ja suoritusaikojen eräkirjaus
description: Tuotosmäärä ilmaisee työn edistymisen valmiina määränä ja tuotantosolun tai kuormitusryhmän käytettynä kapasiteettina.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000773, 99000778, 99000823, 99000827'
ms.date: 03/08/2023
ms.author: edupont
---
# <a name="batch-post-output-and-run-times"></a><a name="batch-post-output-and-run-times"></a><a name="batch-post-output-and-run-times"></a>Tuotos- ja suoritusaikojen eräkirjaus

Tuotosmäärä ilmaisee työn edistymisen valmiina määränä ja tuotantosolun tai kuormitusryhmän käytettynä kapasiteettina.

Tuotospäiväkirjaa voi käyttää seuraaviin:

* Varastomäärän muutos valmiiden nimikkeiden tuotannon mukaan.
* Määrien ja hävikin rekisteröinti kussakin tuotantoreitityksen toiminnossa.
* Tuotantosolujen ja kuormitusryhmien määrityksen ja suoritusajan rekisteröinti.

> [!NOTE]
> Jos tuotannon reititystä käytetään, varasto päivitetään vasta, kun kirjaat viimeisen toiminnon tuotosmäärän.

**Tuotantopäiväkirja**-sivulla voit suorittaa samat tehtävät kuin **Tuotospäiväkirja**-sivulla ja tehdä myös kulutuskirjauksiin liittyviä tehtäviä. Lisätietoja on kohdassa [Yhden vapautetun tuotantotilausrivin kulutuksen ja tuotoksen rekisteröiminen](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Vähintään yhden tuotantotilausrivin tuotosmäärän ja/tai suoritusaikojen kirjaaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotospäiväkirja** ja valitse sitten vastaava linkki.  
2. Täytä kentät tuotantotilauksen tiedoilla, tuotostiedoilla ja/tai suoritusajalla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    **Pura reititys** -toiminnolla voi luoda päiväkirjarivejä tuotantotilauksista.
  
3. Jos toiminto on valmis, valitse **Valmis**-kenttä.  
4. Kirjaa toiminnot valitsemalla **Kirjaa**-toiminto.

    Kapasiteettitapahtumat kirjataan käytetyille tuotantosoluille ja kuormitusryhmille yhdessä aikaa sekä tuotoksen ja hävikin määrää koskevien tietojen kanssa. Jos viimeinen toiminto on kirjattu, nimike lisätään varastoon.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Hävikin kirjaaminen manuaalisti](production-how-to-post-scrap.md)
[Tuotoksen kirjaamisen peruuttaminen](production-how-to-reverse-output-posting.md)
[Tuotanto](production-manage-manufacturing.md)
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)  
[Varasto](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
