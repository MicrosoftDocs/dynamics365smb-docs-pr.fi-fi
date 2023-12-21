---
title: 'Sarja-, erä- ja pakettinumeroita sisältävien nimikkeiden seuraaminen'
description: 'Voit lisätä sarja-, erä- ja pakettinumeroita mihin tahansa lähtevään tai saapuvaan asiakirjaan, ja sen kirjatut nimikeseurantatapahtumat näkyvät niihin liittyvissä nimiketapahtumissa.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 12/19/2023
ms.custom: bap-template
---
# <a name="track-items-with-serial-lot-and-package-numbers"></a>Sarja-, erä- ja pakettinumeroita sisältävien nimikkeiden seuraaminen

Voit määrittää sarja-, erä- ja pakettinumeroita mihin tahansa lähtevään tai saapuvaan asiakirjaan, ja sen kirjatut nimikeseurantatapahtumat näkyvät niihin liittyvissä nimiketapahtumissa. Nimikkeitä seurataan **Nimikkeen seurantarivit** -sivulla, joka avataan saapuvista tai lähtevistä asiakirjoista.

**Nimikkeen seurantarivit** -sivun yläosassa olevassa määräkentissä näkyy rivillä määritettävien nimikkeen seurantanumeroiden määrät ja summat. Määrien on vastattava asiakirjarivejä. Sen osoituksena **Määrittelemätön**-kentässä on 0.

[!INCLUDE [prod_short](includes/prod_short.md)] päivittää saatavuustiedot **Nimikkeen seurantarivit** -sivulle, kun sivu avataan. Tietoja ei päivitetä sivun ollessa avoinna, vaikka varastotiedoissa tai muissa asiakirjoissa tapahtuisi muutoksia kyseisenä aikana.

> [!NOTE]  
> Jotta tässä artikkelissa kuvatut ominaisuudet toimivat, sinun on määritettävä nimikeseuranta. Lisätietoja on kohdassa [Sarja-, erä- ja pakettinumeroita sisältävien nimikkeiden seurannan määrittäminen](inventory-how-setup-item-tracking.md).

## <a name="item-tracking-availability"></a>Nimikeseurannan saatavuus

Sarja-, erä- ja pakettinumeroita käytettäessä [!INCLUDE[prod_short](includes/prod_short.md)] laskee saatavuustiedot ja näyttää ne erilaisilla nimikeseurantasivuilla. Näin nähdään, kuinka paljon erä-, paketti- tai sarjanumeroa käytetään muissa asiakirjoissa. Nämä tiedot vähentävät kaksinkertaisten kohdistuksen aiheuttamia virheitä ja epävarmuutta.

**Nimikkeen seurantarivit** -sivulla voi näkyä varoituskuvake **Saatavuus, eränro**- tai **Saatavuus, sarjanro** -kentässä seuraavista syistä:

* jos osa tai kaikki valitusta määrästä on jo käytössä muissa asiakirjoissa
* jos erä- tai sarjanumero ei ole saatavilla.

**Eränro/sarjanro - luettelo**-, **Eränro/sarjanro - saatavuus**- ja **Nimikeseuranta - valitse tapahtumat** -sivuilla on tietoja nimikkeen käytössä olevasta määrästä. Seuraavassa taulukossa on luettelo asiaankuuluvista kentistä.

|Kenttä|Kuvaus|
|-----|-----------|  
|**Kokonaismäärä**|Varastossa olevan nimikkeen kokonaismäärä.|
|**Pyydetty määrä yhteensä**|Tässä ja muissa asiakirjoissa pyydettyjen nimikkeiden kokonaismäärä.|
|**Nykyinen odottava määrä**|Niiden nimikkeiden määrä, joita on pyydetty tässä asiakirjassa, mutta joita ei ole kirjattu.|
|**Nykyinen pyydetty määrä**|Tässä asiakirjassa käytettäväksi pyydettyjen nimikkeiden määrä|
|**Saatavilla oleva kokonaismäärä**|Varastossa olevien nimikkeiden kokonaismäärä vähennettynä tämän ja muiden asiakirjojen pyytämien nimikkeiden määrällä (pyydetty määrä yhteensä) ja pyydetyn mutta ei vielä tähän asiakirjaan kirjattujen nimikkeiden määrällä (nykyinen odottava määrä).|

