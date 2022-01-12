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
ms.date: 12/16/2021
ms.author: edupont
ms.openlocfilehash: e111c08dc9251898ccecff4e65f768984b123c15
ms.sourcegitcommit: 088bb19634f60891a12736c034ab3e86bdb91891
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2021
ms.locfileid: "7929578"
---
# <a name="combine-shipments-on-a-single-invoice"></a>Toimitusten yhdistäminen yhteen laskuun
Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.  

Ennen kuin koontilaskun voi luoda, samalle asiakkaalle täytyy kirjata useita myyntitoimituksia samassa valuutassa. Toimintoa voi siis käyttää, kun vähintään kaksi myyntitilausta luodaan ja kirjataan toimitetuiksi, mutta ei laskutetuiksi. 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Yhdistä manuaalisesti toimitukset yhteen laskuun  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).
3. Valitse **Tilausasiakkaan nro** asiakas, jolle toimitettujen nimikkeiden lasku lähetetään.  
4. Valitse **Rivit**-pikavälilehdessä **Hae toimitusrivit** -toiminto.  
5. Valitse laskuun sisällytettävä toimitusrivi:  

    - Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.  
    - Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**. Voit käyttää Ctrl-näppäintä valitsemaan useita ei-perättäisiä rivejä.  

    Jos valitsit virheellisen rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa laskun rivit ja ajaa **Hae toimitusrivit** -toiminnon uudelleen.  
7. Kirjaa lasku valitsemalla **Kirjaa**-toiminto.  

> [!TIP]  
> Jos olet toimittanut tilauksia, joissa **tilausasiakkaan nro** on eri kuin **Laskutus asiakkaan nro**, näitä rivejä ei näytetä **Hae toimitusrivit** -raportissa. Lisää **Tilausasiakas**-kenttä sivulle räätälöinnin avulla ja poista suodatin. Nyt voit lisätä toimitusrivejä laskuun riippumatta **tilausasiakkaan nro** -kentän arvosta niin kauan kuin **Laskutus asiakkaan nro** toimitusrivit vastaavat myyntilaskun arvoa.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Yhdistä automaattisesti toimitukset yhteen laskuun  
[!INCLUDE[prod_short](includes/prod_short.md)] valitsee vain ne myyntitilaukset, joissa on valittu **koontilasku**. 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tee koontilasku** ja valitse sitten vastaava linkki. Eräajon pyynnön sivu aukeaa.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Kirjaa laskut** -valintaruutu.  
4. Valitse **OK**-painike.  

> [!NOTE]  
>  Huomaa, että laskut on kirjattava manuaalisesti, jos eräajon **Kirjaa laskut** -valintaruutua ei ole valittu.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Avoimen myyntitilauksen poistaminen koontilaskun kirjauksen jälkeen 
Kun koontilasku on tehty ja kirjattu, laskutetuille riveille luodaan kirjattu myyntilasku. Alkuperäisen puitemyyntitilauksen tai myyntitilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän perusteella.  

Kun laskutat toimitukset näin, säilyvät tilaukset, joista toimitukset kirjattiin, vaikka ne olisi toimitettu ja laskutettu täysin.   

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista laskutetut myyntitilaukset** ja valitse sitten linkki.  
2. Määritä **Numero** -kenttään , mitkä myyntitilaukset poistetaan.  
3. Valitse **OK**-painike.  

Voit myös poistaa manuaalisesti yksittäiset myyntitilaukset.  

Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puitemyyntitilauksissa.

## <a name="see-also"></a>Katso myös  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
