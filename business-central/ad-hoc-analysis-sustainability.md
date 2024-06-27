---
title: Vastuullisuustietojen ad-hoc-analyysi
description: Opettele analysoimaan kestävyystietoja tietojen analysointitilan avulla.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI, sustainability, ESG'
ms.search.form: '6220,'
ms.date: 06/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-sustainability-data"></a>Vastuullisuustietojen ad-hoc-analyysi

Tässä artikkelissa kerrotaan, kuinka voit käyttää **Tietojen analysointi** -ominaisuutta kestävyystietojen analysointiin suoraan luettelosivuilta ja kyselyistä. Sinun ei tarvitse suorittaa raporttia tai siirtyä toiseen sovellukseen, kuten Exceliin. Ominaisuus tarjoaa vuorovaikutteisen ja monipuolisen tavan laskea, tiivistää ja tarkastella tietoja. Sen sijaan, että raportteja suoritetaan vaihtoehdoilla ja suodattimilla, voit lisätä useita välilehtiä, jotka edustavat erilaisia tehtäviä tai näkymiä tiedoista. Esimerkkejä ovat "Päästöjen yleiskatsaus", "Päästöt laajuuden mukaan", tai mikä tahansa muu näkymä, jonka voit kuvitella. Lisätietoja **Tietojen analysointi** -ominaisuuden käytöstä on kohdassa [analyysitilassa olevien luettelo- ja kyselytietojen analysointi](analysis-mode.md).

Käytä seuraavia luettelosivuja kestävyystietojen tapauskohtaiseen analysointiin:

- [Vastuullisuustapahtumat](https://businesscentral.dynamics.com/?page=6220)

## <a name="sustainability-ad-hoc-analysis-scenarios"></a>Kestävyyden ad-hoc-analyysiskenaariot

**Tietojen analysointi** -toiminnon avulla voit tarkistaa tiedot nopeasti ja tehdä tapauskohtaisia analyysejä seuraavasti:

- Jos et halua suorittaa raporttia.
- Jos erityiseen tarpeeseesi sopivaa raporttia ei ole.
- Jos haluat nopeasti iteroida saadaksesi hyvän yleiskuvan osasta liiketoimintaasi.

Seuraavissa osissa on esimerkkejä kestävyysskenaarioista [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa.

| Alue | Vastaanottaja... | Avaa tämä sivu analyysitilassa | Näiden kenttien käyttäminen |
| ---- | ----- | ------------------------------- |------------------- |
| [Päästöjen yleiskuvaus (kokonaissumma luokittain)](#example-emission-overview-sum-by-category) | Analysoi päästöt luokittain. | [Vastuullisuustapahtumat](https://businesscentral.dynamics.com/?page=6220) | **Tililuokka**, **Tilin nimi**, **Päästöjen NH4**, **Päästöjen CO2** ja **Päästöjen N2O**.|
| [Keskimääräiset päästöt luokkaa kohti](#example-average-emissions-by-category) | Analysoi keskimääräiset päästöt luokittain. | [Vastuullisuustapahtumat](https://businesscentral.dynamics.com/?page=6220) | **Tililuokka**, **Tilin nimi**, **Päästöjen NH4**, **Päästöjen CO2** ja **Päästöjen N2O**.|
| [Päästöt laajuuden mukaan](#example-emissions-by-scope) | Analysoi päästöt laajuuden mukaan. | [Vastuullisuustapahtumat](https://businesscentral.dynamics.com/?page=6220) | **Päästöjen laajuus**, **Tililuokka**, **Päästöjen NH4**, **Päästöjen CO2** ja **Päästöjen N2O**.|

## <a name="example-emission-overview-sum-by-category"></a>Esimerkki: Päästöjen yleiskuvaus (kokonaissumma luokittain)

Voit analysoida päästöjä luokan mukaan noudattamalla seuraavia vaiheita:

1. Avaa [Kestävyystapahtumien merkinnät](https://businesscentral.dynamics.com/?page=6220) -sivu ja ota analyysitila käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu).
1. Ota **pivot**-tila käyttöön (sijaitsee suoraan **haku**-kentän yläpuolella).
1. Vedä **Tililuokka** ja **Tilin nimi** -kentät **riviryhmät**-alueelle. Vedä kentät siinä järjestyksessä.
1. Vedä **Päästö NH4**-, **Päästö CO2**- ja **Päästö N2O** -kentät **Arvot**-alueeseen.
1. Nimeä analyysivälilehden nimeksi uudelleen **Päästöjen yleiskatsaus (summa)** tai tuotteiksi, jotka kuvaavat analyysiä puolestasi.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-sustainability-entries.png" alt-text="Esimerkki 1 tietojen analysoinnista kestävyystapahtumamerkintöjen sivulla." lightbox="media/data-analysis-sustainability-entries.png":::

## <a name="example-average-emissions-by-category"></a>Esimerkki: Keskimääräiset päästöt luokkaa kohti

Voit analysoida keskimääräisiä päästöjä luokan mukaan noudattamalla seuraavia vaiheita:

1. Avaa [Kestävyystapahtumien merkinnät](https://businesscentral.dynamics.com/?page=6220) -sivu ja ota analyysitila käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu).
1. Ota **pivot**-tila käyttöön (sijaitsee suoraan **haku**-kentän yläpuolella).
1. Vedä **Tililuokka** ja **Tilin nimi** -kentät **riviryhmät**-alueelle. Vedä kentät siinä järjestyksessä.
1. Vedä **Päästö NH4**-, **Päästö CO2**- ja **Päästö N2O** -kentät **Arvot**-alueeseen.
1. Valitse **Arvot**-alueen jokaiselle kentälle ne ja muuta yhdistämistoiminnoksi `Average`.
1. Nimeä analyysivälilehden nimeksi uudelleen **Päästöjen yleiskatsaus (keskim.)** tai tuotteiksi, jotka kuvaavat analyysiä puolestasi.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-sustainability-entries-avg.png" alt-text="Esimerkki 2 tietojen analysoinnista kestävyystapahtumamerkintöjen sivulla." lightbox="media/data-analysis-sustainability-entries-avg.png":::

## <a name="example-emissions-by-scope"></a>Esimerkki: Päästöt laajuuden mukaan

Voit analysoida päästöjä laajuuden mukaan noudattamalla seuraavia vaiheita:

1. Avaa [Kestävyystapahtumien merkinnät](https://businesscentral.dynamics.com/?page=6220) -sivu ja ota analyysitila käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu).
1. Ota **pivot**-tila käyttöön (sijaitsee suoraan **haku**-kentän yläpuolella).
1. Vedä **Päästöjen laajuus** ja **Tililuokka**-kentät **riviryhmät**-alueelle. Vedä kentät siinä järjestyksessä.
1. Vedä **Päästö NH4**-, **Päästö CO2**- ja **Päästö N2O** -kentät **Arvot**-alueeseen.
1. Nimeä analyysivälilehden nimeksi uudelleen **Päästöjen yleiskatsaus laajuuden mukaan** tai tuotteiksi, jotka kuvaavat analyysiä puolestasi.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-sustainability-entries-scope.png" alt-text="Esimerkki 3 tietojen analysoinnista kestävyystapahtumamerkintöjen sivulla." lightbox="media/data-analysis-sustainability-entries-scope.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-sustainability"></a>Kestävyyden ad-hoc-analyysin tietopohja

Kestävyyspäiväkirjaan lisäämäsi tiedot ovat väliaikaisia, ja voit muuttaa niitä niiden ollessa päiväkirjassa. Kun kirjaat kestävyyspäiväkirjan, tiedot siirretään Kestävyyskirjanpitotapahtumiin yksittäisiin kestävyystileihin, missä niitä ei voi muuttaa. Voit kuitenkin kirjata peruuttavia tai korjaavia tapahtumia. [Kestävyystapahtumien kirjausten](https://businesscentral.dynamics.com/?page=6220) luettelosivu on tärkein tietolähde kestävyystietojen tapauskohtaisessa analyysissa.

Lisätietoja kestävyystapahtumien kirjauksesta on kohdassa [Kestävyystapahtumien tallennus](finance-sustainability-journal.md).

## <a name="see-also"></a>Katso myös

[Kestävyystapahtumien tallentaminen](finance-sustainability-journal.md)  
[Valmiit kestävyysraportit](sustainability-reports.md)   
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)  
[Kestävän kehityksen hallinnan yleiskatsaus](finance-manage-sustainability.md)   
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
