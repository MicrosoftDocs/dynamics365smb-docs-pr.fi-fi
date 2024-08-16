---
title: Tuotoksen hyllyttäminen
description: Tässä artikkelissa käsitellään tuotannon tuotoksen hyllyttämistä.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# <a name="put-away-production-or-assembly-output"></a>Tuotannon tai kokoonpanon tuotoksen hyllyttäminen

Tuotannon hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

Aktivoi seuraavat asetukset saapuvan työnkulun (hyllytyksen) **fyysisen varastoinnin perusmäärityksessä sijainnin Sijainti-kortti**  sivulla:

* Tuotantoa **varten Tuotoksen tuotoksen f. var. Käsittely-kenttä**, valitse **Varastohyllytys**.
* Kokoonpanoprosessit eivät tue varaston hyllytyksiä. Voit kirjata tuotoksen rekisteröimällä kokoonpanotilauksen. Jos käytät varastopaikkoja, voit siirtää nimikkeitä varastopaikkojen välillä myöhemmin. Lisätietoja on kohdassa [Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  
* Projektien hyllytys ei ole käytössä.

Laajennetuissa fyysisen varastoinnin määrityksissä, joissa sijainti vaatii hyllytystä, voit hyllyttää tuotoksen luoden sisäisen hyllytysasiakirjan tai siirtoasiakirjan.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Tuotannon tuotosten hyllyttäminen varastohyllytyksen avulla

Tuotoksen hyllytyksen luonnin ensimmäinen vaihe on luoda saapuvan varastoinnin pyyntö. Tämä pyyntö ilmaisee fyysiselle varastolle, että tuotanto- tai kokoonpanotilauksen tuotos on valmis hyllytettäväksi.

### <a name="to-create-the-inbound-warehouse-request"></a>Saapuvan f. varastoinnin pyyntö

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vapautettu tuotantotilaus** ja valitse sitten vastaava linkki.  
2. Valitse ensin hyllytykseen valmis tuotantotilaus ja sitten **Luo saapuva f. var. pyyntö** -toiminto.  

> [!NOTE]  
> Voit luoda saapuvan fyysisen varastoinnin pyynnön myös valitsemalla **Luo saapuva pyyntö** --kentän, kun päivität tuotantotilauksen. Lisätietoja on kohdassa [Tuotantotilausten päivittäminen tai uudelleensuunnittelu](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-away-output-with-an-inventory-put-away"></a>Tuotoksen hyllyttäminen varaston hyllytyksen avulla

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston hyllytys** ja valitse sitten vastaava linkki.  
2. Luo uusi varaston hyllytys. Lisätietoja on kohdassa [Nimikkeiden hyllyttäminen varaston hyllytyksen avulla](warehouse-how-to-put-items-away-with-inventory-put-aways.md)
3. Voit tarkastella tuotantotilauksen tuotosta valitsemalla ensin **Hae lähdedokumentit** -toiminnon ja sitten vapautetun tuotantotilauksen.  
4. Täytä hyllytysrivit tarpeen mukaan.
5. Kun rivit ovat valmiit kirjaamista varten, valitse **Kirjaa**-toiminto. Kirjaus luo fyysisen varastoinnin tapahtumat ja kirjaa nimikkeiden tuotoksen.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Voit myös luoda **Varaston hyllytyksen** suoraan vapautetusta tuotantotilauksesta. Lisätietoja on kohdassa [Nimikkeiden hyllyttäminen varaston hyllytyksen avulla](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  

Kun kirjaat varaston hyllytyksen, oletetaan, [!INCLUDE [prod_short](includes/prod_short.md)]  että kaikki operaatiot kirjataan vakioreitityksen mukaisesti. Toisien sanoen viimeisimmän toiminnon tuotoksen määrä kirjataan. Voit käyttää tuotospäiväkirjaa kirjaamaan varianssit tuotoksen määrässä sekä asennuksen ja ajoajat. Jos kirjaat osittain sen jälkeen, kun olet luonut varaston hyllytyksen, voit tehdä sen asetusajoissa ja -määrissä kaikkien operaatioiden osalta lukuun ottamatta viimeistä operaatiota. Varaston hyllytys ohjaa viimeistä operaatiota.  

Jos sinun tarvitsee kirjata vain viimeisen operaation asetukset tai ajoaika, aseta viimeisen operaation tuotosmääräksi 0. Voit valita, ettet kirjaa viimeistä riviä ollenkaan poistamalla sen.

## <a name="to-put-away-assembly-and-production-output-in-advanced-warehouse-configurations"></a>Kokoonpanon ja tuotannon tuotoksen hyllyttäminen laajennetuissa fyysisen varastoinnin määrityksissä

Kun tuotanto- tai kokoonpanotilauksen tuotos kirjataan ohjattua hyllytystä ja poimintaa käyttävässä fyysisessä varastossa, tuotos siirtyy tuotanto- tai kokoonpanotilauksessa määritettyyn varastopaikkaan. Lisätietoja nimikkeiden eri siirtotavoista fyysisessä varastoinnissa, jossa on lisäasetuksia, siirry nimikkeiden siirtoon [laajennetuissa fyysisen varastoinnin määrityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Lähdeasiakirjan numeroa, kuten tuotantotilauksen numeroa ei voi syöttää kokoonpano- tai tuotannon tuotosprosessien sisäisessä hyllytyksen, hyllytyksen tai siirron asiakirjoissa.  

## <a name="see-also"></a>Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
