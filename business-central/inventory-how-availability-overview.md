---
title: Saatavuuden yleiskuva
description: Saat tietoja nimikkeiden tai varaston saatavuudesta eri sijainneissa esimerkiksi myynti- tai ostotapahtumien tai ajanjakson mukaan.
documentationcenter: ''
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.search.form: 908, 909, 925, 926, 504, 501, 500, 499, 99000896, 342, 515, 5417, 5415, 5871, 5530, 492, 157, 5540, 5416, 5414, 1872, 1873, 99000902, 353, 491, 9231, 5390
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: d87f18b6af045e371cefe88ed35f62bc028fab2f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514983"
---
# <a name="view-the-availability-of-items"></a>Nimikkeiden saatavuuden tarkasteleminen
Voit saada, liiketoimintaan liittyvän tehtävän kontekstissa, lisätietoja milloin ja mistä nimike on saatavissa, esimerkiksi kun kerrot asiakkaalle toimitusaikataulua.

Voit tarkastella kaikkien nimikkeiden saatavuutta sijainneittain sekä kunkin nimikkeen saatavuutta tapahtuman tai jakson perusteella. Tapahtuma on mikä tahansa suunniteltu nimiketapahtuma, kuten myyntitoimitus tai saapuvan siirron vastaanotto.

> [!NOTE]  
>   Sijaintiin perustuvat saatavuusnäkymät edellyttävät, että varastoa pidetään useissa sijainneissa. Lisätietoja on kohdassa [Sijaintien määrittäminen](inventory-how-setup-locations.md).

Jos käytät varastointitoimintoa, saatavuus vaihtelee varastohuoneen kiintöiden mukaan, kun varastointitoimenpiteitä, kuten noutoja ja siirtoja tapahtuu ja silloin, kun varaston varausjärjestelmät luovat rajoitteita. Varsin monimutkainen algoritmi tarkistaa, että kaikki edellytykset täyttyvät ennen kuin poimintojen määrät määritetään lähteville virroille. Lisätietoja [Lisätietoja: Saatavuus Varastossa](design-details-availability-in-the-warehouse.md)

[!INCLUDE[prod_short](includes/prod_short.md)]ssa saatavuusluvut näytetään yleensä kahdessa eri kentässä, joista molemmilla on eri määritelmä:

* **Määrä saataville** kenttä, joissain kohdin nimeltään **Varasto**, näyttää todellisen, tämänpäiväisen määrän, nimikekirjausten perusteella.
* **Oletettu saatavilla oleva saldo** -kentän arvo on laskennallinen, ja se esittää varastosaldon, johon on lisätty suunnitellut vastaanotot ja josta on vähennetty bruttotarpeet. ([!INCLUDE[prod_short](includes/prod_short.md)] -sovelluksen suunnitellut vastaanotot sisältävät ostotilauksilla ja saapuvilla siirtotilauksilla olevat määrät. Bruttotarpeisiin sisältyvät myyntitilauksilla ja lähtevillä siirtotilauksilla olevat määrät).

> [!TIP]  
>   Oletettu saatavilla oleva saldo soveltuu erityisesti **Nimikk. saatavuus jaksoittain**- ja **Nimikkeen saatavuus tapahtumittain** -sivujen tarkasteluun, koska ne sisältävät päivämäärädimension.  

