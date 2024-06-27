---
title: Ostojen kirjaaminen ostolaskujen avulla
description: 'Tässä artikkelissa kerrotaan, miten varastonimikkeitä ja muita kuin varastonimikkeitä tai resursseja ostetaan luomalla ja kirjaamalla ostolaskuja tai -tilauksia.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="record-purchases-with-purchase-invoices-and-orders"></a>Ostojen kirjaaminen ostolaskujen ja tilausten avulla

Voit luoda ostolaskun tai -tilauksen ostojen kustannusten tallentamiseksi ja ostoreskontran seuraamiseksi. Ostolaskuja ja -tilauksia käytetään varastotasojen dynaamiseen päivittämiseen, jotta voit minimoida varaston kustannukset ja tarjota parempaa asiakaspalvelua. Ostokustannukset, kuten palvelukulut, ja varastoarvot, jotka aiheutuvat ostolaskujen tai -tilausten kirjaamisesta, vaikuttavat tuottolukuihin ja talouden suorituskykyilmaisimiin (KPI) roolikeskuksessasi.

## <a name="record-purchases-with-purchase-invoices"></a>Ostojen kirjaaminen ostolaskujen avulla

Kun varastonimikkeitä vastaanotetaan tai ostettu palvelu on valmis, ostolasku kirjataan varasto- ja taloustietueiden päivittämiseksi ja laskun aktivoimiseksi toimittajalle maksuehtojen mukaan. [Maksujen suorittaminen](payables-make-payments.md).

> [!CAUTION]  
> Älä kirjaa ostolaskun fyysisiä nimikkeitä, ennen kuin vastaanotat nimikkeet ja tiedät oston lopullisen kustannuksen, mahdolliset lisäkustannukset mukaan lukien. Muussa tapauksessa varaston arvo ja voittoluvut voivat olla virheelliset.

### <a name="create-and-post-a-purchase-invoice"></a>Ostolaskun luominen ja kirjaaminen

Seuraavissa vaiheissa kerrotaan, miten ostolasku luodaan. Vaiheet ovat samankaltaisia ostotilauksen luomiselle. Tärkein ero on se, että ostotilauksilla on lisäkenttiä ja -toimintoja nimikkeiden fyysistä käsittelemistä varten.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut**, valitse sitten vastaava linkki.  
2. Syötä **Toimittajan nimi**-kenttään nykyisen toimittajan nimi.

    Muut **Ostolasku**-sivun kentät täytetään nyt valitun toimittajan vakiotiedoilla. Jos toimittajaa ei ole rekisteröity, toimi seuraavasti:

    1. Syötä **Toimittaja nimi** -kenttään uuden toimittajan nimi.
    2. Valitse uuden toimittajan rekisteröimisen valintaikkunassa **Kyllä**.
    3. Lue lisätietoja toimittajan kortin täyttämisestä kohdasta [Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md).  
    4. Kun olet määrittänyt toimittajakortin, valitse **OK** palataksesi **Ostolasku**-sivulle.

3. Täytä tarvittaessa jäljellä olevat kentät **Ostolasku**-sivulla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Voit nyt täyttää ostolaskurivit nimikkeillä tai resursseilla, joita olet ostanut toimittajalta.

    > [!NOTE]  
    > Jos olet määrittänyt toimittajalle toistuvien ostojen rivin, kuten kuukausittaisen täydennystilauksen, voit lisätä nämä rivit laskuun valitsemalla **Hae toistuvat ostorivit** -toiminnon.
4. Syötä **Rivit**-pikavälilehden **Nimikenro**-kenttään varastonimikkeen tai palvelun numero.
5. Syötä **Määrä**-kenttään ostettavien nimikkeiden lukumäärä.

    **Rivisumma**-kenttä päivitetään näyttämään arvoa, joka saadaan kertomalla **Välitön yksikkökustannus** -kentän arvo **Määrä**-kentän arvolla.

    Hinta ja rivin summa näytetään ALV:n kanssa tai ilman riippuen siitä, mitä valitset **Hinnat verojen kanssa** -kenttään toimittajan kortissa.

    Rivien alla olevat summakentät päivitetään automaattisesti aina, kun luot tai muokkaat rivejä ja näytät summat, jotka kirjataan päiväkirjoihin.

