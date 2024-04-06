---
title: Tietojen analysoiminen luettelosivuilla ja kyselyissä tietojen analysointitilan avulla
description: Opettele analysoimaan tietoja Business Centralin tietojen analysointitilan avulla.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 12/08/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-page-and-query-data-using-data-analysis-mode"></a>Luettelosivun ja kyselyn tietojen analysoiminen tietojen analysointitilan avulla

> **KOHDISTETAAN:** Business Central 2023 -julkaisuaallon 1 ja sitä uudemman julkinen esikatselu luettelosivujen analysointia varten; Yleisesti käytettävissä Business Central 2023 -julkaisuaallossa 2, kun haluat analysoida luettelosivujen ja kyselyjen tietoja.

Tässä artikkelissa opit analysoimaan tietoja luettelosivuilta ja kyselyistä *tietojen analysointitilan* avulla. Tietojen analysointitilan avulla voit analysoida tietoja suoraan sivulta ilman, että sinun tarvitsee ajaa raporttia tai vaihtaa muuhun sovellukseen, kuten Exceliin. Se tarjoaa vuorovaikutteisen ja monipuolisen tavan laskea, tiivistää ja tarkastella tietoja. Sen sijaan, että raportteja suoritetaan eri vaihtoehdoilla ja suodattimilla, voit lisätä useita välilehtiä, jotka edustavat erilaisia tehtäviä tai näkymiä tiedoista. Esimerkkejä voivat olla Omat asiakkaat, Seurantanimikkeet, Äskettäin lisätyt toimittajat, Myyntitilastot tai mikä tahansa muu näkymä, jonka voi kuvitella.

> [!TIP]
> Tietojen analysointitilassa on se hyvä puoli, että se ei muuta luettelosivun tai kyselyn taustatietoja tai sivun asettelua, kun se ei ole tietojen analysointitilassa. Joten paras tapa oppia, mitä voit tehdä tietojen analysointitilassa on kokeilla asioita.

## <a name="prerequisites"></a>Vaatimukset

- Jos käytössä on Business Centralin versio 22, tietojen analysointitila on esiversio. Järjestelmänvalvojan on siis otettava se käyttöön, ennen kuin sitä voi alkaa käyttää. Voit ottaa sen käyttöön siirtymällä **Ominaisuuksien hallinta** -sivulle ja ottamalla käyttöön **Ominaisuuden päivitys: analyysitila, analysoi tiedot nopeasti suoraan Business Centralin avulla**. [Lue lisää kohdasta Ominaisuuksien hallinta](/dynamics365/business-central/dev-itpro/administration/feature-management).
- Versiossa 23 ja sitä uudemmissa versioissa tilillesi on määritettävä **DATA ANALYSIS - EXEC** -käyttöoikeuksien joukko tai sisällytettävä järjestelmän objektin **9640 Salli tietojen analysointitila** -suoritusoikeus. Järjestelmänvalvojana voit jättää nämä käyttöoikeudet pois käyttäjiltä, jotka eivät halua käyttää analyysitilaa.

> [!NOTE]
> Saatat huomata joitakin luettelosivuja, joissa ei ole **Analysoi**-valitsinta, jotta siirrytään analyysitilaan. Tämän vuoksi kehittäjät voivat poistaa tiettyjen sivujen analyysitilan käytöstä AL-taulukon [AnalysisModeEnabled-ominaisuuden](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) avulla.

## <a name="get-started"></a>Aloittaminen

1. Avaa luettelosivu tai kysely.

   Voit esimerkiksi käsitellä **Asiakastapahtumat**-sivua valitsemalla ![Suurennuslasin, joka avaa Kerro minulle -ominaisuuden](media/ui-search/search_small.png). -kuvake (<kbd>Alt</kbd>+<kbd>Q</kbd>), syötä *asiakastapahtumat* ja valitse sitten vastaava linkki. 

