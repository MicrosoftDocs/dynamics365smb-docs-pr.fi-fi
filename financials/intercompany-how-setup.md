---
title: "Konsernitapahtuman kirjauksen määrittäminen| Microsoft Docs"
description: "Luo konsernitoimittajat ja -asiakkaat konsernikumppaneina ja määritä konsernin tilikartta."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/20/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cce1f5c30b758155056b00e933c9f6cabfd9f1f4
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-intercompany"></a>Toimintaohje: Konsernin määrittäminen
Jos haluat lähettää yhdestä yrityksestä tapahtuman (kuten myyntipäiväkirjan rivin), jolle luodaan automaattisesti vastaava tapahtuma (kuten ostopäiväkirjan rivi) kumppaniyrityksessä, yrityksillä on oltava yhteinen tilikartta ja dimensiojoukko konsernin tapahtumia varten. Konsernin tilikartta voi olla esimerkiksi pääyrityksen tilikartan yksinkertaistettu versio. Jokainen yritys määrittää oman tilikarttansa vastaavuuden konsernin jaetun tilikartan kanssa ja myös omien dimensioidensa vastaavuuden konsernin dimensioiden kanssa.  

Jokaiselle kumppaniyritykselle on myös määritettävä konsernikumppanin koodi, jonka kaikki yritykset hyväksyvät, ja määrittää se sitten asiakas- ja toimittajakortteihin täyttämällä **Konsernikumppanin koodi** -kenttä.  

Jos luot tai vastaanotat konsernin rivejä, joissa on nimikkeitä, voit joko käyttää omia nimikenumeroja tai määrittää kumppanin nimikenumerot kullekin soveltuvalle nimikkeelle. Nimikenumeron voi määrittää joko nimikkeen kortin **Toimittajan nimikenro**- tai **Yleinen nimikenro** -kenttään. Voit käyttää myös **Nimikeviittaus**-toimintoa: Voit linkittää nimikenumerot nimikkeiden konsernikumppanien kuvauksiin avaamalla kunkin nimikkeen kortin, valitsemalla **Viittaukset**-toiminnon ja määrittämällä sitten nimikkeen ja konsernikumppanin kuvausten väliset viittaukset.  

Jos suorittamiisi konsernin myyntitapahtumiin sisältyy resursseja, täytä kunkin asiaankuuluvan resurssin kortin **Kons.kump. oston KP-tilinro** -kenttä. Tämä on konsernin kirjanpitotilin numero, jolle tämän resurssin summa kirjataan kumppaniyrityksessä. Lisätietoja on ohjeaiheessa  

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Konsernitapahtumien yritysten määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Yrityksen tiedot** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä **Yrityksen tiedot** -ikkunassa **Konsernikumppanin koodi**, **Konsernin Saapuneet-kansion tyyppi**- ja **Konsernin Saapuneet-kansion tiedot** -kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>Konsernikumppanien määrittäminen
1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, kirjoita **Konsernikumppanit** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Uusi**-toiminto.
3. Täytä tarvittavat kentät **Konsernikumppanit**-ikkunassa.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Konsernin toimittajien ja asiakkaiden määrittäminen
1. Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, syötä **Toimittajat** ja valitse sitten aiheeseen liittyvä linkki.
2. Voit käyttää toimittajaa myös **Konsernikumppani**-ikkunan **Toimittajan nro** -kentästä.
3. Avaa sellaisen toimittajan kortti, joka on konsernikumppani. Lisätietoja on kohdassa [Toimintaohje: Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md).
4. Valitse **Konsernikumppanin koodi** -kentässä sopiva konsernikumppanin koodi.
5. Toista vaiheet 1–4 asiakkaiden kohdalla.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Konsernin tilikartan määrittäminen
Konsernikumppanien väliset tapahtumat ovat mahdollisia vasta, kun konsernikumppanit ovat sopineet yhteisestä tilikartasta. Käyttäjän täytyy sopia konsernikumppanien kanssa tilinumeroista, joita kaikki osapuolet käyttävät konsernin tapahtumia luotaessa. Konsernin emoyritys voi esimerkiksi luoda yksinkertaistetun version omasta tilikartastaan, viedä kyseisen tilikartan tietokannasta XML-tiedostoon ja jakaa sen muille konsernin yrityksille.  

Jos oma yritys on emoyhtiö ja sen tarkoitus määrittää konsernin viitekehyksenä käyttämä konsernin tilikartta, noudata kohdan Konsernin tilikartan määrittäminen ohjeita.  