Jos käytät **Nimikkeen seurantarivit** -sivua pitkään tai teet paljon muutoksia käsiteltävänä olevaan nimikkeeseen, voit valita **Päivitä saatavuus** -toiminnon. Lisäksi nimikkeen saatavuus tarkistetaan automaattisesti uudelleen, kun suljet sivun ja vahvistat näin, että saatavuusongelmia ei ole.

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Sarja-/Eränumeroiden määritteleminen saapuvien transaktioiden aikana

Haluat ehkä seurata nimikkeitä heti niiden saapumisen jälkeen. Tällöin ostotilaus on usein keskeinen asiakirja. Voit kuitenkin tehdä nimikeseurantaa missä tahansa saapuvassa asiakirjassa, ja sen kirjatut tapahtumat näkyvät niihin liittyvissä nimiketapahtumissa.

Seurantanumerot siirtyvät automaattisesti kaikkiin lähteviin varastotoimintoihin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  
2. Avaa aiemmin luotu ostotilaus tai luo uusi ostotilaus.
3. Valitse ensin asiakirja ja sitten **Rivit**-pikavälilehdessä **Rivi**-toiminto. Valitse lopuksi **Nimikkeen seurantarivit**, jotta voit avata **Muokkaa –Nimikkeen seurantarivit** -sivun.  

   Voit määrittää sarja- tai eränumeroita seuraavilla tavoilla:  
   - Automaattisesti, valitsemalla **Prosessi** ja sitten **Määritä sarjanro** tai **Määritä eränro**, jotta ohjelma määrittäisi sarja/erä -numerot ennakkoon määritellystä numerosarjasta.  
   - Automaattisesti valitsemalla **Prosessi**, sitten **Luo räätälöidyt sarjanrot** jotta ohjelma automaattisesti määrittää sarja-/eränumerot perustuen numerosarjoihin jotka olet määrittänyt saapuville nimikkeille.  
   - Manuaalisesti syöttämällä sarja-/eränumeroita, esimerkiksi toimittajien numeroita, suoraan.  
   - Manuaalisesti määrittelemällä tietyn numeron kullekin nimikeyksikölle.  

4. Valitse **Luo räätälöity SN** -toiminto, jos haluat automaattisen määrityksen.  
5. Kohteessa **räätälöity sarjanro** -kenttä, syötä sarjanumerolle kuvaava numerosarja. Se voi olla esimerkiksi **S/N-Toim0001**.  
6. Syötä **Lisäys**-kenttään 1 määritelläksesi, että kukin peräkkäinen numero kasvaa yhdellä.  

    Kohteen **Luotava määrä** -kenttä sisältää oletuksena rivimäärän, mutta voit muuttaa sitä.  

7. Järjestä uudet sarjanumerot selkeäksi eräksi valitsemalla **Luo uusi eränro** -valintaruutu.  
7. Valitse **OK**-painike.  

[!INCLUDE [prod_short](includes/prod_short.md)] luo nyt eränumeron, jossa ovat yksilöivät sarjanumerot asiakirjarivin nimikemäärän mukaan. Numeron etuliite on **Räätälöity sarjanro** -kenttään annettu arvo. Ne voivat alkaa esimerkiksi **S/N-Toim0001**-arvosta.  

Otsikon Määrä-kentissä näkyvät sivulla määritettävien nimikeseurantanumeroiden määrät ja summat dynaamisesti. Määrien on vastattava asiakirjarivejä. Sen osoituksena **Määrittelemätön**-kentässä on **0**-arvo.  

Kun kirjaat asiakirjan, nimikeseurantatapahtumat siirretään niihin liittyviin nimiketapahtumiin.

