---
title: Kuinka varaston poimintaluettelo tulostetaan myyntitilauksesta
description: Voit tulostaa varaston poimintaluettelon suoraan myyntitilauksesta, myynnistä, laskusta ja muista lähtevistä myyntiasiakirjoista.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/27/2020
ms.author: sgroespe
ms.openlocfilehash: d5eaad5279445375ec00fdf42dd48bffa5d03645
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324463"
---
# <a name="print-the-picking-list"></a>Tulosta poimintaluettelo
Voit tulostaa varaston poimintaluettelon suoraan myyntitilauksesta, myyntilaskusta tai mistä tahansa muusta asiakirjasta, joka aloittaa tavaroiden lähettämisen.

Tätä raporttia käytetään tyypillisesti yrityksissä, joissa ei ole erillisiä toimintoja varastoinnin hallintaan, joten varastotyöntekijä voi yksinkertaisesti tarkastella tai tulostaa poimintaluetteloa asiaan liittyvällä myyntiasiakirjalla. Yrityksissä, joiden prosessit ovat suurempia tai monimutkaisempia, poiminta suunnitellaan ja suoritetaan erityisen fyysisen varastoinnin asiakirjoissa. Lisätietoja on kohdassa [Nimikkeiden poimiminen](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>Varaston poimintaluettelon tulostaminen myyntitilauksesta  
Seuraava toimenpide perustuu myyntitilaukseen. Vaiheet ovat samanlaiset kaikissa myyntiasiakirjoissa, joita voidaan käyttää nimikkeiden toimituksen käynnistämiseen.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake") -kuvake, anna **Myyntitilaukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa myyntitilaus, johon haluat poimia nimikkeitä.  
3. Valitse **Raportti**-toiminto ja valitse sitten **Poimintaluettelo tilauksen mukaan**-toiminto.  
4. Valitse **Tulosta**-painike, jos haluat tulostaa poimintaluettelon, tai valitse **Esikatselu**, jos haluat katsella raporttia näytössä.

Voit myös tallentaa poimintaluettelon asiakirjana, esimerkiksi lähettääksesi sen jollekulle tai lisätäksesi sen liitteenä myyntitilaukseen. Lue lisätietoja kohteesta [Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta](ui-how-add-link-to-record.md)

> [!NOTE]
> Jos käytit myyntitilauksessa **Pura tuoterakenne** -toimintoa, vain asiaan liittyvän kokoonpanonimikkeen komponentit näkyvät raportissa. Lisätietoja on kohdassa [Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Katso myös  
[Varasto](inventory-manage-inventory.md)  
[Nimikkeiden poiminta](warehouse-pick-items.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)   
