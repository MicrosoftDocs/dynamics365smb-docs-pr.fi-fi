---
title: Käytä tuntiraportteja
description: 'Tässä ohjeaiheessa kerrotaan, miten voit luoda tuntiraportteja, määrittää tietotyyppejä, täyttää tuntiraportteja ja lähettää ne hyväksyntää varten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 03/01/2022
ms.author: edupont
---
# <a name="use-time-sheets" />Käytä tuntiraportteja

Tuntiraportteja voidaan käyttää kohteessa [!INCLUDE [prod_short](includes/prod_short.md)] poissaolojen sekä projektiin käytetyn ajan ja resurssien seuraamiseen. Ajanhallinnan avulla voit tunnistaa ongelmat aikaisessa vaiheessa ja välttää viiveet tai kustannusylitykset. Resurssi voidaan helposti raportoida tuntiraporttien avulla yksityishenkilölle tai koneelle ja esimies voi helposti tarkastella käyttöä ja jakamista. Tässä artikkelissa kerrotaan, miten tuntiraportti luodaan, työtyypit määritetään, tuntiraportti täytetään ja lähetetään hyväksyttäväksi.  

Voit kopioida projektin suunnittelurivit aikaraportista ja käyttää niitä. Näin tehtäessä tiedot on syötettävä vain yhteen paikkaan, ja ne ovat aina ajantasaisia.

Kun olet hyväksynyt projektin aikaraportin tapahtumia, voit julkaista ne asianmukaiseen projekti- tai resurssipäiväkirjaan.

Ennen kuin käytät aikaraportteja, sinun on määritettävä aikaraporttien yleistiedot, järjestelmänvalvoja ja vähintään yksi hyväksyjä. Lisätietoja on kohdassa [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).  

