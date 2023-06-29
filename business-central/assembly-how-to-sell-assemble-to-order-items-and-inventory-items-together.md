---
title: Kokoonpano tilausta varten -nimikkeiden ja varastonimikkeiden myyminen yhdessä
description: 'Jos osa varastoon kokoonpantavasta nimikkeestä ei ole saatavana, jäljellä olevalle määrälle voidaan luoda kokoonpanotilaus.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a><a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Kokoonpano tilausta varten -nimikkeiden ja varastonimikkeiden myyminen yhdessä

Jos kokoonpanon nimikkeen nimikekortin **Kokoonpanokäytäntö**-kenttä sisältää **Kokoonpano varastoon** -kohdan, myyntitilausprosessi olettaa, että nimike on jo kokoonpantu ja että se voidaan poimia varastosta, jos sitä on saatavana. Tämän vuoksi yhtään kokoonpanotilausta ei luoda automaattisesti ja linkitetä myyntitilauksen riviin. Jos osa määrästä tai koko määrä ei ole saatavana, jäljellä olevalle määrälle voidaan luoda kokoonpanotilaus. Se tehdään täyttämällä myyntitilausrivin **Kokoonpantava määrä tilausta varten** -kenttä. Tämä asetus mahdollistaa nimikkeen kokoonpanon tilausta varten, vaikka se on määritetty kokoonpantavaksi varastoon.  

Samalla tavoin joustavasti voidaan toimia, kun myytävänä on tilausta varten kokoonpantavia nimikkeitä ja osa määrästä on jo varastossa. Varastossa oleva määrä vähennetään kokoonpanotilauksesta. Lisätietoja varastonimikkeiden myymisestä on kohdassa [Varastonimikkeiden myyminen tilausta varten kokoonpantavien työnkuluissa](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Tietyt säännöt koskevat **Toimitettava määrä** -kenttää myyntitilauksen riveillä, jotka sisältävät tilausta varten kokoonpantavien määrien ja varastomäärien yhdistelmiä. Lisätietoja säännöistä on kohdassa [Yhdistelmäskenaariot](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> Seuraava toimenpide ei sisällä myyntitilauksen ennen kokoonpanotilauksen luontia sille määrälle tehtäviä vaiheita, joka ei ole saatavana.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a><a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Myy kokoonpano tilausta varten -nimikkeitä ja varastonimikkeitä yhdessä

1. Syötä varastoon kokoonpantavan nimikkeen myyntitilausrivin **Määrä**-kenttään määrä, joka on suurempi kuin varasto. **Tarkista saatavuus** -sivu avautuu. Lisätietoja nimikkeen saatavuudesta on kohdassa [Nimikkeiden saatavuuden näyttäminen](inventory-how-availability-overview.md).
2. Syötä **Kokoonpantava määrä tilausta varten** -kenttään **Määrä yhteensä** -kentän arvo.  
3. Tee tarvittavat muutokset kokoonpanon komponentteihin. Lisätietoja on kohdassa [Tilausta varten kokoonpantavien nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  
4. Vapauta myyntitilaus mahdollistamaan nimikkeiden poiminta ja ei saatavana olevien nimikkeiden kokoonpano. Lisätietoja kokoonpanon vakiovaiheista on kohdassa [Nimikkeiden kokoaminen](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Myyntitilauksen **Varastopaikkakoodi**-kentässä saattaa olla sijaintikortin **Kokoonpanot. toim. var.p.koodi**- tai **Kokoonpanosta-varastop.koodi** -kentän arvo. Siinä tapauksessa myyntitilauksen rivin **Varastopaikkakoodi** saattaa olla virheellinen tässä tilausten varten kokoonpantavien ja varastoon kokoonpantavien määrien yhdistelmässä. Kannattaakin varmistaa uudelleen **Varastopaikkakoodi**-kentässä oleva varastopaikka sopii kaikille määrille. Voit myös kirjoittaa kaksi eri määrää myyntitilauksen eri riveille.  

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Kokoonpanon tuoterakenteiden käyttäminen](assembly-how-work-assembly-boms.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastonhallinnan yleiskatsaus](design-details-warehouse-management.md)
[[!INCLUDE[prod_short](includes/prod_short.md)]in käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
