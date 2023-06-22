---
title: Tavaroiden tai palvelujen nimikekorttien luominen (sisältää videon)
description: 'Voit luoda nimikekortteja palveluille, joita myydään tunteina, ja fyysisille tuotteille. Esimerkkejä ovat kokoonpanon nimikkeet ja valmiit tavarat, joita myydään varastosta.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: edupont
---
# <a name="register-new-items" />Uusien nimikkeiden rekisteröiminen

Nimikkeet ovat muiden tuotteiden ohella liiketoimintasi perusta; ne ovat siis tavaroita ja palveluja, joilla käyt kauppaa. Jokainen nimike on rekisteröitävä nimikekorttina.

Nimikekortti sisältää tiedot, jotka tarvitaan nimikkeiden ostamista, tallentamista, myymistä ja toimittamista varten.

Nimikkeen kortin tyyppi voi olla **Varasto**, **Huolto** tai **Muu kuin varasto**. Se määrittää, onko nimike fyysisen varasto yksikkö, työn aikayksikkö vai fyysinen yksikkö, jota ei seurata varastossa. Lisätietoja on kohdassa [Tietoja nimiketyypeistä](inventory-about-item-types.md).

Nimike voi olla tuoterakenteessa päänimike, jonka alla on alinimikkeitä. Lisätietoja kokoonpanon tuoterakenteista ja tuotannon tuoterakenteista on kohdassa [Tuoterakenteiden käyttäminen](inventory-how-work-BOMs.md).

Jos ostat saman nimikkeen useammalta kuin yhdeltä toimittajalta, voit yhdistää kyseiset toimittajat nimikkeen korttiin. Toimittajat näkyvät sitten **Nimikkeen toimittajaluettelo** -sivulla, jossa voit valita kätevästi vaihtoehtoisen toimittajan.

