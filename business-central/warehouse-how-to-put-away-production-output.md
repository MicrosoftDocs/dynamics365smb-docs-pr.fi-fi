---
title: Tuotannon tuotoksen hyllyttäminen
description: Tässä artikkelissa käsitellään tuotannon tuotoksen hyllyttämistä.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# <a name="put-away-production-or-assembly-output"></a>Tuotannon tai kokoonpanon tuotoksen hyllyttäminen

Tuotannon hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

Jos fyysisen varastoinnin perusmääritykset edellyttävät sijainnissa hyllytyksen käsittelyä, tuotannon tuotos kirjataan ja sen hyllytyksen tallennetaan **Varaston hyllytys** -asiakirjan avulla.  

> [!NOTE]  
> Kokoonpanoprosessit eivät tue varaston hyllytyksiä. Voit kirjata tuotoksen rekisteröimällä kokoonpanotilauksen. Jos käytät varastopaikkoja, voit siirtää nimikkeitä varastopaikkojen välillä myöhemmin. Lisätietoja on kohdassa [Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

Jos laajennetut varastomääritykset edellyttävät sijainnissa sekä hyllytyksen että vastaanoton käsittelyä, voit hyllyttää tuotoksen luomalla joko sisäisen hyllytysasiakirjan tai siirtoasiakirjan.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Tuotannon tuotosten hyllyttäminen varastohyllytyksen avulla

Tuotoksen hyllytyksen luonnin ensimmäinen vaihe on luoda saapuvan varastoinnin pyyntö. Tämä pyyntö ilmaisee fyysiselle varastolle, että tuotanto- tai kokoonpanotilauksen tuotos on valmis hyllytettäväksi.

### <a name="to-create-the-inbound-warehouse-request"></a>Saapuvan f. varastoinnin pyyntö

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vapautettu tuotantotilaus** ja valitse sitten vastaava linkki.  
2. Valitse ensin hyllytykseen valmis tuotantotilaus ja sitten **Luo saapuva f. var. pyyntö** -toiminto.  

> [!NOTE]  
> Voit luoda saapuvan fyysisen varastoinnin pyynnön myös valitsemalla **Luo saapuva pyyntö** --kentän, kun päivität tuotantotilauksen. Lisätietoja on kohdassa [Tuotantotilausten päivittäminen tai uudelleensuunnittelu](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-away-output-with-an-inventory-put-away"></a>Nimikkeiden hyllyttäminen varastohyllytyksen avulla

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston hyllytys** ja valitse sitten vastaava linkki.  
2. Luo uusi varaston hyllytys. Lisätietoja on kohdassa [Nimikkeiden hyllyttäminen varaston hyllytyksen avulla](warehouse-how-to-put-items-away-with-inventory-put-aways.md)
3. Voit tarkastella tuotantotilauksen tuotosta valitsemalla ensin **Hae lähdedokumentit** -toiminnon ja sitten vapautetun tuotantotilauksen.  
4. Täytä hyllytysrivit tarpeen mukaan.
5. Kun rivit ovat valmiit kirjaamista varten, valitse **Kirjaa**-toiminto. Kirjaus luo fyysisen varaston tapahtumat ja kirjaa nimikkeiden tuotoksen.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Voit myös luoda **Varaston hyllytyksen** suoraan vapautetusta tuotantotilauksesta. Lisätietoja on kohdassa [Nimikkeiden hyllyttäminen varaston hyllytyksen avulla](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  

Kun kirjaat varastohyllytyksen, oletuksena on, että kaikki toiminnot kirjataan vakioreitityksen mukaan. Toisien sanoen viimeisimmän toiminnon tuotoksen määrä kirjataan. Voit käyttää tuotospäiväkirjaa kirjaamaan varianssit tuotoksen määrässä sekä asennuksen ja ajoajat. Jos osittainen kirjaus on tehtävä varaston hyllytyksen luonnin jälkeen, se voidaan tehdä kaikkien muiden paitsi viimeisimmän toiminnon määritettyjen aikojen ja määrien osalta. Varaston hyllytys ohjaa viimeistä työvaihetta.  

Jos vain viimeisen toiminnon määritys- tai ajoaika on kirjattava, määritä viimeisen toiminnon tuotoksen määräksi 0. Viimeinen rivi voidaan jättää kirjaamatta myös poistamalla se.

## <a name="to-put-away-assembly-and-production-output-in-advanced-warehouse-configurations"></a>Kokoonpanon tai tuotannon tuloksen hyllytys laajennetuissa varastointimäärityksissä

Kun kirjaat tuotanto- tai kokoonpanotilauksen tuotoksen fyysiseen varastoon, joka käyttää ohjattua hyllytystä ja poimintaa, tuotos sijoitetaan varastopaikkaan, joka on määritetty tuotanto- tai kokoonpanotilauksessa. Lisätietoja erilaisista tavoista siirtää nimikkeitä fyysisessä varastossa laajennettujen määritysten avulla on kohdassa [Nimikkeiden siirtäminen laajennetuissa varastomäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Lähdeasiakirjan numeroa, kuten tuotantotilauksen numeroa ei voi syöttää kokoonpano- tai tuotannon tuotosprosessien sisäisessä hyllytyksen, hyllytyksen tai siirron asiakirjoissa.  

## <a name="see-also"></a>Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
