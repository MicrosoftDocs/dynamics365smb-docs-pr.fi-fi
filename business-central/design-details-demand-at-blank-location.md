---
title: Rakennetiedot – kysyntä ja tarjonta | Microsoft Docs
description: Tässä ohjeaiheessa esitellään kysyntä-termi, jota käytetään kaikenlaiseen bruttokysyntään, kuten myyntitilaukseen ja komponenttitarpeeseen tuotantotilauksesta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f808865bd4fc2113dd5c04071f7ba2e8793fe3af
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185562"
---
# <a name="design-details-demand-at-blank-location"></a>Rakennetiedot: kysyntä tyhjä-sijainnissa
Kun käyttäjä luo kysyntätapahtuman, kuten myyntitilausrivin, ohjelma sallii käyttäjän joskus määrittää sijaintikoodin, mutta ei aina. Tällöin käytetään tyhjää sijaintia.

Riippumatta siitä, onko kysynnällä sijaintikoodeja, suunnittelujärjestelmä toimii suoraviivaisesti seuraavien asioiden toteutuessa:

- Kysyntäriveillä on aina sijaintikoodi, ja järjestelmä käyttää varastointiyksiköiden kaikkia ominaisuuksia, myös asiaankuuluvia sijaintiasetuksia.
- Kysyntäriveillä ei missään tilanteessa käytetä sijaintikoodeja, eikä järjestelmä käytä varastointiyksiköitä eikä sijaintiasetuksia (ks. viimeinen tilanne seuraavassa osiossa).

Jos kysyntätapahtumissa toisinaan on sijaintikoodeja ja toisinaan taas ei, suunnittelujärjestelmä noudattaa asetuksien mukaan tiettyjä sääntöjä.

## <a name="demand-at-location"></a>Kysyntä sijainnissa
Kun suunnittelujärjestelmä havaitsee kysyntää tietyssä sijainnissa, se toimii kolmen keskeisen asetusarvon mukaan. Järjestelmä tarkistaa kyseiset kolme arvoa järjestyksessä suunnitteluajon aikana ja toteuttaa suunnitelmat niiden mukaan.

1. Onko **Sijainti pakollinen** -kentässä valintamerkki?

    Toimet, kun vastaus on Kyllä:

2. Onko nimikkeellä varastointiyksikkö?

    Toimet, kun vastaus on Kyllä:

    Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.

    Toimet, kun vastaus on Ei:

3. Onko Komponentit sijainnissa -kentässä vaadittu sijaintikoodi?

  Toimet, kun vastaus on Kyllä:

  Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.

  Toimet, kun vastaus on Ei:

  Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä, Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit = tyhjä, uusintatilaustapaa käyttävät nimikkeet = Tilaus säilyy käyttäen tilausta muiden asetusten kanssa.

> [!NOTE]
> Poikkeuksellisiin suunnitteluasetuksiin, jotka ovat viimeisen reaktion tulosta vaiheessa 3 yllä, viitataan seuraavassa nimellä "minimivaihtoehto". Tämän suunnitteluasetus kattaa vain tarkan kysynnän. Muut suunnitteluparametrit ohitetaan.

Katso tiedot tämän suunnittelulogiikan variaatioista alla olevasta skenaariot-osiosta.

## <a name="demand-at-blank-location"></a>Kysyntä tyhjässä sijainnissa
Vaikka **Sijainti pakollinen** -kenttä on valittu, ohjelma sallii kysyntärivien luonnin ilman sijaintikoodia. Tätä kutsutaan myös tyhjäksi sijainniksi. Tämä on järjestelmälle poikkeustilanne, koska sijaintien käsittelyä varten on määritetty useita määritysarvoja (esimerkki yllä). Suunnitteluohjelma ei tämän vuoksi luo tällaiselle kysyntäriville suunnitteluriviä.

