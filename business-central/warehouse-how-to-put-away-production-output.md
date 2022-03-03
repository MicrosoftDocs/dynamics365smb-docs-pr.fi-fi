---
title: Tuotannon tuotoksen hyllyttäminen
description: Tuotannon hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina Varaston hyllytys voidaan suorittaa seuraavilla tavoilla.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: e93c4d5abd6b6c3136e95838d10895a8fb1b2b90
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134535"
---
# <a name="put-away-production-or-assembly-output"></a>Tuotannon tai kokoonpanon tuotoksen hyllyttäminen

Tuotannon hyllytystapa määräytyy sen mukaan, miten fyysinen varasto on määritetty sijaintina Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

Jos fyysisen varastoinnin perusmääritykset edellyttävät sijainnissa on hyllytyksen käsittely, tuotannon jälkeinen tulos ja tuotoksen hyllytys kirjataan **Varaston hyllytys** -asiakirjan avulla.  

> [!NOTE]  
> Kokoamisprosessit eivät tue varaston hyllytystä. Voit kirjata tuotoksen rekisteröimällä kokoonpanotilauksen. Jos käytät varastopaikkoja, voit siirtää nimikkeitä varastopaikkojen välillä myöhemmin. Lisätietoja on kohdassa [Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

Jos laajennetut varastomääritykset edellyttävät sijainnissa sekä hyllytyksen että vastaanoton käsittelyä, voit hyllyttää tuotoksen luomalla joko sisäisen hyllytysasiakirjan tai siirtoasiakirjan.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Tuotannon tuotosten hyllyttäminen varastohyllytyksen avulla

Tuotoksen hyllytyksen luonnin ensimmäinen vaihe on saapuvan varastoinnin pyynnön luonti. Tämä pyyntö ilmaisee fyysiselle varastolle, että tuotanto- tai kokoonpanotilauksen tuotos on valmis hyllytettäväksi.

### <a name="to-create-the-inbound-warehouse-request"></a>Saapuvan f. varastoinnin pyyntö  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vapautettu tuotantotilaus** ja valitse sitten vastaava linkki.  
2.  Valitse hyllytystä odottavassa tuotantotilauksessa **Luo saapuva f. var. pyyntö** -toiminto.  

> [!NOTE]  
> Voit luoda saapuvan fyysisen varastoinnin pyynnön myös valitsemalla **Luo saapuva pyyntö** --kentän, kun päivität tuotantotilauksen. Lisätietoja on kohdassa [Tuotantotilausten päivittäminen tai uudelleensuunnitteleminen](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Nimikkeiden hyllyttäminen varastohyllytyksen avulla  
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston hyllytys** ja valitse sitten vastaava linkki.  
2.  Luo uusi varaston hyllytys. Lisätietoja on kohdassa [Nimikkeiden hyllyttäminen varaston hyllytyksillä](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Voit tarkastella tuotantotilauksen tuotosta valitsemalla ensin **Hae lähdedokumentit** -toiminnon ja sitten vapautetun tuotantotilauksen.  
4.  Kirjoita hyllytysriveille halutut tiedot.
5.  Kun rivit ovat valmiit kirjaamista varten, valitse **Kirjaa**-toiminto. Kirjaus luo tarvittavat fyysisen varaston tapahtumat ja kirjaa nimikkeiden tuotoksen.  

Voit myös luoda **Varaston hyllytyksen** suoraan vapautetusta tuotantotilauksesta. Lisätietoja on kohdassa [Nimikkeiden hyllyttäminen varaston hyllytyksillä](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Kun kirjaat varastohyllytyksen, oletuksena on, että kaikki toiminnot kirjataan vakioreitityksen mukaan; toisien sanoen viimeisen toiminnon tuotoksen määrä kirjataan. Voit käyttää tuotospäiväkirjaa kirjataksesi varianssit tuotoksen määrässä sekä asennuksen ja ajoajat. Jos osittainen kirjaus vaaditaan varaston hyllytyksen luonnin jälkeen, näin voidaan tehdä kaikkien paitsi viimeisen toiminnon asetusaikojen ja määrien osalta. Tässä tapauksessa varaston hyllytys ohjaa viimeistä työvaihetta.  

Jos vain viimeisen toiminnon asetus- tai ajoaika on kirjattava, määritä viimeisen toiminnon tuotoksen määräksi 0. Vaihtoehtoisesti voit jättää viimeisen rivin kirjaamatta yksinkertaisesti poistamalla sen.  

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Kokoonpanon tai tuotannon tuloksen hyllytys laajennetuissa varastointimäärityksissä
Kun kirjaat tuotanto- tai kokoonpanotilauksen tuotoksen varastoon, joka on määritetty käyttämään ohjattua hyllytystä ja poimintaa, tuotos sijoitetaan varastopaikkaan, joka on määritetty tuotanto- tai kokoonpanotilauksessa. 

Seuraavassa taulukossa kuvataan eri tapoja siirtää nimikkeitä fyysisessä varastossa käyttäen laajennettuja määrityksiä, joissa kaikki fyysisen varastoinnin aktiviteetit täytyy suorittaa ohjatussa työnkulussa. 

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Siirrä nimikkeitä fyysisen varastoinnin siirtotyökirjan kanssa.|[Nimikkeiden siirtäminen laajennetuissa varastomäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet)|  
|Luo sisäinen hyllytys ja hyllytä tuotettuja ja kokoonpantuja nimikkeitä fyysisen varastoinnin laajennetussa varastointimäärityksessä.|[Sisäisen hyllytyksen luominen](warehouse-how-to-create-put-aways-from-internal-put-aways.md#to-create-an-internal-put-away)|

> [!NOTE]  
> Lähdeasiakirjan numeroa (tuotantotilauksen numeroa) ei voi syöttää sisäisen hyllytyksen, hyllytyksen tai siirron asiakirjoihin kummankaan menettelyn osalta.  

## <a name="see-also"></a>Katso myös  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
