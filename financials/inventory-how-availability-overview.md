---
title: 'Toimintaohje: Saatavuuden yleiskuva| Microsoft Docs'
description: "Artikkelissa käsitellään, miten nimikkeiden saatavuutta voi tarkastella eri sijainneissa myynti- tai ostotapahtumien tai ajanjakson mukaan tai sen mukaan, mikä on nimikkeen sijainti kokoonpanon tuoterakenteessa."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 03/28/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 47071e5e325de8a31663b8d5a59d1ce93e5d0111
ms.contentlocale: fi-fi
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-get-an-availability-overview"></a>Toimintaohje: Saatavuuden yleiskuva
Voit saada, liiketoimintaan liittyvän tehtävän kontekstissa, lisätietoja milloin ja mistä nimike on saatavissa, esimerkiksi kun kerrot asiakkaalle toimitusaikataulua.

Voit tarkastella kaikkien nimikkeiden saatavuutta sijainneittain sekä kunkin nimikkeen saatavuutta tapahtuman, jakson tai sijainnin perusteella. Tapahtuma on mikä tahansa suunniteltu nimiketapahtuma, kuten myyntitoimitus tai saapuvan siirron vastaanotto.

**Huomautus**: Sijaintiin perustuvat saatavuusnäkymät vaativat, että ylläpidät varastoa useammassa sijainnissa. Lisätietoja on kohdassa [Toimintaohje: Sijaintien määrittäminen](inventory-how-setup-locations.md).

