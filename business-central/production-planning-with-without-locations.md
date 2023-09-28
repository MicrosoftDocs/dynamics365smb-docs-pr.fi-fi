---
title: Suunnittelu sijainteja käyttämällä tai ilman niitä
description: 'Tässä aiheessa on tietoja tuotannosta ja valmistuksesta Business Centralissa, mukaan lukien toimitusten suunnittelu.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/15/2022
ms.author: bholtorf
---
# <a name="planning-with-or-without-locations"></a>Suunnittelu sijainteja käyttämällä tai ilman niitä

Ennen kuin alat käyttämään suunnittelumoduulia, kannattaa päättää, haluatko käyttää sijainteja. On olemassa kaksi pääasiallista yksinkertaista tapaa:

* Kysyntäriveillä on aina sijaintikoodi, ja järjestelmä käyttää varastointiyksiköiden kaikkia ominaisuuksia, myös asiaankuuluvia sijaintiasetuksia. Lisätietoja on kohdassa [kysyntä sijainnissa](#demand-at-location).  
* kysyntäriveillä ei ole koskaan sijaintikoodeja, ja järjestelmä käyttää nimikkeen korttia. Katso alla olevaa [Kysyntä "tyhjässä sijainnissa"](#demand-at-blank-location) -skenaariota.

## <a name="demand-at-location"></a>Kysyntä sijainnissa

Kun suunnittelujärjestelmä havaitsee kysyntää tietyssä sijainnissa (rivi, jossa on sijaintikoodi), järjestelmä ryhtyy toimimaan. Toimintamalli määräytyy kahden keskeisen asetusarvon mukaan.  

Järjestelmä tarkistaa kyseiset kaksi arvoa järjestyksessä suunnitteluajon aikana ja toteuttaa suunnitelmat niiden mukaan:  

1. Onko pyydetyn sijainnin nimikkeelle olemassa SKU?  

    Toimet, kun vastaus on Kyllä:  

    Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.  

    Toimet, kun vastaus on Ei:  

2. Sisältääkö **Tuotannon asetukset** -sivun **Komponentit sijainnissa** -kenttä vaadittavan sijaintikoodin?  

    Toimet, kun vastaus on Kyllä:  

    Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.  

    Toimet, kun vastaus on Ei:  

    Nimike suunnitellaan "vähimmäisvaihtoehdon" mukaan, joka kattaa tarkan kysynnän. Suunnitteluparametrit toteutetaan seuraavasti: Uusintatilaustapa = *Erä-erästä*, Sisällytä varasto = *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä. (*Tilaus*-uusintatilaustapaa käyttävät nimikkeet käyttävät yhä *Tilaus*-uusintatilaustapaa sekä muita asetuksia.)

> [!TIP]
> Jos suunnittelet usein kysyntää eri sijainneissa, Varastointiyksiköt-ominaisuutta kannattaa käyttää ja vältät kysyntää tyhjässä sijainnissa. Lisätietoja kohdassa [Varastointiyksiköiden määrittäminen](inventory-how-to-set-up-stockkeeping-units.md)

Tutustu jäljempänä oleviin [esimerkkitilanteisiin](#scenarios).

> [!NOTE]
> **Valmistuksen asetukset** -sivun **Komponentit sijainnissa** -kenttä on erittäin tärkeä sen hallinnassa, miten suunnittelujärjestelmä käsittelee tuotannon kysyntälinjoja.
>
> Mitä tulee tuotantokysyntään, [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelma sijoittaa osajoukot ja komponentit sijaintiin, joka on ilmaistu tuotantotilauksessa. Täyttämällä tämän kentän voit kuitenkin ohjata osajoukot ja komponentit uuteen sijaintiin.
>
> Voit määrittää myös tämän tietylle varastointiyksikölle valitsemalla varastointiyksikön kortin **Komponentit sijainnissa** -kentässä eri koodin. Huomaa kuitenkin, että tämä on harvoin järkevää, koska suunnittelun logiikka saattaa vääristyä varastointiyksikköä suunniteltaessa.

## <a name="demand-at-blank-location"></a>Kysyntä "tyhjässä sijainnissa"

Yleensä, kun suunnittelujärjestelmä havaitsee kysynnän tyhjässä sijainnissa (rivillä, jolla ei ole sijaintikoodia), nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.

**Varastoasetukset**-sivun **Sijainnit pakolliset** -kenttä ja **Tuotannon asetukset** -sivun **Komponentit sijainnissa** -kenttä tai varastointiyksiköt vaikuttavat siihen, miten suunnittelujärjestelmä käsittelee kysyntälinjoja sijaintikoodeilla tai ilman. Jos jokin seuraavista väitteistä on totta, myös tyhjän sijainnin kysyntää pidetään poikkeamana ja suunnittelujärjestelmä reagoi antamalla "minimaalinen vaihtoehto" -vaihtoehdon: Nimike suunnitellaan seuraavien parametrien mukaan: uusintatilaustapa = *erä-erästä* (*tilaus* on edelleen *tilaus*), sisällytä varasto = *Kyllä*, kaikki muut suunnitteluparametrit = tyhjä.

* **Tuotannon asetukset** -sivun **Komponentit sijainnissa** -kentällä on arvo.
* Suunnitellulle nimikkeelle on olemassa varastointiyksikkö.
* **Sijainti pakollinen** -kenttä on valittuna.

## <a name="scenarios"></a>Esimerkkitilanteet

Tutustu jäljempänä oleviin määritystilanteisiin.

### <a name="setup-1"></a>Asetus 1

* Sijainti pakollinen = *Kyllä*  
* Varastointiyksikkö on määritetty kohteeseen *LÄNSI*  
* Komponentit sijainnissa = *ITÄ*  

#### <a name="case-11-demand-is-at-west-location"></a>Tapaus 1.1: Kysyntää *LÄNSI*-sijainnissa

Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti (mahdolliset siirrot mukaan lukien).

#### <a name="case-12-demand-is-at-east-location"></a>Tapaus 1.2: Kysyntää *ITÄ*-sijainnissa

Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.

#### <a name="case-13-demand-is-at-north-location"></a>Tapaus 1.3: Kysyntää *POHJOINEN*-sijainnissa

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = *Erä-erästä* (*Tilaus* on yhä *Tilaus*), Sisällytä varasto = *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.

#### <a name="case-14-demand-is-at-blank-location"></a>Tapaus 1.4: Kysyntää *TYHJÄ*-sijainnissa

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = *Erä-erästä* (*Tilaus* on yhä *Tilaus*), Sisällytä varasto = *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.

### <a name="setup-2"></a>Asetus 2

* Sijainti pakollinen = *Kyllä*  
* Ei varastointiyksikköä  
* Komponentit sijainnissa = *ITÄ*  

#### <a name="case-21-demand-is-at-west-location"></a>Tapaus 2.1: Kysyntää *LÄNSI*-sijainnissa

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = *Erä-erästä* (*Tilaus* on yhä *Tilaus*), Sisällytä varasto = *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.

#### <a name="case-22-demand-is-at-east-location"></a>Tapaus 2.2: Kysyntää *ITÄ*-sijainnissa

Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.  

### <a name="setup-3"></a>Asetus 3

* Sijainti pakollinen = *Ei*  
* Ei varastointiyksikköä  
* Komponentit sijainnissa = *ITÄ*  

#### <a name="case-31-demand-is-at-west-location"></a>Tapaus 3.1: Kysyntää *LÄNSI*-sijainnissa

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = *Erä-erästä* (*Tilaus* on yhä *Tilaus*), Sisällytä varasto = *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.

#### <a name="case-32-demand-is-at-east-location"></a>Tapaus 3.2: Kysyntää *ITÄ*-sijainnissa

Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.  

#### <a name="case-33-demand-is-at-blank-location"></a>Tapaus 3.3: Kysyntää *TYHJÄ*-sijainnissa

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = *Erä-erästä* (*Tilaus* on yhä *Tilaus*), Sisällytä varasto = *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.

### <a name="setup-4"></a>Asetus 4

* Sijainti pakollinen = *Ei*  
* Ei varastointiyksikköä  
* Komponentit sijainnissa = *TYHJÄ*  

#### <a name="case-41-demand-is-at-east-location"></a>Tapaus 4.1: Kysyntää *ITÄ*-sijainnissa

Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = *Erä-erästä* (*Tilaus* on yhä *Tilaus*), Sisällytä varasto = *Kyllä*, kaikki muut suunnitteluparametrit ovat tyhjiä.

#### <a name="case-42-demand-is-at-blank-location"></a>Tapaus 4.2: Kysyntää *TYHJÄ*-sijainnissa

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