### <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Sarja- ja eränumeroiden käsitteleminen, kun saat vastaanottorivit ostolaskusta

Kun haet kirjattuja vastaanottoja tai toimitusrivejä liittyvistä laskuista tai hyvityslaskuista, mitkä tahansa nimikkeen seurantarivit varastoasiakirjoissa siirretään automaattisesti. Niitä kuitenkin käsitellään erityisellä tavalla.

Toiminto tukee seuraavia saapuvia prosesseja:  

- **Hae vastaanottorivit** - ostolaskulta  
- **Hae palautustoimitusrivit** - ostohyvityslaskulta  

Toiminto tukee seuraavia lähteviä prosesseja:  

- **Hae toimitusrivit** - myyntilaskulta. (Käytetään myös yhdistetyille toimituksille.)  
- **Hae palautusvastaanottorivit** - myyntihyvityslaskulta  

Näissä tapauksessa nimikkeen seurantarivit siirretään laskulle tai hyvityslaskulle, mutta **Nimikkeen seurantarivit** -sivu ei salli muuttaa sarja- tai eränumeroita. Vain määriä voidaan muuttaa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.  
2. Avaa ostolasku nimikkeille, jotka ostetaan sarja- tai eränumeroiden perusteella.  
3. Valitse ostolaskun rivin **Rivit**-pikavälilehdessä **Hae vast.oton rivit** -toiminto.  
4. Valitse **Hae vast.oton rivit** -sivulla vastaanottorivi, jolla on nimikkeen seurantarivejä, ja valitse sitten **OK**.  

    Lähdeasiakirja kopioidaan ostolaskulle uutena rivinä, ja sen nimikkeen seurantarivit kopioidaan perusteena olevalle **Nimikkeen seurantarivit** -sivulle.  

5. Valitse ostolaskussa siirretty vastaanottorivi.  
6. Voit tarkastella siirrettyjä nimikkeen seurantarivejä valitsemalla **Rivit**-pikavälilehdessä ensin **Rivit**-toiminto ja sitten **Nimikkeen seurantarivit** -toiminto.  

**Sarjanro**- ja **Eränro**-kenttiä ei voi muuttaa. Voit kuitenkin poistaa kokonaisia rivejä tai muuttaa määriä vastaamaan lähderivillä tehtyjä muutoksia.  

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Sarja- tai eränumeroiden määritteleminen lähtevän tapahtuman aikana

Sarja-/eränumeroiden lähtevä käsittely on tehtävä, jota käytetään useiden eri fyysisen varaston prosessien aikana. Ohjelmassa on kaksi tapaa lisätä sarja- ja eränumerot lähteviin tapahtumiin:  

- Valitse olemassa olevista sarja- tai eränumeroista. Tätä mahdollisuutta käytetään silloin, kun nimikkeen seurantanumerot on jo määritelty saapuvan tapahtuman aikana.
- Määritä sarja- tai eränumerot lähteville tapahtumille. Tätä käytetään, kun nimikkeen seurantanumeroita ei määritetä nimikkeisiin ennen kuin ne myydään ja ne ovat valmiita toimitettaviksi.

### <a name="to-select-from-existing-serial-or-lot-numbers"></a>Olemassa olevista sarja-/eränumeroista valitseminen

Kun käsittelet nimikkeitä, jotka vaativat nimikkeen jäljitystä ja olet luomassa lähteviä tapahtumia, tarvitset yleensä varastossa olevia erä- tai sarjanumeroita.

1. Valitse mistä tahansa lähtevästä asiakirjasta rivi, jolle haluat valita sarja- tai eränumeroita.  
2. Valitse **Rivit**-pikaväliruudussa **Rivi**-toiminto, sitten **Liittyvät tiedot** ja valitse sitten **Nimikkeen seurantarivit**.  
3. Voit määrittää erä- tai sarjanumeron kolmella eri tavalla **Nimikkeen seurantarivit** -sivulla:  

   - Valitse ensin **Sarjanro**-kenttä ja sitten numero **Sarjanroluettelo**-sivulla.
   - Valitse ensin **Eränro**-kenttä ja sitten numero **Eränroluettelo**-sivulla. Valitse **Sarjanro**-kenttä ja valitse sitten numero **Sarjanroluettelo**-sivulla.
   - Valitse **Prosessi**-toiminto ja sitten **Valitse tapahtumat**. **Valitse tapahtumat** -sivulla näkyvät kaikki erä- ja sarjanumerot sekä niiden saatavuustiedot.

