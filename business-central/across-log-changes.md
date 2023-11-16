---
title: Muutosten valvonta
description: 'Voit aktivoida käyttäjälokin niin, että saat historiatiedot kaikista seurattujen taulukoiden tietoihin tehdyistä muutoksista. Voit seurata aktiviteetteja myös tietyn tyyppisillä toimintalokeilla.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: null
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 08/03/2023
ms.custom: bap-template
---
# <a name="auditing-changes-in-business-central"></a>Business Centralin tilintarkastuksen muutokset

Monien liikkeenjohtosovellusten yhteisenä haasteena on välttää ei-toivottuja muutoksia tiedoissa. Kyseessä voi olla mikä tahansa väärästä asiakkaan puhelinnumerosta väärään pääkirjanpitokirjaukseen. Tässä ohjeaiheessa kuvataan, miten voidaan selvittää, mitä muutoksia on tehty, kuka sen muutoksen teki ja milloin se tehtiin.

## <a name="about-the-change-log"></a>Muutoslokista

Voit seurata muutoslokiin avulla kaikkia suoria muutoksia, joita käyttäjä tekee tietokannan tietoihin. Jokainen taulukko ja kenttä voidaan haluttaessa määrittää erikseen seurattavaksi, ja sitten loki aktivoidaan. Muutosloki perustuu seuraamiesi taulukoiden tietoihin tehtyihin muutoksiin. **Muutoslokin tapahtumat** -sivulla tapahtumat järjestetään aikajärjestykseen. Sivulla näkyy kaikki muutokset, jotka tehdään määrittämiesi taulukoiden kenttien arvoihin. 

Muutosten seuraaminen voi vaikuttaa suorituskykyyn. Tämä voi viedä enemmän aikaa ja suurentaa tietokannan kokoa, jolloin kustannukset saattavat nousta. Voit pienentää näitä kustannuksia seuraavasti:

- Valitse taulukot ja toiminnot huolellisesti.
- Älä lisää tapahtumia tai kirjattuja asiakirjoja. Sen sijaan priorisoi järjestelmäkenttiä, kuten Luonut ja Luontipäivämäärä.
- Älä käytä Kaikki kentät -seurantatyyppiä. Valitse sen sijaan "Joitakin kenttiä" ja seuraa vain tärkeimpiä kenttiä.

Muutosloki otetaan pois käytöstä, kun [!INCLUDE [prod_short](includes/prod_short.md)] -sovellus päivitetään seuraavaan versioon. Tämä parantaa suorituskykyä. Päivitysprosessin nopeuttamisen lisäksi tämä auttaa pitämään muutoslokin selkeänä. Kun päivitys on valmis, loki alkaa jäljittämään muutoksia uudelleen.

> [!Important]
> Muutokset näkyvät **Muutoslokin tapahtumat** -kohdassa vasta, kun käyttäjän istunto on käynnistetty uudelleen, mikä tapahtuu seuraavasti:
>
> - Istunto vanhentui ja se päivitettiin.
> - Käyttäjä valitsi toisen yrityksen tai roolikeskuksen.
> - Käyttäjä kirjautui ensin ulos ja sitten takaisin sisään.

### <a name="work-with-the-change-log"></a>Muutoslokin käyttäminen

Voit aktivoida muutoslokin ja poistaa sen aktivoinnin **Muutoslokin asetukset** -sivulla. Kun käyttäjä aktivoi muutoslokin tai poistaa sen aktivoinnin, tämä aktiviteetti kirjataan, joten näet aina, kuka käyttäjistä poisti muutoslokin aktivoinnin tai aktivoi sen uudelleen.

Jos valitset **Muutoslokin asetukset** -sivulla **Taulukot**-toiminnon, voit määrittää sekä taulukot, joiden muutoksia seurataan, että seurattavat muutokset. [!INCLUDE[prod_short](includes/prod_short.md)] seuraa myös useita järjestelmätaulukoita.

> [!NOTE]
> Voit valvoa tiettyjä muutoksia koskevia kenttiä, kuten arkaluonteisia tietoja sisältäviä kenttiä, määrittämällä kenttien seurannan. Jos teet niin, redundanssin välttämiseksi kenttää sisältävä taulukko ei ole käytettävissä muutoslokin määrityksessä. Lisätietoja on kohdassa [Herkkien kenttien valvonta](across-log-changes.md#monitor-sensitive-fields).

Kun olet määrittänyt muutoslokin, aktivoinut sen ja muuttanut tietoja, voit tarkastella ja suodattaa muutoksia **Muutoslokin tapahtumat** -sivulla. Jos haluat poistaa tapahtumia, määritä säilytyskäytäntö, jossa voit asettaa suodattimia päivämäärien ja ajan perusteella. Lisätietoja Teamsin säilytyskäytännöistä on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).  

## <a name="about-activity-logs"></a>Tietoja tapahtumalokeista

Joillakin [!INCLUDE [prod_short](includes/prod_short.md)]in sivuilla voi tarkastella toimintalokeja, joissa näkyy [!INCLUDE [prod_short](includes/prod_short.md)]ista vietävien ja sovellukseen tuotavien tiedostojen tila ja mahdolliset virheet.  

### <a name="work-with-activity-logs"></a>Toimintalokien käyttäminen

Tiedot näytetään **Toimintaloki**-sivulla sen kontekstin mukaan, josta ne avataan. Voit esimerkiksi avata sivun **Document Exchange -palvelun asetukset**-, **Saapuva asiakirja**-, **Kirjattu myyntilasku**- ja **Kirjattu myyntihyvityslasku** -sivuilta. Voit tyhjentää lokitapahtumaluettelon tai poistaa vain yli seitsemän päivää vanhemmat tapahtumat.  