> [!TIP]
> Vuoden 2021 2. julkaisuaallosta eteenpäin voit hallita määritettyjä työaikataulukoita mobiililaitteessa. Järjestelmänvalvoja voi kuitenkin joutua ottamaan **Ominaisuuden päivitys: Uusi tuntiraporttikokemus** -ominaisuuden käyttöön [Ominaisuuksien hallinta](https://businesscentral.dynamics.com/?page=2610) -sivulla, jotta voit käyttää tätä ominaisuutta. Lisätietoja on kohdassa [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).

## <a name="to-create-time-sheets" />Luo aikaraportit

Käytä **Luo aikaraportit** -eräajoa, kun määrität aikaraportit tietylle määrälle ajanjaksoja tai viikkoja. Tämän jälkeen aikaraportin omistaja voi avata sen ja kirjata ajan, joka tehtävään on kulunut. Voit myös valita, että [eräajo suoritetaan automaattisesti aikataulun mukaan](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Sinulla on oltava oikeudet luoda aikaraportteja. Lisätietoja on kohdassa [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraportit** ja valitse sitten vastaava linkki.
2. Valitse **Tuntiraportit**-sivulla **Luo tuntiraportit** -toiminto.
3. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Aikaraportin resurssikortin **Käytä aikaraporttia**- ja **Aikaraportin omistajan käyttäjätunnus** -kenttä on täytettävä.

    Voit halutessasi valita **Aikataulu**-toiminnon ja määrittää, kuinka usein tehtävä suoritetaan automaattisesti. Jos haluat esimerkiksi, että tehtävä suoritetaan viikoittain neljän viikon ajan, määritä **Suoritettavan raportin aikatauluttaminen - Luo aikaraportit** -sivulla kenttä **Seuraavan suorituspäivän kaava** arvoon *4W*. Lisätietoja on kohdassa [Raportin ajoittaminen suoritettavaksi](ui-work-report.md#ScheduleReport).  
4. Valitse **OK**-painike.  

Voit tarkastella samoja tuntiraportteja, jotka olet luonut **Tuntiraportit**-sivulla. Jokainen tuntiraportti koostuu yhdestä tai useammasta rivistä, jotka määrittävät hyväksyntää varten lähetettävän ajan. Seuraavassa taulukossa kuvataan, millaisia rivejä voit lisätä tuntiraporttiin.

| **Kenttä** | **Kuvaus** |
|---|---|
| | Voit lisätä muistiinpanon tai merkin **Kuvaus**-kenttään tuntiraportin riville. Tätä kenttää voi esimerkiksi käyttää tuntiraportin tapahtumien luokittelussa. Jos jätät tuntiraportin rivin **Tyyppi**-kentän tyhjäksi, et voi syöttää tämän rivin viikonpäiväkenttiin aika-arvoja. |
| Poissaolo | Voit rekisteröidä ajan, jonka olet poissa työviikon aikana. Täydennä rivin tiedot määrittämällä poissaolostyyppi **Poissaolon syyn koodi** -kentässä. |
| Kokoonpanotilaus | Käytetään ajan rekisteröintiin kokoonpanotilauksissa. Tämän tyypin tuntiraportin rivi luodaan kirjattaessa kokoonpanotilauksen rivit, joihin resurssi on määritetty käyttämään tuntiraportteja. Et voi valita tämäntyyppistä riviä manuaalisesti. |
| Projekti | Käytä ajankäytön rekisteröintiin projektissa. Saadaksesi rivin tiedot valmiiksi määritä työnumero ja työn tehtävän numero, jolle haluat rekisteröidä aikaa. Voit rekisteröidä ajan riveille, joita et ole aikatauluttanut.|
| Resurssi | Käytä ajankäytön rekisteröintiin resurssissa. Täydennä rivin tiedot antamalla työn kuvaus. |
| Palvelu | Käytä ajankäytön rekisteröintiin huoltotilauksessa tai hyvityslaskussa. |

Jos haluat esimerkiksi lähettää tuntiraportin työviikolle, jolloin työskentelit siivoustehtävissä useimpina päivinä mutta olit yhden päivän poissa lääkärin tapaamisen vuoksi, sinun tulisi lisätä rivejä seuraavassa taulukossa kuvatulla tavalla.

| Tyyppi | Kuvaus | Työtyypin koodi | Poissaolon tyypin koodi |
|--|--|--|--|
| Resurssi | Työaika | Siivous |  |
| Poissaolo | Poissaolo |  | Terveys |
|  | Olin tiistaina poissa lääkärin tapaamisen vuoksi. |  |  |

Tässä hypoteettisessa esimerkissä asianmukaiset tunnit pitäisi rekisteröidä kunkin viikonpäivän asianmukaisiin kenttiin.  

> [!TIP]
> Useimmissa tapauksissa yrityksillä on ennalta määritettyjä työtyyppejä eri rivityypeille. Tällaisissa tapauksissa valitset vain haluamasi työtyypin luettelosta ja lisäät sitten oman kuvauksesi.  
>
> Valitse työtyyppi valitsemalla **Kuvaus**-kentän :::image type="icon" source="media/assist-edit-icon.png" border="false":::-painike, valitsemalla sitten **Toiminnon yksityiskohdat** -toiminto ja määrittämällä se avautuvassa sivussa tai valitsemalla se **Työtyypin koodi**- tai **Poissaolon tyyppi koodi** -kentässä. Tässä tapauksessa voit ohittaa [Työtyyppien määrittäminen ja yhden työtyypin lisääminen tuntiraporttiin](#to-define-work-types-and-add-one-to-a-time-sheet) -osan.  

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets" />Aikaraportin rivien käyttäminen uudelleen muissa aikaraporteissa

Jos aikaraportin tiedot pysyvät samoina ajanjaksosta toiseen, voit tallentaa ajan kopioimalla rivit edelliseltä ajanjaksolta. Sitten vain kirjoitetaan käytetty aika uudelle jaksolle.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraportit** ja valitse sitten vastaava linkki.  
2. Avaa aikaraportti jaksolle, joka on myöhempi kuin olemassa oleva aikaraportti ja sen rivit.  
3. Valitse **Kopioi rivit aiemmasta aikaraportista** -toiminto.

Rivit kopioidaan, mukaan lukien tarkat tiedot, kuten tyyppi ja kuvaus. Jos rivi liittyy projektiin, **Projektinro** kopioidaan. Kaikki kopioitujen rivien tila on **Avoin**. Voit nyt muokata rivejä tarpeen mukaan.

## <a name="to-copy-job-planning-lines-to-a-time-sheet" />Kopioi työn suunnittelurivit aikaraporttiin
Seuraavassa ohjeessa neuvotaan, miten lisätään projektin suunnittelurivejä nopeasti aikaraportille.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraportit** ja valitse sitten vastaava linkki.  
2. Valitse kyseisen ajanjakson tuntiraportti **Tuntiraportit** -sivulla.  
3. Valitse **Luo rivejä projektin suunnittelusta** -toiminto. Kaikki aikaraportin ajanjakson projektin suunnittelurivit kopioidaan sen henkilön tai koneen aikaraporttiin, joka mainitaan aikaraportin **Resurssin nro** -aikaraportissa.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet" />Työtyyppien määrittäminen ja yhden työtyypin lisääminen aikaraporttiin

Voit määrittää työtyypin kaikissa tuntiraporttiriveissä huoltotilauksia, työtilauksia ja resursseja varten. Tällä tavalla voit lisätä tiedot, joita tarvitse asiakkaan laskuttamiseen erityyppisistä töistä.  

1. Valitse **Tuntiraportit**-sivulla asianmukainen tuntiraportti.
2. Valitse **Rivit**-osan ensimmäisen rivin kohdalla **Tyyppi**-kenttä ja valitse sitten asianmukainen tyyppi, kuten *Resurssi*.  
3. Valitse **Kuvaus**-kenttä ja täytä kentät **Tuntiraporttirivin resurssien tiedot** -sivulla. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Jos työtyyppiä ei ole, valitse **Uusi**-toiminto.
    2. Täytä **Työtyypit**-sivulla tarvittavat kentät ja palaa sitten takaisin tuntiraporttiin.
4. Täytä tuntiraportin muut kentät. Lisätietoja on saatavilla [Tuntiraporttirivien täyttäminen ja lähettäminen hyväksyttäväksi](#to-fill-in-time-sheet-lines-and-submit-for-approval) -kohdasta.  

> [!TIP]
> Vastaavat työvaiheet koskevat poissaolokoodien määrittämistä.

## <a name="to-fill-in-time-sheet-lines-and-submit-for-approval" />Aikaraporttirivien täyttäminen ja lähettäminen hyväksyttäväksi

Aikaraportin rekisteröintiä seurataan tunneissa, resurssien perusmittayksikköissä. Oletusarvon mukaan aikaraportti näyttää yleiset työpäivät maanantaista perjantaihin.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraportit** ja valitse sitten vastaava linkki.  
2. Valitse aikaraportti asianmukaiselle kaudelle.
3. Täytä tarvittaessa rivin kentät. Syötä resurssin kunkin viikonpäivän käyttötunnit.  

    Voit useimmissa tapauksissa seurata työtä lisäämällä rivin, jonka tyyppi on *Resurssi*, ja rekisteröimällä sitten kunakin päivänä käytetyt tunnit. Jos haluat rekisteröidä poissaoloja, lisää rivi, jonka tyyppi on *Poissaolo*.  

    > [!TIP]  
    > Voit esikatsella aikaraportin tuntimäärää, jonka olet antanut **Toteutunut/budjetoitu yhteenveto** -tietoruudussa.  
4. Toista vaihe 3 muille resurssin suorittamille työtyypeille.  

    Sinun täytyy seuraavaksi päättää, haluatko lähettää kaikki tuntiraportin rivit vaiko yksittäisiä rivejä.  

    * Jos haluat lähettää tuntiraportin yhden tai useamman rivin osalta, valitse haluamasi rivi ja valitse sitten **Lähetys**-toiminto.

        Valitse lähetyssivulla **Vain valitut rivit** -toiminto. Rivin tila muuttuu *Avoin*-tilasta *Lähetetty*-tilaan.
    * Jos haluat lähettää tuntiraportin kaikkien avoimien rivien osalta, valitse **Lähetys**-toiminto **Tuntiraportti**-sivun yläosasta.  

        Sinua pyydetään vahvistamaan, että haluat lähettää kaikki nykyisen tuntiraportin avoimet rivit.  

    > [!NOTE]  
    > Voit lähettää vain ne aikaraporttirivit, joille on annettu aika.  
5. Muokkaa tietoja rivillä, jonka tilaksi on määritetty **Lähetetty**, valitsemalla rivi ja valitsemalla sitten **Avaa uudelleen** -toiminto.

    > [!NOTE]  
    >   Esimies voi hylätä aikaraporttirivin, joka on lähetetty hyväksyttäväksi. Jos rivin tila on **Hylätty**, voit muuttaa riviä ja valita sitten uudelleen **Lähetä**-kohdan.  
6. Valitse **OK**-painike.

## <a name="to-approve-or-reject-a-time-sheet" />Hyväksy tai hylkää aikaraportti
Aikaraportti on lähetettävä hyväksyttäväksi, jotta sitä voidaan käyttää. Voit hyväksyä ja hylätä aikarapportin yksittäisiä rivenä tai lähettää ne takaisin lähettäjälle lisätoimenpiteitä varten. Aikaraportti voidaan hyväksyä kahdella seuraavalla tavalla:

* aikaraportin järjestelmänvalvoja voi hyväksyä minkä tahansa aikaraportin
* henkilö, joka on määritetty resurssikortin **Aikaraportin hyväksyjän käyttäjätunnus** -kentässä, voi hyväksyä kyseisen resurssin aikaraportteja. Lisätietoja on kohdassa [Aikaraporttien määrittäminen](projects-how-setup-time-sheets.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Päällikön tuntiraportit** ja valitse sitten vastaava linkki.
2. Valitse aikaraportti luettelosta.  
3. **Aikaraportti**-sivulla 
    1. Valitse **Prosessi**-toiminto ja valitse sitten **Hyväksy**-toiminto.
    2. Valitse **Kaikki lähetetyt rivit** -toiminto hyväksyäksesi kaikki rivit tai hyväksy vain **Aikaraportti**-sivulla valitut rivit valitsemalla **Vain valitut rivit** -toiminto.
4. Valitse **OK**-painike.  
5. Vaihtoehtoisesti voit valita **Hylkää**-toiminnon ja suorittaa vaiheet 4 ja 5.  

> [!TIP]  
>   Saat yleiskuvauksen aikaraportin tiedoista **Aikaraportin tila**- ja **Toteutunut/budjetoitu yhteenveto** -tietoruutujen avulla.

Kun olet hyväksynyt tai hylännyt aikaraportin, sitä voi muokata vasta sitten, kun aikaraportti on avattu uudelleen. Seuraavassa kerrotaan, miten hyväksytty tai hylätty aikaraportti avataan uudelleen.

## <a name="to-reopen-a-time-sheet" />Avaa aikaraportti uudelleen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Päällikön tuntiraportit** tai **Tuntiraportit** ja valitse sitten vastaava linkki.
2. Avaa aikaraportti luettelosta.  

    > [!NOTE]  
    >   Voit avata uudelleen vain rivit, joiden tila on **Hyväksytty**. Et voi avata uudelleen rivejä, joiden tila on **Hylätty**. Et voi avata uudelleen aikaraporttia, jos se on kirjattu.  
3. Valitse **Aikaraportti**-sivulla **Avaa uudelleen** -toiminto. Avaa sitten uudelleen kaikki rivit valitsemalla **Kaikki lähetetyt rivit** -toiminto tai avaa uudelleen **Aikaraportti**-sivulla valitut rivit valitsemalla **Vain valitut rivit** -toiminto.
4. Valitse **OK**-painike. Aikaraporttien rivin tai rivien tilaksi tulee **Lähetetty**.  

## <a name="to-view-and-approve-time-sheets-by-job" />Aikaraporttien tarkasteleminen ja hyväksyminen projektin mukaan

Voit määrittää työssä henkilön, joka on vastuussa työstä. Tiedot linkitetään aikaraportin riveihin, jonka pohjalta voidaan luoda luettelo aikaraporteista, jotka vaativat projektipäällikön tarkistuksen ja hyväksynnän. Esimerkiksi tiimin projektipäällikkö voi olla vastuussa yrityksen tietyistä töistä. Tässä tapauksessa esimies ilmaistaan työkortissa nimellä **Vastuuhenkilö**. Aikaraportin tietojen tässä näkymässä näkyvät projektiivin liittyvät projektitehtävät ja käytettyjen tuntien määrä.

> [!NOTE]
> Jotta voit hyväksyä tuntilomakkeet **Esimiehen tuntilomakkeet projektin mukaan** -ikkunassa, sinun on ensin valittava **Aikaraportin projektihyväksyntä** -vaihtoehto **Resurssien määritys** -sivulla. Lisätietoja on kohdassa [Resurssien määrittäminen](projects-how-setup-resources.md).

### <a name="to-approve-or-reject-a-time-sheet-by-job" />Hyväksy tai hylkää aikaraportti projektin mukaan

1. Syötä **Etsi**-ruudussa **Esimiehen aikaraportti projektin mukaan** ja valitse sitten vastaava linkki. [!INCLUDE[prod_short](includes/prod_short.md)] näyttää luettelon niihin projekteihin liittyvistä työaikataulukko riveistä, joista sinulla on vastuu.
2. Valitse **Hyväksy**-toiminto. Hyväksy sitten kaikki rivit valitsemalla **Kaikki lähetetyt rivit** -toiminto tai hyväksy vain **Aikaraportti**-sivulla valitut rivit valitsemalla **Vain valitut rivit** -toiminto.

    > [!NOTE]
    > Voit hyväksyä vain ne tuntilomakkeet, joiden tila on **lähetetty**.

3. Jos haluat antaa lisätietoja hyväksynnästä tai hylkäämisestä, valitse **Aiheeseen liittyvä** -toiminto, valitse **Kommentit** ja sitten **Rivikommentit** ja kirjoita kommentit.
4. Valitse **OK**-painike.

> [!NOTE]
> Kun olet hyväksynyt tai hylännyt aikaraportin rivin projektin mukaan, sitä ei voi avata tai muokata **Tuntiraportti**-ikkunassa.

## <a name="to-post-time-sheet-lines-in-a-resource-journal" />Aikaraporttirivien kirjaaminen resurssipäiväkirjaan
Kun olet hyväksynyt resurssin aikaraportin tapahtumia, voit julkaista ne asianmukaiseen resurssipäiväkirjaan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Resurssipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse **Ehdota rivejä aikaraporteista** -toiminto.  
3. Täytä **Ehdota resurssipäiväkirjan rivejä** -sivulla tarvittavat kentät.  
4. Valitse **OK**-painike. Käytön tapahtumat luodaan resurssipäiväkirjaan. Siellä voit muokata tietoja tarvittaessa.  
5. Valitse **Kirjaa**-toiminto.  
6. Vahvista kirjaus valitsemalla **Tapahtumakirjaukset**-toiminto. Näyttöön avautuu **Resurssitapahtumat**-sivu, jossa näkyvät resurssipäiväkirjan kirjausten tulokset.

## <a name="to-post-time-sheet-lines-in-a-job-journal" />Aikaraporttirivien kirjaaminen projektipäiväkirjaan
Kun olet hyväksynyt työn aikaraportin tapahtumia, voit julkaista ne asianmukaiseen projektipäiväkirjaan.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Projektipäiväkirjat** ja valitse sitten vastaava linkki.  
2. Valitse **Ehdota rivejä aikaraporteista** -toiminto.  
3. Täytä **Ehdota työpäiväkirjan rivejä** -sivulla tarvittavat kentät.  
4. Valitse **OK**-painike. Käytön tapahtumat luodaan projektipäiväkirjaan. Siellä voit muokata tietoja tarvittaessa.  

    > [!NOTE]  
    >   Tietoja työn tyypistä ja siitä, onko työ on veloitettavissa, kopioidaan aikaraporttiriviltä. Voit tarvittaessa vähentää tuntien määrää ja tehdä osittaisen kirjauksen. Jos vähennät määrää, luotava rivi sisältää jäljellä olevat tunnit, kun valitse seuraavan kerran **Ehdota rivejä aikaraporteista** -toiminto.  
5. Valitse **Kirjaa**-toiminto.  
6. Vahvista kirjaus valitsemalla **Tapahtumakirjaukset**-toiminto. Näyttöön avautuu **Projektitapahtumat**-sivu, jossa näkyvät resurssipäiväkirjan kirjausten tulokset.

## <a name="to-archive-time-sheets" />Arkistoi aikaraportit
Kun olet kirjannut aikaraportit, voit arkistoida ne myöhempää käyttöä varten. Kaikki aikaraporttirivit on kirjattava, ennen kuin aikaraportti voidaan arkistoida.

> [!NOTE]  
>   Kun arkistoit aikaraportin, se poistetaan sekä **Aikaraportit**-sivun että **Päällikön aikaraportit** -sivun luettelosta.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraportit** ja valitse sitten vastaava linkki.
2. Valitse **Siirrä aikaraportit arkistoon** -toiminto.  
3. Täytä **Siirrä aikaraportit arkistoon** -sivulla tarvittavat kentät ja valitse sitten **OK**-painike.  
4. Jos haluat tarkastella arkistoituja tuntiraportteja, valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuntiraporttiarkistot** tai **Päällikön tuntiraporttiarkistot** ja valitse vastaava linkki.

## <a name="see-also" />Katso myös
[Projektinhallinta](projects-manage-projects.md)  
[Projektinhallinnan määrittäminen](projects-setup-projects.md)  
[Rahoitus](finance.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
