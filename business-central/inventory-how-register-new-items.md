---
title: Tavaroiden tai palvelujen nimikekorttien luominen
description: 'Voit luoda nimikekortteja palveluille, joita myydään tunteina, ja fyysisille tuotteille. Esimerkkejä ovat kokoonpanon nimikkeet ja valmiit tavarat, joita myydään varastosta.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 08/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Uusien nimikkeiden rekisteröiminen

Nimikkeet, muun muassa, ovat liiketoimintasi, tavaroiden tai palveluiden perusta, jolla käyt kauppaa. Jokainen nimike on rekisteröitävä nimikekorttina.

## Uuden nimikekortin luominen

Seuraavassa taulukossa esitetään, kuinka ketju on määritetty nimikekortissa. Voit kuitenkin luoda uusia nimikekortteja myös kopioimalla aiemmin luotuja kortteja. Lukeaksesi lisää [Uusien nimikkeiden luominen kopioimalla aiemmin luotuja nimikkeitä](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

[!INCLUDE[create_new_item](includes/create_new_item.md)]

## Käytä nimikemalleja

Voit käyttää erityyppisten nimikkeiden asetuksia uudelleen uusia nimikkeitä luotaessa tallentamalla nimikkeitä nimikemalleina. Nimikemallit helpottavat uusien nimikkeiden lisäysprosessia ja lisäävät nimiketietojen johdonmukaisuutta. Kun rekisteröit uuden nimikkeen, näyttöön tulee sivu, jonka avulla voit valita mallin. Kun olet valinnut mallin, sen asetukset täytetään luotavan nimikkeen osalta. Jos vain yksi nimikemalli on olemassa, uudet nimikkeet käyttävät aina kyseistä mallia. 

### Tallenna nimikekortti tallennusmallina

1. Valitse **Nimikekortti**-sivulla **Tallenna mallina** -toiminto. **Nimikemalli**-sivu avautuu ja näyttää nimikekortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Jos haluat käyttää dimensioita uudelleen malleissa, valitse **Aiheeseen liittyvä** toiminto, valitse **nimike** ja sitten **Dimensiot**. Valitun **nimikkeen oletusdimensiot**, joissa näkyvät nimikkeelle määritetyt dimensiokoodit.
4. Muokkaa tai syötä dimensiokoodit, joita käytetään mallin avulla luotuihin uusiin nimikkeen kortteihin.
5. Kun olet määrittänyt uuden nimikemallin, valitse **OK**-painike.

Nimikemalli lisätään nimikemallien luetteloon niin, että sen avulla voit luoda uusia nimikekortteja.

## Nimiketyypit

Voit valita **Nimikkeen kortti** -sivun **Tyyppi**-kentässä nimikkeen käyttötarkoituksen yrityksessä. Valinta määrittää myös sen, missä määrin voit hallita tavaraa varastossa.

* **Varasto** määrittää, että nimike on fyysinen yksikkö, jota hallitaan ja seurataan varastossa.
* **Muu kuin varasto** ovat fyysisiä yksiköitä, joita ei hallita tai seurata varastossa.
* **Huoltonimikkeet** ovat työajan yksikkö, jota käytetään yleensä huoltojen myyntien tai ostojen rekisteröimiseen.

Jos haluat oppia lisää muista kuin varastonimikkeistä, siirry kohtaan [Tietoja nimiketyypeistä](inventory-about-item-types.md).

> [!TIP]
> On myös luettelonimikkeitä, jotka muistuttavat muita kuin varastonimikkeitä siinä, että ne ovat nimikkeitä, joita tarjotaan asiakkaille, mutta joita ei hallita ennen kuin myyt ne. Saat lisätietoja siirtymällä kohtaan [Luettelonimikkeiden käyttäminen](inventory-how-work-nonstock-items.md).  

## Varaston arvostus

Määritä **Arvostusmenetelmä** -kentässä tapa, jolla nimikkeen yksikkökustannukset lasketaan tekemällä oletuksia fyysisestä tavaravirrasta yrityksen läpi. Käytössä on viisi arvostusmenetelmää nimikkeen tyypin mukaan. Lisätietoja varaston arvostuskustannuksista on kohdassa [Suunnittelun yksityiskohdat: Kulujen edut](design-details-costing-methods.md).

> [!NOTE]
> Jos valitset **Keskiarvo**, nimikkeen yksikkökustannus lasketaan kussakin vaiheessa keskimääräisenä yksikkökustannuksena oston jälkeen. Varastonarvostus olettaa, että kaikki varastot myydään samanaikaisesti. Voit valita tällä asetuksella **Keskimääräisten kustannusten laskennan yleiskuvaus** -sivun **Yksikkökustannus**-kentän, jolla voit tarkastella tapahtumahistoriaa, josta keskimääräinen kustannus lasketaan.

## Luokat, määritteet ja variantit

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Lisätietoja varianteista on kohdassa [Tuotevarianttien hallinta](inventory-item-variants.md).  

## Määritä nimikekorvaukset

Voit määrittää nimikkeille korvaavia tuotteita, kuten muita nimikkeitä, joita voidaan käyttää alkuperäisen nimikkeen tilalla.

### Nimikkeen korvaamisen toteuttaminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Etsi haluamasi nimike ja valitse **nro.** Nimikkeen kortti avaamiseksi.  
3. Valitse **Liittyvä**-toiminto, valitse **Nimike** ja sitten **Korvaamiset** avataksesi **Nimikkeen korvaustapahtuma** -sivun.  
4. Valitse **Korvaava nro** -kenttä ja valitse korvaava nimike luettelosta.
5. Täytä tai muuta muita kenttiä sivulla tarvittaessa.

Kun pyydetty määrä ylittää varastossa saatavilla olevan määrän, näyttöön tulee sanoma, jossa ilmoitetaan korvaavien nimikkeiden olemassaolosta.

> [!NOTE]  
> Huomaa, että nimikkeen korvaaminen ei automaattisesti aiheuta nimikkeen korvaamista toisella nimikkeellä esimerkiksi myyntitilausta luotaessa tai tuoterakenteessa. Sen sijaan sinua varoitetaan siitä, että käytettävissäsi on korvaaminen.

## Hinnat ja alennukset

Voit käyttää nimikkeelle erityishintoja tai -alennuksia tiettyjen kriteerien perusteella. Kriteereihin kuuluvat esimerkiksi asiakas, vähimmäistilausmäärä tai lopetuspäivämäärä. Tämä tehdään valitsemalla **Määritä erikoishinnat**- tai **Määritä erikoisalennukset** -toiminto. Jokainen rivi, esimerkiksi **Myyntihinnat**-sivulla, edustaa erikoishintaa. Jokainen sarake vastaa ehtoa, jonka täytyy olla voimassa, jotta asiakkaalle voidaan myöntää erikoishinta, joka syötetään **Myyntihinnat**-sivun **Yksikköhinta**-kenttään. Lisätietoja hinnoittelusta on myyntihinnan [, alennuksen ja maksusopimusten tallentamista koskevissa tehtävissä](sales-how-record-sales-price-discount-payment-agreements.md).

## Täydennys

Voit määrittää, miten nimikkeitä toimitetaan:

* **Ostotilaus**, jos haluat ostaa nimikkeitä.
* **Kokoonpanotilaus** tai **Tuotantotilaus**, jos nimikkeet tuotetaan talon sisällä.

On muitakin asetuksia, jotka täydentävät näitä valintoja.

### Sisällytä nimikkeet tuoterakenteisiin

Voit järjestää hierarkioita, joilla on päänimike, jonka komponenttinimikkeet ovat kokoonpanossa ja tuotannon tuoterakenteessa. Lisätietoja kokoonpanon tuoterakenteesta on kohdassa [Kokoonpanon tuoterakenteiden käyttö](inventory-how-work-BOMs.md).

### Tuotantotilauksissa käytetyt nimikkeet

Rekisteröidäksesi tuotantotilauksissa käytettäviä nimikkeitä määritä täydennysjärjestelmä Täydennys-pikavälilehdessä **Tuotantotilaukseksi**  **·** . Lisätietoja on kohdassa [Tietoja tuotantotilauksista](production-about-production-orders.md).  

### Ensisijaiset ja vaihtoehtoiset toimittajat

Jos ostat saman nimikkeen useammalta kuin yhdeltä toimittajalta, voit yhdistää kyseiset toimittajat nimikkeen. Käytä **Tuotekortti** **Toimittajat**-toimintoa avataksesi **Tuotetoimittajaluettelo**-sivun. 

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Valitse ensin käsiteltävä nimike ja sitten **Muokkaa**-toiminto.  
3. Valitse **Toimittajat**-toiminto.  
4. Valitse Nro-kenttä **.** -kentästä ja valitse toimittaja, jonka haluat määrittää nimikkeelle.  
5. Voit täyttää myös jäljellä olevat rivit.  
6. Toista vaiheet 2–5 kullekin toimittajalle, jolta haluat ostaa nimikkeitä.

Toimittajat näkyvät nyt nimikkeen kortissa avattavassa **Nimikkeen toimittajaluettelo** -sivulla, jossa voit valita kätevästi vaihtoehtoisen toimittajan.

Jos ostat saman nimikkeen useammalta kuin yhdeltä toimittajalta, voit määrittää hintoja ja alennuksia.  Lisätietoja on kohdassa [Erityisten ostohintojen ja -alennusten tallentaminen](purchasing-how-record-purchase-price-discount-payment-agreements.md).

## Hallitse varastoa fyysisessä varastossa

Kun rekisteröit uuden nimikkeen, näyttöön tulee varastoinnin hallintaan liittyviä kenttiä, erityisesti **Fyysinen varasto** -pikavälilehdessä. Jos organisaatiossasi ei käytetä sovelluksen [!INCLUDE [prod_short](includes/prod_short.md)] varastonhallinnan ominaisuuksia, voit ohittaa kyseiset kentät.  

Jos organisaatio myöhemmin määrittää fyysisen varaston hallinnan, kannattaa varmistaa, että jokaisella olemassa olevalla nimikkeellä on oikeat tiedot eri kentissä. Näin fyysisen varaston prosessit voidaan suorittaa odotetulla tavalla. Tietoja voivat olla esimerkiksi **fyysisen varaston luokkakoodi** tai **hyllytysmallin koodi**. Lisätietoja on kohdassa [Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md).  

## Suunnitt.

Kun yrityksesi käyttää toimitussuunnitteluprosesseja [!INCLUDE [prod_short](includes/prod_short.md)]issa, tarvittavat kentät **Suunnittelu**-pikavälilehdessä on täytettävä. Tutustu suunnittelualueeseen kohdassa [Suunnittelutiedot: Suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md).  

Esimerkkejä **Suunnittelu**-pikavälilehden kenttien käytöstä on kohdassa [Asetuksien parhaat käytännöt: Suunnitteluparametrit](setup-best-practices-planning-parameters.md).  

## Nimikekorttien poistaminen

Jos kirjaat nimikkeelle tapahtuman, et voi poistaa korttia, koska nimiketapahtumia voidaan tarvita varaston arvostamiseen tai valvontaan. Voit poistaa nimiketapahtumia tapahtumakirjauksilta ottamalla yhteyttä Microsoft-kumppaniin koodin avulla.  

## Katso myös

[Vaihto-omaisuus](inventory-manage-inventory.md)    
[Mittayksiköiden määrittäminen](inventory-how-setup-units-of-measure.md)    
[Tuotevarianttien hallinta](inventory-item-variants.md)    
[Intrastat-raportoinnin määrittäminen](finance-how-setup-report-intrastat.md#other-intrastat-configurations)    
[Varaston kustannusten täsmäyttäminen pääkirjanpitoon](finance-how-to-post-inventory-costs-to-the-general-ledger.md)    
[Luo numerosarjat](ui-create-number-series.md)    
[Kirjausryhmien määrittäminen](finance-posting-groups.md)    
[Osto](purchasing-manage-purchasing.md)    
[Myynti](sales-manage-sales.md)    
[Tietoja suunnittelutoiminnoista](production-about-planning-functionality.md)    
[Asetusten parhaat käytännöt: suunnitteluparametrit](setup-best-practices-planning-parameters.md)    
[Asetusten parhaat käytännöt: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)    
[Suunnittelun yksityiskohdat: Suunnittelujärjestelmän keskeiset käsitteet](design-details-central-concepts-of-the-planning-system.md)    
[Suunnittelun yksityiskohdat: Kysynnän ja tarjonnan vastapaino](design-details-balancing-demand-and-supply.md)    
[Suunnittelun yksityiskohdat: Suunnitteluparametrit](design-details-planning-parameters.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