Jos oma yritys on tytäryhtiö ja olet vastaanottanut konsernin yleisen tilikartan XML-tiedostona, noudata kohdan Konsernin tilikartan tuominen ohjeita.  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Määrittävän konsernin tilikartan määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake -kuvake"), kirjoita **Konsernin tilikartta** ja valitse sitten aiheeseen liittyvä linkki.
2. Anna **Konsernin tilikartta** -ikkunassa kukin tili ikkunan riville.  
3. Jos konsernin tilikartta on täsmälleen sama tai samankaltainen kuin varsinainen tilikartta, voit täyttää ikkunan automaattisesti valitsemalla **Kopioi tilakartasta** -toiminto. Voit muokata uusia rivejä tarvittaessa.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Konsernin tilikartan vieminen
Jotta konsernikumppanit voisivat tuoda määrittävän tilikartan, se on vietävä tiedostoon.      
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake -kuvake"), kirjoita **Konsernin tilikartta** ja valitse sitten aiheeseen liittyvä linkki.
2. - **Konsernin Tilikartta** -ikkunassa valita **Vie** toiminto, ja valitse sitten **tallentaa** painike.
3. Määritä tiedostonimi sekä sijainti, johon haluat tallentaa XML-tiedoston, ja valitse sitten **Tallenna**-painike.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Voit tuoda konsernin tilikartan seuraavasti  
Kun määrittävällä konsernin tilikartalla on tiedosto, konsernikumppani voi tuoda sen ja varmistaa näin, että käytettävät tilit ovat samoja.  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake -kuvake"), kirjoita **Konsernin tilikartta** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Konsernin tilikartta** -ikkunassa **Tuo**-toiminto.  
3. Valitse XML-tiedoston nimi sekä sijainti ja valitse sitten **Avaa**.  

**Konsernin tilikartta** -ikkunaan on täytetty uudet tai muokatut KP-tilin rivit tiedostossa olevan konsernin tilikartan mukaisesti. Ikkunassa olevat aiemmin luodut liittymättömät rivit eivät muutu.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Voit linkittää konsernin tilikartan yrityksen tilikarttaan seuraavasti  
Kun olet määrittänyt tai tuonut konsernin tilikartan, jonka käytöstä on sovittu konsernikumppanien kesken, kukin konsernin KP-tili on liitettävä oman yrityksen KP-tiliin. Määritä **Konsernin tilikartta** -ikkunassa, kuinka saapuvien tapahtumien konsernin KP-tilit muunnetaan yrityksen tilikartan KP-tileiksi.

Jos konsernin tilikartan tileillä on samoja tilinumeroita kuin tilikartan vastaavilla tileillä, tilit voi linkittää automaattisesti.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake -kuvake"), kirjoita **Konsernin tilikartta** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse ensin automaattisesti linkitettävät rivit ja sitten **Liitä tiliin, jolla on sama nro** -toiminto.  
3. Täytä kunkin sellaisen konsernin kirjanpitotilin **Liitä konsernin KP-tilinumeroon** -kenttä, jota ei linkitetty automaattisesti.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Oletuskonsernikumppanin kirjanpitotilien määrittäminen  
Kun luot konsernin myynti- tai ostorivin tapahtumana lähetettäväksi, annat konsernin tilikartasta tilin, johon summa oletusarvoisesti kirjataan kumppaniyrityksessä. Voit määrittää **Tilikartta**-ikkunassa oletuskonsernikumppanin KP-tilin sellaisia tilejä varten, joita käytät usein lähtevissä konsernin myynti- tai ostoriveissä. Voit määrittää esimerkiksi myyntisaamistilejä varten konsernin tilikartasta vastaavat ostovelkatilit.  

Kun lisäät kirjanpitotilin **Vastatilin nro** -kenttään sille konsernin riville, jonka **Tilityyppi**-kentässä lukee **Konsernikumppani**, **Konsernikumppanin KP-tili** -kenttä täytetään automaattisesti.  

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.  
2. Anna konsernitapahtumissa käytettävän KP-tilin rivin **Konsernikumppanin KP-oletustili** -kentässä konsernin kirjanpitotili, jonka kumppani kirjaa kun kirjaat KP-tilin riville.  
3. Toista vaihe 3 kaikkien sellaisten tilien osalta, joita lisäät usein konsernin päiväkirjan tai asiakirjan riville **Vastatilin nro** -kenttään.

## <a name="to-set-up-intercompany-dimensions"></a>Konsernin dimensioiden määrittäminen
Jos oman yrityksen ja konsernikumppanien välillä halutaan siirtää tapahtumia, joihin on linkitetty dimensioita, kaikkien on hyväksyttävä käytettävät dimensiot. Konsernin emoyritys voi esimerkiksi luoda yksinkertaistetun version omasta dimensiojoukostaan, viedä kyseiset konsernin dimensiot XML-tiedostoon ja jakaa tiedoston muille konsernin yrityksille. Jokainen tytäryhtiö tuo tämän jälkeen XML-tiedoston **Konsernin dimensiot** -ikkunaan ja linkittää konsernin dimensiot oman **Dimensiot**-taulukon dimensioihin.  

