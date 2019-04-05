---
title: Varastoyksikköjen määrittäminen | Microsoft Docs
description: Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/15/2018
ms.author: sgroespe
ms.openlocfilehash: d5582e1857481d32ad146d0732f4c60d1b678c74
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2019
ms.locfileid: "796401"
---
# <a name="set-up-stockkeeping-units"></a>Varastointiyksiköiden määrittäminen
Voit tallentaa tiettyä sijaintia ja/tai tiettyä varianttikoodia koskevat nimikkeen tiedot varastointiyksiköihin.  

 Varastointiyksiköt ovat lisätietona nimikekorteille. Ne eivät korvaa niitä, vaikka liittyvätkin niihin. Varastointiyksiköt mahdollistavat nimikkeen tietojen erittelemisen tietyn sijainnin osalta (esimerkiksi fyysisen varaston tai jakelupaikan osalta) tai saman nimikkeen tietyn variantin osalta (esimerkiksi eri hyllynumeroiden ja eri täydennystietojen osalta).  

## <a name="to-set-up-a-stockkeeping-unit"></a>Varastointiyksiköiden määrittäminen  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastointiyksiköt** ja valitse sitten liittyvä linkki.  
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
