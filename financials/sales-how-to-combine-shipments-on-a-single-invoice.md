---
title: "Toimitusten yhdistäminen yhteen laskuun | Microsoft Docs"
description: "Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilasku-ominaisuutta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e6be50119da5c617ce6dbf603903266f9ced821e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-combine-shipments-on-a-single-invoice"></a>Toimitusten yhdistäminen yhteen laskuun
Jos haluat laskuttaa useamman kuin yhden toimituksen kerralla, voit käyttää koontilaskuominaisuutta.  

 Ennen kuin koontilaskun voi luoda, samalle asiakkaalle täytyy kirjata useita myyntitoimituksia samassa valuutassa. Toimintoa voi siis käyttää, kun vähintään kaksi myyntitilausta on täytetty ja kirjattu toimitetuiksi (muttei laskutetuiksi). **Asiakaskortin** **Toimitus**-pikavälilehden **Tee koontilasku** -valintaruutu on valittava, jotta palautustoimituksia voidaan yhdistää.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Yhdistä manuaalisesti toimitukset yhteen laskuun  
1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Uusi**-toiminto. Lisätietoja on ohjeaiheessa [Toimintaohje: Myynnin laskuttaminen](sales-how-invoice-sales.md).
3. Valitse **Tilausasiakkaan nro** asiakas, jolle toimitettujen nimikkeiden lasku lähetetään.  
4. Valitse **Rivit**-pikavälilehdessä **Hae toimitusrivit** -toiminto.  
5. Valitse laskuun sisällytettävä toimitusrivi:  

    - Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**.  
    - Voit lisätä kaikki rivit valitsemalla kaikki rivit ja valitsemalla sitten **OK**. Voit käyttää Ctrl-näppäintä valitsemaan useita ei-perättäisiä rivejä.  

    Jos valitsit virheellisen rivin tai haluat aloittaa alusta, voit yksinkertaisesti poistaa laskun rivit ja ajaa **Hae toimitusrivit** -toiminnon uudelleen.  
7. Kirjaa lasku valitsemalla **Kirjaa**-toiminto.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Yhdistä automaattisesti toimitukset yhteen laskuun  
1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, kirjoita **Tee koontilasku** ja valitse sitten aiheeseen liittyvä linkki. Eräajon pyynnön ikkuna aukeaa.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Valitse **Kirjaa laskut** -valintaruutu.  
4.  Valitse **OK**-painike.  

> [!NOTE]  
>  Huomaa, että laskut on kirjattava manuaalisesti, jos eräajon **Kirjaa laskut** -valintaruutua ei ole valittu.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Avoimen myyntitilauksen poistaminen koontilaskun kirjauksen jälkeen 
Kun koontilasku on tehty ja kirjattu, laskutetuille riveille luodaan kirjattu myyntilasku. Alkuperäisen puitemyyntitilauksen tai myyntitilauksen **Laskutettu määrä** -kenttä päivitetään laskutetun määrän perusteella.  

Kun laskutat toimitukset näin, säilyvät tilaukset, joista toimitukset kirjattiin, vaikka ne olisi toimitettu ja laskutettu täysin.   

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Poista laskutetut myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Määritä **Numero** -kenttään , mitkä myyntitilaukset poistetaan.  
3. Valitse **OK**-painike.  

Voit myös poistaa manuaalisesti yksittäiset myyntitilaukset.  

Toista vaiheet 1–3 muissa käsiteltävissä asiakirjoissa, kuten puitemyyntitilauksissa.

## <a name="see-also"></a>Katso myös  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

