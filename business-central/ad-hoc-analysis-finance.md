---
title: Taloustietojen tapauskohtainen analyysi
description: Opettele analysoimaan tietoja tietojen analysointitilan avulla taloustiedoissa.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-finance-data"></a>Taloustietojen tapauskohtainen analyysi

Tässä artikkelissa kerrotaan, kuinka voit käyttää **Tietojen analysointi** -ominaisuutta taloustietojen analysointiin suoraan luettelosivuilta ja kyselyistä. Sinun ei tarvitse suorittaa raporttia tai siirtyä toiseen sovellukseen, kuten Exceliin. Ominaisuus tarjoaa vuorovaikutteisen ja monipuolisen tavan laskea, tiivistää ja tarkastella tietoja. Sen sijaan, että raportteja suoritetaan vaihtoehdoilla ja suodattimilla, voit lisätä useita välilehtiä, jotka edustavat erilaisia tehtäviä tai näkymiä tiedoista. Esimerkkejä ovat "Kaikki käyttöomaisuus ajan mittaan", "Myyntisaatava", "Ostovelat", tai mikä tahansa muu näkymä. Lisätietoja **Tietojen analysointi** -ominaisuuden käytöstä on kohdassa [analyysitilassa olevien luettelo- ja kyselytietojen analysointi](analysis-mode.md).

Käytä seuraavia luettelosivuja rahoitusprosessien tapauskohtaisen analysoinnin aloittamiseen:

