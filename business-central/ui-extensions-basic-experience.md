---
title: Peruskokemuksen laajennus | Microsoft Docs
description: 'Tämä laajennus on uudistettu vaihtoehto Microsoft Dynamics C5:lle.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'C5, financials, extension'
ms.search.form: '20600,'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="the-basic-experience-extension"></a><a name="the-basic-experience-extension"></a>Peruskokemuksen laajennus

Jos olet käyttänyt Microsoft Dynamics C5:tä, Microsoft-kumppanit voivat auttaa siirtymisessä moderniin ratkaisuun, joka perustuu [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan, joten voit edelleen nauttia samoista selkeistä ominaisuuksista kuin Dynamics C5:ssä.

Laajennus on tarkoitettu pienille yrityksille, ja se voi tukea enintään kolmea käyttäjää. Jos tarvitset lisää käyttäjiä, sinun on päivitettävä [!INCLUDE[prod_short](includes/prod_short.md)]:n käyttöoikeus ja poistettava tämän laajennuksen asennus.

> [!NOTE]
> Tällä hetkellä tämä laajennus on saatavilla vain asiakkaille Tanskassa ja Islannissa.

## <a name="whats-available"></a><a name="whats-available"></a>Mitä on saatavilla

Seuraavassa taulukossa on kuvattu ominaisuudet, jotka ovat käytettävissä, jos asennat peruskokemukseen laajennuksen.

|Alue  |Toiminnallisuus  |
|---------|---------|
|**Pääkirjanpito** |Perusrahoitus, talousraportit, käyttöomaisuus, pankin hallinta, pankin täsmäytys, maksut, suoraveloitus, dimensiot, useat valuutat, budjetit, työnkulku, asiakirjanhallinta/OCR, konsolidointi, rajoittamattomat yritykset|
|**Myyntireskontra/myynti** |Perussaamiset, myyntilaskutus, myyntialennukset, hinnoittelu, arvonlisävero, yhteystietojen hallinta |
|**Ostoreskontra/osto** |Perusvelat, ostolaskutus |
|**Projektinhallinta** |Projektit, projektin hinnoittelu, työaikataulukot, toimeksiannot tehtävät, resurssit |
|**Varasto** |Perusvarasto, nimikkeen korvaukset, nimikkeen viittaus |

## <a name="getting-started"></a><a name="getting-started"></a>Aloitusopas

Tämä laajennus on hieman erilainen kuin useimmat, ja tarvitset apua Microsoft-kumppanilta laajennuksen asennukseen ja määrittämiseen. Jotta tiedät mitä odottaa, tässä on korkean tason näkymä siitä, mitä Microsoft-kumppani tekee.

1. Uuden [!INCLUDE[prod_short](includes/prod_short.md)] vuokraajan luominen. Tämä voi olla joko kokeiluversio tai pilviratkaisujen toimittajan (CSP) versio.
2. Lisää vähintään yksi käyttäjä, joka on määritetty Azure Active Directory -tiliisi peruskäyttökokemusta varten.
3. Poista kaikki yritykset, myös Cronus-näyteyritys.
4. Luo uusi yritys, joka ei sisällä esimerkkitietoja tai -asetuksia.
5. Lisää **Demo RapidStart** -paketti. <!--what does the package contain?-->
6. Lataa ja asenna peruskokemuksen laajennus AppSourcesta.

## <a name="migrating-data"></a><a name="migrating-data"></a>Tietojen siirto

Tuo Dynamics C5 -tiedot mukana. Kun Microsoft-kumppani on asentanut peruskokemuslaajennuksen, sinulla on tyhjä yritys. Helppo tapa siirtää tietoja Dynamics C5:stä peruskokemukseen on käyttää C5 Data Migration -laajennusta, joka sisältyy [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Laajennus siirtää asiakkaat, toimittajat, nimikkeet ja pääkirjanpidon tilit sekä niiden tapahtumat.

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Tietojen siirron C5-laajennus](ui-extensions-c5-data-migration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
