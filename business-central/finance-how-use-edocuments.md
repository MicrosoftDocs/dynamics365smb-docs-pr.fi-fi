---
title: Sähköisten asiakirjojen käyttäminen myynnissä ja ostoissa
description: Lisätietoja myynti- ja ostolaskuihin liittyvien sähköisten asiakirjojen toimintojen käyttämisestä.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, purchase'
ms.search.form: '42, 43, 51, 6103, 6133, 6121, 9301, 9305, 9308'
ms.date: 10/03/2023
ms.author: altotovi
---

# Sähköisten asiakirjojen käyttäminen myynnissä ja ostoissa

Voit käyttää määritettyjä sähköisiä asiakirjoja myynti- ja ostoasiakirjojen yhteydessä.

Tällä hetkellä voit käyttää seuraavia asiakirjoja sähköisiä asiakirjoja varten:

- Myyntilaskut
- Myyntitilaukset
- Myyntihyvityslaskut
- Ostolaskut
- Ostotilaukset
- Ostohyvityslaskut
- Yleiset päiväkirjat

Tällä hetkellä ostotilausta voidaan käyttää vain silloin, kun asiakirja luodaan toimittajan lähettämästä sähköisestä asiakirjasta. Et kuitenkaan voi päivittää olemassa olevaa asiakirjaa riveillä, jotka olet saanut toimittajaltasi.

## Myynnin sähköiset asiakirjat

Voit luoda ja lähettää asiakkaalle sähköisen laskun, jos luot ensin myyntilaskun ja kirjaat sen. Lisätietoja vakioprosessista on kohdassa [Myynnin laskutus](sales-how-invoice-sales.md).

Kun olet kirjannut myyntiasiakirjan, avaa **Kirjattu myyntilasku** -sivu ja sen jälkeen liittyvä **Sähköinen asiakirja** -sivu.

### Sähköisten asiakirjojen tarkasteleminen

Voit tarkastella aiemmin luotuja sähköisiä asiakirjoja alla olevien ohjeiden avulla.

1. Valitse **Kirjattu myyntilasku** -sivulla **Sähköinen asiakirja** \> **Avaa sähköinen asiakirja**.
2. **Sähköinen asiakirja** -sivun otsikossa näkyvät kirjatun laskun perustiedot.
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

Jos palveluntarjoajan kanssa on ongelmia, eikä asiakirjaa voi lähettää, etsi **Sähköinen asiakirja** -sivulta seuraavat ilmaisimet:

- Otsikon **Sähköisen asiakirjan tila** -kentässä on **Virhe**-tila.
- **Sähköisen asiakirjapalvelun tila** -pikavälilehden **Sähköisen asiakirjan tila** -kentässä on **Lähetysvirhe**-tila.
- **Virheet ja varoitukset** -pikavälilehdessä on yksi tai useita sanomia, joissa on tietoja ongelman syystä.

Kun ongelma on korjattu, suorita manuaalisesti **Lähetä asiakirja** -toiminnot. Jos tarvitset erilaisia toimintoja, kuten **Uudelleenluotu asiakirja**-, **Peruuta asiakirja**- tai **Hae hyväksyntää** -toiminnon, voit suorittaa niitä.

## Sähköiset asiakirjat ostoissa

Dynamics 365 Business Centralin ostojen sähköisten laskujen vastaanotto voidaan tehdä eräajona tai manuaalisesti.

### Eräajon suorittaminen

> [!NOTE]
> Tämä eräajo on tarkoitettu saapuvien laskujen automaattista keräilyä varten. Toiminnon käyttäminen on mahdollista vain, jos se on otettu käyttöön maassa tai alueella.

Aina, kun työjono suoritetaan ja ulkoisella palvelulla on toimittajan lähettämiä saapuvia laskuja, järjestelmä kerää ja tuo kyseiset laskut. Voit suorittaa prosessin loppuun alla olevien ohjeiden avulla.