6. Syötä **Laskun alennussumma** -kenttään summa, joka vähennetään laskun alaosan **Yhteensä sis. ALV:n** -kentässä olevasta arvosta.

    > [!NOTE]  
    > Jos toimittajalle on määritetty laskualennukset, määritetty prosenttiluvun arvo lisätään automaattisesti **Toimittajalaskun alennus-%** -kenttään, jos ehdot täyttyvät. Liittyvä summa syötetään **Laskun alennussumma** -kenttään.
7. Kun vastaanotat ostettuja nimikkeitä tai palveluita, valitse **Kirjaa**.

Osto vaikuttaa nyt varastoon, resurssitapahtumiin ja taloustietueisiin, ja myyjän maksu on aktivoitu. Ostolasku poistetaan ostolaskujen luettelosta ja korvataan uudella asiakirjalla kirjattujen ostolaskujen luettelosta. Lisätietoja ostoasiakirjojen kirjaamista on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md#posting-purchases).

> [!NOTE]
> Kirjatut summat ovat harvoin erilaisia kuin summakenttien summat. Tämä johtuu yleensä arvonlisäveroon (ALV) liittyvistä pyöristyslaskelmista.
>
> Voit tarkistaa kirjattavat summat menemällä **Tilastotiedot**-sivulle. Sivulla otetaan huomioon pyöristyslaskelmat. Jos valitset **Vapauta**-toiminnon, summakentät päivitetään niin, että ne sisältävät pyöristyslaskelmat.

