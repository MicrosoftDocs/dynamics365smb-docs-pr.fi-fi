---
title: Suunnittelu sijainteja käyttämällä tai ilman niitä
description: Tässä aiheessa on tietoja tuotannosta ja valmistuksesta Business Centralissa, mukaan lukien toimitusten suunnittelu.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/16/2021
ms.author: edupont
ms.openlocfilehash: 97ba3a62954ae2d38106f0dc7aa4f1080e483ef5
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8517841"
---
# <a name="planning-with-or-without-locations"></a>Suunnittelu sijainteja käyttämällä tai ilman niitä
Käytetään sijaintikoodeja kysyntäriveillä suunnittelussa tai ei, suunnittelujärjestelmä toimii suoraviivaisesti seuraavien asioiden toteutuessa:  

-   Kysyntäriveillä on aina sijaintikoodi, ja järjestelmä käyttää varastointiyksiköiden kaikkia ominaisuuksia, myös asiaankuuluvia sijaintiasetuksia.  
-   Kysyntäriveillä ei missään tilanteessa käytetä sijaintikoodeja, eikä järjestelmä käytä varastointiyksiköitä eikä sijaintiasetuksia (ks. viimein esimerkkitilanne jäljempänä).  

Jos kysyntäriveillä toisinaan on sijaintikoodeja ja toisinaan taas ei, suunnittelujärjestelmä noudattaa asetuksien mukaan tiettyjä sääntöjä.  

> [!TIP]
> Jos suunnittelet usein kysyntää eri sijainneissa, Varastointiyksiköt-ominaisuutta kannattaa käyttää.

## <a name="demand-at-location"></a>Kysyntä sijainnissa  

Kun suunnittelujärjestelmä havaitsee kysyntää tietyssä sijainnissa (rivi, jossa on sijaintikoodi), järjestelmä ryhtyy toimimaan. Toimintamalli määräytyy kolmen keskeisen asetusarvon mukaan.  

Järjestelmä tarkistaa kyseiset kolme arvoa järjestyksessä suunnitteluajon aikana ja toteuttaa suunnitelmat niiden mukaan:  

1. Onko **Varastoasetukset**-sivun **Sijainti pakollinen** -kentässä rasti?  

    Toimet, kun vastaus on Kyllä:  

2. Onko nimikkeellä varastointiyksikkö?  

    Toimet, kun vastaus on Kyllä:  

    Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.  

    Toimet, kun vastaus on Ei:  

3. Sisältääkö **Tuotannon asetukset** -sivun **Komponentit sijainnissa** -kenttä vaadittavan sijaintikoodin?  

    Toimet, kun vastaus on Kyllä:  

    Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.  

    Toimet, kun vastaus on Ei:  

    Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa =  *Erä-erästä*, Sisällytä varasto =  *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä. ( *Tilaus*-uusintatilaustapaa käyttävät nimikkeet käyttävät yhä  *Tilaus*-uusintatilaustapaa sekä muita asetuksia.)  

> [!NOTE]  
> Tämä "minimaalinen vaihtoehto" kattaa vain tarkan kysynnän. Kaikki määritetyt suunnitteluparametrit ohitetaan.  

Tutustu jäljempänä oleviin esimerkkitilanteisiin.  

> [!TIP]
> **Varastoasetukset**-sivun **Sijainnit pakolliset** -kenttä ja Tuotannon asetukset -sivun **Komponentit sijainnissa** -kenttä ovat erittäin tärkeitä, kun hallitaan sitä, miten suunnittelujärjestelmä käsittelee kysyntärivejä sijaintikoodeilla tai ilman sijaintikoodeja.
>
> Tuotantokysynnän ja ostonimikkeiden yhteydessä (kun suunnittelujärjestelmää käytetään ainoastaan ostosuunnitteluun, ei tuotannon suunnitteluun) [!INCLUDE [prod_short](includes/prod_short.md)] käyttää tuotantotilauksessa ilmaistua sijaintia myös komponenteille. Täyttämällä tämän kentän voit kuitenkin ohjata komponentit uuteen sijaintiin.
>
> Voit määrittää myös tämän tietylle varastointiyksikölle valitsemalla varastointiyksikön kortin **Komponentit sijainnissa** -kentässä eri koodin. Huomaa kuitenkin, että tämä on harvoin järkevää, koska suunnittelun logiikka saattaa vääristyä varastointiyksikköä suunniteltaessa.

Toinen tärkeä kenttä on **Nimike**-kortin **Tilauksen enimmäismäärä** -kenttä. Se määrittää nimiketilausehdotuksen sallitun enimmäismäärän, ja sitä käytetään, jos nimike toimitetaan kiinteässä kuljetusyksikössä, kuten kontissa, jota haluat käyttää täysimääräisesti. Siinä vaiheessa kun ohjelma on huomannut täydennystarpeen ja muuttanut eräkokoa vastaamaan määritettyä uusintatilaustapaa, jos tarpeen se vähentää määrää kattamaan enimmäistilausmäärän jonka olet määrittänyt nimikkeelle. Jos on olemassa lisätarpeita niin ohjelma laskee uusia tilauksia niiden kattamiseksi. Tätä kenttää on tarkoitus käyttää varasto-ohjatun tuotantotavan kanssa.  

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

Jos siis suunnittelet usein kysyntää sijainneissa, Varastointiyksiköt-ominaisuutta kannattaa käyttää.  

## <a name="see-also"></a>Katso myös

[Suunnittelu](production-planning.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastointiyksiköiden määrittäminen](inventory-how-to-set-up-stockkeeping-units.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)  
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]