- [Pääkirjanpidon tapahtumat](https://businesscentral.dynamics.com/?page=20)
- [Asiakastapahtumat](https://businesscentral.dynamics.com/?page=25)
- [Toimittajatapahtumat](https://businesscentral.dynamics.com/?page=29)

## <a name="finance-ad-hoc-analysis-scenarios"></a>Rahoituksen ad-hoc-analyysiskenaariot

**Tietojen analysointi** -toiminnon avulla voit tarkistaa tiedot nopeasti ja tehdä tapauskohtaisia analyysejä seuraavasti:

- Jos et halua suorittaa raporttia.
- Jos erityiseen tarpeeseesi sopivaa raporttia ei ole.
- Jos haluat nopeasti iteroida saadaksesi hyvän yleiskuvan osasta liiketoimintaasi.

Seuraavissa osissa on esimerkkejä rahoitusskenaarioista [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa.

| Alue | Vastaanottaja... | Avaa tämä sivu analyysitilassa | Näiden kenttien käyttäminen |
| ---- | ----- | ------------------------------- |------------------- |
| [Raha-asiat (Myyntireskontra)](#example-finance-accounts-receivables) | Katso, mitä asiakkaasi ovat sinulle velkaa, jaoteltuina esimerkiksi aikaväleihin summien erääntymisen osalta. | [Asiakastapahtumat](https://businesscentral.dynamics.com/?page=25) | **Asiakkaan nimi**, **Eräpäivä** ja **Jäljellä oleva summa** |
| [Raha-asiat (Ostovelat)](#example-finance-accounts-payable) | Katso, mitä olet velkaa toimittajillesi, jaoteltuina aikaväleihin summien erääntymisen osalta. | [Toimittajatapahtumat](https://businesscentral.dynamics.com/?page=29) | **Toimittajan nimi**, **Asiakirjatyyppi**, **Asiakirjan nro**, **Eräpäivä vuosi**, **Eräpäivä kuukausi** ja **Jäljellä oleva summa**. |
| [Raha-asiat (Tuloslaskelma)](#example-finance-income-statement) | Tulot tilikartan tulotileillä, esimerkiksi eriteltyinä aikaväleihin summien kirjauksen ajalta. | [Pääkirjanpidon tapahtumat](https://businesscentral.dynamics.com/?page=20) | **KP-tilinro**, **Kirjauspvm** ja **Summa**. |
| [Raha-asiat (Resurssit yhteensä)](#example-finance-total-assets) | Resurssit tilikartan resurssitileillä, esimerkiksi eriteltyinä aikaväleihin summien kirjauksen ajalta. | [Pääkirjanpidon tapahtumat](https://businesscentral.dynamics.com/?page=20) | **KP-tilinro**, **Kirjauspvm** ja **Summa**. |

### <a name="example-finance-accounts-receivables"></a>Esimerkki: Raha-asiat (Myyntireskontra)

Seuraa näitä vaiheita nähdäksesi, mitä asiakkaasi ovat sinulle velkaa, jaoteltuina aikaväleihin summien erääntymisen osalta:

1. Avaa [Asiakastapahtumamerkinnät](https://businesscentral.dynamics.com/?page=25) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse *Haku*-kentän vieressä oleva ruutu oikealla puolella).
1. Ota **pivot*-tila** käyttöön (sijaitsee **haku**-kentän yläpuolella oikealla).
1. Vedä **Asiakkaan nimi** -kenttä **Riviryhmät**-alueeseen ja vedä **Jäljellä oleva summa** **Arvot**-alueelle.
1. Vedä **Eräpäivä kuukausi** -kentät **Sarakeselitteet**-alueeseen.
1. Jos haluat tehdä analyysin tietyltä vuodelta tai vuosineljännekseltä, käytä suodatinta **Analyysisuodattimet**-valikossa (sivun oikealla puolella, **Sarakkeet**-valikon alapuolella.)
1. Nimeä analyysivälilehden nimeksi uudelleen **Erääntyneet tilit kuukausittain** tai tuotteiksi, jotka kuvaavat analyysiä.

### <a name="example-finance-accounts-payable"></a>Esimerkki: Raha-asiat (Ostovelat)

Seuraa näitä vaiheita nähdäksesi, mitä olet velkaa toimittajillesi, jaoteltuina aikaväleihin summien erääntymisen osalta:

1. Avaa [Toimittajatapahtumien merkinnät](https://businesscentral.dynamics.com/?page=29) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan":::. ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu).
1. Ota **pivot-tila** käyttöön (sijaitsee **haku**-kentän yläpuolella oikealla).
1. Vedä **Toimittajan nimi**-, **Asiakirjatyyppi**- ja **Asiakirjan nro.** -kentät **Riviryhmät**-alueelle ja vedä jäljellä oleva **summa**-kenttä **Arvot**-alueelle.
1. Vedä **Eräpäivä vuosi**- ja **Eräpäivä kuukausi** -kentät **Sarakeselitteet**-alueeseen. Vedä kentät siinä järjestyksessä.
1. Jos haluat tehdä analyysin tietyltä vuodelta tai vuosineljännekseltä, käytä suodatinta **Analyysisuodattimet**-valikossa (sivun oikealla puolella, **Sarakkeet**-valikon alapuolella.)
1. Nimeä analyysivälilehden nimeksi uudelleen **Erääntyneet maksutilit kuukausittain** tai tuotteiksi, jotka kuvaavat analyysiä.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Esimerkki tietojen analysoinnista asiakastapahtumien sivulla" lightbox="media/data-analysis-vendor-ledger-entries.png":::

### <a name="example-finance-income-statement"></a>Esimerkki: Raha-asiat (Tuloslaskelma)

Tee seuraavalla tavalla nähdäksesi tulot tilikartan tulotileillä, esimerkiksi eriteltyinä aikaväleihin summien kirjauksen ajalta:

1. Avaa [Pääkirjanpitotapahtumamerkinnät](https://businesscentral.dynamics.com/?page=20) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu).
1. Ota **pivot-tila** käyttöön (sijaitsee **haku**-kentän yläpuolella oikealla).
1. Vedä **KP-tilin numero** -kenttä **Riviryhmät**-alueeseen ja vedä **Summa** **Arvot**-alueelle.
1. Vedä **Kirjauksen päivä kuukausi** -kentät **Sarakeselitteet**-alueeseen.
1. Suodata käyttämäsi tilit tuloslaskelmaa varten. [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman demotiedoissa nämä tilit alkavat numerolla 4, mutta tilikarttasi saattaa olla erilainen. Aseta suodatin tileille **Analyysisuodattimet**-valikon (sivun oikealla puolella, **Sarakkeet**-valikon alapuolella).

   > [!TIP]
   > Suorita [Alustava saldo jaksoittain](https://businesscentral.dynamics.com/?report=38) -raportti nähdäksesi mitä tilejä asetuksissasi käytetään.

1. Nimeä analyysivälilehden nimeksi uudelleen **Tulot kuukausittain** tai tuotteiksi, jotka kuvaavat analyysiä.

### <a name="example-finance-total-assets"></a>Esimerkki: Raha-asiat (Resurssit yhteensä)

Tee seuraavalla tavalla nähdäksesi resurssit tilikartan resurssitileillä, esimerkiksi eriteltyinä aikaväleihin summien kirjauksen ajalta:

1. Avaa [Pääkirjanpitotapahtumamerkinnät](https://businesscentral.dynamics.com/?page=20) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu oikealla puolella).
1. Ota **pivot-tila** käyttöön (sijaitsee **haku**-kentän yläpuolella oikealla).
1. Vedä **KP-tilin numero** -kenttä **Riviryhmät**-alueeseen ja vedä **Summa** **Arvot**-alueelle.
1. Vedä **Kirjauksen päivä kuukausi** -kentät **Sarakeselitteet**-alueeseen.
1. Suodata käyttämäsi tilit kokonaisresurssilaskelmaa varten. [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelman demotiedoissa nämä tilit alkavat numerolla 10, mutta tilikarttasi saattaa olla erilainen. Aseta suodatin sopiville tileille **Lisäsuodattimet**-valikon (sivun oikealla puolella, **Sarakkeet**-valikon alapuolella.)

   > [!TIP]
   > Suorita [Alustava saldo jaksoittain](https://businesscentral.dynamics.com/?report=38) -raportti nähdäksesi mitä tilejä asetuksissasi käytetään.

1. Nimeä analyysivälilehden nimeksi uudelleen **Tulot kuukausittain** tai tuotteiksi, jotka kuvaavat analyysiä.

## <a name="data-foundation-for-ad-hoc-analysis-on-finance"></a>Rahoituksen ad-hoc-analyysin tietopohja

Kun kirjauskansioita kirjataan, [!INCLUDE [prod_short](includes/prod_short.md)] luo tapahtumat **KP-tapahtuma** -taulukkoon. Tämän vuoksi yleinen rahoitustapauskohtainen analyysi tehdään yleensä [Kirjanpitotapahtumat](https://businesscentral.dynamics.com/?page=20)-sivulla. Myyntisaatavien ja ostovelkojen osalta voit analysoida [asiakastapahtumamerkintöjä](https://businesscentral.dynamics.com/?page=25) ja [toimittajatapahtumia](https://businesscentral.dynamics.com/?page=29).

Saat lisätietoja siirtymällä seuraaviin ohjeartikkeleihin:

- [Myymisen ad-hoc-analyysin tietopohja](ad-hoc-analysis-sales.md#data-foundation-for-ad-hoc-analysis-on-sales)
- [Ostamisen ad-hoc-analyysin tietopohja](ad-hoc-analysis-purchasing.md#data-foundation-for-ad-hoc-analysis-on-purchasing)

## <a name="see-also"></a>Katso myös

[Luettelo- ja kyselytietojen analysoiminen analyysitilassa](analysis-mode.md)  
[Talousanalytiikan yleiskatsaus](bi.md)  
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)  
[Talouden yleiskatsaus](finance.md)   
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
