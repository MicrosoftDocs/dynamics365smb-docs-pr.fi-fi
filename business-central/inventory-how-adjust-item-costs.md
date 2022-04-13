---
title: Nimikekustannusten muokkaaminen manuaalisesti
description: Voit muuttaa nimikkeen varastoarvostuksia manuaalisesti FIFO- tai keskimääräinen arvostus -menetelmillä, kun tuotteiden kustannukset muuttuvat.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 8b547aadab56af50aab5442b2634d4bcd1efe4cc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515009"
---
# <a name="adjust-item-costs"></a>Nimikekustannusten muuttaminen
Nimikekustannus (varastoarvo) voi muuttua, kun ostat nimikkeen ja myyt sen myöhemmin, koska rahtikulut lisätään ostohintaan nimikkeen myynnin jälkeen. Kustannusten muuttamisella on merkitystä etenkin tilanteissa, jossa tavaroita myydään ennen tavaroiden oston laskuttamista. Jotta oikea varastoarvo on tiedossa, nimikekustannukset on mukautettava säännöllisesti. Näin varmistetaan, että tuottotilastot ovat ajan tasalla ja talouden avaintunnusluvut ovat oikein. Katso lisätietoja kohdasta [Rakennetiedot: kustannuksen muutos](design-details-cost-adjustment.md).

