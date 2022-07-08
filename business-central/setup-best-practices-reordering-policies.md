---
title: 'Parhaiden käytäntöjen määrittäminen: Uusintatilaustavat | Microsoft Docs'
description: Uusintatilaustapa-kenttä nimikekorteissa antaa neljä eri suunnittelumetodia, jotka määrittävät, kuinka yksittäiset suunnitteluparametrit käyttäytyvät.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b71ea56c67df7689a268e633880d16fac616027b
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077526"
---
# <a name="setup-best-practices-reordering-policies"></a>Asetukset - parhaat käytännöt: uusintatilaustavat

**Uusintatilaustapa**-kenttä nimikekorteissa antaa neljä eri suunnittelumetodia, jotka määrittävät, kuinka yksittäiset suunnitteluparametrit käyttäytyvät.  

Yksi hyvä perusta uusintatilaustavan valitsemiseen on nimikkeen ABC-luokittelu. Kun käytät ABC-luokittelua varaston valvonnan ja tarjonnan suunnitteluun, nimikkeitä hallitaan kolmen eri luokan mukaan riippuen niiden arvosta ja tilavuudesta suhteessa kokonaismäärään. Seuraavassa taulukossa näkyy kolmen luokan arvo-aseman jako.

|Luokka|Prosenttiosuus kokonaisvarastotilavuudesta|Prosenttiosuus kokonaisvarastoarvosta|
|-----|-----------------------------|----------------------------|
|A|10-20|50-70|
|B|20|20|
|N|60-70|10-30|

ABC-luokittelun mukaisesti vaivaa ja rahaa voidaan säästää soveltamalla matalampiarvoisiin nimikkeisiin alemmantasoista valvontaa kuin korkea-arvoisiin nimikkeisiin. Seuraavassa kuvassa näytetään, mikä [!INCLUDE[prod_short](includes/prod_short.md)]:n sopivin kullekin A,- B,- ja C-kohteille.

![ABC-luokittelu.](media/abc_classification.png "abc_classification")

Seuraava taulukko sisältää parhaat käytännöt neljästä tavasta valitsemiseen.  

|Asetusvaihtoehto|Parhaat käytännöt|Kommentti|  
|------------------|-------------------|-------------|  
|**Tilaus**|Käytä A-nimikkeisiin.<br /><br /> Käytä tilausohjattuihin nimikkeisiin.<br /><br /> Käytä tuotannon ylimmän tason nimikkeissä ja kalliissa komponenteissa ja osakokoonpanoissa.<br /><br /> Käytä nimikkeisiin, jotka on ostettu suoratoimituksina ja serikoistilauksina.<br /><br /> Älä käytä, jos et hyväksy automaattista varausta.|Nimikkeet, kuten nahkasohvat huonekalumyymälässä, ovat arvokkaita nimikkeitä, joiden tilausmäärä on vähäinen ja epäsäännöllinen, joten inventaariota ei hyväksytä tai vaaditut attribuutit vaihtelevat. Paras uusintatilaustapa on siis sellainen, joka suunnitellaan erityisesti kysynnän ehdoilla.|  
|**Erä-erästä**|Käytä B-nimikkeisiin.<br /><br /> Käytä tuotannon komponenteille, jotka esiintyvät useissa tuoterakenteissa. Tämä varmistaa, että saman toimittajan ostotilaukset yhdistetään, jolloin voidaan neuvotella paremmat hinnat.<br /><br /> Käytä, jos et ole varma minkä uusintatilaustavan valitset.|B-nimikkeillä kuten ruokailutuoleilla, on säännöllinen ja melko suuri tilauksen nopeus, mutta myös korkeat ylläpitokustannukset. Paras uusintatilaustapa B-nimikkeille on näin ollen se, joka on edullisin silloin, kun kysyntä otetaan huomioon uusintatilausvälissä.<br /><br /> 80 prosenttia kohteista voi käyttää tätä käytäntöä.<br /><br /> Voidaan käyttää onnistuneesti ilman suunnittelun parametreja.|  
|**Kiinteä uusintatil. määrä**|Käytä C-nimikkeisiin.<br /><br /> Yhdistä uusintatilauspisteparametrien kanssa.<br /><br /> Käytä tuotannon alimman tason komponenteissa.<br /><br /> Älä käytä, jos nimike on usein varattu.|C-nimikkeet, kuten teekupit, ovat vähäsen arvon nimikkeitä, jolla on suuri ja säännöllinen tilausnopeus. Paras uusintatilaustapa C-nimikkeille on siis sellainen, joka varmistaa jatkuvan saatavuuden pysymällä aina uusintatilauspisteen yläpuolella.<br /><br /> Jos käyttäjä varaa määrää kaukaista kysyntää varten, suunnittelun perusta häiriintyy. Vaikka oletettu varastotaso on hyväksyttävä suhteessa uusintatilauspisteeseen, määrät eivät ehkä ole käytettävissä varauksen vuoksi.|  
|**Enimmäismäärä**|Käytä C-nimikkeisiin, joissa on korkeat ylläpitokustannukset tai tallennusrajoitukset.<br /><br /> Yhdistä yksi tai useampi tilauksen valitsin (minimi/maksimi tilausmäärä tai monitilaus).|C-nimikkeet, kuten teekupit, ovat vähäsen arvon nimikkeitä, jolla on suuri ja säännöllinen tilausnopeus. Paras uusintatilaustapa C-nimikkeille on siis sellainen, joka varmistaa jatkuvan saatavuuden pysymällä aina uusintatilauspisteen yläpuolella, mutta varaston enimmäiskapasiteetin alapuolella.<br /><br /> Kun muutat ehdotettua järjestyä, haluat ehkä laskea tilausmäärää määritettyyn enimmäistilausmäärään tai nostaa määritettyyn minimitilausmäärään tai pyöristää vastaamaan määritettyä tilauskerrannaista. **Huomautus:**  Jos tätä käytetään uusintatilauspisteen kanssa, varaston määrä pysyy uusintatilauspisteen määrän ja enimmäismäärän välillä.|  

## <a name="see-related-training-at-microsoft-learn"></a>Lisätietoja aiheeseen liittyvistä kursseista on [Microsoft Learnissa](/learn/paths/replenish-items-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös

 [Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
 [Rakennetiedot: uusintatilauskäytäntöjen käsittely](design-details-handling-reordering-policies.md)  
 [Monimutkaisten sovellusalueiden määrittäminen parhaiden käytäntöjen avulla](set-up-complex-application-areas-using-best-practices.md)  
 [Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]