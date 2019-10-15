---
title: Tietoja suunnittelutoiminnoista | Microsoft Docs
description: Suunnittelujärjestelmä ottaa kaikki kysyntä- ja tarjontatiedot huomioon, nettouttaa tulokset ja luo ehdotuksia, joita noudattamalla tarjonta ja kysyntä voidaan saattaa tasapainoon.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 27a2a105cbb6a8a449de44c564dc448ec6136d61
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313466"
---
# <a name="about-planning-functionality"></a>Tietoja toimintojen suunnittelusta
Suunnittelujärjestelmä ottaa kaikki kysyntä- ja tarjontatiedot huomioon, nettouttaa tulokset ja luo ehdotuksia, joita noudattamalla tarjonta ja kysyntä voidaan saattaa tasapainoon.  

Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Toimitusten suunnittelu](design-details-supply-planning.md)  

> [!NOTE]  
> Saat lisätietoja kaikkien tässä ohjeaiheessa mainittujen kenttien toiminnoista lukemalla työkaluvihjeen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Kysyntä ja tarjonta  
Suunnittelu koostuu kahdesta osasta, jotka ovat kysyntä ja tarjonta. Ne täytyy pitää tasapainossa, jotta kysyntään voidaan varmasti vastata taloudellisesti ja ajallaan.  

- Kysyntä on yleinen termi, jota käytetään kaikenlaista bruttotarpeesta, esimerkiksi myyntitilauksesta, huoltotilauksesta, kokoonpano- tai tuotantotilausten osatarpeesta, lähtevästä siirrosta, puitetilauksesta tai ennusteesta. Näiden lisäksi sovellus sallii myös tiettyjen muiden teknisten kysyntätyyppien käyttämisen. Tällaisia tarpeita ovat esimerkiksi negatiivinen tuotanto- tai ostotilaus, negatiivinen varasto ja ostopalautustilaus.  
- Tarjonta on yleiskäsite mille tahansa täydennykselle, esimerkiksi varastosaldolle, ostotilauksille, kokoonpanotilauksille, tuotantotilauksille tai saapuvalle siirrolle. Vastaavalla tavalla voi olla negatiivinen myynti tai huoltotilaus, negatiivinen osatarve tai myyntipalautus – jotka jollakin tavoin edustavat myös tarjontaa.  

Suunnittelujärjestelmän toinen tavoite on varmistaa, että varasto ei kasva tarpeettoman suureksi. Jos kysyntä vähenee, suunnittelujärjestelmä ehdottaa tehtyjen täydennystilausten lykkäämistä, pienentämistä tai peruuttamista.  

## <a name="planning-calculation"></a>Suunnittelulaskenta  
Suunnittelujärjestelmän perustana ovat arvioitu ja todellinen asiakaskysyntä sekä varaston uusintatilausten parametrit. Kun suunnitelma lasketaan, sovellus ehdottaa tiettyjä toimenpiteitä (toimenpideviestit), jotka liittyvät alihankkijatäydennyksiin, varastojen välisiin siirtoihin tai tuotantoon. Jos täydennystilauksia on jo tehty, ehdotettuja toimenpiteitä voivat olla tilausten lisääminen tai vauhdittaminen muuttuneen kysynnän mukaisiksi.  

Suunnitteluohjelma perustuu brutto-netto-laskutoimituksiin. Suunnitellut tilausvapautukset perustuvat nettovaatimuksiin, ja ne ajoitetaan reititystietojen (valmistettujen nimikkeiden) perusteella tai nimikkeen kortin toimitusajan (ostonimikkeiden) perusteella. Suunniteltujen tilausvapautusten määrät perustuvat suunnittelulaskentaan, ja tilanvapautuksiin vaikuttavat yksittäisissä nimikkeiden korteissa määritettävät parametrit.  

## <a name="planning-with-manual-transfer-orders"></a>Suunnittelu manuaalisia siirtotilauksia käyttäen.
Kuten Var. yks. -kortin **Täydennysjärjestelmä**-kentässä näkyy, suunnittelujärjestelmän voi määrittää luomaan siirtotilauksia, jotka tasapainottavat eri sijaintien kysyntää ja tarjontaa.  

Automaattisten siirtotilausten lisäksi voit tarvittaessa siirtää varastoeriä sijainnista toiseen myös kysynnästä riippumatta. Luo tällöin siirtotilaus siirrettävällä määrälle manuaalisesti. Voit estää suunnittelujärjestelmää puuttumasta manuaaliseen siirtotilaukseen määrittämällä siirtorivien **Suunnittelun joustavuus** -kentän arvoksi Ei mitään.  

Jos sen sijaan haluat, että suunnittelujärjestelmä muuttaa siirtotilauksen määriä ja päivämääriä kysynnän mukaan, määritä **Suunnittelun joustavuus** -kentän arvoksi oletusarvo Rajaton.

## <a name="planning-parameters"></a>Suunnittelun parametrit  
Suunnittelun parametreilla ohjataan sitä, milloin, miten ja kuinka paljon täydennyksiä nimikkeen kortin asetusten (eli varastointiyksikön) ja tuotannon asetusten perusteella tehdään.  

Nimikkeen tai varastointiyksikön korteissa on käytettävissä seuraavat suunnitteluparametrit:  

