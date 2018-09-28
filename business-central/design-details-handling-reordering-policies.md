---
title: "Rakennetiedot – uusintatilauskäytäntöjen käsittely | Microsoft Docs"
description: "Yleiskatsaus tehtävistä, joilla määritetään tuotantosuunnittelun uusintatilauskäytäntö."
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
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b273dedd269d8b86ba4fa7a9d9540c44b701a97e
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-handling-reordering-policies"></a>Rakennetiedot: uusintatilauskäytäntöjen käsittely
Uusintatilausväli on määritettävä, jotta nimike voi osallistua tarjonnan suunnitteluun. Seuraavat neljä jälkitilausohjetta on olemassa:  
  
* Kiinteä uusintatil. määrä  
* Enimmäismäärä  
* Tilaus  
* Erä-erästä  
  
Kiinteä uusintatil. määrä- ja enimmäismäärä-käytännöt liittyvät varaston suunnittelu. Vaikka varaston suunnittelu on teknisesti helpompaa kuin täsmäytys, näiden käytäntöjen tulee toimia yhdessä tarjonnan vaiheittaiseksi täsmäyttämiseksi ja tilausten seuraamiseksi. Jotta näiden kahden välisen integroinnin valvonta ja Käytetyn suunnittelulogiikan näkyvyyden määritys onnistuu, uudelleentilausmenetelmiä käsitellään tiukkojen periaatteiden avulla.  
  
## <a name="in-this-section"></a>Tämän osan sisältö  
[Rakennetiedot: uusintatilauspisteen rooli](design-details-the-role-of-the-reorder-point.md)  
[Rakennetiedot: arvioidun varastotason ja uusintatilauspisteen valvonta](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[Rakennetiedot: aikavälin rooli](design-details-the-role-of-the-time-bucket.md)  
[Rakennetiedot: sallitun ylityksen alapuolella pysytteleminen](design-details-staying-under-the-overflow-level.md)  
[Rakennetiedot: suunnitellun negatiivisen varaston käsittely](design-details-handling-projected-negative-inventory.md)  
[Rakennetiedot: uusintatilauskäytännöt](design-details-reordering-policies.md)  
  
## <a name="see-also"></a>Katso myös  
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)   
[Rakennetiedot: suunnittelun kohdistustaulukko](design-details-planning-assignment-table.md)   
[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)
