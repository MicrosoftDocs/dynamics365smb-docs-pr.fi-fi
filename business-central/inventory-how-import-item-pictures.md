---
title: Useiden nimikekuvien tuominen ZIP-tiedostosta
description: Jos haluat tuoda useita nimikekuvia, anna kuvatiedostoille nimikenumeroita vastaavat nimet, pakkaa ne ZIP-tiedostoon ja hallinnoi sitten nimikekuvien tuontia Tuo nimikekuvat -sivulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.search.form: 30, 461
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 81e628a80fe170789bb174cd393842bdf2db9af5
ms.sourcegitcommit: 1e6addcd6ecc25489fc17388409989440a210895
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/14/2022
ms.locfileid: "7975016"
---
# <a name="import-multiple-item-pictures"></a>Useiden nimikekuvien tuominen
 Voit tuoda kerralla useita nimikekuvia. Sinun tarvitsee vain antaa kuvatiedostoille nimikenumeroita vastaavat nimet, pakata ne zip-tiedostoon ja hallita sitten nimikekuivien tuontia Tuo nimikekuvat -sivulla.

Kaikkia yleisiä tiedostomuotoja tuetaan.

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a>Kuvatiedostojen nimeäminen nimikenimillä ja ZIP-tiedoston valmisteleminen
1. Anna kullekin tiedostolle nimikekuvien tallennussijainnissa nimi, joka vastaa liittyvän nimikkeen numeroa. Esimerkiksi:

    |Nimikkeen nro|Tiedostonimi|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Kerää kaikki tiedostot ZIP-tiedostoon. Valitse esimerkiksi Resurssienhallinnassa ensin tiedostot ja sitten **Lähetä kohteeseen** ja **Pakattu kansio (zip-tiedosto)**.     

## <a name="to-import-item-pictures"></a>Nimikekuvien tuominen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastonhallinnan asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Tuo nimikekuva** -toiminto.
3. Valitse **Valitse ZIP-tiedosto** -kentässä oikea ZIP-kansio ja valitse sitten **Avaa**-painike.

    **Tuo nimikekuvat** -sivulla luodaan jokaiselle nimikkeelle ja kuvalle luodaan rivi.

    > [!NOTE]
    > Jos nimikekortissa on jo kuva, **Kuva on jo olemassa** -valintaruutu on jo valittu. Jos et haluat korvata mitään olemassa olevaa kuvaa, poista **Korvaa kuvat** -valintaruudun valinta. Jos et halua korvata yksittäisiä olemassa olevia kuvia, poista kyseiset rivit.

3. Valitse **Tuo kuvat** -toiminto.

**Tuonnin tila** -kenttä päivitetään näyttämään, onko kuvan tuonti ohitettu tai onko se valmis.       

## <a name="see-also"></a>Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Numerosarjojen luominen](ui-create-number-series.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]