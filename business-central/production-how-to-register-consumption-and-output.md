---
title: Kulutustuotoksen rekisteröiminen tuotantotilaukselle
description: 'Tässä aiheessa kerrotaan, miten rekisteröidään kulutus ja tuotos vapautetun tuotantotilauksen riville, jota tarkastellaan Tuotantopäiväkirja-sivulla.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5510
ms.date: 03/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="register-consumption-and-output-for-one-released-production-order-line"></a>Yhden vapautetun tuotantotilausrivin kulutuksen ja tuotoksen rekisteröiminen

Tämä tehtävä suoritetaan **Tuotantopäiväkirja**-sivulla. Päiväkirjassa yhdistetään erillisten kulutuspäiväkirjan ja tuotospäiväkirjan toiminnot yhteen. Tuotantopäiväkirjassa yhdistyvät erillisten kulutus- ja tuotospäiväkirjojen toiminnot yhdeksi päiväkirjaksi, joka voidaan avata suoraan vapautetusta tuotantotilauksesta. Sitä käytetään pääasiassa komponenttien kulutuksen, lopullisten tuotettujen nimikkeiden määrän sekä operaatioihin käytetyn ajan manuaaliseen kirjaukseen. Arvot kirjataan vapautetun tuotantotilauksen tapahtumiksi: Kulutusmäärät kirjataan negatiivisiksi nimiketapahtumiksi, tuotosmäärät positiivisiksi tapahtumiksi ja käytetyt ajat kapasiteettitapahtumiksi. Kirjattuja arvoja voidaan tarkastella päiväkirjan alaosassa myös todellisina määrinä.  

> [!NOTE]  
> Koska kulutustietoja käsitellään yhdessä tuotostietojen kanssa, päiväkirjassa voidaan esittää linkitetyt komponentit ja toiminnot loogisena prosessirakenteena: komponentit toimintojen alle sisennettyinä. Tämä edellyttää, että käytetään reitityslinkkien koodeja.  

> [!NOTE]  
> Komponentit, joilla ei ole reitityslinkkien koodeja, näkyvät päiväkirjassa ensimmäisinä.  

## <a name="to-register-consumption-and-output"></a>Kulutuksen ja tuotoksen rekisteröiminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vapautetut tuotantotilaukset** ja valitse sitten vastaava linkki.  
2. Avaa rekisteröimistä odottava vapautettu tuotantotilausrivi ja valitse sitten **Rivit**-pikavälilehdessä ensin **Rivi**-toiminto ja lopuksi **Tuotantopäiväkirja**-toiminto.  

    **Tuotantopäiväkirja**-sivu avautuu, ja siinä näkyvät tuotantotilausrivin arviointiperusteeksi päiväkirjarivit **Tuotantotilauksen komponentti** ja **Tuotantotilauksen reititys** -sivujen mukaisesti. Nämä rivit ovat peräisin tuotannossa olevaan nimikkeeseen liitetystä tuoterakenteesta ja reitityksestä.  Lisätietoja on kohdassa [Tuotannon tuoterakenteiden luominen](production-how-to-create-routings.md).  

3. Syötä päiväkirjan yläreunan **Kirjauspvm**-kenttään kirjauspäivämäärä, jota käytetään kaikilla riveillä. Oletusarvona on käsittelypäivämäärä. Kenttä on tarkoitettu nopeaksi keinoksi asettaa kaikille riveille tarvittaessa yhtenäiset kirjauspäivämäärät.  

    > [!NOTE]  
    >  Itse riville annettu kirjauspäivämäärä kumoaa tämän kentän arvon.  

4. Päiväkirjan yläreunan **Materiaalinottotapa**-suodatinkentässä voit valita, näytetäänkö myös kulutus ja tuotos, joka on kirjattu automaattisesti nimikkeelle ja resurssille määritettyjen materiaalinottotapojen mukaan. Lisätietoja on kohdassa [Komponenttien materiaalinoton ottaminen käyttöön toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md).

5. Jatka antamalla muokattaviin kenttiin tarvittavat määrät – kulutus ja tuotos.  
  
    Päiväkirjan kunkintyyppisellä rivillä näytetään vain tarvittavat kentät. Loput ovat tyhjiä ja kirjoitussuojattuja.  

    Kun päiväkirja avataan, siihen on täytetty valmiiksi kirjattavat määrät. Jos mitään ei vielä ole kirjattu, kaikissa määräkentissä näytetään oletusarvona tuotantotilauksesta haetut oletetut määrät. Jos on tehty osittaisia kirjauksia, rivien määräkentissä näytetään jäljellä olevat määrät. Tilaukselle jo kirjatut määrät ja ajat näytetään päiväkirjan alaosassa todellisina tapahtumina.  

    Voit valita, mitkä arvot **Tuotoksen määrä** -kentässä näytetään valmiina, kun päiväkirja avataan ensimmäisen kerran. Valinta tehdään **Tuotannon asetukset** -sivun **Yleinen**-pikavälilehden **Esias. tuotoksen määrä** -kentässä.

    > [!NOTE]  
    >  Huomaa, että vain tapahtumatyyppiä **Tuotos** oleva viimeisellä päiväkirjan rivillä oleva tuotoksen määrä muuttaa varastotasoa päiväkirjan kirjauksen yhteydessä. Älä siis kirjaa päiväkirjaa, jonka viimeisellä tuotosrivillä on esiasetettu tuotoksen oletusmäärä, ennen kuin kaikki lopulliset nimikkeet on todella tuotettu.  

6. Lisää tuotosrivien **Valmis**-kenttään valintamerkki osoittamaan, että toiminto on valmis. Tämä kenttä on yhteydessä tuotantotilauksen reititysrivin **Reitityksen tila** -kenttään.  
7. Rekisteröi annetut määrät valitsemalla **Kirjaa**-toiminto ja sulje päiväkirja.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    Jos arvot pysyvät kirjattuina, päiväkirja sisältää nämä jäljellä olevat arvot, kun se avataan seuraavan kerran. Kirjatut arvot näytetään päiväkirjan alaosassa todellisina arvoina.  

    > [!NOTE]  
    >   Jos kulutettava nimike on suljettu, päiväkirja ei kirjaa nimikkeen kulutusmääriä. Jos kuormitusryhmä tai tuotantosolu on suljettu, päiväkirja ei kirjaa kyseisen tuotosrivin tuotosmääriä eikä prosessiaikoja.  

    > [!NOTE]  
    > Jos päiväkirja suljetaan kirjaamatta, muutokset menetetään.  

> [!WARNING]  
> **Tuotantopäiväkirja**-sivua ei voi käyttää useampi käyttäjä samanaikaisesti. Tämä tarkoittaa, että jos käyttäjä 2 avaa sivun ja kirjoittaa tietoja, kun käyttäjä 1 toimii jo sivulla, 2 käyttäjä menettää tietoja, kun käyttäjä 1 sulkee sivun.  

## <a name="see-also"></a>Katso myös

[Tuotanto](production-manage-manufacturing.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
