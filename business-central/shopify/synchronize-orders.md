---
title: Myyntitilausten synkronoiminen ja täyttäminen
description: Määritä ja suorita myyntitilauksen tuonti ja käsittely Shopifysta.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129, 30150, 30151, 30145, 30147'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# <a name="synchronize-and-fulfill-sales-orders"></a>Myyntitilausten synkronoiminen ja täyttäminen

Tässä artikkelissa kuvataan tarvittavat asetukset ja vaiheet, jotka täytyy suorittaa myyntitilausten synkronoimiseksi ja täyttämiseksi Shopifylla [!INCLUDE[prod_short](../includes/prod_short.md)]issa.

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Tilausten tuonnin määrittäminen Shopify-ostoskortissa

Syötä **Valuuttakoodi**, jos verkkokauppa käyttää eri valuuttaa kuin paikallinen valuutta (PVA). Määritetyllä valuutalla on oltava määritettynä vaihtokurssit. Jos verkkokauppa käyttää samaa valuuttaa kuin [!INCLUDE[prod_short](../includes/prod_short.md)], jätä kenttä tyhjäksi. 

Voit nähdä kaupan valuutan [Kaupan tiedot](https://www.shopify.com/admin/settings/general) -asetuksissa Shopify Adminissa. Shopify voidaan määrittää hyväksymään eri valuuttoja, mutta [!INCLUDE[prod_short](../includes/prod_short.md)] -järjestelmään tuodut tilaukset käyttävät kaupan valuuttaa.

Tavallinen Shopify-tilaus voi sisältää välisumman lisäksi muita kustannuksia, kuten kuljetusmaksuja tai tippejä, jos ne ovat käytössä. Nämä summat kirjataan suoraan KP-tilille, jota haluat käyttää tietyille tapahtumatyypeille:

* **Toimitusmaksujen tili**
* **Myytyjen lahjakorttien tili**: lisätietoja on kohdassa [Lahjakortti](synchronize-orders.md#gift-cards)
* **Tippitili**  

Ota käyttöön **Automaattiset tilaukset**, joiden avulla voit luoda myyntiasiakirjoja automaattisesti [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, kun Shopify-tilaus on tuotu.

Jos haluat vapauttaa myyntiasiakirjan automaattisesti, ota käyttöön **Vapauta myyntitilaukset automaattisesti** -valinta.

Jos valitset **Shopify-tilausnro asiakirjarivillä** -kentän, [!INCLUDE [prod_short](../includes/prod_short.md)] lisää **Kommentti**-tyylin myyntirivit Shopify-tilausnumerolla.

>[!NOTE]
>Myyntiasiakirja kohteessa [!INCLUDE[prod_short](../includes/prod_short.md)] linkittyy Shopify-tilaukseen ja voit lisätä **Shopify-tilausnumeron** kentän myyntitilausten, laskujen ja toimitusten luettelo- tai korttisivuille. Saat lisätietoja kentän lisäämisestä siirtymällä kohtaan [Sivun mukauttamisen aloittaminen **Mukauttaminen** -palkin avulla](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode). 

**Veroalueen prioriteetti** -kentässä voit määrittää prioriteetin, miten veroaluekoodi valitaan tilauksen osoitteissa. Tuotu Shopify-tilaus sisältää tietoja veroista. Verot lasketaan uudelleen, kun luot myyntiasiakirjat, joten on tärkeää, että ALV:n/veron asetukset ovat oikein [!INCLUDE[prod_short](../includes/prod_short.md)]-ohjelmassa. Lisätietoja veroista on ohjeaiheessa [Shopify-yhteyden verojen määrittäminen](setup-taxes.md).

Palautusten ja hyvitysten käsittelyn määrittäminen:

* **Tyhjä** määrittää, että palautuksia ja hyvityksiä ei tuoda eikä käsitellä.
* **Vain tuonti** määrittää, että tuot tietoja, mutta luot vastaavan hyvityslaskun manuaalisesti.
* **Luo hyvityslasku automaattisesti** määrittää, että tiedot tuodaan ja [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelma luo hyvityslaskut automaattisesti. Tämän vaihtoehdon valinta edellyttää, että otat käyttöön **myyntitilauksen automaattinen luonti** -vaihtotoiminnon.

Määrittele palautusten sijainti ja KP-tilit tavaroiden ja muiden hyvitysten palautusta varten.

* **Ei-varastoitavat tuotteiden hyvitysten palautustili** - Määrittää sen KP-tilin numeron nimikkeille, jolla ei tarvitse olla varaston korjausta.
* **Palautustili** - Määrittää KP-tilin hyvitetyn kokonaismäärän ja nimikkeiden kokonaismäärän väliselle erolle.

Lisätietoja [Palautuksista ja hyvityksistä](synchronize-orders.md#returns-and-refunds)

### <a name="shipment-method-mapping"></a>Toimitustavan yhdistäminen

**Toimitustavan koodi** Shopifysta tuoduille myyntiasiakirjoille, voidaan täyttää automaattisesti. **Toimitusehdon yhdistämismääritys** täytyy määrittää.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat määrittää kartoituksen avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Lähetystavan kartoitus** -toiminto. Tämä luo automaattisesti tietueet toimitustavoille, jotka on määritetty **Shopify-hallintaportaalisi** [**Toimitus**](https://www.shopify.com/admin/settings/payments)-asetuksissa.
4. **Nimi**-kentässä voit nähdä toimitus tavan nimen Shopifysta.
5. **Syötä toimitusehdon koodi** ja vastaava toimitustapa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

> [!NOTE]  
> Jos myyntitilaukseen liittyy useita toimituskuluja, vain yksi valitaan toimitustavaksi ja liitetään myyntiasiakirjaan.

### <a name="location-mapping"></a>Sijainnin kartta

Sijainnin yhdistämismääritystä tarvitaan, jotta **Sijaintikoodi**-kenttä täytetään myyntiasiakirjojen rivien osalta, jotka on tuotu Shopifysta. Tämä on tärkeää, jos **Sijainti pakollinen** -valitsin on otettu käyttöön **Varaston asetukset** -kortissa, muuten myyntiasiakirjoja ei voi luoda.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat määrittää sijaintien kartoituksen avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Sijainnit** -toiminto, jolla **Shopify-myymäläsijainnit** avataan.
4. Valitse **Hae Shopify-sijainnit** -toiminto, jos haluat tuoda kaikki Shopifyssa määritetyt sijainnit. Voit etsiä niitä [**Sijainnit**](https://www.shopify.com/admin/settings/locations)-asetuksista **Shopify-hallinta** -paneelista. 
5. Syötä **oletussijaintikoodi** ja vastaava sijainti [!INCLUDE[prod_short](../includes/prod_short.md)]issa.

> [!NOTE]  
> Sijainnin yhdistämismääritystä käytetään myös varaston synkronointiin. Lisätietoja on kohdassa [Synkronoi varasto Shopifyhin](synchronize-items.md#sync-inventory-to-shopify).
  
## <a name="run-the-order-synchronization"></a>Suorita tilausten synkronointi

Seuraavassa kuvataan, miten myyntitilaukset tuodaan ja päivitetään.

> [!NOTE]  
> Arkistoituja tilauksia Shopify ei voi tuoda. Poista **Arkistoi tilaus automaattisesti** -valinta käytöstä **Shopify-hallintapaneelin** **Kassa**-asetusten **Tilauksen käsitteleminen** -osiosta varmistaaksesi, että kaikki tilaukset tuodaan [!INCLUDE[prod_short](../includes/prod_short.md)]iin. Jos sinun täytyy tuoda arkistoituja tilauksia, käytä **Shopify-hallintapaneelin** [Tilaukset](https://www.shopify.com/admin/orders)-sivun **Palauta tilauksia arkistosta** -toimintoa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat tuoda tilauksia avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Tilaukset**-toiminto.
4. Valitse **Synkronoi tilaukset Shopifysta** -toiminto.
5. Määritä tilausten suodattimet tarpeen mukaan. Voit esimerkiksi tuoda kokonaan maksetut tilaukset tai ne, joiden riskitaso on alhainen.

> [!NOTE]  
> Kun suodatat tunnisteen mukaan, käytä suodatintunnuksia `@` ja `*`. Jos esimerkiksi haluat tuoda tilauksia, joissa on *tag1*, käytä `@*tag1*`. `@` varmistaa, että tulos ei riipu kirjainkoosta, kun taas `*` etsii tilauksia, joissa on useita tunnisteita.

6. Valitse **OK**-painike.

Vaihtoehtoisesti voit etsiä **synkronoituja tilauksia Shopifysta** -erätyötä.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoittaminen](background.md#to-schedule-recurring-tasks).

### <a name="under-the-hood"></a>Pinnan alla

Shopify-yhdistin tuo tilaukset kahdessa vaiheessa:

1.  Se tuo tilausotsikot **Tuotavat Shopify-tilaukset** -taulukkoon, kun ne vastaavat tiettyjä ehtoja:
    
* Niitä ei arkistoida. Tämä tarkoittaa, että voit sisällyttää tilaukset synkronointiin tai jättää ne pois synkronoinnin ulkopuolelle arkistoimalla tai avaamalla ne Shopify-järjestelmänvalvojassa.
* Ne on luotu tai muokattu edellisen synkronoinnin jälkeen. Tämä tarkoittaa sitä, että voit pakottaa tietyn tilauksen uudelleentuonnin, jos muutat tilausta, esimerkiksi lisäämällä **Muistiot** tai **Tunnistetiedot**.

2.  Se tuo Shopify-tilauksia ja lisätietoja.
* Shopify-yhdistin käsittelee kaikki ne **Tuotavat Shopify-tilaukset** -taulukon tietueet, jotka vastaavat **Synkronoi tilauksia Shopifysta** -pyyntösivulla määritettyjä suodatinperusteita. Esimerkiksi tunnisteet, kanava tai täyttämisen tila. Jos et ole määrittänyt suodattimia, se käsittelee kaikki tietueet.
* Kun tuot Shopify-tilausta, Shopify-yhdistin pyytää lisätietoja Shopifysta:

    * Tilauksen otsikko
    * Tilausrivit
    * Toimitus- ja täyttämistiedot
    * Tapahtumat
    * Palautukset ja hyvitykset, jos ne on määritetty

**Tuotava Shopify-tilaus** -sivu on hyödyllinen tilausten tuontiongelmien vianmäärityksessä. Voit arvioida saatavilla olevat tilaukset ja tehdä seuraavat vaiheet:

* Tarkista, estääkö virhe tietyn tilauksen tuonnin, ja tutki virheen tietoja. Valitse **sisältää virheen** -kenttä.
* Käsittele vain tiettyjä tilauksia. Sinun täytyy täyttää **kauppakoodi**-kenttä, valita vähintään yksi tilaus ja valita sitten **Tuo valitut tilaukset** -toiminto.
* Poista tilaukset **Tuotava Shopify-tilaus** -sivusta, jos haluat jättää ne synkronoinnin ulkopuolelle.

## <a name="review-imported-orders"></a>Tuotujen tilausten tarkistaminen

Kun tuonti on valmis, voit tutkia Shopify-tilausta ja löytää kaikkia siihen liittyvät tiedot, kuten maksutapahtumat, toimituskulut, riskitason, muut määritteet ja tunnisteet tai täydennykset, jos tilaus oli jo täytetty Shopifyssa. Voit myös tarkastella mitä tahansa asiakkaalle lähetettyä tilausvahvistusta valitsemalla **Shopify-tilasivu**-toiminnon.

> [!NOTE]  
> Voit siirtyä **Shopify-tilaukset**-ikkunaan suoraan, jolloin näet tilaukset, joissa on *avoin* tila kaikista kaupoista. Jos haluat tarkastella valmiita tilauksia, sinun täytyy avata **Shopify-tilaukset**-sivu tietystä **Shopify-ostoskortti**-ikkunasta.

## <a name="create-sales-documents-in-business-central"></a>Luo myyntiasiakirjoja Business Centralissa

Jos **Tilausten automaattinen luominen**-vaihto on otettu käyttöön **Shopify-ostoskortissa**, [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelma yrittää luoda myyntiasiakirjan, kun tilaus tuodaan. Jos sinulla esiintyy ongelmia, kuten jos asiakas tai tuote puuttuu, sinun täytyy korjata ongelmat ja luoda myyntitilaus uudelleen.

### <a name="to-create-sales-documents"></a>Myyntiasiakirjojen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Shopify-kaupat**, valitse sitten vastaava linkki.
2. Valitse kauppa, jolle haluat synkronoida tilaukset avataksesi **Shopify-kauppa-kortti**-sivun.
3. Valitse **Tilaukset**-toiminto.
4. Valitse tilaus, jolle haluat luoda myyntiasiakirjan ja valitse **Luo myyntiasiakirjat** -toiminto.
5. Valitse **Kyllä**.

Jos Shopify-tilaus edellyttää täyttämistä, **myyntitilaus** luodaan. Täytettyjen Shopify-tilausten, kuten vain lahjakortin sisältävien tilausten tai jo Shopifyssa käsiteltyjen tilausten, osalta luodaan **Myyntilasku**.

Myyntiasiakirja luodaan nyt, ja sitä voidaan hallita [!INCLUDE[prod_short](../includes/prod_short.md)]in vakiotoimintojen avulla.

### <a name="manage-missing-customers"></a>Puuttuvien asiakkaiden hallinta

Jos asetuksesi estävät asiakkaan luomisen automaattisesti ja sopivaa asiakasta ei löydy, sinun täytyy kohdistaa asiakas Shopify-tilaukseen manuaalisesti. Voit tehdä tämän muutamalla eri tavalla:

* Voit määrittää **Myyntiasiakasnron** ja **Laskutusasiakkaan nron** suoraan **Shopify-tilaukset**-sivulta valitsemalla asiakkaan olemassa olevien asiakkaiden luettelosta.
* Voit valita asiakasmallin koodin ja luoda ja kohdistaa asiakkaan sitten **Shopify-tilaukset**-sivun **Luo uusi asiakas** -toiminnolla. Huomaa, että Shopify-asiakkaalla täytyy olla vähintään 1 osoite. Shopify-myyntipisteen kautta luoduista tilauksista puuttuvat usein osoitetiedot.
* Voit yhdistää aiemmin luodun asiakkaan **Shopify-asiakkaaseen** **Shopify-asiakas**-ikkunassa ja valita sitten **Shopify-tilaukset** -sivulla **Etsi yhdistämismääritys** -toiminto.

### <a name="how-the-connector-chooses-which-customer-to-use"></a>Miten yhdistin valitsee käytettävän asiakkaan

*Tuo tilaus Shopifysta* -toiminto yrittää valita asiakkaat seuraavassa järjestyksessä:

1. Jos **Oletusasiakasnro** -kenttä määritetään **Shopify-asiakasmallissa**, **Lähettäjämaa/-aluekoodille**, silloin **oletusasiakasnroa** käytetään, riippumatta **asiakkaan tuonti Shopifysta** ja **Asiakkaan yhdistämismäärityksen tyyppi** -kentistä. Lisätietoja kohdassa [Asiakasmalli maata kohti](synchronize-customers.md#customer-template-per-countryregion).
2. Jos **Asiakkaan tuonti Shopifysta** on määritetty arvoon *Ei mitään* ja **Oletusasiakasnro** on määritetty **Shopify-ostoskortti**-sivulla, sitten **Oletusasiakasnro** käytetään.

Seuraavat vaiheet määräytyvät **asiakkaan yhdistämismäärityksen tyypin** mukaan.

* Jos se on **Ota aina oletusasiakas**, silloin yhdistin käyttää asiakasta, joka on määritetty kohdassa **oletusasiakasnro** -kentässä **Shopify-ostoskortti**-sivulla.
* Jos se on **Sähköpostilla/puhelimella**-yhdistin yrittää löytää nykyisen asiakkaan ensin tunnuksella, sitten sähköpostitse, ja sitten puhelinnumeron avulla. Jos asiakasta ei löydy - yhdistin luo uuden asiakkaan.
* Jos se on **Laskutustiedoilla**, yhdistin yrittää löytää olemassa olevan asiakkaan ensin tunnuksella ja sitten laskutusosoitteen tiedoilla. Jos asiakasta ei löydy - yhdistin luo uuden asiakkaan.

> [!NOTE]  
> Yhdistin käyttää laskutusosoitteen tietoja ja luo laskutusasiakkaan [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Tilausasiakas on sama kuin laskutusasiakas.

### <a name="different-processing-rules-for-orders"></a>Tilausten eri prosessisäännöt

Haluat ehkä käsitellä tilauksia eri tavalla säännön mukaan. Esimerkiksi tietyn myyntikanavan tilaukset (kuten POS) käyttävät oletusasiakasta, mutta haluat, että verkkokaupassa on todellista tietoa asiakkaasta.

Eräs tapa korjata tämä vaatimus on luoda ylimääräinen Shopify-kauppakortti ja käyttää suodattimia **Synkronoi tilaukset Shopifysta** -pyyntösivulta.

Esimerkki: sinulla on verkkokauppa sekä Shopify-myyntipiste. Haluat käyttää kiinteätä asiakasta myyntipisteelle, mutta luoda asiakkaita verkkokaupalle [!INCLUDE[prod_short](../includes/prod_short.md)]-ohjelmassa. Seuraavassa on luettelo ylätason vaiheista. Saat lisätietoja siirtymällä vastaaviin ohjeartikkeleihin.

1. Luo Shopify-myymälä nimeltä *KAUPPA* ja linkitä se Shopify-tiliisi.
2. Määritä nimikkeen tai tuotteen synkronointi, jotta tämä säilö hallitsee tuotetietoja.
3. Määrittää, että asiakkaat tuodaan tilausten mukana. Yhdistimen tulisi löytää asiakkaat etsimällä heidän sähköposti osoitteitaan. Jos osoitetta ei löydy, ohjelma käyttää asiakasmallia uuden asiakkaan luomiseen.
4. Luo Shopify-myymälä nimeltä *POS* ja linkitä se samaan Shopify-tiliin.
6. Varmista, että nimikkeen tai tuotteen synkronointi on poistettu käytöstä.
7. Valitse oletusasiakasta käyttävä yhdistin.
8. Luo toistuva työjonotapahtuma raportille 30104 **Synkronoi tilauksia Shopifysta**. Valitse **Shopify-kauppakoodi** **KAUPPA**-kentässä ja käytä suodattimia, kun haluat löytää kaikki tilaukset paitsi ne, jotka POS-myyntikanava luo. Esimerkiksi **<>-myyntipiste**
9. Luo toistuva työjonotapahtuma raportille 30104 **Synkronoi tilauksia Shopifysta**. Valitse **Shopify-kauppakoodi**-kentästä **POS** ja käytä suodattimia POS-myyntikanavan tuottamien tilausten keräämiseen. Esimerkiksi **Myyntipiste**.

Kukin työjono tuo ja käsittelee määritettyjen suodattimien tilaukset ja käyttää vastaavan Shopify-kauppakortin sääntöjä. He esimerkiksi luovat myyntitilauspisteen oletusasiakkaalle.

>[!Important]
> Jos haluat välttää ristiriitoja tilausten käsittelyssä, muista käyttää samaa työjonoluokkaa molemmissa työjonotapahtumissa.

### <a name="impact-of-order-editing"></a>Tilausten muokkaamisen vaikutus

Shopifyssa:

|Muokkaa|Vaikutus jo tuotuun tilaukseen|Vaikutus ensimmäisen kerran tuotavaan tilaukseen|
|------|-----------|-----------|
|Muuta täyttämissijaintia | Alkuperäinen sijainti on riveillä | Täyttämissijainti on synkronoitu kohteeseen [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Muokkaa tilausta ja lisää määrää| Tilausotsikko ja lisätaulukot päivittyvät [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, rivit eivät.| Tuotu tilaus käyttää uutta määrää|
|Muokkaa tilausta ja pienennä määrää| Tilausotsikko ja lisätaulukot päivittyvät [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, rivit eivät.| Tuotu tilaus käyttää alkuperäistä määrää, Jaettava määrä -kentässä on uusi arvo.|
|Muokkaa tilausta ja poista olemassa oleva nimike | Tilausotsikko ja lisätaulukot päivittyvät [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa, rivit eivät.| Poistettu nimike tuodaan edelleen, Jaettava määrä -kentässä on nolla. |
|Muokkaa tilausta ja lisää uusi nimike | Tilausotsikko päivittyy, rivit eivät. | Alkuperäiset ja lisätyt nimikkeet tuodaan. |
|Käsittele tilaus: täytä, päivitä maksutiedot | Tilausotsikko päivittyy, rivit eivät. |Muutoksella ei ole vaikutusta siihen, miten tilaus tuodaan.|
|Peruuta tilaus | Tilausotsikko päivittyy, rivit eivät. |Peruutettua tilausta ei ole tuotu |

Kuten näet, joissakin tapauksissa voi olla kohtuullista poistaa muokattu tilaus [!INCLUDE[prod_short](../includes/prod_short.md)]-ohjelmasta ja tuoda se uutena tilauksena.

[!INCLUDE[prod_short](../includes/prod_short.md)]issa:

|Muokkaa|Vaikutus|
|------|-----------|
|Muuta sijainti toiseen sijaintiin, joka on kartoitettu Shopify-sijainteihin. Kirjaa toimitus. | Tilaus merkitään täytetyksi. Alkuperäistä sijaintia käytetään. |
|Muuta sijainti toiseen sijaintiin, jota ei ole kartoitettu Shopify-sijainteihin. Kirjaa toimitus. | Täydennystä ei synkronoida Shopifyn kanssa. |
|Vähennä määrää. Kirjaa toimitus. | Shopify-tilaus merkitään osittain täytetyksi. |
|Lisää määrää. Kirjaa toimitus. | Täydennystä ei synkronoida Shopifyn kanssa. |
|Lisää uusi nimike. Kirjaa toimitus. | Shopify-tilaus merkitään täytetyksi. Rivejä ei päivitetä. |

## <a name="synchronize-shipments-to-shopify"></a>Synkronoi toimitukset Shopifyhin

Kun Shopify-tilauksesta luotu myyntitilaus toimitetaan, voit synkronoida toimitukset Shopifyn kanssa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 1.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Synkronoi toimitukset Shopifyhin**, valitse sitten vastaava linkki.
2. Määritä toimitusten suodattimet tarpeen mukaan. Voit esimerkiksi päivittää tiettynä päivämääränä kirjatun toimituksen.
3. Valitse **OK**-painike.

Tilaus Shopifyssa merkitään täytetyksi. Asiakas saa automaattisesti toimitusilmoituksen sähköpostilla tai tekstiviestillä. Jos toimitukselle on määritetty kuljetusliike ja seurantakoodi, sähköposti sisältää seurantatiedot.

Vaihtoehtoisesti voit käyttää **Synkronoi toimitukset** -toimintoa Shopifyn myyntitilauksissa tai Shopifyn myyntisivuilla.

Voit ajoittaa tehtävän suoritettavaksi automaattisesti. Lisätietoja on kohdassa [Toistuvien tehtävien ajoittaminen](background.md#to-schedule-recurring-tasks).

>[!Important]
>Kirjatulla toimitusrivillä olevalla sijainnilla, myös tyhjällä sijainnilla, täytyy olla vastaava Shopify-sijainti. Muussa tapauksessa tätä riviä ei lähetetä takaisin Shopifyhin. Lisätietoja on kohdassa [Sijainnin yhdistämismääritys](synchronize-orders.md#location-mapping).

Muista suorittaa **Synkronoi tilaukset Shopifysta** -toiminto päivittääksesi tilauksen jakelun tilan [!INCLUDE[prod_short](../includes/prod_short.md)]issa. Yhdistintoiminto arkistoi myös täysin maksetut ja täytetyt tilaukset sekä Shopifyssa että [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa edellyttäen, että ehdot täyttyvät. 

### <a name="shipping-agents-and-tracking-url"></a>Kuljetusliikkeet ja seuranta-URL-osoite

Jos **Kirjattu myyntitoimitus** -asiakirja sisältää **Kuljetusliikkeen koodi**- ja/tai **Kollin seurantanro** -kentän, nämä tiedot lähetetään Shopify'hin ja asiakkaalle toimituksen vahvistussähköpostissa.

Seurantayritys-kenttä täytetään seuraavassa järjestyksessä (suurimmasta pienimpään) kuljetusliikkeen tietueen perusteella:

* **Shopify-seurantayritys**
* **Nimi**
* **Koodi**

Jos kuljetusliikkeen tietueen **Paketin seurannan URL-osoite** -kenttä on täytetty, toimitusvahvistus sisältää myös seuranta-URL-osoitteen.

## <a name="returns-and-refunds"></a>Palautukset ja hyvitykset

Shopifyn ja [!INCLUDE[prod_short](../includes/prod_short.md)]-ohjelman integroinnissa on tärkeää pystyä synkronoimaan mahdollisimman paljon liiketoimintatietoja. Tämän ansiosta rahoitus- ja varastotasot on helpompi pitää ajan tasalla [!INCLUDE[prod_short](../includes/prod_short.md)]-ohjelmassa. Synkronoitava data sisältää palautuksen ja hyvityksen, jotka tallennettiin Shopifyn järjestelmänvalvojan tai Shopify POS:in avulla.

Palautukset ja hyvitykset tuodaan niihin liittyvien tilausten yhteydessä, jos olet ottanut käsittelytyypin käyttöön Shopify-kauppakortissa.

Palautukset tuodaan vain tiedoksi. Niihin ei liity prosessilogiikkaa.

Rahoitus- ja tarvittaessa varastotapahtumat käsitellään palautusten avulla. Hyvitykset voivat sisältää tuotteita tai vain summia, esimerkiksi jos kauppias on päättänyt hyvittää kuljetusmaksuja tai muun summan.
Voit luoda myyntihyvityslaskuja hyvityksille. Hyvityslaskuissa voi olla seuraavan tyyppisiä rivejä:

|Tyyppi|Nro|Kommentti|
|-|-|-|
|KP-tili|Myytyjen lahjakorttien tili| Käytä lahjakortteihin liittyviin hyvityksiin.|
|KP-tili|Ei varastossa -hyvitystili | Käytä palautuksiin, jotka liittyvät tuotteisiin, joita ei ole varastoitu. |
|Vaihtoehto |Nimikenro| Käytä palautuksiin, jotka liittyvät tuotteisiin, jotka oli varastoitu. Voimassa suoriin hyvityksiin ja hyvityksiin liittyvinä hyvityksinä. Luotto-lisärivin sijaintikoodi asetetaan palautuspaikaksi valitun arvon perusteella.|
|KP-tili| Hyvitystili | Käytä muihin palautettaviin määriin, jotka eivät liity tuotteisiin tai lahjakortteihin. Voit esimerkiksi määrittää palautukseen käytettävän summan manuaalisesti Shopifyssa. |

>[!Note]
>Luotuun hyvityslaskuun käytetään palautussijaintia, myös tyhjiä sijainteja, jotka on määritetty **Shopifyn kauppakortissa**. Järjestelmä ei ota huomioon alkuperäisiä sijainteja tilauksista tai toimituksista.

## <a name="gift-cards"></a>Lahjakortit

Voit myydä Shopify-kaupassa lahjakortteja, joita voidaan käyttää oikeiden tuotteiden maksamiseen.

Kun on kyse lahjakorteista, on tärkeää syöttää **myydyn lahjakortin tili** -kenttään arvo **Shopify-ostoskortti**-ikkunassa. Myyty lahjakortti synkronoidaan yhdessä rivintilausten kanssa. Kohdistettu lahjakortti tuodaan myös tilauksen mukana, mutta nyt tapahtumana. Huomaa, että lahjakortti ei vähennä laskun summaa.

Jos haluat tarkastella myönnettyjä ja käytettyjä lahjakortteja, valitse ![Kerro-ominaisuuden avaava Hehkulamppu.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Lahjakortit**, valitse sitten vastaava linkki.

## <a name="see-also"></a>Katso myös

[Shopifyn yhdistimen käytön aloittaminen](get-started.md)  
