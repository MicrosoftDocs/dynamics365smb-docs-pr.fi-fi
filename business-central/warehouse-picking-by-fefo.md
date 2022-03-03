---
title: FEFO-poiminnan ottaminen käyttöön | Microsoft Docs
description: FEFO (First Expired First Out) on lajittelumenetelmä, joka varmistaa sen, että vanhimmat ja aikaisimman vanhenemispäivämäärän omaavat nimikkeet poimitaan ensin.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1855391f5bf2c0807ac4ffcd8d42e0ea8122fd87
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141855"
---
# <a name="enable-picking-items-by-fefo"></a>FEFO-poiminnan ottaminen käyttöön
FEFO (First Expired First Out) on lajittelumenetelmä, joka varmistaa sen, että vanhimmat ja aikaisimman vanhenemispäivämäärän omaavat nimikkeet poimitaan ensin.  

 Tämä toiminto toimii vain, kun seuraavat ehdot täyttyvät:  

-   Nimikkeellä on oltava sarjanumero tai eränumero.  
-   Nimikkeen seurantakoodiasetuksissa on valittava kenttä **Sarjanumerovarastoseuranta** -kenttä tai **Eränumerovarastoseuranta**.  
-   Nimike on kirjattu varastoon vanhentumispäivämäärän kera.  
-   **Vaadi poiminta**-, **FEFO-poiminta**- ja **Var.paikka pakollinen** -valitsimien on oltava otettuna käyttöön sijainnissa.  

 Kun kaikki ehdot täyttyvät, poimittavat sarja/erä-numeroidut nimikkeet lajitellaan vanhimmat ensin kaikissa poiminnoissa ja siirroissa, lukuun ottamatta nimikkeitä, jotka käyttävät sarjanrokohtaista tai eränumerokohtaista seurantaa.  

> [!NOTE]  
> Jos jotkin sarja- tai eränumeroidut nimikkeet käyttävät erityistä seurantaa, ne otetaan ensin huomioon. Näiden jälkeen jäljellä olevat määrittämättömät sarja-/eränumerot luetellaan FEFO:n mukaan.
<br /><br />
Jos kahdella erä- tai sarjanumeroidulla nimikkeellä on sama vanhentumispäivämäärä, sovellus valitsee nimikkeen, jolla on pienempi sarja- tai eränumero.
<br /><br />
Kun sarja- tai eränumeroituja nimikkeitä poimitaan ohjattua hyllytystä ja poimintaa varten määritetyissä sijainneissa, FEFO poimii vain tyyppiä *Poiminta* olevien varastopaikkojen määrät.  
<br /><br />
Ota varastosiirrot käyttöön FEFO:n mukaan jättämällä **Varastopaikasta**-kenttä tyhjäksi **Varaston siirto**- tai **Siirtotyökirja**-sivulla.  
<br /><br />
Jos **Tiukka vanhentumisen kirj.** -kenttä on valittu **Nimikk. seurantakoodin kortti** -kohdassa, poimintaan sisällytetään vain nimikkeet, jotka eivät ole vanhentuneet, ja rivit lajitellaan FEFO-periaatteen mukaisesti.

## <a name="see-also"></a>Katso myös  
[Nimikkeiden poiminta](warehouse-pick-items.md)   
[Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]