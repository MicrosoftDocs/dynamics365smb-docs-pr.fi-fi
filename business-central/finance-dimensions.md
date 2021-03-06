---
title: Tietojen seuranta ja analysointi vaivattomasti dimensioita käyttämällä
description: Voit käyttää dimensioita tapahtumien luokitteluun esimerkiksi osasto- tai projektikohtaisesti. Tämä helpottaa tietojen seurantaa ja analysointia helpottuu, mikä puolestaan auttaa tekemään hyviä liiketoimintapäätöksiä.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track, business intelligence
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7e3bc7abb3908afc1819ac88c910dff85010c735
ms.sourcegitcommit: cbd00f24fb471381bbfd64670237eda176bd78e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947436"
---
# <a name="working-with-dimensions"></a>Dimensioiden käyttäminen
Dimensiot ovat tapahtumia luokittelevia arvoja, jotta voit seurata ja analysoida tapahtumia asiakirjoissa, kuten myyntitilauksissa. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin.  

Sen sijaan, että määrittäisit kullekin osastolle ja projektille erilliset kirjanpitotilit, voit käyttää dimensioita analyysin perustana ja välttää monimutkaisen tilikartan luomisen. Lisätietoja on kohdassa [Business Intelligence](bi.md).

Voit myös esimerkiksi määrittää *Osasto*-nimisen dimension ja käyttää sitä myyntiasiakirjojen kirjaamisen yhteydessä. Voit sitten käyttää BI-työkaluja, jos haluat selvittää, mitä nimikkeitä kukin osasto myy. Mitä useampia dimensioita käytät, sitä yksityiskohtaisempia raportteja voit käyttää liiketoimintapäätösten apuna. Yksittäisessä myyntitapahtumassa voi esimerkiksi olla tietoja useista dimensioista, kuten  

* tili, jolle nimikkeen myynti on kirjattu  
* nimikkeen myyntipaikka
* nimikkeen myyjä
* nimikkeen ostaneen asiakkaan tyyppi.  

## <a name="analyzing-by-dimensions"></a>Analyysi dimensioittain
Dimensiot ovat tärkeä osa liiketoimintatietoja esimerkiksi analyysinäkymiä määritettäessä. Lisätietoja on kohdassa [Tietojen analysointi dimensioittain](bi-how-analyze-data-dimension.md).

> [!TIP]
> Tapahtumatietoja voi analysoida nopeasti dimensioiden mukaan suodattamalla tilikarttojen loppusummat ja kaikkien tapahtumasivujen tapahtumat dimensioittain käyttämällä **Määritä dimension suodatin** -toimintoa.

> [!NOTE]
> Analyysinäkymissä käytetään usein dimensioiden tietoja. Jos huomataan, että kirjatuissa kirjanpitotapahtumissa on käytetty virheellistä dimensiota, dimension arvot voidaan korjata ja analyysinäkymät päivittää. Tällä tavoin talousraportit ja analyysit pysyvät tarkkoina. Lisätietoja on kohdassa [Vianmääritys ja dimensioiden korjaaminen](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting)

## <a name="dimension-sets"></a>Dimensioyhdistelmät
<!--we describe what they are, but not their value.-->
Dimensioyhdistelmä on dimensioarvojen yksilöllinen yhdistelmä. Se tallennetaan dimensioyhdistelmän tapahtumiksi tietokantaan. Kukin dimensioyhdistelmän tapahtuma edustaa yksittäistä dimensioarvoa. Dimensioyhdistelmä tunnistetaan yhteisellä dimensioyhdistelmän tunnuksella, joka määritetään jokaiselle yhdistelmään kuuluvalle tapahtumalle.  

Kun luot päiväkirjarivin, asiakirjaotsikon tai asiakirjarivin, voit määrittää dimensioarvojen yhdistelmän. Sen sijaan, että tallentaisit jokaisen dimensioarvon erikseen tietokantaan, dimensioyhdistelmä määritetään päiväkirjan rivillä, asiakirjaotsikossa tai asiakirjan rivillä dimensioyhdistelmän tunnuksen avulla.  

