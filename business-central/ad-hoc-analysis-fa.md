---
title: Käyttöomaisuuden tapauskohtainen analyysi
description: Opettele analysoimaan käyttöomaisuuden tietoja tietojen analysointitilan avulla.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5604, 20'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Käyttöomaisuuden tapauskohtainen analyysi

Tässä artikkelissa kerrotaan, kuinka voit käyttää **Tietojen analysointi** -ominaisuutta käyttöomaisuustietojen analysointiin suoraan luettelosivuilta ja kyselyistä. Sinun ei tarvitse suorittaa raporttia tai siirtyä toiseen sovellukseen, kuten Exceliin. Ominaisuus tarjoaa vuorovaikutteisen ja monipuolisen tavan laskea, tiivistää ja tarkastella tietoja. Sen sijaan, että raportteja suoritetaan vaihtoehdoilla ja suodattimilla, voit lisätä useita välilehtiä, jotka edustavat erilaisia tehtäviä tai näkymiä tiedoista. Esimerkkejä ovat "Kaikki resurssit", "Poistot ajan kuluessa", tai mikä tahansa muu näkymä, jonka voit kuvitella. Lisätietoja **Tietojen analysointi** -ominaisuuden käytöstä on kohdassa [analyysitilassa olevien luettelo- ja kyselytietojen analysointi](analysis-mode.md).

Käytä seuraavia luettelosivuja käyttöomaisuusprosessien tapauskohtaisen analysoinnin aloittamiseen:

- [KO-tapahtumat](https://businesscentral.dynamics.com/?page=5604)
- [Pääkirjanpidon tapahtumat](https://businesscentral.dynamics.com/?page=20)

## Käyttöomaisuuden tapauskohtaiset analyysiskenaariot

**Tietojen analysointi** -toiminnon avulla voit tarkistaa tiedot nopeasti ja tehdä tapauskohtaisia analyysejä seuraavasti:

- Jos et halua suorittaa raporttia.
- Jos erityiseen tarpeeseesi sopivaa raporttia ei ole.
- Jos haluat nopeasti iteroida saadaksesi hyvän yleiskuvan osasta liiketoimintaasi.

Seuraavissa osissa on esimerkkejä käyttöomaisuusskenaarioista [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa.

| Alue | Vastaanottaja... | Avaa tämä sivu analyysitilassa | Näiden kenttien käyttäminen |
| ---- | ----- | ------------------------------- |------------------- |
| [Käyttöomaisuus (nykyarvo)](#example-fixed-assets-current-value) | Seuraa käyttöomaisuuden arvoa sekä kaikissa käyttöomaisuuksissa että yhdessä käyttöomaisuudessa. | [KO-tapahtumat](https://businesscentral.dynamics.com/?page=5604) | **Poistokirja**, **KO-nro**, **KO:n kirjauspvm**, **KO:n kirjaustyyppi** ja **Summa** |
| [Resurssien arvon muutokset ajan mittaan](#example-asset-value-changes-over-time) | Resurssien arvon muutosten seuranta ajan mittaan. | [KO-tapahtumat](https://businesscentral.dynamics.com/?page=5604) | **KO:n kirjaustyyppi**, **KO:n kirjauspvm** ja **Summa**- |
|[Käyttöomaisuuden poistot ajan mittaan](#example-fixed-asset-depreciations-over-time) | Seuraa poistoja ajan mittaan sekä kaikissa käyttöomaisuuksissa että yhdessä käyttöomaisuudessa. | [KO-tapahtumat](https://businesscentral.dynamics.com/?page=5604) | **Poistokirja**, **KO-nro**, **KO:n kirjausvuosi**, **KO:n kirjauskuukausi**, **Summa** ja **KO:n kirjaustyyppi** |

### Esimerkki: Käyttöomaisuuden nykyarvo

Voit seurata yhden tai useamman käyttöomaisuuserän arvoa noudattamalla seuraavia vaiheita:

1. Avaa [KO:n kirjanpitomerkinnät](https://businesscentral.dynamics.com/?page=5604) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu oikealla puolella).
1. Vedä **poistokirja** ja **KO-nro.** -kentät **riviryhmät**-alueelle.
1. Valitse **KO:n kirjauspvm**- ja **KO:n kirjaustyyppi** -kentät.
1. Vedä **summa**-kenttä **Arvot**-alueelle.
1. Nimeä analyysivälilehden nimeksi uudelleen **Resurssin yleiskatsaus - arvo** tai tuotteiksi, jotka kuvaavat analyysiä.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Esimerkki siitä, miten tietoja analysoidaan KO-tapahtumat-sivulla omaisuuserän arvon katsomiseksi." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

### Esimerkki: Resurssien arvon muutosten seuranta ajan mittaan

Voit seurata käyttöomaisuuden arvon muutoksia ajan mittaan noudattamalla seuraavia vaiheita:

1. Avaa [KO:n kirjanpitomerkinnät](https://businesscentral.dynamics.com/?page=5604) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu oikealla puolella).
1. Ota **pivot-tila** käyttöön (sijaitsee **haku**-kentän yläpuolella oikealla).
1. Vedä **KO:n kirjaustyyppi** -kenttä **Riviryhmät**-alueelle.
1. Vedä **KO:n kirjausvuosi**- ja **KO:n kirjauskuukausi** -kentät **Sarakeselitteet**-alueeseen.
1. Vedä **summa**-kenttä **Arvot**-alueelle.
1. Nimeä analyysivälilehden nimeksi uudelleen **Resurssin arvon muutokset ajan mittaan** tai tuotteiksi, jotka kuvaavat analyysiä.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png" alt-text="Esimerkki siitä, miten tietoja analysoidaan KO-tapahtumat-sivulla nähdäksesi resurssin arvon muutokset ajan mittaan." lightbox="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png":::

### Esimerkki: käyttöomaisuuden poistot ajan mittaan

Voit seurata yhden tai useamman käyttöomaisuuserän poistoa noudattamalla seuraavia vaiheita:

1. Avaa [KO:n kirjanpitomerkinnät](https://businesscentral.dynamics.com/?page=5604) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu oikealla puolella).
1. Ota **pivot-tila** käyttöön (sijaitsee **haku**-kentän yläpuolella oikealla).
1. Vedä **poistokirja** ja **KO-nro.** -kentät **riviryhmät**-alueelle.
1. Vedä **KO:n kirjausvuosi**- ja **KO:n kirjauskuukausi** -kentät **Sarakeselitteet**-alueeseen.
1. Vedä **summa**-kenttä **Arvot**-alueelle.
1. Valitse **KO:n kirjaustyyppi** -suodatinkentässä **Poisto**.
1. Nimeä analyysivälilehden nimeksi uudelleen **Poistot ajan mittaan** tai tuotteiksi, jotka kuvaavat analyysiä.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png" alt-text="Esimerkki siitä, miten tietoja analysoidaan KO-tapahtumat-sivulla nähdäksesi poistot ajan mittaan." lightbox="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png":::

## Käyttöomaisuuden ad-hoc-analyysin tietopohja

Kun käyttöomaisuuspäiväkirjoja kirjataan, [!INCLUDE [prod_short](includes/prod_short.md)] luo tapahtumat **KO-tapahtuma** -taulukkoon. Tämän vuoksi käyttöomaisuuden tapauskohtainen analyysi tehdään yleensä [KO-tapahtumat](https://businesscentral.dynamics.com/?page=5604)-sivulla.

## Avustajat

*Microsoft ylläpitää tätä artikkelia. Osan esimerkeistä on alun perin kirjoittanut seuraava avustaja.*

* [Aldona Stec](https://www.linkedin.com/in/aldona-stec-25283bb1) | [!INCLUDE[prod_short](includes/prod_short.md)] konsultti

## Katso myös

[Luettelo- ja kyselytietojen analysoiminen analyysitilassa](analysis-mode.md)  
[Käyttöomaisuuden analyysin yleiskatsaus](fa-analytics-overview.md)  
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)  
[Käyttöomaisuuden yleiskatsaus](fa-manage.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]