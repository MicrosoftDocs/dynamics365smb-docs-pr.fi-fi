---
title: Muutosten valvonta
description: 'Voit aktivoida käyttäjälokin niin, että saat historiatiedot kaikista seurattujen taulukoiden tietoihin tehdyistä muutoksista. Voit seurata aktiviteetteja myös tietyn tyyppisillä toimintalokeilla.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Muutosten valvonta

Monien liikkeenjohtosovellusten yhteisenä haasteena on välttää ei-toivottuja muutoksia tiedoissa. Kyseessä voi olla mikä tahansa väärästä asiakkaan puhelinnumerosta väärään pääkirjanpitokirjaukseen. Tässä artikkelissa kuvataan, miten voidaan selvittää, mitä muutoksia on tehty, kuka sen muutoksen teki ja milloin se tehtiin.

## Muutoslokista

Voit seurata muutoslokiin avulla kaikkia suoria muutoksia, joita käyttäjä tekee tietokannan tietoihin. Jokainen taulukko ja kenttä voidaan haluttaessa määrittää erikseen seurattavaksi, ja sitten loki aktivoidaan. Muutosloki perustuu seuraamiesi taulukoiden tietoihin tehtyihin muutoksiin. **Muutoslokin tapahtumat** -sivulla tapahtumat järjestetään aikajärjestykseen. Sivulla näkyy kaikki muutokset, jotka tehdään määrittämiesi taulukoiden kenttien arvoihin.

Muutosten seuraaminen voi vaikuttaa suorituskykyyn. Tämä voi viedä enemmän aikaa ja suurentaa tietokannan kokoa, jolloin kustannukset saattavat nousta. Voit pienentää näitä kustannuksia seuraavilla tavoilla:

- Valitse taulukot ja toiminnot huolellisesti.
- Älä lisää tapahtumia tai kirjattuja asiakirjoja. Sen sijaan priorisoi järjestelmäkenttiä, kuten Luonut ja Luontipäivämäärä.
- Älä käytä **Kaikki kentät** -seurantatyyppiä. Valitse sen sijaan **Joitakin kenttiä** ja seuraa vain tärkeimpiä kenttiä.

> [!NOTE]
> Muutosloki ei seuraa muutoksia sellaisten kenttien osalta, joissa käytetään `autoIncrement property` -ominaisuutta. Ominaisuutta käyttävä kenttä on esimerkki Virhesanomat- ja ALV-raporttirivi-taulukoiden Kokonaisluku-kentästä.