Perussäännön mukaan nimikekortin **Yksikkökustannus**-kentässä olevan arvon perustana on vakiokustannus niiden nimikkeiden osalta, joilla on vakioarvostusmenetelmä. Niiden nimikkeiden osalta, joilla on jokin muista arvostusmenetelmistä, arvon perustana on varastosaldo (laskutetut kustannukset ja oletetut kustannukset) jaettuna saatavilla olevalla määrällä. Lisätietoja on kohdassa [Tietoja yksikkökustannuksen laskennasta](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeiden kustannuksia muutetaan automaattisesti aina varastotapahtuman yhteydessä, kuten kirjattaessa nimikkeen ostolaskua.

Toiminnolla voi myös muuttaa manuaalisesti vähintään yhden nimikkeen kustannuksia. Tämä on kätevää esimerkiksi silloin, kun tiedät, että nimikkeen kustannukset ovat muuttuneet jonkin muun syyn kuin nimiketapahtuman vuoksi.

Nimikkeen kustannuksia muutetaan FIFO- tai Keskiarvo-arvostusmenetelmällä ohjatussa **Määritä oma yritys** -määrityksessä tai nimikkeen kortin **Arvostusmenetelmä**-kentässä tehdyn valinnan mukaan. Lisätietoja on ohjeaiheessa [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

Jos käytössä on FIFO-arvostusmenetelmä, nimikkeen yksikkökustannus on nimikkeen vastaanoton todellinen arvo. Varastonarvostuksessa käytetään oletusta, että ensin varastoon sijoitetut nimikkeet myydään ensin.

Jos käytät Keskiarvo-arvostusmenetelmää, nimikkeen yksikkökustannus lasketaan kussakin vaiheessa keskimääräisenä yksikkökustannuksena oston jälkeen. Varastonarvostus olettaa, että kaikki vaihto-omaisuus myydään samanaikaisesti. Jos nimike käyttää tätä arvostusmenetelmää, voit tarkastella sitä tapahtumahistoriaa, josta keskimääräinen kustannus lasketaan, valitsemalla nimikkeen kortissa **Yksikkökustannus**-kentän.

Kustannusten muuttamistoiminto käsittelee vain arvotapahtumia, joita ei ole vielä muutettu. Jos toiminto kohtaa tilanteen, jossa muutetut saapuvat kustannukset on siirrettävä niihin liittyviin lähteviin tapahtumiin, luodaan uusia muutosarvotapahtumia, jotka perustuvat alkuperäisten arvotapahtumien tietoihin, mutta sisältävät muutossumman. Kustannusten muuttamistoiminto käyttää muutostapahtumassa alkuperäisen arvotapahtuman kirjauspäivämäärää, ellei päivämäärä ole suljetulla varastokaudella. Siinä tapauksessa sovellus käyttää seuraavan avoimen varastokauden aloituspäivämäärää. Jos varastokausia ei käytetä, **Pääkirjanpidon asetukset** -sivun **Ensimm. sallittu kirjauspvm** -kentässä oleva päivämäärä määrittää, milloin muutostapahtuma kirjataan.

## <a name="to-adjust-item-costs-manually"></a>Nimikekustannusten muokkaaminen manuaalisesti
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muuta kust. - Nimiketapahtumat** ja valitse sitten vastaava linkki.
2. Määritä **Muuta kustannuksia - Nimiketapahtumat** -sivulla nimikkeet, joiden kustannuksia muutetaan.
3. Valitse **OK**-painike.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a>Yleisten muutosten tekeminen välittömään yksikkökustannukseen
Jos välitöntä yksikkökustannusta on muutettava useissa nimikkeissä, voit käyttää **Muuta nimikekustannuksia tai -hintoja** -eräajoa.  

 Eräajo muuttaa nimikekortin **Yksikköhinta**-kentän sisällön. Eräajo muuttaa kentän sisällön samalla tavalla kaikille nimikkeille tai valituille nimikkeille. Eräajo kertoo kentässä olevan arvon määrittämälläsi muutoskertoimella.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Muuta nimikekustannuksia tai -hintoja** ja valitse sitten vastaava linkki.  
2. Määritä **Muuta kenttää** -kentässä muutettava nimikkeen tai varastointiyksikön kortin kenttä.  
3. Määritä **Muutoskerroin**-kentässä kerroin, jonka mukaan arvoa muutetaan. Syötä esimerkiksi **1,5**, kun haluat suurentaa arvoa 50 %:lla.  
4. Määritä **Nimike**-pikavälilehdessä määritettävät suodattimet, kuten se, mitä nimikkeitä eräajossa käsitellään.  
5. Valitse **OK**-painike.  

## <a name="understanding-unit-cost-calculation"></a>Tietoja yksikkökustannuksen laskennasta
Perussäännön mukaan nimikekortin **Yksikkökustannus**-kentässä olevan arvon perustana on vakiokustannus niiden nimikkeiden osalta, joilla on vakioarvostusmenetelmä. Niiden nimikkeiden osalta, joilla on jokin muista arvostusmenetelmistä, arvon perustana on varastosaldo (laskutetut kustannukset ja oletetut kustannukset) jaettuna saatavilla olevalla määrällä.  

 Se, miten **Arvostusmenetelmä**-kentän sisältö vaikuttaa myyntien ja ostojen yksikkökustannuksen laskentaan, kuvataan yksityiskohtaisemmin seuraavissa luvuissa.  

## <a name="unit-cost-calculation-for-purchases"></a>Ostojen yksikkökustannuksen laskenta  
 Aina kun ostat nimikkeitä, nimikekortin **Viimeinen välitön kustannus** -kentän arvo kopioidaan ostorivin **Välitön yksikkökustannus** -kenttään tai nimikepäiväkirjan rivin Yksikkösumma-riville.  

 Se, mitä valitset **Kustannustapa**-kentässä vaikuttaa siihen, miten [!INCLUDE[prod_short](includes/prod_short.md)] laskee **Yksikkökustannus**-kentän sisällön riveillä.  

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Kustannusmenetelmät FIFO, LIFO, Spesifi tai Keskimäärä  
 [!INCLUDE[prod_short](includes/prod_short.md)] laskee ostorivin **Yksikkökustannus PVA** -kentän sisällön tai nimikepäiväkirjan rivin **Yksikkökustannus**-kentän sisällön seuraavan laskukaavan mukaan:  

 "Yksikkökustannus (PVA) = (Välitön yksikkökustannus - (Alennussumma / Määrä)) * (1 + Välillinen kustannus-% / 100) + Yleiskustannus  

### <a name="costing-method-standard"></a>Arvostusmenetelmä Vakio  
 Järjestelmä syöttää **yksikkökustannus (PVA)** -kentän ostoriville sekä **yksikkökustannus** -kentän nimikepäiväkirjalle kopioimalla arvon nimikekortin **yksikkökustannus** -kentästä. Jos arvostustapa on vakio perustuu kustannus aina vakiokustannukseen.  

 Kun kirjaat oston, ohjelma kopioi yksikkökustannuksen ostoriviltä tai nimikepäiväkirjan riviltä oston nimikelaskutapahtumaan, ja sen voi nähdä nimikkeen tapahtumaluettelossa.  

### <a name="all-costing-methods"></a>Kaikki arvostusmenetelmät  
 Lähdeasiakirjan rivin yksikkökustannusta käytetään kyseiseen nimiketapahtumaan liittyvän **Kustannussumma todellinen** -kentän (tai tarpeen mukaan **Kustannussumma oletettu** -kentän) sisällön laskennassa huolimatta siitä, mikä nimikkeen arvostusmenetelmä on.  

## <a name="unit-cost-calculation-for-sales"></a>Myyntien yksikkökustannuksen laskenta  
 Kun myyt nimikkeitä, ohjelma kopioi yksikkökustannuksen nimikekortin Yksikkökustannus-kentästä myyntiriville tai nimikepäiväkirjan riville.  

 Kirjauksen yhteydessä ohjelma kopioi yksikkökustannuksen myyntilaskun nimiketapahtumaan, ja se näkyy nimikkeen tapahtumaluettelossa. [!INCLUDE[prod_short](includes/prod_short.md)] käyttää lähdeasiakirjan rivin yksikkökustannusta kyseiseen nimiketapahtumaan liittyvän arvotapahtuman **Kustannussumma todellinen** -kentän (tai tarpeen mukaan **Kustannussumma oletettu** -kentän) sisällön laskennassa.  

## <a name="see-also"></a>Katso myös
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Varasto](inventory-manage-inventory.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]