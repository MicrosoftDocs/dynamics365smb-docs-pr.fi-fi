---
title: Tietoja toimintojen suunnittelusta
description: 'Suunnittelu ottaa kaikki kysyntä- ja tarjontatiedot huomioon, laskee tulosten nettoarvon ja luo ehdotuksia, joita noudattamalla tarjonta ja kysyntä voidaan saattaa tasapainoon.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5430
ms.date: 08/30/2022
ms.author: bholtorf
---
# <a name="about-planning-functionality"></a><a name="about-planning-functionality"></a>Tietoja toimintojen suunnittelusta

Suunnittelujärjestelmä ottaa kaikki kysyntä- ja tarjontatiedot huomioon, nettouttaa tulokset ja luo ehdotuksia, joita noudattamalla tarjonta ja kysyntä voidaan saattaa tasapainoon.  

Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Toimitusten suunnittelu](design-details-supply-planning.md)  

> [!NOTE]  
> Saat lisätietoja kaikkien tässä ohjeaiheessa mainittujen kenttien toiminnoista lukemalla työkaluvihjeen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><a name="demand-and-supply"></a>Kysyntä ja tarjonta

Suunnittelu koostuu kahdesta osasta, jotka ovat kysyntä ja tarjonta. Ne täytyy pitää tasapainossa, jotta kysyntään voidaan varmasti vastata taloudellisesti ja ajallaan.  

- Kysyntä on yleinen termi, jota käytetään kaikenlaista bruttotarpeesta, esimerkiksi myyntitilauksesta, huoltotilauksesta, kokoonpano- tai tuotantotilausten osatarpeesta, lähtevästä siirrosta, puitetilauksesta tai ennusteesta. Näiden lisäksi sovellus sallii myös tiettyjen muiden teknisten kysyntätyyppien käyttämisen. Tällaisia tarpeita ovat esimerkiksi negatiivinen tuotanto- tai ostotilaus, negatiivinen varasto ja ostopalautustilaus.  
- Tarjonta viittaa mihin tahansa täydennykseen, joka voi olla täydennys esimerkiksi varastosaldolle, ostotilauksille, kokoonpanotilauksille, tuotantotilauksille tai saapuvalle siirrolle. Vastaavalla tavalla voi olla negatiivinen myynti tai huoltotilaus, negatiivinen osatarve tai myyntipalautus, joka jollakin tavoin edustaa myös tarjontaa.  

Suunnittelujärjestelmän toinen tavoite on varmistaa, että varasto ei kasva tarpeettoman suureksi. Jos kysyntä vähenee, suunnittelujärjestelmä ehdottaa tehtyjen täydennystilausten lykkäämistä, pienentämistä tai peruuttamista.  

## <a name="planning-calculation"></a><a name="planning-calculation"></a>Suunnittelulaskenta

