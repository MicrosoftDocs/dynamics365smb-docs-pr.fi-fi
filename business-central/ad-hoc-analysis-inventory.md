---
title: Varastotietojen ad-hoc-analyysi
description: Opettele analysoimaan tietoja tietojen analysointitilan avulla varastotiedoissa.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-inventory-data"></a>Varastotietojen ad-hoc-analyysi

Tässä artikkelissa kerrotaan, kuinka voit käyttää **Tietojen analysointi** -ominaisuutta varastotietojen analysointiin suoraan luettelosivuilta ja kyselyistä. Sinun ei tarvitse suorittaa raporttia tai siirtyä toiseen sovellukseen, kuten Exceliin. Ominaisuus tarjoaa vuorovaikutteisen ja monipuolisen tavan laskea, tiivistää ja tarkastella tietoja. Sen sijaan, että raportteja suoritetaan vaihtoehdoilla ja suodattimilla, voit lisätä useita välilehtiä, jotka edustavat erilaisia tehtäviä tai näkymiä tiedoista. Esimerkkejä ovat "vanheneva varasto", "Parhaat myyjät", tai mikä tahansa muu näkymä, jonka voit kuvitella. Lisätietoja **Tietojen analysointi** -ominaisuuden käytöstä on kohdassa [analyysitilassa olevien luettelo- ja kyselytietojen analysointi](analysis-mode.md).

Käytä seuraavia luettelosivuja varastoprosessien tapauskohtaiseen analysointiin:

