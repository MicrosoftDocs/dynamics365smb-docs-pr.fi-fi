---
title: Tietojen seuranta ja analysointi dimensioita käyttämällä
description: 'Dimensioiden avulla voi luokitella tapahtumia osasto- tai projektikohtaisesti. Tämä helpottaa tietojen seurantaa ja analysointia, mikä puolestaan auttaa tekemään hyviä liiketoimintapäätöksiä.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/27/2023
ms.custom: bap-template
ms.search.keywords: 'analysis, history, track, business intelligence'
ms.search.form: '408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253'
---
# Dimensioiden käyttäminen

Dimensiot ovat tapahtumia luokittelevia arvoja, jotta voit seurata ja analysoida tapahtumia asiakirjoissa, kuten myyntitilauksissa. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin.  

Sen sijaan, että määrittäisit kullekin osastolle ja projektille erilliset kirjanpitotilit, voit käyttää dimensioita analyysin perustana ja välttää monimutkaisen tilikartan luomisen. Lisätietoja on kohdassa [Business Intelligence](bi.md).

Voit myös esimerkiksi määrittää *Osasto*-nimisen dimension ja käyttää sitä sitten myyntiasiakirjojen kirjaamisen yhteydessä. Voit sitten käyttää BI-työkaluja, jos haluat selvittää, mitä nimikkeitä kukin osasto myy. Mitä useampia dimensioita käytät, sitä yksityiskohtaisempia raportteja voit käyttää liiketoimintapäätösten apuna. Yksittäisessä myyntitapahtumassa voi itse asiassa olla tietoja useista dimensioista, kuten  

* tili, jolle nimikkeen myynti on kirjattu.  
* nimikkeen myyntipaikka.
* nimikkeen myyjä.
* kuka asiakas osti sen.

## Analyysi dimensioittain

Dimensiot ovat tärkeä osa liiketoimintatietoja esimerkiksi analyysinäkymiä määritettäessä. Lue lisätietoja kohdasta [Analysoi tietoja dimensioiden mukaan](bi-how-analyze-data-dimension.md).

> [!TIP]
> Tapahtumatietoja voi analysoida nopeasti dimensioiden mukaan suodattamalla tilikarttojen loppusummat ja kaikkien tapahtumasivujen tapahtumat dimensioittain käyttämällä **Määritä dimension suodatin** -toimintoa.

