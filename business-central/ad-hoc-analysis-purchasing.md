---
title: Ad-hoc-analyysit ostamisessa
description: Opettele analysoimaan tietoja tietojen analysointitilan avulla ostoissa.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analyses-in-purchasing"></a>Ad-hoc-analyysit ostamisessa

Tässä artikkelissa kerrotaan, kuinka voit analysoida ostotietoja luettelosivuilta ja kyselyistä **Tietojen analysointi** -ominaisuuden avulla. Ominaisuuden avulla voit analysoida tietoja suoraan sivulta ilman, että sinun tarvitsee ajaa raporttia tai avata muuta sovellusta, kuten Exceliä. Tietojen analysointi mahdollistaa vuorovaikutteisen ja monipuolisen tavan laskea, tiivistää ja tarkastella tietoja. Sen sijaan, että raportteja suoritetaan vaihtoehdoilla ja suodattimilla, voit lisätä useita välilehtiä, jotka edustavat erilaisia tehtäviä tai näkymiä tiedoista. Esimerkkejä ovat "Toimittajani", "Ostotilastot", tai mikä tahansa muu näkymä, jonka voit kuvitella. Lisätietoja **Tietojen analysointi** -ominaisuuden käytöstä on kohdassa [analyysitilassa olevien luettelo- ja kyselytietojen analysointi](analysis-mode.md).

Käytä seuraavia luettelosivuja ostoprosessien tapauskohtaiseen analysointiin:

- [Ostotilaukset](https://businesscentral.dynamics.com/?page=9307)
- [Ostorivit](https://businesscentral.dynamics.com/?page=518)
- [Kirjatut ostolaskut](https://businesscentral.dynamics.com/?page=146)
- [Toimittajatapahtumat](https://businesscentral.dynamics.com/?page=29)
- [Pääkirjanpidon tapahtumat](https://businesscentral.dynamics.com/?page=20)

## <a name="ad-hoc-analysis-scenarios-for-purchasing"></a>Ostamisen ad-hoc-analyysiskenaariot

**Tietojen analysointi** -toiminnon avulla voit tarkistaa tiedot nopeasti ja tehdä tapauskohtaisia analyysejä seuraavasti:

- Jos et halua suorittaa raporttia
- Jos erityiseen tarpeeseesi sopivaa raporttia ei ole
- Jos haluat nopeasti iteroida saadaksesi hyvän yleiskuvan osasta liiketoimintaasi.

Seuraavissa osissa on esimerkkejä ostoskenaarioista [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa.

| Alue | Vastaanottaja... | Avaa tämä sivu analyysitilassa | Näiden kenttien käyttäminen |
| ---- | ----- | ------------------------------- |------------------- |
| [GRNI – yleiskatsaus](#example-goods-received-not-invoiced-grni-overview) | Hae vastaanotettujen tavaroiden, ei laskutettujen tavaroiden (GRNI) yleiskuvaus toimittajilta. | [Ostorivit](https://businesscentral.dynamics.com/?page=518) | **Tyyppi**, **Summan laskut. ei laskutettu (PVA)** (suodatin näissä kentissä), **Toimittajan nro**, **Asiakirjan nro**, **Nro** ja **Summan laskut. ei laskutettu (PVA)** <br><br> **HUOMAA:** Jos haluat näyttää kentät, sivua on mukautettava. Lue lisää kohdasta [Työtilan mukauttaminen](ui-personalization-user.md). | 
| [Raha-asiat (Ostovelat)](#example-finance-accounts-payable) | Katso, mitä olet velkaa toimittajillesi, jaoteltuina aikaväleihin summien erääntymisen osalta. | [Toimittajatapahtumat](https://businesscentral.dynamics.com/?page=29) | **Toimittajan nimi**, **Asiakirjatyyppi**, **Asiakirjan nro**, **Eräpäivä vuosi**, **Eräpäivä kuukausi** ja **Jäljellä oleva summa**. |

## <a name="example-goods-received-not-invoiced-grni-overview"></a>Esimerkki: Tavarat vastaanotettu, Ei laskutettu (GRNI) -yleiskuvaus

Voit luoda Tavarat vastaanotettu, ei laskut. (GRNI) -yleiskuvan toimittajista noudattamalla seuraavia vaiheita:

1. Avaa [Ostorivit](https://businesscentral.dynamics.com/?page=518)-luettelosivu.
1. Mukauta sivua ja lisää **Summa vastaanotettu, ei laskut.** -kenttä. Voit mukauttaa sivua valitsemalla **Asetukset** ja sitten **Mukauta**.
1. Valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu oikealla puolella).
1. Aseta seuraavat suodattimet **Lisäsuodattimet**-valikon (sivun alhaalla, **Sarakkeet**-valikon oikealla puolella) alla:
    - **Tyyppi = Nimike**
    - **Summa vast. ot. ei lask. (PVA) > 0**. 
1. Vedä **Toimittajan nro**-, **Asiakirjan nro**- ja **Nro** -ruudut -kentät **riviryhmät**-alueelle. Vedä kentät siinä järjestyksessä.
1. Lisää **Summa vast. ot. ei laskut. (PVA)** -kenttä, kun haluat sisällyttää sen yleiskuvaan.
1. Jos haluat tehdä analyysin tietyltä vuodelta tai vuosineljännekseltä, käytä suodatinta **Analyysisuodattimet**-valikossa. Valikko on sivun oikealla puolella, **sarakkeet**-valikon alapuolella.
1. Nimeä analyysivälilehden nimeksi uudelleen **tavarat vastaanotettu, ei laskutettu (GRNI)** tai tuotteiksi, jotka kuvaavat analyysiä.

## <a name="example-finance-accounts-payable"></a>Esimerkki: Raha-asiat (Ostovelat)

Seuraa näitä vaiheita nähdäksesi, mitä olet velkaa toimittajillesi, jaoteltuina aikaväleihin summien erääntymisen osalta:

1. Avaa [Toimittajatapahtumien merkinnät](https://businesscentral.dynamics.com/?page=29) -luettelosivu ja ota analyysitila käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu oikealla puolella).
1. Ota **pivot-tila** käyttöön (sijaitsee **haku**-kentän yläpuolella oikealla).
1. Vedä **Toimittajan nimi**-, **Asiakirjatyyppi**- ja **Asiakirjan nro.** -kentät **Riviryhmät**-alueelle ja vedä jäljellä oleva **summa**-kenttä **Arvot**-alueelle.
1. Vedä **Eräpäivä vuosi**- ja **Eräpäivä kuukausi** -kentät **Sarakeselitteet**-alueeseen. Vedä kentät siinä järjestyksessä.
1. Jos haluat tehdä analyysin tietyltä vuodelta tai vuosineljännekseltä, käytä suodatinta **Analyysisuodattimet**-valikossa (sivun oikealla puolella, **Sarakkeet**-valikon alapuolella.)
1. Nimeä analyysivälilehden nimeksi uudelleen **Erääntyneet maksutilit kuukausittain** tai tuotteiksi, jotka kuvaavat analyysiä.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Esimerkki tietojen analysoinnista asiakastapahtumien sivulla" lightbox="media/data-analysis-vendor-ledger-entries.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-purchasing"></a>Ostamisen ad-hoc-analyysin tietopohja

Kun kirjaat ostoasiakirjan [!INCLUDE [prod_short](includes/prod_short.md)] päivittää toimittajan tilin, pääkirjanpidon (KP), nimiketapahtumat ja resurssitapahtumat:

- Jokaiselle ostoasiakirjalle luodaan ostotapahtuma **KP-tapahtuma**-taulukkoon. Myös toimittajan tilille **Toimittajatapahtuma**-taulukkoon luodaan tapahtuma ja lisäksi luodaan KP-tapahtuma asianmukaiselle ostovelkatilille. Lisäksi oston kirjauksen tuloksena saattaa olla arvonlisäverotapahtuman (ALV) ja KP-tapahtuman luonti alennussummalle.

- Kullekin ostoriville luodaan soveltuvin osin tapahtumat:
  - **Nimiketapahtumamerkintä**-taulukkoon, jos ostorivin tyyppi on Nimike.
  - **KP-tapahtuma**-taulukkoon, jos ostorivien tyyppi on KP-tili.
  - **Resurssitapahtuman merkintä** -taulukkoon, jos ostorivin tyyppi on Resurssi.
- Lisäksi ostoasiakirjat tallennetaan aina **Tavaran vastaanoton otsikko**- ja **Ostolaskun otsikko** -taulukoihin.

Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md#posting-purchases).

## <a name="see-also"></a>Katso myös

[Ostojen kirjaaminen](purchasing-how-record-purchases.md#posting-purchases)  
[Luettelo- ja kyselytietojen analysoiminen analyysitilassa](analysis-mode.md)  
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)  
[Ostamisen yleiskatsaus](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