## <a name="posted-invoices"></a>Kirjatut laskut

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Voit helposti korjata tai peruuttaa kirjatun ostolaskun ennen kuin maksua toimittajalle. Esimerkiksi, jos sinun täytyy korjata kirjoitusvirhe tai muuttaa ostoa tilausprosessin alkuvaiheessa. Lisätietoja kohdassa [Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Jos haluat peruuttaa oston nimikkeille tai palveluille, jotka on lueteltu kirjatussa ostolaskussa, jonka maksu on käsitelty, luo oston hyvityslasku. Lisätietoja kohdassa [Ostopalautusten tai peruutusten käsittely](purchasing-how-process-purchase-returns-cancellations.md).

[Avaa **Kirjatut ostolaskut** -luettelo](https://businesscentral.dynamics.com/?page=146) [!INCLUDE [prod_short](includes/prod_short.md)] -ratkaisussa.

## <a name="purchasing-noninventory-items"></a>Muiden kuin varastonimikkeiden osto

Ostolaskun rivejä voivat olla **Resurssi**- tai **Nimike**-tyyppiä. Tuotekortit voidaan luokitella edelleen **varasto**-, **palvelu**- tai **ei-varasto**-tyyppiin, mikä määrittää, onko tuote fyysinen varastoyksikkö, työaikayksikkö (koskee myös resursseja) vai fyysinen yksikkö, jota ei säilytetä inventaarioon. Lisätietoja on kohdassa [Uusien nimikkeiden rekisteröinti](inventory-how-register-new-items.md). Ostolaskuprosessi on sama kaikille mainituille nimiketyypeille.

> [!NOTE]
> **Resurssi**-ostorivityypin avulla voit ostaa myös ulkoisia resursseja, kuten esimerkiksi laskuttaa toimittajaa tehdystä työstä. Lisätietoja kohdassa [Resurssien määrittäminen](projects-how-setup-resources.md).
>
> Jos haluat käyttää ostettua resurssia, resurssin kapasiteetti on mahdollisesti määritettävä ja liitettävä manuaalisesti projektiin. Resurssin ostaminen luo resurssitapahtuman. Resurssitapahtumia ei kuitenkaan seurata määrän ja arvon osalta kuten esimerkiksi nimikkeitä. Jos määrän ja arvon seuranta on pakollista, kannattaa harkita muiden rivinimiketyyppien käyttämistä.

## <a name="when-to-use-purchase-orders"></a>Ostotilausten käyttö

Käytä ostotilauksia, jos sinun tarvitsee tallentaa tilausmäärän osittaisia vastaanottoja. Esimerkiksi siksi, että koko määrä ei ole saatavilla toimittajalla. Jos toimitat nimekkeitä suoraan toimittajalta asiakkaalle suoratoimituksena, ostotilauksia on käytettävä. Lisätietoja on kohdassa [Tee suoratoimituksia](sales-how-drop-shipment.md).

Kaikilta muilta osin ostotilaukset toimivat samalla tavalla kuin ostolaskut. Seuraava toimenpide perustuu ostolaskuun. Vaiheet ovat samankaltaisia ostotilaukselle.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="receive-items-with-a-purchase-order"></a>Nimikkeiden vastaanottaminen ostotilauksella

Seuraavat vaiheet kuvailevat, miten nimikkeitä vastaanotetaan ostotilauksella. 

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ostotilaukset**, valitse sitten vastaava linkki.
2. Avaa aiemmin luotu ostotilaus tai luo uusi myyntitilaus.
3. Anna **Vastaanotettava määrä** -kenttään vastaanotettu määrä.

   > [!NOTE]
   > Jos vastaanotettu määrä on suurempi kuin ostotilauksen määrä ja toimittajalle on määritetty vastaanoton ylittävä määrän salliminen, ylimääräinen määrä käsitellään **Vastaanoton ylitys** -kentässä. Lue lisätietoja [Tilattua määrää useampien nimikkeiden vastaanottaminen](purchasing-how-record-purchases.md#receive-more-items-than-you-ordered) -osiosta.
4. Valitse **Kirjaa**-toiminto.

  **Määrä vast.otettu** -kentän arvo päivitetään. Jos vastaanotto on osittainen, arvo on pienempi kuin **Määrä**-kentän arvo.

> [!NOTE]
> Jos käytössä fyysisen varaston käsittely, ostotilauksen **Kirjaa**-toimintoa ei voi käyttää vastaanoton rekisteröintiin. Tämä johtuu siitä, että varastotyöntekijä on jo kirjannut ostotilauksen määrän vastaanotetuksi. Lisätietoja on kohdassa [Rakennetiedot – saapuvan fyysisen varastoinnin virta](design-details-inbound-warehouse-flow.md).

## <a name="receive-more-items-than-you-ordered"></a>Tilattua määrää useamman nimikkeen vastaanottaminen

Jos saapuvia tavaroita on enemmän kuin tilattuja, ne halutaan ehkä vastaanottaa vastaanoton peruuttamisen sijaan. Voi esimerkiksi olla halvempaa pitää ylimääräiset nimikkeet varastossa kuin palauttaa ne. Toimittaja voi myös tarjota alennuksen nimikkeiden pitämisestä.

Seuraavassa videossa kuvataan, miten ylittäviä määriä voi käsitellä.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2PE]

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### <a name="set-up-over-receipts"></a>Vastaanoton ylittävän määrän määrittäminen

Ylittävän määrän koodien luominen määrittämään prosenttiosuus, jolla vastaanotettu määrä voi ylittää tilatun määrän. Prosenttiosuuden määrittäminen **Vastaanoton ylittävän määrän toleranssi-%** -kentässä. Sen jälkeen nimikkeille ja toimittajille määritetään koodi Nimikekortti- tai Toimittajakortti-sivuilla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Vastaanoton ylittävän määrän koodit** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="assign-the-over-receipt-code-to-an-item"></a>Vastaanoton ylittävän määrän koodin määrittäminen nimikkeelle

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet**, valitse sitten vastaava linkki.
2. Avaa nimikkeen **Nimikekortti**-sivu.
3. Valitse **Vastaanoton ylittävän määrän koodi** -kentässä koodin prosenttiosuus. Tämä prosenttiosuus ilmaisee sallitun vastaanoton ylittävän määrän.

Vastaanoton ylittävän määrän koodi on määritetty nimikkeelle. Nimikkeen ostotilaukset tai fyysisen varaston vastaanotot sallivat nyt tilattua määrää suuremman määrän vastaanoton vastaanoton ylittävän määrän toleranssiprosentin mukaan.

> [!NOTE]
> Voit määrittää hyväksynnän työnkulun, jos vastaanoton ylittävät määrät on hyväksyttävä ennen käsittelemistä. Valitse **Hyväksyntä vaaditaan** -valintaruutu **Vastaanoton ylittävän määrän koodit** -sivulla. Lisätietoja on kohdassa [Työnkulkujen luominen](across-how-to-create-workflows.md).

### <a name="over-receive-an-order"></a>Tilauksen vastaanoton ylitys

Ostoriveillä ja varaston vastaanoton riveillä käytetään **Vastaanoton ylittävä määrä** -kenttää tallennettaessa vastaanoton ylittävät määrät. Nämä ovat määriä, jotka ylittävät tilatun määrän arvon **Määrä**-kentässä.

Kun käsittelet vastaanoton ylittävää määrää, voit suurentaa arvoa **Vastaanotettava määrä** -kentässä vastaamaan vastaanotettua määrää. **Vastaanoton ylittävä määrä** -kenttä päivittyy näyttämään ylimääräisen määrän. Vaihtoehtoisesti voit syöttää ylimääräinen määrä **Vastaanoton ylittävä määrä** -kenttään. **Vastaanotettava määrä** -kenttä päivittyy näyttämään tilatun määrän ja ylimääräisen määrän summan. Seuraavassa kerrotaan, miten **Vastaanotettu määrä** -kenttä täytetään.  

1. Jos ostotilauksen tai varaston vastaanoton asiakirjan vastaanotettu määrä on suurempi kuin tilattu, anna **Vastaanotettu määrä** -kenttään vastaanotettu määrä.

    Jos lisäys on määritetyn vastaanoton ylittävän määrän koodin toleranssin rajoissa, **Vastaanoton ylittävä määrä** -kenttä päivittyy näyttämään arvon, jolla **Määrä**-kenttä on ylitetty.

    Jos lisäys ylittää toleranssin, vastaanoton ylittävää määrää ei sallita. Tarkista, salliiko jokin muu vastaanoton ylittävän määrän koodi sen. Muussa tapauksessa voidaan vastaanottaa vain tilattu määrä ja ylimääinen määrä on käsiteltävä muulla tavalla. Se voi tarkoittaa esimerkiksi palauttamista toimittajalle.

2. Kirjaa vastaanotto samalla tavalla kuin muut vastaanotot.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] ei automaattisesti käsittele vastaanoton ylittävien määrien taloudellisia seikkoja. Tämä on käsiteltävä manuaalisesti yhdessä toimittajan kanssa esimerkiksi niin, että toimittaja lähettää uuden tai päivitetyn laskun.

## <a name="external-document-number"></a>Ulkoisen tiedoston numero

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="posting-purchases"></a>Ostojen kirjaaminen

Voit valita ostoasiakirjassa seuraavien kirjaustoimintojen välillä:

* **Kirjaa**
* **Esikatsele kirjausta**
* **Kirjaa ja tulosta**
<!--* **Test Report**-->
* **Kirjaa erä**

Kun ostoasiakirja on kirjattu, toimittajan tili, pääkirjanpito (KP), nimiketapahtumat ja resurssitapahtumat päivitetään.

Jokaiselle ostoasiakirjalle luodaan ostotapahtuma **KP-tapahtuma**-taulukkoon. Myös toimittajan tilille **Toimittajatapahtuma**-taulukkoon luodaan tapahtuma ja lisäksi luodaan KP-tapahtuma asianmukaiselle ostovelkatilille. Lisäksi oston kirjauksen tuloksena saattaa olla arvonlisäverotapahtuman (ALV) ja KP-tapahtuman luonti alennussummalle. Se, kirjataanko alennukselle tapahtuma, määräytyy **Ostojen ja ostovelkojen asetukset** -sivun **Alennuksen kirjaus** -kentän sisällön perusteella.

Kullekin ostoriville luodaan soveltuvin osin tapahtumat:

* **Nimiketapahtuma**-taulukkoon, jos ostorivin tyyppi on **Nimike**.
* **KP-tapahtuma**-taulukkoon, jos ostorivien tyyppi on **KP-tili**.
* **Resurssitapahtuma**-taulukkoon, jos ostorivin tyyppi on **Resurssi**.

Lisäksi ostoasiakirjat tallennetaan aina **Tavaran vastaanoton otsikko**- ja **Ostolaskun otsikko** -taulukoihin.

Kirjausten tuloksena olevia kirjanpitotapahtumia voi aina tarkastella. Tarkista asiakirja valitsemalla **Esikatsele kirjausta** ja tarkastele oletettuja tapahtumia.


> [!IMPORTANT]  
> Kun kirjaat ostotilauksen nimikkeille, voit luoda sekä vastaanoton että laskun. Nämä voidaan luoda joko yhtäaikaa tai erikseen. Voit luoda osittaisen vastaanoton ja osittaisen laskutuksen täyttämällä **Vastaanotettava määrä** ja **Laskutettava määrä** -kentät yksittäisillä ostotilausriveillä ennen kirjausta. Huomaa, ettet voi luoda ostolaskua ostotilauksesta sellaisille tuotteille tai palveluille, joita ei ole vastaanotettu. Siispä ennen laskuttamista on täytynyt tallentaa vastaanotto, tai sinun täytyy valita samanaikainen vastaanotto ja laskutus.

Voit kirjata tai kirjata ja tulostaa. Jos valitset kirjaamisen ja tulostamisen, raportti tulostetaan tilauksen kirjaamisen yhteydessä. **Kirjaa erä** -toiminnon kirjataksesi useita tilauksia samanaikaisesti. Lue lisätietoja kohdasta [Useiden asiakirjojen kirjaaminen samanaikaisesti](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Kirjaustapahtuminen katselu

Kun kirjaus on päättynyt, kirjatut ostorivit poistuvat tilauksesta. Viesti kertoo, milloin kirjaus on suoritettu loppuun. Tämän jälkeen voit nähdä kirjatut tapahtumat useissa kirjattuja tapahtumia sisältävissä sivuilla, kuten **Toimittajatapahtumat**, **KP-tapahtumat**, **Nimiketapahtumat**, **Resurssitapahtumat**, **Ostovastaanotot** ja **Kirjatut ostolaskut**.

Useimmissa tapauksissa voit avata tapahtumat kortista tai asiakirjasta, johon ne vaikuttavat. Valitse esimerkiksi **Toimittajakortti**-sivulla **Tapahtumat**-toiminto.

## <a name="editing-ledger-entries"></a>Kirjaustapahtuminen muokkaus

Voit muokata arvoja kirjattujen ostoasiakirjojen tietyissä kentissä, kuten **Maksuviite**-kentässä. Lisätietoja on kohdassa [Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md). Jos sinulla on enemmän kriittisiä kenttiä, jotka vaikuttavat jäljitysketjuun, sinun täytyy peruuttaa tai kumota kirjaus. Lue lisätietoja kohdasta [Päiväkirjakirjauksen peruuttaminen sekä vastaanottojen tai toimitusten kumoaminen](finance-how-reverse-journal-posting.md).

## <a name="see-also"></a>Katso myös

[Tarjousten pyytäminen](purchasing-how-request-quotes.md)  
[Nimikkeiden ostaminen myyntiin](purchasing-how-purchase-products-sale.md)  
[Suoratoimitusten valmisteleminen](sales-how-drop-shipment.md)  
[Osto](purchasing-manage-purchasing.md)  
[Ostojen määrittäminen](purchasing-setup-purchasing.md)  
[Resurssien määrittäminen](projects-how-setup-resources.md)  
[Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[Kirjattujen asiakirjojen muokkaaminen](across-edit-posted-document.md)  
[Useiden asiakirjojen kirjaaminen samanaikaisesti](ui-batch-posting.md)  
[Osto](purchasing-manage-purchasing.md)  
[Asiakirjojen ja päiväkirjojen kirjaaminen](ui-post-documents-journals.md)  
[Maksamattomien ostolaskujen korjaaminen tai peruuttaminen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
