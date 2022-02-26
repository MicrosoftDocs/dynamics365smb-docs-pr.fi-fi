---
title: Varaston laskeminen, muuttaminen ja uudelleenluokitus
description: Suorita nimiketapahtumien inventointi, tee niissä negatiivisia tai positiivisia oikaisuja ja muuta niiden tietoja, kuten sijaintia tai eränumeroa, nimiketapahtumissa tai fyysisen varaston tapahtumissa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.search.forms: 1327, 393, 392, 390, 7381, 7380, 7319, 7324, 7326, 7365
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 5d8625434a661beb126ca234ea760038a6b75506
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059698"
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a>Varaston laskeminen, muuttaminen ja uudelleenluokitus käyttämällä päiväkirjoja
Vähintään kerran tilikauden aikana tulee suorittaa inventointi (eli laskea kaikki varastossa olevat nimikkeet), jotta nähtäisiin, onko tietokantaan rekisteröity määrä sama kuin varaston fyysinen määrä. Kun varaston fyysinen määrä on tiedossa, se on kirjattava pääkirjanpitoon osana kauden lopun varaston arvostusta.

Vaikka lasket kaikki varaston nimikkeet vähintään kerran vuodessa, voit päättää laskevasi joitain nimikkeitä useammin, koska ne ovat ehkä arvokkaampia tai ne liikkuvat nopeasti varastosta ja ovat suuri osa liiketoimintaa. Voit määrittää tätä varten erityisiä laskentajaksoja. Lisätietoja on kohdassa [Inventoinnin suorittaminen](inventory-how-count-adjust-reclassify.md#to-perform-cycle-counting).

Jos kirjattuja varastomääriä pitää muuttaa laskennan yhteydessä tai muita tarkoituksia varten, inventointitapahtumia voi muuttaa suoraan nimikepäiväkirjan avulla liiketoimintatapahtumia kirjaamatta. Vaihtoehtoisesti voit muuttaa yhden nimikkeen nimikekortissa.

Jos nimiketapahtumien määritteitä on muutettava, voit käyttää nimikkeen uudelleenluokituspäiväkirjaa. Tyypillisiä uudelleenluokiteltavia määritteitä ovat dimensiot ja myyntikampanjan koodit, mutta myös tehdä järjestelmäsiirtoja luokittelemalla varastopaikka- ja sijaintikoodit uudelleen. Sarja- tai eränumeroiden sekä niiden vanhentumispäivämäärien uudelleenluokittelussa on erityisvaiheita. Lisätietoja on kohdassa [Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md).

> [!NOTE]
> Laajennetussa varastointimäärityksessä nimikkeet rekisteröidään varastopaikoissa nimiketapahtumien sijaan fyysisen varastoinnin tapahtumina. Niinpä laskenta, muutokset ja uudelleenluokittelu tehdään tavarapaikkoja tukevissa erityisissä fyysisen varastoinnin päiväkirjoissa. Voit sitten synkronoida uudet tai muuttuneet fyysisen varastoinnin tapahtumat erityistoiminnoilla tapahtumiin liittyviin nimeketapahtumiin siten, että vastaavat varaston määrissä ja arvoissa tapahtuneita muutoksia. Tätä käsitellään tarvittaessa jäljempänä olevissa toimenpidekuvauksissa.

## <a name="to-perform-a-physical-inventory"></a>Inventoinnin suorittaminen
Sinun tulee tehdä inventointi (eli laskea saatavilla olevat nimikkeet) nähdäksesi, onko ohjelmaan rekisteröity määrä sama kuin varaston fyysinen määrä, tilikauden lopussa ellei useamminkin. Jos löytyy eroja, ne tulee kirjata nimiketileille ennen varaston arvostusta.

> [!NOTE]
> Tässä menettelyssä käsitellään inventoinnin tekemistä päiväkirjan avulla **Varastopäiväkirja**-sivulla. Voit tehdä tehtävän myös hyödyntämällä asiakirjoja **Inventointitilaus**- ja **Inventointitallennus**-sivuilla, mikä parantaa hallintaa ja tukee inventoinnin jakamista useiden työntekijöiden kanssa. Lisätietoja on kohdassa [Varastojen laskenta asiakirjoja käyttämällä](inventory-how-count-inventory-with-documents.md).<br /><br />
> Huomaa, että asiakaspohjaisia toimintoja ei voi käyttää varastopaikoissa tai varastotapahtumissa olevien nimikkeiden inventointiin.

Fyysisen laskentajakson lisäksi täydellinen prosessi käsittää seuraavat kolme tehtävää:

- Laske oletettu varasto.
- Tulosta raportti, jota käytetään laskennassa.
- Syötä ja kirjaa todellinen laskettu varasto.

Voit tehdä inventoinnin jommallakummalla tavalla fyysisen varastoinnin asetusten mukaan. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

-   Jos ohjattu hyllytys ja poiminta ei ole käytössä sijainnissa (varastoinnin perusmääritys), käytä **Varastopäiväkirja**-sivua **Varasto**-valikossa. Menettely on lähes sama kuin silloin, kun suoritetaan inventointi ilman syklin laskentaa.  
-   Jos sijainnissa käytetään ohjattua hyllytystä ja poimintaa (laajennettu varastointimääritys), suorita **Laske f.var. muutos** -toiminto käyttämällä ensin **F.var. inventointipvk** -sivua ja sitten **Nimikepäiväkirja**-sivua.

### <a name="to-calculate-the-expected-inventory-in-basic-warehouse-configurations"></a>Oletetun varaston laskeminen varastoinnin perusmäärityksissä
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastopäiväkirjat** ja valitse sitten vastaava linkki.
2. Valitse **Laske varasto** -toiminto.
3. Määritä **Laske varasto** -sivulla ehdot, joita käytetään luotaessa päiväkirjarivejä, kuten sisällytetäänkö nimikkeet, joiden kirjattu varastomäärä on nolla.
4. Aseta suodattimia, jos haluat laskea vain varaston tiettyjä nimikkeitä, varastopaikkoja, sijainteja tai dimensioita.
5. Valitse **OK**-painike.

> [!NOTE]  
>   Ohjelma käsittelee nimiketapahtumat määrittämiesi tietojen mukaan ja luo rivejä inventointipäiväkirjaan. Huomaa, että **Määrä (inventointi)** -kenttään täytetään automaattisesti sama määrä kuin **Määrä (laskettu)** -kenttään. Tämän ominaisuuden ansiosta sinun ei tarvitse syöttää laskettua varastosaldoa niiden nimikkeiden osalta, joiden määrä on sama kuin laskettu määrä. Jos laskettu määrä kuitenkin eroaa **Määrä (laskettu)** -kenttään syötetystä määrästä, korvaa se todellisella lasketulla määrällä.

### <a name="to-print-the-report-to-be-used-when-counting"></a>Laskennassa käytettävän raportin tulostaminen
1. Valitse lasketun oletetun varaston sisältävän **Varastopäiväkirja**-sivulla **Tulosta**-toiminto.
2. Määritä **Inventointiluettelo**-sivulla, näytetäänkö raportissa laskettu määrä ja näkyykö raportissa varastonimikkeiden luettelo sarja ja eränumeroiden mukaan.
3. Määritä suodattimia, jos haluat tulostaa vain tiettyjä varastojen nimikkeiden, varastopaikkojen, sijaintien tai dimensioiden raportteja.
4. Valitse **Tulosta**-painike.

Työntekijät voivat nyt laskea varaston ja merkitä mahdolliset poikkeamat tulostettuun raporttiin.

> [!NOTE]
> Voi kestää useita päiviä, ennen kuin painetut raportit tulevat takaisin lopullista käsittelyä ja kirjaamista varten. Kun määrität ja kirjaat todellisen lasketun varaston, järjestelmä muuttaa varaston vastaamaan oletetun ja todellisen varaston eroa. Sinun täytyy säilyttää alkuperäiset lasketut päiväkirjan rivit eikä laskea oletettua varastoa uudelleen, koska oletettu varasto voi muuttua ja johtaa vääriin varastomääriin. Jos sinun täytyy lähettää useita raportteja, kuten eri sijainteja tai nimikeryhmiä, sinun täytyy luoda ja pitää erilliset päiväkirjan erät.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Todellisen lasketun varaston antaminen ja kirjaaminen fyysisen varastoinnin perusmäärityksissä
1. Jos jollakin **Varastopäiväkirja**-sivun rivillä inventoinnissa määritetty todellinen saatavissa oleva varastomäärä poikkeaa lasketusta määrästä, anna **Määrä (varastotilanne)** -kentässä todellinen saatavissa oleva varastomäärä.

    Liittyvät kentät päivitetään tämän mukaisesti.

    > [!NOTE]  
    >   Jos inventointi paljastaa eroja, jotka johtuvat siitä, että nimikkeitä on kirjattu virheellisten sijaintikoodien kanssa, älä syötä eroja inventointipäiväkirjaan. Käytä sen sijaan uudelleenluokituspäiväkirjaa tai siirtotilausta nimikkeiden ohjaamiseen oikeisiin sijainteihin. Lisätietoja on kohdassa Nimikkeen uudel.luokit. pvk tai Siirtotilausten luominen.

2. Voit muokata lasketut määrät todellisten laskettujen määrien mukaiseksi valitsemalla **Kirjaus**-toiminnon.

    Sekä nimiketapahtumat että fyysiset inventointitapahtumat luodaan. Avaa nimikkeen kortti, jos halkuat tarkastella tuloksena saatavia inventointitapahtumia.

3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
4. Voit tarkistaa inventoinnin avaamalla kyseisen nimikekortin ja valitsemalla sitten **Inventointitapahtumat** -toiminnon.

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Oletetun varaston laskeminen laajennetuissa varastomäärityksissä
Synkronoi nimikekirjanpito ja fyysinen varasto ennen kuin suoritat fyysisen varastoinnin inventoinnin, muutoin inventointipäiväkirjaan ja prosessin viimeisessä vaiheessa nimiketapahtumiin kirjaamasi tulokset ovat inventoinnin tulosten ja muiden fyysisen varastoinnin muutosten yhdistelmä laskettujen nimikkeiden osalta. Lisätietoja on kohdassa [Määrien synkronoiminen nimikekirjauksessa ja varastossa](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries)

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Invent. varastopäiväk.** ja valitse sitten vastaava linkki.  
2. Valitse **Laske varasto** -toiminto. **F. var. laske varasto** -eräajon pyyntösivu avautuu.  
3. Aseta suodattimet rajoittamaan päiväkirjassa laskettavia nimikkeitä ja napsauta sitten **OK**.

    Sovellus luo rivin kullekin varastopaikalle, joka täyttää suodattimen vaatimukset. Tässä vaiheessa voi vielä poistaa joitain rivejä, mutta jos haluat kirjata tulokset inventoinniksi, nimike tulee laskea kaikista varastopaikoista, jotka sisältävät sen.  

     Jos on aikaa laskea nimikkeet vain joistain varastopaikoista, voit löytää eroavaisuuksia, rekisteröidä ne ja myöhemmin kirjata ne nimikepäiväkirjaan käyttämällä **Laske f.var. muutos** -toimintoa.  


### <a name="to-print-the-report-to-be-used-when-counting"></a>Laskennassa käytettävän raportin tulostaminen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston fyysisen varaston luettelo** ja valitse sitten vastaava linkki.  
2. Avaa raportin pyyntösivu ja tulosta luettelot, joihin haluat työntekijöiden kirjaavan kussakin varastopaikassa laskettujen nimikkeiden määrät.  

Työntekijät voivat nyt laskea varaston ja merkitä mahdolliset poikkeamat tulostettuun raporttiin.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Todellisen lasketun varaston antaminen ja kirjaaminen laajennetuissa varastomäärityksissä
1. Kun laskenta on tehty, syötä lasketut määrät fyysisen varastoinnin inventointipäiväkirjan **Määrä (inventointi)** -kenttään.  

    > [!NOTE]  
    >  Ohjelma täyttää fyysisen varastoinnin inventointipäiväkirjassa automaattisesti **Määrä (laskettu)** -kentän fyysisen varaston varastopaikkatietueiden perusteella ja kopioi nämä määrät kunkin rivin **Määrä (inventointi)** -kenttään. Jos fyysisen varaston työntekijän laskema määrä poikkeaa sovelluksen Määrä (inventointi) -kenttään syöttämästä määrästä, syötä tosiasiassa laskettu määrä.  

2. Kun olet antanut kaikki lasketut määrät, valitse **Rekisteröi**-toiminto.  

    Kun päiväkirja rekisteröidään, sovellus luo kaksi fyysisen varastoinnin tapahtumaa fyysisen varaston rekisteriin kunkin rivin osalta, joka laskettiin ja rekisteröitiin:  

    -   Jos lasketut ja inventointimäärät eroavat toisistaan, varastopaikalle rekisteröidään negatiivinen tai positiivinen määrä, ja sijainnin muutoksen varastopaikkaan kirjataan vastamäärä.  
    -   Jos laskettu määrä on sama kuin inventointimäärä, sovellus rekisteröi tapahtuman, jonka arvo on 0, sekä varastopaikalle että muutoksen varastopaikalle. Tapahtumat ovat tallenteita siitä, että rekisteröintipäivämäärän suoritettiin fyysisen varaston inventointi, eikä nimikkeen osalta varastossa ollut eroavaisuuksia.  

Kun fyysisen varastoinnin inventointia rekisteröidään, kirjausta nimiketapahtumiin, inventointitapahtumiin tai arvotapahtumiin ei tapahdu, vaan tietueet ovat valmiina välitöntä täsmäytystä varten heti, kun sitä tarvitaan. Jos haluat kuitenkin ylläpitää tarkkoja tietueita siitä, mitä fyysisessä varastoinnissa tapahtuu, ja jos olet laskenut kaikki varastopaikat, joihin nimikkeet on rekisteröity, fyysisen varastoinnin tulokset tulisi heti kirjata inventoinniksi varastonhallinnassa. Lisätietoja on kohdassa [Määrien synkronoiminen nimikekirjauksessa ja varastossa](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).


## <a name="to-perform-cycle-counting"></a>Inventoinnin suorittaminen
Vaikka lasket kaikki varaston nimikkeet vähintään kerran vuodessa, voit päättää laskevasi joitain nimikkeitä useammin, koska ne ovat ehkä arvokkaampia tai ne liikkuvat nopeasti varastosta ja ovat suuri osa liiketoimintaa. Voit määrittää tätä varten erityisiä laskentajaksoja.

Sykli voidaan laskea jommallakummalla tavalla määritettyjen varastoasetusten mukaan. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

-   Jos ohjattu hyllytys ja poiminta ei ole käytössä sijainnissa (varastoinnin perusmääritys), käytä **Varastopäiväkirja**-sivua **Varasto**-valikossa. Menettely on lähes sama kuin silloin, kun suoritetaan inventointi ilman syklin laskentaa.  
-   Jos sijainnissa käytetään ohjattua hyllytystä ja poimintaa (laajennettu varastointimääritys), suorita **Laske f.var. muutos** -toiminto käyttämällä ensin **F.var. inventointipvk** -sivua ja sitten **Nimikepäiväkirja**-sivua.  

### <a name="to-set-up-counting-periods"></a>Laskentajaksojen määrittäminen
Inventointi suoritetaan tavallisesti toistuvin aikavälein, esimerkiksi kuukausittain, neljännesvuosittain tai vuosittain. Voit määrittää mitä tahansa inventoinnin laskentajaksoja.

Määritä käytettävät inventointijaksot ja määritä yksi niistä kullekin nimikkeelle. Kun suoritat inventoinnin ja käytät inventointipäiväkirjassa **Laske laskentajakso** -vaihtoehtoa, nimikkeiden rivit luodaan automaattisesti.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastotilanteen laskentajaksot** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Laskentajakson määritteleminen nimikkeelle  
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Valitse nimike, jolle haluat määrittää laskentajakson.  
3. Valitse **Inventointijakson koodi** -kentässä sopiva laskentajakso.  
4. Valitse **Kyllä**-painike vaihtaaksesi koodin ja laskeaksesi nimikkeelle ensimmäisen laskentajakson. Kun lasket seuraavan kerran inventointipäiväkirjassa laskentajakson, nimike näkyy rivinä **Inventoinnin nimikevalinta** -sivulla. Voit sitten aloittaa nimikkeen laskennan säännöllisin väliajoin.

### <a name="to-initiate-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Laskennan käynnistäminen laskentakauden perusteella fyysisen varastoinnin perusmäärityksissä
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastopäiväkirjat** ja valitse sitten vastaava linkki.
2. Valitse **Laske laskentajakso** -toiminto.

    Avautuvalla **Inventoinnin nimikevalinta** -sivulla näkyvät nimikkeet, joille on määritetty laskentajaksot ja jotka on laskettava niiden laskentajaksojen mukaisesti.
3. Suorita inventointi. Lisätietoja on kohdassa [Fyysisen varaston inventointi](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).

### <a name="to-initiate-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Laskennan käynnistäminen laskentakauden perusteella laajennetuissa varastomäärityksissä
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Invent. varastopäiväk.** ja valitse sitten vastaava linkki.  
2. Valitse **Laske laskentajakso** -toiminto.

    Avautuvalla **Inventoinnin nimikevalinta** -sivulla näkyvät nimikkeet, joille on määritetty laskentajaksot ja jotka on laskettava niiden laskentajaksojen mukaisesti.
3. Suorita inventointi. Lisätietoja on kohdassa [Fyysisen varaston inventointi](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).  

    > [!NOTE]  
    >  Nimike tulee laskea kaikista varastopaikoista, jotka sisältävät kyseistä nimikettä. Jos poistat joitakin varastopaikan rivejä, jotka sovellus on hakenut laskentaa varten **F. var. inventointi** -sivulle, kaikkia fyysisen varaston nimikkeitä ei silloin lasketa. Jos kirjaat tällaisia epätäydellisiä tuloksia inventointipäiväkirjaan myöhemmin, kirjatut summat ovat virheellisiä.  

## <a name="to-adjust-the-inventory-of-one-item"></a>Yhden nimikkeen varastonimikkeen muuttaminen
Kun nimikkeen fyysinen laskenta on suoritettu varastoalueellasi, voit käyttää **Muuta varasto**-toimintoa todellisen varastomäärän kirjaamiseen.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Valitse nimike, jonka varastoa haluat muuttaa, ja valitse sitten **Muuta varastoa** -toimintoa.
3. Syötä **Uusi varasto** -kenttään varastomäärä, jonka haluat tallentaa nimikkeelle.
4. Valitse **OK**-painike.

Nimikkeen varasto on nyt määritetty. Uusi määrä näkyy **Nimikkeen kortti**-sivun **Varastosaldo** -kentässä.

Voit käyttää **Muuta varastoa** -toimintoa myös yksinkertaisena tapana asettaa ostetut nimikkeet varastoon, jos et tallenna ostoja ostolaskuina tai -tilauksina. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Kun olet muuttanut varastoa, se on päivitettävä nykyisellä lasketulla arvolla. Lisätietoja on kohdassa [Varaston uudelleenarvostus](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-inventory-quantity-of-multiple-items-in-basic-warehouse-configurations"></a>Useiden nimikkeiden varastosaldon muuttaminen fyysisen varastoinnin perusmäärityksissä
Voit kirjata **Nimikepäiväkirja**-sivulla nimiketapahtuman suoraan ja muuttaa varastoa ostojen, myyntien ja positiivisten tai negatiivisten muutosten yhteydessä asiakirjoja käyttämättä.

Jos nimikepäiväkirjaan kirjataan usein samoja tai saman tyyppisiä päiväkirjan rivejä (esimerkiksi materiaalien kulutukseen liittyen), voit helpottaa toistuvien toimien suorittamista **Vakionimikepäiväkirja**-sivun avulla. Lisätietoja on kohdassa [Vakiopäiväkirjojen käyttäminen](ui-work-general-journals.md#working-with-standard-journals).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikepäiväkirjat** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Tee muutokset varastoon valitsemalla **Kirjaa**-toiminto.

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Varastopaikkamäärien muuttaminen laajennetuissa varastomäärityksissä  
Kun käytät ohjattua hyllytystä ja poimintaa, käytä muissa kuin inventointiyhteyksissä **fyysisen varastoinnin nimikepäiväkirjaa** kaikkien todellisten positiivisten muutosten (esimerkiksi puuttuneiden nimikkeiden löytymisen) ja negatiivisten muutosten (esimerkiksi nimikkeiden särkymisen) kirjaamiseen.  

Toisin kuin kirjattaessa muutoksia varaston nimikepäiväkirjaan, fyysisen varastoinnin nimikepäiväkirjaa käytettäessä käytössä on tarkempi muutostaso, jonka avulla määrätietueet pysyvät entistä paremmin ajan tasalla. Fyysisessä varastoinnissa on siis aina tarkat tiedot siitä, kuinka paljon nimikkeitä on saatavilla ja missä ne ovat varastoituina, mutta kutakin muutosrekisteröintiä ei kirjata heti nimiketapahtumiin. Rekisteröintiprosessissa ohjelma hyvittää tai veloittaa oikeaa varastopaikkaa määrän muutoksella ja tekee vastatapahtuman muutosvarastopaikkaan - virtuaalivarastopaikkaan, jossa ei ole oikeita nimikkeitä. Tämä varastopaikka on määritetty sijaintikortin **Var. muutosvarastopaikan koodi** -kentässä.

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **F. var. nimikepvk:t** ja valitse sitten vastaava linkki.  
2.  Täytä otsikon tiedot.  
3.  Täytä rivillä oleva **Nimikkeen nro** -kenttä.  
4.  Syötä varastopaikka, johon olet panemassa ylimääräiset nimikkeet tai josta olet löytänyt puuttuvat nimikkeet.  
5.  Täytä **Määrä**-kenttään määrä, jonka olet havainnut eroavaisuudeksi. Jos olet löytänyt ylimääräisiä nimikkeitä, syötä positiivinen määrä. Jos nimikkeitä puuttuu, syötä negatiivinen määrä.  
6.  Valitse **Rekisteröi**-toiminto.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Muutettujen fyysisen varastoinnin tapahtumien ja liittyvien nimiketapahtumien synkronointi
Fyysisen varastoinnin muutosvarastopaikan tietueet tulee kirjata yrityksen menettelytapojen mukaisin aikavälein nimiketapahtumiin. Joissakin yrityksissä muutokset on hyvä kirjata nimiketapahtumiin joka päivä, kun taas toisissa yrityksissä voi olla järkevämpää täsmäyttää muutokset harvemmin.

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikepäiväkirja** ja valitse sitten vastaava linkki.  
2.  Kirjoita kunkin päiväkirjarivin kenttien tiedot.  
3.  Valitse **Laske f.var. muutos** -toiminto ja täytä tarvittavat suodattimet eräajon pyyntösivulla. Muutokset lasketaan vain Muutosvarastopaikan tapahtumille, jotka täyttävät suodattimen vaatimukset.  
4.  Täytä **Vaihtoehdot**-pikavälilehden **Asiakirjan nro** -kenttään manuaalisesti syöttämäsi numero. Koska tälle eräajolle ei ole määritetty numerosarjaa, käytä fyysisen varastoinnin määrittämää numeromallia tai syötä päivämäärä (päivä-kuukausi-vuosi) ja sen jälkeen nimikirjaimesi.  
5.  Valitse **OK**-painike. Ohjelma laskee yhteen kunkin nimikkeen positiiviset ja negatiiviset muutokset ja luo nimikepäiväkirjaan rivejä kaikille nimikkeille, joiden summa on positiivinen tai negatiivinen määrä.  
6.  Lisää määräerot nimiketapahtumiin kirjaamalla päiväkirjarivit. Fyysisen varastoinnin varastopaikkojen varasto vastaa nyt tarkasti nimiketapahtumien varastoa.  

## <a name="to-reclassify-an-items-lot-number"></a>Nimikkeen eränumeron uudelleenluokittelu
Jos nimiketapahtumien määritteitä on muutettava, voit käyttää nimikkeen uudelleenluokituspäiväkirjaa. Tyypillisiä uudelleenluokiteltavia määritteitä ovat dimensiot ja myyntikampanjan koodit, mutta myös tehdä järjestelmäsiirtoja luokittelemalla varastopaikka- ja sijaintikoodit uudelleen.

Sarja- tai eränumeroiden sekä niiden vanhentumispäivämäärien uudelleenluokittelussa on erityisvaiheita. Lisätietoja on kohdassa [Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md).

Seuraava esimerkki perustuu sijaintikoodiin. Ohjeet ovat vastaavanlaiset myös muiden nimikkeen määritetyyppien kohdalla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen uudell.luokit. pvk:t** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät **Nimik. uud.luok.pvk** -sivulla.
3. Anna **Sijaintikoodi**-kentässä nimikkeen nykyinen sijaintikoodi.
4. Anna **Uusi sijaintikoodi** -kentässä nimikkeen uusi sijaintikoodi.
5. Valitse **Kirjaa**-toiminto.

Lisätietoja nimikkeiden siirtämisestä siten, että toimitus- ja vastaanottomäärien hallinta säilyy, on kohdassa [Varastonimikkeiden siirtäminen sijaintien välillä](inventory-how-transfer-between-locations.md).

## <a name="see-also"></a>Katso myös
[Varastojen laskenta asiakirjoja käyttämällä](inventory-how-count-inventory-with-documents.md)  
[Varasto](inventory-manage-inventory.md)
[Varastoinninhallinta](warehouse-manage-warehouse.md)    
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]