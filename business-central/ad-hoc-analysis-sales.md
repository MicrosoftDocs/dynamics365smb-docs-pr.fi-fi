---
title: Myyntitietojen ad-hoc-analyysi
description: Opettele analysoimaan tietoja tietojen analysointitilan avulla myyntitiedoissa.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Myyntitietojen ad-hoc-analyysi

Tässä artikkelissa kerrotaan, kuinka voit käyttää **Tietojen analysointi** -ominaisuutta myyntitietojen analysointiin suoraan luettelosivuilta ja kyselyistä. Sinun ei tarvitse suorittaa raporttia tai siirtyä toiseen sovellukseen, kuten Exceliin. Ominaisuus tarjoaa vuorovaikutteisen ja monipuolisen tavan laskea, tiivistää ja tarkastella tietoja. Sen sijaan, että raportteja suoritetaan vaihtoehdoilla ja suodattimilla, voit lisätä useita välilehtiä, jotka edustavat erilaisia tehtäviä tai näkymiä tiedoista. Esimerkkejä ovat "Asiakkaani", "Myyntitilastot", tai mikä tahansa muu näkymä, jonka voit kuvitella. Lisätietoja **Tietojen analysointi** -ominaisuuden käytöstä on kohdassa [analyysitilassa olevien luettelo- ja kyselytietojen analysointi](analysis-mode.md).

Käytä seuraavia luettelosivuja myyntiprosessien tapauskohtaiseen analysointiin:

- [Myyntitilaukset](https://businesscentral.dynamics.com/?page=9305)
- Pääkirjanpidon tapahtumat
- [Asiakastapahtumat](https://businesscentral.dynamics.com/?page=25)
- Nimiketapahtumat
- Kirjatut myyntilaskut
- Myyntipalautustilaukset

## Myynnin ad-hoc-analyysiskenaariot

**Tietojen analysointi** -toiminnon avulla voit tarkistaa tiedot nopeasti ja tehdä tapauskohtaisia analyysejä seuraavasti:

- Jos et halua suorittaa raporttia.
- Jos erityiseen tarpeeseesi sopivaa raporttia ei ole.
- Jos haluat nopeasti iteroida saadaksesi hyvän yleiskuvan osasta liiketoimintaasi.

Seuraavissa osissa on esimerkkejä myyntiskenaarioista [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa.

| Alue | Vastaanottaja... | Avaa tämä sivu analyysitilassa | Näiden kenttien käyttäminen |
| ---- | ----- | ------------------------------- |------------------- |
| [Myynti (oletettu myyntivolyymi)](#example-sales-expected-sales-volume) | Analysoi oletettu myyntivolyymi. | [Myyntitilaukset](https://businesscentral.dynamics.com/?page=9305) | **Tilausasiakkaan nimi**, **Tilausasiakkaan nro**, **Nro** , **Summa**, **Asiakirjan pvm-vuosi** ja **Asiakirjan pvm-kuukausi**. |
| [Myynti (asiakasmyynti volyymin mukaan)](#example-sales-customer-sales-by-volume) | Saat nopean yleissilmäyksen asiakkaista, jotka ostavat eniten, ja asiakkaista, jotka ovat eniten velkaa. | [Asiakastapahtumat](https://businesscentral.dynamics.com/?page=25) | **Asiakkaan nimi**, **Asiakirjan nro**, **Summa** ja **Jäljellä oleva summa**. |
| [Raha-asiat (Myyntireskontra)](#example-finance-accounts-receivables) | Katso, mitä asiakkaasi ovat sinulle velkaa, jaoteltuina esimerkiksi aikaväleihin summien erääntymisen osalta. | [Asiakastapahtumat](https://businesscentral.dynamics.com/?page=25) | **Asiakkaan nimi**, **Eräpäivä** ja **Jäljellä oleva summa**. |

## Esimerkki: Myynti (oletettu myyntivolyymi)

Voit analysoida jokaisen asiakkaan oletettujen myyntivolyymien ja toimittamattomien tilausten myyntisummia vuoden tai kuukauden mukaan noudattamalla seuraavia vaiheita:

1. Avaa [Myyntitilaukset](https://businesscentral.dynamics.com/?page=9305)-luettelo ja ota analyysitila käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu).
1. Ota **pivot**-tila käyttöön (sijaitsee suoraan **haku**-kentän yläpuolella).
1. Vedä **Tilausasiakkaan nimi**-, **Tilausasiakkaan nro**- ja **Nro**- -kentät **riviryhmät**-alueelle. Vedä kentät siinä järjestyksessä.
1. Vedä kentän **summa**-kenttä **Arvot**-alueelle.
1. Vedä **Asiakirjan päivä vuosi**- ja **Asiakirjan kuukausi** -kentät **Sarakeselitteet**-alueeseen. Vedä kentät siinä järjestyksessä.
1. Jos haluat tehdä analyysin tietyltä vuodelta tai vuosineljännekseltä, käytä suodatinta **Lisäsuodattimet**-valikossa. Valikko on sivun oikealla puolella, **sarakkeet**-valikon alapuolella.
1. Nimeä analyysivälilehden nimeksi uudelleen **Odotettu myyntimäärä** tai tuotteiksi, jotka kuvaavat analyysiä puolestasi.

## Esimerkki: Myynti (asiakasmyynti volyymin mukaan)

Voit luoda yleiskatsauksen asiakkaista, jotka ostavat eniten tai jotka ovat eniten velkaa, seuraavasti:

1. Avaa [Asiakastapahtumien merkinnät](https://businesscentral.dynamics.com/?page=25) -luettelosivu ja ota analyysitila käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu).
1. Vedä **Asiakkaan nimi** -kenttä **Riviryhmät**-alueeseen ja **Asiakirjan nro** - kenttään kentän alapuolella.
1. Valitse **Summa**- ja **Jäljellä oleva summa** -kentät.
1. Jos haluat tehdä analyysin tietyltä vuodelta tai vuosineljännekseltä, käytä suodatinta **Lisäsuodattimet**-valikossa. Valikko on sivun oikealla puolella, **sarakkeet**-valikon alapuolella.
1. Nimeä analyysivälilehden nimeksi uudelleen **Asiakas myyntimäärän mukaan** tai tuotteiksi, jotka kuvaavat analyysiä puolestasi.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Esimerkki tietojen analysoinnista asiakastapahtumamerkintöjen sivulla." lightbox="media/data-analysis-customer-ledger-entries.png":::

## Esimerkki: Raha-asiat (Myyntireskontra)

Seuraa näitä vaiheita nähdäksesi, mitä asiakkaasi ovat sinulle velkaa, jaoteltuina aikaväleihin summien erääntymisen osalta:

1. Avaa [Asiakastapahtumien merkinnät](https://businesscentral.dynamics.com/?page=25) -luettelosivu ja ota analyysitila käyttöön.
1. Poista kaikki sarakkeet **Sarakkeet**-valikosta (valitse **Haku**-kentän vieressä oleva ruutu).
1. Ota **pivot**-tila käyttöön (sijaitsee suoraan **haku**-kentän yläpuolella).
1. Vedä **Asiakkaan nimi** -kenttä **Riviryhmät**-alueeseen ja vedä **Jäljellä oleva summa** -kenttä **Arvot**-alueelle.
1. Vedä **Eräpäivä kuukausi** -kentät **Sarakeselitteet**-alueeseen.
1. Jos haluat tehdä analyysin tietyltä vuodelta tai vuosineljännekseltä, käytä suodatinta **Lisäsuodattimet**-valikossa. Valikko on sivun oikealla puolella, **sarakkeet**-valikon alapuolella.
1. Nimeä analyysivälilehden nimeksi uudelleen **Erääntyneet tilit kuukausittain** tai tuotteiksi, jotka kuvaavat analyysiä puolestasi.

## Myymisen ad-hoc-analyysin tietopohja

Kun olet syöttänyt tiedot myyntitilauksesta ja lisännyt kaikki myyntitilausrivit, voit kirjata tilauksen. Kirjaus luo toimituksen ja laskun. [!INCLUDE [prod_short](includes/prod_short.md)] päivittää asiakkaan tilin, pääkirjanpidon ja nimiketapahtumien päivittämiseksi:

- Jokaiselle myyntitilaukselle luodaan myyntitapahtuma **KP-tapahtuma**-taulukossa. Myös **Toimittajatapahtuma**-taulukon asiakkaan tilille luodaan tapahtuma. Lisäksi luodaan pääkirjanpidon tapahtuma asianmukaiselle myyntisaamistilille. Lisäksi tilauksen kirjauksen tuloksena saattaa olla ALV-tapahtuman ja KP-tapahtuman luonti alennussummalle.
- Jokaiselle myyntitilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos myyntiriveillä on nimikenumeroita) tai pääkirjanpidon tapahtuma **KP-tapahtuma**-taulukkoon (jos myyntiriveillä on pääkirjanpitotili). Lisäksi myyntitilaukset tallennetaan aina **Lähtevän toimituksen otsikko**- ja **Myyntilaskun otsikko** -taulukoihin.

Jos haluat lisätietoja myyntien kirjauksesta, siirry kohtaan [Myyntien kirjaus](ui-post-sales.md).

## Katso myös

[Myynnin kirjaaminen](ui-post-sales.md)  
[Luettelo- ja kyselytietojen analysoiminen analyysitilassa](analysis-mode.md)  
[Myynnin analyysin yleiskatsaus](sales-analytics-overview.md)  
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)  
[Myynnin yleiskatsaus](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]