Jos oma yritys on emoyhtiö ja sen on tarkoitus määrittää konsernin viitekehyksenä käyttämä konsernin dimensiojoukko, noudata kohdan Konsernin dimensioiden määrittäminen ohjeita.

Jos oma yritys on tytäryhtiö ja on vastaanottanut konsernin viitekehyksenä käytettävät konsernin dimensiot, noudata kohdan Konsernin dimensioiden tuominen ohjeita.

### <a name="to-define-the-intercompany-dimensions"></a>Konsernin dimensioiden määrittäminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Konsernin dimensiot** ja valitse sitten aiheeseen liittyvä linkki.  
2. Anna **Konsernin dimensiot** -ikkunassa kullekin dimensiolle rivi.

    Jos konsernin dimensiot muistuttavat läheisesti yrityksen omia dimensioita, voit täyttää ikkunan automaattisesti valitsemalla **Kopioi dimensioista** -toiminnon. Rivejä voi tämän jälkeen muokata.  
3. Kun valitset **Vie**-toiminnon, voit viedä konsernin dimensiot XML-tiedostoon kumppaniyrityksille jaettavaksi.  
4. Määritä tiedostonimi sekä sijainti, johon haluat tallentaa XML-tiedoston, ja valitse sitten **Tallenna**-painike.  

### <a name="to-import-the-intercompany-dimensions"></a>Konsernin dimensioiden tuominen  
Kun määrittävällä konsernin dimensioilla on tiedosto, konsernikumppanit voivat tuoda sen ja varmistaa näin, että käytettävät dimensiot ovat samoja.  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Konsernin dimensiot** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Konsernin dimensiot** -ikkunassa **Tuo**-toiminto.  
3. Määritä XML-tiedoston nimi sekä sijainti ja valitse sitten **Avaa**.  

**Konsernin dimensiot**- ja **Konsernin dimensioarvot** -ikkunoiden rivit tuodaan.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Voit linkittää konsernin dimensiot oman yrityksen dimensioihin seuraavasti
Kun olet määrittänyt tai tuonut dimensiot, joiden käytöstä olette sopineet konsernikumppanien kesken, kukin konsernin dimensio on yhdistettävä oman yrityksen dimensioon ja päin vastoin. Määritä **Konsernin dimensio** -ikkunassa, kuinka saapuvien tapahtumien konsernin dimensiot muunnetaan yrityksen dimensioluettelon dimensioiksi. Voit määrittää **Dimensiot**-ikkunassa, kuinka yrityksen dimensiot muunnetaan konsernin dimensioiksi lähtevissä tapahtumissa.

Jos konsernin dimensioilla on samoja koodeja kuin yrityksen dimensioluettelon vastaavilla dimensioilla, voit määrittää ohjelman linkittämään dimensiot automaattisesti ja linkittää tilit sitten automaattisesti.

1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Konsernin dimensiot** ja valitse sitten aiheeseen liittyvä linkki.
2. Valitse **Konsernin dimensiot** -ikkunassa rivit, jotka haluat linkittää automaattisesti, ja valitse sitten **Liitä dimensioon, jolla on sama koodi** -toiminto.
3. Jos konsernin dimensiota ei linkitetä automaattisesti, täytä **Liitä dimensiokoodiin** -kenttä.
4. Valitse **Konsernin dimension arvot** -toiminto.
5. Täytä **Konsernin dimension arvot** -ikkunassa **Liitä kons. dim. arvokoodiin** -kenttä.

    Jatka dimensioiden linkittämistä konsernin dimensioihin vastaavasti.
6. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Dimensiot** ja valitse sitten aiheeseen liittyvä linkki.
7. Valitse **Dimensiot**-ikkunassa rivit, jotka haluat linkittää automaattisesti, ja valitse sitten **Liitä konsernin dimensioon, jolla on sama koodi** -toiminto.
8. Jos konsernin dimensiota ei linkitetä automaattisesti, täytä **Liitä konsernin dimensioarvon koodiin** -kenttä.
9. Valitse **Konsernin dimension arvot** -toiminto.
10. Täytä **Konsernin dimension arvot** -ikkunassa **Liitä kons. dim. arvokoodiin** -kenttä.

## <a name="see-also"></a>Katso myös
[Konsernitapahtumien hallinta](intercompany-manage.md)  
[Rahoitus](finance.md)  
[Rahoituksen määrittäminen](finance-setup-finance.md)  
[Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)