1. Kun eräajo on suoritettu loppuun, juuri tuodut laskut ja niiden perustiedot näkyvät **Sähköiset asiakirjat** -sivulla.
2. Voit tarkastella lisätietoja avaamalla tietyn sähköisen asiakirjan.
3. Jos sähköisessä asiakirjassa ja sen yhdistämismäärityksessä ei ollut virheitä tai ongelmia, **Tietue**-kentässä näkyy järjestelmän automaattisesti luoma ostolaskun asiakirjanumero. Avaa asiakirja valitsemalla linkki. Järjestelmän luoma asiakirja ei ole kirjattu asiakirja.
4. Voit siirtyä suoraan ostoasiakirjaan valitsemalla **Tietue**-kentän. Kun olet avannut **Ostolasku**-sivun, tarkista asiakirja. Jos kaikki on nyt oikein, voit kirjata asiakirjan.
5. Kun kirjaat ostoasiakirjan, **Sähköinen asiakirja** -sivun**Tietue**-kentän arvo päivitetään **Lasku**-arvosta **Ostotilaus**-arvoksi, ja kirjatun ostoasiakirjan numero on saatavilla. Voit valita numeron, jos haluat avata kirjatun ostolaskun.

Lokien tiedot ovat samat kuin sähköisten asiakirjojen myyntiprosessissa.

Koska myyntiprosessin virheet liittyvät useimmiten palvelun saatavuuteen, saapuva asiakirja voi sisältää useita syitä. Virheen yleisin syy on se, että järjestelmä ei tunnista toimittajalta saadun sähköisen asiakirjan rivejä. Sen vuoksi ostolaskuun ei voida syöttää rivejä.

Seuraavassa kerrotaan kaksi yleisintä virhettä:

- Jos haluat käyttää suoraan pääkirjanpidon (KP) tilille kirjatun toimittajalaskun tiettyä riviä, **Tekstin linkitys** -arvo on määritettävä oikein. Jos haluat ohittaa tämän virheen ja käyttää KP-tilejä, valitse **Linkitä teksti tiliin** ja luo **Tekstin linkitys** -arvolle ja käytettävälle **Debet-tilin numero** -arvolle tietty yhdistämismääritys.
- Jos haluat seurata varastoa ja käyttää toimittajalaskun rivejä asiakirjarivien nimikkeiden täyttämisessä, määritä oikein **Nimikeviittauksen nro** -arvo. Voit ohittaa tämän virheen linkittämällä ulkoisen nimikkeen nimikenumeroihin nimikkeen viiteluettelon avulla. Saat lisätietoja kohdasta [Nimikkeen viittausten käyttäminen](inventory-how-use-item-cross-refs.md).

Virheiden ja varoitusten korjaamisen jälkeen voit manuaalisesti määrittää, milloin järjestelmän tulee luoda ostolasku asetusten perusteella, valitsemalla **Luo tiedosto**.

### Laskujen tuominen manuaalisesti

Voit tuoda manuaalisesti ulkoisia sähköisiä asiakirjoja alla olevien ohjeiden mukaan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sähköinen asiakirjapalvelu** ja valitse sitten vastaava linkki.
2. Valitse **Sähköinen asiakirjapalvelu** -sivulla aktiivinen palvelu. 
3. Valitse **Vastaanotto** ja lataa toimittajalta saatu sähköisen asiakirjan tiedosto.
4. Jos virhesanoma näkyy jälleen, avaa sähköinen asiakirja ja korjaa virheet.
5. Kun virheet on korjattu, valitse **Tuo manuaalisesti** -ryhmässä **Luo asiakirja**.
6. Kun asiakirja on luotu Business Centralissa, voit tarkastella sitä samalla tavalla kuin eräajoa käytettäessä.

## Sähköisten asiakirjojen tilojen yleiskatsaus

Jos haluat aiempaa paremman yleiskatsauksen yrityksen kaikista sähköisistä asiakirjoista, voit valita **Kirjanpitäjä**-roolikeskuksen, jossa sähköisten asiakirjojen tilat ovat. Siellä voit etsiä sähköistä asiakirjaa koskevat aktiviteetit, joilla on seuraavat tilat:

- **Lähtevät sähköiset asiakirjat:**

    - Käsitelty
    - Työn alla
    - Virhe

- **Saapuvat asiakirjat:**

    - Käsitelty
    - Työn alla
    - Virhe

## Katso myös

[Sähköisten asiakirjojen määrittäminen Business Centralissa](finance-how-setup-edocuments.md)  
[Sähköisten asiakirjojen laajentaminen Business Centralissa](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Taloushallinto](finance.md)  
[Lasku – myynti](sales-how-invoice-sales.md)  
[Ostojen kirjaaminen ostolaskujen ja tilausten avulla](purchasing-how-record-purchases.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