*Luettelonimikkeet* ovat nimikkeitä, joita tarjoat asiakkaille, mutta joita et halua ylläpitää järjestelmässäsi ennen kuin niitä myydään. Luettelonimikkeet eivät ole tavallisia nimikkeitä, joiden tyyppi on **Muu kuin varasto**. Lisätietoja on kohdassa [Luettelonimikkeiden muokkaaminen](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Jos eri nimiketyypeillä on nimikemalleja, sivu avautuu, kun luot uuden nimikekortin, jossa voit valita sopivan mallin. Jos vain yksi nimikemalli on olemassa, uudet nimikekortit käyttävät aina kyseistä mallia.

Seuraavaksi selitetään, miten nimikekortti luodaan alusta lähtien. Voit luoda uusia nimikekortteja myös kopioimalla aiemmin luotuja kortteja. Lisätietoja on kohdassa [Uusien nimikkeiden luominen kopioimalla aiemmin luotuja nimikkeitä](inventory-how-copy-items.md).  

<br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card" />Uuden nimikekortin luominen

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> Määritä **Arvostusmenetelmä** -kentässä tapa, jolla nimikkeen yksikkökustannukset lasketaan tekemällä oletuksia fyysisestä tavaravirrasta yrityksen läpi. Käytössä on viisi arvostusmenetelmää nimikkeen tyypin mukaan. Katso lisätietoja kohdasta [Rakennetiedot: arvostusmenetelmät](design-details-costing-methods.md).
>
> Jos valitset **Keskiarvo**, nimikkeen yksikkökustannus lasketaan kussakin vaiheessa keskimääräisenä yksikkökustannuksena oston jälkeen. Varastonarvostus olettaa, että kaikki varastot myydään samanaikaisesti. Voit valita tällä asetuksella **Keskimääräisten kustannusten laskennan yleiskuvaus** -sivun **Yksikkökustannus**-kentän, jolla voit tarkastella tapahtumahistoriaa, josta keskimääräinen kustannus lasketaan.

Voit tarkastella tai muokata erityiset hinnat tai alennukset, jotka haluat myöntää nimikkeelle, tai toimittajasi myöntää sinulle, jos tietyt ehdot, kuten asiakas, vähimmäistilausmäärä tai päättymispäivämäärä, täyttyvät. Tämä tehdään valitsemalla **Määritä erikoishinnat**- tai **Määritä erikoisalennukset** -toiminto. Jokainen rivi, esimerkiksi **Myyntihinnat**-sivulla, edustaa erikoishintaa. Jokainen sarake vastaa ehtoa, jonka täytyy olla voimassa, jotta asiakkaalle voidaan myöntää erikoishinta, joka syötetään **Myyntihinnat**-sivun **Yksikköhinta**-kenttään. Lisätietoja on kohdassa [myyntihinnan, alennuksen ja maksusopimusten kirjaaminen](sales-how-record-sales-price-discount-payment-agreements.md) tai [erityisten ostohintojen ja alennusten kirjaaminen](purchasing-how-record-purchase-price-discount-payment-agreements.md).

Nimike on nyt rekisteröity ja nimikekortti on valmis käytettäväksi osto- ja myyntiasiakirjoissa.

Jos haluat käyttää tätä nimikekorttia mallina, kun luot uusia nimikkeen kortteja, tallenna se mallina. Lisätietoja on seuraavassa osassa.  

### <a name="to-save-the-item-card-as-a-template" />Nimikekortin tallentaminen mallina

1. Valitse **Nimikekortti**-sivulla **Tallenna mallina** -toiminto. **Nimikemalli**-sivu avautuu ja näyttää nimikekortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-sivu avautuu ja esittää kaikki dimensiokoodit, jotka on määritetty nimikkeelle.
4. Muokkaa tai syötä dimensiokoodit, joita käytetään mallin avulla luotuihin uusiin nimikkeen kortteihin.
5. Kun olet määrittänyt uuden nimikemallin, valitse **OK**-painike.

Nimikemalli lisätään nimikemallien luetteloon niin, että sen avulla voit luoda uusia nimikekortteja.

### <a name="items-used-in-production-orders" />Tuotantotilauksissa käytetyt nimikkeet

Jos halutaan rekisteröidä myöhemmin tuotantotilauksessa käytettäviä nimikkeitä, täydennysjärjestelmä määritetään *tuotantotilauksena* **Täydennys**-pikavälilehdessä. Lisätietoja on kohdassa [Tietoja tuotantotilauksista](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item" />Useiden toimittajien määrittäminen nimikkeille

Jos ostat saman nimikkeen useammalta kuin yhdeltä toimittajalta, sinun tulee syöttää tietoja kustakin nimikkeen toimittajasta, esimerkiksi hinnat, toimitusaika ja alennukset.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Valitse ensin käsiteltävä nimike ja sitten **Muokkaa**-toiminto.  
3. Valitse **Toimittajat**-toiminto.  
4. Valitse **Toimittajan nro** -kenttä, ja valitse toimittaja, jonka haluat määrittää nimikkeelle.  
5. Voit täyttää myös jäljellä olevat rivit.  
6. Toista vaiheet 2–5 kullekin toimittajalle, jolta haluat ostaa nimikkeitä.

Toimittajat näkyvät nyt nimikkeen kortissa avattavassa **Nimikkeen toimittajaluettelo** -sivulla, jossa voit valita kätevästi vaihtoehtoisen toimittajan.

## <a name="set-up-item-substitutions" />Määritä nimikekorvaukset

Voit määrittää nimikkeille korvaavia tuotteita, kuten muita nimikkeitä, joita voidaan käyttää alkuperäisen nimikkeen tilalla.

### <a name="to-make-an-item-substitution" />Nimikkeen korvaamisen toteuttaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Etsi asianmukainen nimike ja avaa nimikekortti valitsemalla **Nimikenro**-painike.  
3. Valitse **Liittyvä**-toiminto, valitse **Nimike** ja sitten **Korvaamiset** avataksesi **Nimikkeen korvaustapahtuma** -sivun.  
4. Valitse **Korvaava nro** -kenttä ja valitse korvaava nimike luettelosta.
5. Täytä tai muuta muita kenttiä sivulla tarvittaessa.

Kun pyydetty määrä on suurempi kuin määrä, joka on saatavilla varastossa, näyttöön tulee viesti, joka ilmoittaa, että korvaavia nimikkeitä on olemassa.

> [!NOTE]  
> Huomaa, että nimikkeen korvaaminen ei automaattisesti aiheuta nimikkeen korvaamista toisella nimikkeellä esimerkiksi myyntitilausta luotaessa tai tuoterakenteessa. Sen sijaan sinua varoitetaan siitä, että käytettävissäsi on korvaaminen.

## <a name="categories-attributes-and-variants" />Luokat, määritteet ja variantit

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Lisätietoja varianteista on kohdassa [Tuotevarianttien hallinta](inventory-item-variants.md).  

## <a name="deleting-item-cards" />Nimikekorttien poistaminen

Jos olet kirjannut nimikkeelle tapahtuman, et voi poistaa korttia, koska nimiketapahtumia voi tarvita varaston arvostamiseen tai valvontaan. Voit poistaa nimiketapahtumia tapahtumakirjauksilta ottamalla yhteyttä Microsoft-kumppaniin koodin avulla.  

## <a name="manage-inventory-in-warehouses" />Hallitse varastoa fyysisessä varastossa

Kun rekisteröit uuden nimikkeen, näyttöön tulee varastoinnin hallintaan liittyviä kenttiä, erityisesti **Fyysinen varasto** -pikavälilehdessä. Jos organisaatiossasi ei käytetä sovelluksen [!INCLUDE [prod_short](includes/prod_short.md)] varastonhallinnan ominaisuuksia, voit ohittaa kyseiset kentät.  

Jos organisaatio myöhemmin määrittää fyysisen varaston hallinnan, kannattaa varmistaa, että jokaisella olemassa olevalla nimikkeellä on oikeat tiedot eri kentissä. Näin fyysisen varaston prosessit voidaan suorittaa odotetulla tavalla. Tietoja voivat olla esimerkiksi **fyysisen varaston luokkakoodi** tai **hyllytysmallin koodi**. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

## <a name="planning" />Suunnitt.

Kun yrityksesi käyttää toimitussuunnitteluprosesseja [!INCLUDE [prod_short](includes/prod_short.md)]issa, tarvittavat kentät **Suunnittelu**-pikavälilehdessä on täytettävä. Tutustu suunnittelualueeseen kohdassa [Suunnittelutiedot: Suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md).  

Esimerkkejä **Suunnittelu**-pikavälilehden kenttien käytöstä on kohdassa [Asetuksien parhaat käytännöt: Suunnitteluparametrit](setup-best-practices-planning-parameters.md).  

## <a name="see-related-microsoft-trainingtrainingmodulescreate-items" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-items/)

## <a name="see-also" />Katso myös

[Varasto](inventory-manage-inventory.md)  
[Mittayksikön määrittäminen](inventory-how-setup-units-of-measure.md)  
[Tuotevarianttien hallinta](inventory-item-variants.md)  
[Intrastat-raportoinnin määrittäminen](finance-how-setup-report-intrastat.md#other-intrastat-configurations)  
[Varaston kustannusten täsmäyttäminen pääkirjanpitoon](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Numerosarjojen luominen](ui-create-number-series.md)  
[Kirjausryhmien määrittäminen](finance-posting-groups.md)  
[Osto](purchasing-manage-purchasing.md)  
[Myynti](sales-manage-sales.md)  
[Tietoja toimintojen suunnittelusta](production-about-planning-functionality.md)  
[Asetukset - parhaat käytännöt: suunnitteluparametrit](setup-best-practices-planning-parameters.md)  
[Asetukset - parhaat käytännöt: toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[Rakennetiedot: Suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)  
[Rakennetiedot: kysynnän ja tarjonnan täsmäytys](design-details-balancing-demand-and-supply.md)  
[Rakennetiedot: suunnittelun parametrit](design-details-planning-parameters.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
