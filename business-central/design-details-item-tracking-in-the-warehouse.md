---
title: Rakennetiedot – nimikkeen seuranta varastossa | Microsoft Docs
description: Sarjanumeron ja eränumeron käsittely on ensisijaisesti varaston tehtävä ja siksi kaikilla saapuvilla ja lähtevillä varastodokumenteilla on perustoimintatarkoitus nimikkeiden seurantanumeroiden määrittämiselle ja valinnalle. Koska varausjärjestelmä perustuu nimiketapahtumiin, sellaisia varastoinnin toimenpideasiakirjoja ei tueta täysin, jotka rekisteröivät vain fyysisen varastoinnin tapahtumia.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e369517d05cd4a9e9c0586f6d7407f0351966def
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917399"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a>Rakennetiedot: nimikkeen seuranta f. varastossa
Sarjanumeron ja eränumeron käsittely on ensisijaisesti varaston tehtävä ja siksi kaikilla saapuvilla ja lähtevillä varastodokumenteilla on perustoimintatarkoitus nimikkeiden seurantanumeroiden määrittämiselle ja valinnalle.  

Koska varausjärjestelmä perustuu nimiketapahtumiin, sellaisia varastoinnin toimenpideasiakirjoja ei tueta täysin, jotka rekisteröivät vain fyysisen varastoinnin tapahtumia. Koska varaukset ja nimikkeen seurantanumerot voidaan käsitellä vain sijaintitasolla, ei lokero- ja vyöhyketasolla, **Nimikkeen seurantarivi**-sivua ei voida avata varastotoiminnon asiakirjoista. Sama koskee **Varaus**-sivua.  

Kun sarja- tai eränumero on lisätty nimikkeeseen varastosijainnissa, se voidaan vapaasti siirtää ja luokitella varastossa uudelleen käyttämällä riippumatonta nimikkeen seurantarakennetta, joka ei ole riippuvainen varausjärjestelmästä. **Sarjanro** ja **eränro** -kenttiin pääsee suoraan varaston asiakirjariveiltä. Kun sarja- tai eränumero myöhemmin ottaa osaa lähtevään kirjaukseen, se synkronoidaan varausjärjestelmän kanssa tavallisen varastopaikan muutoksen osana. Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Integrointi varaston kanssa](design-details-integration-with-inventory.md).  

Varausjärjestelmä ottaa saatavuuden laskennassa kuitenkin huomioon fyysisen varastoinnin toimenpiteet. Esimerkiksi poimintoihin varattuja tai poimituiksi rekisteröityjä nimikkeitä ei voi varata. Lisätietoja on kohdassa [Rakennetiedot: varastosaatavuus](design-details-availability-in-the-warehouse.md).

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: nimikkeen seuranta](design-details-item-tracking.md)  
[Rakennetiedot: integrointi varaston kanssa](design-details-integration-with-inventory.md)  
[Rakennetiedot: varastosaatavuus](design-details-availability-in-the-warehouse.md)  
[Rakennetiedot: nimikkeen seurannan rakenne](design-details-item-tracking-design.md)