## <a name="setting-up-dimensions"></a>Dimensioiden luominen
Voit määrittää päiväkirjojen ja asiakirjojen, kuten myynti- ja ostotilausten, luokitteluun käytettävät dimensiot ja dimension arvot. Dimensiot määritetään **Dimensiot**-sivulla, jossa kullekin dimensiolle luodaan yksi rivi. Dimensioita ovat esimerkiksi *Projekti*, *Osasto*, *Alue* ja *Myyjä*.

Voit määrittää myös arvoja dimensioille. Arvot voivat olla esimerkiksi yrityksen osastoja. Dimension arvot voi määrittää tilikartan kaltaisessa hierarkkisessa rakenteessa, jossa tiedot voi jakaa rakeisuustason mukaan ja jossa dimension arvojen osajoukoista voi laskea summat. Voit määrittää tarvitsemasi määrän dimensiota ja dimension arvoja, ja ne ovat yrityksessä kaikkien käytössä.

Kun dimensiot ja arvot on määritetty, voit määrittää **Pääkirjanpidon asetukset** -sivulla globaalit dimensiot ja pikadimensiot, jotka ovat aina valittavissa kenttinä päiväkirja- ja asiakirjariveillä sekä kirjanpitotapahtumissa ilman, että **Dimensiot**-sivu on ensin avattava. Lisätietoja on kohdassa [Globaalien dimensioiden ja pikadimensioiden määrittäminen](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Globaaleja dimensioita** käytetään suodattimina esimerkiksi raporteissa, erätöissä ja XMLporteissa. Käytössä on vain kaksi globaalia dimensiota, joten valitse usein käytetyt dimensiot.
* **Pikadimensiot** ovat käytössä kenttinä päiväkirjassa, asiakirjan riveillä ja kirjanpitotapahtumissa. Voit luoda niitä enintään kahdeksan.  

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Asiakkaiden, toimittajien ja muiden tilien oletusdimensioiden määrittäminen
Voit määrittää oletusdimension tietylle tilille. Dimensio kopioidaan päiväkirjaan tai asiakirjaan, kun lisäät tilinumeron riville, mutta voit tarvittaessa poistaa koodin rivillä tai muuttaa sitä. Voit määrittää myös dimension, jota tarvitaan tietyn tyyppisen tilitapahtuman kirjaamiseen.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Dimensiot** ja valitse sitten liittyvä linkki.  
2.  Valitse ensin **Dimensiot**-sivulla sopiva dimensio ja sitten **Tilityypin oletusdimensio** -toiminto.  
4.  Täytä rivi kutakin uutta oletusdimensiota varten, jonka haluat määrittää. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Jos haluat tehdä dimensiosta pakollisen, mutta et halua määrittää dimensiolle oletusarvoa, jätä **Dimension arvokoodi** -kenttä tyhjäksi ja valitse **Arvon kirjaaminen** -kentässä **Pakollinen koodi**.  

> [!WARNING]  
>  Jos tiliä käytetään **Muuta vaihtokursseja** -eräajossa tai **Kirjaa varaston kustannus KP:oon** -eräajossa, älä valitse **Koodi pakollinen**- tai **Sama koodi** -vaihtoehtoa. Näissä eräajoissa ei voi käyttää dimensiokoodeja.  

> [!NOTE]  
>  Jos tiliin täytyy liittää dimensio, joka poikkeaa tilityypin oletusdimensiosta, sinun täytyy määrittää tälle tilille oletusdimensio. Tilin oletusdimensio korvaa siten tilityypin oletusdimension.  

### <a name="to-set-up-default-dimension-priorities"></a>Oletus dimensioprioriteettien luominen  
Eri tilityypeille, esimerkiksi asiakas- ja nimiketileille, voi olla määritelty erilaiset oletusdimensiot. Siten ohjelma voi ehdottaa tapahtumalle useampaa kuin yhtä oletusdimensiota. Jotta sellaisia ristiriitatilanteita ei syntyisi, voit soveltaa eri lähteisiin prioriteettisääntöjä.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Oletusdimensioiden tärkeysjärjestykset** ja valitse sitten liittyvä linkki.  
2.  Kirjoita **Oletusdimensioprioriteetit**-sivulla **Lähdekoodi**-kenttään sen tapahtumataulukon lähdekoodi, johon oletusdimension prioriteetteja sovelletaan.  
3.  Täytä rivi kutakin oletusdimension prioriteettia varten, jonka haluat valitulle lähdekoodille.
4.  Toista vaiheet kullekin lähdekoodille, jolle haluat määrittää oletusdimension prioriteetit.  

> [!IMPORTANT]  
>  Jos luot kaksi taulukkoa, joilla on sama lähdekoodin prioriteetti, [!INCLUDE[prod_short](includes/prod_short.md)] hakee aina taulukon, jolla on pienin tunnus.  

### <a name="to-set-up-dimension-combinations"></a>Dimensioiden kombinaatioiden luominen  
Kun haluat estää sellaisten tapahtumien kirjauksen, joissa on väärät tai keskenään ristiriitaiset dimensiot, voit lukita tai rajoittaa tiettyjä kahden kombinaation yhdistelmiä. Lukittu dimensioyhdistelmä tarkoittaa, että et voi kirjata molempia dimensioita samaan tapahtumaan, riippumatta dimension arvoista. Rajoitettu dimensioyhdistelmä sallii molempien dimensioiden kirjaamisen samaan tapahtumaan, mutta vain tiettyjen dimension arvoyhdistelmien osalta.

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") kuvakkeen, syötä **Dimensioiden yhdistelmät** ja valitse sitten liittyvä linkki.  
2.  Valitse **Dimension kombinaatiot**-sivulla dimensioyhdistelmän kentässä ja valitse jokin seuraavista vaihtoehdoista.  

    |Kenttä|Description|
    |----------------------------------|---------------------------------------|  
    |**Ei rajoituksia**|Tällä dimensioyhdistelmällä ei ole rajoituksia. Kaikki dimensioarvot ovat sallittuja.|  
    |**Rajoitettu**|Tällä dimensioyhdistelmällä on rajoituksia, jotka ovat riippuvaisia syöttämistäsi dimensioarvoista. Sinun täytyy määritellä rajoitukset **Dimension arvokombinaatiot** -sivulla.|  
    |**Estetty**|Tämä dimension kombinaatio ei ole sallittu.|  

3.  Jos valitsit vaihtoehdon **Rajoitettu**-asetuksen, sinun täytyy määrittää, mitkä dimensioarvojen yhdistelmät on lukittu. Tee tämä valitsemalla kenttä määrittääksesi dimensioyhdistelmän.  
4.  Valitse seuraavaksi lukittu dimension arvoyhdistelmä ja määritä kenttään arvo **Lukittu**. Tyhjä kenttä tarkoittaa, että kyseinen dimension arvoyhdistelmä on sallittu. Toista nämä toimet, jos lukittuja yhdistelmiä on useita.  

> [!NOTE]  
>  Samat dimensiot näkyvät sekä riveillä että sarakkeissa, ja siksi kaikki dimensioyhdistelmät näkyvät kaksi kertaa. [!INCLUDE[prod_short](includes/prod_short.md)] näyttää asetuksen automaattisesti molemmissa kentissä. Et voi valita mitään niissä kentissä, jotka ovat vasemmassa yläkulmassa ja siitä alaspäin, koska näissä kentissä on sama dimensio sekä riveillä että sarakkeissa.  
>   
>  Valittu vaihtoehto ei ole näkyvissä ennen kuin poistut kentästä.  
>   
>  Jos haluat, että dimensiosta näkyy mieluummin nimi kuin koodi, laita ruksi **Näytä sarakkeen nimi** -kenttään.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>Globaalien dimensioiden ja pikadimensioiden määrittäminen
Globaaleja dimensioita ja pikadimensioita voidaan käyttää suodattimina [!INCLUDE[prod_short](includes/prod_short.md)]issa, kuten raporteissa, erätöissä, kirjanpitotapahtumasivuilla ja analyysinäkymissä. Globaalit dimensiot ja pikadimensiot ovat aina lisättävissä suoraan ilman **Dimensiot**-sivun avaamista. Voit valita päiväkirja- ja asiakirjariveillä rivin kentässä globaalin dimension ja pikadimension. Voit määrittää kaksi globaalia dimensioita ja kahdeksan pikadimensioita. Valitse eniten käyttämäsi dimensiot.

> [!Important]  
> Globaalin dimension tai pikadimension muuttaminen edellyttää, että dimensioon kirjatut tapahtumat päivitetään. Voit muuttaa yleisen dimension käyttämällä **Muuta globaaleja dimensioita** -toimintoa, mutta se voi viedä paljon aikaa ja vaikuttaa suorituskykyyn ja taulukot voivat olla lukittuja päivityksen aikana. Valitse globaalit dimensiot ja pikadimensiot huolellisesti, jotta niitä ei tarvitse vaihtaa myöhemmin. Jos haluat muuttaa pikadimensiota, käytä **Muuta dimensiota** -toimintoa. <br /><br />
> Lisätietoja on kohdassa [Globaalien dimensioiden vaihtaminen](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> Jos lisäät globaalin dimension tai pikadimension tai muutat sitä, sinut kirjataan automaattisesti ulos ja takaisin sisään, jotta uutta arvoa voidaan käyttää.

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon määritykset** ja valitse sitten liittyvä linkki.
2. Täytä **Dimensiot**-pikavälilehden kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>Globaalien dimensioiden muuttaminen
Kun muutat globaalin dimension tai pikadimension, kaikki kyseiset dimensioon kirjatut tapahtumat päivitetään. Koska tämä prosessi voi olla aikaa vievää ja voi vaikuttaa suorituskykyyn, prosessin mukauttamiseksi tietokannan kokoon on käytettävissä kaksi eri toimintatapaa.  

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pääkirjanpidon määritykset** ja valitse sitten liittyvä linkki.
2. Valitse **Muuta globaali dimensio** -toiminto.
3. Valitse sivun yläosasta jokin seuraavista vaihtoehdoista määrittääksesi, missä tilassa eräajo suoritetaan.

    |Asetus|Kuvaus|
    |-|-|
    |**Peräkkäin**|(Oletus) Muutos tehdään yhdessä tapahtumassa, joka peruuttaa kaikki tapahtumat niiden dimensioiden osalta, jotka niillä oli ennen muutosta.<br /><br />Tämä valinta on suositeltava, jos yrityksessä on suhteellisen vähän kirjattuja tapahtumia, joiden suorittaminen kestää lyhyimmän ajan. Prosessi lukitsee monta taulukkoa ja estää muita käyttäjiä, kunnes se on valmis. Huomaa, että suurissa tietokannoissa prosessia ei välttämättä voi suorittaa tässä tilassa. Käytä siinä tapauksessa **rinnakkaistoimintoa**.|
    |**Rinnakkain**|Dimension muutos tapahtuu useissa taustaistunnoissa, ja operaatio jakautuu useaan tapahtumiin. Jos haluat käyttää tätä vaihtoehtoa, ota **Rinnakkaiskäsittely**-valitsin käyttöön. <br /><br />Tämä valinta on suositeltava suurille tietokannoille tai jos yrityksessä on paljon kirjattuja tapahtumia, koska sen suorittaminen kestää lyhyimmän ajan. Huomaa, että tässä tilassa päivitysprosessi ei käynnisty, jos aktiivisia tietokantaistuntoja on enemmän kuin yksi.|  

4. Kirjoita uudet dimensiot **Globaali dimensio 1 -koodi**- ja/tai **Globaali dimensio 2 -koodi** -kenttiin. Tämänhetkiset dimensiot näkyvät harmaana kenttien takana.
5. Valitse tilan mukaan jokin seuraavista:
    * Valitse **Peräkkäinen**-tilassa **Käynnistä**-toiminto.
    * Valitse **Rinnakkainen**-tilassa **Valmistele**-toiminto.

    **Lokitapahtumat**-välilehdelle on täytetty tietoja muuttuneista dimensioista.
7. Kirjaudu ulos kohteesta [!INCLUDE[prod_short](includes/prod_short.md)] ja kirjaudu sitten takaisin sisään.
8. Aloita dimension muutosten rinnakkainen käsitteleminen valitsemalla **Aloita**-toiminto. <!--is this also dependent on the mode?-->

### <a name="example-of-dimension-setup"></a>Esimerkki dimension asetuksista
Oletetaan, että yritys haluaa seurata tapahtumia organisaatiorakenteen ja maantieteellisen sijainnin perusteella. Määrität tätä tarkoitusta varten kaksi dimensiota **Dimensiot**-sivulla:

* **ALUE**  
* **OSASTO**  

| koodi | Name | Koodin otsikko | Suodattimen otsikko |
| --- | --- | --- | --- |
| ALUE |Alue |Aluekoodi |Aluesuodatus |
| OSASTO |Osaston |Osaston koodi |Osastosuodatus |

Lisää **ALUE**-koodiin seuraavat dimension arvot:

| koodi | Name | Dimension arvotyyppi |
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

Voit lisätä kahteen päätason maantieteelliseen alueeseen, Pohjois- ja Etelä-Amerikkaan sekä Eurooppaan, alueellisia alaluokkia alueiden sisentämällä dimension arvot. Tällä tavoin voit raportoida aluekohtaisen myynnin tai kulut ja saada kokonaissumman suurille maantieteellisille alueille. Olisit voinut käyttää dimension arvoina myös maita tai alueita – tai maakuntia tai paikkakuntia sen mukaan, mikä on liiketoiminnan kannalta järkevintä.

> [!NOTE]  
>   Hierarkian määrittämistä varten koodien on oltava aakkosjärjestyksessä. Myös [!INCLUDE[prod_short](includes/prod_short.md)]iin sisältyvät dimension arvojen koodit on otettava tässä huomioon.  

Lisää **OSASTO**-koodiin seuraavat dimension arvot:

| koodi | Name | Dimension arvotyyppi |
| --- | --- | --- |
| HALLINTA |Hallinta |Vakio |
| TUOT |Tuotanto |Vakio |
| MYYNTI |Myynti |Vakio |

Voit lisätä näillä asetuksilla kaksi dimensiota kahtena globaalina dimensiona **Pääkirjanpidon asetukset** -sivulla. Niinpä voit käyttää ALUE- ja OSASTO-koodeja pääkirjanpidon tapahtumien suodattamina sekä kaikissa raporteissa ja eräajoissa. Molemmat globaalit dimensiot ovat myös automaattisesti käytettävissä pikadimensioina tapahtumariveillä ja asiakirjojen otsikoissa.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Useita kertoja käytettyjen dimensioiden yhteenvedon hakeminen
**Oletusdimensiot-useita**-sivu määrittää, miten tiliryhmä käyttää dimensioita ja dimensioarvoja. Voit tehdä sen aktivoimalla useamman tilin ja määrittelemällä sitten oletusdimensiot ja dimensioarvot kaikille niille tileille, jotka aktivoit tililuettelossa. Kun määrittelet aktivoiduille tileille oletusdimensioita, sovellus ehdottaa näitä dimensioita ja dimension arvoja aina, kun jotakin näistä tileistä käytetään esimerkiksi päiväkirjan rivillä. Käyttäjän kannalta tämä helpottaa tapahtumien kirjaamista, sillä dimensiokentät täytetään automaattisesti. Ehdotettuja dimension arvoja voidaan kuitenkin muuttaa, esimerkiksi päiväkirjan rivillä.

**Oletusdimensiot-useita**-sivulla on seuraavat kentät:

|Kenttä|Description|
|-----|-----------|  
|**Dimensiokoodi**|Tässä kentässä näkyvät kaikki dimensiot, jotka on määritetty oletusdimensioksi yhdellä tai useammalla aktivoidulla tilillä. Valitsemalla kentän näet listan kaikista käytettävissä olevista dimensioista. Jos valitset dimension, valittu dimensio määritetään oletusdimensioksi kaikille korostettuina oleville tileille.|
|**Dimension arvokoodi**|Näkyy joko yksittäisen dimensioarvo tai termin (ristiriita). Jos kentässä näkyy dimension arvo, niin kaikilla aktivoiduilla tileillä on sama oletusdimension arvo. Jos kentässä näkyy termi (Ristiriita), niin kaikilla aktivoiduilla tileillä ei ole samaa dimension oletusarvoa. Napsauttamalla kentässä AssistButtonia saat näkyviin luettelon yhden dimension kaikista käytettävissä olevista dimensioarvoista. Jos valitset dimension arvon, valittu dimension arvo määritetään oletusdimension arvoksi kaikille korostettuina oleville tileille.|
|**Arvon kirjaaminen**|Tässä kentässä näkyy joko yksittäinen arvokirjaussääntö tai termi (Ristiriita). Jos kentässä näkyy arvokirjaussääntö, niin kaikilla aktivoiduilla tileillä on sama arvokirjaussääntö dimension arvoa koskien. Jos kentässä näkyy termi (Ristiriita), niin kaikilla aktivoiduilla tileillä ei ole samaa arvokirjaussääntöä dimension arvoa koskien. Napsauttamalla AssistButtonia Arvon kirjaus -kentässä saat näkyviin luettelon arvokirjaussäännöistä. Jos valitset arvokirjaussäännön, valittua arvokirjaussääntöä käytetään kaikille korostettuina oleville tileille.|

## <a name="using-dimensions"></a>Dimensioiden käyttäminen
Voit lisätä asiakirjaan, kuten esimerkiksi myyntitilaukseen, dimension tiedot sekä yksittäiseen asiakirjariviin että itse asiakirjaan. Voit antaa esimerkiksi **Myyntitilaus**-sivulla kahden ensimmäisen pikadimension dimension arvot yksittäisillä myyntiriveillä. Voit myös lisätä lisää dimension tietoja valitsemalla **Dimensiot**-painikkeen.  

Jos käsittelet sen sijaan päiväkirjaa, voit lisätä dimension tietoja tapahtumaan samalla tavalla, jos olet määrittänyt pikadimensiot kentiksi suoraan päiväkirjan riveille.  

Voit määrittää tileille tai tilityypeille oletusdimensioita, jolloin dimensiot tai dimensioiden arvot täytetään automaattisesti.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Globaalien dimensioiden tarkastelu tapahtumasivuilla  
Globaalit dimensiot ovat aina yritys\-kohtaisia ja yrityksen nimeämiä. Kun haluat nähdä yrityksesi globaalit dimensiot, avaa **Pääkirjanpidon asetukset** -sivu.  

Tapahtumasivulla näet, onko tapahtumille globaaleja dimensioita. Kaksi globaalia dimensiota eroavat muista siinä, että niitä voi käyttää suodattimena missä tahansa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman osassa.  

1.  Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten liittyvä linkki.  
2.  Valitse **Tilikartta**-sivulla **Tapahtumakirjaukset**-toiminto.  
3.  Jos haluat nähdä vain merkitykselliset tapahtumat, määritä sivulla vähintään yksi suodatin.  
4.  Jos haluat nähdä tapahtuman kaikki dimensiot, valitse ensin tapahtuma ja sitten **Dimensiot**-toiminto.  

> [!NOTE]  
>  **Tapahtuman dimensiot** -sivulla näkyy kerralla yhden tapahtuman dimensiot. Kun selaat tapahtumia, **Tapahtuman dimensiot** -sivun sisältö muuttuu vastaavasti.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  
[Tietojen analysointi dimensioiden mukaan](bi-how-analyze-data-dimension.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]