[[!INCLUDE[d365fin](includes/d365fin_md.md)]ia käytettäessä saatavuusluvut näytetään kahdessa eri kentässä, ja kullakin on eri määritelmä:

* **Varastosaldo** -kentässä näytetään päivän todellinen saldo kirjattujen nimiketapahtumien perusteella.
* **Oletettu saatavilla oleva saldo** -kentän arvo on laskennallinen, ja se esittää varastosaldon, johon on lisätty suunnitellut vastaanotot ja josta on vähennetty bruttotarpeet. ([[!INCLUDE[d365fin](includes/d365fin_md.md)]ia käytettäessä suunnitellut vastaanotot sisältävät ostotilauksilla ja saapuvilla siirtotilauksilla olevat määrät. Bruttotarpeisiin sisältyvät myyntitilauksilla ja lähtevillä siirtotilauksilla olevat määrät).

**Vihje**: Oletettu saatavilla oleva saldo soveltuu erityisesti **Nimikk. saatavuus jaksoittain** ja **Nimikkeen saatavuus tapahtumittain** -ikkunoiden tarkasteluun, koska ne sisältävät päivämäärädimension.  

**Huomautus**: seuraavissa ohjeissa kuvataan, miten saatavuuden lisätietoja tarkastellaan nimikeluettelosta ja -kortilta. Tietoja voi käyttää myös myyntiasiakirjan riveiltä, jotka koskevat ko. nimikettä. Lisätietoja on kohdassa [Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Voit tarkastella nimikkeen saatavuutta sen vastaanotto- tai toimituspäivän mukaan.
Voit tarkastella nimikkeen saatavuutta **Saatavuus tapahtumittain** -ikkunassa näytettävien suunniteltujen nimiketapahtumien perusteella.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jonka saatavuuden haluat näyttää.
3. Valitse **Nimikkeen saatavuus** -toiminto ja sitten **Tapahtuma**-toiminto.

    **Nimikkeen saatavuus tapahtumittain** -ikkunassa näkyy, miten nimikkeen varastosaldo kehittyy ajan kuluessa suunniteltujen toimitus- ja vastaanottotapahtumien mukaisesti. Ikkunassa on tiivistetty näkymä, joka näyttää kertyneitä tietoja yhdellä rivillä kutakin sellaista aikaväliä kohden, jolloin varastosaldot muuttuvat. Aikavälit, jolloin tapahtuneita tapahtumia ei näytetä. Voit laajentaa kunkin rivin näyttämään tietoja tapahtumasta tai tapahtumista, jotka aiheuttivat kertyneen määrän rivillä.
4. Valitse arvo **Oletettu saatavilla oleva saldo** -kentässä tarkastellaksesi nimiketapahtumia tai avataksesi asiakirjoja, jotka muodostavat arvon.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Nimikkeen saatavuuden tarkastelu eri jaksoissa
Nimikkeen saatavuutta määritettynä aikajaksolla voit tarkastella **Nimikk. saatavuus jaksoittain** -ikkunassa.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jonka saatavuuden haluat näyttää.
3. Valitse **Nimikkeen saatavuus** -toiminto ja sitten **Jakso**-toiminto.

    **Nimikkeen saatavuus jaksoittain** -ikkunassa näkyy, kuinka nimikkeen varastomäärä kehittyy valitsemallasi aikajaksolla, kuten Päivä, Viikko tai Neljännes.
4. Valitse arvo **Oletettu saatavilla oleva saldo** -kentässä tarkastellaksesi nimiketapahtumia tai avataksesi asiakirjoja, jotka muodostavat arvon.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Nimikkeen saatavuuden tarkastelu kaikissa sen varastointipaikoissa
Voit tarkastella nimikkeen saatavuutta kaikissa paikoissa, jossa sitä varastoidaan **Nimikkeen saatavuus sijainnin mukaan** -ikkunassa.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jonka saatavuuden haluat näyttää.
3. Valitse **Nimikkeen saatavuus** -toiminto ja sitten **Sijainti**-toiminto.

    **Nimikkeen saatavuus sijainnin mukaan** -ikkunassa näkyy, kuinka nimikkeen varastosaldo kehittyy jatkossa, kullekin varastosijainnille eriteltynä.
4. Valitse arvo **Varastosaldo** -kentässä tarkastellaksesi nimiketapahtumia tai avataksesi asiakirjoja, jotka muodostavat arvon.
5. Valitse arvo **Oletettu saatavilla oleva saldo** -kentässä tarkastellaksesi nimiketapahtumia tai avataksesi asiakirjoja, jotka muodostavat arvon.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Kaikkien nimikkeiden saatavuuden tarkastelu kaikissa niiden varastointipaikoissa
Voit tarkastella kaikkien nimikkeidesi saatavuutta kaikissa sijainneissa **Nimikkeet sijainneittain** -ikkunassa.

1. Valitse oikeassa yläkulmassa **Etsi sivua tai raporttia** -kuvake ![Etsi sivua tai raporttia](media/ui-search/search_small.png "Etsi sivua tai raporttia -kuvake"), kirjoita **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Valitse **Nimikkeet sijainneittain** -toiminto.

    **Nimikkeet sijainneittain** -ikkunassa näyttää kussakin sijainnissa olevan saldon nimikkeelle.
3. Valitse arvo **Varastosaldo** -kentässä tarkastellaksesi nimiketapahtumia tai avataksesi asiakirjoja, jotka muodostavat arvon.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-boms"></a>Nimikkeen saatavuuden tarkastelu sen mukaan, miten sitä käytetään kokoonpanon tuoterakenteessa
Jos nimike on kokoonpanon tuoterakenteessa joko päänimikkeenä tai osana, voit tarkastella **Nimikkeen saatavuus tuoterakennetason mukaan** -ikkunassa, kuinka monta sen yksikköä tarvitaan. Ikkunassa näkee, kuinka monta pääyksikköä voit tehdä alla olevien rivien alinimikkeiden saatavuuteen perustuen. Kaikki nimikkeet, joilla on kokoonpanon tuoterakenne, näkyvät ikkunassa tiivistettävänä rivinä. Voit laajentaa tämän rivin pohjana sen alla oleville osille ja alemman tason osakokoonpanoille niiden omien tuoterakenteiden kanssa.

Ikkunan avulla voit nähdä, voitko täyttää nimikkeen myyntitilauksen tiettynä päivämääränä tutkimalla sen nykyisen saatavuuden ja määrien kanssa, jotka sen osat voi toimittaa. Voit tunnistaa ikkunan avulla myös pullonkaulat liittyvissä kokoonpanon tuoterakenteissa.

Seuraavat kentät määrittävät saatavuusluvut sekä päänimikkeiden että alinimikkeiden ikkunan kullakin rivillä. Voit luvata näiden lukujen avulla, kuinka monta pääyksikköä voit toimittaa, jos aloitat liittyvän kokoonpanoprosessin.

|Kenttä|Kuvaus|
|------|-----------|
|**Kykenee valmistamaan päänimikettä**|Näyttää, kuinka monta yksikköä päänimikkeen osakokoonpanoa voi tehdä. Kenttä määrittää, kuinka monta pääyksikköä voidaan koota välittömästi. Arvo perustuu rivillä olevan nimikkeen saatavuuteen.|
|**Kykenee valmistamaan tärkeintä nimikettä**|Näyttää, kuinka monta yksikköä päänimikettä voi tehdä. Kenttä määrittää, kuinka monta yksikköä tuoterakenteen ylärivin nimikettä voidaan koota. Arvo perustuu rivillä olevan nimikkeen saatavuuteen.|

**Nimikkeen saatavuus tuoterakennetason mukaan** -ikkunassa on sen kortin tai asiakirjarivin nimikkeen tietoja, jonka ikkuna avattiin. Kohde näkyy aina ylimmällä rivillä. Voit tarkastella muiden nimikkeiden tai kaikkien nimikkeiden tietoja vaihtamalla arvoa **Nimikesuodatus**-kentässä.

**Huomautus:** Oletusarvoisesti rivien luvut näyttävät kaikkien nimikkeiden kokonaissaatavuuden ylimmän nimikkeen alla. Nämä luvut näkyvät **Saatavilla oleva määrä** -kentässä ja kohdistus on ylimmässä nimikkeessä. Tiedot siitä, miten monta osakokoonpanoa voidaan tehdä, voivat olla virheellisiä. Jotta saisit todellista tietoa siitä, kuinka monta näkyvää osakokoonpanoa voit tehdä, sinun on poistettava **Näytä kokonaissaatavuus** -valintaruudun valinta ja tarkistettava sitten **Kykenee valmistamaan päänimikettä** -kentän luku.

**Pullonkaula**-kenttä määrittää, mikä tuoterakenteen nimike estää suuremman valmistusmäärän kuin **Kykenee valmistamaan tärkeintä nimikettä** -kentässä näkyvä määrä. Pullonkaulanimike voi olla esimerkiksi ostettu osa, jonka oletettu vastaanottopäivämäärä on liian myöhään, jotta päänimekettä voitaisiin valmistaa lisää **Tarvitaan päivämäärän mennessä** -kentässä olevaan päivämäärään mennessä.

## <a name="see-also"></a>Katso myös
[Varaston hallinta](inventory-manage-inventory.md)  
[Toimintaohje: Tuoterakenteen käyttäminen](inventory-how-work-BOMs.md)    
[Toimintaohje: Sijaintien määrittäminen](inventory-how-setup-locations.md)  
[Toimintaohje: Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)  
[Toimintaohje: Tuotteiden myyminen](sales-how-sell-products.md)      
[Toimitusketju](madeira-supply-chain.md)  
[Financialsin käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)

