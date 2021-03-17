---
title: Varaston kustannusten kirjaaminen pääkirjanpitoon| Microsoft Docs
description: Kirjanpitojaksojen lopussa (kuukausittain, vuosittain tai muulla aikavälillä) suoritetaan joukko kustannustenhallinta- ja auditointitehtäviä, joiden avulla saadaan oikea ja saldoltaan täsmällinen varaston arvo raportoitavaksi taloushallinto-osastolle. Tilintarkastajat ja kustannusten seurantahenkilöstö vastaavat näistä liiketoiminnan kannalta kriittisistä tehtävistä, ja yksittäisiä nimikkeen arvotapahtumia erityisille kirjanpitotileille siirtävän kirjausrutiinin lisäksi heidän käytettävissään on useita raportteja, jäljitystoimintoja ja erityinen täsmäytystyökalu.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a96a4eebc97ecefc43487af3e31fc3216724c527
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387347"
---
# <a name="reconcile-inventory-costs-with-the-general-ledger"></a>Varaston kustannusten täsmäyttäminen pääkirjanpitoon
Kun kirjaat varastotapahtumia, kuten myyntitoimituksia, ostolaskuja tai varaston muutoksia, muuttuneet nimikekustannukset kirjataan niiden arvotapahtumiin. Jotta varastoarvon muutos päivittyisi talouskirjoihin, varastokustannukset kirjataan automaattisesti pääkirjanpidon liittyviin varastotileihin. Ohjelma kirjaa jokaista itse kirjaamaasi varastotapahtumaa kohti sopivan arvon varastotilille, muutostilille ja myytyjen tuotteiden kustannusten tilille pääkirjanpidossa.

**Varastonhallinnan asetukset** -sivun **Automaattinen kustann. kirjaus** -kenttä määrittää automaattisen kustannusten kirjauksen.

Vaikka kustannukset kirjattaisiin automaattisesti pääkirjanpitoon, on tarpeen varmistaa, että tavaroiden kustannukset välitetään liitetään lähtevälle tapahtumalle. Tämä on erityisen tärkeää, kun myyt tavaroita ennen näiden tavaroiden oston laskutusta. Tätä kutsutaan kustannusmuutokseksi. Nimikekustannukset muutetaan automaattisesti, kun kirjaat nimiketapahtumia, mutta voit muuttaa niitä myös manuaalisesti. Lisätietoja on kohdassa [Nimikekustannuksien muuttaminen](inventory-how-adjust-item-costs.md).

## <a name="to-post-inventory-costs-manually"></a>Varaston kustannusten kirjaus manuaalisesti
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjaa varaston kust. KP:oon** ja valitse sitten liittyvä linkki.
2. Kirjaa varaston kustannukset pääkirjanpitoon suorittamalla eräajo. Ohjelma luo tämän eräajon aikana KP-tapahtumia arvotapahtumien perusteella. Voit kirjata tapahtumat niin, että ne lasketaan yhteen kirjausryhmittäin.

> [!NOTE]  
> Ohjelmassa saattaa tapahtua virhe tämän eräajon aikana, jos asetuksissa on puutteita tai dimension asetus on yhteensopimaton. Jos dimension asetuksissa havaitaan virheitä eräajon aikana, eräajo ohittaa nämä virheet ja käyttää arvotapahtuman dimensioita. Muiden virheiden kohdalla eräajo jättää arvotapahtumat kirjaamatta ja listaa ne raportin lopussa osassa “Ohitetut tapahtumat”. Voit kirjata nämä tapahtumat korjattuasi virheet.

Saat virheluettelon näkyviin ennen kirjauksen eräajon ajoa, kun suoritat **Kirjaa varaston kustannukset kirjanpitoon - Testaa** -raportin. Testiraportissa luetteloidaan kaikki ohjelman virheet testikirjauksen aikana. Voit sitten korjata nämä virheet ja suorittaa varaston kustannusten kirjauksen eräajon niin, että tapahtumia ei ohiteta.

Jos haluat yleiskuvauksen niistä arvoista, jotka pääkirjanpitoon voi kirjata ilman kirjauksen suoritusta, voit suorittaa **Kirjaa varaston kustannus KP:oon** -eräajon. Arvoja ei tällöin oikeasti kirjata pääkirjanpitoon. Voit tehdä tämän poistamalla valintaruudun valinnan **Kirjaa** -kentässä pyyntösivulla. Näin eräajoa suoritettaessa tuotetaan raportti, jossa on arvot, jotka ovat valmiita kirjattaviksi kirjanpitoon, mutta joita ei ole kirjattu.

## <a name="to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger"></a>Varastotapahtumien ja pääkirjanpidon välisen täsmäytyksen tarkistaminen
**Varasto - Kirjanpidon täsmäytys** -sivun sisältö:

