---
title: FEFO-poiminnan ottaminen käyttöön | Microsoft Docs
description: FEFO (First Expired First Out) on lajittelumenetelmä, joka varmistaa sen, että vanhimmat ja aikaisimman vanhenemispäivämäärän omaavat nimikkeet poimitaan ensin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1c7896988545d6f1b8269ead90dff7350bc6f320
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755822"
---
# <a name="enable-picking-items-by-fefo"></a>FEFO-poiminnan ottaminen käyttöön
FEFO (First Expired First Out) on lajittelumenetelmä, joka varmistaa sen, että vanhimmat ja aikaisimman vanhenemispäivämäärän omaavat nimikkeet poimitaan ensin.  

 Tämä toiminto toimii vain, kun seuraavat ehdot täyttyvät:  

-   Nimikkeellä on oltava sarjanumero tai eränumero.  
-   Nimikkeen seurantakoodiasetuksissa on valittava kenttä **Sarjanumerovarastoseuranta** -kenttä tai **Eränumerovarastoseuranta**.  
-   Nimike on kirjattu varastoon vanhentumispäivämäärän kera.  
-   Sijaintikortissa on valittava valintaruutu **Vaadi poiminta**.  
-   Sijaintikortissa on valittava valintaruutu **FEFO-poiminta**.  
-   Sijaintikortissa on valittava **Var.paikka pakollinen** -valintaruutu.  

 Kun kaikki ehdot täyttyvät, poimittavat sarja/erä-numeroidut nimikkeet lajitellaan vanhimmat ensin kaikissa poiminnoissa ja siirroissa, lukuun ottamatta nimikkeitä, jotka käyttävät sarjanrokohtaista tai eränumerokohtaista seurantaa.  

> [!NOTE]  
> Jos jotkin sarja-/eränumeroidut nimikkeet käyttävät erityistä seurantaa, ne otetaan ensin huomioon. Näiden jälkeen jäljellä olevat määrittämättömät sarja-/eränumerot luetellaan FEFO:n mukaan.
<br /><br />
Jos kahdella erä-/sarjanumeroidulla nimikkeellä on sama vanhentumispäivämäärä, sovellus valitsee nimikkeen, jolla on pienempi sarja- tai eränumero.
<br /><br />
Kun sarja- tai eränumeroituja nimikkeitä poimitaan ohjattua hyllytystä ja poimintaa varten määritetyissä sijainneissa, FEFO poimii vain tyyppiä *Poiminta* olevien varastopaikkojen määrät.  
<br /><br />
Ota varastosiirrot käyttöön FEFO:n mukaan joko **Varaston siirto**- tai **Siirtotyökirja**-sivulla ja jätä **Varastopaikasta**-kenttä tyhjäksi.  
<br /><br />
Jos **Tiukka vanhentumisen kirj.** -kenttä on valittuna, poimintaan sisällytetään vain ne kohteet, jotka eivät ole vanhentuneet. Tämä pätee myös silloin, kun et käytä poimintaa FEFO-periaatteen mukaan.

## <a name="see-also"></a>Katso myös  
[Nimikkeiden poiminta](warehouse-pick-items.md)   
[Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)
