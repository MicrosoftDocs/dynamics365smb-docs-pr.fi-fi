---
title: Suunnittelu sijainteja käyttämällä tai ilman niitä | Microsoft Docs
description: Kysyntäriveillä tehtävä sijaintikoodeja käyttävä suunnittelu tai ilman niitä tehtävä suunnittelu on toiminto, jonka ymmärtäminen on tärkeää.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b5c5c12dedfe3f35737888017ed02e0f7d464443
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877685"
---
# <a name="planning-with-or-without-locations"></a>Suunnittelu sijainteja käyttämällä tai ilman niitä
Käytetään sijaintikoodeja kysyntäriveillä suunnittelussa tai ei, suunnittelujärjestelmä toimii suoraviivaisesti seuraavien asioiden toteutuessa:  

-   Kysyntäriveillä on aina sijaintikoodi, ja järjestelmä käyttää varastointiyksiköiden kaikkia ominaisuuksia, myös asiaankuuluvia sijaintiasetuksia.  
-   Kysyntäriveillä ei missään tilanteessa käytetä sijaintikoodeja, eikä järjestelmä käytä varastointiyksiköitä eikä sijaintiasetuksia (ks. viimein esimerkkitilanne jäljempänä).  

Jos kysyntäriveillä toisinaan on sijaintikoodeja ja toisinaan taas ei, suunnittelujärjestelmä noudattaa asetuksien mukaan tiettyjä sääntöjä.  

## <a name="demand-at-location"></a>Kysyntä sijainnissa  
Kun suunnittelujärjestelmä havaitsee kysyntää tietyssä sijainnissa (rivi, jossa on sijaintikoodi), järjestelmä ryhtyy toimimaan. Toimintamalli määräytyy kolmen keskeisen asetusarvon mukaan.  

Järjestelmä tarkistaa kyseiset kolme arvoa järjestyksessä suunnitteluajon aikana ja toteuttaa suunnitelmat niiden mukaan:  

1.  Onko **Sijainti pakollinen** -kentässä valintamerkki?  

    Toimet, kun vastaus on Kyllä:  

2.  Onko nimikkeellä varastointiyksikkö?  

    Toimet, kun vastaus on Kyllä:  

    Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.  

    Toimet, kun vastaus on Ei:  

3.  Onko **Komponentit sijainnissa** -kentässä vaadittu sijaintikoodi?  

    Toimet, kun vastaus on Kyllä:  

    Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.  

    Toimet, kun vastaus on Ei:  

    Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä*, Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä. ( *Tilaus*-uusintatilaustapaa käyttävät nimikkeet käyttävät yhä  *Tilaus*-uusintatilaustapaa sekä muita asetuksia.)  

> [!NOTE]  
>  Tämä "minimaalinen vaihtoehto" kattaa vain tarkan kysynnän. Kaikki määritetyt suunnitteluparametrit ohitetaan.  

Tutustu jäljempänä oleviin esimerkkitilanteisiin.  

## <a name="demand-at-blank-location"></a>Kysyntä "tyhjässä sijainnissa"  
Vaikka **Sijainti pakollinen** -valintaruutu olisi valittu, järjestelmä sallii kysyntärivien luonnin ilman sijaintikoodia. Tätä kutsutaan myös *TYHJÄKSI* sijainniksi. Tämä on järjestelmälle poikkeustilanne, koska sijaintien käsittelyä varten on määritetty useita määritysarvoja (esimerkki yllä). Suunnitteluohjelma ei tämän vuoksi luo tällaiselle kysyntäriville suunnitteluriviä. Jos **Sijainti pakollinen** -kenttää ei ole valittu mutta käytössä on sijainnin asetusarvoja, kyseessä on poikkeustilanne. Suunnittelujärjestelmä reagoi siihen tuottamalla minimaalisen vaihtoehdon:   
Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä *Tilaus)*, Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.  

Tutustu jäljempänä oleviin määritystilanteisiin.  

### <a name="setup-1"></a>Asetukset (1):  

-   Sijainti pakollinen = *Kyllä*  
-   Varastointiyksikkö on määritetty kohteeseen  *PUNAINEN*  
-   Komponentit sijainnissa =  *SININEN*  

#### <a name="case-11-demand-is-at--red-location"></a>Tapaus 1.1: Kysyntää *SININEN*-sijainnissa  

Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti (mahdolliset siirrot mukaan lukien).  

#### <a name="case-12-demand-is-at--blue-location"></a>Tapaus 1.2: Kysyntää *SININEN*-sijainnissa  

Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.  

#### <a name="case-13-demand-is-at--green-location"></a>Tapaus 1.3: Kysyntää  *VIHREÄ*-sijainnissa  

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.  

#### <a name="case-14-demand-is-at--blank-location"></a>Tapaus 1.4: Kysyntää  *TYHJÄ* -sijainnissa  

Nimikettä ei suunnitella, koska kysyntäriville ei ole määritetty sijaintia.  

### <a name="setup-2"></a>Asetukset (2):  

-   Sijainti pakollinen = *Kyllä*  
-   Ei varastointiyksikköä  
-   Komponentit sijainnissa =  *SININEN*  

#### <a name="case-21-demand-is-at--red-location"></a>Tapaus 2.1: Kysyntää  *PUNAINEN*-sijainnissa  

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.  

#### <a name="case-22-demand-is-at--blue-location"></a>Tapaus 2.2: Kysyntää *SININEN*-sijainnissa  

Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.  

### <a name="setup-3"></a>Asetukset (3):  

-   Sijainti pakollinen = *Ei*  
-   Ei varastointiyksikköä  
-   Komponentit sijainnissa =  *SININEN*  

#### <a name="case-31-demand-is-at--red-location"></a>Tapaus 3.1: Kysyntää  *PUNAINEN*-sijainnissa  

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.  

#### <a name="case-32-demand-is-at--blue-location"></a>Tapaus 3.2: Kysyntää *SININEN*-sijainnissa  

Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.  

#### <a name="case-33-demand-is-at--blank-location"></a>Tapaus 3.3: Kysyntää  *TYHJÄ* -sijainnissa  

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.  

### <a name="setup-4"></a>Asetukset (4):  

-   Sijainti pakollinen = *Ei*  
-   Ei varastointiyksikköä  
-   Komponentit sijainnissa =  *TYHJÄ*  

#### <a name="case-41-demand-is-at--blue-location"></a>Tapaus 4.1: Kysyntää  *SININEN*-sijainnissa  

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä* ( *Tilaus* on yhä  *Tilaus*), Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.  

#### <a name="case-42-demand-is-at--blank-location"></a>Tapaus 4.2: Kysyntää  *TYHJÄ* -sijainnissa  

Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.  

Kuten viimeinen esimerkkitilanne osoittaa, kaikkien sijainteihin liittyvien asetusarvojen poistaminen käytöstä on ainoa tapa saada oikeita tuloksia, kun kysyntärivillä ei ole sijaintikoodia. Vastaavasti varastointiyksiköiden käyttäminen on ainoa tapa saada vakaita suunnittelutuloksia sijaintien kysyntään liittyen.  

Jos suunnittelet usein kysyntää sijainneissa, Varastointiyksiköt-ominaisuutta kannattaa ehdottomasti käyttää.  

## <a name="see-also"></a>Katso myös
[Suunnittelu](production-planning.md)    
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