Jos **Sijainti pakollinen** -kenttää ei ole valittu, mutta mikä tahansa sijainnin asetusarvoista on olemassa, se katsotaan myös poikkeamaksi ja suunnittelujärjestelmä reagoi siihen käyttämällä "minimaalinen vaihtoehto"-ominaisuutta: nimike suunnitellaan seuraavien parametrien mukaan: uusintatilaustapa = erä-erästä (tilaus on edelleen tilaus), sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit = tyhjä.

## <a name="scenarios"></a>Esimerkkitilanteet
Seuraavat skenaariot kuvaavat tyhjän paikan kysynnän variaatioita ja kuinka suunnittelujärjestelmä ratkaisee "minimivaihtoehdon".

### <a name="setup-1"></a>Asetukset (1):
Sijainti pakollinen = Kyllä

Varastointiyksikkö on määritetty kohteeseen PUNAINEN

Komponentit sijainnissa = SININEN

#### <a name="case-11-demand-is-at-red-location"></a>Tapaus 1.1: Kysyntä on sijainnissa PUNAINEN
Nimike suunnitellaan Var. yks. -kortin suunnitteluparametrien mukaisesti.

#### <a name="case-12-demand-is-at-blue-location"></a>Tapaus 1.2: Kysyntä on sijainnissa SININEN
Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.

#### <a name="case-13-demand-is-at-green-location"></a>Tapaus 1.3: Kysyntä on sijainnissa VIHREÄ
Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.

#### <a name="case-14-demand-is-at-blank-location"></a>Tapaus 1.4: Kysyntä on sijainnissa TYHJÄ
Nimikettä ei suunnitella, koska kysyntäriville ei ole määritetty sijaintia.

### <a name="setup-2"></a>Asetukset (2):
Sijainti pakollinen = Kyllä

Ei varastointiyksikköä

Komponentit sijainnissa = SININEN

#### <a name="case-21-demand-is-at-red-location"></a>Tapaus 2.1: Kysyntä on sijainnissa PUNAINEN
Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.

#### <a name="case-22-demand-is-at-blue-location"></a>Tapaus 2.2: Kysyntä on sijainnissa SININEN
Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.

### <a name="setup-3"></a>Asetukset (3):
Sijainti pakollinen = Ei

Ei varastointiyksikköä

Komponentit sijainnissa = SININEN

#### <a name="case-31-demand-is-at-red-location"></a>Tapaus 3.1: Kysyntä on sijainnissa PUNAINEN
Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.

#### <a name="case-32-demand-is-at-blue-location"></a>Tapaus 3.2: Kysyntä on sijainnissa SININEN
Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.

#### <a name="case-33-demand-is-at-blank-location"></a>Tapaus 3.3: Kysyntä on sijainnissa TYHJÄ
Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.

### <a name="setup-4"></a>Asetukset (4):
Sijainti pakollinen = Ei

Ei varastointiyksikköä

Komponentit sijainnissa = TYHJÄ

#### <a name="case-41-demand-is-at-blue-location"></a>Tapaus 4.1: Kysyntä on sijainnissa SININEN
Nimikkeen suunnittelu toteutetaan seuraavasti: Uusintatilaustapa = Erä-erästä (Tilaus on yhä Tilaus), Sisällytä varasto = Kyllä, kaikki muut suunnitteluparametrit ovat tyhjiä.

#### <a name="case-42-demand-is-at-blank-location"></a>Tapaus 4.2: Kysyntä on sijainnissa TYHJÄ
Nimike suunnitellaan nimikkeen kortin suunnitteluparametrien mukaisesti.

Kuten edellisessä esimerkkitilanteessa kuvataan, kaikkien sijainteihin liittyvien asetusarvojen poistaminen käytöstä on ainoa tapa saada oikeita tuloksia, kun kysyntärivillä ei ole sijaintikoodia. Vastaavasti varastointiyksiköiden käyttäminen on ainoa tapa saada vakaita suunnittelutuloksia sijaintien kysyntään liittyen. Jos yritykset suunnittelevat usein kysyntää sijainneissa, Varastointiyksiköt-ominaisuutta kannattaa ehdottomasti käyttää.

## <a name="see-also"></a>Katso myös  
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)   
[Rakennetiedot: suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)   
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)
