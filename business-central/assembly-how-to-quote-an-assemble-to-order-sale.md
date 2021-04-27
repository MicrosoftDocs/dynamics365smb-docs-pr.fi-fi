---
title: Kokoonpano tilausta varten -myynnin tarjous | Microsoft Docs
description: Voit mukauttaa kokoonpanonimikettä asiakkaan pyynnöstä myyntiprosessin kokoonpanon hallinnan avulla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 817699281ce0f3b7d057bb2e9ce4d85f97d67b48
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772952"
---
# <a name="quote-an-assemble-to-order-sale"></a>Kokoonpano tilausta varten -myynnin tarjous
Voit mukauttaa kokoonpanonimikettä asiakkaan pyynnöstä myyntiprosessin kokoonpanon hallinnan avulla. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  

Kuin silloin, kun myyt minkä tahansa muun tyyppisen nimikkeen, voit myös luoda myyntitarjouksen muokatulle kokoonpanonimikkeelle ennen kuin se muunnetaan myyntitilaukseksi. Tähän toimenpiteeseen liittyy useita ylimääräisiä vaiheita tavallisen puitemyyntitarjouksen luomiseen verrattuna, ja siinä käytetään linkitetyn kokoonpanotilauksen versiota, joka on puitekokoonpanotarjous.

> [!NOTE]  
>  Kaikentyyppisten tarjousten tapaan kokoonpanotarjousten määriä ei käytetä saatavuusmäärissä, suunnittelussa eikä varauksissa.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Luo myyntitarjous kokoonpano tilausta varten -nimikkeelle  
1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Myyntitarjous** ja valitse sitten liittyvä linkki.  
2.  Luo uusi myyntitarjousrivi yhdellä kokoonpanonimikkeen rivillä. Lisätietoja on kohdassa [Myyntitarjousten tekeminen](sales-how-make-offers.md).  
3.  Anna **Kokoonpantava määrä tilausta varten** -kentässä koko määrä.

    > [!NOTE]  
    >  Älä tee tarjousta osatoimituksesta. Sen vuoksi sinun täytyy syöttää sama määrä, jonka syötit myynnin puitetarjousrivin **Määrä**-kenttään.  

4.  Valitse **Rivit**-pikavalintalehdessä **Rivi**, valitse **Kokoonpano tilausta varten** ja valitse sitten **Kokoonpano tilausta varten -rivit**. Voit myös valita rivin **Kokoonpantava määrä tilausta varten** -kentän.  
5.  Tarkastele tai muokkaa **Kokoonpano tilausta varten -rivit** -sivulla asiakkaan pyytämän tarjouksen mukaisia kokoonpanotilauksen rivejä. Jos haluat tarkastella tietoja, avaa koko puitetarjoustilaus valitsemalla **Näytä asiakirja** -toiminto. Useimpien kenttien sisältöä ei voi muuttaa etkä voi kirjata.  
6.  Kun olet muokannut kokoonpanotilauksen rivejä tarjouksen mukaisesti, sulje **Kokoonpano tilausta varten -rivit** -sivu palataksesi **Myyntitarjous** -sivulle.  
7.  Jos asiakas hyväksyy tarjouksen, luo tarjotusta kokoonpanon nimikkeestä myyntitilaus. Lisätietoja on kohdassa [Myyntitarjousten tekeminen](sales-how-make-offers.md). Linkitetty kokoonpanotarjous ja kaikki muokkaukset on linkitetty uuteen myyntitilaukseen kokoonpanon tai myynnin valmistelua varten.  

## <a name="see-also"></a>Katso myös  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]