4. Syötä **Valittu määrä** -kenttään kunkin erä- tai sarjanumeron käytettävä määrä.
5. Valitse **OK**-painike. Nimikeseurannan tiedot siirretään **Nimikkeen seurantarivit** -sivulle.  

Otsikon Määrä-kentissä näkyvät sivulla määritettävien nimikeseurantanumeroiden määrät ja summat dynaamisesti. Määrien on vastattava asiakirjarivejä. Sen osoituksena **Määrittelemätön**-kentässä on **0**.  

Kun kirjaat asiakirjarivin, nimikeseurantatiedot siirretään niihin liittyviin nimiketapahtumiin.

### <a name="to-assign-new-serial-or-lot-numbers"></a>Uusien erä- tai sarjanumeroiden määritys

Tämä prosessi on voimassa silloin, kun nimikkeet ovat varastossa, eikä niillä ole sarja- tai eränumeroita. Tämän sijaan nimikkeiden seurantanumerot määritetään, kun ne myydään ja ne ovat valmiita toimitettaviksi. Tässä tapauksessa numerot yleensä määritetään ennalta määritetystä numerosarjasta.

1. Valitse asianmukainen asiakirja, esimerkiksi myyntilasku tai myyntitilaus, ja valitse **Rivit**-pikaväliruudussa **Rivi**-toiminto, sitten **Liittyvät tiedot** ja valitse sitten **Nimikkeen seurantarivit** -toiminto.  

    Nimikkeen seurantanumeroita voi nyt määritellä seuraavilla tavoilla:  
    - Automaattisesti esimääritetystä numerosarjasta: valitse **Määritä sarjanro**- tai **Määritä eränro** -toiminto.  
    - Automaattisesti lähtevälle nimikkeelle määritettyjen parametrien mukaan: valitse **Luo räätälöity SN** -toiminto.  
    - Manuaalisesti syöttämällä sarja- tai eränumerot numerosarjoja käyttämättä.  

2. Tässä menetelmässä sarjanumero määritetään automaattisesti valitsemalla **Määritä sarjanro**  

    Kohteen **Luotava määrä** -kenttä sisältää oletuksena rivimäärän, mutta voit muuttaa sitä.  
3. Laita rasti kohtaan **Luo uusi eränro** - kenttään organisoidaksesi uusia sarjanumeroita tiettyyn erään.  
4. Valitse **OK**, jotta ohjelma luo eränumeron ja uusia yksittäisiä sarjanumeroita liittyvien asiakirjarivien perusteella.  

Sivulla määritettävien nimikeseurannan numeroiden määrät ja summat näkyvät dynaamisesti määräkentissä. Määrien on vastattava asiakirjarivejä. Sen osoituksena **Määrittelemätön**-kentässä on **0**.  

Kun asiakirja kirjataan, nimikeseurantatapahtumat siirretään niihin liittyviin nimiketapahtumiin.

### <a name="assign-tracking-numbers-on-source-documents"></a>Seurantanumeroiden määrittäminen lähdeasiakirjoille

