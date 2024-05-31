---
title: Suunnittelun tiedot - vähennyskelvoton ALV
description: 'Tässä artikkelissa on tietoja vähennyskelvottomasta arvonlisäverosta (ALV), joka on ostajan maksettavaksi tuleva ALV, mutta se ei ole vähennyskelpoinen ostajan omasta ALV-velasta.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Suunnittelun tiedot: vähennyskelvoton ALV

Vähennyskelvoton arvonlisävero (ALV) on ostajan maksettavaksi tuleva ALV, mutta se ei ole vähennyskelpoinen ostajan omasta ALV-velasta. Koska voi olla vaikea tietää, missä ja miten nimikettä käytetään, sinun on otettava yhteyttä oman maasi tai alueesi paikallisiin veroviranomaisiin ja selvitettävä, vähennetäänkö tietty prosenttiosuus ALV:stä. Vaikka tiedät, että tietty prosenttiosuus ALV:stä ei ole vähennyskelpoinen, vähennyskelvottomia määriä käsitellään eri malleilla, koska ne liittyvät **nimikkeisiin** ja **käyttöomaisuuteen**.

## Vähennyskelvottoman ALV:n käytön edellytykset

Voit käyttää ja kirjata vähennyskelvottoman ALV:n seuraavasti.

1. Valitse **ALV-asetukset**-sivulla **Ota käyttöön vähennyskelvoton ALV**, jotta ominaisuus otetaan käyttöön.
2. Valitse **ALV-kirjausten asetukset** -sivulta, mitkä ALV-kirjausryhmät voivat käyttää vähennyskelvotonta ALV:tä.

## Esimerkkejä

Seuraavissa esimerkeissä vähennyskelvoton ALV on käytössä ja seuraavat asetukset on suoritettu:

- Tuotteen **ALV-kirjausryhmä**-kentän arvona on **NDVAT**.
- **ALV-kirjausten asetukset** -sivulla:

    - **NDVAT**-arvona on tuotteen ALV-kirjausryhmä, ja **KOTIMAINEN** määritetään liiketoiminnan ALV-kirjausryhmäksi.
    - **ALV-tunnus**-kentän arvon on oltava yksilöivä.
    - Kohteen **ALV-%**-kentän arvoksi on määritetty **25**.
    - **Salli vähennyskelvoton ALV** -kentän arvoksi on asetettu **Salli**.
    - **Vähennyskelvoton ALV-%** -kentän arvoksi on asetettu **100**.
    - **ALV-laskennan tyyppi** -kentän arvoksi on asetettu **Normaali ALV**.
    - Vain myynnin ALV-tili ja ostojen ALV-tili määritetään.

Kaikki esimerkit käyttävät nimikkeitä ja käyttöomaisuutta, joissa tuotteen ALV-kirjausryhmä on **NDVAT**.

### Nimikkeet

Uuden nimikkeen **NDVAT**-arvo on määritetty tuotteen ALV-kirjausryhmäksi. Ostoasiakirjassa **määrä** = **1** ja **välitön kustannus ilman ALV:tä** = **1 000,00**.

Huolimatta käytetystä vaihtoehdosta **ALV-tapahtuman** tulokset ovat samat.

| Asiakirjatyyppi | Tyyppi | Perusosa | Summa | Vähennyskelvoton ALV-peruste | Vähennyskelvoton ALV-summa |
|---|---|---|---|---|---|
| Lasku | Ostot | 0.00 | 0.00 | 1,000.00 | 250.00 |

Tiedot näkyvät **arvotapahtumissa**.

> [!NOTE]
> Voit ottaa käyttöön **Käytä kohteen kustannuksiin** -kentän **ALV-asetukset**-sivulla.

#### Käytä nimikekustannuksille ei ole käytössä

| Nimiketapahtuman tyyppi | Tapahtuman tyyppi | Kustannussumma (todellinen) | Nimiketapahtumien määrä |
|---|---|---|---|
| Ostot | Välitön kustannus | 1,000.00 | 1 |

#### Käytä nimikekustannuksille on käytössä

| Nimiketapahtuman tyyppi | Tapahtuman tyyppi | Kustannussumma (todellinen) | Nimiketapahtumien määrä |
|---|---|---|---|
| Ostot | Välitön kustannus | 1,250.00 | 1 |

### Käyttöomaisuus

Uudella käyttöomaisuuserällä on hankintamenotili, joka on määritetty käyttämään **NDVAT**-tiliä tuotteen ALV-kirjausryhmänä. Ostoasiakirjassa **määrä** = **1** ja **välitön kustannus ilman ALV:tä** = **1 000,00**.

Huolimatta käytetystä vaihtoehdosta **ALV-tapahtuman** tulokset ovat samat.

| Asiakirjatyyppi | Tyyppi | Perusosa | Summa | Vähennyskelvoton ALV-peruste | Vähennyskelvoton ALV-summa |
|---|---|---|---|---|---|
| Lasku | Ostot | 0.00 | 0.00 | 1,000.00 | 250.00 |

Tiedot näkyvät **käyttöomaisuuskirjanpidon tapahtumissa**.

> [!NOTE]
> Voit ottaa käyttöön **Käytä käyttöomaisuuden kustannuksiin** -kentän **ALV-asetukset**-sivulla.

#### Käyttöomaisuuskustannusten käyttö ei ole käytössä

| Asiakirjatyyppi | KO:n kirjaustyyppi | Summa | ALV-summa |
|---|---|---|---|
| Lasku | Hankintameno | 1,000.00 | 250.00 |

#### Käyttöomaisuuskustannusten käyttö on käytössä

| Asiakirjatyyppi | KO:n kirjaustyyppi | Summa | ALV-summa |
|---|---|---|---|
| Lasku | Hankintameno | 1,000.00 | 250.00 |
| Lasku | Hankintameno | 250.00 | 0.00 |

## Katso myös

[Vähennyskelvottoman ALV:n määritys](finance-setup-nondeductible-vat.md)  
[Taloushallinto](finance.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
