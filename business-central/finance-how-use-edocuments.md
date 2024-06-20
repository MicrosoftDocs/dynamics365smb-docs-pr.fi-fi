---
title: Sähköisten asiakirjojen käyttö myynnissä
description: Lisätietoja myyntiin liittyvien sähköisten asiakirjojen toimintojen käyttämisestä.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, deliver'
ms.search.form: '42, 43, 132, 6103, 6133, 6121, 9301, 9305'
ms.date: 04/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Sähköisten asiakirjojen käyttäminen myyntiprosessissa

Voit käyttää määritettyjä sähköisiä asiakirjoja myyntiasiakirjojen yhteydessä.

Tällä hetkellä voit käyttää seuraavia myyntiasiakirjoja sähköisten asiakirjojen toimintojen kanssa:  

- Myyntilaskut
- Myyntitilaukset
- Myyntihyvityslaskut
- Huoltolaskut
- Huollon hyvityslaskut
- Rahoituskululaskut
- Muistutukset

## Myynnin sähköiset asiakirjat  

Voit luoda ja lähettää asiakkaalle sähköisen laskun, jos luot ensin myyntilaskun ja kirjaat sen. Lisätietoja vakioprosessista on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).

Kun olet kirjannut myyntiasiakirjan, avaa **Kirjatut myyntilaskut** -sivu ja sen jälkeen liittyvä **Sähköiset asiakirjat** -sivu.

### Sähköisten asiakirjojen tarkasteleminen   

Voit tarkastella aiemmin luotuja sähköisiä asiakirjoja alla olevien ohjeiden avulla.

1. Valitse **Kirjatut myyntilaskut** -sivulla **Sähköinen asiakirja** ja sitten **Avaa sähköinen asiakirja**.
2. **Sähköiset asiakirjat** -sivun otsikossa näkyvät kirjatun laskun perustiedot.
3. **Tietue**-kentässä on kirjatun myyntilaskun asiakirjanumero. Avaa asiakirja valitsemalla linkki.
4. **Sähköisen asiakirjan tila** -kentässä voit tarkastella asiakirjan reaaliaikaista tilaa ja sen sijaintia prosessiputkessa. Jos asiakirja on kirjattu, tila on **Käsitelty**.

### Sähköisten asiakirjojen tilat ja lokit 

Saat lisätietoja sähköisen asiakirjapalvelun tilan tasosta **Sähköisen asiakirjapalvelun tila** -pikavälilehdestä. Järjestelmä näyttää riveillä vähintään yhden asiakirjan käyttämän palvelun. Yleisimmässä skenaariossa jokainen asiakirja käyttää vain yhtä palvelua. Asiakirja voi kuitenkin käyttää useita palveluita.

- Tarkista **Sähköisen asiakirjan huoltokoodi** -kentästä käytettävissä oleva palvelu.
- Määritä tämän asiakirjan nykyisen palvelun tila **Sähköisen asiakirjan tila** -kentästä.
- Jos haluat lisätietoja, valitse palvelun **Lokit**-kenttä **Sähköisten asiakirjojen lokit** -sivulla. Esille tulee asiakirjojen eri tilojen yhteenveto aikajärjestyksessä.
- Tarkista **Tapahtumanro**- ja **Luotu**-kenttien arvot ja muut **Sähköisten asiakirjojen lokit** -sivun tiedot. **Sähköisen asiakirjan tila** -kentän ensimmäinen tila on **Tuotu**. Se osoittaa, että sähköisen asiakirjan tiedosto on luotu. Seuraava tila on **Lähetetty**. Se osoittaa, että asiakirja on lähetetty palveluntarjoajalle, jos tämä on määritetty.

Saat lisätietoja valitsemalla tapahtuma, jonka tila on **Viety**, ja suorittamalla jonkin seuraavista toiminnoista:

- **Avaa yhdistämislokit** – Saat yleiskatsauksen **Alkuperäinen arvo** -kentän lähdetaulukoista viedyistä kentistä. Jos käytettiin vientiprosessin muutossääntöjä, voit saada myös lopullisen arvon **Uusi arvo** -kenttään.
- **Vie tiedosto** – Vie XML-tiedosto manuaalista tarkistusta varten.

Jos haluat tarkastella itsesi ja sen palvelun välistä viestintää, jolle lähetät asiakirjan, voit valita **Viestintälokit**-kentän. Avaa **Sähköisen asiakirjan viestintälokit** -sivu, jos haluat tarkastella kyseisen palvelun pyynnön ja syiden sanomaa.

Jos palveluntarjoajan kanssa on ongelmia, eikä asiakirjaa voi lähettää, etsi **Sähköiset asiakirjat** -sivulta seuraavat ilmaisimet:

- Otsikon **Sähköisen asiakirjan tila** -kentässä on **Virhe**-tila.
- **Sähköisen asiakirjapalvelun tila** -pikavälilehden **Sähköisen asiakirjan tila** -kentässä on **Lähetysvirhe**-tila.
- **Virheet ja varoitukset** -pikavälilehdessä on yksi tai useita sanomia, joissa on tietoja ongelman syystä.

Kun ongelma on korjattu, suorita manuaalisesti **Lähetä asiakirja** -toiminnot. Jos tarvitset erilaisia toimintoja, kuten **Uudelleenluotu asiakirja**-, **Peruuta asiakirja**- tai **Hae hyväksyntää** -toiminnon, voit suorittaa niitä.

## Sähköisten asiakirjojen tilojen yleiskatsaus

Jos haluat aiempaa paremman yleiskatsauksen yrityksen kaikista sähköisistä asiakirjoista, voit valita **Kirjanpitäjä**-roolikeskuksen, jossa sähköisten asiakirjojen tilat ovat. Siellä voit etsiä sähköistä asiakirjaa koskevat aktiviteetit, joilla on seuraavat tilat:

- **Lähtevät sähköiset asiakirjat:**

    - Käsitelty
    - Työn alla
    - Virhe


## Katso myös

[Toimintaohje: Sähköisten asiakirjojen määrittäminen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa](finance-how-setup-edocuments.md)    
[Tietoja sähköisten asiakirjojen käytöstä ostossa](finance-how-use-edocuments-purchase.md)  
[Sähköisten asiakirjojen laajentaminen [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Taloushallinto](finance.md)    
[Myynnin laskutus](sales-how-invoice-sales.md)    
[Ostojen kirjaaminen ostolaskujen ja tilausten avulla](purchasing-how-record-purchases.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