-   Puskuriaika  
-   Puskurimäärä  
-   Uusintatilaustapa  
-   Uusintatilauspiste
-   Enimmäisvarasto  
-   Sallittu ylitys  
-   Aikaväli  
-   Erän koontijakso  
-   Uudelleenajoitusjakso  
-   Uusintatilausmäärä  
-   Toimitusajan varmistus  
-   Varmuusvaraston määrä  
-   Kokoonpanokäytäntö  
-   Tuotantotapa  

Nimikkeen tai varastointiyksikön korteissa on käytettävissä seuraavat tilausmääritteet:  

-   Vähimmäistilausmäärä  
-   Enimmäistilausmäärä  
-   Tilauskerrannainen  

**Tuotannon asetukset** -sivun yleiset suunnitteluasetukset sisältävät seuraavat kohdat:  

-   Dynaaminen alatason koodi  
-   Nykyinen kysyntäennuste  
-   Käytä ennustetta sijainneissa  
-   Oletus toimitusajan varmistus  
-   Tyhjä ylivuototaso  
-   Yhdistetty tuot-ohj/tarvelask.   
-   Komponentit sijainnissa  
-   Oletusvaimentimen jakso  
-   Oletuspuskurimäärä  

Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Suunnittelun parametrit](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Muut tärkeät suunnittelukentät
### <a name="planning-flexibility"></a>Suunnittelun joustavuus
Voit valita useimpien toimitustilausten, kuten tuotantotilausten, riveillä **Suunnittelun juostavuus** -kentässä **Rajoittaminen** tai **Mitään**.

Näin määritetään, ottaako suunnittelujärjestelmä tuotantotilausrivin osoittaman tarjonnan huomioon toimenpideviestejä laskettaessa.
Jos kentässä on valittu **Rajaton**, suunnittelujärjestelmä sisällyttää rivin laskiessaan toimenpideviestejä. Jos kentässä on valittu **Ei mitään**, rivi on pysyvä, eikä sitä voi muuttaa. Suunnittelujärjestelmä ei sisällytä sitä toimenpideviestien laskentaan.

### <a name="warning"></a>Varoitus
**Suunnittelutyökirja**-sivun **Varoitus**-tietokenttä ilmoittaa poikkeuksellista tilannetta varten luodusta suunnittelurivistä tekstillä, josta käyttäjä voi lukea lisätietoja. Varoitustyyppejä on kolme:

- Hätä
- Poikkeus
- Huomautus
- Hätä

Hätä-varoitus tulee näkyviin kahdessa tilanteessa:

- Varasto on negatiivinen suunnittelun aloituspäivämääränä.
- Nykyhetkeä aikaisempia tarjonta- tai kysyntätapahtumia on olemassa.

Jos nimikkeen varasto on negatiivinen suunnittelun aloituspäivämääränä, suunnittelujärjestelmä ehdottaa negatiiviselle määrälle hätätoimitustilausta, joka saapuu suunnittelun aloituspäivämääränä. Varoitustekstissä kerrotaan aloituspäivämäärä ja hätätilauksen määrä.

Jos asiakirjassa on rivejä, joiden eräpäivä on ennen suunnittelun aloituspäivämäärää, rivit yhdistetään yhdeksi hätätoimitustilaukseksi, jotta nimike saapuisi suunnittelun aloituspäivämääränä.

### <a name="exception"></a>Poikkeus
Poikkeus-varoitus näytetään, jos oletettu saatavilla oleva varasto pienenee varmuusvaraston määrää pienemmäksi.

Suunnittelujärjestelmä ehdottaa toimitustilausta, joka täyttää kysynnän eräpäivänä. Varoitustekstissä kerrotaan nimikkeen varmuusvaraston määrä ja päivämäärä, jolloin se vähenee liian pieneksi.

Varmuusvaraston tason alittaminen aiheuttaa poikkeuksen, koska näin ei pitäisi käydä, jos uusintatilauspiste on määritetty oikein.

> [!NOTE]
> Tarjontaa suunnitteluriveillä, joilla on poikkeusvaroituksia, ei yleensä muokata suunnitteluparametrien mukaan. Suunnittelujärjestelmä ehdottaa sen sijaan vain toimitusmäärää, joka kattaa kysyntämäärän täsmällisesti. Voit kuitenkin määrittää suunnittelun noudattamaan tiettyjä suunnittelurivien suunnitteluparametreja, joihin liittyy tiettyjä varoituksia. Lisätietoja on kohdassa Noudata suunnitteluparametreja poikkeusvaroituksille Laske suunn. - Suunn. työk. -ikkunassa.

### <a name="attention"></a>Huomautus
Huomautus-varoitus tulee näkyviin kahdessa tilanteessa:

- Suunnittelun aloituspäivämäärä on varhaisempi kuin käsittelypäivämäärä.
- Suunnittelurivi ehdottaa vapautetun osto- tai tuotantotilauksen muuttamista.

> [!NOTE]
> Suunnitteluriveillä, joilla on varoituksia, ei valita **Hyväksy toimenpideviesti** -kenttää, koska suunnitteluohjelman oletetaan tutkivan tarkemmin näitä rivejä ennen suunnitelman toteutusta.

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)  
[Suunnittelu](production-planning.md)   
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Asetukset - parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
