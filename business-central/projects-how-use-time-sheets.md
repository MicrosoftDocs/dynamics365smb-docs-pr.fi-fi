---
title: Käytä aikaraportteja
description: 'Tietoja resurssien, projektien ja palveluiden tuntiraporttien luomista, lähettämistä, hyväksymisestä ja kirjaamisesta.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 02/05/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Käytä aikaraportteja

Tässä artikkelissa kerrotaan, kuinka tuntiraportteja voidaan käyttää poissaolojen sekä projektiin käytetyn ajan ja resurssien seuraamiseen. Ajanhallinnan avulla voit tunnistaa ongelmat aikaisessa vaiheessa ja välttää viiveet tai kustannusylitykset. Resurssi voidaan helposti raportoida tuntiraporttien avulla yksityishenkilölle tai koneelle ja esimies voi helposti tarkastella käyttöä ja jakamista.

Voit kopioida projektin suunnittelurivit aikaraportista ja käyttää niitä. Näin tehtäessä tiedot on syötettävä vain yhteen paikkaan, ja ne ovat aina ajantasaisia. Lisätietoja on kohdassa [Projektin suunnittelurivien kopioiminen aikaraporttiin](#copy-project-planning-lines-to-a-time-sheet).

Kun olet hyväksynyt projektin aikaraportin tapahtumat, voit kirjata ne soveltuvaan projekti- tai resurssipäiväkirjaan. Lisätietoja on kohdassa [Aikaraporttirivien kirjaaminen projektipäiväkirjaan](#post-time-sheet-lines-in-a-project-journal) ja [Aikaraporttirivien kirjaaminen resurssipäiväkirjaan](#post-time-sheet-lines-in-a-resource-journal).

Ennen kuin käytät aikaraportteja, sinun on määritettävä aikaraporttien yleistiedot, järjestelmänvalvoja ja vähintään yksi hyväksyjä. Lisätietoja tuntiraporttien määrittämisestä on [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md) -kohdassa.  

> [!TIP]
> Tuntiraportteja voi käyttää mobiililaitteessa. Tämän mahdollistamiseksi on ehkä otettava käyttöön **Käytä uutta tuntiraporttikokemusta** -vaihtopainike [Resurssienhallinnan asetukset](https://businesscentral.dynamics.com/?page=462) -sivulla.

## Luo tuntiraportit

Käytä **Luo tuntiraportit** -sivua, kun määrität aikaraportit tietylle määrälle ajanjaksoja tai viikkoja. Tämän jälkeen aikaraportin omistaja voi avata sen ja kirjata ajan, joka tehtävään on kulunut. Voit myös valita, että [eräajo suoritetaan automaattisesti aikataulun mukaan](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Sinulla on oltava oikeudet luoda aikaraportteja. Lisätietoja käyttöoikeuksista on [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md) -kohdassa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo tuntiraportit** ja valitse sitten vastaava linkki.

    > [!TIP]
    > Voit käyttää **Luo tuntiraportit** -toimintoa myös **Resurssit**-luettelosivulla ja **Resurssin kortti** -sivulla.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Varmista ennen tuntiraporttien luomista resurssille, että **Käytä tuntiraporttia**- ja **Tuntiraportin omistajan käyttäjätunnus** -kentät on määritetty niille **Resurssin kortti** -sivulla.

    Voit halutessasi valita **Aikataulu**-toiminnon ja määrittää, kuinka usein tehtävä suoritetaan automaattisesti. Jos haluat esimerkiksi, että tehtävä suoritetaan viikoittain neljän viikon ajan, määritä **Suoritettavan raportin aikatauluttaminen - Luo aikaraportit** -sivulla kenttä **Seuraavan suorituspäivän kaava** arvoon **4W**. Lisätietoja raporttien ajoittamisesta on ohjeaiheessa [Raportin suorittamisen aikatauluttaminen](ui-work-report.md#ScheduleReport)  

Voit tarkastella samoja tuntiraportteja, jotka luot **Tuntiraportit**-sivulla. Jokainen tuntiraportti koostuu yhdestä tai useammasta rivistä, jotka määrittävät hyväksyntää varten lähetettävän ajan. Seuraavassa taulukossa kuvataan, millaisia rivejä voit lisätä tuntiraporttiin.

| **Kenttä** | **Kuvaus** |
|---|---|
| | Voit lisätä muistiinpanon tai merkin **Kuvaus**-kenttään tuntiraportin riville. Tätä kenttää voi esimerkiksi käyttää tuntiraportin tapahtumien luokittelussa. Jos jätät tuntiraportin rivin **Tyyppi**-kentän tyhjäksi, et voi syöttää tämän rivin viikonpäiväkenttiin aika-arvoja. |
| Poissaolo | Voit rekisteröidä ajan, jonka olet poissa työviikon aikana. Täydennä rivin tiedot määrittämällä poissaolostyyppi **Poissaolon syyn koodi** -kentässä. |
| Kokoonpanotilaus | Käytetään ajan rekisteröintiin kokoonpanotilauksissa. Tämän tyypin tuntiraportin rivi luodaan kirjattaessa kokoonpanotilauksen rivit, joihin resurssi on määritetty käyttämään tuntiraportteja. Et voi valita tämäntyyppistä riviä manuaalisesti. |
| Projekti | Käytä ajankäytön rekisteröintiin projektissa. Rivin tiedot viimeistellään määrittämällä projektin numero ja projektitehtävän numero, jolle aikaa rekisteröidään. Voit rekisteröidä ajan riveille, joita et ole aikatauluttanut.|
| Resurssi | Käytä ajankäytön rekisteröintiin resurssissa. Täydennä rivin tiedot antamalla työn kuvaus. |
| Palvelu | Käytä ajankäytön rekisteröintiin huoltotilauksessa tai hyvityslaskussa. |

Haluat esimerkiksi lähettää tuntiraportin viikolta, jona suoritit siivoustehtäviä ja jona sinulla oli vapaapäivä lääkärikäynnin vuoksi. Seuraavassa taulukossa näkyy, miten tuntiraporttiin lisätään rivejä.

| Tyyppi | Kuvaus | Työtyypin koodi | Poissaolon tyypin koodi |
|--|--|--|--|
| Resurssi | Työaika | Siivous |  |
| Poissaolo | Poissaolo |  | Terveys |
|  | Olin tiistaina poissa lääkärin tapaamisen vuoksi. |  |  |

Tässä hypoteettisessa esimerkissä voit sitten rekisteröidä tunnit kullekin arkipäivälle asianomaisille päiville.  

> [!TIP]
> Useimmissa tapauksissa yrityksillä on ennalta määritettyjä työtyyppejä eri rivityypeille. Tällaisissa tapauksissa valitset vain haluamasi työtyypin luettelosta ja lisäät sitten oman kuvauksesi.  
>
> Valitse työtyyppi valitsemalla **Kuvaus**-kentän :::image type="icon" source="media/assist-edit-icon.png" border="false":::-painike, valitsemalla sitten **Toiminnon yksityiskohdat** -toiminto ja määrittämällä se avautuvassa sivussa tai valitsemalla se **Työtyypin koodi**- tai **Poissaolon tyyppi koodi** -kentässä. Tässä tapauksessa voit ohittaa [Työtyyppien määrittäminen ja yhden työtyypin lisääminen tuntiraporttiin](#define-work-types-and-add-one-to-a-time-sheet) -osan.  

## Aikaraportin rivien käyttäminen uudelleen muissa aikaraporteissa

Jos aikaraportin tiedot pysyvät samoina ajanjaksosta toiseen, voit kopioida rivit edelliseltä ajanjaksolta säästääksesi aikaa. Sitten vain kirjoitetaan käytetty aika uudelle jaksolle.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraportit** ja valitse sitten vastaava linkki.  
2. Avaa aikaraportti jaksolle, joka on myöhempi kuin olemassa oleva aikaraportti ja sen rivit.  
3. Valitse **Kopioi rivit aiemmasta aikaraportista** -toiminto.

Rivit kopioidaan, mukaan lukien tarkat tiedot, kuten tyyppi ja kuvaus. Jos rivi liittyy esimerkiksi projektiin, **Projektinro** kopioidaan. Kaikki kopioitujen rivien tila on **Avoin**. Voit nyt muokata rivejä tarpeen mukaan.

## Projektin suunnittelurivien kopioiminen aikaraporttiin

Seuraavassa ohjeessa neuvotaan, miten projektin suunnittelurivejä lisätään nopeasti aikaraporttiin.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraportit** ja valitse sitten vastaava linkki.  
2. Valitse kyseisen ajanjakson tuntiraportti **Tuntiraportit** -sivulla.  
3. Valitse **Luo rivejä projektin suunnittelusta** -toiminto. Kaikki aikaraportin ajanjakson projektin suunnittelurivit kopioidaan sen henkilön tai koneen aikaraporttiin, joka mainitaan aikaraportin **Resurssin nro** -aikaraportissa.

## Työtyyppien määrittäminen ja yhden työtyypin lisääminen aikaraporttiin

Voit määrittää työtyypin kaikissa tuntiraporttiriveissä huoltotilauksia, projektitilauksia ja resursseja varten. Tällä tavalla voit lisätä tiedot, joita tarvitse asiakkaan laskuttamiseen erityyppisistä töistä.  

1. Valitse **Tuntiraportit**-sivulla asianmukainen tuntiraportti.
2. Valitse **Rivit**-osan ensimmäisen rivin kohdalla **Tyyppi**-kenttä ja valitse sitten asianmukainen tyyppi, kuten *Resurssi*.  
3. Valitse **Kuvaus**-kenttä ja täytä kentät **Tuntiraporttirivin resurssien tiedot** -sivulla. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Jos työtyyppiä ei ole, valitse **Uusi**-toiminto.
    2. Täytä **Työtyypit**-sivulla tarvittavat kentät ja palaa sitten takaisin tuntiraporttiin.
4. Täytä tuntiraportin muut kentät. Lisätietoja on saatavilla [Tuntiraporttirivien täyttäminen ja lähettäminen hyväksyttäväksi](#fill-in-time-sheet-lines-and-submit-for-approval) -kohdasta.  

> [!TIP]
> Voit seurata vastaavia työvaiheita määrittääksesi poissaolokoodit.

## Aikaraporttirivien täyttäminen ja lähettäminen hyväksyttäväksi

Aikaraportin rekisteröintiä seurataan tunneissa, resurssien perusmittayksikköissä. Oletusarvon mukaan aikaraportti näyttää yleiset työpäivät maanantaista perjantaihin.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraportit** ja valitse sitten vastaava linkki.  
2. Valitse aikaraportti asianmukaiselle kaudelle.
3. Täytä tarvittaessa rivin kentät. Syötä resurssin kunkin viikonpäivän käyttötunnit.  

    Voit useimmissa tapauksissa seurata työtä lisäämällä rivin, jonka tyyppi on *Resurssi*, ja rekisteröimällä sitten kunakin päivänä käytetyt tunnit. Jos haluat rekisteröidä poissaoloja, lisää rivi, jonka tyyppi on *Poissaolo*.  

    > [!TIP]  
    > Voit esikatsella aikaraportin **Toteutunut/budjetoitu yhteenveto** -tietoruutuun syötettyjä tuntimääriä.  
4. Toista vaihe 3 muille resurssin suorittamille työtyypeille.  

    Määritä seuraavaksi, toimitetaanko kaikki tai valitut tuntiraportin rivit.  

    * Jos haluat lähettää tuntiraportin yhden tai useamman rivin osalta, valitse haluamasi rivi ja valitse sitten **Lähetys**-toiminto.

        Valitse lähetyssivulla **Vain valitut rivit** -toiminto. Rivin tila muuttuu **Avoin**-tilasta **Lähetetty**-tilaan.
    * Jos haluat lähettää tuntiraportin kaikkien avoimien rivien osalta, valitse **Lähetys**-toiminto **Tuntiraportti**-sivun yläosasta.  

        Vahvista, että haluat lähettää kaikki nykyisen tuntiraportin avoimet rivit.  

    > [!NOTE]  
    > Voit lähettää vain ne aikaraporttirivit, joille on annettu aika.  
5. Muokkaa tietoja rivillä, jonka tilaksi on määritetty **Lähetetty**, valitsemalla rivi ja valitsemalla sitten **Avaa uudelleen** -toiminto.

    > [!NOTE]  
    > Esimies voi hylätä aikaraporttirivin, joka on lähetetty hyväksyttäväksi. Jos rivin tila on **Hylätty**, voit muuttaa riviä ja valita sitten uudelleen **Lähetä**-kohdan.  
6. Valitse **OK**-painike.

## Hyväksy tai hylkää aikaraportti

Aikaraportti on lähetettävä hyväksyttäväksi, jotta sitä voidaan käyttää. Voit hyväksyä ja hylätä aikarapportin yksittäisiä rivenä tai lähettää ne takaisin lähettäjälle. Aikaraportti voidaan hyväksyä kahdella seuraavalla tavalla:

* aikaraportin järjestelmänvalvoja voi hyväksyä minkä tahansa aikaraportin
* henkilö, joka on määritetty resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kentässä, voi hyväksyä kyseisen resurssin aikaraportteja. Lisätietoja hyväksynnän määrittämisestä on [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md) -kohdassa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Päällikön tuntiraportit** ja valitse sitten vastaava linkki.
2. Valitse aikaraportti luettelosta.  
3. **Aikaraportti**-sivulla: 
    1. Valitse **Prosessi**-toiminto ja valitse sitten **Hyväksy**-toiminto.
    2. Valitse **Kaikki lähetetyt rivit** -toiminto hyväksyäksesi kaikki rivit tai hyväksy vain **Aikaraportti**-sivulla valitut rivit valitsemalla **Vain valitut rivit** -toiminto.
4. Valitse **OK**-painike.  
5. Vaihtoehtoisesti voit valita **Hylkää**-toiminnon ja suorittaa vaiheet 4 ja 5.  

> [!TIP]  
> Saat yleiskuvauksen aikaraportin tiedoista **Aikaraportin tila**- ja **Toteutunut/budjetoitu yhteenveto** -tietoruutujen avulla.

Kun hyväksyt tai hylkäät aikaraportin, sitä voi muokata vasta sitten, kun aikaraportti on avattu uudelleen. Seuraavassa kerrotaan, miten hyväksytty tai hylätty aikaraportti avataan uudelleen.

## Avaa aikaraportti uudelleen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Päällikön tuntiraportit** tai **Tuntiraportit** ja valitse sitten vastaava linkki.
2. Avaa aikaraportti luettelosta.  

    > [!NOTE]  
    > Voit avata uudelleen vain rivit, joiden tila on **Hyväksytty**. Et voi avata uudelleen rivejä, joiden tila on **Hylätty** tai joka on kirjattu.  
3. Valitse **Aikaraportti**-sivulla **Avaa uudelleen** -toiminto. Avaa sitten uudelleen kaikki rivit valitsemalla **Kaikki lähetetyt rivit** -toiminto tai avaa uudelleen **Aikaraportti**-sivulla valitut rivit valitsemalla **Vain valitut rivit** -toiminto.
4. Valitse **OK**-painike. Aikaraporttien rivin tai rivien tilaksi tulee **Lähetetty**.  

## Aikaraporttien tarkasteleminen ja hyväksyminen projekteittain

Voit määrittää projektissa projektin vastuuhenkilön. Nämä tiedot on linkitetty tuntiraportin riveihin. Linkin avulla projektipäälliköt voivat nähdä luettelon hyväksyttävistä tuntiraporteista. Esimerkiksi tiimin projektipäällikkö voi olla vastuussa tietyistä yrityksen projekteista. Tässä tapauksessa esihenkilö määritetään Projektikortti-sivulla **vastuuhenkilöksi**. Aikaraportin tietojen tässä näkymässä näkyvät projektiin liittyvät projektitehtävät ja käytettyjen tuntien määrä.

> [!NOTE]
> Tuntiraporttien hyväksyminen **Päällikön aikaraportti projekteittain** -sivulla edellyttää, että ensin valitaan **Tuntiraportti projektihyväksynnän mukaan** -vaihtoehto **Resurssien määritys** -sivulla. Lisätietoja siitä, miten resurssien hyväksyminen määritetään on [Resurssien määrittäminen](projects-how-setup-resources.md) -kohdassa.

### Aikaraportin hyväksyminen tai hylkääminen projekteittain

1. Syötä **Etsi**-ruudussa **Päällikön aikaraportti projekteittain** ja valitse sitten vastaava linkki. [!INCLUDE[prod_short](includes/prod_short.md)] näyttää luettelon niihin projekteihin liittyvistä tuntiraporttiriveistä, jotka ovat omalla vastuulla.
2. Valitse **Hyväksy**-toiminto. Hyväksy sitten kaikki rivit valitsemalla **Kaikki lähetetyt rivit** -toiminto tai hyväksy vain **Aikaraportti**-sivulla valitut rivit valitsemalla **Vain valitut rivit** -toiminto.

    > [!NOTE]
    > Voit hyväksyä vain ne tuntilomakkeet, joiden tila on **lähetetty**.

3. Jos haluat antaa lisätietoja hyväksynnästä tai hylkäämisestä, valitse **Aiheeseen liittyvä** -toiminto, valitse **Kommentit** ja sitten **Rivikommentit**.
4. Valitse **OK**-painike.

> [!NOTE]
> Kun olet hyväksynyt tai hylännyt tuntiraportin rivin projektikohtaisesti, et voi avata sitä uudelleen tai muuttaa sitä **Tuntiraportti**-sivulla.

## Tuntiraporttirivien kirjaaminen resurssipäiväkirjaan

Kun olet hyväksynyt resurssin aikaraportin tapahtumia, voit julkaista ne asianmukaiseen resurssipäiväkirjaan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse **Ehdota rivejä aikaraporteista** -toiminto.  
3. Täytä **Ehdota resurssipäiväkirjan rivejä** -sivulla tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Valitse **OK**-painike. Käytön tapahtumat luodaan resurssipäiväkirjaan. Siellä voit muokata tietoja tarvittaessa.  
5. Valitse **Kirjaa**-toiminto.  
6. Vahvista kirjaus valitsemalla **Tapahtumakirjaukset**-toiminto. Näyttöön avautuu **Resurssitapahtumat**-sivu, jossa näkyvät resurssipäiväkirjan kirjausten tulokset.

## Tuntiraporttirivien kirjaaminen projektipäiväkirjaan

Kun olet hyväksynyt projektin aikaraportin tapahtumat, voit kirjata ne soveltuvaan projektipäiväkirjaan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse **Ehdota rivejä aikaraporteista** -toiminto.  
3. Täytä **Ehdota projektipäiväkirjan rivejä** -sivulla tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Valitse **OK**-painike. Käyttötapahtumat luodaan projektipäiväkirjaan, jossa tietoja voidaan muokata tarvittaessa.  

    > [!NOTE]  
    > Tietoja työn tyypistä ja siitä, onko työ on veloitettavissa, kopioidaan aikaraporttiriviltä. Voit tarvittaessa vähentää tuntien määrää ja tehdä osittaisen kirjauksen. Jos vähennät määrää, rivi sisältää jäljellä olevat tunnit, kun valitse seuraavan kerran **Ehdota rivejä aikaraporteista** -toiminto.  
5. Valitse **Kirjaa**-toiminto.  
6. Vahvista kirjaus valitsemalla **Tapahtumakirjaukset**-toiminto. Avautuvalla **Projektitapahtumat**-sivulla näkyy resurssipäiväkirjan kirjausten tulokset.

## Arkistoi tuntiraportit

Kun olet kirjannut aikaraportit, voit arkistoida ne myöhempää käyttöä varten. Kaikki aikaraportin rivit tulee kirjata ennen arkistoimista.

> [!NOTE]  
> Kun arkistoit aikaraportin, se poistetaan sekä **Aikaraportit**-sivun että **Päällikön aikaraportit** -sivun luettelosta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraportit** ja valitse sitten vastaava linkki.
2. Valitse **Siirrä aikaraportit arkistoon** -toiminto.  
3. Täytä **Siirrä aikaraportit arkistoon** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.  
4. Jos haluat tarkastella arkistoituja tuntiraportteja, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraporttiarkistot** tai **Päällikön tuntiraporttiarkistot** ja valitse vastaava linkki.

## Katso myös

[Projektien hallinta](projects-manage-projects.md)  
[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Taloushallinto](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]