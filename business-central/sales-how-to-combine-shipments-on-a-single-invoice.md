---
title: Toimitusten yhdistäminen yhteen laskuun | Microsoft Docs
description: Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2936e819ba50adde6df021cc0dc2694367c29fc9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778495"
---
# <a name="combine-shipments-on-a-single-invoice"></a>Toimitusten yhdistäminen yhteen laskuun
Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.  

Ennen kuin koontilaskun voi luoda, samalle asiakkaalle täytyy kirjata useita myyntitoimituksia samassa valuutassa. Toimintoa voi siis käyttää, kun vähintään kaksi myyntitilausta luodaan ja kirjataan toimitetuiksi, mutta ei laskutetuiksi. 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Yhdistä manuaalisesti toimitukset yhteen laskuun  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).
3. Valitse **Tilausasiakkaan nro** asiakas, jolle toimitettujen nimikkeiden lasku lähetetään.  
4. Valitse **Rivit**-pikavälilehdessä **Hae toimitusrivit** -toiminto.  
5. Valitse laskuun sisällytettävä toimitusrivi:  

    - Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.  
    - Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**. Voit käyttää Ctrl-näppäintä valitsemaan useita ei-perättäisiä rivejä.  

    Jos valitsit virheellisen rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa laskun rivit ja ajaa **Hae toimitusrivit** -toiminnon uudelleen.  
7. Kirjaa lasku valitsemalla **Kirjaa**-toiminto.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Yhdistä automaattisesti toimitukset yhteen laskuun  
[!INCLUDE[prod_short](includes/prod_short.md)] valitsee vain ne myyntitilaukset, joissa on valittu **koontilasku**. 

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Toimitusten yhdistäminen** ja valitse sitten liittyvä linkki. Eräajon pyynnön sivu aukeaa.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Kirjaa laskut** -valintaruutu.  
4. Valitse **OK**-painike.  

> [!NOTE]  
>  Huomaa, että laskut on kirjattava manuaalisesti, jos eräajon **Kirjaa laskut** -valintaruutua ei ole valittu.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Avoimen myyntitilauksen poistaminen koontilaskun kirjauksen jälkeen 
Kun koontilasku on tehty ja kirjattu, laskutetuille riveille luodaan kirjattu myyntilasku. Alkuperäisen puitemyyntitilauksen tai myyntitilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän perusteella.  

Kun laskutat toimitukset näin, säilyvät tilaukset, joista toimitukset kirjattiin, vaikka ne olisi toimitettu ja laskutettu täysin.   

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Poista laskutetut myyntitilaukset** ja valitse sitten liittyvä linkki.  
2. Määritä **Numero** -kenttään , mitkä myyntitilaukset poistetaan.  
3. Valitse **OK**-painike.  

Voit myös poistaa manuaalisesti yksittäiset myyntitilaukset.  

Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puitemyyntitilauksissa.

## <a name="see-also"></a>Katso myös  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]