## <a name="monitor-sensitive-fields"></a>Valvo herkkiä kenttiä

Luottamuksellisten tietojen suojaaminen ja yksityisyys ovat useimmille yrityksille keskeinen huolenaihe. Jos haluat lisätä suojauskerroksen, voit seurata tärkeitä kenttiä ja saada ilmoituksen sähköpostilla, kun joku muuttaa arvoa. Saatat esimerkiksi haluta saada ilmoituksen, jos joku muuttaa yrityksesi IBAN-numeroa.

> [!NOTE]
> Ilmoitusten lähettäminen sähköpostitse edellyttää, että määrität sähköpostiominaisuuden [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmaan. Lisätietoja on kohdassa [Sähköpostin määrittäminen](admin-how-setup-email.md).

### <a name="set-up-field-monitoring"></a>Määritä kentän seuranta

**Kentän valvonnan asetusten määrittäminen** -avustetun asennusoppaan avulla kentät, joita haluat seurata suodatusehtojen, kuten kenttien tietojen arkaluonteisuusluokituksen perusteella. Lisätietoja on kohdassa [Tietojen arkaluontoisuuden luokitteleminen](admin-classifying-data-sensitivity.md). Oppaassa voidaan myös määrittää henkilö, joka saa sähköposti-ilmoituksen muutoksen tapahtuessa, sekä sähköpostitili, jolla ilmoitus lähetetään. Määritä sekä käyttäjä, jolle ilmoitetaan että tili, josta ilmoitus lähetetään. Kun ohjelma on valmis, voit hallita kentän seurannan asetuksia **Kentän seuranta-asetukset** -sivulla. 

> [!NOTE]
> Kun määrität sähköpostitilin, josta ilmoitukset lähetetään, sinun on lisättävä joko **Microsoft 365**- tai **SMTP**-tilityyppi. Ilmoitukset tulee lähettää tililtä, jota ei ole liitetty todelliseen käyttäjään. Tämän vuoksi et voi valita **Nykyinen käyttäjä** -tilityyppiä. Jos teet näin, ilmoituksia ei lähetetä. 

**Tarkkailtavien kenttien lokitapahtumat** -sivun tapahtumaluettelo kasvaa ajan mittaan. Voit vähentää merkintöjen määrää luomalla säilytyskäytännön, joka poistaa tapahtumat tietyn ajanjakson jälkeen. Lisätietoja on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).

Kun määrität kentän seurannan tai muutat asetuksia, tapahtumat luodaan muutoksesi. Voit määrittää, näytetäänkö seurannan asetuksiin liittyvät tapahtumat näyttämällä vai piilottamalla ne. 

Voit hallita kentän seurannan asetuksia, kuten sen, lähetetäänkö sähköposti-ilmoitus vai merkitäänkö vain lokiin muutos, kunkin **Tarkkailtavat kentät -työkirja** -sivun kentän osalta. Sivulla voit myös lisätä tai poistaa valvottuja kenttiä.

> [!NOTE]
> Kun olet lisännyt yhden tai useamman kentän ja käynnistät seurannan, sinun on kirjauduttava ulos [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmasta ja kirjautua uudelleen sisään, jotta voit ottaa asetukset käyttöön.

### <a name="work-with-field-monitoring"></a>Kentän seurannan käsitteleminen

Tarkkailtujen kenttien kaikkien muutettujen arvojen tapahtumat ovat käytettävissä **Tarkkailtavat kentät-lokin tapahtumat** -sivulla. Merkinnät sisältävät esimerkiksi seuraavat tiedot:

- Kenttä, jonka arvoa on muutettu.
- Alkuperäiset ja uudet arvot.
- Kuka teki muutoksen ja milloin.

Jos haluat tutkia muutosta edelleen, valitse arvo, joka avaa sivun, jossa se on tehty. Voit tarkastella kaikkien tapahtumien luetteloa valitsemalla **Kentän muutostapahtumat**.

### <a name="view-field-monitoring-telemetry"></a>Kentän seurannan telemetrian tarkastelu

Voit määrittää [!INCLUDE[prod_short](includes/prod_short.md)]in lähettämään kentän seurannan aktiviteetit Application Insights -resurssille Microsoft Azuressa. Sitteen Azure Monitorin avulla luot raportteja ja määrität hälytyksiä kerätyille tiedoille. Lisätietoja on [!INCLUDE[prod_short](includes/prod_short.md)]in kehittäjien ja IT-ammattilaisten ohjeen seuraavissa artikkeleissa:

- [Telemetrian seuranta ja analysointi – Application Insightsin käyttöönotto](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Kentän seurannan telemetrian analysointi](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## <a name="define-retention-policies"></a>Määritä säilytyskäytännöt

Voit luoda säilytyskäytäntöjä, jotka poistavat tarpeettomia tietoja lokeista määrittämäsi ajanjakson jälkeen. Esimerkiksi ajan mittaan lokimerkintöjen määrä voi kasvaa. Puhdistamalla vanhoja tapahtumia voit helpottaa keskittymistä viimeaikaisiin ja todennäköisesti osuvimpiin tapahtumiin. Lisätietoja Teamsin säilytyskäytännöistä on kohdassa [Säilytyskäytäntöjen määrittäminen](admin-data-retention-policies.md).

## <a name="see-also"></a>Katso myös

[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Lajitteleminen, hakeminen ja suodattaminen](ui-enter-criteria-filters.md)  
[Sivujen ja tietojen etsiminen Kerro, mitä haluat tehdä -toiminnolla](ui-search.md)  
[Käyttöoikeuksien delegoiminen käyttäjille ja ryhmille](ui-define-granular-permissions.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Määritä säilytyskäytännöt](admin-data-retention-policies.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
