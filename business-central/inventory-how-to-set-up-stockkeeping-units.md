---
title: Varastointiyksiköiden määrittäminen
description: Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 5704, 5700, 5702, 5701
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e61c61f760dd14145ecea76f36903f8a4124cac5
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533749"
---
# <a name="set-up-stockkeeping-units"></a>Varastointiyksiköiden määrittäminen

Voit tallentaa tiettyä sijaintia ja/tai varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.  

Varastointiyksiköt ovat lisätietona nimikekorteille. Ne eivät korvaa niitä, vaikka liittyvätkin niihin. Varastointiyksiköt mahdollistavat nimikkeen tietojen erittelemisen tietyn sijainnin osalta (esimerkiksi fyysisen varaston tai jakelupaikan osalta) tai saman nimikkeen tietyn variantin osalta (esimerkiksi eri hyllynumeroiden ja eri täydennystietojen osalta).  

## <a name="to-set-up-a-stockkeeping-unit"></a>Varastointiyksiköiden määrittäminen  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastointiyksiköt** ja valitse sitten vastaava linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Syötä kortin kentät. Seuraavat kentät ovat pakollisia: **Nimikkeen nro**, **Paikkakoodi**, ja **Varianttikoodi**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Kun olet määrittänyt nimikkeen ensimmäisen varastointiyksikön, **Nimike**-kortin **Varastointiyks. on olemassa** -valintaruutu on valittu.  

Käytä **Luo varastointiyksikkö** -eräajoa, kun haluat luoda nimikkeelle useita varastointiyksiköitä.  

> [!NOTE]  
>  **Varastointiyksikön** kortin tiedoilla on korkeampi prioriteetti kuin **nimikkeen** kortilla.

> [!Warning]
> Jos varastointiyksikkö toimitetaan tuotannon välityksellä, **Vakiokustannus**-kenttää ei käytetä tuotetun nimikkeen todellisten kustannusten laskutuksessa ja oikaisussa. Sen sijaan käytetään pohjana olevan nimikekortin **Vakiokustannus**-kenttää, ja kaikki varianssit lasketaan nimikkeen kustannusjakaumia kohden.<br /><br />
> Koska tuotannon tuoterakenteita ja reititystä ei voida määrittää SKU:ihin, koottu yksikkökustannus ja liittyvät kustannusjakauman laskennat eivät myöskään ole käytettävissä SKU:issa. Lisätietoja on kohdassa [Tietoja vakiokustannusten laskennasta](finance-about-calculating-standard-cost.md).

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/control-inventory-multiple-locations/)

## <a name="see-also"></a>Katso myös

[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