> [!NOTE]
> Analyysinäkymissä käytetään usein dimensioiden tietoja. Jos havaitset, että kirjatuissa pääkirjanpidon (KP) tapahtumissa on käytetty virheellistä dimensiota, voit korjata dimension arvot ja päivittää analyysinäkymät. Tällä tavoin talousraportit ja analyysit pysyvät tarkkoina. Lue lisätietoja kohdasta [Vianmääritys ja dimensioiden korjaaminen](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## Dimensioyhdistelmät

Dimensioyhdistelmä on dimensioarvojen yksilöllinen yhdistelmä. Ne tallennetaan dimensioyhdistelmän tapahtumiksi tietokantaan. Kukin dimensioyhdistelmän tapahtuma edustaa yksittäistä dimensioarvoa. Lisäksi kukin dimensiojoukko ja sen sisällä oleva dimensiojoukon tapahtuma tunnistetaan yleisen dimensiojoukon tunnuksen avulla.  

Kun luot päiväkirjarivin, asiakirjaotsikon tai asiakirjarivin, voit määrittää dimensioarvojen yhdistelmän. Sen sijaan, että tallentaisit jokaisen dimensioarvon erikseen tietokantaan, dimensioyhdistelmä määritetään päiväkirjan rivillä, asiakirjaotsikossa tai asiakirjan rivillä dimensioyhdistelmän tunnuksen avulla.  

## Dimensioiden luominen

Voit määrittää päiväkirjojen ja asiakirjojen, kuten myynti- ja ostotilausten, luokitteluun käytettävät dimensiot ja dimension arvot. Dimensiot määritetään **Dimensiot**-sivulla, jossa kullekin dimensiolle luodaan yksi rivi. Dimensioita ovat esimerkiksi *Projekti*, *Osasto*, *Alue* ja *Myyjä*.

Voit määrittää myös arvoja dimensioille. Oletetaan, että arvot edustavat yrityksesi osastoja. Dimension arvot voi määrittää tilikartan kaltaisessa hierarkkisessa rakenteessa. Tämä tarkoittaa sitä, että tiedot voidaan jakaa rakeisuuden eri tasoihin ja dimension arvojen osajoukkoja voidaan laskea yhteen. Voit määrittää tarvitsemasi määrän dimensiota ja dimension arvoja, ja ne ovat yrityksessä kaikkien käytössä.

Kun dimensiot ja arvot on määritetty, voit määrittää yleiset ja pikadimensiot **Pääkirjanpidon asetukset** -sivulla. Nämä dimensiot ovat sen jälkeen aina käytettävissä, kun haluat valita kenttiä päiväkirjan ja asiakirjan riveille ja tapahtumakirjauksiin avaamatta ensin **dimensio**-sivua. Lisätietoja [Globaalien dimensioiden ja pikadimensioiden määrittäminen](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions) -osassa.

* **Globaaleja dimensioita** käytetään suodattimina esimerkiksi raporteissa, erätöissä ja XMLporteissa. Käytössä on vain kaksi globaalia dimensiota, joten valitse usein käytetyt dimensiot.
* **Pikadimensiot** ovat käytössä kenttinä päiväkirjassa, asiakirjan riveillä ja kirjanpitotapahtumissa. Voit luoda niitä enintään kahdeksan.  

> [!NOTE]
> Kun olet lisännyt uuden dimension mihin tahansa tapahtumaan, kuten riviin tai uuteen tietueeseen, et voi poistaa dimensiota, vaikka et kirjaakaan tapahtumaa. Tämä johtuu siitä, että [!INCLUDE[prod_short](includes/prod_short.md)] luo riville tai tietueelle välittömästi dimensioyhdistelmän. Katso lisätietoja [Dimensiojoukot](finance-dimensions.md#dimension-sets)-osasta.

### Asiakkaiden, toimittajien ja muiden tilien oletusdimensioiden määrittäminen

Voit määrittää oletusdimension tietylle tilille. Dimensio kopioidaan päiväkirjaan tai asiakirjaan, kun lisäät tilinumeron riville, mutta voit tarvittaessa poistaa koodin rivillä tai muuttaa sitä. Voit tarvita myös dimension, jota tarvitaan tietyn tyyppisen tilitapahtuman kirjaamiseen. > 

> [!NOTE]
> Myynti- ja ostoskenaarioissa avautuu oletusarvoisia dimensioprioriteetteja, joihin erityisesti halutaan kiinnittää huomiota. Kun myynti- ja ostoasiakirjoissa käytetään oletusarvoisia dimensioprioriteetteja, [!INCLUDE [prod_short](includes/prod_short.md)] käsittelee tunnistetiedossa olevat dimensiot aina asiakkaalta tai toimittajalta tulevana. Tämä koskee sekä manuaalisesti määritettyjä tai oletusarvoisia dimensioita, ja sillä on merkitystä, kun oletusdimensioita käytetään sijainneissa ja nimikkeissä mutta ei silloin, kun niitä käytetään asiakkaissa tai toimittajissa.
>
> **Esimerkki**
>
> Skenaariossa on seuraavat dimensioasetukset:
>
> * Asiakas, jolla ei ole oletusdimensioita
> * Nimike, jossa HAL on OSASTO-dimension dimensioarvo.
> * Sijainti, jossa TUOT on OSASTO-dimension dimensioarvo.
> * Oletusdimension prioriteetit määritetään järjestyksessä Asiakas > Nimike > Sijainti.
>
> Kun tässä dimensiossa luodaan uusi asiakirjan, dimensioita käytetään seuraavasti:
>
> * Jos uusi asiakirja luodaan ja sijainti lisätään, uusien rivien oletusarvo on TUOT. Kun nimikkeitä sisältäviä rivejä lisätään, [!INCLUDE [prod_short](includes/prod_short.md)] säilyttää TUOT-arvon, koska se tulee asiakirjan tunnistetiedoista.
>
> * Jos uusi asiakirja luodaan ja lisättävien nimikkeiden dimensioarvo on HAL, minkä jälkeen asiakirjan tunnistetiedoissa määritetään sijainti, [!INCLUDE [prod_short](includes/prod_short.md)] kysyy, halutaanko aiemmat rivit korvata ristiriidan vuoksi.
>
> Oletusdimensioiden määritykset, dimensioprioriteetit ja järjestys, jossa tiedot syötetään asiakirjoissa kannattaa testata.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Dimensiot**, valitse sitten vastaava linkki.  
2. Valitse ensin **Dimensiot**-sivulla sopiva dimensio ja sitten **Tilityypin oletusdimensio** -toiminto.  
3. Täytä rivi kutakin uutta oletusdimensiota varten, jonka haluat määrittää. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Jos haluat vaatia dimensiota, mutta et halua määrittää dimensiolle oletusarvoa, jätä **Dimension arvokoodi** -kenttä tyhjäksi ja valitse **Arvon kirjaaminen** -kentässä **Pakollinen koodi**.  

> [!WARNING]  
> Jos tiliä käytetään **Muuta vaihtokursseja**- tai **Kirjaa varaston kustannus KP:oon** -eräajossa, älä valitse **Koodi pakollinen**- tai **Sama koodi** -vaihtoehtoa. Näissä eräajoissa ei voi käyttää dimensiokoodeja.  

> [!NOTE]  
> Jos tiliin täytyy liittää dimensio, joka poikkeaa tilityypin oletusdimensiosta, sinun täytyy määrittää tälle tilille uusi oletusdimensio. Tilin oletusdimensio korvaa siten tilityypin oletusdimension.  

### Oletus dimensioprioriteettien luominen

Eri tilityypeille, esimerkiksi asiakas- ja nimiketileille, voi olla erilaiset oletusdimensiot. Siten ohjelma voi ehdottaa tapahtumalle useampaa kuin yhtä oletusdimensiota. Jotta sellaisia ristiriitatilanteita ei syntyisi, voit soveltaa eri lähteisiin prioriteettisääntöjä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Oletusdimensioprioriteetit**, valitse sitten vastaava linkki.  
2. Kirjoita **Oletusdimensioprioriteetit**-sivulla **Lähdekoodi**-kenttään sen tapahtumataulukon lähdekoodi, johon oletusdimension prioriteetteja sovelletaan.  
3. Täytä rivi kutakin oletusdimension prioriteettia varten, jonka haluat valitulle lähdekoodille.
4. Toista vaiheet kullekin lähdekoodille, jolle haluat määrittää oletusdimension prioriteetit.  

> [!IMPORTANT]  
> Jos luot kaksi taulukkoa, joilla on sama lähdekoodin prioriteetti, [!INCLUDE[prod_short](includes/prod_short.md)] hakee aina taulukon, jolla on pienin tunnus.  

### Dimensioiden kombinaatioiden luominen

Kun haluat estää sellaisten tapahtumien kirjauksen, joissa on väärät tai keskenään ristiriitaiset dimensiot, voit lukita tai rajoittaa tiettyjä kahden kombinaation yhdistelmiä. Lukittu dimensioyhdistelmä tarkoittaa, että et voi kirjata molempia dimensioita samaan tapahtumaan, riippumatta dimension arvoista. Rajoitettu dimensioyhdistelmä taas sallii molempien dimensioiden kirjaamisen samaan tapahtumaan, mutta vain tiettyjen dimension arvoyhdistelmien osalta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Dimension kombinaatiot** ja valitse sitten vastaava linkki.  
2. Valitse **Dimension kombinaatiot** -sivulla dimensioyhdistelmän kentässä jokin seuraavista vaihtoehdoista.  

    |Kenttä|Kuvaus|
    |----------------------------------|---------------------------------------|  
    |**Ei rajoituksia**|Tällä dimensioyhdistelmällä ei ole rajoituksia. Kaikki dimensioarvot ovat sallittuja.|  
    |**Rajoitettu**|Tällä dimensioyhdistelmällä on rajoituksia, jotka ovat riippuvaisia syöttämistäsi dimensioarvoista. Sinun täytyy määritellä rajoitukset **Dimension arvokombinaatiot** -sivulla.|  
    |**Estetty**|Tämä dimension kombinaatio ei ole sallittu.|  

3. Jos valitsit vaihtoehdon **Rajoitettu**-asetuksen, sinun täytyy määrittää, mitkä dimensioarvojen yhdistelmät on lukittu. Tee tämä valitsemalla kenttä määrittääksesi dimension arvoyhdistelmän.  
4. Valitse seuraavaksi lukittu dimension arvoyhdistelmä ja määritä kenttään arvo **Lukittu**. Tyhjä kenttä tarkoittaa, että kyseinen dimension arvoyhdistelmä on sallittu. Toista nämä toimet, jos lukittuja yhdistelmiä on useita.  

> [!NOTE]  
> Samat dimensiot näkyvät sekä riveillä että sarakkeissa, ja siksi kaikki dimensioyhdistelmät näkyvät kaksi kertaa. [!INCLUDE[prod_short](includes/prod_short.md)] näyttää asetuksen automaattisesti molemmissa kentissä. Et voi valita mitään niissä kentissä, jotka ovat vasemmassa yläkulmassa ja siitä alaspäin, koska näissä kentissä on sama dimensio sekä riveillä että sarakkeissa.  
>
> Valittu vaihtoehto ei ole näkyvissä ennen kuin poistut kentästä.  
>
> Jos haluat, että dimensiosta näkyy mieluummin nimi kuin koodi, laita ruksi **Näytä sarakkeen nimi** -kenttään.

### Globaalien dimensioiden ja pikadimensioiden määrittäminen

Globaaleja dimensioita ja pikadimensioita voidaan käyttää suodattimina [!INCLUDE[prod_short](includes/prod_short.md)]issa, kuten raporteissa, erätöissä, kirjanpitotapahtumasivuilla ja analyysinäkymissä. Globaalit dimensiot ja pikadimensiot voidaan lisätä suoraan ilman **Dimensiot**-sivun avaamista. Voit valita päiväkirja- ja asiakirjariveillä rivin kentässä globaalin dimension ja pikadimension. Voit määrittää kaksi globaalia dimensioita ja kahdeksan pikadimensioita. Valitse eniten käyttämäsi dimensiot.

> [!IMPORTANT]
> Globaalin dimension tai pikadimension muuttaminen edellyttää, että dimensioon kirjatut tapahtumat päivitetään. Voit muuttaa yleisen dimension käyttämällä **Muuta globaaleja dimensioita** -toimintoa, mutta se voi viedä paljon aikaa ja vaikuttaa suorituskykyyn ja taulukot voivat olla lukittuja päivityksen aikana. Varmista, että valitset globaalit dimensiot ja pikadimensiot huolellisesti, jotta niitä ei tarvitse vaihtaa myöhemmin. Jos haluat muuttaa pikadimensiota, käytä **Muuta dimensiota** -toimintoa.
>
> Lisätietoja [Globaalien dimensioiden vaihtaminen](finance-dimensions.md#to-change-global-dimensions) -osassa.

> [!NOTE]
> Jos lisäät globaalin dimension tai pikadimension tai muutat sitä, sinut kirjataan automaattisesti ulos ja takaisin sisään, jotta uutta arvoa voidaan käyttää.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset**, valitse sitten vastaava linkki.
2. Täytä **Dimensiot**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Globaalien dimensioiden muuttaminen

Kun muutat globaalin dimension tai pikadimension, kaikki dimensioon kirjatut tapahtumat päivitetään. Koska tämä prosessi voi olla aikaa vievää ja voi vaikuttaa suorituskykyyn, prosessin mukauttamiseksi tietokannan kokoon on käytettävissä kaksi eri toimintatapaa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon asetukset** ja valitse sitten vastaava linkki.
2. Valitse **Muuta globaali dimensio** -toiminto.
3. Valitse sivun yläreunasta yksi seuraavista kahdesta tilasta erätyön suorittamiseksi.

    |Asetus|Kuvaus|
    |-|-|
    |**Peräkkäin**|(Oletus) Muutos tehdään yhdessä tapahtumassa, joka peruuttaa kaikki tapahtumat niiden dimensioiden osalta, jotka niillä oli ennen muutosta.<br /><br />Tämä valinta on suositeltava, jos yrityksessä on suhteellisen vähän kirjattuja tapahtumia, jossa tapauksessa erätyön suorittaminen kestää lyhyimmän ajan. Prosessi lukitsee monta taulukkoa ja estää muita käyttäjiä, kunnes se on valmis. Huomaa, että suurissa tietokannoissa prosessia ei välttämättä voi suorittaa tässä tilassa. Käytä siinä tapauksessa **rinnakkaistoimintoa**.|
    |**Rinnakkain**|Dimension muutos tapahtuu useissa taustaistunnoissa, ja operaatio jakautuu useaan tapahtumiin. Jos haluat käyttää tätä vaihtoehtoa, ota **Rinnakkaiskäsittely**-valitsin käyttöön. <br /><br />Tämä valinta on suositeltava suurille tietokannoille tai jos yrityksessä on paljon kirjattuja tapahtumia, koska sen suorittaminen kestää lyhyimmän ajan. Huomaa, että tässä tilassa päivitysprosessi ei käynnisty, jos aktiivisia tietokantaistuntoja on enemmän kuin yksi.|  

4. Kirjoita uudet dimensiot **Globaali dimensio 1 -koodi**- ja/tai **Globaali dimensio 2 -koodi** -kenttiin. Tämänhetkiset dimensiot näkyvät harmaana kenttien takana.
5. Valitse tilan mukaan jokin seuraavista:
    * Valitse **Peräkkäinen**-tilassa **Käynnistä**-toiminto.
    * Valitse **Rinnakkainen**-tilassa **Valmistele**-toiminto.

    **Lokitapahtumat**-välilehdelle on täytetty tietoja muuttuneista dimensioista.
6. Kirjaudu ulos kohteesta [!INCLUDE[prod_short](includes/prod_short.md)], kirjaudu sitten takaisin sisään.
7. Aloita dimension muutosten rinnakkainen käsitteleminen valitsemalla **Aloita**-toiminto.

### Esimerkki dimension asetuksista

Oletetaan, että yritys haluaa seurata tapahtumia organisaatiorakenteen ja maantieteellisen sijainnin perusteella. Määrität tätä tarkoitusta varten kaksi dimensiota **Dimensiot**-sivulla:

* **ALUE**  
* **OSASTO**  

| koodi | Name | Koodin otsikko | Suodattimen otsikko |
| --- | --- | --- | --- |
| ALUE |Alue |Aluekoodi |Aluesuodatus |
| OSASTO |Osaston |Osaston koodi |Osastosuodatus |

Lisää **ALUE**-koodiin seuraavat dimension arvot:

| Postinumero | Nimi | Dimensioarvon tyyppi |
| --- | --- | --- |
| 10 |Pohjois- ja Etelä-Amerikka |Alkusumma |
| 20 |Pohjois-Amerikka |Vakio |
| 30 |Tyynimeri |Vakio |
| 40 |Etelä-Amerikka |Vakio |
| 50 |Pohjois- ja Etelä-Amerikka, yhteensä |Loppusumma |
| 60 |Eurooppa |Alkusumma |
| 70 |EU |Vakio |
| 80 |Muu kuin EU |Vakio |
| 90 |Eurooppa, Yhteensä |Loppusumma |

Voit lisätä kahteen päätason maantieteelliseen alueeseen, Pohjois- ja Etelä-Amerikkaan sekä Eurooppaan, alueellisia alaluokkia alueiden sisentämällä dimension arvot. Tällä tavoin voit raportoida aluekohtaisen myynnin tai kulut ja saada kokonaissumman suurille maantieteellisille alueille. Olisit voinut käyttää dimension arvoina myös maita, alueita, maakuntia tai paikkakuntia sen mukaan, mikä on liiketoiminnan kannalta järkevintä.

> [!NOTE]  
> Hierarkian määrittämistä varten koodien on oltava aakkosjärjestyksessä. Myös [!INCLUDE[prod_short](includes/prod_short.md)]iin sisältyvät dimension arvojen koodit on otettava tässä huomioon.  

Lisää **OSASTO**-koodiin seuraavat dimension arvot:

| Postinumero | Nimi | Dimensioarvon tyyppi |
| --- | --- | --- |
| HALLINTA |Hallinta |Vakio |
| TUOT |Tuotanto |Vakio |
| MYYNTI |Myynti |Vakio |

Voit lisätä näillä asetuksilla kaksi dimensiota kahtena globaalina dimensiona **Pääkirjanpidon asetukset** -sivulla. Niinpä voit käyttää ALUE- ja OSASTO-koodeja pääkirjanpidon tapahtumien suodattamina sekä kaikissa raporteissa. Molemmat globaalit dimensiot ovat myös automaattisesti käytettävissä pikadimensioina tapahtumariveillä ja asiakirjojen otsikoissa.

## Useita kertoja käytettyjen dimensioiden yhteenvedon hakeminen

**Oletusdimensiot-useita**-sivu määrittää, miten tiliryhmä käyttää dimensioita ja dimensioarvoja. Voit määrittää tämän korostamalla useita tilejä ja määrittämällä sitten oletusdimensiot ja dimension arvot niille. Tämän jälkeen sovellus ehdottaa näitä dimensioita ja dimension arvoja aina kun jotakin näistä tileistä käytetään, esimerkiksi päiväkirjan rivillä. Käyttäjän kannalta tämä helpottaa tapahtumien kirjaamista, sillä dimensiokentät täytetään automaattisesti. Huomaamyös, että ehdotettuja dimension arvoja voidaan muuttaa, esimerkiksi päiväkirjan rivillä.

**Oletusdimensiot-useita**-sivulla on seuraavat kentät:

|Kenttä|Kuvaus|
|-----|-----------|  
|**Dimensiokoodi**|Tässä kentässä näkyvät kaikki dimensiot, jotka on määritetty oletusdimensioksi yhdellä tai useammalla aktivoidulla tilillä. Valitsemalla kentän näet listan kaikista käytettävissä olevista dimensioista. Jos valitset dimension, tämä dimensio määritetään oletusdimensioksi kaikille korostettuina oleville tileille.|
|**Dimension arvokoodi**|Näkyy joko yksittäisen dimensioarvo tai termin (ristiriita). Jos kentässä näkyy dimension arvo, niin kaikilla aktivoiduilla tileillä on sama oletusdimension arvo. Jos kentässä näkyy termi (Ristiriita), niin kaikilla aktivoiduilla tileillä ei ole samaa dimension oletusarvoa. Napsauttamalla kentässä **Dimension koodia** saat näkyviin luettelon yhden dimension kaikista käytettävissä olevista dimensioarvoista. Jos valitset dimension arvon, se määritetään oletusdimension arvoksi kaikille korostettuina oleville tileille.|
|**Arvon kirjaaminen**|Tässä kentässä näkyy joko yksittäinen arvokirjaussääntö tai termi (Ristiriita). Jos kentässä näkyy arvokirjaussääntö, niin kaikilla aktivoiduilla tileillä on sama arvokirjaussääntö dimension arvoa koskien. Jos kentässä näkyy termi (Ristiriita), niin kaikilla aktivoiduilla tileillä ei ole samaa arvokirjaussääntöä dimension arvoa koskien. Napsauttamalla **Arvon kirjaus** -kentässä saat näkyviin luettelon dimension arvokirjaussäännöistä. Jos valitset arvokirjaussäännön, valittua arvokirjaussääntöä käytetään kaikille korostettuina oleville tileille.|

## Dimensioiden käyttö

Voit lisätä asiakirjaan, kuten esimerkiksi myyntitilaukseen, dimension tiedot sekä yksittäiseen asiakirjariviin että itse asiakirjaan. Joten voit antaa **Myyntitilaus**-sivulla kahden ensimmäisen pikadimension dimension arvot yksittäisillä myyntiriveillä. Voit myös lisätä lisää dimension tietoja valitsemalla **Dimensiot**-painikkeen.  

Jos käsittelet sen sijaan päiväkirjaa, voit lisätä dimension tietoja tapahtumaan samalla tavalla, jos olet määrittänyt pikadimensiot kentiksi suoraan päiväkirjan riveille.  

Voit myös määrittää tileille tai tilityypeille oletusdimensioita, jolloin dimensiot tai dimensioiden arvot täytetään automaattisesti.

### Globaalien dimensioiden tarkastelu tapahtumasivuilla

Globaalit dimensiot ovat aina yrityskohtaisia ja yrityksen nimeämiä. Kun haluat nähdä yrityksesi globaalit dimensiot, avaa **Pääkirjanpidon asetukset** -sivu.

Tapahtumasivulla näet, onko tapahtumille globaaleja dimensioita. Kaksi globaalia dimensiota eroavat muista siinä, että niitä voi käyttää suodattimena missä tahansa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman osassa.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta**, valitse sitten vastaava linkki.  
2. Valitse **Tilikartta**-sivulla **Tapahtumakirjaukset**-toiminto.  
3. Jos haluat nähdä vain merkitykselliset tapahtumat, määritä sivulla vähintään yksi suodatin.  
4. Jos haluat nähdä tapahtuman kaikki dimensiot, valitse ensin tapahtuma, sitten **Dimensiot**-toiminto.  

> [!NOTE]  
> **Tapahtuman dimensiot** -sivulla näkyy kerralla yhden tapahtuman dimensiot. Näet, kun selaat tapahtumia, **Tapahtuman dimensiot** -sivun sisältö muuttuu vastaavasti.

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/dimensions-dynamics-365-business-central/index)

## Katso myös

[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  
[Tietojen analysointi dimensioiden mukaan](bi-how-analyze-data-dimension.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
