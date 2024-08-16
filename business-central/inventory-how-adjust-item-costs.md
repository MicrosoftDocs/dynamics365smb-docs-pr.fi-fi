---
title: Nimikkeiden kustannusten muuttaminen manuaalisesti
description: 'Nimikkeen varastoarvostuksia voidaan muuttaa FIFO- tai keskimääräinen arvostus -menetelmillä, kun tuotteiden kustannukset muuttuvat.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 07/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="adjust-item-costs"></a>Nimikekustannusten muuttaminen

Nimikekustannus (varastoarvo) voi muuttua, kun ostat nimikkeen ja myyt sen myöhemmin, koska rahtikulut lisätään ostohintaan nimikkeen myynnin jälkeen. Kustannusten muuttamisella on merkitystä etenkin tilanteissa, jossa tavaroita myydään ennen tavaroiden oston laskuttamista. Jotta oikea varastoarvo olisi aina tiedossa, nimikekustannuksia on muutettava säännöllisesti. Oikeat kustannukset auttavat varmistetaan, että tuottotilastot ovat ajan tasalla ja talouden avaintunnusluvut ovat oikein. Katso lisätietoja kohdasta [Rakennetiedot: kustannuksen muutos](design-details-cost-adjustment.md).

Nimikekortin **Yksikkökustannus**-kentässä olevan arvon perustana on vakiokustannus niiden nimikkeiden osalta, joilla on vakioarvostusmenetelmä. Niiden nimikkeiden osalta, joilla on jokin muu arvostusmenetelmä, arvon perustana on varastosaldo (laskutetut kustannukset ja oletetut kustannukset) jaettuna saatavana olevalla määrällä. Lisätietoja on kohdassa [Tietoja yksikkökustannuksen laskennasta](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeiden kustannuksia muutetaan automaattisesti aina varastotapahtuman yhteydessä, kuten kirjattaessa nimikkeen ostolaskua.

Yhden tai usean nimikkeen kustannuksia voidaan muuttaa myös manuaalisesti. Manuaaliset muutokset ovat käteviä esimerkiksi silloin, kun tiedetään, että nimikkeen kustannukset ovat muuttuneet jonkin muun syyn kuin nimiketapahtuman vuoksi.

Nimikkeen kustannuksia muutetaan FIFO- tai Keskiarvo-arvostusmenetelmällä ohjatussa **Määritä oma yritys** -määrityksessä tai nimikkeen kortin **Arvostusmenetelmä**-kentässä tehdyn valinnan mukaan. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

FIFO-arvostusmenetelmässä nimikkeen yksikkökustannus on nimikkeen vastaanoton todellinen arvo. Varastonarvostuksessa käytetään oletusta, että ensin varastoon sijoitetut nimikkeet myydään ensin.

Jos käytät Keskiarvo-arvostusmenetelmää, nimikkeen yksikkökustannus lasketaan kussakin vaiheessa keskimääräisenä yksikkökustannuksena oston jälkeen. Varastonarvostus olettaa, että kaikki vaihto-omaisuus myydään samanaikaisesti. Jos nimike käyttää tätä arvostusmenetelmää, voit tarkastella sitä tapahtumahistoriaa, josta keskimääräinen kustannus lasketaan, valitsemalla nimikkeen kortissa **Yksikkökustannus**-kentän.

Kustannusten muuttamistoiminto käsittelee vain arvotapahtumia, joita ei ole muutettu. Tilanteessa, jossa muuttuneet saapuvien kustannukset on siirrettävä liittyviin lähteviin tapahtumaan, se luo uusia muutosarvotapahtumia. Muutosarvotapahtumat perustuvat alkuperäisten arvotapahtumien tietoihin sisältäen muutossumman. Kustannusten muuttamistoiminto käyttää muutostapahtumassa alkuperäisen arvotapahtuman kirjauspäivämäärää, ellei päivämäärä ole suljetulla varastokaudella. Siinä tapauksessa sovellus käyttää seuraavan avoimen varastokauden aloituspäivämäärää. Jos varastokausia ei käytetä, **Pääkirjanpidon asetukset** -sivun **Ensimm. sallittu kirjauspvm** -kentässä oleva päivämäärä määrittää, milloin muutostapahtuma kirjataan.

## <a name="to-adjust-item-costs-manually"></a>Nimikekustannusten muokkaaminen manuaalisesti

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muuta kust. - Nimiketapahtumat** ja valitse sitten vastaava linkki.
2. Määritä **Muuta kustannuksia - Nimiketapahtumat** -sivulla nimikkeet, joiden kustannuksia muutetaan.
3. Valitse **OK**-painike.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a>Yleisten muutosten tekeminen välittömään yksikkökustannukseen

Jos välitöntä yksikkökustannusta on muutettava useissa nimikkeissä, voit käyttää **Muuta nimikekustannuksia tai -hintoja** -eräajoa.  

Eräajo muuttaa nimikekortin **Yksikköhinta**-kentän sisällön. Eräajo muuttaa kentän sisällön samalla tavalla kaikille nimikkeille tai valituille nimikkeille. Eräajo kertoo kentässä olevan arvon määrittämälläsi muutoskertoimella.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muuta nimikekustannuksia tai -hintoja** ja valitse sitten vastaava linkki.  
2. Määritä **Muuta kenttää** -kentässä muutettava nimikkeen tai varastointiyksikön kortin kenttä.  
3. Määritä **Muutoskerroin**-kentässä kerroin, jolla arvoa muutetaan. Syötä esimerkiksi **1,5**, kun haluat suurentaa arvoa 50 %:lla.  
4. Määritä **Nimike**-pikavälilehdessä määritettävät suodattimet, kuten se, mitä nimikkeitä eräajossa käsitellään.  
5. Valitse **OK**-painike.  

## <a name="understanding-unit-cost-calculation"></a>Tietoja yksikkökustannuksen laskennasta

Nimikekortin **Yksikkökustannus**-kentässä olevan arvon perustana on vakiokustannus niiden nimikkeiden osalta, joilla on vakioarvostusmenetelmä. Niiden nimikkeiden osalta, joilla on jokin muu arvostusmenetelmä, arvon perustana on varastosaldo (laskutetut kustannukset ja oletetut kustannukset) jaettuna saatavana olevalla määrällä.  

Se, miten **Arvostusmenetelmä**-kentän sisältö vaikuttaa myyntien ja ostojen yksikkökustannuksen laskentaan, kuvataan yksityiskohtaisemmin seuraavissa luvuissa.  

## <a name="unit-cost-calculation-for-purchases"></a>Yksikkökustannusten laskeminen ostoille

Aina kun ostat nimikkeitä, nimikekortin **Viimeinen välitön kustannus** -kentän arvo kopioidaan ostorivin **Välitön yksikkökustannus** -kenttään tai nimikepäiväkirjan rivin **Yksikkösumma**-riville.  

Se, mitä valitset **Kustannustapa**-kentässä vaikuttaa siihen, miten [!INCLUDE[prod_short](includes/prod_short.md)] laskee **Yksikkökustannus**-kentän sisällön riveillä.  

### <a name="fifo-lifo-specific-or-average-costing-methods"></a>Arvostusmenetelmät FIFO, LIFO, spesifi tai keskiarvo

[!INCLUDE[prod_short](includes/prod_short.md)] käyttää seuraavaa kaavaa ostorivin **Yksikkökustannus PVA** -kentän sisällön tai nimikepäiväkirjan rivin **Yksikkökustannus**-kentän sisällön laskemiseen:  

"Yksikkökustannus (PVA) = (Välitön yksikkökustannus - (Alennussumma / Määrä)) * (1 + Välillinen kustannus-% / 100) + Yleiskustannus  

### <a name="standard-costing-method"></a>Vako-arvostusmenetelmä

Järjestelmä syöttää **yksikkökustannus (PVA)** -kentän ostoriville sekä **yksikkökustannus** -kentän nimikepäiväkirjalle kopioimalla arvon nimikekortin **yksikkökustannus** -kentästä. Jos käytössä on vakioarvostusmenetelmä, arvo perustuu aina vakiokustannukseen.  

Kun osto kirjataan, ostorivin tai nimikepäiväkirjan yksikkökustannus kopioidaan oston nimikelaskutapahtumaan. Se näyttää nimikkeen tapahtumaluettelossa.  

### <a name="all-costing-methods"></a>Kaikki arvostusmenetelmät

Lähdeasiakirjan rivin yksikkökustannusta käytetään laskemaan **Kustannussumma (todellinen)** -kentän arvo tai tarvittaessa tähän nimiketapahtumaan liittyvän **Kustannussumma (oletettu)** -kentän arvo. Kustannus sisällytetään laskelmaan nimikkeen arvostusmenetelmästä riippumatta.  

## <a name="unit-cost-calculation-for-sales"></a>Myynnin yksikkökustannusten laskenta

Kun nimikkeitä myydään, yksikkökustannus kopioidaan nimikekortin **Yksikkökustannus**-kentästä myyntiriville tai nimikepäiväkirjan riville.  

Yksikkökustannus kopioidaan kirjattaessa myyntilaskun nimiketapahtumaan, ja se näkyy nimikkeen tapahtumaluettelossa. [!INCLUDE[prod_short](includes/prod_short.md)] käyttää lähdeasiakirjan rivin yksikkökustannusta laskemaan **Kustannussumma (todellinen)** -kentän sisällön tai tarvittaessa **Kustannussumma (oletettu)** -kentän sisällön tähän nimiketapahtumaan liittyvässä arvotapahtumassa.  

## <a name="track-item-cost-adjustments"></a>Nimikekustannusten muutosten seuraaminen

Nimikekustannukset voivat muuttua monista syistä, joten on tärkeää, että kustannusten muutoksia voi seurata. **Varastokustannusmuutos**-sivulla voi hallita ja seurata kustannusten muutosprosessia. Tällä sivulla on näkyvissä nimikkeet sekä niiden kustannuslaskennan parametrit ja kustannusmuutoksen tila. Luettelo voidaan suodattaa keskittymään nimikkeet, joita on muutettava tai jotka jätetty pois kustannusten muutosprosessista. Lisätietoja kustannusmuutosten seurannasta on kohdassa [Nimikekustannusten muutosten seuraaminen](finance-track-inventory-costs.md).

## <a name="see-also"></a>Katso myös

[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Varasto](inventory-manage-inventory.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
