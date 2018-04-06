---
title: "FEFO-poiminnan ottaminen käyttöön | Microsoft Docs"
description: "FEFO (First Expired First Out) on lajittelumenetelmä, joka varmistaa sen, että vanhimmat ja aikaisimman vanhenemispäivämäärän omaavat nimikkeet poimitaan ensin."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e4ee3dc56de6c4ca6b6229c0b436c9407d73534a
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="enable-picking-items-by-fefo"></a>FEFO-poiminnan ottaminen käyttöön
FEFO (First Expired First Out) on lajittelumenetelmä, joka varmistaa sen, että vanhimmat ja aikaisimman vanhenemispäivämäärän omaavat nimikkeet poimitaan ensin.  

 Tämä toiminto toimii vain, kun seuraavat ehdot täyttyvät:  

-   Nimikkeellä on oltava sarjanumero tai eränumero.  
-   Nimikkeen seurantakoodiasetuksissa on valittava kenttä **Sarjanumerokohtainen varastoseuranta** field or the **Eränumerokohtainen varastoseuranta**.  
-   Nimike on kirjattu varastoon vanhentumispäivämäärän kera.  
-   Sijaintikortissa on valittava valintaruutu **Vaadi poiminta**.  
-   Sijaintikortissa on valittava valintaruutu **FEFO-poiminta**.  
-   Sijaintikortissa on valittava **Var.paikka pakollinen** -valintaruutu.  

 Kun kaikki ehdot täyttyvät, poimittavat sarja/erä-numeroidut nimikkeet lajitellaan vanhimmat ensin kaikissa poiminnoissa ja siirroissa, lukuun ottamatta nimikkeitä, jotka käyttävät sarjanrokohtaista tai eränumerokohtaista seurantaa.  

> [!NOTE]  
>  Jos jotkin sarja-/eränumeroidut nimikkeet käyttävät erityistä seurantaa, ne otetaan ensin huomioon. Näiden jälkeen jäljellä olevat määrittämättömät sarja-/eränumerot luetellaan FEFO:n mukaan.  

 Jos kahdella erä-/sarjanumeroidulla nimikkeellä on sama vanhentumispäivämäärä, ohjelma valitsee nimikkeen, jolla on pienempi sarja- tai eränumero. Jos sarja- tai eränumerot ovat samoja, ohjelma valitsee ensimmäisenä rekisteröidyn nimikkeen.  

> [!NOTE]  
>  -   Kun sarja- tai eränumeroituja nimikkeitä poimitaan ohjattua hyllytystä ja poimintaa varten määritetyissä sijainneissa, FEFO poimii vain tyyppiä *Poiminta* olevien varastopaikkojen määrät.  
> -   Ota varastosiirrot käyttöön FEFO:n mukaan joko **Varaston siirto** -ikkunassa tai **Siirtotyökirja** -ikkunassa ja jätä **Varastopaikasta** -kenttä tyhjäksi.  
> -   Jos **Tiukka vanhentumisen kirj.** -kenttä on valittuna, poimintaan sisällytetään vain ne kohteet, jotka eivät ole vanhentuneet. Tämä pätee myös silloin, kun et käytä poimintaa FEFO-periaatteen mukaan.  

## <a name="see-also"></a>Katso myös  
[Nimikkeiden poiminta](warehouse-pick-items.md)   
[Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Rakennetiedot: Fyysisen varaston hallinta](design-details-warehouse-management.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

