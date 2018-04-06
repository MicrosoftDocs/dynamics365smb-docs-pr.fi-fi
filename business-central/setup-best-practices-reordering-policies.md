---
title: "Parhaiden käytäntöjen määrittäminen: Uusintatilaustavat | Microsoft Docs"
description: "**Uusintatilaustapa**-kenttä nimikekorteissa antaa neljä eri suunnittelumetodia, jotka määrittävät, kuinka yksittäiset suunnitteluparametrit käyttäytyvät."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cb0658a768276835fba44ab1e88e6fac05df5397
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-reordering-policies"></a>Asetukset - parhaat käytännöt: uusintatilaustavat
**Uusintatilaustapa**-kenttä nimikekorteissa antaa neljä eri suunnittelumetodia, jotka määrittävät, kuinka yksittäiset suunnitteluparametrit käyttäytyvät.  

Yksi hyvä perusta uusintatilaustavan valitsemiseen on nimikkeen ABC-luokittelu. Kun käytät ABC-luokittelua varaston valvonnan ja tarjonnan suunnitteluun, nimikkeitä hallitaan kolmen eri luokan mukaan riippuen niiden arvosta ja tilavuudesta suhteessa kokonaismäärään. Seuraavassa taulukossa näkyy kolmen luokan arvo-aseman jako.

|Luokka|Prosenttiosuus kokonaisvarastotilavuudesta|Prosenttiosuus kokonaisvarastoarvosta|
|-----|-----------------------------|----------------------------|
|A|10-20|50-70|
|B|20|20|
|N|60-70|10-30|

ABC-luokittelun mukaisesti vaivaa ja rahaa voidaan säästää soveltamalla matalampiarvoisiin nimikkeisiin alemmantasoista valvontaa kuin korkea-arvoisiin nimikkeisiin. Seuraavassa kuvassa näytetään, mikä [!INCLUDE[d365fin](includes/d365fin_md.md)]:n sopivin kullekin A,- B,- ja C-kohteille.

![ABC-luokittelu](media/abc_classification.png "abc_classification")

Seuraava taulukko sisältää parhaat käytännöt neljästä tavasta valitsemiseen.  

|Asetusvaihtoehto|Parhaat käytännöt|Kommentti|  
|------------------|-------------------|-------------|  
|**Tilaus**|Käytä A-nimikkeisiin.<br /><br /> Käytä tilausohjattuihin nimikkeisiin.<br /><br /> Käytä tuotannon ylimmän tason nimikkeissä ja kalliissa komponenteissa ja osakokoonpanoissa.<br /><br /> Käytä nimikkeisiin, jotka on ostettu suoratoimituksina ja serikoistilauksina.<br /><br /> Älä käytä, jos et hyväksy automaattista varausta.|Nimikkeet, kuten nahkasohvat huonekalumyymälässä, ovat arvokkaita nimikkeitä, joiden tilausmäärä on vähäinen ja epäsäännöllinen, joten inventaariota ei hyväksytä tai vaaditut attribuutit vaihtelevat. Paras uusintatilaustapa on siis sellainen, joka suunnitellaan erityisesti kysynnän ehdoilla.|  
|**Erä-erästä**|Käytä B-nimikkeisiin.<br /><br /> Käytä tuotannon komponenteille, jotka esiintyvät useissa tuoterakenteissa. Tämä varmistaa, että saman toimittajan ostotilaukset yhdistetään, jolloin voidaan neuvotella paremmat hinnat.<br /><br /> Käytä, jos et ole varma minkä uusintatilaustavan valitset.|B-nimikkeillä kuten ruokailutuoleilla, on säännöllinen ja melko suuri tilauksen nopeus, mutta myös korkeat ylläpitokustannukset. Paras uusintatilaustapa B-nimikkeille on näin ollen se, joka on edullisin silloin, kun kysyntä otetaan huomioon uusintatilausvälissä.<br /><br /> 80 prosenttia kohteista voi käyttää tätä käytäntöä.<br /><br /> Voidaan käyttää onnistuneesti ilman suunnittelun parametreja.|  
|**Kiinteä uusintatil. määrä**|Käytä C-nimikkeisiin.<br /><br /> Yhdistä uusintatilauspisteparametrien kanssa.<br /><br /> Käytä tuotannon alimman tason komponenteissa.<br /><br /> Älä käytä, jos nimike on usein varattu.|C-nimikkeet, kuten teekupit, ovat vähäsen arvon nimikkeitä, jolla on suuri ja säännöllinen tilausnopeus. Paras uusintatilaustapa C-nimikkeille on siis sellainen, joka varmistaa jatkuvan saatavuuden pysymällä aina uusintatilauspisteen yläpuolella.<br /><br /> Jos käyttäjä varaa määrää kaukaista kysyntää varten, suunnittelun perusta häiriintyy. Vaikka oletettu varastotaso on hyväksyttävä suhteessa uusintatilauspisteeseen, määrät eivät ehkä ole käytettävissä varauksen vuoksi.|  
|**Enimmäismäärä**|Käytä C-nimikkeisiin, joissa on korkeat ylläpitokustannukset tai tallennusrajoitukset.<br /><br /> Yhdistä yksi tai useampi tilauksen valitsin (minimi/maksimi tilausmäärä tai monitilaus).|C-nimikkeet, kuten teekupit, ovat vähäsen arvon nimikkeitä, jolla on suuri ja säännöllinen tilausnopeus. Paras uusintatilaustapa C-nimikkeille on siis sellainen, joka varmistaa jatkuvan saatavuuden pysymällä aina uusintatilauspisteen yläpuolella, mutta varaston enimmäiskapasiteetin alapuolella.<br /><br /> Kun muutat ehdotettua järjestyä, haluat ehkä laskea tilausmäärää määritettyyn enimmäistilausmäärään tai nostaa määritettyyn minimitilausmäärään tai pyöristää vastaamaan määritettyä tilauskerrannaista. **Huomautus:**  Jos tätä käytetään uusintatilauspisteen kanssa, varaston määrä pysyy uusintatilauspisteen määrän ja enimmäismäärän välillä.|  

## <a name="see-also"></a>Katso myös  
 [Asetusten parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md)   
 [Rakennetiedot: Uusintatilauskäytännöt](design-details-reordering-policies.md)   
 [Rakennetiedot: tilaus](design-details-order.md)   
 [Rakennetiedot: erä-erästä](design-details-lot-for-lot.md)   
 [Rakennetiedot: Kiinteä uusintatil. määrä](design-details-fixed-reorder-qty.md)   
 [Rakennetiedot: enimmäismäärä](design-details-maximum-qty.md)   
 [Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla](set-up-complex-application-areas-using-best-practices.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