> [!NOTE]  
>   Seuraavissa ohjeissa kerrotaan, miten saatavuuden lisätietoja tarkastellaan nimikeluettelosta ja -kortilta. Tietoja voi käyttää myös myyntiasiakirjan riveiltä, jotka koskevat ko. nimikettä. Lisätietoja on kohdassa [Tuotteiden myyminen](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Voit tarkastella nimikkeen saatavuutta sen vastaanotto- tai toimituspäivän mukaan.
Voit tarkastella nimikkeen saatavuutta **Saatavuus tapahtumittain** -sivulla näytettävien suunniteltujen nimiketapahtumien perusteella.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Avaa sen nimikkeen kortti, jonka saatavuuden haluat näyttää.
3. Valitse **Nimikkeen saatavuus** -toiminto ja sitten **Tapahtuma**-toiminto.

    **Nimikkeen saatavuus tapahtumittain** -sivulla näkyy, miten nimikkeen varastosaldo kehittyy ajan kuluessa suunniteltujen toimitus- ja vastaanottotapahtumien mukaisesti. Sivulla on tiivistetty näkymä, joka näyttää kertyneitä tietoja yhdellä rivillä kutakin sellaista aikaväliä kohden, jolloin varastosaldot muuttuvat. Aikavälit, jolloin tapahtuneita tapahtumia ei näytetä. Voit laajentaa kunkin rivin näyttämään tietoja tapahtumasta tai tapahtumista, jotka aiheuttivat kertyneen määrän rivillä.
4. Valitse arvo **Oletettu saatavilla oleva saldo** -kentässä tarkastellaksesi nimiketapahtumia tai avataksesi asiakirjoja, jotka muodostavat arvon.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Nimikkeen saatavuuden tarkastelu eri jaksoissa
Nimikkeen saatavuutta määritettynä aikajaksolla voit tarkastella **Nimikk. saatavuus jaksoittain** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Avaa sen nimikkeen kortti, jonka saatavuuden haluat näyttää.
3. Valitse **Nimikkeen saatavuus** -toiminto ja sitten **Jakso**-toiminto.

    **Nimikkeen saatavuus jaksoittain** -sivulla näkyy, kuinka nimikkeen varastomäärä kehittyy valitsemallasi aikajaksolla, kuten Päivä, Viikko tai Neljännes.
4. Valitse arvo **Oletettu saatavilla oleva saldo** -kentässä tarkastellaksesi nimiketapahtumia tai avataksesi asiakirjoja, jotka muodostavat arvon.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Nimikkeen saatavuuden tarkastelu kaikissa sen varastointipaikoissa
Voit tarkastella nimikkeen saatavuutta kaikissa paikoissa, jossa sitä varastoidaan **Nimikkeen saatavuus sijainnin mukaan** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Avaa sen nimikkeen kortti, jonka saatavuuden haluat näyttää.
3. Valitse **Nimikkeen saatavuus** -toiminto ja sitten **Sijainti**-toiminto.

    **Nimikkeen saatavuus sijainnin mukaan** -sivulla näkyy, kuinka nimikkeen varastosaldo kehittyy jatkossa, kullekin varastosijainnille eriteltynä.
4. Valitse arvo **Varastosaldo** -kentässä tarkastellaksesi nimiketapahtumia tai avataksesi asiakirjoja, jotka muodostavat arvon.
5. Valitse arvo **Oletettu saatavilla oleva saldo** -kentässä tarkastellaksesi nimiketapahtumia tai avataksesi asiakirjoja, jotka muodostavat arvon.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Kaikkien nimikkeiden saatavuuden tarkastelu kaikissa niiden varastointipaikoissa
Voit tarkastella kaikkien nimikkeidesi saatavuutta kaikissa sijainneissa **Nimikkeet sijainneittain** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Valitse **Nimikkeet sijainneittain** -toiminto.

    **Nimikkeet sijainneittain** -sivulla näytetään kussakin sijainnissa oleva nimikkeen saldo.
3. Valitse arvo **Varastosaldo** -kentässä tarkastellaksesi nimiketapahtumia tai avataksesi asiakirjoja, jotka muodostavat arvon.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms"></a>Nimikkeen saatavuuden tarkastelu sen mukaan, miten sitä käytetään kokoonpanon tai tuotannon tuoterakenteessa
Jos nimike on kokoonpanon tai tuotannon tuoterakenteessa joko päänimikkeenä tai osana, voit tarkastella **Nimikkeen saatavuus tuoterakennetason mukaan** -sivulla, kuinka monta sen yksikköä tarvitaan. Sivulla näkee, kuinka monta päänimikettä voit tehdä alla olevien rivien alinimikkeiden saatavuuteen perustuen. Kaikki nimikkeet, joilla on kokoonpanon tai tuotannon tuoterakenne, näkyvät sivulla tiivistettävänä rivinä. Voit laajentaa tämän rivin pohjana sen alla oleville osille ja alemman tason osakokoonpanoille niiden omien tuoterakenteiden kanssa.

Sivun avulla voit esimerkiksi nähdä, voitko määrittää nimikkeen myyntitilauksen tiettynä päivämääränä tutkimalla sen nykyisen saatavuuden ja määrien kanssa, jotka sen osat voi toimittaa. Sivun avulla voit myös tunnistaa pullonkaulat liittyvissä tuoterakenteissa.

Seuraavat kentät määrittävät saatavuusluvut sekä päänimikkeiden että alinimikkeiden sivun kullakin rivillä. Voit luvata näiden lukujen avulla, kuinka monta pääyksikköä voit toimittaa, jos aloitat liittyvän kokoonpanoprosessin.

|Kenttä|Kuvaus|
|------|-----------|
|**Kykenee valmistamaan päänimikettä**|Näyttää, kuinka monta yksikköä päänimikkeen osakokoonpanoa voi tehdä. Kenttä määrittää, kuinka monta pääyksikköä voidaan koota välittömästi. Arvo perustuu rivillä olevan nimikkeen saatavuuteen.|
|**Kykenee valmistamaan tärkeintä nimikettä**|Näyttää, kuinka monta yksikköä päänimikettä voi tehdä. Kenttä määrittää, kuinka monta yksikköä tuoterakenteen ylärivin nimikettä voidaan koota. Arvo perustuu rivillä olevan nimikkeen saatavuuteen.|

### <a name="to-view-the-availability-of-an-item-according-to-demand-for-its-parent"></a>Nimikkeen saatavuuden tarkasteleminen pääkohteen kysynnän mukaan
**Nimikkeen saatavuus tuoterakennetason mukaan** -sivulla on sen kortin tai asiakirjarivin nimikkeen tietoja, jonka sivu avattiin. Kohde näkyy aina ylimmällä rivillä. Voit tarkastella muiden nimikkeiden tai kaikkien nimikkeiden tietoja vaihtamalla arvoa **Nimikesuodatus**-kentässä.

> [!NOTE]  
>   Oletusarvon mukaan rivien luvut näyttävät kaikkien nimikkeiden kokonaissaatavuuden ylimmän nimikkeen alla. Nämä luvut näkyvät **Saatavilla oleva määrä** -kentässä ja kohdistus on ylimmässä nimikkeessä. Tiedot siitä, miten monta osakokoonpanoa voidaan tehdä, voivat olla virheellisiä. Jotta saisit todellista tietoa siitä, kuinka monta näkyvää osakokoonpanoa voit tehdä, sinun on poistettava **Näytä kokonaissaatavuus** -valintaruudun valinta ja tarkistettava sitten **Kykenee valmistamaan päänimikettä** -kentän luku.

**Pullonkaula**-kenttä määrittää, mikä tuoterakenteen nimike estää suuremman valmistusmäärän kuin **Kykenee valmistamaan tärkeintä nimikettä** -kentässä näkyvä määrä. Pullonkaulanimike voi olla esimerkiksi ostettu osa, jonka oletettu vastaanottopäivämäärä on liian myöhään, jotta päänimekettä voitaisiin valmistaa lisää **Tarvitaan päivämäärän mennessä** -kentässä olevaan päivämäärään mennessä.

## <a name="to-view-the-availability-of-an-item-by-its-units-of-measure"></a>Nimikkeen saatavuuden näyttäminen mittayksiköinä
**Nimikkeen saatavuusmittayksikkö** -sivu näyttää nimikkeen saatavuuden mittayksiköinä, joina se on varastoitu.

> [!NOTE]  
> Jotta tiedot pysyisi virheettöminä, sinun täytyy muuntaa nimikkeen mittayksiköt. Jos esimerkiksi ostat nimikkeen yhtenä mittayksikkönä, esimerkiksi laatikoina, ja myyt nimikkeitä muussa mitta yksikössä, esimerkiksi kappaleina, sinun täytyy muuntaa mittayksiköt nimikepäiväkirjan avulla tai purkaa nimikkeet eri yksiköiksi. Negatiivisen muutoksen nimikepäiväkirjan rivin avulla voit vähentää varastoa ostomittayksikössä, esimerkiksi laatikoina, ja positiivisen muutoksen avulla, joka lisää varaston määrää myynnin mittayksikössä, esimerkiksi kappaleina. 

## <a name="assembly-availability-page"></a>Kokoonpanon saatavuus -sivu
**Kokoonpanon saatavuus** -sivulla on kokoonpanonimikkeen tarkat saatavuustiedot. Avautuminen:

- Automaattisesti myyntitilausrivistä kokoonpano tilausta varten - tilanteissa, kun syötät määrän, joka saa aikaan osan saatavuusongelman.
- Automaattisesti kokoonpanotilauksen otsikosta, kun syötät Määrä-kenttään arvon, joka saa aikaan osan saatavuusongelman.
- Manuaalisesti, kun avaat sen kokoonpanotilauksesta. Valitse Toiminnot-välilehden Funktiot-ryhmässä Näytä saatavuus.

**Tiedot**-pikavälilehdessä on kokoonpanon nimikkeen yksityiskohtaiset saatavuustiedot, kuten montako kokoonpanotilausten määrää voidaan koota eräpäivään mennessä tarvittavien osien saatavuuden perusteella. Tämä näkyy Mahdollista koota -kentässä Tiedot-pikavälilehdellä.

**Mahdollista koota** -kentän arvo näkyy punaisella fontilla, jos määrä on pienempi kuin **Jäljellä oleva määrä** -kentässä näkyvä määrä, mikä ilmaisee, että osia ei riitä koko määrän kokoamiseen.

**Rivit**-pikavälilehdessä on kokoonpanon komponenttien yksityiskohtaiset saatavuustiedot.

Jos vähintään yksi kokoonpanon komponentti ei ole saatavana, vaikutus näkyy kyseisen rivin **Mahdollista koota** -kentässä niin, että sen määrä on pienempi kuin **Tiedot**-pikavälilehden **Jäljellä oleva määrä** -kentän arvo.

## <a name="see-also"></a>Katso myös
[Varaston hallinta](inventory-manage-inventory.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Tuoterakenteiden käyttäminen](inventory-how-work-BOMs.md)    
[Sijaintien määrittäminen](inventory-how-setup-locations.md)  
[Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md)  
[Tuotteiden myyminen](sales-how-sell-products.md)      
[Business Centralin käyttäminen](ui-work-product.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]