Suunnittelujärjestelmän perustana ovat arvioitu ja todellinen asiakaskysyntä sekä varaston uusintatilausten parametrit. Kun suunnitelma lasketaan, sovellus ehdottaa tiettyjä toimenpiteitä ([toimenpideviestit](production-how-to-run-mps-and-mrp.md#action-messages)), jotka liittyvät alihankkijatäydennyksiin, varastojen välisiin siirtoihin tai tuotantoon. Jos täydennystilauksia on jo tehty, ehdotettuja toimenpiteitä voivat olla tilausten lisääminen tai vauhdittaminen muuttuneen kysynnän mukaisiksi.  

Suunnitteluohjelma perustuu brutto-netto-laskutoimituksiin. Suunnitellut tilausvapautukset perustuvat nettovaatimuksiin, ja ne ajoitetaan reititystietojen (valmistettujen nimikkeiden) perusteella tai nimikkeen kortin toimitusajan (ostonimikkeiden) perusteella. Suunniteltujen tilausvapautusten määrät perustuvat suunnittelulaskentaan, ja tilanvapautuksiin vaikuttavat yksittäisissä nimikkeiden korteissa määritettävät parametrit.  

> [!TIP]
> Suunnittelujärjestelmä perustuu siihen, miten organisaatiosi käyttää sijainteja. Lisätietoja on kohdassa [Suunnittelu sijainneilla tai ilman sijainteja](production-planning-with-without-locations.md).

## <a name="planning-with-manual-transfer-orders"></a><a name="planning-with-manual-transfer-orders"></a>Suunnittelu manuaalisia siirtotilauksia käyttäen.

Kuten Var. yks. -kortin **Täydennysjärjestelmä**-kentässä näkyy, suunnittelujärjestelmän voi määrittää luomaan siirtotilauksia, jotka tasapainottavat eri sijaintien kysyntää ja tarjontaa.  

Automaattisten siirtotilausten lisäksi voit tarvittaessa siirtää varastoeriä sijainnista toiseen myös kysynnästä riippumatta. Luo tällöin siirtotilaus siirrettävällä määrälle manuaalisesti. Voit estää suunnittelujärjestelmää puuttumasta manuaaliseen siirtotilaukseen määrittämällä siirtorivien **Suunnittelun joustavuus** -kentän arvoksi Ei mitään.  

Jos sen sijaan haluat, että suunnittelujärjestelmä muuttaa siirtotilauksen määriä ja päivämääriä kysynnän mukaan, määritä **Suunnittelun joustavuus** -kentän arvoksi oletusarvo Rajaton.

## <a name="planning-parameters"></a><a name="planning-parameters"></a>Suunnittelun parametrit

Suunnittelun parametreilla ohjataan sitä, milloin, miten ja kuinka paljon täydennyksiä nimikkeen kortin asetusten (eli varastointiyksikön) ja tuotannon asetusten perusteella tehdään.  

Nimikkeen tai varastointiyksikön korteissa on käytettävissä seuraavat suunnitteluparametrit:  

- Puskuriaika  
- Puskurimäärä  
- Uusintatilaustapa  
- Uusintatilauspiste
- Enimmäisvarasto  
- Sallittu ylitys  
- Aikaväli  
- Erän koontijakso  
- Uudelleenajoitusjakso  
- Uusintatilausmäärä  
- Toimitusajan varmistus  
- Varmuusvaraston määrä  
- Kokoonpanokäytäntö  
- Tuotantotapa  

Nimikkeen tai varastointiyksikön korteissa on käytettävissä seuraavat tilausmääritteet:  

- Vähimmäistilausmäärä  
- Enimmäistilausmäärä  
- Tilauskerrannainen  

**Tuotannon asetukset** -sivun yleiset suunnitteluasetukset sisältävät seuraavat kohdat:  

- Dynaaminen alatason koodi  
- Nykyinen kysyntäennuste  
- Käytä ennustetta sijainneissa  
- Oletus toimitusajan varmistus  
- Tyhjä ylivuototaso  
- Yhdistetty tuot-ohj/tarvelask.
- Komponentit sijainnissa  
- Oletusvaimentimen jakso  
- Oletuspuskurimäärä  

Lisätietoja on ohjeaiheessa [Rakenteen tiedot: Suunnittelun parametrit](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a><a name="other-important-planning-fields"></a>Muut tärkeät suunnittelukentät

### <a name="planning-flexibility"></a><a name="planning-flexibility"></a>Suunnittelun joustavuus

Voit valita useimpien toimitustilausten, kuten tuotantotilausten, riveillä **Suunnittelun juostavuus** -kentässä **Rajoittaminen** tai **Mitään**.

Näin määritetään, ottaako suunnittelujärjestelmä tuotantotilausrivin osoittaman tarjonnan huomioon toimenpideviestejä laskettaessa.
Jos kentässä on valittu **Rajaton**, suunnittelujärjestelmä sisällyttää rivin laskiessaan toimenpideviestejä. Jos kentässä on valittu **Ei mitään**, rivi on pysyvä, eikä sitä voi muuttaa. Suunnittelujärjestelmä ei sisällytä sitä toimenpideviestien laskentaan.

### <a name="warning"></a><a name="warning"></a>Varoitus

**Suunnittelutyökirja**-sivun **Varoitus**-tietokenttä ilmoittaa poikkeuksellista tilannetta varten luodusta suunnittelurivistä tekstillä, josta käyttäjä voi lukea lisätietoja. Varoitustyyppejä on kolme:

- Hätä
- Poikkeus
- Huomautus
- Hätä

Hätä-varoitus tulee näkyviin kahdessa tilanteessa:

- Varasto on negatiivinen suunnittelun aloituspäivämääränä.
- Nykyhetkeä aikaisempia tarjonta- tai kysyntätapahtumia on olemassa.

Jos nimikkeen varasto on negatiivinen suunnittelun aloituspäivämääränä, suunnittelujärjestelmä ehdottaa negatiiviselle määrälle hätätoimitustilausta, joka saapuu suunnittelun aloituspäivämääränä. Varoitustekstissä kerrotaan aloituspäivämäärä ja hätätilauksen määrä.

Jos asiakirjassa on rivejä, joiden eräpäivä on ennen suunnittelun aloituspäivämäärää, rivit yhdistetään yhdeksi hätätoimitustilaukseksi, jotta nimike saapuisi suunnittelun aloituspäivämääränä.

### <a name="exception"></a><a name="exception"></a>Poikkeus

Poikkeus-varoitus näytetään, jos oletettu saatavilla oleva varasto pienenee varmuusvaraston määrää pienemmäksi.

Suunnittelujärjestelmä ehdottaa toimitustilausta, joka täyttää kysynnän eräpäivänä. Varoitustekstissä kerrotaan nimikkeen varmuusvaraston määrä ja päivämäärä, jolloin se vähenee liian pieneksi.

Varmuusvaraston tason alittaminen aiheuttaa poikkeuksen, koska näin ei pitäisi käydä, jos uusintatilauspiste on määritetty oikein.

> [!NOTE]
> Tarjontaa suunnitteluriveillä, joilla on poikkeusvaroituksia, ei yleensä muokata suunnitteluparametrien mukaan. Suunnittelujärjestelmä ehdottaa sen sijaan vain toimitusmäärää, joka kattaa kysyntämäärän täsmällisesti. Voit kuitenkin määrittää suunnittelun noudattamaan tiettyjä suunnittelurivien suunnitteluparametreja, joihin liittyy tiettyjä varoituksia. Lue lisätietoja **Noudata poikkeusvaroitusten suunnitteluparametreja** -kentästä [Suorita koko suunnittelu, MPS tai MRP](production-how-to-run-mps-and-mrp.md) -artikkelista.

### <a name="attention"></a><a name="attention"></a>Huomautus

Huomautus-varoitus tulee näkyviin kahdessa tilanteessa:

- Suunnittelun aloituspäivämäärä on varhaisempi kuin käsittelypäivämäärä.
- Suunnittelurivi ehdottaa vapautetun osto- tai tuotantotilauksen muuttamista.

> [!NOTE]
> Suunnitteluriveillä, joilla on varoituksia, ei valita **Hyväksy toimenpideviesti** -kenttää, koska suunnitteluohjelman oletetaan tutkivan tarkemmin näitä rivejä ennen suunnitelman toteutusta.

## <a name="planning-worksheets-and-requisition-worksheets"></a><a name="planning-worksheets-and-requisition-worksheets"></a>Suunnittelutyökirjat ja hankintatyökirjat

Kuten [suunnitelmassa](production-planning.md) on kuvattu, voit valita kahdesta taulukosta useimpiin suunnittelutoimintoihin, suunnittelulaskentataulun ja tarvittavan taulukon. Useimmat prosessit kuvataan suunnittelutyötyökirjan perusteella, mutta on olemassa muutamia tilanteita, joissa hankintatyökirjaa suositellaan.

### <a name="requisition-worksheet"></a><a name="requisition-worksheet"></a>Hankintatyökirja

**Hankintatyökirja**-sivu luetteloi nimikkeitä joita haluat tilata. Voit syöttää nimikkeitä työkirjaan seuraavilla tavoilla:

- Syötä nimikkeet työkirjaan manuaalisesti ja täytä liittyvät kentät.

- Käytä **Laske suunnitelma** -eräajoa. Tämä laskee täydennyssuunnitelman nimikkeille ja yksiköille joiden täydennysjärjestelmäksi on asetettu **Osto** tai  **Siirto**. Kun käytät tätä eräajoa ohjelma automaattisesti syöttää **Toimenpideviesti** -kenttään täydennysehdotuksen tälle nimikkeelle. Tämä voisi olla esim. nimikemäärän kasvattamista olemassa olevalle tilaukselle tai uuden tilauksen luominen.

- Jos olet käyttänyt **Laske suunnitelma** -eräajoa **Suunnittelutyökirja**-sivulla laskeaksesi täydennyssuunnitelman, voit käyttää **Toteuta toimenpideviesti** -eräajoa kopioidaksesi osto- ja siirtotilausehdotuksia suunnittelutyökirjasta hankintalistaan. Tämä tulee kyseeseen, jos esimerkiksi tuotantotilauksien ja osto-/siirtotilauksien käsittelijä on eri käyttäjä.

- Voit käyttää **Suoratoimitus** -toimintoa syöttääksesi hankintatyökirjan rivejä. Tämä toiminto käyttää **Hae myyntitilaukset** -eräajoa määrittääkseen myyntitilausrivin jonka haluat määrittää suoratoimitukselle.

- Voit käyttää **Erikoistilaus** -toimintoa syöttääksesi hankintatyökirjan rivejä. Tämä toiminto käyttää **Hae myyntitilaukset** -eräajoa määrittääkseen myyntitilausrivin jonka haluat määrittää erikoistilaukselle.

Hankintatyökirjan rivit sisältävät tietoja nimikkeistä, joita tarvitsee uudelleentilata. Voit muokata ja poistaa rivejä jos haluat muuttaa täydennyssuunnitelmaasi, voit prosessoida rivejä käyttämällä **Toteuta toimenpideviesti** -eräajoa. 

Tietoja suunnittelusta sijaintien ja siirtojen avulla on kohdassa [Suunnitelman luominen sijaintien avulla tai ilman sijainteja](production-planning-with-without-locations.md).

> [!TIP]
> Kun käsittelet **Hankintalista**- tai **Suunnittelutyökirja**-sivuja, voit järjestää rivit lajittelemalla ne sarakkeen nimen mukaan. Tämä on erityisen hyödyllistä Suunnittelutyökirja-sivulla, koska sitä voidaan käyttää usean tason tuotantotilauksissa. Oletusarvoisesti rivit lajitellaan **Nimikenro**-kentän mukaan. Voit ryhmitellä rivit usean tason järjestykseen lajittelemalla **Viitatun tilauksen nro** -kohdan mukaan -kentässä. Myös **Tuotanto-ohjelma tilaus**- ja **Suunnittelun taso** -kenttiä voi käyttää rivien hierarkian näyttämisessä.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/plan-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Katso myös

[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)  
[Suunnittelu](production-planning.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