- osoittaa täsmäytyserot vertaamalla kirjanpidon ja varastokirjausten (arvotapahtumat) tallennuksia
- näyttää varastokirjausten arvotapahtumien täsmäyttämättömät kustannussummat siten, että ne näyttävät olevan linkitetty vastaaviin varastoon liittyviin kirjanpidon tileihin, ja vertaa näitä summia kirjanpidossa samoille tileille tallennettuihin kokonaissummiin
- Vastaa kaksinkertaista KP:n tapahtumarakennetta esittämällä tiedot visuaalisesti sellaisenaan. Esimerkiksi myytyjen tuotteiden kustannusten tapahtumalla on vastaava inventointitapahtuma.
- antaa käyttäjille mahdollisuuden siirtyä tapahtumiin, joista kustannussummat muodostuvat, ja tarkastella niitä
- sisältää suodattimia, joiden avulla analyysiä voi rajata päivämäärän, nimikkeen ja sijainnin mukaan
- selittää täsmäytyserojen syyt tietosanomissa.


Ruudukossa äärimmäisenä vasemmalla olevassa **Nimi**-sarakkeessa on erilaiset varastoon liittyvät KP-tilityypit.

**Varasto**-, **Varasto (väliaikainen)**- ja **KET-varasto**-sarakkeissa on kunkin KP-tilityypin laskutettujen, laskuttamattomien ja keskeneräisten töiden kokonaissummat. Ne lasketaan arvotapahtumista eli summat määritetään niille KP-tilityypeille, joille ne päätyvät kirjanpitoon kirjauksen jälkeen.

**Yhteensä**-sarakkeessa on kolmen varastosarakkeen arvotapahtumien summien kokonaissumma (lihavoituna).

**KP yhteensä** -sarakkeessa on jokaisen kirjanpidossa olevan KP-tilityypin summat (lihavoituna). Summat on laskettu KP-tapahtumista eli ne edustavat kirjanpitoon jo kirjattuja varaston kustannuksia.

**Ero**-sarakkeessa on **KP yhteensä**- ja **Yhteensä**-kenttien summien ero.

**Varasto - Kirjanpidon täsmäytys** -sivun yläosassa voit asettaa suodattimia, jotka rajaavat esimerkiksi haettavien tietojen ajanjaksoa.

Jos valitset **Näytä varoitus** -valintaruudun ja jos varaston kokonaissummien ja pääkirjanpidon kokonaissummien välillä on eroja, sovellus tuo ruudukon **Varoitus**-kenttään sanomia, joissa on erojen selitykset. Jos napsautat Varoitus-kenttää, sovellus antaa lisätietoja varoituksen merkityksestä.

Kun olet määrittänyt kaikki tarvittavat suodattimet, valitse **Näytä matriisi** -toiminto. Ohjelma laskee tiedot ja tuo näyttöön matriisisivun.

Ruudukon äärimmäisenä vasemmalla olevassa sarakkeessa näkyvät varastoon liittyvät pääkirjanpidon tilityypit. Seuraavina ruudukossa näkyvät näiden tilityyppien laskutetut, laskuttamattomat (väliaikaiset) ja KET-varaston kokonaissummat. Nämä kokonaissummat arvotapahtumien perusteella.

Seuraavissa sarakkeissa näkyvät samojen tilityyppien kokonaissummat pääkirjanpidon tapahtumista laskettuina.

Valitsemalla kokonaissummakentän summan voit tarkastella varastoraportin tapahtumia, joiden perusteella kokonaissummat on laskettu. Varaston kokonaissummien osalta varastoraportin tapahtumat ovat nimikkeiden arvotapahtumien summia. Pääkirjanpidon kokonaissummien osalta varastoraportin tapahtumat ovat pääkirjanpidon tapahtumien summia.

## <a name="reporting-costs-and-reconciling-with-the-general-ledger"></a>Kustannukset raportointi ja täsmäyttäminen pääkirjanpidon kanssa
Muut raportit, jäljitysfunktiot ja erityinen täsmäytystyökalu ovat niiden tilintarkastajien tai tarkistajien käytettävissä, jotka vastaavat oikeellisen ja tasapainotetun varastoarvon raportoinnista talousosastolle.

Niitä kuvaillaan seuraavassa taulukossa.    

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Valittujen nimikkeiden varaston arvon tarkastelu. Tietoihin sisältyvät varaston lisäysten ja vähennysten määrät ja arvot valittuna aikana.|**Varaston arvostus** -raportti|  
|Valittujen KET-varaston tuotantotilausten varaston arvon tarkastelu. Tietoihin sisältyvät kulutuksen määrät ja arvot, kapasiteetin käyttö sekä meneillään olevien tuotantotilausten tuotto.|**Varaston arvostus - KET** -raportti|  
|Valittujen nimikkeiden varaston arvon tarkastelu, mukaan lukien todellinen ja oletettu kustannus määritettynä päivämääränä.|**Varaston arvostus - Kust. määr.** -raportti|  
|Raportin käyttäminen kustannusvarianssien analysoimiseksi tai myytyjen tuotteiden kustannusosuuksien selvittämiseksi.|**Kustannusjakaumien erittely** -raportti|  

## <a name="see-also"></a>Katso myös  
[Varaston kustannusten hallinta](finance-manage-inventory-costs.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)    
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]