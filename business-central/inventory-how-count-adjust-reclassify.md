---
title: 'Varaston laskeminen, muuttaminen ja uudelleenluokitus'
description: Tietoja inventaariosta sekä muutosten ja uudelleenluokitusten tekemisestä.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a><a name="count-adjust-and-reclassify-inventory-using-journals"></a><a name="count-adjust-and-reclassify-inventory-using-journals"></a>Varaston laskeminen, muuttaminen ja uudelleenluokitus käyttämällä päiväkirjoja

Kaikkien varastossa olevien nimikkeiden inventointi varmistaa, että määrät ovat oikein. Joissakin yrityksissä inventaario tehdään vuosittain, kun taas toisissa yrityksissä kaikki tai jotkin nimekkeet inventoidaan tätä useammin. Nimikkeiden inventoinnin jälkeen todelliset määrät kirjataan päiväkirjojen avulla kirjanpitoon. Se tehdään esimerkiksi arvostettaessa varaston kauden päättyessä.

Jos osa nimikkeistä on inventoitava muita useammin esimerkiksi niiden arvon vuoksi, siihen käytetään inventointia. Inventoinnissa nimikkeille määritetään erityisiä inventointijaksoja. Lisätietoja on kohdassa [Inventointi](inventory-how-count-adjust-reclassify.md#to-do-cycle-counting).

Määriä voi muuttaa inventaarion tai muun laskennan jälkeen käyttämällä nimikepäiväkirjaa varastotapahtumien muuttamiseen ilman tapahtumien kirjaamista. Yhden nimikkeen määrää voi muuttaa myös nimikekortissa.

Nimiketapahtumien määritteitä voi muuttaa käyttämällä nimikkeen uudelleenluokituspäiväkirjaa. Tyypillisiä uudelleenluokiteltavia määritteitä ovat dimensiot ja myyntikampanjan koodit. Uudelleenluokituspäiväkirjoja voi käyttää myös siirtoihin luokittelemalla uudelleen varastopaikan ja sijainnin koodit. Sarja- tai eränumeroiden sekä niiden vanhentumispäivämäärien uudelleenluokittelussa on erityisvaiheita. Lisätietoja on kohdassa [Sarja- ja eränumeroiden käsitteleminen](inventory-how-work-item-tracking.md).

> [!NOTE]
> Monivaiheissa prosesseissa nimikkeet rekisteröidään varastopaikoissa nimiketapahtumien sijaan fyysisen varastoinnin tapahtumina. Niinpä inventointi, muutokset ja uudelleenluokittelu tehdään varastopaikkoja tukevissa fyysisen varastoinnin päiväkirjoissa. Sen jälkeen uudet tai muuttuneet fyysisen varastoinnin tapahtumat voidaan synkronoida tapahtumiin liittyviin nimeketapahtumiin siten, että ne vastaavat varaston määrissä ja arvoissa tapahtuneita muutoksia.

## <a name="to-count-physical-inventory"></a><a name="to-count-physical-inventory"></a><a name="to-count-physical-inventory"></a>Inventaarion suorittaminen

Tekemällä inventaario eli saatavilla olevien nimikkeiden laskenta voidaan tarkistaa, onko rekisteröity määrä sama kuin fyysisessä varastossa oleva määrä. Inventointi tehdään yleensä tilikauden lopussa, joskin joskus se suoritetaan tätä useammin. Jos määrissä on eroja, todelliset määrät kirjataan nimiketileille <!--accounts, or ledger?--> ennen varaston arvostusta.

> [!NOTE]
> Tässä menettelyssä käsitellään inventaarion tekemistä **Varastopäiväkirja**-sivulla olevan päiväkirjan avulla. **Inventointitilaus**- ja  **Inventointitallennus**-sivuilla on hyödyllisiä asiakirjoja. Nämä asiakirjat tukevat inventointityön hallittua jakamista useille työntekijöille. Lisätietoja on kohdassa [Varastojen laskenta asiakirjoja käyttämällä](inventory-how-count-inventory-with-documents.md).<br /><br />
> On huomattava, että asiakirjapohjaisia toimintoja ei voi käyttää varastopaikoissa tai varastotapahtumissa olevien nimikkeiden inventointiin.

Inventointiprosessi sisältää myös seuraavat tehtävät:

- Laske oletettu varasto.
- Inventoinnissa käytettävän raportin tulostaminen.
- Todellisten määrien syöttäminen ja kirjaaminen.

Varastointimääritysten mukaan inventaario voidaan tehdä jommallakummalla seuraavista tavoista. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

- Sijainnissa, jossa ohjattu hyllytys ja poiminta ei ole käytössä, käytetään **Inventointipäiväkirja**-sivua. Tämä menettely muistuttaa inventaariota, jossa ei tehdä inventointia.  
- Sijainnissa, jossa ohjattu hyllytys ja poiminta on käytössä, käytetään **Fyysisen varaston inventointipäiväkirja**-sivua. Sen jälkeen suoritetaan **Laske fyysisen varaston muutos** -toiminto **Nimikepäiväkirjat**-sivulla. <!--We should say what to do on each of these pages.-->

### <a name="to-calculate-expected-inventory-in-basic-warehouse-configurations"></a><a name="to-calculate-expected-inventory-in-basic-warehouse-configurations"></a><a name="to-calculate-expected-inventory-in-basic-warehouse-configurations"></a>Oletetun varaston laskeminen varastoinnin perusmäärityksissä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Inventointipäiväkirjat** ja valitse sitten vastaava linkki.
2. Valitse **Laske varasto** -toiminto.
3. Määritä **Laske varasto** -sivulla ehdot, joita käytetään luotaessa päiväkirjarivejä, kuten sisällytetäänkö nimikkeet, joiden kirjattu varastomäärä on nolla.
4. Aseta suodattimia, jos haluat laskea vain varaston tiettyjä nimikkeitä, varastopaikkoja, sijainteja tai dimensioita.
5. Valitse **OK**-painike.

> [!NOTE]  
> Nimiketapahtumat käsitellään määritettyjen tietojen mukaan ja rivit luodaan inventointipäiväkirjaan. Huomaa, että **Määrä (inventointi)** -kentässä on sama määrä kuin **Määrä (laskettu)** -kentässä. Nimikkeiden laskettua määrää ei tarvitse syöttää, jos nämä määrät ovat samat. Jos inventoitu määrä ei kuitenkaan ole sama, inventoitu määrä on syötettävä.

### <a name="to-print-the-report-to-be-used-when-counting"></a><a name="to-print-the-report-to-be-used-when-counting"></a><a name="to-print-the-report-to-be-used-when-counting"></a>Laskennassa käytettävän raportin tulostaminen

1. Valitse lasketun oletetun varaston sisältävän **Inventointipäiväkirja**-sivulla **Tulosta**-toiminto.
2. Määritä **Varaston inventointiluettelo** -sivulla, näytetäänkö raportissa laskettu määrä ja varastonimikkeiden luettelo sarja- ja eränumeroiden mukaan.
3. Määritä suodattimia, jos haluat tulostaa vain tiettyjä varastojen nimikkeiden, varastopaikkojen, sijaintien tai dimensioiden raportteja.
4. Valitse **Tulosta**.

Varastotyöntekijät voivat nyt inventoida varaston ja kirjata mahdolliset erot tulostettuun raporttiin.

> [!NOTE]
> Voi kestää useita päiviä, ennen kuin painetut raportit tulevat takaisin lopullista käsittelyä ja kirjaamista varten. Kun määrität ja kirjaat todellisen lasketun varaston, järjestelmä muuttaa varaston vastaamaan oletetun ja todellisen varaston eroa. Alkuperäiset lasketut päiväkirjan rivit on säilytettävä eikä oletettua varastoa lasketa uudelleen, koska oletettu varasto voi muuttua ja johtaa virheellisiin varastomääriin. Jos sinun täytyy lähettää useita raportteja, kuten eri sijainteja tai nimikeryhmiä, sinun täytyy luoda ja pitää erilliset päiväkirjan erät.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a><a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a><a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Todellisen lasketun varaston antaminen ja kirjaaminen fyysisen varastoinnin perusmäärityksissä

1. Jos jollakin **Inventointipäiväkirja**-sivun rivillä inventoinnissa määritetty todellinen saatavissa oleva varastomäärä poikkeaa lasketusta määrästä, anna **Määrä (varastotilanne)** -kentässä todellinen saatavissa oleva varastomäärä.
  
  > [!NOTE]  
  > Jos inventointi paljastaa eroja, joiden syynä on nimikkeiden kirjaaminen virheelliseen sijaintiin, näitä eroja ei syötetä inventointipäiväkirjaan. Sen sijaan käytetään uudelleenluokituspäiväkirjaa tai siirtotilausta nimikkeiden ohjaamiseen oikeisiin sijainteihin. 

2. Voit muokata lasketut määrät todellisten laskettujen määrien mukaiseksi valitsemalla **Kirjaus**-toiminnon.

    Kirjaaminen luo nimiketapahtumat ja fyysiset inventointitapahtumat. Nimikkeen inventointitapahtumat löydetään avaamalla sen Nimikekortti-sivu. <!--Where are they shown on an item?-->

3. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
4. Määritä tarkistetaan avaamalla nimikkeen Nimikekortti-sivu ja valitsemalla **Inventointitapahtumat**-toiminto. <!--I don't see this action -->

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a><a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a><a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Oletetun varaston laskeminen laajennetuissa varastomäärityksissä

Nimiketapahtumat ja fyysinen varasto synkronoidaan <!--warehouse what?--> ennen inventaarion suorittamista. Muussa tapauksessa inventointipäiväkirjaan ja nimiketapahtumiin tehtävät kirjaukset ovat inventaarion tulokset, joihin on yhdistetty muita nimikkeiden fyysisen varaston muutoksia. Lisätietoja on kohdassa [Määrien synkronoiminen nimiketapahtumissa ja fyysisessä varastossa](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries)

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston inventointipäiväkirja** ja valitse sitten vastaava linkki.  
2. Avaa **F. var. laske varasto** -sivu valitsemalla **Laske varasto** -toiminto.  
3. Määritä suodattimen avulla päiväkirjassa inventoitavat nimikkeet ja valitse sitten **OK**.

   [!INCLUDE [prod_short](includes/prod_short.md)] luo kullekin suodattimen vaatimuksia vastaavalle varastopaikalle rivin. Rivejä voidaan poistaa, mutta tulokset halutaan kirjata inventaarioksi, nimike on laskettava kaikissa varastopaikoista, joihin se sisältyy.  

   Jos nimike lasketaan vain joissakin varastopaikoissa, erot voidaan syöttää ja kirjata ne myöhemmin nimikepäiväkirjaan käyttämällä **Laske f.var. muutos** -toimintoa. <!--I don't see this action-->  

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a><a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a><a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Todellisen lasketun varaston antaminen ja kirjaaminen laajennetuissa varastomäärityksissä

1. Syötä **Fyysisen varaston inventointipäiväkirja** -sivulla todelliset määrät **Määrä (varastotilanne)** -kentässä.  

    > [!NOTE]  
    >  **Määrä (laskettu)** -kenttä täytetään varastopaikkatietueiden perusteella. Tämä määrä kopioidaan kunkin rivin  **Määrän (inventointi)** -kenttään. Jos näiden kenttien määrät eivät ole samoja, syöte todellinen määrä.  

2. Kaikkien todellisten määrien syöttämisen jälkeen valitaan **Rekisteröi**-toiminto.  

    Kun päiväkirja rekisteröidään, [!INCLUDE [prod_short](includes/prod_short.md)] luo fyysisen varaston rekisteriin kaksi fyysisen varastoinnin tapahtumaa kunkin lasketun ja rekisteröidyn rivin osalta:  

    - Jos lasketut ja todelliset määrät eroavat toisistaan, varastopaikalle rekisteröidään negatiivinen tai positiivinen määrä, ja sijainnin muutoksen varastopaikkaan kirjataan vastamäärä.  
    - Jos laskettu määrä on sama kuin inventointimäärä, [!INCLUDE [prod_short](includes/prod_short.md)] arvon **0** sekä varastopaikkaan että muutoksen varastopaikkaan. 

Inventaariota rekisteröitäessä ei kirjata nimike-, varastotilanne- eikä arvotapahtumia. Tietueet ovat kuitenkin tarvittaessa käytettävissä täsmäytystä varten. Määrät pysyvät oikeina, kun tulokset kirjataan kaikki varastopaikkojen nimikkeiden laskennan jälkeen varaston varastotilanteena. <!--physical inventory journal-->. Lisätietoja on kohdassa [Määrien synkronoiminen nimiketapahtumissa ja fyysisessä varastossa](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries)

## <a name="to-do-cycle-counting"></a><a name="to-do-cycle-counting"></a><a name="to-do-cycle-counting"></a>Inventoinnin suorittaminen

Nimikkeet voidaan inventoida aina tarvittaessa. Syynä voi olla esimerkiksi niiden arvo tai se, että nimikkeet liikkuvat nopeasti ja ovat olennainen osa liiketoimintaa. Inventointiväli määritetään määrittämällä nimikkeille inventointikaudet.

Inventointi voidaan tehdä fyysisen varaston määritysten mukaan seuraavasti. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

- Sijainnissa, jossa ohjattu hyllytys ja poiminta ei ole käytössä, käytetään **Inventointipäiväkirja**-sivua. Vaiheet muistuttavat inventaariota, jossa ei tehdä inventointia.  
- Sijainnissa, jossa ohjattu hyllytys ja poiminta on käytössä, käytetään **Fyysisen varaston inventointipäiväkirja**-sivua. Sen jälkeen suoritetaan **Laske fyysisen varaston muutos** -toiminto **Nimikepäiväkirjat**-sivulla. <!--we should say what to do on each of these pages-->  

### <a name="to-set-up-counting-periods"></a><a name="to-set-up-counting-periods"></a><a name="to-set-up-counting-periods"></a>Laskentajaksojen määrittäminen

Inventaarion suorittaminen on tavallisesti tehtävä, joka toistuu esimerkiksi kuukausittain, neljännesvuosittain tai vuosittain. Tarvittavien inventointijaksojen määrittämisen jälkeen niistä yksi määritetään kullekin nimikkeelle. Tämän jälkeen nimikkeille luodaan automaattisesti rivit **Inventointipäiväkirja**-sivun **Laske laskentajakso** -toiminnon avulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastotilanteen laskentajaksot** ja valitse sitten vastaava linkki.  
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a><a name="to-assign-a-counting-period-to-an-item"></a><a name="to-assign-a-counting-period-to-an-item"></a>Laskentajakson määritteleminen nimikkeelle

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Valitse nimike, jolle haluat määrittää laskentajakson.  
3. Valitse **Inventointijakson koodi** -kentässä laskentajakso.  

> [!NOTE]
> Jos laskentajaksoa muutetaan, avautuvassa sanomassa on tietoja muutoksen tuloksista. **Kyllä**-painikkeen valinta vaihtaa koodin ja laskee nimikkeen ensimmäisen laskentajakson. Kun lasket seuraavan kerran inventointipäiväkirjassa laskentajakson, nimike näkyy rivinä **Inventoinnin nimikevalinta** -sivulla. Nimike voidaan sitten laskea kausittain.

### <a name="to-start-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a><a name="to-start-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a><a name="to-start-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Laskennan käynnistäminen laskentakauden perusteella fyysisen varastoinnin perusmäärityksissä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Inventointipäiväkirjat** ja valitse sitten vastaava linkki.
2. Valitse **Laske laskentajakso** -toiminto.

    **Inventoinnin nimikevalinta** -sivulla on näkyvissä nimikkeet, jotka on laskettava laskentajaksojen mukaisesti.
3. Tee inventaario. Lisätietoja on kohdassa [Inventaarion tekeminen](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).

### <a name="to-start-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a><a name="to-start-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a><a name="to-start-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Laskennan käynnistäminen laskentakauden perusteella laajennetuissa varastomäärityksissä

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston inventointipäiväkirja** ja valitse sitten vastaava linkki.  
2. Valitse **Laske laskentajakso** -toiminto.

    **Inventoinnin nimikevalinta** -sivulla on näkyvissä nimikkeet, jotka on laskettava laskentajaksojen mukaisesti.
3. Tee inventaario. Lisätietoja on kohdassa [Inventaarion tekeminen](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).  

   > [!NOTE]  
   > Laske nimike kaikissa varastopaikoissa, joihin se sisältyy. Jos **F. var. inventointi** -sivulla inventoitavaksi noudettuja varastopaikkarivejä poistetaan, laskenta on virheellinen, kun se kirjataan inventointipäiväkirjaan.  

## <a name="to-adjust-the-quantity-of-one-item"></a><a name="to-adjust-the-quantity-of-one-item"></a><a name="to-adjust-the-quantity-of-one-item"></a>Yhden nimikkeen määrän muuttaminen

Kun nimike on laskettu fyysisesti, todellinen varastomäärä kirjataan **Muuta varasto** -toiminnolla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Valitse nimike, jonka varastoa haluat muuttaa, ja valitse sitten **Muuta varastoa** -toimintoa.
3. Syötä inventoinnin tulos **Uusi varasto** -kenttään.
4. Valitse **OK**-painike.

<!-- I don't see a "Quantity on Hand" field on the Item Card page. Should this point to the options for viewing availability?

The item’s inventory is adjusted. The new quantity is shown in the **Quantity on Hand** field on the **Item Card** page.-->

**Muuta varastoa** -toimintoa voi käytätä myös kätevänä tapana lisätä ostetut nimikkeet varastoon, jos ostojen kirjaamiseen ei käytetä ostoja ostolaskuja tai tilauksia. Lisätietoja on kohdassa [Tietueiden ostot](purchasing-how-record-purchases.md).

> [!NOTE]  
> Varaston nykyinen arvo päivitetään, kun sitä on muutettu. Lisätietoja on kohdassa [Varaston uudelleenarvostus](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-quantities-of-multiple-items-in-basic-warehouse-configurations"></a><a name="to-adjust-the-quantities-of-multiple-items-in-basic-warehouse-configurations"></a><a name="to-adjust-the-quantities-of-multiple-items-in-basic-warehouse-configurations"></a>Useiden nimikkeiden määrän muuttaminen fyysisen varastoinnin perusmäärityksissä

**Nimikepäiväkirja**-sivulla nimiketapahtuma voidaan kirjata suoraan ja muuttaa varastoa ostojen, myyntien sekä positiivisten tai negatiivisten muutosten osalta asiakirjoja käyttämättä.

Jos nimikepäiväkirjaan kirjataan usein samoja tai saman tyyppisiä päiväkirjan rivejä esimerkiksi materiaalien kulutukseen osalta, toistuvien toimien suorittamista voidaan helpottaa **Vakionimikepäiväkirja**-sivun avulla. Lisätietoja on kohdassa [Vakiopäiväkirjojen käyttäminen](ui-work-general-journals.md#work-with-standard-journals).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikepäiväkirjat** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Muuta määritä valitsemalla **Kirjaa**-toiminto.

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a><a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a><a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Varastopaikkamäärien muuttaminen laajennetuissa varastomäärityksissä

Jos sijainnissa on käytössä ohjattu hyllytys ja poiminta, **Fyysisen varaston nimikepäiväkirja** -sivulla voi kirjata suunnittelemattomia positiivisia ja negatiivisia määrän muutoksia. Kyse on esimerkiksi puuttuvina kirjatuista nimikkeistä, jotka tulevat odottamatta näkyviin, tai rikkoutumisesta johtuvista tappioista.  

Fyysisen varaston nimikepäiväkirjojen avulla saadaan lisää muutostasoja, jotka tarkentavat määriä. Fyysinen varasto tietää, kuinka paljon nimikkeitä varastossa on ja mihin ne on varastoitu, mutta jokaista muutosta ei ole kirjattu nimiketapahtumiin. Määrän muutos mahdollistaa todellisesta varastosta tehdyt hyvitykset ja veloitukset. Vastakirjaus tehdään muutoksen varastopaikkaan. Muutosvarastopaikka on virtuaalivarastopaikka, jossa ei ole todellisia nimikkeitä. Virtuaalivarastopaikka määritetään **Sijaintikortti**-sivujen **Var. muutosvarastopaikan koodi** -kentässä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimik. uud.luok.pvk** ja valitse sitten vastaava linkki.  
2. Täytä otsikon tiedot.  
3. Valitse nimike rivin **Nimikkeen nro** -kentässä.  
4. Syötä varastopaikka, johon ylimääräisiä nimikkeitä ollaan asettamassa tai josta puuttuu nimikkeet.  
5. Syötä **Määrä**-kenttään positiivinen määrä, jos ylimääräisiä nimikkeitä on löytynyt. Jos nimikkeitä puuttuu, syötä negatiivinen määrä.  
6. Valitse **Rekisteröi**-toiminto.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a><a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a><a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Muutettujen fyysisen varastoinnin tapahtumien ja liittyvien nimiketapahtumien synkronointi

Muutosvarastopaikan tietueet kirjataan määritettyjen jaksojen nimiketapahtumiin. Osa yrityksistä kirjaa muutokset päivittäin nimiketapahtumiin, kun toisissa täsmäytys tehdään harvemmin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikepäiväkirja** ja valitse sitten vastaava linkki.  
2. Kirjoita kunkin päiväkirjarivin kenttien tiedot.  
3. Valitse **Laske fyysisen varaston muutos** -toiminnon muutos ja lisää sitten suodattimen **Laske fyysisen varaston muutos** -sivulle. Muutokset lasketaan vain suodatinvaatimukset täyttäville muutosvarastopaikan tapahtumille.  
4. Täytä **Vaihtoehdot**-pikavälilehden **Asiakirjan nro** -kenttään manuaalisesti syöttämäsi numero. Koska tälle eräajolle ei ole määritetty numerosarjaa, käytä fyysisen varastoinnin määrittämää numeromallia tai syötä päivämäärä (päivä-kuukausi-vuosi) ja sen jälkeen nimikirjaimesi.  
5. Valitse **OK**. Kunkin nimikkeen positiiviset ja negatiiviset muutokset lasketaan yhteen, minkä lisäksi nimikepäiväkirjaan luodaan rivit.  
6. Lisää määräerot nimiketapahtumiin kirjaamalla päiväkirjarivit. Varastopaikkojen ja nimiketapahtuvien varastot vastaavat nyt toisiaan.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/adjust-inventory/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Katso myös

[Varastojen laskenta asiakirjoja käyttämällä](inventory-how-count-inventory-with-documents.md)  
[Varasto](inventory-manage-inventory.md)  
[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
