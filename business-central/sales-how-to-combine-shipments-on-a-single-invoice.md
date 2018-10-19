---
title: "Toimitusten yhdistäminen yhteen laskuun | Microsoft Docs"
description: "Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 429002d1eb6bfa487e5a21e54964ce33de175441
ms.contentlocale: fi-fi
ms.lasthandoff: 09/28/2018

---
# <a name="combine-shipments-on-a-single-invoice"></a>Toimitusten yhdistäminen yhteen laskuun
Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta.  

 Ennen kuin koontilaskun voi luoda, samalle asiakkaalle täytyy kirjata useita myyntitoimituksia samassa valuutassa. Toimintoa voi siis käyttää, kun vähintään kaksi myyntitilausta on täytetty ja kirjattu toimitetuiksi (muttei laskutetuiksi). **Asiakaskortin** **Toimitus**-pikavälilehden **Tee koontilasku** -valintaruutu on valittava, jotta palautustoimituksia voidaan yhdistää.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Yhdistä manuaalisesti toimitukset yhteen laskuun  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntilaskut** ja valitse sitten liittyvä linkki.  
2. Valitse **Uusi**-toiminto. Lisätietoja on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).
3. Valitse **Tilausasiakkaan nro** asiakas, jolle toimitettujen nimikkeiden lasku lähetetään.  
4. Valitse **Rivit**-pikavälilehdessä **Hae toimitusrivit** -toiminto.  
5. Valitse laskuun sisällytettävä toimitusrivi:  

    - Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.  
    - Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**. Voit käyttää Ctrl-näppäintä valitsemaan useita ei-perättäisiä rivejä.  

    Jos valitsit virheellisen rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa laskun rivit ja ajaa **Hae toimitusrivit** -toiminnon uudelleen.  
7. Kirjaa lasku valitsemalla **Kirjaa**-toiminto.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Yhdistä automaattisesti toimitukset yhteen laskuun  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tee koontilasku** ja valitse sitten liittyvä linkki. Eräajon pyynnön ikkuna aukeaa.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Kirjaa laskut** -valintaruutu.  
4.  Valitse **OK**-painike.  

> [!NOTE]  
>  Huomaa, että laskut on kirjattava manuaalisesti, jos eräajon **Kirjaa laskut** -valintaruutua ei ole valittu.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Avoimen myyntitilauksen poistaminen koontilaskun kirjauksen jälkeen 
Kun koontilasku on tehty ja kirjattu, laskutetuille riveille luodaan kirjattu myyntilasku. Alkuperäisen puitemyyntitilauksen tai myyntitilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän perusteella.  

Kun laskutat toimitukset näin, säilyvät tilaukset, joista toimitukset kirjattiin, vaikka ne olisi toimitettu ja laskutettu täysin.   

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista laskutetut myyntitilaukset** ja valitse sitten liittyvä linkki.  
2. Määritä **Numero** -kenttään , mitkä myyntitilaukset poistetaan.  
3. Valitse **OK**-painike.  

Voit myös poistaa manuaalisesti yksittäiset myyntitilaukset.  

Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puitemyyntitilauksissa.

## <a name="see-also"></a>Katso myös  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

