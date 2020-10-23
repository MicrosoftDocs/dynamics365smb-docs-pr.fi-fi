---
title: Varastoyksikköjen määrittäminen | Microsoft Docs
description: Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4f5a1933e803322367b241e772d796f1365f9d11
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915458"
---
# <a name="set-up-stockkeeping-units"></a>Varastointiyksiköiden määrittäminen
Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.  

 Varastointiyksiköt ovat lisätietona nimikekorteille. Ne eivät korvaa niitä, vaikka liittyvätkin niihin. Varastointiyksiköt mahdollistavat nimikkeen tietojen erittelemisen tietyn sijainnin osalta (esimerkiksi fyysisen varaston tai jakelupaikan osalta) tai saman nimikkeen tietyn variantin osalta (esimerkiksi eri hyllynumeroiden ja eri täydennystietojen osalta).  

## <a name="to-set-up-a-stockkeeping-unit"></a>Varastointiyksiköiden määrittäminen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Varastointiyksiköt** ja valitse sitten liittyvä linkki.  
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
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