2. Ota käyttöön **analysoi**-vaihtokytkin sivun yläosan toimintopalkissa.

    Tietojen analysointitila avaa tiedot kokemukseen, joka on optimoitu tietojen analysointia varten.  Tietojen analysointi -tilassa normaali toimintopalkki korvataan erityisellä tietojen analysointitilan rivillä. Seuraava kuva havainnollistaa sivun eri alueita tietojen analysointitilassa.

   [![Näyttää yhteenvedon tietojen analysointitilassa olevasta sivusta](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Jokainen alue selitetään seuraavissa osissa.

3. Käytä eri alueita tietojen muokkaamiseen, yhteenvetojen tekemiseen ja analysointiin. Katso lisätietoja seuraavissa osissa.

4. Kun haluat poistua analysointitilasta, ota **Analysoi**-vaihtokytkin pois käytöstä.

   Lisäämäsi analyysivälilehdet säilyvät, kunnes poistat ne. Joten jos palaat tietojen analysointitilaan uudelleen, näet ne juuri sellaisina kuin ne jätit.

> [!NOTE]
> Analyysitilassa näkyviä tietoja ohjataan luettelosivulla määritettyjen suodattimien tai näkymien avulla. Tämän ansiosta voit suodattaa tiedot ennen analyysitilan syöttämistä.

## <a name="work-with-data-analysis-mode"></a>Tietojen analysointitilan käsitteleminen

Tietojen analysointitilassa sivu on jaettu kahteen alueeseen:

- Pääalue, joka koostuu tietoalueesta (1), yhteenvetopalkista (2) ja välilehtipalkista (5)
- Tietojenkäsittelyalue, joka koostuu kahdesta ruudusta: sarakkeet (3) ja analyysisuodattimet (4).

### <a name="data-area-1"></a>Tietoalue (1)

Tietoalue näyttää luettelosivun kyselyn rivit ja sarakkeet, ja tiedoista tehdään yhteenveto. Tietoalue tarjoaa monipuolisen tavan hallita sarakkeiden asettelua ja nopean tavan saada yhteenveto tiedoista. Numeerisia arvoja sisältävissä sarakkeissa sarakkeen kaikkien arvojen summa näkyy viimeisellä rivillä, ellet ole määrittänyt riviryhmiä. Tässä tapauksessa summat näkyvät ryhmien välisumina.  

![Näyttää sivun tietoalueen yleiskuvan tietojen analysointitilassa](media/analysis-mode-data-area.png)

- Jos haluat siirtää sarakkeen, valitse se ja vedä se analyysisi kannalta järkevimpään paikkaan.
- Lajittele sarakkeessa valitsemalla sarakkeen otsikko. Jos haluat lajitella useita sarakkeita, pidä <kbd>Vaihto</kbd>-näppäintä painettuna samalla, kun valitset sarakeotsikot, joiden mukaan haluat lajitella.
- Napsauta saraketta hiiren kakkospainikkeella tai siirrä osoitin sen päälle ja valitse valikkokuvake ![Näyttää tietojen analyysitilassa sarakkeen kuvakkeen, joka avaa toimintojen valikon](media/analysis-mode-column-menu-icon.png) käyttääksesi useita toimintoja, joita voit tehdä sarakkeissa. Esimerkiksi:

  - Jos haluat kiinnittää sarakkeen tietoalueen vasempaan tai oikeaan reunaan niin, että se ei siirry pois näytöstä vieritettäessä, valitse ![Näyttää kuvakkeen sarakkeessa tietojen analysointitilassa, joka avaa toimintojen valikon](media/analysis-mode-column-menu-icon.png) > **PIN-koodin sarake** > **PIN-koodi vasen** -sarakkeen osa.
  - Määritä tietosuodattimet suoraan sarakemääritykseen **analyysisuodattimet**-ruutujen sijaan. Voit vielä tarkastella tietoja asiaan liittyvistä tiedoista ja kustakin rivistä sekä avata kortin ja lukea lisätietoja tietystä kohteesta.
- Käytä tietoaluetta tietojen vuorovaikutukseen. Sarakkeissa, jotka sisältävät numeerisia arvoja, voit saada kuvaavia tilastoja kenttäjoukosta merkitsemällä ne. Tilastotiedot näkyvät sivun alaosassa tilarivillä (2).
- Vie tiedot Excel- tai csv-muodossa. Napsauta hiiren kakkospainikkeella tietoaluetta tai valittua solua, johon vienti tehdään.

### <a name="summary-bar-2"></a>Yhteenvetopalkki (2)

Yhteenvetopalkki on sivun alaosassa, ja se näyttää luettelosivun tai kyselyn tietoja koskevat tilastotiedot. Kun käytät sarakkeita, joiden arvot voidaan tiivistää, kuten useiden rivien valitseminen sarakkeista, jotka näyttävät summat, tiedot päivitetään.

![Näyttää yhteenvedon tietojen analysointitilassa olevasta yhteenvetopalkista](media/analysis-mode-totals-row.png)

Seuraavassa taulukossa kuvataan kokonaissummat-alueessa näkyvät numerot:

|Luku|Kuvaus|
|-|-|
|Rivit|Valittujen rivien määrä osana käytettävissä olevien rivien kokonaismäärää. |
|Rivejä yhteensä|Suodattamattoman luettelon tai kyselyn rivien määrä.|
|Suodatettu|Luetteloon tai kyselyyn kohdistettujen suodattimien tuloksena näkyvien rivien määrä.|
|Keskiarvo|Kaikkien valittujen yhteenlaskettavien kenttien keskimääräinen arvo.|
|Määrä|Valittujen rivien määrä.|
|Min.|Kaikkien valittujen yhteenlaskettavien kenttien vähimmäisarvo.|
|Maks.|Kaikkien valittujen yhteenlaskettavien kenttien enimmäisarvo.|
|Summa|Kaikkien valittujen yhteenlaskettavien kenttien arvojen kokonaissumma.|

### <a name="columns-3"></a>Sarakkeet (3)

**Sarakkeet** on toinen kahdesta ruudusta, jotka toimivat yhdessä määrittääkseen analyysin. Toinen alue on **Analyysisuodattimet**-ruutu. **Sarakkeet**-ruutua käytetään tietojen yhteenvetoon. **Sarakkeet**-ruudun avulla voit määrittää, mitkä sarakkeet sisällytetään analyysiin.

![Näyttää sarakeruudun yleiskuvan tietojen analysointitilassa](media/analysis-mode-columns-2.png)

|Alueet|Kuvaus|
|-|-|
|Etsi/tarkista tai tyhjennä kaikki ruudut|Hae sarakkeita. Merkitse valintaruutu valitaksesi/tyhjentääksesi kaikki sarakkeet.|
|Valintaruudut|Tämä alue sisältää jokaisen luettelon tai kyselyn lähdetaulukon kentän valintaruudun. Tämän alueen avulla voit muuttaa näkyvät sarakkeet. Valitse valintaruutu, jos haluat näyttää sivun kentän sarakkeen. Piilota sarake poistamalla valintaruudun valinta. |
|Riviryhmät|Tämän alueen avulla voit ryhmitellä ja laskea yhteen tai useampaan kenttään tietoja. Voit sisällyttää vain muita kuin numeerisia kenttiä, kuten tekstiä, päivämäärä- ja kellonaikakenttiä. Riviryhmiä käytetään usein pivot-tilassa.|
|Arvot|Tämän alueen avulla voit määrittää kentät, joille haluat laskea summan. Voit sisällyttää vain sellaiset kentät, jotka sisältävät numeroita, jotka voidaan laskea yhteen. Esimerkiksi ei teksti-, päivä määrä- tai kellonaikakenttä.|

Jos haluat siirtää kentän yhdeltä alueelta toiselle, valitse sieppauskuvake ![Näyttää yhteenvedon analysointitilassa olevasta sivusta](media/column-grab-icon.png) luettelon sarakkeen viereen ja vedä kohde alueelle. Et voi siirtää kenttää alueelle, jossa sitä ei sallita.

### <a name="analysis-filters-4"></a>Analyysisuodattimet (4)

**Analyysisuodattimet**-ruudun avulla voit määrittää lisää sarakkeita, jotka rajoittavat luettelon tietoja. Määritä sarakkeiden suodattimet rajoittamaan luettelo- ja seuraavien summien arvot vain niihin tapahtumiin, joista olet kiinnostunut määrittämiesi kriteerien perusteella. Oletetaan esimerkiksi, että olet kiinnostunut vain tietyn summan ylittävien asiakkaiden tai myyntitilausten tiedoista. Jos haluat asettaa suodattimen, valitse sarake, valitse vertailuoperaatio luettelosta (kuten **yhtä kuin** tai **alkaa**) ja syötä sitten arvo.

![Näyttää suodatinruudun yleiskuvan analysointitilassa](media/analysis-mode-filters.png)

> [!NOTE]
> Lisäsuodattimet koskevat vain nykyistä analyysivälilehteä. Tämän ansiosta voit määrittää juuri ne ylimääräiset tietosuodattimet, joita tarvitaan tietyssä analyysissä.

### <a name="tabs-5"></a>Välilehdet (5)

Yläosassa olevien välilehtien alueen avulla voit luoda eri kokoonpanoja (sarakkeita ja analyysisuodattimia) erillisiin välilehtiin, joissa voit käsitellä välilehtien tietoja itsenäisesti. Oletusarvoisesti aina on vähintään yksi välilehti eli **Analyysi 1**. Välilehtien lisääminen on hyödyllistä usein käytettyjen analyysimääritysten tallentamiseen tietojoukossa. Sinulla voi olla esimerkiksi sarkaimia pivot-tilan tietojen analysointia varten ja muita sarkaimia, jotka suodattavat rivien alijoukkoon. Jotkin välilehdet saattavat näyttää yksityiskohtaisen näkymän, jossa on useita sarakkeita, ja toisissa on vain muutamia avainsarakkeita.

Tässä on joitain vinkkejä useiden analyysivälilehtien käyttämiseen:

- Jos haluat lisätä uuden välilehden, valitse viimeisen analyysivälilehden vieressä oleva suuri **+**-merkki.
- Valitse välilehdellä alanuoli, kun haluat avata välilehdessä tehtävät toimet, kuten nimetä uudelleen, monistaa, poistaa ja siirtää.

   - **Delete** poistaa avoinna olevan välilehden. **Poista kaikki** poistaa kaikki lisäämäsi välilehdet, paitsi oletusvälilehden **Analyysi 1**.
- Et voi poistaa **Analyysi 1**:tä kokonaan, mutta voit nimetä sen uudelleen käyttämällä **Nimeä uudelleen** -toimintoa ja poistamalla tekemäsi muutokset **Poista**- tai **Poista kaikki** -toiminnolla.  

- Lisäämäsi ja määrittämäsi analyysivälilehdet säilyvät, kunnes poistat ne. Joten jos palaat tietojen analysointitilaan uudelleen, näet ne juuri sellaisina kuin ne jätit.

   > [!TIP]
   > Määrittämäsi välilehdet näkyvät vain sinulle. Muut käyttäjät näkevät vain määrittämäsi välilehdet.
- Voit kopioida analyysivälilehtiä. Kopioiminen voi olla hyödyllistä, jos haluat kokeilla välilehden muuttamista alkuperäistä muuttamatta tai jos haluat luoda eri muunnelmia samasta analyysista.


## <a name="date-hierarchies"></a>Päivämäärähierarkiat

Analyysitilassa tietojoukon päivämääräkentät luodaan kolmen erillisen kentän vuosi-neljännesvuosi-kuukausi-hierarkian avulla. Tämä hierarkia perustuu normaaliin kalenteriin, ei Business Centralissa määritettyyn kirjanpitokalenteriin.

Lisäkenttien nimet ovat _\<field name\> vuosi_, _\<field name\> neljännesvuosi_ ja _\<field name\> kuukausi_. Jos esimerkiksi tietojoukko sisältää kentän nimeltä _Kirjauspvm_, vastaava päivämäärähierarkia sisältää kentät nimeltä _Kirjauspvm:n vuosi_, _Kirjauspvm:n neljännesvuosi_ ja _Kirjauspvm:n kuukausi_.

> [!NOTE]
> Päivämäärähierarkia koskee tällä hetkellä vain päivämäärätyyppisiä kenttiä, ei päivämäärä/aika-tyyppisiä kenttiä.

## <a name="pivot-mode"></a>Pivot-tila

Voit käyttää pivot-tilaa analysoidaksesi suurta määrää numeerisia tietoja, välisummatietoja luokittain ja alaluokkia. Pivot-tila on kuin [pivot-taulukot Microsoft Excelissä](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Voit ottaa pivot-tilan käyttöön tai poistaa sen käytöstä liu'uttamalla **pivot-tila**-kytkintä **sarakkeet**-ruudussa (3). Kun käynnistät pivot-tilan, **sarakeotsikko**-alue tulee näkyviin ruutuun. **Sarakeotsikko**-alueen avulla voit ryhmitellä rivien kokonaissummat luokkiin. **Sarakeotsikko**-alueeseen lisättävät kentät näkyvät tietoalueen sarakkeina (1).

Tietojen analysoinnin luominen pivot-tilaan tarkoittaa kenttien siirtämistä kolmeen alueeseen: **riviryhmiin**, **sarakeotsikoihin** ja **arvoihin**. Seuraava kuva kuvaa, missä kentät yhdistyvät tietoalueeseen (1), missä `sum` on laskettu tieto ja valinnaisesti myös **Arvot**.

<table>
<tr><th></th><th>Sarakkeen selite</th><th></th><th>Sarakkeen selite</th><th></th></tr>
<tr><th>Riviryhmä</th><th>Arvo</th><th>Arvo</th><th>Arvo</th><th>Arvo</th></tr>
<tr><td>rivi</td><td>summa</td><td>summa</td><td>summa</td><td>summa</td></tr>
<tr><td>rivi</td><td>summa</td><td>summa</td><td>summa</td><td>summa</td></tr>
<tr><td>rivi</td><td>summa</td><td>summa</td><td>summa</td><td>summa</td></tr>
<tr><td>rivi</td><td>summa</td><td>summa</td><td>summa</td><td>summa</td></tr>
</table>

> [!TIP]
> Sarakkeet, joissa on vain muutama mahdollinen arvo, ovat parhaita ehdokkaita käytettäväksi sarakkeiden **Arvoissa**.


## <a name="analyze-large-amounts-of-data"></a>Suurten tietomäärien analysointi

Jos analysoitava tietojoukko ylittää 100 000 riviä, ehdotetaan, että syötät analyysitilan, joka on optimoitu suurille tietojoukoille. Tällä hetkellä on olemassa kaksi rajoitusta, jos siirryt tähän tilaan: 

- Seuraavien neljän tietotyypin kenttien muotoilu saattaa muuttua: 

   - valuutta 
   - desimaalit (näytetään aina kahdella desimaalilla) 
   - päivämäärät (näkyy aina muodossa VVVV-KK-PP)
   - aikavyöhykkeet
- Kentillä, joita käytetään pivot-tilassa ja jotka lisätään sarakeotsikoihin, on oltava pieni määrä erillisiä arvoja.

   Jos otat pivot-tilan käyttöön ja vedät kentän **Sarakeotsikot**-alueelle, jolla kentän taustalla olleilla tiedoilla on liian monta eri arvoa, selainvälilehti ei ehkä vastaa ja sulkeutuu lopulta, jolloin aloitat alusta uudessa istunnossa. Tällöin älä käännä kenttää tai aseta suodatinta kenttään ennen kuin lisäät sen **Sarakeotsikot**-alueeseen.

## <a name="share-data-analysis"></a>Jaa data-analyysi

Kun olet tehnyt analyysin välilehdessä, voit jakaa sen linkkinä työtoverien ja muiden organisaatiosi työntekijöiden kanssa suoraan asiakasohjelmasta. Vain vastaanottajat, joilla on yrityksen käyttöoikeus ja tiedot, voivat käyttää linkkiä.

1. Valitse analyysivälilehden alanuolipää ja valitse sitten **Kopioi linkki**.

   ![Näyttää analyysin kopioimisen toiminnon](media/copy-analysis.svg)

   Näyttöön **tulee Linkitä kohteeseen \<tab name\>** -valintaikkuna.

1. Jakamasi analyysi linkitetään oletusarvoisesti sen yrityksen sivulle tai kyselyyn, jota parhaillaan käsittelet. Tämä näkyy **Kopioi**-painikkeen kohdan `company=<company_name>` vieressä olevassa URL-kentässä. Jos haluat lähettää linkin analyysiin, joka ei liity tiettyyn yritykseen, määritä **Yritys:** -kentän arvoksi **Älä linkitä tiettyyn yritykseen**.

   ![Näyttää analyysivälilehden kopiointilinkin valintaikkunan](media/analysis-link-copied.svg)

1. Valitse **Kopioi**.

1. Liitä linkki haluamaasi viestintävälineisiin, esimerkiksi Wordiin, Outlookiin, Teamsiin tai OneNoteen. 

2. Kun vastaanottaja on vastaanotettu, hän voi valita linkin ja avata sivun tai kyselyn analyysin Business Centralissa. Ohjelma pyytää heitä määrittämään uuden analyysivälilehden nimen, joka luodaan.  

## <a name="limitations-in-2023-release-wave-1-preview"></a>Rajoitukset vuoden 2023 julkaisuaallossa 1 (esiversio)

Tämän ominaisuuden julkisella esiversiolla on seuraavat rajoitukset:

- Analyysitilan näkymässä on enintään 100 000 riviä. Jos ylität tämän rajan, saat viestin, jossa se kerrotaan. Voit kiertää tämän rajoituksen määrittämällä sivun suodattimet ennen analysointitilaan siirtymistä, jos mahdollista. Esimerkiksi ehkä haluat analysoida tiettyä asiakasryhmää tai haluat tietoja vain kuluvasta vuodesta. Voit myös valita ennalta määritetyn näkymän, jos se toimii analyyseissä.
- Jaa data-analyysi -toiminto ei ole käytettävissä.
- Tällä hetkellä käytettävissä ei ole mahdollisuutta tallentaa ensisijaista tietojen analyysivalintoja luettelosivuille ja tallentaa analyysivalikot analyysivälilehteä kohti.

## <a name="see-also"></a>Katso myös

[Ad-hoc-tietoanalyysi](reports-adhoc-analysis.md)  
[Tarkasteleminen ja muokkaaminen Excelissä](across-work-with-excel.md)  
