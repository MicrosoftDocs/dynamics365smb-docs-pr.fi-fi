---
title: Puitekokoonpanotilauksien luominen | Microsoft Docs
description: Luo mukautetuille kokoonpanonimikkeille puitemyyntitilauksia, ennen kuin teet säännöllisesti todelliset myyntitilaukset puitetilauksen sopimuksen mukaisesti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 84232aadd133527d06ff0bf2b65490d5dfe8d651
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917699"
---
# <a name="create-blanket-assembly-orders"></a>Puitekokoonpanotilausten luominen
Voit mukauttaa kokoonpanonimikettä asiakkaan pyynnöstä myyntiprosessin kokoonpanon hallinnan avulla. Lisätietoja on kohdassa [Kokoonpano tilausta varten -nimikkeiden myyminen](assembly-how-to-sell-items-assembled-to-order.md).  

 Samalla tavalla kuin minkä tahansa nimiketyypin kohdalla, voit myös luoda puitemyyntitilauksia mukautetun kokoonpanon osille ennen kuin teet säännöllisesti todelliset myyntitilaukset puitetilauksen sopimuksen mukaisesti. Tähän toimenpiteeseen liittyy useita ylimääräisiä vaiheita tavallisen puitemyyntitilauksen luomiseen verrattuna, ja siinä käytetään linkitetyn kokoonpanotilauksen versiota, joka on puitekokoonpanotilaus.

> [!NOTE]  
>  Kuten kaikissa puitetilauksissa, kokoonpanon joukkotilausten määrät ovat vain ennusteita, eikä niitä käytetä, ennen kuin ne muunnetaan todellisiksi kokoonpanotilauksiksi. Tämän vuoksi tilaustoiminnot, kuten saatavuus, laskenta, varaus ja nimikeseuranta, eivät ole aktiivisia kokoonpanon puitetilauksissa.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Luo puitekokokoonpanotilaus kokoonpano\-tilausta\-varten -nimikkeelle  
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Puitemyyntitilaukset** ja valitse sitten liittyvä linkki.  
2. Luo uusi puitemyyntitilaus yhdellä kokoonpanonimikkeen rivillä. Lisätietoja on kohdassa [Puitemyyntitilausten luominen](sales-how-to-create-blanket-sales-orders.md).  
3. Kirjoita koko määrä puitekokoonpanotilausrivin **Kokoonpantava määrä tilausta varten** -kenttään.

    > [!NOTE]  
    >  Sinun ei pitäisi luoda puitetilaussopimusta osittaiselle määrälle. Tämän vuoksi täytyy syöttää sama määrä, joka on syötetty myynnin puitetilausrivin **Määrä**-kenttään.  

4. Valitse **Kokoonpano tilausta varten** -toiminto ja valitse sitten **Kokoonpano tilausta varten -rivit** -toiminto. Vaihtoehtoisesti voit valita rivin **Kokoonpantava määrä tilausta varten** -kentän.  
5. Tarkastele tai muokkaa **Kokoonpano tilausta varten -rivit** -sivulla asiakkaan kanssa tekemäsi puitetilaussopimuksen mukaisia kokoonpanotilauksen rivejä. Jos haluat tarkastella tietoja, avaa koko puitekokoonpanotilaus valitsemalla **Näytä asiakirja** -toiminto. Useimpien kenttien sisältöä ei voi muuttaa etkä voi kirjata.  
6. Kun olet muokannut kokoonpanotilauksen rivejä puitetilauksen sopimuksen mukaisesti, sulje **Kokoonpano tilausta varten -rivit** -sivu ja palaa **Puitemyyntitilaus** -sivulle.  
7. Kun asiakas pyytää puitemyyntitilaukseen perustuvan myyntitilauksen luomista, luo myyntitilaus sovitulle kokoonpanon nimikkeelle tai nimikkeille. Lisätietoja on kohdassa [Puitemyyntitilausten luominen](sales-how-to-create-blanket-sales-orders.md).

Linkitetty puitekokoonpanotilaus ja kaikki muokkaukset on linkitetty uuteen myyntitilaukseen kokoonpanon tai myynnin valmistelua varten.  

## <a name="see-also"></a>Katso myös
[Puitemyyntitilausten luominen](sales-how-to-create-blanket-sales-orders.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)  
[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
