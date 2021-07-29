---
title: Varastoyksikköjen määrittäminen | Microsoft Docs
description: Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 6a59bf05139f4b073470092aa136018d9f3d988e
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445649"
---
# <a name="set-up-stockkeeping-units"></a>Varastointiyksiköiden määrittäminen
Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.  

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

## <a name="see-also"></a>Katso myös  
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]