Muutosloki otetaan pois käytöstä, kun [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus päivitetään seuraavaan versioon. Tämä parantaa suorituskykyä. Päivitysprosessin nopeuttamisen lisäksi lokien poistaminen käytöstä auttaa pitämään muutoslokin selkeänä. Kun päivitys on valmis, loki alkaa jäljittämään muutoksia uudelleen.

> [!Important]
> Muutokset näkyvät **Muutoslokin tapahtumat** -kohdassa vasta, kun käyttäjän istunto on käynnistetty uudelleen, mikä tapahtuu seuraavasti:
>
> - Istunto vanhentui ja se päivitettiin.
> - Käyttäjä valitsi toisen yrityksen tai roolikeskuksen.
> - Käyttäjä kirjautui ensin ulos ja sitten takaisin sisään.

## Muutoslokin määrittäminen

**Muutoslokin asetukset** -sivulla voit ottaa muutoslokin käyttöön tai poistaa sen käytöstä. Kun teet näin, aktiviteetti kirjataan lokiin, joten voit aina nähdä, kuka muutoksen teki.

Jos valitset **Muutoslokin asetukset** -sivulla **Taulukot**-toiminnon, voit määrittää sekä taulukot, joiden muutoksia seurataan, että seurattavat muutokset. [!INCLUDE[prod_short](includes/prod_short.md)] seuraa myös useita järjestelmätaulukoita.

> [!NOTE]
> Voit valvoa tiettyjä muutoksia koskevia kenttiä, kuten arkaluonteisia tietoja sisältäviä kenttiä, määrittämällä kenttien seurannan. Jos teet niin, redundanssin välttämiseksi kenttää sisältävä taulukko ei ole käytettävissä muutoslokin määrityksessä. Lisätietoja on kohdassa [Herkkien kenttien valvonta](across-log-changes.md#monitor-sensitive-fields).

Kun olet määrittänyt muutoslokin, aktivoinut sen ja muuttanut tietoja, voit tarkastella ja suodattaa muutoksia **Muutoslokin tapahtumat** -sivulla. Jos haluat poistaa tapahtumia, määritä säilytyskäytäntö, jossa voit asettaa suodattimia päivämäärien ja ajan perusteella. Lisätietoja Teamsin säilytyskäytännöistä on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).  

## Tietojen analysointi muutoslokissa

**Tietojen analysointi** -toiminnon avulla voit analysoida muutoslokin tietoja [Muutoslokin tapahtumat](https://businesscentral.dynamics.com/?page=595) -sivulta. Sinun ei tarvitse suorittaa raporttia tai avata toista sovellusta, kuten Exceliä. Ominaisuus tarjoaa vuorovaikutteisen ja monipuolisen tavan laskea, tiivistää ja tarkastella tietoja. Sen sijaan, että raportteja suoritetaan vaihtoehdoilla ja suodattimilla, voit lisätä useita välilehtiä, jotka edustavat erilaisia tehtäviä tai näkymiä tiedoista. Joitakin esimerkkejä ovat "Kuka muutti mitäkin tietoa ja milloin" tai "Tieto muuttuu taulukon/kentän mukaan" tai mikä tahansa muu näkymä, jonka voit kuvitella. Lisätietoja **Tietojen analysointi** -ominaisuuden käytöstä on kohdassa [analyysitilassa olevien luettelo- ja kyselytietojen analysointi](analysis-mode.md).

### Muutoslokin ad-hoc-analyysiskenaariot

Seuraavissa osissa on esimerkkejä skenaarioista, joissa muutoslokin analysoiminen voi helpottaa muutosten seurantaa ja tarkastamista.

| Alue | Vastaanottaja... | Avaa tämä sivu analyysitilassa | Näiden kenttien käyttäminen |
| ---- | ----- | ------------------------------- |------------------- |
| [Kuka muutti mitä tietoja ja milloin](#example-who-changed-what-data-and-when) | Katso kuka muutti mitä tietoja. | [Muutoslokin tapahtumat](https://businesscentral.dynamics.com/?page=595) | **Käyttäjätunnus**, **Pvm ja aika**, **Taulukon otsikko**, **Kentän otsikko**, **Perusavainarvo 2**, **Perusavainarvo 3**, **Muutoksen tyyppi**, **Vanha arvo** ja **Uusi arvo**. |
| [Tietojen muutokset taulukon/kentän mukaan](#example-data-changes-by-tablefield) | Tietojen muutosten katsominen taulukon/kentän mukaan, sekä muutoksen tekijä. | [Muutoslokin tapahtumat](https://businesscentral.dynamics.com/?page=595) | **Taulukon otsikko**, **Kentän otsikko**, **Käyttäjätunnus**, **Pvm ja aika**, **Perusavainarvo 2**, **Perusavainarvo 3**, **Muutoksen tyyppi**, **Vanha arvo** ja **Uusi arvo**. |

### Esimerkki: Kuka muutti mitä tietoja ja milloin

Kun haluat analysoida, Kuka muutti mitä tietoja milloin, noudata seuraavia vaiheita:

1. Avaa [Muutoslokien merkinnät](https://businesscentral.dynamics.com/?page=595) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: -kuvake ja ota analyysitila käyttöön.
1. Poista kaikki sarakkeet **Sarakkeet**-valikosta (valitse **Haku**-kentän vieressä oleva ruutu oikealla).
1. Vedä **Käyttäjätunnus**-kenttä (kuka sen teki) **Riviryhmät**-alueeseen.
1. Valitsee nyt seuraavat kentät:
   - Jos haluat näyttää, milloin se tapahtui, valitse **Pvm ja Aika**.
   - Jos haluat näyttää taulukon, jossa se tapahtui, valitse **Taulukon otsikko**. 
   - Jos haluat näyttää, mikä kenttä, valitse **Kentän otsikko**.
   - Voit näyttää kentän koodin valitsemalla **Perusavainarvo 2**. 
   - Voit näyttää yrityksen nimen valitsemalla **Perusavainarvo 3**.
   - Jos haluat näyttää, oliko muutos lisäys-, päivitys- vai poistotoiminto, valitse **Muutoksen tyyppi**.
   - Näytä muutos valitsemalla **Vanha arvo** ja **Uusi arvo**.
1. Nimeä analyysivälilehden nimeksi uudelleen **Kuka muutti mitä tietoja milloin** tai tuotteiksi, jotka kuvaavat analyysiä.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source=" media/data-analysis-change-log-entries-Who-changed-What-data-When.png" alt-text="Esimerkki tietoanalyysin tekemisestä Muutoslokin tapahtumat -sivulla (Kuka muutti mitä tietoja milloin) -sivulla." lightbox="media/data-analysis-change-log-entries-Who-changed-What-data-When.png":::

### Esimerkki: tietojen muutokset taulukon/kentän mukaan

Voit analysoida tietojen muutoksia taulukon/kentän mukaan noudattamalla seuraavia vaiheita:

1. Avaa [Muutoslokien merkinnät](https://businesscentral.dynamics.com/?page=595) -luettelosivu ja valitse :::image type="content" source="media/analysis-mode-icon.png" alt-text="Siirry analyysitilaan."::: -kuvake ja ota analyysitila käyttöön.
1. Poista kaikki sarakkeet **Sarakkeet**-valikosta (valitse **Haku**-kentän vieressä oleva ruutu oikealla).
1. Vedä **Taulukon otsikko** (missä taulukossa)- ja **Kentän otsikko** (missä kentässä) -kentät **Riviryhmät** -alueeseen.
1. Valitsee nyt seuraavat kentät:
   - Jos haluat näyttää, milloin se tapahtui, valitse **Pvm ja Aika**
   - Jos haluat näyttää, kuka muutoksen teki, valitse **Käyttäjätunnus**.
   - Voit näyttää kentän koodin valitsemalla **Perusavainarvo 2**.
   - Voit näyttää yrityksen nimen valitsemalla **Perusavainarvo 3** (yleensä yrityksen nimi), 
   - Jos haluat näyttää, oliko muutos lisäys-, päivitys- vai poistotoiminto, valitse **Muutoksen tyyppi**.
   - Näytä muutos valitsemalla **Vanha arvo** ja **Uusi arvo**.
1. Nimeä analyysivälilehden nimeksi uudelleen **Tietojen muutokset taulukon + kentän mukaan** tai tuotteiksi, jotka kuvaavat analyysiä.

Seuraavassa kuvassa on näiden työvaiheiden tulokset.

:::image type="content" source=" media/data-analysis-change-log-entries-data-changes-by-table-field.png" alt-text="Esimerkki tietoanalyysin tekemisestä Muutoslokin tapahtumat -sivulla (tietojen muutokset taulukon/kentän mukaan) -sivulla." lightbox="media/data-analysis-change-log-entries-data-changes-by-table-field.png":::

## Tietoja tapahtumalokeista

Joillakin [!INCLUDE [prod_short](includes/prod_short.md)]in sivuilla voi tarkastella toimintalokeja, joissa näkyy [!INCLUDE [prod_short](includes/prod_short.md)]ista vietävien ja sovellukseen tuotavien tiedostojen tila ja mahdolliset virheet.  

### Toimintalokien käyttäminen

Tiedot näytetään **Toimintaloki**-sivulla sen kontekstin mukaan, josta avasit ne. Voit esimerkiksi avata sivun **Document Exchange -palvelun asetukset**-, **Saapuva asiakirja**-, **Kirjattu myyntilasku**- ja **Kirjattu myyntihyvityslasku** -sivuilta. Voit tyhjentää lokitapahtumaluettelon tai poistaa vain yli seitsemän päivää vanhemmat tapahtumat.  

## Valvo herkkiä kenttiä

Luottamuksellisten tietojen suojaaminen ja yksityisyys ovat useimmille yrityksille keskeinen huolenaihe. Jos haluat lisätä suojauskerroksen, voit seurata tärkeitä kenttiä ja saada sähköpostiviestin, kun joku muuttaa arvoa. Saatat esimerkiksi haluta saada ilmoituksen, jos joku muuttaa yrityksesi IBAN-numeroa.

> [!NOTE]
> Ilmoitusten lähettäminen sähköpostitse edellyttää, että määrität sähköpostiominaisuuden [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

### Määritä kentän seuranta

**Kentän valvonnan asetusten määrittäminen** -avustetun asennusoppaan avulla kentät, joita haluat seurata suodatusehtojen, kuten kenttien tietojen arkaluonteisuusluokituksen perusteella. Lisätietoja on kohdassa [Tietojen arkaluontoisuuden luokitteleminen](admin-classifying-data-sensitivity.md). Oppaassa voidaan myös määrittää henkilö, joka saa sähköposti-ilmoituksen muutoksen tapahtuessa, sekä sähköpostitili, jolla ilmoitus lähetetään. Määritä sekä käyttäjä, jolle ilmoitetaan että tili, josta ilmoitus lähetetään. Kun ohjelma on valmis, voit hallita kentän seurannan asetuksia **Kentän seuranta-asetukset** -sivulla.

> [!NOTE]
> Kun määrität sähköpostitilin, josta ilmoitukset lähetetään, sinun on lisättävä joko **Microsoft 365**- tai **SMTP**-tilityyppi. Ilmoitukset tulee lähettää tililtä, jota ei ole liitetty todelliseen käyttäjään. Tämän vuoksi et voi valita **Nykyinen käyttäjä** -tilityyppiä. Jos teet näin, ilmoituksia ei lähetetä.

**Tarkkailtavien kenttien lokitapahtumat** -sivun tapahtumaluettelo kasvaa ajan mittaan. Voit vähentää merkintöjen määrää luomalla säilytyskäytännön, joka poistaa tapahtumat tietyn ajanjakson jälkeen. Lisätietoja on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).

Kun määrität kentän seurannan tai muutat asetuksia, tapahtumat luodaan muutoksesi. Voit määrittää, näytetäänkö seurannan asetuksiin liittyvät tapahtumat näyttämällä vai piilottamalla ne.

Voit hallita kentän seurannan asetuksia, kuten sen, lähetetäänkö sähköposti-ilmoitus vai merkitäänkö vain lokiin muutos, kunkin **Tarkkailtavat kentät -työkirja** -sivun kentän osalta. Sivulla voit myös lisätä tai poistaa valvottuja kenttiä.

> [!NOTE]
> Kun olet lisännyt yhden tai useamman kentän ja käynnistät seurannan, sinun on kirjauduttava ulos [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta ja kirjautua uudelleen sisään, jotta voit ottaa asetukset käyttöön.

### Kentän seurannan käsitteleminen

Tarkkailtujen kenttien kaikkien muutettujen arvojen tapahtumat ovat käytettävissä **Tarkkailtavat kentät-lokin tapahtumat** -sivulla. Merkinnät sisältävät esimerkiksi seuraavat tiedot:

- Kenttä, jossa arvoa on muutettiin.
- Alkuperäiset ja uudet arvot.
- Kuka teki muutoksen ja milloin.

Jos haluat tutkia muutosta edelleen, valitse arvo, joka avaa sivun, jossa se on tehty. Voit tarkastella kaikkien tapahtumien luetteloa valitsemalla **Kentän muutostapahtumat**.

### Kentän seurannan telemetrian tarkastelu

Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in lähettämään kentän seurannan aktiviteetit Application Insights -resurssille Microsoft Azuressa. Sitteen Azure Monitorin avulla luot raportteja ja määrität hälytyksiä kerätyille tiedoille. Lisätietoja on [!INCLUDE[prod_short](includes/prod_short.md)]in kehittäjien ja IT-ammattilaisten ohjeen seuraavissa artikkeleissa:

- [Telemetrian seuranta ja analysointi – Application Insightsin käyttöönotto](/dynamics365/business-central/dev-itpro/administration/telemetry-overview?toc=/dynamics365/business-central/toc.json#enable)
- [Kentän seurannan telemetrian analysointi](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)

## Määritä säilytyskäytännöt

Voit luoda säilytyskäytäntöjä, jotka poistavat tarpeettomia tietoja lokeista määrittämäsi ajanjakson jälkeen. Esimerkiksi ajan mittaan lokimerkintöjen määrä voi kasvaa. Puhdistamalla vanhoja tapahtumia voit helpottaa keskittymistä viimeaikaisiin ja todennäköisesti osuvimpiin tapahtumiin. Lisätietoja Teamsin säilytyskäytännöistä on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).

## Katso myös

[Valvo herkkiä kenttiä](across-log-changes.md#monitor-sensitive-fields)  
[Kentän seurannan telemetrian analysointi](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)  
[Määritä säilytyskäytännöt](admin-data-retention-policies.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Käyttöoikeuksien delegoiminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