Jotkin yritykset määrittävät erityiset sarja- tai eränumerot lähdeasiakirjassa, kuten myyntitilauksissa. Näin tehdään esimerkiksi silloin, kun asiakas pyytää tiettyä erää. Kun varaston poiminta-asiakirjan tai fyysisen varaston poiminta-asiakirja luodaan lähtevästä lähdeasiakirjasta, jossa sarja- tai eränumerot on jo määritelty, **Nimikkeen seurantarivit** -sivun varastopoiminnan kenttiä ei voi muuttaa. Ainoa poikkeus on **Käsiteltävä määrä** -kenttä. Siinä tapauksessa varaston poimintarivit määrittelevät nimikkeen seurantanumerot yksittäisillä ottamis- ja asettamisriveillä. Määrä on jo jaettu yksilöllisiin sarja-/eränumeroyhdistelmiin, koska myyntitilaus määrittää toimitettavat nimikkeen seurantanumerot.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Siirtotilausten sarja- ja eränumeroiden käsitteleminen

Eri sijaintien välillä siirrettävien sarja- ja eränumeroiden käsittelyn menetelmät ovat samanlaisia kuin ne, joita käytetään silloin, kun nimikkeitä ostetaan ja myydään.  

Tulee ottaa huomioon, että siirtotilaukset ovat ainutlaatuisia siinä suhteessa, että sekä toimitus että vastaanotto tehdään samalle siirtoriville. Tästä johtuen joudutaan käyttämään samaa **Nimikkeen seurantarivit** -sivua. Nimikkeen seurantanumerot, jotka toimitettiin yhdestä paikasta, täytyy vastaanottaa muuttumattomana seuraavassa paikassa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirtotilaukset** ja valitse sitten vastaava linkki.  
2. Avaa siirtotilaus, jonka haluat käsitellä. Valitse **Rivit**-pikavälilehdessä ensin **Rivi**-toiminto, sitten **Nimikkeen seurantarivit** -toiminto ja lopuksi **Toimitus**-toiminto.  
3. **Nimikkeen seurantarivit** -sivulla voit määrittää sarja- tai eränumeroita, kuten mille muulle tahansa lähtevälle nimiketapahtumalle.  

    Kun käsittelyssä ovat siirtonimikkeiden sarja- tai eränumerot, nimikkeille on jo tavallisesti määritelty numerot. Tämän vuoksi usein valitaan olemassa olevia sarja- tai eränumeroita.  

4. Kirjaa siirtotilaus, ensin toimita ja sitten vastaanota, tallentaaksesi sen, että nimikkeet siirretään niiden nimikkeen seurantatapahtumat mukanaan.  

Siirron aikana **Nimikkeen seurantarivit** -sivun arvoja ei voi muuttaa.  

## <a name="to-record-additional-serial-or-lot-number-information"></a>Sarja-/Eränumeroiden lisätietojen tallentaminen

Jos sinun täytyy linkittää erityistietoja nimikkeen seurantanumeroon, esimerkiksi laadunvarmistuksen osalta, näin voidaan tehdä sarja- tai eränumerotietojen kortissa.

1. Avaa asiakirja, johon on määritetty sarja- tai eränumeroita.
2. Avaa **Nimikkeen seurantarivit** -sivu nimikkeelle, jonka tiedot haluat syöttää.
3. Valitse **Rivi**-toiminto ja sitten esimerkiksi **Sarjanron tietokortti** -toiminto.  
4. Luo uusi merkintä valitsemalla luettelon yläreunassa plusmerkki **(+)**. **Sarjanumero** ja **Eränro** -kentät esitäytetään nimikeseurantarivien perusteella.
5. Syötä lyhyesti tietoja **Kuvaus**-kenttään, esimerkiksi tiedot kohteen kunnosta.  
6. Valitse **Liittyvä**-toiminto, valitse **Sarjanro**-toiminto ja luo sitten erillinen kommenttitietue valitsemalla **Kommentti**-toiminto.  
7. Valitse **Estetty**-kenttä sulkeaksesi sarja-/eränumerot pois kaikista transaktioista.  

<!--If you create serial numbers in bulk by using the **Create Customized SN** or **Assign Serial No.** actions, you can enable **Create SN Information** and an information card will be created for each tracking line.

Alternatively, you can create an information card when you post journals or documents. On the **Item Tracking Code** page, turn on the **Create SN Info. on posting** or **Create SN Info. on posting** toggles. -->