- [Nimiketapahtumat](https://businesscentral.dynamics.com/?page=38)

## <a name="inventory-ad-hoc-analysis-scenarios"></a>Varastoinnin ad-hoc-analyysiskenaariot

**Tietojen analysointi** -toiminnon avulla voit tarkistaa tiedot nopeasti ja tehdä tapauskohtaisia analyysejä seuraavasti:

- Jos et halua suorittaa raporttia.
- Jos erityiseen tarpeeseesi sopivaa raporttia ei ole.
- Jos haluat nopeasti iteroida saadaksesi hyvän yleiskuvan osasta liiketoimintaasi.

Seuraavissa osissa on esimerkkejä varastoskenaarioista [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa.

| Alue | Vastaanottaja... | Avaa tämä sivu analyysitilassa | Näiden kenttien käyttäminen |
| ---- | ----- | ------------------------------- |------------------- |
| [Käytettävissä oleva varasto](#example-inventory-on-hand) | Varastossa käytettävissä olevien nimikkeiden yleiskuvauksen hakeminen. | [Nimiketapahtumat](https://businesscentral.dynamics.com/?page=38) | **Nimikenumero**, **Jäljellä oleva määrä** |
|[Esimerkki: seuraa vanhentuvaa tai vanhaa varastoa](#example-track-expiring-or-old-stock) | Hanki yleiskuvaus varastossa olevista nimikkeistä, jotka ovat olleet varastossa pitkään ja jotka eivät myy hyvin. | [Nimiketapahtumat](https://businesscentral.dynamics.com/?page=38) | **Kirjauspvm.vuosi**, **Kirjauspvm.kuukausi**, **Nimikkeen nro**, **Kirjauspvm**, **Tapahtuman tyyppi**, **Määrä** ja **Jäljellä oleva määrä**. |
| [Palautetut nimikkeet palautuksen syyn mukaan](#example-returned-items-by-return-reason) | Asiakkaiden palauttamien tavaroiden yleiskuvauksen hakeminen palautuksen syyn mukaan luokiteltuna. Käytä tätä laadunvalvonnan analysointiin. | [Nimiketapahtumat](https://businesscentral.dynamics.com/?page=38) | **Palautuksen syykoodi**, **Kirjauspvm-kuukausi**, **Määrä** , **Kustannussumma**, **Kirjauspvm**, **Asiakirjatyyppi**, **Nimikkeen nro** ja **Asiakirjan nro**. |
| Varaston läpikulkumäärä | Hanki yleiskuvaus varaston ostoista ja myynneistä kuukauden tai vuosineljänneksen mukaan. | [Nimiketapahtumat](https://businesscentral.dynamics.com/?page=38) | **Kirjauspvm-vuosi**, **Kirjauspvm-kuukausi**, **Nimikkeen nro**, **Määrä**, **Myyntisumma**, **Kustannussumma (todellinen)** ja **Kirjauspvm-kuukausi** |
| [Varastosiirrot] | Tutustu varaston tavaroiden siirtoon sijaintien välillä. | [Nimiketapahtumat](https://businesscentral.dynamics.com/?page=38) | **Sijaintikoodi**, **Määrä**, **Kirjauspvm**, **Nimikkeen nro** |

## <a name="example-inventory-on-hand"></a>Esimerkki: Käytettävissä oleva varasto

Voit analysoida varastossa olevia nimikkeitä noudattamalla seuraavia vaiheita:

1. Avaa [Nimikkeen kirjanpitomerkinnät](https://businesscentral.dynamics.com/?page=38) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu).
1. Vedä kentän **Nimikkeen numero** -kenttä **Riviryhmät**-alueelle. Vedä kentät siinä järjestyksessä.
1. Vedä kentän **Jäljellä oleva määrä** -kenttä **Arvot**-alueille.
1. Aseta **Ei yhtä suuri** -suodattimeksi **0** **jäljellä olevalle määrälle**. Jos negatiiviset varastotasot eivät ole sallittuja, määritä suodatin **suuremmaksi kuin** **0**.
1. Vaihtoehtoisesti voit lisätä analyysiin muita kenttiä ja ehkä muuttaa sijaintia tai muita kenttiä.
1. Nimeä analyysivälilehden nimeksi uudelleen **Käytettävissä oleva varasto** tai tuotteiksi, jotka kuvaavat analyysiä.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-inventory-on-hand.png" alt-text="Esimerkki varastosaldotietojen analyysin tekemisestä." lightbox="media/data-analysis-inventory-on-hand.png":::

## <a name="example-track-expiring-or-old-stock"></a>Esimerkki: seuraa vanhentuvaa tai vanhaa varastoa

Seuraa näitä ohjeita hankkiaksesi yleiskuvauksen varastossa olevista nimikkeistä, jotka ovat olleet varastossa pitkään ja jotka eivät myy hyvin:

1. Avaa [Nimikkeen kirjanpitomerkinnät](https://businesscentral.dynamics.com/?page=38) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu oikealla puolella).
1. Vedä **Kirjauspvm. vuosi**, **Kirjauspvm. kuukausi** ja **Nimikenro.**-kentät **riviryhmät**-alueelle. Vedä kentät siinä järjestyksessä.
1. Valitse **Sarakkeet**-alueessa **Kirjauspvm.**, **Tapahtuman tyyppi**-, **Määrä**- ja **Jäljellä oleva määrä** -kentät.
1. Määritä "vanha" määrittämällä **Vähemmän kuin** suodattimen arvo **kirjauspäivämääräksi**.
1. Nimeä analyysivälilehden nimeksi uudelleen **Vanha varasto** tai tuotteiksi, jotka kuvaavat analyysiä.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Esimerkki jäännöserän tietojen analysoinnista nimiketapahtumamerkintöjen sivulla." lightbox="media/data-analysis-inventory-dead-stock.png":::

## <a name="example-returned-items-by-return-reason"></a>Esimerkki: Palautetut nimikkeet palautuksen syyn mukaan

Voit analysoida palautettuja nimikkeitä niiden palautuksen syiden mukaan lajiteltuina noudattamalla seuraavia vaiheita:

1. Avaa [nimiketapahtumat](https://businesscentral.dynamics.com/?page=38)-luettelo.
1. Lisää **Palautussyykoodi**-kenttä mukauttamalla sivua. Valitse **Asetukset**-valikosta **Mukauta**.
1. Poistu mukautustilasta.
1. Valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu oikealla puolella).
1. Vedä **Palautuksen syykoodi**- ja **Kirjauspvm.pvm-kuukausi**-kentät **Riviryhmät**-alueeseen. Vedä kentät siinä järjestyksessä.
1. Vedä **Määrä**- ja **Kustannussumma**-kentät **Arvot**-alueeseen.
1. Lisää muut analyysiin haluamasi kentät ja ota ne käyttöön **Sarakkeet**-alueella. Voit esimerkiksi lisätä **kirjauspvm**-, **Asiakirjatyyppi**-, **Nimikkeen nro.**- ja**Asiakirjan nro.** -kentät.
1. Nimeä analyysivälilehden nimeksi uudelleen **Palautetut nimikkeet palautussyyn mukaan** tai tuotteiksi, jotka kuvaavat analyysiä.  

## <a name="example-inventory-throughput"></a>Esimerkki: Varaston läpikulkumäärä

1. Avaa [Nimikkeen kirjanpitomerkinnät](https://businesscentral.dynamics.com/?page=38) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu oikealla puolella).
1. Ota **pivot-tila** käyttöön (sijaitsee **haku**-kentän yläpuolella oikealla).
1. Vedä **Kirjauspvm. vuosi**, **Kirjauspvm. kuukausi** ja **Nimikenro.**-kentät **riviryhmät**-alueelle.
1. Vedä **Määrä**- , **Myyntisumma**- **Kulumäärä (todellinen)**-kentät **Arvot**-alueeseen.
1. Vedä **Kirjauksen päivä kuukausi** -kentät **Sarakeryhmät**-alueeseen.
1. Nimeä analyysivälilehden nimeksi uudelleen **Varaston läpikulkumäärä kuukausittain** tai tuotteiksi, jotka kuvaavat analyysiä.  

## <a name="inventory-movements"></a>Varastosiirrot

Voit seurata varaston siirtoja sijaintien välillä noudattamalla seuraavia vaiheita:

1. Avaa [Nimikkeen kirjanpitomerkinnät](https://businesscentral.dynamics.com/?page=38) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: ottaaksesi analyysitilan käyttöön.
1. Siirry **Sarakkeet**-valikkoon ja poista kaikki sarakkeet (valitse **Haku**-kentän vieressä oleva ruutu oikealla puolella).
1. Vedä **Sijaintikoodi**-kenttä **Riviryhmät**-alueelle.
1. Vedä **määrä**-kenttä **Arvot**-alueelle.
1. Lisää muut analyysiin haluamasi kentät ja ota ne käyttöön **Sarakkeet**-alueella. Voit esimerkiksi lisätä **Nimikkeen nro** -kentän.
1. Nimeä analyysivälilehden nimeksi uudelleen **Varaston liikkeet** tai tuotteiksi, jotka kuvaavat analyysiä.  

   > [!TIP]
   > Jos lisäät Kirjauspvm-kentän, voit seurata myös ajan mittaan tapahtuvia siirtoja.

## <a name="data-foundation-for-ad-hoc-analysis-on-inventory"></a>Varaston ad-hoc-analyysin tietopohja

Kun kirjaat myyntitilauksen [!INCLUDE [prod_short](includes/prod_short.md)] päivittää asiakkaan tilin, pääkirjanpidon ja nimiketapahtumat.

- Kullekin myyntitilausriville luodaan nimiketapahtuma **Nimiketapahtuma**-taulukkoon (jos myyntiriveillä on nimikenumeroita). Lisäksi myyntitilaukset tallennetaan aina **Lähtevän toimituksen otsikko**- ja **Myyntilaskun otsikko** -taulukoihin. Jos haluat lisätietoja myyntien kirjauksesta, siirry kohtaan [Myyntien kirjaus](ui-post-sales.md).

Kun kirjaat ostoasiakirjan [!INCLUDE [prod_short](includes/prod_short.md)] päivittää toimittajan tilin, pääkirjanpidon (KP), nimiketapahtumat ja resurssitapahtumat.

- Kullekin ostoriville luodaan soveltuvin osin tapahtumia **Nimiketapahtuma**-taulukkoon (jos ostorivi on Nimike-tyyppinen). Lisäksi ostoasiakirjat tallennetaan aina **Tavaran vastaanoton otsikko**- ja **Ostolaskun otsikko** -taulukoihin. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md#posting-purchases).

## <a name="see-also"></a>Katso myös

[Luettelo- ja kyselytietojen analysoiminen analyysitilassa](analysis-mode.md)  
[Varaston analyysien yleiskatsaus](inventory-analytics-overview.md)  
[Analytiikan, liiketoimintatietojen ja raportoinnin yleiskatsaus](reports-bi-reporting.md)  
[Varaston yleiskatsaus](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
