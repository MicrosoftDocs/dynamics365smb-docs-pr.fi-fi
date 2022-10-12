---
title: Poiminta sisäisissä toiminnoissa laajennetuissa varastomäärityksissä
description: Jos sijainnit käyttävät poimintaa ja toimituksia, poimi komponentteja tuotannon, kokoonpanon ja projektin toimintoja varten F.varastoinnin poiminta -sivulla.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/02/2022
ms.author: bholtorf
ms.openlocfilehash: 2ef879e5dbabb9281114d62a956ad4b10113c199
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607551"
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Tuotanto-, kokoonpano- ja projektipoiminta laajennetuissa varastointimäärityksissä

Jos sijainti on määritetty laajennetuissa varastomäärityksissä käyttämään poimintaa ja toimitusta, tuotannon ja kokoonpanon toimintojen komponentteja voi poimia **F.varastoinnin poiminta** -sivulla.  

Voit siirtää kohteita varastopaikasta toiseen **Siirtotyökirja**-sivulla spontaanisti ilman viittausta lähdeasiakirjaan. Lisätietoja on kohdassa [Nimikkeiden siirtäminen laajennetussa varastointimäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Lisätietoja nimikkeiden poiminnasta niissä fyysisen varaston perussijainneissa, jotka on määritetty vain poimintaa varten, on kohdassa [Komponenttien siirtäminen toiminta-alueelle fyysisen varastoinnin määrityksissä](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

> [!NOTE]
> Fyysisen varastoinnin poiminta-asiakirjaa voi luoda alusta alkaen, koska poiminta-aktiviteetti on aina osa työnkulkua sekä veto- että työntötilanteessa.  

Voit luoda fyysisen varastoinnin poiminta-asiakirjan valitsemalla push-muodissa **Luo F.var. poiminta** lähdeasiakirjassa, kuten julkaistu kokoonpanotilaus tai fyysisen varaston toimitus. Lisätietoja on kohdassa [Nimikkeiden poiminta fyysisen varaston poiminnassa](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Voit myös luoda fyysisen varastoinnin poiminta-asiakirjan käyttämällä **Poimintatyökirja**-sivua poimintapyyntöjen havaitsemiseksi. Tämä menetelmä on hyödyllinen toimituksessa ja sisäisessä toiminnassa. Tämän jälkeen voit luoda vaadittavat fyysisen varastoinnin poiminta-asiakirjat.  

Seuraavassa ohjeissa selitetään vetotilanne, jossa **Valitse työkirja** -sivulla poimitaan komponentteja vapautetulle tuotantotilaukselle. Menettely koskee myös kokoonpanotilauksia.  

Luodaksesi poimintapyynnöt sekä veto- että työntötilanteille, kyseiset lähdeasiakirjat on vapautettava. Vapauta sisäisten toimintojen lähdeasiakirjat seuraavilla tavoilla.  

|Lähdeasiakirja|Vapautustapa|  
|---------------------|--------------------|  
|Tuotantotilaus|Muuta tilauksen tyypiksi vapautettu tuotantotilaus.|  
|Kokoonpanotilaus|Muuta tilaksi Vapautettu.|
|Projektit | Muuta tilaksi Avoin.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Komponenttien poiminta poimintatyökirjoista

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poimintatyökirja** ja valitse sitten vastaava linkki.  
2. Valitse ensin **Hae f. varastoinnin asiakirjat** -toiminto ja sitten komponenttirivit vapautetusta tuotantotilauksesta.  
3. Järjestä rivit, jotta poiminta on mahdollisimman tehokasta. Haluat ehkä yhdistää rivit työntekijän ajan tallentamista varten.  
4. Valitse **Luo poiminta** -toiminto.  
5. Määritä, miten voit luoda fyysisen varastoinnin poiminta-asiakirjat ja lajitella poimintarivit täyttämällä kentät **Luo poiminta** -sivulla.  
6. Valitse **OK**-painike. Varastopoiminta-asiakirjat on luotu poimintarivien kanssa jokaiselle osalle, jota tarvitaan sisäisessäl toiminnassa.  

Toimintoalueilla, kuten tuotannon varastopaikoissa, voi olla oletusvarastopaikka vaadituille komponenteille. Jos se on olemassa, oletusvarastopaikkakoodi lisätään fyysisen varaston poiminta-asiakirjaan osoittamaan, minne nimikkeet sijoitetaan. Lisätietoja on työkaluvihjeissä **Tuotannon valmisteluvarastopaikkakoodi** tai **Kokoonpanoon-varastop.koodi** -kentässä.

## <a name="filling-the-consumption-bin"></a>Kulutuksen varastopaikan täyttäminen

Tämä työnkulkukaavio näyttää, miten tuotantotilauksen osarivien **Varastopaikkakoodi**-kenttä täytetään sijaintiasetusten mukaisesti.

![Varastopaikkojen työnkulkukaavio.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Katso myös

[Varastoinninhallinta](warehouse-manage-warehouse.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