Voit muokata luotuja sarja- tai erätietokortteja myöhemmin.

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Aiemmin luotujen sarja- tai eränumerotietojen muokkaaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Valitse nimike, jolla on nimikkeen seurantakoodi ja sarja- tai eränumerotietoja.
3. Valitse **Nimikkeen kortti** -sivulla ensin **Tapahtumat**-toiminto ja sitten **Tapahtumakirjaukset**.
4. Valitse **Eränro** tai **Sarjanumero** -kenttä. Jos nimikkeen seurantanumerolla on tietoja, **Eränumeron tietoluettelo**- tai **Sarjanumeron tietoluettelo** -sivu avautuu.  
5. Valitse ensin kortti ja sitten **Eränumerotietojen tai sarjanumerotietojen kortti** -toiminto.  
6. Muokkaa lyhyttä kuvaustekstiä, kommenttitietuetta tai **Suljettu**-kenttää.  

Et voi muuttaa sarja- tai eränumeroita tai määriä. Tehdäksesi näin sinun tulee luokitella nimiketapahtuma uudelleen. Lisätietoja uudelleenluokittelusta on kohdassa [Sarja- ja eränumeroiden uudelleenluokittelu](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a>Erä- tai sarjanumeroiden uudelleenluokittelu

Nimikkeiden seurannan uudelleenluokittelu tarkoittaa erä- tai sarjanumeron muuttamista uudeksi erä- tai sarjanumeroksi tai vanhentumispäivämäärän muuttamista uudeksi vanhentumispäivämääräksi. Jos käytät eriä, voit myös yhdistää useita eriä yhdeksi eräksi. Voit suorittaa nämä tehtävät nimikkeen uudelleenluokituspäiväkirjassa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimik. uud.luok.pvk** ja valitse sitten vastaava linkki.  
2. Täytä rivi asianmukaisilla tiedoilla. Lisätietoja on kohdassa [Varastojen laskenta asiakirjoja käyttämällä](inventory-how-count-inventory-with-documents.md) tai [Varaston laskeminen, muuttaminen ja uudelleenluokitus päiväkirjojen avulla](inventory-how-count-adjust-reclassify.md).
3. Valitse **Nimikkeen seurantarivit** -toiminto.  
4. Napsauta **Sarjanro**- tai **Eränro**-kentässä olevaa AssistButtonia ja valitse nykyinen sarja- tai eränumero.  
5. Jos haluat syöttää uuden nimikeseurannan numeron, syötä se **Uusi sarjanro**- tai **Uusi eränro** -kenttään. Jos haluat, voit yhdistää eriä yhdeksi uudeksi tai olemassa olevaksi eräksi.  

    > [!NOTE]  
    > Kun luokittelet uudelleen vanhenemispäivät, ehdotetaan ensin kohteita, joiden lähtevien tapahtumien vanhenemispäivämäärät ovat aikaisimmat. Lisätietoja on kohdassa [FEFO-poiminta](warehouse-picking-by-fefo.md).  

6. Voit määrittää sarja- tai eränumerolle uuden vanhentumispäivämäärän syöttämällä sen **Uusi vanhentumispvm** -kenttään.  

    > [!IMPORTANT]  
    > * Jos luokittelet erän uudelleen samalle eränumerolle eri vanhentumispäivämäärällä, koko erä on luokiteltava uudelleen käyttämällä vain yhtä nimikkeen uudelleenluokituspäiväkirjan riviä. 
    > * Jos luokittelet uudelleen useita eriä yhdeksi uudeksi eräksi, sinun on syötettävä kaikille erille sama vanhentumispäivämäärä. 
    > * Jos luokittelet yhden erän uudelleen toiseksi olemassa olevaksi eräksi, jolla on eri vanhentumispäivämäärä, sinun on käytettävä toisen erän vanhentumispäivämäärää. 
    > * Jos jätät **Uusi vanhentumispvm** -kentän tyhjäksi, erä- tai sarjanumero luokitellaan uudelleen ilman vanhentumispäivämäärää.  

7. Jos vanhalla sarja- tai eränumerolla on aiempia tietoja, voit kopioida ne uudelle sarja- tai eränumerolle.  

    1. Valitse **Nimikkeen seurantarivit** -sivulle **Uuden sarjanumeron tiedot**- tai **Uuden eränumeron tiedot** -toiminto.  
    2. Voit kopioida vanhan erä- tai sarjanumeron tiedot valitsemalla **Kopioi tiedot** -toiminnon.  
    3. Valitse tietoluettelosivulla erä- tai sarjanumero, josta haluat kopioida, ja valitse sitten **OK**.  

8. Jos haluat muokata erä- tai sarjanumeron olemassa olevia tietoja, voit tallentaa erä- tai sarjatietoja.  
9. Kirjaamalla päiväkirjan voit linkittää uusitun nimikeseurannan numerot tai vanhentumispäivämäärät liitettyyn nimiketapahtumaan

## <a name="scan-barcodes-with-the-business-central-mobile-app"></a>Viivakoodien skannaaminen Business Central -mobiilisovelluksen kanssa

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Jos haluat skannata useita sarja-, erä- tai pakettiviivakoodeja **Nimikkeen seurantarivit** -sivulla, voit käyttää **Skannaa useita** -toimintoa. Viivakoodin skannauksen jälkeen sen arvo syötetään sivun kenttään, jolloin seuraava pikasyöttökenttä tulee saataville. Viivakoodinlukija-kuvakkeen avulla voit myös täyttää tietyt kentät.

Seuraavissa taulukoissa ovat sivut, jotka tukevat viivakoodien lukemista [!INCLUDE [prod_short](includes/prod_short.md)] -mobiilisovelluksen nimikeseurannassa.

|Sivu  |Kenttäarvoja, jotka voi lukea  |
|---------|---------|
|Nimikkeen seurantarivit     |* Sarjanro<br><br>* Uusi sarjanro<br><br>* Eränro<br><br>* Uusi eränro<br><br>* Paketin nro<br><br>* Uusi pakettinro|
|F.var. Nimikkeen seurantarivit     |* Sarjanro<br><br>* Uusi sarjanro<br><br>* Eränro<br><br>* Uusi eränro<br><br>* Paketin nro<br><br>* Uusi pakettinro|
|Nimikkeen jäljitys     |* Sarjanron suodatus<br><br>* Eränron suodatus<br><br>* Paketin nro Suodata |
|Nimikepäiväkirja     |* Sarjanro<br><br>* Eränro<br><br>* Paketin nro     |
|F.varastoinnin toimintorivi     |* Sarjanro<br><br>* Eränro<br><br>* Paketin nro<br><br>**Huomautus**: Seuraavat sivut käyttävät F.varastoinnin toimintorivi -sivua:<br><br>* sivu 5780 "F.var. poiminnan alilomake"<br><br>* sivu 7378 "Var. poiminnan alilomake"<br><br>* sivu 5771 "F.var. hyllytyksen alilomake"<br><br>* sivu 7316 "F. var. siirron alilomake"<br><br>* sivu 7376 "Var. hyllytyksen alilomake"<br><br>* sivu 7383 "Var. siirron alilomake"        |
|F.var. Invent. varastopäiväk.     |* Sarjanro<br><br>* Eränro<br><br>* Paketin nro         |

## <a name="see-also"></a>Katso myös

[Sarja-, erä- ja pakettinumeroita sisältävän nimikeseurannan määrittäminen](inventory-how-setup-item-tracking.md)  
[Nimikeseurannan nimikkeiden jäljittäminen](inventory-how-to-trace-item-tracked-items.md)  
[Varasto](inventory-manage-inventory.md)  
[Rakennetiedot: Nimikkeen seuranta](design-details-item-tracking.md)  
[Rakennetiedot – nimikkeen seuranta ja varaukset](design-details-item-tracking-and-reservations.md)  
[Nimikkeiden varaaminen](inventory-how-to-reserve-items.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
